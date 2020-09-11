---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs
ms.openlocfilehash: 547e9a451283de55658a95a8134ecb8a838f9e50
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011407"
---
# <span data-ttu-id="f88f6-104">0.9.579-Interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="f88f6-104">0.9.579 - interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="f88f6-105">Аргументы события для события WebResourceResponseReceived.</span><span class="sxs-lookup"><span data-stu-id="f88f6-105">Event args for the WebResourceResponseReceived event.</span></span>

## <span data-ttu-id="f88f6-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="f88f6-106">Summary</span></span>

 <span data-ttu-id="f88f6-107">Участников</span><span class="sxs-lookup"><span data-stu-id="f88f6-107">Members</span></span>                        | <span data-ttu-id="f88f6-108">Описания</span><span class="sxs-lookup"><span data-stu-id="f88f6-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f88f6-109">get_Request</span><span class="sxs-lookup"><span data-stu-id="f88f6-109">get_Request</span></span>](#get_request) | <span data-ttu-id="f88f6-110">Объект запроса веб-ресурса.</span><span class="sxs-lookup"><span data-stu-id="f88f6-110">Web resource request object.</span></span> <span data-ttu-id="f88f6-111">Все изменения, внесенные в этот объект, будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="f88f6-111">Any modifications to this object will be ignored.</span></span>
[<span data-ttu-id="f88f6-112">get_Response</span><span class="sxs-lookup"><span data-stu-id="f88f6-112">get_Response</span></span>](#get_response) | <span data-ttu-id="f88f6-113">Объект ответа на веб-ресурс.</span><span class="sxs-lookup"><span data-stu-id="f88f6-113">Web resource response object.</span></span>
[<span data-ttu-id="f88f6-114">PopulateResponseContent</span><span class="sxs-lookup"><span data-stu-id="f88f6-114">PopulateResponseContent</span></span>](#populateresponsecontent) | <span data-ttu-id="f88f6-115">Метод Async для запроса потока содержимого ответа.</span><span class="sxs-lookup"><span data-stu-id="f88f6-115">Async method to request the Content stream of the response.</span></span>

<span data-ttu-id="f88f6-116">Будет содержать запрос, отправленный по мере его отправки, и ответ, полученный от него.</span><span class="sxs-lookup"><span data-stu-id="f88f6-116">Will contain the request as it was sent and the response as it was received.</span></span> <span data-ttu-id="f88f6-117">Примечание. чтобы получить поток содержимого ответа, сначала вызовите PopulateResponseContent и дождитесь завершения асинхронного вызова, в противном случае возвращаемый объект потока содержимого будет иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="f88f6-117">Note: To get the response content stream, first call PopulateResponseContent and wait for the async call to complete, otherwise the content stream object returned will be null.</span></span>

## <span data-ttu-id="f88f6-118">Участников</span><span class="sxs-lookup"><span data-stu-id="f88f6-118">Members</span></span>

#### <span data-ttu-id="f88f6-119">get_Request</span><span class="sxs-lookup"><span data-stu-id="f88f6-119">get_Request</span></span> 

<span data-ttu-id="f88f6-120">Объект запроса веб-ресурса.</span><span class="sxs-lookup"><span data-stu-id="f88f6-120">Web resource request object.</span></span> <span data-ttu-id="f88f6-121">Все изменения, внесенные в этот объект, будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="f88f6-121">Any modifications to this object will be ignored.</span></span>

> <span data-ttu-id="f88f6-122">общедоступные значения HRESULT [get_Request](#get_request)(запрос ICoreWebView2WebResourceRequest \* \*)</span><span class="sxs-lookup"><span data-stu-id="f88f6-122">public HRESULT [get_Request](#get_request)(ICoreWebView2WebResourceRequest \*\* request)</span></span>

#### <span data-ttu-id="f88f6-123">get_Response</span><span class="sxs-lookup"><span data-stu-id="f88f6-123">get_Response</span></span> 

<span data-ttu-id="f88f6-124">Объект ответа на веб-ресурс.</span><span class="sxs-lookup"><span data-stu-id="f88f6-124">Web resource response object.</span></span>

> <span data-ttu-id="f88f6-125">общедоступные значения HRESULT [get_Response](#get_response)(ICoreWebView2WebResourceResponse \* \* Response)</span><span class="sxs-lookup"><span data-stu-id="f88f6-125">public HRESULT [get_Response](#get_response)(ICoreWebView2WebResourceResponse \*\* response)</span></span>

<span data-ttu-id="f88f6-126">Все изменения, внесенные в этот объект, будут игнорироваться.</span><span class="sxs-lookup"><span data-stu-id="f88f6-126">Any modifications to this object will be ignored.</span></span>

#### <span data-ttu-id="f88f6-127">PopulateResponseContent</span><span class="sxs-lookup"><span data-stu-id="f88f6-127">PopulateResponseContent</span></span> 

<span data-ttu-id="f88f6-128">Метод Async для запроса потока содержимого ответа.</span><span class="sxs-lookup"><span data-stu-id="f88f6-128">Async method to request the Content stream of the response.</span></span>

> <span data-ttu-id="f88f6-129">общедоступные значения HRESULT [PopulateResponseContent](#populateresponsecontent)(обработчик[ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler](icorewebview2experimentalwebresourceresponsereceivedeventargspopulateresponsecontentcompletedhandler.md) \*)</span><span class="sxs-lookup"><span data-stu-id="f88f6-129">public HRESULT [PopulateResponseContent](#populateresponsecontent)([ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler](icorewebview2experimentalwebresourceresponsereceivedeventargspopulateresponsecontentcompletedhandler.md) \* handler)</span></span>

```cpp
                    args->PopulateResponseContent(
                        Callback<
                            ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgsPopulateResponseContentCompletedHandler>(
                            [this, webResourceRequest, webResourceResponse](HRESULT result) {
                                std::wstring message =
                                    L"{ \"kind\": \"event\", \"name\": "
                                    L"\"WebResourceResponseReceived\", \"args\": {"
                                    L"\"request\": " +
                                    RequestToJsonString(webResourceRequest.get()) +
                                    L", "
                                    L"\"response\": " +
                                    ResponseToJsonString(webResourceResponse.get()) + L"}";

                                message +=
                                    WebViewPropertiesToJsonString(m_webviewEventSource.get());
                                message += L"}";
                                PostEventMessage(message);
                                return S_OK;
                            })
                            .Get());
```

