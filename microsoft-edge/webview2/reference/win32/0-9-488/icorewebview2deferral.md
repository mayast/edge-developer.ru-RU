---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: bd2ff8092ce0b8367ce4cc381e94dbd273ae1849
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880831"
---
# <span data-ttu-id="67b5c-104">0.9.515-Interface ICoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="67b5c-104">0.9.515 - interface ICoreWebView2Deferral</span></span> 

> [!NOTE]
> <span data-ttu-id="67b5c-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="67b5c-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="67b5c-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="67b5c-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2Deferral
  : public IUnknown
```

<span data-ttu-id="67b5c-107">Этот интерфейс используется для выполнения РБП для аргументов события, которые поддерживают сбор расходов будущих периодов с помощью методаического РБП.</span><span class="sxs-lookup"><span data-stu-id="67b5c-107">This interface is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="67b5c-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="67b5c-108">Summary</span></span>

 <span data-ttu-id="67b5c-109">Участников</span><span class="sxs-lookup"><span data-stu-id="67b5c-109">Members</span></span>                        | <span data-ttu-id="67b5c-110">Описания</span><span class="sxs-lookup"><span data-stu-id="67b5c-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="67b5c-111">Выполнено</span><span class="sxs-lookup"><span data-stu-id="67b5c-111">Complete</span></span>](#complete) | <span data-ttu-id="67b5c-112">Завершает связанное отложенное событие.</span><span class="sxs-lookup"><span data-stu-id="67b5c-112">Completes the associated deferred event.</span></span>

## <span data-ttu-id="67b5c-113">Участников</span><span class="sxs-lookup"><span data-stu-id="67b5c-113">Members</span></span>

#### <span data-ttu-id="67b5c-114">Выполнено</span><span class="sxs-lookup"><span data-stu-id="67b5c-114">Complete</span></span> 

<span data-ttu-id="67b5c-115">Завершает связанное отложенное событие.</span><span class="sxs-lookup"><span data-stu-id="67b5c-115">Completes the associated deferred event.</span></span>

> <span data-ttu-id="67b5c-116">общедоступное значение HRESULT [Complete](#complete)()</span><span class="sxs-lookup"><span data-stu-id="67b5c-116">public HRESULT [Complete](#complete)()</span></span>

<span data-ttu-id="67b5c-117">"Завершить" следует вызывать только один раз для каждого периода отсрочки.</span><span class="sxs-lookup"><span data-stu-id="67b5c-117">Complete should only be called once for each deferral taken.</span></span>

