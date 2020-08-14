---
description: Сведения об отладке элементов управления WebView2.
title: Приступая к отладке приложений WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/13/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: dcdeeadc2c25bcf50834176706b8d181f06f994a
ms.sourcegitcommit: 6c7ededf8677fd7add5e4060e92f9ec4cfdb6952
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/13/2020
ms.locfileid: "10927925"
---
# Приступая к отладке приложений WebView2  

Цель элемента управления Microsoft Edge WebView2 заключается в том, чтобы сочетать лучший из функций разработки веб-и собственных приложений, а также средств и инструментов.  Когда вы разрабатываете приложение WebView2, необходимо выполнить отладку приложения.  В этой статье описаны различные инструменты для отладки вашего веб-и собственного кода в приложении WebView2.  

## [Microsoft Edge DevTools](#tab/devtools)  

Используйте [средства разработчика Microsoft EDGE (Chromium)][DevtoolsGuideChromiumMain] для отладки содержимого веб-страницы, отображаемого в элементах управления WebView2, таким же образом, как и при отладке на других страницах, отображаемых в Microsoft Edge.  Чтобы открыть DevTools, установите фокус на элементе управления WebView, а затем выполните одно из указанных ниже действий.  

*   Выберите `F12` .  
*   Выберите `Ctrl` + `Shift` + `I` .  
*   Откройте контекстное меню, а затем щелкните правой кнопкой мыши и выберите команду `Inspect` .  

Дополнительные сведения можно найти в разделе [Общие сведения о DevTools][DevtoolsGuideChromiumMain].  

:::image type="complex" source="./media/f12.png" alt-text="Отладка DevTools" lightbox="./media/f12.png":::
   Отладка DevTools  
:::image-end:::  

## [VisualStudio](#tab/visualstudio)  

Visual Studio предоставляет различные инструменты отладки для веб-и машинного кода в приложениях WebView2.  В разделе Visual Studio главным фокусом является Отладка элементов управления WebView, однако другие методы отладки в Visual Studio можно использовать в обычном режиме.  Используйте следующий процесс для отладки веб-и машинного кода в приложениях Win32 или только для надстроек Office.  

> [!IMPORTANT]
> При отладке приложения в Visual Studio с присоединенным отладчиком машинного кода выбор `F12` может инициировать собственный отладчик вместо средств разработчика.  `Ctrl` + `Shift` + `I` Чтобы избежать ситуации, выберите или используйте контекстное меню \ (щелкните правой кнопкой мыши).  

Прежде чем начать, убедитесь, что выполнены следующие требования.  

*   Для отладки скриптов приложение должно быть запущено в Visual Studio.  
*   Вы не можете прикрепить отладчик к выполняющемуся процессу WebView2.  
*   Установите Visual Studio 2019 версии 16,4 Preview 2 или более поздней версии.  

Установка и настройка средств отладки сценариев в Visual Studio.  

1.  Выполните указанные ниже действия, чтобы установить компонент **диагностики JavaScript** в **классических разработках с + +**.  

    1. На панели проводника Windows введите `Visual Studio Installer` .  
    1. Щелкните **Установщик Visual Studio** , чтобы открыть его.  
    1. В установщике Visual Studio на установленной версии нажмите кнопку **Дополнительно** , а затем выберите команду **изменить**.  
    1. В Visual Studio в разделе **рабочие нагрузки**выберите параметр **Разработка классической среды на C++** .  
        
        :::image type="complex" source="./media/workloads.png" alt-text="Экран изменения рабочей нагрузки в Visual Studio" lightbox="./media/workloads.png":::
            Экран изменения рабочей нагрузки в Visual Studio :::image-end:::  
        
    1.  Выберите **отдельные компоненты**.  
    1.  В поле поиска введите `JavaScript diagnostics` .  
    1.  Выберите параметр **диагностики JavaScript** .  
    1.  Нажмите кнопку **изменить**. 
        
        :::image type="complex" source="./media/indivcomp.png" alt-text="Вкладка "изменение отдельных компонентов" в Visual Studio" lightbox="./media/indivcomp.png":::
           Вкладка "изменение отдельных компонентов" в Visual Studio  
        :::image-end:::  
        
1.  Включите отладку сценариев для приложений WebView2.  
    1.  В проекте WebView2 откройте контекстное меню, а затем щелкните правой кнопкой мыши и выберите пункт **Свойства**.  
    1.  В разделе **Свойства конфигурации**выберите пункт **Отладка**.  
    1.  В разделе **Тип отладчика**выберите **JavaScript (WebView2)**.  
        
        :::image type="complex" source="./media/enbjs.png" alt-text="Свойство конфигурации отладки в Visual Studio" lightbox="./media/enbjs.png":::
           Свойство конфигурации **отладки** в Visual Studio  
        :::image-end:::  
        
Выполните указанные ниже действия, чтобы выполнить отладку приложения WebView2.  

1.  Чтобы задать точку останова в исходном коде, наведите указатель мыши на левый номер строки и выберите точку останова.  Адаптеры отладки JS-и ст не выполняют сопоставление исходного пути.  Вы должны открыть именно тот же путь, связанный с вашим WebView2.  
    
    :::image type="complex" source="./media/breakpoint.png" alt-text="Добавление точки останова в Visual Studio" lightbox="./media/breakpoint.png"::: 
       Добавление точки останова в Visual Studio  
    :::image-end:::  
    
1.  Чтобы запустить отладчик, выберите битовый Размер платформы, а затем нажмите зеленую кнопку воспроизведения рядом с **местным отладчиком Windows**.  Приложение запустится, и отладчик подключится к первому процессу WebView2, который вы создали.  
    
    :::image type="complex" source="./media/run.png" alt-text=" Локальный отладчик Windows для Visual Studio" lightbox="./media/run.png"::: 
       **Локальный отладчик Windows** для Visual Studio  
    :::image-end:::  
    
1.  В **консоли отладки**найдите выходные данные отладчика.  
    
    :::image type="complex" source="./media/console.png" alt-text=" Консоль отладки Visual Studio" lightbox="./media/console.png"::: 
       **Консоль отладки** Visual Studio  
    :::image-end:::  
    
* * *  

## См. также  

*   Чтобы приступить к работе с WebView2, ознакомьтесь со статьей [руководства Приступая к работе с WebView2][Webview2MainGettingStarted].  
*   Полный пример возможностей WebView2 можно найти в репозитории [WebView2Samples][GithubMicrosoftedgeWebview2samples] на GitHub.
*   Более подробную информацию об API WebView2 можно найти в [справочнике API][Webview2ApiReference].
*   Дополнительные сведения о WebView2ах можно найти в статьях [ресурсы WebView2][Webview2MainNextSteps].

## Знакомство с командой Microsoft Edge WebView  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  

<!-- links -->  

[DevtoolsGuideChromiumMain]: ../../devtools-guide-chromium.md "Инструменты разработчика Microsoft EDGE (Chromium)"  

[Webview2ReferenceDotnet09515MicrosoftWebWebview2CoreCorewebview2environmentoptionsAdditionalbrowserarguments]: ../reference/dotnet/0-9-515/microsoft-web-webview2-core-corewebview2environmentoptions.md#additionalbrowserarguments "Класс AdditionalBrowserArguments-0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2EnvironmentOptions | Документы Microsoft"  
[Webview2ReferenceWin3209538Webview2IdlParameters]: ../reference/win32/0-9-538/webview2-idl.md#createcorewebview2environment  "CreateCoreWebView2Environment-Globals | Документы Microsoft"  
[Webview2ApiReference]: ../webview2-api-reference.md "Справочник по API Microsoft Edge WebView2 | Документы Microsoft"  
[Webview2MainNextSteps]: ../index.md#next-steps "Дальнейшие действия — введение в Microsoft Edge WebView2 (Предварительная версия) | Документы Microsoft"  
[Webview2MainGettingStarted]: ../index.md#getting-started "Приступая к работе: знакомство с Microsoft Edge WebView2 (Предварительная версия) | Документы Microsoft"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  
[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples-MicrosoftEdge/WebView2Samples | GitHub"  

[GithubMicrosoftVscodeJSDebugWhatsNew]: https://github.com/microsoft/vscode-js-debug#whats-new "Новые возможности -Отладчик JavaScript для Visual Studio Code-Microsoft/vscode-JS-Debug | GitHub"  

[GithubMicrosoftVscodeEdgeDebug2ReadmeChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Microsoft EDGE (Chromium) WebView Applications-Debugger (код Visual Studio) — отладчик для Microsoft Edge-Microsoft/vscode-Edge-debug2 | GitHub"  
