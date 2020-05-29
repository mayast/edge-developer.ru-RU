---
description: Автоматизация и тестирование в Microsoft Edge с помощью Puppeteer
title: Puppeteer
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/27/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft EDGE, веб-разработка, разработчик, инструменты, Автоматизация и тестирование
ms.openlocfilehash: a78bdc0eb96db018818ef122c772bc9023adac46
ms.sourcegitcommit: 4187d4c3fbf4ef99a3b8a63db8a182355c84c1f9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601939"
---
# <span data-ttu-id="104a0-104">Puppeteer</span><span class="sxs-lookup"><span data-stu-id="104a0-104">Puppeteer</span></span>  

<span data-ttu-id="104a0-105">[Puppeteer][|::ref1::|Main] — это библиотека [узлов][NodejsMain] , которая предоставляет интерфейс API высокого уровня для управления Microsoft Edge \ (Chromium \) по [протоколу DevTools][GithubChromedevtoolsProtocol].</span><span class="sxs-lookup"><span data-stu-id="104a0-105">[Puppeteer][|::ref1::|Main] is a [Node][NodejsMain] library which provides a high-level API to control Microsoft Edge \(Chromium\) over the [DevTools Protocol][GithubChromedevtoolsProtocol].</span></span>  <span data-ttu-id="104a0-106">Puppeteer по умолчанию работает без [монитора][WikiHeadlessBrowser] , что означает, что пользовательский интерфейс не отображается, а вместо этого необходимо использовать командную строку.</span><span class="sxs-lookup"><span data-stu-id="104a0-106">Puppeteer runs [headless][WikiHeadlessBrowser] by default, which means that you do not see a UI, and instead must use the command-line.</span></span>  <span data-ttu-id="104a0-107">Вы также можете настроить Puppeteer на выполнение полных \ (без монитора \) Microsoft EDGE или Chromium.</span><span class="sxs-lookup"><span data-stu-id="104a0-107">You may also configure Puppeteer to run full \(non-headless\) Microsoft Edge or Chromium as well.</span></span>  

<span data-ttu-id="104a0-108">По умолчанию при установке Puppeteer программа установки загружает последнюю версию [Chromium][ChromiumHome]— обозреватель Open-Source, на котором [также построен Microsoft Edge][MicrosoftBlogsWindowsExperience20181206].</span><span class="sxs-lookup"><span data-stu-id="104a0-108">By default, when you install Puppeteer, the installer downloads a recent version of [Chromium][ChromiumHome], the open-source browser that [Microsoft Edge is also built upon][MicrosoftBlogsWindowsExperience20181206].</span></span>  <span data-ttu-id="104a0-109">Если у вас установлен Microsoft Edge \ (Chromium \), вы можете использовать [puppeteer-Core][PuppeteerApivscore].</span><span class="sxs-lookup"><span data-stu-id="104a0-109">If you have Microsoft Edge \(Chromium\) installed, you may use [puppeteer-core][PuppeteerApivscore].</span></span>  `puppeteer-core` <span data-ttu-id="104a0-110">— Это упрощенная версия Puppeteer, которая запускает уже установленный браузер, например Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="104a0-110">is a lightweight version of Puppeteer that launches an existing browser installation, like Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="104a0-111">Чтобы скачать Microsoft Edge \ (Chromium \), обратитесь к разделу [Загрузка каналов предварительной оценки Microsoft Edge][MicrosoftedgeinsiderDownload].</span><span class="sxs-lookup"><span data-stu-id="104a0-111">To download Microsoft Edge \(Chromium\), see [Download Microsoft Edge Insider Channels][MicrosoftedgeinsiderDownload].</span></span>

## <span data-ttu-id="104a0-112">Установка puppeteer-Core</span><span class="sxs-lookup"><span data-stu-id="104a0-112">Installing puppeteer-core</span></span>  

<span data-ttu-id="104a0-113">Вы можете добавить `puppeteer-core` на веб-сайт или в приложение одну из указанных ниже команд.</span><span class="sxs-lookup"><span data-stu-id="104a0-113">You may add `puppeteer-core` to your website or app with one of the following commands.</span></span>  

```shell
npm i puppeteer-core
```  

```shell
yarn add puppeteer-core
```  

## <span data-ttu-id="104a0-114">Запуск Microsoft Edge с puppeteer (Core)</span><span class="sxs-lookup"><span data-stu-id="104a0-114">Launch Microsoft Edge with puppeteer-core</span></span>  

> [!NOTE]
> `puppeteer-core` <span data-ttu-id="104a0-115">опирается на узел v 8.9.0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="104a0-115">relies on Node v8.9.0 or later.</span></span>  <span data-ttu-id="104a0-116">В примере ниже используется элемент `async` / `await` , который поддерживается только в node v 7.6.0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="104a0-116">The example below uses `async`/`await` which is only supported in Node v7.6.0 or later.</span></span>  <span data-ttu-id="104a0-117">Запустите `node -v` из командной строки, чтобы убедиться, что у вас есть совместимая версия файла Node. js.</span><span class="sxs-lookup"><span data-stu-id="104a0-117">Run `node -v` from the command-line to ensure you have a compatible version of Node.js.</span></span>  

`puppeteer-core` <span data-ttu-id="104a0-118">Знакомство с пользователями других платформ тестирования браузера, таких как веб- [дисковод][WebDriverEdgehtmlMain].</span><span class="sxs-lookup"><span data-stu-id="104a0-118">should be familiar to users of other browser-testing-frameworks like [WebDriver][WebDriverEdgehtmlMain].</span></span>  <span data-ttu-id="104a0-119">Вы создаете экземпляр браузера, открываете страницу, а затем управляете ею с помощью API Puppeteer.</span><span class="sxs-lookup"><span data-stu-id="104a0-119">You create an instance of the browser, open a page, and then manipulate it with the Puppeteer API.</span></span>  <span data-ttu-id="104a0-120">В приведенном ниже примере кода `puppeteer-core` запускается Microsoft Edge \ (Chromium \), осуществляется переход на `https://www.microsoftedgeinsider.com` снимок экрана и сохранение его как `example.png` .</span><span class="sxs-lookup"><span data-stu-id="104a0-120">In the following code sample, `puppeteer-core` launches Microsoft Edge \(Chromium\), navigates to `https://www.microsoftedgeinsider.com`, and saves a screenshot as `example.png`.</span></span>  

<span data-ttu-id="104a0-121">Скопируйте приведенный ниже пример кода и сохраните его как `example.js` .</span><span class="sxs-lookup"><span data-stu-id="104a0-121">Copy the code sample below and save it as `example.js`.</span></span>  

```javascript
const puppeteer = require('puppeteer-core');

(async () => {
  const browser = await puppeteer.launch({
    executablePath: 'C:\\Program Files (x86)\\Microsoft\\Edge Dev\\Application\\msedge.exe'
  });
  const page = await browser.newPage();
  await page.goto('https://www.microsoftedgeinsider.com');
  await page.screenshot({path: 'example.png'});

  await browser.close();
})();
```  

<span data-ttu-id="104a0-122">Измените `executablePath` этот элемент, чтобы он указывал на установленный Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="104a0-122">Change `executablePath` to point to your installation of Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="104a0-123">Например, в macOS `executablePath` для Microsoft Edge Канарские должно быть установлено значение `/Applications/Microsoft\ Edge\ Canary.app/` .</span><span class="sxs-lookup"><span data-stu-id="104a0-123">For example, on macOS, the `executablePath` for Microsoft Edge Canary should be set to `/Applications/Microsoft\ Edge\ Canary.app/`.</span></span>  <span data-ttu-id="104a0-124">Чтобы найти `executablePath` , перейдите к `edge://version` .</span><span class="sxs-lookup"><span data-stu-id="104a0-124">To find the `executablePath`, navigate to `edge://version`.</span></span>  <span data-ttu-id="104a0-125">В конце необходимо сохранить изменения.</span><span class="sxs-lookup"><span data-stu-id="104a0-125">Save your changes.</span></span>  

> [!NOTE]
> <span data-ttu-id="104a0-126">Microsoft Edge \ (EdgeHTML \) не работает с другими приложениями `puppeteer-core` .</span><span class="sxs-lookup"><span data-stu-id="104a0-126">Microsoft Edge \(EdgeHTML\) does not work with `puppeteer-core`.</span></span>  <span data-ttu-id="104a0-127">Чтобы продолжить работу в этом примере, необходимо установить [каналы предварительной оценки Microsoft Edge][MicrosoftedgeinsiderDownload] .</span><span class="sxs-lookup"><span data-stu-id="104a0-127">You must install the [Microsoft Edge Insider channels][MicrosoftedgeinsiderDownload] to continue following this example.</span></span>  

<span data-ttu-id="104a0-128">Теперь запустите `example.js` из командной строки.</span><span class="sxs-lookup"><span data-stu-id="104a0-128">Now run `example.js` from the command-line.</span></span>  

```shell
node example.js
```  

`puppeteer-core` <span data-ttu-id="104a0-129">запускает Microsoft EDGE, переходит `https://www.microsoftedgeinsider.com` и сохраняет снимок экрана 800px x 600px страницы.</span><span class="sxs-lookup"><span data-stu-id="104a0-129">launches Microsoft Edge, navigates to `https://www.microsoftedgeinsider.com` and saves an 800px x 600px screenshot of the page.</span></span>  <span data-ttu-id="104a0-130">Вы можете настроить размер страницы с помощью [Page. setViewport ()][PuppeteerApipagesetviewport].</span><span class="sxs-lookup"><span data-stu-id="104a0-130">You are able to customize the page size with [page.setViewport()][PuppeteerApipagesetviewport].</span></span>  

:::image type="complex" source="./media/puppeteer-example.png" alt-text="Пример PNG-файла, созданного примером. js":::
   <span data-ttu-id="104a0-132">Рисунок 1: `example.png` файл, созданный с помощью</span><span class="sxs-lookup"><span data-stu-id="104a0-132">Figure 1:  The `example.png` file produced by</span></span> `example.js`  
:::image-end:::  

<!--  
> ##### Figure 1  
> The `example.png` file produced by `example.js`  
> ![The example.png file produced by example.js](./media/puppeteer-example.png)  
-->  

<span data-ttu-id="104a0-133">Это простой пример сценариев автоматизации и тестирования, включенных в Puppeteer и `puppeteer-core` .</span><span class="sxs-lookup"><span data-stu-id="104a0-133">This is just a simple example of the automation and testing scenarios enabled by Puppeteer and `puppeteer-core`.</span></span>  <span data-ttu-id="104a0-134">Дополнительные сведения о Puppeteer и том, как это работает, можно найти в статьях [Puppeteer][|::ref2::|Main].</span><span class="sxs-lookup"><span data-stu-id="104a0-134">For more information about Puppeteer and how it works, see [Puppeteer][|::ref2::|Main].</span></span>  

## <span data-ttu-id="104a0-135">Отправка отзыва</span><span class="sxs-lookup"><span data-stu-id="104a0-135">Send Feedback</span></span>  

<span data-ttu-id="104a0-136">Группа разработчиков Edge может услышать отзывы об использовании Puppeteer `puppeteer-core` и Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="104a0-136">The Edge Developer team is eager to hear your feedback about using Puppeteer, `puppeteer-core`, and Microsoft Edge.</span></span>  <span data-ttu-id="104a0-137">С помощью значка " **Отправить отзыв** " в Microsoft Edge DevTools или твит [@EdgeDevTools][TwitterIntentTweetEdgedevtools] , чтобы группа Microsoft Edge знала, что вы думаете.</span><span class="sxs-lookup"><span data-stu-id="104a0-137">Use the **Send Feedback** icon in the Microsoft Edge DevTools or tweet [@EdgeDevTools][TwitterIntentTweetEdgedevtools] to let the Microsoft Edge team know what you think.</span></span>  


:::image type="complex" source="./devtools-guide-chromium/media/devtools-feedback.png" alt-text="Значок обратной связи в Microsoft Edge DevTools":::
   <span data-ttu-id="104a0-139">Рисунок 2: значок **обратной связи** в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="104a0-139">Figure 2:  The **Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!--  
> ##### Figure 2  
> The **Feedback** icon in the Microsoft Edge DevTools  
> ![The Feedback icon in the Microsoft Edge DevTools](./devtools-guide-chromium/media/devtools-feedback.png)  
-->  

<!--## See also  

*   [WebDriver (Chromium)][WebdriverChromiumMain]  
*   [WebDriver (EdgeHTML)][WebdriverEdgehtmlMain]  
*   [Chrome DevTools Protocol Viewer on GitHub][GithubChromedevtoolsProtocol]  
*   [Microsoft Edge: Making the web better through more open source collaboration on Microsoft Experience Blog][MicrosoftBlogsWindowsExperience20181206]  
*   [Download Microsoft Edge Insider Channels][MicrosoftedgeinsiderDownload]  
*   [Chromium on The Chromium Projects][ChromiumHome]  
*   [Node.js][NodejsMain]  
*   [Puppeteer][PuppeteerMain]  
*   [puppeteer vs. puppeteer-core][PuppeteerApivscore]  
*   [page.setViewport() on Puppeteer][PuppeteerApipagesetviewport]  
*   [Headless browser on Wikipedia][WikiHeadlessBrowser]  -->  

<!-- image links -->  

<!-- links -->  

[WebdriverChromiumMain]: ./webdriver-chromium.md "Chromium"  
[WebdriverEdgehtmlMain]: ./webdriver.md "EdgeHTML"  

[GithubChromedevtoolsProtocol]: https://chromedevtools.github.io/devtools-protocol "Средство просмотра протоколов Chrome DevTools | GitHub"  

[MicrosoftBlogsWindowsExperience20181206]: https://blogs.windows.com/windowsexperience/2018/12/06/microsoft-edge-making-the-web-better-through-more-open-source-collaboration "Microsoft Edge: улучшение веб-сайта с помощью более эффективной работы в открытых источниках | Блог Microsoft Experience"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Скачайте каналы предварительной оценки Microsoft Edge"  

[ChromiumHome]: https://www.chromium.org/Home "Chromium | Проекты Chromium"  

[NodejsMain]: https://nodejs.org "Node. js"  

[PuppeteerMain]: https://pptr.dev "Puppeteer"  
[PuppeteerApivscore]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-puppeteer-vs-puppeteer-core "puppeteer и puppeteer-Core | Puppeteer"  
[PuppeteerApipagesetviewport]: https://pptr.dev/#?product=Puppeteer&version=v2.0.0&show=api-pagesetviewportviewport "Page. setViewport (окно просмотра) | Puppeteer"  

[TwitterIntentTweetEdgedevtools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools-опубликовать твит | Контента"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Автономный браузер | Википедии"  
