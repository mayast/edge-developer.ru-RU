---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: f40d0baa415ccc76747993c4070bb05eaf76fe56
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878612"
---
# <span data-ttu-id="4a1b5-104">0.8.355-Interface IWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="4a1b5-104">0.8.355 - interface IWebView2Deferral</span></span> 

> [!NOTE]
> <span data-ttu-id="4a1b5-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="4a1b5-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="4a1b5-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="4a1b5-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2Deferral
  : public IUnknown
```

<span data-ttu-id="4a1b5-107">Этот интерфейс используется для выполнения РБП для аргументов события, которые поддерживают сбор расходов будущих периодов с помощью методаического РБП.</span><span class="sxs-lookup"><span data-stu-id="4a1b5-107">This interface is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="4a1b5-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="4a1b5-108">Summary</span></span>

 <span data-ttu-id="4a1b5-109">Участников</span><span class="sxs-lookup"><span data-stu-id="4a1b5-109">Members</span></span>                        | <span data-ttu-id="4a1b5-110">Описания</span><span class="sxs-lookup"><span data-stu-id="4a1b5-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4a1b5-111">Выполнено</span><span class="sxs-lookup"><span data-stu-id="4a1b5-111">Complete</span></span>](#complete) | <span data-ttu-id="4a1b5-112">Завершает связанное отложенное событие.</span><span class="sxs-lookup"><span data-stu-id="4a1b5-112">Completes the associated deferred event.</span></span>

## <span data-ttu-id="4a1b5-113">Участников</span><span class="sxs-lookup"><span data-stu-id="4a1b5-113">Members</span></span>

#### <span data-ttu-id="4a1b5-114">Выполнено</span><span class="sxs-lookup"><span data-stu-id="4a1b5-114">Complete</span></span> 

<span data-ttu-id="4a1b5-115">Завершает связанное отложенное событие.</span><span class="sxs-lookup"><span data-stu-id="4a1b5-115">Completes the associated deferred event.</span></span>

> <span data-ttu-id="4a1b5-116">общедоступное значение HRESULT [Complete](#complete)()</span><span class="sxs-lookup"><span data-stu-id="4a1b5-116">public HRESULT [Complete](#complete)()</span></span>

<span data-ttu-id="4a1b5-117">"Завершить" следует вызывать только один раз для каждого периода отсрочки.</span><span class="sxs-lookup"><span data-stu-id="4a1b5-117">Complete should only be called once for each deferral taken.</span></span>

