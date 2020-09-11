---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ExperimentalNewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2ExperimentalNewWindowRequestedEventArgs
ms.openlocfilehash: 855425e5cbdd594c7a4bca12efe1827035ca2f3a
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011106"
---
# <span data-ttu-id="ed169-104">0.9.579-Interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="ed169-104">0.9.579 - interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="ed169-105">Аргументы события для события NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="ed169-105">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="ed169-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="ed169-106">Summary</span></span>

 <span data-ttu-id="ed169-107">Участников</span><span class="sxs-lookup"><span data-stu-id="ed169-107">Members</span></span>                        | <span data-ttu-id="ed169-108">Описания</span><span class="sxs-lookup"><span data-stu-id="ed169-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ed169-109">get_WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="ed169-109">get_WindowFeatures</span></span>](#get_windowfeatures) | <span data-ttu-id="ed169-110">Функциональные возможности, заданные в окне вызова Window. Open.</span><span class="sxs-lookup"><span data-stu-id="ed169-110">Window features specified by the window.open call.</span></span>

<span data-ttu-id="ed169-111">Событие возникает, когда содержимое в WebView запрашивается на открытие нового окна (посредством Window. Open () и т. д.).</span><span class="sxs-lookup"><span data-stu-id="ed169-111">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="ed169-112">Участников</span><span class="sxs-lookup"><span data-stu-id="ed169-112">Members</span></span>

#### <span data-ttu-id="ed169-113">get_WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="ed169-113">get_WindowFeatures</span></span> 

<span data-ttu-id="ed169-114">Функциональные возможности, заданные в окне вызова Window. Open.</span><span class="sxs-lookup"><span data-stu-id="ed169-114">Window features specified by the window.open call.</span></span>

> <span data-ttu-id="ed169-115">общедоступные значения HRESULT [get_WindowFeatures](#get_windowfeatures)([ICoreWebView2ExperimentalWindowFeatures](icorewebview2experimentalwindowfeatures.md) \* \* WindowFeatures)</span><span class="sxs-lookup"><span data-stu-id="ed169-115">public HRESULT [get_WindowFeatures](#get_windowfeatures)([ICoreWebView2ExperimentalWindowFeatures](icorewebview2experimentalwindowfeatures.md) \*\* windowFeatures)</span></span>

<span data-ttu-id="ed169-116">Эти функции можно учитывать при размещении и изменении размера новых окон WebView.</span><span class="sxs-lookup"><span data-stu-id="ed169-116">These features can be considered for positioning and sizing of new webview windows.</span></span>

