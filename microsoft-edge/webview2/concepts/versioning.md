---
description: Модели управления версиями, используемые для Microsoft Edge WebView2
title: Управление версиями Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/22/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения WPF, WPF, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "браузер", HTML Edge
ms.openlocfilehash: acf3103f39d33586ee0614aeb0f10de0ab71c89a
ms.sourcegitcommit: b3555043e9d5aefa5a9e36ba4d73934d41559f49
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/23/2020
ms.locfileid: "10894314"
---
# Общие сведения о версиях SDK для WebView2  

WebView2 зависит от Microsoft Edge для функционирования.  Для каждого WebView2 SDK требуется, чтобы была установлена минимальная версия браузера.  Минимальная версия отражается в версии пакета SDK.  Например, если вы используете этот параметр `SDK package version 0.9.488` , необходимо установить Microsoft Edge с номером сборки 488 или более поздней.  Версия браузера также указывается в [заметках о выпуске][Releasenotes]WebView2.  Дополнительные сведения о последних выпусках браузера можно найти в разделе [каналы браузера][DeployedgeChannels].  

> [!NOTE]
> WebView2 в настоящее время является предварительной версией.  Несмотря на то, что группа WebView стремится обеспечить обратную совместимость между версиями браузеров и пакетами SDK, она не гарантируется, так как более поздние версии браузера могут не поддерживать предыдущие версии SDK.  Если между версиями браузеров и пакетами SDK есть коренные изменения, мы указываем изменения в [заметках о выпуске][Releasenotes].  

В будущем мы планируем изменить модель распределения для приложений WebView2.  Дополнительные сведения можно найти в разделе [Режим распространения Evergreen][DistributionEvergreenMode].  
 
## Пакет для выпуска и предварительной версии  

В предварительной версии пакет выпусков включает указанные ниже.  

*   [API C/C++ для Win32][ReferenceWin3209538]: API в SDK, которые должны оставаться прежними.  

В предварительной версии пакет предварительной версии включает следующие компоненты:  

*   API-интерфейсы .NET: [WPF][ReferenceWpf09515], [WinForms][ReferenceWinforms09515]и [ядро][ReferenceDotnet09538]  
*   Экспериментальные API.  Дополнительные сведения можно найти в разделе [экспериментальные API-интерфейсы](#experimental-apis) .  

## Экспериментальные API-интерфейсы  

Мы тестируем экспериментальные API, которые могут представлять будущие функции.  Экспериментальные API-интерфейсы помечены как `experimental` в SDK.  Экспериментальные API-интерфейсы могут поставляться в пакете выпуска как полностью стабильные API-интерфейсы.  Вы должны ожидать, что все экспериментальные API будут изменяться перед выпуском.  Пожалуйста, оцените экспериментальные API-интерфейсы и поделитесь отзывами с помощью [WebViewа обратной связи][GithubMicrosoftedgeWebviewfeedback].   

> [!CAUTION]
> Старайтесь не использовать экспериментальные API в производственных приложениях.  

## Стратегия  

После того как WebView2 пойдет в устойчивое общее доступное состояние, пакет выпуска включает все стабильные, поддерживаемые API Win32 C/C++ и .NET.  Пакет предварительной версии включает экспериментальные API-интерфейсы, которые изменяются на основе отзывов и общих аналитических приложений.  

<!--## Versioning  

After you have used a particular version of the SDK to build your app, your app may end up running with an older or newer version of installed browser binaries.  Until version 1.0.0.0 of WebView2 there may be breaking changes during updates that prevent your SDK from working with different versions of installed browser binaries.  After version 1.0.0.0, different versions of the SDK may work with different versions of the installed browser by using the following best practices.  

1.  To account for breaking changes to the API be sure to check for failure when requesting the DLL export `CreateCoreWebView2Environment` and when running `QueryInterface` on any `CoreWebView2` object.  A return value of `E_NOINTERFACE` indicates that the SDK is not compatible with the Microsoft Edge browser binaries.  
1.  Checking for failure from `QueryInterface` also accounts for cases where the SDK is newer than the version of the Microsoft Edge browser and your app attempts to use an interface of which the Microsoft Edge browser is unaware.  

1.  When an interface is unavailable, you may consider disabling the associated feature if possible, or otherwise informing your users to update their browsers.  -->  

<!--links -->

[DistributionEvergreenMode]: ./distribution.md#evergreen-distribution-mode "Режим распространения Evergreen — распространение приложений с помощью WebView2 | Документы Microsoft"  
[ReferenceDotnet09538]: ../reference/dotnet/0-9-538-reference-webview2.md "Ссылка (WebView2) | Документы Microsoft"  
[ReferenceWinforms09515]: ../reference/winforms/0-9-515-reference-webview2.md "Ссылка (WebView2) | Документы Microsoft"  
[ReferenceWin3209538]: ../reference/win32/0-9-538-reference-webview2.md "Ссылка (WebView2) | Документы Microsoft"  
[ReferenceWpf09515]: ../reference/wpf/0-9-515-reference-webview2.md "Ссылка (WebView2) | Документы Microsoft"  
[Releasenotes]: ../releasenotes.md "Заметки о выпуске для WebView2 SDK | Документы Microsoft"  

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Общие сведения о каналах Microsoft Edge | Документы Microsoft"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  
