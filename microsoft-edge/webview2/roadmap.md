---
description: Узнайте о том, что дальше в WebView2
title: План для Microsoft Edge WebView 2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/22/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 151eca3da5909b9d418451617b6bf09319752c55
ms.sourcegitcommit: 288bd2a1bec418a84d1f0bda013c1913886bd269
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/01/2020
ms.locfileid: "10844413"
---
# WebView2ная схема Microsoft Edge  

##### Последнее обновление: Май 2020  

Элемент управления WebView2 позволяет разработчикам внедрять веб-технологии в собственные приложения.  На следующей странице приведена схема перспективной схемы для WebView2.  

> [!NOTE]
> WebView2 находится в активном состоянии, а план продолжает развиваться, основываясь на изменениях рынка и отзывах пользователей, поэтому обратите внимание на то, что описанные здесь планы не являются исчерпывающими, и их может изменить.  

Если у вас возникли проблемы или вопросы о планах, оставьте отзыв в [репозитории обратной связи][GithubMicrosoftedgeWebviewfeedbackMain].  

Для будущих обновлений группа разработчиков WebView2 планирует следующие основные усилия.  

:::row:::
   :::column span="1":::
      Установщик среды выполнения WebView2  
   :::column-end:::
   :::column span="2":::
      *   4 квартал 2020
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Фиксированная версия  
   :::column-end:::
   :::column span="2":::
      *   4 квартал 2020  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      Общая доступность  
   :::column-end:::
   :::column span="2":::
      *   Win32 C/C++ \ (Q4 2020 \)  
      *   .NET \ (Q4 2020 \)  
      *   [WinUI 3,0][GithubMicrosoftUiXamlRoadmap]  
   :::column-end:::
:::row-end:::  

## Среда выполнения и установщик WebView2  

[Модель распространения Evergreen][ConceptDistributionEvergreenModel] позволяет целевому объекту или цепочке установить среду выполнения WebView2 на компьютер пользователя.  Предварительная версия среды выполнения WebView2 и установщика должна быть доступна Q3 2020 и Дж в Q4 2020.  

## Фиксированная версия  

С помощью [фиксированной модели распространения версий][ConceptsDistributionFixedVersionModel] можно упаковать двоичные файлы Microsoft EDGE в собственное приложение.  Инженерные задачи в настоящее время в предварительной версии не запланировались до конца Q3 2020 и Дж 4 квартала 2020.  

## Общая доступность  

### Win32 C/C++  

Пакет SDK для Win32 C/C++ должен быть в 4 квартале 2020 вскоре после среды выполнения WebView2 и установщика GA.  

### .NET  

.NET SDK упаковывает пакет SDK C/C++ для Win32.  Предполагается, что пакет .NET SDK вскоре скоро будет после того, как Win32 C/C++ GA в 4 квартале 2020.  

### WinUI 3,0  

Вы можете получить доступ к WebView2 в приложениях UWP с помощью [Win UI 3,0][UwpToolkitsWinui3Index], в настоящее время в Alpha.  Дополнительные сведения о том, как своевременно поддерживаться, можно найти в разделе [планы библиотеки пользовательского интерфейса Windows][GithubMicrosoftUiXamlRoadmap].  

<!-- links -->  

[ConceptDistributionEvergreenModel]: ./concepts/distribution.md#evergreen-distribution-mode "Модель распространения Evergreen — распространение приложений с помощью WebView2 | Документы Microsoft"  
[ConceptsDistributionFixedVersionModel]: ./concepts/distribution.md#fixed-version-distribution-mode "Стандартная модель распространения версий — распространение приложений с помощью WebView2 | Документы Microsoft"  

[UwpToolkitsWinui3Index]: /uwp/toolkits/winui3/index "Библиотека пользовательского интерфейса Windows 3,0 Preview 1 (Май 2020) | Документы Microsoft"  

[GithubMicrosoftedgeWebviewfeedbackMain]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  

[GithubMicrosoftUiXamlRoadmap]: https://github.com/microsoft/microsoft-ui-xaml/blob/master/docs/roadmap.md "План библиотеки пользовательского интерфейса Windows — Microsoft/Microsoft-UI-XAML | GitHub"  
