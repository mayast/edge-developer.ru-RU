---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2SourceChangedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 8a9f1b1e44353796c6d3b57d3f4c6f3d4997aad5
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880201"
---
# <span data-ttu-id="511f6-104">0.9.430-Interface ICoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="511f6-104">0.9.430 - interface ICoreWebView2SourceChangedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="511f6-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="511f6-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="511f6-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="511f6-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="511f6-107">Аргументы события для события SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="511f6-107">Event args for the SourceChanged event.</span></span>

## <span data-ttu-id="511f6-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="511f6-108">Summary</span></span>

 <span data-ttu-id="511f6-109">Участников</span><span class="sxs-lookup"><span data-stu-id="511f6-109">Members</span></span>                        | <span data-ttu-id="511f6-110">Описания</span><span class="sxs-lookup"><span data-stu-id="511f6-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="511f6-111">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="511f6-111">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="511f6-112">Значение true, если страница, на которую осуществляется переход, является новым документом.</span><span class="sxs-lookup"><span data-stu-id="511f6-112">True if the page being navigated to is a new document.</span></span>

## <span data-ttu-id="511f6-113">Участников</span><span class="sxs-lookup"><span data-stu-id="511f6-113">Members</span></span>

#### <span data-ttu-id="511f6-114">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="511f6-114">get_IsNewDocument</span></span> 

<span data-ttu-id="511f6-115">Значение true, если страница, на которую осуществляется переход, является новым документом.</span><span class="sxs-lookup"><span data-stu-id="511f6-115">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="511f6-116">общедоступные значения HRESULT [get_IsNewDocument](#get_isnewdocument)(bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="511f6-116">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

