---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: 280fe2d970d78bf1ea7a79b21f5081510ee27053
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878773"
---
# <span data-ttu-id="71a1e-104">Структура Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="71a1e-104">Microsoft.Web.WebView2.Core.CoreWebView2PhysicalKeyStatus struct</span></span> 

<span data-ttu-id="71a1e-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="71a1e-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="71a1e-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="71a1e-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="71a1e-107">Структура, представляющая данные, Упакованные в LPARAM, предоставленные событию ключа Win32.</span><span class="sxs-lookup"><span data-stu-id="71a1e-107">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

## <span data-ttu-id="71a1e-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="71a1e-108">Summary</span></span>

 <span data-ttu-id="71a1e-109">Участников</span><span class="sxs-lookup"><span data-stu-id="71a1e-109">Members</span></span>                        | <span data-ttu-id="71a1e-110">Описания</span><span class="sxs-lookup"><span data-stu-id="71a1e-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="71a1e-111">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="71a1e-111">IsExtendedKey</span></span>](#isextendedkey) | <span data-ttu-id="71a1e-112">Указывает на то, является ли ключ дополнительным ключом.</span><span class="sxs-lookup"><span data-stu-id="71a1e-112">Indicates whether the key is an extended key.</span></span>
[<span data-ttu-id="71a1e-113">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="71a1e-113">IsKeyReleased</span></span>](#iskeyreleased) | <span data-ttu-id="71a1e-114">Состояние перехода.</span><span class="sxs-lookup"><span data-stu-id="71a1e-114">The transition state.</span></span>
[<span data-ttu-id="71a1e-115">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="71a1e-115">IsMenuKeyDown</span></span>](#ismenukeydown) | <span data-ttu-id="71a1e-116">Код контекста.</span><span class="sxs-lookup"><span data-stu-id="71a1e-116">The context code.</span></span>
[<span data-ttu-id="71a1e-117">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="71a1e-117">RepeatCount</span></span>](#repeatcount) | <span data-ttu-id="71a1e-118">Число повторов для текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="71a1e-118">The repeat count for the current message.</span></span>
[<span data-ttu-id="71a1e-119">ScanCode</span><span class="sxs-lookup"><span data-stu-id="71a1e-119">ScanCode</span></span>](#scancode) | <span data-ttu-id="71a1e-120">Код сканирования.</span><span class="sxs-lookup"><span data-stu-id="71a1e-120">The scan code.</span></span>
[<span data-ttu-id="71a1e-121">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="71a1e-121">WasKeyDown</span></span>](#waskeydown) | <span data-ttu-id="71a1e-122">Предыдущее состояние ключа.</span><span class="sxs-lookup"><span data-stu-id="71a1e-122">The previous key state.</span></span>

<span data-ttu-id="71a1e-123">Подробные сведения о WM_KEYDOWN вы увидите в документации по адресу [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown) .</span><span class="sxs-lookup"><span data-stu-id="71a1e-123">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown).</span></span>

## <span data-ttu-id="71a1e-124">Участников</span><span class="sxs-lookup"><span data-stu-id="71a1e-124">Members</span></span>

#### <span data-ttu-id="71a1e-125">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="71a1e-125">IsExtendedKey</span></span> 

<span data-ttu-id="71a1e-126">Указывает на то, является ли ключ дополнительным ключом.</span><span class="sxs-lookup"><span data-stu-id="71a1e-126">Indicates whether the key is an extended key.</span></span>

> <span data-ttu-id="71a1e-127">public int [IsExtendedKey](#isextendedkey)</span><span class="sxs-lookup"><span data-stu-id="71a1e-127">public int [IsExtendedKey](#isextendedkey)</span></span>

#### <span data-ttu-id="71a1e-128">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="71a1e-128">IsKeyReleased</span></span> 

<span data-ttu-id="71a1e-129">Состояние перехода.</span><span class="sxs-lookup"><span data-stu-id="71a1e-129">The transition state.</span></span>

> <span data-ttu-id="71a1e-130">public int [IsKeyReleased](#iskeyreleased)</span><span class="sxs-lookup"><span data-stu-id="71a1e-130">public int [IsKeyReleased](#iskeyreleased)</span></span>

#### <span data-ttu-id="71a1e-131">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="71a1e-131">IsMenuKeyDown</span></span> 

<span data-ttu-id="71a1e-132">Код контекста.</span><span class="sxs-lookup"><span data-stu-id="71a1e-132">The context code.</span></span>

> <span data-ttu-id="71a1e-133">public int [IsMenuKeyDown](#ismenukeydown)</span><span class="sxs-lookup"><span data-stu-id="71a1e-133">public int [IsMenuKeyDown](#ismenukeydown)</span></span>

#### <span data-ttu-id="71a1e-134">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="71a1e-134">RepeatCount</span></span> 

<span data-ttu-id="71a1e-135">Число повторов для текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="71a1e-135">The repeat count for the current message.</span></span>

> <span data-ttu-id="71a1e-136">Открытый uint [repeatCount](#repeatcount)</span><span class="sxs-lookup"><span data-stu-id="71a1e-136">public uint [RepeatCount](#repeatcount)</span></span>

#### <span data-ttu-id="71a1e-137">ScanCode</span><span class="sxs-lookup"><span data-stu-id="71a1e-137">ScanCode</span></span> 

<span data-ttu-id="71a1e-138">Код сканирования.</span><span class="sxs-lookup"><span data-stu-id="71a1e-138">The scan code.</span></span>

> <span data-ttu-id="71a1e-139">Открытый uint [ScanCode](#scancode)</span><span class="sxs-lookup"><span data-stu-id="71a1e-139">public uint [ScanCode](#scancode)</span></span>

#### <span data-ttu-id="71a1e-140">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="71a1e-140">WasKeyDown</span></span> 

<span data-ttu-id="71a1e-141">Предыдущее состояние ключа.</span><span class="sxs-lookup"><span data-stu-id="71a1e-141">The previous key state.</span></span>

> <span data-ttu-id="71a1e-142">public int [WasKeyDown](#waskeydown)</span><span class="sxs-lookup"><span data-stu-id="71a1e-142">public int [WasKeyDown](#waskeydown)</span></span>

