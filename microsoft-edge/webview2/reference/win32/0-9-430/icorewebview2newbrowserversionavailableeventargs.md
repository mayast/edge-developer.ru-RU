---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NewBrowserVersionAvailableEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 9f56ba33534c76cb1bd60c01a88eedfced45f1fb
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884864"
---
# <span data-ttu-id="982df-104">0.9.430-Interface ICoreWebView2NewBrowserVersionAvailableEventArgs</span><span class="sxs-lookup"><span data-stu-id="982df-104">0.9.430 - interface ICoreWebView2NewBrowserVersionAvailableEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2NewBrowserVersionAvailableEventArgs
  : public IUnknown
```

<span data-ttu-id="982df-105">Аргументы события для события NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="982df-105">Event args for the NewBrowserVersionAvailable event.</span></span>

## <span data-ttu-id="982df-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="982df-106">Summary</span></span>

 <span data-ttu-id="982df-107">Участников</span><span class="sxs-lookup"><span data-stu-id="982df-107">Members</span></span>                        | <span data-ttu-id="982df-108">Описания</span><span class="sxs-lookup"><span data-stu-id="982df-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="982df-109">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="982df-109">get_NewVersion</span></span>](#get_newversion) | <span data-ttu-id="982df-110">Сведения о версии браузера для текущего [ICoreWebView2Environment](ICoreWebView2Environment.md).</span><span class="sxs-lookup"><span data-stu-id="982df-110">The browser version info of the current [ICoreWebView2Environment](ICoreWebView2Environment.md).</span></span>

## <span data-ttu-id="982df-111">Участников</span><span class="sxs-lookup"><span data-stu-id="982df-111">Members</span></span>

#### <span data-ttu-id="982df-112">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="982df-112">get_NewVersion</span></span> 

<span data-ttu-id="982df-113">Сведения о версии браузера для текущего [ICoreWebView2Environment](ICoreWebView2Environment.md).</span><span class="sxs-lookup"><span data-stu-id="982df-113">The browser version info of the current [ICoreWebView2Environment](ICoreWebView2Environment.md).</span></span>

> <span data-ttu-id="982df-114">общедоступные значения HRESULT [get_NewVersion](#get_newversion)(LPWSTR \* NewVersion)</span><span class="sxs-lookup"><span data-stu-id="982df-114">public HRESULT [get_NewVersion](#get_newversion)(LPWSTR \* newVersion)</span></span>

