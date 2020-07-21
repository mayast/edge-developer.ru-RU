---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2AcceleratorKeyPressedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 280df2816696ce4abce118976b3eb9abf76267e3
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884416"
---
# <span data-ttu-id="656b0-104">0.9.430-Interface ICoreWebView2AcceleratorKeyPressedEventArgs</span><span class="sxs-lookup"><span data-stu-id="656b0-104">0.9.430 - interface ICoreWebView2AcceleratorKeyPressedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2AcceleratorKeyPressedEventArgs
  : public IUnknown
```

<span data-ttu-id="656b0-105">Аргументы события для события AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="656b0-105">Event args for the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="656b0-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="656b0-106">Summary</span></span>

 <span data-ttu-id="656b0-107">Участников</span><span class="sxs-lookup"><span data-stu-id="656b0-107">Members</span></span>                        | <span data-ttu-id="656b0-108">Описания</span><span class="sxs-lookup"><span data-stu-id="656b0-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="656b0-109">get_KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="656b0-109">get_KeyEventKind</span></span>](#get_keyeventkind) | <span data-ttu-id="656b0-110">Тип события key, который привел к инициированию события.</span><span class="sxs-lookup"><span data-stu-id="656b0-110">The key event type that caused the event to be fired.</span></span>
[<span data-ttu-id="656b0-111">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="656b0-111">get_VirtualKey</span></span>](#get_virtualkey) | <span data-ttu-id="656b0-112">Виртуальный код клавиши Win32 клавиши, которая была нажата или отпущена.</span><span class="sxs-lookup"><span data-stu-id="656b0-112">The Win32 virtual key code of the key that was pressed or released.</span></span>
[<span data-ttu-id="656b0-113">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="656b0-113">get_KeyEventLParam</span></span>](#get_keyeventlparam) | <span data-ttu-id="656b0-114">Значение LPARAM, сопровождающее сообщение в окне.</span><span class="sxs-lookup"><span data-stu-id="656b0-114">The LPARAM value that accompanied the window message.</span></span>
[<span data-ttu-id="656b0-115">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="656b0-115">get_PhysicalKeyStatus</span></span>](#get_physicalkeystatus) | <span data-ttu-id="656b0-116">Структура, представляющая данные, передаваемые в отношении LPARAM сообщения окна.</span><span class="sxs-lookup"><span data-stu-id="656b0-116">A structure representing the information passed in the LPARAM of the window message.</span></span>
[<span data-ttu-id="656b0-117">get_Handled</span><span class="sxs-lookup"><span data-stu-id="656b0-117">get_Handled</span></span>](#get_handled) | <span data-ttu-id="656b0-118">Во время вызова обработчика AcceleratorKeyPressedEvent WebView блокируется, ожидая решения, если ускоритель будет обрабатываться хостом или нет.</span><span class="sxs-lookup"><span data-stu-id="656b0-118">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>
[<span data-ttu-id="656b0-119">put_Handled</span><span class="sxs-lookup"><span data-stu-id="656b0-119">put_Handled</span></span>](#put_handled) | <span data-ttu-id="656b0-120">Задает свойство Handled.</span><span class="sxs-lookup"><span data-stu-id="656b0-120">Sets the Handled property.</span></span>

## <span data-ttu-id="656b0-121">Участников</span><span class="sxs-lookup"><span data-stu-id="656b0-121">Members</span></span>

#### <span data-ttu-id="656b0-122">get_KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="656b0-122">get_KeyEventKind</span></span> 

<span data-ttu-id="656b0-123">Тип события key, который привел к инициированию события.</span><span class="sxs-lookup"><span data-stu-id="656b0-123">The key event type that caused the event to be fired.</span></span>

> <span data-ttu-id="656b0-124">общедоступные значения HRESULT [get_KeyEventKind](#get_keyeventkind)(CORE_WEBVIEW2_KEY_EVENT_KIND \* KeyEventKind)</span><span class="sxs-lookup"><span data-stu-id="656b0-124">public HRESULT [get_KeyEventKind](#get_keyeventkind)(CORE_WEBVIEW2_KEY_EVENT_KIND \* keyEventKind)</span></span>

#### <span data-ttu-id="656b0-125">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="656b0-125">get_VirtualKey</span></span> 

<span data-ttu-id="656b0-126">Виртуальный код клавиши Win32 клавиши, которая была нажата или отпущена.</span><span class="sxs-lookup"><span data-stu-id="656b0-126">The Win32 virtual key code of the key that was pressed or released.</span></span>

> <span data-ttu-id="656b0-127">общедоступные значения HRESULT [get_VirtualKey](#get_virtualkey)(uint \* VirtualKey)</span><span class="sxs-lookup"><span data-stu-id="656b0-127">public HRESULT [get_VirtualKey](#get_virtualkey)(UINT \* virtualKey)</span></span>

<span data-ttu-id="656b0-128">Это одна из констант виртуальной клавиши Win32, например VK_RETURN или значение ASCII (прописная), например "A".</span><span class="sxs-lookup"><span data-stu-id="656b0-128">This will be one of the Win32 virtual key constants such as VK_RETURN or an (uppercase) ASCII value such as 'A'.</span></span> <span data-ttu-id="656b0-129">Вы можете проверить, нажаты ли клавиши CTRL или ALT, вызвав GetKeyState (VK_CONTROL) или GetKeyState (VK_MENU).</span><span class="sxs-lookup"><span data-stu-id="656b0-129">You can check whether Ctrl or Alt are pressed by calling GetKeyState(VK_CONTROL) or GetKeyState(VK_MENU).</span></span>

#### <span data-ttu-id="656b0-130">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="656b0-130">get_KeyEventLParam</span></span> 

<span data-ttu-id="656b0-131">Значение LPARAM, сопровождающее сообщение в окне.</span><span class="sxs-lookup"><span data-stu-id="656b0-131">The LPARAM value that accompanied the window message.</span></span>

> <span data-ttu-id="656b0-132">общедоступное значение HRESULT [get_KeyEventLParam](#get_keyeventlparam)(int \* lParam)</span><span class="sxs-lookup"><span data-stu-id="656b0-132">public HRESULT [get_KeyEventLParam](#get_keyeventlparam)(INT \* lParam)</span></span>

<span data-ttu-id="656b0-133">Ознакомьтесь с документацией по WM_KEYDOWN и WM_KEYUP сообщениям.</span><span class="sxs-lookup"><span data-stu-id="656b0-133">See the documentation for the WM_KEYDOWN and WM_KEYUP messages.</span></span>

#### <span data-ttu-id="656b0-134">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="656b0-134">get_PhysicalKeyStatus</span></span> 

<span data-ttu-id="656b0-135">Структура, представляющая данные, передаваемые в отношении LPARAM сообщения окна.</span><span class="sxs-lookup"><span data-stu-id="656b0-135">A structure representing the information passed in the LPARAM of the window message.</span></span>

> <span data-ttu-id="656b0-136">общедоступные значения HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(CORE_WEBVIEW2_PHYSICAL_KEY_STATUS \* PhysicalKeyStatus)</span><span class="sxs-lookup"><span data-stu-id="656b0-136">public HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(CORE_WEBVIEW2_PHYSICAL_KEY_STATUS \* physicalKeyStatus)</span></span>

#### <span data-ttu-id="656b0-137">get_Handled</span><span class="sxs-lookup"><span data-stu-id="656b0-137">get_Handled</span></span> 

<span data-ttu-id="656b0-138">Во время вызова обработчика AcceleratorKeyPressedEvent WebView блокируется, ожидая решения, если ускоритель будет обрабатываться хостом или нет.</span><span class="sxs-lookup"><span data-stu-id="656b0-138">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>

> <span data-ttu-id="656b0-139">общедоступные значения HRESULT [get_Handled](#get_handled)(логический \* обработанный)</span><span class="sxs-lookup"><span data-stu-id="656b0-139">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

<span data-ttu-id="656b0-140">Если для свойства Handled установлено значение TRUE, это не позволит WebView выполнить действие по умолчанию для этого ключа ускорителя.</span><span class="sxs-lookup"><span data-stu-id="656b0-140">If the Handled property is set to TRUE then this will prevent the WebView from performing the default action for this accelerator key.</span></span> <span data-ttu-id="656b0-141">В противном случае WebView выполнит действие по умолчанию для сочетания клавиш.</span><span class="sxs-lookup"><span data-stu-id="656b0-141">Otherwise the WebView will perform the default action for the accelerator key.</span></span>

#### <span data-ttu-id="656b0-142">put_Handled</span><span class="sxs-lookup"><span data-stu-id="656b0-142">put_Handled</span></span> 

<span data-ttu-id="656b0-143">Задает свойство Handled.</span><span class="sxs-lookup"><span data-stu-id="656b0-143">Sets the Handled property.</span></span>

> <span data-ttu-id="656b0-144">общедоступные значения HRESULT [put_Handled](#put_handled)(логический параметр обработан)</span><span class="sxs-lookup"><span data-stu-id="656b0-144">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

