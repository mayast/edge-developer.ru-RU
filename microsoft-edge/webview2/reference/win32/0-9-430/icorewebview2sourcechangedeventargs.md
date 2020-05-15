---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 69c569be7e712d0f5cfddbaa180419be8d475ad0
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655005"
---
# <span data-ttu-id="9101d-104">интерфейс ICoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="9101d-104">interface ICoreWebView2SourceChangedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="9101d-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="9101d-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="9101d-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="9101d-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="9101d-107">Аргументы события для события SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="9101d-107">Event args for the SourceChanged event.</span></span>

## <span data-ttu-id="9101d-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="9101d-108">Summary</span></span>

 <span data-ttu-id="9101d-109">Участников</span><span class="sxs-lookup"><span data-stu-id="9101d-109">Members</span></span>                        | <span data-ttu-id="9101d-110">Описания</span><span class="sxs-lookup"><span data-stu-id="9101d-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9101d-111">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="9101d-111">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="9101d-112">Значение true, если страница, на которую осуществляется переход, является новым документом.</span><span class="sxs-lookup"><span data-stu-id="9101d-112">True if the page being navigated to is a new document.</span></span>

## <span data-ttu-id="9101d-113">Участников</span><span class="sxs-lookup"><span data-stu-id="9101d-113">Members</span></span>

#### <span data-ttu-id="9101d-114">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="9101d-114">get_IsNewDocument</span></span> 

<span data-ttu-id="9101d-115">Значение true, если страница, на которую осуществляется переход, является новым документом.</span><span class="sxs-lookup"><span data-stu-id="9101d-115">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="9101d-116">общедоступные значения HRESULT [get_IsNewDocument](#get_isnewdocument)(bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="9101d-116">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

