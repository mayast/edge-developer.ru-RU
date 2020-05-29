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
# <span data-ttu-id="97312-104">Класс Microsoft. Web. WebView2. WPF. WebView2</span><span class="sxs-lookup"><span data-stu-id="97312-104">Microsoft.Web.WebView2.Wpf.WebView2 class</span></span> 

<span data-ttu-id="97312-105">Пространство имен: Microsoft. Web. WebView2. WPF </span><span class="sxs-lookup"><span data-stu-id="97312-105">Namespace: Microsoft.Web.WebView2.Wpf</span></span>\
<span data-ttu-id="97312-106">Сборка: Microsoft. Web. WebView2. WPF. dll</span><span class="sxs-lookup"><span data-stu-id="97312-106">Assembly: Microsoft.Web.WebView2.Wpf.dll</span></span>

```
class Microsoft.Web.WebView2.Wpf.WebView2
  : public HwndHost
```

<span data-ttu-id="97312-107">Элемент управления для внедрения веб-содержимого в приложение WPF.</span><span class="sxs-lookup"><span data-stu-id="97312-107">A control to embed web content in a WPF application.</span></span>

## <span data-ttu-id="97312-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="97312-108">Summary</span></span>

 <span data-ttu-id="97312-109">Участников</span><span class="sxs-lookup"><span data-stu-id="97312-109">Members</span></span>                        | <span data-ttu-id="97312-110">Описания</span><span class="sxs-lookup"><span data-stu-id="97312-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="97312-111">ContentLoading</span><span class="sxs-lookup"><span data-stu-id="97312-111">ContentLoading</span></span>](#contentloading) | <span data-ttu-id="97312-112">Обертка для события CoreWebView2. ContentLoading в CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="97312-112">A wrapper around the CoreWebView2.ContentLoading event of CoreWebView2.</span></span>
[<span data-ttu-id="97312-113">CoreWebView2Ready</span><span class="sxs-lookup"><span data-stu-id="97312-113">CoreWebView2Ready</span></span>](#corewebview2ready) | <span data-ttu-id="97312-114">Это событие запускается, когда CoreWebView2 элемента управления завершает инициализацию (независимо от того, как был инициирована инициализация), но до того, как он будет использоваться для чего-либо.</span><span class="sxs-lookup"><span data-stu-id="97312-114">This event is triggered when the control's CoreWebView2 has finished being initialized (regardless of how initialization was triggered) but before it is used for anything.</span></span>
[<span data-ttu-id="97312-115">NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="97312-115">NavigationCompleted</span></span>](#navigationcompleted) | <span data-ttu-id="97312-116">Обертка для события CoreWebView2. NavigationCompleted в CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="97312-116">A wrapper around the CoreWebView2.NavigationCompleted event of CoreWebView2.</span></span>
[<span data-ttu-id="97312-117">NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="97312-117">NavigationStarting</span></span>](#navigationstarting) | <span data-ttu-id="97312-118">Обертка для события CoreWebView2. NavigationStarting в CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="97312-118">A wrapper around the CoreWebView2.NavigationStarting event of CoreWebView2.</span></span>
[<span data-ttu-id="97312-119">SourceChanged</span><span class="sxs-lookup"><span data-stu-id="97312-119">SourceChanged</span></span>](#sourcechanged) | <span data-ttu-id="97312-120">Обертка для события CoreWebView2. SourceChanged в CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="97312-120">A wrapper around the CoreWebView2.SourceChanged event of CoreWebView2.</span></span>
[<span data-ttu-id="97312-121">WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="97312-121">WebMessageReceived</span></span>](#webmessagereceived) | <span data-ttu-id="97312-122">Обертка для события CoreWebView2. WebMessageReceived в CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="97312-122">A wrapper around the CoreWebView2.WebMessageReceived event of CoreWebView2.</span></span>
[<span data-ttu-id="97312-123">CanGoBack</span><span class="sxs-lookup"><span data-stu-id="97312-123">CanGoBack</span></span>](#cangoback) | <span data-ttu-id="97312-124">Возвращает значение "истина", если WebView может перейти к предыдущей странице в журнале переходов.</span><span class="sxs-lookup"><span data-stu-id="97312-124">Returns true if the WebView can navigate to a previous page in the navigation history.</span></span>
[<span data-ttu-id="97312-125">CanGoForward</span><span class="sxs-lookup"><span data-stu-id="97312-125">CanGoForward</span></span>](#cangoforward) | <span data-ttu-id="97312-126">Возвращает значение "истина", если WebView может перейти к следующей странице в журнале переходов.</span><span class="sxs-lookup"><span data-stu-id="97312-126">Returns true if the WebView can navigate to a next page in the navigation history.</span></span>
[<span data-ttu-id="97312-127">CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="97312-127">CoreWebView2</span></span>](#corewebview2) | <span data-ttu-id="97312-128">Получить доступ ко всем функциональным возможностям базового API Core. CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="97312-128">Access the complete functionality of the underlying Core.CoreWebView2 COM API.</span></span>
[<span data-ttu-id="97312-129">CreationProperties</span><span class="sxs-lookup"><span data-stu-id="97312-129">CreationProperties</span></span>](#creationproperties) | <span data-ttu-id="97312-130">Возвращает или задает набор параметров, которые используются при инициализации CoreWebView2 элемента управления.</span><span class="sxs-lookup"><span data-stu-id="97312-130">Gets or sets a bag of options which are used during initialization of the control's CoreWebView2.</span></span>
[<span data-ttu-id="97312-131">Источник</span><span class="sxs-lookup"><span data-stu-id="97312-131">Source</span></span>](#source) | <span data-ttu-id="97312-132">Универсальный код ресурса (URI) верхнего уровня, который в данный момент отображает WebView (или будет отображаться после инициализации его CoreWebView2).</span><span class="sxs-lookup"><span data-stu-id="97312-132">The top-level Uri which the WebView is currently displaying (or will display once initialization of its CoreWebView2 is finished).</span></span>
[<span data-ttu-id="97312-133">EnsureCoreWebView2Async</span><span class="sxs-lookup"><span data-stu-id="97312-133">EnsureCoreWebView2Async</span></span>](#ensurecorewebview2async) | <span data-ttu-id="97312-134">Явным образом инициализируйте инициализацию CoreWebView2 элемента управления.</span><span class="sxs-lookup"><span data-stu-id="97312-134">Explicitly trigger initialization of the control's CoreWebView2.</span></span>
[<span data-ttu-id="97312-135">ExecuteScriptAsync</span><span class="sxs-lookup"><span data-stu-id="97312-135">ExecuteScriptAsync</span></span>](#executescriptasync) | <span data-ttu-id="97312-136">Выполняет код JavaScript из параметра javaScript в текущем документе верхнего уровня, отображаемом в WebView.</span><span class="sxs-lookup"><span data-stu-id="97312-136">Executes JavaScript code from the javaScript parameter in the current top level document rendered in the WebView.</span></span>
[<span data-ttu-id="97312-137">GoBack</span><span class="sxs-lookup"><span data-stu-id="97312-137">GoBack</span></span>](#goback) | <span data-ttu-id="97312-138">Переход по WebView на предыдущую страницу в истории навигации.</span><span class="sxs-lookup"><span data-stu-id="97312-138">Navigates the WebView to the previous page in the navigation history.</span></span>
[<span data-ttu-id="97312-139">GoForward</span><span class="sxs-lookup"><span data-stu-id="97312-139">GoForward</span></span>](#goforward) | <span data-ttu-id="97312-140">Переход по WebView к следующей странице в истории навигации.</span><span class="sxs-lookup"><span data-stu-id="97312-140">Navigates the WebView to the next page in the navigation history.</span></span>
[<span data-ttu-id="97312-141">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="97312-141">NavigateToString</span></span>](#navigatetostring) | <span data-ttu-id="97312-142">Запускает навигацию для htmlContent в качестве исходного HTML-кода нового документа.</span><span class="sxs-lookup"><span data-stu-id="97312-142">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>
[<span data-ttu-id="97312-143">Перезагрузить</span><span class="sxs-lookup"><span data-stu-id="97312-143">Reload</span></span>](#reload) | <span data-ttu-id="97312-144">Перезагружает текущую страницу.</span><span class="sxs-lookup"><span data-stu-id="97312-144">Reloads the current page.</span></span>
[<span data-ttu-id="97312-145">Stop</span><span class="sxs-lookup"><span data-stu-id="97312-145">Stop</span></span>](#stop) | <span data-ttu-id="97312-146">Остановка всех переходов и ожидающих выборок ресурсов.</span><span class="sxs-lookup"><span data-stu-id="97312-146">Stops all navigations and pending resource fetches.</span></span>
[<span data-ttu-id="97312-147">WebView2</span><span class="sxs-lookup"><span data-stu-id="97312-147">WebView2</span></span>](#webview2) | <span data-ttu-id="97312-148">Создает новый экземпляр элемента управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="97312-148">Creates a new instance of a WebView2 control.</span></span>

<span data-ttu-id="97312-149">Этот элемент управления — это программа-оболочка для API WebView2, в которой можно найти документацию по этому адресу: [https://aka.ms/webview2](https://aka.ms/webview2) вы можете напрямую получить доступ к основному интерфейсу ICoreWebView2 и ко всем его функциональным возможностям с помощью свойства CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="97312-149">This control is effectively a wrapper around the WebView2 COM API, which you can find documentation for here: [https://aka.ms/webview2](https://aka.ms/webview2) You can directly access the underlying ICoreWebView2 interface and all of its functionality by accessing the CoreWebView2 property.</span></span> <span data-ttu-id="97312-150">Некоторые из наиболее распространенных функциональных возможностей COM также доступны непосредственно через методы оболочки, свойства и события в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="97312-150">Some of the most common COM functionality is also accessible directly through wrapper methods/properties/events on the control.</span></span>

<span data-ttu-id="97312-151">После создания свойство CoreWebView2 элемента управления будет иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="97312-151">Upon creation, the control's CoreWebView2 property will be null.</span></span> <span data-ttu-id="97312-152">Это связано с тем, что создание CoreWebView2 является дорогостоящей операцией, которая включает в себя такие вещи, как запуск процессов браузеров Edge.</span><span class="sxs-lookup"><span data-stu-id="97312-152">This is because creating the CoreWebView2 is an expensive operation which involves things like launching Edge browser processes.</span></span> <span data-ttu-id="97312-153">Существует два способа создания CoreWebView2:1) вызовите метод EnsureCoreWebView2Async.</span><span class="sxs-lookup"><span data-stu-id="97312-153">There are two ways to cause the CoreWebView2 to be created: 1) Call the EnsureCoreWebView2Async method.</span></span> <span data-ttu-id="97312-154">Это называется явной инициализацией.</span><span class="sxs-lookup"><span data-stu-id="97312-154">This is referred to as explicit initialization.</span></span> <span data-ttu-id="97312-155">2) задайте свойство Source (например, это может быть выполнено из разметки).</span><span class="sxs-lookup"><span data-stu-id="97312-155">2) Set the Source property (which could be done from markup, for example).</span></span> <span data-ttu-id="97312-156">Это называется неявной инициализацией.</span><span class="sxs-lookup"><span data-stu-id="97312-156">This is referred to as implicit initialization.</span></span> <span data-ttu-id="97312-157">Любой из вариантов начнет инициализацию в фоновом режиме и вернется к вызывающему абоненту, не дожидаясь завершения.</span><span class="sxs-lookup"><span data-stu-id="97312-157">Either option will start initialization in the background and return back to the caller without waiting for it to finish.</span></span> <span data-ttu-id="97312-158">Чтобы задать параметры, касающиеся процесса инициализации, перед инициализацией следует либо передать собственный CoreWebView2Environment EnsureCoreWebView2Async, либо задать свойство CreationProperties элемента управления до инициализации.</span><span class="sxs-lookup"><span data-stu-id="97312-158">To specify options regarding the initialization process, either pass your own CoreWebView2Environment to EnsureCoreWebView2Async or set the control's CreationProperties property prior to initialization.</span></span>

<span data-ttu-id="97312-159">После завершения инициализации (независимо от того, как она была активирована), произойдет следующее: 1) будет вызвано событие CoreWebView2Ready элемента управления.</span><span class="sxs-lookup"><span data-stu-id="97312-159">When initialization has finished (regardless of how it was triggered) then the following things will occur, in this order: 1) The control's CoreWebView2Ready event will be invoked.</span></span> <span data-ttu-id="97312-160">Если вам необходимо выполнить одну из операций настройки в CoreWebView2 перед ее использованием, необходимо сделать это в обработчике для этого события.</span><span class="sxs-lookup"><span data-stu-id="97312-160">If you need to perform one time setup operations on the CoreWebView2 prior to its use then you should do so in a handler for that event.</span></span> <span data-ttu-id="97312-161">2) Если для универсального кода ресурса (URI) задано значение свойства Source, элемент управления начнет переход к нему в фоновом режиме (т. е. Эти действия будут продолжены, не дожидаясь завершения навигации).</span><span class="sxs-lookup"><span data-stu-id="97312-161">2) If a Uri has been set to the Source property then the control will start navigating to it in the background (i.e. these steps will continue without waiting for the navigation to finish).</span></span> <span data-ttu-id="97312-162">3) задача, возвращенная из EnsureCoreWebView2Async, будет завершена.</span><span class="sxs-lookup"><span data-stu-id="97312-162">3) The Task returned from EnsureCoreWebView2Async will complete.</span></span>

<span data-ttu-id="97312-163">Дополнительные сведения о методах, свойствах и событиях, вовлеченных в процесс инициализации, можно найти в соответствующей документации.</span><span class="sxs-lookup"><span data-stu-id="97312-163">For more details about any of the methods/properties/events involved in the initialization process, see its specific documentation.</span></span>

<span data-ttu-id="97312-164">Поскольку CoreWebView2 элемента управления — очень высокоплотный объект (потенциально ответственный за множественные процессы и мегабайты дискового пространства), элемент управления реализует интерфейс IDisposable для предоставления явных средств для его освобождения.</span><span class="sxs-lookup"><span data-stu-id="97312-164">Because the control's CoreWebView2 is a very heavyweight object (potentially responsible for multiple running processes and megabytes of disk space) the control implements IDisposable to provide an explicit means to free it.</span></span> <span data-ttu-id="97312-165">Вызов Dispose освобождает CoreWebView2 и базовые ресурсы (за исключением случаев, которые также используются другими представлениями) и сбрасывает CoreWebView2 на null.</span><span class="sxs-lookup"><span data-stu-id="97312-165">Calling Dispose will release the CoreWebView2 and its underlying resources (except any that are also being used by other WebViews), and reset CoreWebView2 to null.</span></span> <span data-ttu-id="97312-166">После вызова Dispose невозможно повторно инициализировать CoreWebView2, и любая попытка использования функций, требующих, вызовет ObjectDisposedException.</span><span class="sxs-lookup"><span data-stu-id="97312-166">After Dispose has been called the CoreWebView2 cannot be re-initialized, and any attempt to use functionality which requires it will throw an ObjectDisposedException.</span></span>

<span data-ttu-id="97312-167">Обратите внимание, что этот элемент управления расширяет HwndHost, чтобы внедрять окна, которые находятся за пределами экосистемы WPF.</span><span class="sxs-lookup"><span data-stu-id="97312-167">Note that this control extends HwndHost in order to embed windows which live outside of the WPF ecosystem.</span></span> <span data-ttu-id="97312-168">Это имеет некоторые последствия для поведения ввода и вывода элемента управления, а также функции, наследуемые от UIElement и FrameworkElement.</span><span class="sxs-lookup"><span data-stu-id="97312-168">This has some implications regarding the control's input and output behavior as well as the functionality it "inherits" from UIElement and FrameworkElement.</span></span> <span data-ttu-id="97312-169">Для получения дополнительных сведений ознакомьтесь с документацией по взаимодействию HwndHost и WPF/Win32.</span><span class="sxs-lookup"><span data-stu-id="97312-169">See the HwndHost and WPF/Win32 interop documentation for more info:</span></span>

* [https://docs.microsoft.com/dotnet/api/system.windows.interop.hwndhost](https://docs.microsoft.com/dotnet/api/system.windows.interop.hwndhost)

* [https://docs.microsoft.com/dotnet/framework/wpf/advanced/wpf-and-win32-interoperation#hwnds-inside-wpf](https://docs.microsoft.com/dotnet/framework/wpf/advanced/wpf-and-win32-interoperation#hwnds-inside-wpf)

## <span data-ttu-id="97312-170">Участников</span><span class="sxs-lookup"><span data-stu-id="97312-170">Members</span></span>

#### <span data-ttu-id="97312-171">ContentLoading</span><span class="sxs-lookup"><span data-stu-id="97312-171">ContentLoading</span></span> 

<span data-ttu-id="97312-172">Обертка для события CoreWebView2. ContentLoading в CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="97312-172">A wrapper around the CoreWebView2.ContentLoading event of CoreWebView2.</span></span>

> <span data-ttu-id="97312-173">событие EventHandler< CoreWebView2ContentLoadingEventArgs > [ContentLoading](#contentloading)</span><span class="sxs-lookup"><span data-stu-id="97312-173">public event EventHandler< CoreWebView2ContentLoadingEventArgs > [ContentLoading](#contentloading)</span></span>

<span data-ttu-id="97312-174">Единственное различие между этим событием и CoreWebView2. ContentLoading — первый параметр, передаваемый обработчикам.</span><span class="sxs-lookup"><span data-stu-id="97312-174">The only difference between this event and CoreWebView2.ContentLoading is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="97312-175">Обработчики этого события получат элемент управления WebView2, в то время как обработчики для CoreWebView2. ContentLoading получат экземпляр CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="97312-175">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.ContentLoading will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="97312-176">CoreWebView2Ready</span><span class="sxs-lookup"><span data-stu-id="97312-176">CoreWebView2Ready</span></span> 

<span data-ttu-id="97312-177">Это событие запускается, когда CoreWebView2 элемента управления завершает инициализацию (независимо от того, как был инициирована инициализация), но до того, как он будет использоваться для чего-либо.</span><span class="sxs-lookup"><span data-stu-id="97312-177">This event is triggered when the control's CoreWebView2 has finished being initialized (regardless of how initialization was triggered) but before it is used for anything.</span></span>

> <span data-ttu-id="97312-178">событие EventHandler< EventArgs > [CoreWebView2Ready](#corewebview2ready)</span><span class="sxs-lookup"><span data-stu-id="97312-178">public event EventHandler< EventArgs > [CoreWebView2Ready](#corewebview2ready)</span></span>

<span data-ttu-id="97312-179">Вы должны обработать это событие, если вам необходимо выполнить одну операцию настройки в CoreWebView2, которая будет применяться ко всем их использованию (например, добавлять обработчики событий, настраивать параметры, устанавливать сценарии создания документов, добавлять объекты узла).</span><span class="sxs-lookup"><span data-stu-id="97312-179">You should handle this event if you need to perform one time setup operations on the CoreWebView2 which you want to affect all of its usages (e.g. adding event handlers, configuring settings, installing document creation scripts, adding host objects).</span></span> <span data-ttu-id="97312-180">Ознакомьтесь с документацией по классу WebView2 для обзора инициализации.</span><span class="sxs-lookup"><span data-stu-id="97312-180">See the WebView2 class documentation for an initialization overview.</span></span>

<span data-ttu-id="97312-181">Это событие не предоставляет никаких аргументов, а отправитель — элемент управления WebView2, чье свойство CoreWebView2 теперь будет действительно допустимым (то есть не NULL) в первый раз.</span><span class="sxs-lookup"><span data-stu-id="97312-181">This event doesn't provide any arguments, and the sender will be the WebView2 control, whose CoreWebView2 property will now be valid (i.e. non-null) for the first time.</span></span>

#### <span data-ttu-id="97312-182">NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="97312-182">NavigationCompleted</span></span> 

<span data-ttu-id="97312-183">Обертка для события CoreWebView2. NavigationCompleted в CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="97312-183">A wrapper around the CoreWebView2.NavigationCompleted event of CoreWebView2.</span></span>

> <span data-ttu-id="97312-184">событие EventHandler< CoreWebView2NavigationCompletedEventArgs > [NavigationCompleted](#navigationcompleted)</span><span class="sxs-lookup"><span data-stu-id="97312-184">public event EventHandler< CoreWebView2NavigationCompletedEventArgs > [NavigationCompleted](#navigationcompleted)</span></span>

<span data-ttu-id="97312-185">Единственное различие между этим событием и CoreWebView2. NavigationCompleted — первый параметр, передаваемый обработчикам.</span><span class="sxs-lookup"><span data-stu-id="97312-185">The only difference between this event and CoreWebView2.NavigationCompleted is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="97312-186">Обработчики этого события получат элемент управления WebView2, в то время как обработчики для CoreWebView2. NavigationCompleted получат экземпляр CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="97312-186">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.NavigationCompleted will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="97312-187">NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="97312-187">NavigationStarting</span></span> 

<span data-ttu-id="97312-188">Обертка для события CoreWebView2. NavigationStarting в CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="97312-188">A wrapper around the CoreWebView2.NavigationStarting event of CoreWebView2.</span></span>

> <span data-ttu-id="97312-189">событие EventHandler< CoreWebView2NavigationStartingEventArgs > [NavigationStarting](#navigationstarting)</span><span class="sxs-lookup"><span data-stu-id="97312-189">public event EventHandler< CoreWebView2NavigationStartingEventArgs > [NavigationStarting](#navigationstarting)</span></span>

<span data-ttu-id="97312-190">Единственное различие между этим событием и CoreWebView2. NavigationStarting — первый параметр, передаваемый обработчикам.</span><span class="sxs-lookup"><span data-stu-id="97312-190">The only difference between this event and CoreWebView2.NavigationStarting is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="97312-191">Обработчики этого события получат элемент управления WebView2, в то время как обработчики для CoreWebView2. NavigationStarting получат экземпляр CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="97312-191">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.NavigationStarting will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="97312-192">SourceChanged</span><span class="sxs-lookup"><span data-stu-id="97312-192">SourceChanged</span></span> 

<span data-ttu-id="97312-193">Обертка для события CoreWebView2. SourceChanged в CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="97312-193">A wrapper around the CoreWebView2.SourceChanged event of CoreWebView2.</span></span>

> <span data-ttu-id="97312-194">событие EventHandler< CoreWebView2SourceChangedEventArgs > [SourceChanged](#sourcechanged)</span><span class="sxs-lookup"><span data-stu-id="97312-194">public event EventHandler< CoreWebView2SourceChangedEventArgs > [SourceChanged](#sourcechanged)</span></span>

<span data-ttu-id="97312-195">Единственное различие между этим событием и CoreWebView2. SourceChanged — первый параметр, передаваемый обработчикам.</span><span class="sxs-lookup"><span data-stu-id="97312-195">The only difference between this event and CoreWebView2.SourceChanged is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="97312-196">Обработчики этого события получат элемент управления WebView2, в то время как обработчики для CoreWebView2. SourceChanged получат экземпляр CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="97312-196">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.SourceChanged will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="97312-197">WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="97312-197">WebMessageReceived</span></span> 

<span data-ttu-id="97312-198">Обертка для события CoreWebView2. WebMessageReceived в CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="97312-198">A wrapper around the CoreWebView2.WebMessageReceived event of CoreWebView2.</span></span>

> <span data-ttu-id="97312-199">событие EventHandler< CoreWebView2WebMessageReceivedEventArgs > [WebMessageReceived](#webmessagereceived)</span><span class="sxs-lookup"><span data-stu-id="97312-199">public event EventHandler< CoreWebView2WebMessageReceivedEventArgs > [WebMessageReceived](#webmessagereceived)</span></span>

<span data-ttu-id="97312-200">Единственное различие между этим событием и CoreWebView2. WebMessageReceived — первый параметр, передаваемый обработчикам.</span><span class="sxs-lookup"><span data-stu-id="97312-200">The only difference between this event and CoreWebView2.WebMessageReceived is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="97312-201">Обработчики этого события получат элемент управления WebView2, в то время как обработчики для CoreWebView2. WebMessageReceived получат экземпляр CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="97312-201">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.WebMessageReceived will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="97312-202">CanGoBack</span><span class="sxs-lookup"><span data-stu-id="97312-202">CanGoBack</span></span> 

<span data-ttu-id="97312-203">Возвращает значение "истина", если WebView может перейти к предыдущей странице в журнале переходов.</span><span class="sxs-lookup"><span data-stu-id="97312-203">Returns true if the WebView can navigate to a previous page in the navigation history.</span></span>

> <span data-ttu-id="97312-204">Открытый логический [CanGoBack](#cangoback)</span><span class="sxs-lookup"><span data-stu-id="97312-204">public bool [CanGoBack](#cangoback)</span></span>

<span data-ttu-id="97312-205">Обертка для свойства CoreWebView2. CanGoBack в CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="97312-205">Wrapper around the CoreWebView2.CanGoBack property of CoreWebView2.</span></span> <span data-ttu-id="97312-206">Если CoreWebView2 не инициализирован, но возвращает значение false.</span><span class="sxs-lookup"><span data-stu-id="97312-206">If CoreWebView2 isn't initialized yet then returns false.</span></span>

#### <span data-ttu-id="97312-207">CanGoForward</span><span class="sxs-lookup"><span data-stu-id="97312-207">CanGoForward</span></span> 

<span data-ttu-id="97312-208">Возвращает значение "истина", если WebView может перейти к следующей странице в журнале переходов.</span><span class="sxs-lookup"><span data-stu-id="97312-208">Returns true if the WebView can navigate to a next page in the navigation history.</span></span>

> <span data-ttu-id="97312-209">Открытый логический [CanGoForward](#cangoforward)</span><span class="sxs-lookup"><span data-stu-id="97312-209">public bool [CanGoForward](#cangoforward)</span></span>

<span data-ttu-id="97312-210">Обертка для свойства CoreWebView2. CanGoForward в CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="97312-210">Wrapper around the CoreWebView2.CanGoForward property of CoreWebView2.</span></span> <span data-ttu-id="97312-211">Если CoreWebView2 не инициализирован, но возвращает значение false.</span><span class="sxs-lookup"><span data-stu-id="97312-211">If CoreWebView2 isn't initialized yet then returns false.</span></span>

#### <span data-ttu-id="97312-212">CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="97312-212">CoreWebView2</span></span> 

<span data-ttu-id="97312-213">Получить доступ ко всем функциональным возможностям базового API Core. CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="97312-213">Access the complete functionality of the underlying Core.CoreWebView2 COM API.</span></span>

> <span data-ttu-id="97312-214">общедоступная CoreWebView2 [CoreWebView2](#corewebview2)</span><span class="sxs-lookup"><span data-stu-id="97312-214">public CoreWebView2 [CoreWebView2](#corewebview2)</span></span>

<span data-ttu-id="97312-215">Возвращает значение null, пока инициализация не будет завершена.</span><span class="sxs-lookup"><span data-stu-id="97312-215">Returns null until initialization has completed.</span></span> <span data-ttu-id="97312-216">Ознакомьтесь с документацией по классу WebView2 для обзора инициализации.</span><span class="sxs-lookup"><span data-stu-id="97312-216">See the WebView2 class documentation for an initialization overview.</span></span>

##### <span data-ttu-id="97312-217">Исключения</span><span class="sxs-lookup"><span data-stu-id="97312-217">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="97312-218">Создается, если вызывающий поток не является потоком, который создал этот объект (обычно это поток пользовательского интерфейса).</span><span class="sxs-lookup"><span data-stu-id="97312-218">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="97312-219">Для получения дополнительных сведений ознакомьтесь с DispatcherObject. VerifyAccess.</span><span class="sxs-lookup"><span data-stu-id="97312-219">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="97312-220">Вызывается, если метод Dispose уже вызывался для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="97312-220">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="97312-221">CreationProperties</span><span class="sxs-lookup"><span data-stu-id="97312-221">CreationProperties</span></span> 

<span data-ttu-id="97312-222">Возвращает или задает набор параметров, которые используются при инициализации CoreWebView2 элемента управления.</span><span class="sxs-lookup"><span data-stu-id="97312-222">Gets or sets a bag of options which are used during initialization of the control's CoreWebView2.</span></span>

> <span data-ttu-id="97312-223">общедоступная CoreWebView2CreationProperties [CreationProperties](#creationproperties)</span><span class="sxs-lookup"><span data-stu-id="97312-223">public CoreWebView2CreationProperties [CreationProperties](#creationproperties)</span></span>

<span data-ttu-id="97312-224">Настройка этого свойства не будет выполнена после начала инициализации CoreWebView2 элемента управления (старое значение будет сохранено).</span><span class="sxs-lookup"><span data-stu-id="97312-224">Setting this property won't work after initialization of the control's CoreWebView2 has started (the old value will be retained).</span></span> <span data-ttu-id="97312-225">Ознакомьтесь с документацией по классу WebView2 для обзора инициализации.</span><span class="sxs-lookup"><span data-stu-id="97312-225">See the WebView2 class documentation for an initialization overview.</span></span>

#### <span data-ttu-id="97312-226">Источник</span><span class="sxs-lookup"><span data-stu-id="97312-226">Source</span></span> 

<span data-ttu-id="97312-227">Универсальный код ресурса (URI) верхнего уровня, который в данный момент отображает WebView (или будет отображаться после инициализации его CoreWebView2).</span><span class="sxs-lookup"><span data-stu-id="97312-227">The top-level Uri which the WebView is currently displaying (or will display once initialization of its CoreWebView2 is finished).</span></span>

> <span data-ttu-id="97312-228">общедоступный [источник](#source) URI</span><span class="sxs-lookup"><span data-stu-id="97312-228">public Uri [Source](#source)</span></span>

<span data-ttu-id="97312-229">Как правило, это свойство эквивалентно получению свойства CoreWebView2. Source объекта CoreWebView2 и установке этого свойства эквивалентно вызову метода CoreWebView2. Navigate для CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="97312-229">Generally speaking, getting this property is equivalent to getting the CoreWebView2.Source property of CoreWebView2 and setting this property is equivalent to calling the CoreWebView2.Navigate method on CoreWebView2.</span></span> <span data-ttu-id="97312-230">При получении значения этого свойства до инициализации CoreWebView2 будет извлечен последний URI, для которого был задан этот параметр.</span><span class="sxs-lookup"><span data-stu-id="97312-230">Getting this property before the CoreWebView2 has been initialized will retrieve the last Uri which was set to it.</span></span> <span data-ttu-id="97312-231">Если задать это свойство до инициализации CoreWebView2, инициализация начнется в фоновом режиме (если еще не выполняется), после чего WebView2 будет переходить к указанному универсальному коду ресурса (URI).</span><span class="sxs-lookup"><span data-stu-id="97312-231">Setting this property before the CoreWebView2 has been initialized will cause initialization to start in the background (if not already in progress), after which the WebView2 will navigate to the specified Uri.</span></span> <span data-ttu-id="97312-232">Ознакомьтесь с документацией по классу WebView2 для обзора инициализации.</span><span class="sxs-lookup"><span data-stu-id="97312-232">See the WebView2 class documentation for an initialization overview.</span></span>

##### <span data-ttu-id="97312-233">Исключения</span><span class="sxs-lookup"><span data-stu-id="97312-233">Exceptions</span></span>
* `ObjectDisposedException` <span data-ttu-id="97312-234">Вызывается, если метод Dispose уже вызывался для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="97312-234">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="97312-235">EnsureCoreWebView2Async</span><span class="sxs-lookup"><span data-stu-id="97312-235">EnsureCoreWebView2Async</span></span> 

<span data-ttu-id="97312-236">Явным образом инициализируйте инициализацию CoreWebView2 элемента управления.</span><span class="sxs-lookup"><span data-stu-id="97312-236">Explicitly trigger initialization of the control's CoreWebView2.</span></span>

> <span data-ttu-id="97312-237">общедоступная задача [EnsureCoreWebView2Async](#ensurecorewebview2async)(среда CoreWebView2Environment)</span><span class="sxs-lookup"><span data-stu-id="97312-237">public Task [EnsureCoreWebView2Async](#ensurecorewebview2async)(CoreWebView2Environment environment)</span></span>

<span data-ttu-id="97312-238">Ознакомьтесь с документацией по классу WebView2 для обзора инициализации.</span><span class="sxs-lookup"><span data-stu-id="97312-238">See the WebView2 class documentation for an initialization overview.</span></span>

##### <span data-ttu-id="97312-239">Параметры</span><span class="sxs-lookup"><span data-stu-id="97312-239">Parameters</span></span>
* `environment` <span data-ttu-id="97312-240">Предварительно созданный CoreWebView2Environment, который должен использоваться для создания CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="97312-240">A pre-created CoreWebView2Environment that should be used to create the CoreWebView2.</span></span> <span data-ttu-id="97312-241">Создание собственной среды позволяет управлять несколькими параметрами, которые влияют на то, как CoreWebView2 инициализируется.</span><span class="sxs-lookup"><span data-stu-id="97312-241">Creating your own environment gives you control over several options that affect how the CoreWebView2 is initialized.</span></span> <span data-ttu-id="97312-242">Если вы перейдете к этому методу среду, она переопределит все параметры, заданные в свойстве CreationProperties.</span><span class="sxs-lookup"><span data-stu-id="97312-242">If you pass an environment to this method then it will override any settings specified on the CreationProperties property.</span></span> <span data-ttu-id="97312-243">Если вы передали null (значение по умолчанию) и для него не установлено значение CreationProperties, среда по умолчанию будет создана и использоваться автоматически.</span><span class="sxs-lookup"><span data-stu-id="97312-243">If you pass null (the default value) and no value has been set to CreationProperties then a default environment will be created and used automatically.</span></span> 

##### <span data-ttu-id="97312-244">Дает</span><span class="sxs-lookup"><span data-stu-id="97312-244">Returns</span></span>
<span data-ttu-id="97312-245">Задача, представляющая собой процесс инициализации фона.</span><span class="sxs-lookup"><span data-stu-id="97312-245">A Task that represents the background initialization process.</span></span> <span data-ttu-id="97312-246">После завершения задачи свойство CoreWebView2 будет доступно для использования (то есть без значения NULL).</span><span class="sxs-lookup"><span data-stu-id="97312-246">When the task completes then the CoreWebView2 property will be available for use (i.e. non-null).</span></span> <span data-ttu-id="97312-247">Обратите внимание, что событие CoreWebView2Ready элемента управления будет вызвано до завершения задачи.</span><span class="sxs-lookup"><span data-stu-id="97312-247">Note that the control's CoreWebView2Ready event will be invoked before the task completes.</span></span> 

<span data-ttu-id="97312-248">Повторный вызов этого метода не повлияет (любая указанная среда игнорируется) и возвращает ту же задачу, что и первый вызов.</span><span class="sxs-lookup"><span data-stu-id="97312-248">Calling this method additional times will have no effect (any specified environment is ignored) and return the same Task as the first call.</span></span> <span data-ttu-id="97312-249">Вызов этого метода после того, как инициализация вызывается явным образом посредством задания свойства Source, не будет оказывать никакого воздействия (любая указанная среда игнорируется) и просто возвращать задачу, представляющую уже выполняющуюся инициализацию.</span><span class="sxs-lookup"><span data-stu-id="97312-249">Calling this method after initialization has been implicitly triggered by setting the Source property will have no effect (any specified environment is ignored) and simply return a Task representing that initialization already in progress.</span></span> <span data-ttu-id="97312-250">Обратите внимание, что несмотря на то, что этот метод является асинхронным и возвращает задачу, она по-прежнему должна вызываться в потоке пользовательского интерфейса, например в большинстве открытых функций элементов управления пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="97312-250">Note that even though this method is asynchronous and returns a Task, it still must be called on the UI thread like most public functionality of most UI controls.</span></span> 

##### <span data-ttu-id="97312-251">Исключения</span><span class="sxs-lookup"><span data-stu-id="97312-251">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="97312-252">Создается, если вызывающий поток не является потоком, который создал этот объект (обычно это поток пользовательского интерфейса).</span><span class="sxs-lookup"><span data-stu-id="97312-252">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="97312-253">Для получения дополнительных сведений ознакомьтесь с DispatcherObject. VerifyAccess.</span><span class="sxs-lookup"><span data-stu-id="97312-253">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="97312-254">Вызывается, если метод Dispose уже вызывался для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="97312-254">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="97312-255">ExecuteScriptAsync</span><span class="sxs-lookup"><span data-stu-id="97312-255">ExecuteScriptAsync</span></span> 

<span data-ttu-id="97312-256">Выполняет код JavaScript из параметра javaScript в текущем документе верхнего уровня, отображаемом в WebView.</span><span class="sxs-lookup"><span data-stu-id="97312-256">Executes JavaScript code from the javaScript parameter in the current top level document rendered in the WebView.</span></span>

> <span data-ttu-id="97312-257">общедоступная асинхронная задача< String > [ExecuteScriptAsync](#executescriptasync)(String JavaScript)</span><span class="sxs-lookup"><span data-stu-id="97312-257">public async Task< string > [ExecuteScriptAsync](#executescriptasync)(string javaScript)</span></span>

<span data-ttu-id="97312-258">Эквивалентно вызову CoreWebView2. ExecuteScriptAsync на CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="97312-258">Equivalent to calling CoreWebView2.ExecuteScriptAsync on CoreWebView2</span></span>

##### <span data-ttu-id="97312-259">Исключения</span><span class="sxs-lookup"><span data-stu-id="97312-259">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="97312-260">Вызывается, если CoreWebView2 еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="97312-260">Thrown if CoreWebView2 hasn't been initialized yet.</span></span>

* `InvalidOperationException` <span data-ttu-id="97312-261">Создается, если вызывающий поток не является потоком, который создал этот объект (обычно это поток пользовательского интерфейса).</span><span class="sxs-lookup"><span data-stu-id="97312-261">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="97312-262">Для получения дополнительных сведений ознакомьтесь с DispatcherObject. VerifyAccess.</span><span class="sxs-lookup"><span data-stu-id="97312-262">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="97312-263">Вызывается, если метод Dispose уже вызывался для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="97312-263">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="97312-264">GoBack</span><span class="sxs-lookup"><span data-stu-id="97312-264">GoBack</span></span> 

<span data-ttu-id="97312-265">Переход по WebView на предыдущую страницу в истории навигации.</span><span class="sxs-lookup"><span data-stu-id="97312-265">Navigates the WebView to the previous page in the navigation history.</span></span>

> <span data-ttu-id="97312-266">общедоступная void [GoBack](#goback)()</span><span class="sxs-lookup"><span data-stu-id="97312-266">public void [GoBack](#goback)()</span></span>

<span data-ttu-id="97312-267">Эквивалентно вызову CoreWebView2. GoBack на CoreWebView2, если CoreWebView2 еще не инициализирован, но не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="97312-267">Equivalent to calling CoreWebView2.GoBack on CoreWebView2 If CoreWebView2 hasn't been initialized yet then does nothing.</span></span>

##### <span data-ttu-id="97312-268">Исключения</span><span class="sxs-lookup"><span data-stu-id="97312-268">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="97312-269">Создается, если вызывающий поток не является потоком, который создал этот объект (обычно это поток пользовательского интерфейса).</span><span class="sxs-lookup"><span data-stu-id="97312-269">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="97312-270">Для получения дополнительных сведений ознакомьтесь с DispatcherObject. VerifyAccess.</span><span class="sxs-lookup"><span data-stu-id="97312-270">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="97312-271">Вызывается, если метод Dispose уже вызывался для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="97312-271">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="97312-272">GoForward</span><span class="sxs-lookup"><span data-stu-id="97312-272">GoForward</span></span> 

<span data-ttu-id="97312-273">Переход по WebView к следующей странице в истории навигации.</span><span class="sxs-lookup"><span data-stu-id="97312-273">Navigates the WebView to the next page in the navigation history.</span></span>

> <span data-ttu-id="97312-274">общедоступная void [GoForward](#goforward)()</span><span class="sxs-lookup"><span data-stu-id="97312-274">public void [GoForward](#goforward)()</span></span>

<span data-ttu-id="97312-275">Эквивалентно вызову CoreWebView2. GoForward в CoreWebView2, если CoreWebView2 еще не инициализирован, но не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="97312-275">Equivalent to calling CoreWebView2.GoForward on CoreWebView2 If CoreWebView2 hasn't been initialized yet then does nothing.</span></span>

##### <span data-ttu-id="97312-276">Исключения</span><span class="sxs-lookup"><span data-stu-id="97312-276">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="97312-277">Создается, если вызывающий поток не является потоком, который создал этот объект (обычно это поток пользовательского интерфейса).</span><span class="sxs-lookup"><span data-stu-id="97312-277">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="97312-278">Для получения дополнительных сведений ознакомьтесь с DispatcherObject. VerifyAccess.</span><span class="sxs-lookup"><span data-stu-id="97312-278">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="97312-279">Вызывается, если метод Dispose уже вызывался для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="97312-279">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="97312-280">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="97312-280">NavigateToString</span></span> 

<span data-ttu-id="97312-281">Запускает навигацию для htmlContent в качестве исходного HTML-кода нового документа.</span><span class="sxs-lookup"><span data-stu-id="97312-281">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>

> <span data-ttu-id="97312-282">Public void [NavigateToString](#navigatetostring)(строка htmlContent)</span><span class="sxs-lookup"><span data-stu-id="97312-282">public void [NavigateToString](#navigatetostring)(string htmlContent)</span></span>

<span data-ttu-id="97312-283">Эквивалентно вызову CoreWebView2. NavigateToString на CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="97312-283">Equivalent to calling CoreWebView2.NavigateToString on CoreWebView2</span></span>

##### <span data-ttu-id="97312-284">Исключения</span><span class="sxs-lookup"><span data-stu-id="97312-284">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="97312-285">Вызывается, если CoreWebView2 еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="97312-285">Thrown if CoreWebView2 hasn't been initialized yet.</span></span>

<span data-ttu-id="97312-286">" <exception cref="InvalidOperationException"> Создается, если вызывающий поток не является потоком, который создал этот объект (обычно — потоком пользовательского интерфейса).</span><span class="sxs-lookup"><span data-stu-id="97312-286">" <exception cref="InvalidOperationException">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span>  <span data-ttu-id="97312-287">Для получения дополнительных сведений </exception>
<exception cref="ObjectDisposedException"> Ознакомьтесь с DispatcherObject. VerifyAccess. Вызывается, если метод Dispose уже вызывался для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="97312-287">See DispatcherObject.VerifyAccess for more info.</exception>
<exception cref="ObjectDisposedException">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="97312-288">Перезагрузить</span><span class="sxs-lookup"><span data-stu-id="97312-288">Reload</span></span> 

<span data-ttu-id="97312-289">Перезагружает текущую страницу.</span><span class="sxs-lookup"><span data-stu-id="97312-289">Reloads the current page.</span></span>

> <span data-ttu-id="97312-290">общедоступный void [Reload](#reload)()</span><span class="sxs-lookup"><span data-stu-id="97312-290">public void [Reload](#reload)()</span></span>

<span data-ttu-id="97312-291">Эквивалентно вызову CoreWebView2. Reload для CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="97312-291">Equivalent to calling CoreWebView2.Reload on CoreWebView2</span></span>

##### <span data-ttu-id="97312-292">Исключения</span><span class="sxs-lookup"><span data-stu-id="97312-292">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="97312-293">Вызывается, если CoreWebView2 еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="97312-293">Thrown if CoreWebView2 hasn't been initialized yet.</span></span>

<span data-ttu-id="97312-294">" <exception cref="InvalidOperationException"> Создается, если вызывающий поток не является потоком, который создал этот объект (обычно — потоком пользовательского интерфейса).</span><span class="sxs-lookup"><span data-stu-id="97312-294">" <exception cref="InvalidOperationException">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span>  <span data-ttu-id="97312-295">Для получения дополнительных сведений </exception>
<exception cref="ObjectDisposedException"> Ознакомьтесь с DispatcherObject. VerifyAccess. Вызывается, если метод Dispose уже вызывался для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="97312-295">See DispatcherObject.VerifyAccess for more info.</exception>
<exception cref="ObjectDisposedException">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="97312-296">Stop</span><span class="sxs-lookup"><span data-stu-id="97312-296">Stop</span></span> 

<span data-ttu-id="97312-297">Остановка всех переходов и ожидающих выборок ресурсов.</span><span class="sxs-lookup"><span data-stu-id="97312-297">Stops all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="97312-298">открытая пустая [Отмена](#stop)()</span><span class="sxs-lookup"><span data-stu-id="97312-298">public void [Stop](#stop)()</span></span>

<span data-ttu-id="97312-299">Эквивалентно вызову CoreWebView2. Stop на CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="97312-299">Equivalent to calling CoreWebView2.Stop on CoreWebView2</span></span>

##### <span data-ttu-id="97312-300">Исключения</span><span class="sxs-lookup"><span data-stu-id="97312-300">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="97312-301">Вызывается, если CoreWebView2 еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="97312-301">Thrown if CoreWebView2 hasn't been initialized yet.</span></span>

<span data-ttu-id="97312-302">" <exception cref="InvalidOperationException"> Создается, если вызывающий поток не является потоком, который создал этот объект (обычно — потоком пользовательского интерфейса).</span><span class="sxs-lookup"><span data-stu-id="97312-302">" <exception cref="InvalidOperationException">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span>  <span data-ttu-id="97312-303">Для получения дополнительных сведений </exception>
<exception cref="ObjectDisposedException"> Ознакомьтесь с DispatcherObject. VerifyAccess. Вызывается, если метод Dispose уже вызывался для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="97312-303">See DispatcherObject.VerifyAccess for more info.</exception>
<exception cref="ObjectDisposedException">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="97312-304">WebView2</span><span class="sxs-lookup"><span data-stu-id="97312-304">WebView2</span></span> 

<span data-ttu-id="97312-305">Создает новый экземпляр элемента управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="97312-305">Creates a new instance of a WebView2 control.</span></span>

> <span data-ttu-id="97312-306">общедоступная [WebView2](#webview2)()</span><span class="sxs-lookup"><span data-stu-id="97312-306">public [WebView2](#webview2)()</span></span>

<span data-ttu-id="97312-307">Обратите внимание, что CoreWebView2 элемента управления будет иметь значение null до инициализации.</span><span class="sxs-lookup"><span data-stu-id="97312-307">Note that the control's CoreWebView2 will be null until initialized.</span></span> <span data-ttu-id="97312-308">Ознакомьтесь с документацией по классу WebView2 для обзора инициализации.</span><span class="sxs-lookup"><span data-stu-id="97312-308">See the WebView2 class documentation for an initialization overview.</span></span>

