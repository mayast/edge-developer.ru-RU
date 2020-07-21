---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2WebView3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: a095b1ed085cd49a597195e01da21cde53b9095d
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884745"
---
# <span data-ttu-id="f0f2b-104">0.8.355-Interface IWebView2WebView3</span><span class="sxs-lookup"><span data-stu-id="f0f2b-104">0.8.355 - interface IWebView2WebView3</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebView3
  : public IWebView2WebView
```

<span data-ttu-id="f0f2b-105">Дополнительные функции, реализованные основным объектом WebView.</span><span class="sxs-lookup"><span data-stu-id="f0f2b-105">Additional functionality implemented by the primary WebView object.</span></span>

## <span data-ttu-id="f0f2b-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="f0f2b-106">Summary</span></span>

 <span data-ttu-id="f0f2b-107">Участников</span><span class="sxs-lookup"><span data-stu-id="f0f2b-107">Members</span></span>                        | <span data-ttu-id="f0f2b-108">Описания</span><span class="sxs-lookup"><span data-stu-id="f0f2b-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f0f2b-109">Stop</span><span class="sxs-lookup"><span data-stu-id="f0f2b-109">Stop</span></span>](#stop) | <span data-ttu-id="f0f2b-110">Остановите все переходы и ожидающие выборки ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f0f2b-110">Stop all navigations and pending resource fetches.</span></span>
[<span data-ttu-id="f0f2b-111">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="f0f2b-111">add_NewWindowRequested</span></span>](#add_newwindowrequested) | <span data-ttu-id="f0f2b-112">Добавьте обработчик событий для события NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="f0f2b-112">Add an event handler for the NewWindowRequested event.</span></span>
[<span data-ttu-id="f0f2b-113">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="f0f2b-113">remove_NewWindowRequested</span></span>](#remove_newwindowrequested) | <span data-ttu-id="f0f2b-114">Удалите обработчик событий, добавленный ранее add_NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="f0f2b-114">Remove an event handler previously added with add_NewWindowRequested.</span></span>
[<span data-ttu-id="f0f2b-115">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="f0f2b-115">add_DocumentTitleChanged</span></span>](#add_documenttitlechanged) | <span data-ttu-id="f0f2b-116">Добавьте обработчик событий для события DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="f0f2b-116">Add an event handler for the DocumentTitleChanged event.</span></span>
[<span data-ttu-id="f0f2b-117">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="f0f2b-117">remove_DocumentTitleChanged</span></span>](#remove_documenttitlechanged) | <span data-ttu-id="f0f2b-118">Удалите обработчик событий, добавленный ранее add_DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="f0f2b-118">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>
[<span data-ttu-id="f0f2b-119">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="f0f2b-119">get_DocumentTitle</span></span>](#get_documenttitle) | <span data-ttu-id="f0f2b-120">Название текущего документа верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="f0f2b-120">The title for the current top level document.</span></span>

<span data-ttu-id="f0f2b-121">Вы можете QueryInterface для этого интерфейса из объекта, реализующего [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="f0f2b-121">You can QueryInterface for this interface from the object that implements [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="f0f2b-122">Дополнительные сведения вы видите в интерфейсе [IWebView2WebView](IWebView2WebView.md) .</span><span class="sxs-lookup"><span data-stu-id="f0f2b-122">See the [IWebView2WebView](IWebView2WebView.md) interface for more details.</span></span>

## <span data-ttu-id="f0f2b-123">Участников</span><span class="sxs-lookup"><span data-stu-id="f0f2b-123">Members</span></span>

#### <span data-ttu-id="f0f2b-124">Stop</span><span class="sxs-lookup"><span data-stu-id="f0f2b-124">Stop</span></span> 

<span data-ttu-id="f0f2b-125">Остановите все переходы и ожидающие выборки ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f0f2b-125">Stop all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="f0f2b-126">открытая [Остановка](#stop)HRESULT ()</span><span class="sxs-lookup"><span data-stu-id="f0f2b-126">public HRESULT [Stop](#stop)()</span></span>

#### <span data-ttu-id="f0f2b-127">add_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="f0f2b-127">add_NewWindowRequested</span></span> 

<span data-ttu-id="f0f2b-128">Добавьте обработчик событий для события NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="f0f2b-128">Add an event handler for the NewWindowRequested event.</span></span>

> <span data-ttu-id="f0f2b-129">общедоступные значения HRESULT [add_NewWindowRequested](#add_newwindowrequested)([IWebView2NewWindowRequestedEventHandler](IWebView2NewWindowRequestedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="f0f2b-129">public HRESULT [add_NewWindowRequested](#add_newwindowrequested)([IWebView2NewWindowRequestedEventHandler](IWebView2NewWindowRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="f0f2b-130">Вызывается, когда содержимое в WebView запросило открыть новое окно, например с помощью Window. Open.</span><span class="sxs-lookup"><span data-stu-id="f0f2b-130">Fires when content inside the WebView requested to open a new window, such as through window.open.</span></span> <span data-ttu-id="f0f2b-131">Приложение может передавать целевую WebView, которая будет считаться открытым окном.</span><span class="sxs-lookup"><span data-stu-id="f0f2b-131">The app can pass a target webview that will be considered the opened window.</span></span>

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

#### <span data-ttu-id="f0f2b-132">remove_NewWindowRequested</span><span class="sxs-lookup"><span data-stu-id="f0f2b-132">remove_NewWindowRequested</span></span> 

<span data-ttu-id="f0f2b-133">Удалите обработчик событий, добавленный ранее add_NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="f0f2b-133">Remove an event handler previously added with add_NewWindowRequested.</span></span>

> <span data-ttu-id="f0f2b-134">общедоступные значения HRESULT [remove_NewWindowRequested](#remove_newwindowrequested)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="f0f2b-134">public HRESULT [remove_NewWindowRequested](#remove_newwindowrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="f0f2b-135">add_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="f0f2b-135">add_DocumentTitleChanged</span></span> 

<span data-ttu-id="f0f2b-136">Добавьте обработчик событий для события DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="f0f2b-136">Add an event handler for the DocumentTitleChanged event.</span></span>

> <span data-ttu-id="f0f2b-137">общедоступные значения HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([IWebView2DocumentTitleChangedEventHandler](IWebView2DocumentTitleChangedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="f0f2b-137">public HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([IWebView2DocumentTitleChangedEventHandler](IWebView2DocumentTitleChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="f0f2b-138">Событие активируется, когда свойство DocumentTitle объекта WebView изменяется и может срабатывать до или после события NavigationCompleted.</span><span class="sxs-lookup"><span data-stu-id="f0f2b-138">The event fires when the DocumentTitle property of the WebView changes and may fire before or after the NavigationCompleted event.</span></span>

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

#### <span data-ttu-id="f0f2b-139">remove_DocumentTitleChanged</span><span class="sxs-lookup"><span data-stu-id="f0f2b-139">remove_DocumentTitleChanged</span></span> 

<span data-ttu-id="f0f2b-140">Удалите обработчик событий, добавленный ранее add_DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="f0f2b-140">Remove an event handler previously added with add_DocumentTitleChanged.</span></span>

> <span data-ttu-id="f0f2b-141">общедоступные значения HRESULT [remove_DocumentTitleChanged](#remove_documenttitlechanged)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="f0f2b-141">public HRESULT [remove_DocumentTitleChanged](#remove_documenttitlechanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="f0f2b-142">get_DocumentTitle</span><span class="sxs-lookup"><span data-stu-id="f0f2b-142">get_DocumentTitle</span></span> 

<span data-ttu-id="f0f2b-143">Название текущего документа верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="f0f2b-143">The title for the current top level document.</span></span>

> <span data-ttu-id="f0f2b-144">общедоступные значения HRESULT [get_DocumentTitle](#get_documenttitle)(LPWSTR \* Title)</span><span class="sxs-lookup"><span data-stu-id="f0f2b-144">public HRESULT [get_DocumentTitle](#get_documenttitle)(LPWSTR \* title)</span></span>

<span data-ttu-id="f0f2b-145">Если документ не имеет явного заголовка или не является пустым, используется значение по умолчанию, которое может быть или не совпадать с URI документа.</span><span class="sxs-lookup"><span data-stu-id="f0f2b-145">If the document has no explicit title or is otherwise empty, a default that may or may not match the URI of the document will be used.</span></span>

