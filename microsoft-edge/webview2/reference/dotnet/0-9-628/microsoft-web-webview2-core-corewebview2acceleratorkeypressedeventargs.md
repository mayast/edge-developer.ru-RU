---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2AcceleratorKeyPressedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: 16af4247c494d1d09155110755d7936487f2e84e
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012490"
---
# <span data-ttu-id="8b84f-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2AcceleratorKeyPressedEventArgs</span><span class="sxs-lookup"><span data-stu-id="8b84f-104">Microsoft.Web.WebView2.Core.CoreWebView2AcceleratorKeyPressedEventArgs class</span></span> 

<span data-ttu-id="8b84f-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="8b84f-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="8b84f-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="8b84f-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="8b84f-107">Аргументы события для события AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="8b84f-107">Event args for the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="8b84f-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="8b84f-108">Summary</span></span>

 <span data-ttu-id="8b84f-109">Участников</span><span class="sxs-lookup"><span data-stu-id="8b84f-109">Members</span></span>                        | <span data-ttu-id="8b84f-110">Описания</span><span class="sxs-lookup"><span data-stu-id="8b84f-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8b84f-111">Handled</span><span class="sxs-lookup"><span data-stu-id="8b84f-111">Handled</span></span>](#handled) | <span data-ttu-id="8b84f-112">Во время вызова обработчика AcceleratorKeyPressedEvent WebView блокируется, ожидая решения, если ускоритель будет обрабатываться хостом или нет.</span><span class="sxs-lookup"><span data-stu-id="8b84f-112">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>
[<span data-ttu-id="8b84f-113">KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="8b84f-113">KeyEventKind</span></span>](#keyeventkind) | <span data-ttu-id="8b84f-114">Тип события key, который привел к инициированию события.</span><span class="sxs-lookup"><span data-stu-id="8b84f-114">The key event type that caused the event to be fired.</span></span>
[<span data-ttu-id="8b84f-115">KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="8b84f-115">KeyEventLParam</span></span>](#keyeventlparam) | <span data-ttu-id="8b84f-116">Значение LPARAM, сопровождающее сообщение в окне.</span><span class="sxs-lookup"><span data-stu-id="8b84f-116">The LPARAM value that accompanied the window message.</span></span>
[<span data-ttu-id="8b84f-117">PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="8b84f-117">PhysicalKeyStatus</span></span>](#physicalkeystatus) | <span data-ttu-id="8b84f-118">Структура, представляющая данные, передаваемые в отношении LPARAM сообщения окна.</span><span class="sxs-lookup"><span data-stu-id="8b84f-118">A structure representing the information passed in the LPARAM of the window message.</span></span>
[<span data-ttu-id="8b84f-119">VirtualKey</span><span class="sxs-lookup"><span data-stu-id="8b84f-119">VirtualKey</span></span>](#virtualkey) | <span data-ttu-id="8b84f-120">Виртуальный код клавиши Win32 клавиши, которая была нажата или отпущена.</span><span class="sxs-lookup"><span data-stu-id="8b84f-120">The Win32 virtual key code of the key that was pressed or released.</span></span>

## <span data-ttu-id="8b84f-121">Участников</span><span class="sxs-lookup"><span data-stu-id="8b84f-121">Members</span></span>

#### <span data-ttu-id="8b84f-122">Handled</span><span class="sxs-lookup"><span data-stu-id="8b84f-122">Handled</span></span> 

<span data-ttu-id="8b84f-123">Во время вызова обработчика AcceleratorKeyPressedEvent WebView блокируется, ожидая решения, если ускоритель будет обрабатываться хостом или нет.</span><span class="sxs-lookup"><span data-stu-id="8b84f-123">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>

> <span data-ttu-id="8b84f-124">общедоступный логический том [обработан](#handled)</span><span class="sxs-lookup"><span data-stu-id="8b84f-124">public bool [Handled](#handled)</span></span>

<span data-ttu-id="8b84f-125">Если для свойства Handled установлено значение TRUE, это не позволит WebView выполнить действие по умолчанию для этого ключа ускорителя.</span><span class="sxs-lookup"><span data-stu-id="8b84f-125">If the Handled property is set to TRUE then this will prevent the WebView from performing the default action for this accelerator key.</span></span> <span data-ttu-id="8b84f-126">В противном случае WebView выполнит действие по умолчанию для сочетания клавиш.</span><span class="sxs-lookup"><span data-stu-id="8b84f-126">Otherwise the WebView will perform the default action for the accelerator key.</span></span>

#### <span data-ttu-id="8b84f-127">KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="8b84f-127">KeyEventKind</span></span> 

<span data-ttu-id="8b84f-128">Тип события key, который привел к инициированию события.</span><span class="sxs-lookup"><span data-stu-id="8b84f-128">The key event type that caused the event to be fired.</span></span>

> <span data-ttu-id="8b84f-129">общедоступная [CoreWebView2KeyEventKind](./namespace-microsoft-web-webview2-core.md) [KeyEventKind](#keyeventkind)</span><span class="sxs-lookup"><span data-stu-id="8b84f-129">public [CoreWebView2KeyEventKind](./namespace-microsoft-web-webview2-core.md) [KeyEventKind](#keyeventkind)</span></span>

#### <span data-ttu-id="8b84f-130">KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="8b84f-130">KeyEventLParam</span></span> 

<span data-ttu-id="8b84f-131">Значение LPARAM, сопровождающее сообщение в окне.</span><span class="sxs-lookup"><span data-stu-id="8b84f-131">The LPARAM value that accompanied the window message.</span></span>

> <span data-ttu-id="8b84f-132">public int [KeyEventLParam](#keyeventlparam)</span><span class="sxs-lookup"><span data-stu-id="8b84f-132">public int [KeyEventLParam](#keyeventlparam)</span></span>

<span data-ttu-id="8b84f-133">Ознакомьтесь с документацией по WM_KEYDOWN и WM_KEYUP сообщениям.</span><span class="sxs-lookup"><span data-stu-id="8b84f-133">See the documentation for the WM_KEYDOWN and WM_KEYUP messages.</span></span>

#### <span data-ttu-id="8b84f-134">PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="8b84f-134">PhysicalKeyStatus</span></span> 

<span data-ttu-id="8b84f-135">Структура, представляющая данные, передаваемые в отношении LPARAM сообщения окна.</span><span class="sxs-lookup"><span data-stu-id="8b84f-135">A structure representing the information passed in the LPARAM of the window message.</span></span>

> <span data-ttu-id="8b84f-136">общедоступная [CoreWebView2PhysicalKeyStatus](microsoft-web-webview2-core-corewebview2physicalkeystatus.md) [PhysicalKeyStatus](#physicalkeystatus)</span><span class="sxs-lookup"><span data-stu-id="8b84f-136">public [CoreWebView2PhysicalKeyStatus](microsoft-web-webview2-core-corewebview2physicalkeystatus.md) [PhysicalKeyStatus](#physicalkeystatus)</span></span>

#### <span data-ttu-id="8b84f-137">VirtualKey</span><span class="sxs-lookup"><span data-stu-id="8b84f-137">VirtualKey</span></span> 

<span data-ttu-id="8b84f-138">Виртуальный код клавиши Win32 клавиши, которая была нажата или отпущена.</span><span class="sxs-lookup"><span data-stu-id="8b84f-138">The Win32 virtual key code of the key that was pressed or released.</span></span>

> <span data-ttu-id="8b84f-139">Открытый uint [VirtualKey](#virtualkey)</span><span class="sxs-lookup"><span data-stu-id="8b84f-139">public uint [VirtualKey](#virtualkey)</span></span>

<span data-ttu-id="8b84f-140">Это одна из констант виртуальной клавиши Win32, например VK_RETURN или значение ASCII (прописная), например "A".</span><span class="sxs-lookup"><span data-stu-id="8b84f-140">This will be one of the Win32 virtual key constants such as VK_RETURN or an (uppercase) ASCII value such as 'A'.</span></span> <span data-ttu-id="8b84f-141">Вы можете проверить, нажаты ли клавиши CTRL или ALT, вызвав GetKeyState (VK_CONTROL) или GetKeyState (VK_MENU).</span><span class="sxs-lookup"><span data-stu-id="8b84f-141">You can check whether Ctrl or Alt are pressed by calling GetKeyState(VK_CONTROL) or GetKeyState(VK_MENU).</span></span>

