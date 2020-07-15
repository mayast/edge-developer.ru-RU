---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 4df74c4a645b6bfa17228860f627910d374e19c4
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878724"
---
# <span data-ttu-id="86d8e-104">класс 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="86d8e-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2Deferral class</span></span> 

> [!NOTE]
> <span data-ttu-id="86d8e-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="86d8e-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="86d8e-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="86d8e-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="86d8e-107">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="86d8e-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="86d8e-108">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="86d8e-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="86d8e-109">Этот класс используется для выполнения РБП для аргументов события, которые поддерживают сбор расходов будущих периодов с помощью методаического РБП.</span><span class="sxs-lookup"><span data-stu-id="86d8e-109">This class is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="86d8e-110">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="86d8e-110">Summary</span></span>

 <span data-ttu-id="86d8e-111">Участников</span><span class="sxs-lookup"><span data-stu-id="86d8e-111">Members</span></span>                        | <span data-ttu-id="86d8e-112">Описания</span><span class="sxs-lookup"><span data-stu-id="86d8e-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="86d8e-113">Выполнено</span><span class="sxs-lookup"><span data-stu-id="86d8e-113">Complete</span></span>](#complete) | <span data-ttu-id="86d8e-114">Завершает связанное отложенное событие.</span><span class="sxs-lookup"><span data-stu-id="86d8e-114">Completes the associated deferred event.</span></span>

## <span data-ttu-id="86d8e-115">Участников</span><span class="sxs-lookup"><span data-stu-id="86d8e-115">Members</span></span>

#### <span data-ttu-id="86d8e-116">Выполнено</span><span class="sxs-lookup"><span data-stu-id="86d8e-116">Complete</span></span> 

<span data-ttu-id="86d8e-117">Завершает связанное отложенное событие.</span><span class="sxs-lookup"><span data-stu-id="86d8e-117">Completes the associated deferred event.</span></span>

> <span data-ttu-id="86d8e-118">общедоступный void [Complete](#complete)()</span><span class="sxs-lookup"><span data-stu-id="86d8e-118">public void [Complete](#complete)()</span></span>

<span data-ttu-id="86d8e-119">"Завершить" следует вызывать только один раз для каждого периода отсрочки.</span><span class="sxs-lookup"><span data-stu-id="86d8e-119">Complete should only be called once for each deferral taken.</span></span>

