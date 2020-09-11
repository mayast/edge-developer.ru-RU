---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ExperimentalCompositionController
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2ExperimentalCompositionController
ms.openlocfilehash: bf73ce6a5e3a1171bf731e953c3016f9baea2ff1
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012472"
---
# интерфейс ICoreWebView2ExperimentalCompositionController 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

```
interface ICoreWebView2ExperimentalCompositionController
  : public IUnknown
```

Этот интерфейс является расширением интерфейса [ICoreWebView2Controller](icorewebview2controller.md) для поддержки визуального размещения.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[add_CursorChanged](#add_cursorchanged) | Добавьте обработчик событий для события CursorChanged.
[CreateCoreWebView2PointerInfoFromPointerId](#createcorewebview2pointerinfofrompointerid) | Вспомогательная функция для преобразования pointerId, полученного из системы, в [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).
[get_Cursor](#get_cursor) | Текущий курсор, WebView рассчитает, что он должен быть.
[get_RootVisualTarget](#get_rootvisualtarget) | RootVisualTarget — это визуальный элемент в визуальном дереве размещающего приложения.
[get_UIAProvider](#get_uiaprovider) | Возвращает поставщик модели автоматизации пользовательского интерфейса для WebView.
[put_RootVisualTarget](#put_rootvisualtarget) | Задайте свойство RootVisualTarget.
[remove_CursorChanged](#remove_cursorchanged) | Удалите обработчик событий, добавленный ранее add_CursorChanged.
[SendMouseInput](#sendmouseinput) | Если eventKind COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL или COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL, mouseData задает величину движения колесика.
[SendPointerInput](#sendpointerinput) | SendPointerInput принимает вводные данные и указатель пера для типов, определенных в COREWEBVIEW2_POINTER_EVENT_KIND.
[COREWEBVIEW2_MATRIX_4X4](#corewebview2_matrix_4x4) | Матрица, представляющая трехмерное преобразование.
[COREWEBVIEW2_MOUSE_EVENT_KIND](#corewebview2_mouse_event_kind) | Тип событий мыши, используемый функцией SendMouseInput для передачи типа события мыши, отправляемого в WebView.
[COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS](#corewebview2_mouse_event_virtual_keys) | Виртуальные ключи событий мыши, связанные с COREWEBVIEW2_MOUSE_EVENT_KINDом для SendMouseInput.
[COREWEBVIEW2_POINTER_EVENT_KIND](#corewebview2_pointer_event_kind) | Тип события указателя, используемый функцией SendPointerInput для передачи типа события указателя, отправляемого в WebView.

Объект, реализующий интерфейс ICoreWebView2ExperimentalCompositionController, также будет реализовывать [ICoreWebView2Controller](icorewebview2controller.md). Предполагается, что вызывающие объекты используют [ICoreWebView2Controller](icorewebview2controller.md) для изменения размера, видимости, фокусировки и т. д., а затем используют ICoreWebView2ExperimentalCompositionController для подключения к дереву композиции и предоставления входных данных для WebView.

## Участников

#### add_CursorChanged 

Добавьте обработчик событий для события CursorChanged.

> общедоступные значения HRESULT [add_CursorChanged](#add_cursorchanged)([ICoreWebView2ExperimentalCursorChangedEventHandler](icorewebview2experimentalcursorchangedeventhandler.md) * eventHandler, EventRegistrationToken * token)

Событие срабатывает, когда WebView считает, что курсор должен быть изменен. Например, если курсор мыши установлен по умолчанию, но затем перемещается поверх текста, он может попытаться перейти на курсор IBeam.

Ожидается, что разработчик отправляет COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE сообщения (в дополнение к COREWEBVIEW2_MOUSE_EVENT_KIND_MOVE сообщениям) через API SendMouseInput. Это необходимо для того, чтобы убедиться в том, что указатель мыши находится в WebView, отправляющем события CursorChanged.

```cpp
        // Register a handler for the CursorChanged event.
        CHECK_FAILURE(m_compositionController->add_CursorChanged(
            Callback<ICoreWebView2ExperimentalCursorChangedEventHandler>(
                [this](ICoreWebView2ExperimentalCompositionController* sender, IUnknown* args)
                    -> HRESULT {
                    HRESULT hr = S_OK;
                    HCURSOR cursor;
                        CHECK_FAILURE(sender->get_Cursor(&cursor));
                    if (SUCCEEDED(hr))
                    {
                        SetClassLongPtr(
                            m_appWindow->GetMainWindow(), GCLP_HCURSOR, (LONG_PTR)cursor);
                    }
                    return hr;
                })
                .Get(),
            &m_cursorChangedToken));
```

#### CreateCoreWebView2PointerInfoFromPointerId 

Вспомогательная функция для преобразования pointerId, полученного из системы, в [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md).

> общедоступные значения HRESULT [CreateCoreWebView2PointerInfoFromPointerId](#createcorewebview2pointerinfofrompointerid)(uint POINTERID, HWND parentWindow, struct COREWEBVIEW2_MATRIX_4X4 Transform, [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) * * pointerInfo)

parentWindow — HWND, который содержит WebView. Это может быть любой HWND в дереве HWND, который включает WebView. COREWEBVIEW2_MATRIX_4X4 является преобразованием из дескриптора HWND в WebView. Возвращенный [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) используется в SendPointerInfo. Тип указателя должен быть либо пером, либо сенсорным, либо функция завершится сбоем.

#### get_Cursor 

Текущий курсор, WebView рассчитает, что он должен быть.

> общедоступные значения HRESULT [get_Cursor](#get_cursor)(HCURSOR * Cursor)

Курсор должен быть установлен в WM_SETCURSOR с помощью:: SetCursor или установлен на соответствующий родительский или предок родительского объекта WebView By:: SetClassLongPtr. HCURSOR можно освободить таким образом, чтобы CopyCursor и DestroyCursor, чтобы сохранить собственную копию, если вы еще не настраиваете курсор.

#### get_RootVisualTarget 

RootVisualTarget — это визуальный элемент в визуальном дереве размещающего приложения.

> общедоступные значения HRESULT [get_RootVisualTarget](#get_rootvisualtarget)(IUnknown * * Target)

Этот визуальный элемент — это то, где WebView будет подключаться к визуальному дереву. Приложение использует этот визуальный элемент, чтобы расположить WebView в приложении. Чтобы изменить размер WebView, приложению по-прежнему нужно использовать свойство Boundss. Свойством RootVisualTarget может быть IDCompositionVisual или Windows:: UI:: композиция:: ContainerVisual. WebView подключится к визуальному дереву для предоставленного визуального элемента перед возвратом из метода присваивания свойств. Приложение должно быть зафиксировано на своем устройстве, в котором задано свойство RootVisualTarget. Свойство RootVisualTarget поддерживает значение nullptr, чтобы отключить WebView от визуального дерева приложения. 
```cpp
            // Set the host app visual that the WebView will connect its visual
            // tree to.
            BuildDCompTreeUsingVisual();
            if (m_isDcompTargetMode)
            {
                if (!m_dcompTarget)
                {
                    m_dcompTarget = Make<DCompTargetImpl>(this);
                }
                CHECK_FAILURE(
                    m_compositionController->put_RootVisualTarget(m_dcompTarget.get()));
            }
            else
            {
                CHECK_FAILURE(
                    m_compositionController->put_RootVisualTarget(m_dcompWebViewVisual.get()));
            }
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

#### get_UIAProvider 

Возвращает поставщик модели автоматизации пользовательского интерфейса для WebView.

> общедоступные значения HRESULT [get_UIAProvider](#get_uiaprovider)(IUnknown * * Provider)

#### put_RootVisualTarget 

Задайте свойство RootVisualTarget.

> общедоступные значения HRESULT [put_RootVisualTarget](#put_rootvisualtarget)(объект IUnknown *)

#### remove_CursorChanged 

Удалите обработчик событий, добавленный ранее add_CursorChanged.

> общедоступные значения HRESULT [remove_CursorChanged](#remove_cursorchanged)(маркер EventRegistrationToken)

#### SendMouseInput 

Если eventKind COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL или COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL, mouseData задает величину движения колесика.

> Public HRESULT [SendMouseInput](#sendmouseinput)([COREWEBVIEW2_MOUSE_EVENT_KIND](#corewebview2_mouse_event_kind) eventKind, [COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS](#corewebview2_mouse_event_virtual_keys) virtualKeys, UINT32 mouseData, точка Point)

Положительное значение указывает на то, что колесико было повернуто вперед от пользователя; отрицательное значение указывает на то, что колесико было повернуто на обратном направлении к пользователю. Один щелчок мыши определяется как WHEEL_DELTA (120). Если eventKind COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOUBLE_CLICK COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOWN или COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_UP, то mouseData указывает, какие кнопки X были нажаты или отпущены. Это значение должно быть 1, если первая кнопка X нажата/выпущена, и 2 при нажатии или отпускании второй кнопки X. Если eventKind COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE, то virtualKeys, mouseData и Point должны равняться нулю. Если eventKind — любое другое значение, mouseData должно равняться нулю. Ожидается, что точка должна находиться в пространстве координат клиента WebView. Для отслеживания событий мыши, которые запускаются в WebView и потенциально могут перемещаться за пределы WebView и ведущего приложения, рекомендуется использовать вызов SetCapture и ReleaseCapture. Чтобы выйти из всплывающих окон, также рекомендуется отправлять COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE сообщения. 
```cpp
bool ViewComponent::OnMouseMessage(UINT message, WPARAM wParam, LPARAM lParam)
{
    // Manually relay mouse messages to the WebView
#ifdef USE_WEBVIEW2_WIN10
    if (m_dcompDevice || m_wincompCompositor)
#else
    if (m_dcompDevice)
#endif
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

#### SendPointerInput 

SendPointerInput принимает вводные данные и указатель пера для типов, определенных в COREWEBVIEW2_POINTER_EVENT_KIND.

> общедоступные значения HRESULT [SendPointerInput](#sendpointerinput)([COREWEBVIEW2_POINTER_EVENT_KIND](#corewebview2_pointer_event_kind) eventKind, [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) * pointerInfo)

Все входные данные указателя из системы должны быть преобразованы в [ICoreWebView2ExperimentalPointerInfo](icorewebview2experimentalpointerinfo.md) первыми.

#### COREWEBVIEW2_MATRIX_4X4 

Матрица, представляющая трехмерное преобразование.

> typedef [COREWEBVIEW2_MATRIX_4X4](#corewebview2_matrix_4x4)

Это преобразование используется для вычисления правильных координат при вызове CreateCoreWebView2PointerInfoFromPointerId. Это эквивалентно D2D1_MATRIX_4X4_F

#### COREWEBVIEW2_MOUSE_EVENT_KIND 

Тип событий мыши, используемый функцией SendMouseInput для передачи типа события мыши, отправляемого в WebView.

> [COREWEBVIEW2_MOUSE_EVENT_KIND](#corewebview2_mouse_event_kind) перечисления

 Данные                         | Описания
--------------------------------|---------------------------------------------
COREWEBVIEW2_MOUSE_EVENT_KIND_HORIZONTAL_WHEEL            | Событие прокрутки колесика мыши по горизонтали WM_MOUSEHWHEEL.
COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_DOUBLE_CLICK            | Левая кнопка дважды щелкните событие мыши, WM_LBUTTONDBLCLK.
COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_DOWN            | Левая кнопка вниз события мыши, WM_LBUTTONDOWN.
COREWEBVIEW2_MOUSE_EVENT_KIND_LEFT_BUTTON_UP            | Левая кнопка — событие мыши, WM_LBUTTONUP.
COREWEBVIEW2_MOUSE_EVENT_KIND_LEAVE            | Событие выхода из мыши, WM_MOUSELEAVE.
COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_DOUBLE_CLICK            | Средняя кнопка дважды щелкните событие мыши, WM_MBUTTONDBLCLK.
COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_DOWN            | Средняя кнопка вниз: событие мыши, WM_MBUTTONDOWN.
COREWEBVIEW2_MOUSE_EVENT_KIND_MIDDLE_BUTTON_UP            | Средняя кнопка: событие мыши, WM_MBUTTONUP.
COREWEBVIEW2_MOUSE_EVENT_KIND_MOVE            | Событие перемещения мыши, WM_MOUSEMOVE.
COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_DOUBLE_CLICK            | Щелчок правой кнопкой мыши дважды щелкните событие мыши, WM_RBUTTONDBLCLK.
COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_DOWN            | Щелчок правой кнопкой мыши, WM_RBUTTONDOWN.
COREWEBVIEW2_MOUSE_EVENT_KIND_RIGHT_BUTTON_UP            | Щелкните правой кнопкой мыши событие мыши, WM_RBUTTONUP.
COREWEBVIEW2_MOUSE_EVENT_KIND_WHEEL            | Событие прокрутки колесика мыши, WM_MOUSEWHEEL.
COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOUBLE_CLICK            | Первая или вторая кнопка X дважды щелкните событие мыши, WM_XBUTTONDBLCLK.
COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_DOWN            | Первая или вторая кнопка X вниз, WM_XBUTTONDOWN.
COREWEBVIEW2_MOUSE_EVENT_KIND_X_BUTTON_UP            | Первая или вторая кнопка X — событие мыши, WM_XBUTTONUP.

Значения этого перечисления выравниваются с учетом соответствующих оконных сообщений WM_ *.

#### COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS 

Виртуальные ключи событий мыши, связанные с COREWEBVIEW2_MOUSE_EVENT_KINDом для SendMouseInput.

> [COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS](#corewebview2_mouse_event_virtual_keys) перечисления

 Данные                         | Описания
--------------------------------|---------------------------------------------
COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_NONE            | Дополнительные клавиши не нажаты.
COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_LEFT_BUTTON            | Щелчок левой кнопкой мыши не работает, MK_LBUTTON.
COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_RIGHT_BUTTON            | Щелчок правой кнопкой мыши не работает, MK_RBUTTON.
COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_SHIFT            | Клавиша SHIFT нажата вниз, MK_SHIFT.
COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_CONTROL            | Клавиша CTRL нажата, MK_CONTROL.
COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_MIDDLE_BUTTON            | Средняя нажатие кнопки мыши не работает, MK_MBUTTON.
COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_X_BUTTON1            | Первая кнопка X нажата MK_XBUTTON1.
COREWEBVIEW2_MOUSE_EVENT_VIRTUAL_KEYS_X_BUTTON2            | Вторая кнопка X нажата MK_XBUTTON2.

Эти значения можно объединить в битовый флаг, если для события была нажата несколько виртуальных клавиш. Значения этого перечисления выравниваются с соответствующими клавишами мыши MK_ *.

#### COREWEBVIEW2_POINTER_EVENT_KIND 

Тип события указателя, используемый функцией SendPointerInput для передачи типа события указателя, отправляемого в WebView.

> [COREWEBVIEW2_POINTER_EVENT_KIND](#corewebview2_pointer_event_kind) перечисления

 Данные                         | Описания
--------------------------------|---------------------------------------------
COREWEBVIEW2_POINTER_EVENT_KIND_ACTIVATE            | Соответствует WM_POINTERACTIVATE.
COREWEBVIEW2_POINTER_EVENT_KIND_DOWN            | Соответствует WM_POINTERDOWN.
COREWEBVIEW2_POINTER_EVENT_KIND_ENTER            | Соответствует WM_POINTERENTER.
COREWEBVIEW2_POINTER_EVENT_KIND_LEAVE            | Соответствует WM_POINTERLEAVE.
COREWEBVIEW2_POINTER_EVENT_KIND_UP            | Соответствует WM_POINTERUP.
COREWEBVIEW2_POINTER_EVENT_KIND_UPDATE            | Соответствует WM_POINTERUPDATE.

Значения этого перечисления выравниваются с учетом соответствующих оконных сообщений WM_POINTER *.

