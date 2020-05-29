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
ms.openlocfilehash: 532c898845125564ad5af6460dc8d1ff6464abfb
ms.sourcegitcommit: 83efa259be89cc773a82751242495a0a919d54cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2020
ms.locfileid: "10687806"
---
# <span data-ttu-id="a1b92-104">Класс Microsoft. Web. WebView2. WinForms. WebView2</span><span class="sxs-lookup"><span data-stu-id="a1b92-104">Microsoft.Web.WebView2.WinForms.WebView2 class</span></span> 

<span data-ttu-id="a1b92-105">Пространство имен: Microsoft. Web. WebView2. WinForms </span><span class="sxs-lookup"><span data-stu-id="a1b92-105">Namespace: Microsoft.Web.WebView2.WinForms</span></span>\
<span data-ttu-id="a1b92-106">Assembly: Microsoft. Web. WebView2. WinForms. dll</span><span class="sxs-lookup"><span data-stu-id="a1b92-106">Assembly: Microsoft.Web.WebView2.WinForms.dll</span></span>

```
class Microsoft.Web.WebView2.WinForms.WebView2
  : public Control
```

<span data-ttu-id="a1b92-107">Элемент управления для внедрения WebView2 в WinForms.</span><span class="sxs-lookup"><span data-stu-id="a1b92-107">Control to embed WebView2 in WinForms.</span></span>

## <span data-ttu-id="a1b92-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="a1b92-108">Summary</span></span>

 <span data-ttu-id="a1b92-109">Участников</span><span class="sxs-lookup"><span data-stu-id="a1b92-109">Members</span></span>                        | <span data-ttu-id="a1b92-110">Описания</span><span class="sxs-lookup"><span data-stu-id="a1b92-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a1b92-111">ContentLoading</span><span class="sxs-lookup"><span data-stu-id="a1b92-111">ContentLoading</span></span>](#contentloading) | <span data-ttu-id="a1b92-112">ContentLoading отправляется после того, как начинается переход с нового URI и начинается визуализация содержимого этого URI.</span><span class="sxs-lookup"><span data-stu-id="a1b92-112">ContentLoading dispatches after a navigation begins to a new URI and the content of that URI begins to render.</span></span>
[<span data-ttu-id="a1b92-113">CoreWebView2Ready</span><span class="sxs-lookup"><span data-stu-id="a1b92-113">CoreWebView2Ready</span></span>](#corewebview2ready) | <span data-ttu-id="a1b92-114">Это событие запускается, когда [CoreWebView2](#corewebview2) элемента управления завершает инициализацию (независимо от того, как был инициирована инициализация), но до того, как он будет использоваться для чего-либо.</span><span class="sxs-lookup"><span data-stu-id="a1b92-114">This event is triggered when the control's [CoreWebView2](#corewebview2) has finished being initialized (regardless of how initialization was triggered) but before it is used for anything.</span></span>
[<span data-ttu-id="a1b92-115">NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="a1b92-115">NavigationCompleted</span></span>](#navigationcompleted) | <span data-ttu-id="a1b92-116">NavigationCompleted отправляется после того, как переход по документу верхнего уровня завершает обработку успешно или нет.</span><span class="sxs-lookup"><span data-stu-id="a1b92-116">NavigationCompleted dispatches after a navigate of the top level document completes rendering either successfully or not.</span></span>
[<span data-ttu-id="a1b92-117">NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="a1b92-117">NavigationStarting</span></span>](#navigationstarting) | <span data-ttu-id="a1b92-118">NavigationStarting отправляется перед началом новой навигации для документа верхнего уровня в WebView2.</span><span class="sxs-lookup"><span data-stu-id="a1b92-118">NavigationStarting dispatches before a new navigate starts for the top level document of the WebView2.</span></span>
[<span data-ttu-id="a1b92-119">SourceChanged</span><span class="sxs-lookup"><span data-stu-id="a1b92-119">SourceChanged</span></span>](#sourcechanged) | <span data-ttu-id="a1b92-120">SourceChanged отправляется после изменения исходного свойства.</span><span class="sxs-lookup"><span data-stu-id="a1b92-120">SourceChanged dispatches after the Source property changes.</span></span>
[<span data-ttu-id="a1b92-121">WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="a1b92-121">WebMessageReceived</span></span>](#webmessagereceived) | <span data-ttu-id="a1b92-122">WebMessageReceived отправляет сообщение на узел приложения с помощью отправки по сети `chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="a1b92-122">WebMessageReceived dispatches after web content sends a message to the app host via `chrome.webview.postMessage`.</span></span>
[<span data-ttu-id="a1b92-123">CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="a1b92-123">CoreWebView2</span></span>](#corewebview2) | <span data-ttu-id="a1b92-124">Основной CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="a1b92-124">The underlying CoreWebView2.</span></span>
[<span data-ttu-id="a1b92-125">Источник</span><span class="sxs-lookup"><span data-stu-id="a1b92-125">Source</span></span>](#source) | <span data-ttu-id="a1b92-126">Свойство Source — это URI документа верхнего уровня в WebView2.</span><span class="sxs-lookup"><span data-stu-id="a1b92-126">The Source property is the URI of the top level document of the WebView2.</span></span>
[<span data-ttu-id="a1b92-127">ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="a1b92-127">ZoomFactor</span></span>](#zoomfactor) | <span data-ttu-id="a1b92-128">Коэффициент масштабирования для WebView.</span><span class="sxs-lookup"><span data-stu-id="a1b92-128">The zoom factor for the WebView.</span></span>
[<span data-ttu-id="a1b92-129">CanGoBack</span><span class="sxs-lookup"><span data-stu-id="a1b92-129">CanGoBack</span></span>](#cangoback) | <span data-ttu-id="a1b92-130">Возвращает значение истина, если WebView может перейти на предыдущую страницу в истории навигации с помощью метода GoBack.</span><span class="sxs-lookup"><span data-stu-id="a1b92-130">Returns true if the webview can navigate to a previous page in the navigation history via the GoBack method.</span></span>
[<span data-ttu-id="a1b92-131">CanGoForward</span><span class="sxs-lookup"><span data-stu-id="a1b92-131">CanGoForward</span></span>](#cangoforward) | <span data-ttu-id="a1b92-132">Возвращает значение "истина", если WebView может перейти к следующей странице в журнале переходов с помощью метода GoForward.</span><span class="sxs-lookup"><span data-stu-id="a1b92-132">Returns true if the webview can navigate to a next page in the navigation history via the GoForward method.</span></span>
[<span data-ttu-id="a1b92-133">EnsureCoreWebView2Async</span><span class="sxs-lookup"><span data-stu-id="a1b92-133">EnsureCoreWebView2Async</span></span>](#ensurecorewebview2async) | <span data-ttu-id="a1b92-134">Явным образом инициализируйте инициализацию [CoreWebView2](#corewebview2)элемента управления.</span><span class="sxs-lookup"><span data-stu-id="a1b92-134">Explicitly trigger initialization of the control's [CoreWebView2](#corewebview2).</span></span>
[<span data-ttu-id="a1b92-135">ExecuteScriptAsync</span><span class="sxs-lookup"><span data-stu-id="a1b92-135">ExecuteScriptAsync</span></span>](#executescriptasync) | <span data-ttu-id="a1b92-136">Выполняет представленный сценарий в документе верхнего уровня элемента WebView2.</span><span class="sxs-lookup"><span data-stu-id="a1b92-136">Executes the provided script in the top level document of the WebView2.</span></span>
[<span data-ttu-id="a1b92-137">GoBack</span><span class="sxs-lookup"><span data-stu-id="a1b92-137">GoBack</span></span>](#goback) | <span data-ttu-id="a1b92-138">Переход на предыдущую страницу в истории навигации.</span><span class="sxs-lookup"><span data-stu-id="a1b92-138">Navigate to the previous page in navigation history.</span></span>
[<span data-ttu-id="a1b92-139">GoForward</span><span class="sxs-lookup"><span data-stu-id="a1b92-139">GoForward</span></span>](#goforward) | <span data-ttu-id="a1b92-140">Переход к следующей странице в журнале переходов.</span><span class="sxs-lookup"><span data-stu-id="a1b92-140">Navigate to the next page in navigation history.</span></span>
[<span data-ttu-id="a1b92-141">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="a1b92-141">NavigateToString</span></span>](#navigatetostring) | <span data-ttu-id="a1b92-142">Обрабатывают представленный HTML-код как документ верхнего уровня для элемента WebView2.</span><span class="sxs-lookup"><span data-stu-id="a1b92-142">Render the provided HTML as the top level document of the WebView2.</span></span>
[<span data-ttu-id="a1b92-143">Перезагрузить</span><span class="sxs-lookup"><span data-stu-id="a1b92-143">Reload</span></span>](#reload) | <span data-ttu-id="a1b92-144">Перезагрузите документ верхнего уровня в WebView2.</span><span class="sxs-lookup"><span data-stu-id="a1b92-144">Reload the top level document of the WebView2.</span></span>
[<span data-ttu-id="a1b92-145">Stop</span><span class="sxs-lookup"><span data-stu-id="a1b92-145">Stop</span></span>](#stop) | <span data-ttu-id="a1b92-146">Остановите ход выполнения навигации в WebView2.</span><span class="sxs-lookup"><span data-stu-id="a1b92-146">Stop any in progress navigation in the WebView2.</span></span>
[<span data-ttu-id="a1b92-147">WebView2</span><span class="sxs-lookup"><span data-stu-id="a1b92-147">WebView2</span></span>](#webview2) | <span data-ttu-id="a1b92-148">Создайте новый элемент управления WebView2 WinForms.</span><span class="sxs-lookup"><span data-stu-id="a1b92-148">Create a new WebView2 WinForms control.</span></span>

## <span data-ttu-id="a1b92-149">Участников</span><span class="sxs-lookup"><span data-stu-id="a1b92-149">Members</span></span>

#### <span data-ttu-id="a1b92-150">ContentLoading</span><span class="sxs-lookup"><span data-stu-id="a1b92-150">ContentLoading</span></span> 

<span data-ttu-id="a1b92-151">ContentLoading отправляется после того, как начинается переход с нового URI и начинается визуализация содержимого этого URI.</span><span class="sxs-lookup"><span data-stu-id="a1b92-151">ContentLoading dispatches after a navigation begins to a new URI and the content of that URI begins to render.</span></span>

> <span data-ttu-id="a1b92-152">событие EventHandler< CoreWebView2ContentLoadingEventArgs > [ContentLoading](#contentloading)</span><span class="sxs-lookup"><span data-stu-id="a1b92-152">public event EventHandler< CoreWebView2ContentLoadingEventArgs > [ContentLoading](#contentloading)</span></span>

<span data-ttu-id="a1b92-153">Это эквивалентно событию ContentLoading в CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="a1b92-153">This is equivalent to the ContentLoading event on the CoreWebView2.</span></span> <span data-ttu-id="a1b92-154">Более подробную информацию вы увидите в документации CoreWebView2. ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="a1b92-154">See CoreWebView2.ContentLoading documentation for more information.</span></span>

#### <span data-ttu-id="a1b92-155">CoreWebView2Ready</span><span class="sxs-lookup"><span data-stu-id="a1b92-155">CoreWebView2Ready</span></span> 

<span data-ttu-id="a1b92-156">Это событие запускается, когда [CoreWebView2](#corewebview2) элемента управления завершает инициализацию (независимо от того, как был инициирована инициализация), но до того, как он будет использоваться для чего-либо.</span><span class="sxs-lookup"><span data-stu-id="a1b92-156">This event is triggered when the control's [CoreWebView2](#corewebview2) has finished being initialized (regardless of how initialization was triggered) but before it is used for anything.</span></span>

> <span data-ttu-id="a1b92-157">событие EventHandler< EventArgs > [CoreWebView2Ready](#corewebview2ready)</span><span class="sxs-lookup"><span data-stu-id="a1b92-157">public event EventHandler< EventArgs > [CoreWebView2Ready](#corewebview2ready)</span></span>

<span data-ttu-id="a1b92-158">Вы должны обработать это событие, если вам необходимо выполнить одну операцию настройки в CoreWebView2, которая будет применяться ко всем их использованию (например, добавлять обработчики событий, настраивать параметры, устанавливать сценарии создания документов, добавлять объекты узла).</span><span class="sxs-lookup"><span data-stu-id="a1b92-158">You should handle this event if you need to perform one time setup operations on the CoreWebView2 which you want to affect all of its usages (e.g. adding event handlers, configuring settings, installing document creation scripts, adding host objects).</span></span>

<span data-ttu-id="a1b92-159">Это событие не предоставляет никаких аргументов, а отправитель — элемент управления WebView2, чье свойство CoreWebView2 теперь будет действительно допустимым (то есть не NULL) в первый раз.</span><span class="sxs-lookup"><span data-stu-id="a1b92-159">This event doesn't provide any arguments, and the sender will be the WebView2 control, whose CoreWebView2 property will now be valid (i.e. non-null) for the first time.</span></span>

#### <span data-ttu-id="a1b92-160">NavigationCompleted</span><span class="sxs-lookup"><span data-stu-id="a1b92-160">NavigationCompleted</span></span> 

<span data-ttu-id="a1b92-161">NavigationCompleted отправляется после того, как переход по документу верхнего уровня завершает обработку успешно или нет.</span><span class="sxs-lookup"><span data-stu-id="a1b92-161">NavigationCompleted dispatches after a navigate of the top level document completes rendering either successfully or not.</span></span>

> <span data-ttu-id="a1b92-162">событие EventHandler< CoreWebView2NavigationCompletedEventArgs > [NavigationCompleted](#navigationcompleted)</span><span class="sxs-lookup"><span data-stu-id="a1b92-162">public event EventHandler< CoreWebView2NavigationCompletedEventArgs > [NavigationCompleted](#navigationcompleted)</span></span>

<span data-ttu-id="a1b92-163">Это эквивалентно событию NavigationCompleted в CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="a1b92-163">This is equivalent to the NavigationCompleted event on the CoreWebView2.</span></span> <span data-ttu-id="a1b92-164">Более подробную информацию вы увидите в документации CoreWebView2. NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="a1b92-164">See CoreWebView2.NavigationCompleted documentation for more information.</span></span>

#### <span data-ttu-id="a1b92-165">NavigationStarting</span><span class="sxs-lookup"><span data-stu-id="a1b92-165">NavigationStarting</span></span> 

<span data-ttu-id="a1b92-166">NavigationStarting отправляется перед началом новой навигации для документа верхнего уровня в WebView2.</span><span class="sxs-lookup"><span data-stu-id="a1b92-166">NavigationStarting dispatches before a new navigate starts for the top level document of the WebView2.</span></span>

> <span data-ttu-id="a1b92-167">событие EventHandler< CoreWebView2NavigationStartingEventArgs > [NavigationStarting](#navigationstarting)</span><span class="sxs-lookup"><span data-stu-id="a1b92-167">public event EventHandler< CoreWebView2NavigationStartingEventArgs > [NavigationStarting](#navigationstarting)</span></span>

<span data-ttu-id="a1b92-168">Это эквивалентно событию NavigationStarting в CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="a1b92-168">This is equivalent to the NavigationStarting event on the CoreWebView2.</span></span> <span data-ttu-id="a1b92-169">Более подробную информацию вы увидите в документации CoreWebView2. NavigationStarting.</span><span class="sxs-lookup"><span data-stu-id="a1b92-169">See CoreWebView2.NavigationStarting documentation for more information.</span></span>

#### <span data-ttu-id="a1b92-170">SourceChanged</span><span class="sxs-lookup"><span data-stu-id="a1b92-170">SourceChanged</span></span> 

<span data-ttu-id="a1b92-171">SourceChanged отправляется после изменения исходного свойства.</span><span class="sxs-lookup"><span data-stu-id="a1b92-171">SourceChanged dispatches after the Source property changes.</span></span>

> <span data-ttu-id="a1b92-172">событие EventHandler< CoreWebView2SourceChangedEventArgs > [SourceChanged](#sourcechanged)</span><span class="sxs-lookup"><span data-stu-id="a1b92-172">public event EventHandler< CoreWebView2SourceChangedEventArgs > [SourceChanged](#sourcechanged)</span></span>

<span data-ttu-id="a1b92-173">Это может происходить во время навигации или в случае, если сценарий на странице изменяет URI документа.</span><span class="sxs-lookup"><span data-stu-id="a1b92-173">This may happen during a navigation or if otherwise the script in the page changes the URI of the document.</span></span> <span data-ttu-id="a1b92-174">Это эквивалентно событию SourceChanged в CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="a1b92-174">This is equivalent to the SourceChanged event on the CoreWebView2.</span></span> <span data-ttu-id="a1b92-175">Более подробную информацию вы увидите в документации CoreWebView2. SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="a1b92-175">See CoreWebView2.SourceChanged documentation for more information.</span></span>

#### <span data-ttu-id="a1b92-176">WebMessageReceived</span><span class="sxs-lookup"><span data-stu-id="a1b92-176">WebMessageReceived</span></span> 

<span data-ttu-id="a1b92-177">WebMessageReceived отправляет сообщение на узел приложения с помощью отправки по сети `chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="a1b92-177">WebMessageReceived dispatches after web content sends a message to the app host via `chrome.webview.postMessage`.</span></span>

> <span data-ttu-id="a1b92-178">событие EventHandler< CoreWebView2WebMessageReceivedEventArgs > [WebMessageReceived](#webmessagereceived)</span><span class="sxs-lookup"><span data-stu-id="a1b92-178">public event EventHandler< CoreWebView2WebMessageReceivedEventArgs > [WebMessageReceived](#webmessagereceived)</span></span>

<span data-ttu-id="a1b92-179">Это эквивалентно событию WebMessageReceived в CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="a1b92-179">This is equivalent to the WebMessageReceived event on the CoreWebView2.</span></span> <span data-ttu-id="a1b92-180">Более подробную информацию вы увидите в документации CoreWebView2. WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="a1b92-180">See CoreWebView2.WebMessageReceived documentation for more information.</span></span>

#### <span data-ttu-id="a1b92-181">CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="a1b92-181">CoreWebView2</span></span> 

<span data-ttu-id="a1b92-182">Основной CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="a1b92-182">The underlying CoreWebView2.</span></span>

> <span data-ttu-id="a1b92-183">общедоступная CoreWebView2 [CoreWebView2](#corewebview2)</span><span class="sxs-lookup"><span data-stu-id="a1b92-183">public CoreWebView2 [CoreWebView2](#corewebview2)</span></span>

<span data-ttu-id="a1b92-184">Это свойство используется для выполнения дополнительных операций с содержимым WebView2, чем представлено в WebView2.</span><span class="sxs-lookup"><span data-stu-id="a1b92-184">Use this property to perform more operations on the WebView2 content than is exposed on the WebView2.</span></span> <span data-ttu-id="a1b92-185">Это значение равно null, пока оно не будет инициализировано.</span><span class="sxs-lookup"><span data-stu-id="a1b92-185">This value is null until it is initialized.</span></span> <span data-ttu-id="a1b92-186">Вы можете принудительно инициализировать базовый CoreWebView2 с помощью метода InitializeAsync.</span><span class="sxs-lookup"><span data-stu-id="a1b92-186">You can force the underlying CoreWebView2 to initialize via the InitializeAsync method.</span></span>

#### <span data-ttu-id="a1b92-187">Источник</span><span class="sxs-lookup"><span data-stu-id="a1b92-187">Source</span></span> 

<span data-ttu-id="a1b92-188">Свойство Source — это URI документа верхнего уровня в WebView2.</span><span class="sxs-lookup"><span data-stu-id="a1b92-188">The Source property is the URI of the top level document of the WebView2.</span></span>

> <span data-ttu-id="a1b92-189">общедоступный [источник](#source) URI</span><span class="sxs-lookup"><span data-stu-id="a1b92-189">public Uri [Source](#source)</span></span>

<span data-ttu-id="a1b92-190">Установка источника эквивалентна вызову CoreWebView2. Navigate.</span><span class="sxs-lookup"><span data-stu-id="a1b92-190">Setting the Source is equivalent to calling CoreWebView2.Navigate.</span></span> <span data-ttu-id="a1b92-191">Если базовый CoreWebView2 еще не инициализирован, это свойство имеет значение about: blank.</span><span class="sxs-lookup"><span data-stu-id="a1b92-191">If the underlying CoreWebView2 is not yet initialized, this property is "about:blank".</span></span> <span data-ttu-id="a1b92-192">Если для свойства задан неабсолютный URI или пустое значение, свойство остается неизменным.</span><span class="sxs-lookup"><span data-stu-id="a1b92-192">If the property is set to a non-absolute URI or null, the property remains unchanged.</span></span> <span data-ttu-id="a1b92-193">Дополнительные сведения вы видите в CoreWebView2. навигации по документации.</span><span class="sxs-lookup"><span data-stu-id="a1b92-193">See CoreWebView2.Navigate documentation for more information.</span></span>

#### <span data-ttu-id="a1b92-194">ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="a1b92-194">ZoomFactor</span></span> 

<span data-ttu-id="a1b92-195">Коэффициент масштабирования для WebView.</span><span class="sxs-lookup"><span data-stu-id="a1b92-195">The zoom factor for the WebView.</span></span>

> <span data-ttu-id="a1b92-196">общедоступная двойная [ZoomFactor](#zoomfactor)</span><span class="sxs-lookup"><span data-stu-id="a1b92-196">public double [ZoomFactor](#zoomfactor)</span></span>

#### <span data-ttu-id="a1b92-197">CanGoBack</span><span class="sxs-lookup"><span data-stu-id="a1b92-197">CanGoBack</span></span> 

<span data-ttu-id="a1b92-198">Возвращает значение истина, если WebView может перейти на предыдущую страницу в истории навигации с помощью метода GoBack.</span><span class="sxs-lookup"><span data-stu-id="a1b92-198">Returns true if the webview can navigate to a previous page in the navigation history via the GoBack method.</span></span>

> <span data-ttu-id="a1b92-199">Открытый логический [CanGoBack](#cangoback)</span><span class="sxs-lookup"><span data-stu-id="a1b92-199">public bool [CanGoBack](#cangoback)</span></span>

<span data-ttu-id="a1b92-200">Это эквивалентно свойству CanGoBack в CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="a1b92-200">This is equivalent to the CanGoBack property on the CoreWebView2.</span></span> <span data-ttu-id="a1b92-201">Если базовый CoreWebView2 еще не инициализирован, это свойство имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="a1b92-201">If the underlying CoreWebView2 is not yet initialized, this property is false.</span></span> <span data-ttu-id="a1b92-202">Более подробную информацию вы увидите в документации CoreWebView2. CanGoBack.</span><span class="sxs-lookup"><span data-stu-id="a1b92-202">See CoreWebView2.CanGoBack documentation for more information.</span></span>

#### <span data-ttu-id="a1b92-203">CanGoForward</span><span class="sxs-lookup"><span data-stu-id="a1b92-203">CanGoForward</span></span> 

<span data-ttu-id="a1b92-204">Возвращает значение "истина", если WebView может перейти к следующей странице в журнале переходов с помощью метода GoForward.</span><span class="sxs-lookup"><span data-stu-id="a1b92-204">Returns true if the webview can navigate to a next page in the navigation history via the GoForward method.</span></span>

> <span data-ttu-id="a1b92-205">Открытый логический [CanGoForward](#cangoforward)</span><span class="sxs-lookup"><span data-stu-id="a1b92-205">public bool [CanGoForward](#cangoforward)</span></span>

<span data-ttu-id="a1b92-206">Это эквивалентно свойству CanGoForward в CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="a1b92-206">This is equivalent to the CanGoForward property on the CoreWebView2.</span></span> <span data-ttu-id="a1b92-207">Если базовый CoreWebView2 еще не инициализирован, это свойство имеет значение false.</span><span class="sxs-lookup"><span data-stu-id="a1b92-207">If the underlying CoreWebView2 is not yet initialized, this property is false.</span></span> <span data-ttu-id="a1b92-208">Более подробную информацию вы увидите в документации CoreWebView2. CanGoForward.</span><span class="sxs-lookup"><span data-stu-id="a1b92-208">See CoreWebView2.CanGoForward documentation for more information.</span></span>

#### <span data-ttu-id="a1b92-209">EnsureCoreWebView2Async</span><span class="sxs-lookup"><span data-stu-id="a1b92-209">EnsureCoreWebView2Async</span></span> 

<span data-ttu-id="a1b92-210">Явным образом инициализируйте инициализацию [CoreWebView2](#corewebview2)элемента управления.</span><span class="sxs-lookup"><span data-stu-id="a1b92-210">Explicitly trigger initialization of the control's [CoreWebView2](#corewebview2).</span></span>

> <span data-ttu-id="a1b92-211">общедоступная задача [EnsureCoreWebView2Async](#ensurecorewebview2async)(среда CoreWebView2Environment)</span><span class="sxs-lookup"><span data-stu-id="a1b92-211">public Task [EnsureCoreWebView2Async](#ensurecorewebview2async)(CoreWebView2Environment environment)</span></span>

##### <span data-ttu-id="a1b92-212">Параметры</span><span class="sxs-lookup"><span data-stu-id="a1b92-212">Parameters</span></span>
* `environment` <span data-ttu-id="a1b92-213">Предварительно созданный CoreWebView2Environment, который должен использоваться для создания CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="a1b92-213">A pre-created CoreWebView2Environment that should be used to create the CoreWebView2.</span></span> <span data-ttu-id="a1b92-214">Создание собственной среды позволяет управлять несколькими параметрами, которые влияют на то, как CoreWebView2 инициализируется.</span><span class="sxs-lookup"><span data-stu-id="a1b92-214">Creating your own environment gives you control over several options that affect how the CoreWebView2 is initialized.</span></span> <span data-ttu-id="a1b92-215">Если вы передаете null (значение по умолчанию), среда по умолчанию будет создана и использоваться автоматически.</span><span class="sxs-lookup"><span data-stu-id="a1b92-215">If you pass null (the default value) then a default environment will be created and used automatically.</span></span> 

##### <span data-ttu-id="a1b92-216">Дает</span><span class="sxs-lookup"><span data-stu-id="a1b92-216">Returns</span></span>
<span data-ttu-id="a1b92-217">Задача, представляющая собой процесс инициализации фона.</span><span class="sxs-lookup"><span data-stu-id="a1b92-217">A Task that represents the background initialization process.</span></span> <span data-ttu-id="a1b92-218">После завершения задачи свойство CoreWebView2 будет доступно для использования (то есть без значения NULL).</span><span class="sxs-lookup"><span data-stu-id="a1b92-218">When the task completes then the CoreWebView2 property will be available for use (i.e. non-null).</span></span> <span data-ttu-id="a1b92-219">Обратите внимание, что событие [CoreWebView2Ready](#corewebview2ready) элемента управления будет вызвано до завершения задачи.</span><span class="sxs-lookup"><span data-stu-id="a1b92-219">Note that the control's [CoreWebView2Ready](#corewebview2ready) event will be invoked before the task completes.</span></span> 

<span data-ttu-id="a1b92-220">Повторный вызов этого метода не повлияет (любая указанная среда игнорируется) и возвращает ту же задачу, что и первый вызов.</span><span class="sxs-lookup"><span data-stu-id="a1b92-220">Calling this method additional times will have no effect (any specified environment is ignored) and return the same Task as the first call.</span></span> <span data-ttu-id="a1b92-221">Вызов этого метода после того, как инициализация вызывается явным образом посредством задания свойства [Source](#source) , не будет оказывать никакого воздействия (любая указанная среда игнорируется) и просто возвращать задачу, представляющую уже выполняющуюся инициализацию.</span><span class="sxs-lookup"><span data-stu-id="a1b92-221">Calling this method after initialization has been implicitly triggered by setting the [Source](#source) property will have no effect (any specified environment is ignored) and simply return a Task representing that initialization already in progress.</span></span> 

##### <span data-ttu-id="a1b92-222">Исключения</span><span class="sxs-lookup"><span data-stu-id="a1b92-222">Exceptions</span></span>
* `System.InvalidOperationException` <span data-ttu-id="a1b92-223">Вызывается при вызове из потока, не относящегося к пользовательскому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="a1b92-223">Thrown when invoked from non-UI thread.</span></span>

#### <span data-ttu-id="a1b92-224">ExecuteScriptAsync</span><span class="sxs-lookup"><span data-stu-id="a1b92-224">ExecuteScriptAsync</span></span> 

<span data-ttu-id="a1b92-225">Выполняет представленный сценарий в документе верхнего уровня элемента WebView2.</span><span class="sxs-lookup"><span data-stu-id="a1b92-225">Executes the provided script in the top level document of the WebView2.</span></span>

> <span data-ttu-id="a1b92-226">общедоступная асинхронная задача< String > [ExecuteScriptAsync](#executescriptasync)(строковый сценарий)</span><span class="sxs-lookup"><span data-stu-id="a1b92-226">public async Task< string > [ExecuteScriptAsync](#executescriptasync)(string script)</span></span>

<span data-ttu-id="a1b92-227">Это эквивалентно методу ExecuteScriptAsync в CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="a1b92-227">This is equivalent to the ExecuteScriptAsync method on the CoreWebView2.</span></span> <span data-ttu-id="a1b92-228">Если базовый CoreWebView2 еще не инициализирован, этот метод создает исключение InvalidOperationException.</span><span class="sxs-lookup"><span data-stu-id="a1b92-228">If the underlying CoreWebView2 is not yet initialized, this method throws an InvalidOperationException.</span></span> <span data-ttu-id="a1b92-229">Более подробную информацию вы увидите в документации CoreWebView2. ExecuteScriptAsync.</span><span class="sxs-lookup"><span data-stu-id="a1b92-229">See CoreWebView2.ExecuteScriptAsync documentation for more information.</span></span>

#### <span data-ttu-id="a1b92-230">GoBack</span><span class="sxs-lookup"><span data-stu-id="a1b92-230">GoBack</span></span> 

<span data-ttu-id="a1b92-231">Переход на предыдущую страницу в истории навигации.</span><span class="sxs-lookup"><span data-stu-id="a1b92-231">Navigate to the previous page in navigation history.</span></span>

> <span data-ttu-id="a1b92-232">общедоступная void [GoBack](#goback)()</span><span class="sxs-lookup"><span data-stu-id="a1b92-232">public void [GoBack](#goback)()</span></span>

<span data-ttu-id="a1b92-233">Это эквивалентно методу GoBack для CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="a1b92-233">This is equivalent to the GoBack method on the CoreWebView2.</span></span> <span data-ttu-id="a1b92-234">Если базовый CoreWebView2 еще не инициализирован, этот метод не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="a1b92-234">If the underlying CoreWebView2 is not yet initialized, this method does nothing.</span></span> <span data-ttu-id="a1b92-235">Более подробную информацию вы увидите в документации по CoreWebView2. GoBack.</span><span class="sxs-lookup"><span data-stu-id="a1b92-235">See CoreWebView2.GoBack documentation for more information.</span></span>

#### <span data-ttu-id="a1b92-236">GoForward</span><span class="sxs-lookup"><span data-stu-id="a1b92-236">GoForward</span></span> 

<span data-ttu-id="a1b92-237">Переход к следующей странице в журнале переходов.</span><span class="sxs-lookup"><span data-stu-id="a1b92-237">Navigate to the next page in navigation history.</span></span>

> <span data-ttu-id="a1b92-238">общедоступная void [GoForward](#goforward)()</span><span class="sxs-lookup"><span data-stu-id="a1b92-238">public void [GoForward](#goforward)()</span></span>

<span data-ttu-id="a1b92-239">Это эквивалентно методу GoForward в CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="a1b92-239">This is equivalent to the GoForward method on the CoreWebView2.</span></span> <span data-ttu-id="a1b92-240">Если базовый CoreWebView2 еще не инициализирован, этот метод не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="a1b92-240">If the underlying CoreWebView2 is not yet initialized, this method does nothing.</span></span> <span data-ttu-id="a1b92-241">Более подробную информацию вы увидите в документации CoreWebView2. GoForward.</span><span class="sxs-lookup"><span data-stu-id="a1b92-241">See CoreWebView2.GoForward documentation for more information.</span></span>

#### <span data-ttu-id="a1b92-242">NavigateToString</span><span class="sxs-lookup"><span data-stu-id="a1b92-242">NavigateToString</span></span> 

<span data-ttu-id="a1b92-243">Обрабатывают представленный HTML-код как документ верхнего уровня для элемента WebView2.</span><span class="sxs-lookup"><span data-stu-id="a1b92-243">Render the provided HTML as the top level document of the WebView2.</span></span>

> <span data-ttu-id="a1b92-244">Public void [NavigateToString](#navigatetostring)(строка htmlContent)</span><span class="sxs-lookup"><span data-stu-id="a1b92-244">public void [NavigateToString](#navigatetostring)(string htmlContent)</span></span>

<span data-ttu-id="a1b92-245">Это эквивалентно методу NavigateToString в CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="a1b92-245">This is equivalent to the NavigateToString method on the CoreWebView2.</span></span> <span data-ttu-id="a1b92-246">Если базовый CoreWebView2 еще не инициализирован, этот метод создает исключение InvalidOperationException.</span><span class="sxs-lookup"><span data-stu-id="a1b92-246">If the underlying CoreWebView2 is not yet initialized, this method throws an InvalidOperationException.</span></span> <span data-ttu-id="a1b92-247">Более подробную информацию вы увидите в документации CoreWebView2. NavigateToString.</span><span class="sxs-lookup"><span data-stu-id="a1b92-247">See CoreWebView2.NavigateToString documentation for more information.</span></span>

#### <span data-ttu-id="a1b92-248">Перезагрузить</span><span class="sxs-lookup"><span data-stu-id="a1b92-248">Reload</span></span> 

<span data-ttu-id="a1b92-249">Перезагрузите документ верхнего уровня в WebView2.</span><span class="sxs-lookup"><span data-stu-id="a1b92-249">Reload the top level document of the WebView2.</span></span>

> <span data-ttu-id="a1b92-250">общедоступный void [Reload](#reload)()</span><span class="sxs-lookup"><span data-stu-id="a1b92-250">public void [Reload](#reload)()</span></span>

<span data-ttu-id="a1b92-251">Это эквивалентно методу Reload для CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="a1b92-251">This is equivalent to the Reload method on the CoreWebView2.</span></span> <span data-ttu-id="a1b92-252">Если базовый CoreWebView2 еще не инициализирован, этот метод создает исключение InvalidOperationException.</span><span class="sxs-lookup"><span data-stu-id="a1b92-252">If the underlying CoreWebView2 is not yet initialized, this method throws an InvalidOperationException.</span></span> <span data-ttu-id="a1b92-253">Дополнительные сведения смотрите в разделе CoreWebView2. повторно загрузите документацию.</span><span class="sxs-lookup"><span data-stu-id="a1b92-253">See CoreWebView2.Reload documentation for more information.</span></span>

#### <span data-ttu-id="a1b92-254">Stop</span><span class="sxs-lookup"><span data-stu-id="a1b92-254">Stop</span></span> 

<span data-ttu-id="a1b92-255">Остановите ход выполнения навигации в WebView2.</span><span class="sxs-lookup"><span data-stu-id="a1b92-255">Stop any in progress navigation in the WebView2.</span></span>

> <span data-ttu-id="a1b92-256">открытая пустая [Отмена](#stop)()</span><span class="sxs-lookup"><span data-stu-id="a1b92-256">public void [Stop](#stop)()</span></span>

<span data-ttu-id="a1b92-257">Это эквивалентно методу Stop в CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="a1b92-257">This is equivalent to the Stop method on the CoreWebView2.</span></span> <span data-ttu-id="a1b92-258">Если базовый CoreWebView2 еще не инициализирован, этот метод не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="a1b92-258">If the underlying CoreWebView2 is not yet initialized, this method does nothing.</span></span> <span data-ttu-id="a1b92-259">Для получения дополнительных сведений ознакомьтесь со статьей CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="a1b92-259">See CoreWebView2.Stop documentation for more information.</span></span>

#### <span data-ttu-id="a1b92-260">WebView2</span><span class="sxs-lookup"><span data-stu-id="a1b92-260">WebView2</span></span> 

<span data-ttu-id="a1b92-261">Создайте новый элемент управления WebView2 WinForms.</span><span class="sxs-lookup"><span data-stu-id="a1b92-261">Create a new WebView2 WinForms control.</span></span>

> <span data-ttu-id="a1b92-262">общедоступная [WebView2](#webview2)()</span><span class="sxs-lookup"><span data-stu-id="a1b92-262">public [WebView2](#webview2)()</span></span>

<span data-ttu-id="a1b92-263">После создания свойство CoreWebView2 имеет значение null.</span><span class="sxs-lookup"><span data-stu-id="a1b92-263">After construction the CoreWebView2 property is null.</span></span> <span data-ttu-id="a1b92-264">Вызовите [EnsureCoreWebView2Async](#ensurecorewebview2async) , чтобы инициализировать базовый CoreWebView2.</span><span class="sxs-lookup"><span data-stu-id="a1b92-264">Call [EnsureCoreWebView2Async](#ensurecorewebview2async) to initialize the underlying CoreWebView2.</span></span>

