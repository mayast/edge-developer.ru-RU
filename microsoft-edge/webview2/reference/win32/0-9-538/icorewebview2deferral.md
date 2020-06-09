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
ms.openlocfilehash: b5fcd04d702483778ef31549c2e7d989ebfe3689
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699186"
---
# <span data-ttu-id="ab4f7-104">интерфейс ICoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="ab4f7-104">interface ICoreWebView2Deferral</span></span> 

```
interface ICoreWebView2Deferral
  : public IUnknown
```

<span data-ttu-id="ab4f7-105">Этот интерфейс используется для выполнения РБП для аргументов события, которые поддерживают сбор расходов будущих периодов с помощью методаического РБП.</span><span class="sxs-lookup"><span data-stu-id="ab4f7-105">This interface is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="ab4f7-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="ab4f7-106">Summary</span></span>

 <span data-ttu-id="ab4f7-107">Участников</span><span class="sxs-lookup"><span data-stu-id="ab4f7-107">Members</span></span>                        | <span data-ttu-id="ab4f7-108">Описания</span><span class="sxs-lookup"><span data-stu-id="ab4f7-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ab4f7-109">Выполнено</span><span class="sxs-lookup"><span data-stu-id="ab4f7-109">Complete</span></span>](#complete) | <span data-ttu-id="ab4f7-110">Завершает связанное отложенное событие.</span><span class="sxs-lookup"><span data-stu-id="ab4f7-110">Completes the associated deferred event.</span></span>

## <span data-ttu-id="ab4f7-111">Участников</span><span class="sxs-lookup"><span data-stu-id="ab4f7-111">Members</span></span>

#### <span data-ttu-id="ab4f7-112">Выполнено</span><span class="sxs-lookup"><span data-stu-id="ab4f7-112">Complete</span></span> 

<span data-ttu-id="ab4f7-113">Завершает связанное отложенное событие.</span><span class="sxs-lookup"><span data-stu-id="ab4f7-113">Completes the associated deferred event.</span></span>

> <span data-ttu-id="ab4f7-114">общедоступное значение HRESULT [Complete](#complete)()</span><span class="sxs-lookup"><span data-stu-id="ab4f7-114">public HRESULT [Complete](#complete)()</span></span>

<span data-ttu-id="ab4f7-115">"Завершить" следует вызывать только один раз для каждого периода отсрочки.</span><span class="sxs-lookup"><span data-stu-id="ab4f7-115">Complete should only be called once for each deferral taken.</span></span>

