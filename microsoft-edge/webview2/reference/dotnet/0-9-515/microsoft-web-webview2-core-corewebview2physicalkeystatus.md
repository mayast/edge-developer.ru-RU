---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: da7069fb4dad164720bb697a250a216a0bd452ad
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881202"
---
# <span data-ttu-id="3e3c1-104">Структура 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="3e3c1-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2PhysicalKeyStatus struct</span></span> 

> [!NOTE]
> <span data-ttu-id="3e3c1-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="3e3c1-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="3e3c1-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="3e3c1-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="3e3c1-107">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="3e3c1-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="3e3c1-108">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="3e3c1-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="3e3c1-109">Структура, представляющая данные, Упакованные в LPARAM, предоставленные событию ключа Win32.</span><span class="sxs-lookup"><span data-stu-id="3e3c1-109">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

## <span data-ttu-id="3e3c1-110">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="3e3c1-110">Summary</span></span>

 <span data-ttu-id="3e3c1-111">Участников</span><span class="sxs-lookup"><span data-stu-id="3e3c1-111">Members</span></span>                        | <span data-ttu-id="3e3c1-112">Описания</span><span class="sxs-lookup"><span data-stu-id="3e3c1-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3e3c1-113">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="3e3c1-113">IsExtendedKey</span></span>](#isextendedkey) | <span data-ttu-id="3e3c1-114">Указывает на то, является ли ключ дополнительным ключом.</span><span class="sxs-lookup"><span data-stu-id="3e3c1-114">Indicates whether the key is an extended key.</span></span>
[<span data-ttu-id="3e3c1-115">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="3e3c1-115">IsKeyReleased</span></span>](#iskeyreleased) | <span data-ttu-id="3e3c1-116">Состояние перехода.</span><span class="sxs-lookup"><span data-stu-id="3e3c1-116">The transition state.</span></span>
[<span data-ttu-id="3e3c1-117">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="3e3c1-117">IsMenuKeyDown</span></span>](#ismenukeydown) | <span data-ttu-id="3e3c1-118">Код контекста.</span><span class="sxs-lookup"><span data-stu-id="3e3c1-118">The context code.</span></span>
[<span data-ttu-id="3e3c1-119">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="3e3c1-119">RepeatCount</span></span>](#repeatcount) | <span data-ttu-id="3e3c1-120">Число повторов для текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="3e3c1-120">The repeat count for the current message.</span></span>
[<span data-ttu-id="3e3c1-121">ScanCode</span><span class="sxs-lookup"><span data-stu-id="3e3c1-121">ScanCode</span></span>](#scancode) | <span data-ttu-id="3e3c1-122">Код сканирования.</span><span class="sxs-lookup"><span data-stu-id="3e3c1-122">The scan code.</span></span>
[<span data-ttu-id="3e3c1-123">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="3e3c1-123">WasKeyDown</span></span>](#waskeydown) | <span data-ttu-id="3e3c1-124">Предыдущее состояние ключа.</span><span class="sxs-lookup"><span data-stu-id="3e3c1-124">The previous key state.</span></span>

<span data-ttu-id="3e3c1-125">Подробные сведения о WM_KEYDOWN вы увидите в документации по адресу [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown) .</span><span class="sxs-lookup"><span data-stu-id="3e3c1-125">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown).</span></span>

## <span data-ttu-id="3e3c1-126">Участников</span><span class="sxs-lookup"><span data-stu-id="3e3c1-126">Members</span></span>

#### <span data-ttu-id="3e3c1-127">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="3e3c1-127">IsExtendedKey</span></span> 

<span data-ttu-id="3e3c1-128">Указывает на то, является ли ключ дополнительным ключом.</span><span class="sxs-lookup"><span data-stu-id="3e3c1-128">Indicates whether the key is an extended key.</span></span>

> <span data-ttu-id="3e3c1-129">public int [IsExtendedKey](#isextendedkey)</span><span class="sxs-lookup"><span data-stu-id="3e3c1-129">public int [IsExtendedKey](#isextendedkey)</span></span>

#### <span data-ttu-id="3e3c1-130">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="3e3c1-130">IsKeyReleased</span></span> 

<span data-ttu-id="3e3c1-131">Состояние перехода.</span><span class="sxs-lookup"><span data-stu-id="3e3c1-131">The transition state.</span></span>

> <span data-ttu-id="3e3c1-132">public int [IsKeyReleased](#iskeyreleased)</span><span class="sxs-lookup"><span data-stu-id="3e3c1-132">public int [IsKeyReleased](#iskeyreleased)</span></span>

#### <span data-ttu-id="3e3c1-133">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="3e3c1-133">IsMenuKeyDown</span></span> 

<span data-ttu-id="3e3c1-134">Код контекста.</span><span class="sxs-lookup"><span data-stu-id="3e3c1-134">The context code.</span></span>

> <span data-ttu-id="3e3c1-135">public int [IsMenuKeyDown](#ismenukeydown)</span><span class="sxs-lookup"><span data-stu-id="3e3c1-135">public int [IsMenuKeyDown](#ismenukeydown)</span></span>

#### <span data-ttu-id="3e3c1-136">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="3e3c1-136">RepeatCount</span></span> 

<span data-ttu-id="3e3c1-137">Число повторов для текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="3e3c1-137">The repeat count for the current message.</span></span>

> <span data-ttu-id="3e3c1-138">Открытый uint [repeatCount](#repeatcount)</span><span class="sxs-lookup"><span data-stu-id="3e3c1-138">public uint [RepeatCount](#repeatcount)</span></span>

#### <span data-ttu-id="3e3c1-139">ScanCode</span><span class="sxs-lookup"><span data-stu-id="3e3c1-139">ScanCode</span></span> 

<span data-ttu-id="3e3c1-140">Код сканирования.</span><span class="sxs-lookup"><span data-stu-id="3e3c1-140">The scan code.</span></span>

> <span data-ttu-id="3e3c1-141">Открытый uint [ScanCode](#scancode)</span><span class="sxs-lookup"><span data-stu-id="3e3c1-141">public uint [ScanCode](#scancode)</span></span>

#### <span data-ttu-id="3e3c1-142">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="3e3c1-142">WasKeyDown</span></span> 

<span data-ttu-id="3e3c1-143">Предыдущее состояние ключа.</span><span class="sxs-lookup"><span data-stu-id="3e3c1-143">The previous key state.</span></span>

> <span data-ttu-id="3e3c1-144">public int [WasKeyDown](#waskeydown)</span><span class="sxs-lookup"><span data-stu-id="3e3c1-144">public int [WasKeyDown](#waskeydown)</span></span>

