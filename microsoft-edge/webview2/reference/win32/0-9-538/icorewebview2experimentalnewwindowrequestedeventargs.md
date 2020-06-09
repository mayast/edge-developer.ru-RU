---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 1d91bb767045179a5d8de3700f86ff6d92a9ef36
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699294"
---
# <span data-ttu-id="f6886-104">интерфейс ICoreWebView2ExperimentalNewWindowRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="f6886-104">interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="f6886-105">Это экспериментальный API-интерфейс, поставляемый с предварительной версией SDK версии 0.9.538.</span><span class="sxs-lookup"><span data-stu-id="f6886-105">This an experimental API that is shipped with our prerelease SDK version 0.9.538.</span></span>

```
interface ICoreWebView2ExperimentalNewWindowRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="f6886-106">Аргументы события для события NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="f6886-106">Event args for the NewWindowRequested event.</span></span>

## <span data-ttu-id="f6886-107">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="f6886-107">Summary</span></span>

 <span data-ttu-id="f6886-108">Участников</span><span class="sxs-lookup"><span data-stu-id="f6886-108">Members</span></span>                        | <span data-ttu-id="f6886-109">Описания</span><span class="sxs-lookup"><span data-stu-id="f6886-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f6886-110">get_WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="f6886-110">get_WindowFeatures</span></span>](#get_windowfeatures) | <span data-ttu-id="f6886-111">Функциональные возможности, заданные в окне вызова Window. Open.</span><span class="sxs-lookup"><span data-stu-id="f6886-111">Window features specified by the window.open call.</span></span>

<span data-ttu-id="f6886-112">Событие возникает, когда содержимое в WebView запрашивается на открытие нового окна (посредством Window. Open () и т. д.).</span><span class="sxs-lookup"><span data-stu-id="f6886-112">The event is fired when content inside webview requested to a open a new window (through window.open() and so on.)</span></span>

## <span data-ttu-id="f6886-113">Участников</span><span class="sxs-lookup"><span data-stu-id="f6886-113">Members</span></span>

#### <span data-ttu-id="f6886-114">get_WindowFeatures</span><span class="sxs-lookup"><span data-stu-id="f6886-114">get_WindowFeatures</span></span> 

<span data-ttu-id="f6886-115">Функциональные возможности, заданные в окне вызова Window. Open.</span><span class="sxs-lookup"><span data-stu-id="f6886-115">Window features specified by the window.open call.</span></span>

> <span data-ttu-id="f6886-116">общедоступные значения HRESULT [get_WindowFeatures](#get_windowfeatures)([ICoreWebView2ExperimentalWindowFeatures](icorewebview2experimentalwindowfeatures.md) \* \* WindowFeatures)</span><span class="sxs-lookup"><span data-stu-id="f6886-116">public HRESULT [get_WindowFeatures](#get_windowfeatures)([ICoreWebView2ExperimentalWindowFeatures](icorewebview2experimentalwindowfeatures.md) \*\* windowFeatures)</span></span>

<span data-ttu-id="f6886-117">Эти функции можно учитывать при размещении и изменении размера новых окон WebView.</span><span class="sxs-lookup"><span data-stu-id="f6886-117">These features can be considered for positioning and sizing of new webview windows.</span></span>

