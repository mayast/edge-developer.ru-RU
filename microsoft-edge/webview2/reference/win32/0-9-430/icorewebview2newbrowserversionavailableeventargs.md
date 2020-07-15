---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NewBrowserVersionAvailableEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: f59b5acac510b66eae0e1ada51e28b6dd9363ca8
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877856"
---
# <span data-ttu-id="c383a-104">0.9.430-Interface ICoreWebView2NewBrowserVersionAvailableEventArgs</span><span class="sxs-lookup"><span data-stu-id="c383a-104">0.9.430 - interface ICoreWebView2NewBrowserVersionAvailableEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="c383a-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="c383a-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="c383a-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="c383a-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NewBrowserVersionAvailableEventArgs
  : public IUnknown
```

<span data-ttu-id="c383a-107">Аргументы события для события NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="c383a-107">Event args for the NewBrowserVersionAvailable event.</span></span>

## <span data-ttu-id="c383a-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="c383a-108">Summary</span></span>

 <span data-ttu-id="c383a-109">Участников</span><span class="sxs-lookup"><span data-stu-id="c383a-109">Members</span></span>                        | <span data-ttu-id="c383a-110">Описания</span><span class="sxs-lookup"><span data-stu-id="c383a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c383a-111">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="c383a-111">get_NewVersion</span></span>](#get_newversion) | <span data-ttu-id="c383a-112">Сведения о версии браузера для текущего [ICoreWebView2Environment](ICoreWebView2Environment.md).</span><span class="sxs-lookup"><span data-stu-id="c383a-112">The browser version info of the current [ICoreWebView2Environment](ICoreWebView2Environment.md).</span></span>

## <span data-ttu-id="c383a-113">Участников</span><span class="sxs-lookup"><span data-stu-id="c383a-113">Members</span></span>

#### <span data-ttu-id="c383a-114">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="c383a-114">get_NewVersion</span></span> 

<span data-ttu-id="c383a-115">Сведения о версии браузера для текущего [ICoreWebView2Environment](ICoreWebView2Environment.md).</span><span class="sxs-lookup"><span data-stu-id="c383a-115">The browser version info of the current [ICoreWebView2Environment](ICoreWebView2Environment.md).</span></span>

> <span data-ttu-id="c383a-116">общедоступные значения HRESULT [get_NewVersion](#get_newversion)(LPWSTR \* NewVersion)</span><span class="sxs-lookup"><span data-stu-id="c383a-116">public HRESULT [get_NewVersion](#get_newversion)(LPWSTR \* newVersion)</span></span>

