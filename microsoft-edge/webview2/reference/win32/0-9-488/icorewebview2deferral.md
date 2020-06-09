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
ms.openlocfilehash: 7d21db7c3f0a66f60f32e92b3951151b8d13a002
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698080"
---
# <span data-ttu-id="fdca2-104">интерфейс ICoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="fdca2-104">interface ICoreWebView2Deferral</span></span> 

> [!NOTE]
> <span data-ttu-id="fdca2-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="fdca2-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="fdca2-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="fdca2-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2Deferral
  : public IUnknown
```

<span data-ttu-id="fdca2-107">Этот интерфейс используется для выполнения РБП для аргументов события, которые поддерживают сбор расходов будущих периодов с помощью методаического РБП.</span><span class="sxs-lookup"><span data-stu-id="fdca2-107">This interface is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="fdca2-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="fdca2-108">Summary</span></span>

 <span data-ttu-id="fdca2-109">Участников</span><span class="sxs-lookup"><span data-stu-id="fdca2-109">Members</span></span>                        | <span data-ttu-id="fdca2-110">Описания</span><span class="sxs-lookup"><span data-stu-id="fdca2-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="fdca2-111">Выполнено</span><span class="sxs-lookup"><span data-stu-id="fdca2-111">Complete</span></span>](#complete) | <span data-ttu-id="fdca2-112">Завершает связанное отложенное событие.</span><span class="sxs-lookup"><span data-stu-id="fdca2-112">Completes the associated deferred event.</span></span>

## <span data-ttu-id="fdca2-113">Участников</span><span class="sxs-lookup"><span data-stu-id="fdca2-113">Members</span></span>

#### <span data-ttu-id="fdca2-114">Выполнено</span><span class="sxs-lookup"><span data-stu-id="fdca2-114">Complete</span></span> 

<span data-ttu-id="fdca2-115">Завершает связанное отложенное событие.</span><span class="sxs-lookup"><span data-stu-id="fdca2-115">Completes the associated deferred event.</span></span>

> <span data-ttu-id="fdca2-116">общедоступное значение HRESULT [Complete](#complete)()</span><span class="sxs-lookup"><span data-stu-id="fdca2-116">public HRESULT [Complete](#complete)()</span></span>

<span data-ttu-id="fdca2-117">"Завершить" следует вызывать только один раз для каждого периода отсрочки.</span><span class="sxs-lookup"><span data-stu-id="fdca2-117">Complete should only be called once for each deferral taken.</span></span>

