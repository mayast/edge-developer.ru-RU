---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: ebaab6dfe0781f544e89e86afc9f16ab50cb9222
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654892"
---
# <span data-ttu-id="f259d-104">интерфейс ICoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="f259d-104">interface ICoreWebView2Deferral</span></span> 

```
interface ICoreWebView2Deferral
  : public IUnknown
```

<span data-ttu-id="f259d-105">Этот интерфейс используется для выполнения РБП для аргументов события, которые поддерживают сбор расходов будущих периодов с помощью методаического РБП.</span><span class="sxs-lookup"><span data-stu-id="f259d-105">This interface is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="f259d-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="f259d-106">Summary</span></span>

 <span data-ttu-id="f259d-107">Участников</span><span class="sxs-lookup"><span data-stu-id="f259d-107">Members</span></span>                        | <span data-ttu-id="f259d-108">Описания</span><span class="sxs-lookup"><span data-stu-id="f259d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f259d-109">Выполнено</span><span class="sxs-lookup"><span data-stu-id="f259d-109">Complete</span></span>](#complete) | <span data-ttu-id="f259d-110">Завершает связанное отложенное событие.</span><span class="sxs-lookup"><span data-stu-id="f259d-110">Completes the associated deferred event.</span></span>

## <span data-ttu-id="f259d-111">Участников</span><span class="sxs-lookup"><span data-stu-id="f259d-111">Members</span></span>

#### <span data-ttu-id="f259d-112">Выполнено</span><span class="sxs-lookup"><span data-stu-id="f259d-112">Complete</span></span> 

<span data-ttu-id="f259d-113">Завершает связанное отложенное событие.</span><span class="sxs-lookup"><span data-stu-id="f259d-113">Completes the associated deferred event.</span></span>

> <span data-ttu-id="f259d-114">общедоступное значение HRESULT [Complete](#complete)()</span><span class="sxs-lookup"><span data-stu-id="f259d-114">public HRESULT [Complete](#complete)()</span></span>

<span data-ttu-id="f259d-115">"Завершить" следует вызывать только один раз для каждого периода отсрочки.</span><span class="sxs-lookup"><span data-stu-id="f259d-115">Complete should only be called once for each deferral taken.</span></span>

