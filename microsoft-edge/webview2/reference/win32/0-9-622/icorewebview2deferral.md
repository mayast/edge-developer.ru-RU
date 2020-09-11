---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2Deferral
ms.openlocfilehash: d8abff93df317a42c1bfe89dd32ac1d5f7e8c329
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012570"
---
# <span data-ttu-id="c5eb3-104">интерфейс ICoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="c5eb3-104">interface ICoreWebView2Deferral</span></span> 

```
interface ICoreWebView2Deferral
  : public IUnknown
```

<span data-ttu-id="c5eb3-105">Этот интерфейс используется для выполнения РБП для аргументов события, которые поддерживают сбор расходов будущих периодов с помощью методаического РБП.</span><span class="sxs-lookup"><span data-stu-id="c5eb3-105">This interface is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="c5eb3-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="c5eb3-106">Summary</span></span>

 <span data-ttu-id="c5eb3-107">Участников</span><span class="sxs-lookup"><span data-stu-id="c5eb3-107">Members</span></span>                        | <span data-ttu-id="c5eb3-108">Описания</span><span class="sxs-lookup"><span data-stu-id="c5eb3-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c5eb3-109">Выполнено</span><span class="sxs-lookup"><span data-stu-id="c5eb3-109">Complete</span></span>](#complete) | <span data-ttu-id="c5eb3-110">Завершает связанное отложенное событие.</span><span class="sxs-lookup"><span data-stu-id="c5eb3-110">Completes the associated deferred event.</span></span>

## <span data-ttu-id="c5eb3-111">Участников</span><span class="sxs-lookup"><span data-stu-id="c5eb3-111">Members</span></span>

#### <span data-ttu-id="c5eb3-112">Выполнено</span><span class="sxs-lookup"><span data-stu-id="c5eb3-112">Complete</span></span> 

<span data-ttu-id="c5eb3-113">Завершает связанное отложенное событие.</span><span class="sxs-lookup"><span data-stu-id="c5eb3-113">Completes the associated deferred event.</span></span>

> <span data-ttu-id="c5eb3-114">общедоступное значение HRESULT [Complete](#complete)()</span><span class="sxs-lookup"><span data-stu-id="c5eb3-114">public HRESULT [Complete](#complete)()</span></span>

<span data-ttu-id="c5eb3-115">"Завершить" следует вызывать только один раз для каждого периода отсрочки.</span><span class="sxs-lookup"><span data-stu-id="c5eb3-115">Complete should only be called once for each deferral taken.</span></span>

