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
# 0.9.430-Interface ICoreWebView2Host 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2Host
  : public IUnknown
```

Этот интерфейс является владельцем объекта CoreWebView2 и предоставляет поддержку изменения размеров, отображения и скрытия, фокусировки и других функциональных возможностей, связанных с окнами и композицией.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[get_IsVisible](#get_isvisible) | Свойство Visible определяет, нужно ли отображать или скрывать WebView.
[put_IsVisible](#put_isvisible) | Задайте свойство Visible.
[get_Bounds](#get_bounds) | Границы WebView.
[put_Bounds](#put_bounds) | Задайте свойство Bounds.
[get_ZoomFactor](#get_zoomfactor) | Коэффициент масштабирования для WebView.
[put_ZoomFactor](#put_zoomfactor) | Задайте свойство ZoomFactor.
[add_ZoomFactorChanged](#add_zoomfactorchanged) | Добавьте обработчик событий для события ZoomFactorChanged.
[remove_ZoomFactorChanged](#remove_zoomfactorchanged) | Удалите обработчик событий, добавленный ранее add_ZoomFactorChanged.
[SetBoundsAndZoomFactor](#setboundsandzoomfactor) | Одновременное обновление границ и свойств ZoomFactor.
[MoveFocus](#movefocus) | Перемещение фокуса в WebView.
[add_MoveFocusRequested](#add_movefocusrequested) | Добавьте обработчик событий для события MoveFocusRequested.
[remove_MoveFocusRequested](#remove_movefocusrequested) | Удалите обработчик событий, добавленный ранее add_MoveFocusRequested.
[add_GotFocus](#add_gotfocus) | Добавьте обработчик событий для события GotFocus.
[remove_GotFocus](#remove_gotfocus) | Удалите обработчик событий, добавленный ранее add_GotFocus.
[add_LostFocus](#add_lostfocus) | Добавьте обработчик для события LostFocus.
[remove_LostFocus](#remove_lostfocus) | Удалите обработчик событий, добавленный ранее add_LostFocus.
[add_AcceleratorKeyPressed](#add_acceleratorkeypressed) | Добавьте обработчик событий для события AcceleratorKeyPressed.
[remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed) | Удалите обработчик событий, добавленный ранее add_AcceleratorKeyPressed.
[get_ParentWindow](#get_parentwindow) | Родительское окно, предоставленное приложением, используемое этим WebView, для отрисовки содержимого.
[put_ParentWindow](#put_parentwindow) | Установка родительского окна для WebView.
[NotifyParentWindowPositionChanged](#notifyparentwindowpositionchanged) | Это уведомление отделено от put_Bounds, которое указывает на то, что WebView родительский элемент HWND (или какой-либо его предок) переместился.
[Close (закрыть)](#close) | Закрывает WebView и очищает основной экземпляр браузера.
[get_CoreWebView2](#get_corewebview2) | Возвращает CoreWebView2, связанный с этим CoreWebView2Host.
[CORE_WEBVIEW2_MOVE_FOCUS_REASON](#core_webview2_move_focus_reason) | Причина для перемещения фокуса.
[CORE_WEBVIEW2_KEY_EVENT_KIND](#core_webview2_key_event_kind) | Тип события клавиши, которое инициировало событие AcceleratorKeyPressed.
[CORE_WEBVIEW2_PHYSICAL_KEY_STATUS](#core_webview2_physical_key_status) | Структура, представляющая данные, Упакованные в LPARAM, предоставленные событию ключа Win32.

CoreWebView2Host владеет CoreWebView2 и, если все ссылки на CoreWebView2Host выходит из него, WebView будет закрыт.

## Участников

#### get_IsVisible 

Свойство Visible определяет, нужно ли отображать или скрывать WebView.

> общедоступные значения HRESULT [get_IsVisible](#get_isvisible)(bool * Visible)

Если для свойства Visible задано значение false, WebView будет прозрачным и не будет обрабатываться. Однако это не повлияет на окно, содержащее WebView (параметр HWND, переданный в CreateCoreWebView2Host). Если вы хотите, чтобы окно не исчезало, вызовите для него функцию ShowWindow прямо в дополнение к изменению свойства Visible. WebView — это дочернее окно не получает оконные сообщения, когда окно свертывания или восстановления находится в верхней части окна. Для повышения производительности разработчик должен установить для свойства WebView значение false, если окно приложения свернуто, и вернуть значение true при восстановлении окна приложения. Это можно сделать, обрабатывая команды SC_MINIMIZE и SC_RESTORE при получении WM_SYSCOMMAND сообщения.

```cpp
void ViewComponent::ToggleVisibility()
{
    BOOL visible;
    m_host->get_IsVisible(&visible);
    m_isVisible = !visible;
    m_host->put_IsVisible(m_isVisible);
}
```

#### put_IsVisible 

Задайте свойство Visible.

> общедоступные значения HRESULT [put_IsVisible](#put_isvisible)(bool-Visible)

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

#### get_Bounds 

Границы WebView.

> общедоступные значения HRESULT [get_Bounds](#get_bounds)(границы Rect *)

Границы задаются относительно родительского дескриптора HWND. Приложение может располагать WebView двумя способами:

1. Создание дочернего HWND, который является родительским дескриптором HWND WebView. Расположите это окно в том месте, где должен быть WebView. В этом случае используйте (0, 0) для левого верхнего угла WebView Bound's (сдвиг).

1. Используйте окно самого высокого приложения в качестве родительского HWND WebView. Задайте Bound's левый верхний угол WebView, чтобы WebView правильно расположиться в приложении. Значения границ находятся в пространстве координат основного приложения.

#### put_Bounds 

Задайте свойство Bounds.

> общедоступные значения HRESULT [put_Bounds](#put_bounds)(границы Rect)

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

#### get_ZoomFactor 

Коэффициент масштабирования для WebView.

> общедоступные значения HRESULT [get_ZoomFactor](#get_zoomfactor)(Double * ZoomFactor)

Обратите внимание, что изменение коэффициента масштабирования может привести к `window.innerWidth/innerHeight` изменению масштаба страницы. Коэффициент масштабирования, примененный ведущим приложением путем вызова put_ZoomFactor, становится новым масштабом по умолчанию для WebView. Этот коэффициент масштабирования применяется для всех переходов и — коэффициент масштабирования WebView возвращается, когда пользователь нажимает клавиши CTRL + 0. При изменении коэффициента масштабирования пользователем (в результате использования приложения, получающего ZoomFactorChanged) это масштабирование применяется только к текущей странице. Любой пользователь, который применяет масштабирование, используется только для текущей страницы и сбрасывается на панели навигации. Указывать zoomFactor меньше или равно 0 не разрешается. WebView также имеет внутренний поддерживаемый диапазон коэффициента масштабирования. Если указанный коэффициент масштаба выходит за пределы этого диапазона, он будет нормализован в пределах диапазона, а событие ZoomFactorChanged будет инициировано для фактического коэффициента масштабирования. При выполнении этой нормализации диапазона свойство ZoomFactor будет указывать коэффициент масштабирования, указанный в предыдущем изменении свойства ZoomFactor, пока событие ZoomFactorChanged не будет получено после WebView применяет нормализованный коэффициент масштабирования.

#### put_ZoomFactor 

Задайте свойство ZoomFactor.

> общедоступный [PUT_ZOOMFACTOR](#put_zoomfactor)HRESULT (двойной ZoomFactor)

#### add_ZoomFactorChanged 

Добавьте обработчик событий для события ZoomFactorChanged.

> общедоступные значения HRESULT [add_ZoomFactorChanged](#add_zoomfactorchanged)([ICoreWebView2ZoomFactorChangedEventHandler](ICoreWebView2ZoomFactorChangedEventHandler.md) * eventHandler, EventRegistrationToken * token)

Событие срабатывает, когда изменяется свойство ZoomFactor объекта WebView. Событие может срабатывать из-за того, что вызывающий объект изменил свойство ZoomFactor или пользователь вручную изменял масштаб. При изменении вызывающим абонентом с помощью свойства ZoomFactor внутренний коэффициент масштабирования немедленно обновляется, и событие ZoomFactorChanged не выводится. WebView связывает последний использованный коэффициент масштабирования для каждого сайта. Поэтому коэффициент масштабирования может изменяться при переходе на другую страницу. При изменении коэффициента масштабирования из-за этого событие ZoomFactorChanged срабатывает сразу после события ContentLoading.

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

#### remove_ZoomFactorChanged 

Удалите обработчик событий, добавленный ранее add_ZoomFactorChanged.

> общедоступные значения HRESULT [remove_ZoomFactorChanged](#remove_zoomfactorchanged)(маркер EventRegistrationToken)

#### SetBoundsAndZoomFactor 

Одновременное обновление границ и свойств ZoomFactor.

> общедоступные значения HRESULT [SetBoundsAndZoomFactor](#setboundsandzoomfactor)(границы Rect, Double zoomFactor)

Эта операция является атомарной из perspecive узла. После того как вы вернете эту функцию, свойства Bounds и ZoomFactor будут обновлены при успешном выполнении функции, или ни один из них не будет обновляться при сбое функции. Если границы и ZoomFactor обновляются одним масштабом (то есть границы и ZoomFactor оба двойных), то страница не будет видеть изменение в Window. innerWidth/innerHeight, а WebView будет отображать содержимое на новом размере и масштабе без промежуточных преобразований. Эта функция также может использоваться для обновления только одного из ZoomFactor или границ путем передачи нового значения для одного и текущего значения другого.

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

#### MoveFocus 

Перемещение фокуса в WebView.

> общедоступные значения HRESULT [MoveFocus](#movefocus)(причина[CORE_WEBVIEW2_MOVE_FOCUS_REASON](#core_webview2_move_focus_reason) )

WebView получит фокус, и фокус будет установлен на элемент корреспондента на странице, которая размещена в WebView. В целях программной причины фокус установлен на ранее сфокусированный элемент или элемент по умолчанию, если нет ранее фокусируемого элемента. В следующей причине фокус задается для первого элемента. По этой причине фокус установлен на последний элемент. WebView также может сосредоточиться на взаимодействии с пользователем, например, щелкнув на WebView или TAB. Для табуляции приложение может вызвать MoveFocus с помощью кнопки Далее или назад, чтобы выровнять элементы Tab и SHIFT + TAB, если это необходимо, если WebView является следующим элементом с вкладками. Кроме того, приложение может вызвать IsDialogMessage как часть цикла обработки сообщений, чтобы платформа автоматически обрабатывала табуляцию. Платформа будет повернута на все окна с помощью WS_TABSTOP. Когда WebView получает фокус из IsDialogMessage, он будет внутренне размещать фокус на первом или последнем элементе Tab и Shift + Tab соответственно.

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

#### add_MoveFocusRequested 

Добавьте обработчик событий для события MoveFocusRequested.

> общедоступные значения HRESULT [add_MoveFocusRequested](#add_movefocusrequested)([ICoreWebView2MoveFocusRequestedEventHandler](ICoreWebView2MoveFocusRequestedEventHandler.md) * eventHandler, EventRegistrationToken * token)

MoveFocusRequested активируется, когда пользователь пытается выполнить переход из WebView. При срабатывании этого события фокус WebView не изменился.

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

#### remove_MoveFocusRequested 

Удалите обработчик событий, добавленный ранее add_MoveFocusRequested.

> общедоступные значения HRESULT [remove_MoveFocusRequested](#remove_movefocusrequested)(маркер EventRegistrationToken)

#### add_GotFocus 

Добавьте обработчик событий для события GotFocus.

> общедоступные значения HRESULT [add_GotFocus](#add_gotfocus)([ICoreWebView2FocusChangedEventHandler](ICoreWebView2FocusChangedEventHandler.md) * eventHandler, EventRegistrationToken * token)

Получение фокуса срабатывает, когда WebView получил фокусировку.

#### remove_GotFocus 

Удалите обработчик событий, добавленный ранее add_GotFocus.

> общедоступные значения HRESULT [remove_GotFocus](#remove_gotfocus)(маркер EventRegistrationToken)

#### add_LostFocus 

Добавьте обработчик для события LostFocus.

> общедоступные значения HRESULT [add_LostFocus](#add_lostfocus)([ICoreWebView2FocusChangedEventHandler](ICoreWebView2FocusChangedEventHandler.md) * eventHandler, EventRegistrationToken * token)

LostFocus вызывается, когда WebView теряет фокус. В случае, если возникает событие MoveFocusRequested, фокус по-прежнему находится в WebView при срабатывании события MoveFocusRequested. Потерянный фокус срабатывает только в том случае, если код приложения или действие по умолчанию, заданное MoveFocusRequested события, задали фокус от WebView.

#### remove_LostFocus 

Удалите обработчик событий, добавленный ранее add_LostFocus.

> общедоступные значения HRESULT [remove_LostFocus](#remove_lostfocus)(маркер EventRegistrationToken)

#### add_AcceleratorKeyPressed 

Добавьте обработчик событий для события AcceleratorKeyPressed.

> общедоступные значения HRESULT [add_AcceleratorKeyPressed](#add_acceleratorkeypressed)([ICoreWebView2AcceleratorKeyPressedEventHandler](ICoreWebView2AcceleratorKeyPressedEventHandler.md) * eventHandler, EventRegistrationToken * token)

AcceleratorKeyPressed активируется при нажатии или отпускании клавиши сочетания клавиш в том случае, если WebView имеет фокус. Клавиша считается ускорителем по одной из следующих способов:

1. В данный момент удерживается клавиша CTRL или ALT;

1. Нажатая клавиша не сопоставляется с символом. Некоторые неопределенные клавиши никогда не рассматриваются как ускорители, например Shift. Клавиша ESC всегда считается ускорителем.

Событие с автоматическим нажатием клавиши, вызванное удерживанием нажатой клавиши, также срабатывает. Чтобы отфильтровать эти данные, Проверьте аргументы события "KeyEventLParam" или "PhysicalKeyStatus".

В оконном режиме этот обработчик событий вызывается синхронно. До тех пор пока вы не вызываете Handle () для аргументов события или не будет возвращен обработчик событий, процесс браузера будет заблокирован и исходящие межпроцессные вызовы COM не будут работать с RPC_E_CANTCALLOUT_ININPUTSYNCCALL. Однако все методы API CoreWebView2 будут работать.

В режиме безоконный обработчик событий вызывается асинхронно. Дальнейшие входные данные не доходят до браузера, пока обработчик событий не возвратит или не завершит вызов (), но сам процесс браузера не будет заблокирован, а исходящие вызовы COM будут работать нормально.

Рекомендуется, чтобы вы могли узнать, что вы хотите обрабатывать клавишу быстрого вызова (TRUE), как и раньше.

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

#### remove_AcceleratorKeyPressed 

Удалите обработчик событий, добавленный ранее add_AcceleratorKeyPressed.

> общедоступные значения HRESULT [remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed)(маркер EventRegistrationToken)

#### get_ParentWindow 

Родительское окно, предоставленное приложением, используемое этим WebView, для отрисовки содержимого.

> общедоступные значения HRESULT [get_ParentWindow](#get_parentwindow)(HWND * topLevelWindow)

Этот API первоначально возвращает окно, передаваемое в CreateCoreWebView2Host.

#### put_ParentWindow 

Установка родительского окна для WebView.

> общедоступные значения HRESULT [put_ParentWindow](#put_parentwindow)(HWND topLevelWindow)

Это приведет к тому, что WebView перестанет достать родительским окном до вновь заданной окна.

#### NotifyParentWindowPositionChanged 

Это уведомление отделено от put_Bounds, которое указывает на то, что WebView родительский элемент HWND (или какой-либо его предок) переместился.

> общедоступные значения HRESULT [NotifyParentWindowPositionChanged](#notifyparentwindowpositionchanged)()

Это необходимо для правильной работы специальных возможностей и некоторых диалоговых окон в WebView. 

```cpp
    if (message == WM_MOVE || message == WM_MOVING)
    {
        m_host->NotifyParentWindowPositionChanged();
        return true;
    }
```

#### Close (закрыть) 

Закрывает WebView и очищает основной экземпляр браузера.

> общедоступное значение HRESULT [Close](#close)()

Очистка браузера instace освобождает ресурсы, переключающие WebView. Экземпляр браузера будет закрыт, если он не используется другими веб – представлениями.

После вызова метода Close все вызовы методов завершатся сбоем, и обработчики событий прекратятся. В частности, WebView будет освобождать ссылки на обработчики событий при вызове Close.

Метод Close вызывается неявно, когда CoreWebView2Host теряет свою конечную ссылку и является независимым. Но рекомендуется явным образом вызывать метод Close, чтобы избежать случайного цикла ссылок между WebView и кодом приложения. В частности, если вы захватываете ссылку на WebView в обработчике событий, вы создадите цикл ссылки между WebView и обработчиком событий. Вызов Close приведет к прерыванию этого цикла, освобождая все обработчики событий. Но чтобы избежать такой ситуации, рекомендуется как явным образом вызвать метод Close для WebView и не захватить ссылку на WebView, чтобы убедиться, что WebView может быть корректно очищено.

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

#### get_CoreWebView2 

Возвращает CoreWebView2, связанный с этим CoreWebView2Host.

> общедоступные значения HRESULT [get_CoreWebView2](#get_corewebview2)([ICoreWebView2](ICoreWebView2.md) * * CoreWebView2)

#### CORE_WEBVIEW2_MOVE_FOCUS_REASON 

Причина для перемещения фокуса.

> [CORE_WEBVIEW2_MOVE_FOCUS_REASON](#core_webview2_move_focus_reason) перечисления

 Данные                         | Описания
--------------------------------|---------------------------------------------
CORE_WEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC            | Настройка кода фокуса на WebView.
CORE_WEBVIEW2_MOVE_FOCUS_REASON_NEXT            | Перемещение фокуса из-за прохождения вкладки вперед.
CORE_WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS            | Перемещение фокуса из-за перемещения по табуляции назад.

#### CORE_WEBVIEW2_KEY_EVENT_KIND 

Тип события клавиши, которое инициировало событие AcceleratorKeyPressed.

> [CORE_WEBVIEW2_KEY_EVENT_KIND](#core_webview2_key_event_kind) перечисления

 Данные                         | Описания
--------------------------------|---------------------------------------------
CORE_WEBVIEW2_KEY_EVENT_KIND_KEY_DOWN            | ВыWM_KEYDOWN сообщение в окне.
CORE_WEBVIEW2_KEY_EVENT_KIND_KEY_UP            | ВыWM_KEYUP сообщение в окне.
CORE_WEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_DOWN            | ВыWM_SYSKEYDOWN сообщение в окне.
CORE_WEBVIEW2_KEY_EVENT_KIND_SYSTEM_KEY_UP            | ВыWM_SYSKEYUP сообщение в окне.

#### CORE_WEBVIEW2_PHYSICAL_KEY_STATUS 

Структура, представляющая данные, Упакованные в LPARAM, предоставленные событию ключа Win32.

> typedef [CORE_WEBVIEW2_PHYSICAL_KEY_STATUS](#core_webview2_physical_key_status)

Подробные сведения об WM_KEYDOWN вы увидите в документации по адресу[https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)

