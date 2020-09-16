---
description: Политика безопасности контента для расширений EDGE (Chromium).
title: Политика безопасности контента (CSP)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, Разработка расширений, расширения браузера, надстройки, центр партнера, разработчик
ms.openlocfilehash: f3769639465d048c42ad0705f74598fbd1db8a20
ms.sourcegitcommit: d360e419b5f96f4f691cf7330b0d8dff9126f82e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015718"
---
# Политика безопасности контента \ (CSP \)  

Чтобы уменьшить класс потенциальных проблем с межсайтовыми сценариями, в системе расширений Microsoft Edge включена общая концепция [политики безопасности контента \ (CSP)][W3CContentSecurityPolicy].  В этом разделе представлены довольно строгие политики, которые делают расширения более безопасными по умолчанию и предоставляют возможность создавать и применять правила, регулирующие типы содержимого, которое может быть загружено и запущено вашими расширениями и приложениями.  

Как правило, CSP работает как блок/allowlistingный механизм для ресурсов, загруженных или выполняемых вашими расширениями.  Определение разумной политики для вашего расширения позволяет внимательно рассмотреть ресурсы, необходимые для расширения, и попросить браузера убедиться, что это единственные ресурсы, к которым у вашего расширения есть доступ.  Эти политики обеспечивают безопасность, а также над разрешениями узла ваши запросы на расширение; они являются дополнительным уровнем защиты, а не заменой.  

В Интернете такая политика определяется с помощью заголовка или `meta` элемента HTTP.  В системе расширений Microsoft Edge ни один из них не является подходящим механизмом.  Вместо этого политика расширения определяется с помощью `manifest.json` файла расширения следующим образом:  

```javascript
{
    ...,
    "content_security_policy": "[POLICY STRING GOES HERE]"
    ...
}
```  

> Для получения подробных сведений о синтаксисе CSP ознакомьтесь со [спецификацией политики безопасности содержимого][W3CContentSecurityPolicy] и статьей ["Общие сведения о политике безопасности контента"][HTML5RocksIntroductionContentSecurityPolicy] на HTML5Rocks.  

## Ограничения политики по умолчанию  

Пакеты, для которых не определена `manifest_version` Политика безопасности контента по умолчанию.  Для тех, кто выберет `manifest_version` 2, есть стандартная политика безопасности содержимого:  

```javascript
script-src 'self'; object-src 'self'
```  

Эта политика обеспечивает безопасность путем ограничения расширений и приложений тремя способами:  

**Eval и связанные функции отключены**  

Следующие программы не работают.  

```javascript
alert(eval("foo.bar.baz"));
window.setTimeout("alert('hi')", 10);
window.setInterval("alert('hi')", 10);
new Function("return foo.bar.baz");
```  

Вычисление строк JavaScript так же, как и в случае, — это распространенный вектор атаки XSS.  Вместо этого необходимо написать следующий код:

```javascript
alert(foo && foo.bar && foo.bar.baz);
window.setTimeout(function() { alert('hi'); }, 10);
window.setInterval(function() { alert('hi'); }, 10);
function() { return foo && foo.bar && foo.bar.baz };
```  

**Встроенные сценарии JavaScript не выполняются**  

Встроенные сценарии JavaScript не выполняются.  Это ограничение BANS как встроенные `<script>` блоки, так и встроенные обработчики событий, такие как `<button onclick="...">` .

Первое ограничение — это очистка огромного класса межсайтовых атак с помощью сценариев, что делает невозможным случайный запуск сценария, предоставленного вредоносным сторонним лицом.  Тем не менее, в этом случае необходимо написать код с четким разделением между содержимым и поведением (что нужно делать, если вы хотите, чтобы все это правильно, верно? \).  Например, это можно сделать более четким.  Вы можете попытаться создать всплывающее действие браузера в виде одного `pop-up.html` содержащего:  

```html
<!doctype html>
<html>
    <head>
        <title>My Awesome Pop-up!</title>
        <script>
            function awesome() {
                // do something awesome!
            }
            
            function totallyAwesome() {
                // do something TOTALLY awesome!
            }
            
            function clickHandler(element) {
                setTimeout("awesome(); totallyAwesome()", 1000);
            }
            
            function main() {
                // Initialization work goes here.
            }
        </script>
    </head>
    <body onload="main();">
        <button onclick="clickHandler(this)">
            Click for awesomeness!
        </button>
    </body>
</html>
```  

Необходимо изменить три действия, чтобы сделать эту работу нужной, чтобы она выглядела так, как вы ожидаете.  

*   `clickHandler`Определение должно быть перемещено во внешний файл JavaScript \ ( `popup.js` может быть хорошим целевым).  
*   Определение обработчика встроенных событий должно быть переписано в отношении `addEventListener` и извлечено `popup.js` .  
    Если вы запускаете программу с помощью такого кода `<body onload="main();">` , замените ее на `DOMContentLoaded` событие в документе или `load` событие в окне (в зависимости от ваших требований).  Используйте бывший, так как он обычно инициируется быстрее.  

*   `setTimeout`Необходимо переписать вызов, чтобы избежать преобразования строки `"awesome(); totallyAwesome()"` в JavaScript для выполнения.  
    Эти изменения могут выглядеть примерно так, как показано ниже.  

```javascript
function awesome() {
    // Do something awesome!
}

function totallyAwesome() {
    // do something TOTALLY awesome!
}

function awesomeTask() {
    awesome();
    totallyAwesome();
}

function clickHandler(e) {
    setTimeout(awesomeTask, 1000);
}

function main() {
    // Initialization work goes here.
}

// Add event listeners once the DOM has fully loaded by listening for the
// `DOMContentLoaded` event on the document, and adding your listeners to
// specific elements when it triggers.
document.addEventListener('DOMContentLoaded', function () {
    document.querySelector('button').addEventListener('click', clickHandler);
    main();
});
```  

```html
<!doctype html>
<html>
    <head>
        <title>My Awesome Pop-up!</title>
        <script src="popup.js"></script>
    </head>
    <body>
        <button>Click for awesomeness!</button>
    </body>
</html>
```  

**Загружаются только локальный сценарий и ресурсы объектов.**  

Ресурсы сценариев и объектов можно загружать только из пакета расширения, но не из веб-сайта.  Это гарантирует, что ваше расширение будет выполнять только код, который вы только что утвердили, и не позволяя вредоносному сетевому злоумышленнику перенаправлять запрос на ресурс.  

Вместо того чтобы писать код, зависящий от библиотеки, загружаемой из внешней сети CDN, рассматривайте в пакете расширения определенную версию jQuery.  Это значит, что вместо:  

```html
<!doctype html>
<html>
    <head>
        <title>My Awesome Pop-up!</title>
        <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.7.1/jquery.min.js"></script>
    </head>
    <body>
        <button>Click for awesomeness!</button>
    </body>
</html>
```  

Скачайте файл, включите его в пакет и напишите следующее:  

```html
<!doctype html>
<html>
    <head>
        <title>My Awesome Pop-up!</title>
        <script src="jquery.min.js"></script>
    </head>
    <body>
        <button>Click for awesomeness!</button>
    </body>
</html>
```  

## Применяйте политику по умолчанию  

**Встроенный сценарий**  

<!-- Up until Chrome 45, there was no mechanism for relaxing the restriction against running inline JavaScript.  In particular, setting a script policy that includes `'unsafe-inline'` has no effect.  

As of Chrome 46, -->  

Встроенные скрипты можно разрешить, указав хэш-код в исходном коде в политике в формате Base64.  Этот хэш-код должен быть префиксом используемого хэш-алгоритма \ (SHA256, SHA384 или SHA512 \).  В качестве примера для элементов в этом примере следует ознакомиться с [использованием хеша \<script\> ][W3CContentSecurityPolicyLevel2ScriptSrcHashUsage] .  

**Удаленный сценарий**  

Если вам нужны внешние ресурсы JavaScript или объект, вы можете ослабить политику в ограниченном масштабе, allowlisting безопасные источники, из которых следует принимать сценарии.  Убедитесь, что ресурсы среды выполнения, загруженные с повышенными разрешениями расширения, представляют собой именно те ресурсы, которые вы ожидаете, и не заменяются активным злоумышленником сети.  Поскольку [атака "злоумышленник из-за середины"][WikiManMiddleAttacks] является тривиальной и необнаруживаемой по протоколу HTTP, эти источники не принимаются.  

В настоящее время разработчики могут доменов источники со следующими схемами:,, `blob` `filesystem` `https` и `extension` .  Для схем должны быть явно указаны ведущие части источника `https` `extension` .  Универсальные подстановочные знаки, такие как HTTPS: `https://*` и `https://*.com` не разрешены; подстановочные знаки поддомены, такие как `https://*.example.com` разрешены.  Домены в [списке общедоступных суффиксов][PublicSuffixList] также просматриваются как общие домены верхнего уровня.  Чтобы загрузить ресурс из этих доменов, поддомены должны быть явно указаны в списке.  Например, `https://*.cloudfront.net` является недопустимым, но `https://XXXX.cloudfront.net` и `https://*.XXXX.cloudfront.net` может быть allowlisted.  

Для упрощения разработки ресурсы, загруженные через HTTP с серверов на локальном компьютере, могут быть allowlisted.  Вы можете доменов сценарии и источники объектов на любом порту либо `http://127.0.0.1` или `http://localhost` .  

> [!NOTE]
> Ограничение для ресурсов, загруженных по протоколу HTTP, применяется только к тем ресурсам, которые выполняются напрямую.  Вы по-прежнему свободны, например, чтобы создавать соединения XMLHTTPRequest для любого источника, который вам нравится; политика по умолчанию не ограничивает `connect-src` или никакие другие директивы CSP каким бы то ни было.  

Неявное определение политики, позволяющее загружать ресурсы сценария из example.com по HTTPS, может выглядеть так:  

```javascript
"content_security_policy": "script-src 'self' https://example.com; object-src 'self'"
```  

> [!NOTE]
> Оба `script-src` и `object-src` определяются политикой.  Microsoft EDGE не допускает политику, которая не ограничивает каждый из этих значений на \ (не менее \) " `self` .  

<!-- Making use of Google Analytics is the canonical example for this sort of policy definition.  It is common enough that an Analytics boilerplate of sorts is provided in the Event Tracking with Google Analytics sample Extension, and a brief tutorial that goes into more detail.  -->  

**Оцененный JavaScript**  

Политику и `eval()` связанные с ней функции, такие как `setTimeout(String)` и, `setInterval(String)` и `new Function(String)` они могут быть ослаблены путем добавления `unsafe-eval` к политике.  

```javascript
"content_security_policy": "script-src 'self' 'unsafe-eval'; object-src 'self'"
```  

Тем не менее, мы настоятельно рекомендуем сделать это.  Эти функции являются глобальными векторами атак XSS.  

## Усиление политики по умолчанию  

Разумеется, вы, конечно же, заследуете эту политику в отношении того, какое расширение позволит вам повысить безопасность за счет удобства.  Чтобы указать, что расширение может загружать только ресурсы любого типа \ (изображения и т. д.) из связанного пакета расширения, например, `default-src 'self'` может быть уместным.  

<!-- The Mappy sample Extension is a good example of an Extension that is been locked down above and beyond the defaults.  -->  

## Сценарии содержимого  

Обсуждаемая политика применяется к фоновым страницам и страницам событий расширения.  Применение сценариев содержимого к скриптам содержимого в расширении более сложно.  

Как правило, в скриптах содержимого не распространяется расширение CSP.  Так как сценарии содержимого не являются HTML, основным эффектом является то, что они могут использоваться `eval` даже в том случае, если не указан CSP расширения `unsafe-eval` , но это не рекомендуется.  Кроме того, CSP страницы не применяется к скриптам содержимого.  Более сложная программа — это `<script>` теги, с помощью которых сценарии содержимого создают и помещаются в модель DOM той страницы, на которой они запущены.  На эти ссылки указываются сценарии внедрения, пересылаемые в модели DOM.  

Вставленные сценарии модели, которые выполняются сразу после введения на страницу.  Представьте сценарий содержимого с помощью следующего кода как простой пример:  

```javascript
document.write("<script>alert(1);</script>");
 ```  

Этот сценарий содержимого вызывает `alert` немедленное выполнение `document.write()` .  Обратите внимание на то, что это действие выполняется независимо от политики, которая может быть указана на странице.
Тем не менее, в этом случае все сложнее в рамках вставленного сценария DOM и для любого сценария, который не запускается сразу после вставки.  Представьте, что ваше расширение запущено на странице, предоставляющей соответствующий CSP, который указывает `script-src 'self'` .  Теперь представьте, что сценарий содержимого запускает следующий код:  

```javascript
document.write("<button onclick='alert(1);'>click me</button>'");
```  

Если пользователь нажмет на эту кнопку, `onclick` сценарий не запускается.  Это связано с тем, что сценарий не был немедленно запущен, а код не интерпретируется, пока событие нажатия не будет рассматриваться как часть скрипта содержимого, поэтому CSP на странице \ (не расширение \) ограничил поведение.  А так как этот CSP не указан `unsafe-inline` , обработчик встроенных событий блокируется.  
Правильный способ реализации нужного поведения в этом случае может быть `onclick` следующим: добавьте обработчик как функцию из сценария содержимого, как описано ниже.  

```javascript
document.write("<button id='mybutton'>click me</button>'");
var button = document.getElementById('mybutton');
button.onclick = function() {
      alert(1);
};
```  

Если сценарий содержимого выполняет указанные ниже действия, возникает другая подобная ошибка.  

```javascript
var script = document.createElement('script');
script.innerHTML = 'alert(1);'
document.getElementById('body').appendChild(script);
```  

В этом случае запускается сценарий, и отображается оповещение.  Тем не менее, сделайте следующее:  

```javascript
var script = document.createElement('script');
script.innerHTML = 'eval("alert(1);")';
=document.getElementById('body').appendChild(script);
```  

При запуске исходного сценария Звонок `eval` блокируется.  Таким образом, если исходная среда выполнения сценария разрешена, поведение в сценарии регулируется CSP страницы.  
Таким образом, в зависимости от того, как вы пишете внедренные сценарии DOM в расширении, изменения в CSP страницы могут повлиять на работу вашего расширения.  Так как на сценарии контента не влияет поставщик служб (CSP) страницы, это может быть вызвано тем, что это может повлиять на расширение в сценарий содержимого, а не на добавленные в DOM сценарии.  

<!-- image links -->  

<!-- links -->  

[HTML5RocksIntroductionContentSecurityPolicy]: https://www.html5rocks.com/en/tutorials/security/content-security-policy "Общие сведения о политике безопасности содержимого — HTML5 Rocks"  
[PublicSuffixList]: https://publicsuffix.org/list "ПРОСМОТР СПИСКА ОТКРЫТЫХ СУФФИКСОВ"  
[W3CContentSecurityPolicyLevel2ScriptSrcHashUsage]: https://www.w3.org/TR/CSP2#script-src-hash-usage "Использование хэша для <сценарий \ > элементы: уровень политики безопасности содержимого 2"  
[W3CContentSecurityPolicy]: https://w3c.github.io/webappsec-csp "Уровень политики безопасности содержимого 3"  
[WikiManMiddleAttacks]: https://en.wikipedia.org/wiki/Man-in-the-middle_attack "Атака "злоумышленник в середине" — Википедии"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> [Здесь](https://developer.chrome.com/extensions/contentSecurityPolicy)будет найдена исходная страница.  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
