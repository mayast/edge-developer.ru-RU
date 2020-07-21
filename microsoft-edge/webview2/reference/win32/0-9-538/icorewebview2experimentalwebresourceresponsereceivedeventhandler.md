---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler
ms.openlocfilehash: 9447420abddfdb44394042d6742ed1dafd299adf
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886566"
---
# <span data-ttu-id="faa29-104">интерфейс ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="faa29-104">interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalWebResourceResponseReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="faa29-105">Активируется при получении ответа на запрос на веб-ресурс в WebView.</span><span class="sxs-lookup"><span data-stu-id="faa29-105">Fires when a response for a request is received for a Web resource in the webview.</span></span>

## <span data-ttu-id="faa29-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="faa29-106">Summary</span></span>

 <span data-ttu-id="faa29-107">Участников</span><span class="sxs-lookup"><span data-stu-id="faa29-107">Members</span></span>                        | <span data-ttu-id="faa29-108">Описания</span><span class="sxs-lookup"><span data-stu-id="faa29-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="faa29-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="faa29-109">Invoke</span></span>](#invoke) | <span data-ttu-id="faa29-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="faa29-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="faa29-111">Ведущее приложение может использовать это событие для просмотра фактического запроса и ответа на веб-ресурс.</span><span class="sxs-lookup"><span data-stu-id="faa29-111">Host can use this event to view the actual request and response for a Web resource.</span></span> <span data-ttu-id="faa29-112">Сюда входят любые изменения запроса или ответа, внесенные сетевым стеком (например, Добавление заголовков авторизации) после того, как событие WebResourceRequested для связанного запроса будет инициировано.</span><span class="sxs-lookup"><span data-stu-id="faa29-112">This includes any request or response modifications made by the network stack (such as adding of Authorization headers) after the WebResourceRequested event for the associated request has fired.</span></span> <span data-ttu-id="faa29-113">Изменения, внесенные в объекты запроса или ответа, игнорируются.</span><span class="sxs-lookup"><span data-stu-id="faa29-113">Modifications made to the request or response objects are ignored.</span></span>

## <span data-ttu-id="faa29-114">Участников</span><span class="sxs-lookup"><span data-stu-id="faa29-114">Members</span></span>

#### <span data-ttu-id="faa29-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="faa29-115">Invoke</span></span> 

<span data-ttu-id="faa29-116">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="faa29-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="faa29-117">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2Experimental](icorewebview2experimental.md) \* sender, [ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs](icorewebview2experimentalwebresourceresponsereceivedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="faa29-117">public HRESULT [Invoke](#invoke)([ICoreWebView2Experimental](icorewebview2experimental.md) \* sender, [ICoreWebView2ExperimentalWebResourceResponseReceivedEventArgs](icorewebview2experimentalwebresourceresponsereceivedeventargs.md) \* args)</span></span>

