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
ms.openlocfilehash: c23e6bcd18e3b0fe7d2ee9b279e65fc81fe89d3d
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654676"
---
# <span data-ttu-id="464a7-104">интерфейс IWebView2WebResourceRequestedEventArgs2</span><span class="sxs-lookup"><span data-stu-id="464a7-104">interface IWebView2WebResourceRequestedEventArgs2</span></span> 

> [!NOTE]
> <span data-ttu-id="464a7-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="464a7-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="464a7-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="464a7-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebResourceRequestedEventArgs2
  : public IWebView2WebResourceRequestedEventArgs
```

<span data-ttu-id="464a7-107">Аргументы события для события WebResourceRequested.</span><span class="sxs-lookup"><span data-stu-id="464a7-107">Event args for the WebResourceRequested event.</span></span>

## <span data-ttu-id="464a7-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="464a7-108">Summary</span></span>

 <span data-ttu-id="464a7-109">Участников</span><span class="sxs-lookup"><span data-stu-id="464a7-109">Members</span></span>                        | <span data-ttu-id="464a7-110">Описания</span><span class="sxs-lookup"><span data-stu-id="464a7-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="464a7-111">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="464a7-111">get_ResourceContext</span></span>](#get_resourcecontext) | <span data-ttu-id="464a7-112">Контексты запросов веб-ресурсов.</span><span class="sxs-lookup"><span data-stu-id="464a7-112">The web resource request contexts.</span></span>

## <span data-ttu-id="464a7-113">Участников</span><span class="sxs-lookup"><span data-stu-id="464a7-113">Members</span></span>

#### <span data-ttu-id="464a7-114">get_ResourceContext</span><span class="sxs-lookup"><span data-stu-id="464a7-114">get_ResourceContext</span></span> 

<span data-ttu-id="464a7-115">Контексты запросов веб-ресурсов.</span><span class="sxs-lookup"><span data-stu-id="464a7-115">The web resource request contexts.</span></span>

> <span data-ttu-id="464a7-116">общедоступные значения HRESULT [get_ResourceContext](#get_resourcecontext)(WEBVIEW2_WEB_RESOURCE_CONTEXT \* контекст)</span><span class="sxs-lookup"><span data-stu-id="464a7-116">public HRESULT [get_ResourceContext](#get_resourcecontext)(WEBVIEW2_WEB_RESOURCE_CONTEXT \* context)</span></span>

