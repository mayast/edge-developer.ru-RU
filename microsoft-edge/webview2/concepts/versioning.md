---
description: Модели управления версиями, используемые для Microsoft Edge WebView2
title: Управление версиями Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/22/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения WPF, WPF, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "браузер", HTML Edge
ms.openlocfilehash: 3862576134d1179fb24b2ce865f705b2bf1db8a6
ms.sourcegitcommit: de171a8e7ccd9f23846f3cd06519e4a0104f1c52
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/23/2020
ms.locfileid: "10757608"
---
# Общие сведения о версиях SDK для WebView2  

WebView2 зависит от Microsoft Edge для функционирования. Для каждого WebView2 SDK требуется, чтобы была установлена минимальная версия браузера.  Минимальная версия отражается в версии пакета SDK.  Например, если вы используете этот параметр `SDK package version 0.9.488` , необходимо установить Microsoft Edge с номером сборки 488 или более поздней. Версия браузера также указывается в [заметках о выпуске][Webview2Releasenotes]WebView2.  Дополнительные сведения о последних выпусках браузера можно найти в разделе [каналы браузера][DeployedgeChannels].  

> [!NOTE]
> WebView2 в настоящее время является предварительной версией.  Несмотря на то, что группа Microsoft Edge WebView гарантирует обратную совместимость между версиями браузеров и пакетами SDK, это не гарантирует, что некоторые более поздние версии браузера могут не поддерживать старые версии SDK.  Если между версиями браузеров и пакетами SDK есть коренные изменения, группа Microsoft Edge WebView указывает изменения в [заметках о выпуске][Webview2Releasenotes].  

В будущем модель распределения для WebView2 приложений изменится. Дополнительные сведения можно найти в разделе [Среда выполнения WebView2][Webview2IndexEdgeRuntime].  
 
## Пакет для выпуска и предварительной версии  

В предварительной версии пакет выпусков включает указанные ниже.  

*   [API C/C++ для Win32][Webview2ReferenceWin3209538]: API в SDK, которые должны оставаться прежними. 

В предварительной версии пакет предварительной версии включает указанные ниже.  

*   API-интерфейсы .NET: [WPF][Webview2ReferenceWpf09515], [WinForms][Webview2ReferenceWinforms09515]и [ядро][Webview2ReferenceDotnet09538]
*   Экспериментальные API.  Дополнительные сведения можно найти в разделе [API Experimantal](#experimental-apis) .  

### Экспериментальные API-интерфейсы  

Группа WebView тестирует API-интерфейсы, которые представляют собой будущие функции, названные экспериментальными API.  Экспериментальные API-интерфейсы помечены как `experimental` в SDK.  Некоторые экспериментальные API-интерфейсы могут поставляться в пакете выпуска как полностью стабильные API-интерфейсы.  Вы должны ожидать, что все экспериментальные API будут изменяться перед выпуском.  Пожалуйста, оцените экспериментальные API-интерфейсы и поделитесь отзывами с помощью [WebViewа обратной связи][GithubMicrosoftedgeWebviewfeedback].   

> [!CAUTION]
> Старайтесь не использовать экспериментальные API в производственных приложениях.  

### Стратегия  

После того как WebView2 пойдет в устойчивое общее доступное состояние, пакет выпуска включает все стабильные, поддерживаемые API Win32 C/C++ и .NET.  Пакет предварительной версии включает экспериментальные API-интерфейсы, которые изменяются на основе отзывов и общих аналитических приложений.  

<!--links -->

[Webview2IndexEdgeRuntime]: ./distribution.md#microsoft-edge-webview2-runtime "Microsoft Edge WebView2-распространение приложений с помощью WebView2 | Документы Microsoft"  
[Webview2ReferenceDotnet09538]: ../reference/dotnet/0-9-538-reference-webview2.md "Ссылка (WebView2) | Документы Microsoft"  
[Webview2ReferenceWinforms09515]: ../reference/winforms/0-9-515-reference-webview2.md "Ссылка (WebView2) | Документы Microsoft"  
[Webview2ReferenceWin3209538]: ../reference/win32/0-9-538-reference-webview2.md "Ссылка (WebView2) | Документы Microsoft"  
[Webview2ReferenceWpf09515]: ../reference/wpf/0-9-515-reference-webview2.md "Ссылка (WebView2) | Документы Microsoft"  
[Webview2Releasenotes]: ../releasenotes.md "Заметки о выпуске для WebView2 SDK | Документы Microsoft"  

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Общие сведения о каналах Microsoft Edge | Документы Microsoft"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  
