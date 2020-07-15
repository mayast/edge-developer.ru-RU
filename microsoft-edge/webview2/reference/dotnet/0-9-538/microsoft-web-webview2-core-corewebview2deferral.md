---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: 77a3540a64c9894f10cb0c03998dafda90e4f15b
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878934"
---
# <span data-ttu-id="6f2e7-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="6f2e7-104">Microsoft.Web.WebView2.Core.CoreWebView2Deferral class</span></span> 

<span data-ttu-id="6f2e7-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="6f2e7-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="6f2e7-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="6f2e7-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="6f2e7-107">Этот класс используется для выполнения РБП для аргументов события, которые поддерживают сбор расходов будущих периодов с помощью методаического РБП.</span><span class="sxs-lookup"><span data-stu-id="6f2e7-107">This class is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="6f2e7-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="6f2e7-108">Summary</span></span>

 <span data-ttu-id="6f2e7-109">Участников</span><span class="sxs-lookup"><span data-stu-id="6f2e7-109">Members</span></span>                        | <span data-ttu-id="6f2e7-110">Описания</span><span class="sxs-lookup"><span data-stu-id="6f2e7-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6f2e7-111">Выполнено</span><span class="sxs-lookup"><span data-stu-id="6f2e7-111">Complete</span></span>](#complete) | <span data-ttu-id="6f2e7-112">Завершает связанное отложенное событие.</span><span class="sxs-lookup"><span data-stu-id="6f2e7-112">Completes the associated deferred event.</span></span>

## <span data-ttu-id="6f2e7-113">Участников</span><span class="sxs-lookup"><span data-stu-id="6f2e7-113">Members</span></span>

#### <span data-ttu-id="6f2e7-114">Выполнено</span><span class="sxs-lookup"><span data-stu-id="6f2e7-114">Complete</span></span> 

<span data-ttu-id="6f2e7-115">Завершает связанное отложенное событие.</span><span class="sxs-lookup"><span data-stu-id="6f2e7-115">Completes the associated deferred event.</span></span>

> <span data-ttu-id="6f2e7-116">общедоступный void [Complete](#complete)()</span><span class="sxs-lookup"><span data-stu-id="6f2e7-116">public void [Complete](#complete)()</span></span>

<span data-ttu-id="6f2e7-117">"Завершить" следует вызывать только один раз для каждого периода отсрочки.</span><span class="sxs-lookup"><span data-stu-id="6f2e7-117">Complete should only be called once for each deferral taken.</span></span>

