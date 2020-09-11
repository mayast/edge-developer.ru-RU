---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: 62cd86772d45e1bf9eee7d1821a90b723e1af7db
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11011050"
---
# <span data-ttu-id="d8007-104">класс 0.9.579-Microsoft. Web. WebView2. Core. CoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="d8007-104">0.9.579 - Microsoft.Web.WebView2.Core.CoreWebView2Deferral class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="d8007-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="d8007-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="d8007-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="d8007-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="d8007-107">Этот класс используется для выполнения РБП для аргументов события, которые поддерживают сбор расходов будущих периодов с помощью методаического РБП.</span><span class="sxs-lookup"><span data-stu-id="d8007-107">This class is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="d8007-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="d8007-108">Summary</span></span>

 <span data-ttu-id="d8007-109">Участников</span><span class="sxs-lookup"><span data-stu-id="d8007-109">Members</span></span>                        | <span data-ttu-id="d8007-110">Описания</span><span class="sxs-lookup"><span data-stu-id="d8007-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d8007-111">Выполнено</span><span class="sxs-lookup"><span data-stu-id="d8007-111">Complete</span></span>](#complete) | <span data-ttu-id="d8007-112">Завершает связанное отложенное событие.</span><span class="sxs-lookup"><span data-stu-id="d8007-112">Completes the associated deferred event.</span></span>

## <span data-ttu-id="d8007-113">Участников</span><span class="sxs-lookup"><span data-stu-id="d8007-113">Members</span></span>

#### <span data-ttu-id="d8007-114">Выполнено</span><span class="sxs-lookup"><span data-stu-id="d8007-114">Complete</span></span> 

<span data-ttu-id="d8007-115">Завершает связанное отложенное событие.</span><span class="sxs-lookup"><span data-stu-id="d8007-115">Completes the associated deferred event.</span></span>

> <span data-ttu-id="d8007-116">общедоступный void [Complete](#complete)()</span><span class="sxs-lookup"><span data-stu-id="d8007-116">public void [Complete](#complete)()</span></span>

<span data-ttu-id="d8007-117">"Завершить" следует вызывать только один раз для каждого периода отсрочки.</span><span class="sxs-lookup"><span data-stu-id="d8007-117">Complete should only be called once for each deferral taken.</span></span>

