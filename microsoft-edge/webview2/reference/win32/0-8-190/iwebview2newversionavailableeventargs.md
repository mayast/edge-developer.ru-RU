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
ms.openlocfilehash: 0314c796865d3d745b831d050498f59868e38e8f
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654956"
---
# <span data-ttu-id="a618f-104">интерфейс IWebView2NewVersionAvailableEventArgs</span><span class="sxs-lookup"><span data-stu-id="a618f-104">interface IWebView2NewVersionAvailableEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="a618f-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="a618f-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="a618f-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="a618f-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2NewVersionAvailableEventArgs
  : public IUnknown
```

<span data-ttu-id="a618f-107">Аргументы события для события NewVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="a618f-107">Event args for the NewVersionAvailable event.</span></span>

## <span data-ttu-id="a618f-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="a618f-108">Summary</span></span>

 <span data-ttu-id="a618f-109">Участников</span><span class="sxs-lookup"><span data-stu-id="a618f-109">Members</span></span>                        | <span data-ttu-id="a618f-110">Описания</span><span class="sxs-lookup"><span data-stu-id="a618f-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a618f-111">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="a618f-111">get_NewVersion</span></span>](#get_newversion) | <span data-ttu-id="a618f-112">Сведения о версии браузера для текущего [IWebView2Environment](IWebView2Environment.md).</span><span class="sxs-lookup"><span data-stu-id="a618f-112">The browser version info of the current [IWebView2Environment](IWebView2Environment.md).</span></span>

## <span data-ttu-id="a618f-113">Участников</span><span class="sxs-lookup"><span data-stu-id="a618f-113">Members</span></span>

#### <span data-ttu-id="a618f-114">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="a618f-114">get_NewVersion</span></span> 

<span data-ttu-id="a618f-115">Сведения о версии браузера для текущего [IWebView2Environment](IWebView2Environment.md).</span><span class="sxs-lookup"><span data-stu-id="a618f-115">The browser version info of the current [IWebView2Environment](IWebView2Environment.md).</span></span>

> <span data-ttu-id="a618f-116">общедоступные значения HRESULT [get_NewVersion](#get_newversion)(LPWSTR \* NewVersion)</span><span class="sxs-lookup"><span data-stu-id="a618f-116">public HRESULT [get_NewVersion](#get_newversion)(LPWSTR \* newVersion)</span></span>

