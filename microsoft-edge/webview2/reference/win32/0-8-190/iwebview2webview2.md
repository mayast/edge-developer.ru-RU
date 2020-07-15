---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 52218ddcbecdaf3bdb736af877493c85d4460c10
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878045"
---
# <span data-ttu-id="f52e3-104">0.8.355-Interface IWebView2WebView2</span><span class="sxs-lookup"><span data-stu-id="f52e3-104">0.8.355 - interface IWebView2WebView2</span></span> 

> [!NOTE]
> <span data-ttu-id="f52e3-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="f52e3-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="f52e3-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="f52e3-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebView2
  : public IUnknown
```

<span data-ttu-id="f52e3-107">Дополнительные функции, реализованные основным объектом WebView.</span><span class="sxs-lookup"><span data-stu-id="f52e3-107">Additional functionality implemented by the primary WebView object.</span></span>

## <span data-ttu-id="f52e3-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="f52e3-108">Summary</span></span>

 <span data-ttu-id="f52e3-109">Участников</span><span class="sxs-lookup"><span data-stu-id="f52e3-109">Members</span></span>                        | <span data-ttu-id="f52e3-110">Описания</span><span class="sxs-lookup"><span data-stu-id="f52e3-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f52e3-111">Stop</span><span class="sxs-lookup"><span data-stu-id="f52e3-111">Stop</span></span>](#stop) | <span data-ttu-id="f52e3-112">Остановите все переходы и ожидающие выборки ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f52e3-112">Stop all navigations and pending resource fetches.</span></span>

<span data-ttu-id="f52e3-113">Вы можете QueryInterface для этого интерфейса из объекта, реализующего [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="f52e3-113">You can QueryInterface for this interface from the object that implements [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="f52e3-114">Дополнительные сведения вы видите в интерфейсе [IWebView2WebView](IWebView2WebView.md) .</span><span class="sxs-lookup"><span data-stu-id="f52e3-114">See the [IWebView2WebView](IWebView2WebView.md) interface for more details.</span></span>

## <span data-ttu-id="f52e3-115">Участников</span><span class="sxs-lookup"><span data-stu-id="f52e3-115">Members</span></span>

#### <span data-ttu-id="f52e3-116">Stop</span><span class="sxs-lookup"><span data-stu-id="f52e3-116">Stop</span></span> 

<span data-ttu-id="f52e3-117">Остановите все переходы и ожидающие выборки ресурсов.</span><span class="sxs-lookup"><span data-stu-id="f52e3-117">Stop all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="f52e3-118">открытая [Остановка](#stop)HRESULT ()</span><span class="sxs-lookup"><span data-stu-id="f52e3-118">public HRESULT [Stop](#stop)()</span></span>

