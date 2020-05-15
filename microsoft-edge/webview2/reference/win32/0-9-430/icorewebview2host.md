---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 4fe7d149aa422fb98ad3b63e63943533f00c84e5
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654775"
---
# <span data-ttu-id="d7915-104">интерфейс ICoreWebView2Host</span><span class="sxs-lookup"><span data-stu-id="d7915-104">interface ICoreWebView2Host</span></span> 

> [!NOTE]
> <span data-ttu-id="d7915-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="d7915-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="d7915-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="d7915-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2Host
  : public IUnknown
```

<span data-ttu-id="d7915-107">Этот интерфейс является владельцем объекта CoreWebView2 и предоставляет поддержку изменения размеров, отображения и скрытия, фокусировки и других функциональных возможностей, связанных с окнами и композицией.</span><span class="sxs-lookup"><span data-stu-id="d7915-107">This interface is the owner of the CoreWebView2 object, and provides support for resizing, showing and hiding, focusing, and other functionality related to windowing and composition.</span></span>

## <span data-ttu-id="d7915-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="d7915-108">Summary</span></span>

 <span data-ttu-id="d7915-109">Участников</span><span class="sxs-lookup"><span data-stu-id="d7915-109">Members</span></span>                        | <span data-ttu-id="d7915-110">Описания</span><span class="sxs-lookup"><span data-stu-id="d7915-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d7915-111">get_IsVisible</span><span class="sxs-lookup"><span data-stu-id="d7915-111">get_IsVisible</span></span>](#get_isvisible) | <span data-ttu-id="d7915-112">Свойство Visible определяет, нужно ли отображать или скрывать WebView.</span><span class="sxs-lookup"><span data-stu-id="d7915-112">The IsVisible property determines whether to show or hide the webview.</span></span>
[<span data-ttu-id="d7915-113">put_IsVisible</span><span class="sxs-lookup"><span data-stu-id="d7915-113">put_IsVisible</span></span>](#put_isvisible) | <span data-ttu-id="d7915-114">Задайте свойство Visible.</span><span class="sxs-lookup"><span data-stu-id="d7915-114">Set the IsVisible property.</span></span>
[<span data-ttu-id="d7915-115">get_Bounds</span><span class="sxs-lookup"><span data-stu-id="d7915-115">get_Bounds</span></span>](#get_bounds) | <span data-ttu-id="d7915-116">Границы WebView.</span><span class="sxs-lookup"><span data-stu-id="d7915-116">The webview bounds.</span></span>
[<span data-ttu-id="d7915-117">put_Bounds</span><span class="sxs-lookup"><span data-stu-id="d7915-117">put_Bounds</span></span>](#put_bounds) | <span data-ttu-id="d7915-118">Задайте свойство Bounds.</span><span class="sxs-lookup"><span data-stu-id="d7915-118">Set the Bounds property.</span></span>
[<span data-ttu-id="d7915-119">get_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="d7915-119">get_ZoomFactor</span></span>](#get_zoomfactor) | <span data-ttu-id="d7915-120">Коэффициент масштабирования для WebView.</span><span class="sxs-lookup"><span data-stu-id="d7915-120">The zoom factor for the WebView.</span></span>
[<span data-ttu-id="d7915-121">put_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="d7915-121">put_ZoomFactor</span></span>](#put_zoomfactor) | <span data-ttu-id="d7915-122">Задайте свойство ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="d7915-122">Set the ZoomFactor property.</span></span>
[<span data-ttu-id="d7915-123">add_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="d7915-123">add_ZoomFactorChanged</span></span>](#add_zoomfactorchanged) | <span data-ttu-id="d7915-124">Добавьте обработчик событий для события ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="d7915-124">Add an event handler for the ZoomFactorChanged event.</span></span>
[<span data-ttu-id="d7915-125">remove_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="d7915-125">remove_ZoomFactorChanged</span></span>](#remove_zoomfactorchanged) | <span data-ttu-id="d7915-126">Удалите обработчик событий, добавленный ранее add_ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="d7915-126">Remove an event handler previously added with add_ZoomFactorChanged.</span></span>
[<span data-ttu-id="d7915-127">SetBoundsAndZoomFactor</span><span class="sxs-lookup"><span data-stu-id="d7915-127">SetBoundsAndZoomFactor</span></span>](#setboundsandzoomfactor) | <span data-ttu-id="d7915-128">Одновременное обновление границ и свойств ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="d7915-128">Update Bounds and ZoomFactor properties at the same time.</span></span>
[<span data-ttu-id="d7915-129">MoveFocus</span><span class="sxs-lookup"><span data-stu-id="d7915-129">MoveFocus</span></span>](#movefocus) | <span data-ttu-id="d7915-130">Перемещение фокуса в WebView.</span><span class="sxs-lookup"><span data-stu-id="d7915-130">Move focus into WebView.</span></span>
[<span data-ttu-id="d7915-131">add_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="d7915-131">add_MoveFocusRequested</span></span>](#add_movefocusrequested) | <span data-ttu-id="d7915-132">Добавьте обработчик событий для события MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="d7915-132">Add an event handler for the MoveFocusRequested event.</span></span>
[<span data-ttu-id="d7915-133">remove_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="d7915-133">remove_MoveFocusRequested</span></span>](#remove_movefocusrequested) | <span data-ttu-id="d7915-134">Удалите обработчик событий, добавленный ранее add_MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="d7915-134">Remove an event handler previously added with add_MoveFocusRequested.</span></span>
[<span data-ttu-id="d7915-135">add_GotFocus</span><span class="sxs-lookup"><span data-stu-id="d7915-135">add_GotFocus</span></span>](#add_gotfocus) | <span data-ttu-id="d7915-136">Добавьте обработчик событий для события GotFocus.</span><span class="sxs-lookup"><span data-stu-id="d7915-136">Add an event handler for the GotFocus event.</span></span>
[<span data-ttu-id="d7915-137">remove_GotFocus</span><span class="sxs-lookup"><span data-stu-id="d7915-137">remove_GotFocus</span></span>](#remove_gotfocus) | <span data-ttu-id="d7915-138">Удалите обработчик событий, добавленный ранее add_GotFocus.</span><span class="sxs-lookup"><span data-stu-id="d7915-138">Remove an event handler previously added with add_GotFocus.</span></span>
[<span data-ttu-id="d7915-139">add_LostFocus</span><span class="sxs-lookup"><span data-stu-id="d7915-139">add_LostFocus</span></span>](#add_lostfocus) | <span data-ttu-id="d7915-140">Добавьте обработчик для события LostFocus.</span><span class="sxs-lookup"><span data-stu-id="d7915-140">Add an event handler for the LostFocus event.</span></span>
[<span data-ttu-id="d7915-141">remove_LostFocus</span><span class="sxs-lookup"><span data-stu-id="d7915-141">remove_LostFocus</span></span>](#remove_lostfocus) | <span data-ttu-id="d7915-142">Удалите обработчик событий, добавленный ранее add_LostFocus.</span><span class="sxs-lookup"><span data-stu-id="d7915-142">Remove an event handler previously added with add_LostFocus.</span></span>
[<span data-ttu-id="d7915-143">add_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="d7915-143">add_AcceleratorKeyPressed</span></span>](#add_acceleratorkeypressed) | <span data-ttu-id="d7915-144">Добавьте обработчик событий для события AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="d7915-144">Add an event handler for the AcceleratorKeyPressed event.</span></span>
[<span data-ttu-id="d7915-145">remove_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="d7915-145">remove_AcceleratorKeyPressed</span></span>](#remove_acceleratorkeypressed) | <span data-ttu-id="d7915-146">Удалите обработчик событий, добавленный ранее add_AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="d7915-146">Remove an event handler previously added with add_AcceleratorKeyPressed.</span></span>
[<span data-ttu-id="d7915-147">get_ParentWindow</span><span class="sxs-lookup"><span data-stu-id="d7915-147">get_ParentWindow</span></span>](#get_parentwindow) | <span data-ttu-id="d7915-148">Родительское окно, предоставленное приложением, используемое этим WebView, для отрисовки содержимого.</span><span class="sxs-lookup"><span data-stu-id="d7915-148">The parent window provided by the app that this WebView is using to render content.</span></span>
[<span data-ttu-id="d7915-149">put_ParentWindow</span><span class="sxs-lookup"><span data-stu-id="d7915-149">put_ParentWindow</span></span>](#put_parentwindow) | <span data-ttu-id="d7915-150">Установка родительского окна для WebView.</span><span class="sxs-lookup"><span data-stu-id="d7915-150">Set the parent window for the WebView.</span></span>
[<span data-ttu-id="d7915-151">NotifyParentWindowPositionChanged</span><span class="sxs-lookup"><span data-stu-id="d7915-151">NotifyParentWindowPositionChanged</span></span>](#notifyparentwindowpositionchanged) | <span data-ttu-id="d7915-152">Это уведомление отделено от put_Bounds, которое указывает на то, что WebView родительский элемент HWND (или какой-либо его предок) переместился.</span><span class="sxs-lookup"><span data-stu-id="d7915-152">This is a notification separate from put_Bounds that tells WebView its parent (or any ancestor) HWND moved.</span></span>
[<span data-ttu-id="d7915-153">Close (закрыть)</span><span class="sxs-lookup"><span data-stu-id="d7915-153">Close</span></span>](#close) | <span data-ttu-id="d7915-154">Закрывает WebView и очищает основной экземпляр браузера.</span><span class="sxs-lookup"><span data-stu-id="d7915-154">Closes the WebView and cleans up the underlying browser instance.</span></span>
[<span data-ttu-id="d7915-155">get_CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="d7915-155">get_CoreWebView2</span></span>](#get_corewebview2) | <span data-ttu-id="d7915-156">Возвращает CoreWebView2, связанный с этим CoreWebView2Host.</span><span class="sxs-lookup"><span data-stu-id="d7915-156">Gets the CoreWebView2 associated with this CoreWebView2Host.</span></span>
[<span data-ttu-id="d7915-157">CORE_WEBVIEW2_MOVE_FOCUS_REASON</span><span class="sxs-lookup"><span data-stu-id="d7915-157">CORE_WEBVIEW2_MOVE_FOCUS_REASON</span></span>](#core_webview2_move_focus_reason) | <span data-ttu-id="d7915-158">Причина для перемещения фокуса.</span><span class="sxs-lookup"><span data-stu-id="d7915-158">Reason for moving focus.</span></span>
[<span data-ttu-id="d7915-159">CORE_WEBVIEW2_KEY_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="d7915-159">CORE_WEBVIEW2_KEY_EVENT_KIND</span></span>](#core_webview2_key_event_kind) | <span data-ttu-id="d7915-160">Тип события клавиши, которое инициировало событие AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="d7915-160">The type of key event that triggered an AcceleratorKeyPressed event.</span></span>
[<span data-ttu-id="d7915-161">CORE_WEBVIEW2_PHYSICAL_KEY_STATUS</span><span class="sxs-lookup"><span data-stu-id="d7915-161">CORE_WEBVIEW2_PHYSICAL_KEY_STATUS</span></span>](#core_webview2_physical_key_status) | <span data-ttu-id="d7915-162">Структура, представляющая данные, Упакованные в LPARAM, предоставленные событию ключа Win32.</span><span class="sxs-lookup"><span data-stu-id="d7915-162">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

<span data-ttu-id="d7915-163">CoreWebView2Host владеет CoreWebView2 и, если все ссылки на CoreWebView2Host выходит из него, WebView будет закрыт.</span><span class="sxs-lookup"><span data-stu-id="d7915-163">The CoreWebView2Host owns the CoreWebView2, and if all references to the CoreWebView2Host go away, the WebView will be closed.</span></span>

## <span data-ttu-id="d7915-164">Участников</span><span class="sxs-lookup"><span data-stu-id="d7915-164">Members</span></span>

#### <span data-ttu-id="d7915-165">get_IsVisible</span><span class="sxs-lookup"><span data-stu-id="d7915-165">get_IsVisible</span></span> 

<span data-ttu-id="d7915-166">Свойство Visible определяет, нужно ли отображать или скрывать WebView.</span><span class="sxs-lookup"><span data-stu-id="d7915-166">The IsVisible property determines whether to show or hide the webview.</span></span>

> <span data-ttu-id="d7915-167">общедоступные значения HRESULT [get_IsVisible](#get_isvisible)(bool \* Visible)</span><span class="sxs-lookup"><span data-stu-id="d7915-167">public HRESULT [get_IsVisible](#get_isvisible)(BOOL \* isVisible)</span></span>

<span data-ttu-id="d7915-168">Если для свойства Visible задано значение false, WebView будет прозрачным и не будет обрабатываться.</span><span class="sxs-lookup"><span data-stu-id="d7915-168">If IsVisible is set to false, the webview will be transparent and will not be rendered.</span></span> <span data-ttu-id="d7915-169">Однако это не повлияет на окно, содержащее WebView (параметр HWND, переданный в CreateCoreWebView2Host).</span><span class="sxs-lookup"><span data-stu-id="d7915-169">However, this will not affect the window containing the webview (the HWND parameter that was passed to CreateCoreWebView2Host).</span></span> <span data-ttu-id="d7915-170">Если вы хотите, чтобы окно не исчезало, вызовите для него функцию ShowWindow прямо в дополнение к изменению свойства Visible.</span><span class="sxs-lookup"><span data-stu-id="d7915-170">If you want that window to disappear too, call ShowWindow on it directly in addition to modifying the IsVisible property.</span></span> <span data-ttu-id="d7915-171">WebView — это дочернее окно не получает оконные сообщения, когда окно свертывания или восстановления находится в верхней части окна.</span><span class="sxs-lookup"><span data-stu-id="d7915-171">WebView as a child window won't get window messages when the top window is minimized or restored.</span></span> <span data-ttu-id="d7915-172">Для повышения производительности разработчик должен установить для свойства WebView значение false, если окно приложения свернуто, и вернуть значение true при восстановлении окна приложения.</span><span class="sxs-lookup"><span data-stu-id="d7915-172">For performance reason, developer should set IsVisible property of the WebView to false when the app window is minimized and back to true when app window is restored.</span></span> <span data-ttu-id="d7915-173">Это можно сделать, обрабатывая команды SC_MINIMIZE и SC_RESTORE при получении WM_SYSCOMMAND сообщения.</span><span class="sxs-lookup"><span data-stu-id="d7915-173">App window can do this by handling SC_MINIMIZE and SC_RESTORE command upon receiving WM_SYSCOMMAND message.</span></span>

```cpp
void ViewComponent::ToggleVisibility()
{
    BOOL visible;
    m_host->get_IsVisible(&visible);
    m_isVisible = !visible;
    m_host->put_IsVisible(m_isVisible);
}
```

#### <span data-ttu-id="d7915-174">put_IsVisible</span><span class="sxs-lookup"><span data-stu-id="d7915-174">put_IsVisible</span></span> 

<span data-ttu-id="d7915-175">Задайте свойство Visible.</span><span class="sxs-lookup"><span data-stu-id="d7915-175">Set the IsVisible property.</span></span>

> <span data-ttu-id="d7915-176">общедоступные значения HRESULT [put_IsVisible](#put_isvisible)(bool-Visible)</span><span class="sxs-lookup"><span data-stu-id="d7915-176">public HRESULT [put_IsVisible](#put_isvisible)(BOOL isVisible)</span></span>

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

#### <span data-ttu-id="d7915-177">get_Bounds</span><span class="sxs-lookup"><span data-stu-id="d7915-177">get_Bounds</span></span> 

<span data-ttu-id="d7915-178">Границы WebView.</span><span class="sxs-lookup"><span data-stu-id="d7915-178">The webview bounds.</span></span>

> <span data-ttu-id="d7915-179">общедоступные значения HRESULT [get_Bounds](#get_bounds)(границы Rect \*)</span><span class="sxs-lookup"><span data-stu-id="d7915-179">public HRESULT [get_Bounds](#get_bounds)(RECT \* bounds)</span></span>

<span data-ttu-id="d7915-180">Границы задаются относительно родительского дескриптора HWND.</span><span class="sxs-lookup"><span data-stu-id="d7915-180">Bounds are relative to the parent HWND.</span></span> <span data-ttu-id="d7915-181">Приложение может располагать WebView двумя способами:</span><span class="sxs-lookup"><span data-stu-id="d7915-181">The app has two ways it can position a WebView:</span></span>

1. <span data-ttu-id="d7915-182">Создание дочернего HWND, который является родительским дескриптором HWND WebView.</span><span class="sxs-lookup"><span data-stu-id="d7915-182">Create a child HWND that is the WebView parent HWND.</span></span> <span data-ttu-id="d7915-183">Расположите это окно в том месте, где должен быть WebView.</span><span class="sxs-lookup"><span data-stu-id="d7915-183">Position this window where the WebView should be.</span></span> <span data-ttu-id="d7915-184">В этом случае используйте (0, 0) для левого верхнего угла WebView Bound's (сдвиг).</span><span class="sxs-lookup"><span data-stu-id="d7915-184">In this case, use (0, 0) for the WebView's Bound's top left corner (the offset).</span></span>

1. <span data-ttu-id="d7915-185">Используйте окно самого высокого приложения в качестве родительского HWND WebView.</span><span class="sxs-lookup"><span data-stu-id="d7915-185">Use the app's top most window as the WebView parent HWND.</span></span> <span data-ttu-id="d7915-186">Задайте Bound's левый верхний угол WebView, чтобы WebView правильно расположиться в приложении.</span><span class="sxs-lookup"><span data-stu-id="d7915-186">Set the WebView's Bound's top left corner so that the WebView is positioned correctly in the app.</span></span> <span data-ttu-id="d7915-187">Значения границ находятся в пространстве координат основного приложения.</span><span class="sxs-lookup"><span data-stu-id="d7915-187">The Bound's values are in the host's coordinate space.</span></span>

#### <span data-ttu-id="d7915-188">put_Bounds</span><span class="sxs-lookup"><span data-stu-id="d7915-188">put_Bounds</span></span> 

<span data-ttu-id="d7915-189">Задайте свойство Bounds.</span><span class="sxs-lookup"><span data-stu-id="d7915-189">Set the Bounds property.</span></span>

> <span data-ttu-id="d7915-190">общедоступные значения HRESULT [put_Bounds](#put_bounds)(границы Rect)</span><span class="sxs-lookup"><span data-stu-id="d7915-190">public HRESULT [put_Bounds](#put_bounds)(RECT bounds)</span></span>

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

#### <span data-ttu-id="d7915-191">get_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="d7915-191">get_ZoomFactor</span></span> 

<span data-ttu-id="d7915-192">Коэффициент масштабирования для WebView.</span><span class="sxs-lookup"><span data-stu-id="d7915-192">The zoom factor for the WebView.</span></span>

> <span data-ttu-id="d7915-193">общедоступные значения HRESULT [get_ZoomFactor](#get_zoomfactor)(Double \* ZoomFactor)</span><span class="sxs-lookup"><span data-stu-id="d7915-193">public HRESULT [get_ZoomFactor](#get_zoomfactor)(double \* zoomFactor)</span></span>

<span data-ttu-id="d7915-194">Обратите внимание, что изменение коэффициента масштабирования может привести к `window.innerWidth/innerHeight` изменению масштаба страницы.</span><span class="sxs-lookup"><span data-stu-id="d7915-194">Note that changing zoom factor could cause `window.innerWidth/innerHeight` and page layout to change.</span></span> <span data-ttu-id="d7915-195">Коэффициент масштабирования, примененный ведущим приложением путем вызова put_ZoomFactor, становится новым масштабом по умолчанию для WebView.</span><span class="sxs-lookup"><span data-stu-id="d7915-195">A zoom factor that is applied by the host by calling put_ZoomFactor becomes the new default zoom for the WebView.</span></span> <span data-ttu-id="d7915-196">Этот коэффициент масштабирования применяется для всех переходов и — коэффициент масштабирования WebView возвращается, когда пользователь нажимает клавиши CTRL + 0.</span><span class="sxs-lookup"><span data-stu-id="d7915-196">This zoom factor applies across navigations and is the zoom factor WebView is returned to when the user presses ctrl+0.</span></span> <span data-ttu-id="d7915-197">При изменении коэффициента масштабирования пользователем (в результате использования приложения, получающего ZoomFactorChanged) это масштабирование применяется только к текущей странице.</span><span class="sxs-lookup"><span data-stu-id="d7915-197">When the zoom factor is changed by the user (resulting in the app receiving ZoomFactorChanged), that zoom applies only for the current page.</span></span> <span data-ttu-id="d7915-198">Любой пользователь, который применяет масштабирование, используется только для текущей страницы и сбрасывается на панели навигации.</span><span class="sxs-lookup"><span data-stu-id="d7915-198">Any user applied zoom is only for the current page and is reset on a navigation.</span></span> <span data-ttu-id="d7915-199">Указывать zoomFactor меньше или равно 0 не разрешается.</span><span class="sxs-lookup"><span data-stu-id="d7915-199">Specifying a zoomFactor less than or equal to 0 is not allowed.</span></span> <span data-ttu-id="d7915-200">WebView также имеет внутренний поддерживаемый диапазон коэффициента масштабирования.</span><span class="sxs-lookup"><span data-stu-id="d7915-200">WebView also has an internal supported zoom factor range.</span></span> <span data-ttu-id="d7915-201">Если указанный коэффициент масштаба выходит за пределы этого диапазона, он будет нормализован в пределах диапазона, а событие ZoomFactorChanged будет инициировано для фактического коэффициента масштабирования.</span><span class="sxs-lookup"><span data-stu-id="d7915-201">When a specified zoom factor is out of that range, it will be normalized to be within the range, and a ZoomFactorChanged event will be fired for the real applied zoom factor.</span></span> <span data-ttu-id="d7915-202">При выполнении этой нормализации диапазона свойство ZoomFactor будет указывать коэффициент масштабирования, указанный в предыдущем изменении свойства ZoomFactor, пока событие ZoomFactorChanged не будет получено после WebView применяет нормализованный коэффициент масштабирования.</span><span class="sxs-lookup"><span data-stu-id="d7915-202">When this range normalization happens, the ZoomFactor property will report the zoom factor specified during the previous modification of the ZoomFactor property until the ZoomFactorChanged event is received after webview applies the normalized zoom factor.</span></span>

#### <span data-ttu-id="d7915-203">put_ZoomFactor</span><span class="sxs-lookup"><span data-stu-id="d7915-203">put_ZoomFactor</span></span> 

<span data-ttu-id="d7915-204">Задайте свойство ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="d7915-204">Set the ZoomFactor property.</span></span>

> <span data-ttu-id="d7915-205">общедоступный [PUT_ZOOMFACTOR](#put_zoomfactor)HRESULT (двойной ZoomFactor)</span><span class="sxs-lookup"><span data-stu-id="d7915-205">public HRESULT [put_ZoomFactor](#put_zoomfactor)(double zoomFactor)</span></span>

#### <span data-ttu-id="d7915-206">add_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="d7915-206">add_ZoomFactorChanged</span></span> 

<span data-ttu-id="d7915-207">Добавьте обработчик событий для события ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="d7915-207">Add an event handler for the ZoomFactorChanged event.</span></span>

> <span data-ttu-id="d7915-208">общедоступные значения HRESULT [add_ZoomFactorChanged](#add_zoomfactorchanged)([ICoreWebView2ZoomFactorChangedEventHandler](ICoreWebView2ZoomFactorChangedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="d7915-208">public HRESULT [add_ZoomFactorChanged](#add_zoomfactorchanged)([ICoreWebView2ZoomFactorChangedEventHandler](ICoreWebView2ZoomFactorChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="d7915-209">Событие срабатывает, когда изменяется свойство ZoomFactor объекта WebView.</span><span class="sxs-lookup"><span data-stu-id="d7915-209">The event fires when the ZoomFactor property of the WebView changes.</span></span> <span data-ttu-id="d7915-210">Событие может срабатывать из-за того, что вызывающий объект изменил свойство ZoomFactor или пользователь вручную изменял масштаб.</span><span class="sxs-lookup"><span data-stu-id="d7915-210">The event could fire because the caller modified the ZoomFactor property, or due to the user manually modifying the zoom.</span></span> <span data-ttu-id="d7915-211">При изменении вызывающим абонентом с помощью свойства ZoomFactor внутренний коэффициент масштабирования немедленно обновляется, и событие ZoomFactorChanged не выводится.</span><span class="sxs-lookup"><span data-stu-id="d7915-211">When it is modified by the caller via the ZoomFactor property, the internal zoom factor is updated immediately and there will be no ZoomFactorChanged event.</span></span> <span data-ttu-id="d7915-212">WebView связывает последний использованный коэффициент масштабирования для каждого сайта.</span><span class="sxs-lookup"><span data-stu-id="d7915-212">WebView associates the last used zoom factor for each site.</span></span> <span data-ttu-id="d7915-213">Поэтому коэффициент масштабирования может изменяться при переходе на другую страницу.</span><span class="sxs-lookup"><span data-stu-id="d7915-213">Therefore, it is possible for the zoom factor to change when navigating to a different page.</span></span> <span data-ttu-id="d7915-214">При изменении коэффициента масштабирования из-за этого событие ZoomFactorChanged срабатывает сразу после события ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="d7915-214">When the zoom factor changes due to this, the ZoomFactorChanged event fires right after the ContentLoading event.</span></span>

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

#### <span data-ttu-id="d7915-215">remove_ZoomFactorChanged</span><span class="sxs-lookup"><span data-stu-id="d7915-215">remove_ZoomFactorChanged</span></span> 

<span data-ttu-id="d7915-216">Удалите обработчик событий, добавленный ранее add_ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="d7915-216">Remove an event handler previously added with add_ZoomFactorChanged.</span></span>

> <span data-ttu-id="d7915-217">общедоступные значения HRESULT [remove_ZoomFactorChanged](#remove_zoomfactorchanged)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="d7915-217">public HRESULT [remove_ZoomFactorChanged](#remove_zoomfactorchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="d7915-218">SetBoundsAndZoomFactor</span><span class="sxs-lookup"><span data-stu-id="d7915-218">SetBoundsAndZoomFactor</span></span> 

<span data-ttu-id="d7915-219">Одновременное обновление границ и свойств ZoomFactor.</span><span class="sxs-lookup"><span data-stu-id="d7915-219">Update Bounds and ZoomFactor properties at the same time.</span></span>

> <span data-ttu-id="d7915-220">общедоступные значения HRESULT [SetBoundsAndZoomFactor](#setboundsandzoomfactor)(границы Rect, Double zoomFactor)</span><span class="sxs-lookup"><span data-stu-id="d7915-220">public HRESULT [SetBoundsAndZoomFactor](#setboundsandzoomfactor)(RECT bounds,double zoomFactor)</span></span>

<span data-ttu-id="d7915-221">Эта операция является атомарной из perspecive узла.</span><span class="sxs-lookup"><span data-stu-id="d7915-221">This operation is atomic from the host's perspecive.</span></span> <span data-ttu-id="d7915-222">После того как вы вернете эту функцию, свойства Bounds и ZoomFactor будут обновлены при успешном выполнении функции, или ни один из них не будет обновляться при сбое функции.</span><span class="sxs-lookup"><span data-stu-id="d7915-222">After returning from this function, the Bounds and ZoomFactor properties will have both been updated if the function is successful, or neither will be updated if the function fails.</span></span> <span data-ttu-id="d7915-223">Если границы и ZoomFactor обновляются одним масштабом (то есть границы и ZoomFactor оба двойных), то страница не будет видеть изменение в Window. innerWidth/innerHeight, а WebView будет отображать содержимое на новом размере и масштабе без промежуточных преобразований.</span><span class="sxs-lookup"><span data-stu-id="d7915-223">If Bounds and ZoomFactor are both updated by the same scale (i.e. Bounds and ZoomFactor are both doubled), then the page will not see a change in window.innerWidth/innerHeight and the WebView will render the content at the new size and zoom without intermediate renderings.</span></span> <span data-ttu-id="d7915-224">Эта функция также может использоваться для обновления только одного из ZoomFactor или границ путем передачи нового значения для одного и текущего значения другого.</span><span class="sxs-lookup"><span data-stu-id="d7915-224">This function can also be used to update just one of ZoomFactor or Bounds by passing in the new value for one and the current value for the other.</span></span>

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

#### <span data-ttu-id="d7915-225">MoveFocus</span><span class="sxs-lookup"><span data-stu-id="d7915-225">MoveFocus</span></span> 

<span data-ttu-id="d7915-226">Перемещение фокуса в WebView.</span><span class="sxs-lookup"><span data-stu-id="d7915-226">Move focus into WebView.</span></span>

> <span data-ttu-id="d7915-227">общедоступные значения HRESULT [MoveFocus](#movefocus)(причина[CORE_WEBVIEW2_MOVE_FOCUS_REASON](#core_webview2_move_focus_reason) )</span><span class="sxs-lookup"><span data-stu-id="d7915-227">public HRESULT [MoveFocus](#movefocus)([CORE_WEBVIEW2_MOVE_FOCUS_REASON](#core_webview2_move_focus_reason) reason)</span></span>

<span data-ttu-id="d7915-228">WebView получит фокус, и фокус будет установлен на элемент корреспондента на странице, которая размещена в WebView.</span><span class="sxs-lookup"><span data-stu-id="d7915-228">WebView will get focus and focus will be set to correspondent element in the page hosted in the WebView.</span></span> <span data-ttu-id="d7915-229">В целях программной причины фокус установлен на ранее сфокусированный элемент или элемент по умолчанию, если нет ранее фокусируемого элемента.</span><span class="sxs-lookup"><span data-stu-id="d7915-229">For Programmatic reason, focus is set to previously focused element or the default element if there is no previously focused element.</span></span> <span data-ttu-id="d7915-230">В следующей причине фокус задается для первого элемента.</span><span class="sxs-lookup"><span data-stu-id="d7915-230">For Next reason, focus is set to the first element.</span></span> <span data-ttu-id="d7915-231">По этой причине фокус установлен на последний элемент.</span><span class="sxs-lookup"><span data-stu-id="d7915-231">For Previous reason, focus is set to the last element.</span></span> <span data-ttu-id="d7915-232">WebView также может сосредоточиться на взаимодействии с пользователем, например, щелкнув на WebView или TAB.</span><span class="sxs-lookup"><span data-stu-id="d7915-232">WebView can also got focus through user interaction like clicking into WebView or Tab into it.</span></span> <span data-ttu-id="d7915-233">Для табуляции приложение может вызвать MoveFocus с помощью кнопки Далее или назад, чтобы выровнять элементы Tab и SHIFT + TAB, если это необходимо, если WebView является следующим элементом с вкладками.</span><span class="sxs-lookup"><span data-stu-id="d7915-233">For tabbing, the app can call MoveFocus with Next or Previous to align with tab and shift+tab respectively when it decides the WebView is the next tabbable element.</span></span> <span data-ttu-id="d7915-234">Кроме того, приложение может вызвать IsDialogMessage как часть цикла обработки сообщений, чтобы платформа автоматически обрабатывала табуляцию.</span><span class="sxs-lookup"><span data-stu-id="d7915-234">Or, the app can call IsDialogMessage as part of its message loop to allow the platform to auto handle tabbing.</span></span> <span data-ttu-id="d7915-235">Платформа будет повернута на все окна с помощью WS_TABSTOP.</span><span class="sxs-lookup"><span data-stu-id="d7915-235">The platform will rotate through all windows with WS_TABSTOP.</span></span> <span data-ttu-id="d7915-236">Когда WebView получает фокус из IsDialogMessage, он будет внутренне размещать фокус на первом или последнем элементе Tab и Shift + Tab соответственно.</span><span class="sxs-lookup"><span data-stu-id="d7915-236">When the WebView gets focus from IsDialogMessage, it will internally put the focus on the first or last element for tab and shift+tab respectively.</span></span>

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

#### <span data-ttu-id="d7915-237">add_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="d7915-237">add_MoveFocusRequested</span></span> 

<span data-ttu-id="d7915-238">Добавьте обработчик событий для события MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="d7915-238">Add an event handler for the MoveFocusRequested event.</span></span>

> <span data-ttu-id="d7915-239">общедоступные значения HRESULT [add_MoveFocusRequested](#add_movefocusrequested)([ICoreWebView2MoveFocusRequestedEventHandler](ICoreWebView2MoveFocusRequestedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="d7915-239">public HRESULT [add_MoveFocusRequested](#add_movefocusrequested)([ICoreWebView2MoveFocusRequestedEventHandler](ICoreWebView2MoveFocusRequestedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="d7915-240">MoveFocusRequested активируется, когда пользователь пытается выполнить переход из WebView.</span><span class="sxs-lookup"><span data-stu-id="d7915-240">MoveFocusRequested fires when user tries to tab out of the WebView.</span></span> <span data-ttu-id="d7915-241">При срабатывании этого события фокус WebView не изменился.</span><span class="sxs-lookup"><span data-stu-id="d7915-241">The WebView's focus has not changed when this event is fired.</span></span>

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

#### <span data-ttu-id="d7915-242">remove_MoveFocusRequested</span><span class="sxs-lookup"><span data-stu-id="d7915-242">remove_MoveFocusRequested</span></span> 

<span data-ttu-id="d7915-243">Удалите обработчик событий, добавленный ранее add_MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="d7915-243">Remove an event handler previously added with add_MoveFocusRequested.</span></span>

> <span data-ttu-id="d7915-244">общедоступные значения HRESULT [remove_MoveFocusRequested](#remove_movefocusrequested)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="d7915-244">public HRESULT [remove_MoveFocusRequested](#remove_movefocusrequested)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="d7915-245">add_GotFocus</span><span class="sxs-lookup"><span data-stu-id="d7915-245">add_GotFocus</span></span> 

<span data-ttu-id="d7915-246">Добавьте обработчик событий для события GotFocus.</span><span class="sxs-lookup"><span data-stu-id="d7915-246">Add an event handler for the GotFocus event.</span></span>

> <span data-ttu-id="d7915-247">общедоступные значения HRESULT [add_GotFocus](#add_gotfocus)([ICoreWebView2FocusChangedEventHandler](ICoreWebView2FocusChangedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="d7915-247">public HRESULT [add_GotFocus](#add_gotfocus)([ICoreWebView2FocusChangedEventHandler](ICoreWebView2FocusChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="d7915-248">Получение фокуса срабатывает, когда WebView получил фокусировку.</span><span class="sxs-lookup"><span data-stu-id="d7915-248">GotFocus fires when WebView got focus.</span></span>

#### <span data-ttu-id="d7915-249">remove_GotFocus</span><span class="sxs-lookup"><span data-stu-id="d7915-249">remove_GotFocus</span></span> 

<span data-ttu-id="d7915-250">Удалите обработчик событий, добавленный ранее add_GotFocus.</span><span class="sxs-lookup"><span data-stu-id="d7915-250">Remove an event handler previously added with add_GotFocus.</span></span>

> <span data-ttu-id="d7915-251">общедоступные значения HRESULT [remove_GotFocus](#remove_gotfocus)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="d7915-251">public HRESULT [remove_GotFocus](#remove_gotfocus)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="d7915-252">add_LostFocus</span><span class="sxs-lookup"><span data-stu-id="d7915-252">add_LostFocus</span></span> 

<span data-ttu-id="d7915-253">Добавьте обработчик для события LostFocus.</span><span class="sxs-lookup"><span data-stu-id="d7915-253">Add an event handler for the LostFocus event.</span></span>

> <span data-ttu-id="d7915-254">общедоступные значения HRESULT [add_LostFocus](#add_lostfocus)([ICoreWebView2FocusChangedEventHandler](ICoreWebView2FocusChangedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="d7915-254">public HRESULT [add_LostFocus](#add_lostfocus)([ICoreWebView2FocusChangedEventHandler](ICoreWebView2FocusChangedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="d7915-255">LostFocus вызывается, когда WebView теряет фокус.</span><span class="sxs-lookup"><span data-stu-id="d7915-255">LostFocus fires when WebView lost focus.</span></span> <span data-ttu-id="d7915-256">В случае, если возникает событие MoveFocusRequested, фокус по-прежнему находится в WebView при срабатывании события MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="d7915-256">In the case where MoveFocusRequested event is fired, the focus is still on WebView when MoveFocusRequested event fires.</span></span> <span data-ttu-id="d7915-257">Потерянный фокус срабатывает только в том случае, если код приложения или действие по умолчанию, заданное MoveFocusRequested события, задали фокус от WebView.</span><span class="sxs-lookup"><span data-stu-id="d7915-257">Lost focus only fires afterwards when app's code or default action of MoveFocusRequested event set focus away from WebView.</span></span>

#### <span data-ttu-id="d7915-258">remove_LostFocus</span><span class="sxs-lookup"><span data-stu-id="d7915-258">remove_LostFocus</span></span> 

<span data-ttu-id="d7915-259">Удалите обработчик событий, добавленный ранее add_LostFocus.</span><span class="sxs-lookup"><span data-stu-id="d7915-259">Remove an event handler previously added with add_LostFocus.</span></span>

> <span data-ttu-id="d7915-260">общедоступные значения HRESULT [remove_LostFocus](#remove_lostfocus)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="d7915-260">public HRESULT [remove_LostFocus](#remove_lostfocus)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="d7915-261">add_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="d7915-261">add_AcceleratorKeyPressed</span></span> 

<span data-ttu-id="d7915-262">Добавьте обработчик событий для события AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="d7915-262">Add an event handler for the AcceleratorKeyPressed event.</span></span>

> <span data-ttu-id="d7915-263">общедоступные значения HRESULT [add_AcceleratorKeyPressed](#add_acceleratorkeypressed)([ICoreWebView2AcceleratorKeyPressedEventHandler](ICoreWebView2AcceleratorKeyPressedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="d7915-263">public HRESULT [add_AcceleratorKeyPressed](#add_acceleratorkeypressed)([ICoreWebView2AcceleratorKeyPressedEventHandler](ICoreWebView2AcceleratorKeyPressedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="d7915-264">AcceleratorKeyPressed активируется при нажатии или отпускании клавиши сочетания клавиш в том случае, если WebView имеет фокус.</span><span class="sxs-lookup"><span data-stu-id="d7915-264">AcceleratorKeyPressed fires when an accelerator key or key combo is pressed or released while the WebView is focused.</span></span> <span data-ttu-id="d7915-265">Клавиша считается ускорителем по одной из следующих способов:</span><span class="sxs-lookup"><span data-stu-id="d7915-265">A key is considered an accelerator if either:</span></span>

1. <span data-ttu-id="d7915-266">В данный момент удерживается клавиша CTRL или ALT;</span><span class="sxs-lookup"><span data-stu-id="d7915-266">Ctrl or Alt is currently being held, or</span></span>

1. <span data-ttu-id="d7915-267">Нажатая клавиша не сопоставляется с символом.</span><span class="sxs-lookup"><span data-stu-id="d7915-267">the pressed key does not map to a character.</span></span> <span data-ttu-id="d7915-268">Некоторые неопределенные клавиши никогда не рассматриваются как ускорители, например Shift.</span><span class="sxs-lookup"><span data-stu-id="d7915-268">A few specific keys are never considered accelerators, such as Shift.</span></span> <span data-ttu-id="d7915-269">Клавиша ESC всегда считается ускорителем.</span><span class="sxs-lookup"><span data-stu-id="d7915-269">The Escape key is always considered an accelerator.</span></span>

<span data-ttu-id="d7915-270">Событие с автоматическим нажатием клавиши, вызванное удерживанием нажатой клавиши, также срабатывает.</span><span class="sxs-lookup"><span data-stu-id="d7915-270">Autorepeated key events caused by holding the key down will also fire this event.</span></span> <span data-ttu-id="d7915-271">Чтобы отфильтровать эти данные, Проверьте аргументы события "KeyEventLParam" или "PhysicalKeyStatus".</span><span class="sxs-lookup"><span data-stu-id="d7915-271">You can filter these out by checking the event args' KeyEventLParam or PhysicalKeyStatus.</span></span>

<span data-ttu-id="d7915-272">В оконном режиме этот обработчик событий вызывается синхронно.</span><span class="sxs-lookup"><span data-stu-id="d7915-272">In windowed mode, this event handler is called synchronously.</span></span> <span data-ttu-id="d7915-273">До тех пор пока вы не вызываете Handle () для аргументов события или не будет возвращен обработчик событий, процесс браузера будет заблокирован и исходящие межпроцессные вызовы COM не будут работать с RPC_E_CANTCALLOUT_ININPUTSYNCCALL.</span><span class="sxs-lookup"><span data-stu-id="d7915-273">Until you call Handle() on the event args or the event handler returns, the browser process will be blocked and outgoing cross-process COM calls will fail with RPC_E_CANTCALLOUT_ININPUTSYNCCALL.</span></span> <span data-ttu-id="d7915-274">Однако все методы API CoreWebView2 будут работать.</span><span class="sxs-lookup"><span data-stu-id="d7915-274">All CoreWebView2 API methods will work, however.</span></span>

<span data-ttu-id="d7915-275">В режиме безоконный обработчик событий вызывается асинхронно.</span><span class="sxs-lookup"><span data-stu-id="d7915-275">In windowless mode, the event handler is called asynchronously.</span></span> <span data-ttu-id="d7915-276">Дальнейшие входные данные не доходят до браузера, пока обработчик событий не возвратит или не завершит вызов (), но сам процесс браузера не будет заблокирован, а исходящие вызовы COM будут работать нормально.</span><span class="sxs-lookup"><span data-stu-id="d7915-276">Further input will not reach the browser until the event handler returns or Handle() is called, but the browser process itself will not be blocked, and outgoing COM calls will work normally.</span></span>

<span data-ttu-id="d7915-277">Рекомендуется, чтобы вы могли узнать, что вы хотите обрабатывать клавишу быстрого вызова (TRUE), как и раньше.</span><span class="sxs-lookup"><span data-stu-id="d7915-277">It is recommended to call Handle(TRUE) as early as you can know that you want to handle the accelerator key.</span></span>

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

#### <span data-ttu-id="d7915-278">remove_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="d7915-278">remove_AcceleratorKeyPressed</span></span> 

<span data-ttu-id="d7915-279">Удалите обработчик событий, добавленный ранее add_AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="d7915-279">Remove an event handler previously added with add_AcceleratorKeyPressed.</span></span>

> <span data-ttu-id="d7915-280">общедоступные значения HRESULT [remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="d7915-280">public HRESULT [remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="d7915-281">get_ParentWindow</span><span class="sxs-lookup"><span data-stu-id="d7915-281">get_ParentWindow</span></span> 

<span data-ttu-id="d7915-282">Родительское окно, предоставленное приложением, используемое этим WebView, для отрисовки содержимого.</span><span class="sxs-lookup"><span data-stu-id="d7915-282">The parent window provided by the app that this WebView is using to render content.</span></span>

> <span data-ttu-id="d7915-283">общедоступные значения HRESULT [get_ParentWindow](#get_parentwindow)(HWND \* topLevelWindow)</span><span class="sxs-lookup"><span data-stu-id="d7915-283">public HRESULT [get_ParentWindow](#get_parentwindow)(HWND \* topLevelWindow)</span></span>

<span data-ttu-id="d7915-284">Этот API первоначально возвращает окно, передаваемое в CreateCoreWebView2Host.</span><span class="sxs-lookup"><span data-stu-id="d7915-284">This API initially returns the window passed into CreateCoreWebView2Host.</span></span>

#### <span data-ttu-id="d7915-285">put_ParentWindow</span><span class="sxs-lookup"><span data-stu-id="d7915-285">put_ParentWindow</span></span> 

<span data-ttu-id="d7915-286">Установка родительского окна для WebView.</span><span class="sxs-lookup"><span data-stu-id="d7915-286">Set the parent window for the WebView.</span></span>

> <span data-ttu-id="d7915-287">общедоступные значения HRESULT [put_ParentWindow](#put_parentwindow)(HWND topLevelWindow)</span><span class="sxs-lookup"><span data-stu-id="d7915-287">public HRESULT [put_ParentWindow](#put_parentwindow)(HWND topLevelWindow)</span></span>

<span data-ttu-id="d7915-288">Это приведет к тому, что WebView перестанет достать родительским окном до вновь заданной окна.</span><span class="sxs-lookup"><span data-stu-id="d7915-288">This will cause the WebView to reparent its window to the newly provided window.</span></span>

#### <span data-ttu-id="d7915-289">NotifyParentWindowPositionChanged</span><span class="sxs-lookup"><span data-stu-id="d7915-289">NotifyParentWindowPositionChanged</span></span> 

<span data-ttu-id="d7915-290">Это уведомление отделено от put_Bounds, которое указывает на то, что WebView родительский элемент HWND (или какой-либо его предок) переместился.</span><span class="sxs-lookup"><span data-stu-id="d7915-290">This is a notification separate from put_Bounds that tells WebView its parent (or any ancestor) HWND moved.</span></span>

> <span data-ttu-id="d7915-291">общедоступные значения HRESULT [NotifyParentWindowPositionChanged](#notifyparentwindowpositionchanged)()</span><span class="sxs-lookup"><span data-stu-id="d7915-291">public HRESULT [NotifyParentWindowPositionChanged](#notifyparentwindowpositionchanged)()</span></span>

<span data-ttu-id="d7915-292">Это необходимо для правильной работы специальных возможностей и некоторых диалоговых окон в WebView.</span><span class="sxs-lookup"><span data-stu-id="d7915-292">This is needed for accessibility and certain dialogs in WebView to work correctly.</span></span> 

```cpp
    if (message == WM_MOVE || message == WM_MOVING)
    {
        m_host->NotifyParentWindowPositionChanged();
        return true;
    }
```

#### <span data-ttu-id="d7915-293">Close (закрыть)</span><span class="sxs-lookup"><span data-stu-id="d7915-293">Close</span></span> 

<span data-ttu-id="d7915-294">Закрывает WebView и очищает основной экземпляр браузера.</span><span class="sxs-lookup"><span data-stu-id="d7915-294">Closes the WebView and cleans up the underlying browser instance.</span></span>

> <span data-ttu-id="d7915-295">общедоступное значение HRESULT [Close](#close)()</span><span class="sxs-lookup"><span data-stu-id="d7915-295">public HRESULT [Close](#close)()</span></span>

<span data-ttu-id="d7915-296">Очистка браузера instace освобождает ресурсы, переключающие WebView.</span><span class="sxs-lookup"><span data-stu-id="d7915-296">Cleaning up the browser instace will release the resources powering the WebView.</span></span> <span data-ttu-id="d7915-297">Экземпляр браузера будет закрыт, если он не используется другими веб – представлениями.</span><span class="sxs-lookup"><span data-stu-id="d7915-297">The browser instance will be shut down if there are no other WebViews using it.</span></span>

<span data-ttu-id="d7915-298">После вызова метода Close все вызовы методов завершатся сбоем, и обработчики событий прекратятся.</span><span class="sxs-lookup"><span data-stu-id="d7915-298">After calling Close, all method calls will fail and event handlers will stop firing.</span></span> <span data-ttu-id="d7915-299">В частности, WebView будет освобождать ссылки на обработчики событий при вызове Close.</span><span class="sxs-lookup"><span data-stu-id="d7915-299">Specifically, the WebView will release its references to its event handlers when Close is called.</span></span>

<span data-ttu-id="d7915-300">Метод Close вызывается неявно, когда CoreWebView2Host теряет свою конечную ссылку и является независимым.</span><span class="sxs-lookup"><span data-stu-id="d7915-300">Close is implicitly called when the CoreWebView2Host loses its final reference and is destructed.</span></span> <span data-ttu-id="d7915-301">Но рекомендуется явным образом вызывать метод Close, чтобы избежать случайного цикла ссылок между WebView и кодом приложения.</span><span class="sxs-lookup"><span data-stu-id="d7915-301">But it is best practice to explicitly call Close to avoid any accidental cycle of references between the WebView and the app code.</span></span> <span data-ttu-id="d7915-302">В частности, если вы захватываете ссылку на WebView в обработчике событий, вы создадите цикл ссылки между WebView и обработчиком событий.</span><span class="sxs-lookup"><span data-stu-id="d7915-302">Specifically, if you capture a reference to the WebView in an event handler you will create a reference cycle between the WebView and the event handler.</span></span> <span data-ttu-id="d7915-303">Вызов Close приведет к прерыванию этого цикла, освобождая все обработчики событий.</span><span class="sxs-lookup"><span data-stu-id="d7915-303">Calling Close will break this cycle by releasing all event handlers.</span></span> <span data-ttu-id="d7915-304">Но чтобы избежать такой ситуации, рекомендуется как явным образом вызвать метод Close для WebView и не захватить ссылку на WebView, чтобы убедиться, что WebView может быть корректно очищено.</span><span class="sxs-lookup"><span data-stu-id="d7915-304">But to avoid this situation it is best practice both to explicitly call Close on the WebView and to not capture a reference to the WebView to ensure the WebView can be cleaned up correctly.</span></span>

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

#### <span data-ttu-id="d7915-305">get_CoreWebView2</span><span class="sxs-lookup"><span data-stu-id="d7915-305">get_CoreWebView2</span></span> 

<span data-ttu-id="d7915-306">Возвращает CoreWebView2, связанный с этим CoreWebView2Host.</span><span class="sxs-lookup"><span data-stu-id="d7915-306">Gets the CoreWebView2 associated with this CoreWebView2Host.</span></span>

> <span data-ttu-id="d7915-307">общедоступные значения HRESULT [get_CoreWebView2](#get_corewebview2)([ICoreWebView2](ICoreWebView2.md) \* \* CoreWebView2)</span><span class="sxs-lookup"><span data-stu-id="d7915-307">public HRESULT [get_CoreWebView2](#get_corewebview2)([ICoreWebView2](ICoreWebView2.md) \*\* coreWebView2)</span></span>

#### <span data-ttu-id="d7915-308">CORE_WEBVIEW2_MOVE_FOCUS_REASON</span><span class="sxs-lookup"><span data-stu-id="d7915-308">CORE_WEBVIEW2_MOVE_FOCUS_REASON</span></span> 

<span data-ttu-id="d7915-309">Причина для перемещения фокуса.</span><span class="sxs-lookup"><span data-stu-id="d7915-309">Reason for moving focus.</span></span>

> <span data-ttu-id="d7915-310">[CORE_WEBVIEW2_MOVE_FOCUS_REASON](#core_webview2_move_focus_reason) перечисления</span><span class="sxs-lookup"><span data-stu-id="d7915-310">enum [CORE_WEBVIEW2_MOVE_FOCUS_REASON](#core_webview2_move_focus_reason)</span></span>

 <span data-ttu-id="d7915-311">Данные</span><span class="sxs-lookup"><span data-stu-id="d7915-311">Values</span></span>                         | <span data-ttu-id="d7915-312">Описания</span><span class="sxs-lookup"><span data-stu-id="d7915-312">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="d7915-313">CORE_WEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC</span><span class="sxs-lookup"><span data-stu-id="d7915-313">CORE_WEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC</span></span>            | <span data-ttu-id="d7915-314">Настройка кода фокуса на WebView.</span><span class="sxs-lookup"><span data-stu-id="d7915-314">Code setting focus into WebView.</span></span>
<span data-ttu-id="d7915-315">CORE_WEBVIEW2_MOVE_FOCUS_REASON_NEXT</span><span class="sxs-lookup"><span data-stu-id="d7915-315">CORE_WEBVIEW2_MOVE_FOCUS_REASON_NEXT</span></span>            | <span data-ttu-id="d7915-316">Перемещение фокуса из-за прохождения вкладки вперед.</span><span class="sxs-lookup"><span data-stu-id="d7915-316">Moving focus due to Tab traversal forward.</span></span>
<span data-ttu-id="d7915-317">CORE_WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS</span><span class="sxs-lookup"><span data-stu-id="d7915-317">CORE_WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS</span></span>            | <span data-ttu-id="d7915-318">Перемещение фокуса из-за перемещения по табуляции назад.</span><span class="sxs-lookup"><span data-stu-id="d7915-318">Moving focus due to Tab traversal backward.</span></span>

#### <span data-ttu-id="d7915-319">CORE_WEBVIEW2_KEY_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="d7915-319">CORE_WEBVIEW2_KEY_EVENT_KIND</span></span> 

<span data-ttu-id="d7915-320">Тип события клавиши, которое инициировало событие AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="d7915-320">The type of key event that triggered an AcceleratorKeyPressed event.</span></span>

> <span data-ttu-id="d7915-321">[CORE_WEBVIEW2_KEY_EVENT_KIND](#core_webview2_key_event_kind) перечисления</span><span class="sxs-lookup"><span data-stu-id="d7915-321">enum [CORE_WEBVIEW2_KEY_EVENT_KIND](#core_webview2_key_event_kind)</span></span>

 <span data-ttu-id="d7915-322">Данные</span><span class="sxs-lookup"><span data-stu-id="d7915-322">Values</span></span>                         | <span data-ttu-id="d7915-323">Описания</span><span class="sxs-lookup"><span data-stu-id="d7915-323">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="d7915-324">CORE_WEBVIEW2_KEY_EVENT_KIND_KEY_DOWN</span><span class="sxs-lookup"><span data-stu-id="d7915-324">CORE_WEBVIEW2_KEY_EVENT_KIND_KEY_DOWN</span></span>            | <span data-ttu-id="d7915-325">ВыWM_KEYDOWN сообщение в окне.</span><span class="sxs-lookup"><span data-stu-id="d7915-325">Correspond to window message WM_KEYDOWN.</span></span>
<span data-ttu-id="d7915-326">CORE_WEBVIEW2_KEY_EVENT_KIND_KEY_UP</span><span class="sxs-lookup"><span data-stu-id="d7915-326">CORE_WEBVIEW2_KEY_EVENT_KIND_KEY_UP</span></span>            | <span data-ttu-id="d7915-327">ВыWM_KEYUP сообщение в окне.</span><span class="sxs-lookup"><span data-stu-id="d7915-327">Correspond to window message WM_KEYUP.</span></span>
<span data-ttu-id="d7915-328">CORE_WEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_DOWN</span><span class="sxs-lookup"><span data-stu-id="d7915-328">CORE_WEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_DOWN</span></span>            | <span data-ttu-id="d7915-329">ВыWM_SYSKEYDOWN сообщение в окне.</span><span class="sxs-lookup"><span data-stu-id="d7915-329">Correspond to window message WM_SYSKEYDOWN.</span></span>
<span data-ttu-id="d7915-330">CORE_WEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_UP</span><span class="sxs-lookup"><span data-stu-id="d7915-330">CORE_WEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_UP</span></span>            | <span data-ttu-id="d7915-331">ВыWM_SYSKEYUP сообщение в окне.</span><span class="sxs-lookup"><span data-stu-id="d7915-331">Correspond to window message WM_SYSKEYUP.</span></span>

#### <span data-ttu-id="d7915-332">CORE_WEBVIEW2_PHYSICAL_KEY_STATUS</span><span class="sxs-lookup"><span data-stu-id="d7915-332">CORE_WEBVIEW2_PHYSICAL_KEY_STATUS</span></span> 

<span data-ttu-id="d7915-333">Структура, представляющая данные, Упакованные в LPARAM, предоставленные событию ключа Win32.</span><span class="sxs-lookup"><span data-stu-id="d7915-333">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

> <span data-ttu-id="d7915-334">typedef [CORE_WEBVIEW2_PHYSICAL_KEY_STATUS](#core_webview2_physical_key_status)</span><span class="sxs-lookup"><span data-stu-id="d7915-334">typedef [CORE_WEBVIEW2_PHYSICAL_KEY_STATUS](#core_webview2_physical_key_status)</span></span>

<span data-ttu-id="d7915-335">Подробные сведения об WM_KEYDOWN вы увидите в документации по адресу[https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)</span><span class="sxs-lookup"><span data-stu-id="d7915-335">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)</span></span>

