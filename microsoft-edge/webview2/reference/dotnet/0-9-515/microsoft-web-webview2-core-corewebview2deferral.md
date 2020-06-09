---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: bf198781d67761e9d6c29ee9c6a274462e92a61d
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697674"
---
# <span data-ttu-id="009db-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="009db-104">Microsoft.Web.WebView2.Core.CoreWebView2Deferral class</span></span> 

> [!NOTE]
> <span data-ttu-id="009db-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="009db-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="009db-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="009db-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="009db-107">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="009db-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="009db-108">Сборка: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="009db-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="009db-109">Этот класс используется для выполнения РБП для аргументов события, которые поддерживают сбор расходов будущих периодов с помощью методаического РБП.</span><span class="sxs-lookup"><span data-stu-id="009db-109">This class is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="009db-110">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="009db-110">Summary</span></span>

 <span data-ttu-id="009db-111">Участников</span><span class="sxs-lookup"><span data-stu-id="009db-111">Members</span></span>                        | <span data-ttu-id="009db-112">Описания</span><span class="sxs-lookup"><span data-stu-id="009db-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="009db-113">Выполнено</span><span class="sxs-lookup"><span data-stu-id="009db-113">Complete</span></span>](#complete) | <span data-ttu-id="009db-114">Завершает связанное отложенное событие.</span><span class="sxs-lookup"><span data-stu-id="009db-114">Completes the associated deferred event.</span></span>

## <span data-ttu-id="009db-115">Участников</span><span class="sxs-lookup"><span data-stu-id="009db-115">Members</span></span>

#### <span data-ttu-id="009db-116">Выполнено</span><span class="sxs-lookup"><span data-stu-id="009db-116">Complete</span></span> 

<span data-ttu-id="009db-117">Завершает связанное отложенное событие.</span><span class="sxs-lookup"><span data-stu-id="009db-117">Completes the associated deferred event.</span></span>

> <span data-ttu-id="009db-118">общедоступный void [Complete](#complete)()</span><span class="sxs-lookup"><span data-stu-id="009db-118">public void [Complete](#complete)()</span></span>

<span data-ttu-id="009db-119">"Завершить" следует вызывать только один раз для каждого периода отсрочки.</span><span class="sxs-lookup"><span data-stu-id="009db-119">Complete should only be called once for each deferral taken.</span></span>

