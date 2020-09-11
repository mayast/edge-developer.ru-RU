---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2WebResourceRequestedEventHandler
ms.openlocfilehash: a1bf9e05e403df10fc8e45ff5b5bc19f28558e3c
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010376"
---
# <span data-ttu-id="87b93-104">0.9.579-Interface ICoreWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="87b93-104">0.9.579 - interface ICoreWebView2WebResourceRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="87b93-105">Активируется при выполнении запроса URL-адреса (с помощью сети, файла и т. д.) в WebView для фильтрации контекста ресурсов и URL-адреса, указанных в AddWebResourceRequestedFilter.</span><span class="sxs-lookup"><span data-stu-id="87b93-105">Fires when a URL request (through network, file etc.) is made in the webview for a Web resource matching resource context filter and URL specified in AddWebResourceRequestedFilter.</span></span>

## <span data-ttu-id="87b93-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="87b93-106">Summary</span></span>

 <span data-ttu-id="87b93-107">Участников</span><span class="sxs-lookup"><span data-stu-id="87b93-107">Members</span></span>                        | <span data-ttu-id="87b93-108">Описания</span><span class="sxs-lookup"><span data-stu-id="87b93-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="87b93-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="87b93-109">Invoke</span></span>](#invoke) | <span data-ttu-id="87b93-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="87b93-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="87b93-111">Основное приложение может просматривать и изменять запрос, а также предоставлять ответ в соответствии с похожим шаблоном на HTTP, в этом случае запрос немедленно завершен.</span><span class="sxs-lookup"><span data-stu-id="87b93-111">The host can view and modify the request or provide a response in a similar pattern to HTTP, in which case the request immediately completed.</span></span> <span data-ttu-id="87b93-112">Это не может содержать заголовки запросов, добавленные сетевым стеком, например заголовки авторизации.</span><span class="sxs-lookup"><span data-stu-id="87b93-112">This may not contain any request headers that are added by the network stack, such as Authorization headers.</span></span>

## <span data-ttu-id="87b93-113">Участников</span><span class="sxs-lookup"><span data-stu-id="87b93-113">Members</span></span>

#### <span data-ttu-id="87b93-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="87b93-114">Invoke</span></span> 

<span data-ttu-id="87b93-115">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="87b93-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="87b93-116">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="87b93-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span></span>

