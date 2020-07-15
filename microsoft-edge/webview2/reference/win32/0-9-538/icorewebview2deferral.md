---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2Deferral
ms.openlocfilehash: 85c8a795a79bae461ad958e6586b9bf1f6778075
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880124"
---
# <span data-ttu-id="5515d-104">интерфейс ICoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="5515d-104">interface ICoreWebView2Deferral</span></span> 

```
interface ICoreWebView2Deferral
  : public IUnknown
```

<span data-ttu-id="5515d-105">Этот интерфейс используется для выполнения РБП для аргументов события, которые поддерживают сбор расходов будущих периодов с помощью методаического РБП.</span><span class="sxs-lookup"><span data-stu-id="5515d-105">This interface is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="5515d-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="5515d-106">Summary</span></span>

 <span data-ttu-id="5515d-107">Участников</span><span class="sxs-lookup"><span data-stu-id="5515d-107">Members</span></span>                        | <span data-ttu-id="5515d-108">Описания</span><span class="sxs-lookup"><span data-stu-id="5515d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5515d-109">Выполнено</span><span class="sxs-lookup"><span data-stu-id="5515d-109">Complete</span></span>](#complete) | <span data-ttu-id="5515d-110">Завершает связанное отложенное событие.</span><span class="sxs-lookup"><span data-stu-id="5515d-110">Completes the associated deferred event.</span></span>

## <span data-ttu-id="5515d-111">Участников</span><span class="sxs-lookup"><span data-stu-id="5515d-111">Members</span></span>

#### <span data-ttu-id="5515d-112">Выполнено</span><span class="sxs-lookup"><span data-stu-id="5515d-112">Complete</span></span> 

<span data-ttu-id="5515d-113">Завершает связанное отложенное событие.</span><span class="sxs-lookup"><span data-stu-id="5515d-113">Completes the associated deferred event.</span></span>

> <span data-ttu-id="5515d-114">общедоступное значение HRESULT [Complete](#complete)()</span><span class="sxs-lookup"><span data-stu-id="5515d-114">public HRESULT [Complete](#complete)()</span></span>

<span data-ttu-id="5515d-115">"Завершить" следует вызывать только один раз для каждого периода отсрочки.</span><span class="sxs-lookup"><span data-stu-id="5515d-115">Complete should only be called once for each deferral taken.</span></span>

