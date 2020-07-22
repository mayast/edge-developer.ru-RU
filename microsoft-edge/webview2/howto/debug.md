---
description: Сведения об отладке элементов управления WebView2.
title: Отладка WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 232104abc360cfa660d567ffb66535213fcb3ae0
ms.sourcegitcommit: a82aa5fc1ada35cd8274490fbff3c0a850785835
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/21/2020
ms.locfileid: "10888588"
---
# Отладка с помощью WebView2  

Цель элемента управления Microsoft Edge WebView2 — объединение лучшей из функций разработки веб-приложений и собственного приложения, а также средств разработчика.  На следующей странице описаны различные инструменты для разработки с помощью элементов управления WebView2.  

## Microsoft Edge DevTools  

Используйте [средства разработчика Microsoft EDGE (Chromium)][DevtoolsMain] для отладки веб-содержимого, отображаемого в элементах управления WebView2, таким же образом, как и при использовании Microsoft Edge.  Чтобы открыть DevTools, установите фокус в окне WebView, а затем выполните одно из указанных ниже действий.  

*   Выберите `F12` .  
*   Выберите `Ctrl` + `Shift` + `I` .  
*   Откройте контекстное меню, а затем щелкните правой кнопкой мыши и выберите команду `Inspect` .  

:::image type="complex" source="../media/f12.png" alt-text="Microsoft Edge DevTools" lightbox="../media/f12.png":::
   Microsoft Edge DevTools  
:::image-end:::  

> [!IMPORTANT]
> При отладке приложения в Visual Studio с присоединенным отладчиком машинного кода выбор `F12` может инициировать собственный отладчик вместо средств разработчика.  Использование `Ctrl` + `Shift` + `I` или использование контекстного меню \ (щелкните правой кнопкой мыши, чтобы избежать ситуации).  

## VisualStudio  

Вы можете использовать Visual Studio для одновременной разработки кода приложения и сценариев отладки.  

Учитывайте указанные ниже моменты.  

*   Visual Studio поддерживает сценарии отладки только при запуске приложения в Visual Studio.  \ (Подключение запущенного процесса для отладки не поддерживается. \)  
*   Конечный сценарий отладки WebView не поддерживается.  

Используйте отладчик сценариев в Visual Studio 2019 версии 16,4 Preview 2 и более поздних версий для отладки сценария в Visual Studio.  

Настройте отладчик.  

*   Убедитесь, что компонент **диагностики JavaScript** установлен на **рабочем столе с** рабочей нагрузкой C++.  
    
    1.  Перейдите в раздел **приложения & параметры компонентов** в Windows.  Найдите его с помощью панели задач Windows.  
    1.  Нажмите кнопку **изменить**.  
    1.  Убедитесь, что выбраны флажки **Диагностика** и **Разработка классической среды на C++** .  
        
        :::image type="complex" source="../media/appsandfeatures.png" alt-text="Приложения и компоненты" lightbox="../media/appsandfeatures.png":::
           Приложения и компоненты  
        :::image-end:::  
        
*   Включите отладку сценариев WebView2.  
    1.  Наведите указатель мыши на проект, откройте контекстное меню (щелкните правой кнопкой мыши \) и выберите пункт **Свойства**.  
    1.  На вкладке **Свойства конфигурации**выберите пункт **Отладка**.  
    1.  В свойстве **Тип отладчика** выполните поиск в списке параметров и выберите **JavaScript (WebView2)**.  
        
        :::image type="complex" source="../media/enbjs.png" alt-text="Отладчик JavaScript для Visual Studio" lightbox="../media/enbjs.png":::
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

Код Visual Studio можно использовать для отладки сценариев, которые выполняются в элементах управления WebView2.  Дополнительные сведения можно найти в разделе [приложения Microsoft EDGE (Chromium) WebView][GithubMicrosoftVscodeEdgeDebug2MainChromiumWebviewApplications].  

<!--todo:  add See also heading  -->  

## Знакомство с командой Microsoft Edge WebView  

Помогите вам создать более WebView2ную работу, отправив свой отзыв.  Чтобы отправить запросы на функции или отчеты об ошибках, посетите [репозиторий обратной связи][GithubMicrosoftedgeWebviewfeedback] .  

<!-- links -->  

[DevtoolsMain]: /microsoft-edge/devtools-guide-chromium "Инструменты разработчика Microsoft EDGE (Chromium) | Документы Microsoft"  

[GithubMicrosoftVscodeEdgeDebug2MainChromiumWebviewApplications]: https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications "Microsoft EDGE (Chromium) WebView Applications-VS-Debugger для Microsoft Edge | GitHub"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  
