---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2AcceleratorKeyPressedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 885ad6b161fbde6721e1812735ab50d7e0c3e8d9
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885054"
---
# <span data-ttu-id="6e0df-104">0.8.355-Interface IWebView2AcceleratorKeyPressedEventArgs</span><span class="sxs-lookup"><span data-stu-id="6e0df-104">0.8.355 - interface IWebView2AcceleratorKeyPressedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2AcceleratorKeyPressedEventArgs
  : public IUnknown
```

<span data-ttu-id="6e0df-105">Аргументы события для события AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="6e0df-105">Event args for the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="6e0df-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="6e0df-106">Summary</span></span>

 <span data-ttu-id="6e0df-107">Участников</span><span class="sxs-lookup"><span data-stu-id="6e0df-107">Members</span></span>                        | <span data-ttu-id="6e0df-108">Описания</span><span class="sxs-lookup"><span data-stu-id="6e0df-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6e0df-109">get_KeyEventType</span><span class="sxs-lookup"><span data-stu-id="6e0df-109">get_KeyEventType</span></span>](#get_keyeventtype) | <span data-ttu-id="6e0df-110">Тип события key, который привел к инициированию события.</span><span class="sxs-lookup"><span data-stu-id="6e0df-110">The key event type that caused the event to be fired.</span></span>
[<span data-ttu-id="6e0df-111">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="6e0df-111">get_VirtualKey</span></span>](#get_virtualkey) | <span data-ttu-id="6e0df-112">Виртуальный код клавиши Win32 клавиши, которая была нажата или отпущена.</span><span class="sxs-lookup"><span data-stu-id="6e0df-112">The Win32 virtual key code of the key that was pressed or released.</span></span>
[<span data-ttu-id="6e0df-113">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="6e0df-113">get_KeyEventLParam</span></span>](#get_keyeventlparam) | <span data-ttu-id="6e0df-114">Значение LPARAM, сопровождающее сообщение в окне.</span><span class="sxs-lookup"><span data-stu-id="6e0df-114">The LPARAM value that accompanied the window message.</span></span>
[<span data-ttu-id="6e0df-115">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="6e0df-115">get_PhysicalKeyStatus</span></span>](#get_physicalkeystatus) | <span data-ttu-id="6e0df-116">Структура, представляющая данные, передаваемые в отношении LPARAM сообщения окна.</span><span class="sxs-lookup"><span data-stu-id="6e0df-116">A structure representing the information passed in the LPARAM of the window message.</span></span>
[<span data-ttu-id="6e0df-117">Рабатывайте</span><span class="sxs-lookup"><span data-stu-id="6e0df-117">Handle</span></span>](#handle) | <span data-ttu-id="6e0df-118">Вызов этого действия позволит продолжить процесс браузера.</span><span class="sxs-lookup"><span data-stu-id="6e0df-118">Calling this will allow the browser process to continue.</span></span>

## <span data-ttu-id="6e0df-119">Участников</span><span class="sxs-lookup"><span data-stu-id="6e0df-119">Members</span></span>

#### <span data-ttu-id="6e0df-120">get_KeyEventType</span><span class="sxs-lookup"><span data-stu-id="6e0df-120">get_KeyEventType</span></span> 

<span data-ttu-id="6e0df-121">Тип события key, который привел к инициированию события.</span><span class="sxs-lookup"><span data-stu-id="6e0df-121">The key event type that caused the event to be fired.</span></span>

> <span data-ttu-id="6e0df-122">общедоступные значения HRESULT [get_KeyEventType](#get_keyeventtype)(WEBVIEW2_KEY_EVENT_TYPE \* KeyEventType)</span><span class="sxs-lookup"><span data-stu-id="6e0df-122">public HRESULT [get_KeyEventType](#get_keyeventtype)(WEBVIEW2_KEY_EVENT_TYPE \* keyEventType)</span></span>

<span data-ttu-id="6e0df-123">Это один из WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN, WEBVIEW2_KEY_EVENT_TYPE_KEY_UP, WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN или WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_UP.</span><span class="sxs-lookup"><span data-stu-id="6e0df-123">This is one of WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN, WEBVIEW2_KEY_EVENT_TYPE_KEY_UP, WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN, or WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_UP.</span></span>

#### <span data-ttu-id="6e0df-124">get_VirtualKey</span><span class="sxs-lookup"><span data-stu-id="6e0df-124">get_VirtualKey</span></span> 

<span data-ttu-id="6e0df-125">Виртуальный код клавиши Win32 клавиши, которая была нажата или отпущена.</span><span class="sxs-lookup"><span data-stu-id="6e0df-125">The Win32 virtual key code of the key that was pressed or released.</span></span>

> <span data-ttu-id="6e0df-126">общедоступные значения HRESULT [get_VirtualKey](#get_virtualkey)(uint \* VirtualKey)</span><span class="sxs-lookup"><span data-stu-id="6e0df-126">public HRESULT [get_VirtualKey](#get_virtualkey)(UINT \* virtualKey)</span></span>

<span data-ttu-id="6e0df-127">Это одна из констант виртуальной клавиши Win32, например VK_RETURN или значение ASCII (прописная), например "A".</span><span class="sxs-lookup"><span data-stu-id="6e0df-127">This will be one of the Win32 virtual key constants such as VK_RETURN or an (uppercase) ASCII value such as 'A'.</span></span> <span data-ttu-id="6e0df-128">Вы можете проверить, нажаты ли клавиши CTRL или ALT, вызвав GetKeyState (VK_CONTROL) или GetKeyState (VK_MENU).</span><span class="sxs-lookup"><span data-stu-id="6e0df-128">You can check whether Ctrl or Alt are pressed by calling GetKeyState(VK_CONTROL) or GetKeyState(VK_MENU).</span></span>

#### <span data-ttu-id="6e0df-129">get_KeyEventLParam</span><span class="sxs-lookup"><span data-stu-id="6e0df-129">get_KeyEventLParam</span></span> 

<span data-ttu-id="6e0df-130">Значение LPARAM, сопровождающее сообщение в окне.</span><span class="sxs-lookup"><span data-stu-id="6e0df-130">The LPARAM value that accompanied the window message.</span></span>

> <span data-ttu-id="6e0df-131">общедоступное значение HRESULT [get_KeyEventLParam](#get_keyeventlparam)(int \* lParam)</span><span class="sxs-lookup"><span data-stu-id="6e0df-131">public HRESULT [get_KeyEventLParam](#get_keyeventlparam)(INT \* lParam)</span></span>

<span data-ttu-id="6e0df-132">Ознакомьтесь с документацией по WM_KEYDOWN и WM_KEYUP сообщениям.</span><span class="sxs-lookup"><span data-stu-id="6e0df-132">See the documentation for the WM_KEYDOWN and WM_KEYUP messages.</span></span>

#### <span data-ttu-id="6e0df-133">get_PhysicalKeyStatus</span><span class="sxs-lookup"><span data-stu-id="6e0df-133">get_PhysicalKeyStatus</span></span> 

<span data-ttu-id="6e0df-134">Структура, представляющая данные, передаваемые в отношении LPARAM сообщения окна.</span><span class="sxs-lookup"><span data-stu-id="6e0df-134">A structure representing the information passed in the LPARAM of the window message.</span></span>

> <span data-ttu-id="6e0df-135">общедоступные значения HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(WEBVIEW2_PHYSICAL_KEY_STATUS \* PhysicalKeyStatus)</span><span class="sxs-lookup"><span data-stu-id="6e0df-135">public HRESULT [get_PhysicalKeyStatus](#get_physicalkeystatus)(WEBVIEW2_PHYSICAL_KEY_STATUS \* physicalKeyStatus)</span></span>

#### <span data-ttu-id="6e0df-136">Рабатывайте</span><span class="sxs-lookup"><span data-stu-id="6e0df-136">Handle</span></span> 

<span data-ttu-id="6e0df-137">Вызов этого действия позволит продолжить процесс браузера.</span><span class="sxs-lookup"><span data-stu-id="6e0df-137">Calling this will allow the browser process to continue.</span></span>

> <span data-ttu-id="6e0df-138">общедоступный [дескриптор](#handle)HRESULT (обработанные логические значения)</span><span class="sxs-lookup"><span data-stu-id="6e0df-138">public HRESULT [Handle](#handle)(BOOL handled)</span></span>

<span data-ttu-id="6e0df-139">Передача значения TRUE не позволит браузеру выполнить действие по умолчанию для этого ключа ускорителя.</span><span class="sxs-lookup"><span data-stu-id="6e0df-139">Passing TRUE will prevent the browser from performing the default action for this accelerator key.</span></span> <span data-ttu-id="6e0df-140">Если обработчик событий возвращается без [дескриптора вызова ()](#handle), то он эквивалентен дескриптору вызова (false).</span><span class="sxs-lookup"><span data-stu-id="6e0df-140">If the event handler returns without calling [Handle()](#handle), it is equivalent to calling Handle(FALSE).</span></span> <span data-ttu-id="6e0df-141">Вызов [дескриптора ()](#handle) после того, как он уже был вызван, или возвращенный обработчик событий не выполняет никаких действий.</span><span class="sxs-lookup"><span data-stu-id="6e0df-141">Calling [Handle()](#handle) after it has already been called or the event handler has returned will do nothing.</span></span>

