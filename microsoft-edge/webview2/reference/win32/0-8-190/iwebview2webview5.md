---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 3c32cd59e75eb81bf69661d01f6044a0628ba35d
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654613"
---
# <span data-ttu-id="58674-104">интерфейс IWebView2WebView5</span><span class="sxs-lookup"><span data-stu-id="58674-104">interface IWebView2WebView5</span></span> 

> [!NOTE]
> <span data-ttu-id="58674-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="58674-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="58674-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="58674-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebView5
  : public IWebView2WebView4
```

<span data-ttu-id="58674-107">Дополнительные функции, реализованные основным объектом WebView.</span><span class="sxs-lookup"><span data-stu-id="58674-107">Additional functionality implemented by the primary WebView object.</span></span>

## <span data-ttu-id="58674-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="58674-108">Summary</span></span>

 <span data-ttu-id="58674-109">Участников</span><span class="sxs-lookup"><span data-stu-id="58674-109">Members</span></span>                        | <span data-ttu-id="58674-110">Описания</span><span class="sxs-lookup"><span data-stu-id="58674-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="58674-111">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="58674-111">add_ContainsFullScreenElementChanged</span></span>](#add_containsfullscreenelementchanged) | <span data-ttu-id="58674-112">Уведомляет об изменении свойства ContainsFullScreenElement.</span><span class="sxs-lookup"><span data-stu-id="58674-112">Notifies when the ContainsFullScreenElement property changes.</span></span>
[<span data-ttu-id="58674-113">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="58674-113">remove_ContainsFullScreenElementChanged</span></span>](#remove_containsfullscreenelementchanged) | <span data-ttu-id="58674-114">Удалите обработчик событий, добавленный ранее с помощью соответствующего метода события add_.</span><span class="sxs-lookup"><span data-stu-id="58674-114">Remove an event handler previously added with the corresponding add_ event method.</span></span>
[<span data-ttu-id="58674-115">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="58674-115">get_ContainsFullScreenElement</span></span>](#get_containsfullscreenelement) | <span data-ttu-id="58674-116">Указывает, содержит ли WebView элемент HTML на весь экран.</span><span class="sxs-lookup"><span data-stu-id="58674-116">Indicates if the WebView contains a fullscreen HTML element.</span></span>
[<span data-ttu-id="58674-117">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="58674-117">add_WebResourceRequested</span></span>](#add_webresourcerequested) | <span data-ttu-id="58674-118">Добавьте обработчик событий для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="58674-118">Add an event handler for the WebResourceRequested event.</span></span>
[<span data-ttu-id="58674-119">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="58674-119">AddWebResourceRequestedFilter</span></span>](#addwebresourcerequestedfilter) | <span data-ttu-id="58674-120">Добавляет в событие WebResourceRequested код URI и фильтр контекста ресурсов.</span><span class="sxs-lookup"><span data-stu-id="58674-120">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>
[<span data-ttu-id="58674-121">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="58674-121">RemoveWebResourceRequestedFilter</span></span>](#removewebresourcerequestedfilter) | <span data-ttu-id="58674-122">Удаляет соответствующий фильтр веб-ресурсов, который ранее был добавлен для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="58674-122">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>

<span data-ttu-id="58674-123">Вы можете QueryInterface для этого интерфейса из объекта, реализующего [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="58674-123">You can QueryInterface for this interface from the object that implements [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="58674-124">Дополнительные сведения вы видите в интерфейсе [IWebView2WebView](IWebView2WebView.md) .</span><span class="sxs-lookup"><span data-stu-id="58674-124">See the [IWebView2WebView](IWebView2WebView.md) interface for more details.</span></span>

## <span data-ttu-id="58674-125">Участников</span><span class="sxs-lookup"><span data-stu-id="58674-125">Members</span></span>

#### <span data-ttu-id="58674-126">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="58674-126">add_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="58674-127">Уведомляет об изменении свойства ContainsFullScreenElement.</span><span class="sxs-lookup"><span data-stu-id="58674-127">Notifies when the ContainsFullScreenElement property changes.</span></span>

> <span data-ttu-id="58674-128">общедоступные значения HRESULT [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)([IWebView2ContainsFullScreenElementChangedEventHandler](IWebView2ContainsFullScreenElementChangedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="58674-128">public HRESULT [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)([IWebView2ContainsFullScreenElementChangedEventHandler](IWebView2ContainsFullScreenElementChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="58674-129">Это означает, что HTML-элемент, находящиеся внутри WebView, помещается на размер WebView или выходит за экран.</span><span class="sxs-lookup"><span data-stu-id="58674-129">This means that an HTML element inside the WebView is entering fullscreen to the size of the WebView or leaving fullscreen.</span></span> <span data-ttu-id="58674-130">Это событие полезно, если, например, элемент видео запрашивается на весь экран.</span><span class="sxs-lookup"><span data-stu-id="58674-130">This event is useful when, for example, a video element requests to go fullscreen.</span></span> <span data-ttu-id="58674-131">Прослушиватель ContainsFullScreenElementChanged может затем изменить размер WebView в ответе.</span><span class="sxs-lookup"><span data-stu-id="58674-131">The listener of ContainsFullScreenElementChanged can then resize the WebView in response.</span></span>

```cpp
    // Register a handler for the ContainsFullScreenChanged event.
    CHECK_FAILURE(m_webView->add_ContainsFullScreenElementChanged(
        Callback<IWebView2ContainsFullScreenElementChangedEventHandler>(
            [this](IWebView2WebView5* sender, IUnknown* args) -> HRESULT {
                if (m_fullScreenAllowed)
                {
                    CHECK_FAILURE(sender->get_ContainsFullScreenElement(&m_containsFullscreenElement));
                    if (m_containsFullscreenElement)
                    {
                        EnterFullScreen();
                    }
                    else
                    {
                        ExitFullScreen();
                    }
                }
                return S_OK;
            })
            .Get(),
        nullptr));
```

#### <span data-ttu-id="58674-132">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="58674-132">remove_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="58674-133">Удалите обработчик событий, добавленный ранее с помощью соответствующего метода события add_.</span><span class="sxs-lookup"><span data-stu-id="58674-133">Remove an event handler previously added with the corresponding add_ event method.</span></span>

> <span data-ttu-id="58674-134">общедоступные значения HRESULT [remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="58674-134">public HRESULT [remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="58674-135">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="58674-135">get_ContainsFullScreenElement</span></span> 

<span data-ttu-id="58674-136">Указывает, содержит ли WebView элемент HTML на весь экран.</span><span class="sxs-lookup"><span data-stu-id="58674-136">Indicates if the WebView contains a fullscreen HTML element.</span></span>

> <span data-ttu-id="58674-137">общедоступные значения HRESULT [get_ContainsFullScreenElement](#get_containsfullscreenelement)(bool \* ContainsFullScreenElement)</span><span class="sxs-lookup"><span data-stu-id="58674-137">public HRESULT [get_ContainsFullScreenElement](#get_containsfullscreenelement)(BOOL \* containsFullScreenElement)</span></span>

#### <span data-ttu-id="58674-138">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="58674-138">add_WebResourceRequested</span></span> 

<span data-ttu-id="58674-139">Добавьте обработчик событий для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="58674-139">Add an event handler for the WebResourceRequested event.</span></span>

> <span data-ttu-id="58674-140">общедоступные значения HRESULT [add_WebResourceRequested](#add_webresourcerequested)([IWebView2WebResourceRequestedEventHandler](IWebView2WebResourceRequestedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="58674-140">public HRESULT [add_WebResourceRequested](#add_webresourcerequested)([IWebView2WebResourceRequestedEventHandler](IWebView2WebResourceRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="58674-141">Активируется, когда WebView выполняет запрос HTTP к соответствующему URL-адресу и фильтру контекста ресурсов, добавленному с помощью AddWebResourceRequestedFilter.</span><span class="sxs-lookup"><span data-stu-id="58674-141">Fires when the WebView is performing an HTTP request to a matching URL and resource context filter that was added with AddWebResourceRequestedFilter.</span></span> <span data-ttu-id="58674-142">Для срабатывания события необходимо добавить хотя бы один фильтр.</span><span class="sxs-lookup"><span data-stu-id="58674-142">At least one filter must be added for the event to fire.</span></span>

```cpp
        if (m_blockImages)
        {
            m_webView->AddWebResourceRequestedFilter(L"*", WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE);
            CHECK_FAILURE(m_webView->add_WebResourceRequested(
                Callback<IWebView2WebResourceRequestedEventHandler>(
                    [this](
                        IWebView2WebView* sender,
                        IWebView2WebResourceRequestedEventArgs* args) {
                        wil::com_ptr<IWebView2WebResourceRequestedEventArgs2>
                            webResourceEventArgs2;
                        args->QueryInterface(IID_PPV_ARGS(&webResourceEventArgs2));
                        WEBVIEW2_WEB_RESOURCE_CONTEXT resourceContext;
                        CHECK_FAILURE(
                            webResourceEventArgs2->get_ResourceContext(&resourceContext));
                        // Ensure that the type is image
                        if (resourceContext != WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE)
                        {
                            return E_INVALIDARG;
                        }
                        // Override the response with an empty one to block the image.
                        // If put_Response is not called, the request will continue as normal.
                        wil::com_ptr<IWebView2WebResourceResponse> response;
                        CHECK_FAILURE(m_webViewEnvironment->CreateWebResourceResponse(
                            nullptr, 403 /*NoContent*/, L"Blocked", L"", &response));
                        CHECK_FAILURE(args->put_Response(response.get()));
                        return S_OK;
                    })
                    .Get(),
                &m_webResourceRequestedTokenForImageBlocking));
        }
        else
        {
            CHECK_FAILURE(m_webView->remove_WebResourceRequested(
                m_webResourceRequestedTokenForImageBlocking));
        }
```

#### <span data-ttu-id="58674-143">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="58674-143">AddWebResourceRequestedFilter</span></span> 

<span data-ttu-id="58674-144">Добавляет в событие WebResourceRequested код URI и фильтр контекста ресурсов.</span><span class="sxs-lookup"><span data-stu-id="58674-144">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>

> <span data-ttu-id="58674-145">общедоступный HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(LPCWSTR const uri,[WEBVIEW2_WEB_RESOURCE_CONTEXT](IWebView2WebView.md#webview2_web_resource_context) const разделе ResourceContext)</span><span class="sxs-lookup"><span data-stu-id="58674-145">public HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(LPCWSTR const uri,[WEBVIEW2_WEB_RESOURCE_CONTEXT](IWebView2WebView.md#webview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="58674-146">Параметр URI может быть строкой с подстановочными знаками ("": ноль или больше; "?": только один).</span><span class="sxs-lookup"><span data-stu-id="58674-146">URI parameter can be a wildcard string ('': zero or more, '?': exactly one).</span></span> <span data-ttu-id="58674-147">nullptr эквивалентен L "".</span><span class="sxs-lookup"><span data-stu-id="58674-147">nullptr is equivalent to L"".</span></span> <span data-ttu-id="58674-148">Описание фильтров контекста ресурсов приведено в разделе WEBVIEW2_WEB_RESOURCE_CONTEXT перечисление.</span><span class="sxs-lookup"><span data-stu-id="58674-148">See WEBVIEW2_WEB_RESOURCE_CONTEXT enum for description of resource context filters.</span></span>

#### <span data-ttu-id="58674-149">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="58674-149">RemoveWebResourceRequestedFilter</span></span> 

<span data-ttu-id="58674-150">Удаляет соответствующий фильтр веб-ресурсов, который ранее был добавлен для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="58674-150">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>

> <span data-ttu-id="58674-151">общедоступный HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(LPCWSTR const uri,[WEBVIEW2_WEB_RESOURCE_CONTEXT](IWebView2WebView.md#webview2_web_resource_context) const разделе ResourceContext)</span><span class="sxs-lookup"><span data-stu-id="58674-151">public HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(LPCWSTR const uri,[WEBVIEW2_WEB_RESOURCE_CONTEXT](IWebView2WebView.md#webview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="58674-152">Если один и тот же фильтр был добавлен несколько значений, его необходимо будет удалить столько, сколько вхождений было добавлено для эффективного.</span><span class="sxs-lookup"><span data-stu-id="58674-152">If the same filter was added multiple times, then it will need to be removed as many times as it was added for the removal to be effective.</span></span> <span data-ttu-id="58674-153">Возвращает E_INVALIDARG для фильтра, который еще не был добавлен.</span><span class="sxs-lookup"><span data-stu-id="58674-153">Returns E_INVALIDARG for a filter that was never added.</span></span>

