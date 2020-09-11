---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ExperimentalCompositionController
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2ExperimentalCompositionController
ms.openlocfilehash: 893628746e52ee8501e357f965d49324446d6470
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010217"
---
# <span data-ttu-id="ed35f-104">0.9.579-Interface ICoreWebView2ExperimentalCompositionController</span><span class="sxs-lookup"><span data-stu-id="ed35f-104">0.9.579 - interface ICoreWebView2ExperimentalCompositionController</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalCompositionController
  : public IUnknown
```

<span data-ttu-id="ed35f-105">Этот интерфейс является расширением интерфейса [ICoreWebView2Controller](icorewebview2controller.md) для поддержки визуального размещения.</span><span class="sxs-lookup"><span data-stu-id="ed35f-105">This interface is an extension of the [ICoreWebView2Controller](icorewebview2controller.md) interface to support visual hosting.</span></span>

## <span data-ttu-id="ed35f-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="ed35f-106">Summary</span></span>

 <span data-ttu-id="ed35f-107">Участников</span><span class="sxs-lookup"><span data-stu-id="ed35f-107">Members</span></span>                        | <span data-ttu-id="ed35f-108">Описания</span><span class="sxs-lookup"><span data-stu-id="ed35f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ed35f-109">add_CursorChanged</span><span class="sxs-lookup"><span data-stu-id="ed35f-109">add_CursorChanged</span></span>](#add_cursorchanged) | <span data-ttu-id="ed35f-110">Добавьте обработчик событий для события CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="ed35f-110">Add an event handler for the CursorChanged event.</span></span>
[<span data-ttu-id="ed35f-111">CreateCoreWebView2PointerInfoFromPointerId</span><span class="sxs-lookup"><span data-stu-id="ed35f-111">CreateCoreWebView2PointerInfoFromPointerId</span></span>](#createcorewebview2pointerinfofrompointerid) | <span data-ttu-id="ed35f-112">Вспомогательная функция для преобразования pointerId, полученного из системы, в [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).</span><span class="sxs-lookup"><span data-stu-id="ed35f-112">A helper function to convert a pointerId received from the system into an [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).</span></span>
[<span data-ttu-id="ed35f-113">get_Cursor</span><span class="sxs-lookup"><span data-stu-id="ed35f-113">get_Cursor</span></span>](#get_cursor) | <span data-ttu-id="ed35f-114">Текущий курсор, WebView рассчитает, что он должен быть.</span><span class="sxs-lookup"><span data-stu-id="ed35f-114">The current cursor that WebView thinks it should be.</span></span>
[<span data-ttu-id="ed35f-115">get_RootVisualTarget</span><span class="sxs-lookup"><span data-stu-id="ed35f-115">get_RootVisualTarget</span></span>](#get_rootvisualtarget) | <span data-ttu-id="ed35f-116">RootVisualTarget — это визуальный элемент в визуальном дереве размещающего приложения.</span><span class="sxs-lookup"><span data-stu-id="ed35f-116">The RootVisualTarget is a visual in the hosting app's visual tree.</span></span>
[<span data-ttu-id="ed35f-117">get_UIAProvider</span><span class="sxs-lookup"><span data-stu-id="ed35f-117">get_UIAProvider</span></span>](#get_uiaprovider) | <span data-ttu-id="ed35f-118">Возвращает поставщик модели автоматизации пользовательского интерфейса для WebView.</span><span class="sxs-lookup"><span data-stu-id="ed35f-118">Returns the UI Automation Provider for the WebView.</span></span>
[<span data-ttu-id="ed35f-119">put_RootVisualTarget</span><span class="sxs-lookup"><span data-stu-id="ed35f-119">put_RootVisualTarget</span></span>](#put_rootvisualtarget) | <span data-ttu-id="ed35f-120">Задайте свойство RootVisualTarget.</span><span class="sxs-lookup"><span data-stu-id="ed35f-120">Set the RootVisualTarget property.</span></span>
[<span data-ttu-id="ed35f-121">remove_CursorChanged</span><span class="sxs-lookup"><span data-stu-id="ed35f-121">remove_CursorChanged</span></span>](#remove_cursorchanged) | <span data-ttu-id="ed35f-122">Удалите обработчик событий, добавленный ранее add_CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="ed35f-122">Remove an event handler previously added with add_CursorChanged.</span></span>
[<span data-ttu-id="ed35f-123">SendMouseInput</span><span class="sxs-lookup"><span data-stu-id="ed35f-123">SendMouseInput</span></span>](#sendmouseinput) | <span data-ttu-id="ed35f-124">Если eventKind COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL или COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL, mouseData задает величину движения колесика.</span><span class="sxs-lookup"><span data-stu-id="ed35f-124">If eventKind is COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL or COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL, then mouseData specifies the amount of wheel movement.</span></span>
[<span data-ttu-id="ed35f-125">SendPointerInput</span><span class="sxs-lookup"><span data-stu-id="ed35f-125">SendPointerInput</span></span>](#sendpointerinput) | <span data-ttu-id="ed35f-126">SendPointerInput принимает вводные данные и указатель пера для типов, определенных в COREWEBVIEW2_POINTER_EVENT_KIND.</span><span class="sxs-lookup"><span data-stu-id="ed35f-126">SendPointerInput accepts touch or pen pointer input of types defined in COREWEBVIEW2_POINTER_EVENT_KIND.</span></span>
[<span data-ttu-id="ed35f-127">COREWEBVIEW2_MATRIX_4X4</span><span class="sxs-lookup"><span data-stu-id="ed35f-127">COREWEBVIEW2_MATRIX_4X4</span></span>](#corewebview2_matrix_4x4) | <span data-ttu-id="ed35f-128">Матрица, представляющая трехмерное преобразование.</span><span class="sxs-lookup"><span data-stu-id="ed35f-128">Matrix that represents a 3D transform.</span></span>
[<span data-ttu-id="ed35f-129">COREWEBVIEW2_MOUSE_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="ed35f-129">COREWEBVIEW2_MOUSE_EVENT_KIND</span></span>](#corewebview2_mouse_event_kind) | <span data-ttu-id="ed35f-130">Тип событий мыши, используемый функцией SendMouseInput для передачи типа события мыши, отправляемого в WebView.</span><span class="sxs-lookup"><span data-stu-id="ed35f-130">Mouse event type used by SendMouseInput to convey the type of mouse event being sent to WebView.</span></span>
[<span data-ttu-id="ed35f-131">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS</span><span class="sxs-lookup"><span data-stu-id="ed35f-131">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS</span></span>](#corewebview2_mouse_event_virtual_keys) | <span data-ttu-id="ed35f-132">Виртуальные ключи событий мыши, связанные с COREWEBVIEW2_MOUSE_EVENT_KINDом для SendMouseInput.</span><span class="sxs-lookup"><span data-stu-id="ed35f-132">Mouse event virtual keys associated with a COREWEBVIEW2_MOUSE_EVENT_KIND for SendMouseInput.</span></span>
[<span data-ttu-id="ed35f-133">COREWEBVIEW2_POINTER_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="ed35f-133">COREWEBVIEW2_POINTER_EVENT_KIND</span></span>](#corewebview2_pointer_event_kind) | <span data-ttu-id="ed35f-134">Тип события указателя, используемый функцией SendPointerInput для передачи типа события указателя, отправляемого в WebView.</span><span class="sxs-lookup"><span data-stu-id="ed35f-134">Pointer event type used by SendPointerInput to convey the type of pointer event being sent to WebView.</span></span>

<span data-ttu-id="ed35f-135">Объект, реализующий интерфейс ICoreWebView2ExperimentalCompositionController, также будет реализовывать [ICoreWebView2Controller](icorewebview2controller.md).</span><span class="sxs-lookup"><span data-stu-id="ed35f-135">An object implementing the ICoreWebView2ExperimentalCompositionController interface will also implement [ICoreWebView2Controller](icorewebview2controller.md).</span></span> <span data-ttu-id="ed35f-136">Предполагается, что вызывающие объекты используют [ICoreWebView2Controller](icorewebview2controller.md) для изменения размера, видимости, фокусировки и т. д., а затем используют ICoreWebView2ExperimentalCompositionController для подключения к дереву композиции и предоставления входных данных для WebView.</span><span class="sxs-lookup"><span data-stu-id="ed35f-136">Callers are expected to use [ICoreWebView2Controller](icorewebview2controller.md) for resizing, visibility, focus, and so on, and then use ICoreWebView2ExperimentalCompositionController to connect to a composition tree and provide input meant for the WebView.</span></span>

## <span data-ttu-id="ed35f-137">Участников</span><span class="sxs-lookup"><span data-stu-id="ed35f-137">Members</span></span>

#### <span data-ttu-id="ed35f-138">add_CursorChanged</span><span class="sxs-lookup"><span data-stu-id="ed35f-138">add_CursorChanged</span></span> 

<span data-ttu-id="ed35f-139">Добавьте обработчик событий для события CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="ed35f-139">Add an event handler for the CursorChanged event.</span></span>

> <span data-ttu-id="ed35f-140">общедоступные значения HRESULT [add_CursorChanged](#add_cursorchanged)([ICoreWebView2ExperimentalCursorChangedEventHandler](icorewebview2experimentalcursorchangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="ed35f-140">public HRESULT [add_CursorChanged](#add_cursorchanged)([ICoreWebView2ExperimentalCursorChangedEventHandler](icorewebview2experimentalcursorchangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="ed35f-141">Событие срабатывает, когда WebView считает, что курсор должен быть изменен.</span><span class="sxs-lookup"><span data-stu-id="ed35f-141">The event fires when WebView thinks the cursor should be changed.</span></span> <span data-ttu-id="ed35f-142">Например, если курсор мыши установлен по умолчанию, но затем перемещается поверх текста, он может попытаться перейти на курсор IBeam.</span><span class="sxs-lookup"><span data-stu-id="ed35f-142">For example, when the mouse cursor is currently the default cursor but is then moved over text, it may try to change to the IBeam cursor.</span></span>

<span data-ttu-id="ed35f-143">Ожидается, что разработчик отправляет COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE сообщения (в дополнение к COREWEBVIEW2_MOUSE_EVENT_KIND_MOVE сообщениям) через API SendMouseInput.</span><span class="sxs-lookup"><span data-stu-id="ed35f-143">It is expected for the developer to send COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE messages (in addition to COREWEBVIEW2_MOUSE_EVENT_KIND_MOVE messages) through the SendMouseInput API.</span></span> <span data-ttu-id="ed35f-144">Это необходимо для того, чтобы убедиться в том, что указатель мыши находится в WebView, отправляющем события CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="ed35f-144">This is to ensure that the mouse is actually within the WebView that sends out CursorChanged events.</span></span>

```cpp
        // Register a handler for the CursorChanged event.
        CHECK_FAILURE(m_compositionController->add_CursorChanged(
            Callback<ICoreWebView2ExperimentalCursorChangedEventHandler>(
                [this](ICoreWebView2ExperimentalCompositionController* sender,
                    IUnknown* args) -> HRESULT {
                        HCURSOR cursor;
                        CHECK_FAILURE(sender->get_Cursor(&cursor));
                        SetClassLongPtr(m_appWindow->GetMainWindow(), GCLP_HCURSOR, (LONG_PTR)cursor);
                        return S_OK;
                })
            .Get(),
                    &m_cursorChangedToken));
```

#### <span data-ttu-id="ed35f-145">CreateCoreWebView2PointerInfoFromPointerId</span><span class="sxs-lookup"><span data-stu-id="ed35f-145">CreateCoreWebView2PointerInfoFromPointerId</span></span> 

<span data-ttu-id="ed35f-146">Вспомогательная функция для преобразования pointerId, полученного из системы, в [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).</span><span class="sxs-lookup"><span data-stu-id="ed35f-146">A helper function to convert a pointerId received from the system into an [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).</span></span>

> <span data-ttu-id="ed35f-147">общедоступные значения HRESULT [CreateCoreWebView2PointerInfoFromPointerId](#createcorewebview2pointerinfofrompointerid)(uint POINTERID, HWND parentWindow, struct COREWEBVIEW2_MATRIX_4X4 Transform, [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) \* \* pointerInfo)</span><span class="sxs-lookup"><span data-stu-id="ed35f-147">public HRESULT [CreateCoreWebView2PointerInfoFromPointerId](#createcorewebview2pointerinfofrompointerid)(UINT pointerId, HWND parentWindow, struct COREWEBVIEW2_MATRIX_4X4 transform, [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) \*\* pointerInfo)</span></span>

<span data-ttu-id="ed35f-148">parentWindow — HWND, который содержит WebView.</span><span class="sxs-lookup"><span data-stu-id="ed35f-148">parentWindow is the HWND that contains the webview.</span></span> <span data-ttu-id="ed35f-149">Это может быть любой HWND в дереве HWND, который включает WebView.</span><span class="sxs-lookup"><span data-stu-id="ed35f-149">This can be any HWND in the hwnd tree that contains the webview.</span></span> <span data-ttu-id="ed35f-150">COREWEBVIEW2_MATRIX_4X4 является преобразованием из дескриптора HWND в WebView.</span><span class="sxs-lookup"><span data-stu-id="ed35f-150">The COREWEBVIEW2_MATRIX_4X4 is the transform from that HWND to the webview.</span></span> <span data-ttu-id="ed35f-151">Возвращенный [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) используется в SendPointerInfo.</span><span class="sxs-lookup"><span data-stu-id="ed35f-151">The returned [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) is used in SendPointerInfo.</span></span> <span data-ttu-id="ed35f-152">Тип указателя должен быть либо пером, либо сенсорным, либо функция завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="ed35f-152">The pointer type must be either pen or touch or the function will fail.</span></span>


#### <span data-ttu-id="ed35f-153">get_Cursor</span><span class="sxs-lookup"><span data-stu-id="ed35f-153">get_Cursor</span></span> 

<span data-ttu-id="ed35f-154">Текущий курсор, WebView рассчитает, что он должен быть.</span><span class="sxs-lookup"><span data-stu-id="ed35f-154">The current cursor that WebView thinks it should be.</span></span>

> <span data-ttu-id="ed35f-155">общедоступные значения HRESULT [get_Cursor](#get_cursor)(HCURSOR \* Cursor)</span><span class="sxs-lookup"><span data-stu-id="ed35f-155">public HRESULT [get_Cursor](#get_cursor)(HCURSOR \* cursor)</span></span>

<span data-ttu-id="ed35f-156">Курсор должен быть установлен в WM_SETCURSOR с помощью:: SetCursor или установлен на соответствующий родительский или предок родительского объекта WebView By:: SetClassLongPtr.</span><span class="sxs-lookup"><span data-stu-id="ed35f-156">The cursor should be set in WM_SETCURSOR through ::SetCursor or set on the corresponding parent/ancestor HWND of the WebView through ::SetClassLongPtr.</span></span> <span data-ttu-id="ed35f-157">HCURSOR можно освободить таким образом, чтобы CopyCursor и DestroyCursor, чтобы сохранить собственную копию, если вы еще не настраиваете курсор.</span><span class="sxs-lookup"><span data-stu-id="ed35f-157">The HCURSOR can be freed so CopyCursor/DestroyCursor is recommended to keep your own copy if you are doing more than immediately setting the cursor.</span></span>

#### <span data-ttu-id="ed35f-158">get_RootVisualTarget</span><span class="sxs-lookup"><span data-stu-id="ed35f-158">get_RootVisualTarget</span></span> 

<span data-ttu-id="ed35f-159">RootVisualTarget — это визуальный элемент в визуальном дереве размещающего приложения.</span><span class="sxs-lookup"><span data-stu-id="ed35f-159">The RootVisualTarget is a visual in the hosting app's visual tree.</span></span>

> <span data-ttu-id="ed35f-160">общедоступные значения HRESULT [get_RootVisualTarget](#get_rootvisualtarget)(IUnknown \* \* Target)</span><span class="sxs-lookup"><span data-stu-id="ed35f-160">public HRESULT [get_RootVisualTarget](#get_rootvisualtarget)(IUnknown \*\* target)</span></span>

<span data-ttu-id="ed35f-161">Этот визуальный элемент — это то, где WebView будет подключаться к визуальному дереву.</span><span class="sxs-lookup"><span data-stu-id="ed35f-161">This visual is where the WebView will connect its visual tree.</span></span> <span data-ttu-id="ed35f-162">Приложение использует этот визуальный элемент, чтобы расположить WebView в приложении.</span><span class="sxs-lookup"><span data-stu-id="ed35f-162">The app uses this visual to position the WebView within the app.</span></span> <span data-ttu-id="ed35f-163">Чтобы изменить размер WebView, приложению по-прежнему нужно использовать свойство Boundss.</span><span class="sxs-lookup"><span data-stu-id="ed35f-163">The app still needs to use the Bounds property to size the WebView.</span></span> <span data-ttu-id="ed35f-164">Свойством RootVisualTarget может быть IDCompositionVisual или Windows:: UI:: композиция:: ContainerVisual.</span><span class="sxs-lookup"><span data-stu-id="ed35f-164">The RootVisualTarget property can be an IDCompositionVisual or a Windows::UI::Composition::ContainerVisual.</span></span> <span data-ttu-id="ed35f-165">WebView подключится к визуальному дереву для предоставленного визуального элемента перед возвратом из метода присваивания свойств.</span><span class="sxs-lookup"><span data-stu-id="ed35f-165">WebView will connect its visual tree to the provided visual before returning from the property setter.</span></span> <span data-ttu-id="ed35f-166">Приложение должно быть зафиксировано на своем устройстве, в котором задано свойство RootVisualTarget.</span><span class="sxs-lookup"><span data-stu-id="ed35f-166">The app needs to commit on its device setting the RootVisualTarget property.</span></span> <span data-ttu-id="ed35f-167">Свойство RootVisualTarget поддерживает значение nullptr, чтобы отключить WebView от визуального дерева приложения.</span><span class="sxs-lookup"><span data-stu-id="ed35f-167">The RootVisualTarget property supports being set to nullptr to disconnect the WebView from the app's visual tree.</span></span> 
```cpp
            // Set the host app visual that the WebView will connect its visual
            // tree to.
            BuildDCompTreeUsingVisual();
            CHECK_FAILURE(m_compositionController->put_RootVisualTarget(m_dcompWebViewVisual.get()));
            CHECK_FAILURE(m_dcompDevice->Commit());
```

```cpp
// Create host app visual that the WebView will connect to.
//   - Create a IDCompositionTarget for the host window
//   - Create a visual and set that as the IDCompositionTarget's root
//   - Create another visual and add that to the IDCompositionTarget's root.
//     This visual will be the visual root for the WebView.
void ViewComponent::BuildDCompTreeUsingVisual()
{
    CHECK_FAILURE_BOOL(m_dcompDevice != nullptr);

    if (m_dcompWebViewVisual == nullptr)
    {
        CHECK_FAILURE(m_dcompDevice->CreateTargetForHwnd(
            m_appWindow->GetMainWindow(), TRUE, &m_dcompHwndTarget));
        CHECK_FAILURE(m_dcompDevice->CreateVisual(&m_dcompRootVisual));
        CHECK_FAILURE(m_dcompHwndTarget->SetRoot(m_dcompRootVisual.get()));
        CHECK_FAILURE(m_dcompDevice->CreateVisual(&m_dcompWebViewVisual));
        CHECK_FAILURE(m_dcompRootVisual->AddVisual(m_dcompWebViewVisual.get(), TRUE, nullptr));
    }
}
```

#### <span data-ttu-id="ed35f-168">get_UIAProvider</span><span class="sxs-lookup"><span data-stu-id="ed35f-168">get_UIAProvider</span></span> 

<span data-ttu-id="ed35f-169">Возвращает поставщик модели автоматизации пользовательского интерфейса для WebView.</span><span class="sxs-lookup"><span data-stu-id="ed35f-169">Returns the UI Automation Provider for the WebView.</span></span>

> <span data-ttu-id="ed35f-170">общедоступные значения HRESULT [get_UIAProvider](#get_uiaprovider)(IUnknown \* \* Provider)</span><span class="sxs-lookup"><span data-stu-id="ed35f-170">public HRESULT [get_UIAProvider](#get_uiaprovider)(IUnknown \*\* provider)</span></span>

#### <span data-ttu-id="ed35f-171">put_RootVisualTarget</span><span class="sxs-lookup"><span data-stu-id="ed35f-171">put_RootVisualTarget</span></span> 

<span data-ttu-id="ed35f-172">Задайте свойство RootVisualTarget.</span><span class="sxs-lookup"><span data-stu-id="ed35f-172">Set the RootVisualTarget property.</span></span>

> <span data-ttu-id="ed35f-173">общедоступные значения HRESULT [put_RootVisualTarget](#put_rootvisualtarget)(объект IUnknown \*)</span><span class="sxs-lookup"><span data-stu-id="ed35f-173">public HRESULT [put_RootVisualTarget](#put_rootvisualtarget)(IUnknown \* target)</span></span>

#### <span data-ttu-id="ed35f-174">remove_CursorChanged</span><span class="sxs-lookup"><span data-stu-id="ed35f-174">remove_CursorChanged</span></span> 

<span data-ttu-id="ed35f-175">Удалите обработчик событий, добавленный ранее add_CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="ed35f-175">Remove an event handler previously added with add_CursorChanged.</span></span>

> <span data-ttu-id="ed35f-176">общедоступные значения HRESULT [remove_CursorChanged](#remove_cursorchanged)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="ed35f-176">public HRESULT [remove_CursorChanged](#remove_cursorchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="ed35f-177">SendMouseInput</span><span class="sxs-lookup"><span data-stu-id="ed35f-177">SendMouseInput</span></span> 

<span data-ttu-id="ed35f-178">Если eventKind COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL или COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL, mouseData задает величину движения колесика.</span><span class="sxs-lookup"><span data-stu-id="ed35f-178">If eventKind is COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL or COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL, then mouseData specifies the amount of wheel movement.</span></span>

> <span data-ttu-id="ed35f-179">Public HRESULT [SendMouseInput](#sendmouseinput)([COREWEBVIEW2_MOUSE_EVENT_KIND](#corewebview2_mouse_event_kind) eventKind, [COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS](#corewebview2_mouse_event_virtual_keys) virtualKeys, UINT32 mouseData, точка Point)</span><span class="sxs-lookup"><span data-stu-id="ed35f-179">public HRESULT [SendMouseInput](#sendmouseinput)([COREWEBVIEW2_MOUSE_EVENT_KIND](#corewebview2_mouse_event_kind) eventKind, [COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS](#corewebview2_mouse_event_virtual_keys) virtualKeys, UINT32 mouseData, POINT point)</span></span>

<span data-ttu-id="ed35f-180">Положительное значение указывает на то, что колесико было повернуто вперед от пользователя; отрицательное значение указывает на то, что колесико было повернуто на обратном направлении к пользователю.</span><span class="sxs-lookup"><span data-stu-id="ed35f-180">A positive value indicates that the wheel was rotated forward, away from the user; a negative value indicates that the wheel was rotated backward, toward the user.</span></span> <span data-ttu-id="ed35f-181">Один щелчок мыши определяется как WHEEL_DELTA (120).</span><span class="sxs-lookup"><span data-stu-id="ed35f-181">One wheel click is defined as WHEEL_DELTA, which is 120.</span></span> <span data-ttu-id="ed35f-182">Если eventKind COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOUBLE_CLICK COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOWN или COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_UP, то mouseData указывает, какие кнопки X были нажаты или отпущены.</span><span class="sxs-lookup"><span data-stu-id="ed35f-182">If eventKind is COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOUBLE_CLICK COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOWN, or COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_UP, then mouseData specifies which X buttons were pressed or released.</span></span> <span data-ttu-id="ed35f-183">Это значение должно быть 1, если первая кнопка X нажата/выпущена, и 2 при нажатии или отпускании второй кнопки X.</span><span class="sxs-lookup"><span data-stu-id="ed35f-183">This value should be 1 if the first X button is pressed/released and 2 if the second X button is pressed/released.</span></span> <span data-ttu-id="ed35f-184">Если eventKind COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE, то virtualKeys, mouseData и Point должны равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="ed35f-184">If eventKind is COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE, then virtualKeys, mouseData, and point should all be zero.</span></span> <span data-ttu-id="ed35f-185">Если eventKind — любое другое значение, mouseData должно равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="ed35f-185">If eventKind is any other value, then mouseData should be zero.</span></span> <span data-ttu-id="ed35f-186">Ожидается, что точка должна находиться в пространстве координат клиента WebView.</span><span class="sxs-lookup"><span data-stu-id="ed35f-186">Point is expected to be in the client coordinate space of the WebView.</span></span> <span data-ttu-id="ed35f-187">Для отслеживания событий мыши, которые запускаются в WebView и потенциально могут перемещаться за пределы WebView и ведущего приложения, рекомендуется использовать вызов SetCapture и ReleaseCapture.</span><span class="sxs-lookup"><span data-stu-id="ed35f-187">To track mouse events that start in the WebView and can potentially move outside of the WebView and host application, calling SetCapture and ReleaseCapture is recommended.</span></span> <span data-ttu-id="ed35f-188">Чтобы выйти из всплывающих окон, также рекомендуется отправлять COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE сообщения.</span><span class="sxs-lookup"><span data-stu-id="ed35f-188">To dismiss hover popups, it is also recommended to send COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE messages.</span></span> 
```cpp
bool ViewComponent::OnMouseMessage(UINT message, WPARAM wParam, LPARAM lParam)
{
    // Manually relay mouse messages to the WebView
    if (m_dcompDevice || m_wincompHelper)
    {
        POINT point;
        POINTSTOPOINT(point, lParam);
        if (message == WM_MOUSEWHEEL || message == WM_MOUSEHWHEEL)
        {
            // Mouse wheel messages are delivered in screen coordinates.
            // SendMouseInput expects client coordinates for the WebView, so convert
            // the point from screen to client.
            ::ScreenToClient(m_appWindow->GetMainWindow(), &point);
        }
        // Send the message to the WebView if the mouse location is inside the
        // bounds of the WebView, if the message is telling the WebView the
        // mouse has left the client area, or if we are currently capturing
        // mouse events.
        bool isMouseInWebView = PtInRect(&m_webViewBounds, point);
        if (isMouseInWebView || message == WM_MOUSELEAVE || m_isCapturingMouse)
        {
            DWORD mouseData = 0;

            switch (message)
            {
            case WM_MOUSEWHEEL:
            case WM_MOUSEHWHEEL:
                mouseData = GET_WHEEL_DELTA_WPARAM(wParam);
                break;
            case WM_XBUTTONDBLCLK:
            case WM_XBUTTONDOWN:
            case WM_XBUTTONUP:
                mouseData = GET_XBUTTON_WPARAM(wParam);
                break;
            case WM_MOUSEMOVE:
                if (!m_isTrackingMouse)
                {
                    // WebView needs to know when the mouse leaves the client area
                    // so that it can dismiss hover popups. TrackMouseEvent will
                    // provide a notification when the mouse leaves the client area.
                    TrackMouseEvents(TME_LEAVE);
                    m_isTrackingMouse = true;
                }
                break;
            case WM_MOUSELEAVE:
                m_isTrackingMouse = false;
                break;
            }

            // We need to capture the mouse in case the user drags the
            // mouse outside of the window bounds and we still need to send
            // mouse messages to the WebView process. This is useful for
            // scenarios like dragging the scroll bar or panning a map.
            // This is very similar to the Pointer Message case where a
            // press started inside of the WebView.
            if (message == WM_LBUTTONDOWN || message == WM_MBUTTONDOWN ||
                message == WM_RBUTTONDOWN || message == WM_XBUTTONDOWN)
            {
                if (isMouseInWebView && ::GetCapture() != m_appWindow->GetMainWindow())
                {
                    m_isCapturingMouse = true;
                    ::SetCapture(m_appWindow->GetMainWindow());
                }
            }
            else if (message == WM_LBUTTONUP || message == WM_MBUTTONUP ||
                message == WM_RBUTTONUP || message == WM_XBUTTONUP)
            {
                if (::GetCapture() == m_appWindow->GetMainWindow())
                {
                    m_isCapturingMouse = false;
                    ::ReleaseCapture();
                }
            }

            // Adjust the point from app client coordinates to webview client coordinates.
            // WM_MOUSELEAVE messages don't have a point, so don't adjust the point.
            if (message != WM_MOUSELEAVE)
            {
                point.x -= m_webViewBounds.left;
                point.y -= m_webViewBounds.top;
            }

            CHECK_FAILURE(m_compositionController->SendMouseInput(
                static_cast<COREWEBVIEW2_MOUSE_EVENT_KIND>(message),
                static_cast<COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS>(GET_KEYSTATE_WPARAM(wParam)),
                mouseData, point));
            return true;
        }
        else if (message == WM_MOUSEMOVE && m_isTrackingMouse)
        {
            // When the mouse moves outside of the WebView, but still inside the app
            // turn off mouse tracking and send the WebView a leave event.
            m_isTrackingMouse = false;
            TrackMouseEvents(TME_LEAVE | TME_CANCEL);
            OnMouseMessage(WM_MOUSELEAVE, 0, 0);
        }
    }
    return false;
}
```

#### <span data-ttu-id="ed35f-189">SendPointerInput</span><span class="sxs-lookup"><span data-stu-id="ed35f-189">SendPointerInput</span></span> 

<span data-ttu-id="ed35f-190">SendPointerInput принимает вводные данные и указатель пера для типов, определенных в COREWEBVIEW2_POINTER_EVENT_KIND.</span><span class="sxs-lookup"><span data-stu-id="ed35f-190">SendPointerInput accepts touch or pen pointer input of types defined in COREWEBVIEW2_POINTER_EVENT_KIND.</span></span>

> <span data-ttu-id="ed35f-191">Public HRESULT [SendPointerInput](#sendpointerinput)([COREWEBVIEW2_POINTER_EVENT_KIND](#corewebview2_pointer_event_kind) EventType, [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) \* pointerInfo)</span><span class="sxs-lookup"><span data-stu-id="ed35f-191">public HRESULT [SendPointerInput](#sendpointerinput)([COREWEBVIEW2_POINTER_EVENT_KIND](#corewebview2_pointer_event_kind) eventType, [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) \* pointerInfo)</span></span>

<span data-ttu-id="ed35f-192">Все входные данные указателя из системы должны быть преобразованы в [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) первыми.</span><span class="sxs-lookup"><span data-stu-id="ed35f-192">Any pointer input from the system must be converted into an [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) first.</span></span>

#### <span data-ttu-id="ed35f-193">COREWEBVIEW2_MATRIX_4X4</span><span class="sxs-lookup"><span data-stu-id="ed35f-193">COREWEBVIEW2_MATRIX_4X4</span></span> 

<span data-ttu-id="ed35f-194">Матрица, представляющая трехмерное преобразование.</span><span class="sxs-lookup"><span data-stu-id="ed35f-194">Matrix that represents a 3D transform.</span></span>

> <span data-ttu-id="ed35f-195">typedef [COREWEBVIEW2_MATRIX_4X4](#corewebview2_matrix_4x4)</span><span class="sxs-lookup"><span data-stu-id="ed35f-195">typedef [COREWEBVIEW2_MATRIX_4X4](#corewebview2_matrix_4x4)</span></span>

<span data-ttu-id="ed35f-196">Это преобразование используется для вычисления правильных координат при вызове CreateCoreWebView2PointerInfoFromPointerId.</span><span class="sxs-lookup"><span data-stu-id="ed35f-196">This transform is used to calculate correct coordinates when calling CreateCoreWebView2PointerInfoFromPointerId.</span></span> <span data-ttu-id="ed35f-197">Это эквивалентно D2D1_MATRIX_4X4_F</span><span class="sxs-lookup"><span data-stu-id="ed35f-197">This is equivalent to a D2D1_MATRIX_4X4_F</span></span>

#### <span data-ttu-id="ed35f-198">COREWEBVIEW2_MOUSE_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="ed35f-198">COREWEBVIEW2_MOUSE_EVENT_KIND</span></span> 

<span data-ttu-id="ed35f-199">Тип событий мыши, используемый функцией SendMouseInput для передачи типа события мыши, отправляемого в WebView.</span><span class="sxs-lookup"><span data-stu-id="ed35f-199">Mouse event type used by SendMouseInput to convey the type of mouse event being sent to WebView.</span></span>

> <span data-ttu-id="ed35f-200">[COREWEBVIEW2_MOUSE_EVENT_KIND](#corewebview2_mouse_event_kind) перечисления</span><span class="sxs-lookup"><span data-stu-id="ed35f-200">enum [COREWEBVIEW2_MOUSE_EVENT_KIND](#corewebview2_mouse_event_kind)</span></span>

 <span data-ttu-id="ed35f-201">Данные</span><span class="sxs-lookup"><span data-stu-id="ed35f-201">Values</span></span>                         | <span data-ttu-id="ed35f-202">Описания</span><span class="sxs-lookup"><span data-stu-id="ed35f-202">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="ed35f-203">COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL</span><span class="sxs-lookup"><span data-stu-id="ed35f-203">COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL</span></span>            | <span data-ttu-id="ed35f-204">Событие прокрутки колесика мыши по горизонтали WM_MOUSEHWHEEL.</span><span class="sxs-lookup"><span data-stu-id="ed35f-204">Mouse horizontal wheel scroll event, WM_MOUSEHWHEEL.</span></span>
<span data-ttu-id="ed35f-205">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_DOUBLE_CLICK</span><span class="sxs-lookup"><span data-stu-id="ed35f-205">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_DOUBLE_CLICK</span></span>            | <span data-ttu-id="ed35f-206">Левая кнопка дважды щелкните событие мыши, WM_LBUTTONDBLCLK.</span><span class="sxs-lookup"><span data-stu-id="ed35f-206">Left button double click mouse event, WM_LBUTTONDBLCLK.</span></span>
<span data-ttu-id="ed35f-207">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_DOWN</span><span class="sxs-lookup"><span data-stu-id="ed35f-207">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_DOWN</span></span>            | <span data-ttu-id="ed35f-208">Левая кнопка вниз события мыши, WM_LBUTTONDOWN.</span><span class="sxs-lookup"><span data-stu-id="ed35f-208">Left button down mouse event, WM_LBUTTONDOWN.</span></span>
<span data-ttu-id="ed35f-209">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_UP</span><span class="sxs-lookup"><span data-stu-id="ed35f-209">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_UP</span></span>            | <span data-ttu-id="ed35f-210">Левая кнопка — событие мыши, WM_LBUTTONUP.</span><span class="sxs-lookup"><span data-stu-id="ed35f-210">Left button up mouse event, WM_LBUTTONUP.</span></span>
<span data-ttu-id="ed35f-211">COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE</span><span class="sxs-lookup"><span data-stu-id="ed35f-211">COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE</span></span>            | <span data-ttu-id="ed35f-212">Событие выхода из мыши, WM_MOUSELEAVE.</span><span class="sxs-lookup"><span data-stu-id="ed35f-212">Mouse leave event, WM_MOUSELEAVE.</span></span>
<span data-ttu-id="ed35f-213">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_DOUBLE_CLICK</span><span class="sxs-lookup"><span data-stu-id="ed35f-213">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_DOUBLE_CLICK</span></span>            | <span data-ttu-id="ed35f-214">Средняя кнопка дважды щелкните событие мыши, WM_MBUTTONDBLCLK.</span><span class="sxs-lookup"><span data-stu-id="ed35f-214">Middle button double click mouse event, WM_MBUTTONDBLCLK.</span></span>
<span data-ttu-id="ed35f-215">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_DOWN</span><span class="sxs-lookup"><span data-stu-id="ed35f-215">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_DOWN</span></span>            | <span data-ttu-id="ed35f-216">Средняя кнопка вниз: событие мыши, WM_MBUTTONDOWN.</span><span class="sxs-lookup"><span data-stu-id="ed35f-216">Middle button down mouse event, WM_MBUTTONDOWN.</span></span>
<span data-ttu-id="ed35f-217">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_UP</span><span class="sxs-lookup"><span data-stu-id="ed35f-217">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_UP</span></span>            | <span data-ttu-id="ed35f-218">Средняя кнопка: событие мыши, WM_MBUTTONUP.</span><span class="sxs-lookup"><span data-stu-id="ed35f-218">Middle button up mouse event, WM_MBUTTONUP.</span></span>
<span data-ttu-id="ed35f-219">COREWEBVIEW2_MOUSE_EVENT_KIND_MOVE</span><span class="sxs-lookup"><span data-stu-id="ed35f-219">COREWEBVIEW2_MOUSE_EVENT_KIND_MOVE</span></span>            | <span data-ttu-id="ed35f-220">Событие перемещения мыши, WM_MOUSEMOVE.</span><span class="sxs-lookup"><span data-stu-id="ed35f-220">Mouse move event, WM_MOUSEMOVE.</span></span>
<span data-ttu-id="ed35f-221">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_DOUBLE_CLICK</span><span class="sxs-lookup"><span data-stu-id="ed35f-221">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_DOUBLE_CLICK</span></span>            | <span data-ttu-id="ed35f-222">Щелчок правой кнопкой мыши дважды щелкните событие мыши, WM_RBUTTONDBLCLK.</span><span class="sxs-lookup"><span data-stu-id="ed35f-222">Right button double click mouse event, WM_RBUTTONDBLCLK.</span></span>
<span data-ttu-id="ed35f-223">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_DOWN</span><span class="sxs-lookup"><span data-stu-id="ed35f-223">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_DOWN</span></span>            | <span data-ttu-id="ed35f-224">Щелчок правой кнопкой мыши, WM_RBUTTONDOWN.</span><span class="sxs-lookup"><span data-stu-id="ed35f-224">Right button down mouse event, WM_RBUTTONDOWN.</span></span>
<span data-ttu-id="ed35f-225">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_UP</span><span class="sxs-lookup"><span data-stu-id="ed35f-225">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_UP</span></span>            | <span data-ttu-id="ed35f-226">Щелкните правой кнопкой мыши событие мыши, WM_RBUTTONUP.</span><span class="sxs-lookup"><span data-stu-id="ed35f-226">Right button up mouse event, WM_RBUTTONUP.</span></span>
<span data-ttu-id="ed35f-227">COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL</span><span class="sxs-lookup"><span data-stu-id="ed35f-227">COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL</span></span>            | <span data-ttu-id="ed35f-228">Событие прокрутки колесика мыши, WM_MOUSEWHEEL.</span><span class="sxs-lookup"><span data-stu-id="ed35f-228">Mouse wheel scroll event, WM_MOUSEWHEEL.</span></span>
<span data-ttu-id="ed35f-229">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOUBLE_CLICK</span><span class="sxs-lookup"><span data-stu-id="ed35f-229">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOUBLE_CLICK</span></span>            | <span data-ttu-id="ed35f-230">Первая или вторая кнопка X дважды щелкните событие мыши, WM_XBUTTONDBLCLK.</span><span class="sxs-lookup"><span data-stu-id="ed35f-230">First or second X button double click mouse event, WM_XBUTTONDBLCLK.</span></span>
<span data-ttu-id="ed35f-231">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOWN</span><span class="sxs-lookup"><span data-stu-id="ed35f-231">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOWN</span></span>            | <span data-ttu-id="ed35f-232">Первая или вторая кнопка X вниз, WM_XBUTTONDOWN.</span><span class="sxs-lookup"><span data-stu-id="ed35f-232">First or second X button down mouse event, WM_XBUTTONDOWN.</span></span>
<span data-ttu-id="ed35f-233">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_UP</span><span class="sxs-lookup"><span data-stu-id="ed35f-233">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_UP</span></span>            | <span data-ttu-id="ed35f-234">Первая или вторая кнопка X — событие мыши, WM_XBUTTONUP.</span><span class="sxs-lookup"><span data-stu-id="ed35f-234">First or second X button up mouse event, WM_XBUTTONUP.</span></span>

<span data-ttu-id="ed35f-235">Значения этого перечисления выравниваются с учетом соответствующих оконных сообщений WM_ \*.</span><span class="sxs-lookup"><span data-stu-id="ed35f-235">The values of this enum align with the matching WM_\* window messages.</span></span>

#### <span data-ttu-id="ed35f-236">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS</span><span class="sxs-lookup"><span data-stu-id="ed35f-236">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS</span></span> 

<span data-ttu-id="ed35f-237">Виртуальные ключи событий мыши, связанные с COREWEBVIEW2_MOUSE_EVENT_KINDом для SendMouseInput.</span><span class="sxs-lookup"><span data-stu-id="ed35f-237">Mouse event virtual keys associated with a COREWEBVIEW2_MOUSE_EVENT_KIND for SendMouseInput.</span></span>

> <span data-ttu-id="ed35f-238">[COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS](#corewebview2_mouse_event_virtual_keys) перечисления</span><span class="sxs-lookup"><span data-stu-id="ed35f-238">enum [COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS](#corewebview2_mouse_event_virtual_keys)</span></span>

 <span data-ttu-id="ed35f-239">Данные</span><span class="sxs-lookup"><span data-stu-id="ed35f-239">Values</span></span>                         | <span data-ttu-id="ed35f-240">Описания</span><span class="sxs-lookup"><span data-stu-id="ed35f-240">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="ed35f-241">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_NONE</span><span class="sxs-lookup"><span data-stu-id="ed35f-241">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_NONE</span></span>            | <span data-ttu-id="ed35f-242">Дополнительные клавиши не нажаты.</span><span class="sxs-lookup"><span data-stu-id="ed35f-242">No additional keys pressed.</span></span>
<span data-ttu-id="ed35f-243">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_LEFT_BUTTON</span><span class="sxs-lookup"><span data-stu-id="ed35f-243">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_LEFT_BUTTON</span></span>            | <span data-ttu-id="ed35f-244">Щелчок левой кнопкой мыши не работает, MK_LBUTTON.</span><span class="sxs-lookup"><span data-stu-id="ed35f-244">Left mouse button is down, MK_LBUTTON.</span></span>
<span data-ttu-id="ed35f-245">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_RIGHT_BUTTON</span><span class="sxs-lookup"><span data-stu-id="ed35f-245">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_RIGHT_BUTTON</span></span>            | <span data-ttu-id="ed35f-246">Щелчок правой кнопкой мыши не работает, MK_RBUTTON.</span><span class="sxs-lookup"><span data-stu-id="ed35f-246">Right mouse button is down, MK_RBUTTON.</span></span>
<span data-ttu-id="ed35f-247">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_SHIFT</span><span class="sxs-lookup"><span data-stu-id="ed35f-247">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_SHIFT</span></span>            | <span data-ttu-id="ed35f-248">Клавиша SHIFT нажата вниз, MK_SHIFT.</span><span class="sxs-lookup"><span data-stu-id="ed35f-248">SHIFT key is down, MK_SHIFT.</span></span>
<span data-ttu-id="ed35f-249">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_CONTROL</span><span class="sxs-lookup"><span data-stu-id="ed35f-249">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_CONTROL</span></span>            | <span data-ttu-id="ed35f-250">Клавиша CTRL нажата, MK_CONTROL.</span><span class="sxs-lookup"><span data-stu-id="ed35f-250">CTRL key is down, MK_CONTROL.</span></span>
<span data-ttu-id="ed35f-251">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_MIDDLE_BUTTON</span><span class="sxs-lookup"><span data-stu-id="ed35f-251">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_MIDDLE_BUTTON</span></span>            | <span data-ttu-id="ed35f-252">Средняя нажатие кнопки мыши не работает, MK_MBUTTON.</span><span class="sxs-lookup"><span data-stu-id="ed35f-252">Middle mouse button is down, MK_MBUTTON.</span></span>
<span data-ttu-id="ed35f-253">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_X_BUTTON1</span><span class="sxs-lookup"><span data-stu-id="ed35f-253">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_X_BUTTON1</span></span>            | <span data-ttu-id="ed35f-254">Первая кнопка X нажата MK_XBUTTON1.</span><span class="sxs-lookup"><span data-stu-id="ed35f-254">First X button is down, MK_XBUTTON1.</span></span>
<span data-ttu-id="ed35f-255">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_X_BUTTON2</span><span class="sxs-lookup"><span data-stu-id="ed35f-255">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_X_BUTTON2</span></span>            | <span data-ttu-id="ed35f-256">Вторая кнопка X нажата MK_XBUTTON2.</span><span class="sxs-lookup"><span data-stu-id="ed35f-256">Second X button is down, MK_XBUTTON2.</span></span>

<span data-ttu-id="ed35f-257">Эти значения можно объединить в битовый флаг, если для события была нажата несколько виртуальных клавиш.</span><span class="sxs-lookup"><span data-stu-id="ed35f-257">These values can be combined into a bit flag if more than one virtual key is pressed for the event.</span></span> <span data-ttu-id="ed35f-258">Значения этого перечисления выравниваются с соответствующими клавишами мыши MK_ \*.</span><span class="sxs-lookup"><span data-stu-id="ed35f-258">The values of this enum align with the matching MK_\* mouse keys.</span></span>

#### <span data-ttu-id="ed35f-259">COREWEBVIEW2_POINTER_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="ed35f-259">COREWEBVIEW2_POINTER_EVENT_KIND</span></span> 

<span data-ttu-id="ed35f-260">Тип события указателя, используемый функцией SendPointerInput для передачи типа события указателя, отправляемого в WebView.</span><span class="sxs-lookup"><span data-stu-id="ed35f-260">Pointer event type used by SendPointerInput to convey the type of pointer event being sent to WebView.</span></span>

> <span data-ttu-id="ed35f-261">[COREWEBVIEW2_POINTER_EVENT_KIND](#corewebview2_pointer_event_kind) перечисления</span><span class="sxs-lookup"><span data-stu-id="ed35f-261">enum [COREWEBVIEW2_POINTER_EVENT_KIND](#corewebview2_pointer_event_kind)</span></span>

 <span data-ttu-id="ed35f-262">Данные</span><span class="sxs-lookup"><span data-stu-id="ed35f-262">Values</span></span>                         | <span data-ttu-id="ed35f-263">Описания</span><span class="sxs-lookup"><span data-stu-id="ed35f-263">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="ed35f-264">COREWEBVIEW2_POINTER_EVENT_KIND_ACTIVATE</span><span class="sxs-lookup"><span data-stu-id="ed35f-264">COREWEBVIEW2_POINTER_EVENT_KIND_ACTIVATE</span></span>            | <span data-ttu-id="ed35f-265">Соответствует WM_POINTERACTIVATE.</span><span class="sxs-lookup"><span data-stu-id="ed35f-265">Corresponds to WM_POINTERACTIVATE.</span></span>
<span data-ttu-id="ed35f-266">COREWEBVIEW2_POINTER_EVENT_KIND_DOWN</span><span class="sxs-lookup"><span data-stu-id="ed35f-266">COREWEBVIEW2_POINTER_EVENT_KIND_DOWN</span></span>            | <span data-ttu-id="ed35f-267">Соответствует WM_POINTERDOWN.</span><span class="sxs-lookup"><span data-stu-id="ed35f-267">Corresponds to WM_POINTERDOWN.</span></span>
<span data-ttu-id="ed35f-268">COREWEBVIEW2_POINTER_EVENT_KIND_ENTER</span><span class="sxs-lookup"><span data-stu-id="ed35f-268">COREWEBVIEW2_POINTER_EVENT_KIND_ENTER</span></span>            | <span data-ttu-id="ed35f-269">Соответствует WM_POINTERENTER.</span><span class="sxs-lookup"><span data-stu-id="ed35f-269">Corresponds to WM_POINTERENTER.</span></span>
<span data-ttu-id="ed35f-270">COREWEBVIEW2_POINTER_EVENT_KIND_LEAVE</span><span class="sxs-lookup"><span data-stu-id="ed35f-270">COREWEBVIEW2_POINTER_EVENT_KIND_LEAVE</span></span>            | <span data-ttu-id="ed35f-271">Соответствует WM_POINTERLEAVE.</span><span class="sxs-lookup"><span data-stu-id="ed35f-271">Corresponds to WM_POINTERLEAVE.</span></span>
<span data-ttu-id="ed35f-272">COREWEBVIEW2_POINTER_EVENT_KIND_UP</span><span class="sxs-lookup"><span data-stu-id="ed35f-272">COREWEBVIEW2_POINTER_EVENT_KIND_UP</span></span>            | <span data-ttu-id="ed35f-273">Соответствует WM_POINTERUP.</span><span class="sxs-lookup"><span data-stu-id="ed35f-273">Corresponds to WM_POINTERUP.</span></span>
<span data-ttu-id="ed35f-274">COREWEBVIEW2_POINTER_EVENT_KIND_UPDATE</span><span class="sxs-lookup"><span data-stu-id="ed35f-274">COREWEBVIEW2_POINTER_EVENT_KIND_UPDATE</span></span>            | <span data-ttu-id="ed35f-275">Соответствует WM_POINTERUPDATE.</span><span class="sxs-lookup"><span data-stu-id="ed35f-275">Corresponds to WM_POINTERUPDATE.</span></span>

<span data-ttu-id="ed35f-276">Значения этого перечисления выравниваются с учетом соответствующих оконных сообщений WM_POINTER \*.</span><span class="sxs-lookup"><span data-stu-id="ed35f-276">The values of this enum align with the matching WM_POINTER\* window messages.</span></span>

