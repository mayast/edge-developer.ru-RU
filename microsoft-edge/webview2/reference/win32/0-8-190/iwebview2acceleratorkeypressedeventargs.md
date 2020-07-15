---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2AcceleratorKeyPressedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 5d052488d23f3d016ba2fd71eb929d5aa2ebea6e
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877366"
---
# <span data-ttu-id="7f7f3-104">0.8.355-Interface IWebView2AcceleratorKeyPressedEventArgs</span><span class="sxs-lookup"><span data-stu-id="7f7f3-104">0.8.355 - interface IWebView2AcceleratorKeyPressedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="7f7f3-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="7f7f3-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="7f7f3-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="7f7f3-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2AcceleratorKeyPressedEventArgs
  : public IUnknown
```

<span data-ttu-id="7f7f3-107">Аргументы события для события AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="7f7f3-107">Event args for the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="7f7f3-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="7f7f3-108">Summary</span></span>

 <span data-ttu-id="7f7f3-109">Участников</span><span class="sxs-lookup"><span data-stu-id="7f7f3-109">Members</span></span>                        | <span data-ttu-id="7f7f3-110">Описания</span><span class="sxs-lookup"><span data-stu-id="7f7f3-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7f7f3-111">get_KeyEventType</span><span class="sxs-lookup"><span data-stu-id="7f7f3-111">get_KeyEventType</span></span>](#get_keyeventtype) | <span data-ttu-id="7f7f3-112">Тип события key, который привел к инициированию события.</span><span class="sxs-lookup"><span data-stu-id="7f7f3-112">The key event type that caused the event to be fired.</span></span>
[<span data-ttu-id="7f7f3-113">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="7f7f3-113">get_VirtualKey</span></span>](#get_virtualkey) | <span data-ttu-id="7f7f3-114">Виртуальный код клавиши Win32 клавиши, которая была нажата или отпущена.</span><span class="sxs-lookup"><span data-stu-id="7f7f3-114">The Win32 virtual key code of the key that was pressed or released.</span></span>
[<span data-ttu-id="7f7f3-115">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="7f7f3-115">get_KeyEventLParam</span></span>](#get_keyeventlparam) | <span data-ttu-id="7f7f3-116">Значение LPARAM, сопровождающее сообщение в окне.</span><span class="sxs-lookup"><span data-stu-id="7f7f3-116">The LPARAM value that accompanied the window message.</span></span>
[<span data-ttu-id="7f7f3-117">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="7f7f3-117">get_PhysicalKeyStatus</span></span>](#get_physicalkeystatus) | <span data-ttu-id="7f7f3-118">Структура, представляющая данные, передаваемые в отношении LPARAM сообщения окна.</span><span class="sxs-lookup"><span data-stu-id="7f7f3-118">A structure representing the information passed in the LPARAM of the window message.</span></span>
[<span data-ttu-id="7f7f3-119">Рабатывайте</span><span class="sxs-lookup"><span data-stu-id="7f7f3-119">Handle</span></span>](#handle) | <span data-ttu-id="7f7f3-120">Вызов этого действия позволит продолжить процесс браузера.</span><span class="sxs-lookup"><span data-stu-id="7f7f3-120">Calling this will allow the browser process to continue.</span></span>

## <span data-ttu-id="7f7f3-121">Участников</span><span class="sxs-lookup"><span data-stu-id="7f7f3-121">Members</span></span>

#### <span data-ttu-id="7f7f3-122">get_KeyEventType</span><span class="sxs-lookup"><span data-stu-id="7f7f3-122">get_KeyEventType</span></span> 

<span data-ttu-id="7f7f3-123">Тип события key, который привел к инициированию события.</span><span class="sxs-lookup"><span data-stu-id="7f7f3-123">The key event type that caused the event to be fired.</span></span>

> <span data-ttu-id="7f7f3-124">общедоступные значения HRESULT [get_KeyEventType](#get_keyeventtype)(WEBVIEW2_KEY_EVENT_TYPE \* KeyEventType)</span><span class="sxs-lookup"><span data-stu-id="7f7f3-124">public HRESULT [get_KeyEventType](#get_keyeventtype)(WEBVIEW2_KEY_EVENT_TYPE \* keyEventType)</span></span>

<span data-ttu-id="7f7f3-125">Это один из WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN, WEBVIEW2_KEY_EVENT_TYPE_KEY_UP, WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN или WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_UP.</span><span class="sxs-lookup"><span data-stu-id="7f7f3-125">This is one of WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN, WEBVIEW2_KEY_EVENT_TYPE_KEY_UP, WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN, or WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_UP.</span></span>

#### <span data-ttu-id="7f7f3-126">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="7f7f3-126">get_VirtualKey</span></span> 

<span data-ttu-id="7f7f3-127">Виртуальный код клавиши Win32 клавиши, которая была нажата или отпущена.</span><span class="sxs-lookup"><span data-stu-id="7f7f3-127">The Win32 virtual key code of the key that was pressed or released.</span></span>

> <span data-ttu-id="7f7f3-128">общедоступные значения HRESULT [get_VirtualKey](#get_virtualkey)(uint \* VirtualKey)</span><span class="sxs-lookup"><span data-stu-id="7f7f3-128">public HRESULT [get_VirtualKey](#get_virtualkey)(UINT \* virtualKey)</span></span>

<span data-ttu-id="7f7f3-129">Это одна из констант виртуальной клавиши Win32, например VK_RETURN или значение ASCII (прописная), например "A".</span><span class="sxs-lookup"><span data-stu-id="7f7f3-129">This will be one of the Win32 virtual key constants such as VK_RETURN or an (uppercase) ASCII value such as 'A'.</span></span> <span data-ttu-id="7f7f3-130">Вы можете проверить, нажаты ли клавиши CTRL или ALT, вызвав GetKeyState (VK_CONTROL) или GetKeyState (VK_MENU).</span><span class="sxs-lookup"><span data-stu-id="7f7f3-130">You can check whether Ctrl or Alt are pressed by calling GetKeyState(VK_CONTROL) or GetKeyState(VK_MENU).</span></span>

#### <span data-ttu-id="7f7f3-131">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="7f7f3-131">get_KeyEventLParam</span></span> 

<span data-ttu-id="7f7f3-132">Значение LPARAM, сопровождающее сообщение в окне.</span><span class="sxs-lookup"><span data-stu-id="7f7f3-132">The LPARAM value that accompanied the window message.</span></span>

> <span data-ttu-id="7f7f3-133">общедоступное значение HRESULT [get_KeyEventLParam](#get_keyeventlparam)(int \* lParam)</span><span class="sxs-lookup"><span data-stu-id="7f7f3-133">public HRESULT [get_KeyEventLParam](#get_keyeventlparam)(INT \* lParam)</span></span>

<span data-ttu-id="7f7f3-134">Ознакомьтесь с документацией по WM_KEYDOWN и WM_KEYUP сообщениям.</span><span class="sxs-lookup"><span data-stu-id="7f7f3-134">See the documentation for the WM_KEYDOWN and WM_KEYUP messages.</span></span>

#### <span data-ttu-id="7f7f3-135">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="7f7f3-135">get_PhysicalKeyStatus</span></span> 

<span data-ttu-id="7f7f3-136">Структура, представляющая данные, передаваемые в отношении LPARAM сообщения окна.</span><span class="sxs-lookup"><span data-stu-id="7f7f3-136">A structure representing the information passed in the LPARAM of the window message.</span></span>

> <span data-ttu-id="7f7f3-137">общедоступные значения HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(WEBVIEW2_PHYSICAL_KEY_STATUS \* PhysicalKeyStatus)</span><span class="sxs-lookup"><span data-stu-id="7f7f3-137">public HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(WEBVIEW2_PHYSICAL_KEY_STATUS \* physicalKeyStatus)</span></span>

#### <span data-ttu-id="7f7f3-138">Рабатывайте</span><span class="sxs-lookup"><span data-stu-id="7f7f3-138">Handle</span></span> 

<span data-ttu-id="7f7f3-139">Вызов этого действия позволит продолжить процесс браузера.</span><span class="sxs-lookup"><span data-stu-id="7f7f3-139">Calling this will allow the browser process to continue.</span></span>

> <span data-ttu-id="7f7f3-140">общедоступный [дескриптор](#handle)HRESULT (обработанные логические значения)</span><span class="sxs-lookup"><span data-stu-id="7f7f3-140">public HRESULT [Handle](#handle)(BOOL handled)</span></span>

<span data-ttu-id="7f7f3-141">Передача значения TRUE не позволит браузеру выполнить действие по умолчанию для этого ключа ускорителя.</span><span class="sxs-lookup"><span data-stu-id="7f7f3-141">Passing TRUE will prevent the browser from performing the default action for this accelerator key.</span></span> <span data-ttu-id="7f7f3-142">Если обработчик событий возвращается без [дескриптора вызова ()](#handle), то он эквивалентен дескриптору вызова (false).</span><span class="sxs-lookup"><span data-stu-id="7f7f3-142">If the event handler returns without calling [Handle()](#handle), it is equivalent to calling Handle(FALSE).</span></span> <span data-ttu-id="7f7f3-143">Вызов [дескриптора ()](#handle) после того, как он уже был вызван, или возвращенный обработчик событий не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="7f7f3-143">Calling [Handle()](#handle) after it has already been called or the event handler has returned will do nothing.</span></span>

