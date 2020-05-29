---
description: Расширение "Начало работы", часть 1
title: Динамическое добавление изображения NASA под тегом текста страницы с помощью сценариев содержимого
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/08/2020
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: Edge — Chromium, Web Development, HTML, CSS, JavaScript, разработчик, расширения
ms.openlocfilehash: b37184f0188b72ec868ab3de3f2341c0694ee42c
ms.sourcegitcommit: 0bc1312a1e6a0ac37cf385201db4361fc05184fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/28/2020
ms.locfileid: "10683646"
---
# <span data-ttu-id="aaa3f-104">Динамическое добавление изображения NASA под тегом текста страницы с помощью сценариев содержимого</span><span class="sxs-lookup"><span data-stu-id="aaa3f-104">Dynamically Insert NASA Picture Below The Page Body Tag Using Content Scripts</span></span>  
  
[<span data-ttu-id="aaa3f-105">Источник пакета расширения для этой части завершен</span><span class="sxs-lookup"><span data-stu-id="aaa3f-105">Completed Extension Package Source for This Part</span></span>][ArchiveExtensionGettingStartedPart2]  

## <span data-ttu-id="aaa3f-106">Обзор</span><span class="sxs-lookup"><span data-stu-id="aaa3f-106">Overview</span></span>  

<span data-ttu-id="aaa3f-107">В части 2 Вы намерены обновить всплывающее меню таким образом, чтобы в нем не отображалось статическое изображение, которое вы раньше, но заменить это изображение заголовком и стандартной кнопкой HTML.</span><span class="sxs-lookup"><span data-stu-id="aaa3f-107">In part 2, you learn to update your pop-up menu to not show the static stars image you had before, but to replace that image with a title and a standard HTML button.</span></span>  <span data-ttu-id="aaa3f-108">Эта кнопка, если она выбрана, передает изображение звезды, внедренное в расширение, на страницу содержимого.</span><span class="sxs-lookup"><span data-stu-id="aaa3f-108">That button, when selected, passes that stars image, which is embedded in the Extension, to the content page.</span></span>  <span data-ttu-id="aaa3f-109">Это изображение будет вставлено на вкладку активного браузера.</span><span class="sxs-lookup"><span data-stu-id="aaa3f-109">That image, is inserted into the active browser tab.</span></span>  

*   <span data-ttu-id="aaa3f-110">Технологии расширения, описанные в этом руководстве</span><span class="sxs-lookup"><span data-stu-id="aaa3f-110">Extension technologies covered in this guide</span></span>  
    *   <span data-ttu-id="aaa3f-111">Добавление библиотек JavaScript в расширение</span><span class="sxs-lookup"><span data-stu-id="aaa3f-111">Injecting JavaScript libraries into Extension</span></span>  
    *   <span data-ttu-id="aaa3f-112">Предоставление расширений ресурсов вкладкам браузера</span><span class="sxs-lookup"><span data-stu-id="aaa3f-112">Exposing Extension assets to browser tabs</span></span>  
    *   <span data-ttu-id="aaa3f-113">Включение страниц содержимого на существующие вкладки браузера</span><span class="sxs-lookup"><span data-stu-id="aaa3f-113">Including content pages in existing browser tabs</span></span>  
    *   <span data-ttu-id="aaa3f-114">Прослушивание сообщений на страницах с содержимым из всплывающих окон и ответа на них</span><span class="sxs-lookup"><span data-stu-id="aaa3f-114">Having content pages listen for messages from pop-ups and respond</span></span>  

## <span data-ttu-id="aaa3f-115">Удаление изображения из всплывающего окна и замена его на кнопку</span><span class="sxs-lookup"><span data-stu-id="aaa3f-115">Remove the image from the pop-up and replace it with a button</span></span>  

<span data-ttu-id="aaa3f-116">Сначала обновите `popup.html` файл с помощью перенаправленной текстовой разметки, в которой отображается заголовок и кнопка.</span><span class="sxs-lookup"><span data-stu-id="aaa3f-116">First, update your `popup.html` file with some straight forward markup that displays a title and a button.</span></span>  <span data-ttu-id="aaa3f-117">Вы запрограммироване кнопку чуть ниже, но теперь просто включите ссылку на пустой файл JavaScript `popup.js` .</span><span class="sxs-lookup"><span data-stu-id="aaa3f-117">You program that button shortly, but for now, just include a reference to an empty JavaScript file `popup.js`.</span></span>  <span data-ttu-id="aaa3f-118">Вот обновление HTML.</span><span class="sxs-lookup"><span data-stu-id="aaa3f-118">Here is update HTML.</span></span>  

```html
<html>
    <head>
        <meta charset="utf-8" />
        <style>
            body {
                width: 500px;
            }
            button {
                background-color: #336dab;
                border: none;
                color: white;
                padding: 15px 32px;
                text-align: center;
                font-size: 16px;
            }
        </style>
    </head>
    <body>
        <h1>Show the NASA Picture of the Day</h1>
        <h2>(select the image to remove)</h2>
        <button id="sendmessageid">Display</button>
        <script src="popup.js"></script>
    </body>
</html>
```  

<span data-ttu-id="aaa3f-119">После того как вы обновите свое расширение и настроили значок запуска расширения, появится следующее всплывающее окно, содержащее кнопку отображения.</span><span class="sxs-lookup"><span data-stu-id="aaa3f-119">After updating your Extension and selecting the Extension launch icon, the have the following pop-up includes a display button.</span></span>  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="экран Popup. HTML после нажатия на значок расширения":::
   <span data-ttu-id="aaa3f-121">экран Popup. HTML после нажатия на значок расширения</span><span class="sxs-lookup"><span data-stu-id="aaa3f-121">popup.html display after pressing the Extension icon</span></span>
:::image-end:::

<!--![popup.html display after pressing the Extension icon][ImagePart2Popupdialog]  -->  

## <span data-ttu-id="aaa3f-122">Обновлена стратегия отображения изображения в верхней части вкладки браузера</span><span class="sxs-lookup"><span data-stu-id="aaa3f-122">Updated strategy to display image at the top of the browser tab</span></span>  

<span data-ttu-id="aaa3f-123">После добавления кнопки Следующая задача — сделать так, чтобы она выместит `images/stars.jpeg` файл изображения в верхней части активной вкладки.</span><span class="sxs-lookup"><span data-stu-id="aaa3f-123">After adding the button, the next task is to make it bring up the `images/stars.jpeg` image file at the top of the active tab page.</span></span>  

<span data-ttu-id="aaa3f-124">Помните, что каждая вкладка имеет уникальный собственный поток, и расширение имеет отдельный поток.</span><span class="sxs-lookup"><span data-stu-id="aaa3f-124">Remember, each tab page has a unique own thread and the Extension has a separate thread.</span></span>  <span data-ttu-id="aaa3f-125">Таким образом, необходимо сначала создать сценарий содержимого и внедрить этот сценарий содержимого на страницу вкладки.</span><span class="sxs-lookup"><span data-stu-id="aaa3f-125">So, you must first create a content script and inject that content script into the tab page.</span></span>  <span data-ttu-id="aaa3f-126">После этого вы должны отправить сообщение с помощью всплывающего окна на странице вкладки, в которой будет отображаться этот сценарий содержимого и как его отобразить.</span><span class="sxs-lookup"><span data-stu-id="aaa3f-126">Once you do that, you must send a message from your pop-up to that content script running on the tab page telling that content script what image to show, and how to show it.</span></span>  

## <span data-ttu-id="aaa3f-127">Создание всплывающего сценария JavaScript для отправки сообщения</span><span class="sxs-lookup"><span data-stu-id="aaa3f-127">Creating the pop-up JavaScript to send a message</span></span>  

<span data-ttu-id="aaa3f-128">Сначала нужно создать `popup/popup.js` и добавить код, чтобы отправить сообщение в несозданный сценарий содержимого, который вы должны создать и внедрить на вкладку браузера.  Для этого следующий код добавляет `onclick` событие в всплывающую кнопку отображения.</span><span class="sxs-lookup"><span data-stu-id="aaa3f-128">First, create `popup/popup.js` and add code to send a message to your not-yet-created content script that you must momentarily create and inject into your browser tab.  To do that, the following code adds an `onclick` event to your pop-up display button.</span></span>  

```javascript
const sendMessageId = document.getElementById("sendmessageid");
if (sendMessageId) {
  sendMessageId.onclick = function() {
    // do something
  };
}
```  

<span data-ttu-id="aaa3f-129">В `onclick` событии необходимо найти текущую вкладку браузера \ (если у вас есть только один из них, она будет находиться в одном случае).</span><span class="sxs-lookup"><span data-stu-id="aaa3f-129">In the `onclick` event, what you must do is find the current browser tab \(if there is only one open it is that one\).</span></span>  <span data-ttu-id="aaa3f-130">После того как вы найдете эту вкладку, используйте `chrome.tabs.sendmessage` API-интерфейс расширения для отправки сообщения на эту вкладку.</span><span class="sxs-lookup"><span data-stu-id="aaa3f-130">Then, once you find that tab, use the `chrome.tabs.sendmessage` Extension API to send a message to that tab.</span></span>  

<span data-ttu-id="aaa3f-131">В этом сообщении нужно добавить URL-адрес изображения, которое вы хотите отобразить, и вы хотите отправить уникальный идентификатор, который должен быть назначен этому вставленному изображению.</span><span class="sxs-lookup"><span data-stu-id="aaa3f-131">In that message you must include the URL to the image you want to display, and you want to send a unique ID that should be assigned to that inserted image.</span></span>  <span data-ttu-id="aaa3f-132">Вы можете выбрать, чтобы JavaScript мог создавать содержимое, но для более поздних причин создать этот уникальный идентификатор здесь `popup.js` и передать его в сценарий содержимого, который еще не создан.</span><span class="sxs-lookup"><span data-stu-id="aaa3f-132">You may choose to let the content insertion JavaScript generate that, but for reasons that become apparent later, generate that unique ID here in `popup.js` and pass it to the not-yet-created content script.</span></span>  

<span data-ttu-id="aaa3f-133">Обновленный `popup/popup.js` файл.</span><span class="sxs-lookup"><span data-stu-id="aaa3f-133">Here is your updated `popup/popup.js` file.</span></span>  <span data-ttu-id="aaa3f-134">Кроме того, вы можете передать текущий идентификатор табуляции, который вам понадобится в более позднем разделе, но пока не будет использован.</span><span class="sxs-lookup"><span data-stu-id="aaa3f-134">Also, pass in the current tab ID which you should need in a later section but for now, is not be used.</span></span>  

```javascript
const sendMessageId = document.getElementById("sendmessageid");
if (sendMessageId) {
    sendMessageId.onclick = function() {
        chrome.tabs.query({ active: true, currentWindow: true }, function(tabs) {
            chrome.tabs.sendMessage(
                tabs[0].id,
                {
                    url: chrome.extension.getURL("images/stars.jpeg"),
                    imageDivId: `${guidGenerator()}`,
                    tabId: tabs[0].id
                },
                function(response) {
                    window.close();
                }
            );
            function guidGenerator() {
                const S4 = function () {
                    return (((1 + Math.random()) * 0x10000) | 0).toString(16).substring(1);
                };
                return (S4() + S4() + "-" + S4() + "-" + S4() + "-" + S4() + "-" + S4() + S4() + S4());
            }
        });
    };
}
```  

## <span data-ttu-id="aaa3f-135">Создание звезд. JPEG, доступного на любой вкладке браузера</span><span class="sxs-lookup"><span data-stu-id="aaa3f-135">Making your stars.jpeg available from any browser tab</span></span>  

<span data-ttu-id="aaa3f-136">Возможно, вы захотите заинтересовать причины, по которым следует `images/stars.jpeg` использовать `chrome.extension.getURL` API расширения Chrome вместо того, чтобы просто передавать относительный URL-адрес без дополнительного префикса, как в предыдущем разделе.</span><span class="sxs-lookup"><span data-stu-id="aaa3f-136">You are probably wondering why, when you pass the `images/stars.jpeg` must you use the `chrome.extension.getURL` chrome Extension API instead of just passing in the relative URL without the extra prefix like in the previous section.</span></span>  <span data-ttu-id="aaa3f-137">Таким образом, этот дополнительный префикс, возвращаемый `getUrl` с подключенным изображением, выглядит примерно так, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="aaa3f-137">By the way, that extra prefix, returned by `getUrl` with the image attached looks something like the following.</span></span>  

```http
extension://inigobacliaghocjiapeaaoemkjifjhp/images/stars.jpeg
```  

<span data-ttu-id="aaa3f-138">Причина в том, что вы вставляете изображение с помощью `src` атрибута `img` элемента на странице содержимого.</span><span class="sxs-lookup"><span data-stu-id="aaa3f-138">The reason is that you are injecting the image using the `src` attribute of the `img` element into the content page.</span></span>  <span data-ttu-id="aaa3f-139">Страница содержимого выполняется в отдельном потоке, не совпадающем с потоком, на котором запущено расширение.</span><span class="sxs-lookup"><span data-stu-id="aaa3f-139">The content page is running on a unique thread that is not the same as the thread running the Extension.</span></span>  <span data-ttu-id="aaa3f-140">Для правильной работы вы должны предоставить статический файл изображения в качестве веб-актива.</span><span class="sxs-lookup"><span data-stu-id="aaa3f-140">You must expose the static image file as a web asset for it to work correctly.</span></span>  

<span data-ttu-id="aaa3f-141">Для этого необходимо добавить в файл еще одну запись `manifest.json` .</span><span class="sxs-lookup"><span data-stu-id="aaa3f-141">To do that, you must add another entry in the `manifest.json` file.</span></span>  <span data-ttu-id="aaa3f-142">Вы должны объявить изображение доступным на любом из вкладок браузера.  Этот параметр является следующим: \ (вы должны увидеть его в полном `manifest.json` файле ниже, когда вы добавите объявление сценария содержимого, которое появится на странице \).</span><span class="sxs-lookup"><span data-stu-id="aaa3f-142">You must declare the image to be accessible from any browser tab.  That entry is as follows \(you should see it in the full `manifest.json` file below when you add the content script declaration coming up\).</span></span>  

```json
"web_accessible_resources": [
    "images/*.jpeg"
]
```  

<span data-ttu-id="aaa3f-143">Теперь вы написали код в `popup.js` файле для отправки сообщения на страницу содержимого, внедренную на текущую активную вкладку, но вы не создали и не добавили эту страницу содержимого.</span><span class="sxs-lookup"><span data-stu-id="aaa3f-143">You have now written the code in your `popup.js` file to send a message to the content page that is embedded on the current active tab page, but you have not created and injected that content page.</span></span>  <span data-ttu-id="aaa3f-144">Сделайте это прямо сейчас.</span><span class="sxs-lookup"><span data-stu-id="aaa3f-144">Do that now.</span></span>  

## <span data-ttu-id="aaa3f-145">Обновление манифеста. JSON для контента и веб-доступа</span><span class="sxs-lookup"><span data-stu-id="aaa3f-145">Updating your manifest.json for content and web access</span></span>  

<span data-ttu-id="aaa3f-146">Обновленный `manifest.json` , который включает в себя `content-scripts` и `web_accessible_resources` следующий.</span><span class="sxs-lookup"><span data-stu-id="aaa3f-146">The updated `manifest.json` that includes the `content-scripts` and `web_accessible_resources` is as follows.</span></span>  

```json
{
    "name": "NASA Picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A Chromium Extension to show the NASA Picture of the Day.",
    "icons": {
        "16": "icons/nasapod16x16.png",
        "32": "icons/nasapod32x32.png",
        "48": "icons/nasapod48x48.png",
        "128": "icons/nasapod128x128.png"
    },
    "browser_action": {
        "default_popup": "popup/popup.html"
    },
    "content_scripts": [
        {
            "matches": [
              "<all_urls>"
            ],
            "js": ["lib/jquery.min.js","content-scripts/content.js"]
        }
    ],
    "web_accessible_resources": [
        "images/*.jpeg"
    ]
}
```  

<span data-ttu-id="aaa3f-147">Добавленный раздел `content_scripts` .</span><span class="sxs-lookup"><span data-stu-id="aaa3f-147">The section you added is `content_scripts`.</span></span>  <span data-ttu-id="aaa3f-148">Этот атрибут `matches` указывает на то `<all_urls>` , что все файлы, упомянутые в разделе " **content_scripts** ", вставляются во все вкладки браузера при загрузке каждой страницы.</span><span class="sxs-lookup"><span data-stu-id="aaa3f-148">The attribute `matches` set to `<all_urls>` means that all the files mention in the **content_scripts** section is injected into all browser tab pages when each are loaded.</span></span>  <span data-ttu-id="aaa3f-149">Допустимые типы файлов, которые можно внедрить здесь: JavaScript и CSS.</span><span class="sxs-lookup"><span data-stu-id="aaa3f-149">The allowable types of files that are able to be injected here are javascript and css.</span></span>  <span data-ttu-id="aaa3f-150">Кроме того, вы добавите `libjquery.min.js` .</span><span class="sxs-lookup"><span data-stu-id="aaa3f-150">You also added `libjquery.min.js`.</span></span>  <span data-ttu-id="aaa3f-151">Вы можете включить эти возможности из файла download, упомянутого в верхней части раздела.</span><span class="sxs-lookup"><span data-stu-id="aaa3f-151">You are able to include that from the download mentioned at the top of the section.</span></span>  

## <span data-ttu-id="aaa3f-152">Добавление jQuery и понимание связанного потока</span><span class="sxs-lookup"><span data-stu-id="aaa3f-152">Adding jQuery and understanding the associated thread</span></span>  

<span data-ttu-id="aaa3f-153">В сценариях содержимого, которые вы вставляете, спланируйте использование jQuery \ ( `$` \).</span><span class="sxs-lookup"><span data-stu-id="aaa3f-153">In the content scripts you are injecting, plan on using jQuery \(`$`\).</span></span>  <span data-ttu-id="aaa3f-154">Вы добавили версию minified для jQuery и помещаем ее в пакет расширения как `lib\jquery.min.js` .</span><span class="sxs-lookup"><span data-stu-id="aaa3f-154">You added a minified version of jQuery and put it in your Extension package as `lib\jquery.min.js`.</span></span>  <span data-ttu-id="aaa3f-155">Эти сценарии содержимого выполняются в отдельной изолированной среде сортировки, что означает, что jQuery, вставленный в `popup.js` страницу, не предоставляет доступ к содержимому.</span><span class="sxs-lookup"><span data-stu-id="aaa3f-155">These content scripts run in an individual sandbox of sorts, which means that the jQuery injected into the `popup.js` page does not share with the content.</span></span>  

<span data-ttu-id="aaa3f-156">Имейте в виду, что даже если на вкладке браузер запущен JavaScript на загруженной веб-странице, доступ к содержимому не имеет доступа.</span><span class="sxs-lookup"><span data-stu-id="aaa3f-156">Keep in mind that even if the browser tab has JavaScript running on it on the loaded web page, any content injected does not have access to that.</span></span>  <span data-ttu-id="aaa3f-157">Этот внедренный JavaScript просто имеет доступ к фактической загруженной модели DOM на вкладке "браузер".</span><span class="sxs-lookup"><span data-stu-id="aaa3f-157">That injected JavaScript just has access to the actual DOM loaded in that browser tab.</span></span>  

## <span data-ttu-id="aaa3f-158">Добавление прослушивателя сообщений сценария содержимого</span><span class="sxs-lookup"><span data-stu-id="aaa3f-158">Adding the content script message listener</span></span>  

<span data-ttu-id="aaa3f-159">Здесь показано, что `content-scripts\content.js` файл, который добавляется в каждую вкладку браузера на основе вашего `manifest.json` `content-scripts` раздела.</span><span class="sxs-lookup"><span data-stu-id="aaa3f-159">Here is that `content-scripts\content.js` file that gets injected into every browser tab page based on your `manifest.json` `content-scripts` section.</span></span>  

```javascript
chrome.runtime.onMessage.addListener(function(request, sender, sendResponse) {
    $("body").prepend(
        `<img  src="${request.url}" id="${request.imageDivId}"
               class="slide-image" /> `
    );
    $("head").prepend(
        `<style>
          .slide-image {
              height: auto;
              width: 100vw;
          }
        </style>`
    );
    $(`#${request.imageDivId}`).click(function() {
        $(`#${request.imageDivId}`).remove(`#${request.imageDivId}`);
    });
    sendResponse({ fromcontent: "This message is from content.js" });
});
```  

<span data-ttu-id="aaa3f-160">Обратите внимание, что все указанные выше сценарии JavaScript — это регистрация `listener` с помощью `chrome.runtime.onMessage.addListener` метода API расширения.</span><span class="sxs-lookup"><span data-stu-id="aaa3f-160">Notice that all the above JavaScript does is to register a `listener` using the `chrome.runtime.onMessage.addListener` Extension API method.</span></span>  <span data-ttu-id="aaa3f-161">Этот прослушиватель ждет сообщения, которые вы отправили ранее из `popup.js` описанных выше `chrome.tabs.sendMessage` методов расширения API.</span><span class="sxs-lookup"><span data-stu-id="aaa3f-161">This listener waits for messages like the one you sent from the `popup.js` described earlier with the `chrome.tabs.sendMessage` Extension API method.</span></span>  

<span data-ttu-id="aaa3f-162">Первый параметр `addListener` метода — это функция, первый параметр которой — Request, — сведения о переданном сообщении.</span><span class="sxs-lookup"><span data-stu-id="aaa3f-162">The first parameter of the `addListener` method is a function whose first parameter, request, is the details of the message being passed in.</span></span>  <span data-ttu-id="aaa3f-163">Не забывайте, что `popup.js` при использовании `sendMessage` метода эти атрибуты первого параметра — `url` и `imageDivId` .</span><span class="sxs-lookup"><span data-stu-id="aaa3f-163">Remember, from `popup.js`, when you used the `sendMessage` method, those attributes of the first parameter are `url` and `imageDivId`.</span></span>  

<span data-ttu-id="aaa3f-164">Если событие обрабатывается прослушивателем, выполняется функция, которая является первым параметром.</span><span class="sxs-lookup"><span data-stu-id="aaa3f-164">When an event is processed by the listener, the function that is the first parameter is run.</span></span>  <span data-ttu-id="aaa3f-165">Первый параметр этой функции — объект, которому назначены атрибуты `sendMessage` .</span><span class="sxs-lookup"><span data-stu-id="aaa3f-165">The first parameter of that function is an object that has attributes as assigned by `sendMessage`.</span></span>  <span data-ttu-id="aaa3f-166">Эта функция просто обрабатывает три строки сценария jQuery.</span><span class="sxs-lookup"><span data-stu-id="aaa3f-166">That function simply processes the three jQuery script lines.</span></span>  

*   <span data-ttu-id="aaa3f-167">Первый динамически вставляет в заголовок DOM **\<style\>** раздел, который необходимо назначить `slide-image` `img` элементу как класс.</span><span class="sxs-lookup"><span data-stu-id="aaa3f-167">The first dynamically inserts into the DOM header a **\<style\>** section that you must assign as a `slide-image` class to your `img` element.</span></span>  
*   <span data-ttu-id="aaa3f-168">Вторая — добавляет `img` элемент прямо под `body` вкладкой браузера, которому назначен класс, а также `slide-image` `imageDivId` как идентификатор этого элемента изображения.</span><span class="sxs-lookup"><span data-stu-id="aaa3f-168">The second, appends an `img` element right below the `body` of your browser tab that has the `slide-image` class assigned as well as the `imageDivId` as the ID of that image element.</span></span>  
*   <span data-ttu-id="aaa3f-169">Третья добавляет `click` событие, которое охватывает все изображение, позволяя пользователю выбрать место на изображении и удалить его из страницы \ (вместе с прослушивателем событий \).</span><span class="sxs-lookup"><span data-stu-id="aaa3f-169">The third adds a `click` event that covers the entire image allowing the user to select any place on the image and that image is be removed from the page \(along with it is event listener\).</span></span>  

## <span data-ttu-id="aaa3f-170">Добавление функции для удаления отображаемого изображения при выделении</span><span class="sxs-lookup"><span data-stu-id="aaa3f-170">Adding functionality to remove the displayed image when selected</span></span>  

<span data-ttu-id="aaa3f-171">Теперь при переходе на любую страницу и выборе значка **расширения** всплывающее меню отображается следующим образом.</span><span class="sxs-lookup"><span data-stu-id="aaa3f-171">Now, when you browse to any page and select your **Extension** icon, the pop-up menu is displayed as follows.</span></span>  

:::image type="complex" source="./media/part2-popupdialog.png" alt-text="экран Popup. HTML после нажатия на значок расширения":::
   <span data-ttu-id="aaa3f-173">экран Popup. HTML после нажатия на значок расширения</span><span class="sxs-lookup"><span data-stu-id="aaa3f-173">popup.html display after pressing the Extension icon</span></span>
:::image-end:::

<!--![popup.html display after pressing the Extension icon][ImagePart2Popupdialog]  -->  

<span data-ttu-id="aaa3f-174">После `Display` нажатия кнопки вы получите более ранний вариант.</span><span class="sxs-lookup"><span data-stu-id="aaa3f-174">When you select the `Display` button, you get what is below.</span></span>  <span data-ttu-id="aaa3f-175">Если вы выберете в любом месте `stars.jpeg` изображения, то этот элемент изображения удаляется, а страницы вкладок — на то, что было первоначально отображено.</span><span class="sxs-lookup"><span data-stu-id="aaa3f-175">If you select anywhere on the `stars.jpeg` image, that image element is removed and tab pages collapses back to what was originally displayed.</span></span>  

:::image type="complex" source="./media/part2-showingimage.png" alt-text="Изображение, показанное в браузере":::
   <span data-ttu-id="aaa3f-177">Изображение, показанное в браузере</span><span class="sxs-lookup"><span data-stu-id="aaa3f-177">The image showing in browser</span></span>
:::image-end:::

<!--![The image showing in browser][ImagePart2Showingimage]  -->  

<span data-ttu-id="aaa3f-178">Вы создали расширение, которое успешно отправляет сообщение из всплывающего окна значка расширения, в динамически вставленный сценарий JavaScript, выполняющийся как содержимое на вкладке "браузер".  Введенное содержимое задает элемент изображения для отображения статичных звезд JPEG.</span><span class="sxs-lookup"><span data-stu-id="aaa3f-178">You have now created an Extension that successfully sends a message from the Extension icon pop-up, to the dynamically inserted JavaScript running as content on the browser tab.  That injected content set the image element to display your static stars jpeg.</span></span>  

<!-- image links -->  

<!--[ImagePart2Popupdialog]: ./media/part2-popupdialog.png "popup.html display after pressing the Extension icon"  -->  
<!--[ImagePart2Showingimage]: ./media/part2-showingimage.png "The image showing in browser"  -->

<!-- links -->  

[ArchiveExtensionGettingStartedPart2]: ./extension-source/extension-getting-started-part2.zip "Источник пакета расширения для этой части завершен | Документы Microsoft"  