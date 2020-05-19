---
description: Сведения об отладке элементов управления WebView2.
title: Отладка WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/19/2020
ms.topic: how-to
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 386bc237257be0ade8c48bc1c737b0151a882719
ms.sourcegitcommit: 5bdffe91a6594f77eeffa4e864fda90a02784771
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/19/2020
ms.locfileid: "10659716"
---
# Отладка при разработке с помощью элементов управления WebView2  

Цель элемента управления Microsoft Edge WebView2 — объединение лучшей из функций разработки веб-приложений и собственного приложения, а также средств разработчика.  В этой статье описываются различные инструменты, которые следует использовать при разработке с помощью элементов управления WebView2.  

## Microsoft Edge DevTools  

Используйте [средства разработчика Microsoft EDGE (Chromium)](/microsoft-edge/devtools-guide-chromium) для отладки веб-содержимого, отображаемого в элементах управления WebView2, таким же образом, как и при использовании Microsoft Edge.  Чтобы открыть DevTools, установите фокус в окне WebView и воспользуйтесь одним из указанных ниже способов.  
*   Выберите `F12` .  
*   Выберите `Ctrl` + `Shift` + `I` .  
*   Откройте контекстное меню \ (щелкните правой кнопкой мыши, > выбрать `Inspect` .  

:::image type="complex" source="../media/f12.png" alt-text="Microsoft Edge DevTools":::
   Microsoft Edge DevTools  
:::image-end:::  

> [!NOTE]
> При отладке приложения в Visual Studio с присоединенным отладчиком машинного кода выбор `F12` может инициировать собственный отладчик вместо средств разработчика.  Использование `Ctrl` + `Shift` + `I` или использование контекстного меню \ (щелкните правой кнопкой мыши, чтобы избежать такой ситуации).  

## Visual Studio  

Используйте отладчик сценариев в Visual Studio 2019 версии 16,4 Preview 2 и более поздних версий для отладки сценария в Visual Studio.  Убедитесь, что компонент **диагностики JavaScript** установлен на **рабочем столе с** рабочей нагрузкой C++.  

:::image type="complex" source="../media/vs-js-diagnostics.jpg" alt-text="Диагностика JavaScript в Visual Studio":::
   Диагностика JavaScript в Visual Studio  
:::image-end:::  

<!--todo: Please update the image to use a red rectangle to outline the portion of the screen to highlight  -->  

Чтобы включить отладку сценариев WebView2, откройте контекстное меню в проекте, а затем щелкните правой кнопкой мыши > выберите пункт **Свойства**.  На вкладке **Свойства конфигурации**выберите пункт **Отладка**.  В свойстве **Type Debugger (тип отладчика** **) выберите JavaScript (WebView2)** в списке параметров. 

:::image type="complex" source="../media/vs-script-debugger.jpg" alt-text="Отладчик JavaScript для Visual Studio":::
   Отладчик JavaScript для Visual Studio  
:::image-end:::  

<!--todo: Please update the image to use a red rectangle to outline the portion of the screen to highlight  -->  

## Visual Studio Code  

Код Visual Studio можно использовать для отладки сценариев, которые выполняются в элементах управления WebView2.  Дополнительные сведения можно найти в разделе [приложения Microsoft EDGE (Chromium) WebView](https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications).  

<!--todo:  add See also heading  -->  

## Знакомство с командой Microsoft Edge WebView  

Помогите вам создать более WebView2ную работу, отправив свой отзыв.  Чтобы отправить запросы на функции или отчеты об ошибках, посетите [репозиторий обратной связи](https://aka.ms/webviewfeedback) .  
