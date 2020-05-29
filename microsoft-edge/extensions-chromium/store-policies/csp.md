---
description: Политика безопасности контента для расширений EDGE (Chromium).
title: Политика безопасности контента (CSP)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: Edge-Chromium, Разработка расширений, расширения браузера, надстройки, центр партнера, разработчик
ms.openlocfilehash: 52d6d0afb38401250183788726013d521a269f06
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571607"
---
# <span data-ttu-id="04e6c-104">Политика безопасности контента \ (CSP \)</span><span class="sxs-lookup"><span data-stu-id="04e6c-104">Content Security Policy \(CSP\)</span></span>  

<span data-ttu-id="04e6c-105">Чтобы уменьшить класс потенциальных проблем с межсайтовыми сценариями, в системе расширений Microsoft Edge включена общая концепция [политики безопасности контента \ (CSP)][W3CContentSecurityPolicy].</span><span class="sxs-lookup"><span data-stu-id="04e6c-105">In order to mitigate a large class of potential cross-site scripting issues, the Microsoft Edge Extension system has incorporated the general concept of [Content Security Policy \(CSP\)][W3CContentSecurityPolicy].</span></span>  <span data-ttu-id="04e6c-106">В этом разделе представлены довольно строгие политики, которые делают расширения более безопасными по умолчанию и предоставляют возможность создавать и применять правила, регулирующие типы содержимого, которое может быть загружено и запущено вашими расширениями и приложениями.</span><span class="sxs-lookup"><span data-stu-id="04e6c-106">This introduces some fairly strict policies that make Extensions more secure by default, and provides you with the ability to create and enforce rules governing the types of content that may be loaded and run by your Extensions and applications.</span></span>  

<span data-ttu-id="04e6c-107">Как правило, CSP работает как блок/allowlistingный механизм для ресурсов, загруженных или выполняемых вашими расширениями.</span><span class="sxs-lookup"><span data-stu-id="04e6c-107">In general, CSP works as a block/allowlisting mechanism for resources loaded or run by your Extensions.</span></span>  <span data-ttu-id="04e6c-108">Определение разумной политики для вашего расширения позволяет внимательно рассмотреть ресурсы, необходимые для расширения, и попросить браузера убедиться, что это единственные ресурсы, к которым у вашего расширения есть доступ.</span><span class="sxs-lookup"><span data-stu-id="04e6c-108">Defining a reasonable policy for your Extension enables you to carefully consider the resources that your Extension requires, and to ask the browser to ensure that those are the only resources your Extension has access to.</span></span>  <span data-ttu-id="04e6c-109">Эти политики обеспечивают безопасность, а также над разрешениями узла ваши запросы на расширение; они являются дополнительным уровнем защиты, а не заменой.</span><span class="sxs-lookup"><span data-stu-id="04e6c-109">These policies provide security over and above the host permissions your Extension requests; they are an additional layer of protection, not a replacement.</span></span>  

<span data-ttu-id="04e6c-110">В Интернете такая политика определяется с помощью заголовка или `meta` элемента HTTP.</span><span class="sxs-lookup"><span data-stu-id="04e6c-110">On the web, such a policy is defined via an HTTP header or `meta` element.</span></span>  <span data-ttu-id="04e6c-111">В системе расширений Microsoft Edge ни один из них не является подходящим механизмом.</span><span class="sxs-lookup"><span data-stu-id="04e6c-111">Inside the Microsoft Edge Extension system, neither is an appropriate mechanism.</span></span>  <span data-ttu-id="04e6c-112">Вместо этого политика расширения определяется с помощью `manifest.json` файла расширения следующим образом:</span><span class="sxs-lookup"><span data-stu-id="04e6c-112">Instead, an Extension policy is defined via the `manifest.json` file for the Extension as follows:</span></span>  

```javascript
{
    ...,
    "content_security_policy": "[POLICY STRING GOES HERE]"
    ...
}
```  

> <span data-ttu-id="04e6c-113">Для получения подробных сведений о синтаксисе CSP ознакомьтесь со [спецификацией политики безопасности содержимого][W3CContentSecurityPolicy] и статьей ["Общие сведения о политике безопасности контента"][HTML5RocksIntroductionContentSecurityPolicy] на HTML5Rocks.</span><span class="sxs-lookup"><span data-stu-id="04e6c-113">For full details regarding the CSP syntax, please take a look at the [Content Security Policy specification][W3CContentSecurityPolicy] , and the ["An Introduction to Content Security Policy"][HTML5RocksIntroductionContentSecurityPolicy] article on HTML5Rocks.</span></span>  

## <span data-ttu-id="04e6c-114">Ограничения политики по умолчанию</span><span class="sxs-lookup"><span data-stu-id="04e6c-114">Default Policy Restrictions</span></span>  

<span data-ttu-id="04e6c-115">Пакеты, для которых не определена `manifest_version` Политика безопасности контента по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="04e6c-115">Packages that do not define a `manifest_version` do not have a default content security policy.</span></span>  <span data-ttu-id="04e6c-116">Для тех, кто выберет `manifest_version` 2, есть стандартная политика безопасности содержимого:</span><span class="sxs-lookup"><span data-stu-id="04e6c-116">Those that select `manifest_version` 2, have a default content security policy of:</span></span>  

```javascript
script-src 'self'; object-src 'self'
```  

<span data-ttu-id="04e6c-117">Эта политика обеспечивает безопасность путем ограничения расширений и приложений тремя способами:</span><span class="sxs-lookup"><span data-stu-id="04e6c-117">This policy adds security by limiting Extensions and applications in three ways:</span></span>  

**<span data-ttu-id="04e6c-118">Eval и связанные функции отключены</span><span class="sxs-lookup"><span data-stu-id="04e6c-118">Eval and related functions are disabled</span></span>**  

<span data-ttu-id="04e6c-119">Следующие программы не работают.</span><span class="sxs-lookup"><span data-stu-id="04e6c-119">Code like the following does not work:</span></span>  

```javascript
alert(eval("foo.bar.baz"));
window.setTimeout("alert('hi')", 10);
window.setInterval("alert('hi')", 10);
new Function("return foo.bar.baz");
```  

<span data-ttu-id="04e6c-120">Вычисление строк JavaScript так же, как и в случае, — это распространенный вектор атаки XSS.</span><span class="sxs-lookup"><span data-stu-id="04e6c-120">Evaluating strings of JavaScript like this is a common XSS attack vector.</span></span>  <span data-ttu-id="04e6c-121">Вместо этого необходимо написать следующий код:</span><span class="sxs-lookup"><span data-stu-id="04e6c-121">Instead, you should write code like:</span></span>

```javascript
alert(foo && foo.bar && foo.bar.baz);
window.setTimeout(function() { alert('hi'); }, 10);
window.setInterval(function() { alert('hi'); }, 10);
function() { return foo && foo.bar && foo.bar.baz };
```  

**<span data-ttu-id="04e6c-122">Встроенные сценарии JavaScript не выполняются</span><span class="sxs-lookup"><span data-stu-id="04e6c-122">Inline JavaScript are not run</span></span>**  

<span data-ttu-id="04e6c-123">Встроенные сценарии JavaScript не выполняются.</span><span class="sxs-lookup"><span data-stu-id="04e6c-123">Inline JavaScript are not run.</span></span>  <span data-ttu-id="04e6c-124">Это ограничение BANS как встроенные `<script>` блоки, так и встроенные обработчики событий, такие как `<button onclick="...">` .</span><span class="sxs-lookup"><span data-stu-id="04e6c-124">This restriction bans both inline `<script>` blocks and inline event handlers, such as `<button onclick="...">`.</span></span>

<span data-ttu-id="04e6c-125">Первое ограничение — это очистка огромного класса межсайтовых атак с помощью сценариев, что делает невозможным случайный запуск сценария, предоставленного вредоносным сторонним лицом.</span><span class="sxs-lookup"><span data-stu-id="04e6c-125">The first restriction wipes out a huge class of cross-site scripting attacks by making it impossible for you to accidentally run the script provided by a malicious third-party.</span></span>  <span data-ttu-id="04e6c-126">Тем не менее, в этом случае необходимо написать код с четким разделением между содержимым и поведением (что нужно делать, если вы хотите, чтобы все это правильно, верно? \).</span><span class="sxs-lookup"><span data-stu-id="04e6c-126">It does, however, require you to write your code with a clean separation between content and behavior \(which you should of course do anyway, right?\).</span></span>  <span data-ttu-id="04e6c-127">Например, это можно сделать более четким.</span><span class="sxs-lookup"><span data-stu-id="04e6c-127">An example may make this clearer.</span></span>  <span data-ttu-id="04e6c-128">Вы можете попытаться создать всплывающее действие браузера в виде одного `pop-up.html` содержащего:</span><span class="sxs-lookup"><span data-stu-id="04e6c-128">You may try to write a Browser Action pop-up as a single `pop-up.html` containing:</span></span>  

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

<span data-ttu-id="04e6c-129">Необходимо изменить три действия, чтобы сделать эту работу нужной, чтобы она выглядела так, как вы ожидаете.</span><span class="sxs-lookup"><span data-stu-id="04e6c-129">Three things must change in order to make this work the way you expect it to:</span></span>  

*   <span data-ttu-id="04e6c-130">`clickHandler`Определение должно быть перемещено во внешний файл JavaScript \ ( `popup.js` может быть хорошим целевым).</span><span class="sxs-lookup"><span data-stu-id="04e6c-130">The `clickHandler` definition must be moved into an external JavaScript file \(`popup.js` may be a good target).</span></span>  
*   <span data-ttu-id="04e6c-131">Определение обработчика встроенных событий должно быть переписано в отношении `addEventListener` и извлечено `popup.js` .</span><span class="sxs-lookup"><span data-stu-id="04e6c-131">The inline event handler definitions must be rewritten in terms of `addEventListener` and extracted into `popup.js`.</span></span>  
    <span data-ttu-id="04e6c-132">Если вы запускаете программу с помощью такого кода `<body onload="main();">` , замените ее на `DOMContentLoaded` событие в документе или `load` событие в окне (в зависимости от ваших требований).</span><span class="sxs-lookup"><span data-stu-id="04e6c-132">If you are currently starting your program using code like `<body onload="main();">`, consider replacing it by hooking into the `DOMContentLoaded` event of the document, or the `load` event of the window, depending on your requirements.</span></span>  <span data-ttu-id="04e6c-133">Используйте бывший, так как он обычно инициируется быстрее.</span><span class="sxs-lookup"><span data-stu-id="04e6c-133">Use the former, since it generally triggers more quickly.</span></span>  

*   <span data-ttu-id="04e6c-134">`setTimeout`Необходимо переписать вызов, чтобы избежать преобразования строки `"awesome(); totallyAwesome()"` в JavaScript для выполнения.</span><span class="sxs-lookup"><span data-stu-id="04e6c-134">The `setTimeout` call must be rewritten to avoid converting the string `"awesome(); totallyAwesome()"` into JavaScript for running.</span></span>  
    <span data-ttu-id="04e6c-135">Эти изменения могут выглядеть примерно так, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="04e6c-135">Those changes may look something like the following:</span></span>  

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

**<span data-ttu-id="04e6c-136">Загружаются только локальный сценарий и ресурсы объектов.</span><span class="sxs-lookup"><span data-stu-id="04e6c-136">Only local script and object resources are loaded</span></span>**  

<span data-ttu-id="04e6c-137">Ресурсы сценариев и объектов можно загружать только из пакета расширения, но не из веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="04e6c-137">Script and object resources are only able to be loaded from the Extension package, not from the web at large.</span></span>  <span data-ttu-id="04e6c-138">Это гарантирует, что ваше расширение будет выполнять только код, который вы только что утвердили, и не позволяя вредоносному сетевому злоумышленнику перенаправлять запрос на ресурс.</span><span class="sxs-lookup"><span data-stu-id="04e6c-138">This ensures that your Extension only runs the code you specifically approved, preventing an active network attacker from maliciously redirecting your request for a resource.</span></span>  

<span data-ttu-id="04e6c-139">Вместо того чтобы писать код, зависящий от библиотеки, загружаемой из внешней сети CDN, рассматривайте в пакете расширения определенную версию jQuery.</span><span class="sxs-lookup"><span data-stu-id="04e6c-139">Instead of writing code that depends on jQuery \(or any other library\) loading from an external CDN, consider including the specific version of jQuery in your Extension package.</span></span>  <span data-ttu-id="04e6c-140">Это значит, что вместо:</span><span class="sxs-lookup"><span data-stu-id="04e6c-140">That is, instead of:</span></span>  

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

<span data-ttu-id="04e6c-141">Скачайте файл, включите его в пакет и напишите следующее:</span><span class="sxs-lookup"><span data-stu-id="04e6c-141">Download the file, include it in your package, and write:</span></span>  

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

## <span data-ttu-id="04e6c-142">Применяйте политику по умолчанию</span><span class="sxs-lookup"><span data-stu-id="04e6c-142">Relaxing the default policy</span></span>  

**<span data-ttu-id="04e6c-143">Встроенный сценарий</span><span class="sxs-lookup"><span data-stu-id="04e6c-143">Inline Script</span></span>**  

<!-- Up until Chrome 45, there was no mechanism for relaxing the restriction against running inline JavaScript.  In particular, setting a script policy that includes `'unsafe-inline'` has no effect.  

As of Chrome 46, -->  

<span data-ttu-id="04e6c-144">Встроенные скрипты можно разрешить, указав хэш-код в исходном коде в политике в формате Base64.</span><span class="sxs-lookup"><span data-stu-id="04e6c-144">Inline scripts are able to be allowed by specifying the base64-encoded hash of the source code in the policy.</span></span>  <span data-ttu-id="04e6c-145">Этот хэш-код должен быть префиксом используемого хэш-алгоритма \ (SHA256, SHA384 или SHA512 \).</span><span class="sxs-lookup"><span data-stu-id="04e6c-145">This hash must be prefixed by the used hash algorithm \(sha256, sha384 or sha512\).</span></span>  <span data-ttu-id="04e6c-146">Пример: [использование хэша для элементов <Script \ >][W3CContentSecurityPolicyLevel2ScriptSrcHashUsage] .</span><span class="sxs-lookup"><span data-stu-id="04e6c-146">See [Hash usage for \<script\> elements][W3CContentSecurityPolicyLevel2ScriptSrcHashUsage] for an example.</span></span>  

**<span data-ttu-id="04e6c-147">Удаленный сценарий</span><span class="sxs-lookup"><span data-stu-id="04e6c-147">Remote Script</span></span>**  

<span data-ttu-id="04e6c-148">Если вам нужны внешние ресурсы JavaScript или объект, вы можете ослабить политику в ограниченном масштабе, allowlisting безопасные источники, из которых следует принимать сценарии.</span><span class="sxs-lookup"><span data-stu-id="04e6c-148">If you require some external JavaScript or object resources, you may relax the policy to a limited extent by allowlisting secure origins from which scripts should be accepted.</span></span>  <span data-ttu-id="04e6c-149">Убедитесь, что ресурсы среды выполнения, загруженные с повышенными разрешениями расширения, представляют собой именно те ресурсы, которые вы ожидаете, и не заменяются активным злоумышленником сети.</span><span class="sxs-lookup"><span data-stu-id="04e6c-149">Verify that runtime resources loaded with with elevated permissions of an Extension are exactly the resources you expect, and are not replaced by an active network attacker.</span></span>  <span data-ttu-id="04e6c-150">Поскольку [атака "злоумышленник из-за середины"][WikiManMiddleAttacks] является тривиальной и необнаруживаемой по протоколу HTTP, эти источники не принимаются.</span><span class="sxs-lookup"><span data-stu-id="04e6c-150">As [man-in-the-middle attacks][WikiManMiddleAttacks] are both trivial and undetectable over HTTP, those origins are not accepted.</span></span>  

<span data-ttu-id="04e6c-151">В настоящее время разработчики могут доменов источники со следующими схемами:,, `blob` `filesystem` `https` и `extension` .</span><span class="sxs-lookup"><span data-stu-id="04e6c-151">Currently, developers are able to allowlist origins with the following schemes: `blob`, `filesystem`, `https`, and `extension`.</span></span>  <span data-ttu-id="04e6c-152">Для схем должны быть явно указаны ведущие части источника `https` `extension` .</span><span class="sxs-lookup"><span data-stu-id="04e6c-152">The host part of the origin must explicitly be specified for the `https` and `extension` schemes.</span></span>  <span data-ttu-id="04e6c-153">Универсальные подстановочные знаки, такие как HTTPS: `https://*` и `https://*.com` не разрешены; подстановочные знаки поддомены, такие как `https://*.example.com` разрешены.</span><span class="sxs-lookup"><span data-stu-id="04e6c-153">Generic wildcards such as https:, `https://*` and `https://*.com` are not allowed; subdomain wildcards such as `https://*.example.com` are allowed.</span></span>  <span data-ttu-id="04e6c-154">Домены в [списке общедоступных суффиксов][PublicSuffixList] также просматриваются как общие домены верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="04e6c-154">Domains in the [Public Suffix list][PublicSuffixList] are also viewed as generic top-level domains.</span></span>  <span data-ttu-id="04e6c-155">Чтобы загрузить ресурс из этих доменов, поддомены должны быть явно указаны в списке.</span><span class="sxs-lookup"><span data-stu-id="04e6c-155">To load a resource from these domains, the subdomain must explicitly be listed.</span></span>  <span data-ttu-id="04e6c-156">Например, `https://*.cloudfront.net` является недопустимым, но `https://XXXX.cloudfront.net` и `https://*.XXXX.cloudfront.net` может быть allowlisted.</span><span class="sxs-lookup"><span data-stu-id="04e6c-156">For example, `https://*.cloudfront.net` is not valid, but `https://XXXX.cloudfront.net` and `https://*.XXXX.cloudfront.net` are able to be allowlisted.</span></span>  

<span data-ttu-id="04e6c-157">Для упрощения разработки ресурсы, загруженные через HTTP с серверов на локальном компьютере, могут быть allowlisted.</span><span class="sxs-lookup"><span data-stu-id="04e6c-157">For development ease, resources loaded over HTTP from servers on your local machine are able to be allowlisted.</span></span>  <span data-ttu-id="04e6c-158">Вы можете доменов сценарии и источники объектов на любом порту либо `http://127.0.0.1` или `http://localhost` .</span><span class="sxs-lookup"><span data-stu-id="04e6c-158">You may allowlist script and object sources on any port of either `http://127.0.0.1` or `http://localhost`.</span></span>  

> [!NOTE]
> <span data-ttu-id="04e6c-159">Ограничение для ресурсов, загруженных по протоколу HTTP, применяется только к тем ресурсам, которые выполняются напрямую.</span><span class="sxs-lookup"><span data-stu-id="04e6c-159">The restriction against resources loaded over HTTP applies only to those resources which are directly run.</span></span>  <span data-ttu-id="04e6c-160">Вы по-прежнему свободны, например, чтобы создавать соединения XMLHTTPRequest для любого источника, который вам нравится; политика по умолчанию не ограничивает `connect-src` или никакие другие директивы CSP каким бы то ни было.</span><span class="sxs-lookup"><span data-stu-id="04e6c-160">You are still free, for example, to make XMLHTTPRequest connections to any origin you like; the default policy does not restrict `connect-src` or any of the other CSP directives in any way.</span></span>  

<span data-ttu-id="04e6c-161">Неявное определение политики, позволяющее загружать ресурсы сценария из example.com по HTTPS, может выглядеть так:</span><span class="sxs-lookup"><span data-stu-id="04e6c-161">A relaxed policy definition which allows script resources to be loaded from example.com over HTTPS may look like:</span></span>  

```javascript
"content_security_policy": "script-src 'self' https://example.com; object-src 'self'"
```  

> [!NOTE]
> <span data-ttu-id="04e6c-162">Оба `script-src` и `object-src` определяются политикой.</span><span class="sxs-lookup"><span data-stu-id="04e6c-162">Both `script-src` and `object-src` are defined by the policy.</span></span>  <span data-ttu-id="04e6c-163">Microsoft EDGE не допускает политику, которая не ограничивает каждый из этих значений на \ (не менее \) " `self` .</span><span class="sxs-lookup"><span data-stu-id="04e6c-163">Microsoft Edge does not accept a policy that does not limit each of these values to \(at least\) '`self`'.</span></span>  

<!-- Making use of Google Analytics is the canonical example for this sort of policy definition.  It is common enough that an Analytics boilerplate of sorts is provided in the Event Tracking with Google Analytics sample Extension, and a brief tutorial that goes into more detail.  -->  

**<span data-ttu-id="04e6c-164">Оцененный JavaScript</span><span class="sxs-lookup"><span data-stu-id="04e6c-164">Evaluated JavaScript</span></span>**  

<span data-ttu-id="04e6c-165">Политику и `eval()` связанные с ней функции, такие как `setTimeout(String)` и, `setInterval(String)` и `new Function(String)` они могут быть ослаблены путем добавления `unsafe-eval` к политике.</span><span class="sxs-lookup"><span data-stu-id="04e6c-165">The policy against `eval()` and related functions like `setTimeout(String)`, `setInterval(String)`, and `new Function(String)` are able to be relaxed by adding `unsafe-eval` to your policy:</span></span>  

```javascript
"content_security_policy": "script-src 'self' 'unsafe-eval'; object-src 'self'"
```  

<span data-ttu-id="04e6c-166">Тем не менее, мы настоятельно рекомендуем сделать это.</span><span class="sxs-lookup"><span data-stu-id="04e6c-166">However, we strongly recommend against doing this.</span></span>  <span data-ttu-id="04e6c-167">Эти функции являются глобальными векторами атак XSS.</span><span class="sxs-lookup"><span data-stu-id="04e6c-167">These functions are notorious XSS attack vectors.</span></span>  

## <span data-ttu-id="04e6c-168">Усиление политики по умолчанию</span><span class="sxs-lookup"><span data-stu-id="04e6c-168">Tightening the default policy</span></span>  

<span data-ttu-id="04e6c-169">Разумеется, вы, конечно же, заследуете эту политику в отношении того, какое расширение позволит вам повысить безопасность за счет удобства.</span><span class="sxs-lookup"><span data-stu-id="04e6c-169">You may, of course, tighten this policy to whatever extent your Extension allows in order to increase security at the expense of convenience.</span></span>  <span data-ttu-id="04e6c-170">Чтобы указать, что расширение может загружать только ресурсы любого типа \ (изображения и т. д.) из связанного пакета расширения, например, `default-src 'self'` может быть уместным.</span><span class="sxs-lookup"><span data-stu-id="04e6c-170">To specify that your Extension are able to only load resources of any type \(images, and so on\) from the associated Extension package, for example, a policy of `default-src 'self'` may be appropriate.</span></span>  

<!-- The Mappy sample Extension is a good example of an Extension that is been locked down above and beyond the defaults.  -->  

## <span data-ttu-id="04e6c-171">Сценарии содержимого</span><span class="sxs-lookup"><span data-stu-id="04e6c-171">Content Scripts</span></span>  

<span data-ttu-id="04e6c-172">Обсуждаемая политика применяется к фоновым страницам и страницам событий расширения.</span><span class="sxs-lookup"><span data-stu-id="04e6c-172">The policy being discussing applies to the background pages and event pages of the Extension.</span></span>  <span data-ttu-id="04e6c-173">Применение сценариев содержимого к скриптам содержимого в расширении более сложно.</span><span class="sxs-lookup"><span data-stu-id="04e6c-173">How the content scripts apply to the content scripts of the Extension is more complicated.</span></span>  

<span data-ttu-id="04e6c-174">Как правило, в скриптах содержимого не распространяется расширение CSP.</span><span class="sxs-lookup"><span data-stu-id="04e6c-174">Content scripts are generally not subject to the CSP of the Extension.</span></span>  <span data-ttu-id="04e6c-175">Так как сценарии содержимого не являются HTML, основным эффектом является то, что они могут использоваться `eval` даже в том случае, если не указан CSP расширения `unsafe-eval` , но это не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="04e6c-175">Since content scripts are not HTML, the main impact of this is that they may use `eval` even if the CSP of the Extension does not specify `unsafe-eval`, although this is not recommended.</span></span>  <span data-ttu-id="04e6c-176">Кроме того, CSP страницы не применяется к скриптам содержимого.</span><span class="sxs-lookup"><span data-stu-id="04e6c-176">Additionally, the CSP of the page does not apply to content scripts.</span></span>  <span data-ttu-id="04e6c-177">Более сложная программа — это `<script>` теги, с помощью которых сценарии содержимого создают и помещаются в модель DOM той страницы, на которой они запущены.</span><span class="sxs-lookup"><span data-stu-id="04e6c-177">More complicated are `<script>` tags that content scripts create and put into the DOM of the page they are running on.</span></span>  <span data-ttu-id="04e6c-178">На эти ссылки указываются сценарии внедрения, пересылаемые в модели DOM.</span><span class="sxs-lookup"><span data-stu-id="04e6c-178">These are referenced as DOM injected scripts going forward.</span></span>  

<span data-ttu-id="04e6c-179">Вставленные сценарии модели, которые выполняются сразу после введения на страницу.</span><span class="sxs-lookup"><span data-stu-id="04e6c-179">DOM injected scripts that run immediately upon injection into the page runs as you may expect.</span></span>  <span data-ttu-id="04e6c-180">Представьте сценарий содержимого с помощью следующего кода как простой пример:</span><span class="sxs-lookup"><span data-stu-id="04e6c-180">Imagine a content script with the following code as a simple example:</span></span>  

```javascript
document.write("<script>alert(1);</script>");
 ```  

<span data-ttu-id="04e6c-181">Этот сценарий содержимого вызывает `alert` немедленное выполнение `document.write()` .</span><span class="sxs-lookup"><span data-stu-id="04e6c-181">This content script causes an `alert` immediately upon the `document.write()`.</span></span>  <span data-ttu-id="04e6c-182">Обратите внимание на то, что это действие выполняется независимо от политики, которая может быть указана на странице.</span><span class="sxs-lookup"><span data-stu-id="04e6c-182">Note that this runs regardless of the policy a page may specify.</span></span>
<span data-ttu-id="04e6c-183">Тем не менее, в этом случае все сложнее в рамках вставленного сценария DOM и для любого сценария, который не запускается сразу после вставки.</span><span class="sxs-lookup"><span data-stu-id="04e6c-183">However, the behavior becomes more complicated both inside that DOM injected script and for any script that does not immediately run upon injection.</span></span>  <span data-ttu-id="04e6c-184">Представьте, что ваше расширение запущено на странице, предоставляющей соответствующий CSP, который указывает `script-src 'self'` .</span><span class="sxs-lookup"><span data-stu-id="04e6c-184">Imagine that your Extension is running on a page that provides an associated CSP that specifies `script-src 'self'`.</span></span>  <span data-ttu-id="04e6c-185">Теперь представьте, что сценарий содержимого запускает следующий код:</span><span class="sxs-lookup"><span data-stu-id="04e6c-185">Now imagine the content script runs the following code:</span></span>  

```javascript
document.write("<button onclick='alert(1);'>click me</button>'");
```  

<span data-ttu-id="04e6c-186">Если пользователь нажмет на эту кнопку, `onclick` сценарий не запускается.</span><span class="sxs-lookup"><span data-stu-id="04e6c-186">If a user clicks on that button, the `onclick` script does not run.</span></span>  <span data-ttu-id="04e6c-187">Это связано с тем, что сценарий не был немедленно запущен, а код не интерпретируется, пока событие нажатия не будет рассматриваться как часть скрипта содержимого, поэтому CSP на странице \ (не расширение \) ограничил поведение.</span><span class="sxs-lookup"><span data-stu-id="04e6c-187">This is because the script did not immediately run and code is not interpreted until the click event occurs is not considered part of the content script, so the CSP of the page \(not of the Extension\) restricts the behavior.</span></span>  <span data-ttu-id="04e6c-188">А так как этот CSP не указан `unsafe-inline` , обработчик встроенных событий блокируется.</span><span class="sxs-lookup"><span data-stu-id="04e6c-188">And since that CSP does not specify `unsafe-inline`, the inline event handler is blocked.</span></span>  
<span data-ttu-id="04e6c-189">Правильный способ реализации нужного поведения в этом случае может быть `onclick` следующим: добавьте обработчик как функцию из сценария содержимого, как описано ниже.</span><span class="sxs-lookup"><span data-stu-id="04e6c-189">The correct way to implement the desired behavior in this case may be to add the `onclick` handler as a function from the content script as follows:</span></span>  

```javascript
document.write("<button id='mybutton'>click me</button>'");
var button = document.getElementById('mybutton');
button.onclick = function() {
      alert(1);
};
```  

<span data-ttu-id="04e6c-190">Если сценарий содержимого выполняет указанные ниже действия, возникает другая подобная ошибка.</span><span class="sxs-lookup"><span data-stu-id="04e6c-190">Another similar issue arises if the content script runs the following:</span></span>  

```javascript
var script = document.createElement('script');
script.innerHTML = 'alert(1);'
document.getElementById('body').appendChild(script);
```  

<span data-ttu-id="04e6c-191">В этом случае запускается сценарий, и отображается оповещение.</span><span class="sxs-lookup"><span data-stu-id="04e6c-191">In this case, the script runs and the alert displays.</span></span>  <span data-ttu-id="04e6c-192">Тем не менее, сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="04e6c-192">However, take this case:</span></span>  

```javascript
var script = document.createElement('script');
script.innerHTML = 'eval("alert(1);")';
=document.getElementById('body').appendChild(script);
```  

<span data-ttu-id="04e6c-193">При запуске исходного сценария Звонок `eval` блокируется.</span><span class="sxs-lookup"><span data-stu-id="04e6c-193">While the initial script runs, the call to `eval` is blocked.</span></span>  <span data-ttu-id="04e6c-194">Таким образом, если исходная среда выполнения сценария разрешена, поведение в сценарии регулируется CSP страницы.</span><span class="sxs-lookup"><span data-stu-id="04e6c-194">That is, while the initial script runtime is allowed, the behavior within the script is regulated by the CSP of the page.</span></span>  
<span data-ttu-id="04e6c-195">Таким образом, в зависимости от того, как вы пишете внедренные сценарии DOM в расширении, изменения в CSP страницы могут повлиять на работу вашего расширения.</span><span class="sxs-lookup"><span data-stu-id="04e6c-195">Thus, depending on how you write DOM injected scripts in your Extension, changes to the CSP of the page may affect the behavior of your Extension.</span></span>  <span data-ttu-id="04e6c-196">Так как на сценарии контента не влияет поставщик служб (CSP) страницы, это может быть вызвано тем, что это может повлиять на расширение в сценарий содержимого, а не на добавленные в DOM сценарии.</span><span class="sxs-lookup"><span data-stu-id="04e6c-196">Since content scripts are not affected by the CSP of the page, this a great reason to put as much behavior as possible of your Extension into the content script rather than DOM injected scripts.</span></span>  

<!-- image links -->  

<!-- links -->  

[HTML5RocksIntroductionContentSecurityPolicy]: https://www.html5rocks.com/en/tutorials/security/content-security-policy "Общие сведения о политике безопасности содержимого — HTML5 Rocks"  
[PublicSuffixList]: https://publicsuffix.org/list "ПРОСМОТР СПИСКА ОТКРЫТЫХ СУФФИКСОВ"  
[W3CContentSecurityPolicyLevel2ScriptSrcHashUsage]: https://www.w3.org/TR/CSP2#script-src-hash-usage "Использование хэша для <сценарий \ > элементы: уровень политики безопасности содержимого 2"  
[W3CContentSecurityPolicy]: https://w3c.github.io/webappsec-csp "Уровень политики безопасности содержимого 3"  
[WikiManMiddleAttacks]: https://en.wikipedia.org/wiki/Man-in-the-middle_attack "Атака "злоумышленник в середине" — Википедии"  

> [!NOTE]
> <span data-ttu-id="04e6c-202">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="04e6c-202">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="04e6c-203">[Здесь](https://developer.chrome.com/extensions/contentSecurityPolicy)будет найдена исходная страница.</span><span class="sxs-lookup"><span data-stu-id="04e6c-203">The original page is found [here](https://developer.chrome.com/extensions/contentSecurityPolicy).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="04e6c-205">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="04e6c-205">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
