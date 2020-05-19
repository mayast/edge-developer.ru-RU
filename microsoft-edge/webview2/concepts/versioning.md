---
description: Модели управления версиями, используемые для Microsoft Edge WebView2
title: Управление версиями Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/19/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения WPF, WPF, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "браузер", HTML Edge
ms.openlocfilehash: 78184d3c670aa39e0a7f4a31e1216b5bc730c16e
ms.sourcegitcommit: 5bdffe91a6594f77eeffa4e864fda90a02784771
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/19/2020
ms.locfileid: "10659673"
---
# Сведения о версиях браузеров и WebView2  

WebView2 зависит от Microsoft Edge для функционирования.  Для каждого WebView2 SDK требуется, чтобы была установлена минимальная версия браузера.  Эта версия браузера указана в [заметках о выпуске][Webview2Releasenotes].  Минимальная версия может отображаться в версии пакета SDK.  Например, если вы используете этот параметр `SDK package version 0.9.488` , необходимо установить Microsoft Edge с номером сборки 488 или более поздней.  Дополнительные сведения о последних выпусках браузера можно найти в разделе [каналы браузера][DeployedgeChannels].  

> [!NOTE]
> WebView2 в настоящее время является предварительной версией.  Несмотря на то, что группа Microsoft Edge WebView гарантирует обратную совместимость между версиями браузеров и пакетами SDK, это не гарантирует, что некоторые более поздние версии браузера могут не поддерживать старые версии SDK.  Если между версиями браузеров и пакетами SDK есть коренные изменения, группа Microsoft Edge WebView указывает изменения в [заметках о выпуске][Webview2Releasenotes].  

В будущем группа Microsoft Edge WebViews планирует изменить модель распространения.  Microsoft Edge WebView Teams, чтобы удалить прямую зависимость в браузере Microsoft Edge из WebView2.  Дополнительные сведения можно найти в разделе [распространение][Webview2Distibution] [среды выполнения WebView2][Webview2IndexEdgeRuntime] .  

## Экспериментальные API-интерфейсы  

Несмотря на то, что WebView2 является предварительным просмотром, для API в пакете SDK должны оставаться одинаковыми.  В пакет SDK включены [экспериментальные API][Webview2ReferenceWin3209488Experimental] .  Пожалуйста, оцените экспериментальные API-интерфейсы и отправьте отзыв с помощью [репозитория обратной связи WebView][GithubMicrosoftedgeWebviewfeedback].  

### Стратегия  

После того как WebView2 пойдет в устойчивое общее состояние, и мы выпустим пакет 1.0.0 SDK, планы Microsoft Edge WebView Teams, чтобы переместить все экспериментальные API в предварительную версию пакета.  Предварительная версия пакета продолжает разрешать отзыв и сведения о новейших функциях, в то время как в стабильном выпуске поддерживается обратная совместимость.  

<!--links -->

[Webview2Distibution]: ./distribution.md "Распространение приложений с помощью WebView2 | Документы Microsoft"  
[Webview2IndexEdgeRuntime]: ./distribution.md#microsoft-edge-webview2-runtime "Microsoft Edge WebView2-распространение приложений с помощью WebView2 | Документы Microsoft"  
[Webview2ReferenceWin3209488Experimental]: ../reference/win32/0-9-488-reference-webview2.md#experimental "Экспериментальный справочник (WebView2) | Документы Microsoft"  
[Webview2Releasenotes]: ../releasenotes.md "Заметки о выпуске для WebView2 SDK | Документы Microsoft"  

[DeployedgeChannels]: /deployedge/microsoft-edge-channels "Общие сведения о каналах Microsoft Edge | Документы Microsoft"  

[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  
