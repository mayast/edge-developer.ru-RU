---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2WebResourceRequestedEventArgs2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 80ea596f28d1afeb451ce20d495961ca4eed507a
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878115"
---
# <span data-ttu-id="87d5a-104">0.8.355-Interface IWebView2WebResourceRequestedEventArgs2</span><span class="sxs-lookup"><span data-stu-id="87d5a-104">0.8.355 - interface IWebView2WebResourceRequestedEventArgs2</span></span> 

> [!NOTE]
> <span data-ttu-id="87d5a-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="87d5a-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="87d5a-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="87d5a-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebResourceRequestedEventArgs2
  : public IWebView2WebResourceRequestedEventArgs
```

<span data-ttu-id="87d5a-107">Аргументы события для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="87d5a-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="87d5a-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="87d5a-108">Summary</span></span>

 <span data-ttu-id="87d5a-109">Участников</span><span class="sxs-lookup"><span data-stu-id="87d5a-109">Members</span></span>                        | <span data-ttu-id="87d5a-110">Описания</span><span class="sxs-lookup"><span data-stu-id="87d5a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="87d5a-111">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="87d5a-111">get_ResourceContext</span></span>](#get_resourcecontext) | <span data-ttu-id="87d5a-112">Контексты запросов веб-ресурсов.</span><span class="sxs-lookup"><span data-stu-id="87d5a-112">The web resource request contexts.</span></span>

## <span data-ttu-id="87d5a-113">Участников</span><span class="sxs-lookup"><span data-stu-id="87d5a-113">Members</span></span>

#### <span data-ttu-id="87d5a-114">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="87d5a-114">get_ResourceContext</span></span> 

<span data-ttu-id="87d5a-115">Контексты запросов веб-ресурсов.</span><span class="sxs-lookup"><span data-stu-id="87d5a-115">The web resource request contexts.</span></span>

> <span data-ttu-id="87d5a-116">общедоступные значения HRESULT [get_ResourceContext](#get_resourcecontext)(WEBVIEW2_WEB_RESOURCE_CONTEXT \* контекст)</span><span class="sxs-lookup"><span data-stu-id="87d5a-116">public HRESULT [get_ResourceContext](#get_resourcecontext)(WEBVIEW2_WEB_RESOURCE_CONTEXT \* context)</span></span>

