---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: b30b6e35388ab01433b2c879db82d9c4136fae99
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885426"
---
# <span data-ttu-id="2af9c-104">0.9.515-Interface ICoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="2af9c-104">0.9.515 - interface ICoreWebView2Deferral</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2Deferral
  : public IUnknown
```

<span data-ttu-id="2af9c-105">Этот интерфейс используется для выполнения РБП для аргументов события, которые поддерживают сбор расходов будущих периодов с помощью методаического РБП.</span><span class="sxs-lookup"><span data-stu-id="2af9c-105">This interface is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="2af9c-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="2af9c-106">Summary</span></span>

 <span data-ttu-id="2af9c-107">Участников</span><span class="sxs-lookup"><span data-stu-id="2af9c-107">Members</span></span>                        | <span data-ttu-id="2af9c-108">Описания</span><span class="sxs-lookup"><span data-stu-id="2af9c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2af9c-109">Выполнено</span><span class="sxs-lookup"><span data-stu-id="2af9c-109">Complete</span></span>](#complete) | <span data-ttu-id="2af9c-110">Завершает связанное отложенное событие.</span><span class="sxs-lookup"><span data-stu-id="2af9c-110">Completes the associated deferred event.</span></span>

## <span data-ttu-id="2af9c-111">Участников</span><span class="sxs-lookup"><span data-stu-id="2af9c-111">Members</span></span>

#### <span data-ttu-id="2af9c-112">Выполнено</span><span class="sxs-lookup"><span data-stu-id="2af9c-112">Complete</span></span> 

<span data-ttu-id="2af9c-113">Завершает связанное отложенное событие.</span><span class="sxs-lookup"><span data-stu-id="2af9c-113">Completes the associated deferred event.</span></span>

> <span data-ttu-id="2af9c-114">общедоступное значение HRESULT [Complete](#complete)()</span><span class="sxs-lookup"><span data-stu-id="2af9c-114">public HRESULT [Complete](#complete)()</span></span>

<span data-ttu-id="2af9c-115">"Завершить" следует вызывать только один раз для каждого периода отсрочки.</span><span class="sxs-lookup"><span data-stu-id="2af9c-115">Complete should only be called once for each deferral taken.</span></span>

