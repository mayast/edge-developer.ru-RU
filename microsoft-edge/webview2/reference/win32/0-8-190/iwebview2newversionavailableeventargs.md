---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2NewVersionAvailableEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 4271cc1002de70db2803a5bd6d4be73748bf5bbb
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885872"
---
# <span data-ttu-id="6e2a3-104">0.8.355-Interface IWebView2NewVersionAvailableEventArgs</span><span class="sxs-lookup"><span data-stu-id="6e2a3-104">0.8.355 - interface IWebView2NewVersionAvailableEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2NewVersionAvailableEventArgs
  : public IUnknown
```

<span data-ttu-id="6e2a3-105">Аргументы события для события NewVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="6e2a3-105">Event args for the NewVersionAvailable event.</span></span>

## <span data-ttu-id="6e2a3-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="6e2a3-106">Summary</span></span>

 <span data-ttu-id="6e2a3-107">Участников</span><span class="sxs-lookup"><span data-stu-id="6e2a3-107">Members</span></span>                        | <span data-ttu-id="6e2a3-108">Описания</span><span class="sxs-lookup"><span data-stu-id="6e2a3-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6e2a3-109">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="6e2a3-109">get_NewVersion</span></span>](#get_newversion) | <span data-ttu-id="6e2a3-110">Сведения о версии браузера для текущего [IWebView2Environment](IWebView2Environment.md).</span><span class="sxs-lookup"><span data-stu-id="6e2a3-110">The browser version info of the current [IWebView2Environment](IWebView2Environment.md).</span></span>

## <span data-ttu-id="6e2a3-111">Участников</span><span class="sxs-lookup"><span data-stu-id="6e2a3-111">Members</span></span>

#### <span data-ttu-id="6e2a3-112">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="6e2a3-112">get_NewVersion</span></span> 

<span data-ttu-id="6e2a3-113">Сведения о версии браузера для текущего [IWebView2Environment](IWebView2Environment.md).</span><span class="sxs-lookup"><span data-stu-id="6e2a3-113">The browser version info of the current [IWebView2Environment](IWebView2Environment.md).</span></span>

> <span data-ttu-id="6e2a3-114">общедоступные значения HRESULT [get_NewVersion](#get_newversion)(LPWSTR \* NewVersion)</span><span class="sxs-lookup"><span data-stu-id="6e2a3-114">public HRESULT [get_NewVersion](#get_newversion)(LPWSTR \* newVersion)</span></span>

