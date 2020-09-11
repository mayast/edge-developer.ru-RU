---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2Experimental
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2Experimental
ms.openlocfilehash: 44795ab425e814054dd3d58cba585f1badfbf431
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012510"
---
# <span data-ttu-id="618cb-104">интерфейс ICoreWebView2Experimental</span><span class="sxs-lookup"><span data-stu-id="618cb-104">interface ICoreWebView2Experimental</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2Experimental
  : public IUnknown
```

## <span data-ttu-id="618cb-105">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="618cb-105">Summary</span></span>

 <span data-ttu-id="618cb-106">Участников</span><span class="sxs-lookup"><span data-stu-id="618cb-106">Members</span></span>                        | <span data-ttu-id="618cb-107">Описания</span><span class="sxs-lookup"><span data-stu-id="618cb-107">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="618cb-108">add_WebResourceResponseReceived</span><span class="sxs-lookup"><span data-stu-id="618cb-108">add_WebResourceResponseReceived</span></span>](#add_webresourceresponsereceived) | <span data-ttu-id="618cb-109">Добавьте обработчик событий для события WebResourceResponseReceived.</span><span class="sxs-lookup"><span data-stu-id="618cb-109">Add an event handler for the WebResourceResponseReceived event.</span></span>
[<span data-ttu-id="618cb-110">remove_WebResourceResponseReceived</span><span class="sxs-lookup"><span data-stu-id="618cb-110">remove_WebResourceResponseReceived</span></span>](#remove_webresourceresponsereceived) | <span data-ttu-id="618cb-111">Удаляет обработчик событий WebResourceResponseReceived, добавленный ранее add_WebResourceResponseReceived.</span><span class="sxs-lookup"><span data-stu-id="618cb-111">Removes the WebResourceResponseReceived event handler previously added with add_WebResourceResponseReceived.</span></span>

## <span data-ttu-id="618cb-112">Участников</span><span class="sxs-lookup"><span data-stu-id="618cb-112">Members</span></span>

#### <span data-ttu-id="618cb-113">add_WebResourceResponseReceived</span><span class="sxs-lookup"><span data-stu-id="618cb-113">add_WebResourceResponseReceived</span></span> 

<span data-ttu-id="618cb-114">Добавьте обработчик событий для события WebResourceResponseReceived.</span><span class="sxs-lookup"><span data-stu-id="618cb-114">Add an event handler for the WebResourceResponseReceived event.</span></span>

> <span data-ttu-id="618cb-115">общедоступные значения HRESULT [add_WebResourceResponseReceived](#add_webresourceresponsereceived)([ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler](icorewebview2experimentalwebresourceresponsereceivedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="618cb-115">public HRESULT [add_WebResourceResponseReceived](#add_webresourceresponsereceived)([ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler](icorewebview2experimentalwebresourceresponsereceivedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="618cb-116">Событие WebResourceResponseReceived срабатывает после того, как WebView получил и обработал ответ для запроса на веб-ресурс.</span><span class="sxs-lookup"><span data-stu-id="618cb-116">WebResourceResponseReceived event fires after the WebView has received and processed the response for a WebResource request.</span></span> <span data-ttu-id="618cb-117">Аргументы события включают в себя WebResourceRequest, отправленный по каналу и WebResourceResponse, включая все дополнительные заголовки, добавленные сетевым стеком, которые не были включены как часть связанного события WebResourceRequested, например заголовки проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="618cb-117">The event args include the WebResourceRequest as sent by the wire and WebResourceResponse received, including any additional headers added by the network stack that were not be included as part of the associated WebResourceRequested event, such as Authentication headers.</span></span> 
```cpp
    wil::com_ptr<ICoreWebView2Experimental> webviewExperimental;
    CHECK_FAILURE(m_appWindow->GetWebView()->QueryInterface(IID_PPV_ARGS(&webviewExperimental)));
    CHECK_FAILURE(webviewExperimental->add_WebResourceResponseReceived(
        Callback<ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler>(
            [this](
                ICoreWebView2Experimental* sender,
                ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs* args) {           
                wil::com_ptr<ICoreWebView2WebResourceRequest> request;
                CHECK_FAILURE(args->get_Request(&request));
                wil::unique_cotaskmem_string uri;
                CHECK_FAILURE(request->get_Uri(&uri));
                if (wcscmp(uri.get(), L"https://authenticationtest.com/HTTPAuth/") == 0)
                {
                    wil::com_ptr<ICoreWebView2HttpRequestHeaders> requestHeaders;
                    CHECK_FAILURE(request->get_Headers(&requestHeaders));

                    wil::unique_cotaskmem_string authHeaderValue;
                    if (requestHeaders->GetHeader(L"Authorization", &authHeaderValue) == S_OK)
                    {
                        std::wstring message(L"Authorization: ");
                        message += authHeaderValue.get();
                        MessageBox(nullptr, message.c_str(), nullptr, MB_OK);
                        m_appWindow->DeleteComponent(this);
                    }
                }
                
                return S_OK;
            })
            .Get(),
        &m_webResourceResponseReceivedToken));
```

#### <span data-ttu-id="618cb-118">remove_WebResourceResponseReceived</span><span class="sxs-lookup"><span data-stu-id="618cb-118">remove_WebResourceResponseReceived</span></span> 

<span data-ttu-id="618cb-119">Удаляет обработчик событий WebResourceResponseReceived, добавленный ранее add_WebResourceResponseReceived.</span><span class="sxs-lookup"><span data-stu-id="618cb-119">Removes the WebResourceResponseReceived event handler previously added with add_WebResourceResponseReceived.</span></span>

> <span data-ttu-id="618cb-120">общедоступные значения HRESULT [remove_WebResourceResponseReceived](#remove_webresourceresponsereceived)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="618cb-120">public HRESULT [remove_WebResourceResponseReceived](#remove_webresourceresponsereceived)(EventRegistrationToken token)</span></span>

