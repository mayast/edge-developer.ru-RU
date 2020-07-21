---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2WebView5
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: bc48c5d495c2182ba39b867fdb46ce7af503f5ba
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884689"
---
# <span data-ttu-id="07743-104">0.8.355-Interface IWebView2WebView5</span><span class="sxs-lookup"><span data-stu-id="07743-104">0.8.355 - interface IWebView2WebView5</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebView5
  : public IWebView2WebView4
```

<span data-ttu-id="07743-105">Дополнительные функции, реализованные основным объектом WebView.</span><span class="sxs-lookup"><span data-stu-id="07743-105">Additional functionality implemented by the primary WebView object.</span></span>

## <span data-ttu-id="07743-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="07743-106">Summary</span></span>

 <span data-ttu-id="07743-107">Участников</span><span class="sxs-lookup"><span data-stu-id="07743-107">Members</span></span>                        | <span data-ttu-id="07743-108">Описания</span><span class="sxs-lookup"><span data-stu-id="07743-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="07743-109">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="07743-109">add_ContainsFullScreenElementChanged</span></span>](#add_containsfullscreenelementchanged) | <span data-ttu-id="07743-110">Уведомляет об изменении свойства ContainsFullScreenElement.</span><span class="sxs-lookup"><span data-stu-id="07743-110">Notifies when the ContainsFullScreenElement property changes.</span></span>
[<span data-ttu-id="07743-111">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="07743-111">remove_ContainsFullScreenElementChanged</span></span>](#remove_containsfullscreenelementchanged) | <span data-ttu-id="07743-112">Удалите обработчик событий, добавленный ранее с помощью соответствующего метода события add_.</span><span class="sxs-lookup"><span data-stu-id="07743-112">Remove an event handler previously added with the corresponding add_ event method.</span></span>
[<span data-ttu-id="07743-113">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="07743-113">get_ContainsFullScreenElement</span></span>](#get_containsfullscreenelement) | <span data-ttu-id="07743-114">Указывает, содержит ли WebView элемент HTML на весь экран.</span><span class="sxs-lookup"><span data-stu-id="07743-114">Indicates if the WebView contains a fullscreen HTML element.</span></span>
[<span data-ttu-id="07743-115">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="07743-115">add_WebResourceRequested</span></span>](#add_webresourcerequested) | <span data-ttu-id="07743-116">Добавьте обработчик событий для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="07743-116">Add an event handler for the WebResourceRequested event.</span></span>
[<span data-ttu-id="07743-117">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="07743-117">AddWebResourceRequestedFilter</span></span>](#addwebresourcerequestedfilter) | <span data-ttu-id="07743-118">Добавляет в событие WebResourceRequested код URI и фильтр контекста ресурсов.</span><span class="sxs-lookup"><span data-stu-id="07743-118">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>
[<span data-ttu-id="07743-119">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="07743-119">RemoveWebResourceRequestedFilter</span></span>](#removewebresourcerequestedfilter) | <span data-ttu-id="07743-120">Удаляет соответствующий фильтр веб-ресурсов, который ранее был добавлен для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="07743-120">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>

<span data-ttu-id="07743-121">Вы можете QueryInterface для этого интерфейса из объекта, реализующего [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="07743-121">You can QueryInterface for this interface from the object that implements [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="07743-122">Дополнительные сведения вы видите в интерфейсе [IWebView2WebView](IWebView2WebView.md) .</span><span class="sxs-lookup"><span data-stu-id="07743-122">See the [IWebView2WebView](IWebView2WebView.md) interface for more details.</span></span>

## <span data-ttu-id="07743-123">Участников</span><span class="sxs-lookup"><span data-stu-id="07743-123">Members</span></span>

#### <span data-ttu-id="07743-124">add_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="07743-124">add_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="07743-125">Уведомляет об изменении свойства ContainsFullScreenElement.</span><span class="sxs-lookup"><span data-stu-id="07743-125">Notifies when the ContainsFullScreenElement property changes.</span></span>

> <span data-ttu-id="07743-126">общедоступные значения HRESULT [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)([IWebView2ContainsFullScreenElementChangedEventHandler](IWebView2ContainsFullScreenElementChangedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="07743-126">public HRESULT [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)([IWebView2ContainsFullScreenElementChangedEventHandler](IWebView2ContainsFullScreenElementChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="07743-127">Это означает, что HTML-элемент, находящиеся внутри WebView, помещается на размер WebView или выходит за экран.</span><span class="sxs-lookup"><span data-stu-id="07743-127">This means that an HTML element inside the WebView is entering fullscreen to the size of the WebView or leaving fullscreen.</span></span> <span data-ttu-id="07743-128">Это событие полезно, если, например, элемент видео запрашивается на весь экран.</span><span class="sxs-lookup"><span data-stu-id="07743-128">This event is useful when, for example, a video element requests to go fullscreen.</span></span> <span data-ttu-id="07743-129">Прослушиватель ContainsFullScreenElementChanged может затем изменить размер WebView в ответе.</span><span class="sxs-lookup"><span data-stu-id="07743-129">The listener of ContainsFullScreenElementChanged can then resize the WebView in response.</span></span>

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

#### <span data-ttu-id="07743-130">remove_ContainsFullScreenElementChanged</span><span class="sxs-lookup"><span data-stu-id="07743-130">remove_ContainsFullScreenElementChanged</span></span> 

<span data-ttu-id="07743-131">Удалите обработчик событий, добавленный ранее с помощью соответствующего метода события add_.</span><span class="sxs-lookup"><span data-stu-id="07743-131">Remove an event handler previously added with the corresponding add_ event method.</span></span>

> <span data-ttu-id="07743-132">общедоступные значения HRESULT [remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="07743-132">public HRESULT [remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="07743-133">get_ContainsFullScreenElement</span><span class="sxs-lookup"><span data-stu-id="07743-133">get_ContainsFullScreenElement</span></span> 

<span data-ttu-id="07743-134">Указывает, содержит ли WebView элемент HTML на весь экран.</span><span class="sxs-lookup"><span data-stu-id="07743-134">Indicates if the WebView contains a fullscreen HTML element.</span></span>

> <span data-ttu-id="07743-135">общедоступные значения HRESULT [get_ContainsFullScreenElement](#get_containsfullscreenelement)(bool \* ContainsFullScreenElement)</span><span class="sxs-lookup"><span data-stu-id="07743-135">public HRESULT [get_ContainsFullScreenElement](#get_containsfullscreenelement)(BOOL \* containsFullScreenElement)</span></span>

#### <span data-ttu-id="07743-136">add_WebResourceRequested</span><span class="sxs-lookup"><span data-stu-id="07743-136">add_WebResourceRequested</span></span> 

<span data-ttu-id="07743-137">Добавьте обработчик событий для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="07743-137">Add an event handler for the WebResourceRequested event.</span></span>

> <span data-ttu-id="07743-138">общедоступные значения HRESULT [add_WebResourceRequested](#add_webresourcerequested)([IWebView2WebResourceRequestedEventHandler](IWebView2WebResourceRequestedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="07743-138">public HRESULT [add_WebResourceRequested](#add_webresourcerequested)([IWebView2WebResourceRequestedEventHandler](IWebView2WebResourceRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="07743-139">Активируется, когда WebView выполняет запрос HTTP к соответствующему URL-адресу и фильтру контекста ресурсов, добавленному с помощью AddWebResourceRequestedFilter.</span><span class="sxs-lookup"><span data-stu-id="07743-139">Fires when the WebView is performing an HTTP request to a matching URL and resource context filter that was added with AddWebResourceRequestedFilter.</span></span> <span data-ttu-id="07743-140">Для срабатывания события необходимо добавить хотя бы один фильтр.</span><span class="sxs-lookup"><span data-stu-id="07743-140">At least one filter must be added for the event to fire.</span></span>

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

#### <span data-ttu-id="07743-141">AddWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="07743-141">AddWebResourceRequestedFilter</span></span> 

<span data-ttu-id="07743-142">Добавляет в событие WebResourceRequested код URI и фильтр контекста ресурсов.</span><span class="sxs-lookup"><span data-stu-id="07743-142">Adds a URI and resource context filter to the WebResourceRequested event.</span></span>

> <span data-ttu-id="07743-143">общедоступный HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(LPCWSTR const uri,[WEBVIEW2_WEB_RESOURCE_CONTEXT](IWebView2WebView.md#webview2_web_resource_context) const разделе ResourceContext)</span><span class="sxs-lookup"><span data-stu-id="07743-143">public HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(LPCWSTR const uri,[WEBVIEW2_WEB_RESOURCE_CONTEXT](IWebView2WebView.md#webview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="07743-144">Параметр URI может быть строкой с подстановочными знаками ("": ноль или больше; "?": только один).</span><span class="sxs-lookup"><span data-stu-id="07743-144">URI parameter can be a wildcard string ('': zero or more, '?': exactly one).</span></span> <span data-ttu-id="07743-145">nullptr эквивалентен L "".</span><span class="sxs-lookup"><span data-stu-id="07743-145">nullptr is equivalent to L"".</span></span> <span data-ttu-id="07743-146">Описание фильтров контекста ресурсов приведено в разделе WEBVIEW2_WEB_RESOURCE_CONTEXT перечисление.</span><span class="sxs-lookup"><span data-stu-id="07743-146">See WEBVIEW2_WEB_RESOURCE_CONTEXT enum for description of resource context filters.</span></span>

#### <span data-ttu-id="07743-147">RemoveWebResourceRequestedFilter</span><span class="sxs-lookup"><span data-stu-id="07743-147">RemoveWebResourceRequestedFilter</span></span> 

<span data-ttu-id="07743-148">Удаляет соответствующий фильтр веб-ресурсов, который ранее был добавлен для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="07743-148">Removes a matching WebResource filter that was previously added for the WebResourceRequested event.</span></span>

> <span data-ttu-id="07743-149">общедоступный HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(LPCWSTR const uri,[WEBVIEW2_WEB_RESOURCE_CONTEXT](IWebView2WebView.md#webview2_web_resource_context) const разделе ResourceContext)</span><span class="sxs-lookup"><span data-stu-id="07743-149">public HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(LPCWSTR const uri,[WEBVIEW2_WEB_RESOURCE_CONTEXT](IWebView2WebView.md#webview2_web_resource_context) const resourceContext)</span></span>

<span data-ttu-id="07743-150">Если один и тот же фильтр был добавлен несколько значений, его необходимо будет удалить столько, сколько вхождений было добавлено для эффективного.</span><span class="sxs-lookup"><span data-stu-id="07743-150">If the same filter was added multiple times, then it will need to be removed as many times as it was added for the removal to be effective.</span></span> <span data-ttu-id="07743-151">Возвращает E_INVALIDARG для фильтра, который еще не был добавлен.</span><span class="sxs-lookup"><span data-stu-id="07743-151">Returns E_INVALIDARG for a filter that was never added.</span></span>

