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
ms.openlocfilehash: bd63bda6b7835ff5edb30b8b1b22f877f4c96e14
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697597"
---
# <span data-ttu-id="b2f3e-104">Структура Microsoft. Web. WebView2. Core. CoreWebView2PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="b2f3e-104">Microsoft.Web.WebView2.Core.CoreWebView2PhysicalKeyStatus struct</span></span> 

> [!NOTE]
> <span data-ttu-id="b2f3e-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="b2f3e-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="b2f3e-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="b2f3e-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="b2f3e-107">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="b2f3e-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="b2f3e-108">Сборка: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="b2f3e-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="b2f3e-109">Структура, представляющая данные, Упакованные в LPARAM, предоставленные событию ключа Win32.</span><span class="sxs-lookup"><span data-stu-id="b2f3e-109">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

## <span data-ttu-id="b2f3e-110">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="b2f3e-110">Summary</span></span>

 <span data-ttu-id="b2f3e-111">Участников</span><span class="sxs-lookup"><span data-stu-id="b2f3e-111">Members</span></span>                        | <span data-ttu-id="b2f3e-112">Описания</span><span class="sxs-lookup"><span data-stu-id="b2f3e-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b2f3e-113">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="b2f3e-113">IsExtendedKey</span></span>](#isextendedkey) | <span data-ttu-id="b2f3e-114">Указывает на то, является ли ключ дополнительным ключом.</span><span class="sxs-lookup"><span data-stu-id="b2f3e-114">Indicates whether the key is an extended key.</span></span>
[<span data-ttu-id="b2f3e-115">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="b2f3e-115">IsKeyReleased</span></span>](#iskeyreleased) | <span data-ttu-id="b2f3e-116">Состояние перехода.</span><span class="sxs-lookup"><span data-stu-id="b2f3e-116">The transition state.</span></span>
[<span data-ttu-id="b2f3e-117">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="b2f3e-117">IsMenuKeyDown</span></span>](#ismenukeydown) | <span data-ttu-id="b2f3e-118">Код контекста.</span><span class="sxs-lookup"><span data-stu-id="b2f3e-118">The context code.</span></span>
[<span data-ttu-id="b2f3e-119">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="b2f3e-119">RepeatCount</span></span>](#repeatcount) | <span data-ttu-id="b2f3e-120">Число повторов для текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="b2f3e-120">The repeat count for the current message.</span></span>
[<span data-ttu-id="b2f3e-121">ScanCode</span><span class="sxs-lookup"><span data-stu-id="b2f3e-121">ScanCode</span></span>](#scancode) | <span data-ttu-id="b2f3e-122">Код сканирования.</span><span class="sxs-lookup"><span data-stu-id="b2f3e-122">The scan code.</span></span>
[<span data-ttu-id="b2f3e-123">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="b2f3e-123">WasKeyDown</span></span>](#waskeydown) | <span data-ttu-id="b2f3e-124">Предыдущее состояние ключа.</span><span class="sxs-lookup"><span data-stu-id="b2f3e-124">The previous key state.</span></span>

<span data-ttu-id="b2f3e-125">Подробные сведения о WM_KEYDOWN вы увидите в документации по адресу [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown) .</span><span class="sxs-lookup"><span data-stu-id="b2f3e-125">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown).</span></span>

## <span data-ttu-id="b2f3e-126">Участников</span><span class="sxs-lookup"><span data-stu-id="b2f3e-126">Members</span></span>

#### <span data-ttu-id="b2f3e-127">IsExtendedKey</span><span class="sxs-lookup"><span data-stu-id="b2f3e-127">IsExtendedKey</span></span> 

<span data-ttu-id="b2f3e-128">Указывает на то, является ли ключ дополнительным ключом.</span><span class="sxs-lookup"><span data-stu-id="b2f3e-128">Indicates whether the key is an extended key.</span></span>

> <span data-ttu-id="b2f3e-129">public int [IsExtendedKey](#isextendedkey)</span><span class="sxs-lookup"><span data-stu-id="b2f3e-129">public int [IsExtendedKey](#isextendedkey)</span></span>

#### <span data-ttu-id="b2f3e-130">IsKeyReleased</span><span class="sxs-lookup"><span data-stu-id="b2f3e-130">IsKeyReleased</span></span> 

<span data-ttu-id="b2f3e-131">Состояние перехода.</span><span class="sxs-lookup"><span data-stu-id="b2f3e-131">The transition state.</span></span>

> <span data-ttu-id="b2f3e-132">public int [IsKeyReleased](#iskeyreleased)</span><span class="sxs-lookup"><span data-stu-id="b2f3e-132">public int [IsKeyReleased](#iskeyreleased)</span></span>

#### <span data-ttu-id="b2f3e-133">IsMenuKeyDown</span><span class="sxs-lookup"><span data-stu-id="b2f3e-133">IsMenuKeyDown</span></span> 

<span data-ttu-id="b2f3e-134">Код контекста.</span><span class="sxs-lookup"><span data-stu-id="b2f3e-134">The context code.</span></span>

> <span data-ttu-id="b2f3e-135">public int [IsMenuKeyDown](#ismenukeydown)</span><span class="sxs-lookup"><span data-stu-id="b2f3e-135">public int [IsMenuKeyDown](#ismenukeydown)</span></span>

#### <span data-ttu-id="b2f3e-136">RepeatCount</span><span class="sxs-lookup"><span data-stu-id="b2f3e-136">RepeatCount</span></span> 

<span data-ttu-id="b2f3e-137">Число повторов для текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="b2f3e-137">The repeat count for the current message.</span></span>

> <span data-ttu-id="b2f3e-138">Открытый uint [repeatCount](#repeatcount)</span><span class="sxs-lookup"><span data-stu-id="b2f3e-138">public uint [RepeatCount](#repeatcount)</span></span>

#### <span data-ttu-id="b2f3e-139">ScanCode</span><span class="sxs-lookup"><span data-stu-id="b2f3e-139">ScanCode</span></span> 

<span data-ttu-id="b2f3e-140">Код сканирования.</span><span class="sxs-lookup"><span data-stu-id="b2f3e-140">The scan code.</span></span>

> <span data-ttu-id="b2f3e-141">Открытый uint [ScanCode](#scancode)</span><span class="sxs-lookup"><span data-stu-id="b2f3e-141">public uint [ScanCode](#scancode)</span></span>

#### <span data-ttu-id="b2f3e-142">WasKeyDown</span><span class="sxs-lookup"><span data-stu-id="b2f3e-142">WasKeyDown</span></span> 

<span data-ttu-id="b2f3e-143">Предыдущее состояние ключа.</span><span class="sxs-lookup"><span data-stu-id="b2f3e-143">The previous key state.</span></span>

> <span data-ttu-id="b2f3e-144">public int [WasKeyDown](#waskeydown)</span><span class="sxs-lookup"><span data-stu-id="b2f3e-144">public int [WasKeyDown](#waskeydown)</span></span>

