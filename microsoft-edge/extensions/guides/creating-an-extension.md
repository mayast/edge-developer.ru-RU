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
# <span data-ttu-id="7ac1d-104">Создание расширения Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7ac1d-104">Creating A Microsoft Edge Extension</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="7ac1d-105">В этом руководстве рассказывается, как создать расширение для Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-105">In this guide, learn to create an extension for Microsoft Edge.</span></span>  <span data-ttu-id="7ac1d-106">Этот пример расширения позволяет управлять определенными CSS для [docs.Microsoft.com][MicrosoftDocs] страниц, включая процесс создания файла манифеста, пользовательского интерфейса и сценариев фона и содержимого.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-106">This example extension allows you to manipulate specific CSS for [docs.microsoft.com][MicrosoftDocs] pages including walking you through creation of a manifest file, the user interface, and background and content scripts.</span></span>  

:::image type="complex" source="../media/color-changer_header.png" alt-text="Docs.microsoft.com текст изменился на синий":::
   <span data-ttu-id="7ac1d-108">Docs.microsoft.com текст изменился на синий</span><span class="sxs-lookup"><span data-stu-id="7ac1d-108">Docs.microsoft.com body changed to blue</span></span>
:::image-end:::

<!--![Docs.microsoft.com body changed to blue][ImageColorChangerHeader]  -->  

<span data-ttu-id="7ac1d-109">В этом руководстве предполагается, что вы понимаете, что такое расширение браузера и как оно работает.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-109">This tutorial assumes you have basic understanding of what a browser extension is and how it work.</span></span>  <span data-ttu-id="7ac1d-110">Более подробное описание стандартных блоков для расширений можно найти в разделе [Анатомия расширения][MDNAnatomyExtension].</span><span class="sxs-lookup"><span data-stu-id="7ac1d-110">For more imformation about the building blocks for extensions, see [Anatomy of an extension][MDNAnatomyExtension].</span></span>  

<span data-ttu-id="7ac1d-111">Скачайте код для [полного примера на GitHub][GithubMicrosoftEdgeExtensionsDemosColorChanger].</span><span class="sxs-lookup"><span data-stu-id="7ac1d-111">Download the code for the [full sample on GitHub][GithubMicrosoftEdgeExtensionsDemosColorChanger].</span></span>  

## <span data-ttu-id="7ac1d-112">Создание файла манифеста</span><span class="sxs-lookup"><span data-stu-id="7ac1d-112">Building the manifest file</span></span>  

<span data-ttu-id="7ac1d-113">Для начала создайте каталог для расширения и назовите его `color-changer` .</span><span class="sxs-lookup"><span data-stu-id="7ac1d-113">To begin, create a directory for your extension and name it `color-changer`.</span></span>  

<span data-ttu-id="7ac1d-114">В `color-changer` папке создайте файл с именем `manifest.json` .</span><span class="sxs-lookup"><span data-stu-id="7ac1d-114">Inside the `color-changer` folder, create a file named `manifest.json`.</span></span>  <span data-ttu-id="7ac1d-115">`manifest.json`Файл является обязательным для всех расширений и предоставляет важную информацию для расширения, начиная от имени расширения до разрешений.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-115">The `manifest.json` file is required for all extensions and provides important information for the extension, ranging from the extension name to the permissions.</span></span>  

> [!NOTE] 
> <span data-ttu-id="7ac1d-116">В этом руководстве описаны все ключи манифеста, которые необходимо использовать в этом руководстве, но для списка поддерживаемых и рекомендуемых ключей манифестов — [Поддерживаемые ключи манифеста][ExtensionsApisupportManifestKeys].</span><span class="sxs-lookup"><span data-stu-id="7ac1d-116">This guide walks you through all the manifest keys you must use in this guide, but for a list of all supported and recommended manifest keys, see [Supported manifest keys][ExtensionsApisupportManifestKeys].</span></span>  

<span data-ttu-id="7ac1d-117">Внутри `manifest.json` добавьте следующий код.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-117">Inside `manifest.json`, add the following code.</span></span>  

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

### <span data-ttu-id="7ac1d-118">Определение ключа манифеста</span><span class="sxs-lookup"><span data-stu-id="7ac1d-118">Manifest key definitions</span></span>  

| <span data-ttu-id="7ac1d-119">Раздел</span><span class="sxs-lookup"><span data-stu-id="7ac1d-119">Key</span></span> | <span data-ttu-id="7ac1d-120">Сведения</span><span class="sxs-lookup"><span data-stu-id="7ac1d-120">Details</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="7ac1d-121">name</span><span class="sxs-lookup"><span data-stu-id="7ac1d-121">name</span></span>][MDNManifestjsonName] | <span data-ttu-id="7ac1d-122">Имя расширения.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-122">The name of the extension.</span></span>  |  
| [<span data-ttu-id="7ac1d-123">созданные</span><span class="sxs-lookup"><span data-stu-id="7ac1d-123">author</span></span>][MDNManifestjsonAuthor] | <span data-ttu-id="7ac1d-124">Автор расширения.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-124">The author of the extension.</span></span>  |  
| [<span data-ttu-id="7ac1d-125">version</span><span class="sxs-lookup"><span data-stu-id="7ac1d-125">version</span></span>][MDNManifestjsonVersion] | <span data-ttu-id="7ac1d-126">Номер версии расширения.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-126">The extension version number.</span></span>  |  
| [<span data-ttu-id="7ac1d-127">description</span><span class="sxs-lookup"><span data-stu-id="7ac1d-127">description</span></span>][MDNManifestjsonDescription] | <span data-ttu-id="7ac1d-128">Описание расширения, отображаемое в разделе "о программе" в меню "расширение" в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-128">The description of the extension displayed in the About section of the extension menu in Microsoft Edge.</span></span>  |  
| [<span data-ttu-id="7ac1d-129">правами</span><span class="sxs-lookup"><span data-stu-id="7ac1d-129">permissions</span></span>][MDNManifestjsonPermissions] | <span data-ttu-id="7ac1d-130">Массив строк, запрашивающих разрешение на расширение.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-130">An array of strings requesting permissions for the extension.</span></span>  <span data-ttu-id="7ac1d-131">Для расширения вы запрашиваете разрешения на просмотр веб-сайтов, которые посещаете \ ("вкладки" "), а также обновляют контент по URL-адресам, соответствующим" `*://docs.microsoft.com/*` ".</span><span class="sxs-lookup"><span data-stu-id="7ac1d-131">For your extension, you are requesting permissions to see the websites visited \("tabs"\) and to update content on URLs matching "`*://docs.microsoft.com/*`".</span></span>  |  
| [<span data-ttu-id="7ac1d-132">browser_action</span><span class="sxs-lookup"><span data-stu-id="7ac1d-132">browser_action</span></span>][MDNManifestjsonBrowserAction] | <span data-ttu-id="7ac1d-133">Содержат сведения о значке.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-133">Contains the information for an icon.</span></span> <span data-ttu-id="7ac1d-134">Значок будет размещен на панели инструментов Microsoft Edge справа от адресной строки.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-134">The icon is placed on the Microsoft Edge toolbar, to the right of the address bar.</span></span>  |  

#### <span data-ttu-id="7ac1d-135">определение ключа browser_action</span><span class="sxs-lookup"><span data-stu-id="7ac1d-135">browser_action Key definitions</span></span>  

| <span data-ttu-id="7ac1d-136">Раздел</span><span class="sxs-lookup"><span data-stu-id="7ac1d-136">Key</span></span> | <span data-ttu-id="7ac1d-137">Сведения</span><span class="sxs-lookup"><span data-stu-id="7ac1d-137">Details</span></span> |  
|:--- |:--- |  
| `default_icon` | <span data-ttu-id="7ac1d-138">Значок, который используется на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-138">The icon that is used in the toolbar.</span></span>  |  
| `default_title` | <span data-ttu-id="7ac1d-139">Текст, который отображается, когда пользователь наводит указатель мыши на значок на панели инструментов.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-139">The text that is displayed when a user hovers over the icon in the toolbar.</span></span>  |  
| `default_popup` | <span data-ttu-id="7ac1d-140">Путь к файлу HTML всплывающего окна.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-140">The path to the HTML file for the pop-up window.</span></span>  |  

<span data-ttu-id="7ac1d-141">Теперь, когда вы создали файл манифеста, вам понадобится пользовательский интерфейс для расширения.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-141">Now that you have created the manifest file, you need a user interface for the extension.</span></span>  

## <span data-ttu-id="7ac1d-142">Создание всплывающего окна</span><span class="sxs-lookup"><span data-stu-id="7ac1d-142">Creating the pop-up</span></span>  

<span data-ttu-id="7ac1d-143">Для расширения создайте всплывающее окно для пользовательского интерфейса, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-143">For your extension, create a pop-up for the user interface, like below.</span></span>  

:::image type="complex" source="../media/color-changer_popup.png" alt-text="Всплывающий интерфейс расширения":::
   <span data-ttu-id="7ac1d-145">Всплывающий интерфейс расширения</span><span class="sxs-lookup"><span data-stu-id="7ac1d-145">The pop-up interface of the extension</span></span>
:::image-end:::

<!--![The pop-up interface of the extension][ImageColorChangerPopup]  -->  

<span data-ttu-id="7ac1d-146">Создайте файл с именем `popup.html` в корне `color-changer` папки.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-146">Create a file named `popup.html` in the root of your `color-changer` folder.</span></span>  <span data-ttu-id="7ac1d-147">Вставьте следующий код в `popup.html` .</span><span class="sxs-lookup"><span data-stu-id="7ac1d-147">Paste the following code into `popup.html`.</span></span>  

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

<span data-ttu-id="7ac1d-148">В `popup.html` необходимо создать заголовок, абзац и три кнопки \ (AliceBlue, Cornsilk и Reset \).</span><span class="sxs-lookup"><span data-stu-id="7ac1d-148">In `popup.html`, you create a title, a paragraph, and three buttons \(Aliceblue, Cornsilk, and Reset\).</span></span>  

<span data-ttu-id="7ac1d-149">Теперь создайте папку с именем `css` и внутри нее `styles.css` .</span><span class="sxs-lookup"><span data-stu-id="7ac1d-149">Now create a folder named `css` and inside create a file named `styles.css`.</span></span>  <span data-ttu-id="7ac1d-150">Добавьте стили ниже.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-150">Add the styles below.</span></span>  

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

<span data-ttu-id="7ac1d-151">Этот CSS обеспечивает расширение некоторых основных стилей.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-151">This CSS gives our extension some basic styles.</span></span>  <span data-ttu-id="7ac1d-152">Вы можете добавить дополнительные стили, чтобы настроить расширение.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-152">Feel free to add more styles to customize your extension.</span></span>  

<span data-ttu-id="7ac1d-153">Затем необходимо создать файл JavaScript, который будет взаимодействовать с всплывающим окном.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-153">Next, you must create the JavaScript file that interacts with the pop-up.</span></span>  <span data-ttu-id="7ac1d-154">Создание `js` папки и файла с именем " `popup.js` внутри".</span><span class="sxs-lookup"><span data-stu-id="7ac1d-154">Create a `js` folder and a file named `popup.js` inside.</span></span>  <span data-ttu-id="7ac1d-155">Обновите `popup.js` с помощью следующего кода.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-155">Update `popup.js` with the following code.</span></span>  

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

<span data-ttu-id="7ac1d-156">В `popup.js` API-интерфейсе [вкладок][MDNApiTabs] можно взаимодействовать с вкладками браузера и внедрять сценарии и стили в содержимое страницы.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-156">In `popup.js`, the [tabs][MDNApiTabs] API allows you to interact with the tabs of the browser and inject script and styles into the page content.</span></span>  <span data-ttu-id="7ac1d-157">С помощью метода [Табуляторы. insertCSS ()][MDNApiTabsInsertcss] вы вставляете на страницу УКАЗАННУЮ таблицу стилей, которая изменяет цвет заголовка [docs.Microsoft.com][MicrosoftDocs] на другой при нажатии указанной кнопки.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-157">Using the [tabs.insertCSS()][MDNApiTabsInsertcss] method, you inject the specified CSS into the page which changes the header on [docs.microsoft.com][MicrosoftDocs] to a different color when the specified button is clicked.</span></span>  

<span data-ttu-id="7ac1d-158">Теперь, когда у вас есть основные функциональные возможности всплывающего окна, добавьте в расширение значки.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-158">Now that you have the basic pop-up functionality, add icons to the extension.</span></span>  

## <span data-ttu-id="7ac1d-159">Добавление значков</span><span class="sxs-lookup"><span data-stu-id="7ac1d-159">Adding icons</span></span>  

<span data-ttu-id="7ac1d-160">Значки используются для представления расширения на панели инструментов браузера, в меню "расширения" и в других местах.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-160">Icons are used to represent the extension in the browser toolbar, the extensions menu, and other places.</span></span>  <span data-ttu-id="7ac1d-161">Скачайте [значки для расширения в GitHub][GithubMicrosoftEdgeExtensionsDemosColorChangerImages].</span><span class="sxs-lookup"><span data-stu-id="7ac1d-161">Download the [icons for your extension on GitHub][GithubMicrosoftEdgeExtensionsDemosColorChangerImages].</span></span> <span data-ttu-id="7ac1d-162">Дополнительные сведения о значках расширений в Microsoft EDGE можно найти в разделе [руководство по проектированию][ExtensionsGuidesDesignIcons].</span><span class="sxs-lookup"><span data-stu-id="7ac1d-162">For more information about extension icons in Microsoft Edge, see [Design Guide][ExtensionsGuidesDesignIcons].</span></span>  

<span data-ttu-id="7ac1d-163">После того как вы загрузили значки расширений, сохраните значки в `images` папке внутри нее `color-changer` .</span><span class="sxs-lookup"><span data-stu-id="7ac1d-163">After you download the extension icons, save the icons in an `images` folder inside `color-changer`.</span></span>  

<span data-ttu-id="7ac1d-164">Значок, который отображается на панели инструментов, задается в `default_icon` разделе [browser_action][MDNManifestjsonBrowserAction] , который вы уже добавили в файл манифеста в более ранних разделах.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-164">The icon that appears in the toolbar is set using `default_icon` inside of the [browser_action][MDNManifestjsonBrowserAction] key, which you already added to your manifest file in an earlier section.</span></span>  

<span data-ttu-id="7ac1d-165">`icons`Ключ определяет, какие значки следует использовать в меню "параметры расширений".</span><span class="sxs-lookup"><span data-stu-id="7ac1d-165">The `icons` key defines which icons should be used in the Extensions settings menus.</span></span>  <span data-ttu-id="7ac1d-166">Ниже показано, как задать несколько значков с разными размерами для учета различных разрешений экрана.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-166">Below, you are specifying multiple icons with different sizes to account for different screen resolutions.</span></span>  <span data-ttu-id="7ac1d-167">Имена значков `25` и `48` Высота значков в пикселях.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-167">The name of the icons, `25` and `48` are the heights in pixels of the icons.</span></span>  

<span data-ttu-id="7ac1d-168">В файле [manifest. JSON][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] включите в него ключ верхнего уровня `icons` .</span><span class="sxs-lookup"><span data-stu-id="7ac1d-168">In the [manifest.json][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] file, include a top-level key for `icons`.</span></span>  

```json
  "icons": {
    "25": "images/color-changer25.png",
    "48": "images/color-changer48.png"
  }
```  

### <span data-ttu-id="7ac1d-169">Определение ключа манифеста</span><span class="sxs-lookup"><span data-stu-id="7ac1d-169">Manifest Key definitions</span></span>  

| <span data-ttu-id="7ac1d-170">Раздел</span><span class="sxs-lookup"><span data-stu-id="7ac1d-170">Key</span></span> | <span data-ttu-id="7ac1d-171">Сведения</span><span class="sxs-lookup"><span data-stu-id="7ac1d-171">Details</span></span> |  
|:--- |:--- |  
| [<span data-ttu-id="7ac1d-172">значки</span><span class="sxs-lookup"><span data-stu-id="7ac1d-172">icons</span></span>][MDNManifestjsonIcons] | <span data-ttu-id="7ac1d-173">Значки для расширения с парами "ключ-значение" размера изображения `px` и путем изображения относительно корневого каталога расширения.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-173">The icons for your extension with key-value pairs of image size in `px` and image path relative to the root directory of the extension.</span></span> |  

> [!NOTE]
> <span data-ttu-id="7ac1d-174">С помощью значков, указанных `inactive##.png` в папке Images ниже, в этом руководстве.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-174">Use the icons named `inactive##.png` located in the images folder later in this guide.</span></span>  

## <span data-ttu-id="7ac1d-175">Проверка расширения</span><span class="sxs-lookup"><span data-stu-id="7ac1d-175">Testing the extension</span></span>  

<span data-ttu-id="7ac1d-176">Теперь, когда вы добавили пользовательский интерфейс и создали значки, проверьте расширение.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-176">Now that you have added the user interface and created icons, test your extension.</span></span>  <span data-ttu-id="7ac1d-177">Пошаговые инструкции по [добавлению расширения][ExtensionsGuidesAddingRemovingExtensionsAdding] в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-177">Walk through the steps for [Adding an extension][ExtensionsGuidesAddingRemovingExtensionsAdding] to Microsoft Edge.</span></span>  <span data-ttu-id="7ac1d-178">Затем вернитесь к этому руководству.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-178">Afterwards, return to this guide.</span></span>  

<span data-ttu-id="7ac1d-179">После добавления расширения перейдите на любую страницу [docs.Microsoft.com][MicrosoftDocs] .</span><span class="sxs-lookup"><span data-stu-id="7ac1d-179">After you add your extension, navigate to any [docs.microsoft.com][MicrosoftDocs] page.</span></span>  <span data-ttu-id="7ac1d-180">После нажатия на действие браузера появится следующее всплывающее окно.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-180">You should see the following pop-up after clicking on the browser action.</span></span>  <span data-ttu-id="7ac1d-181">Цвет основного текста [docs.Microsoft.com][MicrosoftDocs] также должен изменить цвет.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-181">The color of the [docs.microsoft.com][MicrosoftDocs] body should also change color.</span></span>  

:::row:::
   :::column span="1":::
      :::image type="complex" source="../media/color-changer_header_aliceblue.png" alt-text="Заголовок Docs.microsoft.com изменен на AliceBlue":::
         <span data-ttu-id="7ac1d-183">Заголовок Docs.microsoft.com изменен на AliceBlue</span><span class="sxs-lookup"><span data-stu-id="7ac1d-183">Docs.microsoft.com header changed to Aliceblue</span></span> :::image-end:::
      
      <!--![Docs.microsoft.com header changed to Aliceblue][ImageColorChangerHeaderAliceblue]  -->
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="../media/color-changer_header_cornsilk.png" alt-text="Заголовок Docs.microsoft.com изменен на Cornsilk":::
         <span data-ttu-id="7ac1d-185">Заголовок Docs.microsoft.com изменен на Cornsilk</span><span class="sxs-lookup"><span data-stu-id="7ac1d-185">Docs.microsoft.com header changed to Cornsilk</span></span> :::image-end:::
      
      <!--![Docs.microsoft.com header changed to Cornsilk][ImageColorChangerHeaderCornsilk]  -->
   :::column-end:::
:::row-end:::

<span data-ttu-id="7ac1d-186">Если вы столкнулись с ошибками или неработоспособными функциями, ознакомьтесь с руководством по [расширениям отладки][ExtensionsGuidesDebuggingExtensions] или Скачайте [полный пример в GitHub][GithubMicrosoftEdgeExtensionsDemosColorChanger].</span><span class="sxs-lookup"><span data-stu-id="7ac1d-186">If you encounter any errors or functionality that does not work, see the [Debugging extensions][ExtensionsGuidesDebuggingExtensions] guide or download the [full sample on GitHub][GithubMicrosoftEdgeExtensionsDemosColorChanger].</span></span>  

## <span data-ttu-id="7ac1d-187">Добавление содержимого и фоновых сценариев</span><span class="sxs-lookup"><span data-stu-id="7ac1d-187">Adding content and background scripts</span></span>  

<span data-ttu-id="7ac1d-188">Чтобы отключить расширение работы со страницами за пределами домена [docs.Microsoft.com][MicrosoftDocs] , перейдите на один шаг вперед и добавьте логику.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-188">Go one step further and add logic to disable the extension from working on pages outside the [docs.microsoft.com][MicrosoftDocs] domain.</span></span>  

<span data-ttu-id="7ac1d-189">Сначала необходимо создать [сценарий содержимого][MDNContentScripts].</span><span class="sxs-lookup"><span data-stu-id="7ac1d-189">You must first create a [content script][MDNContentScripts].</span></span>  <span data-ttu-id="7ac1d-190">Затем необходимо создать скрипты содержимого, которые выполняются в контексте определенной веб-страницы, и получить доступ к содержимому веб-страницы и взаимодействовать с фоновыми сценариями.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-190">Next, you must create content scripts that run in the context of a particular web page, are able to access the content of a web page, and are able to communicate with background scripts.</span></span>  <span data-ttu-id="7ac1d-191">В `js` каталоге создайте файл с именем `content.js` и добавьте следующий код.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-191">Inside of your `js` directory, create a file named `content.js` and add the following code.</span></span>  

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

<span data-ttu-id="7ac1d-192">Этот сценарий получает URL-адрес текущей страницы `document.location.href` и проверяет, находится ли текущая страница в домене [docs.Microsoft.com][MicrosoftDocs] .</span><span class="sxs-lookup"><span data-stu-id="7ac1d-192">This script gets the URL of the current page through `document.location.href` and verifies whether the current page is on the [docs.microsoft.com][MicrosoftDocs] domain.</span></span>  <span data-ttu-id="7ac1d-193">Если страница не находится в домене [docs.Microsoft.com][MicrosoftDocs] \ (например, [https://www.bing.com/][|::ref1::|] \), пути к неактивным значкам \ (Затененные значки \) отправляются в фоновый сценарий с помощью [среды выполнения. SendMessage ()][MDNApiRuntimeSendmessage].</span><span class="sxs-lookup"><span data-stu-id="7ac1d-193">If the page is not on the [docs.microsoft.com][MicrosoftDocs] domain \(for example  [https://www.bing.com/][|::ref1::|]\), the paths to the inactive icons \(grayed out icons\) are sent to the background script using [runtime.sendMessage()][MDNApiRuntimeSendmessage].</span></span>  

<span data-ttu-id="7ac1d-194">Вы должны обновить файл [manifest. JSON][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] , добавив в него следующий `content_scripts` раздел.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-194">You must update the [manifest.json][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] file to include the following `content_scripts` key.</span></span>  

```json
  "content_scripts": [{
    "matches": [
        "<all_urls>"
    ],
    "js": ["js/content.js"],
    "run_at": "document_end"
}]
```  

### <span data-ttu-id="7ac1d-195">Определение ключа манифеста</span><span class="sxs-lookup"><span data-stu-id="7ac1d-195">Manifest Key definitions</span></span>  

| <span data-ttu-id="7ac1d-196">Раздел</span><span class="sxs-lookup"><span data-stu-id="7ac1d-196">Key</span></span> | <span data-ttu-id="7ac1d-197">Сведения</span><span class="sxs-lookup"><span data-stu-id="7ac1d-197">Details</span></span> |  
|:--- |:---- |  
| [<span data-ttu-id="7ac1d-198">content_scripts</span><span class="sxs-lookup"><span data-stu-id="7ac1d-198">content_scripts</span></span>][MDNManifestjsonContentScripts] | <span data-ttu-id="7ac1d-199">Сведения о том, какие скрипты содержимого должен загружать браузер.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-199">Contains the information about which content scripts the browser should load.</span></span> |  

#### <span data-ttu-id="7ac1d-200">определение ключа content_scripts</span><span class="sxs-lookup"><span data-stu-id="7ac1d-200">content_scripts Key definitions</span></span>  

| <span data-ttu-id="7ac1d-201">Раздел</span><span class="sxs-lookup"><span data-stu-id="7ac1d-201">Key</span></span> | <span data-ttu-id="7ac1d-202">Сведения</span><span class="sxs-lookup"><span data-stu-id="7ac1d-202">Details</span></span> |  
|:--- |:---- |  
| `matches` <span data-ttu-id="7ac1d-203">\ (обязательно)</span><span class="sxs-lookup"><span data-stu-id="7ac1d-203">\(required\)</span></span> | <span data-ttu-id="7ac1d-204">Шаблон URL-адреса для сопоставления перед загрузкой сценария содержимого.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-204">The URL pattern to match prior to loading the content script.</span></span> |  
| `js` | <span data-ttu-id="7ac1d-205">Сценарий, который должен быть загружен на совпадающие URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-205">The script that should be loaded on matching URLs.</span></span> |  
| `run_at` | <span data-ttu-id="7ac1d-206">Указывает, где были добавлены файлы JavaScript из `js` ключа.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-206">Specifies where the JavaScript files from the `js` key are injected.</span></span> |  

<span data-ttu-id="7ac1d-207">Затем необходимо создать [фоновый сценарий][MDNAnatomyExtensionBackgroundScripts].</span><span class="sxs-lookup"><span data-stu-id="7ac1d-207">Next, you must create a [background script][MDNAnatomyExtensionBackgroundScripts].</span></span>  <span data-ttu-id="7ac1d-208">Фоновые сценарии выполняются в фоновом режиме браузера, не загружаются независимо от времени существования веб-страницы или окна браузера, и смогут общаться с помощью сценариев содержимого.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-208">Background scripts run in the background of the browser, run independently of the lifetime of a web page or browser window, and are able to communicate with content scripts.</span></span>  

<span data-ttu-id="7ac1d-209">В своей `js` папке создайте файл с именем `background.js` и добавьте следующий код.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-209">Inside of your `js` folder, create a file named `background.js` and add the following code.</span></span>  

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

<span data-ttu-id="7ac1d-210">Метод [Runtime. onmessage][MDNApiRuntimeOnmessage] осуществляет прослушивание для [Runtime. SendMessage ()][MDNApiRuntimeSendmessage] в скрипте содержимого.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-210">The [runtime.onMessage][MDNApiRuntimeOnmessage] method listens for [runtime.sendMessage()][MDNApiRuntimeSendmessage] from the content script.</span></span>  <span data-ttu-id="7ac1d-211">Если домен страницы не [docs.Microsoft.com][MicrosoftDocs], метод [browserAction. setIcon ()][MDNApiBrowseractionSeticon] задает пути к значкам для неактивных изображений.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-211">If the domain of the page is not [docs.microsoft.com][MicrosoftDocs], then [browserAction.setIcon()][MDNApiBrowseractionSeticon] method sets the icon paths to the inactive images.</span></span>  

<span data-ttu-id="7ac1d-212">Кроме того, сценарий отключает действие браузера \ ([browserAction. Disable][MDApiBrowseractionDisable]\), чтобы пользователи не могли щелкнуть действие браузера за пределами страницы [docs.Microsoft.com][MicrosoftDocs] .</span><span class="sxs-lookup"><span data-stu-id="7ac1d-212">The script also disables the browser action \([browserAction.disable][MDApiBrowseractionDisable]\), so that users are not able to click on the browser action outside of a [docs.microsoft.com][MicrosoftDocs] page.</span></span>  

<span data-ttu-id="7ac1d-213">Вы должны добавить фоновый сценарий в файл [manifest. JSON][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] .</span><span class="sxs-lookup"><span data-stu-id="7ac1d-213">You must add the background script to the [manifest.json][GithubMicrosoftEdgeExtensionsDemosColorChangerManifestjson] file.</span></span>  <span data-ttu-id="7ac1d-214">Добавьте `background` в манифест следующий раздел.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-214">Add the following `background` key to your manifest.</span></span>  

```json
"background": {
    "scripts": ["js/background.js"],
    "persistent": true
  }
```  

### <span data-ttu-id="7ac1d-215">Определение ключа манифеста</span><span class="sxs-lookup"><span data-stu-id="7ac1d-215">Manifest Key definitions</span></span>  

| <span data-ttu-id="7ac1d-216">Раздел</span><span class="sxs-lookup"><span data-stu-id="7ac1d-216">Key</span></span> | <span data-ttu-id="7ac1d-217">Сведения</span><span class="sxs-lookup"><span data-stu-id="7ac1d-217">Details</span></span>|  
|:--- |:--- |  
| [<span data-ttu-id="7ac1d-218">фон</span><span class="sxs-lookup"><span data-stu-id="7ac1d-218">background</span></span>][MDNManifestjsonBackground] | <span data-ttu-id="7ac1d-219">В этом разделе содержатся фоновые сценарии.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-219">Contains the background scripts.</span></span> |  

#### <span data-ttu-id="7ac1d-220">определения фоновых ключей</span><span class="sxs-lookup"><span data-stu-id="7ac1d-220">background Key definitions</span></span>  

| <span data-ttu-id="7ac1d-221">Раздел</span><span class="sxs-lookup"><span data-stu-id="7ac1d-221">Key</span></span> | <span data-ttu-id="7ac1d-222">Сведения</span><span class="sxs-lookup"><span data-stu-id="7ac1d-222">Details</span></span> |  
|:--- |:--- |  
| `scripts` | <span data-ttu-id="7ac1d-223">Путь к файлу JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-223">The path to a JavaScript file.</span></span> |  
| `persistent` <span data-ttu-id="7ac1d-224">(обязательно)</span><span class="sxs-lookup"><span data-stu-id="7ac1d-224">(required)</span></span> | <span data-ttu-id="7ac1d-225">Это значение должно быть равно `true` или `false` .</span><span class="sxs-lookup"><span data-stu-id="7ac1d-225">This must be set to `true` or `false`.</span></span>  <span data-ttu-id="7ac1d-226">Если задано значение `true` , фоновый сценарий загружается и сохраняется для всего раздела просмотра.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-226">If set to `true`, the background script is loaded and persists for the entire browsing section.</span></span>  <span data-ttu-id="7ac1d-227">Если задано значение `false` , фоновый сценарий загружается с задержкой и сохраняется для сеанса просмотра.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-227">If set to `false`, the background script is loaded with a delay and persists for the browsing session.</span></span> |  

<span data-ttu-id="7ac1d-228">Перезагрузите расширение и протестируйте еще раз.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-228">Reload your extension and test again.</span></span>  <span data-ttu-id="7ac1d-229">Чтобы перезагрузить расширение, нажмите кнопку " **...** " для настройки и других параметров в Microsoft EDGE, **выберите расширения**, щелкните расширение \ (**сменщик цветов**) и нажмите кнопку " **загрузить расширение**".</span><span class="sxs-lookup"><span data-stu-id="7ac1d-229">To reload your extension: click the **...** for settings and more in Microsoft Edge, click **Extensions**, click on your extension \(**Color Changer**\), and click **Reload extension**.</span></span>  

<span data-ttu-id="7ac1d-230">Теперь откройте новую вкладку или обновите существующую, а не [docs.Microsoft.com][MicrosoftDocs] страницу.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-230">Now, open a new tab or refresh an existing tab that is not a [docs.microsoft.com][MicrosoftDocs] page.</span></span>  <span data-ttu-id="7ac1d-231">Вы увидите значок "Неактивный" и не сможете выбрать действие браузера.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-231">You should see the inactive icon and not be able to click on the browser action.</span></span>  

<span data-ttu-id="7ac1d-232">Поздравляем!</span><span class="sxs-lookup"><span data-stu-id="7ac1d-232">Congratulations!</span></span>  <span data-ttu-id="7ac1d-233">Вы создали расширение Microsoft Edge!</span><span class="sxs-lookup"><span data-stu-id="7ac1d-233">You created an extension for Microsoft Edge!</span></span>  <span data-ttu-id="7ac1d-234">Просмотр [полного примера в GitHub][GithubMicrosoftEdgeExtensionsDemosColorChanger].</span><span class="sxs-lookup"><span data-stu-id="7ac1d-234">View the [full sample on GitHub][GithubMicrosoftEdgeExtensionsDemosColorChanger].</span></span>  <span data-ttu-id="7ac1d-235">Продолжайте читать, чтобы узнать больше о расширениях.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-235">Continue reading to learn more about extensions.</span></span>  

## <span data-ttu-id="7ac1d-236">Написание более сложного расширения</span><span class="sxs-lookup"><span data-stu-id="7ac1d-236">Writing a more complex extension</span></span>  

<span data-ttu-id="7ac1d-237">Хотите написать более сложное расширение?</span><span class="sxs-lookup"><span data-stu-id="7ac1d-237">Want to write a more complex extension?</span></span>  <span data-ttu-id="7ac1d-238">Взгляните на расширение Beastify на MDN в статье, [второе расширение][MDNYourSecondWebextension].</span><span class="sxs-lookup"><span data-stu-id="7ac1d-238">Take a look at the Beastify extension on MDN in the article, [Your second extension][MDNYourSecondWebextension].</span></span>  <span data-ttu-id="7ac1d-239">Модель расширения для Microsoft Edge немного отличается от модели расширения для Firefox, так как расширение Beastify, созданное во [втором расширении][MDNYourSecondWebextension] , было адаптировано для работы в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-239">The extension model for Microsoft Edge differs slightly from the extension model for Firefox, the Beastify extension created in [Your second extension][MDNYourSecondWebextension] was adapted to function in Microsoft Edge.</span></span>  <span data-ttu-id="7ac1d-240">Посмотрите, есть ли вы на [GitHub][GithubMicrosoftEdgeExtensionsDemosBeastify].</span><span class="sxs-lookup"><span data-stu-id="7ac1d-240">Check it out on [GitHub][GithubMicrosoftEdgeExtensionsDemosBeastify].</span></span>  

<span data-ttu-id="7ac1d-241">Просматривая статью в MDN, [второе расширение][MDNYourSecondWebextension], имейте в виду следующие разделы.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-241">While walking through the article on MDN, [Your second extension][MDNYourSecondWebextension], keep in mind the following sections.</span></span>  

### <span data-ttu-id="7ac1d-242">Интерфейсы API</span><span class="sxs-lookup"><span data-stu-id="7ac1d-242">APIs</span></span>  

<span data-ttu-id="7ac1d-243">Список поддерживаемых API расширений в Microsoft Edge вы видите на странице [Поддерживаемые интерфейсы API][ExtensionsAPIsupportApis] .</span><span class="sxs-lookup"><span data-stu-id="7ac1d-243">See the [Supported APIs][ExtensionsAPIsupportApis] page for a list of supported extensions APIs in Microsoft Edge.</span></span>  

### <span data-ttu-id="7ac1d-244">Размеры значков</span><span class="sxs-lookup"><span data-stu-id="7ac1d-244">Icon sizes</span></span>  

<span data-ttu-id="7ac1d-245">Предпочтительные размеры значков расширений для Microsoft Edge: `20px` ,, `25px` `30px` и `40px` .</span><span class="sxs-lookup"><span data-stu-id="7ac1d-245">Preferred extension icon sizes for Microsoft Edge are `20px`, `25px`, `30px`, and `40px`.</span></span>  <span data-ttu-id="7ac1d-246">Другие поддерживаемые размеры: `19px` , `35px` и `38px` .</span><span class="sxs-lookup"><span data-stu-id="7ac1d-246">Other supported sizes are `19px`, `35px`, and `38px`.</span></span>  <span data-ttu-id="7ac1d-247">Дополнительные сведения о размерах значков и рекомендуемых практических рекомендациях можно найти в руководстве по [проектированию][ExtensionsGuidesDesign] .</span><span class="sxs-lookup"><span data-stu-id="7ac1d-247">For more info on icon sizes and best practices, see the [Design][ExtensionsGuidesDesign] guide.</span></span>  

### <span data-ttu-id="7ac1d-248">JavaScript</span><span class="sxs-lookup"><span data-stu-id="7ac1d-248">JavaScript</span></span>  

<span data-ttu-id="7ac1d-249">Модель расширения для Microsoft EDGE не поддерживает JavaScript.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-249">The extension model for Microsoft Edge does not support JavaScript Promises.</span></span>  <span data-ttu-id="7ac1d-250">Вместо этого используйте обратные вызовы.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-250">Instead, use callbacks.</span></span>  <span data-ttu-id="7ac1d-251">Подробнее о том, как использовать обратные вызовы в расширении, можно найти в демонстрационных примерах [быстрой печати][GithubMicrosoftEdgeExtensionsDemosQuickPrint] и [замены текста][GithubMicrosoftEdgeExtensionsDemosTextSwap] .</span><span class="sxs-lookup"><span data-stu-id="7ac1d-251">For more examples of using callbacks in an extension, take a look at the  [Quick Print][GithubMicrosoftEdgeExtensionsDemosQuickPrint] and [Text Swap][GithubMicrosoftEdgeExtensionsDemosTextSwap] demos.</span></span>  

<span data-ttu-id="7ac1d-252">Рассмотрим пример [быстрой печати][GithubMicrosoftEdgeExtensionsDemosQuickPrint] в следующем видео.</span><span class="sxs-lookup"><span data-stu-id="7ac1d-252">Walk through the [Quick Print][GithubMicrosoftEdgeExtensionsDemosQuickPrint] example in the following video.</span></span>  

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Adding-a-Background-Script-to-you-Edge-Extension/player]  

### <span data-ttu-id="7ac1d-253">Manifest. JSON</span><span class="sxs-lookup"><span data-stu-id="7ac1d-253">Manifest.json</span></span>  

*   <span data-ttu-id="7ac1d-254">Этот `author` ключ требуется в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7ac1d-254">The `author` key is required in Microsoft Edge</span></span>  
*   <span data-ttu-id="7ac1d-255">Этот `activeTab` ключ не поддерживается в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7ac1d-255">The `activeTab` key is not supported in Microsoft Edge</span></span>  

<span data-ttu-id="7ac1d-256">Дополнительные сведения о [расширениях браузеров][MDNBrowserExtensions]можно найти в [MDN веб-документах][MDNWebDocs].</span><span class="sxs-lookup"><span data-stu-id="7ac1d-256">For more information on [Browser Extensions][MDNBrowserExtensions], see [MDN web docs][MDNWebDocs].</span></span>  

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
