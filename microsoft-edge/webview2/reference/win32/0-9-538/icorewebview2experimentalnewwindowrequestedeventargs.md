---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ExperimentalNewWindowRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2ExperimentalNewWindowRequestedEventArgs
ms.openlocfilehash: 39d52b1231e767739b63b3759cdd08e4c9b26be3
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879991"
---
# <span data-ttu-id="74089-104">интерфейс ICoreWebView2ExperimentalNewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="74089-104">interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="74089-105">Это экспериментальный API-интерфейс, поставляемый с предварительной версией SDK версии 0.9.538.</span><span class="sxs-lookup"><span data-stu-id="74089-105">This an experimental API that is shipped with our prerelease SDK version 0.9.538.</span></span>

```
interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="74089-106">Аргументы события для события NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="74089-106">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="74089-107">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="74089-107">Summary</span></span>

 <span data-ttu-id="74089-108">Участников</span><span class="sxs-lookup"><span data-stu-id="74089-108">Members</span></span>                        | <span data-ttu-id="74089-109">Описания</span><span class="sxs-lookup"><span data-stu-id="74089-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="74089-110">get_WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="74089-110">get_WindowFeatures</span></span>](#get_windowfeatures) | <span data-ttu-id="74089-111">Функциональные возможности, заданные в окне вызова Window. Open.</span><span class="sxs-lookup"><span data-stu-id="74089-111">Window features specified by the window.open call.</span></span>

<span data-ttu-id="74089-112">Событие возникает, когда содержимое в WebView запрашивается на открытие нового окна (посредством Window. Open () и т. д.).</span><span class="sxs-lookup"><span data-stu-id="74089-112">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="74089-113">Участников</span><span class="sxs-lookup"><span data-stu-id="74089-113">Members</span></span>

#### <span data-ttu-id="74089-114">get_WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="74089-114">get_WindowFeatures</span></span> 

<span data-ttu-id="74089-115">Функциональные возможности, заданные в окне вызова Window. Open.</span><span class="sxs-lookup"><span data-stu-id="74089-115">Window features specified by the window.open call.</span></span>

> <span data-ttu-id="74089-116">общедоступные значения HRESULT [get_WindowFeatures](#get_windowfeatures)([ICoreWebView2ExperimentalWindowFeatures](icorewebview2experimentalwindowfeatures.md) \* \* WindowFeatures)</span><span class="sxs-lookup"><span data-stu-id="74089-116">public HRESULT [get_WindowFeatures](#get_windowfeatures)([ICoreWebView2ExperimentalWindowFeatures](icorewebview2experimentalwindowfeatures.md) \*\* windowFeatures)</span></span>

<span data-ttu-id="74089-117">Эти функции можно учитывать при размещении и изменении размера новых окон WebView.</span><span class="sxs-lookup"><span data-stu-id="74089-117">These features can be considered for positioning and sizing of new webview windows.</span></span>

