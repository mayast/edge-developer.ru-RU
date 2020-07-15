---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2AcceleratorKeyPressedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: ecf68bfc338d06fdd2d1a104126685ca105810b0
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879382"
---
# <span data-ttu-id="e6706-104">класс 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2AcceleratorKeyPressedEventArgs</span><span class="sxs-lookup"><span data-stu-id="e6706-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2AcceleratorKeyPressedEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="e6706-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="e6706-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="e6706-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="e6706-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="e6706-107">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="e6706-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="e6706-108">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="e6706-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="e6706-109">Аргументы события для события AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="e6706-109">Event args for the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="e6706-110">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="e6706-110">Summary</span></span>

 <span data-ttu-id="e6706-111">Участников</span><span class="sxs-lookup"><span data-stu-id="e6706-111">Members</span></span>                        | <span data-ttu-id="e6706-112">Описания</span><span class="sxs-lookup"><span data-stu-id="e6706-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e6706-113">Handled</span><span class="sxs-lookup"><span data-stu-id="e6706-113">Handled</span></span>](#handled) | <span data-ttu-id="e6706-114">Во время вызова обработчика AcceleratorKeyPressedEvent WebView блокируется, ожидая решения, если ускоритель будет обрабатываться хостом или нет.</span><span class="sxs-lookup"><span data-stu-id="e6706-114">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>
[<span data-ttu-id="e6706-115">KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="e6706-115">KeyEventKind</span></span>](#keyeventkind) | <span data-ttu-id="e6706-116">Тип события key, который привел к инициированию события.</span><span class="sxs-lookup"><span data-stu-id="e6706-116">The key event type that caused the event to be fired.</span></span>
[<span data-ttu-id="e6706-117">KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="e6706-117">KeyEventLParam</span></span>](#keyeventlparam) | <span data-ttu-id="e6706-118">Значение LPARAM, сопровождающее сообщение в окне.</span><span class="sxs-lookup"><span data-stu-id="e6706-118">The LPARAM value that accompanied the window message.</span></span>
[<span data-ttu-id="e6706-119">PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="e6706-119">PhysicalKeyStatus</span></span>](#physicalkeystatus) | <span data-ttu-id="e6706-120">Структура, представляющая данные, передаваемые в отношении LPARAM сообщения окна.</span><span class="sxs-lookup"><span data-stu-id="e6706-120">A structure representing the information passed in the LPARAM of the window message.</span></span>
[<span data-ttu-id="e6706-121">VirtualKey</span><span class="sxs-lookup"><span data-stu-id="e6706-121">VirtualKey</span></span>](#virtualkey) | <span data-ttu-id="e6706-122">Виртуальный код клавиши Win32 клавиши, которая была нажата или отпущена.</span><span class="sxs-lookup"><span data-stu-id="e6706-122">The Win32 virtual key code of the key that was pressed or released.</span></span>

## <span data-ttu-id="e6706-123">Участников</span><span class="sxs-lookup"><span data-stu-id="e6706-123">Members</span></span>

#### <span data-ttu-id="e6706-124">Handled</span><span class="sxs-lookup"><span data-stu-id="e6706-124">Handled</span></span> 

<span data-ttu-id="e6706-125">Во время вызова обработчика AcceleratorKeyPressedEvent WebView блокируется, ожидая решения, если ускоритель будет обрабатываться хостом или нет.</span><span class="sxs-lookup"><span data-stu-id="e6706-125">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>

> <span data-ttu-id="e6706-126">общедоступный логический том [обработан](#handled)</span><span class="sxs-lookup"><span data-stu-id="e6706-126">public bool [Handled](#handled)</span></span>

<span data-ttu-id="e6706-127">Если для свойства Handled установлено значение TRUE, это не позволит WebView выполнить действие по умолчанию для этого ключа ускорителя.</span><span class="sxs-lookup"><span data-stu-id="e6706-127">If the Handled property is set to TRUE then this will prevent the WebView from performing the default action for this accelerator key.</span></span> <span data-ttu-id="e6706-128">В противном случае WebView выполнит действие по умолчанию для сочетания клавиш.</span><span class="sxs-lookup"><span data-stu-id="e6706-128">Otherwise the WebView will perform the default action for the accelerator key.</span></span>

#### <span data-ttu-id="e6706-129">KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="e6706-129">KeyEventKind</span></span> 

<span data-ttu-id="e6706-130">Тип события key, который привел к инициированию события.</span><span class="sxs-lookup"><span data-stu-id="e6706-130">The key event type that caused the event to be fired.</span></span>

> <span data-ttu-id="e6706-131">общедоступная [CoreWebView2KeyEventKind](./namespace-microsoft-web-webview2-core.md) [KeyEventKind](#keyeventkind)</span><span class="sxs-lookup"><span data-stu-id="e6706-131">public [CoreWebView2KeyEventKind](./namespace-microsoft-web-webview2-core.md) [KeyEventKind](#keyeventkind)</span></span>

#### <span data-ttu-id="e6706-132">KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="e6706-132">KeyEventLParam</span></span> 

<span data-ttu-id="e6706-133">Значение LPARAM, сопровождающее сообщение в окне.</span><span class="sxs-lookup"><span data-stu-id="e6706-133">The LPARAM value that accompanied the window message.</span></span>

> <span data-ttu-id="e6706-134">public int [KeyEventLParam](#keyeventlparam)</span><span class="sxs-lookup"><span data-stu-id="e6706-134">public int [KeyEventLParam](#keyeventlparam)</span></span>

<span data-ttu-id="e6706-135">Ознакомьтесь с документацией по WM_KEYDOWN и WM_KEYUP сообщениям.</span><span class="sxs-lookup"><span data-stu-id="e6706-135">See the documentation for the WM_KEYDOWN and WM_KEYUP messages.</span></span>

#### <span data-ttu-id="e6706-136">PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="e6706-136">PhysicalKeyStatus</span></span> 

<span data-ttu-id="e6706-137">Структура, представляющая данные, передаваемые в отношении LPARAM сообщения окна.</span><span class="sxs-lookup"><span data-stu-id="e6706-137">A structure representing the information passed in the LPARAM of the window message.</span></span>

> <span data-ttu-id="e6706-138">общедоступная [CoreWebView2PhysicalKeyStatus](microsoft-web-webview2-core-corewebview2physicalkeystatus.md) [PhysicalKeyStatus](#physicalkeystatus)</span><span class="sxs-lookup"><span data-stu-id="e6706-138">public [CoreWebView2PhysicalKeyStatus](microsoft-web-webview2-core-corewebview2physicalkeystatus.md) [PhysicalKeyStatus](#physicalkeystatus)</span></span>

#### <span data-ttu-id="e6706-139">VirtualKey</span><span class="sxs-lookup"><span data-stu-id="e6706-139">VirtualKey</span></span> 

<span data-ttu-id="e6706-140">Виртуальный код клавиши Win32 клавиши, которая была нажата или отпущена.</span><span class="sxs-lookup"><span data-stu-id="e6706-140">The Win32 virtual key code of the key that was pressed or released.</span></span>

> <span data-ttu-id="e6706-141">Открытый uint [VirtualKey](#virtualkey)</span><span class="sxs-lookup"><span data-stu-id="e6706-141">public uint [VirtualKey](#virtualkey)</span></span>

<span data-ttu-id="e6706-142">Это одна из констант виртуальной клавиши Win32, например VK_RETURN или значение ASCII (прописная), например "A".</span><span class="sxs-lookup"><span data-stu-id="e6706-142">This will be one of the Win32 virtual key constants such as VK_RETURN or an (uppercase) ASCII value such as 'A'.</span></span> <span data-ttu-id="e6706-143">Вы можете проверить, нажаты ли клавиши CTRL или ALT, вызвав GetKeyState (VK_CONTROL) или GetKeyState (VK_MENU).</span><span class="sxs-lookup"><span data-stu-id="e6706-143">You can check whether Ctrl or Alt are pressed by calling GetKeyState(VK_CONTROL) or GetKeyState(VK_MENU).</span></span>

