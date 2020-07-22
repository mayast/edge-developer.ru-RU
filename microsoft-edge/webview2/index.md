---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView 2
title: Элемент управления Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, CoreWebView2, ICoreWebView2Host, элементы управления браузером, EDGE HTML, Windows Forms, WinForms, WPF, .NET
ms.openlocfilehash: ea3d25d16aa9e8c182d564c68615b9643c9993b4
ms.sourcegitcommit: a82aa5fc1ada35cd8274490fbff3c0a850785835
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/21/2020
ms.locfileid: "10888600"
---
# Введение в Microsoft Edge WebView2 (Предварительная версия)  

Элемент управления Microsoft Edge WebView2 позволяет внедрять в собственные приложения веб-технологии \ (HTML, CSS и JavaScript).  Элемент управления WebView2 использует [Microsoft EDGE (Chromium)][MicrosoftedgeinsiderMain] в качестве обработчика обработки для отображения веб-содержимого в собственных приложениях.  С помощью WebView2 вы можете внедрить веб-код в различные части собственного приложения или создать для него приложение целиком в рамках одного WebView.  Сведения о том, как приступить к созданию приложения WebView2, можно найти в разделе Начало [работы](#getting-started).  

:::image type="complex" source="./media/WebView2/whatwebview.png" alt-text="Что такое WebView" lightbox="./media/WebView2/whatwebview.png":::
   Что такое WebView  
:::image-end:::  

> [!NOTE]
> Предварительная версия WebView2 предназначена для раннего создания прототипов и сбора отзывов, помогающих в создании API.  Вы не должны использовать предварительный просмотр в производственных приложениях, так как это может привести к коренным изменениям.  Дополнительные сведения можно найти в разделе [Webview2Releasenotes].  

## Подход к гибридным приложениям  

Разработчикам часто приходится определять создание веб-приложения или собственного приложения.  Решение на основе компромиссов между абонентами и возможностями.  Веб-приложения допускают широкий доступ к ним.  Как и веб-разработчик, вы можете использовать больше всего, если не все ваши коды на разных платформах.  Однако в собственных приложениях используются возможности всей платформы машинного кода.  

:::image type="complex" source="./media/WebView2/webnative.png" alt-text="Исходный веб-сайт" lightbox="./media/WebView2/webnative.png":::
   Исходный веб-сайт  
:::image-end:::  

Гибридные приложения позволяют разработчикам использовать преимущества обоих миров.  Разработчики гибридных приложений выигрывают от широкого и мощного веб-платформы, а также мощь и полную функциональность собственной платформы.  

## Преимущества WebView2   

:::image type="complex" source="./media/WebView2/webviewreasons.png" alt-text="Причины WebView" lightbox="./media/WebView2/webviewreasons.png":::
   Причины WebView  
:::image-end:::  

:::row:::
   :::column span="1":::
      **Веб-экосистема \ "&й навык"**  
      Используйте все веб-платформы, библиотеки, Инструментарий и все, что есть в веб-экосистеме.  
   :::column-end:::
   :::column span="1":::
      **Быстрые инновации**  
      Веб-разработки допускают более быстрые развертывание и итерации.  
   :::column-end:::
   :::column span="1":::
      **Поддержка Windows 7, 8, 10**  
      Поддержка согласованного взаимодействия с пользователем в Windows 7, 8 и 10.  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      **Собственные возможности**  
      Получить доступ к полному набору API для собственных интерфейсов.  
   :::column-end:::
   :::column span="1":::
      **Совместное использование кода**  
      Добавление веб-кода в базу кода для более высокой повторной работы на нескольких платформах.  
   :::column-end:::
   :::column span="1":::
      **Служба поддержки Майкрософт**  
      Корпорация Майкрософт предоставляет поддержку и добавляет новые запросы на доступ к функциям, когда WebView2 отпущена как завершенный.  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      **Распространение Evergreen**  
      Полагаться на обновленную версию Chromium с помощью регулярных обновлений платформы и исправлений для системы безопасности.  
   :::column-end:::
   :::column span="1":::
      **Исправлено** \ (скоро)  
      Выберите, чтобы упаковать биты Chromium в приложении.  
   :::column-end:::
   :::column span="1":::
      **Добавочное внедрение**  
      Добавление части веб-компонентов в приложение.  
   :::column-end:::
:::row-end:::

## Начало работы  

Чтобы создать и протестировать приложение с помощью элемента управления WebView2, необходимо установить [Microsoft EDGE (Chromium)][MicrosoftedgeinsiderDownload] и [WebView2 SDK][NugetPackagesMicrosoftWebWebView2] .  Чтобы приступить к работе, выберите один из следующих параметров.  

*   [Начало работы с Win32 C/C++][Webview2GettingstartedWin32]  
*   [Начало работы с WPF][Webview2GettingstartedWpf]  
*   [Приступая к работе с WinForms][Webview2GettingstartedWinforms]  
*   [Начало работы с WinUI3][Webview2GettingstartedWinui]  

В репозитории [примеров WebView2][GithubMicrosoftedgeWebview2samples] содержатся примеры, демонстрирующие все функции SDK WebView2 и использование API.  По мере добавления дополнительных функций в пакет SDK для WebView2, образцы приложений будут обновлены.  

## Поддерживаемые платформы  

Предварительный просмотр для разработчиков доступен в следующих средах программирования.  

*   Win32 C/C++  
*   .NET Framework 4.6.2 или более поздняя версия  
*   .NET Core 3,0 или более поздняя версия  
*   [WinUI 3,0][UwpToolkitsWinui3]  

Вы можете запускать приложения WebView2 в следующих версиях Windows.  

*   Windows 10;  
*   Windows 8.1  
*   Windows 8  
*   Windows 7  
*   WindowsServer2016  
*   Windows Server 2012  
*   Windows Server 2012R2  
*   Windows Server2008R2  

## Дальнейшие действия  

Дополнительные сведения о том, как создавать и развертывать приложения WebView2, можно узнать в концептуальной документации и руководствах.  

#### Понятия  

*   [Общие сведения о версиях SDK для WebView2][Webview2ConceptsVersioning]
*   [Распространение приложений с помощью WebView2][Webview2ConceptsDistribution]  
*   [Рекомендации по разработке защищенных приложений WebView2][Webview2ConceptsSecurity]
*   [Управление папкой "данные пользователя" в приложениях WebView2][Webview2ConceptsUserdatafolder]
 
#### Практические руководства  

*   [Отладка с помощью WebView2][Webview2HowtoDebug]  
*   [Автоматизация и тестирование WebView2 с помощью драйвера Microsoft Edge][Webview2HowtoWebdriver]  

## Связь с командой WebView2  

Помогите вам создать более WebView2ную работу, отправив свой отзыв.  Сведения о том, как отправлять запросы функций или отчеты об ошибках, можно найти в [репозитории WebView отзыв][GithubMicrosoftedgeWebviewfeddback] .  Кроме того, лучше всего искать известные проблемы.  

> [!NOTE]
> Во время предварительного просмотра мы собираем данные, которые помогут вам создать более качественный продукт.  Чтобы отключить сбор данных WebView2, перейдите к `edge://settings/privacy` коллекции данных браузера и отключите ее.  

<!-- links -->  

[Webview2ConceptsDistribution]: ./concepts/distribution.md "Распространение приложений с помощью WebView2 | Документы Microsoft"  
[Webview2ConceptsSecurity]: ./concepts/security.md "Рекомендации по разработке безопасных приложений WebView2 | Документы Microsoft"  
[Webview2ConceptsUserdatafolder]: ./concepts/userdatafolder.md "Управление папкой "данные пользователя" | Документы Microsoft"  
[Webview2ConceptsVersioning]: ./concepts/versioning.md "Общие сведения о версиях SDK для WebView2 | Документы Microsoft"  
[Webview2GettingstartedWin32]: ./gettingstarted/win32.md "Начало работы с WebView2 (Предварительная версия для разработчиков) | Документы Microsoft"   
[Webview2GettingstartedWinforms]: ./gettingstarted/winforms.md "Начало работы с WebView2 в приложениях для Windows Forms (Предварительная версия) | Документы Microsoft"  
[Webview2GettingstartedWinui]: ./gettingstarted/winui.md "Начало работы с WebView2 в WinUI3 (Предварительная версия) | Документы Microsoft"  
[Webview2GettingstartedWpf]: ./gettingstarted/wpf.md "Начало работы с WebView2 в WPF (Предварительная версия) | Документы Microsoft"  
[Webview2HowtoDebug]: ./howto/debug.md "Отладка с помощью WebView2 | Документы Microsoft"  
[Webview2HowtoWebdriver]: ./howto/webdriver.md "Автоматизация и тестирование WebView2 с помощью драйвера Microsoft Edge | Документы Microsoft"  
[Webview2Releasenotes]: ./releasenotes.md "Заметки о выпуске WEBVIEW2RELEASENOTES для WebView2 SDK | Документы Microsoft"  

[UwpToolkitsWinui3]: ./gettingstarted/winui.md "Библиотека пользовательского интерфейса Windows 3 Preview (2020 июля) | Документы Microsoft"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeddback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback-MicrosoftEdge/WebViewFeedback | GitHub" 

[MicrosoftedgeinsiderMain]: https://www.microsoftedgeinsider.com "Предварительная оценка Microsoft Edge"  
[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Загрузить программу предварительной оценки Microsoft Edge"  

[NugetPackagesMicrosoftWebWebView2]: https://www.nuget.org/packages/Microsoft.Web.WebView2 "Microsoft. Web. WebView2 | Коллекция NuGet"  
