---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ExperimentalNewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2ExperimentalNewWindowRequestedEventArgs
ms.openlocfilehash: d18ccc91d16213cf0a915420b406b65823b3f9d9
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886453"
---
# <span data-ttu-id="8e5f2-104">интерфейс ICoreWebView2ExperimentalNewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="8e5f2-104">interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs</span></span> 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="8e5f2-105">Аргументы события для события NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="8e5f2-105">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="8e5f2-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="8e5f2-106">Summary</span></span>

 <span data-ttu-id="8e5f2-107">Участников</span><span class="sxs-lookup"><span data-stu-id="8e5f2-107">Members</span></span>                        | <span data-ttu-id="8e5f2-108">Описания</span><span class="sxs-lookup"><span data-stu-id="8e5f2-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8e5f2-109">get_WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="8e5f2-109">get_WindowFeatures</span></span>](#get_windowfeatures) | <span data-ttu-id="8e5f2-110">Функциональные возможности, заданные в окне вызова Window. Open.</span><span class="sxs-lookup"><span data-stu-id="8e5f2-110">Window features specified by the window.open call.</span></span>

<span data-ttu-id="8e5f2-111">Событие возникает, когда содержимое в WebView запрашивается на открытие нового окна (посредством Window. Open () и т. д.).</span><span class="sxs-lookup"><span data-stu-id="8e5f2-111">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="8e5f2-112">Участников</span><span class="sxs-lookup"><span data-stu-id="8e5f2-112">Members</span></span>

#### <span data-ttu-id="8e5f2-113">get_WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="8e5f2-113">get_WindowFeatures</span></span> 

<span data-ttu-id="8e5f2-114">Функциональные возможности, заданные в окне вызова Window. Open.</span><span class="sxs-lookup"><span data-stu-id="8e5f2-114">Window features specified by the window.open call.</span></span>

> <span data-ttu-id="8e5f2-115">общедоступные значения HRESULT [get_WindowFeatures](#get_windowfeatures)([ICoreWebView2ExperimentalWindowFeatures](icorewebview2experimentalwindowfeatures.md) \* \* WindowFeatures)</span><span class="sxs-lookup"><span data-stu-id="8e5f2-115">public HRESULT [get_WindowFeatures](#get_windowfeatures)([ICoreWebView2ExperimentalWindowFeatures](icorewebview2experimentalwindowfeatures.md) \*\* windowFeatures)</span></span>

<span data-ttu-id="8e5f2-116">Эти функции можно учитывать при размещении и изменении размера новых окон WebView.</span><span class="sxs-lookup"><span data-stu-id="8e5f2-116">These features can be considered for positioning and sizing of new webview windows.</span></span>

