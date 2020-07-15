---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2Controller
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 8e0f95f8346f4c4b60b6de2676503b79c743afcb
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880824"
---
# <span data-ttu-id="7f92f-104">0.9.515-Interface ICoreWebView2Controller</span><span class="sxs-lookup"><span data-stu-id="7f92f-104">0.9.515 - interface ICoreWebView2Controller</span></span> 

> [!NOTE]
> <span data-ttu-id="7f92f-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="7f92f-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="7f92f-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="7f92f-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2Controller
  : public IUnknown
```

<span data-ttu-id="7f92f-107">Этот интерфейс является владельцем объекта CoreWebView2 и предоставляет поддержку изменения размеров, отображения и скрытия, фокусировки и других функциональных возможностей, связанных с окнами и композицией.</span><span class="sxs-lookup"><span data-stu-id="7f92f-107">This interface is the owner of the CoreWebView2 object, and provides support for resizing, showing and hiding, focusing, and other functionality related to windowing and composition.</span></span>

## <span data-ttu-id="7f92f-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="7f92f-108">Summary</span></span>

 <span data-ttu-id="7f92f-109">Участников</span><span class="sxs-lookup"><span data-stu-id="7f92f-109">Members</span></span>                        | <span data-ttu-id="7f92f-110">Описания</span><span class="sxs-lookup"><span data-stu-id="7f92f-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7f92f-111">add_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="7f92f-111">add_AcceleratorKeyPressed</span></span>](#add_acceleratorkeypressed) | <span data-ttu-id="7f92f-112">Добавьте обработчик событий для события AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="7f92f-112">Add an event handler for the AcceleratorKeyPressed event.</span></span>
[<span data-ttu-id="7f92f-113">add_GotFocus</span><span class="sxs-lookup"><span data-stu-id="7f92f-113">add_GotFocus</span></span>](#add_gotfocus) | <span data-ttu-id="7f92f-114">Добавьте обработчик событий для события GotFocus.</span><span class="sxs-lookup"><span data-stu-id="7f92f-114">Add an event handler for the GotFocus event.</span></span>
[<span data-ttu-id="7f92f-115">add_LostFocus</span><span class="sxs-lookup"><span data-stu-id="7f92f-115">add_LostFocus</span></span>](#add_lostfocus) | <span data-ttu-id="7f92f-116">Добавьте обработчик для события LostFocus.</span><span class="sxs-lookup"><span data-stu-id="7f92f-116">Add an event handler for the LostFocus event.</span></span>
[<span data-ttu-id="7f92f-117">add_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="7f92f-117">add_MoveFocusRequested</span></span>](#add_movefocusrequested) | <span data-ttu-id="7f92f-118">Добавьте обработчик событий для события MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="7f92f-118">Add an event handler for the MoveFocusRequested event.</span></span>
[<span data-ttu-id="7f92f-119">add_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="7f92f-119">add_ZoomFactorChanged</span></span>](#add_zoomfactorchanged) | <span data-ttu-id="7f92f-120">Добавьте обработчик событий для события ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="7f92f-120">Add an event handler for the ZoomFactorChanged event.</span></span>
[<span data-ttu-id="7f92f-121">Close (закрыть)</span><span class="sxs-lookup"><span data-stu-id="7f92f-121">Close</span></span>](#close) | <span data-ttu-id="7f92f-122">Закрывает WebView и очищает основной экземпляр браузера.</span><span class="sxs-lookup"><span data-stu-id="7f92f-122">Closes the WebView and cleans up the underlying browser instance.</span></span>
[<span data-ttu-id="7f92f-123">get_Bounds</span><span class="sxs-lookup"><span data-stu-id="7f92f-123">get_Bounds</span></span>](#get_bounds) | <span data-ttu-id="7f92f-124">Границы WebView.</span><span class="sxs-lookup"><span data-stu-id="7f92f-124">The webview bounds.</span></span>
[<span data-ttu-id="7f92f-125">get_CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="7f92f-125">get_CoreWebView2</span></span>](#get_corewebview2) | <span data-ttu-id="7f92f-126">Возвращает CoreWebView2, связанный с этим CoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="7f92f-126">Gets the CoreWebView2 associated with this CoreWebView2Controller.</span></span>
[<span data-ttu-id="7f92f-127">get_IsVisible</span><span class="sxs-lookup"><span data-stu-id="7f92f-127">get_IsVisible</span></span>](#get_isvisible) | <span data-ttu-id="7f92f-128">Свойство Visible определяет, нужно ли отображать или скрывать WebView.</span><span class="sxs-lookup"><span data-stu-id="7f92f-128">The IsVisible property determines whether to show or hide the webview.</span></span>
[<span data-ttu-id="7f92f-129">get_ParentWindow</span><span class="sxs-lookup"><span data-stu-id="7f92f-129">get_ParentWindow</span></span>](#get_parentwindow) | <span data-ttu-id="7f92f-130">Родительское окно, предоставленное приложением, используемое этим WebView, для отрисовки содержимого.</span><span class="sxs-lookup"><span data-stu-id="7f92f-130">The parent window provided by the app that this WebView is using to render content.</span></span>
[<span data-ttu-id="7f92f-131">get_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="7f92f-131">get_ZoomFactor</span></span>](#get_zoomfactor) | <span data-ttu-id="7f92f-132">Коэффициент масштабирования для WebView.</span><span class="sxs-lookup"><span data-stu-id="7f92f-132">The zoom factor for the WebView.</span></span>
[<span data-ttu-id="7f92f-133">MoveFocus</span><span class="sxs-lookup"><span data-stu-id="7f92f-133">MoveFocus</span></span>](#movefocus) | <span data-ttu-id="7f92f-134">Перемещение фокуса в WebView.</span><span class="sxs-lookup"><span data-stu-id="7f92f-134">Move focus into WebView.</span></span>
[<span data-ttu-id="7f92f-135">NotifyParentWindowPositionChanged</span><span class="sxs-lookup"><span data-stu-id="7f92f-135">NotifyParentWindowPositionChanged</span></span>](#notifyparentwindowpositionchanged) | <span data-ttu-id="7f92f-136">Это уведомление отделено от границ, которые сообщают WebView, что родительский HWND (или любой предк) переместился.</span><span class="sxs-lookup"><span data-stu-id="7f92f-136">This is a notification separate from Bounds that tells WebView its parent (or any ancestor) HWND moved.</span></span>
[<span data-ttu-id="7f92f-137">put_Bounds</span><span class="sxs-lookup"><span data-stu-id="7f92f-137">put_Bounds</span></span>](#put_bounds) | <span data-ttu-id="7f92f-138">Задайте свойство Bounds.</span><span class="sxs-lookup"><span data-stu-id="7f92f-138">Set the Bounds property.</span></span>
[<span data-ttu-id="7f92f-139">put_IsVisible</span><span class="sxs-lookup"><span data-stu-id="7f92f-139">put_IsVisible</span></span>](#put_isvisible) | <span data-ttu-id="7f92f-140">Задайте свойство Visible.</span><span class="sxs-lookup"><span data-stu-id="7f92f-140">Set the IsVisible property.</span></span>
[<span data-ttu-id="7f92f-141">put_ParentWindow</span><span class="sxs-lookup"><span data-stu-id="7f92f-141">put_ParentWindow</span></span>](#put_parentwindow) | <span data-ttu-id="7f92f-142">Установка родительского окна для WebView.</span><span class="sxs-lookup"><span data-stu-id="7f92f-142">Set the parent window for the WebView.</span></span>
[<span data-ttu-id="7f92f-143">put_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="7f92f-143">put_ZoomFactor</span></span>](#put_zoomfactor) | <span data-ttu-id="7f92f-144">Задайте свойство ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="7f92f-144">Set the ZoomFactor property.</span></span>
[<span data-ttu-id="7f92f-145">remove_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="7f92f-145">remove_AcceleratorKeyPressed</span></span>](#remove_acceleratorkeypressed) | <span data-ttu-id="7f92f-146">Удалите обработчик событий, добавленный ранее add_AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="7f92f-146">Remove an event handler previously added with add_AcceleratorKeyPressed.</span></span>
[<span data-ttu-id="7f92f-147">remove_GotFocus</span><span class="sxs-lookup"><span data-stu-id="7f92f-147">remove_GotFocus</span></span>](#remove_gotfocus) | <span data-ttu-id="7f92f-148">Удалите обработчик событий, добавленный ранее add_GotFocus.</span><span class="sxs-lookup"><span data-stu-id="7f92f-148">Remove an event handler previously added with add_GotFocus.</span></span>
[<span data-ttu-id="7f92f-149">remove_LostFocus</span><span class="sxs-lookup"><span data-stu-id="7f92f-149">remove_LostFocus</span></span>](#remove_lostfocus) | <span data-ttu-id="7f92f-150">Удалите обработчик событий, добавленный ранее add_LostFocus.</span><span class="sxs-lookup"><span data-stu-id="7f92f-150">Remove an event handler previously added with add_LostFocus.</span></span>
[<span data-ttu-id="7f92f-151">remove_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="7f92f-151">remove_MoveFocusRequested</span></span>](#remove_movefocusrequested) | <span data-ttu-id="7f92f-152">Удалите обработчик событий, добавленный ранее add_MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="7f92f-152">Remove an event handler previously added with add_MoveFocusRequested.</span></span>
[<span data-ttu-id="7f92f-153">remove_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="7f92f-153">remove_ZoomFactorChanged</span></span>](#remove_zoomfactorchanged) | <span data-ttu-id="7f92f-154">Удалите обработчик событий, добавленный ранее add_ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="7f92f-154">Remove an event handler previously added with add_ZoomFactorChanged.</span></span>
[<span data-ttu-id="7f92f-155">SetBoundsAndZoomFactor</span><span class="sxs-lookup"><span data-stu-id="7f92f-155">SetBoundsAndZoomFactor</span></span>](#setboundsandzoomfactor) | <span data-ttu-id="7f92f-156">Одновременное обновление границ и свойств ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="7f92f-156">Update Bounds and ZoomFactor properties at the same time.</span></span>

<span data-ttu-id="7f92f-157">CoreWebView2Controller владеет CoreWebView2 и, если все ссылки на CoreWebView2Controller выходит из него, WebView будет закрыт.</span><span class="sxs-lookup"><span data-stu-id="7f92f-157">The CoreWebView2Controller owns the CoreWebView2, and if all references to the CoreWebView2Controller go away, the WebView will be closed.</span></span>

## <span data-ttu-id="7f92f-158">Участников</span><span class="sxs-lookup"><span data-stu-id="7f92f-158">Members</span></span>

#### <span data-ttu-id="7f92f-159">add_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="7f92f-159">add_AcceleratorKeyPressed</span></span> 

<span data-ttu-id="7f92f-160">Добавьте обработчик событий для события AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="7f92f-160">Add an event handler for the AcceleratorKeyPressed event.</span></span>

> <span data-ttu-id="7f92f-161">общедоступные значения HRESULT [add_AcceleratorKeyPressed](#add_acceleratorkeypressed)([ICoreWebView2AcceleratorKeyPressedEventHandler](icorewebview2acceleratorkeypressedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="7f92f-161">public HRESULT [add_AcceleratorKeyPressed](#add_acceleratorkeypressed)([ICoreWebView2AcceleratorKeyPressedEventHandler](icorewebview2acceleratorkeypressedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="7f92f-162">AcceleratorKeyPressed активируется при нажатии или отпускании клавиши сочетания клавиш в том случае, если WebView имеет фокус.</span><span class="sxs-lookup"><span data-stu-id="7f92f-162">AcceleratorKeyPressed fires when an accelerator key or key combo is pressed or released while the WebView is focused.</span></span> <span data-ttu-id="7f92f-163">Клавиша считается ускорителем по одной из следующих способов:</span><span class="sxs-lookup"><span data-stu-id="7f92f-163">A key is considered an accelerator if either:</span></span>

1. <span data-ttu-id="7f92f-164">В данный момент удерживается клавиша CTRL или ALT;</span><span class="sxs-lookup"><span data-stu-id="7f92f-164">Ctrl or Alt is currently being held, or</span></span>

1. <span data-ttu-id="7f92f-165">Нажатая клавиша не сопоставляется с символом.</span><span class="sxs-lookup"><span data-stu-id="7f92f-165">the pressed key does not map to a character.</span></span> <span data-ttu-id="7f92f-166">Некоторые неопределенные клавиши никогда не рассматриваются как ускорители, например Shift.</span><span class="sxs-lookup"><span data-stu-id="7f92f-166">A few specific keys are never considered accelerators, such as Shift.</span></span> <span data-ttu-id="7f92f-167">Клавиша ESC всегда считается ускорителем.</span><span class="sxs-lookup"><span data-stu-id="7f92f-167">The Escape key is always considered an accelerator.</span></span>

<span data-ttu-id="7f92f-168">Событие с автоматическим нажатием клавиши, вызванное удерживанием нажатой клавиши, также срабатывает.</span><span class="sxs-lookup"><span data-stu-id="7f92f-168">Autorepeated key events caused by holding the key down will also fire this event.</span></span> <span data-ttu-id="7f92f-169">Чтобы отфильтровать эти данные, Проверьте аргументы события "KeyEventLParam" или "PhysicalKeyStatus".</span><span class="sxs-lookup"><span data-stu-id="7f92f-169">You can filter these out by checking the event args' KeyEventLParam or PhysicalKeyStatus.</span></span>

<span data-ttu-id="7f92f-170">В оконном режиме этот обработчик событий вызывается синхронно.</span><span class="sxs-lookup"><span data-stu-id="7f92f-170">In windowed mode, this event handler is called synchronously.</span></span> <span data-ttu-id="7f92f-171">До тех пор пока вы не вызываете Handle () для аргументов события или не будет возвращен обработчик событий, процесс браузера будет заблокирован и исходящие межпроцессные вызовы COM не будут работать с RPC_E_CANTCALLOUT_ININPUTSYNCCALL.</span><span class="sxs-lookup"><span data-stu-id="7f92f-171">Until you call Handle() on the event args or the event handler returns, the browser process will be blocked and outgoing cross-process COM calls will fail with RPC_E_CANTCALLOUT_ININPUTSYNCCALL.</span></span> <span data-ttu-id="7f92f-172">Однако все методы API CoreWebView2 будут работать.</span><span class="sxs-lookup"><span data-stu-id="7f92f-172">All CoreWebView2 API methods will work, however.</span></span>

<span data-ttu-id="7f92f-173">В режиме безоконный обработчик событий вызывается асинхронно.</span><span class="sxs-lookup"><span data-stu-id="7f92f-173">In windowless mode, the event handler is called asynchronously.</span></span> <span data-ttu-id="7f92f-174">Дальнейшие входные данные не доходят до браузера, пока обработчик событий не возвратит или не завершит вызов (), но сам процесс браузера не будет заблокирован, а исходящие вызовы COM будут работать нормально.</span><span class="sxs-lookup"><span data-stu-id="7f92f-174">Further input will not reach the browser until the event handler returns or Handle() is called, but the browser process itself will not be blocked, and outgoing COM calls will work normally.</span></span>

<span data-ttu-id="7f92f-175">Рекомендуется, чтобы вы могли узнать, что вы хотите обрабатывать клавишу быстрого вызова (TRUE), как и раньше.</span><span class="sxs-lookup"><span data-stu-id="7f92f-175">It is recommended to call Handle(TRUE) as early as you can know that you want to handle the accelerator key.</span></span>

```cpp
    // Register a handler for the AcceleratorKeyPressed event.
    CHECK_FAILURE(m_controller->add_AcceleratorKeyPressed(
        Callback<ICoreWebView2AcceleratorKeyPressedEventHandler>(
            [this](
                ICoreWebView2Controller* sender,
                ICoreWebView2AcceleratorKeyPressedEventArgs* args) -> HRESULT {
                COREWEBVIEW2_KEY_EVENT_KIND kind;
                CHECK_FAILURE(args->get_KeyEventKind(&kind));
                // We only care about key down events.
                if (kind == COREWEBVIEW2_KEY_EVENT_KIND_KEY_DOWN ||
                    kind == COREWEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_DOWN)
                {
                    UINT key;
                    CHECK_FAILURE(args->get_VirtualKey(&key));
                    // Check if the key is one we want to handle.
                    if (std::function<void()> action =
                            m_appWindow->GetAcceleratorKeyFunction(key))
                    {
                        // Keep the browser from handling this key, whether it's autorepeated or
                        // not.
                        CHECK_FAILURE(args->put_Handled(TRUE));

                        // Filter out autorepeated keys.
                        COREWEBVIEW2_PHYSICAL_KEY_STATUS status;
                        CHECK_FAILURE(args->get_PhysicalKeyStatus(&status));
                        if (!status.WasKeyDown)
                        {
                            // Perform the action asynchronously to avoid blocking the
                            // browser process's event queue.
                            m_appWindow->RunAsync(action);
                        }
                    }
                }
                return S_OK;
            })
            .Get(),
        &m_acceleratorKeyPressedToken));
```

#### <span data-ttu-id="7f92f-176">add_GotFocus</span><span class="sxs-lookup"><span data-stu-id="7f92f-176">add_GotFocus</span></span> 

<span data-ttu-id="7f92f-177">Добавьте обработчик событий для события GotFocus.</span><span class="sxs-lookup"><span data-stu-id="7f92f-177">Add an event handler for the GotFocus event.</span></span>

> <span data-ttu-id="7f92f-178">общедоступные значения HRESULT [add_GotFocus](#add_gotfocus)([ICoreWebView2FocusChangedEventHandler](icorewebview2focuschangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="7f92f-178">public HRESULT [add_GotFocus](#add_gotfocus)([ICoreWebView2FocusChangedEventHandler](icorewebview2focuschangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="7f92f-179">Получение фокуса срабатывает, когда WebView получил фокусировку.</span><span class="sxs-lookup"><span data-stu-id="7f92f-179">GotFocus fires when WebView got focus.</span></span>

#### <span data-ttu-id="7f92f-180">add_LostFocus</span><span class="sxs-lookup"><span data-stu-id="7f92f-180">add_LostFocus</span></span> 

<span data-ttu-id="7f92f-181">Добавьте обработчик для события LostFocus.</span><span class="sxs-lookup"><span data-stu-id="7f92f-181">Add an event handler for the LostFocus event.</span></span>

> <span data-ttu-id="7f92f-182">общедоступные значения HRESULT [add_LostFocus](#add_lostfocus)([ICoreWebView2FocusChangedEventHandler](icorewebview2focuschangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="7f92f-182">public HRESULT [add_LostFocus](#add_lostfocus)([ICoreWebView2FocusChangedEventHandler](icorewebview2focuschangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="7f92f-183">LostFocus вызывается, когда WebView теряет фокус.</span><span class="sxs-lookup"><span data-stu-id="7f92f-183">LostFocus fires when WebView lost focus.</span></span> <span data-ttu-id="7f92f-184">В случае, если возникает событие MoveFocusRequested, фокус по-прежнему находится в WebView при срабатывании события MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="7f92f-184">In the case where MoveFocusRequested event is fired, the focus is still on WebView when MoveFocusRequested event fires.</span></span> <span data-ttu-id="7f92f-185">Потерянный фокус срабатывает только в том случае, если код приложения или действие по умолчанию, заданное MoveFocusRequested события, задали фокус от WebView.</span><span class="sxs-lookup"><span data-stu-id="7f92f-185">Lost focus only fires afterwards when app's code or default action of MoveFocusRequested event set focus away from WebView.</span></span>

#### <span data-ttu-id="7f92f-186">add_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="7f92f-186">add_MoveFocusRequested</span></span> 

<span data-ttu-id="7f92f-187">Добавьте обработчик событий для события MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="7f92f-187">Add an event handler for the MoveFocusRequested event.</span></span>

> <span data-ttu-id="7f92f-188">общедоступные значения HRESULT [add_MoveFocusRequested](#add_movefocusrequested)([ICoreWebView2MoveFocusRequestedEventHandler](icorewebview2movefocusrequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="7f92f-188">public HRESULT [add_MoveFocusRequested](#add_movefocusrequested)([ICoreWebView2MoveFocusRequestedEventHandler](icorewebview2movefocusrequestedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="7f92f-189">MoveFocusRequested активируется, когда пользователь пытается выполнить переход из WebView.</span><span class="sxs-lookup"><span data-stu-id="7f92f-189">MoveFocusRequested fires when user tries to tab out of the WebView.</span></span> <span data-ttu-id="7f92f-190">При срабатывании этого события фокус WebView не изменился.</span><span class="sxs-lookup"><span data-stu-id="7f92f-190">The WebView's focus has not changed when this event is fired.</span></span>

```cpp
    // Register a handler for the MoveFocusRequested event.
    // This event will be fired when the user tabs out of the webview.
    // The handler will focus another window in the app, depending on which
    // direction the focus is being shifted.
    CHECK_FAILURE(m_controller->add_MoveFocusRequested(
        Callback<ICoreWebView2MoveFocusRequestedEventHandler>(
            [this](
                ICoreWebView2Controller* sender,
                ICoreWebView2MoveFocusRequestedEventArgs* args) -> HRESULT {
                if (!g_autoTabHandle)
                {
                    COREWEBVIEW2_MOVE_FOCUS_REASON reason;
                    CHECK_FAILURE(args->get_Reason(&reason));

                    if (reason == COREWEBVIEW2_MOVE_FOCUS_REASON_NEXT)
                    {
                        TabForwards(-1);
                    }
                    else if (reason == COREWEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS)
                    {
                        TabBackwards(int(m_tabbableWindows.size()));
                    }
                    CHECK_FAILURE(args->put_Handled(TRUE));
                }
                return S_OK;
            })
            .Get(),
        &m_moveFocusRequestedToken));
```

#### <span data-ttu-id="7f92f-191">add_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="7f92f-191">add_ZoomFactorChanged</span></span> 

<span data-ttu-id="7f92f-192">Добавьте обработчик событий для события ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="7f92f-192">Add an event handler for the ZoomFactorChanged event.</span></span>

> <span data-ttu-id="7f92f-193">общедоступные значения HRESULT [add_ZoomFactorChanged](#add_zoomfactorchanged)([ICoreWebView2ZoomFactorChangedEventHandler](icorewebview2zoomfactorchangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="7f92f-193">public HRESULT [add_ZoomFactorChanged](#add_zoomfactorchanged)([ICoreWebView2ZoomFactorChangedEventHandler](icorewebview2zoomfactorchangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="7f92f-194">Событие срабатывает, когда изменяется свойство ZoomFactor объекта WebView.</span><span class="sxs-lookup"><span data-stu-id="7f92f-194">The event fires when the ZoomFactor property of the WebView changes.</span></span> <span data-ttu-id="7f92f-195">Событие может срабатывать из-за того, что вызывающий объект изменил свойство ZoomFactor или пользователь вручную изменял масштаб.</span><span class="sxs-lookup"><span data-stu-id="7f92f-195">The event could fire because the caller modified the ZoomFactor property, or due to the user manually modifying the zoom.</span></span> <span data-ttu-id="7f92f-196">При изменении вызывающим абонентом с помощью свойства ZoomFactor внутренний коэффициент масштабирования немедленно обновляется, и событие ZoomFactorChanged не выводится.</span><span class="sxs-lookup"><span data-stu-id="7f92f-196">When it is modified by the caller via the ZoomFactor property, the internal zoom factor is updated immediately and there will be no ZoomFactorChanged event.</span></span> <span data-ttu-id="7f92f-197">WebView связывает последний использованный коэффициент масштабирования для каждого сайта.</span><span class="sxs-lookup"><span data-stu-id="7f92f-197">WebView associates the last used zoom factor for each site.</span></span> <span data-ttu-id="7f92f-198">Поэтому коэффициент масштабирования может изменяться при переходе на другую страницу.</span><span class="sxs-lookup"><span data-stu-id="7f92f-198">Therefore, it is possible for the zoom factor to change when navigating to a different page.</span></span> <span data-ttu-id="7f92f-199">При изменении коэффициента масштабирования из-за этого событие ZoomFactorChanged срабатывает сразу после события ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="7f92f-199">When the zoom factor changes due to this, the ZoomFactorChanged event fires right after the ContentLoading event.</span></span>

```cpp
    // Register a handler for the ZoomFactorChanged event.
    // This handler just announces the new level of zoom on the window's title bar.
    CHECK_FAILURE(m_controller->add_ZoomFactorChanged(
        Callback<ICoreWebView2ZoomFactorChangedEventHandler>(
            [this](ICoreWebView2Controller* sender, IUnknown* args) -> HRESULT {
                double zoomFactor;
                CHECK_FAILURE(sender->get_ZoomFactor(&zoomFactor));

                std::wstring message = L"WebView2APISample (Zoom: " +
                                       std::to_wstring(int(zoomFactor * 100)) + L"%)";
                SetWindowText(m_appWindow->GetMainWindow(), message.c_str());
                return S_OK;
            })
            .Get(),
        &m_zoomFactorChangedToken));
```

#### <span data-ttu-id="7f92f-200">Close (закрыть)</span><span class="sxs-lookup"><span data-stu-id="7f92f-200">Close</span></span> 

<span data-ttu-id="7f92f-201">Закрывает WebView и очищает основной экземпляр браузера.</span><span class="sxs-lookup"><span data-stu-id="7f92f-201">Closes the WebView and cleans up the underlying browser instance.</span></span>

> <span data-ttu-id="7f92f-202">общедоступное значение HRESULT [Close](#close)()</span><span class="sxs-lookup"><span data-stu-id="7f92f-202">public HRESULT [Close](#close)()</span></span>

<span data-ttu-id="7f92f-203">Очистка экземпляра браузера приведет к освобождению ресурсов, WebView в сети.</span><span class="sxs-lookup"><span data-stu-id="7f92f-203">Cleaning up the browser instance will release the resources powering the WebView.</span></span> <span data-ttu-id="7f92f-204">Экземпляр браузера будет закрыт, если он не используется другими веб – представлениями.</span><span class="sxs-lookup"><span data-stu-id="7f92f-204">The browser instance will be shut down if there are no other WebViews using it.</span></span>

<span data-ttu-id="7f92f-205">После вызова метода Close все вызовы методов завершатся сбоем, и обработчики событий прекратятся.</span><span class="sxs-lookup"><span data-stu-id="7f92f-205">After calling Close, all method calls will fail and event handlers will stop firing.</span></span> <span data-ttu-id="7f92f-206">В частности, WebView будет освобождать ссылки на обработчики событий при вызове Close.</span><span class="sxs-lookup"><span data-stu-id="7f92f-206">Specifically, the WebView will release its references to its event handlers when Close is called.</span></span>

<span data-ttu-id="7f92f-207">Метод Close вызывается неявно, когда CoreWebView2Controller теряет свою конечную ссылку и является независимым.</span><span class="sxs-lookup"><span data-stu-id="7f92f-207">Close is implicitly called when the CoreWebView2Controller loses its final reference and is destructed.</span></span> <span data-ttu-id="7f92f-208">Но рекомендуется явным образом вызывать метод Close, чтобы избежать случайного цикла ссылок между WebView и кодом приложения.</span><span class="sxs-lookup"><span data-stu-id="7f92f-208">But it is best practice to explicitly call Close to avoid any accidental cycle of references between the WebView and the app code.</span></span> <span data-ttu-id="7f92f-209">В частности, если вы захватываете ссылку на WebView в обработчике событий, вы создадите цикл ссылки между WebView и обработчиком событий.</span><span class="sxs-lookup"><span data-stu-id="7f92f-209">Specifically, if you capture a reference to the WebView in an event handler you will create a reference cycle between the WebView and the event handler.</span></span> <span data-ttu-id="7f92f-210">Вызов Close приведет к прерыванию этого цикла, освобождая все обработчики событий.</span><span class="sxs-lookup"><span data-stu-id="7f92f-210">Calling Close will break this cycle by releasing all event handlers.</span></span> <span data-ttu-id="7f92f-211">Но чтобы избежать такой ситуации, рекомендуется как явным образом вызвать метод Close для WebView и не захватить ссылку на WebView, чтобы убедиться, что WebView может быть корректно очищено.</span><span class="sxs-lookup"><span data-stu-id="7f92f-211">But to avoid this situation it is best practice both to explicitly call Close on the WebView and to not capture a reference to the WebView to ensure the WebView can be cleaned up correctly.</span></span>

```cpp
// Close the WebView and deinitialize related state. This doesn't close the app window.
void AppWindow::CloseWebView(bool cleanupUserDataFolder)
{
    DeleteAllComponents();
    if (m_controller)
    {
        m_controller->Close();
        m_controller = nullptr;
        m_webView = nullptr;
    }
    m_webViewEnvironment = nullptr;
    if (cleanupUserDataFolder)
    {
        // For non-UWP apps, the default user data folder {Executable File Name}.WebView2
        // is in the same directory next to the app executable. If end
        // developers specify userDataFolder during WebView environment
        // creation, they would need to pass in that explicit value here.
        // For more information about userDataFolder:
        // https://docs.microsoft.com/microsoft-edge/hosting/webview2/reference/win32/0-9-488/webview2-idl#createwebview2environmentwithoptions
        WCHAR userDataFolder[MAX_PATH] = L"";
        // Obtain the absolute path for relative paths that include "./" or "../"
        _wfullpath(
            userDataFolder, GetLocalPath(L"WebView2APISample.exe.WebView2").c_str(), MAX_PATH);
        std::wstring userDataFolderPath(userDataFolder);

        std::wstring message = L"Are you sure you want to clean up the user data folder at\n";
        message += userDataFolderPath;
        message += L"\n?\nWarning: This action is not reversible.\n\n";
        message += L"Click No if there are other open WebView instances.\n";

        if (MessageBox(m_mainWindow, message.c_str(), L"Cleanup User Data Folder", MB_YESNO) ==
            IDYES)
        {
            CHECK_FAILURE(DeleteFileRecursive(userDataFolderPath));
        }
    }
}
```

#### <span data-ttu-id="7f92f-212">get_Bounds</span><span class="sxs-lookup"><span data-stu-id="7f92f-212">get_Bounds</span></span> 

<span data-ttu-id="7f92f-213">Границы WebView.</span><span class="sxs-lookup"><span data-stu-id="7f92f-213">The webview bounds.</span></span>

> <span data-ttu-id="7f92f-214">общедоступные значения HRESULT [get_Bounds](#get_bounds)(границы Rect \*)</span><span class="sxs-lookup"><span data-stu-id="7f92f-214">public HRESULT [get_Bounds](#get_bounds)(RECT \* bounds)</span></span>

<span data-ttu-id="7f92f-215">Границы задаются относительно родительского дескриптора HWND.</span><span class="sxs-lookup"><span data-stu-id="7f92f-215">Bounds are relative to the parent HWND.</span></span> <span data-ttu-id="7f92f-216">Приложение может располагать WebView двумя способами:</span><span class="sxs-lookup"><span data-stu-id="7f92f-216">The app has two ways it can position a WebView:</span></span>

1. <span data-ttu-id="7f92f-217">Создание дочернего HWND, который является родительским дескриптором HWND WebView.</span><span class="sxs-lookup"><span data-stu-id="7f92f-217">Create a child HWND that is the WebView parent HWND.</span></span> <span data-ttu-id="7f92f-218">Расположите это окно в том месте, где должен быть WebView.</span><span class="sxs-lookup"><span data-stu-id="7f92f-218">Position this window where the WebView should be.</span></span> <span data-ttu-id="7f92f-219">В этом случае используйте (0, 0) для левого верхнего угла WebView Bound's (сдвиг).</span><span class="sxs-lookup"><span data-stu-id="7f92f-219">In this case, use (0, 0) for the WebView's Bound's top left corner (the offset).</span></span>

1. <span data-ttu-id="7f92f-220">Используйте окно самого высокого приложения в качестве родительского HWND WebView.</span><span class="sxs-lookup"><span data-stu-id="7f92f-220">Use the app's top most window as the WebView parent HWND.</span></span> <span data-ttu-id="7f92f-221">Задайте Bound's левый верхний угол WebView, чтобы WebView правильно расположиться в приложении.</span><span class="sxs-lookup"><span data-stu-id="7f92f-221">Set the WebView's Bound's top left corner so that the WebView is positioned correctly in the app.</span></span> <span data-ttu-id="7f92f-222">Значения границ находятся в пространстве координат основного приложения.</span><span class="sxs-lookup"><span data-stu-id="7f92f-222">The Bound's values are in the host's coordinate space.</span></span>

#### <span data-ttu-id="7f92f-223">get_CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="7f92f-223">get_CoreWebView2</span></span> 

<span data-ttu-id="7f92f-224">Возвращает CoreWebView2, связанный с этим CoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="7f92f-224">Gets the CoreWebView2 associated with this CoreWebView2Controller.</span></span>

> <span data-ttu-id="7f92f-225">общедоступные значения HRESULT [get_CoreWebView2](#get_corewebview2)([ICoreWebView2](icorewebview2.md) \* \* CoreWebView2)</span><span class="sxs-lookup"><span data-stu-id="7f92f-225">public HRESULT [get_CoreWebView2](#get_corewebview2)([ICoreWebView2](icorewebview2.md) \*\* coreWebView2)</span></span>

#### <span data-ttu-id="7f92f-226">get_IsVisible</span><span class="sxs-lookup"><span data-stu-id="7f92f-226">get_IsVisible</span></span> 

<span data-ttu-id="7f92f-227">Свойство Visible определяет, нужно ли отображать или скрывать WebView.</span><span class="sxs-lookup"><span data-stu-id="7f92f-227">The IsVisible property determines whether to show or hide the webview.</span></span>

> <span data-ttu-id="7f92f-228">общедоступные значения HRESULT [get_IsVisible](#get_isvisible)(bool \* Visible)</span><span class="sxs-lookup"><span data-stu-id="7f92f-228">public HRESULT [get_IsVisible](#get_isvisible)(BOOL \* isVisible)</span></span>

<span data-ttu-id="7f92f-229">Если для свойства Visible задано значение false, WebView будет прозрачным и не будет обрабатываться.</span><span class="sxs-lookup"><span data-stu-id="7f92f-229">If IsVisible is set to false, the webview will be transparent and will not be rendered.</span></span> <span data-ttu-id="7f92f-230">Однако это не повлияет на окно, содержащее WebView (параметр HWND, переданный в CreateCoreWebView2Controller).</span><span class="sxs-lookup"><span data-stu-id="7f92f-230">However, this will not affect the window containing the webview (the HWND parameter that was passed to CreateCoreWebView2Controller).</span></span> <span data-ttu-id="7f92f-231">Если вы хотите, чтобы окно не исчезало, вызовите для него функцию ShowWindow прямо в дополнение к изменению свойства Visible.</span><span class="sxs-lookup"><span data-stu-id="7f92f-231">If you want that window to disappear too, call ShowWindow on it directly in addition to modifying the IsVisible property.</span></span> <span data-ttu-id="7f92f-232">WebView — это дочернее окно не получает оконные сообщения, когда окно свертывания или восстановления находится в верхней части окна.</span><span class="sxs-lookup"><span data-stu-id="7f92f-232">WebView as a child window won't get window messages when the top window is minimized or restored.</span></span> <span data-ttu-id="7f92f-233">Для повышения производительности разработчик должен установить для свойства WebView значение false, если окно приложения свернуто, и вернуть значение true при восстановлении окна приложения.</span><span class="sxs-lookup"><span data-stu-id="7f92f-233">For performance reason, developer should set IsVisible property of the WebView to false when the app window is minimized and back to true when app window is restored.</span></span> <span data-ttu-id="7f92f-234">Это можно сделать, обрабатывая команды SC_MINIMIZE и SC_RESTORE при получении WM_SYSCOMMAND сообщения.</span><span class="sxs-lookup"><span data-stu-id="7f92f-234">App window can do this by handling SC_MINIMIZE and SC_RESTORE command upon receiving WM_SYSCOMMAND message.</span></span>

```cpp
void ViewComponent::ToggleVisibility()
{
    BOOL visible;
    m_controller->get_IsVisible(&visible);
    m_isVisible = !visible;
    m_controller->put_IsVisible(m_isVisible);
}
```

#### <span data-ttu-id="7f92f-235">get_ParentWindow</span><span class="sxs-lookup"><span data-stu-id="7f92f-235">get_ParentWindow</span></span> 

<span data-ttu-id="7f92f-236">Родительское окно, предоставленное приложением, используемое этим WebView, для отрисовки содержимого.</span><span class="sxs-lookup"><span data-stu-id="7f92f-236">The parent window provided by the app that this WebView is using to render content.</span></span>

> <span data-ttu-id="7f92f-237">общедоступные значения HRESULT [get_ParentWindow](#get_parentwindow)(HWND \* topLevelWindow)</span><span class="sxs-lookup"><span data-stu-id="7f92f-237">public HRESULT [get_ParentWindow](#get_parentwindow)(HWND \* topLevelWindow)</span></span>

<span data-ttu-id="7f92f-238">Этот API первоначально возвращает окно, передаваемое в CreateCoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="7f92f-238">This API initially returns the window passed into CreateCoreWebView2Controller.</span></span>

#### <span data-ttu-id="7f92f-239">get_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="7f92f-239">get_ZoomFactor</span></span> 

<span data-ttu-id="7f92f-240">Коэффициент масштабирования для WebView.</span><span class="sxs-lookup"><span data-stu-id="7f92f-240">The zoom factor for the WebView.</span></span>

> <span data-ttu-id="7f92f-241">общедоступные значения HRESULT [get_ZoomFactor](#get_zoomfactor)(Double \* ZoomFactor)</span><span class="sxs-lookup"><span data-stu-id="7f92f-241">public HRESULT [get_ZoomFactor](#get_zoomfactor)(double \* zoomFactor)</span></span>

<span data-ttu-id="7f92f-242">Обратите внимание, что изменение коэффициента масштабирования может привести к `window.innerWidth/innerHeight` изменению масштаба страницы.</span><span class="sxs-lookup"><span data-stu-id="7f92f-242">Note that changing zoom factor could cause `window.innerWidth/innerHeight` and page layout to change.</span></span> <span data-ttu-id="7f92f-243">Коэффициент масштабирования, примененный ведущим приложением путем вызова ZoomFactor, становится новым масштабом по умолчанию для WebView.</span><span class="sxs-lookup"><span data-stu-id="7f92f-243">A zoom factor that is applied by the host by calling ZoomFactor becomes the new default zoom for the WebView.</span></span> <span data-ttu-id="7f92f-244">Этот коэффициент масштабирования применяется для всех переходов и — коэффициент масштабирования WebView возвращается, когда пользователь нажимает клавиши CTRL + 0.</span><span class="sxs-lookup"><span data-stu-id="7f92f-244">This zoom factor applies across navigations and is the zoom factor WebView is returned to when the user presses ctrl+0.</span></span> <span data-ttu-id="7f92f-245">При изменении коэффициента масштабирования пользователем (в результате использования приложения, получающего ZoomFactorChanged) это масштабирование применяется только к текущей странице.</span><span class="sxs-lookup"><span data-stu-id="7f92f-245">When the zoom factor is changed by the user (resulting in the app receiving ZoomFactorChanged), that zoom applies only for the current page.</span></span> <span data-ttu-id="7f92f-246">Любой пользователь, который применяет масштабирование, используется только для текущей страницы и сбрасывается на панели навигации.</span><span class="sxs-lookup"><span data-stu-id="7f92f-246">Any user applied zoom is only for the current page and is reset on a navigation.</span></span> <span data-ttu-id="7f92f-247">Указывать zoomFactor меньше или равно 0 не разрешается.</span><span class="sxs-lookup"><span data-stu-id="7f92f-247">Specifying a zoomFactor less than or equal to 0 is not allowed.</span></span> <span data-ttu-id="7f92f-248">WebView также имеет внутренний поддерживаемый диапазон коэффициента масштабирования.</span><span class="sxs-lookup"><span data-stu-id="7f92f-248">WebView also has an internal supported zoom factor range.</span></span> <span data-ttu-id="7f92f-249">Если указанный коэффициент масштаба выходит за пределы этого диапазона, он будет нормализован в пределах диапазона, а событие ZoomFactorChanged будет инициировано для фактического коэффициента масштабирования.</span><span class="sxs-lookup"><span data-stu-id="7f92f-249">When a specified zoom factor is out of that range, it will be normalized to be within the range, and a ZoomFactorChanged event will be fired for the real applied zoom factor.</span></span> <span data-ttu-id="7f92f-250">При выполнении этой нормализации диапазона свойство ZoomFactor будет указывать коэффициент масштабирования, указанный в предыдущем изменении свойства ZoomFactor, пока событие ZoomFactorChanged не будет получено после WebView применяет нормализованный коэффициент масштабирования.</span><span class="sxs-lookup"><span data-stu-id="7f92f-250">When this range normalization happens, the ZoomFactor property will report the zoom factor specified during the previous modification of the ZoomFactor property until the ZoomFactorChanged event is received after webview applies the normalized zoom factor.</span></span>

#### <span data-ttu-id="7f92f-251">MoveFocus</span><span class="sxs-lookup"><span data-stu-id="7f92f-251">MoveFocus</span></span> 

<span data-ttu-id="7f92f-252">Перемещение фокуса в WebView.</span><span class="sxs-lookup"><span data-stu-id="7f92f-252">Move focus into WebView.</span></span>

> <span data-ttu-id="7f92f-253">общедоступные значения HRESULT [MoveFocus](#movefocus)(причина COREWEBVIEW2_MOVE_FOCUS_REASON)</span><span class="sxs-lookup"><span data-stu-id="7f92f-253">public HRESULT [MoveFocus](#movefocus)(COREWEBVIEW2_MOVE_FOCUS_REASON reason)</span></span>

<span data-ttu-id="7f92f-254">WebView получит фокус, и фокус будет установлен на элемент корреспондента на странице, которая размещена в WebView.</span><span class="sxs-lookup"><span data-stu-id="7f92f-254">WebView will get focus and focus will be set to correspondent element in the page hosted in the WebView.</span></span> <span data-ttu-id="7f92f-255">В целях программной причины фокус установлен на ранее сфокусированный элемент или элемент по умолчанию, если нет ранее фокусируемого элемента.</span><span class="sxs-lookup"><span data-stu-id="7f92f-255">For Programmatic reason, focus is set to previously focused element or the default element if there is no previously focused element.</span></span> <span data-ttu-id="7f92f-256">В следующей причине фокус задается для первого элемента.</span><span class="sxs-lookup"><span data-stu-id="7f92f-256">For Next reason, focus is set to the first element.</span></span> <span data-ttu-id="7f92f-257">По этой причине фокус установлен на последний элемент.</span><span class="sxs-lookup"><span data-stu-id="7f92f-257">For Previous reason, focus is set to the last element.</span></span> <span data-ttu-id="7f92f-258">WebView также может сосредоточиться на взаимодействии с пользователем, например, щелкнув на WebView или TAB.</span><span class="sxs-lookup"><span data-stu-id="7f92f-258">WebView can also got focus through user interaction like clicking into WebView or Tab into it.</span></span> <span data-ttu-id="7f92f-259">Для табуляции приложение может вызвать MoveFocus с помощью кнопки Далее или назад, чтобы выровнять элементы Tab и SHIFT + TAB, если это необходимо, если WebView является следующим элементом с вкладками.</span><span class="sxs-lookup"><span data-stu-id="7f92f-259">For tabbing, the app can call MoveFocus with Next or Previous to align with tab and shift+tab respectively when it decides the WebView is the next tabbable element.</span></span> <span data-ttu-id="7f92f-260">Кроме того, приложение может вызвать IsDialogMessage как часть цикла обработки сообщений, чтобы платформа автоматически обрабатывала табуляцию.</span><span class="sxs-lookup"><span data-stu-id="7f92f-260">Or, the app can call IsDialogMessage as part of its message loop to allow the platform to auto handle tabbing.</span></span> <span data-ttu-id="7f92f-261">Платформа будет повернута на все окна с помощью WS_TABSTOP.</span><span class="sxs-lookup"><span data-stu-id="7f92f-261">The platform will rotate through all windows with WS_TABSTOP.</span></span> <span data-ttu-id="7f92f-262">Когда WebView получает фокус из IsDialogMessage, он будет внутренне размещать фокус на первом или последнем элементе Tab и Shift + Tab соответственно.</span><span class="sxs-lookup"><span data-stu-id="7f92f-262">When the WebView gets focus from IsDialogMessage, it will internally put the focus on the first or last element for tab and shift+tab respectively.</span></span>

```cpp
    while (GetMessage(&msg, nullptr, 0, 0))
    {
        if (!TranslateAccelerator(msg.hwnd, hAccelTable, &msg))
        {
            // Calling IsDialogMessage handles Tab traversal automatically. If the
            // app wants the platform to auto handle tab, then call IsDialogMessage
            // before calling TranslateMessage/DispatchMessage. If the app wants to
            // handle tabbing itself, then skip calling IsDialogMessage and call
            // TranslateMessage/DispatchMessage directly.
            if (!g_autoTabHandle || !IsDialogMessage(GetAncestor(msg.hwnd, GA_ROOT), &msg))
            {
                TranslateMessage(&msg);
                DispatchMessage(&msg);
            }
        }
    }
```

```cpp
        if (wParam == VK_TAB)
        {
            // Find out if the window is one we've customized for tab handling
            for (size_t i = 0; i < m_tabbableWindows.size(); i++)
            {
                if (m_tabbableWindows[i].first == hWnd)
                {
                    if (GetKeyState(VK_SHIFT) < 0)
                    {
                        TabBackwards(i);
                    }
                    else
                    {
                        TabForwards(i);
                    }
                    return true;
                }
            }
        }
```

```cpp
void ControlComponent::TabForwards(int currentIndex)
{
    // Find first enabled window after the active one
    for (size_t i = currentIndex + 1; i < m_tabbableWindows.size(); i++)
    {
        HWND hwnd = m_tabbableWindows.at(i).first;
        if (IsWindowEnabled(hwnd))
        {
            SetFocus(hwnd);
            return;
        }
    }
    // If this is the last enabled window, tab forwards into the WebView.
    m_controller->MoveFocus(COREWEBVIEW2_MOVE_FOCUS_REASON_NEXT);
}

void ControlComponent::TabBackwards(int currentIndex)
{
    // Find first enabled window before the active one
    for (int i = currentIndex - 1; i >= 0; i--)
    {
        HWND hwnd = m_tabbableWindows.at(i).first;
        if (IsWindowEnabled(hwnd))
        {
            SetFocus(hwnd);
            return;
        }
    }
    // If this is the last enabled window, tab forwards into the WebView.
    CHECK_FAILURE(m_controller->MoveFocus(COREWEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS));
}
```

#### <span data-ttu-id="7f92f-263">NotifyParentWindowPositionChanged</span><span class="sxs-lookup"><span data-stu-id="7f92f-263">NotifyParentWindowPositionChanged</span></span> 

<span data-ttu-id="7f92f-264">Это уведомление отделено от границ, которые сообщают WebView, что родительский HWND (или любой предк) переместился.</span><span class="sxs-lookup"><span data-stu-id="7f92f-264">This is a notification separate from Bounds that tells WebView its parent (or any ancestor) HWND moved.</span></span>

> <span data-ttu-id="7f92f-265">общедоступные значения HRESULT [NotifyParentWindowPositionChanged](#notifyparentwindowpositionchanged)()</span><span class="sxs-lookup"><span data-stu-id="7f92f-265">public HRESULT [NotifyParentWindowPositionChanged](#notifyparentwindowpositionchanged)()</span></span>

<span data-ttu-id="7f92f-266">Это необходимо для правильной работы специальных возможностей и некоторых диалоговых окон в WebView.</span><span class="sxs-lookup"><span data-stu-id="7f92f-266">This is needed for accessibility and certain dialogs in WebView to work correctly.</span></span> 
```cpp
    if (message == WM_MOVE || message == WM_MOVING)
    {
        m_controller->NotifyParentWindowPositionChanged();
        return true;
    }
```

#### <span data-ttu-id="7f92f-267">put_Bounds</span><span class="sxs-lookup"><span data-stu-id="7f92f-267">put_Bounds</span></span> 

<span data-ttu-id="7f92f-268">Задайте свойство Bounds.</span><span class="sxs-lookup"><span data-stu-id="7f92f-268">Set the Bounds property.</span></span>

> <span data-ttu-id="7f92f-269">общедоступные значения HRESULT [put_Bounds](#put_bounds)(границы Rect)</span><span class="sxs-lookup"><span data-stu-id="7f92f-269">public HRESULT [put_Bounds](#put_bounds)(RECT bounds)</span></span>

```cpp
// Update the bounds of the WebView window to fit available space.
void ViewComponent::ResizeWebView()
{
    SIZE webViewSize = {
            LONG((m_webViewBounds.right - m_webViewBounds.left) * m_webViewRatio * m_webViewScale),
            LONG((m_webViewBounds.bottom - m_webViewBounds.top) * m_webViewRatio * m_webViewScale) };

    RECT desiredBounds = m_webViewBounds;
    desiredBounds.bottom = LONG(
        webViewSize.cy + m_webViewBounds.top);
    desiredBounds.right = LONG(
        webViewSize.cx + m_webViewBounds.left);

    m_controller->put_Bounds(desiredBounds);
    if (m_compositionController)
    {
        POINT webViewOffset = {m_webViewBounds.left, m_webViewBounds.top};

        if (m_dcompDevice)
        {
            CHECK_FAILURE(m_dcompRootVisual->SetOffsetX(float(webViewOffset.x)));
            CHECK_FAILURE(m_dcompRootVisual->SetOffsetY(float(webViewOffset.y)));
            CHECK_FAILURE(m_dcompRootVisual->SetClip(
                {0, 0, float(webViewSize.cx), float(webViewSize.cy)}));
            CHECK_FAILURE(m_dcompDevice->Commit());
        }
        else if (m_wincompHelper)
        {
            m_wincompHelper->UpdateSizeAndPosition(webViewOffset, webViewSize);
        }
    }
}
```

#### <span data-ttu-id="7f92f-270">put_IsVisible</span><span class="sxs-lookup"><span data-stu-id="7f92f-270">put_IsVisible</span></span> 

<span data-ttu-id="7f92f-271">Задайте свойство Visible.</span><span class="sxs-lookup"><span data-stu-id="7f92f-271">Set the IsVisible property.</span></span>

> <span data-ttu-id="7f92f-272">общедоступные значения HRESULT [put_IsVisible](#put_isvisible)(bool-Visible)</span><span class="sxs-lookup"><span data-stu-id="7f92f-272">public HRESULT [put_IsVisible](#put_isvisible)(BOOL isVisible)</span></span>

```cpp
    if (message == WM_SYSCOMMAND)
    {
        if (wParam == SC_MINIMIZE)
        {
            // Hide the webview when the app window is minimized.
            m_controller->put_IsVisible(FALSE);
        }
        else if (wParam == SC_RESTORE)
        {
            // When the app window is restored, show the webview
            // (unless the user has toggle visibility off).
            if (m_isVisible)
            {
                m_controller->put_IsVisible(TRUE);
            }
        }
    }
```

#### <span data-ttu-id="7f92f-273">put_ParentWindow</span><span class="sxs-lookup"><span data-stu-id="7f92f-273">put_ParentWindow</span></span> 

<span data-ttu-id="7f92f-274">Установка родительского окна для WebView.</span><span class="sxs-lookup"><span data-stu-id="7f92f-274">Set the parent window for the WebView.</span></span>

> <span data-ttu-id="7f92f-275">общедоступные значения HRESULT [put_ParentWindow](#put_parentwindow)(HWND topLevelWindow)</span><span class="sxs-lookup"><span data-stu-id="7f92f-275">public HRESULT [put_ParentWindow](#put_parentwindow)(HWND topLevelWindow)</span></span>

<span data-ttu-id="7f92f-276">Это приведет к тому, что WebView перестанет достать родительским окном до вновь заданной окна.</span><span class="sxs-lookup"><span data-stu-id="7f92f-276">This will cause the WebView to reparent its window to the newly provided window.</span></span>

#### <span data-ttu-id="7f92f-277">put_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="7f92f-277">put_ZoomFactor</span></span> 

<span data-ttu-id="7f92f-278">Задайте свойство ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="7f92f-278">Set the ZoomFactor property.</span></span>

> <span data-ttu-id="7f92f-279">общедоступный [PUT_ZOOMFACTOR](#put_zoomfactor)HRESULT (двойной ZoomFactor)</span><span class="sxs-lookup"><span data-stu-id="7f92f-279">public HRESULT [put_ZoomFactor](#put_zoomfactor)(double zoomFactor)</span></span>

#### <span data-ttu-id="7f92f-280">remove_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="7f92f-280">remove_AcceleratorKeyPressed</span></span> 

<span data-ttu-id="7f92f-281">Удалите обработчик событий, добавленный ранее add_AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="7f92f-281">Remove an event handler previously added with add_AcceleratorKeyPressed.</span></span>

> <span data-ttu-id="7f92f-282">общедоступные значения HRESULT [remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="7f92f-282">public HRESULT [remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="7f92f-283">remove_GotFocus</span><span class="sxs-lookup"><span data-stu-id="7f92f-283">remove_GotFocus</span></span> 

<span data-ttu-id="7f92f-284">Удалите обработчик событий, добавленный ранее add_GotFocus.</span><span class="sxs-lookup"><span data-stu-id="7f92f-284">Remove an event handler previously added with add_GotFocus.</span></span>

> <span data-ttu-id="7f92f-285">общедоступные значения HRESULT [remove_GotFocus](#remove_gotfocus)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="7f92f-285">public HRESULT [remove_GotFocus](#remove_gotfocus)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="7f92f-286">remove_LostFocus</span><span class="sxs-lookup"><span data-stu-id="7f92f-286">remove_LostFocus</span></span> 

<span data-ttu-id="7f92f-287">Удалите обработчик событий, добавленный ранее add_LostFocus.</span><span class="sxs-lookup"><span data-stu-id="7f92f-287">Remove an event handler previously added with add_LostFocus.</span></span>

> <span data-ttu-id="7f92f-288">общедоступные значения HRESULT [remove_LostFocus](#remove_lostfocus)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="7f92f-288">public HRESULT [remove_LostFocus](#remove_lostfocus)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="7f92f-289">remove_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="7f92f-289">remove_MoveFocusRequested</span></span> 

<span data-ttu-id="7f92f-290">Удалите обработчик событий, добавленный ранее add_MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="7f92f-290">Remove an event handler previously added with add_MoveFocusRequested.</span></span>

> <span data-ttu-id="7f92f-291">общедоступные значения HRESULT [remove_MoveFocusRequested](#remove_movefocusrequested)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="7f92f-291">public HRESULT [remove_MoveFocusRequested](#remove_movefocusrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="7f92f-292">remove_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="7f92f-292">remove_ZoomFactorChanged</span></span> 

<span data-ttu-id="7f92f-293">Удалите обработчик событий, добавленный ранее add_ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="7f92f-293">Remove an event handler previously added with add_ZoomFactorChanged.</span></span>

> <span data-ttu-id="7f92f-294">общедоступные значения HRESULT [remove_ZoomFactorChanged](#remove_zoomfactorchanged)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="7f92f-294">public HRESULT [remove_ZoomFactorChanged](#remove_zoomfactorchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="7f92f-295">SetBoundsAndZoomFactor</span><span class="sxs-lookup"><span data-stu-id="7f92f-295">SetBoundsAndZoomFactor</span></span> 

<span data-ttu-id="7f92f-296">Одновременное обновление границ и свойств ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="7f92f-296">Update Bounds and ZoomFactor properties at the same time.</span></span>

> <span data-ttu-id="7f92f-297">общедоступные значения HRESULT [SetBoundsAndZoomFactor](#setboundsandzoomfactor)(границы Rect, Double zoomFactor)</span><span class="sxs-lookup"><span data-stu-id="7f92f-297">public HRESULT [SetBoundsAndZoomFactor](#setboundsandzoomfactor)(RECT bounds, double zoomFactor)</span></span>

<span data-ttu-id="7f92f-298">Эта операция является атомарной с точки зрения хоста.</span><span class="sxs-lookup"><span data-stu-id="7f92f-298">This operation is atomic from the host's perspective.</span></span> <span data-ttu-id="7f92f-299">После того как вы вернете эту функцию, свойства Bounds и ZoomFactor будут обновлены при успешном выполнении функции, или ни один из них не будет обновляться при сбое функции.</span><span class="sxs-lookup"><span data-stu-id="7f92f-299">After returning from this function, the Bounds and ZoomFactor properties will have both been updated if the function is successful, or neither will be updated if the function fails.</span></span> <span data-ttu-id="7f92f-300">Если границы и ZoomFactor обновляются одним масштабом (то есть границы и ZoomFactor оба двойных), то страница не будет видеть изменение в Window. innerWidth/innerHeight, а WebView будет отображать содержимое на новом размере и масштабе без промежуточных преобразований.</span><span class="sxs-lookup"><span data-stu-id="7f92f-300">If Bounds and ZoomFactor are both updated by the same scale (i.e. Bounds and ZoomFactor are both doubled), then the page will not see a change in window.innerWidth/innerHeight and the WebView will render the content at the new size and zoom without intermediate renderings.</span></span> <span data-ttu-id="7f92f-301">Эта функция также может использоваться для обновления только одного из ZoomFactor или границ путем передачи нового значения для одного и текущего значения другого.</span><span class="sxs-lookup"><span data-stu-id="7f92f-301">This function can also be used to update just one of ZoomFactor or Bounds by passing in the new value for one and the current value for the other.</span></span>

```cpp
void ViewComponent::SetScale(float scale)
{
    RECT bounds;
    CHECK_FAILURE(m_controller->get_Bounds(&bounds));
    double scaleChange = scale / m_webViewScale;

    bounds.bottom = LONG(
        (bounds.bottom - bounds.top) * scaleChange + bounds.top);
    bounds.right = LONG(
        (bounds.right - bounds.left) * scaleChange + bounds.left);

    m_webViewScale = scale;
    m_controller->SetBoundsAndZoomFactor(bounds, scale);
}
```

