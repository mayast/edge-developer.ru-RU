---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2WebView3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: cfb99be772170ee458fa252133f90240d75af3db
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878052"
---
# <span data-ttu-id="a7cbf-104">0.8.355-Interface IWebView2WebView3</span><span class="sxs-lookup"><span data-stu-id="a7cbf-104">0.8.355 - interface IWebView2WebView3</span></span> 

> [!NOTE]
> <span data-ttu-id="a7cbf-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="a7cbf-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="a7cbf-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="a7cbf-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebView3
  : public IWebView2WebView
```

<span data-ttu-id="a7cbf-107">Дополнительные функции, реализованные основным объектом WebView.</span><span class="sxs-lookup"><span data-stu-id="a7cbf-107">Additional functionality implemented by the primary WebView object.</span></span>

## <span data-ttu-id="a7cbf-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="a7cbf-108">Summary</span></span>

 <span data-ttu-id="a7cbf-109">Участников</span><span class="sxs-lookup"><span data-stu-id="a7cbf-109">Members</span></span>                        | <span data-ttu-id="a7cbf-110">Описания</span><span class="sxs-lookup"><span data-stu-id="a7cbf-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a7cbf-111">Stop</span><span class="sxs-lookup"><span data-stu-id="a7cbf-111">Stop</span></span>](#stop) | <span data-ttu-id="a7cbf-112">Остановите все переходы и ожидающие выборки ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a7cbf-112">Stop all navigations and pending resource fetches.</span></span>
[<span data-ttu-id="a7cbf-113">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="a7cbf-113">add_NewWindowRequested</span></span>](#add_newwindowrequested) | <span data-ttu-id="a7cbf-114">Добавьте обработчик событий для события NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="a7cbf-114">Add an event handler for the NewWindowRequested event.</span></span>
[<span data-ttu-id="a7cbf-115">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="a7cbf-115">remove_NewWindowRequested</span></span>](#remove_newwindowrequested) | <span data-ttu-id="a7cbf-116">Удалите обработчик событий, добавленный ранее add_NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="a7cbf-116">Remove an event handler previously added with add_NewWindowRequested.</span></span>
[<span data-ttu-id="a7cbf-117">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="a7cbf-117">add_DocumentTitleChanged</span></span>](#add_documenttitlechanged) | <span data-ttu-id="a7cbf-118">Добавьте обработчик событий для события DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="a7cbf-118">Add an event handler for the DocumentTitleChanged event.</span></span>
[<span data-ttu-id="a7cbf-119">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="a7cbf-119">remove_DocumentTitleChanged</span></span>](#remove_documenttitlechanged) | <span data-ttu-id="a7cbf-120">Удалите обработчик событий, добавленный ранее add_DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="a7cbf-120">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>
[<span data-ttu-id="a7cbf-121">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="a7cbf-121">get_DocumentTitle</span></span>](#get_documenttitle) | <span data-ttu-id="a7cbf-122">Название текущего документа верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="a7cbf-122">The title for the current top level document.</span></span>

<span data-ttu-id="a7cbf-123">Вы можете QueryInterface для этого интерфейса из объекта, реализующего [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="a7cbf-123">You can QueryInterface for this interface from the object that implements [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="a7cbf-124">Дополнительные сведения вы видите в интерфейсе [IWebView2WebView](IWebView2WebView.md) .</span><span class="sxs-lookup"><span data-stu-id="a7cbf-124">See the [IWebView2WebView](IWebView2WebView.md) interface for more details.</span></span>

## <span data-ttu-id="a7cbf-125">Участников</span><span class="sxs-lookup"><span data-stu-id="a7cbf-125">Members</span></span>

#### <span data-ttu-id="a7cbf-126">Stop</span><span class="sxs-lookup"><span data-stu-id="a7cbf-126">Stop</span></span> 

<span data-ttu-id="a7cbf-127">Остановите все переходы и ожидающие выборки ресурсов.</span><span class="sxs-lookup"><span data-stu-id="a7cbf-127">Stop all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="a7cbf-128">открытая [Остановка](#stop)HRESULT ()</span><span class="sxs-lookup"><span data-stu-id="a7cbf-128">public HRESULT [Stop](#stop)()</span></span>

#### <span data-ttu-id="a7cbf-129">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="a7cbf-129">add_NewWindowRequested</span></span> 

<span data-ttu-id="a7cbf-130">Добавьте обработчик событий для события NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="a7cbf-130">Add an event handler for the NewWindowRequested event.</span></span>

> <span data-ttu-id="a7cbf-131">общедоступные значения HRESULT [add_NewWindowRequested](#add_newwindowrequested)([IWebView2NewWindowRequestedEventHandler](IWebView2NewWindowRequestedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="a7cbf-131">public HRESULT [add_NewWindowRequested](#add_newwindowrequested)([IWebView2NewWindowRequestedEventHandler](IWebView2NewWindowRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="a7cbf-132">Вызывается, когда содержимое в WebView запросило открыть новое окно, например с помощью Window. Open.</span><span class="sxs-lookup"><span data-stu-id="a7cbf-132">Fires when content inside the WebView requested to open a new window, such as through window.open.</span></span> <span data-ttu-id="a7cbf-133">Приложение может передавать целевую WebView, которая будет считаться открытым окном.</span><span class="sxs-lookup"><span data-stu-id="a7cbf-133">The app can pass a target webview that will be considered the opened window.</span></span>

```cpp
    // Register a handler for the NewWindowRequested event.
    // This handler will defer the event, create a new app window, and then once the
    // new window is ready, it'll provide that new window's WebView as the response to
    // the request.
    CHECK_FAILURE(m_webView->add_NewWindowRequested(
        Callback<IWebView2NewWindowRequestedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2NewWindowRequestedEventArgs* args) {
                wil::com_ptr<IWebView2Deferral> deferral;
                CHECK_FAILURE(args->GetDeferral(&deferral));

                auto newAppWindow = new AppWindow(L"");
                newAppWindow->m_onWebViewFirstInitialized = [args, deferral, newAppWindow]() {
                    CHECK_FAILURE(args->put_NewWindow(newAppWindow->m_webView.get()));
                    CHECK_FAILURE(args->put_Handled(TRUE));
                    CHECK_FAILURE(deferral->Complete());
                };

                return S_OK;
            })
            .Get(),
        nullptr));
```

#### <span data-ttu-id="a7cbf-134">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="a7cbf-134">remove_NewWindowRequested</span></span> 

<span data-ttu-id="a7cbf-135">Удалите обработчик событий, добавленный ранее add_NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="a7cbf-135">Remove an event handler previously added with add_NewWindowRequested.</span></span>

> <span data-ttu-id="a7cbf-136">общедоступные значения HRESULT [remove_NewWindowRequested](#remove_newwindowrequested)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="a7cbf-136">public HRESULT [remove_NewWindowRequested](#remove_newwindowrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="a7cbf-137">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="a7cbf-137">add_DocumentTitleChanged</span></span> 

<span data-ttu-id="a7cbf-138">Добавьте обработчик событий для события DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="a7cbf-138">Add an event handler for the DocumentTitleChanged event.</span></span>

> <span data-ttu-id="a7cbf-139">общедоступные значения HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([IWebView2DocumentTitleChangedEventHandler](IWebView2DocumentTitleChangedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="a7cbf-139">public HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([IWebView2DocumentTitleChangedEventHandler](IWebView2DocumentTitleChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="a7cbf-140">Событие активируется, когда свойство DocumentTitle объекта WebView изменяется и может срабатывать до или после события NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="a7cbf-140">The event fires when the DocumentTitle property of the WebView changes and may fire before or after the NavigationCompleted event.</span></span>

```cpp
    // Register a handler for the DocumentTitleChanged event.
    // This handler just announces the new title on the window's title bar.
    CHECK_FAILURE(m_webView->add_DocumentTitleChanged(
        Callback<IWebView2DocumentTitleChangedEventHandler>(
            [this](IWebView2WebView3* sender, IUnknown* args) -> HRESULT {
                wil::unique_cotaskmem_string title;
                CHECK_FAILURE(sender->get_DocumentTitle(&title));
                SetWindowText(m_appWindow->GetMainWindow(), title.get());
                return S_OK;
            })
            .Get(),
        &m_documentTitleChangedToken));
```

#### <span data-ttu-id="a7cbf-141">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="a7cbf-141">remove_DocumentTitleChanged</span></span> 

<span data-ttu-id="a7cbf-142">Удалите обработчик событий, добавленный ранее add_DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="a7cbf-142">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>

> <span data-ttu-id="a7cbf-143">общедоступные значения HRESULT [remove_DocumentTitleChanged](#remove_documenttitlechanged)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="a7cbf-143">public HRESULT [remove_DocumentTitleChanged](#remove_documenttitlechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="a7cbf-144">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="a7cbf-144">get_DocumentTitle</span></span> 

<span data-ttu-id="a7cbf-145">Название текущего документа верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="a7cbf-145">The title for the current top level document.</span></span>

> <span data-ttu-id="a7cbf-146">общедоступные значения HRESULT [get_DocumentTitle](#get_documenttitle)(LPWSTR \* Title)</span><span class="sxs-lookup"><span data-stu-id="a7cbf-146">public HRESULT [get_DocumentTitle](#get_documenttitle)(LPWSTR \* title)</span></span>

<span data-ttu-id="a7cbf-147">Если документ не имеет явного заголовка или не является пустым, используется значение по умолчанию, которое может быть или не совпадать с URI документа.</span><span class="sxs-lookup"><span data-stu-id="a7cbf-147">If the document has no explicit title or is otherwise empty, a default that may or may not match the URI of the document will be used.</span></span>

