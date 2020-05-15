---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 5c84cfb703c8901560307b7bba8bc7887cb19377
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654624"
---
# интерфейс IWebView2WebView 

> [!NOTE]
> Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355. Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.

```
interface IWebView2WebView
  : public IUnknown
```

WebView2 позволяет размещать веб-содержимое с помощью новейшей технологии веб-браузера.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[get_Settings](#get_settings) | Объект [IWebView2Settings](IWebView2Settings.md) , содержащий различные изменяемые параметры для запущенного WebView.
[get_Source](#get_source) | Универсальный код ресурса (URI) текущего документа верхнего уровня.
[Которому](#navigate) | Применяет навигацию по документу верхнего уровня к указанному универсальному коду ресурса (URI).
[MoveFocus](#movefocus) | Перемещение фокуса в WebView.
[NavigateToString](#navigatetostring) | Запускает навигацию для htmlContent в качестве исходного HTML-кода нового документа.
[add_NavigationStarting](#add_navigationstarting) | Добавьте обработчик событий для события NavigationStarting.
[remove_NavigationStarting](#remove_navigationstarting) | Удалите обработчик событий, добавленный ранее add_NavigationStarting.
[add_DocumentStateChanged](#add_documentstatechanged) | Добавьте обработчик событий для события DocumentStateChanged.
[remove_DocumentStateChanged](#remove_documentstatechanged) | Удалите обработчик событий, добавленный ранее add_DocumentStateChanged.
[add_NavigationCompleted](#add_navigationcompleted) | Добавьте обработчик событий для события NavigationCompleted.
[remove_NavigationCompleted](#remove_navigationcompleted) | Удалите обработчик событий, добавленный ранее add_NavigationCompleted.
[add_FrameNavigationStarting](#add_framenavigationstarting) | Добавьте обработчик событий для события FrameNavigationStarting.
[remove_FrameNavigationStarting](#remove_framenavigationstarting) | Удалите обработчик событий, добавленный ранее add_FrameNavigationStarting.
[add_MoveFocusRequested](#add_movefocusrequested) | Добавьте обработчик событий для события MoveFocusRequested.
[remove_MoveFocusRequested](#remove_movefocusrequested) | Удалите обработчик событий, добавленный ранее add_MoveFocusRequested.
[add_GotFocus](#add_gotfocus) | Добавьте обработчик событий для события GotFocus.
[remove_GotFocus](#remove_gotfocus) | Удалите обработчик событий, добавленный ранее add_GotFocus.
[add_LostFocus](#add_lostfocus) | Добавьте обработчик для события LostFocus.
[remove_LostFocus](#remove_lostfocus) | Удалите обработчик событий, добавленный ранее add_LostFocus.
[add_WebResourceRequested_deprecated](#add_webresourcerequested_deprecated) | Этот API будет устаревшим, воспользуйтесь новым add_WebResourceRequested API.
[remove_WebResourceRequested](#remove_webresourcerequested) | Удалите обработчик событий, добавленный ранее add_WebResourceRequested.
[add_ScriptDialogOpening](#add_scriptdialogopening) | Добавьте обработчик событий для события ScriptDialogOpening.
[remove_ScriptDialogOpening](#remove_scriptdialogopening) | Удалите обработчик событий, добавленный ранее add_ScriptDialogOpening.
[add_ZoomFactorChanged](#add_zoomfactorchanged) | Добавьте обработчик событий для события ZoomFactorChanged.
[remove_ZoomFactorChanged](#remove_zoomfactorchanged) | Удалите обработчик событий, добавленный ранее add_ZoomFactorChanged.
[add_PermissionRequested](#add_permissionrequested) | Добавьте обработчик событий для события PermissionRequested.
[remove_PermissionRequested](#remove_permissionrequested) | Удалите обработчик событий, добавленный ранее add_PermissionRequested.
[add_ProcessFailed](#add_processfailed) | Добавьте обработчик событий для события ProcessFailed.
[remove_ProcessFailed](#remove_processfailed) | Удалите обработчик событий, добавленный ранее add_ProcessFailed.
[AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated) | Добавьте предоставленный JavaScript в список сценариев, которые должны выполняться после создания глобального объекта, но до начала синтаксического анализа HTML-документа и перед выполнением любого другого сценария, включенного в документ HTML.
[RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated) | Удалите соответствующий сценарий JavaScript, добавленный через AddScriptToExecuteOnDocumentCreated.
[ExecuteScript](#executescript) | Выполнение кода JavaScript из параметра JavaScript в текущем документе верхнего уровня, отображаемом в WebView.
[CapturePreview](#capturepreview) | Запишите изображение того, что WebView на экране.
[Перезагрузить](#reload) | Перезагрузите текущую страницу.
[get_Bounds](#get_bounds) | Границы WebView.
[put_Bounds](#put_bounds) | Задайте свойство Bounds.
[get_ZoomFactor](#get_zoomfactor) | Коэффициент увеличения для текущей страницы в WebView.
[put_ZoomFactor](#put_zoomfactor) | Задайте свойство ZoomFactor.
[get_IsVisible](#get_isvisible) | Свойство Visible определяет, нужно ли отображать или скрывать WebView.
[put_IsVisible](#put_isvisible) | Задайте свойство Visible.
[PostWebMessageAsJson](#postwebmessageasjson) | Опубликуйте указанное сообщение в документе верхнего уровня в этом [IWebView2WebView]().
[PostWebMessageAsString](#postwebmessageasstring) | Это вспомогательный объект для отправки сообщения, которое является простой строкой, а не строкой JSON-представления объекта JavaScript.
[add_WebMessageReceived](#add_webmessagereceived) | Это событие срабатывает, если задан параметр IsWebMessageEnabled и документ верхнего уровня для вызовов WebView `window.chrome.webview.postMessage` .
[remove_WebMessageReceived](#remove_webmessagereceived) | Удалите обработчик событий, добавленный ранее add_WebMessageReceived.
[Close (закрыть)](#close) | Закрывает WebView и очищает основной экземпляр браузера.
[CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod) | Вызовите асинхронный метод DevToolsProtocol.
[add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived) | Подпишитесь на событие DevToolsProtocol.
[remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived) | Удалите обработчик событий, добавленный ранее add_DevToolsProtocolEventReceived.
[get_BrowserProcessId](#get_browserprocessid) | Идентификатор процесса браузера, на котором размещается WebView.
[get_CanGoBack](#get_cangoback) | Можно переходить по WebView на предыдущую страницу в истории навигации.
[get_CanGoForward](#get_cangoforward) | Можно переходить по WebView на следующую страницу в истории навигации.
[GoBack](#goback) | Переход по WebView на предыдущую страницу в истории навигации.
[GoForward](#goforward) | Переход по WebView к следующей странице в истории навигации.
[WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#webview2_capture_preview_image_format) | Формат изображения, используемый в методе [IWebView2WebView:: CapturePreview](#capturepreview) .
[WEBVIEW2_SCRIPT_DIALOG_KIND](#webview2_script_dialog_kind) | Диалоговое окно вида JavaScript, используемое в интерфейсе [IWebView2ScriptDialogOpeningEventHandler](IWebView2ScriptDialogOpeningEventHandler.md) .
[WEBVIEW2_PROCESS_FAILED_KIND](#webview2_process_failed_kind) | Состояние сбоя процесса, используемого в интерфейсе [IWebView2ProcessFailedEventHandler](IWebView2ProcessFailedEventHandler.md) .
[WEBVIEW2_PERMISSION_TYPE](#webview2_permission_type) | Тип запроса разрешения.
[WEBVIEW2_PERMISSION_STATE](#webview2_permission_state) | Ответ на запрос разрешения.
[WEBVIEW2_MOVE_FOCUS_REASON](#webview2_move_focus_reason) | Причина для перемещения фокуса.
[WEBVIEW2_WEB_ERROR_STATUS](#webview2_web_error_status) | Значения состояния ошибки для переходов по веб-страницам.
[WEBVIEW2_WEB_RESOURCE_CONTEXT](#webview2_web_resource_context) | Перечисление для контекстов запросов веб-ресурсов.

## События навигации

Обычной последовательностью событий навигации является NavigationStarting, DocumentStateChanged и NavigationCompleted.

![Dot-Inline-dotgraph-1. png](media/dot-inline-dotgraph-1.png)

Обратите внимание, что это для событий навигации с одинаковым событием NavigationId arg. События навигации с различными аргументы события NavigationId могут перекрывать друг друга. Например, если вы запускаете навигацию для события NavigationStarting, а затем запускаете другую навигацию, вы увидите NavigationStarting для первой навигации, за которой следует NavigationStarting второй переход, а затем — NavigationCompleted для первого перехода, а затем все оставшиеся события навигации для второй навигации. В случае возникновения ошибок может возникнуть или не быть событием DocumentStateChanged в зависимости от того, проявляется ли переход на страницу ошибки. В случае перенаправления HTTP в строке есть несколько событий NavigationStarting, для которых после первого будет задано значение параметра redirect.

Для подразделов внутри WebView создается только событие NavigationStarting, которое дает узлу возможность блокировать навигацию по подфреймам.

## Модель процесса

WebView2 использует ту же модель процессов, что и веб-браузер EDGE. В сеансе пользователя имеется один процесс браузера Edge для определенного каталога данных пользователя, который будет обрабатывать любой процесс вызова WebView2, указывающий на этот каталог данных пользователя. Это означает, что один процесс браузера Edge может обслуживать несколько процессов вызова и один процесс вызова может использовать несколько процессов браузера Edge.

![Dot-Inline-dotgraph-2. png](media/dot-inline-dotgraph-2.png)

В процессе работы с браузером может быть некоторое количество процессов обработки. Они создаются по мере необходимости для того, чтобы обслуживать потенциально несколько кадров в разных представлениях. Количество процессов обработки может различаться в зависимости от функции браузера "изоляция сайта" и количества отдельных отключенных относящихся к отсоединенным источникам, отображаемым в соответствующих веб-представлениях.

![Dot-Inline-dotgraph-3. png](media/dot-inline-dotgraph-3.png)

Вы можете реагировать на сбои и зависания в этих процессах браузера и отрисовки с помощью события ProcessFailure.

С помощью метода Close можно безопасно завершить работу связанных браузеров и процессов обработки.

## Потоковая модель

WebView2 должен создаваться в потоке пользовательского интерфейса. В частности, поток с конвейером сообщений. Все обратные вызовы будут происходить в этом потоке, и звонки в WebView должны выполняться в этом потоке. Небезопасно использовать WebView из другого потока.

Обратные вызовы, включая обработчики событий и обработчики завершения выполняются последовательно. Это значит, что если у вас есть обработчик событий и начало цикла обработки сообщений, другие обработчики событий или обратные вызовы завершения будут запущены повторно.

## Безопасность

Всегда проверяйте свойство Source объекта WebView, прежде чем использовать ExecuteScript, PostWebMessageAsJson, PostWebMessageAsString или любой другой метод для отправки данных в WebView. WebView может перейти на другую страницу с помощью конечного пользователя, взаимодействующего со страницей или сценарием на странице, вызывающем навигацию. Также будьте внимательны с AddScriptToExecuteOnDocumentCreated. Все будущие переходы запустят этот сценарий и предоставляют доступ к сведениям, предназначенным только для определенного происхождения, может быть предоставлен доступ к любому HTML-документу.

При исследовании результата вызова метода ExecuteScript, события WebMessageReceived, всегда следует проверять источник отправителя или любой другой механизм получения данных из HTML-документа в WebView проверять URI HTML-документа, что вы ожидаете.

Когда вы создаете сообщение для отправки в WebView, предпочитать использование PostWebMessageAsJson и создавайте строковый параметр JSON с помощью библиотеки JSON. Это позволит избежать возможного ДТП данных в строку или сценарий JSON и убедиться, что злоумышленник, управляющий неуправляемым вводом, может изменить оставшуюся часть сообщения JSON или выполнить произвольный сценарий.

## Типы строк

Выход из параметров строки: LPWSTR строки, заканчивающиеся нулем. Вызываемый объект выделяет строку с помощью функции CoTaskMemAlloc. Владение передается вызывающему абоненту и вызывающему абоненту, чтобы освободить память с помощью CoTaskMemFree.

Строка в параметрах — LPCWSTR строки, заканчивающиеся нулем. Вызывающий объект гарантирует допустимость строки в течение синхронного вызова функции. Если вызываемый объект должен сохранить это значение в некоторой точке после завершения вызова функции, вызываемый объект должен выделять собственную копию строкового значения.

## Синтаксический анализ URI и JSON

Различные методы предоставляют или допускают URI и JSON в виде строк. Для синтаксического анализа и создания этих строк используйте собственную библиотеку предпочтительных.

Если приложение WinRT доступно для вашего приложения, вы можете использовать для `RuntimeClass_Windows_Data_Json_JsonObject` `IJsonObjectStatics` анализа или создания строк JSON либо `RuntimeClass_Windows_Foundation_Uri` `IUriRuntimeClassFactory` для синтаксического анализа и создания URI. Обе эти операции работают в приложениях Win32.

Если вы используете IUri и CreateUri для синтаксического анализа URI, вы можете использовать следующие флаги создания URI, чтобы поведение CreateUri более точно соответствовало синтаксическому анализу URI в WebView: `Uri_CREATE_ALLOW_IMPLICIT_FILE_SCHEME | Uri_CREATE_NO_DECODE_EXTRA_INFO`

## Отладка

Откройте DevTools с помощью стандартных сочетаний клавиш: `F12` или `Ctrl+Shift+I` . Вы можете использовать `--auto-open-devtools-for-tabs` параметр аргумента Command, чтобы окно DevTools было открыто немедленно при первом создании WebView. Сведения о том, как предоставить дополнительные аргументы командной строки для процесса браузера, можно найти в документации CreateWebView. Изучите раздел реестра LoaderOverride для использования разных сборок WebView2 без изменения вашего приложения в документации CreateWebView.

## Управление версиями

После того как вы использовали определенную версию SDK для создания приложения, ваше приложение может завершить работу с более ранней или более поздней версией установленных двоичных файлов браузера. До версии 1.0.0.0 WebView2 на этапе обновления могут возрушиться изменения, которые не позволят пакету SDK работать с различными версиями установленных двоичных файлов браузера. После того как версия 1.0.0.0 может работать с различными версиями пакета SDK, следуйте приведенным ниже рекомендациям.

Для учета критических изменений в API убедитесь, что при вызове функции экспорта DLL CreateWebView2Environment и при вызове QueryInterface для любого объекта WebView2 возникла ошибка. Возвращаемое значение E_NOINTERFACE может указывать на то, что пакет SDK несовместим с двоичными файлами браузера Edge.

Проверка сбоя из QueryInterface также учитывает ситуации, в которых пакет SDK более новый, чем версия браузера EDGE, и ваше приложение пытается использовать интерфейс, на котором нет браузера Edge.

Если интерфейс недоступен, вы можете отключать связанный компонент, если это возможно, или иным образом информировать конечного пользователя о необходимости обновления браузера.

## Участников

#### get_Settings 

Объект [IWebView2Settings](IWebView2Settings.md) , содержащий различные изменяемые параметры для запущенного WebView.

> общедоступные значения HRESULT [get_Settings](#get_settings)([IWebView2Settings](IWebView2Settings.md) * * параметры)

#### get_Source 

Универсальный код ресурса (URI) текущего документа верхнего уровня.

> общедоступные значения HRESULT [get_Source](#get_source)(LPWSTR * URI)

Это значение может изменяться в рамках обработки события DocumentStateChanged в некоторых случаях, например при переходе к другому сайту или для навигации по фрагменту. Оно останется прежним для других типов переходов, таких как перегрузка страниц или History. pushState с тем же URL-адресом, что и у текущей страницы.

```cpp
    // Register a handler for the DocumentStateChanged event.
    // This handler will read the webview's source URI and update
    // the app's address bar.
    CHECK_FAILURE(m_webView->add_DocumentStateChanged(
        Callback<IWebView2DocumentStateChangedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2DocumentStateChangedEventArgs* args)
                -> HRESULT {
                wil::unique_cotaskmem_string uri;
                sender->get_Source(&uri);
                if (wcscmp(uri.get(), L"about:blank") == 0)
                {
                    uri = wil::make_cotaskmem_string(L"");
                }
                SetWindowText(m_toolbar->addressBarWindow, uri.get());

                return S_OK;
            })
            .Get(),
        &m_documentStateChangedToken));
```

#### Которому 

Применяет навигацию по документу верхнего уровня к указанному универсальному коду ресурса (URI).

> общедоступное значение HRESULT [навигации](#navigate)(URI LPCWSTR)

Дополнительные сведения приведены в разделе события навигации. Обратите внимание, что при этом начинается переход и соответствующее событие NavigationStarting будет срабатывать после завершения этого вызова навигации.

```cpp
void ControlComponent::NavigateToAddressBar()
{
    WCHAR uri[2048] = L"";
    GetWindowText(m_toolbar->addressBarWindow, uri, ARRAYSIZE(uri));
    CHECK_FAILURE(m_webView->Navigate(uri));
}
```

#### MoveFocus 

Перемещение фокуса в WebView.

> общедоступные значения HRESULT [MoveFocus](#movefocus)(причина[WEBVIEW2_MOVE_FOCUS_REASON](#webview2_move_focus_reason) )

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
    m_webView->MoveFocus(WEBVIEW2_MOVE_FOCUS_REASON_NEXT);
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
    CHECK_FAILURE(m_webView->MoveFocus(WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS));
}
```

#### NavigateToString 

Запускает навигацию для htmlContent в качестве исходного HTML-кода нового документа.

> общедоступные значения HRESULT [NavigateToString](#navigatetostring)(LPCWSTR htmlContent)

Параметр htmlContent не может быть больше 2 МБ символов. В качестве источника новой страницы будет указано пустое значение.

```cpp
                static const PCWSTR htmlContent =
                    L"<h1>Domain Blocked</h1>"
                    L"<p>You've attempted to navigate to a domain in the blocked "
                    L"sites list. Press back to return to the previous page.</p>";
                CHECK_FAILURE(sender->NavigateToString(htmlContent));
```

#### add_NavigationStarting 

Добавьте обработчик событий для события NavigationStarting.

> общедоступные значения HRESULT [add_NavigationStarting](#add_navigationstarting)([IWebView2NavigationStartingEventHandler](IWebView2NavigationStartingEventHandler.md) * eventHandler, EventRegistrationToken * token)

NavigationStarting активируется, когда основной кадр WebView запрашивает разрешение на переход на другой URI. Это будет срабатывать и для перенаправления.

```cpp
    // Register a handler for the NavigationStarting event.
    // This handler will check the domain being navigated to, and if the domain
    // matches a list of blocked sites, it will cancel the navigation and
    // possibly display a warning page.  It will also disable JavaScript on
    // selected websites.
    CHECK_FAILURE(m_webView->add_NavigationStarting(
        Callback<IWebView2NavigationStartingEventHandler>(
            [this](IWebView2WebView* sender,
                   IWebView2NavigationStartingEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Uri(&uri));

        if (ShouldBlockUri(uri.get()))
        {
            CHECK_FAILURE(args->put_Cancel(true));

            // If the user clicked a link to navigate, show a warning page.
            BOOL userInitiated;
            CHECK_FAILURE(args->get_IsUserInitiated(&userInitiated));
            if (userInitiated)
            {
                static const PCWSTR htmlContent =
                    L"<h1>Domain Blocked</h1>"
                    L"<p>You've attempted to navigate to a domain in the blocked "
                    L"sites list. Press back to return to the previous page.</p>";
                CHECK_FAILURE(sender->NavigateToString(htmlContent));
            }
        }
        // Changes to settings will apply at the next navigation, which includes the
        // navigation after a NavigationStarting event.  We can use this to change
        // settings according to what site we're visiting.
        if (ShouldBlockScriptForUri(uri.get()))
        {
            m_settings->put_IsScriptEnabled(FALSE);
        }
        else
        {
            m_settings->put_IsScriptEnabled(m_isScriptEnabled);
        }
        return S_OK;
    }).Get(), &m_navigationStartingToken));
```

#### remove_NavigationStarting 

Удалите обработчик событий, добавленный ранее add_NavigationStarting.

> общедоступные значения HRESULT [remove_NavigationStarting](#remove_navigationstarting)(маркер EventRegistrationToken)

#### add_DocumentStateChanged 

Добавьте обработчик событий для события DocumentStateChanged.

> общедоступные значения HRESULT [add_DocumentStateChanged](#add_documentstatechanged)([IWebView2DocumentStateChangedEventHandler](IWebView2DocumentStateChangedEventHandler.md) * eventHandler, EventRegistrationToken * token)

DocumentStateChanged активируется, когда начнется загрузка нового содержимого в основной кадр WebView или происходит та же Навигация по страницам (например, с помощью навигации фрагментов или журнала. pushState навигации). Это следует за событием NavigationStarting и предшествует событию NavigationCompleted.

```cpp
    // Register a handler for the DocumentStateChanged event.
    // This handler will read the webview's source URI and update
    // the app's address bar.
    CHECK_FAILURE(m_webView->add_DocumentStateChanged(
        Callback<IWebView2DocumentStateChangedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2DocumentStateChangedEventArgs* args)
                -> HRESULT {
                wil::unique_cotaskmem_string uri;
                sender->get_Source(&uri);
                if (wcscmp(uri.get(), L"about:blank") == 0)
                {
                    uri = wil::make_cotaskmem_string(L"");
                }
                SetWindowText(m_toolbar->addressBarWindow, uri.get());

                return S_OK;
            })
            .Get(),
        &m_documentStateChangedToken));
```

#### remove_DocumentStateChanged 

Удалите обработчик событий, добавленный ранее add_DocumentStateChanged.

> общедоступные значения HRESULT [remove_DocumentStateChanged](#remove_documentstatechanged)(маркер EventRegistrationToken)

#### add_NavigationCompleted 

Добавьте обработчик событий для события NavigationCompleted.

> общедоступные значения HRESULT [add_NavigationCompleted](#add_navigationcompleted)([IWebView2NavigationCompletedEventHandler](IWebView2NavigationCompletedEventHandler.md) * eventHandler, EventRegistrationToken * token)

Событие NavigationCompleted активируется, когда WebView полностью загружен (Body. onload) или загрузка остановлена с ошибкой.

```cpp
    // Register a handler for the NavigationCompleted event.
    // Check whether the navigation succeeded, and if not, do something.
    // Also update the Back, Forward, and Cancel buttons.
    CHECK_FAILURE(m_webView->add_NavigationCompleted(
        Callback<IWebView2NavigationCompletedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2NavigationCompletedEventArgs* args)
                -> HRESULT {
                BOOL success;
                CHECK_FAILURE(args->get_IsSuccess(&success));
                if (!success)
                {
                    WEBVIEW2_WEB_ERROR_STATUS webErrorStatus;
                    CHECK_FAILURE(args->get_WebErrorStatus(&webErrorStatus));
                    if (webErrorStatus == WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED)
                    {
                        // Do something here if you want to handle a specific error case.
                        // In most cases this isn't necessary, because the WebView will
                        // display its own error page automatically.
                    }
                }

                BOOL canGoBack;
                BOOL canGoForward;
                sender->get_CanGoBack(&canGoBack);
                sender->get_CanGoForward(&canGoForward);
                EnableWindow(m_toolbar->backWindow, canGoBack);
                EnableWindow(m_toolbar->forwardWindow, canGoForward);
                EnableWindow(m_toolbar->cancelWindow, FALSE);
                return S_OK;
            })
            .Get(),
        &m_navigationCompletedToken));
```

#### remove_NavigationCompleted 

Удалите обработчик событий, добавленный ранее add_NavigationCompleted.

> общедоступные значения HRESULT [remove_NavigationCompleted](#remove_navigationcompleted)(маркер EventRegistrationToken)

#### add_FrameNavigationStarting 

Добавьте обработчик событий для события FrameNavigationStarting.

> общедоступные значения HRESULT [add_FrameNavigationStarting](#add_framenavigationstarting)([IWebView2NavigationStartingEventHandler](IWebView2NavigationStartingEventHandler.md) * eventHandler, EventRegistrationToken * token)

FrameNavigationStarting активируется, когда дочерний кадр в WebView, запрашивающий разрешение на переход к другому URI. Это будет срабатывать и для перенаправления.

```cpp
    // Register a handler for the FrameNavigationStarting event.
    // This handler will prevent a frame from navigating to a blocked domain.
    CHECK_FAILURE(m_webView->add_FrameNavigationStarting(
        Callback<IWebView2NavigationStartingEventHandler>(
            [this](IWebView2WebView* sender,
                   IWebView2NavigationStartingEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Uri(&uri));

        if (ShouldBlockUri(uri.get()))
        {
            CHECK_FAILURE(args->put_Cancel(true));
        }
        return S_OK;
    }).Get(), &m_frameNavigationStartingToken));
```

#### remove_FrameNavigationStarting 

Удалите обработчик событий, добавленный ранее add_FrameNavigationStarting.

> общедоступные значения HRESULT [remove_FrameNavigationStarting](#remove_framenavigationstarting)(маркер EventRegistrationToken)

#### add_MoveFocusRequested 

Добавьте обработчик событий для события MoveFocusRequested.

> общедоступные значения HRESULT [add_MoveFocusRequested](#add_movefocusrequested)([IWebView2MoveFocusRequestedEventHandler](IWebView2MoveFocusRequestedEventHandler.md) * eventHandler, EventRegistrationToken * token)

MoveFocusRequested активируется, когда пользователь пытается выполнить переход из WebView. При срабатывании этого события фокус WebView не изменился.

```cpp
    // Register a handler for the MoveFocusRequested event.
    // This event will be fired when the user tabs out of the webview.
    // The handler will focus another window in the app, depending on which
    // direction the focus is being shifted.
    CHECK_FAILURE(m_webView->add_MoveFocusRequested(
        Callback<IWebView2MoveFocusRequestedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2MoveFocusRequestedEventArgs* args)
                -> HRESULT {
                if (!g_autoTabHandle)
                {
                    WEBVIEW2_MOVE_FOCUS_REASON reason;
                    CHECK_FAILURE(args->get_Reason(&reason));

                    if (reason == WEBVIEW2_MOVE_FOCUS_REASON_NEXT)
                    {
                        TabForwards(-1);
                    }
                    else if (reason == WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS)
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

> общедоступные значения HRESULT [add_GotFocus](#add_gotfocus)([IWebView2FocusChangedEventHandler](IWebView2FocusChangedEventHandler.md) * eventHandler, EventRegistrationToken * token)

Получение фокуса срабатывает, когда WebView получил фокусировку.

#### remove_GotFocus 

Удалите обработчик событий, добавленный ранее add_GotFocus.

> общедоступные значения HRESULT [remove_GotFocus](#remove_gotfocus)(маркер EventRegistrationToken)

#### add_LostFocus 

Добавьте обработчик для события LostFocus.

> общедоступные значения HRESULT [add_LostFocus](#add_lostfocus)([IWebView2FocusChangedEventHandler](IWebView2FocusChangedEventHandler.md) * eventHandler, EventRegistrationToken * token)

LostFocus вызывается, когда WebView теряет фокус. В случае, если возникает событие MoveFocusRequested, фокус по-прежнему находится в WebView при срабатывании события MoveFocusRequested. Потерянный фокус срабатывает только в том случае, если код приложения или действие по умолчанию, заданное MoveFocusRequested события, задали фокус от WebView.

#### remove_LostFocus 

Удалите обработчик событий, добавленный ранее add_LostFocus.

> общедоступные значения HRESULT [remove_LostFocus](#remove_lostfocus)(маркер EventRegistrationToken)

#### add_WebResourceRequested_deprecated 

Этот API будет устаревшим, воспользуйтесь новым add_WebResourceRequested API.

> открытые значения HRESULT [add_WebResourceRequested_deprecated](#add_webresourcerequested_deprecated)(LPCWSTR * const urlFilter,[WEBVIEW2_WEB_RESOURCE_CONTEXT](#webview2_web_resource_context) * const resourceContextFilter, SIZE_T filterLength,[IWebView2WebResourceRequestedEventHandler](IWebView2WebResourceRequestedEventHandler.md) * eventHandler, EventRegistrationToken * token)

Добавьте обработчик событий для события WebResourceRequested. Активируется, когда WebView выполняет HTTP-запрос. Используйте urlFilter для передачи списка с размером filterLength URL-адресов для прослушивания. Каждый элемент URL-адреса также поддерживает подстановочные знаки: "*" соответствует нулю или нескольким символам, а "?" соответствует одному символу. Для каждой записи urlFilter укажите соответствующие resourceContextFilter, представляющие типы ресурсов, которые должны срабатывать WebResourceRequested. Если filterLength 0, то событие будет срабатывать для всех сетевых запросов. Поддерживаются следующие контексты ресурсов: документ, таблица стилей, изображение, мультимедиа, шрифт, сценарий, XHR, выборка.

```cpp
        if (m_blockImages)
        {
            m_webView->AddWebResourceRequestedFilter(L"*", WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE);
            CHECK_FAILURE(m_webView->add_WebResourceRequested(
                Callback<IWebView2WebResourceRequestedEventHandler>(
                    [this](
                        IWebView2WebView* sender,
                        IWebView2WebResourceRequestedEventArgs* args) {
                        wil::com_ptr<IWebView2WebResourceRequestedEventArgs2>
                            webResourceEventArgs2;
                        args->QueryInterface(IID_PPV_ARGS(&webResourceEventArgs2));
                        WEBVIEW2_WEB_RESOURCE_CONTEXT resourceContext;
                        CHECK_FAILURE(
                            webResourceEventArgs2->get_ResourceContext(&resourceContext));
                        // Ensure that the type is image
                        if (resourceContext != WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE)
                        {
                            return E_INVALIDARG;
                        }
                        // Override the response with an empty one to block the image.
                        // If put_Response is not called, the request will continue as normal.
                        wil::com_ptr<IWebView2WebResourceResponse> response;
                        CHECK_FAILURE(m_webViewEnvironment->CreateWebResourceResponse(
                            nullptr, 403 /*NoContent*/, L"Blocked", L"", &response));
                        CHECK_FAILURE(args->put_Response(response.get()));
                        return S_OK;
                    })
                    .Get(),
                &m_webResourceRequestedTokenForImageBlocking));
        }
        else
        {
            CHECK_FAILURE(m_webView->remove_WebResourceRequested(
                m_webResourceRequestedTokenForImageBlocking));
        }
```

#### remove_WebResourceRequested 

Удалите обработчик событий, добавленный ранее add_WebResourceRequested.

> общедоступные значения HRESULT [remove_WebResourceRequested](#remove_webresourcerequested)(маркер EventRegistrationToken)

#### add_ScriptDialogOpening 

Добавьте обработчик событий для события ScriptDialogOpening.

> общедоступные значения HRESULT [add_ScriptDialogOpening](#add_scriptdialogopening)([IWebView2ScriptDialogOpeningEventHandler](IWebView2ScriptDialogOpeningEventHandler.md) * eventHandler, EventRegistrationToken * token)

Событие активируется, когда диалоговое окно JavaScript (предупреждение, подтверждение или запрос) будет отображаться для WebView. Это событие срабатывает только в том случае, если свойству IWebView2Settings:: AreDefaultScriptDialogsEnabled задано значение false.

```cpp
    // Register a handler for the ScriptDialogOpening event.
    // This handler will set up a custom prompt dialog for the user,
    // and may defer the event if the setting to defer dialogs is enabled.
    CHECK_FAILURE(m_webView->add_ScriptDialogOpening(
        Callback<IWebView2ScriptDialogOpeningEventHandler>(
            [this](
                IWebView2WebView* sender,
                IWebView2ScriptDialogOpeningEventArgs* args) -> HRESULT
    {
        wil::com_ptr<IWebView2ScriptDialogOpeningEventArgs> eventArgs = args;
        auto showDialog = [this, eventArgs]
        {
            wil::unique_cotaskmem_string uri;
            WEBVIEW2_SCRIPT_DIALOG_KIND type;
            wil::unique_cotaskmem_string message;
            wil::unique_cotaskmem_string defaultText;

            CHECK_FAILURE(eventArgs->get_Uri(&uri));
            CHECK_FAILURE(eventArgs->get_Kind(&type));
            CHECK_FAILURE(eventArgs->get_Message(&message));
            CHECK_FAILURE(eventArgs->get_DefaultText(&defaultText));

            std::wstring promptString = std::wstring(L"The page at '")
                + uri.get() + L"' says:";
            TextInputDialog dialog(
                m_appWindow->GetMainWindow(),
                L"Script Dialog",
                promptString.c_str(),
                message.get(),
                defaultText.get(),
                /* readonly */ type != WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT);
            if (dialog.confirmed)
            {
                CHECK_FAILURE(eventArgs->put_ResultText(dialog.input.c_str()));
                CHECK_FAILURE(eventArgs->Accept());
            }
        };

        if (m_deferScriptDialogs)
        {
            wil::com_ptr<IWebView2Deferral> deferral;
            CHECK_FAILURE(args->GetDeferral(&deferral));
            m_completeDeferredDialog = [showDialog, deferral]
            {
                showDialog();
                CHECK_FAILURE(deferral->Complete());
            };
        }
        else
        {
            showDialog();
        }

        return S_OK;
    }).Get(), &m_scriptDialogOpeningToken));
```

#### remove_ScriptDialogOpening 

Удалите обработчик событий, добавленный ранее add_ScriptDialogOpening.

> общедоступные значения HRESULT [remove_ScriptDialogOpening](#remove_scriptdialogopening)(маркер EventRegistrationToken)

#### add_ZoomFactorChanged 

Добавьте обработчик событий для события ZoomFactorChanged.

> общедоступные значения HRESULT [add_ZoomFactorChanged](#add_zoomfactorchanged)([IWebView2ZoomFactorChangedEventHandler](IWebView2ZoomFactorChangedEventHandler.md) * eventHandler, EventRegistrationToken * token)

Событие срабатывает, когда изменяется свойство ZoomFactor объекта WebView. Событие может срабатывать из-за того, что вызывающий объект изменил свойство ZoomFactor или пользователь вручную изменял масштаб. При изменении вызывающим абонентом с помощью свойства ZoomFactor внутренний коэффициент масштабирования немедленно обновляется, и событие ZoomFactorChanged не выводится. WebView связывает последний использованный коэффициент масштабирования для каждого сайта. Поэтому коэффициент масштабирования может изменяться при переходе на другую страницу. При изменении коэффициента масштабирования из-за этого событие ZoomFactorChanged срабатывает сразу после события DocumentStateChanged.

```cpp
    // Register a handler for the ZoomFactorChanged event.
    // This handler just announces the new level of zoom on the window's title bar.
    CHECK_FAILURE(m_webView->add_ZoomFactorChanged(
        Callback<IWebView2ZoomFactorChangedEventHandler>(
            [this](IWebView2WebView* sender, IUnknown* args) -> HRESULT {
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

#### add_PermissionRequested 

Добавьте обработчик событий для события PermissionRequested.

> общедоступные значения HRESULT [add_PermissionRequested](#add_permissionrequested)([IWebView2PermissionRequestedEventHandler](IWebView2PermissionRequestedEventHandler.md) * eventHandler, EventRegistrationToken * token)

Вызывается, когда содержимое в WebView запрашивает разрешение на доступ к некоторым привилегированным ресурсам.

```cpp
    // Register a handler for the PermissionRequested event.
    // This handler prompts the user to allow or deny the request.
    CHECK_FAILURE(m_webView->add_PermissionRequested(
        Callback<IWebView2PermissionRequestedEventHandler>(
            [this](
                IWebView2WebView* sender,
                IWebView2PermissionRequestedEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        WEBVIEW2_PERMISSION_TYPE type = WEBVIEW2_PERMISSION_TYPE_UNKNOWN_PERMISSION;
        BOOL userInitiated = FALSE;

        CHECK_FAILURE(args->get_Uri(&uri));
        CHECK_FAILURE(args->get_PermissionType(&type));
        CHECK_FAILURE(args->get_IsUserInitiated(&userInitiated));

        std::wstring message = L"Do you want to grant permission for ";
        message += NameOfPermissionType(type);
        message += L" to the website at ";
        message += uri.get();
        message += L"?\n\n";
        message += (userInitiated
            ? L"This request came from a user gesture."
            : L"This request did not come from a user gesture.");

        int response = MessageBox(nullptr, message.c_str(), L"Permission Request",
                                   MB_YESNOCANCEL | MB_ICONWARNING);

        WEBVIEW2_PERMISSION_STATE state =
              response == IDYES ? WEBVIEW2_PERMISSION_STATE_ALLOW
            : response == IDNO  ? WEBVIEW2_PERMISSION_STATE_DENY
            :                     WEBVIEW2_PERMISSION_STATE_DEFAULT;
        CHECK_FAILURE(args->put_State(state));

        return S_OK;
    }).Get(), &m_permissionRequestedToken));
```

#### remove_PermissionRequested 

Удалите обработчик событий, добавленный ранее add_PermissionRequested.

> общедоступные значения HRESULT [remove_PermissionRequested](#remove_permissionrequested)(маркер EventRegistrationToken)

#### add_ProcessFailed 

Добавьте обработчик событий для события ProcessFailed.

> общедоступные значения HRESULT [add_ProcessFailed](#add_processfailed)([IWebView2ProcessFailedEventHandler](IWebView2ProcessFailedEventHandler.md) * eventHandler, EventRegistrationToken * token)

Активируется, когда WebView процесс неожиданно завершился или перестал отвечать на запросы.

```cpp
    // Register a handler for the ProcessFailed event.
    // This handler checks if the browser process failed, and asks the user if
    // they want to recreate the webview.
    CHECK_FAILURE(m_webView->add_ProcessFailed(
        Callback<IWebView2ProcessFailedEventHandler>(
            [this](IWebView2WebView* sender,
                IWebView2ProcessFailedEventArgs* args) -> HRESULT
    {
        WEBVIEW2_PROCESS_FAILED_KIND failureType;
        CHECK_FAILURE(args->get_ProcessFailedKind(&failureType));
        if (failureType == WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED)
        {
            int button = MessageBox(
                m_appWindow->GetMainWindow(),
                L"Browser process exited unexpectedly.  Recreate webview?",
                L"Browser process exited",
                MB_YESNO);
            if (button == IDYES)
            {
                m_appWindow->ReinitializeWebView();
            }
        }
        return S_OK;
    }).Get(), &m_processFailedToken));
```

#### remove_ProcessFailed 

Удалите обработчик событий, добавленный ранее add_ProcessFailed.

> общедоступные значения HRESULT [remove_ProcessFailed](#remove_processfailed)(маркер EventRegistrationToken)

#### AddScriptToExecuteOnDocumentCreated 

Добавьте предоставленный JavaScript в список сценариев, которые должны выполняться после создания глобального объекта, но до начала синтаксического анализа HTML-документа и перед выполнением любого другого сценария, включенного в документ HTML.

> общедоступные значения HRESULT [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)(LPCWSTR JavaScript,[IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler.md) * обработчик)

Вставленный сценарий будет применяться ко всем документам верхнего уровня и дочерним элементам навигации, пока они не будут удалены с помощью RemoveScriptToExecuteOnDocumentCreated. Это применяется асинхронно, и вы должны дождаться выполнения обработчика завершения, прежде чем можно будет убедиться, что сценарий готов к выполнению для навигации в будущем.

Обратите внимание, что если в HTML-документе есть изолированная [Среда с определенными свойствами или](https://developer.mozilla.org/docs/Web/HTML/Element/iframe#attr-sandbox) [заголовок HTTP Content-Security-Policy](https://developer.mozilla.org/docs/Web/HTTP/Headers/Content-Security-Policy) , это повлияет на выполнение сценария. Таким образом, например, если ключевое слово "Allow-Modal" не задано, вызовы `alert` функции будут игнорироваться.

```cpp
// Prompt the user for some script and register it to execute whenever a new page loads.
void ScriptComponent::AddInitializeScript()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Add Initialize Script",
        L"Initialization Script:",
        L"Enter the JavaScript code to run as the initialization script that "
            L"runs before any script in the HTML document.",
    // This example script stops child frames from opening new windows.  Because
    // the initialization script runs before any script in the HTML document, we
    // can trust the results of our checks on window.parent and window.top.
        L"if (window.parent !== window.top) {\r\n"
        L"    delete window.open;\r\n"
        L"}");
    if (dialog.confirmed)
    {
        m_webView->AddScriptToExecuteOnDocumentCreated(
            dialog.input.c_str(),
            Callback<IWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler>(
                [this](HRESULT error, PCWSTR id) -> HRESULT
        {
            m_lastInitializeScriptId = id;
            MessageBox(nullptr, id, L"AddScriptToExecuteOnDocumentCreated Id", MB_OK);
            return S_OK;
        }).Get());

    }
}
```

#### RemoveScriptToExecuteOnDocumentCreated 

Удалите соответствующий сценарий JavaScript, добавленный через AddScriptToExecuteOnDocumentCreated.

> общедоступные значения HRESULT [RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated)(ИД LPCWSTR)

#### ExecuteScript 

Выполнение кода JavaScript из параметра JavaScript в текущем документе верхнего уровня, отображаемом в WebView.

> общедоступные значения HRESULT [ExecuteScript](#executescript)(LPCWSTR JavaScript,[IWebView2ExecuteScriptCompletedHandler](IWebView2ExecuteScriptCompletedHandler.md) * обработчик)

Это выполняется асинхронно и по завершении, если обработчик предоставлен в параметре ExecuteScriptCompletedHandler, вызывается его метод Invoke с результатом вычисления предоставленного JavaScript. Результирующее значение — это строка в кодировке JSON. Если результат не определен, содержит цикл ссылки или не может быть закодирован в JSON, значение NULL JSON будет возвращено в виде строки null. Обратите внимание, что функция без явного возвращаемого значения возвращает значение undefine. Если выполняемый сценарий создает необработанное исключение, результат также равен null. Этот метод применяется асинхронно. Если вызов выполняется, когда WebView находится на одном документе, а переход происходит после того, как вызов выполнен, но перед выполнением JavaScript, то сценарий не будет выполнен, а обработчик будет вызван с E_FAIL для параметра errorCode. ExecuteScript будет работать даже в том случае, если IsScriptEnabled имеет значение FALSE.

```cpp
// Prompt the user for some script and then execute it.
void ScriptComponent::InjectScript()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Inject Script",
        L"Enter script code:",
        L"Enter the JavaScript code to run in the webview.",
        L"window.getComputedStyle(document.body).backgroundColor");
    if (dialog.confirmed)
    {
        m_webView->ExecuteScript(dialog.input.c_str(),
            Callback<IWebView2ExecuteScriptCompletedHandler>(
                [](HRESULT error, PCWSTR result) -> HRESULT
        {
            if (error != S_OK) {
                ShowFailure(error, L"ExecuteScript failed");
            }
            MessageBox(nullptr, result, L"ExecuteScript Result", MB_OK);
            return S_OK;
        }).Get());
    }
}
```

#### CapturePreview 

Запишите изображение того, что WebView на экране.

> Public HRESULT [CapturePreview](#capturepreview)([WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#webview2_capture_preview_image_format) ImageFormat, IStream * ImageStream,[IWebView2CapturePreviewCompletedHandler](IWebView2CapturePreviewCompletedHandler.md) * обработчик)

Укажите формат изображения с помощью параметра imageFormat. Результирующие двоичные данные изображения записываются в указанный параметр imageStream. Когда CapturePreview закончит запись в поток, вызывается метод Invoke в указанном параметре обработчика.

```cpp
// Show the user a file selection dialog, then save a screenshot of the WebView
// to the selected file.
void FileComponent::SaveScreenshot()
{
    OPENFILENAME openFileName = {};
    openFileName.lStructSize = sizeof(openFileName);
    openFileName.hwndOwner = nullptr;
    openFileName.hInstance = nullptr;
    WCHAR fileName[MAX_PATH] = L"WebView2_Screenshot.png";
    openFileName.lpstrFile = fileName;
    openFileName.lpstrFilter = L"PNG File\0*.png\0";
    openFileName.nMaxFile = ARRAYSIZE(fileName);
    openFileName.Flags = OFN_OVERWRITEPROMPT;

    if (GetSaveFileName(&openFileName))
    {
        wil::com_ptr<IStream> stream;
        CHECK_FAILURE(SHCreateStreamOnFileEx(
            fileName, STGM_READWRITE | STGM_CREATE, FILE_ATTRIBUTE_NORMAL, TRUE, nullptr,
            &stream));

        HWND mainWindow = m_appWindow->GetMainWindow();

        CHECK_FAILURE(m_webView->CapturePreview(
            WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG, stream.get(),
            Callback<IWebView2CapturePreviewCompletedHandler>(
                [mainWindow](HRESULT error_code) -> HRESULT {
                    CHECK_FAILURE(error_code);

                    MessageBox(mainWindow, L"Preview Captured", L"Preview Captured", MB_OK);
                    return S_OK;
                })
                .Get()));
    }
}
```

#### Перезагрузить 

Перезагрузите текущую страницу.

> общедоступная [Перезагрузка](#reload)HRESULT ()

Это похоже на то, что переход к URI текущего документа верхнего уровня, включая все события навигации, которые обрабатывались, и учитывает любые записи в кэше HTTP. Но история «назад» и «вперед» не будет изменена.

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
    RECT desiredBounds = m_webViewBounds;
    desiredBounds.bottom = LONG(
        (m_webViewBounds.bottom - m_webViewBounds.top) * m_webViewRatio + m_webViewBounds.top);
    desiredBounds.right = LONG(
        (m_webViewBounds.right - m_webViewBounds.left) * m_webViewRatio + m_webViewBounds.left);

    m_webView->put_Bounds(desiredBounds);
}
```

#### get_ZoomFactor 

Коэффициент увеличения для текущей страницы в WebView.

> общедоступные значения HRESULT [get_ZoomFactor](#get_zoomfactor)(Double * ZoomFactor)

Коэффициент масштабирования сохраняется на каждом сайте. Обратите внимание, что изменение коэффициента масштабирования может привести к `window.innerWidth/innerHeight` изменению масштаба страницы. Когда WebView переходит на страницу с другого сайта, коэффициент масштабирования, заданный для предыдущей страницы, не будет применен. Если приложение захочет задать коэффициент масштабирования для определенной страницы, самое раннее место — в обработчике событий DocumentStateChanged. Обратите внимание, что если это так, может возникнуть событие ZoomFactorChanged для коэффициента материализованных масштабов перед получением события ZoomFactorChanged для указанного коэффициента масштабирования. Указывать zoomFactor меньше или равно 0 не разрешается. WebView также имеет внутренний поддерживаемый диапазон коэффициента масштабирования. Если указанный коэффициент масштаба выходит за пределы этого диапазона, он будет нормализован в пределах диапазона, а событие ZoomFactorChanged будет инициировано для фактического коэффициента масштабирования. При выполнении этой нормализации диапазона свойство ZoomFactor будет указывать коэффициент масштабирования, указанный в предыдущем изменении свойства ZoomFactor, пока событие ZoomFactorChanged не будет получено после WebView применяет нормализованный коэффициент масштабирования.

#### put_ZoomFactor 

Задайте свойство ZoomFactor.

> общедоступный [PUT_ZOOMFACTOR](#put_zoomfactor)HRESULT (двойной ZoomFactor)

#### get_IsVisible 

Свойство Visible определяет, нужно ли отображать или скрывать WebView.

> общедоступные значения HRESULT [get_IsVisible](#get_isvisible)(bool * Visible)

Если для свойства Visible задано значение false, WebView будет прозрачным и не будет обрабатываться. Однако это не повлияет на окно, содержащее WebView (параметр HWND, переданный в CreateWebView). Если вы хотите, чтобы окно не исчезало, вызовите для него функцию ShowWindow прямо в дополнение к изменению свойства Visible. WebView — это дочернее окно не получает оконные сообщения, когда окно свертывания или восстановления находится в верхней части окна. Для повышения производительности разработчик должен установить для свойства WebView значение false, если окно приложения свернуто, и вернуть значение true при восстановлении окна приложения. Это можно сделать, обрабатывая команды SC_MINIMIZE и SC_RESTORE при получении WM_SYSCOMMAND сообщения.

```cpp
void ViewComponent::ToggleVisibility()
{
    BOOL visible;
    m_webView->get_IsVisible(&visible);
    m_isVisible = !visible;
    m_webView->put_IsVisible(m_isVisible);
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
            m_webView->put_IsVisible(FALSE);
        }
        else if (wParam == SC_RESTORE)
        {
            // When the app window is restored, show the webview
            // (unless the user has toggle visibility off).
            if (m_isVisible)
            {
                m_webView->put_IsVisible(TRUE);
            }
        }
    }
```

#### PostWebMessageAsJson 

Опубликуйте указанное сообщение в документе верхнего уровня в этом [IWebView2WebView]().

> общедоступные значения HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)

Срабатывает событие Window. Chrome. WebView для документа верхнего уровня. JavaScript в этом документе может подписываться на событие и отменять подписку с помощью следующих действий: 

```cpp
window.chrome.webview.addEventListener('message', handler)
window.chrome.webview.removeEventListener('message', handler)
```

 Аргументы события представляют собой экземпляр `MessageEvent` . Параметр IWebView2Settings:: IsWebMessageEnabled должен быть истинным, или этот метод завершится сбоем с E_INVALIDARG. Свойство данных аргумента "событие" — это строковый параметр веб-сообщения, проанализированный как строка JSON, в объект JavaScript. Свойство Source аргумента "событие" является ссылкой на `window.chrome.webview` объект. Сведения о том, как отправлять сообщения из HTML-документа на WebView на узел, можно найти в SetWebMessageReceivedEventHandler. Это сообщение отправляется асинхронно. Если переход выполняется до того, как сообщение будет отправлено на страницу, оно не будет отправлено.

```cpp
    // Setup the web message received event handler before navigating to
    // ensure we don't miss any messages.
    CHECK_FAILURE(m_webView->add_WebMessageReceived(
        Microsoft::WRL::Callback<IWebView2WebMessageReceivedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2WebMessageReceivedEventArgs* args)
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Source(&uri));

        // Always validate that the origin of the message is what you expect.
        if (uri.get() != m_sampleUri)
        {
            return S_OK;
        }
        wil::unique_cotaskmem_string messageRaw;
        CHECK_FAILURE(args->get_WebMessageAsString(&messageRaw));
        std::wstring message = messageRaw.get();

        if (message.compare(0, 13, L"SetTitleText ") == 0)
        {
            m_appWindow->SetTitleText(message.substr(13).c_str());
        }
        else if (message.compare(L"GetWindowBounds") == 0)
        {
            RECT bounds = m_appWindow->GetWindowBounds();
            std::wstring reply =
                L"{\"WindowBounds\":\"Left:" + std::to_wstring(bounds.left)
                + L"\\nTop:" + std::to_wstring(bounds.top)
                + L"\\nRight:" + std::to_wstring(bounds.right)
                + L"\\nBottom:" + std::to_wstring(bounds.bottom)
                + L"\"}";
            CHECK_FAILURE(sender->PostWebMessageAsJson(reply.c_str()));
        }
        return S_OK;
    }).Get(), &m_webMessageReceivedToken));
```

#### PostWebMessageAsString 

Это вспомогательный объект для отправки сообщения, которое является простой строкой, а не строкой JSON-представления объекта JavaScript.

> общедоступные значения HRESULT [PostWebMessageAsString](#postwebmessageasstring)(LPCWSTR webMessageAsString)

Это выполняется точно так же, как и PostWebMessageAsJson, но `window.chrome.webview` свойство Data события ARG имеет строковое значение с тем же значением, что и webMessageAsString. Используйте это вместо PostWebMessageAsJson, если вы хотите общаться с помощью простых строк, а не объектов JSON.

#### add_WebMessageReceived 

Это событие срабатывает, если задан параметр IsWebMessageEnabled и документ верхнего уровня для вызовов WebView `window.chrome.webview.postMessage` .

> общедоступные значения HRESULT [add_WebMessageReceived](#add_webmessagereceived)(обработчик[IWebView2WebMessageReceivedEventHandler](IWebView2WebMessageReceivedEventHandler.md) *, EventRegistrationToken * token)

Функция i, в `void postMessage(object)` которой объект — это любой объект, поддерживаемый преобразованием JSON.

```cpp
        window.chrome.webview.addEventListener('message', arg => {
            if ("SetColor" in arg.data) {
                document.getElementById("colorable").style.color = arg.data.SetColor;
            }
            if ("WindowBounds" in arg.data) {
                document.getElementById("window-bounds").value = arg.data.WindowBounds;
            }
        });

        function SetTitleText() {
            let titleText = document.getElementById("title-text");
            window.chrome.webview.postMessage(`SetTitleText ${titleText.value}`);
        }
        function GetWindowBounds() {
            window.chrome.webview.postMessage("GetWindowBounds");
        }
```

 При вызове [IWebView2WebMessageReceivedEventHandler](IWebView2WebMessageReceivedEventHandler.md) набор с помощью этого метода SetWebMessageReceivedEventHandler вызывается с помощью параметра объекта i, преобразованного в строку JSON.

```cpp
    // Setup the web message received event handler before navigating to
    // ensure we don't miss any messages.
    CHECK_FAILURE(m_webView->add_WebMessageReceived(
        Microsoft::WRL::Callback<IWebView2WebMessageReceivedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2WebMessageReceivedEventArgs* args)
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Source(&uri));

        // Always validate that the origin of the message is what you expect.
        if (uri.get() != m_sampleUri)
        {
            return S_OK;
        }
        wil::unique_cotaskmem_string messageRaw;
        CHECK_FAILURE(args->get_WebMessageAsString(&messageRaw));
        std::wstring message = messageRaw.get();

        if (message.compare(0, 13, L"SetTitleText ") == 0)
        {
            m_appWindow->SetTitleText(message.substr(13).c_str());
        }
        else if (message.compare(L"GetWindowBounds") == 0)
        {
            RECT bounds = m_appWindow->GetWindowBounds();
            std::wstring reply =
                L"{\"WindowBounds\":\"Left:" + std::to_wstring(bounds.left)
                + L"\\nTop:" + std::to_wstring(bounds.top)
                + L"\\nRight:" + std::to_wstring(bounds.right)
                + L"\\nBottom:" + std::to_wstring(bounds.bottom)
                + L"\"}";
            CHECK_FAILURE(sender->PostWebMessageAsJson(reply.c_str()));
        }
        return S_OK;
    }).Get(), &m_webMessageReceivedToken));
```

#### remove_WebMessageReceived 

Удалите обработчик событий, добавленный ранее add_WebMessageReceived.

> общедоступные значения HRESULT [remove_WebMessageReceived](#remove_webmessagereceived)(маркер EventRegistrationToken)

#### Close (закрыть) 

Закрывает WebView и очищает основной экземпляр браузера.

> общедоступное значение HRESULT [Close](#close)()

Очистка браузера instace освобождает ресурсы, переключающие WebView. Экземпляр браузера будет закрыт, если он не используется другими веб – представлениями.

После вызова метода Close все вызовы методов завершатся сбоем, и обработчики событий прекратятся. В частности, WebView будет освобождать ссылки на обработчики событий при вызове Close.

Метод Close вызывается неявно, когда WebView теряет свою конечную ссылку и является независимым. Но рекомендуется явным образом вызывать метод Close, чтобы избежать случайного цикла ссылок между WebView и кодом приложения. В частности, если вы захватываете ссылку на WebView в обработчике событий, вы создадите цикл ссылки между WebView и обработчиком событий. Закрыть, чтобы прервать этот цикл, освобождая все обработчики событий. Но чтобы избежать такой ситуации, рекомендуется явно вызвать метод Close для WebView и не захватывать ссылку на WebView, чтобы убедиться в том, что WebView может быть корректно очищено.

```cpp
// Close the WebView and deinitialize related state. This doesn't close the app window.
void AppWindow::CloseWebView()
{
    DeleteAllComponents();
    if (m_webView)
    {
        m_webView->Close();
        m_webView = nullptr;
    }
    m_webViewEnvironment = nullptr;
}
```

#### CallDevToolsProtocolMethod 

Вызовите асинхронный метод DevToolsProtocol.

> общедоступные значения HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR METHODNAME, LPCWSTR ParametersAsJson,[IWebView2CallDevToolsProtocolMethodCompletedHandler](IWebView2CallDevToolsProtocolMethodCompletedHandler.md) * handler)

Список и описание доступных методов можно найти в [средстве просмотра протокола DevTools](https://aka.ms/DevToolsProtocolDocs) . Параметр methodName — это полное имя метода в формате `{domain}.{method}` . Параметр parametersAsJson является строкой в формате JSON, содержащей параметры соответствующего метода. Метод Invoke обработчика вызывается, когда метод асинхронно завершается. Вызов Invoke будет вызываться с возвращаемым методом объектом в виде строки JSON.

```cpp
// Prompt the user for the name and parameters of a CDP method, then call it.
void ScriptComponent::CallCdpMethod()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Call CDP Method",
        L"CDP method name:",
        L"Enter the CDP method name to call, followed by a space,\r\n"
            L"followed by the parameters in JSON format.",
        L"Runtime.evaluate {\"expression\":\"alert(\\\"test\\\")\"}");
    if (dialog.confirmed)
    {
        size_t delimiterPos = dialog.input.find(L' ');
        std::wstring methodName = dialog.input.substr(0, delimiterPos);
        std::wstring methodParams =
            (delimiterPos < dialog.input.size()
                ? dialog.input.substr(delimiterPos + 1)
                : L"{}");

        m_webView->CallDevToolsProtocolMethod(
            methodName.c_str(),
            methodParams.c_str(),
            Callback<IWebView2CallDevToolsProtocolMethodCompletedHandler>(
                [](HRESULT error, PCWSTR resultJson) -> HRESULT
                {
                    MessageBox(nullptr, resultJson, L"CDP Method Result", MB_OK);
                    return S_OK;
                }).Get());
    }
}
```

#### add_DevToolsProtocolEventReceived 

Подпишитесь на событие DevToolsProtocol.

> общедоступные значения HRESULT [add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived)(LPCWSTR eventName,[IWebView2DevToolsProtocolEventReceivedEventHandler](IWebView2DevToolsProtocolEventReceivedEventHandler.md) * обработчик, EventRegistrationToken * token)

Список и описание доступных событий можно найти в [средстве просмотра протокола DevTools](https://aka.ms/DevToolsProtocolDocs) . Параметр eventName — это полное имя события в формате `{domain}.{event}` . Метод Invoke обработчика вызывается каждый раз, когда будет срабатывать соответствующее событие DevToolsProtocol. Вызов вызывается с использованием объекта аргументов события, содержащего объект Parameter события CDP, в виде строки JSON.

```cpp
// Prompt the user to name a CDP event, and then subscribe to that event.
void ScriptComponent::SubscribeToCdpEvent()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Subscribe to CDP Event",
        L"CDP event name:",
        L"Enter the name of the CDP event to subscribe to.\r\n"
            L"You may also have to call the \"enable\" method of the\r\n"
            L"event's domain to receive events (for example \"Log.enable\").\r\n",
        L"Log.entryAdded");
    if (dialog.confirmed)
    {
        std::wstring eventName = dialog.input;
        // If we are already subscribed to this event, unsubscribe first.
        auto preexistingToken = m_devToolsProtocolEventReceivedTokenMap.find(eventName);
        if (preexistingToken != m_devToolsProtocolEventReceivedTokenMap.end())
        {
            CHECK_FAILURE(m_webView->remove_DevToolsProtocolEventReceived(
                eventName.c_str(),
                preexistingToken->second));
        }

        CHECK_FAILURE(m_webView->add_DevToolsProtocolEventReceived(
            eventName.c_str(),
            Callback<IWebView2DevToolsProtocolEventReceivedEventHandler>(
                [eventName](IWebView2WebView* sender,
                            IWebView2DevToolsProtocolEventReceivedEventArgs* args)
                -> HRESULT
        {
            wil::unique_cotaskmem_string parameterObjectAsJson;
            CHECK_FAILURE(args->get_ParameterObjectAsJson(&parameterObjectAsJson));
            MessageBox(nullptr, parameterObjectAsJson.get(),
                       (L"CDP Event Fired: " + eventName).c_str(), MB_OK);
            return S_OK;
        }).Get(), &m_devToolsProtocolEventReceivedTokenMap[eventName]));
    }
}
```

#### remove_DevToolsProtocolEventReceived 

Удалите обработчик событий, добавленный ранее add_DevToolsProtocolEventReceived.

> общедоступные значения HRESULT [remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived)(LPCWSTR eventName, EventRegistrationToken token)

#### get_BrowserProcessId 

Идентификатор процесса браузера, на котором размещается WebView.

> общедоступные значения HRESULT [get_BrowserProcessId](#get_browserprocessid)(UINT32 * Value)

#### get_CanGoBack 

Можно переходить по WebView на предыдущую страницу в истории навигации.

> общедоступные значения HRESULT [get_CanGoBack](#get_cangoback)(bool * CanGoBack)

get_CanGoBack изменить значение с помощью события DocumentStateChanged.

#### get_CanGoForward 

Можно переходить по WebView на следующую страницу в истории навигации.

> общедоступные значения HRESULT [get_CanGoForward](#get_cangoforward)(bool * CanGoForward)

get_CanGoForward изменить значение с помощью события DocumentStateChanged.

#### GoBack 

Переход по WebView на предыдущую страницу в истории навигации.

> общедоступное значение HRESULT [GoBack](#goback)()

#### GoForward 

Переход по WebView к следующей странице в истории навигации.

> общедоступные значения HRESULT [GoForward](#goforward)()

#### WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT 

Формат изображения, используемый в методе [IWebView2WebView:: CapturePreview](#capturepreview) .

> [WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#webview2_capture_preview_image_format) перечисления

 Данные                         | Описания
--------------------------------|---------------------------------------------
WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG            | Формат изображения PNG.
WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG            | Формат изображения JPEG.

#### WEBVIEW2_SCRIPT_DIALOG_KIND 

Диалоговое окно вида JavaScript, используемое в интерфейсе [IWebView2ScriptDialogOpeningEventHandler](IWebView2ScriptDialogOpeningEventHandler.md) .

> [WEBVIEW2_SCRIPT_DIALOG_KIND](#webview2_script_dialog_kind) перечисления

 Данные                         | Описания
--------------------------------|---------------------------------------------
WEBVIEW2_SCRIPT_DIALOG_KIND_ALERT            | Диалоговое окно, вызываемое с помощью функции Window. Alert JavaScript.
WEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM            | Диалоговое окно, вызываемое с помощью функции Window. Confirm JavaScript.
WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT            | Диалоговое окно, вызываемое с помощью функции Window. prompt JavaScript.

#### WEBVIEW2_PROCESS_FAILED_KIND 

Состояние сбоя процесса, используемого в интерфейсе [IWebView2ProcessFailedEventHandler](IWebView2ProcessFailedEventHandler.md) .

> [WEBVIEW2_PROCESS_FAILED_KIND](#webview2_process_failed_kind) перечисления

 Данные                         | Описания
--------------------------------|---------------------------------------------
WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED            | Указывает, что процесс браузера неожиданно завершился.
WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED            | Указывает, что процесс обработки неожиданно завершился.
WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE            | Указывает на то, что процесс рендеринга перестает отвечать на запросы.

#### WEBVIEW2_PERMISSION_TYPE 

Тип запроса разрешения.

> [WEBVIEW2_PERMISSION_TYPE](#webview2_permission_type) перечисления

 Данные                         | Описания
--------------------------------|---------------------------------------------
WEBVIEW2_PERMISSION_TYPE_UNKNOWN_PERMISSION            | Неизвестное разрешение.
WEBVIEW2_PERMISSION_TYPE_MICROPHONE            | Разрешение на запись звука.
WEBVIEW2_PERMISSION_TYPE_CAMERA            | Разрешение на захват видео.
WEBVIEW2_PERMISSION_TYPE_GEOLOCATION            | Разрешение на доступ к географической позиции.
WEBVIEW2_PERMISSION_TYPE_NOTIFICATIONS            | Разрешение на отправку веб-уведомлений.
WEBVIEW2_PERMISSION_TYPE_OTHER_SENSORS            | Разрешение на доступ к универсальному датчику.
WEBVIEW2_PERMISSION_TYPE_CLIPBOARD_READ            | Разрешение на чтение системного буфера обмена без жеста пользователя.

#### WEBVIEW2_PERMISSION_STATE 

Ответ на запрос разрешения.

> [WEBVIEW2_PERMISSION_STATE](#webview2_permission_state) перечисления

 Данные                         | Описания
--------------------------------|---------------------------------------------
WEBVIEW2_PERMISSION_STATE_DEFAULT            | Используйте поведение браузера по умолчанию, которое обычно запрашивает у пользователей решение.
WEBVIEW2_PERMISSION_STATE_ALLOW            | Предоставьте разрешение на запрос.
WEBVIEW2_PERMISSION_STATE_DENY            | Отказ от запроса разрешения.

#### WEBVIEW2_MOVE_FOCUS_REASON 

Причина для перемещения фокуса.

> [WEBVIEW2_MOVE_FOCUS_REASON](#webview2_move_focus_reason) перечисления

 Данные                         | Описания
--------------------------------|---------------------------------------------
WEBVIEW2_MOVE_FOCUS_REASON_PROGRAMMATIC            | Настройка кода фокуса на WebView.
WEBVIEW2_MOVE_FOCUS_REASON_NEXT            | Перемещение фокуса из-за прохождения вкладки вперед.
WEBVIEW2_MOVE_FOCUS_REASON_PREVIOUS            | Перемещение фокуса из-за перемещения по табуляции назад.

#### WEBVIEW2_WEB_ERROR_STATUS 

Значения состояния ошибки для переходов по веб-страницам.

> [WEBVIEW2_WEB_ERROR_STATUS](#webview2_web_error_status) перечисления

 Данные                         | Описания
--------------------------------|---------------------------------------------
WEBVIEW2_WEB_ERROR_STATUS_UNKNOWN            | Произошла неизвестная ошибка.
WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT            | Общее имя сертификата SSL не совпадает с веб-адресом.
WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED            | Срок действия сертификата SSL истек.
WEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS            | SSL-сертификат клиента включает ошибки.
WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED            | SSL-сертификат отозван.
WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID            | Недействительный сертификат SSL.
WEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE            | Узел недостижим.
WEBVIEW2_WEB_ERROR_STATUS_TIMEOUT            | Время ожидания соединения истекло.
WEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE            | Сервер вернул недопустимый или нераспознанный ответ.
WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED            | Соединение было прервано.
WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET            | Подключение было сброшено.
WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED            | Соединение с Интернетом разорвано.
WEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT            | Не удается подключиться к конечному объекту.
WEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED            | Не удалось разрешить указанное имя узла.
WEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED            | Операция была отменена.
WEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED            | Перенаправление запроса завершилось сбоем.
WEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR            | Произошла непредвиденная ошибка.

#### WEBVIEW2_WEB_RESOURCE_CONTEXT 

Перечисление для контекстов запросов веб-ресурсов.

> [WEBVIEW2_WEB_RESOURCE_CONTEXT](#webview2_web_resource_context) перечисления

 Данные                         | Описания
--------------------------------|---------------------------------------------
WEBVIEW2_WEB_RESOURCE_CONTEXT_ALL            | Все ресурсы.
WEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT            | Ресурсы документов.
WEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET            | Ресурсы CSS.
WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE            | Графические ресурсы.
WEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA            | Другие мультимедийные ресурсы, например видео.
WEBVIEW2_WEB_RESOURCE_CONTEXT_FONT            | Ресурсы шрифта.
WEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT            | Ресурсы сценария.
WEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST            | HTTP-запросы.
WEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH            | Получение взаимодействия API.
WEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK            | TextTrack ресурсы.
WEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE            | 
WEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET            | 
WEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST            | 
WEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE            | 
WEBVIEW2_WEB_RESOURCE_CONTEXT_PING            | 
WEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT            | 
WEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER            | Другие ресурсы.
