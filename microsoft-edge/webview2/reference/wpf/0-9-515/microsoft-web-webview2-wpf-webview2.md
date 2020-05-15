---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/13/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: f2c3bcb5334abc907a838971ebc1773b6485194f
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654695"
---
# <span data-ttu-id="85414-104">Класс Microsoft. Web. WebView2. WPF. WebView2</span><span class="sxs-lookup"><span data-stu-id="85414-104">Microsoft.Web.WebView2.Wpf.WebView2 class</span></span> 

<span data-ttu-id="85414-105">Пространство имен: Microsoft. Web. WebView2. WPF </span><span class="sxs-lookup"><span data-stu-id="85414-105">Namespace: Microsoft.Web.WebView2.Wpf</span></span>\
<span data-ttu-id="85414-106">Сборка: Microsoft. Web. WebView2. WPF. dll</span><span class="sxs-lookup"><span data-stu-id="85414-106">Assembly: Microsoft.Web.WebView2.Wpf.dll</span></span>

```
class Microsoft.Web.WebView2.Wpf.WebView2
  : public HwndHost
```

<span data-ttu-id="85414-107">Элемент управления для внедрения веб-содержимого в приложение WPF.</span><span class="sxs-lookup"><span data-stu-id="85414-107">A control to embed web content in a WPF application.</span></span>

## <span data-ttu-id="85414-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="85414-108">Summary</span></span>

 <span data-ttu-id="85414-109">Участников</span><span class="sxs-lookup"><span data-stu-id="85414-109">Members</span></span>                        | <span data-ttu-id="85414-110">Описания</span><span class="sxs-lookup"><span data-stu-id="85414-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="85414-111">ContentLoading</span><span class="sxs-lookup"><span data-stu-id="85414-111">ContentLoading</span></span>](#contentloading) | <span data-ttu-id="85414-112">Обертка для события CoreWebView2. ContentLoading в CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="85414-112">A wrapper around the CoreWebView2.ContentLoading event of CoreWebView2.</span></span>
[<span data-ttu-id="85414-113">CoreWebView2Ready</span><span class="sxs-lookup"><span data-stu-id="85414-113">CoreWebView2Ready</span></span>](#corewebview2ready) | <span data-ttu-id="85414-114">Это событие запускается, когда CoreWebView2 элемента управления завершает инициализацию (независимо от того, как был инициирована инициализация), но до того, как он будет использоваться для чего-либо.</span><span class="sxs-lookup"><span data-stu-id="85414-114">This event is triggered when the control's CoreWebView2 has finished being initialized (regardless of how initialization was triggered) but before it is used for anything.</span></span>
[<span data-ttu-id="85414-115">NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="85414-115">NavigationCompleted</span></span>](#navigationcompleted) | <span data-ttu-id="85414-116">Обертка для события CoreWebView2. NavigationCompleted в CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="85414-116">A wrapper around the CoreWebView2.NavigationCompleted event of CoreWebView2.</span></span>
[<span data-ttu-id="85414-117">NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="85414-117">NavigationStarting</span></span>](#navigationstarting) | <span data-ttu-id="85414-118">Обертка для события CoreWebView2. NavigationStarting в CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="85414-118">A wrapper around the CoreWebView2.NavigationStarting event of CoreWebView2.</span></span>
[<span data-ttu-id="85414-119">SourceChanged</span><span class="sxs-lookup"><span data-stu-id="85414-119">SourceChanged</span></span>](#sourcechanged) | <span data-ttu-id="85414-120">Обертка для события CoreWebView2. SourceChanged в CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="85414-120">A wrapper around the CoreWebView2.SourceChanged event of CoreWebView2.</span></span>
[<span data-ttu-id="85414-121">WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="85414-121">WebMessageReceived</span></span>](#webmessagereceived) | <span data-ttu-id="85414-122">Обертка для события CoreWebView2. WebMessageReceived в CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="85414-122">A wrapper around the CoreWebView2.WebMessageReceived event of CoreWebView2.</span></span>
[<span data-ttu-id="85414-123">CanGoBack</span><span class="sxs-lookup"><span data-stu-id="85414-123">CanGoBack</span></span>](#cangoback) | <span data-ttu-id="85414-124">Возвращает значение "истина", если WebView может перейти к предыдущей странице в журнале переходов.</span><span class="sxs-lookup"><span data-stu-id="85414-124">Returns true if the WebView can navigate to a previous page in the navigation history.</span></span>
[<span data-ttu-id="85414-125">CanGoForward</span><span class="sxs-lookup"><span data-stu-id="85414-125">CanGoForward</span></span>](#cangoforward) | <span data-ttu-id="85414-126">Возвращает значение "истина", если WebView может перейти к следующей странице в журнале переходов.</span><span class="sxs-lookup"><span data-stu-id="85414-126">Returns true if the WebView can navigate to a next page in the navigation history.</span></span>
[<span data-ttu-id="85414-127">CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="85414-127">CoreWebView2</span></span>](#corewebview2) | <span data-ttu-id="85414-128">Получить доступ ко всем функциональным возможностям базового API Core. CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="85414-128">Access the complete functionality of the underlying Core.CoreWebView2 COM API.</span></span>
[<span data-ttu-id="85414-129">CreationProperties</span><span class="sxs-lookup"><span data-stu-id="85414-129">CreationProperties</span></span>](#creationproperties) | <span data-ttu-id="85414-130">Возвращает или задает набор параметров, которые используются при инициализации CoreWebView2 элемента управления.</span><span class="sxs-lookup"><span data-stu-id="85414-130">Gets or sets a bag of options which are used during initialization of the control's CoreWebView2.</span></span>
[<span data-ttu-id="85414-131">Источник</span><span class="sxs-lookup"><span data-stu-id="85414-131">Source</span></span>](#source) | <span data-ttu-id="85414-132">Универсальный код ресурса (URI) верхнего уровня, который в данный момент отображает WebView (или будет отображаться после инициализации его CoreWebView2).</span><span class="sxs-lookup"><span data-stu-id="85414-132">The top-level Uri which the WebView is currently displaying (or will display once initialization of its CoreWebView2 is finished).</span></span>
[<span data-ttu-id="85414-133">EnsureCoreWebView2Async</span><span class="sxs-lookup"><span data-stu-id="85414-133">EnsureCoreWebView2Async</span></span>](#ensurecorewebview2async) | <span data-ttu-id="85414-134">Явным образом инициализируйте инициализацию CoreWebView2 элемента управления.</span><span class="sxs-lookup"><span data-stu-id="85414-134">Explicitly trigger initialization of the control's CoreWebView2.</span></span>
[<span data-ttu-id="85414-135">ExecuteScriptAsync</span><span class="sxs-lookup"><span data-stu-id="85414-135">ExecuteScriptAsync</span></span>](#executescriptasync) | <span data-ttu-id="85414-136">Выполняет код JavaScript из параметра javaScript в текущем документе верхнего уровня, отображаемом в WebView.</span><span class="sxs-lookup"><span data-stu-id="85414-136">Executes JavaScript code from the javaScript parameter in the current top level document rendered in the WebView.</span></span>
[<span data-ttu-id="85414-137">GoBack</span><span class="sxs-lookup"><span data-stu-id="85414-137">GoBack</span></span>](#goback) | <span data-ttu-id="85414-138">Переход по WebView на предыдущую страницу в истории навигации.</span><span class="sxs-lookup"><span data-stu-id="85414-138">Navigates the WebView to the previous page in the navigation history.</span></span>
[<span data-ttu-id="85414-139">GoForward</span><span class="sxs-lookup"><span data-stu-id="85414-139">GoForward</span></span>](#goforward) | <span data-ttu-id="85414-140">Переход по WebView к следующей странице в истории навигации.</span><span class="sxs-lookup"><span data-stu-id="85414-140">Navigates the WebView to the next page in the navigation history.</span></span>
[<span data-ttu-id="85414-141">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="85414-141">NavigateToString</span></span>](#navigatetostring) | <span data-ttu-id="85414-142">Запускает навигацию для htmlContent в качестве исходного HTML-кода нового документа.</span><span class="sxs-lookup"><span data-stu-id="85414-142">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>
[<span data-ttu-id="85414-143">Перезагрузить</span><span class="sxs-lookup"><span data-stu-id="85414-143">Reload</span></span>](#reload) | <span data-ttu-id="85414-144">Перезагружает текущую страницу.</span><span class="sxs-lookup"><span data-stu-id="85414-144">Reloads the current page.</span></span>
[<span data-ttu-id="85414-145">Stop</span><span class="sxs-lookup"><span data-stu-id="85414-145">Stop</span></span>](#stop) | <span data-ttu-id="85414-146">Остановка всех переходов и ожидающих выборок ресурсов.</span><span class="sxs-lookup"><span data-stu-id="85414-146">Stops all navigations and pending resource fetches.</span></span>
[<span data-ttu-id="85414-147">WebView2</span><span class="sxs-lookup"><span data-stu-id="85414-147">WebView2</span></span>](#webview2) | <span data-ttu-id="85414-148">Создает новый экземпляр элемента управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="85414-148">Creates a new instance of a WebView2 control.</span></span>
[<span data-ttu-id="85414-149">BuildWindowCore</span><span class="sxs-lookup"><span data-stu-id="85414-149">BuildWindowCore</span></span>](#buildwindowcore) | <span data-ttu-id="85414-150">Это значение переопределяется из HwndHost и вызывается, чтобы сообщить нам о необходимости создать HWND.</span><span class="sxs-lookup"><span data-stu-id="85414-150">This is overridden from HwndHost and is called to instruct us to create our HWND.</span></span>
[<span data-ttu-id="85414-151">DestroyWindowCore</span><span class="sxs-lookup"><span data-stu-id="85414-151">DestroyWindowCore</span></span>](#destroywindowcore) | <span data-ttu-id="85414-152">Это значение переопределяется из HwndHost и вызывается, чтобы дать нам команду уничтожить наш HWND.</span><span class="sxs-lookup"><span data-stu-id="85414-152">This is overridden from HwndHost and is called to instruct us to destroy our HWND.</span></span>
[<span data-ttu-id="85414-153">Ликвидация</span><span class="sxs-lookup"><span data-stu-id="85414-153">Dispose</span></span>](#dispose) | <span data-ttu-id="85414-154">Этот базовый класс вызывается в соответствии с типичной реализацией шаблона IDispose.</span><span class="sxs-lookup"><span data-stu-id="85414-154">This is called by our base class according to the typical implementation of the IDispose pattern.</span></span>
[<span data-ttu-id="85414-155">HasFocusWithinCore</span><span class="sxs-lookup"><span data-stu-id="85414-155">HasFocusWithinCore</span></span>](#hasfocuswithincore) | <span data-ttu-id="85414-156">Это значение переопределяется из HwndHost и вызывается, когда для WPF требуется узнать, находится ли фокус в нашем элементе управления/окне.</span><span class="sxs-lookup"><span data-stu-id="85414-156">This is overridden from HwndHost and is called when WPF needs to know if the focus is in our control/window.</span></span>
[<span data-ttu-id="85414-157">OnKeyDown</span><span class="sxs-lookup"><span data-stu-id="85414-157">OnKeyDown</span></span>](#onkeydown) | <span data-ttu-id="85414-158">Это значение переопределяется из UIElement и вызывается, чтобы позволить нам обрабатывать нажатия клавиши ввода.</span><span class="sxs-lookup"><span data-stu-id="85414-158">This is overridden from UIElement and called to allow us to handle key press input.</span></span>
[<span data-ttu-id="85414-159">OnKeyUp</span><span class="sxs-lookup"><span data-stu-id="85414-159">OnKeyUp</span></span>](#onkeyup) | <span data-ttu-id="85414-160">Смотрите клавишу KeyDown.</span><span class="sxs-lookup"><span data-stu-id="85414-160">See OnKeyDown.</span></span>
[<span data-ttu-id="85414-161">OnPreviewKeyDown</span><span class="sxs-lookup"><span data-stu-id="85414-161">OnPreviewKeyDown</span></span>](#onpreviewkeydown) | <span data-ttu-id="85414-162">Это "предварительный просмотр" (т. е.</span><span class="sxs-lookup"><span data-stu-id="85414-162">This is the "Preview" (i.e.</span></span>
[<span data-ttu-id="85414-163">OnPreviewKeyUp</span><span class="sxs-lookup"><span data-stu-id="85414-163">OnPreviewKeyUp</span></span>](#onpreviewkeyup) | <span data-ttu-id="85414-164">Смотрите OnPreviewKeyDown.</span><span class="sxs-lookup"><span data-stu-id="85414-164">See OnPreviewKeyDown.</span></span>
[<span data-ttu-id="85414-165">OnWindowPositionChanged</span><span class="sxs-lookup"><span data-stu-id="85414-165">OnWindowPositionChanged</span></span>](#onwindowpositionchanged) | <span data-ttu-id="85414-166">Этот метод переопределен из HwndHost и вызывается, когда изменилось положение элемента управления.</span><span class="sxs-lookup"><span data-stu-id="85414-166">This is overridden from HwndHost and called when our control's location has changed.</span></span>
[<span data-ttu-id="85414-167">TabIntoCore</span><span class="sxs-lookup"><span data-stu-id="85414-167">TabIntoCore</span></span>](#tabintocore) | <span data-ttu-id="85414-168">Это значение переопределяется из HwndHost и вызывается, чтобы сообщить нам, что переход на вкладку привел к переходу фокуса на наш элемент управления/окно.</span><span class="sxs-lookup"><span data-stu-id="85414-168">This is overridden from HwndHost and is called to inform us that tabbing has caused the focus to move into our control/window.</span></span>

<span data-ttu-id="85414-169">Этот элемент управления — это программа-оболочка для API WebView2, в которой можно найти документацию по этому адресу: [https://aka.ms/webview2](https://aka.ms/webview2) вы можете напрямую получить доступ к основному интерфейсу ICoreWebView2 и ко всем его функциональным возможностям с помощью свойства CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="85414-169">This control is effectively a wrapper around the WebView2 COM API, which you can find documentation for here: [https://aka.ms/webview2](https://aka.ms/webview2) You can directly access the underlying ICoreWebView2 interface and all of its functionality by accessing the CoreWebView2 property.</span></span> <span data-ttu-id="85414-170">Некоторые из наиболее распространенных функциональных возможностей COM также доступны непосредственно через методы оболочки, свойства и события в элементе управления.</span><span class="sxs-lookup"><span data-stu-id="85414-170">Some of the most common COM functionality is also accessible directly through wrapper methods/properties/events on the control.</span></span>

<span data-ttu-id="85414-171">После создания свойство CoreWebView2 элемента управления будет иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="85414-171">Upon creation, the control's CoreWebView2 property will be null.</span></span> <span data-ttu-id="85414-172">Это связано с тем, что создание CoreWebView2 является дорогостоящей операцией, которая включает в себя такие вещи, как запуск процессов браузеров Edge.</span><span class="sxs-lookup"><span data-stu-id="85414-172">This is because creating the CoreWebView2 is an expensive operation which involves things like launching Edge browser processes.</span></span> <span data-ttu-id="85414-173">Существует два способа создания CoreWebView2:1) вызовите метод EnsureCoreWebView2Async.</span><span class="sxs-lookup"><span data-stu-id="85414-173">There are two ways to cause the CoreWebView2 to be created: 1) Call the EnsureCoreWebView2Async method.</span></span> <span data-ttu-id="85414-174">Это называется явной инициализацией.</span><span class="sxs-lookup"><span data-stu-id="85414-174">This is referred to as explicit initialization.</span></span> <span data-ttu-id="85414-175">2) задайте свойство Source (например, это может быть выполнено из разметки).</span><span class="sxs-lookup"><span data-stu-id="85414-175">2) Set the Source property (which could be done from markup, for example).</span></span> <span data-ttu-id="85414-176">Это называется неявной инициализацией.</span><span class="sxs-lookup"><span data-stu-id="85414-176">This is referred to as implicit initialization.</span></span> <span data-ttu-id="85414-177">Любой из вариантов начнет инициализацию в фоновом режиме и вернется к вызывающему абоненту, не дожидаясь завершения.</span><span class="sxs-lookup"><span data-stu-id="85414-177">Either option will start initialization in the background and return back to the caller without waiting for it to finish.</span></span> <span data-ttu-id="85414-178">Чтобы задать параметры, касающиеся процесса инициализации, перед инициализацией следует либо передать собственный CoreWebView2Environment EnsureCoreWebView2Async, либо задать свойство CreationProperties элемента управления до инициализации.</span><span class="sxs-lookup"><span data-stu-id="85414-178">To specify options regarding the initialization process, either pass your own CoreWebView2Environment to EnsureCoreWebView2Async or set the control's CreationProperties property prior to initialization.</span></span>

<span data-ttu-id="85414-179">После завершения инициализации (независимо от того, как она была активирована), произойдет следующее: 1) будет вызвано событие CoreWebView2Ready элемента управления.</span><span class="sxs-lookup"><span data-stu-id="85414-179">When initialization has finished (regardless of how it was triggered) then the following things will occur, in this order: 1) The control's CoreWebView2Ready event will be invoked.</span></span> <span data-ttu-id="85414-180">Если вам необходимо выполнить одну из операций настройки в CoreWebView2 перед ее использованием, необходимо сделать это в обработчике для этого события.</span><span class="sxs-lookup"><span data-stu-id="85414-180">If you need to perform one time setup operations on the CoreWebView2 prior to its use then you should do so in a handler for that event.</span></span> <span data-ttu-id="85414-181">2) Если для универсального кода ресурса (URI) задано значение свойства Source, элемент управления начнет переход к нему в фоновом режиме (т. е. Эти действия будут продолжены, не дожидаясь завершения навигации).</span><span class="sxs-lookup"><span data-stu-id="85414-181">2) If a Uri has been set to the Source property then the control will start navigating to it in the background (i.e. these steps will continue without waiting for the navigation to finish).</span></span> <span data-ttu-id="85414-182">3) задача, возвращенная из EnsureCoreWebView2Async, будет завершена.</span><span class="sxs-lookup"><span data-stu-id="85414-182">3) The Task returned from EnsureCoreWebView2Async will complete.</span></span>

<span data-ttu-id="85414-183">Дополнительные сведения о методах, свойствах и событиях, вовлеченных в процесс инициализации, можно найти в соответствующей документации.</span><span class="sxs-lookup"><span data-stu-id="85414-183">For more details about any of the methods/properties/events involved in the initialization process, see its specific documentation.</span></span>

<span data-ttu-id="85414-184">Поскольку CoreWebView2 элемента управления — очень высокоплотный объект (потенциально ответственный за множественные процессы и мегабайты дискового пространства), элемент управления реализует интерфейс IDisposable для предоставления явных средств для его освобождения.</span><span class="sxs-lookup"><span data-stu-id="85414-184">Because the control's CoreWebView2 is a very heavyweight object (potentially responsible for multiple running processes and megabytes of disk space) the control implements IDisposable to provide an explicit means to free it.</span></span> <span data-ttu-id="85414-185">Вызов Dispose освобождает CoreWebView2 и базовые ресурсы (за исключением случаев, которые также используются другими представлениями) и сбрасывает CoreWebView2 на null.</span><span class="sxs-lookup"><span data-stu-id="85414-185">Calling Dispose will release the CoreWebView2 and its underlying resources (except any that are also being used by other WebViews), and reset CoreWebView2 to null.</span></span> <span data-ttu-id="85414-186">После вызова Dispose невозможно повторно инициализировать CoreWebView2, и любая попытка использования функций, требующих, вызовет ObjectDisposedException.</span><span class="sxs-lookup"><span data-stu-id="85414-186">After Dispose has been called the CoreWebView2 cannot be re-initialized, and any attempt to use functionality which requires it will throw an ObjectDisposedException.</span></span>

<span data-ttu-id="85414-187">Обратите внимание, что этот элемент управления расширяет HwndHost, чтобы внедрять окна, которые находятся за пределами экосистемы WPF.</span><span class="sxs-lookup"><span data-stu-id="85414-187">Note that this control extends HwndHost in order to embed windows which live outside of the WPF ecosystem.</span></span> <span data-ttu-id="85414-188">Это имеет некоторые последствия для поведения ввода и вывода элемента управления, а также функции, наследуемые от UIElement и FrameworkElement.</span><span class="sxs-lookup"><span data-stu-id="85414-188">This has some implications regarding the control's input and output behavior as well as the functionality it "inherits" from UIElement and FrameworkElement.</span></span> <span data-ttu-id="85414-189">Для получения дополнительных сведений ознакомьтесь с документацией по взаимодействию HwndHost и WPF/Win32.</span><span class="sxs-lookup"><span data-stu-id="85414-189">See the HwndHost and WPF/Win32 interop documentation for more info:</span></span>

* [https://docs.microsoft.com/dotnet/api/system.windows.interop.hwndhost](https://docs.microsoft.com/dotnet/api/system.windows.interop.hwndhost)

* [https://docs.microsoft.com/dotnet/framework/wpf/advanced/wpf-and-win32-interoperation#hwnds-inside-wpf](https://docs.microsoft.com/dotnet/framework/wpf/advanced/wpf-and-win32-interoperation#hwnds-inside-wpf)

## <span data-ttu-id="85414-190">Участников</span><span class="sxs-lookup"><span data-stu-id="85414-190">Members</span></span>

#### <span data-ttu-id="85414-191">ContentLoading</span><span class="sxs-lookup"><span data-stu-id="85414-191">ContentLoading</span></span> 

<span data-ttu-id="85414-192">Обертка для события CoreWebView2. ContentLoading в CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="85414-192">A wrapper around the CoreWebView2.ContentLoading event of CoreWebView2.</span></span>

> <span data-ttu-id="85414-193">событие EventHandler< CoreWebView2ContentLoadingEventArgs > [ContentLoading](#contentloading)</span><span class="sxs-lookup"><span data-stu-id="85414-193">public event EventHandler< CoreWebView2ContentLoadingEventArgs > [ContentLoading](#contentloading)</span></span>

<span data-ttu-id="85414-194">Единственное различие между этим событием и CoreWebView2. ContentLoading — первый параметр, передаваемый обработчикам.</span><span class="sxs-lookup"><span data-stu-id="85414-194">The only difference between this event and CoreWebView2.ContentLoading is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="85414-195">Обработчики этого события получат элемент управления WebView2, в то время как обработчики для CoreWebView2. ContentLoading получат экземпляр CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="85414-195">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.ContentLoading will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="85414-196">CoreWebView2Ready</span><span class="sxs-lookup"><span data-stu-id="85414-196">CoreWebView2Ready</span></span> 

<span data-ttu-id="85414-197">Это событие запускается, когда CoreWebView2 элемента управления завершает инициализацию (независимо от того, как был инициирована инициализация), но до того, как он будет использоваться для чего-либо.</span><span class="sxs-lookup"><span data-stu-id="85414-197">This event is triggered when the control's CoreWebView2 has finished being initialized (regardless of how initialization was triggered) but before it is used for anything.</span></span>

> <span data-ttu-id="85414-198">событие EventHandler< EventArgs > [CoreWebView2Ready](#corewebview2ready)</span><span class="sxs-lookup"><span data-stu-id="85414-198">public event EventHandler< EventArgs > [CoreWebView2Ready](#corewebview2ready)</span></span>

<span data-ttu-id="85414-199">Вы должны обработать это событие, если вам необходимо выполнить одну операцию настройки в CoreWebView2, которая будет применяться ко всем их использованию (например, добавлять обработчики событий, настраивать параметры, устанавливать сценарии создания документов, добавлять объекты узла).</span><span class="sxs-lookup"><span data-stu-id="85414-199">You should handle this event if you need to perform one time setup operations on the CoreWebView2 which you want to affect all of its usages (e.g. adding event handlers, configuring settings, installing document creation scripts, adding host objects).</span></span> <span data-ttu-id="85414-200">Ознакомьтесь с документацией по классу WebView2 для обзора инициализации.</span><span class="sxs-lookup"><span data-stu-id="85414-200">See the WebView2 class documentation for an initialization overview.</span></span>

<span data-ttu-id="85414-201">Это событие не предоставляет никаких аргументов, а отправитель — элемент управления WebView2, чье свойство CoreWebView2 теперь будет действительно допустимым (то есть не NULL) в первый раз.</span><span class="sxs-lookup"><span data-stu-id="85414-201">This event doesn't provide any arguments, and the sender will be the WebView2 control, whose CoreWebView2 property will now be valid (i.e. non-null) for the first time.</span></span>

#### <span data-ttu-id="85414-202">NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="85414-202">NavigationCompleted</span></span> 

<span data-ttu-id="85414-203">Обертка для события CoreWebView2. NavigationCompleted в CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="85414-203">A wrapper around the CoreWebView2.NavigationCompleted event of CoreWebView2.</span></span>

> <span data-ttu-id="85414-204">событие EventHandler< CoreWebView2NavigationCompletedEventArgs > [NavigationCompleted](#navigationcompleted)</span><span class="sxs-lookup"><span data-stu-id="85414-204">public event EventHandler< CoreWebView2NavigationCompletedEventArgs > [NavigationCompleted](#navigationcompleted)</span></span>

<span data-ttu-id="85414-205">Единственное различие между этим событием и CoreWebView2. NavigationCompleted — первый параметр, передаваемый обработчикам.</span><span class="sxs-lookup"><span data-stu-id="85414-205">The only difference between this event and CoreWebView2.NavigationCompleted is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="85414-206">Обработчики этого события получат элемент управления WebView2, в то время как обработчики для CoreWebView2. NavigationCompleted получат экземпляр CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="85414-206">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.NavigationCompleted will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="85414-207">NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="85414-207">NavigationStarting</span></span> 

<span data-ttu-id="85414-208">Обертка для события CoreWebView2. NavigationStarting в CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="85414-208">A wrapper around the CoreWebView2.NavigationStarting event of CoreWebView2.</span></span>

> <span data-ttu-id="85414-209">событие EventHandler< CoreWebView2NavigationStartingEventArgs > [NavigationStarting](#navigationstarting)</span><span class="sxs-lookup"><span data-stu-id="85414-209">public event EventHandler< CoreWebView2NavigationStartingEventArgs > [NavigationStarting](#navigationstarting)</span></span>

<span data-ttu-id="85414-210">Единственное различие между этим событием и CoreWebView2. NavigationStarting — первый параметр, передаваемый обработчикам.</span><span class="sxs-lookup"><span data-stu-id="85414-210">The only difference between this event and CoreWebView2.NavigationStarting is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="85414-211">Обработчики этого события получат элемент управления WebView2, в то время как обработчики для CoreWebView2. NavigationStarting получат экземпляр CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="85414-211">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.NavigationStarting will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="85414-212">SourceChanged</span><span class="sxs-lookup"><span data-stu-id="85414-212">SourceChanged</span></span> 

<span data-ttu-id="85414-213">Обертка для события CoreWebView2. SourceChanged в CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="85414-213">A wrapper around the CoreWebView2.SourceChanged event of CoreWebView2.</span></span>

> <span data-ttu-id="85414-214">событие EventHandler< CoreWebView2SourceChangedEventArgs > [SourceChanged](#sourcechanged)</span><span class="sxs-lookup"><span data-stu-id="85414-214">public event EventHandler< CoreWebView2SourceChangedEventArgs > [SourceChanged](#sourcechanged)</span></span>

<span data-ttu-id="85414-215">Единственное различие между этим событием и CoreWebView2. SourceChanged — первый параметр, передаваемый обработчикам.</span><span class="sxs-lookup"><span data-stu-id="85414-215">The only difference between this event and CoreWebView2.SourceChanged is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="85414-216">Обработчики этого события получат элемент управления WebView2, в то время как обработчики для CoreWebView2. SourceChanged получат экземпляр CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="85414-216">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.SourceChanged will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="85414-217">WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="85414-217">WebMessageReceived</span></span> 

<span data-ttu-id="85414-218">Обертка для события CoreWebView2. WebMessageReceived в CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="85414-218">A wrapper around the CoreWebView2.WebMessageReceived event of CoreWebView2.</span></span>

> <span data-ttu-id="85414-219">событие EventHandler< CoreWebView2WebMessageReceivedEventArgs > [WebMessageReceived](#webmessagereceived)</span><span class="sxs-lookup"><span data-stu-id="85414-219">public event EventHandler< CoreWebView2WebMessageReceivedEventArgs > [WebMessageReceived](#webmessagereceived)</span></span>

<span data-ttu-id="85414-220">Единственное различие между этим событием и CoreWebView2. WebMessageReceived — первый параметр, передаваемый обработчикам.</span><span class="sxs-lookup"><span data-stu-id="85414-220">The only difference between this event and CoreWebView2.WebMessageReceived is the first parameter that's passed to handlers.</span></span> <span data-ttu-id="85414-221">Обработчики этого события получат элемент управления WebView2, в то время как обработчики для CoreWebView2. WebMessageReceived получат экземпляр CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="85414-221">Handlers of this event will receive the WebView2 control, whereas handlers of CoreWebView2.WebMessageReceived will receive the CoreWebView2 instance.</span></span>

#### <span data-ttu-id="85414-222">CanGoBack</span><span class="sxs-lookup"><span data-stu-id="85414-222">CanGoBack</span></span> 

<span data-ttu-id="85414-223">Возвращает значение "истина", если WebView может перейти к предыдущей странице в журнале переходов.</span><span class="sxs-lookup"><span data-stu-id="85414-223">Returns true if the WebView can navigate to a previous page in the navigation history.</span></span>

> <span data-ttu-id="85414-224">Открытый логический [CanGoBack](#cangoback)</span><span class="sxs-lookup"><span data-stu-id="85414-224">public bool [CanGoBack](#cangoback)</span></span>

<span data-ttu-id="85414-225">Обертка для свойства CoreWebView2. CanGoBack в CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="85414-225">Wrapper around the CoreWebView2.CanGoBack property of CoreWebView2.</span></span> <span data-ttu-id="85414-226">Если CoreWebView2 не инициализирован, но возвращает значение false.</span><span class="sxs-lookup"><span data-stu-id="85414-226">If CoreWebView2 isn't initialized yet then returns false.</span></span>

#### <span data-ttu-id="85414-227">CanGoForward</span><span class="sxs-lookup"><span data-stu-id="85414-227">CanGoForward</span></span> 

<span data-ttu-id="85414-228">Возвращает значение "истина", если WebView может перейти к следующей странице в журнале переходов.</span><span class="sxs-lookup"><span data-stu-id="85414-228">Returns true if the WebView can navigate to a next page in the navigation history.</span></span>

> <span data-ttu-id="85414-229">Открытый логический [CanGoForward](#cangoforward)</span><span class="sxs-lookup"><span data-stu-id="85414-229">public bool [CanGoForward](#cangoforward)</span></span>

<span data-ttu-id="85414-230">Обертка для свойства CoreWebView2. CanGoForward в CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="85414-230">Wrapper around the CoreWebView2.CanGoForward property of CoreWebView2.</span></span> <span data-ttu-id="85414-231">Если CoreWebView2 не инициализирован, но возвращает значение false.</span><span class="sxs-lookup"><span data-stu-id="85414-231">If CoreWebView2 isn't initialized yet then returns false.</span></span>

#### <span data-ttu-id="85414-232">CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="85414-232">CoreWebView2</span></span> 

<span data-ttu-id="85414-233">Получить доступ ко всем функциональным возможностям базового API Core. CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="85414-233">Access the complete functionality of the underlying Core.CoreWebView2 COM API.</span></span>

> <span data-ttu-id="85414-234">общедоступная CoreWebView2 [CoreWebView2](#corewebview2)</span><span class="sxs-lookup"><span data-stu-id="85414-234">public CoreWebView2 [CoreWebView2](#corewebview2)</span></span>

<span data-ttu-id="85414-235">Возвращает значение null, пока инициализация не будет завершена.</span><span class="sxs-lookup"><span data-stu-id="85414-235">Returns null until initialization has completed.</span></span> <span data-ttu-id="85414-236">Ознакомьтесь с документацией по классу WebView2 для обзора инициализации.</span><span class="sxs-lookup"><span data-stu-id="85414-236">See the WebView2 class documentation for an initialization overview.</span></span>

##### <span data-ttu-id="85414-237">Исключения</span><span class="sxs-lookup"><span data-stu-id="85414-237">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="85414-238">Создается, если вызывающий поток не является потоком, который создал этот объект (обычно это поток пользовательского интерфейса).</span><span class="sxs-lookup"><span data-stu-id="85414-238">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="85414-239">Для получения дополнительных сведений ознакомьтесь с DispatcherObject. VerifyAccess.</span><span class="sxs-lookup"><span data-stu-id="85414-239">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="85414-240">Вызывается, если метод Dispose уже вызывался для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="85414-240">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="85414-241">CreationProperties</span><span class="sxs-lookup"><span data-stu-id="85414-241">CreationProperties</span></span> 

<span data-ttu-id="85414-242">Возвращает или задает набор параметров, которые используются при инициализации CoreWebView2 элемента управления.</span><span class="sxs-lookup"><span data-stu-id="85414-242">Gets or sets a bag of options which are used during initialization of the control's CoreWebView2.</span></span>

> <span data-ttu-id="85414-243">общедоступная CoreWebView2CreationProperties [CreationProperties](#creationproperties)</span><span class="sxs-lookup"><span data-stu-id="85414-243">public CoreWebView2CreationProperties [CreationProperties](#creationproperties)</span></span>

<span data-ttu-id="85414-244">Настройка этого свойства не будет выполнена после начала инициализации CoreWebView2 элемента управления (старое значение будет сохранено).</span><span class="sxs-lookup"><span data-stu-id="85414-244">Setting this property won't work after initialization of the control's CoreWebView2 has started (the old value will be retained).</span></span> <span data-ttu-id="85414-245">Ознакомьтесь с документацией по классу WebView2 для обзора инициализации.</span><span class="sxs-lookup"><span data-stu-id="85414-245">See the WebView2 class documentation for an initialization overview.</span></span>

#### <span data-ttu-id="85414-246">Источник</span><span class="sxs-lookup"><span data-stu-id="85414-246">Source</span></span> 

<span data-ttu-id="85414-247">Универсальный код ресурса (URI) верхнего уровня, который в данный момент отображает WebView (или будет отображаться после инициализации его CoreWebView2).</span><span class="sxs-lookup"><span data-stu-id="85414-247">The top-level Uri which the WebView is currently displaying (or will display once initialization of its CoreWebView2 is finished).</span></span>

> <span data-ttu-id="85414-248">общедоступный [источник](#source) URI</span><span class="sxs-lookup"><span data-stu-id="85414-248">public Uri [Source](#source)</span></span>

<span data-ttu-id="85414-249">Как правило, это свойство эквивалентно получению свойства CoreWebView2. Source объекта CoreWebView2 и установке этого свойства эквивалентно вызову метода CoreWebView2. Navigate для CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="85414-249">Generally speaking, getting this property is equivalent to getting the CoreWebView2.Source property of CoreWebView2 and setting this property is equivalent to calling the CoreWebView2.Navigate method on CoreWebView2.</span></span> <span data-ttu-id="85414-250">При получении значения этого свойства до инициализации CoreWebView2 будет извлечен последний URI, для которого был задан этот параметр.</span><span class="sxs-lookup"><span data-stu-id="85414-250">Getting this property before the CoreWebView2 has been initialized will retrieve the last Uri which was set to it.</span></span> <span data-ttu-id="85414-251">Если задать это свойство до инициализации CoreWebView2, инициализация начнется в фоновом режиме (если еще не выполняется), после чего WebView2 будет переходить к указанному универсальному коду ресурса (URI).</span><span class="sxs-lookup"><span data-stu-id="85414-251">Setting this property before the CoreWebView2 has been initialized will cause initialization to start in the background (if not already in progress), after which the WebView2 will navigate to the specified Uri.</span></span> <span data-ttu-id="85414-252">Ознакомьтесь с документацией по классу WebView2 для обзора инициализации.</span><span class="sxs-lookup"><span data-stu-id="85414-252">See the WebView2 class documentation for an initialization overview.</span></span>

##### <span data-ttu-id="85414-253">Исключения</span><span class="sxs-lookup"><span data-stu-id="85414-253">Exceptions</span></span>
* `ObjectDisposedException` <span data-ttu-id="85414-254">Вызывается, если метод Dispose уже вызывался для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="85414-254">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="85414-255">EnsureCoreWebView2Async</span><span class="sxs-lookup"><span data-stu-id="85414-255">EnsureCoreWebView2Async</span></span> 

<span data-ttu-id="85414-256">Явным образом инициализируйте инициализацию CoreWebView2 элемента управления.</span><span class="sxs-lookup"><span data-stu-id="85414-256">Explicitly trigger initialization of the control's CoreWebView2.</span></span>

> <span data-ttu-id="85414-257">общедоступная задача [EnsureCoreWebView2Async](#ensurecorewebview2async)(среда CoreWebView2Environment)</span><span class="sxs-lookup"><span data-stu-id="85414-257">public Task [EnsureCoreWebView2Async](#ensurecorewebview2async)(CoreWebView2Environment environment)</span></span>

<span data-ttu-id="85414-258">Ознакомьтесь с документацией по классу WebView2 для обзора инициализации.</span><span class="sxs-lookup"><span data-stu-id="85414-258">See the WebView2 class documentation for an initialization overview.</span></span>

##### <span data-ttu-id="85414-259">Параметры</span><span class="sxs-lookup"><span data-stu-id="85414-259">Parameters</span></span>
* `environment` <span data-ttu-id="85414-260">Предварительно созданный CoreWebView2Environment, который должен использоваться для создания CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="85414-260">A pre-created CoreWebView2Environment that should be used to create the CoreWebView2.</span></span> <span data-ttu-id="85414-261">Создание собственной среды позволяет управлять несколькими параметрами, которые влияют на то, как CoreWebView2 инициализируется.</span><span class="sxs-lookup"><span data-stu-id="85414-261">Creating your own environment gives you control over several options that affect how the CoreWebView2 is initialized.</span></span> <span data-ttu-id="85414-262">Если вы перейдете к этому методу среду, она переопределит все параметры, заданные в свойстве CreationProperties.</span><span class="sxs-lookup"><span data-stu-id="85414-262">If you pass an environment to this method then it will override any settings specified on the CreationProperties property.</span></span> <span data-ttu-id="85414-263">Если вы передали null (значение по умолчанию) и для него не установлено значение CreationProperties, среда по умолчанию будет создана и использоваться автоматически.</span><span class="sxs-lookup"><span data-stu-id="85414-263">If you pass null (the default value) and no value has been set to CreationProperties then a default environment will be created and used automatically.</span></span> 

##### <span data-ttu-id="85414-264">Дает</span><span class="sxs-lookup"><span data-stu-id="85414-264">Returns</span></span>
<span data-ttu-id="85414-265">Задача, представляющая собой процесс инициализации фона.</span><span class="sxs-lookup"><span data-stu-id="85414-265">A Task that represents the background initialization process.</span></span> <span data-ttu-id="85414-266">После завершения задачи свойство CoreWebView2 будет доступно для использования (то есть без значения NULL).</span><span class="sxs-lookup"><span data-stu-id="85414-266">When the task completes then the CoreWebView2 property will be available for use (i.e. non-null).</span></span> <span data-ttu-id="85414-267">Обратите внимание, что событие CoreWebView2Ready элемента управления будет вызвано до завершения задачи.</span><span class="sxs-lookup"><span data-stu-id="85414-267">Note that the control's CoreWebView2Ready event will be invoked before the task completes.</span></span> 

<span data-ttu-id="85414-268">Повторный вызов этого метода не повлияет (любая указанная среда игнорируется) и возвращает ту же задачу, что и первый вызов.</span><span class="sxs-lookup"><span data-stu-id="85414-268">Calling this method additional times will have no effect (any specified environment is ignored) and return the same Task as the first call.</span></span> <span data-ttu-id="85414-269">Вызов этого метода после того, как инициализация вызывается явным образом посредством задания свойства Source, не будет оказывать никакого воздействия (любая указанная среда игнорируется) и просто возвращать задачу, представляющую уже выполняющуюся инициализацию.</span><span class="sxs-lookup"><span data-stu-id="85414-269">Calling this method after initialization has been implicitly triggered by setting the Source property will have no effect (any specified environment is ignored) and simply return a Task representing that initialization already in progress.</span></span> <span data-ttu-id="85414-270">Обратите внимание, что несмотря на то, что этот метод является асинхронным и возвращает задачу, она по-прежнему должна вызываться в потоке пользовательского интерфейса, например в большинстве открытых функций элементов управления пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="85414-270">Note that even though this method is asynchronous and returns a Task, it still must be called on the UI thread like most public functionality of most UI controls.</span></span> 

##### <span data-ttu-id="85414-271">Исключения</span><span class="sxs-lookup"><span data-stu-id="85414-271">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="85414-272">Создается, если вызывающий поток не является потоком, который создал этот объект (обычно это поток пользовательского интерфейса).</span><span class="sxs-lookup"><span data-stu-id="85414-272">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="85414-273">Для получения дополнительных сведений ознакомьтесь с DispatcherObject. VerifyAccess.</span><span class="sxs-lookup"><span data-stu-id="85414-273">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="85414-274">Вызывается, если метод Dispose уже вызывался для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="85414-274">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="85414-275">ExecuteScriptAsync</span><span class="sxs-lookup"><span data-stu-id="85414-275">ExecuteScriptAsync</span></span> 

<span data-ttu-id="85414-276">Выполняет код JavaScript из параметра javaScript в текущем документе верхнего уровня, отображаемом в WebView.</span><span class="sxs-lookup"><span data-stu-id="85414-276">Executes JavaScript code from the javaScript parameter in the current top level document rendered in the WebView.</span></span>

> <span data-ttu-id="85414-277">общедоступная асинхронная задача< String > [ExecuteScriptAsync](#executescriptasync)(String JavaScript)</span><span class="sxs-lookup"><span data-stu-id="85414-277">public async Task< string > [ExecuteScriptAsync](#executescriptasync)(string javaScript)</span></span>

<span data-ttu-id="85414-278">Эквивалентно вызову CoreWebView2. ExecuteScriptAsync на CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="85414-278">Equivalent to calling CoreWebView2.ExecuteScriptAsync on CoreWebView2</span></span>

##### <span data-ttu-id="85414-279">Исключения</span><span class="sxs-lookup"><span data-stu-id="85414-279">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="85414-280">Вызывается, если CoreWebView2 еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="85414-280">Thrown if CoreWebView2 hasn't been initialized yet.</span></span>

* `InvalidOperationException` <span data-ttu-id="85414-281">Создается, если вызывающий поток не является потоком, который создал этот объект (обычно это поток пользовательского интерфейса).</span><span class="sxs-lookup"><span data-stu-id="85414-281">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="85414-282">Для получения дополнительных сведений ознакомьтесь с DispatcherObject. VerifyAccess.</span><span class="sxs-lookup"><span data-stu-id="85414-282">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="85414-283">Вызывается, если метод Dispose уже вызывался для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="85414-283">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="85414-284">GoBack</span><span class="sxs-lookup"><span data-stu-id="85414-284">GoBack</span></span> 

<span data-ttu-id="85414-285">Переход по WebView на предыдущую страницу в истории навигации.</span><span class="sxs-lookup"><span data-stu-id="85414-285">Navigates the WebView to the previous page in the navigation history.</span></span>

> <span data-ttu-id="85414-286">общедоступная void [GoBack](#goback)()</span><span class="sxs-lookup"><span data-stu-id="85414-286">public void [GoBack](#goback)()</span></span>

<span data-ttu-id="85414-287">Эквивалентно вызову CoreWebView2. GoBack на CoreWebView2, если CoreWebView2 еще не инициализирован, но не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="85414-287">Equivalent to calling CoreWebView2.GoBack on CoreWebView2 If CoreWebView2 hasn't been initialized yet then does nothing.</span></span>

##### <span data-ttu-id="85414-288">Исключения</span><span class="sxs-lookup"><span data-stu-id="85414-288">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="85414-289">Создается, если вызывающий поток не является потоком, который создал этот объект (обычно это поток пользовательского интерфейса).</span><span class="sxs-lookup"><span data-stu-id="85414-289">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="85414-290">Для получения дополнительных сведений ознакомьтесь с DispatcherObject. VerifyAccess.</span><span class="sxs-lookup"><span data-stu-id="85414-290">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="85414-291">Вызывается, если метод Dispose уже вызывался для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="85414-291">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="85414-292">GoForward</span><span class="sxs-lookup"><span data-stu-id="85414-292">GoForward</span></span> 

<span data-ttu-id="85414-293">Переход по WebView к следующей странице в истории навигации.</span><span class="sxs-lookup"><span data-stu-id="85414-293">Navigates the WebView to the next page in the navigation history.</span></span>

> <span data-ttu-id="85414-294">общедоступная void [GoForward](#goforward)()</span><span class="sxs-lookup"><span data-stu-id="85414-294">public void [GoForward](#goforward)()</span></span>

<span data-ttu-id="85414-295">Эквивалентно вызову CoreWebView2. GoForward в CoreWebView2, если CoreWebView2 еще не инициализирован, но не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="85414-295">Equivalent to calling CoreWebView2.GoForward on CoreWebView2 If CoreWebView2 hasn't been initialized yet then does nothing.</span></span>

##### <span data-ttu-id="85414-296">Исключения</span><span class="sxs-lookup"><span data-stu-id="85414-296">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="85414-297">Создается, если вызывающий поток не является потоком, который создал этот объект (обычно это поток пользовательского интерфейса).</span><span class="sxs-lookup"><span data-stu-id="85414-297">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span> <span data-ttu-id="85414-298">Для получения дополнительных сведений ознакомьтесь с DispatcherObject. VerifyAccess.</span><span class="sxs-lookup"><span data-stu-id="85414-298">See DispatcherObject.VerifyAccess for more info.</span></span>

* `ObjectDisposedException` <span data-ttu-id="85414-299">Вызывается, если метод Dispose уже вызывался для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="85414-299">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="85414-300">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="85414-300">NavigateToString</span></span> 

<span data-ttu-id="85414-301">Запускает навигацию для htmlContent в качестве исходного HTML-кода нового документа.</span><span class="sxs-lookup"><span data-stu-id="85414-301">Initiates a navigation to htmlContent as source HTML of a new document.</span></span>

> <span data-ttu-id="85414-302">Public void [NavigateToString](#navigatetostring)(строка htmlContent)</span><span class="sxs-lookup"><span data-stu-id="85414-302">public void [NavigateToString](#navigatetostring)(string htmlContent)</span></span>

<span data-ttu-id="85414-303">Эквивалентно вызову CoreWebView2. NavigateToString на CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="85414-303">Equivalent to calling CoreWebView2.NavigateToString on CoreWebView2</span></span>

##### <span data-ttu-id="85414-304">Исключения</span><span class="sxs-lookup"><span data-stu-id="85414-304">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="85414-305">Вызывается, если CoreWebView2 еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="85414-305">Thrown if CoreWebView2 hasn't been initialized yet.</span></span>

<span data-ttu-id="85414-306">" <exception cref="InvalidOperationException"> Создается, если вызывающий поток не является потоком, который создал этот объект (обычно — потоком пользовательского интерфейса).</span><span class="sxs-lookup"><span data-stu-id="85414-306">" <exception cref="InvalidOperationException">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span>  <span data-ttu-id="85414-307">Для получения дополнительных сведений </exception>
<exception cref="ObjectDisposedException"> Ознакомьтесь с DispatcherObject. VerifyAccess. Вызывается, если метод Dispose уже вызывался для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="85414-307">See DispatcherObject.VerifyAccess for more info.</exception>
<exception cref="ObjectDisposedException">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="85414-308">Перезагрузить</span><span class="sxs-lookup"><span data-stu-id="85414-308">Reload</span></span> 

<span data-ttu-id="85414-309">Перезагружает текущую страницу.</span><span class="sxs-lookup"><span data-stu-id="85414-309">Reloads the current page.</span></span>

> <span data-ttu-id="85414-310">общедоступный void [Reload](#reload)()</span><span class="sxs-lookup"><span data-stu-id="85414-310">public void [Reload](#reload)()</span></span>

<span data-ttu-id="85414-311">Эквивалентно вызову CoreWebView2. Reload для CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="85414-311">Equivalent to calling CoreWebView2.Reload on CoreWebView2</span></span>

##### <span data-ttu-id="85414-312">Исключения</span><span class="sxs-lookup"><span data-stu-id="85414-312">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="85414-313">Вызывается, если CoreWebView2 еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="85414-313">Thrown if CoreWebView2 hasn't been initialized yet.</span></span>

<span data-ttu-id="85414-314">" <exception cref="InvalidOperationException"> Создается, если вызывающий поток не является потоком, который создал этот объект (обычно — потоком пользовательского интерфейса).</span><span class="sxs-lookup"><span data-stu-id="85414-314">" <exception cref="InvalidOperationException">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span>  <span data-ttu-id="85414-315">Для получения дополнительных сведений </exception>
<exception cref="ObjectDisposedException"> Ознакомьтесь с DispatcherObject. VerifyAccess. Вызывается, если метод Dispose уже вызывался для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="85414-315">See DispatcherObject.VerifyAccess for more info.</exception>
<exception cref="ObjectDisposedException">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="85414-316">Stop</span><span class="sxs-lookup"><span data-stu-id="85414-316">Stop</span></span> 

<span data-ttu-id="85414-317">Остановка всех переходов и ожидающих выборок ресурсов.</span><span class="sxs-lookup"><span data-stu-id="85414-317">Stops all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="85414-318">открытая пустая [Отмена](#stop)()</span><span class="sxs-lookup"><span data-stu-id="85414-318">public void [Stop](#stop)()</span></span>

<span data-ttu-id="85414-319">Эквивалентно вызову CoreWebView2. Stop на CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="85414-319">Equivalent to calling CoreWebView2.Stop on CoreWebView2</span></span>

##### <span data-ttu-id="85414-320">Исключения</span><span class="sxs-lookup"><span data-stu-id="85414-320">Exceptions</span></span>
* `InvalidOperationException` <span data-ttu-id="85414-321">Вызывается, если CoreWebView2 еще не инициализирован.</span><span class="sxs-lookup"><span data-stu-id="85414-321">Thrown if CoreWebView2 hasn't been initialized yet.</span></span>

<span data-ttu-id="85414-322">" <exception cref="InvalidOperationException"> Создается, если вызывающий поток не является потоком, который создал этот объект (обычно — потоком пользовательского интерфейса).</span><span class="sxs-lookup"><span data-stu-id="85414-322">" <exception cref="InvalidOperationException">Thrown if the calling thread isn't the thread which created this object (usually the UI thread).</span></span>  <span data-ttu-id="85414-323">Для получения дополнительных сведений </exception>
<exception cref="ObjectDisposedException"> Ознакомьтесь с DispatcherObject. VerifyAccess. Вызывается, если метод Dispose уже вызывался для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="85414-323">See DispatcherObject.VerifyAccess for more info.</exception>
<exception cref="ObjectDisposedException">Thrown if Dispose has already been called on the control.</span></span>

#### <span data-ttu-id="85414-324">WebView2</span><span class="sxs-lookup"><span data-stu-id="85414-324">WebView2</span></span> 

<span data-ttu-id="85414-325">Создает новый экземпляр элемента управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="85414-325">Creates a new instance of a WebView2 control.</span></span>

> <span data-ttu-id="85414-326">общедоступная [WebView2](#webview2)()</span><span class="sxs-lookup"><span data-stu-id="85414-326">public [WebView2](#webview2)()</span></span>

<span data-ttu-id="85414-327">Обратите внимание, что CoreWebView2 элемента управления будет иметь значение null до инициализации.</span><span class="sxs-lookup"><span data-stu-id="85414-327">Note that the control's CoreWebView2 will be null until initialized.</span></span> <span data-ttu-id="85414-328">Ознакомьтесь с документацией по классу WebView2 для обзора инициализации.</span><span class="sxs-lookup"><span data-stu-id="85414-328">See the WebView2 class documentation for an initialization overview.</span></span>

#### <span data-ttu-id="85414-329">BuildWindowCore</span><span class="sxs-lookup"><span data-stu-id="85414-329">BuildWindowCore</span></span> 

<span data-ttu-id="85414-330">Это значение переопределяется из HwndHost и вызывается, чтобы сообщить нам о необходимости создать HWND.</span><span class="sxs-lookup"><span data-stu-id="85414-330">This is overridden from HwndHost and is called to instruct us to create our HWND.</span></span>

> <span data-ttu-id="85414-331">Protected override HandleRef [BuildWindowCore](#buildwindowcore)(HandleRef hwndParent)</span><span class="sxs-lookup"><span data-stu-id="85414-331">protected override HandleRef [BuildWindowCore](#buildwindowcore)(HandleRef hwndParent)</span></span>

##### <span data-ttu-id="85414-332">Параметры</span><span class="sxs-lookup"><span data-stu-id="85414-332">Parameters</span></span>
* `hwndParent` <span data-ttu-id="85414-333">HWND, который необходимо использовать в качестве родительского элемента, который мы создаем.</span><span class="sxs-lookup"><span data-stu-id="85414-333">The HWND that we should use as the parent of the one we create.</span></span>

##### <span data-ttu-id="85414-334">Дает</span><span class="sxs-lookup"><span data-stu-id="85414-334">Returns</span></span>
<span data-ttu-id="85414-335">Созданный дескриптор HWND.</span><span class="sxs-lookup"><span data-stu-id="85414-335">The HWND that we created.</span></span>

#### <span data-ttu-id="85414-336">DestroyWindowCore</span><span class="sxs-lookup"><span data-stu-id="85414-336">DestroyWindowCore</span></span> 

<span data-ttu-id="85414-337">Это значение переопределяется из HwndHost и вызывается, чтобы дать нам команду уничтожить наш HWND.</span><span class="sxs-lookup"><span data-stu-id="85414-337">This is overridden from HwndHost and is called to instruct us to destroy our HWND.</span></span>

> <span data-ttu-id="85414-338">Protected override void [DestroyWindowCore](#destroywindowcore)(HandleRef HWND)</span><span class="sxs-lookup"><span data-stu-id="85414-338">protected override void [DestroyWindowCore](#destroywindowcore)(HandleRef hwnd)</span></span>

##### <span data-ttu-id="85414-339">Параметры</span><span class="sxs-lookup"><span data-stu-id="85414-339">Parameters</span></span>
* `hwnd` <span data-ttu-id="85414-340">HWND, который нам нужно уничтожить.</span><span class="sxs-lookup"><span data-stu-id="85414-340">Our HWND that we need to destroy.</span></span>

#### <span data-ttu-id="85414-341">Ликвидация</span><span class="sxs-lookup"><span data-stu-id="85414-341">Dispose</span></span> 

<span data-ttu-id="85414-342">Этот базовый класс вызывается в соответствии с типичной реализацией шаблона IDispose.</span><span class="sxs-lookup"><span data-stu-id="85414-342">This is called by our base class according to the typical implementation of the IDispose pattern.</span></span>

> <span data-ttu-id="85414-343">защищенное переопределение void [Dispose](#dispose)(bool disposing)</span><span class="sxs-lookup"><span data-stu-id="85414-343">protected override void [Dispose](#dispose)(bool disposing)</span></span>

<span data-ttu-id="85414-344">Мы реализуем ее, освобождая все наши базовые COM-ресурсы, в том числе наш CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="85414-344">We implement it by releasing all of our underlying COM resources, including our CoreWebView2.</span></span>

##### <span data-ttu-id="85414-345">Параметры</span><span class="sxs-lookup"><span data-stu-id="85414-345">Parameters</span></span>
* `disposing` <span data-ttu-id="85414-346">Значение true, если вызывающий объект явным образом вызывает Dispose, и false, если мы завершаем себя.</span><span class="sxs-lookup"><span data-stu-id="85414-346">True if a caller is explicitly calling Dispose, false if we're being finalized.</span></span>

#### <span data-ttu-id="85414-347">HasFocusWithinCore</span><span class="sxs-lookup"><span data-stu-id="85414-347">HasFocusWithinCore</span></span> 

<span data-ttu-id="85414-348">Это значение переопределяется из HwndHost и вызывается, когда для WPF требуется узнать, находится ли фокус в нашем элементе управления/окне.</span><span class="sxs-lookup"><span data-stu-id="85414-348">This is overridden from HwndHost and is called when WPF needs to know if the focus is in our control/window.</span></span>

> <span data-ttu-id="85414-349">bool protected override [HasFocusWithinCore](#hasfocuswithincore)()</span><span class="sxs-lookup"><span data-stu-id="85414-349">protected override bool [HasFocusWithinCore](#hasfocuswithincore)()</span></span>

<span data-ttu-id="85414-350">WPF не может самостоятельно знать, так как мы размещаете окно, отличное от WPF, поэтому он запрашивает его, вызывая этот метод.</span><span class="sxs-lookup"><span data-stu-id="85414-350">WPF can't know on its own since we're hosting a non-WPF window, so instead it asks us by calling this.</span></span> <span data-ttu-id="85414-351">Для ответа мы просто отслеживаем состояние на основе событий CoreWebView2, которые инициируются, когда он получает или теряет фокус.</span><span class="sxs-lookup"><span data-stu-id="85414-351">To answer, we just track state based on CoreWebView2 events that fire when it gains or loses focus.</span></span>

##### <span data-ttu-id="85414-352">Дает</span><span class="sxs-lookup"><span data-stu-id="85414-352">Returns</span></span>
<span data-ttu-id="85414-353">Значение true, если фокус находится в нашем элементе управления/окне, в противном случае — значение false.</span><span class="sxs-lookup"><span data-stu-id="85414-353">True if the focus is in our control/window, false if it isn't.</span></span>

#### <span data-ttu-id="85414-354">OnKeyDown</span><span class="sxs-lookup"><span data-stu-id="85414-354">OnKeyDown</span></span> 

<span data-ttu-id="85414-355">Это значение переопределяется из UIElement и вызывается, чтобы позволить нам обрабатывать нажатия клавиши ввода.</span><span class="sxs-lookup"><span data-stu-id="85414-355">This is overridden from UIElement and called to allow us to handle key press input.</span></span>

> <span data-ttu-id="85414-356">Protected override void [OnKeyDown](#onkeydown)(KeyEventArgs e)</span><span class="sxs-lookup"><span data-stu-id="85414-356">protected override void [OnKeyDown](#onkeydown)(KeyEventArgs e)</span></span>

<span data-ttu-id="85414-357">Платформа WPF никогда не должна вызывать этот метод в ответ на события клавиатуры, так как мы разключаемся окном, не являющимся WPF.</span><span class="sxs-lookup"><span data-stu-id="85414-357">WPF should never actually call this in response to keyboard events because we're hosting a non-WPF window.</span></span> <span data-ttu-id="85414-358">Когда в нашем окне фокуса, данные пересылаются непосредственно в него, а не в окно верхнего уровня WPF и на систему ввода.</span><span class="sxs-lookup"><span data-stu-id="85414-358">When our window has focus Windows will send the input directly to it rather than to WPF's top-level window and input system.</span></span> <span data-ttu-id="85414-359">Это переопределение следует вызывать только в том случае, если вы явным образом пересылаете клавишу быстрого ввода из CoreWebView2 в WPF (в CoreWebView2Controller_AcceleratorKeyPressed).</span><span class="sxs-lookup"><span data-stu-id="85414-359">This override should only be called when we're explicitly forwarding accelerator key input from the CoreWebView2 to WPF (in CoreWebView2Controller_AcceleratorKeyPressed).</span></span> <span data-ttu-id="85414-360">Несмотря на это, этот KeyDownEvent активируется, так как наша реализация PreviewKeyDownEvent явным образом запускает ее, а соответствующие системы WPF — с обычной системой.</span><span class="sxs-lookup"><span data-stu-id="85414-360">Even then, this KeyDownEvent is only triggered because our PreviewKeyDownEvent implementation explicitly triggers it, matching WPF's usual system.</span></span> <span data-ttu-id="85414-361">Итак, процесс: CoreWebView2Controller_AcceleratorKeyPressed-> вызвать PreviewKeyDownEvent-> OnPreviewKeyDown-> вызвать KeyDownEvent-> OnKeyDown</span><span class="sxs-lookup"><span data-stu-id="85414-361">So the process is: CoreWebView2Controller_AcceleratorKeyPressed -> raise PreviewKeyDownEvent -> OnPreviewKeyDown -> raise KeyDownEvent -> OnKeyDown</span></span>

#### <span data-ttu-id="85414-362">OnKeyUp</span><span class="sxs-lookup"><span data-stu-id="85414-362">OnKeyUp</span></span> 

<span data-ttu-id="85414-363">Смотрите клавишу KeyDown.</span><span class="sxs-lookup"><span data-stu-id="85414-363">See OnKeyDown.</span></span>

> <span data-ttu-id="85414-364">Protected override void [OnKeyUp](#onkeyup)(KeyEventArgs e)</span><span class="sxs-lookup"><span data-stu-id="85414-364">protected override void [OnKeyUp](#onkeyup)(KeyEventArgs e)</span></span>

#### <span data-ttu-id="85414-365">OnPreviewKeyDown</span><span class="sxs-lookup"><span data-stu-id="85414-365">OnPreviewKeyDown</span></span> 

<span data-ttu-id="85414-366">Это "предварительный просмотр" (т. е.</span><span class="sxs-lookup"><span data-stu-id="85414-366">This is the "Preview" (i.e.</span></span>

> <span data-ttu-id="85414-367">Protected override void [OnPreviewKeyDown](#onpreviewkeydown)(KeyEventArgs e)</span><span class="sxs-lookup"><span data-stu-id="85414-367">protected override void [OnPreviewKeyDown](#onpreviewkeydown)(KeyEventArgs e)</span></span>

<span data-ttu-id="85414-368">для создания туннелей), поэтому на самом деле оно происходит в первую очередь.</span><span class="sxs-lookup"><span data-stu-id="85414-368">tunneling) version of OnKeyDown, so it actually happens first.</span></span> <span data-ttu-id="85414-369">Как и в случае с помощью клавиш со стрелками, этот метод будет вызываться только в том случае, если вы явным образом перейдете на клавиши CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="85414-369">Like OnKeyDown, this will only ever be called if we're explicitly forwarding key presses from the CoreWebView2.</span></span> <span data-ttu-id="85414-370">Чтобы имитировать стандартную обработку ввода в WPF, когда мы получим это, мы постараемся обойти и отпустить стандартную KeyDownEventную восходящую очередь.</span><span class="sxs-lookup"><span data-stu-id="85414-370">In order to mimic WPF's standard input handling, when we receive this we turn around and fire off the standard bubbling KeyDownEvent.</span></span> <span data-ttu-id="85414-371">Таким образом, другие пользователи в дереве WPF будут видеть одну и ту же стандартную пару событий ввода, которые сам WPF инициировал при обработке нажатия клавиши.</span><span class="sxs-lookup"><span data-stu-id="85414-371">That way others in the WPF tree see the same standard pair of input events that WPF itself would have triggered if it were handling the key press.</span></span>

#### <span data-ttu-id="85414-372">OnPreviewKeyUp</span><span class="sxs-lookup"><span data-stu-id="85414-372">OnPreviewKeyUp</span></span> 

<span data-ttu-id="85414-373">Смотрите OnPreviewKeyDown.</span><span class="sxs-lookup"><span data-stu-id="85414-373">See OnPreviewKeyDown.</span></span>

> <span data-ttu-id="85414-374">Protected override void [OnPreviewKeyUp](#onpreviewkeyup)(KeyEventArgs e)</span><span class="sxs-lookup"><span data-stu-id="85414-374">protected override void [OnPreviewKeyUp](#onpreviewkeyup)(KeyEventArgs e)</span></span>

#### <span data-ttu-id="85414-375">OnWindowPositionChanged</span><span class="sxs-lookup"><span data-stu-id="85414-375">OnWindowPositionChanged</span></span> 

<span data-ttu-id="85414-376">Этот метод переопределен из HwndHost и вызывается, когда изменилось положение элемента управления.</span><span class="sxs-lookup"><span data-stu-id="85414-376">This is overridden from HwndHost and called when our control's location has changed.</span></span>

> <span data-ttu-id="85414-377">Protected override void [OnWindowPositionChanged](#onwindowpositionchanged)(Rect rcBoundingBox)</span><span class="sxs-lookup"><span data-stu-id="85414-377">protected override void [OnWindowPositionChanged](#onwindowpositionchanged)(Rect rcBoundingBox)</span></span>

<span data-ttu-id="85414-378">HwndHost позаботится о том, что мы создали HWND.</span><span class="sxs-lookup"><span data-stu-id="85414-378">The HwndHost takes care of updating the HWND we created.</span></span> <span data-ttu-id="85414-379">Что нам нужно сделать — это переместить наш CoreWebView2 в соответствие с новым расположением.</span><span class="sxs-lookup"><span data-stu-id="85414-379">What we need to do is move our CoreWebView2 to match the new location.</span></span>

#### <span data-ttu-id="85414-380">TabIntoCore</span><span class="sxs-lookup"><span data-stu-id="85414-380">TabIntoCore</span></span> 

<span data-ttu-id="85414-381">Это значение переопределяется из HwndHost и вызывается, чтобы сообщить нам, что переход на вкладку привел к переходу фокуса на наш элемент управления/окно.</span><span class="sxs-lookup"><span data-stu-id="85414-381">This is overridden from HwndHost and is called to inform us that tabbing has caused the focus to move into our control/window.</span></span>

> <span data-ttu-id="85414-382">[TabIntoCore](#tabintocore)protected override bool (запрос TraversalRequest)</span><span class="sxs-lookup"><span data-stu-id="85414-382">protected override bool [TabIntoCore](#tabintocore)(TraversalRequest request)</span></span>

<span data-ttu-id="85414-383">Так как WPF не может управлять переходом фокуса на HWND, не относящийся к WPF, он делегирует переход нам здесь.</span><span class="sxs-lookup"><span data-stu-id="85414-383">Since WPF can't manage the transition of focus to a non-WPF HWND, it delegates the transition to us here.</span></span> <span data-ttu-id="85414-384">Итак, наша задача – это просто поместить фокус на внешний HWND.</span><span class="sxs-lookup"><span data-stu-id="85414-384">So our job is just to place the focus in our external HWND.</span></span>

##### <span data-ttu-id="85414-385">Параметры</span><span class="sxs-lookup"><span data-stu-id="85414-385">Parameters</span></span>
* `request` <span data-ttu-id="85414-386">Информация о том, как перемещается фокус.</span><span class="sxs-lookup"><span data-stu-id="85414-386">Information about how the focus is moving.</span></span>

##### <span data-ttu-id="85414-387">Дает</span><span class="sxs-lookup"><span data-stu-id="85414-387">Returns</span></span>
<span data-ttu-id="85414-388">Значение true, чтобы указать, что мы обработали навигацию, или ложь, чтобы указать, что мы не смогли.</span><span class="sxs-lookup"><span data-stu-id="85414-388">True to indicate that we handled the navigation, or false to indicate that we didn't.</span></span>

