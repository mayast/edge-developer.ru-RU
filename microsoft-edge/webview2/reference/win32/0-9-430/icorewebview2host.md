---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2Host
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 39566c867c28739d21dd99c369d161d29a308946
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885620"
---
# <span data-ttu-id="64f91-104">0.9.430-Interface ICoreWebView2Host</span><span class="sxs-lookup"><span data-stu-id="64f91-104">0.9.430 - interface ICoreWebView2Host</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2Host
  : public IUnknown
```

<span data-ttu-id="64f91-105">Этот интерфейс является владельцем объекта CoreWebView2 и предоставляет поддержку изменения размеров, отображения и скрытия, фокусировки и других функциональных возможностей, связанных с окнами и композицией.</span><span class="sxs-lookup"><span data-stu-id="64f91-105">This interface is the owner of the CoreWebView2 object, and provides support for resizing, showing and hiding, focusing, and other functionality related to windowing and composition.</span></span>

## <span data-ttu-id="64f91-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="64f91-106">Summary</span></span>

 <span data-ttu-id="64f91-107">Участников</span><span class="sxs-lookup"><span data-stu-id="64f91-107">Members</span></span>                        | <span data-ttu-id="64f91-108">Описания</span><span class="sxs-lookup"><span data-stu-id="64f91-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="64f91-109">get_IsVisible</span><span class="sxs-lookup"><span data-stu-id="64f91-109">get_IsVisible</span></span>](#get_isvisible) | <span data-ttu-id="64f91-110">Свойство Visible определяет, нужно ли отображать или скрывать WebView.</span><span class="sxs-lookup"><span data-stu-id="64f91-110">The IsVisible property determines whether to show or hide the webview.</span></span>
[<span data-ttu-id="64f91-111">put_IsVisible</span><span class="sxs-lookup"><span data-stu-id="64f91-111">put_IsVisible</span></span>](#put_isvisible) | <span data-ttu-id="64f91-112">Задайте свойство Visible.</span><span class="sxs-lookup"><span data-stu-id="64f91-112">Set the IsVisible property.</span></span>
[<span data-ttu-id="64f91-113">get_Bounds</span><span class="sxs-lookup"><span data-stu-id="64f91-113">get_Bounds</span></span>](#get_bounds) | <span data-ttu-id="64f91-114">Границы WebView.</span><span class="sxs-lookup"><span data-stu-id="64f91-114">The webview bounds.</span></span>
[<span data-ttu-id="64f91-115">put_Bounds</span><span class="sxs-lookup"><span data-stu-id="64f91-115">put_Bounds</span></span>](#put_bounds) | <span data-ttu-id="64f91-116">Задайте свойство Bounds.</span><span class="sxs-lookup"><span data-stu-id="64f91-116">Set the Bounds property.</span></span>
[<span data-ttu-id="64f91-117">get_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="64f91-117">get_ZoomFactor</span></span>](#get_zoomfactor) | <span data-ttu-id="64f91-118">Коэффициент масштабирования для WebView.</span><span class="sxs-lookup"><span data-stu-id="64f91-118">The zoom factor for the WebView.</span></span>
[<span data-ttu-id="64f91-119">put_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="64f91-119">put_ZoomFactor</span></span>](#put_zoomfactor) | <span data-ttu-id="64f91-120">Задайте свойство ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="64f91-120">Set the ZoomFactor property.</span></span>
[<span data-ttu-id="64f91-121">add_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="64f91-121">add_ZoomFactorChanged</span></span>](#add_zoomfactorchanged) | <span data-ttu-id="64f91-122">Добавьте обработчик событий для события ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="64f91-122">Add an event handler for the ZoomFactorChanged event.</span></span>
[<span data-ttu-id="64f91-123">remove_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="64f91-123">remove_ZoomFactorChanged</span></span>](#remove_zoomfactorchanged) | <span data-ttu-id="64f91-124">Удалите обработчик событий, добавленный ранее add_ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="64f91-124">Remove an event handler previously added with add_ZoomFactorChanged.</span></span>
[<span data-ttu-id="64f91-125">SetBoundsAndZoomFactor</span><span class="sxs-lookup"><span data-stu-id="64f91-125">SetBoundsAndZoomFactor</span></span>](#setboundsandzoomfactor) | <span data-ttu-id="64f91-126">Одновременное обновление границ и свойств ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="64f91-126">Update Bounds and ZoomFactor properties at the same time.</span></span>
[<span data-ttu-id="64f91-127">MoveFocus</span><span class="sxs-lookup"><span data-stu-id="64f91-127">MoveFocus</span></span>](#movefocus) | <span data-ttu-id="64f91-128">Перемещение фокуса в WebView.</span><span class="sxs-lookup"><span data-stu-id="64f91-128">Move focus into WebView.</span></span>
[<span data-ttu-id="64f91-129">add_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="64f91-129">add_MoveFocusRequested</span></span>](#add_movefocusrequested) | <span data-ttu-id="64f91-130">Добавьте обработчик событий для события MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="64f91-130">Add an event handler for the MoveFocusRequested event.</span></span>
[<span data-ttu-id="64f91-131">remove_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="64f91-131">remove_MoveFocusRequested</span></span>](#remove_movefocusrequested) | <span data-ttu-id="64f91-132">Удалите обработчик событий, добавленный ранее add_MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="64f91-132">Remove an event handler previously added with add_MoveFocusRequested.</span></span>
[<span data-ttu-id="64f91-133">add_GotFocus</span><span class="sxs-lookup"><span data-stu-id="64f91-133">add_GotFocus</span></span>](#add_gotfocus) | <span data-ttu-id="64f91-134">Добавьте обработчик событий для события GotFocus.</span><span class="sxs-lookup"><span data-stu-id="64f91-134">Add an event handler for the GotFocus event.</span></span>
[<span data-ttu-id="64f91-135">remove_GotFocus</span><span class="sxs-lookup"><span data-stu-id="64f91-135">remove_GotFocus</span></span>](#remove_gotfocus) | <span data-ttu-id="64f91-136">Удалите обработчик событий, добавленный ранее add_GotFocus.</span><span class="sxs-lookup"><span data-stu-id="64f91-136">Remove an event handler previously added with add_GotFocus.</span></span>
[<span data-ttu-id="64f91-137">add_LostFocus</span><span class="sxs-lookup"><span data-stu-id="64f91-137">add_LostFocus</span></span>](#add_lostfocus) | <span data-ttu-id="64f91-138">Добавьте обработчик для события LostFocus.</span><span class="sxs-lookup"><span data-stu-id="64f91-138">Add an event handler for the LostFocus event.</span></span>
[<span data-ttu-id="64f91-139">remove_LostFocus</span><span class="sxs-lookup"><span data-stu-id="64f91-139">remove_LostFocus</span></span>](#remove_lostfocus) | <span data-ttu-id="64f91-140">Удалите обработчик событий, добавленный ранее add_LostFocus.</span><span class="sxs-lookup"><span data-stu-id="64f91-140">Remove an event handler previously added with add_LostFocus.</span></span>
[<span data-ttu-id="64f91-141">add_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="64f91-141">add_AcceleratorKeyPressed</span></span>](#add_acceleratorkeypressed) | <span data-ttu-id="64f91-142">Добавьте обработчик событий для события AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="64f91-142">Add an event handler for the AcceleratorKeyPressed event.</span></span>
[<span data-ttu-id="64f91-143">remove_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="64f91-143">remove_AcceleratorKeyPressed</span></span>](#remove_acceleratorkeypressed) | <span data-ttu-id="64f91-144">Удалите обработчик событий, добавленный ранее add_AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="64f91-144">Remove an event handler previously added with add_AcceleratorKeyPressed.</span></span>
[<span data-ttu-id="64f91-145">get_ParentWindow</span><span class="sxs-lookup"><span data-stu-id="64f91-145">get_ParentWindow</span></span>](#get_parentwindow) | <span data-ttu-id="64f91-146">Родительское окно, предоставленное приложением, используемое этим WebView, для отрисовки содержимого.</span><span class="sxs-lookup"><span data-stu-id="64f91-146">The parent window provided by the app that this WebView is using to render content.</span></span>
[<span data-ttu-id="64f91-147">put_ParentWindow</span><span class="sxs-lookup"><span data-stu-id="64f91-147">put_ParentWindow</span></span>](#put_parentwindow) | <span data-ttu-id="64f91-148">Установка родительского окна для WebView.</span><span class="sxs-lookup"><span data-stu-id="64f91-148">Set the parent window for the WebView.</span></span>
[<span data-ttu-id="64f91-149">NotifyParentWindowPositionChanged</span><span class="sxs-lookup"><span data-stu-id="64f91-149">NotifyParentWindowPositionChanged</span></span>](#notifyparentwindowpositionchanged) | <span data-ttu-id="64f91-150">Это уведомление отделено от put_Bounds, которое указывает на то, что WebView родительский элемент HWND (или какой-либо его предок) переместился.</span><span class="sxs-lookup"><span data-stu-id="64f91-150">This is a notification separate from put_Bounds that tells WebView its parent (or any ancestor) HWND moved.</span></span>
[<span data-ttu-id="64f91-151">Close (закрыть)</span><span class="sxs-lookup"><span data-stu-id="64f91-151">Close</span></span>](#close) | <span data-ttu-id="64f91-152">Закрывает WebView и очищает основной экземпляр браузера.</span><span class="sxs-lookup"><span data-stu-id="64f91-152">Closes the WebView and cleans up the underlying browser instance.</span></span>
[<span data-ttu-id="64f91-153">get_CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="64f91-153">get_CoreWebView2</span></span>](#get_corewebview2) | <span data-ttu-id="64f91-154">Возвращает CoreWebView2, связанный с этим CoreWebView2Host.</span><span class="sxs-lookup"><span data-stu-id="64f91-154">Gets the CoreWebView2 associated with this CoreWebView2Host.</span></span>
[<span data-ttu-id="64f91-155">CORE_WEBVIEW2_MOVE_FOCUS_REASON</span><span class="sxs-lookup"><span data-stu-id="64f91-155">CORE_WEBVIEW2_MOVE_FOCUS_REASON</span></span>](#core_webview2_move_focus_reason) | <span data-ttu-id="64f91-156">Причина для перемещения фокуса.</span><span class="sxs-lookup"><span data-stu-id="64f91-156">Reason for moving focus.</span></span>
[<span data-ttu-id="64f91-157">CORE_WEBVIEW2_KEY_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="64f91-157">CORE_WEBVIEW2_KEY_EVENT_KIND</span></span>](#core_webview2_key_event_kind) | <span data-ttu-id="64f91-158">Тип события клавиши, которое инициировало событие AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="64f91-158">The type of key event that triggered an AcceleratorKeyPressed event.</span></span>
[<span data-ttu-id="64f91-159">CORE_WEBVIEW2_PHYSICAL_KEY_STATUS</span><span class="sxs-lookup"><span data-stu-id="64f91-159">CORE_WEBVIEW2_PHYSICAL_KEY_STATUS</span></span>](#core_webview2_physical_key_status) | <span data-ttu-id="64f91-160">Структура, представляющая данные, Упакованные в LPARAM, предоставленные событию ключа Win32.</span><span class="sxs-lookup"><span data-stu-id="64f91-160">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

<span data-ttu-id="64f91-161">CoreWebView2Host владеет CoreWebView2 и, если все ссылки на CoreWebView2Host выходит из него, WebView будет закрыт.</span><span class="sxs-lookup"><span data-stu-id="64f91-161">The CoreWebView2Host owns the CoreWebView2, and if all references to the CoreWebView2Host go away, the WebView will be closed.</span></span>

## <span data-ttu-id="64f91-162">Участников</span><span class="sxs-lookup"><span data-stu-id="64f91-162">Members</span></span>

#### <span data-ttu-id="64f91-163">get_IsVisible</span><span class="sxs-lookup"><span data-stu-id="64f91-163">get_IsVisible</span></span> 

<span data-ttu-id="64f91-164">Свойство Visible определяет, нужно ли отображать или скрывать WebView.</span><span class="sxs-lookup"><span data-stu-id="64f91-164">The IsVisible property determines whether to show or hide the webview.</span></span>

> <span data-ttu-id="64f91-165">общедоступные значения HRESULT [get_IsVisible](#get_isvisible)(bool \* Visible)</span><span class="sxs-lookup"><span data-stu-id="64f91-165">public HRESULT [get_IsVisible](#get_isvisible)(BOOL \* isVisible)</span></span>

<span data-ttu-id="64f91-166">Если для свойства Visible задано значение false, WebView будет прозрачным и не будет обрабатываться.</span><span class="sxs-lookup"><span data-stu-id="64f91-166">If IsVisible is set to false, the webview will be transparent and will not be rendered.</span></span> <span data-ttu-id="64f91-167">Однако это не повлияет на окно, содержащее WebView (параметр HWND, переданный в CreateCoreWebView2Host).</span><span class="sxs-lookup"><span data-stu-id="64f91-167">However, this will not affect the window containing the webview (the HWND parameter that was passed to CreateCoreWebView2Host).</span></span> <span data-ttu-id="64f91-168">Если вы хотите, чтобы окно не исчезало, вызовите для него функцию ShowWindow прямо в дополнение к изменению свойства Visible.</span><span class="sxs-lookup"><span data-stu-id="64f91-168">If you want that window to disappear too, call ShowWindow on it directly in addition to modifying the IsVisible property.</span></span> <span data-ttu-id="64f91-169">WebView — это дочернее окно не получает оконные сообщения, когда окно свертывания или восстановления находится в верхней части окна.</span><span class="sxs-lookup"><span data-stu-id="64f91-169">WebView as a child window won't get window messages when the top window is minimized or restored.</span></span> <span data-ttu-id="64f91-170">Для повышения производительности разработчик должен установить для свойства WebView значение false, если окно приложения свернуто, и вернуть значение true при восстановлении окна приложения.</span><span class="sxs-lookup"><span data-stu-id="64f91-170">For performance reason, developer should set IsVisible property of the WebView to false when the app window is minimized and back to true when app window is restored.</span></span> <span data-ttu-id="64f91-171">Это можно сделать, обрабатывая команды SC_MINIMIZE и SC_RESTORE при получении WM_SYSCOMMAND сообщения.</span><span class="sxs-lookup"><span data-stu-id="64f91-171">App window can do this by handling SC_MINIMIZE and SC_RESTORE command upon receiving WM_SYSCOMMAND message.</span></span>

```cpp
void ViewComponent::ToggleVisibility()
{
    BOOL visible;
    m_host->get_IsVisible(&visible);
    m_isVisible = !visible;
    m_host->put_IsVisible(m_isVisible);
}
```

#### <span data-ttu-id="64f91-172">put_IsVisible</span><span class="sxs-lookup"><span data-stu-id="64f91-172">put_IsVisible</span></span> 

<span data-ttu-id="64f91-173">Задайте свойство Visible.</span><span class="sxs-lookup"><span data-stu-id="64f91-173">Set the IsVisible property.</span></span>

> <span data-ttu-id="64f91-174">общедоступные значения HRESULT [put_IsVisible](#put_isvisible)(bool-Visible)</span><span class="sxs-lookup"><span data-stu-id="64f91-174">public HRESULT [put_IsVisible](#put_isvisible)(BOOL isVisible)</span></span>

```cpp
    if (message == WM_SYSCOMMAND)
    {
        if (wParam == SC_MINIMIZE)
        {
            // Hide the webview when the app window is minimized.
            m_host->put_IsVisible(FALSE);
        }
        else if (wParam == SC_RESTORE)
        {
            // When the app window is restored, show the webview
            // (unless the user has toggle visibility off).
            if (m_isVisible)
            {
                m_host->put_IsVisible(TRUE);
            }
        }
    }
```

#### <span data-ttu-id="64f91-175">get_Bounds</span><span class="sxs-lookup"><span data-stu-id="64f91-175">get_Bounds</span></span> 

<span data-ttu-id="64f91-176">Границы WebView.</span><span class="sxs-lookup"><span data-stu-id="64f91-176">The webview bounds.</span></span>

> <span data-ttu-id="64f91-177">общедоступные значения HRESULT [get_Bounds](#get_bounds)(границы Rect \*)</span><span class="sxs-lookup"><span data-stu-id="64f91-177">public HRESULT [get_Bounds](#get_bounds)(RECT \* bounds)</span></span>

<span data-ttu-id="64f91-178">Границы задаются относительно родительского дескриптора HWND.</span><span class="sxs-lookup"><span data-stu-id="64f91-178">Bounds are relative to the parent HWND.</span></span> <span data-ttu-id="64f91-179">Приложение может располагать WebView двумя способами:</span><span class="sxs-lookup"><span data-stu-id="64f91-179">The app has two ways it can position a WebView:</span></span>

1. <span data-ttu-id="64f91-180">Создание дочернего HWND, который является родительским дескриптором HWND WebView.</span><span class="sxs-lookup"><span data-stu-id="64f91-180">Create a child HWND that is the WebView parent HWND.</span></span> <span data-ttu-id="64f91-181">Расположите это окно в том месте, где должен быть WebView.</span><span class="sxs-lookup"><span data-stu-id="64f91-181">Position this window where the WebView should be.</span></span> <span data-ttu-id="64f91-182">В этом случае используйте (0, 0) для левого верхнего угла WebView Bound's (сдвиг).</span><span class="sxs-lookup"><span data-stu-id="64f91-182">In this case, use (0, 0) for the WebView's Bound's top left corner (the offset).</span></span>

1. <span data-ttu-id="64f91-183">Используйте окно самого высокого приложения в качестве родительского HWND WebView.</span><span class="sxs-lookup"><span data-stu-id="64f91-183">Use the app's top most window as the WebView parent HWND.</span></span> <span data-ttu-id="64f91-184">Задайте Bound's левый верхний угол WebView, чтобы WebView правильно расположиться в приложении.</span><span class="sxs-lookup"><span data-stu-id="64f91-184">Set the WebView's Bound's top left corner so that the WebView is positioned correctly in the app.</span></span> <span data-ttu-id="64f91-185">Значения границ находятся в пространстве координат основного приложения.</span><span class="sxs-lookup"><span data-stu-id="64f91-185">The Bound's values are in the host's coordinate space.</span></span>

#### <span data-ttu-id="64f91-186">put_Bounds</span><span class="sxs-lookup"><span data-stu-id="64f91-186">put_Bounds</span></span> 

<span data-ttu-id="64f91-187">Задайте свойство Bounds.</span><span class="sxs-lookup"><span data-stu-id="64f91-187">Set the Bounds property.</span></span>

> <span data-ttu-id="64f91-188">общедоступные значения HRESULT [put_Bounds](#put_bounds)(границы Rect)</span><span class="sxs-lookup"><span data-stu-id="64f91-188">public HRESULT [put_Bounds](#put_bounds)(RECT bounds)</span></span>

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

    m_host->put_Bounds(desiredBounds);
}
```

#### <span data-ttu-id="64f91-189">get_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="64f91-189">get_ZoomFactor</span></span> 

<span data-ttu-id="64f91-190">Коэффициент масштабирования для WebView.</span><span class="sxs-lookup"><span data-stu-id="64f91-190">The zoom factor for the WebView.</span></span>

> <span data-ttu-id="64f91-191">общедоступные значения HRESULT [get_ZoomFactor](#get_zoomfactor)(Double \* ZoomFactor)</span><span class="sxs-lookup"><span data-stu-id="64f91-191">public HRESULT [get_ZoomFactor](#get_zoomfactor)(double \* zoomFactor)</span></span>

<span data-ttu-id="64f91-192">Обратите внимание, что изменение коэффициента масштабирования может привести к `window.innerWidth/innerHeight` изменению масштаба страницы.</span><span class="sxs-lookup"><span data-stu-id="64f91-192">Note that changing zoom factor could cause `window.innerWidth/innerHeight` and page layout to change.</span></span> <span data-ttu-id="64f91-193">Коэффициент масштабирования, примененный ведущим приложением путем вызова put_ZoomFactor, становится новым масштабом по умолчанию для WebView.</span><span class="sxs-lookup"><span data-stu-id="64f91-193">A zoom factor that is applied by the host by calling put_ZoomFactor becomes the new default zoom for the WebView.</span></span> <span data-ttu-id="64f91-194">Этот коэффициент масштабирования применяется для всех переходов и — коэффициент масштабирования WebView возвращается, когда пользователь нажимает клавиши CTRL + 0.</span><span class="sxs-lookup"><span data-stu-id="64f91-194">This zoom factor applies across navigations and is the zoom factor WebView is returned to when the user presses ctrl+0.</span></span> <span data-ttu-id="64f91-195">При изменении коэффициента масштабирования пользователем (в результате использования приложения, получающего ZoomFactorChanged) это масштабирование применяется только к текущей странице.</span><span class="sxs-lookup"><span data-stu-id="64f91-195">When the zoom factor is changed by the user (resulting in the app receiving ZoomFactorChanged), that zoom applies only for the current page.</span></span> <span data-ttu-id="64f91-196">Любой пользователь, который применяет масштабирование, используется только для текущей страницы и сбрасывается на панели навигации.</span><span class="sxs-lookup"><span data-stu-id="64f91-196">Any user applied zoom is only for the current page and is reset on a navigation.</span></span> <span data-ttu-id="64f91-197">Указывать zoomFactor меньше или равно 0 не разрешается.</span><span class="sxs-lookup"><span data-stu-id="64f91-197">Specifying a zoomFactor less than or equal to 0 is not allowed.</span></span> <span data-ttu-id="64f91-198">WebView также имеет внутренний поддерживаемый диапазон коэффициента масштабирования.</span><span class="sxs-lookup"><span data-stu-id="64f91-198">WebView also has an internal supported zoom factor range.</span></span> <span data-ttu-id="64f91-199">Если указанный коэффициент масштаба выходит за пределы этого диапазона, он будет нормализован в пределах диапазона, а событие ZoomFactorChanged будет инициировано для фактического коэффициента масштабирования.</span><span class="sxs-lookup"><span data-stu-id="64f91-199">When a specified zoom factor is out of that range, it will be normalized to be within the range, and a ZoomFactorChanged event will be fired for the real applied zoom factor.</span></span> <span data-ttu-id="64f91-200">При выполнении этой нормализации диапазона свойство ZoomFactor будет указывать коэффициент масштабирования, указанный в предыдущем изменении свойства ZoomFactor, пока событие ZoomFactorChanged не будет получено после WebView применяет нормализованный коэффициент масштабирования.</span><span class="sxs-lookup"><span data-stu-id="64f91-200">When this range normalization happens, the ZoomFactor property will report the zoom factor specified during the previous modification of the ZoomFactor property until the ZoomFactorChanged event is received after webview applies the normalized zoom factor.</span></span>

#### <span data-ttu-id="64f91-201">put_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="64f91-201">put_ZoomFactor</span></span> 

<span data-ttu-id="64f91-202">Задайте свойство ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="64f91-202">Set the ZoomFactor property.</span></span>

> <span data-ttu-id="64f91-203">общедоступный [PUT_ZOOMFACTOR](#put_zoomfactor)HRESULT (двойной ZoomFactor)</span><span class="sxs-lookup"><span data-stu-id="64f91-203">public HRESULT [put_ZoomFactor](#put_zoomfactor)(double zoomFactor)</span></span>

#### <span data-ttu-id="64f91-204">add_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="64f91-204">add_ZoomFactorChanged</span></span> 

<span data-ttu-id="64f91-205">Добавьте обработчик событий для события ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="64f91-205">Add an event handler for the ZoomFactorChanged event.</span></span>

> <span data-ttu-id="64f91-206">общедоступные значения HRESULT [add_ZoomFactorChanged](#add_zoomfactorchanged)([ICoreWebView2ZoomFactorChangedEventHandler](ICoreWebView2ZoomFactorChangedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="64f91-206">public HRESULT [add_ZoomFactorChanged](#add_zoomfactorchanged)([ICoreWebView2ZoomFactorChangedEventHandler](ICoreWebView2ZoomFactorChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="64f91-207">Событие срабатывает, когда изменяется свойство ZoomFactor объекта WebView.</span><span class="sxs-lookup"><span data-stu-id="64f91-207">The event fires when the ZoomFactor property of the WebView changes.</span></span> <span data-ttu-id="64f91-208">Событие может срабатывать из-за того, что вызывающий объект изменил свойство ZoomFactor или пользователь вручную изменял масштаб.</span><span class="sxs-lookup"><span data-stu-id="64f91-208">The event could fire because the caller modified the ZoomFactor property, or due to the user manually modifying the zoom.</span></span> <span data-ttu-id="64f91-209">При изменении вызывающим абонентом с помощью свойства ZoomFactor внутренний коэффициент масштабирования немедленно обновляется, и событие ZoomFactorChanged не выводится.</span><span class="sxs-lookup"><span data-stu-id="64f91-209">When it is modified by the caller via the ZoomFactor property, the internal zoom factor is updated immediately and there will be no ZoomFactorChanged event.</span></span> <span data-ttu-id="64f91-210">WebView связывает последний использованный коэффициент масштабирования для каждого сайта.</span><span class="sxs-lookup"><span data-stu-id="64f91-210">WebView associates the last used zoom factor for each site.</span></span> <span data-ttu-id="64f91-211">Поэтому коэффициент масштабирования может изменяться при переходе на другую страницу.</span><span class="sxs-lookup"><span data-stu-id="64f91-211">Therefore, it is possible for the zoom factor to change when navigating to a different page.</span></span> <span data-ttu-id="64f91-212">При изменении коэффициента масштабирования из-за этого событие ZoomFactorChanged срабатывает сразу после события ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="64f91-212">When the zoom factor changes due to this, the ZoomFactorChanged event fires right after the ContentLoading event.</span></span>

```cpp
    // Register a handler for the ZoomFactorChanged event.
    // This handler just announces the new level of zoom on the window's title bar.
    CHECK_FAILURE(m_host->add_ZoomFactorChanged(
        Callback<ICoreWebView2ZoomFactorChangedEventHandler>(
            [this](ICoreWebView2Host* sender, IUnknown* args) -> HRESULT {
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

#### <span data-ttu-id="64f91-213">remove_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="64f91-213">remove_ZoomFactorChanged</span></span> 

<span data-ttu-id="64f91-214">Удалите обработчик событий, добавленный ранее add_ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="64f91-214">Remove an event handler previously added with add_ZoomFactorChanged.</span></span>

> <span data-ttu-id="64f91-215">общедоступные значения HRESULT [remove_ZoomFactorChanged](#remove_zoomfactorchanged)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="64f91-215">public HRESULT [remove_ZoomFactorChanged](#remove_zoomfactorchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="64f91-216">SetBoundsAndZoomFactor</span><span class="sxs-lookup"><span data-stu-id="64f91-216">SetBoundsAndZoomFactor</span></span> 

<span data-ttu-id="64f91-217">Одновременное обновление границ и свойств ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="64f91-217">Update Bounds and ZoomFactor properties at the same time.</span></span>

> <span data-ttu-id="64f91-218">общедоступные значения HRESULT [SetBoundsAndZoomFactor](#setboundsandzoomfactor)(границы Rect, Double zoomFactor)</span><span class="sxs-lookup"><span data-stu-id="64f91-218">public HRESULT [SetBoundsAndZoomFactor](#setboundsandzoomfactor)(RECT bounds,double zoomFactor)</span></span>

<span data-ttu-id="64f91-219">Эта операция является атомарной из perspecive узла.</span><span class="sxs-lookup"><span data-stu-id="64f91-219">This operation is atomic from the host's perspecive.</span></span> <span data-ttu-id="64f91-220">После того как вы вернете эту функцию, свойства Bounds и ZoomFactor будут обновлены при успешном выполнении функции, или ни один из них не будет обновляться при сбое функции.</span><span class="sxs-lookup"><span data-stu-id="64f91-220">After returning from this function, the Bounds and ZoomFactor properties will have both been updated if the function is successful, or neither will be updated if the function fails.</span></span> <span data-ttu-id="64f91-221">Если границы и ZoomFactor обновляются одним масштабом (то есть границы и ZoomFactor оба двойных), то страница не будет видеть изменение в Window. innerWidth/innerHeight, а WebView будет отображать содержимое на новом размере и масштабе без промежуточных преобразований.</span><span class="sxs-lookup"><span data-stu-id="64f91-221">If Bounds and ZoomFactor are both updated by the same scale (i.e. Bounds and ZoomFactor are both doubled), then the page will not see a change in window.innerWidth/innerHeight and the WebView will render the content at the new size and zoom without intermediate renderings.</span></span> <span data-ttu-id="64f91-222">Эта функция также может использоваться для обновления только одного из ZoomFactor или границ путем передачи нового значения для одного и текущего значения другого.</span><span class="sxs-lookup"><span data-stu-id="64f91-222">This function can also be used to update just one of ZoomFactor or Bounds by passing in the new value for one and the current value for the other.</span></span>

```cpp
void ViewComponent::SetScale(float scale)
{
    RECT bounds;
    CHECK_FAILURE(m_host->get_Bounds(&bounds));
    double scaleChange = scale / m_webViewScale;

    bounds.bottom = LONG(
        (bounds.bottom - bounds.top) * scaleChange + bounds.top);
    bounds.right = LONG(
        (bounds.right - bounds.left) * scaleChange + bounds.left);

    m_webViewScale = scale;
    m_host->SetBoundsAndZoomFactor(bounds, scale);
}
```

#### <span data-ttu-id="64f91-223">MoveFocus</span><span class="sxs-lookup"><span data-stu-id="64f91-223">MoveFocus</span></span> 

<span data-ttu-id="64f91-224">Перемещение фокуса в WebView.</span><span class="sxs-lookup"><span data-stu-id="64f91-224">Move focus into WebView.</span></span>

> <span data-ttu-id="64f91-225">общедоступные значения HRESULT [MoveFocus](#movefocus)(причина[CORE_WEBVIEW2_MOVE_FOCUS_REASON](#core_webview2_move_focus_reason) )</span><span class="sxs-lookup"><span data-stu-id="64f91-225">public HRESULT [MoveFocus](#movefocus)([CORE_WEBVIEW2_MOVE_FOCUS_REASON](#core_webview2_move_focus_reason) reason)</span></span>

<span data-ttu-id="64f91-226">WebView получит фокус, и фокус будет установлен на элемент корреспондента на странице, которая размещена в WebView.</span><span class="sxs-lookup"><span data-stu-id="64f91-226">WebView will get focus and focus will be set to correspondent element in the page hosted in the WebView.</span></span> <span data-ttu-id="64f91-227">В целях программной причины фокус установлен на ранее сфокусированный элемент или элемент по умолчанию, если нет ранее фокусируемого элемента.</span><span class="sxs-lookup"><span data-stu-id="64f91-227">For Programmatic reason, focus is set to previously focused element or the default element if there is no previously focused element.</span></span> <span data-ttu-id="64f91-228">В следующей причине фокус задается для первого элемента.</span><span class="sxs-lookup"><span data-stu-id="64f91-228">For Next reason, focus is set to the first element.</span></span> <span data-ttu-id="64f91-229">По этой причине фокус установлен на последний элемент.</span><span class="sxs-lookup"><span data-stu-id="64f91-229">For Previous reason, focus is set to the last element.</span></span> <span data-ttu-id="64f91-230">WebView также может сосредоточиться на взаимодействии с пользователем, например, щелкнув на WebView или TAB.</span><span class="sxs-lookup"><span data-stu-id="64f91-230">WebView can also got focus through user interaction like clicking into WebView or Tab into it.</span></span> <span data-ttu-id="64f91-231">Для табуляции приложение может вызвать MoveFocus с помощью кнопки Далее или назад, чтобы выровнять элементы Tab и SHIFT + TAB, если это необходимо, если WebView является следующим элементом с вкладками.</span><span class="sxs-lookup"><span data-stu-id="64f91-231">For tabbing, the app can call MoveFocus with Next or Previous to align with tab and shift+tab respectively when it decides the WebView is the next tabbable element.</span></span> <span data-ttu-id="64f91-232">Кроме того, приложение может вызвать IsDialogMessage как часть цикла обработки сообщений, чтобы платформа автоматически обрабатывала табуляцию.</span><span class="sxs-lookup"><span data-stu-id="64f91-232">Or, the app can call IsDialogMessage as part of its message loop to allow the platform to auto handle tabbing.</span></span> <span data-ttu-id="64f91-233">Платформа будет повернута на все окна с помощью WS_TABSTOP.</span><span class="sxs-lookup"><span data-stu-id="64f91-233">The platform will rotate through all windows with WS_TABSTOP.</span></span> <span data-ttu-id="64f91-234">Когда WebView получает фокус из IsDialogMessage, он будет внутренне размещать фокус на первом или последнем элементе Tab и Shift + Tab соответственно.</span><span class="sxs-lookup"><span data-stu-id="64f91-234">When the WebView gets focus from IsDialogMessage, it will internally put the focus on the first or last element for tab and shift+tab respectively.</span></span>

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
            for (int i = 0; i < m_tabbableWindows.size(); i++)
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
    for (int i = currentIndex + 1; i < m_tabbableWindows.size(); i++)
    {
        HWND hwnd = m_tabbableWindows.at(i).first;
        if (IsWindowEnabled(hwnd))
        {
            SetFocus(hwnd);
            return;
        }
    }
    // If this is the last enabled window, tab forwards into the WebView.
    m_host->MoveFocus(CORE_WEBVIEW2_MOVE_FOCUS_REASON_NEXT);
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
    CHECK_FAILURE(m_host->MoveFocus(CORE_WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS));
}
```

#### <span data-ttu-id="64f91-235">add_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="64f91-235">add_MoveFocusRequested</span></span> 

<span data-ttu-id="64f91-236">Добавьте обработчик событий для события MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="64f91-236">Add an event handler for the MoveFocusRequested event.</span></span>

> <span data-ttu-id="64f91-237">общедоступные значения HRESULT [add_MoveFocusRequested](#add_movefocusrequested)([ICoreWebView2MoveFocusRequestedEventHandler](ICoreWebView2MoveFocusRequestedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="64f91-237">public HRESULT [add_MoveFocusRequested](#add_movefocusrequested)([ICoreWebView2MoveFocusRequestedEventHandler](ICoreWebView2MoveFocusRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="64f91-238">MoveFocusRequested активируется, когда пользователь пытается выполнить переход из WebView.</span><span class="sxs-lookup"><span data-stu-id="64f91-238">MoveFocusRequested fires when user tries to tab out of the WebView.</span></span> <span data-ttu-id="64f91-239">При срабатывании этого события фокус WebView не изменился.</span><span class="sxs-lookup"><span data-stu-id="64f91-239">The WebView's focus has not changed when this event is fired.</span></span>

```cpp
    // Register a handler for the MoveFocusRequested event.
    // This event will be fired when the user tabs out of the webview.
    // The handler will focus another window in the app, depending on which
    // direction the focus is being shifted.
    CHECK_FAILURE(m_host->add_MoveFocusRequested(
        Callback<ICoreWebView2MoveFocusRequestedEventHandler>(
            [this](
                ICoreWebView2Host* sender,
                ICoreWebView2MoveFocusRequestedEventArgs* args) -> HRESULT {
                if (!g_autoTabHandle)
                {
                    CORE_WEBVIEW2_MOVE_FOCUS_REASON reason;
                    CHECK_FAILURE(args->get_Reason(&reason));

                    if (reason == CORE_WEBVIEW2_MOVE_FOCUS_REASON_NEXT)
                    {
                        TabForwards(-1);
                    }
                    else if (reason == CORE_WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS)
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

#### <span data-ttu-id="64f91-240">remove_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="64f91-240">remove_MoveFocusRequested</span></span> 

<span data-ttu-id="64f91-241">Удалите обработчик событий, добавленный ранее add_MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="64f91-241">Remove an event handler previously added with add_MoveFocusRequested.</span></span>

> <span data-ttu-id="64f91-242">общедоступные значения HRESULT [remove_MoveFocusRequested](#remove_movefocusrequested)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="64f91-242">public HRESULT [remove_MoveFocusRequested](#remove_movefocusrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="64f91-243">add_GotFocus</span><span class="sxs-lookup"><span data-stu-id="64f91-243">add_GotFocus</span></span> 

<span data-ttu-id="64f91-244">Добавьте обработчик событий для события GotFocus.</span><span class="sxs-lookup"><span data-stu-id="64f91-244">Add an event handler for the GotFocus event.</span></span>

> <span data-ttu-id="64f91-245">общедоступные значения HRESULT [add_GotFocus](#add_gotfocus)([ICoreWebView2FocusChangedEventHandler](ICoreWebView2FocusChangedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="64f91-245">public HRESULT [add_GotFocus](#add_gotfocus)([ICoreWebView2FocusChangedEventHandler](ICoreWebView2FocusChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="64f91-246">Получение фокуса срабатывает, когда WebView получил фокусировку.</span><span class="sxs-lookup"><span data-stu-id="64f91-246">GotFocus fires when WebView got focus.</span></span>

#### <span data-ttu-id="64f91-247">remove_GotFocus</span><span class="sxs-lookup"><span data-stu-id="64f91-247">remove_GotFocus</span></span> 

<span data-ttu-id="64f91-248">Удалите обработчик событий, добавленный ранее add_GotFocus.</span><span class="sxs-lookup"><span data-stu-id="64f91-248">Remove an event handler previously added with add_GotFocus.</span></span>

> <span data-ttu-id="64f91-249">общедоступные значения HRESULT [remove_GotFocus](#remove_gotfocus)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="64f91-249">public HRESULT [remove_GotFocus](#remove_gotfocus)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="64f91-250">add_LostFocus</span><span class="sxs-lookup"><span data-stu-id="64f91-250">add_LostFocus</span></span> 

<span data-ttu-id="64f91-251">Добавьте обработчик для события LostFocus.</span><span class="sxs-lookup"><span data-stu-id="64f91-251">Add an event handler for the LostFocus event.</span></span>

> <span data-ttu-id="64f91-252">общедоступные значения HRESULT [add_LostFocus](#add_lostfocus)([ICoreWebView2FocusChangedEventHandler](ICoreWebView2FocusChangedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="64f91-252">public HRESULT [add_LostFocus](#add_lostfocus)([ICoreWebView2FocusChangedEventHandler](ICoreWebView2FocusChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="64f91-253">LostFocus вызывается, когда WebView теряет фокус.</span><span class="sxs-lookup"><span data-stu-id="64f91-253">LostFocus fires when WebView lost focus.</span></span> <span data-ttu-id="64f91-254">В случае, если возникает событие MoveFocusRequested, фокус по-прежнему находится в WebView при срабатывании события MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="64f91-254">In the case where MoveFocusRequested event is fired, the focus is still on WebView when MoveFocusRequested event fires.</span></span> <span data-ttu-id="64f91-255">Потерянный фокус срабатывает только в том случае, если код приложения или действие по умолчанию, заданное MoveFocusRequested события, задали фокус от WebView.</span><span class="sxs-lookup"><span data-stu-id="64f91-255">Lost focus only fires afterwards when app's code or default action of MoveFocusRequested event set focus away from WebView.</span></span>

#### <span data-ttu-id="64f91-256">remove_LostFocus</span><span class="sxs-lookup"><span data-stu-id="64f91-256">remove_LostFocus</span></span> 

<span data-ttu-id="64f91-257">Удалите обработчик событий, добавленный ранее add_LostFocus.</span><span class="sxs-lookup"><span data-stu-id="64f91-257">Remove an event handler previously added with add_LostFocus.</span></span>

> <span data-ttu-id="64f91-258">общедоступные значения HRESULT [remove_LostFocus](#remove_lostfocus)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="64f91-258">public HRESULT [remove_LostFocus](#remove_lostfocus)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="64f91-259">add_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="64f91-259">add_AcceleratorKeyPressed</span></span> 

<span data-ttu-id="64f91-260">Добавьте обработчик событий для события AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="64f91-260">Add an event handler for the AcceleratorKeyPressed event.</span></span>

> <span data-ttu-id="64f91-261">общедоступные значения HRESULT [add_AcceleratorKeyPressed](#add_acceleratorkeypressed)([ICoreWebView2AcceleratorKeyPressedEventHandler](ICoreWebView2AcceleratorKeyPressedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="64f91-261">public HRESULT [add_AcceleratorKeyPressed](#add_acceleratorkeypressed)([ICoreWebView2AcceleratorKeyPressedEventHandler](ICoreWebView2AcceleratorKeyPressedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="64f91-262">AcceleratorKeyPressed активируется при нажатии или отпускании клавиши сочетания клавиш в том случае, если WebView имеет фокус.</span><span class="sxs-lookup"><span data-stu-id="64f91-262">AcceleratorKeyPressed fires when an accelerator key or key combo is pressed or released while the WebView is focused.</span></span> <span data-ttu-id="64f91-263">Клавиша считается ускорителем по одной из следующих способов:</span><span class="sxs-lookup"><span data-stu-id="64f91-263">A key is considered an accelerator if either:</span></span>

1. <span data-ttu-id="64f91-264">В данный момент удерживается клавиша CTRL или ALT;</span><span class="sxs-lookup"><span data-stu-id="64f91-264">Ctrl or Alt is currently being held, or</span></span>

1. <span data-ttu-id="64f91-265">Нажатая клавиша не сопоставляется с символом.</span><span class="sxs-lookup"><span data-stu-id="64f91-265">the pressed key does not map to a character.</span></span> <span data-ttu-id="64f91-266">Некоторые неопределенные клавиши никогда не рассматриваются как ускорители, например Shift.</span><span class="sxs-lookup"><span data-stu-id="64f91-266">A few specific keys are never considered accelerators, such as Shift.</span></span> <span data-ttu-id="64f91-267">Клавиша ESC всегда считается ускорителем.</span><span class="sxs-lookup"><span data-stu-id="64f91-267">The Escape key is always considered an accelerator.</span></span>

<span data-ttu-id="64f91-268">Событие с автоматическим нажатием клавиши, вызванное удерживанием нажатой клавиши, также срабатывает.</span><span class="sxs-lookup"><span data-stu-id="64f91-268">Autorepeated key events caused by holding the key down will also fire this event.</span></span> <span data-ttu-id="64f91-269">Чтобы отфильтровать эти данные, Проверьте аргументы события "KeyEventLParam" или "PhysicalKeyStatus".</span><span class="sxs-lookup"><span data-stu-id="64f91-269">You can filter these out by checking the event args' KeyEventLParam or PhysicalKeyStatus.</span></span>

<span data-ttu-id="64f91-270">В оконном режиме этот обработчик событий вызывается синхронно.</span><span class="sxs-lookup"><span data-stu-id="64f91-270">In windowed mode, this event handler is called synchronously.</span></span> <span data-ttu-id="64f91-271">До тех пор пока вы не вызываете Handle () для аргументов события или не будет возвращен обработчик событий, процесс браузера будет заблокирован и исходящие межпроцессные вызовы COM не будут работать с RPC_E_CANTCALLOUT_ININPUTSYNCCALL.</span><span class="sxs-lookup"><span data-stu-id="64f91-271">Until you call Handle() on the event args or the event handler returns, the browser process will be blocked and outgoing cross-process COM calls will fail with RPC_E_CANTCALLOUT_ININPUTSYNCCALL.</span></span> <span data-ttu-id="64f91-272">Однако все методы API CoreWebView2 будут работать.</span><span class="sxs-lookup"><span data-stu-id="64f91-272">All CoreWebView2 API methods will work, however.</span></span>

<span data-ttu-id="64f91-273">В режиме безоконный обработчик событий вызывается асинхронно.</span><span class="sxs-lookup"><span data-stu-id="64f91-273">In windowless mode, the event handler is called asynchronously.</span></span> <span data-ttu-id="64f91-274">Дальнейшие входные данные не доходят до браузера, пока обработчик событий не возвратит или не завершит вызов (), но сам процесс браузера не будет заблокирован, а исходящие вызовы COM будут работать нормально.</span><span class="sxs-lookup"><span data-stu-id="64f91-274">Further input will not reach the browser until the event handler returns or Handle() is called, but the browser process itself will not be blocked, and outgoing COM calls will work normally.</span></span>

<span data-ttu-id="64f91-275">Рекомендуется, чтобы вы могли узнать, что вы хотите обрабатывать клавишу быстрого вызова (TRUE), как и раньше.</span><span class="sxs-lookup"><span data-stu-id="64f91-275">It is recommended to call Handle(TRUE) as early as you can know that you want to handle the accelerator key.</span></span>

```cpp
    // Register a handler for the AcceleratorKeyPressed event.
    CHECK_FAILURE(m_host->add_AcceleratorKeyPressed(
        Callback<ICoreWebView2AcceleratorKeyPressedEventHandler>(
            [this](
                ICoreWebView2Host* sender,
                ICoreWebView2AcceleratorKeyPressedEventArgs* args) -> HRESULT {
                CORE_WEBVIEW2_KEY_EVENT_KIND kind;
                CHECK_FAILURE(args->get_KeyEventKind(&kind));
                // We only care about key down events.
                if (kind == CORE_WEBVIEW2_KEY_EVENT_KIND_KEY_DOWN ||
                    kind == CORE_WEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_DOWN)
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
                        CORE_WEBVIEW2_PHYSICAL_KEY_STATUS status;
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

#### <span data-ttu-id="64f91-276">remove_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="64f91-276">remove_AcceleratorKeyPressed</span></span> 

<span data-ttu-id="64f91-277">Удалите обработчик событий, добавленный ранее add_AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="64f91-277">Remove an event handler previously added with add_AcceleratorKeyPressed.</span></span>

> <span data-ttu-id="64f91-278">общедоступные значения HRESULT [remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="64f91-278">public HRESULT [remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="64f91-279">get_ParentWindow</span><span class="sxs-lookup"><span data-stu-id="64f91-279">get_ParentWindow</span></span> 

<span data-ttu-id="64f91-280">Родительское окно, предоставленное приложением, используемое этим WebView, для отрисовки содержимого.</span><span class="sxs-lookup"><span data-stu-id="64f91-280">The parent window provided by the app that this WebView is using to render content.</span></span>

> <span data-ttu-id="64f91-281">общедоступные значения HRESULT [get_ParentWindow](#get_parentwindow)(HWND \* topLevelWindow)</span><span class="sxs-lookup"><span data-stu-id="64f91-281">public HRESULT [get_ParentWindow](#get_parentwindow)(HWND \* topLevelWindow)</span></span>

<span data-ttu-id="64f91-282">Этот API первоначально возвращает окно, передаваемое в CreateCoreWebView2Host.</span><span class="sxs-lookup"><span data-stu-id="64f91-282">This API initially returns the window passed into CreateCoreWebView2Host.</span></span>

#### <span data-ttu-id="64f91-283">put_ParentWindow</span><span class="sxs-lookup"><span data-stu-id="64f91-283">put_ParentWindow</span></span> 

<span data-ttu-id="64f91-284">Установка родительского окна для WebView.</span><span class="sxs-lookup"><span data-stu-id="64f91-284">Set the parent window for the WebView.</span></span>

> <span data-ttu-id="64f91-285">общедоступные значения HRESULT [put_ParentWindow](#put_parentwindow)(HWND topLevelWindow)</span><span class="sxs-lookup"><span data-stu-id="64f91-285">public HRESULT [put_ParentWindow](#put_parentwindow)(HWND topLevelWindow)</span></span>

<span data-ttu-id="64f91-286">Это приведет к тому, что WebView перестанет достать родительским окном до вновь заданной окна.</span><span class="sxs-lookup"><span data-stu-id="64f91-286">This will cause the WebView to reparent its window to the newly provided window.</span></span>

#### <span data-ttu-id="64f91-287">NotifyParentWindowPositionChanged</span><span class="sxs-lookup"><span data-stu-id="64f91-287">NotifyParentWindowPositionChanged</span></span> 

<span data-ttu-id="64f91-288">Это уведомление отделено от put_Bounds, которое указывает на то, что WebView родительский элемент HWND (или какой-либо его предок) переместился.</span><span class="sxs-lookup"><span data-stu-id="64f91-288">This is a notification separate from put_Bounds that tells WebView its parent (or any ancestor) HWND moved.</span></span>

> <span data-ttu-id="64f91-289">общедоступные значения HRESULT [NotifyParentWindowPositionChanged](#notifyparentwindowpositionchanged)()</span><span class="sxs-lookup"><span data-stu-id="64f91-289">public HRESULT [NotifyParentWindowPositionChanged](#notifyparentwindowpositionchanged)()</span></span>

<span data-ttu-id="64f91-290">Это необходимо для правильной работы специальных возможностей и некоторых диалоговых окон в WebView.</span><span class="sxs-lookup"><span data-stu-id="64f91-290">This is needed for accessibility and certain dialogs in WebView to work correctly.</span></span> 

```cpp
    if (message == WM_MOVE || message == WM_MOVING)
    {
        m_host->NotifyParentWindowPositionChanged();
        return true;
    }
```

#### <span data-ttu-id="64f91-291">Close (закрыть)</span><span class="sxs-lookup"><span data-stu-id="64f91-291">Close</span></span> 

<span data-ttu-id="64f91-292">Закрывает WebView и очищает основной экземпляр браузера.</span><span class="sxs-lookup"><span data-stu-id="64f91-292">Closes the WebView and cleans up the underlying browser instance.</span></span>

> <span data-ttu-id="64f91-293">общедоступное значение HRESULT [Close](#close)()</span><span class="sxs-lookup"><span data-stu-id="64f91-293">public HRESULT [Close](#close)()</span></span>

<span data-ttu-id="64f91-294">Очистка браузера instace освобождает ресурсы, переключающие WebView.</span><span class="sxs-lookup"><span data-stu-id="64f91-294">Cleaning up the browser instace will release the resources powering the WebView.</span></span> <span data-ttu-id="64f91-295">Экземпляр браузера будет закрыт, если он не используется другими веб – представлениями.</span><span class="sxs-lookup"><span data-stu-id="64f91-295">The browser instance will be shut down if there are no other WebViews using it.</span></span>

<span data-ttu-id="64f91-296">После вызова метода Close все вызовы методов завершатся сбоем, и обработчики событий прекратятся.</span><span class="sxs-lookup"><span data-stu-id="64f91-296">After calling Close, all method calls will fail and event handlers will stop firing.</span></span> <span data-ttu-id="64f91-297">В частности, WebView будет освобождать ссылки на обработчики событий при вызове Close.</span><span class="sxs-lookup"><span data-stu-id="64f91-297">Specifically, the WebView will release its references to its event handlers when Close is called.</span></span>

<span data-ttu-id="64f91-298">Метод Close вызывается неявно, когда CoreWebView2Host теряет свою конечную ссылку и является независимым.</span><span class="sxs-lookup"><span data-stu-id="64f91-298">Close is implicitly called when the CoreWebView2Host loses its final reference and is destructed.</span></span> <span data-ttu-id="64f91-299">Но рекомендуется явным образом вызывать метод Close, чтобы избежать случайного цикла ссылок между WebView и кодом приложения.</span><span class="sxs-lookup"><span data-stu-id="64f91-299">But it is best practice to explicitly call Close to avoid any accidental cycle of references between the WebView and the app code.</span></span> <span data-ttu-id="64f91-300">В частности, если вы захватываете ссылку на WebView в обработчике событий, вы создадите цикл ссылки между WebView и обработчиком событий.</span><span class="sxs-lookup"><span data-stu-id="64f91-300">Specifically, if you capture a reference to the WebView in an event handler you will create a reference cycle between the WebView and the event handler.</span></span> <span data-ttu-id="64f91-301">Вызов Close приведет к прерыванию этого цикла, освобождая все обработчики событий.</span><span class="sxs-lookup"><span data-stu-id="64f91-301">Calling Close will break this cycle by releasing all event handlers.</span></span> <span data-ttu-id="64f91-302">Но чтобы избежать такой ситуации, рекомендуется как явным образом вызвать метод Close для WebView и не захватить ссылку на WebView, чтобы убедиться, что WebView может быть корректно очищено.</span><span class="sxs-lookup"><span data-stu-id="64f91-302">But to avoid this situation it is best practice both to explicitly call Close on the WebView and to not capture a reference to the WebView to ensure the WebView can be cleaned up correctly.</span></span>

```cpp
// Close the WebView and deinitialize related state. This doesn't close the app window.
void AppWindow::CloseWebView(bool cleanupUserDataFolder)
{
    DeleteAllComponents();
    if (m_host)
    {
        m_host->Close();
        m_host = nullptr;
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
        // https://docs.microsoft.com/microsoft-edge/hosting/webview2/reference/win32/0-9-488/webview2.idl#createwebview2environmentwithdetails
        WCHAR userDataFolder[MAX_PATH] = L"";
        // Obtain the absolute path for relative paths that include "./" or "../"
        _wfullpath(
            userDataFolder, GetLocalPath(L"WebView2APISample.exe.WebView2").c_str(), MAX_PATH);
        std::wstring userDataFolderPath(userDataFolder);

        std::wstring message = L"Are you sure you want to clean up the user data folder at\n";
        message += userDataFolderPath;
        message += L"\n?\nWarning: This action is not reversible.\n\n";
        message += L"Click No if there are other open WebView instnaces.\n";

        if (MessageBox(m_mainWindow, message.c_str(), L"Cleanup User Data Folder", MB_YESNO) ==
            IDYES)
        {
            CHECK_FAILURE(DeleteFileRecursive(userDataFolderPath));
        }
    }
}
```

#### <span data-ttu-id="64f91-303">get_CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="64f91-303">get_CoreWebView2</span></span> 

<span data-ttu-id="64f91-304">Возвращает CoreWebView2, связанный с этим CoreWebView2Host.</span><span class="sxs-lookup"><span data-stu-id="64f91-304">Gets the CoreWebView2 associated with this CoreWebView2Host.</span></span>

> <span data-ttu-id="64f91-305">общедоступные значения HRESULT [get_CoreWebView2](#get_corewebview2)([ICoreWebView2](ICoreWebView2.md) \* \* CoreWebView2)</span><span class="sxs-lookup"><span data-stu-id="64f91-305">public HRESULT [get_CoreWebView2](#get_corewebview2)([ICoreWebView2](ICoreWebView2.md) \*\* coreWebView2)</span></span>

#### <span data-ttu-id="64f91-306">CORE_WEBVIEW2_MOVE_FOCUS_REASON</span><span class="sxs-lookup"><span data-stu-id="64f91-306">CORE_WEBVIEW2_MOVE_FOCUS_REASON</span></span> 

<span data-ttu-id="64f91-307">Причина для перемещения фокуса.</span><span class="sxs-lookup"><span data-stu-id="64f91-307">Reason for moving focus.</span></span>

> <span data-ttu-id="64f91-308">[CORE_WEBVIEW2_MOVE_FOCUS_REASON](#core_webview2_move_focus_reason) перечисления</span><span class="sxs-lookup"><span data-stu-id="64f91-308">enum [CORE_WEBVIEW2_MOVE_FOCUS_REASON](#core_webview2_move_focus_reason)</span></span>

 <span data-ttu-id="64f91-309">Данные</span><span class="sxs-lookup"><span data-stu-id="64f91-309">Values</span></span>                         | <span data-ttu-id="64f91-310">Описания</span><span class="sxs-lookup"><span data-stu-id="64f91-310">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="64f91-311">CORE_WEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC</span><span class="sxs-lookup"><span data-stu-id="64f91-311">CORE_WEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC</span></span>            | <span data-ttu-id="64f91-312">Настройка кода фокуса на WebView.</span><span class="sxs-lookup"><span data-stu-id="64f91-312">Code setting focus into WebView.</span></span>
<span data-ttu-id="64f91-313">CORE_WEBVIEW2_MOVE_FOCUS_REASON_NEXT</span><span class="sxs-lookup"><span data-stu-id="64f91-313">CORE_WEBVIEW2_MOVE_FOCUS_REASON_NEXT</span></span>            | <span data-ttu-id="64f91-314">Перемещение фокуса из-за прохождения вкладки вперед.</span><span class="sxs-lookup"><span data-stu-id="64f91-314">Moving focus due to Tab traversal forward.</span></span>
<span data-ttu-id="64f91-315">CORE_WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS</span><span class="sxs-lookup"><span data-stu-id="64f91-315">CORE_WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS</span></span>            | <span data-ttu-id="64f91-316">Перемещение фокуса из-за перемещения по табуляции назад.</span><span class="sxs-lookup"><span data-stu-id="64f91-316">Moving focus due to Tab traversal backward.</span></span>

#### <span data-ttu-id="64f91-317">CORE_WEBVIEW2_KEY_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="64f91-317">CORE_WEBVIEW2_KEY_EVENT_KIND</span></span> 

<span data-ttu-id="64f91-318">Тип события клавиши, которое инициировало событие AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="64f91-318">The type of key event that triggered an AcceleratorKeyPressed event.</span></span>

> <span data-ttu-id="64f91-319">[CORE_WEBVIEW2_KEY_EVENT_KIND](#core_webview2_key_event_kind) перечисления</span><span class="sxs-lookup"><span data-stu-id="64f91-319">enum [CORE_WEBVIEW2_KEY_EVENT_KIND](#core_webview2_key_event_kind)</span></span>

 <span data-ttu-id="64f91-320">Данные</span><span class="sxs-lookup"><span data-stu-id="64f91-320">Values</span></span>                         | <span data-ttu-id="64f91-321">Описания</span><span class="sxs-lookup"><span data-stu-id="64f91-321">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="64f91-322">CORE_WEBVIEW2_KEY_EVENT_KIND_KEY_DOWN</span><span class="sxs-lookup"><span data-stu-id="64f91-322">CORE_WEBVIEW2_KEY_EVENT_KIND_KEY_DOWN</span></span>            | <span data-ttu-id="64f91-323">ВыWM_KEYDOWN сообщение в окне.</span><span class="sxs-lookup"><span data-stu-id="64f91-323">Correspond to window message WM_KEYDOWN.</span></span>
<span data-ttu-id="64f91-324">CORE_WEBVIEW2_KEY_EVENT_KIND_KEY_UP</span><span class="sxs-lookup"><span data-stu-id="64f91-324">CORE_WEBVIEW2_KEY_EVENT_KIND_KEY_UP</span></span>            | <span data-ttu-id="64f91-325">ВыWM_KEYUP сообщение в окне.</span><span class="sxs-lookup"><span data-stu-id="64f91-325">Correspond to window message WM_KEYUP.</span></span>
<span data-ttu-id="64f91-326">CORE_WEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_DOWN</span><span class="sxs-lookup"><span data-stu-id="64f91-326">CORE_WEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_DOWN</span></span>            | <span data-ttu-id="64f91-327">ВыWM_SYSKEYDOWN сообщение в окне.</span><span class="sxs-lookup"><span data-stu-id="64f91-327">Correspond to window message WM_SYSKEYDOWN.</span></span>
<span data-ttu-id="64f91-328">CORE_WEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_UP</span><span class="sxs-lookup"><span data-stu-id="64f91-328">CORE_WEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_UP</span></span>            | <span data-ttu-id="64f91-329">ВыWM_SYSKEYUP сообщение в окне.</span><span class="sxs-lookup"><span data-stu-id="64f91-329">Correspond to window message WM_SYSKEYUP.</span></span>

#### <span data-ttu-id="64f91-330">CORE_WEBVIEW2_PHYSICAL_KEY_STATUS</span><span class="sxs-lookup"><span data-stu-id="64f91-330">CORE_WEBVIEW2_PHYSICAL_KEY_STATUS</span></span> 

<span data-ttu-id="64f91-331">Структура, представляющая данные, Упакованные в LPARAM, предоставленные событию ключа Win32.</span><span class="sxs-lookup"><span data-stu-id="64f91-331">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

> <span data-ttu-id="64f91-332">typedef [CORE_WEBVIEW2_PHYSICAL_KEY_STATUS](#core_webview2_physical_key_status)</span><span class="sxs-lookup"><span data-stu-id="64f91-332">typedef [CORE_WEBVIEW2_PHYSICAL_KEY_STATUS](#core_webview2_physical_key_status)</span></span>

<span data-ttu-id="64f91-333">Подробные сведения об WM_KEYDOWN вы увидите в документации по адресу[https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)</span><span class="sxs-lookup"><span data-stu-id="64f91-333">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)</span></span>

