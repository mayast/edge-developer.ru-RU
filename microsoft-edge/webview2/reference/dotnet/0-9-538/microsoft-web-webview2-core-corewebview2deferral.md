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
ms.openlocfilehash: 935e8edb4db54e7bbb707cb2dc704ba312ed3196
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699146"
---
# <span data-ttu-id="45d27-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2Deferral</span><span class="sxs-lookup"><span data-stu-id="45d27-104">Microsoft.Web.WebView2.Core.CoreWebView2Deferral class</span></span> 

<span data-ttu-id="45d27-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="45d27-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="45d27-106">Сборка: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="45d27-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="45d27-107">Этот класс используется для выполнения РБП для аргументов события, которые поддерживают сбор расходов будущих периодов с помощью методаического РБП.</span><span class="sxs-lookup"><span data-stu-id="45d27-107">This class is used to complete deferrals on event args that support getting deferrals via their GetDeferral method.</span></span>

## <span data-ttu-id="45d27-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="45d27-108">Summary</span></span>

 <span data-ttu-id="45d27-109">Участников</span><span class="sxs-lookup"><span data-stu-id="45d27-109">Members</span></span>                        | <span data-ttu-id="45d27-110">Описания</span><span class="sxs-lookup"><span data-stu-id="45d27-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="45d27-111">Выполнено</span><span class="sxs-lookup"><span data-stu-id="45d27-111">Complete</span></span>](#complete) | <span data-ttu-id="45d27-112">Завершает связанное отложенное событие.</span><span class="sxs-lookup"><span data-stu-id="45d27-112">Completes the associated deferred event.</span></span>

## <span data-ttu-id="45d27-113">Участников</span><span class="sxs-lookup"><span data-stu-id="45d27-113">Members</span></span>

#### <span data-ttu-id="45d27-114">Выполнено</span><span class="sxs-lookup"><span data-stu-id="45d27-114">Complete</span></span> 

<span data-ttu-id="45d27-115">Завершает связанное отложенное событие.</span><span class="sxs-lookup"><span data-stu-id="45d27-115">Completes the associated deferred event.</span></span>

> <span data-ttu-id="45d27-116">общедоступный void [Complete](#complete)()</span><span class="sxs-lookup"><span data-stu-id="45d27-116">public void [Complete](#complete)()</span></span>

<span data-ttu-id="45d27-117">"Завершить" следует вызывать только один раз для каждого периода отсрочки.</span><span class="sxs-lookup"><span data-stu-id="45d27-117">Complete should only be called once for each deferral taken.</span></span>

