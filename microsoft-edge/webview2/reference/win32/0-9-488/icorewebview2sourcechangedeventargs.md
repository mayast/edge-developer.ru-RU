---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 6d4c5e7893f9be78baca25e8976ca889ef9826c0
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654965"
---
# <span data-ttu-id="68352-104">интерфейс ICoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="68352-104">interface ICoreWebView2SourceChangedEventArgs</span></span> 

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="68352-105">Аргументы события для события SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="68352-105">Event args for the SourceChanged event.</span></span>

## <span data-ttu-id="68352-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="68352-106">Summary</span></span>

 <span data-ttu-id="68352-107">Участников</span><span class="sxs-lookup"><span data-stu-id="68352-107">Members</span></span>                        | <span data-ttu-id="68352-108">Описания</span><span class="sxs-lookup"><span data-stu-id="68352-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="68352-109">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="68352-109">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="68352-110">Значение true, если страница, на которую осуществляется переход, является новым документом.</span><span class="sxs-lookup"><span data-stu-id="68352-110">True if the page being navigated to is a new document.</span></span>

## <span data-ttu-id="68352-111">Участников</span><span class="sxs-lookup"><span data-stu-id="68352-111">Members</span></span>

#### <span data-ttu-id="68352-112">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="68352-112">get_IsNewDocument</span></span> 

<span data-ttu-id="68352-113">Значение true, если страница, на которую осуществляется переход, является новым документом.</span><span class="sxs-lookup"><span data-stu-id="68352-113">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="68352-114">общедоступные значения HRESULT [get_IsNewDocument](#get_isnewdocument)(bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="68352-114">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

