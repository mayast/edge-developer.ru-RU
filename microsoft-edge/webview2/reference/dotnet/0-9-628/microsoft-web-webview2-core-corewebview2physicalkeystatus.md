---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: adecd3b23369935b1dc5729e894eaf1c295a06d3
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012444"
---
# <span data-ttu-id="8a394-104">Структура Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="8a394-104">Microsoft.Web.WebView2.Core.CoreWebView2PhysicalKeyStatus struct</span></span> 

<span data-ttu-id="8a394-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="8a394-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="8a394-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="8a394-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="8a394-107">Структура, представляющая данные, Упакованные в LPARAM, предоставленные событию ключа Win32.</span><span class="sxs-lookup"><span data-stu-id="8a394-107">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

## <span data-ttu-id="8a394-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="8a394-108">Summary</span></span>

 <span data-ttu-id="8a394-109">Участников</span><span class="sxs-lookup"><span data-stu-id="8a394-109">Members</span></span>                        | <span data-ttu-id="8a394-110">Описания</span><span class="sxs-lookup"><span data-stu-id="8a394-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8a394-111">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="8a394-111">IsExtendedKey</span></span>](#isextendedkey) | <span data-ttu-id="8a394-112">Указывает на то, является ли ключ дополнительным ключом.</span><span class="sxs-lookup"><span data-stu-id="8a394-112">Indicates whether the key is an extended key.</span></span>
[<span data-ttu-id="8a394-113">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="8a394-113">IsKeyReleased</span></span>](#iskeyreleased) | <span data-ttu-id="8a394-114">Состояние перехода.</span><span class="sxs-lookup"><span data-stu-id="8a394-114">The transition state.</span></span>
[<span data-ttu-id="8a394-115">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="8a394-115">IsMenuKeyDown</span></span>](#ismenukeydown) | <span data-ttu-id="8a394-116">Код контекста.</span><span class="sxs-lookup"><span data-stu-id="8a394-116">The context code.</span></span>
[<span data-ttu-id="8a394-117">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="8a394-117">RepeatCount</span></span>](#repeatcount) | <span data-ttu-id="8a394-118">Число повторов для текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="8a394-118">The repeat count for the current message.</span></span>
[<span data-ttu-id="8a394-119">ScanCode</span><span class="sxs-lookup"><span data-stu-id="8a394-119">ScanCode</span></span>](#scancode) | <span data-ttu-id="8a394-120">Код сканирования.</span><span class="sxs-lookup"><span data-stu-id="8a394-120">The scan code.</span></span>
[<span data-ttu-id="8a394-121">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="8a394-121">WasKeyDown</span></span>](#waskeydown) | <span data-ttu-id="8a394-122">Предыдущее состояние ключа.</span><span class="sxs-lookup"><span data-stu-id="8a394-122">The previous key state.</span></span>

<span data-ttu-id="8a394-123">Подробные сведения о WM_KEYDOWN вы увидите в документации по адресу [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown) .</span><span class="sxs-lookup"><span data-stu-id="8a394-123">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown).</span></span>

## <span data-ttu-id="8a394-124">Участников</span><span class="sxs-lookup"><span data-stu-id="8a394-124">Members</span></span>

#### <span data-ttu-id="8a394-125">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="8a394-125">IsExtendedKey</span></span> 

<span data-ttu-id="8a394-126">Указывает на то, является ли ключ дополнительным ключом.</span><span class="sxs-lookup"><span data-stu-id="8a394-126">Indicates whether the key is an extended key.</span></span>

> <span data-ttu-id="8a394-127">public int [IsExtendedKey](#isextendedkey)</span><span class="sxs-lookup"><span data-stu-id="8a394-127">public int [IsExtendedKey](#isextendedkey)</span></span>

#### <span data-ttu-id="8a394-128">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="8a394-128">IsKeyReleased</span></span> 

<span data-ttu-id="8a394-129">Состояние перехода.</span><span class="sxs-lookup"><span data-stu-id="8a394-129">The transition state.</span></span>

> <span data-ttu-id="8a394-130">public int [IsKeyReleased](#iskeyreleased)</span><span class="sxs-lookup"><span data-stu-id="8a394-130">public int [IsKeyReleased](#iskeyreleased)</span></span>

#### <span data-ttu-id="8a394-131">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="8a394-131">IsMenuKeyDown</span></span> 

<span data-ttu-id="8a394-132">Код контекста.</span><span class="sxs-lookup"><span data-stu-id="8a394-132">The context code.</span></span>

> <span data-ttu-id="8a394-133">public int [IsMenuKeyDown](#ismenukeydown)</span><span class="sxs-lookup"><span data-stu-id="8a394-133">public int [IsMenuKeyDown](#ismenukeydown)</span></span>

#### <span data-ttu-id="8a394-134">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="8a394-134">RepeatCount</span></span> 

<span data-ttu-id="8a394-135">Число повторов для текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="8a394-135">The repeat count for the current message.</span></span>

> <span data-ttu-id="8a394-136">Открытый uint [repeatCount](#repeatcount)</span><span class="sxs-lookup"><span data-stu-id="8a394-136">public uint [RepeatCount](#repeatcount)</span></span>

#### <span data-ttu-id="8a394-137">ScanCode</span><span class="sxs-lookup"><span data-stu-id="8a394-137">ScanCode</span></span> 

<span data-ttu-id="8a394-138">Код сканирования.</span><span class="sxs-lookup"><span data-stu-id="8a394-138">The scan code.</span></span>

> <span data-ttu-id="8a394-139">Открытый uint [ScanCode](#scancode)</span><span class="sxs-lookup"><span data-stu-id="8a394-139">public uint [ScanCode](#scancode)</span></span>

#### <span data-ttu-id="8a394-140">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="8a394-140">WasKeyDown</span></span> 

<span data-ttu-id="8a394-141">Предыдущее состояние ключа.</span><span class="sxs-lookup"><span data-stu-id="8a394-141">The previous key state.</span></span>

> <span data-ttu-id="8a394-142">public int [WasKeyDown](#waskeydown)</span><span class="sxs-lookup"><span data-stu-id="8a394-142">public int [WasKeyDown](#waskeydown)</span></span>

