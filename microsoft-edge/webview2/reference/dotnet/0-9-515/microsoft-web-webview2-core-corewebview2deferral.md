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
ms.openlocfilehash: fec7fd7399222d8223d1022cd1e528bc9ed0d161
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654934"
---
# <span data-ttu-id="3589d-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="3589d-104">Microsoft.Web.WebView2.Core.CoreWebView2Deferral class</span></span> 

<span data-ttu-id="3589d-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="3589d-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="3589d-106">Сборка: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="3589d-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="3589d-107">Этот класс используется для выполнения РБП для аргументов события, которые поддерживают сбор расходов будущих периодов с помощью методаического РБП.</span><span class="sxs-lookup"><span data-stu-id="3589d-107">This class is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="3589d-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="3589d-108">Summary</span></span>

 <span data-ttu-id="3589d-109">Участников</span><span class="sxs-lookup"><span data-stu-id="3589d-109">Members</span></span>                        | <span data-ttu-id="3589d-110">Описания</span><span class="sxs-lookup"><span data-stu-id="3589d-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3589d-111">Выполнено</span><span class="sxs-lookup"><span data-stu-id="3589d-111">Complete</span></span>](#complete) | <span data-ttu-id="3589d-112">Завершает связанное отложенное событие.</span><span class="sxs-lookup"><span data-stu-id="3589d-112">Completes the associated deferred event.</span></span>

## <span data-ttu-id="3589d-113">Участников</span><span class="sxs-lookup"><span data-stu-id="3589d-113">Members</span></span>

#### <span data-ttu-id="3589d-114">Выполнено</span><span class="sxs-lookup"><span data-stu-id="3589d-114">Complete</span></span> 

<span data-ttu-id="3589d-115">Завершает связанное отложенное событие.</span><span class="sxs-lookup"><span data-stu-id="3589d-115">Completes the associated deferred event.</span></span>

> <span data-ttu-id="3589d-116">общедоступный void [Complete](#complete)()</span><span class="sxs-lookup"><span data-stu-id="3589d-116">public void [Complete](#complete)()</span></span>

<span data-ttu-id="3589d-117">"Завершить" следует вызывать только один раз для каждого периода отсрочки.</span><span class="sxs-lookup"><span data-stu-id="3589d-117">Complete should only be called once for each deferral taken.</span></span>

