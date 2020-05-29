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
# Puppeteer  

[Puppeteer][|::ref1::|Main] — это библиотека [узлов][NodejsMain] , которая предоставляет интерфейс API высокого уровня для управления Microsoft Edge \ (Chromium \) по [протоколу DevTools][GithubChromedevtoolsProtocol].  Puppeteer по умолчанию работает без [монитора][WikiHeadlessBrowser] , что означает, что пользовательский интерфейс не отображается, а вместо этого необходимо использовать командную строку.  Вы также можете настроить Puppeteer на выполнение полных \ (без монитора \) Microsoft EDGE или Chromium.  

По умолчанию при установке Puppeteer программа установки загружает последнюю версию [Chromium][ChromiumHome]— обозреватель Open-Source, на котором [также построен Microsoft Edge][MicrosoftBlogsWindowsExperience20181206].  Если у вас установлен Microsoft Edge \ (Chromium \), вы можете использовать [puppeteer-Core][PuppeteerApivscore].  `puppeteer-core` — Это упрощенная версия Puppeteer, которая запускает уже установленный браузер, например Microsoft Edge \ (Chromium \).  Чтобы скачать Microsoft Edge \ (Chromium \), обратитесь к разделу [Загрузка каналов предварительной оценки Microsoft Edge][MicrosoftedgeinsiderDownload].

## Установка puppeteer-Core  

Вы можете добавить `puppeteer-core` на веб-сайт или в приложение одну из указанных ниже команд.  

```shell
npm i puppeteer-core
```  

```shell
yarn add puppeteer-core
```  

## Запуск Microsoft Edge с puppeteer (Core)  

> [!NOTE]
> `puppeteer-core` опирается на узел v 8.9.0 или более поздней версии.  В примере ниже используется элемент `async` / `await` , который поддерживается только в node v 7.6.0 или более поздней версии.  Запустите `node -v` из командной строки, чтобы убедиться, что у вас есть совместимая версия файла Node. js.  

`puppeteer-core` Знакомство с пользователями других платформ тестирования браузера, таких как веб- [дисковод][WebDriverEdgehtmlMain].  Вы создаете экземпляр браузера, открываете страницу, а затем управляете ею с помощью API Puppeteer.  В приведенном ниже примере кода `puppeteer-core` запускается Microsoft Edge \ (Chromium \), осуществляется переход на `https://www.microsoftedgeinsider.com` снимок экрана и сохранение его как `example.png` .  

Скопируйте приведенный ниже пример кода и сохраните его как `example.js` .  

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

Измените `executablePath` этот элемент, чтобы он указывал на установленный Microsoft Edge \ (Chromium \).  Например, в macOS `executablePath` для Microsoft Edge Канарские должно быть установлено значение `/Applications/Microsoft\ Edge\ Canary.app/` .  Чтобы найти `executablePath` , перейдите к `edge://version` .  В конце необходимо сохранить изменения.  

> [!NOTE]
> Microsoft Edge \ (EdgeHTML \) не работает с другими приложениями `puppeteer-core` .  Чтобы продолжить работу в этом примере, необходимо установить [каналы предварительной оценки Microsoft Edge][MicrosoftedgeinsiderDownload] .  

Теперь запустите `example.js` из командной строки.  

```shell
node example.js
```  

`puppeteer-core` запускает Microsoft EDGE, переходит `https://www.microsoftedgeinsider.com` и сохраняет снимок экрана 800px x 600px страницы.  Вы можете настроить размер страницы с помощью [Page. setViewport ()][PuppeteerApipagesetviewport].  

:::image type="complex" source="./media/puppeteer-example.png" alt-text="Пример PNG-файла, созданного примером. js":::
   Рисунок 1: `example.png` файл, созданный с помощью `example.js`  
:::image-end:::  

<!--  
> ##### Figure 1  
> The `example.png` file produced by `example.js`  
> ![The example.png file produced by example.js](./media/puppeteer-example.png)  
-->  

Это простой пример сценариев автоматизации и тестирования, включенных в Puppeteer и `puppeteer-core` .  Дополнительные сведения о Puppeteer и том, как это работает, можно найти в статьях [Puppeteer][|::ref2::|Main].  

## Отправка отзыва  

Группа разработчиков Edge может услышать отзывы об использовании Puppeteer `puppeteer-core` и Microsoft Edge.  С помощью значка " **Отправить отзыв** " в Microsoft Edge DevTools или твит [@EdgeDevTools][TwitterIntentTweetEdgedevtools] , чтобы группа Microsoft Edge знала, что вы думаете.  


:::image type="complex" source="./devtools-guide-chromium/media/devtools-feedback.png" alt-text="Значок обратной связи в Microsoft Edge DevTools":::
   Рисунок 2: значок **обратной связи** в Microsoft Edge DevTools  
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
