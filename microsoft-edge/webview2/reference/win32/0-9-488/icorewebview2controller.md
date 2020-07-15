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
# 0.9.515-Interface ICoreWebView2Controller 

> [!NOTE]
> Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515. Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.

```
interface ICoreWebView2Controller
  : public IUnknown
```

Этот интерфейс является владельцем объекта CoreWebView2 и предоставляет поддержку изменения размеров, отображения и скрытия, фокусировки и других функциональных возможностей, связанных с окнами и композицией.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[add_AcceleratorKeyPressed](#add_acceleratorkeypressed) | Добавьте обработчик событий для события AcceleratorKeyPressed.
[add_GotFocus](#add_gotfocus) | Добавьте обработчик событий для события GotFocus.
[add_LostFocus](#add_lostfocus) | Добавьте обработчик для события LostFocus.
[add_MoveFocusRequested](#add_movefocusrequested) | Добавьте обработчик событий для события MoveFocusRequested.
[add_ZoomFactorChanged](#add_zoomfactorchanged) | Добавьте обработчик событий для события ZoomFactorChanged.
[Close (закрыть)](#close) | Закрывает WebView и очищает основной экземпляр браузера.
[get_Bounds](#get_bounds) | Границы WebView.
[get_CoreWebView2](#get_corewebview2) | Возвращает CoreWebView2, связанный с этим CoreWebView2Controller.
[get_IsVisible](#get_isvisible) | Свойство Visible определяет, нужно ли отображать или скрывать WebView.
[get_ParentWindow](#get_parentwindow) | Родительское окно, предоставленное приложением, используемое этим WebView, для отрисовки содержимого.
[get_ZoomFactor](#get_zoomfactor) | Коэффициент масштабирования для WebView.
[MoveFocus](#movefocus) | Перемещение фокуса в WebView.
[NotifyParentWindowPositionChanged](#notifyparentwindowpositionchanged) | Это уведомление отделено от границ, которые сообщают WebView, что родительский HWND (или любой предк) переместился.
[put_Bounds](#put_bounds) | Задайте свойство Bounds.
[put_IsVisible](#put_isvisible) | Задайте свойство Visible.
[put_ParentWindow](#put_parentwindow) | Установка родительского окна для WebView.
[put_ZoomFactor](#put_zoomfactor) | Задайте свойство ZoomFactor.
[remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed) | Удалите обработчик событий, добавленный ранее add_AcceleratorKeyPressed.
[remove_GotFocus](#remove_gotfocus) | Удалите обработчик событий, добавленный ранее add_GotFocus.
[remove_LostFocus](#remove_lostfocus) | Удалите обработчик событий, добавленный ранее add_LostFocus.
[remove_MoveFocusRequested](#remove_movefocusrequested) | Удалите обработчик событий, добавленный ранее add_MoveFocusRequested.
[remove_ZoomFactorChanged](#remove_zoomfactorchanged) | Удалите обработчик событий, добавленный ранее add_ZoomFactorChanged.
[SetBoundsAndZoomFactor](#setboundsandzoomfactor) | Одновременное обновление границ и свойств ZoomFactor.

CoreWebView2Controller владеет CoreWebView2 и, если все ссылки на CoreWebView2Controller выходит из него, WebView будет закрыт.

## Участников

#### add_AcceleratorKeyPressed 

Добавьте обработчик событий для события AcceleratorKeyPressed.

> общедоступные значения HRESULT [add_AcceleratorKeyPressed](#add_acceleratorkeypressed)([ICoreWebView2AcceleratorKeyPressedEventHandler](icorewebview2acceleratorkeypressedeventhandler.md) * eventHandler, EventRegistrationToken * token)

AcceleratorKeyPressed активируется при нажатии или отпускании клавиши сочетания клавиш в том случае, если WebView имеет фокус. Клавиша считается ускорителем по одной из следующих способов:

1. В данный момент удерживается клавиша CTRL или ALT;

1. Нажатая клавиша не сопоставляется с символом. Некоторые неопределенные клавиши никогда не рассматриваются как ускорители, например Shift. Клавиша ESC всегда считается ускорителем.

Событие с автоматическим нажатием клавиши, вызванное удерживанием нажатой клавиши, также срабатывает. Чтобы отфильтровать эти данные, Проверьте аргументы события "KeyEventLParam" или "PhysicalKeyStatus".

В оконном режиме этот обработчик событий вызывается синхронно. До тех пор пока вы не вызываете Handle () для аргументов события или не будет возвращен обработчик событий, процесс браузера будет заблокирован и исходящие межпроцессные вызовы COM не будут работать с RPC_E_CANTCALLOUT_ININPUTSYNCCALL. Однако все методы API CoreWebView2 будут работать.

В режиме безоконный обработчик событий вызывается асинхронно. Дальнейшие входные данные не доходят до браузера, пока обработчик событий не возвратит или не завершит вызов (), но сам процесс браузера не будет заблокирован, а исходящие вызовы COM будут работать нормально.

Рекомендуется, чтобы вы могли узнать, что вы хотите обрабатывать клавишу быстрого вызова (TRUE), как и раньше.

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

#### add_GotFocus 

Добавьте обработчик событий для события GotFocus.

> общедоступные значения HRESULT [add_GotFocus](#add_gotfocus)([ICoreWebView2FocusChangedEventHandler](icorewebview2focuschangedeventhandler.md) * eventHandler, EventRegistrationToken * token)

Получение фокуса срабатывает, когда WebView получил фокусировку.

#### add_LostFocus 

Добавьте обработчик для события LostFocus.

> общедоступные значения HRESULT [add_LostFocus](#add_lostfocus)([ICoreWebView2FocusChangedEventHandler](icorewebview2focuschangedeventhandler.md) * eventHandler, EventRegistrationToken * token)

LostFocus вызывается, когда WebView теряет фокус. В случае, если возникает событие MoveFocusRequested, фокус по-прежнему находится в WebView при срабатывании события MoveFocusRequested. Потерянный фокус срабатывает только в том случае, если код приложения или действие по умолчанию, заданное MoveFocusRequested события, задали фокус от WebView.

#### add_MoveFocusRequested 

Добавьте обработчик событий для события MoveFocusRequested.

> общедоступные значения HRESULT [add_MoveFocusRequested](#add_movefocusrequested)([ICoreWebView2MoveFocusRequestedEventHandler](icorewebview2movefocusrequestedeventhandler.md) * eventHandler, EventRegistrationToken * token)

MoveFocusRequested активируется, когда пользователь пытается выполнить переход из WebView. При срабатывании этого события фокус WebView не изменился.

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

#### add_ZoomFactorChanged 

Добавьте обработчик событий для события ZoomFactorChanged.

> общедоступные значения HRESULT [add_ZoomFactorChanged](#add_zoomfactorchanged)([ICoreWebView2ZoomFactorChangedEventHandler](icorewebview2zoomfactorchangedeventhandler.md) * eventHandler, EventRegistrationToken * token)

Событие срабатывает, когда изменяется свойство ZoomFactor объекта WebView. Событие может срабатывать из-за того, что вызывающий объект изменил свойство ZoomFactor или пользователь вручную изменял масштаб. При изменении вызывающим абонентом с помощью свойства ZoomFactor внутренний коэффициент масштабирования немедленно обновляется, и событие ZoomFactorChanged не выводится. WebView связывает последний использованный коэффициент масштабирования для каждого сайта. Поэтому коэффициент масштабирования может изменяться при переходе на другую страницу. При изменении коэффициента масштабирования из-за этого событие ZoomFactorChanged срабатывает сразу после события ContentLoading.

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

#### Close (закрыть) 

Закрывает WebView и очищает основной экземпляр браузера.

> общедоступное значение HRESULT [Close](#close)()

Очистка экземпляра браузера приведет к освобождению ресурсов, WebView в сети. Экземпляр браузера будет закрыт, если он не используется другими веб – представлениями.

После вызова метода Close все вызовы методов завершатся сбоем, и обработчики событий прекратятся. В частности, WebView будет освобождать ссылки на обработчики событий при вызове Close.

Метод Close вызывается неявно, когда CoreWebView2Controller теряет свою конечную ссылку и является независимым. Но рекомендуется явным образом вызывать метод Close, чтобы избежать случайного цикла ссылок между WebView и кодом приложения. В частности, если вы захватываете ссылку на WebView в обработчике событий, вы создадите цикл ссылки между WebView и обработчиком событий. Вызов Close приведет к прерыванию этого цикла, освобождая все обработчики событий. Но чтобы избежать такой ситуации, рекомендуется как явным образом вызвать метод Close для WebView и не захватить ссылку на WebView, чтобы убедиться, что WebView может быть корректно очищено.

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

#### get_Bounds 

Границы WebView.

> общедоступные значения HRESULT [get_Bounds](#get_bounds)(границы Rect *)

Границы задаются относительно родительского дескриптора HWND. Приложение может располагать WebView двумя способами:

1. Создание дочернего HWND, который является родительским дескриптором HWND WebView. Расположите это окно в том месте, где должен быть WebView. В этом случае используйте (0, 0) для левого верхнего угла WebView Bound's (сдвиг).

1. Используйте окно самого высокого приложения в качестве родительского HWND WebView. Задайте Bound's левый верхний угол WebView, чтобы WebView правильно расположиться в приложении. Значения границ находятся в пространстве координат основного приложения.

#### get_CoreWebView2 

Возвращает CoreWebView2, связанный с этим CoreWebView2Controller.

> общедоступные значения HRESULT [get_CoreWebView2](#get_corewebview2)([ICoreWebView2](icorewebview2.md) * * CoreWebView2)

#### get_IsVisible 

Свойство Visible определяет, нужно ли отображать или скрывать WebView.

> общедоступные значения HRESULT [get_IsVisible](#get_isvisible)(bool * Visible)

Если для свойства Visible задано значение false, WebView будет прозрачным и не будет обрабатываться. Однако это не повлияет на окно, содержащее WebView (параметр HWND, переданный в CreateCoreWebView2Controller). Если вы хотите, чтобы окно не исчезало, вызовите для него функцию ShowWindow прямо в дополнение к изменению свойства Visible. WebView — это дочернее окно не получает оконные сообщения, когда окно свертывания или восстановления находится в верхней части окна. Для повышения производительности разработчик должен установить для свойства WebView значение false, если окно приложения свернуто, и вернуть значение true при восстановлении окна приложения. Это можно сделать, обрабатывая команды SC_MINIMIZE и SC_RESTORE при получении WM_SYSCOMMAND сообщения.

```cpp
void ViewComponent::ToggleVisibility()
{
    BOOL visible;
    m_controller->get_IsVisible(&visible);
    m_isVisible = !visible;
    m_controller->put_IsVisible(m_isVisible);
}
```

#### get_ParentWindow 

Родительское окно, предоставленное приложением, используемое этим WebView, для отрисовки содержимого.

> общедоступные значения HRESULT [get_ParentWindow](#get_parentwindow)(HWND * topLevelWindow)

Этот API первоначально возвращает окно, передаваемое в CreateCoreWebView2Controller.

#### get_ZoomFactor 

Коэффициент масштабирования для WebView.

> общедоступные значения HRESULT [get_ZoomFactor](#get_zoomfactor)(Double * ZoomFactor)

Обратите внимание, что изменение коэффициента масштабирования может привести к `window.innerWidth/innerHeight` изменению масштаба страницы. Коэффициент масштабирования, примененный ведущим приложением путем вызова ZoomFactor, становится новым масштабом по умолчанию для WebView. Этот коэффициент масштабирования применяется для всех переходов и — коэффициент масштабирования WebView возвращается, когда пользователь нажимает клавиши CTRL + 0. При изменении коэффициента масштабирования пользователем (в результате использования приложения, получающего ZoomFactorChanged) это масштабирование применяется только к текущей странице. Любой пользователь, который применяет масштабирование, используется только для текущей страницы и сбрасывается на панели навигации. Указывать zoomFactor меньше или равно 0 не разрешается. WebView также имеет внутренний поддерживаемый диапазон коэффициента масштабирования. Если указанный коэффициент масштаба выходит за пределы этого диапазона, он будет нормализован в пределах диапазона, а событие ZoomFactorChanged будет инициировано для фактического коэффициента масштабирования. При выполнении этой нормализации диапазона свойство ZoomFactor будет указывать коэффициент масштабирования, указанный в предыдущем изменении свойства ZoomFactor, пока событие ZoomFactorChanged не будет получено после WebView применяет нормализованный коэффициент масштабирования.

#### MoveFocus 

Перемещение фокуса в WebView.

> общедоступные значения HRESULT [MoveFocus](#movefocus)(причина COREWEBVIEW2_MOVE_FOCUS_REASON)

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

#### NotifyParentWindowPositionChanged 

Это уведомление отделено от границ, которые сообщают WebView, что родительский HWND (или любой предк) переместился.

> общедоступные значения HRESULT [NotifyParentWindowPositionChanged](#notifyparentwindowpositionchanged)()

Это необходимо для правильной работы специальных возможностей и некоторых диалоговых окон в WebView. 
```cpp
    if (message == WM_MOVE || message == WM_MOVING)
    {
        m_controller->NotifyParentWindowPositionChanged();
        return true;
    }
```

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

#### put_IsVisible 

Задайте свойство Visible.

> общедоступные значения HRESULT [put_IsVisible](#put_isvisible)(bool-Visible)

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

#### put_ParentWindow 

Установка родительского окна для WebView.

> общедоступные значения HRESULT [put_ParentWindow](#put_parentwindow)(HWND topLevelWindow)

Это приведет к тому, что WebView перестанет достать родительским окном до вновь заданной окна.

#### put_ZoomFactor 

Задайте свойство ZoomFactor.

> общедоступный [PUT_ZOOMFACTOR](#put_zoomfactor)HRESULT (двойной ZoomFactor)

#### remove_AcceleratorKeyPressed 

Удалите обработчик событий, добавленный ранее add_AcceleratorKeyPressed.

> общедоступные значения HRESULT [remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed)(маркер EventRegistrationToken)

#### remove_GotFocus 

Удалите обработчик событий, добавленный ранее add_GotFocus.

> общедоступные значения HRESULT [remove_GotFocus](#remove_gotfocus)(маркер EventRegistrationToken)

#### remove_LostFocus 

Удалите обработчик событий, добавленный ранее add_LostFocus.

> общедоступные значения HRESULT [remove_LostFocus](#remove_lostfocus)(маркер EventRegistrationToken)

#### remove_MoveFocusRequested 

Удалите обработчик событий, добавленный ранее add_MoveFocusRequested.

> общедоступные значения HRESULT [remove_MoveFocusRequested](#remove_movefocusrequested)(маркер EventRegistrationToken)

#### remove_ZoomFactorChanged 

Удалите обработчик событий, добавленный ранее add_ZoomFactorChanged.

> общедоступные значения HRESULT [remove_ZoomFactorChanged](#remove_zoomfactorchanged)(маркер EventRegistrationToken)

#### SetBoundsAndZoomFactor 

Одновременное обновление границ и свойств ZoomFactor.

> общедоступные значения HRESULT [SetBoundsAndZoomFactor](#setboundsandzoomfactor)(границы Rect, Double zoomFactor)

Эта операция является атомарной с точки зрения хоста. После того как вы вернете эту функцию, свойства Bounds и ZoomFactor будут обновлены при успешном выполнении функции, или ни один из них не будет обновляться при сбое функции. Если границы и ZoomFactor обновляются одним масштабом (то есть границы и ZoomFactor оба двойных), то страница не будет видеть изменение в Window. innerWidth/innerHeight, а WebView будет отображать содержимое на новом размере и масштабе без промежуточных преобразований. Эта функция также может использоваться для обновления только одного из ZoomFactor или границ путем передачи нового значения для одного и текущего значения другого.

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

