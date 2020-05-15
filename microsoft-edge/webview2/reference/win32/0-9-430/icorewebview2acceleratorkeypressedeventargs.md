---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/24/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 1168749b27488831d914a4f64c0830f39d53415f
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655030"
---
# <span data-ttu-id="1c780-104">интерфейс ICoreWebView2AcceleratorKeyPressedEventArgs</span><span class="sxs-lookup"><span data-stu-id="1c780-104">interface ICoreWebView2AcceleratorKeyPressedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="1c780-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="1c780-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="1c780-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="1c780-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2AcceleratorKeyPressedEventArgs
  : public IUnknown
```

<span data-ttu-id="1c780-107">Аргументы события для события AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="1c780-107">Event args for the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="1c780-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="1c780-108">Summary</span></span>

 <span data-ttu-id="1c780-109">Участников</span><span class="sxs-lookup"><span data-stu-id="1c780-109">Members</span></span>                        | <span data-ttu-id="1c780-110">Описания</span><span class="sxs-lookup"><span data-stu-id="1c780-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1c780-111">get_KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="1c780-111">get_KeyEventKind</span></span>](#get_keyeventkind) | <span data-ttu-id="1c780-112">Тип события key, который привел к инициированию события.</span><span class="sxs-lookup"><span data-stu-id="1c780-112">The key event type that caused the event to be fired.</span></span>
[<span data-ttu-id="1c780-113">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="1c780-113">get_VirtualKey</span></span>](#get_virtualkey) | <span data-ttu-id="1c780-114">Виртуальный код клавиши Win32 клавиши, которая была нажата или отпущена.</span><span class="sxs-lookup"><span data-stu-id="1c780-114">The Win32 virtual key code of the key that was pressed or released.</span></span>
[<span data-ttu-id="1c780-115">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="1c780-115">get_KeyEventLParam</span></span>](#get_keyeventlparam) | <span data-ttu-id="1c780-116">Значение LPARAM, сопровождающее сообщение в окне.</span><span class="sxs-lookup"><span data-stu-id="1c780-116">The LPARAM value that accompanied the window message.</span></span>
[<span data-ttu-id="1c780-117">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="1c780-117">get_PhysicalKeyStatus</span></span>](#get_physicalkeystatus) | <span data-ttu-id="1c780-118">Структура, представляющая данные, передаваемые в отношении LPARAM сообщения окна.</span><span class="sxs-lookup"><span data-stu-id="1c780-118">A structure representing the information passed in the LPARAM of the window message.</span></span>
[<span data-ttu-id="1c780-119">get_Handled</span><span class="sxs-lookup"><span data-stu-id="1c780-119">get_Handled</span></span>](#get_handled) | <span data-ttu-id="1c780-120">Во время вызова обработчика AcceleratorKeyPressedEvent WebView блокируется, ожидая решения, если ускоритель будет обрабатываться хостом или нет.</span><span class="sxs-lookup"><span data-stu-id="1c780-120">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>
[<span data-ttu-id="1c780-121">put_Handled</span><span class="sxs-lookup"><span data-stu-id="1c780-121">put_Handled</span></span>](#put_handled) | <span data-ttu-id="1c780-122">Задает свойство Handled.</span><span class="sxs-lookup"><span data-stu-id="1c780-122">Sets the Handled property.</span></span>

## <span data-ttu-id="1c780-123">Участников</span><span class="sxs-lookup"><span data-stu-id="1c780-123">Members</span></span>

#### <span data-ttu-id="1c780-124">get_KeyEventKind</span><span class="sxs-lookup"><span data-stu-id="1c780-124">get_KeyEventKind</span></span> 

<span data-ttu-id="1c780-125">Тип события key, который привел к инициированию события.</span><span class="sxs-lookup"><span data-stu-id="1c780-125">The key event type that caused the event to be fired.</span></span>

> <span data-ttu-id="1c780-126">общедоступные значения HRESULT [get_KeyEventKind](#get_keyeventkind)(CORE_WEBVIEW2_KEY_EVENT_KIND \* KeyEventKind)</span><span class="sxs-lookup"><span data-stu-id="1c780-126">public HRESULT [get_KeyEventKind](#get_keyeventkind)(CORE_WEBVIEW2_KEY_EVENT_KIND \* keyEventKind)</span></span>

#### <span data-ttu-id="1c780-127">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="1c780-127">get_VirtualKey</span></span> 

<span data-ttu-id="1c780-128">Виртуальный код клавиши Win32 клавиши, которая была нажата или отпущена.</span><span class="sxs-lookup"><span data-stu-id="1c780-128">The Win32 virtual key code of the key that was pressed or released.</span></span>

> <span data-ttu-id="1c780-129">общедоступные значения HRESULT [get_VirtualKey](#get_virtualkey)(uint \* VirtualKey)</span><span class="sxs-lookup"><span data-stu-id="1c780-129">public HRESULT [get_VirtualKey](#get_virtualkey)(UINT \* virtualKey)</span></span>

<span data-ttu-id="1c780-130">Это одна из констант виртуальной клавиши Win32, например VK_RETURN или значение ASCII (прописная), например "A".</span><span class="sxs-lookup"><span data-stu-id="1c780-130">This will be one of the Win32 virtual key constants such as VK_RETURN or an (uppercase) ASCII value such as 'A'.</span></span> <span data-ttu-id="1c780-131">Вы можете проверить, нажаты ли клавиши CTRL или ALT, вызвав GetKeyState (VK_CONTROL) или GetKeyState (VK_MENU).</span><span class="sxs-lookup"><span data-stu-id="1c780-131">You can check whether Ctrl or Alt are pressed by calling GetKeyState(VK_CONTROL) or GetKeyState(VK_MENU).</span></span>

#### <span data-ttu-id="1c780-132">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="1c780-132">get_KeyEventLParam</span></span> 

<span data-ttu-id="1c780-133">Значение LPARAM, сопровождающее сообщение в окне.</span><span class="sxs-lookup"><span data-stu-id="1c780-133">The LPARAM value that accompanied the window message.</span></span>

> <span data-ttu-id="1c780-134">общедоступное значение HRESULT [get_KeyEventLParam](#get_keyeventlparam)(int \* lParam)</span><span class="sxs-lookup"><span data-stu-id="1c780-134">public HRESULT [get_KeyEventLParam](#get_keyeventlparam)(INT \* lParam)</span></span>

<span data-ttu-id="1c780-135">Ознакомьтесь с документацией по WM_KEYDOWN и WM_KEYUP сообщениям.</span><span class="sxs-lookup"><span data-stu-id="1c780-135">See the documentation for the WM_KEYDOWN and WM_KEYUP messages.</span></span>

#### <span data-ttu-id="1c780-136">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="1c780-136">get_PhysicalKeyStatus</span></span> 

<span data-ttu-id="1c780-137">Структура, представляющая данные, передаваемые в отношении LPARAM сообщения окна.</span><span class="sxs-lookup"><span data-stu-id="1c780-137">A structure representing the information passed in the LPARAM of the window message.</span></span>

> <span data-ttu-id="1c780-138">общедоступные значения HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(CORE_WEBVIEW2_PHYSICAL_KEY_STATUS \* PhysicalKeyStatus)</span><span class="sxs-lookup"><span data-stu-id="1c780-138">public HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(CORE_WEBVIEW2_PHYSICAL_KEY_STATUS \* physicalKeyStatus)</span></span>

#### <span data-ttu-id="1c780-139">get_Handled</span><span class="sxs-lookup"><span data-stu-id="1c780-139">get_Handled</span></span> 

<span data-ttu-id="1c780-140">Во время вызова обработчика AcceleratorKeyPressedEvent WebView блокируется, ожидая решения, если ускоритель будет обрабатываться хостом или нет.</span><span class="sxs-lookup"><span data-stu-id="1c780-140">During AcceleratorKeyPressedEvent handler invocation the WebView is blocked waiting for the decision of if the accelerator will be handled by the host or not.</span></span>

> <span data-ttu-id="1c780-141">общедоступные значения HRESULT [get_Handled](#get_handled)(логический \* обработанный)</span><span class="sxs-lookup"><span data-stu-id="1c780-141">public HRESULT [get_Handled](#get_handled)(BOOL \* handled)</span></span>

<span data-ttu-id="1c780-142">Если для свойства Handled установлено значение TRUE, это не позволит WebView выполнить действие по умолчанию для этого ключа ускорителя.</span><span class="sxs-lookup"><span data-stu-id="1c780-142">If the Handled property is set to TRUE then this will prevent the WebView from performing the default action for this accelerator key.</span></span> <span data-ttu-id="1c780-143">В противном случае WebView выполнит действие по умолчанию для сочетания клавиш.</span><span class="sxs-lookup"><span data-stu-id="1c780-143">Otherwise the WebView will perform the default action for the accelerator key.</span></span>

#### <span data-ttu-id="1c780-144">put_Handled</span><span class="sxs-lookup"><span data-stu-id="1c780-144">put_Handled</span></span> 

<span data-ttu-id="1c780-145">Задает свойство Handled.</span><span class="sxs-lookup"><span data-stu-id="1c780-145">Sets the Handled property.</span></span>

> <span data-ttu-id="1c780-146">общедоступные значения HRESULT [put_Handled](#put_handled)(логический параметр обработан)</span><span class="sxs-lookup"><span data-stu-id="1c780-146">public HRESULT [put_Handled](#put_handled)(BOOL handled)</span></span>

