---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2Deferral
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 135289994bdfe5481018c479b7a1d9c372ecb256
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885111"
---
# <span data-ttu-id="2cfc9-104">класс 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="2cfc9-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2Deferral class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="2cfc9-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="2cfc9-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="2cfc9-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="2cfc9-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="2cfc9-107">Этот класс используется для выполнения РБП для аргументов события, которые поддерживают сбор расходов будущих периодов с помощью методаического РБП.</span><span class="sxs-lookup"><span data-stu-id="2cfc9-107">This class is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="2cfc9-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="2cfc9-108">Summary</span></span>

 <span data-ttu-id="2cfc9-109">Участников</span><span class="sxs-lookup"><span data-stu-id="2cfc9-109">Members</span></span>                        | <span data-ttu-id="2cfc9-110">Описания</span><span class="sxs-lookup"><span data-stu-id="2cfc9-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2cfc9-111">Выполнено</span><span class="sxs-lookup"><span data-stu-id="2cfc9-111">Complete</span></span>](#complete) | <span data-ttu-id="2cfc9-112">Завершает связанное отложенное событие.</span><span class="sxs-lookup"><span data-stu-id="2cfc9-112">Completes the associated deferred event.</span></span>

## <span data-ttu-id="2cfc9-113">Участников</span><span class="sxs-lookup"><span data-stu-id="2cfc9-113">Members</span></span>

#### <span data-ttu-id="2cfc9-114">Выполнено</span><span class="sxs-lookup"><span data-stu-id="2cfc9-114">Complete</span></span> 

<span data-ttu-id="2cfc9-115">Завершает связанное отложенное событие.</span><span class="sxs-lookup"><span data-stu-id="2cfc9-115">Completes the associated deferred event.</span></span>

> <span data-ttu-id="2cfc9-116">общедоступный void [Complete](#complete)()</span><span class="sxs-lookup"><span data-stu-id="2cfc9-116">public void [Complete](#complete)()</span></span>

<span data-ttu-id="2cfc9-117">"Завершить" следует вызывать только один раз для каждого периода отсрочки.</span><span class="sxs-lookup"><span data-stu-id="2cfc9-117">Complete should only be called once for each deferral taken.</span></span>

