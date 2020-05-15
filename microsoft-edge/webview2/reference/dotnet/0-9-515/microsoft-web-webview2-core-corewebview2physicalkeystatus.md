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
ms.openlocfilehash: 28ed6db251095e2baf6474950c6839dc4a5a8633
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655054"
---
# <span data-ttu-id="074fb-104">Структура Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="074fb-104">Microsoft.Web.WebView2.Core.CoreWebView2PhysicalKeyStatus struct</span></span> 

<span data-ttu-id="074fb-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="074fb-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="074fb-106">Сборка: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="074fb-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="074fb-107">Структура, представляющая данные, Упакованные в LPARAM, предоставленные событию ключа Win32.</span><span class="sxs-lookup"><span data-stu-id="074fb-107">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

## <span data-ttu-id="074fb-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="074fb-108">Summary</span></span>

 <span data-ttu-id="074fb-109">Участников</span><span class="sxs-lookup"><span data-stu-id="074fb-109">Members</span></span>                        | <span data-ttu-id="074fb-110">Описания</span><span class="sxs-lookup"><span data-stu-id="074fb-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="074fb-111">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="074fb-111">IsExtendedKey</span></span>](#isextendedkey) | <span data-ttu-id="074fb-112">Указывает на то, является ли ключ дополнительным ключом.</span><span class="sxs-lookup"><span data-stu-id="074fb-112">Indicates whether the key is an extended key.</span></span>
[<span data-ttu-id="074fb-113">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="074fb-113">IsKeyReleased</span></span>](#iskeyreleased) | <span data-ttu-id="074fb-114">Состояние перехода.</span><span class="sxs-lookup"><span data-stu-id="074fb-114">The transition state.</span></span>
[<span data-ttu-id="074fb-115">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="074fb-115">IsMenuKeyDown</span></span>](#ismenukeydown) | <span data-ttu-id="074fb-116">Код контекста.</span><span class="sxs-lookup"><span data-stu-id="074fb-116">The context code.</span></span>
[<span data-ttu-id="074fb-117">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="074fb-117">RepeatCount</span></span>](#repeatcount) | <span data-ttu-id="074fb-118">Число повторов для текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="074fb-118">The repeat count for the current message.</span></span>
[<span data-ttu-id="074fb-119">ScanCode</span><span class="sxs-lookup"><span data-stu-id="074fb-119">ScanCode</span></span>](#scancode) | <span data-ttu-id="074fb-120">Код сканирования.</span><span class="sxs-lookup"><span data-stu-id="074fb-120">The scan code.</span></span>
[<span data-ttu-id="074fb-121">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="074fb-121">WasKeyDown</span></span>](#waskeydown) | <span data-ttu-id="074fb-122">Предыдущее состояние ключа.</span><span class="sxs-lookup"><span data-stu-id="074fb-122">The previous key state.</span></span>

<span data-ttu-id="074fb-123">Подробные сведения о WM_KEYDOWN вы увидите в документации по адресу [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown) .</span><span class="sxs-lookup"><span data-stu-id="074fb-123">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown).</span></span>

## <span data-ttu-id="074fb-124">Участников</span><span class="sxs-lookup"><span data-stu-id="074fb-124">Members</span></span>

#### <span data-ttu-id="074fb-125">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="074fb-125">IsExtendedKey</span></span> 

<span data-ttu-id="074fb-126">Указывает на то, является ли ключ дополнительным ключом.</span><span class="sxs-lookup"><span data-stu-id="074fb-126">Indicates whether the key is an extended key.</span></span>

> <span data-ttu-id="074fb-127">public int [IsExtendedKey](#isextendedkey)</span><span class="sxs-lookup"><span data-stu-id="074fb-127">public int [IsExtendedKey](#isextendedkey)</span></span>

#### <span data-ttu-id="074fb-128">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="074fb-128">IsKeyReleased</span></span> 

<span data-ttu-id="074fb-129">Состояние перехода.</span><span class="sxs-lookup"><span data-stu-id="074fb-129">The transition state.</span></span>

> <span data-ttu-id="074fb-130">public int [IsKeyReleased](#iskeyreleased)</span><span class="sxs-lookup"><span data-stu-id="074fb-130">public int [IsKeyReleased](#iskeyreleased)</span></span>

#### <span data-ttu-id="074fb-131">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="074fb-131">IsMenuKeyDown</span></span> 

<span data-ttu-id="074fb-132">Код контекста.</span><span class="sxs-lookup"><span data-stu-id="074fb-132">The context code.</span></span>

> <span data-ttu-id="074fb-133">public int [IsMenuKeyDown](#ismenukeydown)</span><span class="sxs-lookup"><span data-stu-id="074fb-133">public int [IsMenuKeyDown](#ismenukeydown)</span></span>

#### <span data-ttu-id="074fb-134">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="074fb-134">RepeatCount</span></span> 

<span data-ttu-id="074fb-135">Число повторов для текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="074fb-135">The repeat count for the current message.</span></span>

> <span data-ttu-id="074fb-136">Открытый uint [repeatCount](#repeatcount)</span><span class="sxs-lookup"><span data-stu-id="074fb-136">public uint [RepeatCount](#repeatcount)</span></span>

#### <span data-ttu-id="074fb-137">ScanCode</span><span class="sxs-lookup"><span data-stu-id="074fb-137">ScanCode</span></span> 

<span data-ttu-id="074fb-138">Код сканирования.</span><span class="sxs-lookup"><span data-stu-id="074fb-138">The scan code.</span></span>

> <span data-ttu-id="074fb-139">Открытый uint [ScanCode](#scancode)</span><span class="sxs-lookup"><span data-stu-id="074fb-139">public uint [ScanCode](#scancode)</span></span>

#### <span data-ttu-id="074fb-140">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="074fb-140">WasKeyDown</span></span> 

<span data-ttu-id="074fb-141">Предыдущее состояние ключа.</span><span class="sxs-lookup"><span data-stu-id="074fb-141">The previous key state.</span></span>

> <span data-ttu-id="074fb-142">public int [WasKeyDown](#waskeydown)</span><span class="sxs-lookup"><span data-stu-id="074fb-142">public int [WasKeyDown](#waskeydown)</span></span>

