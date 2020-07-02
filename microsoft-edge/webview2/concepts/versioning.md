---
description: Модели управления версиями, используемые для Microsoft Edge WebView2
title: Управление версиями Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения WPF, WPF, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "браузер", HTML Edge
ms.openlocfilehash: 059bbeb34f372af0cef944e484599c0b50543cc9
ms.sourcegitcommit: 288bd2a1bec418a84d1f0bda013c1913886bd269
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/01/2020
ms.locfileid: "10844427"
---
# Общие сведения о версиях SDK для WebView2  

WebView2 зависит от Microsoft Edge для функционирования.  Для каждого WebView2 SDK требуется, чтобы была установлена минимальная версия браузера.  Минимальная версия отражается в версии пакета SDK.  Например, если вы используете этот параметр `SDK package version 0.9.488` , необходимо установить Microsoft Edge с номером сборки 488 или более поздней.  Версия браузера также указывается в [заметках о выпуске][Releasenotes]WebView2.  Дополнительные сведения о последних выпусках браузера можно найти в разделе [каналы браузера][DeployedgeChannels].  

> [!NOTE]
> WebView2 в настоящее время является предварительной версией.  Несмотря на то, что группа WebView стремится обеспечить обратную совместимость между версиями браузеров и пакетами SDK, она не гарантируется, так как более поздние версии браузера могут не поддерживать более ранние версии SDK.  Если между версиями браузеров и пакетами SDK есть коренные изменения, Группа WebView указывает изменения в [заметках о выпуске][Releasenotes].  

В будущем группа WebView планирует изменить модель распределения для WebView2 приложений.  Дополнительные сведения можно найти в разделе Просмотр [режима распространения Evergreen][DistributionEvergreenMode].  
 
## Пакет для выпуска и предварительной версии  

В предварительной версии пакет выпусков включает указанные ниже.  

*   [API C/C++ для Win32][ReferenceWin3209538]: API в SDK, которые должны оставаться прежними. 

В предварительной версии пакет предварительной версии включает следующие компоненты:  

*   API-интерфейсы .NET: [WPF][ReferenceWpf09515], [WinForms][ReferenceWinforms09515]и [ядро][ReferenceDotnet09538]
*   Экспериментальные API.  Дополнительные сведения можно найти в разделе [экспериментальные API-интерфейсы](#experimental-apis) .  

### Экспериментальные API-интерфейсы  

Группа WebView тестирует API-интерфейсы, которые представляют собой будущие функции, названные экспериментальными API.  Экспериментальные API-интерфейсы помечены как `experimental` в SDK.  Некоторые экспериментальные API-интерфейсы могут поставляться в пакете выпуска как полностью стабильные API-интерфейсы.  Вы должны ожидать, что все экспериментальные API будут изменяться перед выпуском.  Пожалуйста, оцените экспериментальные API-интерфейсы и поделитесь отзывами с помощью [WebViewа обратной связи][GithubMicrosoftedgeWebviewfeedback].   

> [!CAUTION]
> Старайтесь не использовать экспериментальные API в производственных приложениях.  

### Стратегия  

После того как WebView2 пойдет в устойчивое общее доступное состояние, пакет выпуска включает все стабильные, поддерживаемые API Win32 C/C++ и .NET.  Пакет предварительной версии включает экспериментальные API-интерфейсы, которые изменяются на основе отзывов и общих аналитических приложений.  

<!--links -->

[DistributionEvergreenMode]: ./distribution.md#evergreen-distribution-mode "Режим распространения Evergreen — распространение приложений с помощью WebView2 | Документы Microsoft"  
[ReferenceDotnet09538]: ../reference/dotnet/0-9-538-reference-webview2.md "Ссылка (WebView2) | Документы Microsoft"  
[ReferenceWinforms09515]: ../reference/winforms/0-9-515-reference-webview2.md "Ссылка (WebView2) | Документы Microsoft"  
[ReferenceWin3209538]: ../reference/win32/0-9-538-reference-webview2.md "Ссылка (WebView2) | Документы Microsoft"  
[ReferenceWpf09515]: ../reference/wpf/0-9-515-reference-webview2.md "Ссылка (WebView2) | Документы Microsoft"  
[Releasenotes]: ../releasenotes.md "Заметки о выпуске для WebView2 SDK | Документы Microsoft"  

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Общие сведения о каналах Microsoft Edge | Документы Microsoft"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  
