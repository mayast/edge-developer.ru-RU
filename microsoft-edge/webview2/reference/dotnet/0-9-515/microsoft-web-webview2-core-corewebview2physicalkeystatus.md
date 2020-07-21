---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: eecf4dd59d12c30667defd4e078e8624718bde26
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884591"
---
# <span data-ttu-id="a8837-104">Структура 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="a8837-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2PhysicalKeyStatus struct</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="a8837-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="a8837-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="a8837-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="a8837-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="a8837-107">Структура, представляющая данные, Упакованные в LPARAM, предоставленные событию ключа Win32.</span><span class="sxs-lookup"><span data-stu-id="a8837-107">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

## <span data-ttu-id="a8837-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="a8837-108">Summary</span></span>

 <span data-ttu-id="a8837-109">Участников</span><span class="sxs-lookup"><span data-stu-id="a8837-109">Members</span></span>                        | <span data-ttu-id="a8837-110">Описания</span><span class="sxs-lookup"><span data-stu-id="a8837-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a8837-111">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="a8837-111">IsExtendedKey</span></span>](#isextendedkey) | <span data-ttu-id="a8837-112">Указывает на то, является ли ключ дополнительным ключом.</span><span class="sxs-lookup"><span data-stu-id="a8837-112">Indicates whether the key is an extended key.</span></span>
[<span data-ttu-id="a8837-113">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="a8837-113">IsKeyReleased</span></span>](#iskeyreleased) | <span data-ttu-id="a8837-114">Состояние перехода.</span><span class="sxs-lookup"><span data-stu-id="a8837-114">The transition state.</span></span>
[<span data-ttu-id="a8837-115">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="a8837-115">IsMenuKeyDown</span></span>](#ismenukeydown) | <span data-ttu-id="a8837-116">Код контекста.</span><span class="sxs-lookup"><span data-stu-id="a8837-116">The context code.</span></span>
[<span data-ttu-id="a8837-117">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="a8837-117">RepeatCount</span></span>](#repeatcount) | <span data-ttu-id="a8837-118">Число повторов для текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="a8837-118">The repeat count for the current message.</span></span>
[<span data-ttu-id="a8837-119">ScanCode</span><span class="sxs-lookup"><span data-stu-id="a8837-119">ScanCode</span></span>](#scancode) | <span data-ttu-id="a8837-120">Код сканирования.</span><span class="sxs-lookup"><span data-stu-id="a8837-120">The scan code.</span></span>
[<span data-ttu-id="a8837-121">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="a8837-121">WasKeyDown</span></span>](#waskeydown) | <span data-ttu-id="a8837-122">Предыдущее состояние ключа.</span><span class="sxs-lookup"><span data-stu-id="a8837-122">The previous key state.</span></span>

<span data-ttu-id="a8837-123">Подробные сведения о WM_KEYDOWN вы увидите в документации по адресу [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown) .</span><span class="sxs-lookup"><span data-stu-id="a8837-123">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown).</span></span>

## <span data-ttu-id="a8837-124">Участников</span><span class="sxs-lookup"><span data-stu-id="a8837-124">Members</span></span>

#### <span data-ttu-id="a8837-125">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="a8837-125">IsExtendedKey</span></span> 

<span data-ttu-id="a8837-126">Указывает на то, является ли ключ дополнительным ключом.</span><span class="sxs-lookup"><span data-stu-id="a8837-126">Indicates whether the key is an extended key.</span></span>

> <span data-ttu-id="a8837-127">public int [IsExtendedKey](#isextendedkey)</span><span class="sxs-lookup"><span data-stu-id="a8837-127">public int [IsExtendedKey](#isextendedkey)</span></span>

#### <span data-ttu-id="a8837-128">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="a8837-128">IsKeyReleased</span></span> 

<span data-ttu-id="a8837-129">Состояние перехода.</span><span class="sxs-lookup"><span data-stu-id="a8837-129">The transition state.</span></span>

> <span data-ttu-id="a8837-130">public int [IsKeyReleased](#iskeyreleased)</span><span class="sxs-lookup"><span data-stu-id="a8837-130">public int [IsKeyReleased](#iskeyreleased)</span></span>

#### <span data-ttu-id="a8837-131">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="a8837-131">IsMenuKeyDown</span></span> 

<span data-ttu-id="a8837-132">Код контекста.</span><span class="sxs-lookup"><span data-stu-id="a8837-132">The context code.</span></span>

> <span data-ttu-id="a8837-133">public int [IsMenuKeyDown](#ismenukeydown)</span><span class="sxs-lookup"><span data-stu-id="a8837-133">public int [IsMenuKeyDown](#ismenukeydown)</span></span>

#### <span data-ttu-id="a8837-134">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="a8837-134">RepeatCount</span></span> 

<span data-ttu-id="a8837-135">Число повторов для текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="a8837-135">The repeat count for the current message.</span></span>

> <span data-ttu-id="a8837-136">Открытый uint [repeatCount](#repeatcount)</span><span class="sxs-lookup"><span data-stu-id="a8837-136">public uint [RepeatCount](#repeatcount)</span></span>

#### <span data-ttu-id="a8837-137">ScanCode</span><span class="sxs-lookup"><span data-stu-id="a8837-137">ScanCode</span></span> 

<span data-ttu-id="a8837-138">Код сканирования.</span><span class="sxs-lookup"><span data-stu-id="a8837-138">The scan code.</span></span>

> <span data-ttu-id="a8837-139">Открытый uint [ScanCode](#scancode)</span><span class="sxs-lookup"><span data-stu-id="a8837-139">public uint [ScanCode](#scancode)</span></span>

#### <span data-ttu-id="a8837-140">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="a8837-140">WasKeyDown</span></span> 

<span data-ttu-id="a8837-141">Предыдущее состояние ключа.</span><span class="sxs-lookup"><span data-stu-id="a8837-141">The previous key state.</span></span>

> <span data-ttu-id="a8837-142">public int [WasKeyDown](#waskeydown)</span><span class="sxs-lookup"><span data-stu-id="a8837-142">public int [WasKeyDown](#waskeydown)</span></span>

