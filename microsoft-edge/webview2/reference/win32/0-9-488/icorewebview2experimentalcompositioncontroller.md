---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: e6499c77a17fd9ff4563359cdf05dc4a32f19a51
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654827"
---
# <span data-ttu-id="d53c0-104">интерфейс ICoreWebView2ExperimentalCompositionController</span><span class="sxs-lookup"><span data-stu-id="d53c0-104">interface ICoreWebView2ExperimentalCompositionController</span></span> 

> [!NOTE]
> <span data-ttu-id="d53c0-105">Это экспериментальный API-интерфейс, поставляемый с предварительной версией SDK версии 0.9.488.</span><span class="sxs-lookup"><span data-stu-id="d53c0-105">This an experimental API that is shipped with our prerelease SDK version 0.9.488.</span></span>

```
interface ICoreWebView2ExperimentalCompositionController
  : public IUnknown
```

<span data-ttu-id="d53c0-106">Этот интерфейс является расширением интерфейса ICoreWebView2Controller для поддержки визуального размещения.</span><span class="sxs-lookup"><span data-stu-id="d53c0-106">This interface is an extension of the ICoreWebView2Controller interface to support visual hosting.</span></span>

## <span data-ttu-id="d53c0-107">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="d53c0-107">Summary</span></span>

 <span data-ttu-id="d53c0-108">Участников</span><span class="sxs-lookup"><span data-stu-id="d53c0-108">Members</span></span>                        | <span data-ttu-id="d53c0-109">Описания</span><span class="sxs-lookup"><span data-stu-id="d53c0-109">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d53c0-110">add_CursorChanged</span><span class="sxs-lookup"><span data-stu-id="d53c0-110">add_CursorChanged</span></span>](#add_cursorchanged) | <span data-ttu-id="d53c0-111">Добавьте обработчик событий для события CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="d53c0-111">Add an event handler for the CursorChanged event.</span></span>
[<span data-ttu-id="d53c0-112">CreateCoreWebView2PointerInfoFromPointerId</span><span class="sxs-lookup"><span data-stu-id="d53c0-112">CreateCoreWebView2PointerInfoFromPointerId</span></span>](#createcorewebview2pointerinfofrompointerid) | <span data-ttu-id="d53c0-113">Вспомогательная функция для преобразования pointerId, полученного из системы, в [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).</span><span class="sxs-lookup"><span data-stu-id="d53c0-113">A helper function to convert a pointerId received from the system into an [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).</span></span>
[<span data-ttu-id="d53c0-114">get_Cursor</span><span class="sxs-lookup"><span data-stu-id="d53c0-114">get_Cursor</span></span>](#get_cursor) | <span data-ttu-id="d53c0-115">Текущий курсор, WebView рассчитает, что он должен быть.</span><span class="sxs-lookup"><span data-stu-id="d53c0-115">The current cursor that WebView thinks it should be.</span></span>
[<span data-ttu-id="d53c0-116">get_RootVisualTarget</span><span class="sxs-lookup"><span data-stu-id="d53c0-116">get_RootVisualTarget</span></span>](#get_rootvisualtarget) | <span data-ttu-id="d53c0-117">RootVisualTarget — это визуальный элемент в визуальном дереве размещающего приложения.</span><span class="sxs-lookup"><span data-stu-id="d53c0-117">The RootVisualTarget is a visual in the hosting app's visual tree.</span></span>
[<span data-ttu-id="d53c0-118">get_UIAProvider</span><span class="sxs-lookup"><span data-stu-id="d53c0-118">get_UIAProvider</span></span>](#get_uiaprovider) | <span data-ttu-id="d53c0-119">Возвращает поставщик модели автоматизации пользовательского интерфейса для WebView.</span><span class="sxs-lookup"><span data-stu-id="d53c0-119">Returns the UI Automation Provider for the WebView.</span></span>
[<span data-ttu-id="d53c0-120">put_RootVisualTarget</span><span class="sxs-lookup"><span data-stu-id="d53c0-120">put_RootVisualTarget</span></span>](#put_rootvisualtarget) | <span data-ttu-id="d53c0-121">Задайте свойство RootVisualTarget.</span><span class="sxs-lookup"><span data-stu-id="d53c0-121">Set the RootVisualTarget property.</span></span>
[<span data-ttu-id="d53c0-122">remove_CursorChanged</span><span class="sxs-lookup"><span data-stu-id="d53c0-122">remove_CursorChanged</span></span>](#remove_cursorchanged) | <span data-ttu-id="d53c0-123">Удалите обработчик событий, добавленный ранее add_CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="d53c0-123">Remove an event handler previously added with add_CursorChanged.</span></span>
[<span data-ttu-id="d53c0-124">SendMouseInput</span><span class="sxs-lookup"><span data-stu-id="d53c0-124">SendMouseInput</span></span>](#sendmouseinput) | <span data-ttu-id="d53c0-125">Если eventKind COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL или COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL, mouseData задает величину движения колесика.</span><span class="sxs-lookup"><span data-stu-id="d53c0-125">If eventKind is COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL or COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL, then mouseData specifies the amount of wheel movement.</span></span>
[<span data-ttu-id="d53c0-126">SendPointerInput</span><span class="sxs-lookup"><span data-stu-id="d53c0-126">SendPointerInput</span></span>](#sendpointerinput) | <span data-ttu-id="d53c0-127">SendPointerInput принимает вводные данные и указатель пера для типов, определенных в COREWEBVIEW2_POINTER_EVENT_KIND.</span><span class="sxs-lookup"><span data-stu-id="d53c0-127">SendPointerInput accepts touch or pen pointer input of types defined in COREWEBVIEW2_POINTER_EVENT_KIND.</span></span>
[<span data-ttu-id="d53c0-128">COREWEBVIEW2_MATRIX_4X4</span><span class="sxs-lookup"><span data-stu-id="d53c0-128">COREWEBVIEW2_MATRIX_4X4</span></span>](#corewebview2_matrix_4x4) | <span data-ttu-id="d53c0-129">Матрица, представляющая трехмерное преобразование.</span><span class="sxs-lookup"><span data-stu-id="d53c0-129">Matrix that represents a 3D transform.</span></span>
[<span data-ttu-id="d53c0-130">COREWEBVIEW2_MOUSE_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="d53c0-130">COREWEBVIEW2_MOUSE_EVENT_KIND</span></span>](#corewebview2_mouse_event_kind) | <span data-ttu-id="d53c0-131">Тип событий мыши, используемый функцией SendMouseInput для передачи типа события мыши, отправляемого в WebView.</span><span class="sxs-lookup"><span data-stu-id="d53c0-131">Mouse event type used by SendMouseInput to convey the type of mouse event being sent to WebView.</span></span>
[<span data-ttu-id="d53c0-132">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS</span><span class="sxs-lookup"><span data-stu-id="d53c0-132">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS</span></span>](#corewebview2_mouse_event_virtual_keys) | <span data-ttu-id="d53c0-133">Виртуальные ключи событий мыши, связанные с COREWEBVIEW2_MOUSE_EVENT_KINDом для SendMouseInput.</span><span class="sxs-lookup"><span data-stu-id="d53c0-133">Mouse event virtual keys associated with a COREWEBVIEW2_MOUSE_EVENT_KIND for SendMouseInput.</span></span>
[<span data-ttu-id="d53c0-134">COREWEBVIEW2_POINTER_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="d53c0-134">COREWEBVIEW2_POINTER_EVENT_KIND</span></span>](#corewebview2_pointer_event_kind) | <span data-ttu-id="d53c0-135">Тип события указателя, используемый функцией SendPointerInput для передачи типа события указателя, отправляемого в WebView.</span><span class="sxs-lookup"><span data-stu-id="d53c0-135">Pointer event type used by SendPointerInput to convey the type of pointer event being sent to WebView.</span></span>

<span data-ttu-id="d53c0-136">Объект, реализующий интерфейс ICoreWebView2ExperimentalCompositionController, также будет реализовывать ICoreWebView2Controller.</span><span class="sxs-lookup"><span data-stu-id="d53c0-136">An object implementing the ICoreWebView2ExperimentalCompositionController interface will also implement ICoreWebView2Controller.</span></span> <span data-ttu-id="d53c0-137">Предполагается, что вызывающие объекты используют ICoreWebView2Controller для изменения размера, видимости, фокусировки и т. д., а затем используют ICoreWebView2ExperimentalCompositionController для подключения к дереву композиции и предоставления входных данных для WebView.</span><span class="sxs-lookup"><span data-stu-id="d53c0-137">Callers are expected to use ICoreWebView2Controller for resizing, visibility, focus, and so on, and then use ICoreWebView2ExperimentalCompositionController to connect to a composition tree and provide input meant for the WebView.</span></span>

## <span data-ttu-id="d53c0-138">Участников</span><span class="sxs-lookup"><span data-stu-id="d53c0-138">Members</span></span>

#### <span data-ttu-id="d53c0-139">add_CursorChanged</span><span class="sxs-lookup"><span data-stu-id="d53c0-139">add_CursorChanged</span></span> 

<span data-ttu-id="d53c0-140">Добавьте обработчик событий для события CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="d53c0-140">Add an event handler for the CursorChanged event.</span></span>

> <span data-ttu-id="d53c0-141">общедоступные значения HRESULT [add_CursorChanged](#add_cursorchanged)([ICoreWebView2ExperimentalCursorChangedEventHandler](icorewebview2experimentalcursorchangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="d53c0-141">public HRESULT [add_CursorChanged](#add_cursorchanged)([ICoreWebView2ExperimentalCursorChangedEventHandler](icorewebview2experimentalcursorchangedeventhandler.md) \* eventHandler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="d53c0-142">Событие срабатывает, когда WebView считает, что курсор должен быть изменен.</span><span class="sxs-lookup"><span data-stu-id="d53c0-142">The event fires when WebView thinks the cursor should be changed.</span></span> <span data-ttu-id="d53c0-143">Например, если курсор мыши установлен по умолчанию, но затем перемещается поверх текста, он может попытаться перейти на курсор IBeam.</span><span class="sxs-lookup"><span data-stu-id="d53c0-143">For example, when the mouse cursor is currently the default cursor but is then moved over text, it may try to change to the IBeam cursor.</span></span>

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

#### <span data-ttu-id="d53c0-144">CreateCoreWebView2PointerInfoFromPointerId</span><span class="sxs-lookup"><span data-stu-id="d53c0-144">CreateCoreWebView2PointerInfoFromPointerId</span></span> 

<span data-ttu-id="d53c0-145">Вспомогательная функция для преобразования pointerId, полученного из системы, в [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).</span><span class="sxs-lookup"><span data-stu-id="d53c0-145">A helper function to convert a pointerId received from the system into an [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).</span></span>

> <span data-ttu-id="d53c0-146">общедоступные значения HRESULT [CreateCoreWebView2PointerInfoFromPointerId](#createcorewebview2pointerinfofrompointerid)(uint POINTERID, HWND parentWindow, struct COREWEBVIEW2_MATRIX_4X4 Transform, [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) \* \* pointerInfo)</span><span class="sxs-lookup"><span data-stu-id="d53c0-146">public HRESULT [CreateCoreWebView2PointerInfoFromPointerId](#createcorewebview2pointerinfofrompointerid)(UINT pointerId, HWND parentWindow, struct COREWEBVIEW2_MATRIX_4X4 transform, [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) \*\* pointerInfo)</span></span>

<span data-ttu-id="d53c0-147">parentWindow — HWND, который содержит WebView.</span><span class="sxs-lookup"><span data-stu-id="d53c0-147">parentWindow is the HWND that contains the webview.</span></span> <span data-ttu-id="d53c0-148">Это может быть любой HWND в дереве HWND, который включает WebView.</span><span class="sxs-lookup"><span data-stu-id="d53c0-148">This can be any HWND in the hwnd tree that contains the webview.</span></span> <span data-ttu-id="d53c0-149">COREWEBVIEW2_MATRIX_4X4 является преобразованием из дескриптора HWND в WebView.</span><span class="sxs-lookup"><span data-stu-id="d53c0-149">The COREWEBVIEW2_MATRIX_4X4 is the transform from that HWND to the webview.</span></span> <span data-ttu-id="d53c0-150">Возвращенный [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) используется в SendPointerInfo.</span><span class="sxs-lookup"><span data-stu-id="d53c0-150">The returned [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) is used in SendPointerInfo.</span></span> <span data-ttu-id="d53c0-151">Тип указателя должен быть либо пером, либо сенсорным, либо функция завершится сбоем.</span><span class="sxs-lookup"><span data-stu-id="d53c0-151">The pointer type must be either pen or touch or the function will fail.</span></span>



#### <span data-ttu-id="d53c0-152">get_Cursor</span><span class="sxs-lookup"><span data-stu-id="d53c0-152">get_Cursor</span></span> 

<span data-ttu-id="d53c0-153">Текущий курсор, WebView рассчитает, что он должен быть.</span><span class="sxs-lookup"><span data-stu-id="d53c0-153">The current cursor that WebView thinks it should be.</span></span>

> <span data-ttu-id="d53c0-154">общедоступные значения HRESULT [get_Cursor](#get_cursor)(HCURSOR \* Cursor)</span><span class="sxs-lookup"><span data-stu-id="d53c0-154">public HRESULT [get_Cursor](#get_cursor)(HCURSOR \* cursor)</span></span>

<span data-ttu-id="d53c0-155">Курсор должен быть установлен в WM_SETCURSOR с помощью:: SetCursor или установлен на соответствующий родительский или предок родительского объекта WebView By:: SetClassLongPtr.</span><span class="sxs-lookup"><span data-stu-id="d53c0-155">The cursor should be set in WM_SETCURSOR through ::SetCursor or set on the corresponding parent/ancestor HWND of the WebView through ::SetClassLongPtr.</span></span> <span data-ttu-id="d53c0-156">HCURSOR можно освободить таким образом, чтобы CopyCursor и DestroyCursor, чтобы сохранить собственную копию, если вы еще не настраиваете курсор.</span><span class="sxs-lookup"><span data-stu-id="d53c0-156">The HCURSOR can be freed so CopyCursor/DestroyCursor is recommended to keep your own copy if you are doing more than immediately setting the cursor.</span></span>

#### <span data-ttu-id="d53c0-157">get_RootVisualTarget</span><span class="sxs-lookup"><span data-stu-id="d53c0-157">get_RootVisualTarget</span></span> 

<span data-ttu-id="d53c0-158">RootVisualTarget — это визуальный элемент в визуальном дереве размещающего приложения.</span><span class="sxs-lookup"><span data-stu-id="d53c0-158">The RootVisualTarget is a visual in the hosting app's visual tree.</span></span>

> <span data-ttu-id="d53c0-159">общедоступные значения HRESULT [get_RootVisualTarget](#get_rootvisualtarget)(IUnknown \* \* Target)</span><span class="sxs-lookup"><span data-stu-id="d53c0-159">public HRESULT [get_RootVisualTarget](#get_rootvisualtarget)(IUnknown \*\* target)</span></span>

<span data-ttu-id="d53c0-160">Этот визуальный элемент — это то, где WebView будет подключаться к визуальному дереву.</span><span class="sxs-lookup"><span data-stu-id="d53c0-160">This visual is where the WebView will connect its visual tree.</span></span> <span data-ttu-id="d53c0-161">Приложение использует этот визуальный элемент, чтобы расположить WebView в приложении.</span><span class="sxs-lookup"><span data-stu-id="d53c0-161">The app uses this visual to position the WebView within the app.</span></span> <span data-ttu-id="d53c0-162">Чтобы изменить размер WebView, приложению по-прежнему нужно использовать свойство Boundss.</span><span class="sxs-lookup"><span data-stu-id="d53c0-162">The app still needs to use the Bounds property to size the WebView.</span></span> <span data-ttu-id="d53c0-163">Свойством RootVisualTarget может быть IDCompositionVisual или Windows:: UI:: композиция:: ContainerVisual.</span><span class="sxs-lookup"><span data-stu-id="d53c0-163">The RootVisualTarget property can be an IDCompositionVisual or a Windows::UI::Composition::ContainerVisual.</span></span> <span data-ttu-id="d53c0-164">WebView подключится к визуальному дереву для предоставленного визуального элемента перед возвратом из метода присваивания свойств.</span><span class="sxs-lookup"><span data-stu-id="d53c0-164">WebView will connect its visual tree to the provided visual before returning from the property setter.</span></span> <span data-ttu-id="d53c0-165">Приложение должно быть зафиксировано на своем устройстве, в котором задано свойство RootVisualTarget.</span><span class="sxs-lookup"><span data-stu-id="d53c0-165">The app needs to commit on its device setting the RootVisualTarget property.</span></span> <span data-ttu-id="d53c0-166">Свойство RootVisualTarget поддерживает значение nullptr, чтобы отключить WebView от визуального дерева приложения.</span><span class="sxs-lookup"><span data-stu-id="d53c0-166">The RootVisualTarget property supports being set to nullptr to disconnect the WebView from the app's visual tree.</span></span> 
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

#### <span data-ttu-id="d53c0-167">get_UIAProvider</span><span class="sxs-lookup"><span data-stu-id="d53c0-167">get_UIAProvider</span></span> 

<span data-ttu-id="d53c0-168">Возвращает поставщик модели автоматизации пользовательского интерфейса для WebView.</span><span class="sxs-lookup"><span data-stu-id="d53c0-168">Returns the UI Automation Provider for the WebView.</span></span>

> <span data-ttu-id="d53c0-169">общедоступные значения HRESULT [get_UIAProvider](#get_uiaprovider)(IUnknown \* \* Provider)</span><span class="sxs-lookup"><span data-stu-id="d53c0-169">public HRESULT [get_UIAProvider](#get_uiaprovider)(IUnknown \*\* provider)</span></span>

#### <span data-ttu-id="d53c0-170">put_RootVisualTarget</span><span class="sxs-lookup"><span data-stu-id="d53c0-170">put_RootVisualTarget</span></span> 

<span data-ttu-id="d53c0-171">Задайте свойство RootVisualTarget.</span><span class="sxs-lookup"><span data-stu-id="d53c0-171">Set the RootVisualTarget property.</span></span>

> <span data-ttu-id="d53c0-172">общедоступные значения HRESULT [put_RootVisualTarget](#put_rootvisualtarget)(объект IUnknown \*)</span><span class="sxs-lookup"><span data-stu-id="d53c0-172">public HRESULT [put_RootVisualTarget](#put_rootvisualtarget)(IUnknown \* target)</span></span>

#### <span data-ttu-id="d53c0-173">remove_CursorChanged</span><span class="sxs-lookup"><span data-stu-id="d53c0-173">remove_CursorChanged</span></span> 

<span data-ttu-id="d53c0-174">Удалите обработчик событий, добавленный ранее add_CursorChanged.</span><span class="sxs-lookup"><span data-stu-id="d53c0-174">Remove an event handler previously added with add_CursorChanged.</span></span>

> <span data-ttu-id="d53c0-175">общедоступные значения HRESULT [remove_CursorChanged](#remove_cursorchanged)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="d53c0-175">public HRESULT [remove_CursorChanged](#remove_cursorchanged)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="d53c0-176">SendMouseInput</span><span class="sxs-lookup"><span data-stu-id="d53c0-176">SendMouseInput</span></span> 

<span data-ttu-id="d53c0-177">Если eventKind COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL или COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL, mouseData задает величину движения колесика.</span><span class="sxs-lookup"><span data-stu-id="d53c0-177">If eventKind is COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL or COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL, then mouseData specifies the amount of wheel movement.</span></span>

> <span data-ttu-id="d53c0-178">Public HRESULT [SendMouseInput](#sendmouseinput)([COREWEBVIEW2_MOUSE_EVENT_KIND](#corewebview2_mouse_event_kind) eventKind, [COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS](#corewebview2_mouse_event_virtual_keys) virtualKeys, UINT32 mouseData, точка Point)</span><span class="sxs-lookup"><span data-stu-id="d53c0-178">public HRESULT [SendMouseInput](#sendmouseinput)([COREWEBVIEW2_MOUSE_EVENT_KIND](#corewebview2_mouse_event_kind) eventKind, [COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS](#corewebview2_mouse_event_virtual_keys) virtualKeys, UINT32 mouseData, POINT point)</span></span>

<span data-ttu-id="d53c0-179">Положительное значение указывает на то, что колесико было повернуто вперед от пользователя; отрицательное значение указывает на то, что колесико было повернуто на обратном направлении к пользователю.</span><span class="sxs-lookup"><span data-stu-id="d53c0-179">A positive value indicates that the wheel was rotated forward, away from the user; a negative value indicates that the wheel was rotated backward, toward the user.</span></span> <span data-ttu-id="d53c0-180">Один щелчок мыши определяется как WHEEL_DELTA (120).</span><span class="sxs-lookup"><span data-stu-id="d53c0-180">One wheel click is defined as WHEEL_DELTA, which is 120.</span></span> <span data-ttu-id="d53c0-181">Если eventKind COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOUBLE_CLICK COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOWN или COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_UP, то mouseData указывает, какие кнопки X были нажаты или отпущены.</span><span class="sxs-lookup"><span data-stu-id="d53c0-181">If eventKind is COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOUBLE_CLICK COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOWN, or COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_UP, then mouseData specifies which X buttons were pressed or released.</span></span> <span data-ttu-id="d53c0-182">Это значение должно быть 1, если первая кнопка X нажата/выпущена, и 2 при нажатии или отпускании второй кнопки X.</span><span class="sxs-lookup"><span data-stu-id="d53c0-182">This value should be 1 if the first X button is pressed/released and 2 if the second X button is pressed/released.</span></span> <span data-ttu-id="d53c0-183">Если eventKind COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE, то virtualKeys, mouseData и Point должны равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="d53c0-183">If eventKind is COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE, then virtualKeys, mouseData, and point should all be zero.</span></span> <span data-ttu-id="d53c0-184">Если eventKind — любое другое значение, mouseData должно равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="d53c0-184">If eventKind is any other value, then mouseData should be zero.</span></span> <span data-ttu-id="d53c0-185">Ожидается, что точка должна находиться в пространстве координат клиента WebView.</span><span class="sxs-lookup"><span data-stu-id="d53c0-185">Point is expected to be in the client coordinate space of the WebView.</span></span> <span data-ttu-id="d53c0-186">Для отслеживания событий мыши, которые запускаются в WebView и потенциально могут перемещаться за пределы WebView и ведущего приложения, рекомендуется использовать вызов SetCapture и ReleaseCapture.</span><span class="sxs-lookup"><span data-stu-id="d53c0-186">To track mouse events that start in the WebView and can potentially move outside of the WebView and host application, calling SetCapture and ReleaseCapture is recommended.</span></span> <span data-ttu-id="d53c0-187">Чтобы выйти из всплывающих окон, также рекомендуется отправлять WM_MOUSELEAVE сообщения.</span><span class="sxs-lookup"><span data-stu-id="d53c0-187">To dismiss hover popups, it is also recommended to send WM_MOUSELEAVE messages.</span></span> 
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

#### <span data-ttu-id="d53c0-188">SendPointerInput</span><span class="sxs-lookup"><span data-stu-id="d53c0-188">SendPointerInput</span></span> 

<span data-ttu-id="d53c0-189">SendPointerInput принимает вводные данные и указатель пера для типов, определенных в COREWEBVIEW2_POINTER_EVENT_KIND.</span><span class="sxs-lookup"><span data-stu-id="d53c0-189">SendPointerInput accepts touch or pen pointer input of types defined in COREWEBVIEW2_POINTER_EVENT_KIND.</span></span>

> <span data-ttu-id="d53c0-190">Public HRESULT [SendPointerInput](#sendpointerinput)([COREWEBVIEW2_POINTER_EVENT_KIND](#corewebview2_pointer_event_kind) EventType, [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) \* pointerInfo)</span><span class="sxs-lookup"><span data-stu-id="d53c0-190">public HRESULT [SendPointerInput](#sendpointerinput)([COREWEBVIEW2_POINTER_EVENT_KIND](#corewebview2_pointer_event_kind) eventType, [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) \* pointerInfo)</span></span>

<span data-ttu-id="d53c0-191">Все входные данные указателя из системы должны быть преобразованы в [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) первыми.</span><span class="sxs-lookup"><span data-stu-id="d53c0-191">Any pointer input from the system must be converted into an [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) first.</span></span>

#### <span data-ttu-id="d53c0-192">COREWEBVIEW2_MATRIX_4X4</span><span class="sxs-lookup"><span data-stu-id="d53c0-192">COREWEBVIEW2_MATRIX_4X4</span></span> 

<span data-ttu-id="d53c0-193">Матрица, представляющая трехмерное преобразование.</span><span class="sxs-lookup"><span data-stu-id="d53c0-193">Matrix that represents a 3D transform.</span></span>

> <span data-ttu-id="d53c0-194">typedef [COREWEBVIEW2_MATRIX_4X4](#corewebview2_matrix_4x4)</span><span class="sxs-lookup"><span data-stu-id="d53c0-194">typedef [COREWEBVIEW2_MATRIX_4X4](#corewebview2_matrix_4x4)</span></span>

<span data-ttu-id="d53c0-195">Это преобразование используется для вычисления правильных координат при вызове CreateCoreWebView2PointerInfoFromPointerId.</span><span class="sxs-lookup"><span data-stu-id="d53c0-195">This transform is used to calculate correct coordinates when calling CreateCoreWebView2PointerInfoFromPointerId.</span></span> <span data-ttu-id="d53c0-196">Это эквивалентно D2D1_MATRIX_4X4_F</span><span class="sxs-lookup"><span data-stu-id="d53c0-196">This is equivalent to a D2D1_MATRIX_4X4_F</span></span>

#### <span data-ttu-id="d53c0-197">COREWEBVIEW2_MOUSE_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="d53c0-197">COREWEBVIEW2_MOUSE_EVENT_KIND</span></span> 

<span data-ttu-id="d53c0-198">Тип событий мыши, используемый функцией SendMouseInput для передачи типа события мыши, отправляемого в WebView.</span><span class="sxs-lookup"><span data-stu-id="d53c0-198">Mouse event type used by SendMouseInput to convey the type of mouse event being sent to WebView.</span></span>

> <span data-ttu-id="d53c0-199">[COREWEBVIEW2_MOUSE_EVENT_KIND](#corewebview2_mouse_event_kind) перечисления</span><span class="sxs-lookup"><span data-stu-id="d53c0-199">enum [COREWEBVIEW2_MOUSE_EVENT_KIND](#corewebview2_mouse_event_kind)</span></span>

 <span data-ttu-id="d53c0-200">Данные</span><span class="sxs-lookup"><span data-stu-id="d53c0-200">Values</span></span>                         | <span data-ttu-id="d53c0-201">Описания</span><span class="sxs-lookup"><span data-stu-id="d53c0-201">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="d53c0-202">COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL</span><span class="sxs-lookup"><span data-stu-id="d53c0-202">COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL</span></span>            | <span data-ttu-id="d53c0-203">Событие прокрутки колесика мыши по горизонтали WM_MOUSEHWHEEL.</span><span class="sxs-lookup"><span data-stu-id="d53c0-203">Mouse horizontal wheel scroll event, WM_MOUSEHWHEEL.</span></span>
<span data-ttu-id="d53c0-204">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_DOUBLE_CLICK</span><span class="sxs-lookup"><span data-stu-id="d53c0-204">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_DOUBLE_CLICK</span></span>            | <span data-ttu-id="d53c0-205">Левая кнопка дважды щелкните событие мыши, WM_LBUTTONDBLCLK.</span><span class="sxs-lookup"><span data-stu-id="d53c0-205">Left button double click mouse event, WM_LBUTTONDBLCLK.</span></span>
<span data-ttu-id="d53c0-206">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_DOWN</span><span class="sxs-lookup"><span data-stu-id="d53c0-206">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_DOWN</span></span>            | <span data-ttu-id="d53c0-207">Левая кнопка вниз события мыши, WM_LBUTTONDOWN.</span><span class="sxs-lookup"><span data-stu-id="d53c0-207">Left button down mouse event, WM_LBUTTONDOWN.</span></span>
<span data-ttu-id="d53c0-208">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_UP</span><span class="sxs-lookup"><span data-stu-id="d53c0-208">COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_UP</span></span>            | <span data-ttu-id="d53c0-209">Левая кнопка — событие мыши, WM_LBUTTONUP.</span><span class="sxs-lookup"><span data-stu-id="d53c0-209">Left button up mouse event, WM_LBUTTONUP.</span></span>
<span data-ttu-id="d53c0-210">COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE</span><span class="sxs-lookup"><span data-stu-id="d53c0-210">COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE</span></span>            | <span data-ttu-id="d53c0-211">Событие выхода из мыши, WM_MOUSELEAVE.</span><span class="sxs-lookup"><span data-stu-id="d53c0-211">Mouse leave event, WM_MOUSELEAVE.</span></span>
<span data-ttu-id="d53c0-212">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_DOUBLE_CLICK</span><span class="sxs-lookup"><span data-stu-id="d53c0-212">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_DOUBLE_CLICK</span></span>            | <span data-ttu-id="d53c0-213">Средняя кнопка дважды щелкните событие мыши, WM_MBUTTONDBLCLK.</span><span class="sxs-lookup"><span data-stu-id="d53c0-213">Middle button double click mouse event, WM_MBUTTONDBLCLK.</span></span>
<span data-ttu-id="d53c0-214">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_DOWN</span><span class="sxs-lookup"><span data-stu-id="d53c0-214">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_DOWN</span></span>            | <span data-ttu-id="d53c0-215">Средняя кнопка вниз: событие мыши, WM_MBUTTONDOWN.</span><span class="sxs-lookup"><span data-stu-id="d53c0-215">Middle button down mouse event, WM_MBUTTONDOWN.</span></span>
<span data-ttu-id="d53c0-216">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_UP</span><span class="sxs-lookup"><span data-stu-id="d53c0-216">COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_UP</span></span>            | <span data-ttu-id="d53c0-217">Средняя кнопка: событие мыши, WM_MBUTTONUP.</span><span class="sxs-lookup"><span data-stu-id="d53c0-217">Middle button up mouse event, WM_MBUTTONUP.</span></span>
<span data-ttu-id="d53c0-218">COREWEBVIEW2_MOUSE_EVENT_KIND_MOVE</span><span class="sxs-lookup"><span data-stu-id="d53c0-218">COREWEBVIEW2_MOUSE_EVENT_KIND_MOVE</span></span>            | <span data-ttu-id="d53c0-219">Событие перемещения мыши, WM_MOUSEMOVE.</span><span class="sxs-lookup"><span data-stu-id="d53c0-219">Mouse move event, WM_MOUSEMOVE.</span></span>
<span data-ttu-id="d53c0-220">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_DOUBLE_CLICK</span><span class="sxs-lookup"><span data-stu-id="d53c0-220">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_DOUBLE_CLICK</span></span>            | <span data-ttu-id="d53c0-221">Щелчок правой кнопкой мыши дважды щелкните событие мыши, WM_RBUTTONDBLCLK.</span><span class="sxs-lookup"><span data-stu-id="d53c0-221">Right button double click mouse event, WM_RBUTTONDBLCLK.</span></span>
<span data-ttu-id="d53c0-222">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_DOWN</span><span class="sxs-lookup"><span data-stu-id="d53c0-222">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_DOWN</span></span>            | <span data-ttu-id="d53c0-223">Щелчок правой кнопкой мыши, WM_RBUTTONDOWN.</span><span class="sxs-lookup"><span data-stu-id="d53c0-223">Right button down mouse event, WM_RBUTTONDOWN.</span></span>
<span data-ttu-id="d53c0-224">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_UP</span><span class="sxs-lookup"><span data-stu-id="d53c0-224">COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_UP</span></span>            | <span data-ttu-id="d53c0-225">Щелкните правой кнопкой мыши событие мыши, WM_RBUTTONUP.</span><span class="sxs-lookup"><span data-stu-id="d53c0-225">Right button up mouse event, WM_RBUTTONUP.</span></span>
<span data-ttu-id="d53c0-226">COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL</span><span class="sxs-lookup"><span data-stu-id="d53c0-226">COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL</span></span>            | <span data-ttu-id="d53c0-227">Событие прокрутки колесика мыши, WM_MOUSEWHEEL.</span><span class="sxs-lookup"><span data-stu-id="d53c0-227">Mouse wheel scroll event, WM_MOUSEWHEEL.</span></span>
<span data-ttu-id="d53c0-228">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOUBLE_CLICK</span><span class="sxs-lookup"><span data-stu-id="d53c0-228">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOUBLE_CLICK</span></span>            | <span data-ttu-id="d53c0-229">Первая или вторая кнопка X дважды щелкните событие мыши, WM_XBUTTONDBLCLK.</span><span class="sxs-lookup"><span data-stu-id="d53c0-229">First or second X button double click mouse event, WM_XBUTTONDBLCLK.</span></span>
<span data-ttu-id="d53c0-230">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOWN</span><span class="sxs-lookup"><span data-stu-id="d53c0-230">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOWN</span></span>            | <span data-ttu-id="d53c0-231">Первая или вторая кнопка X вниз, WM_XBUTTONDOWN.</span><span class="sxs-lookup"><span data-stu-id="d53c0-231">First or second X button down mouse event, WM_XBUTTONDOWN.</span></span>
<span data-ttu-id="d53c0-232">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_UP</span><span class="sxs-lookup"><span data-stu-id="d53c0-232">COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_UP</span></span>            | <span data-ttu-id="d53c0-233">Первая или вторая кнопка X — событие мыши, WM_XBUTTONUP.</span><span class="sxs-lookup"><span data-stu-id="d53c0-233">First or second X button up mouse event, WM_XBUTTONUP.</span></span>

<span data-ttu-id="d53c0-234">Значения этого перечисления выравниваются с учетом соответствующих оконных сообщений WM_ \*.</span><span class="sxs-lookup"><span data-stu-id="d53c0-234">The values of this enum align with the matching WM_\* window messages.</span></span>

#### <span data-ttu-id="d53c0-235">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS</span><span class="sxs-lookup"><span data-stu-id="d53c0-235">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS</span></span> 

<span data-ttu-id="d53c0-236">Виртуальные ключи событий мыши, связанные с COREWEBVIEW2_MOUSE_EVENT_KINDом для SendMouseInput.</span><span class="sxs-lookup"><span data-stu-id="d53c0-236">Mouse event virtual keys associated with a COREWEBVIEW2_MOUSE_EVENT_KIND for SendMouseInput.</span></span>

> <span data-ttu-id="d53c0-237">[COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS](#corewebview2_mouse_event_virtual_keys) перечисления</span><span class="sxs-lookup"><span data-stu-id="d53c0-237">enum [COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS](#corewebview2_mouse_event_virtual_keys)</span></span>

 <span data-ttu-id="d53c0-238">Данные</span><span class="sxs-lookup"><span data-stu-id="d53c0-238">Values</span></span>                         | <span data-ttu-id="d53c0-239">Описания</span><span class="sxs-lookup"><span data-stu-id="d53c0-239">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="d53c0-240">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_NONE</span><span class="sxs-lookup"><span data-stu-id="d53c0-240">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_NONE</span></span>            | <span data-ttu-id="d53c0-241">Дополнительные клавиши не нажаты.</span><span class="sxs-lookup"><span data-stu-id="d53c0-241">No additional keys pressed.</span></span>
<span data-ttu-id="d53c0-242">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_LEFT_BUTTON</span><span class="sxs-lookup"><span data-stu-id="d53c0-242">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_LEFT_BUTTON</span></span>            | <span data-ttu-id="d53c0-243">Щелчок левой кнопкой мыши не работает, MK_LBUTTON.</span><span class="sxs-lookup"><span data-stu-id="d53c0-243">Left mouse button is down, MK_LBUTTON.</span></span>
<span data-ttu-id="d53c0-244">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_RIGHT_BUTTON</span><span class="sxs-lookup"><span data-stu-id="d53c0-244">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_RIGHT_BUTTON</span></span>            | <span data-ttu-id="d53c0-245">Щелчок правой кнопкой мыши не работает, MK_RBUTTON.</span><span class="sxs-lookup"><span data-stu-id="d53c0-245">Right mouse button is down, MK_RBUTTON.</span></span>
<span data-ttu-id="d53c0-246">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_SHIFT</span><span class="sxs-lookup"><span data-stu-id="d53c0-246">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_SHIFT</span></span>            | <span data-ttu-id="d53c0-247">Клавиша SHIFT нажата вниз, MK_SHIFT.</span><span class="sxs-lookup"><span data-stu-id="d53c0-247">SHIFT key is down, MK_SHIFT.</span></span>
<span data-ttu-id="d53c0-248">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_CONTROL</span><span class="sxs-lookup"><span data-stu-id="d53c0-248">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_CONTROL</span></span>            | <span data-ttu-id="d53c0-249">Клавиша CTRL нажата, MK_CONTROL.</span><span class="sxs-lookup"><span data-stu-id="d53c0-249">CTRL key is down, MK_CONTROL.</span></span>
<span data-ttu-id="d53c0-250">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_MIDDLE_BUTTON</span><span class="sxs-lookup"><span data-stu-id="d53c0-250">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_MIDDLE_BUTTON</span></span>            | <span data-ttu-id="d53c0-251">Средняя нажатие кнопки мыши не работает, MK_MBUTTON.</span><span class="sxs-lookup"><span data-stu-id="d53c0-251">Middle mouse button is down, MK_MBUTTON.</span></span>
<span data-ttu-id="d53c0-252">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_X_BUTTON1</span><span class="sxs-lookup"><span data-stu-id="d53c0-252">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_X_BUTTON1</span></span>            | <span data-ttu-id="d53c0-253">Первая кнопка X нажата MK_XBUTTON1.</span><span class="sxs-lookup"><span data-stu-id="d53c0-253">First X button is down, MK_XBUTTON1.</span></span>
<span data-ttu-id="d53c0-254">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_X_BUTTON2</span><span class="sxs-lookup"><span data-stu-id="d53c0-254">COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_X_BUTTON2</span></span>            | <span data-ttu-id="d53c0-255">Вторая кнопка X нажата MK_XBUTTON2.</span><span class="sxs-lookup"><span data-stu-id="d53c0-255">Second X button is down, MK_XBUTTON2.</span></span>

<span data-ttu-id="d53c0-256">Эти значения можно объединить в битовый флаг, если для события была нажата несколько виртуальных клавиш.</span><span class="sxs-lookup"><span data-stu-id="d53c0-256">These values can be combined into a bit flag if more than one virtual key is pressed for the event.</span></span> <span data-ttu-id="d53c0-257">Значения этого перечисления выравниваются с соответствующими клавишами мыши MK_ \*.</span><span class="sxs-lookup"><span data-stu-id="d53c0-257">The values of this enum align with the matching MK_\* mouse keys.</span></span>

#### <span data-ttu-id="d53c0-258">COREWEBVIEW2_POINTER_EVENT_KIND</span><span class="sxs-lookup"><span data-stu-id="d53c0-258">COREWEBVIEW2_POINTER_EVENT_KIND</span></span> 

<span data-ttu-id="d53c0-259">Тип события указателя, используемый функцией SendPointerInput для передачи типа события указателя, отправляемого в WebView.</span><span class="sxs-lookup"><span data-stu-id="d53c0-259">Pointer event type used by SendPointerInput to convey the type of pointer event being sent to WebView.</span></span>

> <span data-ttu-id="d53c0-260">[COREWEBVIEW2_POINTER_EVENT_KIND](#corewebview2_pointer_event_kind) перечисления</span><span class="sxs-lookup"><span data-stu-id="d53c0-260">enum [COREWEBVIEW2_POINTER_EVENT_KIND](#corewebview2_pointer_event_kind)</span></span>

 <span data-ttu-id="d53c0-261">Данные</span><span class="sxs-lookup"><span data-stu-id="d53c0-261">Values</span></span>                         | <span data-ttu-id="d53c0-262">Описания</span><span class="sxs-lookup"><span data-stu-id="d53c0-262">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="d53c0-263">COREWEBVIEW2_POINTER_EVENT_KIND_ACTIVATE</span><span class="sxs-lookup"><span data-stu-id="d53c0-263">COREWEBVIEW2_POINTER_EVENT_KIND_ACTIVATE</span></span>            | <span data-ttu-id="d53c0-264">Соответствует WM_POINTERACTIVATE.</span><span class="sxs-lookup"><span data-stu-id="d53c0-264">Corresponds to WM_POINTERACTIVATE.</span></span>
<span data-ttu-id="d53c0-265">COREWEBVIEW2_POINTER_EVENT_KIND_DOWN</span><span class="sxs-lookup"><span data-stu-id="d53c0-265">COREWEBVIEW2_POINTER_EVENT_KIND_DOWN</span></span>            | <span data-ttu-id="d53c0-266">Соответствует WM_POINTERDOWN.</span><span class="sxs-lookup"><span data-stu-id="d53c0-266">Corresponds to WM_POINTERDOWN.</span></span>
<span data-ttu-id="d53c0-267">COREWEBVIEW2_POINTER_EVENT_KIND_ENTER</span><span class="sxs-lookup"><span data-stu-id="d53c0-267">COREWEBVIEW2_POINTER_EVENT_KIND_ENTER</span></span>            | <span data-ttu-id="d53c0-268">Соответствует WM_POINTERENTER.</span><span class="sxs-lookup"><span data-stu-id="d53c0-268">Corresponds to WM_POINTERENTER.</span></span>
<span data-ttu-id="d53c0-269">COREWEBVIEW2_POINTER_EVENT_KIND_LEAVE</span><span class="sxs-lookup"><span data-stu-id="d53c0-269">COREWEBVIEW2_POINTER_EVENT_KIND_LEAVE</span></span>            | <span data-ttu-id="d53c0-270">Соответствует WM_POINTERLEAVE.</span><span class="sxs-lookup"><span data-stu-id="d53c0-270">Corresponds to WM_POINTERLEAVE.</span></span>
<span data-ttu-id="d53c0-271">COREWEBVIEW2_POINTER_EVENT_KIND_UP</span><span class="sxs-lookup"><span data-stu-id="d53c0-271">COREWEBVIEW2_POINTER_EVENT_KIND_UP</span></span>            | <span data-ttu-id="d53c0-272">Соответствует WM_POINTERUP.</span><span class="sxs-lookup"><span data-stu-id="d53c0-272">Corresponds to WM_POINTERUP.</span></span>
<span data-ttu-id="d53c0-273">COREWEBVIEW2_POINTER_EVENT_KIND_UPDATE</span><span class="sxs-lookup"><span data-stu-id="d53c0-273">COREWEBVIEW2_POINTER_EVENT_KIND_UPDATE</span></span>            | <span data-ttu-id="d53c0-274">Соответствует WM_POINTERUPDATE.</span><span class="sxs-lookup"><span data-stu-id="d53c0-274">Corresponds to WM_POINTERUPDATE.</span></span>

<span data-ttu-id="d53c0-275">Значения этого перечисления выравниваются с учетом соответствующих оконных сообщений WM_POINTER \*.</span><span class="sxs-lookup"><span data-stu-id="d53c0-275">The values of this enum align with the matching WM_POINTER\* window messages.</span></span>

