---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: d43cbe741cc9cd8b027a21115133db9377a95658
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654806"
---
# <span data-ttu-id="313e8-104">интерфейс IWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="313e8-104">interface IWebView2Deferral</span></span> 

> [!NOTE]
> <span data-ttu-id="313e8-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="313e8-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="313e8-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="313e8-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2Deferral
  : public IUnknown
```

<span data-ttu-id="313e8-107">Этот интерфейс используется для выполнения РБП для аргументов события, которые поддерживают сбор расходов будущих периодов с помощью методаического РБП.</span><span class="sxs-lookup"><span data-stu-id="313e8-107">This interface is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="313e8-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="313e8-108">Summary</span></span>

 <span data-ttu-id="313e8-109">Участников</span><span class="sxs-lookup"><span data-stu-id="313e8-109">Members</span></span>                        | <span data-ttu-id="313e8-110">Описания</span><span class="sxs-lookup"><span data-stu-id="313e8-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="313e8-111">Выполнено</span><span class="sxs-lookup"><span data-stu-id="313e8-111">Complete</span></span>](#complete) | <span data-ttu-id="313e8-112">Завершает связанное отложенное событие.</span><span class="sxs-lookup"><span data-stu-id="313e8-112">Completes the associated deferred event.</span></span>

## <span data-ttu-id="313e8-113">Участников</span><span class="sxs-lookup"><span data-stu-id="313e8-113">Members</span></span>

#### <span data-ttu-id="313e8-114">Выполнено</span><span class="sxs-lookup"><span data-stu-id="313e8-114">Complete</span></span> 

<span data-ttu-id="313e8-115">Завершает связанное отложенное событие.</span><span class="sxs-lookup"><span data-stu-id="313e8-115">Completes the associated deferred event.</span></span>

> <span data-ttu-id="313e8-116">общедоступное значение HRESULT [Complete](#complete)()</span><span class="sxs-lookup"><span data-stu-id="313e8-116">public HRESULT [Complete](#complete)()</span></span>

<span data-ttu-id="313e8-117">"Завершить" следует вызывать только один раз для каждого периода отсрочки.</span><span class="sxs-lookup"><span data-stu-id="313e8-117">Complete should only be called once for each deferral taken.</span></span>

