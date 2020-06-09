---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView 2
title: Элемент управления Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/21/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, CoreWebView2, ICoreWebView2Host, элементы управления браузером, EDGE HTML, Windows Forms, WinForms, WPF, .NET
ms.openlocfilehash: 1b140d9f644c7a864cac4966bb4cfdd400feeb0d
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697744"
---
# Введение в Microsoft Edge WebView2 (Предварительная версия)  

Элемент управления Microsoft Edge WebView2 позволяет внедрять в собственные приложения веб-технологии \ (HTML, CSS и JavaScript).  Элемент управления WebView2 использует [Microsoft EDGE (Chromium)](https://www.microsoftedgeinsider.com) в качестве обработчика обработки для отображения веб-содержимого в собственных приложениях.  С помощью WebView2 вы можете внедрить веб-код в различные части собственного приложения или создать для него приложение целиком в рамках одного WebView.  Сведения о том, как приступить к созданию приложения WebView2, можно найти в разделе Начало [работы](./index.md#getting-started).  

:::image type="complex" source="./media/WebView2/whatwebview.png" alt-text="Что такое WebView":::
   Что такое WebView  
:::image-end:::  

> [!NOTE]
> Предварительная версия WebView2 предназначена для раннего создания прототипов и сбора отзывов, помогающих в создании API.  Группа Microsoft Edge WebView не рекомендует использовать предварительный просмотр в производственных приложениях, так как это может привести к [коренным изменениям](./releasenotes.md).  

## Подход к гибридным приложениям  

Разработчикам часто приходится выбирать между созданием веб-приложения или собственного приложения.  Решение на основе компромиссов между абонентами и возможностями.  Веб-приложения допускают широкий доступ к ним.  Как и веб-разработчик, вы можете использовать больше всего, если не все ваши коды на разных платформах.  Однако в собственных приложениях используются возможности всей платформы машинного кода.  

:::image type="complex" source="./media/WebView2/webnative.png" alt-text="Исходный веб-сайт":::
   Исходный веб-сайт  
:::image-end:::  

Гибридные приложения позволяют разработчикам использовать преимущества обоих миров.  Разработчики гибридных приложений выигрывают от широкого и мощного веб-платформы, а также мощь и полную функциональность собственной платформы.  

## Преимущества WebView2   

:::image type="complex" source="./media/WebView2/webviewreasons.png" alt-text="Причины WebView":::
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

Чтобы создать и протестировать приложение с помощью элемента управления WebView2, необходимо установить [Microsoft EDGE (Chromium)](https://www.microsoftedgeinsider.com/download) и [WebView2 SDK](https://aka.ms/webviewnuget) .  Чтобы приступить к работе, выберите один из следующих параметров.  

*   [Начало работы с Win32 C/C++](./gettingstarted/win32.md)  
*   [Начало работы с WPF](./gettingstarted/wpf.md)  
*   [Приступая к работе с WinForms](./gettingstarted/winforms.md)  

В репозитории [примеров WebView2](https://github.com/MicrosoftEdge/WebView2Samples) содержатся примеры, демонстрирующие все функции WebView2 SDK и модели использования API. По мере добавления дополнительных функций в пакет SDK для WebView2, образцы приложений будут обновлены.   

## Поддерживаемые платформы  

Предварительный просмотр для разработчиков доступен в следующих средах программирования.  

*   Win32 C/C++  
*   .NET Framework 4.6.2 или более поздняя версия  
*   .NET Core 3,0 или более поздняя версия  
*   [WinUI 3,0](/uwp/toolkits/winui3/)  

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

Более подробную информацию о том, как создавать и развертывать приложения WebView2, вывлекать концептуальную документацию и практические руководства.  

#### Понятия  

*   [WebView2 SDK и Microsoft Edge Versions](./concepts/versioning.md)
*   [Распространение приложений WebView2](./concepts/distribution.md)  
 
#### Практические руководства  

*   [Отладка WebView2 с помощью DevTools и Visual Studio, отладка скриптов](./howto/debug.md)  
*   [Автоматизация и отладка WebView2 с помощью Microsoft EdgeDriver](./howto/webdriver.md)  

<!--todo: add how-tos when available  -->  

## Связь с командой WebView2  

Помогите вам создать более WebView2ную работу, отправив свой отзыв.  Чтобы отправить запросы на функции или отчеты об ошибках, посетите [репозиторий обратной связи](https://aka.ms/webviewfeedback) WebView.  Кроме того, лучше всего искать известные проблемы.  

> [!NOTE]
> В предварительной версии для разработчиков группа Microsoft Edge WebView также собирает данные, которые помогут вам создать более подWebView.  Пользователи могут отключить сбор данных WebView, перейдя `edge://settings/privacy` в браузер Microsoft EDGE и отключив коллекцию данных браузера.  
