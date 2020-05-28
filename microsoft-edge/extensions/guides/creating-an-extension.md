---
description: Сведения о том, как создать расширение Microsoft Edge
title: Создание расширения
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: EDGE, веб-разработка, HTML, CSS, JavaScript, разработчик
ms.custom: seodec18
ms.openlocfilehash: a08fc6bd604ce810895e7103f7f6384dbedc9f78
ms.sourcegitcommit: 0bc1312a1e6a0ac37cf385201db4361fc05184fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/28/2020
ms.locfileid: "10683653"
---
# Создание расширения Microsoft Edge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

В этом руководстве рассказывается, как создать расширение для Microsoft Edge.  Этот пример расширения позволяет управлять определенными CSS для [docs.Microsoft.com][MicrosoftDocs] страниц, включая процесс создания файла манифеста, пользовательского интерфейса и сценариев фона и содержимого.  

:::image type="complex" source="../media/color-changer_header.png" alt-text="Docs.microsoft.com текст изменился на синий":::
   Docs.microsoft.com текст изменился на синий
:::image-end:::

<!--![Docs.microsoft.com body changed to blue][ImageColorChangerHeader]  -->  

В этом руководстве предполагается, что вы понимаете, что такое расширение браузера и как оно работает.  Более подробное описание стандартных блоков для расширений можно найти в разделе [Анатомия расширения][MDNAnatomyExtension].  

Скачайте код для [полного примера на GitHub][GithubMicrosoftEdgeExtensionsDemosColorChanger].  

## Создание файла манифеста  

Для начала создайте каталог для расширения и назовите его `color-changer` .  

В `color-changer` папке создайте файл с именем `manifest.json` .  `manifest.json`Файл является обязательным для всех расширений и предоставляет важную информацию для расширения, начиная от имени расширения до разрешений.  

> [!NOTE] 
> В этом руководстве описаны все ключи манифеста, которые необходимо использовать в этом руководстве, но для списка поддерживаемых и рекомендуемых ключей манифестов — [Поддерживаемые ключи манифеста][ExtensionsApisupportManifestKeys].  

Внутри `manifest.json` добавьте следующий код.  

```json
{
  "name": "Color Changer",
  "author": "Microsoft Edge Extension Developer",
  "version": "1.0",
  "description": "Change the color of the body on docs.microsoft.com",
  "permissions": [
    "*://docs.microsoft.com/*",
    "tabs"
  ], 
  "browser_action": {
    "default_icon": {
      "20": "images/color-changer20.png",
      "40": "images/color-changer40.png"
    },
    "default_title": "Color Changer",
    "default_popup": "popup.html"
  }
}
```  

### Определение ключа манифеста  

| Раздел | Сведения |  
|:--- |:--- |  
| [name][MDNManifestjsonName] | Имя расширения.  |  
| [созданные][MDNManifestjsonAuthor] | Автор расширения.  |  
| [version][MDNManifestjsonVersion] | Номер версии расширения.  |  
| [description][MDNManifestjsonDescription] | Описание расширения, отображаемое в разделе "о программе" в меню "расширение" в Microsoft Edge.  |  
| [правами][MDNManifestjsonPermissions] | Массив строк, запрашивающих разрешение на расширение.  Для расширения вы запрашиваете разрешения на просмотр веб-сайтов, которые посещаете \ ("вкладки" "), а также обновляют контент по URL-адресам, соответствующим" `*://docs.microsoft.com/*` ".  |  
| [browser_action][MDNManifestjsonBrowserAction] | Содержат сведения о значке. Значок будет размещен на панели инструментов Microsoft Edge справа от адресной строки.  |  

#### определение ключа browser_action  

| Раздел | Сведения |  
|:--- |:--- |  
| `default_icon` | Значок, который используется на панели инструментов.  |  
| `default_title` | Текст, который отображается, когда пользователь наводит указатель мыши на значок на панели инструментов.  |  
| `default_popup` | Путь к файлу HTML всплывающего окна.  |  

Теперь, когда вы создали файл манифеста, вам понадобится пользовательский интерфейс для расширения.  

## Создание всплывающего окна  

Для расширения создайте всплывающее окно для пользовательского интерфейса, как показано ниже.  

:::image type="complex" source="../media/color-changer_popup.png" alt-text="Всплывающий интерфейс расширения":::
   Всплывающий интерфейс расширения
:::image-end:::

<!--![The pop-up interface of the extension][ImageColorChangerPopup]  -->  

Создайте файл с именем `popup.html` в корне `color-changer` папки.  Вставьте следующий код в `popup.html` .  

```html
<!DOCTYPE html>
<html>
    <head>
        <link rel="stylesheet" type="text/css" href="css/styles.css" />
    </head>
    <body>
        <h1>Creating a Microsoft Edge Extension</h1>
        <p>Color Changer</p>
        <input id="aliceblue" type="button" value="Aliceblue" />
        <input id="cornsilk" type="button" value="Cornsilk" />
        <input id="reset" type="button" value="Reset" />
        <script src="js/popup.js"></script>
    </body>
</html>
```  

В `popup.html` необходимо создать заголовок, абзац и три кнопки \ (AliceBlue, Cornsilk и Reset \).  

Теперь создайте папку с именем `css` и внутри нее `styles.css` .  Добавьте стили ниже.  

```css
/* main styles */
* {
    font-family: 'Segoe UI';
}

h1 {
    font-weight: 600;
    font-size: .9em;
}

p {
    font-weight: 500;
    font-size: .8em;
    margin-bottom: 10px;  
}
```  

Этот CSS обеспечивает расширение некоторых основных стилей.  Вы можете добавить дополнительные стили, чтобы настроить расширение.  

Затем необходимо создать файл JavaScript, который будет взаимодействовать с всплывающим окном.  Создание `js` папки и файла с именем " `popup.js` внутри".  Обновите `popup.js` с помощью следующего кода.  

```JavaScript
// get the buttons by id
let aliceblue = document.getElementById('aliceblue');
let cornsilk = document.getElementById('cornsilk');
let reset = document.getElementById('reset');

// use tabs.insertCSS to change header color on button click

// aliceblue
aliceblue.onclick = () => {
  browser.tabs.insertCSS({code: "body { background: aliceblue !important; }"});
};

// cornsilk
cornsilk.onclick = () => {
  browser.tabs.insertCSS({code: "body { background: cornsilk !important; }"});
};

// back to original
reset.onclick = () => {
  browser.tabs.insertCSS({code: "body { background: none !important; }"});
};
```  

В `popup.js` API-интерфейсе [вкладок][MDNApiTabs] можно взаимодействовать с вкладками браузера и внедрять сценарии и стили в содержимое страницы.  С помощью метода [Табуляторы. insertCSS ()][MDNApiTabsInsertcss] вы вставляете на страницу УКАЗАННУЮ таблицу стилей, которая изменяет цвет заголовка [docs.Microsoft.com][MicrosoftDocs] на другой при нажатии указанной кнопки.  

Теперь, когда у вас есть основные функциональные возможности всплывающего окна, добавьте в расширение значки.  

## Добавление значков  

Значки используются для представления расширения на панели инструментов браузера, в меню "расширения" и в других местах.  Скачайте [значки для расширения в GitHub][GithubMicrosoftEdgeExtensionsDemosColorChangerImages]. Дополнительные сведения о значках расширений в Microsoft EDGE можно найти в разделе [руководство по проектированию][ExtensionsGuidesDesignIcons].  

После того как вы загрузили значки расширений, сохраните значки в `images` папке внутри нее `color-changer` .  

Значок, который отображается на панели инструментов, задается в `default_icon` разделе [browser_action][MDNManifestjsonBrowserAction] , который вы уже добавили в файл манифеста в более ранних разделах.  

`icons`Ключ определяет, какие значки следует использовать в меню "параметры расширений".  Ниже показано, как задать несколько значков с разными размерами для учета различных разрешений экрана.  Имена значков `25` и `48` Высота значков в пикселях.  

В файле [manifest. JSON][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] включите в него ключ верхнего уровня `icons` .  

```json
  "icons": {
    "25": "images/color-changer25.png",
    "48": "images/color-changer48.png"
  }
```  

### Определение ключа манифеста  

| Раздел | Сведения |  
|:--- |:--- |  
| [значки][MDNManifestjsonIcons] | Значки для расширения с парами "ключ-значение" размера изображения `px` и путем изображения относительно корневого каталога расширения. |  

> [!NOTE]
> С помощью значков, указанных `inactive##.png` в папке Images ниже, в этом руководстве.  

## Проверка расширения  

Теперь, когда вы добавили пользовательский интерфейс и создали значки, проверьте расширение.  Пошаговые инструкции по [добавлению расширения][ExtensionsGuidesAddingRemovingExtensionsAdding] в Microsoft Edge.  Затем вернитесь к этому руководству.  

После добавления расширения перейдите на любую страницу [docs.Microsoft.com][MicrosoftDocs] .  После нажатия на действие браузера появится следующее всплывающее окно.  Цвет основного текста [docs.Microsoft.com][MicrosoftDocs] также должен изменить цвет.  

:::row:::
   :::column span="1":::
      :::image type="complex" source="../media/color-changer_header_aliceblue.png" alt-text="Заголовок Docs.microsoft.com изменен на AliceBlue":::
         Заголовок Docs.microsoft.com изменен на AliceBlue :::image-end:::
      
      <!--![Docs.microsoft.com header changed to Aliceblue][ImageColorChangerHeaderAliceblue]  -->
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="../media/color-changer_header_cornsilk.png" alt-text="Заголовок Docs.microsoft.com изменен на Cornsilk":::
         Заголовок Docs.microsoft.com изменен на Cornsilk :::image-end:::
      
      <!--![Docs.microsoft.com header changed to Cornsilk][ImageColorChangerHeaderCornsilk]  -->
   :::column-end:::
:::row-end:::

Если вы столкнулись с ошибками или неработоспособными функциями, ознакомьтесь с руководством по [расширениям отладки][ExtensionsGuidesDebuggingExtensions] или Скачайте [полный пример в GitHub][GithubMicrosoftEdgeExtensionsDemosColorChanger].  

## Добавление содержимого и фоновых сценариев  

Чтобы отключить расширение работы со страницами за пределами домена [docs.Microsoft.com][MicrosoftDocs] , перейдите на один шаг вперед и добавьте логику.  

Сначала необходимо создать [сценарий содержимого][MDNContentScripts].  Затем необходимо создать скрипты содержимого, которые выполняются в контексте определенной веб-страницы, и получить доступ к содержимому веб-страницы и взаимодействовать с фоновыми сценариями.  В `js` каталоге создайте файл с именем `content.js` и добавьте следующий код.  

```javascript
// get the URL of the page
var url = document.location.href;

// if not on a docs.microsoft.com domain
if (url.indexOf("//docs.microsoft.com") === -1) {
    // send inactive icons
    browser.runtime.sendMessage({
        "iconPath20": "images/inactive20.png",
        "iconPath40": "images/inactive40.png"
    });
}
```  

Этот сценарий получает URL-адрес текущей страницы `document.location.href` и проверяет, находится ли текущая страница в домене [docs.Microsoft.com][MicrosoftDocs] .  Если страница не находится в домене [docs.Microsoft.com][MicrosoftDocs] \ (например, [https://www.bing.com/][|::ref1::|] \), пути к неактивным значкам \ (Затененные значки \) отправляются в фоновый сценарий с помощью [среды выполнения. SendMessage ()][MDNApiRuntimeSendmessage].  

Вы должны обновить файл [manifest. JSON][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] , добавив в него следующий `content_scripts` раздел.  

```json
  "content_scripts": [{
    "matches": [
        "<all_urls>"
    ],
    "js": ["js/content.js"],
    "run_at": "document_end"
}]
```  

### Определение ключа манифеста  

| Раздел | Сведения |  
|:--- |:---- |  
| [content_scripts][MDNManifestjsonContentScripts] | Сведения о том, какие скрипты содержимого должен загружать браузер. |  

#### определение ключа content_scripts  

| Раздел | Сведения |  
|:--- |:---- |  
| `matches` \ (обязательно) | Шаблон URL-адреса для сопоставления перед загрузкой сценария содержимого. |  
| `js` | Сценарий, который должен быть загружен на совпадающие URL-адреса. |  
| `run_at` | Указывает, где были добавлены файлы JavaScript из `js` ключа. |  

Затем необходимо создать [фоновый сценарий][MDNAnatomyExtensionBackgroundScripts].  Фоновые сценарии выполняются в фоновом режиме браузера, не загружаются независимо от времени существования веб-страницы или окна браузера, и смогут общаться с помощью сценариев содержимого.  

В своей `js` папке создайте файл с именем `background.js` и добавьте следующий код.  

```javascript
// listen for sendMessage() from content script
browser.runtime.onMessage.addListener(
    function (request, sender, sendResponse) {
        // set the icon for the browser action from sendMessage() in content script
        browser.browserAction.setIcon({
            path: {
                "20": request.iconPath20,
                "40": request.iconPath40
            },
            tabId: sender.tab.id
        });
        // disable browser action for the current tab
        browser.browserAction.disable(sender.tab.id);
    });
```  

Метод [Runtime. onmessage][MDNApiRuntimeOnmessage] осуществляет прослушивание для [Runtime. SendMessage ()][MDNApiRuntimeSendmessage] в скрипте содержимого.  Если домен страницы не [docs.Microsoft.com][MicrosoftDocs], метод [browserAction. setIcon ()][MDNApiBrowseractionSeticon] задает пути к значкам для неактивных изображений.  

Кроме того, сценарий отключает действие браузера \ ([browserAction. Disable][MDApiBrowseractionDisable]\), чтобы пользователи не могли щелкнуть действие браузера за пределами страницы [docs.Microsoft.com][MicrosoftDocs] .  

Вы должны добавить фоновый сценарий в файл [manifest. JSON][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] .  Добавьте `background` в манифест следующий раздел.  

```json
"background": {
    "scripts": ["js/background.js"],
    "persistent": true
  }
```  

### Определение ключа манифеста  

| Раздел | Сведения|  
|:--- |:--- |  
| [фон][MDNManifestjsonBackground] | В этом разделе содержатся фоновые сценарии. |  

#### определения фоновых ключей  

| Раздел | Сведения |  
|:--- |:--- |  
| `scripts` | Путь к файлу JavaScript. |  
| `persistent` (обязательно) | Это значение должно быть равно `true` или `false` .  Если задано значение `true` , фоновый сценарий загружается и сохраняется для всего раздела просмотра.  Если задано значение `false` , фоновый сценарий загружается с задержкой и сохраняется для сеанса просмотра. |  

Перезагрузите расширение и протестируйте еще раз.  Чтобы перезагрузить расширение, нажмите кнопку " **...** " для настройки и других параметров в Microsoft EDGE, **выберите расширения**, щелкните расширение \ (**сменщик цветов**) и нажмите кнопку " **загрузить расширение**".  

Теперь откройте новую вкладку или обновите существующую, а не [docs.Microsoft.com][MicrosoftDocs] страницу.  Вы увидите значок "Неактивный" и не сможете выбрать действие браузера.  

Поздравляем!  Вы создали расширение Microsoft Edge!  Просмотр [полного примера в GitHub][GithubMicrosoftEdgeExtensionsDemosColorChanger].  Продолжайте читать, чтобы узнать больше о расширениях.  

## Написание более сложного расширения  

Хотите написать более сложное расширение?  Взгляните на расширение Beastify на MDN в статье, [второе расширение][MDNYourSecondWebextension].  Модель расширения для Microsoft Edge немного отличается от модели расширения для Firefox, так как расширение Beastify, созданное во [втором расширении][MDNYourSecondWebextension] , было адаптировано для работы в Microsoft Edge.  Посмотрите, есть ли вы на [GitHub][GithubMicrosoftEdgeExtensionsDemosBeastify].  

Просматривая статью в MDN, [второе расширение][MDNYourSecondWebextension], имейте в виду следующие разделы.  

### Интерфейсы API  

Список поддерживаемых API расширений в Microsoft Edge вы видите на странице [Поддерживаемые интерфейсы API][ExtensionsAPIsupportApis] .  

### Размеры значков  

Предпочтительные размеры значков расширений для Microsoft Edge: `20px` ,, `25px` `30px` и `40px` .  Другие поддерживаемые размеры: `19px` , `35px` и `38px` .  Дополнительные сведения о размерах значков и рекомендуемых практических рекомендациях можно найти в руководстве по [проектированию][ExtensionsGuidesDesign] .  

### JavaScript  

Модель расширения для Microsoft EDGE не поддерживает JavaScript.  Вместо этого используйте обратные вызовы.  Подробнее о том, как использовать обратные вызовы в расширении, можно найти в демонстрационных примерах [быстрой печати][GithubMicrosoftEdgeExtensionsDemosQuickPrint] и [замены текста][GithubMicrosoftEdgeExtensionsDemosTextSwap] .  

Рассмотрим пример [быстрой печати][GithubMicrosoftEdgeExtensionsDemosQuickPrint] в следующем видео.  

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Adding-a-Background-Script-to-you-Edge-Extension/player]  

### Manifest. JSON  

*   Этот `author` ключ требуется в Microsoft Edge  
*   Этот `activeTab` ключ не поддерживается в Microsoft Edge  

Дополнительные сведения о [расширениях браузеров][MDNBrowserExtensions]можно найти в [MDN веб-документах][MDNWebDocs].  

<!-- image links -->  

<!--[ImageColorChangerHeader]: ../media/color-changer_header.png "Docs.microsoft.com body changed to blue"  -->  
<!--[ImageColorChangerPopup]: ../media/color-changer_popup.png "The pop-up interface of the extension"  -->  
<!--[ImageColorChangerHeaderAliceblue]: ../media/color-changer_header_aliceblue.png "[Docs.microsoft.com header changed to Aliceblue"  -->  
<!--[ImageColorChangerHeaderCornsilk]: ../media/color-changer_header_cornsilk.png "Docs.microsoft.com header changed to Cornsilk"  -->  

<!-- links -->  

[ExtensionsGuidesAddingRemovingExtensionsAdding]: ./adding-and-removing-extensions.md#adding-an-extension "Добавление расширения, перемещение и удаление расширений для Microsoft Edge | Документы Microsoft"  
[ExtensionsGuidesDebuggingExtensions]: ./debugging-extensions.md "Отладка расширений | Документы Microsoft"  
[ExtensionsGuidesDesign]: ./design.md "Рекомендации по проектированию для расширений Microsoft Edge | Документы Microsoft"  
[ExtensionsGuidesDesignIcons]: ./design.md#icons "Значки — руководство по проектированию для расширений Microsoft Edge | Документы Microsoft"  
[ExtensionsAPIsupportApis]: ../api-support/supported-apis.md "Поддерживаемые API | Документы Microsoft"  
[ExtensionsApisupportManifestKeys]: ../api-support/supported-manifest-keys.md "Поддерживаемые ключи манифеста | Документы Microsoft"  

[MicrosoftDocs]: https://docs.microsoft.com "Документы Microsoft"  

[MDNWebDocs]: https://developer.mozilla.org "MDN веб-документы"  
[MDNBrowserExtensions]: https://developer.mozilla.org/Add-ons/WebExtensions "Расширения браузера | MDN"  
[MDNAnatomyExtension]: https://developer.mozilla.org/Add-ons/WebExtensions/Anatomy_of_a_WebExtension "Анатомия расширения | MDN"  
[MDNAnatomyExtensionBackgroundScripts]: https://developer.mozilla.org/Add-ons/WebExtensions/Anatomy_of_a_WebExtension#Background_scripts "Фоновые сценарии — Анатомия расширения | MDN"  
[MDApiBrowseractionDisable]: https://developer.mozilla.org/Add-ons/WebExtensions/API/browserAction/disable "browserAction. Disable ()-API | MDN" 
[MDNApiBrowseractionSeticon]: https://developer.mozilla.org/Add-ons/WebExtensions/API/browserAction/setIcon "browserAction. setIcon ()-API | MDN"  
[MDNApiRuntimeOnmessage]: https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/onmessage "Runtime. onmessage-API | MDN"  
[MDNApiRuntimeSendmessage]: https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendMessage "Runtime. sendMessage ()-API | MDN"  
[MDNApiTabs]: https://developer.mozilla.org/Add-ons/WebExtensions/API/tabs "Табуляция — API | MDN"  
[MDNApiTabsInsertcss]: https://developer.mozilla.org/Add-ons/WebExtensions/API/tabs/insertCSS "Табуляторы. insertCSS ()-API | MDN"  
[MDNContentScripts]: https://developer.mozilla.org/Add-ons/WebExtensions/Content_scripts "Сценарии содержимого | MDN"  
[MDNManifestjsonAuthor]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/author "Author-manifest. JSON | MDN"  
[MDNManifestjsonBackground]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/background "Background-manifest. JSON | MDN"  
[MDNManifestjsonBrowserAction]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/browser_action "browser_action-manifest. JSON | MDN"  
[MDNManifestjsonContentScripts]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/content_scripts "content_scripts-manifest. JSON | MDN"  
[MDNManifestjsonDescription]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/description "Описание-manifest. JSON | MDN"  
[MDNManifestjsonIcons]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/icons "значки — manifest. JSON | MDN"  
[MDNManifestjsonName]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/name "Name-manifest. JSON | MDN"  
[MDNManifestjsonPermissions]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/permissions "разрешения-manifest. JSON | MDN"  
[MDNManifestjsonVersion]: https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/version "Версия-manifest. JSON | MDN"  
[MDNYourSecondWebextension]: https://developer.mozilla.org/Add-ons/WebExtensions/Your_second_WebExtension "Второе расширение | MDN"  

[Bing]: https://www.bing.com "Закончил"  

[GithubMicrosoftEdgeExtensionsDemosBeastify]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/beastify_edge "Beastify-MicrosoftEdge/MicrosoftEdge-Extensions-демоны | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosColorChanger]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/color_changer "Сменщик цветов — MicrosoftEdge/MicrosoftEdge-Extensions-демоны | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosColorChangerImages]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/color_changer/images "Images — сменщика цветов — MicrosoftEdge/MicrosoftEdge-Extensions-демоны | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/blob/master/color_changer/manifest.json "Manifest. JSON — сменщик цветов — MicrosoftEdge/MicrosoftEdge-Extensions-демоны | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosQuickPrint]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/quick_print "Быстрая печать — MicrosoftEdge/MicrosoftEdge-Extensions-демоны | GitHub"  
[GithubMicrosoftEdgeExtensionsDemosTextSwap]: https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/text_swap "Text swap-MicrosoftEdge/MicrosoftEdge-Extensions-демоны | GitHub"  
