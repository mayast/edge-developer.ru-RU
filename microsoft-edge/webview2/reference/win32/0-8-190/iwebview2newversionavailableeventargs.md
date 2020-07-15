---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2NewVersionAvailableEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: e8965ebe2e0434d83b4d6e8eabe74466adb7cec6
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878346"
---
# <span data-ttu-id="d0cdd-104">0.8.355-Interface IWebView2NewVersionAvailableEventArgs</span><span class="sxs-lookup"><span data-stu-id="d0cdd-104">0.8.355 - interface IWebView2NewVersionAvailableEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="d0cdd-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="d0cdd-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="d0cdd-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="d0cdd-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2NewVersionAvailableEventArgs
  : public IUnknown
```

<span data-ttu-id="d0cdd-107">Аргументы события для события NewVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="d0cdd-107">Event args for the NewVersionAvailable event.</span></span>

## <span data-ttu-id="d0cdd-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="d0cdd-108">Summary</span></span>

 <span data-ttu-id="d0cdd-109">Участников</span><span class="sxs-lookup"><span data-stu-id="d0cdd-109">Members</span></span>                        | <span data-ttu-id="d0cdd-110">Описания</span><span class="sxs-lookup"><span data-stu-id="d0cdd-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d0cdd-111">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="d0cdd-111">get_NewVersion</span></span>](#get_newversion) | <span data-ttu-id="d0cdd-112">Сведения о версии браузера для текущего [IWebView2Environment](IWebView2Environment.md).</span><span class="sxs-lookup"><span data-stu-id="d0cdd-112">The browser version info of the current [IWebView2Environment](IWebView2Environment.md).</span></span>

## <span data-ttu-id="d0cdd-113">Участников</span><span class="sxs-lookup"><span data-stu-id="d0cdd-113">Members</span></span>

#### <span data-ttu-id="d0cdd-114">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="d0cdd-114">get_NewVersion</span></span> 

<span data-ttu-id="d0cdd-115">Сведения о версии браузера для текущего [IWebView2Environment](IWebView2Environment.md).</span><span class="sxs-lookup"><span data-stu-id="d0cdd-115">The browser version info of the current [IWebView2Environment](IWebView2Environment.md).</span></span>

> <span data-ttu-id="d0cdd-116">общедоступные значения HRESULT [get_NewVersion](#get_newversion)(LPWSTR \* NewVersion)</span><span class="sxs-lookup"><span data-stu-id="d0cdd-116">public HRESULT [get_NewVersion](#get_newversion)(LPWSTR \* newVersion)</span></span>

