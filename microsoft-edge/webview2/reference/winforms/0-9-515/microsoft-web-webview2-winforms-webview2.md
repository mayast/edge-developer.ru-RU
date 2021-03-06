---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. WinForms. WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: 7d707c2a6ecb8127074735f06ba6d4f1f28eea0c
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879452"
---
# Класс Microsoft. Web. WebView2. WinForms. WebView2 

Пространство имен: Microsoft. Web. WebView2. WinForms \
Сборка: Microsoft.Web.WebView2.WinForms.dll

```
class Microsoft.Web.WebView2.WinForms.WebView2
  : public Control
```

Элемент управления для внедрения WebView2 в WinForms.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[ContentLoading](#contentloading) | ContentLoading отправляется после того, как начинается переход с нового URI и начинается визуализация содержимого этого URI.
[CoreWebView2Ready](#corewebview2ready) | Это событие запускается, когда [CoreWebView2](#corewebview2) элемента управления завершает инициализацию (независимо от того, как был инициирована инициализация), но до того, как он будет использоваться для чего-либо.
[NavigationCompleted](#navigationcompleted) | NavigationCompleted отправляется после того, как переход по документу верхнего уровня завершает обработку успешно или нет.
[NavigationStarting](#navigationstarting) | NavigationStarting отправляется перед началом новой навигации для документа верхнего уровня в WebView2.
[SourceChanged](#sourcechanged) | SourceChanged отправляется после изменения исходного свойства.
[WebMessageReceived](#webmessagereceived) | WebMessageReceived отправляет сообщение на узел приложения с помощью отправки по сети `chrome.webview.postMessage` .
[CoreWebView2](#corewebview2) | Основной CoreWebView2.
[Источник](#source) | Свойство Source — это URI документа верхнего уровня в WebView2.
[ZoomFactor](#zoomfactor) | Коэффициент масштабирования для WebView.
[CanGoBack](#cangoback) | Возвращает значение истина, если WebView может перейти на предыдущую страницу в истории навигации с помощью метода GoBack.
[CanGoForward](#cangoforward) | Возвращает значение "истина", если WebView может перейти к следующей странице в журнале переходов с помощью метода GoForward.
[EnsureCoreWebView2Async](#ensurecorewebview2async) | Явным образом инициализируйте инициализацию [CoreWebView2](#corewebview2)элемента управления.
[ExecuteScriptAsync](#executescriptasync) | Выполняет представленный сценарий в документе верхнего уровня элемента WebView2.
[GoBack](#goback) | Переход на предыдущую страницу в истории навигации.
[GoForward](#goforward) | Переход к следующей странице в журнале переходов.
[NavigateToString](#navigatetostring) | Обрабатывают представленный HTML-код как документ верхнего уровня для элемента WebView2.
[Перезагрузить](#reload) | Перезагрузите документ верхнего уровня в WebView2.
[Stop](#stop) | Остановите ход выполнения навигации в WebView2.
[WebView2](#webview2) | Создайте новый элемент управления WebView2 WinForms.

## Участников

#### ContentLoading 

ContentLoading отправляется после того, как начинается переход с нового URI и начинается визуализация содержимого этого URI.

> событие EventHandler< CoreWebView2ContentLoadingEventArgs > [ContentLoading](#contentloading)

Это эквивалентно событию ContentLoading в CoreWebView2. Более подробную информацию вы увидите в документации CoreWebView2. ContentLoading.

#### CoreWebView2Ready 

Это событие запускается, когда [CoreWebView2](#corewebview2) элемента управления завершает инициализацию (независимо от того, как был инициирована инициализация), но до того, как он будет использоваться для чего-либо.

> событие EventHandler< EventArgs > [CoreWebView2Ready](#corewebview2ready)

Вы должны обработать это событие, если вам необходимо выполнить одну операцию настройки в CoreWebView2, которая будет применяться ко всем их использованию (например, добавлять обработчики событий, настраивать параметры, устанавливать сценарии создания документов, добавлять объекты узла).

Это событие не предоставляет никаких аргументов, а отправитель — элемент управления WebView2, чье свойство CoreWebView2 теперь будет действительно допустимым (то есть не NULL) в первый раз.

#### NavigationCompleted 

NavigationCompleted отправляется после того, как переход по документу верхнего уровня завершает обработку успешно или нет.

> событие EventHandler< CoreWebView2NavigationCompletedEventArgs > [NavigationCompleted](#navigationcompleted)

Это эквивалентно событию NavigationCompleted в CoreWebView2. Более подробную информацию вы увидите в документации CoreWebView2. NavigationCompleted.

#### NavigationStarting 

NavigationStarting отправляется перед началом новой навигации для документа верхнего уровня в WebView2.

> событие EventHandler< CoreWebView2NavigationStartingEventArgs > [NavigationStarting](#navigationstarting)

Это эквивалентно событию NavigationStarting в CoreWebView2. Более подробную информацию вы увидите в документации CoreWebView2. NavigationStarting.

#### SourceChanged 

SourceChanged отправляется после изменения исходного свойства.

> событие EventHandler< CoreWebView2SourceChangedEventArgs > [SourceChanged](#sourcechanged)

Это может происходить во время навигации или в случае, если сценарий на странице изменяет URI документа. Это эквивалентно событию SourceChanged в CoreWebView2. Более подробную информацию вы увидите в документации CoreWebView2. SourceChanged.

#### WebMessageReceived 

WebMessageReceived отправляет сообщение на узел приложения с помощью отправки по сети `chrome.webview.postMessage` .

> событие EventHandler< CoreWebView2WebMessageReceivedEventArgs > [WebMessageReceived](#webmessagereceived)

Это эквивалентно событию WebMessageReceived в CoreWebView2. Более подробную информацию вы увидите в документации CoreWebView2. WebMessageReceived.

#### CoreWebView2 

Основной CoreWebView2.

> общедоступная CoreWebView2 [CoreWebView2](#corewebview2)

Это свойство используется для выполнения дополнительных операций с содержимым WebView2, чем представлено в WebView2. Это значение равно null, пока оно не будет инициализировано. Вы можете принудительно инициализировать базовый CoreWebView2 с помощью метода InitializeAsync.

#### Источник 

Свойство Source — это URI документа верхнего уровня в WebView2.

> общедоступный [источник](#source) URI

Установка источника эквивалентна вызову CoreWebView2. Navigate. Если базовый CoreWebView2 еще не инициализирован, это свойство имеет значение about: blank. Если для свойства задан неабсолютный URI или пустое значение, свойство остается неизменным. Дополнительные сведения вы видите в CoreWebView2. навигации по документации.

#### ZoomFactor 

Коэффициент масштабирования для WebView.

> общедоступная двойная [ZoomFactor](#zoomfactor)

#### CanGoBack 

Возвращает значение истина, если WebView может перейти на предыдущую страницу в истории навигации с помощью метода GoBack.

> Открытый логический [CanGoBack](#cangoback)

Это эквивалентно свойству CanGoBack в CoreWebView2. Если базовый CoreWebView2 еще не инициализирован, это свойство имеет значение false. Более подробную информацию вы увидите в документации CoreWebView2. CanGoBack.

#### CanGoForward 

Возвращает значение "истина", если WebView может перейти к следующей странице в журнале переходов с помощью метода GoForward.

> Открытый логический [CanGoForward](#cangoforward)

Это эквивалентно свойству CanGoForward в CoreWebView2. Если базовый CoreWebView2 еще не инициализирован, это свойство имеет значение false. Более подробную информацию вы увидите в документации CoreWebView2. CanGoForward.

#### EnsureCoreWebView2Async 

Явным образом инициализируйте инициализацию [CoreWebView2](#corewebview2)элемента управления.

> общедоступная задача [EnsureCoreWebView2Async](#ensurecorewebview2async)(среда CoreWebView2Environment)

##### Параметры
* `environment` Предварительно созданный CoreWebView2Environment, который должен использоваться для создания CoreWebView2. Создание собственной среды позволяет управлять несколькими параметрами, которые влияют на то, как CoreWebView2 инициализируется. Если вы передаете null (значение по умолчанию), среда по умолчанию будет создана и использоваться автоматически. 

##### Дает
Задача, представляющая собой процесс инициализации фона. После завершения задачи свойство CoreWebView2 будет доступно для использования (то есть без значения NULL). Обратите внимание, что событие [CoreWebView2Ready](#corewebview2ready) элемента управления будет вызвано до завершения задачи. 

Повторный вызов этого метода не повлияет (любая указанная среда игнорируется) и возвращает ту же задачу, что и первый вызов. Вызов этого метода после того, как инициализация вызывается явным образом посредством задания свойства [Source](#source) , не будет оказывать никакого воздействия (любая указанная среда игнорируется) и просто возвращать задачу, представляющую уже выполняющуюся инициализацию. 

##### Исключения
* `System.InvalidOperationException` Вызывается при вызове из потока, не относящегося к пользовательскому интерфейсу.

#### ExecuteScriptAsync 

Выполняет представленный сценарий в документе верхнего уровня элемента WebView2.

> общедоступная асинхронная задача< String > [ExecuteScriptAsync](#executescriptasync)(строковый сценарий)

Это эквивалентно методу ExecuteScriptAsync в CoreWebView2. Если базовый CoreWebView2 еще не инициализирован, этот метод создает исключение InvalidOperationException. Более подробную информацию вы видите в CoreWebView2.Exeдокументации cuteScriptAsync.

#### GoBack 

Переход на предыдущую страницу в истории навигации.

> общедоступная void [GoBack](#goback)()

Это эквивалентно методу GoBack для CoreWebView2. Если базовый CoreWebView2 еще не инициализирован, этот метод не выполняет никаких действий. Более подробную информацию вы увидите в документации по CoreWebView2. GoBack.

#### GoForward 

Переход к следующей странице в журнале переходов.

> общедоступная void [GoForward](#goforward)()

Это эквивалентно методу GoForward в CoreWebView2. Если базовый CoreWebView2 еще не инициализирован, этот метод не выполняет никаких действий. Более подробную информацию вы увидите в документации CoreWebView2. GoForward.

#### NavigateToString 

Обрабатывают представленный HTML-код как документ верхнего уровня для элемента WebView2.

> Public void [NavigateToString](#navigatetostring)(строка htmlContent)

Это эквивалентно методу NavigateToString в CoreWebView2. Если базовый CoreWebView2 еще не инициализирован, этот метод создает исключение InvalidOperationException. Более подробную информацию вы увидите в документации CoreWebView2. NavigateToString.

#### Перезагрузить 

Перезагрузите документ верхнего уровня в WebView2.

> общедоступный void [Reload](#reload)()

Это эквивалентно методу Reload для CoreWebView2. Если базовый CoreWebView2 еще не инициализирован, этот метод создает исключение InvalidOperationException. Дополнительные сведения смотрите в разделе CoreWebView2. повторно загрузите документацию.

#### Stop 

Остановите ход выполнения навигации в WebView2.

> открытая пустая [Отмена](#stop)()

Это эквивалентно методу Stop в CoreWebView2. Если базовый CoreWebView2 еще не инициализирован, этот метод не выполняет никаких действий. Для получения дополнительных сведений ознакомьтесь со статьей CoreWebView2.

#### WebView2 

Создайте новый элемент управления WebView2 WinForms.

> общедоступная [WebView2](#webview2)()

После создания свойство CoreWebView2 имеет значение null. Вызовите [EnsureCoreWebView2Async](#ensurecorewebview2async) , чтобы инициализировать базовый CoreWebView2.

