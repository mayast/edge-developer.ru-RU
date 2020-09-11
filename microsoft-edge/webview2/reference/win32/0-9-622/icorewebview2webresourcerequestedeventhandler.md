---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2WebResourceRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2WebResourceRequestedEventHandler
ms.openlocfilehash: 6aa36c8b28a3e47a796324987687ab23179aae10
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012397"
---
# <span data-ttu-id="9e43d-104">интерфейс ICoreWebView2WebResourceRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="9e43d-104">interface ICoreWebView2WebResourceRequestedEventHandler</span></span> 

```
interface ICoreWebView2WebResourceRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="9e43d-105">Активируется при выполнении запроса URL-адреса (с помощью сети, файла и т. д.) в WebView для фильтрации контекста ресурсов и URL-адреса, указанных в AddWebResourceRequestedFilter.</span><span class="sxs-lookup"><span data-stu-id="9e43d-105">Fires when a URL request (through network, file etc.) is made in the webview for a Web resource matching resource context filter and URL specified in AddWebResourceRequestedFilter.</span></span>

## <span data-ttu-id="9e43d-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="9e43d-106">Summary</span></span>

 <span data-ttu-id="9e43d-107">Участников</span><span class="sxs-lookup"><span data-stu-id="9e43d-107">Members</span></span>                        | <span data-ttu-id="9e43d-108">Описания</span><span class="sxs-lookup"><span data-stu-id="9e43d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9e43d-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="9e43d-109">Invoke</span></span>](#invoke) | <span data-ttu-id="9e43d-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="9e43d-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="9e43d-111">Основное приложение может просматривать и изменять запрос, а также предоставлять ответ в соответствии с похожим шаблоном на HTTP, в этом случае запрос немедленно завершен.</span><span class="sxs-lookup"><span data-stu-id="9e43d-111">The host can view and modify the request or provide a response in a similar pattern to HTTP, in which case the request immediately completed.</span></span> <span data-ttu-id="9e43d-112">Это не может содержать заголовки запросов, добавленные сетевым стеком, например заголовки авторизации.</span><span class="sxs-lookup"><span data-stu-id="9e43d-112">This may not contain any request headers that are added by the network stack, such as Authorization headers.</span></span>

## <span data-ttu-id="9e43d-113">Участников</span><span class="sxs-lookup"><span data-stu-id="9e43d-113">Members</span></span>

#### <span data-ttu-id="9e43d-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="9e43d-114">Invoke</span></span> 

<span data-ttu-id="9e43d-115">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="9e43d-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="9e43d-116">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="9e43d-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebResourceRequestedEventArgs](icorewebview2webresourcerequestedeventargs.md) \* args)</span></span>

