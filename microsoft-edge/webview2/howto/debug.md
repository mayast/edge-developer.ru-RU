---
description: Сведения об отладке элементов управления WebView2.
title: Отладка WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/22/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: ad6f334e5796d2f22146f2853ae1ef1d854e329c
ms.sourcegitcommit: b3555043e9d5aefa5a9e36ba4d73934d41559f49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/23/2020
ms.locfileid: "10894321"
---
# Отладка с помощью WebView2  

Цель элемента управления Microsoft Edge WebView2 — объединение лучшей из функций разработки веб-приложений и собственного приложения, а также средств разработчика.  На следующей странице описаны различные инструменты для разработки с помощью элементов управления WebView2.  

## Microsoft Edge DevTools  

Используйте [средства разработчика Microsoft EDGE (Chromium)][DevtoolsGuideChromiumMain] для отладки веб-содержимого, отображаемого в элементах управления WebView2, таким же образом, как и при использовании Microsoft Edge.  Чтобы открыть DevTools, установите фокус в окне WebView, а затем выполните одно из указанных ниже действий.  
*   Выберите `F12` .  
*   Выберите `Ctrl` + `Shift` + `I` .  
*   Откройте контекстное меню \ (щелкните правой кнопкой мыши, > выбрать `Inspect` .  

:::image type="complex" source="../media/f12.png" alt-text="Microsoft Edge DevTools" lightbox="../media/f12.png":::
   Microsoft Edge DevTools  
:::image-end:::  

> [!NOTE]
> При отладке приложения в Visual Studio с прикрепленным отладчиком машинного кода `F12` вместо средств разработчика может возникнуть нажатие клавиш отладчика машинного кода.  `Ctrl` + `Shift` + `I` Чтобы избежать такой ситуации, нажмите или используйте контекстное меню (щелкните правой кнопкой мыши).  

> [!NOTE]
> Вы можете использовать `--auto-open-devtools-for-tabs` аргумент командной строки, чтобы открыть новое окно DevTools при первом создании WebView.  <!--See `CreateCoreWebView2Controller` documentation for how to provide additional command-line arguments to the browser process.  See `LoaderOverride` registry key to examine different builds of WebView2 without modifying your application in the `CreateCoreWebView2Controller` documentation.  -->  

## VisualStudio  

Используйте отладчик сценариев в Visual Studio 2019 версии 16,4 Preview 2 и более поздних версий для отладки сценария в Visual Studio.  Убедитесь, что компонент **диагностики JavaScript** установлен на **рабочем столе с** рабочей нагрузкой C++.  

:::image type="complex" source="../media/vs-js-diagnostics.jpg" alt-text="Диагностика JavaScript в Visual Studio":::
   Диагностика JavaScript в Visual Studio  
:::image-end:::  

<!--todo: Please update the image to use a red rectangle to outline the portion of the screen to highlight  -->  

Чтобы включить отладку сценариев WebView2, откройте контекстное меню в проекте, а затем щелкните правой кнопкой мыши > выберите пункт **Свойства**.  

*   На вкладке **Свойства конфигурации**выберите пункт **Отладка**.  
*   В свойстве **Type Debugger (тип отладчика** **) выберите JavaScript (WebView2)** в списке параметров. 

:::image type="complex" source="../media/vs-script-debugger.jpg" alt-text="Отладчик JavaScript для Visual Studio":::
   Отладчик JavaScript для Visual Studio  
:::image-end:::  

<!--todo: Please update the image to use a red rectangle to outline the portion of the screen to highlight  -->  

Все настроено и готово к отладке.  

Чтобы выполнить отладку, выполните указанные ниже действия.  

1.  Установка точек останова  
    *   Откройте файл сценария и установите точку останова в нужном месте.  
        
        > [!NOTE]
        > Адаптеры отладки JS/TS не выполняют сопоставление исходного пути.Вы должны открыть именно тот же путь, связанный с вашим WebView2.  
        
1.  Выполнение кода  
    *   Выберите соответствующую версию сборки и среду выполнения, а затем запустите локальный отладчик Windows.  
1.  Просмотр консоли отладки  
    *   Вы запускаете приложение, и отладчик подключается после создания первого webview2.На экране появятся все ожидающие результаты отладки.  
        
        > [!NOTE]
        > Этот метод отладки в настоящее время ограничен приложениями Win32 и надстройками Office.  
        
## Visual Studio Code  

Код Visual Studio можно использовать для отладки сценариев, которые выполняются в элементах управления WebView2.  Дополнительные сведения можно найти в разделе [приложения Microsoft EDGE (Chromium) WebView][GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications].  

<!--todo:  add See also heading  -->  

## Знакомство с командой Microsoft Edge WebView  

Помогите вам создать более WebView2ную работу, отправив свой отзыв.  Чтобы отправить запросы на функции или отчеты об ошибках, посетите [репозиторий обратной связи][GithubMicrosoftedgeWebviewfeedbackMain] .  

<!--## Debugging  

Open DevTools with the normal shortcuts: `F12` or `Ctrl+Shift+I`. You can use the `--auto-open-devtools-for-tabs` command argument switch to have the DevTools window open immediately when first creating a WebView. See CreateCoreWebView2Controller documentation for how to provide additional command line arguments to the browser process. Check out the LoaderOverride registry key for trying out different builds of WebView2 without modifying your application in the CreateCoreWebView2Controller documentation.  -->  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Инструменты разработчика Microsoft EDGE (Chromium)"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Microsoft EDGE (Chromium) WebView Applications-VS-Debugger для Microsoft Edge-Microsoft/vscode-Edge-debug2 | GitHub"  
