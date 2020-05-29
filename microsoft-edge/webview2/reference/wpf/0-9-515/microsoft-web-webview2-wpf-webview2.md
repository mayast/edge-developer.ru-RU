---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/27/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: a0030e1a2a77d65963bd8333f2071485ab2fe308
ms.sourcegitcommit: 83efa259be89cc773a82751242495a0a919d54cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2020
ms.locfileid: "10687799"
---
# Класс Microsoft. Web. WebView2. WPF. WebView2 

Пространство имен: Microsoft. Web. WebView2. WPF \
Сборка: Microsoft. Web. WebView2. WPF. dll

```
class Microsoft.Web.WebView2.Wpf.WebView2
  : public HwndHost
```

Элемент управления для внедрения веб-содержимого в приложение WPF.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[ContentLoading](#contentloading) | Обертка для события CoreWebView2. ContentLoading в CoreWebView2.
[CoreWebView2Ready](#corewebview2ready) | Это событие запускается, когда CoreWebView2 элемента управления завершает инициализацию (независимо от того, как был инициирована инициализация), но до того, как он будет использоваться для чего-либо.
[NavigationCompleted](#navigationcompleted) | Обертка для события CoreWebView2. NavigationCompleted в CoreWebView2.
[NavigationStarting](#navigationstarting) | Обертка для события CoreWebView2. NavigationStarting в CoreWebView2.
[SourceChanged](#sourcechanged) | Обертка для события CoreWebView2. SourceChanged в CoreWebView2.
[WebMessageReceived](#webmessagereceived) | Обертка для события CoreWebView2. WebMessageReceived в CoreWebView2.
[CanGoBack](#cangoback) | Возвращает значение "истина", если WebView может перейти к предыдущей странице в журнале переходов.
[CanGoForward](#cangoforward) | Возвращает значение "истина", если WebView может перейти к следующей странице в журнале переходов.
[CoreWebView2](#corewebview2) | Получить доступ ко всем функциональным возможностям базового API Core. CoreWebView2.
[CreationProperties](#creationproperties) | Возвращает или задает набор параметров, которые используются при инициализации CoreWebView2 элемента управления.
[Источник](#source) | Универсальный код ресурса (URI) верхнего уровня, который в данный момент отображает WebView (или будет отображаться после инициализации его CoreWebView2).
[EnsureCoreWebView2Async](#ensurecorewebview2async) | Явным образом инициализируйте инициализацию CoreWebView2 элемента управления.
[ExecuteScriptAsync](#executescriptasync) | Выполняет код JavaScript из параметра javaScript в текущем документе верхнего уровня, отображаемом в WebView.
[GoBack](#goback) | Переход по WebView на предыдущую страницу в истории навигации.
[GoForward](#goforward) | Переход по WebView к следующей странице в истории навигации.
[NavigateToString](#navigatetostring) | Запускает навигацию для htmlContent в качестве исходного HTML-кода нового документа.
[Перезагрузить](#reload) | Перезагружает текущую страницу.
[Stop](#stop) | Остановка всех переходов и ожидающих выборок ресурсов.
[WebView2](#webview2) | Создает новый экземпляр элемента управления WebView2.

Этот элемент управления — это программа-оболочка для API WebView2, в которой можно найти документацию по этому адресу: [https://aka.ms/webview2](https://aka.ms/webview2) вы можете напрямую получить доступ к основному интерфейсу ICoreWebView2 и ко всем его функциональным возможностям с помощью свойства CoreWebView2. Некоторые из наиболее распространенных функциональных возможностей COM также доступны непосредственно через методы оболочки, свойства и события в элементе управления.

После создания свойство CoreWebView2 элемента управления будет иметь значение null. Это связано с тем, что создание CoreWebView2 является дорогостоящей операцией, которая включает в себя такие вещи, как запуск процессов браузеров Edge. Существует два способа создания CoreWebView2:1) вызовите метод EnsureCoreWebView2Async. Это называется явной инициализацией. 2) задайте свойство Source (например, это может быть выполнено из разметки). Это называется неявной инициализацией. Любой из вариантов начнет инициализацию в фоновом режиме и вернется к вызывающему абоненту, не дожидаясь завершения. Чтобы задать параметры, касающиеся процесса инициализации, перед инициализацией следует либо передать собственный CoreWebView2Environment EnsureCoreWebView2Async, либо задать свойство CreationProperties элемента управления до инициализации.

После завершения инициализации (независимо от того, как она была активирована), произойдет следующее: 1) будет вызвано событие CoreWebView2Ready элемента управления. Если вам необходимо выполнить одну из операций настройки в CoreWebView2 перед ее использованием, необходимо сделать это в обработчике для этого события. 2) Если для универсального кода ресурса (URI) задано значение свойства Source, элемент управления начнет переход к нему в фоновом режиме (т. е. Эти действия будут продолжены, не дожидаясь завершения навигации). 3) задача, возвращенная из EnsureCoreWebView2Async, будет завершена.

Дополнительные сведения о методах, свойствах и событиях, вовлеченных в процесс инициализации, можно найти в соответствующей документации.

Поскольку CoreWebView2 элемента управления — очень высокоплотный объект (потенциально ответственный за множественные процессы и мегабайты дискового пространства), элемент управления реализует интерфейс IDisposable для предоставления явных средств для его освобождения. Вызов Dispose освобождает CoreWebView2 и базовые ресурсы (за исключением случаев, которые также используются другими представлениями) и сбрасывает CoreWebView2 на null. После вызова Dispose невозможно повторно инициализировать CoreWebView2, и любая попытка использования функций, требующих, вызовет ObjectDisposedException.

Обратите внимание, что этот элемент управления расширяет HwndHost, чтобы внедрять окна, которые находятся за пределами экосистемы WPF. Это имеет некоторые последствия для поведения ввода и вывода элемента управления, а также функции, наследуемые от UIElement и FrameworkElement. Для получения дополнительных сведений ознакомьтесь с документацией по взаимодействию HwndHost и WPF/Win32.

* [https://docs.microsoft.com/dotnet/api/system.windows.interop.hwndhost](https://docs.microsoft.com/dotnet/api/system.windows.interop.hwndhost)

* [https://docs.microsoft.com/dotnet/framework/wpf/advanced/wpf-and-win32-interoperation#hwnds-inside-wpf](https://docs.microsoft.com/dotnet/framework/wpf/advanced/wpf-and-win32-interoperation#hwnds-inside-wpf)

## Участников

#### ContentLoading 

Обертка для события CoreWebView2. ContentLoading в CoreWebView2.

> событие EventHandler< CoreWebView2ContentLoadingEventArgs > [ContentLoading](#contentloading)

Единственное различие между этим событием и CoreWebView2. ContentLoading — первый параметр, передаваемый обработчикам. Обработчики этого события получат элемент управления WebView2, в то время как обработчики для CoreWebView2. ContentLoading получат экземпляр CoreWebView2.

#### CoreWebView2Ready 

Это событие запускается, когда CoreWebView2 элемента управления завершает инициализацию (независимо от того, как был инициирована инициализация), но до того, как он будет использоваться для чего-либо.

> событие EventHandler< EventArgs > [CoreWebView2Ready](#corewebview2ready)

Вы должны обработать это событие, если вам необходимо выполнить одну операцию настройки в CoreWebView2, которая будет применяться ко всем их использованию (например, добавлять обработчики событий, настраивать параметры, устанавливать сценарии создания документов, добавлять объекты узла). Ознакомьтесь с документацией по классу WebView2 для обзора инициализации.

Это событие не предоставляет никаких аргументов, а отправитель — элемент управления WebView2, чье свойство CoreWebView2 теперь будет действительно допустимым (то есть не NULL) в первый раз.

#### NavigationCompleted 

Обертка для события CoreWebView2. NavigationCompleted в CoreWebView2.

> событие EventHandler< CoreWebView2NavigationCompletedEventArgs > [NavigationCompleted](#navigationcompleted)

Единственное различие между этим событием и CoreWebView2. NavigationCompleted — первый параметр, передаваемый обработчикам. Обработчики этого события получат элемент управления WebView2, в то время как обработчики для CoreWebView2. NavigationCompleted получат экземпляр CoreWebView2.

#### NavigationStarting 

Обертка для события CoreWebView2. NavigationStarting в CoreWebView2.

> событие EventHandler< CoreWebView2NavigationStartingEventArgs > [NavigationStarting](#navigationstarting)

Единственное различие между этим событием и CoreWebView2. NavigationStarting — первый параметр, передаваемый обработчикам. Обработчики этого события получат элемент управления WebView2, в то время как обработчики для CoreWebView2. NavigationStarting получат экземпляр CoreWebView2.

#### SourceChanged 

Обертка для события CoreWebView2. SourceChanged в CoreWebView2.

> событие EventHandler< CoreWebView2SourceChangedEventArgs > [SourceChanged](#sourcechanged)

Единственное различие между этим событием и CoreWebView2. SourceChanged — первый параметр, передаваемый обработчикам. Обработчики этого события получат элемент управления WebView2, в то время как обработчики для CoreWebView2. SourceChanged получат экземпляр CoreWebView2.

#### WebMessageReceived 

Обертка для события CoreWebView2. WebMessageReceived в CoreWebView2.

> событие EventHandler< CoreWebView2WebMessageReceivedEventArgs > [WebMessageReceived](#webmessagereceived)

Единственное различие между этим событием и CoreWebView2. WebMessageReceived — первый параметр, передаваемый обработчикам. Обработчики этого события получат элемент управления WebView2, в то время как обработчики для CoreWebView2. WebMessageReceived получат экземпляр CoreWebView2.

#### CanGoBack 

Возвращает значение "истина", если WebView может перейти к предыдущей странице в журнале переходов.

> Открытый логический [CanGoBack](#cangoback)

Обертка для свойства CoreWebView2. CanGoBack в CoreWebView2. Если CoreWebView2 не инициализирован, но возвращает значение false.

#### CanGoForward 

Возвращает значение "истина", если WebView может перейти к следующей странице в журнале переходов.

> Открытый логический [CanGoForward](#cangoforward)

Обертка для свойства CoreWebView2. CanGoForward в CoreWebView2. Если CoreWebView2 не инициализирован, но возвращает значение false.

#### CoreWebView2 

Получить доступ ко всем функциональным возможностям базового API Core. CoreWebView2.

> общедоступная CoreWebView2 [CoreWebView2](#corewebview2)

Возвращает значение null, пока инициализация не будет завершена. Ознакомьтесь с документацией по классу WebView2 для обзора инициализации.

##### Исключения
* `InvalidOperationException` Создается, если вызывающий поток не является потоком, который создал этот объект (обычно это поток пользовательского интерфейса). Для получения дополнительных сведений ознакомьтесь с DispatcherObject. VerifyAccess.

* `ObjectDisposedException` Вызывается, если метод Dispose уже вызывался для элемента управления.

#### CreationProperties 

Возвращает или задает набор параметров, которые используются при инициализации CoreWebView2 элемента управления.

> общедоступная CoreWebView2CreationProperties [CreationProperties](#creationproperties)

Настройка этого свойства не будет выполнена после начала инициализации CoreWebView2 элемента управления (старое значение будет сохранено). Ознакомьтесь с документацией по классу WebView2 для обзора инициализации.

#### Источник 

Универсальный код ресурса (URI) верхнего уровня, который в данный момент отображает WebView (или будет отображаться после инициализации его CoreWebView2).

> общедоступный [источник](#source) URI

Как правило, это свойство эквивалентно получению свойства CoreWebView2. Source объекта CoreWebView2 и установке этого свойства эквивалентно вызову метода CoreWebView2. Navigate для CoreWebView2. При получении значения этого свойства до инициализации CoreWebView2 будет извлечен последний URI, для которого был задан этот параметр. Если задать это свойство до инициализации CoreWebView2, инициализация начнется в фоновом режиме (если еще не выполняется), после чего WebView2 будет переходить к указанному универсальному коду ресурса (URI). Ознакомьтесь с документацией по классу WebView2 для обзора инициализации.

##### Исключения
* `ObjectDisposedException` Вызывается, если метод Dispose уже вызывался для элемента управления.

#### EnsureCoreWebView2Async 

Явным образом инициализируйте инициализацию CoreWebView2 элемента управления.

> общедоступная задача [EnsureCoreWebView2Async](#ensurecorewebview2async)(среда CoreWebView2Environment)

Ознакомьтесь с документацией по классу WebView2 для обзора инициализации.

##### Параметры
* `environment` Предварительно созданный CoreWebView2Environment, который должен использоваться для создания CoreWebView2. Создание собственной среды позволяет управлять несколькими параметрами, которые влияют на то, как CoreWebView2 инициализируется. Если вы перейдете к этому методу среду, она переопределит все параметры, заданные в свойстве CreationProperties. Если вы передали null (значение по умолчанию) и для него не установлено значение CreationProperties, среда по умолчанию будет создана и использоваться автоматически. 

##### Дает
Задача, представляющая собой процесс инициализации фона. После завершения задачи свойство CoreWebView2 будет доступно для использования (то есть без значения NULL). Обратите внимание, что событие CoreWebView2Ready элемента управления будет вызвано до завершения задачи. 

Повторный вызов этого метода не повлияет (любая указанная среда игнорируется) и возвращает ту же задачу, что и первый вызов. Вызов этого метода после того, как инициализация вызывается явным образом посредством задания свойства Source, не будет оказывать никакого воздействия (любая указанная среда игнорируется) и просто возвращать задачу, представляющую уже выполняющуюся инициализацию. Обратите внимание, что несмотря на то, что этот метод является асинхронным и возвращает задачу, она по-прежнему должна вызываться в потоке пользовательского интерфейса, например в большинстве открытых функций элементов управления пользовательского интерфейса. 

##### Исключения
* `InvalidOperationException` Создается, если вызывающий поток не является потоком, который создал этот объект (обычно это поток пользовательского интерфейса). Для получения дополнительных сведений ознакомьтесь с DispatcherObject. VerifyAccess.

* `ObjectDisposedException` Вызывается, если метод Dispose уже вызывался для элемента управления.

#### ExecuteScriptAsync 

Выполняет код JavaScript из параметра javaScript в текущем документе верхнего уровня, отображаемом в WebView.

> общедоступная асинхронная задача< String > [ExecuteScriptAsync](#executescriptasync)(String JavaScript)

Эквивалентно вызову CoreWebView2. ExecuteScriptAsync на CoreWebView2

##### Исключения
* `InvalidOperationException` Вызывается, если CoreWebView2 еще не инициализирован.

* `InvalidOperationException` Создается, если вызывающий поток не является потоком, который создал этот объект (обычно это поток пользовательского интерфейса). Для получения дополнительных сведений ознакомьтесь с DispatcherObject. VerifyAccess.

* `ObjectDisposedException` Вызывается, если метод Dispose уже вызывался для элемента управления.

#### GoBack 

Переход по WebView на предыдущую страницу в истории навигации.

> общедоступная void [GoBack](#goback)()

Эквивалентно вызову CoreWebView2. GoBack на CoreWebView2, если CoreWebView2 еще не инициализирован, но не выполняет никаких действий.

##### Исключения
* `InvalidOperationException` Создается, если вызывающий поток не является потоком, который создал этот объект (обычно это поток пользовательского интерфейса). Для получения дополнительных сведений ознакомьтесь с DispatcherObject. VerifyAccess.

* `ObjectDisposedException` Вызывается, если метод Dispose уже вызывался для элемента управления.

#### GoForward 

Переход по WebView к следующей странице в истории навигации.

> общедоступная void [GoForward](#goforward)()

Эквивалентно вызову CoreWebView2. GoForward в CoreWebView2, если CoreWebView2 еще не инициализирован, но не выполняет никаких действий.

##### Исключения
* `InvalidOperationException` Создается, если вызывающий поток не является потоком, который создал этот объект (обычно это поток пользовательского интерфейса). Для получения дополнительных сведений ознакомьтесь с DispatcherObject. VerifyAccess.

* `ObjectDisposedException` Вызывается, если метод Dispose уже вызывался для элемента управления.

#### NavigateToString 

Запускает навигацию для htmlContent в качестве исходного HTML-кода нового документа.

> Public void [NavigateToString](#navigatetostring)(строка htmlContent)

Эквивалентно вызову CoreWebView2. NavigateToString на CoreWebView2

##### Исключения
* `InvalidOperationException` Вызывается, если CoreWebView2 еще не инициализирован.

" <exception cref="InvalidOperationException"> Создается, если вызывающий поток не является потоком, который создал этот объект (обычно — потоком пользовательского интерфейса).  Для получения дополнительных сведений </exception>
<exception cref="ObjectDisposedException"> Ознакомьтесь с DispatcherObject. VerifyAccess. Вызывается, если метод Dispose уже вызывался для элемента управления.

#### Перезагрузить 

Перезагружает текущую страницу.

> общедоступный void [Reload](#reload)()

Эквивалентно вызову CoreWebView2. Reload для CoreWebView2

##### Исключения
* `InvalidOperationException` Вызывается, если CoreWebView2 еще не инициализирован.

" <exception cref="InvalidOperationException"> Создается, если вызывающий поток не является потоком, который создал этот объект (обычно — потоком пользовательского интерфейса).  Для получения дополнительных сведений </exception>
<exception cref="ObjectDisposedException"> Ознакомьтесь с DispatcherObject. VerifyAccess. Вызывается, если метод Dispose уже вызывался для элемента управления.

#### Stop 

Остановка всех переходов и ожидающих выборок ресурсов.

> открытая пустая [Отмена](#stop)()

Эквивалентно вызову CoreWebView2. Stop на CoreWebView2

##### Исключения
* `InvalidOperationException` Вызывается, если CoreWebView2 еще не инициализирован.

" <exception cref="InvalidOperationException"> Создается, если вызывающий поток не является потоком, который создал этот объект (обычно — потоком пользовательского интерфейса).  Для получения дополнительных сведений </exception>
<exception cref="ObjectDisposedException"> Ознакомьтесь с DispatcherObject. VerifyAccess. Вызывается, если метод Dispose уже вызывался для элемента управления.

#### WebView2 

Создает новый экземпляр элемента управления WebView2.

> общедоступная [WebView2](#webview2)()

Обратите внимание, что CoreWebView2 элемента управления будет иметь значение null до инициализации. Ознакомьтесь с документацией по классу WebView2 для обзора инициализации.

