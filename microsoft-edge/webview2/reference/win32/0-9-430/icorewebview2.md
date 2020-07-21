---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: d80570a82559fccb6ae3896f7543ed75959436fa
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884430"
---
# 0.9.430-Interface ICoreWebView2 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2
  : public IUnknown
```

WebView2 позволяет размещать веб-содержимое с помощью новейшей технологии веб-браузера.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[get_Settings](#get_settings) | Объект ICoreWebView2Settings, содержащий различные изменяемые параметры для запущенного WebView.
[get_Source](#get_source) | Универсальный код ресурса (URI) текущего документа верхнего уровня.
[Которому](#navigate) | Применяет навигацию по документу верхнего уровня к указанному универсальному коду ресурса (URI).
[NavigateToString](#navigatetostring) | Запускает навигацию для htmlContent в качестве исходного HTML-кода нового документа.
[add_NavigationStarting](#add_navigationstarting) | Добавьте обработчик событий для события NavigationStarting.
[remove_NavigationStarting](#remove_navigationstarting) | Удалите обработчик событий, добавленный ранее add_NavigationStarting.
[add_ContentLoading](#add_contentloading) | Добавьте обработчик событий для события ContentLoading.
[remove_ContentLoading](#remove_contentloading) | Удалите обработчик событий, добавленный ранее add_ContentLoading.
[add_SourceChanged](#add_sourcechanged) | SourceChanged активируется при изменении свойства Source.
[remove_SourceChanged](#remove_sourcechanged) | Удалите обработчик событий, добавленный ранее add_SourceChanged.
[add_HistoryChanged](#add_historychanged) | Счетовизменение сведений об прослушивать изменение истории переходов для документа верхнего уровня.
[remove_HistoryChanged](#remove_historychanged) | Удалите обработчик событий, добавленный ранее add_HistoryChanged.
[add_NavigationCompleted](#add_navigationcompleted) | Добавьте обработчик событий для события NavigationCompleted.
[remove_NavigationCompleted](#remove_navigationcompleted) | Удалите обработчик событий, добавленный ранее add_NavigationCompleted.
[add_FrameNavigationStarting](#add_framenavigationstarting) | Добавьте обработчик событий для события FrameNavigationStarting.
[remove_FrameNavigationStarting](#remove_framenavigationstarting) | Удалите обработчик событий, добавленный ранее add_FrameNavigationStarting.
[add_ScriptDialogOpening](#add_scriptdialogopening) | Добавьте обработчик событий для события ScriptDialogOpening.
[remove_ScriptDialogOpening](#remove_scriptdialogopening) | Удалите обработчик событий, добавленный ранее add_ScriptDialogOpening.
[add_PermissionRequested](#add_permissionrequested) | Добавьте обработчик событий для события PermissionRequested.
[remove_PermissionRequested](#remove_permissionrequested) | Удалите обработчик событий, добавленный ранее add_PermissionRequested.
[add_ProcessFailed](#add_processfailed) | Добавьте обработчик событий для события ProcessFailed.
[remove_ProcessFailed](#remove_processfailed) | Удалите обработчик событий, добавленный ранее add_ProcessFailed.
[AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated) | Добавьте предоставленный JavaScript в список сценариев, которые должны выполняться после создания глобального объекта, но до начала синтаксического анализа HTML-документа и перед выполнением любого другого сценария, включенного в документ HTML.
[RemoveScriptToExecuteOnDocumentCreated](#removescripttoexecuteondocumentcreated) | Удалите соответствующий сценарий JavaScript, добавленный через AddScriptToExecuteOnDocumentCreated.
[ExecuteScript](#executescript) | Выполнение кода JavaScript из параметра JavaScript в текущем документе верхнего уровня, отображаемом в WebView.
[CapturePreview](#capturepreview) | Запишите изображение того, что WebView на экране.
[Перезагрузить](#reload) | Перезагрузите текущую страницу.
[PostWebMessageAsJson](#postwebmessageasjson) | Опубликуйте указанное сообщение в документе верхнего уровня в этом WebView.
[PostWebMessageAsString](#postwebmessageasstring) | Это вспомогательный объект для отправки сообщения, которое является простой строкой, а не строкой JSON-представления объекта JavaScript.
[add_WebMessageReceived](#add_webmessagereceived) | Это событие срабатывает, если задан параметр IsWebMessageEnabled и документ верхнего уровня для вызовов WebView `window.chrome.webview.postMessage` .
[remove_WebMessageReceived](#remove_webmessagereceived) | Удалите обработчик событий, добавленный ранее add_WebMessageReceived.
[CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod) | Вызовите асинхронный метод DevToolsProtocol.
[get_BrowserProcessId](#get_browserprocessid) | Идентификатор процесса браузера, на котором размещается WebView.
[get_CanGoBack](#get_cangoback) | Возвращает значение "истина", если WebView может перейти к предыдущей странице в журнале переходов.
[get_CanGoForward](#get_cangoforward) | Возвращает значение "истина", если WebView может перейти к следующей странице в журнале переходов.
[GoBack](#goback) | Переход по WebView на предыдущую страницу в истории навигации.
[GoForward](#goforward) | Переход по WebView к следующей странице в истории навигации.
[GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver) | Получение приемника событий протокола DevTools, который позволяет подписаться на событие протокола DevTools.
[Stop](#stop) | Остановите все переходы и ожидающие выборки ресурсов.
[add_NewWindowRequested](#add_newwindowrequested) | Добавьте обработчик событий для события NewWindowRequested.
[remove_NewWindowRequested](#remove_newwindowrequested) | Удалите обработчик событий, добавленный ранее add_NewWindowRequested.
[add_DocumentTitleChanged](#add_documenttitlechanged) | Добавьте обработчик событий для события DocumentTitleChanged.
[remove_DocumentTitleChanged](#remove_documenttitlechanged) | Удалите обработчик событий, добавленный ранее add_DocumentTitleChanged.
[get_DocumentTitle](#get_documenttitle) | Название текущего документа верхнего уровня.
[AddRemoteObject](#addremoteobject) | Добавьте предоставленный объект узла в сценарий, выполняемый в WebView с указанным именем.
[RemoveRemoteObject](#removeremoteobject) | Удалите объект узла, заданный именем, чтобы он больше не будет доступен из кода JavaScript в WebView.
[OpenDevToolsWindow](#opendevtoolswindow) | Открытие окна DevTools для текущего документа в WebView.
[add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged) | Уведомляет об изменении свойства ContainsFullScreenElement.
[remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged) | Удалите обработчик событий, добавленный ранее с помощью соответствующего метода события add_.
[get_ContainsFullScreenElement](#get_containsfullscreenelement) | Указывает, содержит ли WebView элемент HTML на весь экран.
[add_WebResourceRequested](#add_webresourcerequested) | Добавьте обработчик событий для события WebResourceRequested.
[remove_WebResourceRequested](#remove_webresourcerequested) | Удалите обработчик событий, добавленный ранее add_WebResourceRequested.
[AddWebResourceRequestedFilter](#addwebresourcerequestedfilter) | Добавляет в событие WebResourceRequested код URI и фильтр контекста ресурсов.
[RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter) | Удаляет соответствующий фильтр веб-ресурсов, который ранее был добавлен для события WebResourceRequested.
[add_WindowCloseRequested](#add_windowcloserequested) | Добавьте обработчик событий для события WindowCloseRequested.
[remove_WindowCloseRequested](#remove_windowcloserequested) | Удалите обработчик событий, добавленный ранее add_WindowCloseRequested.
[CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#core_webview2_capture_preview_image_format) | Формат изображения, используемый в методе ICoreWebView2:: CapturePreview.
[CORE_WEBVIEW2_SCRIPT_DIALOG_KIND](#core_webview2_script_dialog_kind) | Диалоговое окно вида JavaScript, используемое в интерфейсе ICoreWebView2ScriptDialogOpeningEventHandler.
[CORE_WEBVIEW2_PROCESS_FAILED_KIND](#core_webview2_process_failed_kind) | Состояние сбоя процесса, используемого в интерфейсе ICoreWebView2ProcessFailedEventHandler.
[CORE_WEBVIEW2_PERMISSION_KIND](#core_webview2_permission_kind) | Тип запроса разрешения.
[CORE_WEBVIEW2_PERMISSION_STATE](#core_webview2_permission_state) | Ответ на запрос разрешения.
[CORE_WEBVIEW2_WEB_ERROR_STATUS](#core_webview2_web_error_status) | Значения состояния ошибки для переходов по веб-страницам.
[CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context) | Перечисление для контекстов запросов веб-ресурсов.

## События навигации

Обычной последовательностью событий навигации является NavigationStarting, SourceChanged, ContentLoading, а затем NavigationCompleted.

![dot-inline-dotgraph-1.png](media/dot-inline-dotgraph-1.png)

Обратите внимание, что это для событий навигации с одинаковым событием NavigationId arg. События навигации с различными аргументы события NavigationId могут перекрывать друг друга. Например, если вы запускаете навигацию для события NavigationStarting, а затем запускаете другую навигацию, вы увидите NavigationStarting для первой навигации, за которой следует NavigationStarting второй переход, а затем — NavigationCompleted для первого перехода, а затем все оставшиеся события навигации для второй навигации. В случае возникновения ошибок может возникнуть или не быть событием ContentLoading в зависимости от того, проявляется ли переход на страницу ошибки. В случае перенаправления HTTP в строке есть несколько событий NavigationStarting, для которых после первого будет задано значение параметра redirect.

Чтобы отслеживать или отменять навигацию внутри подкадров в WebView, используйте FrameNavigationStarting.

## Модель процесса

WebView2 использует ту же модель процессов, что и веб-браузер EDGE. В сеансе пользователя имеется один процесс браузера Edge для определенного каталога данных пользователя, который будет обрабатывать любой процесс вызова WebView2, указывающий на этот каталог данных пользователя. Это означает, что один процесс браузера Edge может обслуживать несколько процессов вызова и один процесс вызова может использовать несколько процессов браузера Edge.

![dot-inline-dotgraph-2.png](media/dot-inline-dotgraph-2.png)

В процессе работы с браузером может быть некоторое количество процессов обработки. Они создаются по мере необходимости для того, чтобы обслуживать потенциально несколько кадров в разных представлениях. Количество процессов обработки может различаться в зависимости от функции браузера "изоляция сайта" и количества отдельных отключенных относящихся к отсоединенным источникам, отображаемым в соответствующих веб-представлениях.

![dot-inline-dotgraph-3.png](media/dot-inline-dotgraph-3.png)

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

Откройте DevTools с помощью стандартных сочетаний клавиш: `F12` или `Ctrl+Shift+I` . Вы можете использовать `--auto-open-devtools-for-tabs` параметр аргумента Command, чтобы окно DevTools было открыто немедленно при первом создании WebView. Сведения о том, как предоставить дополнительные аргументы командной строки для процесса браузера, можно найти в документации CreateCoreWebView2Host. Изучите раздел реестра LoaderOverride для использования разных сборок WebView2 без изменения вашего приложения в документации CreateCoreWebView2Host.

## Управление версиями

После того как вы использовали определенную версию SDK для создания приложения, ваше приложение может завершить работу с более ранней или более поздней версией установленных двоичных файлов браузера. До версии 1.0.0.0 WebView2 на этапе обновления могут возрушиться изменения, которые не позволят пакету SDK работать с различными версиями установленных двоичных файлов браузера. После того как версия 1.0.0.0 может работать с различными версиями пакета SDK, следуйте приведенным ниже рекомендациям.

Для учета критических изменений в API убедитесь, что при вызове функции экспорта DLL CreateCoreWebView2Environment и при вызове QueryInterface для любого объекта CoreWebView2 возникла ошибка. Возвращаемое значение E_NOINTERFACE может указывать на то, что пакет SDK несовместим с двоичными файлами браузера Edge.

Проверка сбоя из QueryInterface также учитывает ситуации, в которых пакет SDK более новый, чем версия браузера EDGE, и ваше приложение пытается использовать интерфейс, на котором нет браузера Edge.

Если интерфейс недоступен, вы можете отключать связанный компонент, если это возможно, или иным образом информировать конечного пользователя о необходимости обновления браузера.

## Участников

#### get_Settings 

Объект ICoreWebView2Settings, содержащий различные изменяемые параметры для запущенного WebView.

> общедоступные значения HRESULT [get_Settings](#get_settings)(ICoreWebView2Settings * * параметры)

#### get_Source 

Универсальный код ресурса (URI) текущего документа верхнего уровня.

> общедоступные значения HRESULT [get_Source](#get_source)(LPWSTR * URI)

Это значение может изменяться в рамках обработки события SourceChanged в некоторых случаях, например при переходе к другому сайту или для навигации по фрагменту. Оно останется прежним для других типов переходов, таких как перегрузка страниц или History. pushState с тем же URL-адресом, что и у текущей страницы.

```cpp
    // Register a handler for the SourceChanged event.
    // This handler will read the webview's source URI and update
    // the app's address bar.
    CHECK_FAILURE(m_webView->add_SourceChanged(
        Callback<ICoreWebView2SourceChangedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2SourceChangedEventArgs* args)
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
        &m_sourceChangedToken));
```

#### Которому 

Применяет навигацию по документу верхнего уровня к указанному универсальному коду ресурса (URI).

> общедоступное значение HRESULT [навигации](#navigate)(URI LPCWSTR)

Дополнительные сведения приведены в разделе события навигации. Обратите внимание, что при этом начинается переход и соответствующее событие NavigationStarting будет срабатывать после завершения этого вызова навигации.

```cpp
void ControlComponent::NavigateToAddressBar()
{
    int length = GetWindowTextLength(m_toolbar->addressBarWindow);
    std::wstring uri(length, 0);
    PWSTR buffer = const_cast<PWSTR>(uri.data());
    GetWindowText(m_toolbar->addressBarWindow, buffer, length + 1);

    HRESULT hr = m_webView->Navigate(uri.c_str());
    if (hr == E_INVALIDARG)
    {
        // An invalid URI was provided.
        if (uri.find(L' ') == std::wstring::npos
            && uri.find(L'.') != std::wstring::npos)
        {
            // If it contains a dot and no spaces, try tacking http:// on the front.
            hr = m_webView->Navigate((L"http://" + uri).c_str());
        }
        else
        {
            // Otherwise treat it as a web search. We aren't bothering to escape
            // URL syntax characters such as & and #
            hr = m_webView->Navigate((L"https://bing.com/search?q=" + uri).c_str());
        }
    }
    if (hr != E_INVALIDARG) {
        CHECK_FAILURE(hr);
    }
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

> общедоступные значения HRESULT [add_NavigationStarting](#add_navigationstarting)([ICoreWebView2NavigationStartingEventHandler](ICoreWebView2NavigationStartingEventHandler.md) * eventHandler, EventRegistrationToken * token)

NavigationStarting активируется, когда основной кадр WebView запрашивает разрешение на переход на другой URI. Это будет срабатывать и для перенаправления.

```cpp
    // Register a handler for the NavigationStarting event.
    // This handler will check the domain being navigated to, and if the domain
    // matches a list of blocked sites, it will cancel the navigation and
    // possibly display a warning page.  It will also disable JavaScript on
    // selected websites.
    CHECK_FAILURE(m_webView->add_NavigationStarting(
        Callback<ICoreWebView2NavigationStartingEventHandler>(
            [this](ICoreWebView2* sender,
                   ICoreWebView2NavigationStartingEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Uri(&uri));

        if (ShouldBlockUri(uri.get()))
        {
            CHECK_FAILURE(args->put_Cancel(true));

            // If the user clicked a link to navigate, show a warning page.
            BOOL userInitiated;
            CHECK_FAILURE(args->get_IsUserInitiated(&userInitiated));
            static const PCWSTR htmlContent =
              L"<h1>Domain Blocked</h1>"
              L"<p>You've attempted to navigate to a domain in the blocked "
              L"sites list. Press back to return to the previous page.</p>";
            CHECK_FAILURE(sender->NavigateToString(htmlContent));
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

#### add_ContentLoading 

Добавьте обработчик событий для события ContentLoading.

> общедоступные значения HRESULT [add_ContentLoading](#add_contentloading)([ICoreWebView2ContentLoadingEventHandler](ICoreWebView2ContentLoadingEventHandler.md) * eventHandler, EventRegistrationToken * token)

ContentLoading срабатывает перед загрузкой содержимого, в том числе сценариев, добавленных с помощью AddScriptToExecuteOnDocumentCreated ContentLoading, не будет срабатывать при выполнении одной навигации по страницам (например, с помощью навигации фрагментов или журнала. pushState навигации). Это следует за событиями NavigationStarting и SourceChanged и предшествовать событиям HistoryChanged и NavigationCompleted.

#### remove_ContentLoading 

Удалите обработчик событий, добавленный ранее add_ContentLoading.

> общедоступные значения HRESULT [remove_ContentLoading](#remove_contentloading)(маркер EventRegistrationToken)

#### add_SourceChanged 

SourceChanged активируется при изменении свойства Source.

> общедоступные значения HRESULT [add_SourceChanged](#add_sourcechanged)([ICoreWebView2SourceChangedEventHandler](ICoreWebView2SourceChangedEventHandler.md) * eventHandler, EventRegistrationToken * token)

SourceChanged срабатывает для переходов на другой сайт или элементы навигации фрагментов. Она не будет срабатывать для других типов переходов, таких как перегрузка страниц или History. pushState с тем же URL-адресом, что и у текущей страницы. SourceChanged срабатывает перед ContentLoading для перехода к новому документу. Добавьте обработчик событий для события SourceChanged. 

```cpp
    // Register a handler for the SourceChanged event.
    // This handler will read the webview's source URI and update
    // the app's address bar.
    CHECK_FAILURE(m_webView->add_SourceChanged(
        Callback<ICoreWebView2SourceChangedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2SourceChangedEventArgs* args)
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
        &m_sourceChangedToken));
```

#### remove_SourceChanged 

Удалите обработчик событий, добавленный ранее add_SourceChanged.

> общедоступные значения HRESULT [remove_SourceChanged](#remove_sourcechanged)(маркер EventRegistrationToken)

#### add_HistoryChanged 

Счетовизменение сведений об прослушивать изменение истории переходов для документа верхнего уровня.

> общедоступные значения HRESULT [add_HistoryChanged](#add_historychanged)([ICoreWebView2HistoryChangedEventHandler](ICoreWebView2HistoryChangedEventHandler.md) * eventHandler, EventRegistrationToken * token)

Используйте Счетовизменение сведений об, чтобы проверить, изменилось ли get_CanGoBack/get_CanGoForward значения. HistoryChanged также срабатывает для использования GoBack и GoForward. HistoryChanged срабатывает после SourceChanged и ContentLoading. Добавьте обработчик событий для события HistoryChanged. 

```cpp
    // Register a handler for the HistoryChanged event.
    // Update the Back, Forward buttons.
    CHECK_FAILURE(m_webView->add_HistoryChanged(
        Callback<ICoreWebView2HistoryChangedEventHandler>(
            [this](ICoreWebView2* sender, IUnknown* args) -> HRESULT {
                BOOL canGoBack;
                BOOL canGoForward;
                sender->get_CanGoBack(&canGoBack);
                sender->get_CanGoForward(&canGoForward);
                EnableWindow(m_toolbar->backWindow, canGoBack);
                EnableWindow(m_toolbar->forwardWindow, canGoForward);

                return S_OK;
            })
            .Get(),
        &m_historyChangedToken));
```

#### remove_HistoryChanged 

Удалите обработчик событий, добавленный ранее add_HistoryChanged.

> общедоступные значения HRESULT [remove_HistoryChanged](#remove_historychanged)(маркер EventRegistrationToken)

#### add_NavigationCompleted 

Добавьте обработчик событий для события NavigationCompleted.

> общедоступные значения HRESULT [add_NavigationCompleted](#add_navigationcompleted)([ICoreWebView2NavigationCompletedEventHandler](ICoreWebView2NavigationCompletedEventHandler.md) * eventHandler, EventRegistrationToken * token)

Событие NavigationCompleted активируется, когда WebView полностью загружен (Body. onload) или загрузка остановлена с ошибкой.

```cpp
    // Register a handler for the NavigationCompleted event.
    // Check whether the navigation succeeded, and if not, do something.
    // Also update the Cancel buttons.
    CHECK_FAILURE(m_webView->add_NavigationCompleted(
        Callback<ICoreWebView2NavigationCompletedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2NavigationCompletedEventArgs* args)
                -> HRESULT {
                BOOL success;
                CHECK_FAILURE(args->get_IsSuccess(&success));
                if (!success)
                {
                    CORE_WEBVIEW2_WEB_ERROR_STATUS webErrorStatus;
                    CHECK_FAILURE(args->get_WebErrorStatus(&webErrorStatus));
                    if (webErrorStatus == CORE_WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED)
                    {
                        // Do something here if you want to handle a specific error case.
                        // In most cases this isn't necessary, because the WebView will
                        // display its own error page automatically.
                    }
                }
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

> общедоступные значения HRESULT [add_FrameNavigationStarting](#add_framenavigationstarting)([ICoreWebView2NavigationStartingEventHandler](ICoreWebView2NavigationStartingEventHandler.md) * eventHandler, EventRegistrationToken * token)

FrameNavigationStarting активируется, когда дочерний кадр в WebView, запрашивающий разрешение на переход к другому URI. Это будет срабатывать и для перенаправления.

```cpp
    // Register a handler for the FrameNavigationStarting event.
    // This handler will prevent a frame from navigating to a blocked domain.
    CHECK_FAILURE(m_webView->add_FrameNavigationStarting(
        Callback<ICoreWebView2NavigationStartingEventHandler>(
            [this](ICoreWebView2* sender,
                   ICoreWebView2NavigationStartingEventArgs* args) -> HRESULT
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

#### add_ScriptDialogOpening 

Добавьте обработчик событий для события ScriptDialogOpening.

> общедоступные значения HRESULT [add_ScriptDialogOpening](#add_scriptdialogopening)([ICoreWebView2ScriptDialogOpeningEventHandler](ICoreWebView2ScriptDialogOpeningEventHandler.md) * eventHandler, EventRegistrationToken * token)

Событие активируется, когда диалоговое окно JavaScript (предупреждение, подтверждение или запрос) будет отображаться для WebView. Это событие срабатывает только в том случае, если свойству ICoreWebView2Settings:: AreDefaultScriptDialogsEnabled задано значение false. Событие ScriptDialogOpening можно использовать, чтобы подавить диалоговые окна или заменить диалоговые окна по умолчанию пользовательскими диалоговыми окноми.

```cpp
    // Register a handler for the ScriptDialogOpening event.
    // This handler will set up a custom prompt dialog for the user,
    // and may defer the event if the setting to defer dialogs is enabled.
    CHECK_FAILURE(m_webView->add_ScriptDialogOpening(
        Callback<ICoreWebView2ScriptDialogOpeningEventHandler>(
            [this](
                ICoreWebView2* sender,
                ICoreWebView2ScriptDialogOpeningEventArgs* args) -> HRESULT
    {
        wil::com_ptr<ICoreWebView2ScriptDialogOpeningEventArgs> eventArgs = args;
        auto showDialog = [this, eventArgs]
        {
            wil::unique_cotaskmem_string uri;
            CORE_WEBVIEW2_SCRIPT_DIALOG_KIND type;
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
                /* readonly */ type != CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT);
            if (dialog.confirmed)
            {
                CHECK_FAILURE(eventArgs->put_ResultText(dialog.input.c_str()));
                CHECK_FAILURE(eventArgs->Accept());
            }
        };

        if (m_deferScriptDialogs)
        {
            wil::com_ptr<ICoreWebView2Deferral> deferral;
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

#### add_PermissionRequested 

Добавьте обработчик событий для события PermissionRequested.

> общедоступные значения HRESULT [add_PermissionRequested](#add_permissionrequested)([ICoreWebView2PermissionRequestedEventHandler](ICoreWebView2PermissionRequestedEventHandler.md) * eventHandler, EventRegistrationToken * token)

Вызывается, когда содержимое в WebView запрашивает разрешение на доступ к некоторым привилегированным ресурсам.

```cpp
    // Register a handler for the PermissionRequested event.
    // This handler prompts the user to allow or deny the request.
    CHECK_FAILURE(m_webView->add_PermissionRequested(
        Callback<ICoreWebView2PermissionRequestedEventHandler>(
            [this](
                ICoreWebView2* sender,
                ICoreWebView2PermissionRequestedEventArgs* args) -> HRESULT
    {
        wil::unique_cotaskmem_string uri;
        CORE_WEBVIEW2_PERMISSION_KIND kind = CORE_WEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION;
        BOOL userInitiated = FALSE;

        CHECK_FAILURE(args->get_Uri(&uri));
        CHECK_FAILURE(args->get_PermissionKind(&kind));
        CHECK_FAILURE(args->get_IsUserInitiated(&userInitiated));

        std::wstring message = L"Do you want to grant permission for ";
        message += NameOfPermissionKind(kind);
        message += L" to the website at ";
        message += uri.get();
        message += L"?\n\n";
        message += (userInitiated
            ? L"This request came from a user gesture."
            : L"This request did not come from a user gesture.");

        int response = MessageBox(nullptr, message.c_str(), L"Permission Request",
                                   MB_YESNOCANCEL | MB_ICONWARNING);

        CORE_WEBVIEW2_PERMISSION_STATE state =
              response == IDYES ? CORE_WEBVIEW2_PERMISSION_STATE_ALLOW
            : response == IDNO  ? CORE_WEBVIEW2_PERMISSION_STATE_DENY
            :                     CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT;
        CHECK_FAILURE(args->put_State(state));

        return S_OK;
    }).Get(), &m_permissionRequestedToken));
```

#### remove_PermissionRequested 

Удалите обработчик событий, добавленный ранее add_PermissionRequested.

> общедоступные значения HRESULT [remove_PermissionRequested](#remove_permissionrequested)(маркер EventRegistrationToken)

#### add_ProcessFailed 

Добавьте обработчик событий для события ProcessFailed.

> общедоступные значения HRESULT [add_ProcessFailed](#add_processfailed)([ICoreWebView2ProcessFailedEventHandler](ICoreWebView2ProcessFailedEventHandler.md) * eventHandler, EventRegistrationToken * token)

Активируется, когда WebView процесс неожиданно завершился или перестал отвечать на запросы.

```cpp
    // Register a handler for the ProcessFailed event.
    // This handler checks if the browser process failed, and asks the user if
    // they want to recreate the webview.
    CHECK_FAILURE(m_webView->add_ProcessFailed(
        Callback<ICoreWebView2ProcessFailedEventHandler>(
            [this](ICoreWebView2* sender,
                ICoreWebView2ProcessFailedEventArgs* args) -> HRESULT
    {
        CORE_WEBVIEW2_PROCESS_FAILED_KIND failureType;
        CHECK_FAILURE(args->get_ProcessFailedKind(&failureType));
        if (failureType == CORE_WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED)
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
        else if (failureType == CORE_WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE)
        {
            int button = MessageBox(
                m_appWindow->GetMainWindow(),
                L"Browser render process has stopped responding.  Recreate webview?",
                L"Web page unresponsive", MB_YESNO);
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

> общедоступные значения HRESULT [AddScriptToExecuteOnDocumentCreated](#addscripttoexecuteondocumentcreated)(LPCWSTR JavaScript,[ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler](ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler.md) * обработчик)

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
            Callback<ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler>(
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

> общедоступные значения HRESULT [ExecuteScript](#executescript)(LPCWSTR JavaScript,[ICoreWebView2ExecuteScriptCompletedHandler](ICoreWebView2ExecuteScriptCompletedHandler.md) * обработчик)

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
            Callback<ICoreWebView2ExecuteScriptCompletedHandler>(
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

> Public HRESULT [CapturePreview](#capturepreview)([CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#core_webview2_capture_preview_image_format) ImageFormat, IStream * ImageStream,[ICoreWebView2CapturePreviewCompletedHandler](ICoreWebView2CapturePreviewCompletedHandler.md) * обработчик)

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
            CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG, stream.get(),
            Callback<ICoreWebView2CapturePreviewCompletedHandler>(
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

#### PostWebMessageAsJson 

Опубликуйте указанное сообщение в документе верхнего уровня в этом WebView.

> общедоступные значения HRESULT [PostWebMessageAsJson](#postwebmessageasjson)(LPCWSTR webMessageAsJson)

Срабатывает событие Window. Chrome. WebView для документа верхнего уровня. JavaScript в этом документе может подписываться на событие и отменять подписку с помощью следующих действий: 

```cpp
window.chrome.webview.addEventListener('message', handler)
window.chrome.webview.removeEventListener('message', handler)
```

 Аргументы события представляют собой экземпляр `MessageEvent` . Параметр ICoreWebView2Settings:: IsWebMessageEnabled должен быть истинным, или этот метод завершится сбоем с E_INVALIDARG. Свойство данных аргумента "событие" — это строковый параметр веб-сообщения, проанализированный как строка JSON, в объект JavaScript. Свойство Source аргумента "событие" является ссылкой на `window.chrome.webview` объект. Сведения о том, как отправлять сообщения из HTML-документа на WebView на узел, можно найти в SetWebMessageReceivedEventHandler. Это сообщение отправляется асинхронно. Если переход выполняется до того, как сообщение будет отправлено на страницу, оно не будет отправлено.

```cpp
    // Setup the web message received event handler before navigating to
    // ensure we don't miss any messages.
    CHECK_FAILURE(m_webView->add_WebMessageReceived(
        Microsoft::WRL::Callback<ICoreWebView2WebMessageReceivedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2WebMessageReceivedEventArgs* args)
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Source(&uri));

        // Always validate that the origin of the message is what you expect.
        if (uri.get() != m_sampleUri)
        {
            return S_OK;
        }
        wil::unique_cotaskmem_string messageRaw;
        CHECK_FAILURE(args->TryGetWebMessageAsString(&messageRaw));
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

> общедоступные значения HRESULT [add_WebMessageReceived](#add_webmessagereceived)(обработчик[ICoreWebView2WebMessageReceivedEventHandler](ICoreWebView2WebMessageReceivedEventHandler.md) *, EventRegistrationToken * token)

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

 При вызове [ICoreWebView2WebMessageReceivedEventHandler](ICoreWebView2WebMessageReceivedEventHandler.md) набор с помощью этого метода SetWebMessageReceivedEventHandler вызывается с помощью параметра объекта i, преобразованного в строку JSON.

```cpp
    // Setup the web message received event handler before navigating to
    // ensure we don't miss any messages.
    CHECK_FAILURE(m_webView->add_WebMessageReceived(
        Microsoft::WRL::Callback<ICoreWebView2WebMessageReceivedEventHandler>(
            [this](ICoreWebView2* sender, ICoreWebView2WebMessageReceivedEventArgs* args)
    {
        wil::unique_cotaskmem_string uri;
        CHECK_FAILURE(args->get_Source(&uri));

        // Always validate that the origin of the message is what you expect.
        if (uri.get() != m_sampleUri)
        {
            return S_OK;
        }
        wil::unique_cotaskmem_string messageRaw;
        CHECK_FAILURE(args->TryGetWebMessageAsString(&messageRaw));
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

#### CallDevToolsProtocolMethod 

Вызовите асинхронный метод DevToolsProtocol.

> общедоступные значения HRESULT [CallDevToolsProtocolMethod](#calldevtoolsprotocolmethod)(LPCWSTR METHODNAME, LPCWSTR ParametersAsJson,[ICoreWebView2CallDevToolsProtocolMethodCompletedHandler](ICoreWebView2CallDevToolsProtocolMethodCompletedHandler.md) * handler)

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
            Callback<ICoreWebView2CallDevToolsProtocolMethodCompletedHandler>(
                [](HRESULT error, PCWSTR resultJson) -> HRESULT
                {
                    MessageBox(nullptr, resultJson, L"CDP Method Result", MB_OK);
                    return S_OK;
                }).Get());
    }
}
```

#### get_BrowserProcessId 

Идентификатор процесса браузера, на котором размещается WebView.

> общедоступные значения HRESULT [get_BrowserProcessId](#get_browserprocessid)(UINT32 * Value)

#### get_CanGoBack 

Возвращает значение "истина", если WebView может перейти к предыдущей странице в журнале переходов.

> общедоступные значения HRESULT [get_CanGoBack](#get_cangoback)(bool * CanGoBack)

Событие HistoryChanged будет срабатывать, если get_CanGoBack изменит значение.

#### get_CanGoForward 

Возвращает значение "истина", если WebView может перейти к следующей странице в журнале переходов.

> общедоступные значения HRESULT [get_CanGoForward](#get_cangoforward)(bool * CanGoForward)

Событие HistoryChanged будет срабатывать, если get_CanGoForward изменит значение.

#### GoBack 

Переход по WebView на предыдущую страницу в истории навигации.

> общедоступное значение HRESULT [GoBack](#goback)()

#### GoForward 

Переход по WebView к следующей странице в истории навигации.

> общедоступные значения HRESULT [GoForward](#goforward)()

#### GetDevToolsProtocolEventReceiver 

Получение приемника событий протокола DevTools, который позволяет подписаться на событие протокола DevTools.

> общедоступные значения HRESULT [GetDevToolsProtocolEventReceiver](#getdevtoolsprotocoleventreceiver)(LPCWSTR eventName,[ICoreWebView2DevToolsProtocolEventReceiver](ICoreWebView2DevToolsProtocolEventReceiver.md) * * ресивер)

Параметр eventName — это полное имя события в формате `{domain}.{event}` . Список событий протоколов DevTools и аргументов событий можно найти в [средстве просмотра протокола DevTools](https://aka.ms/DevToolsProtocolDocs) .

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
        wil::com_ptr<ICoreWebView2DevToolsProtocolEventReceiver> receiver;
        CHECK_FAILURE(
            m_webView->GetDevToolsProtocolEventReceiver(eventName.c_str(), &receiver));

        // If we are already subscribed to this event, unsubscribe first.
        auto preexistingToken = m_devToolsProtocolEventReceivedTokenMap.find(eventName);
        if (preexistingToken != m_devToolsProtocolEventReceivedTokenMap.end())
        {
            CHECK_FAILURE(receiver->remove_DevToolsProtocolEventReceived(
                preexistingToken->second));
        }

        CHECK_FAILURE(receiver->add_DevToolsProtocolEventReceived(
            Callback<ICoreWebView2DevToolsProtocolEventReceivedEventHandler>(
                [eventName](
                    ICoreWebView2* sender,
                    ICoreWebView2DevToolsProtocolEventReceivedEventArgs* args) -> HRESULT {
                    wil::unique_cotaskmem_string parameterObjectAsJson;
                    CHECK_FAILURE(args->get_ParameterObjectAsJson(&parameterObjectAsJson));
                    MessageBox(
                        nullptr, parameterObjectAsJson.get(),
                        (L"CDP Event Fired: " + eventName).c_str(), MB_OK);
                    return S_OK;
                })
                .Get(),
            &m_devToolsProtocolEventReceivedTokenMap[eventName]));
    }
}
```

#### Stop 

Остановите все переходы и ожидающие выборки ресурсов.

> открытая [Остановка](#stop)HRESULT ()

Не останавливает сценарии.

#### add_NewWindowRequested 

Добавьте обработчик событий для события NewWindowRequested.

> общедоступные значения HRESULT [add_NewWindowRequested](#add_newwindowrequested)([ICoreWebView2NewWindowRequestedEventHandler](ICoreWebView2NewWindowRequestedEventHandler.md) * eventHandler, EventRegistrationToken * token)

Вызывается, когда содержимое в WebView запросило открыть новое окно, например с помощью Window. Open. Приложение может передавать целевую WebView, которая будет считаться открытым окном.

```cpp
    // Register a handler for the NewWindowRequested event.
    // This handler will defer the event, create a new app window, and then once the
    // new window is ready, it'll provide that new window's WebView as the response to
    // the request.
    CHECK_FAILURE(m_webView->add_NewWindowRequested(
        Callback<ICoreWebView2NewWindowRequestedEventHandler>(
            [this](
                ICoreWebView2* sender,
                ICoreWebView2NewWindowRequestedEventArgs* args) {
                wil::com_ptr<ICoreWebView2Deferral> deferral;
                CHECK_FAILURE(args->GetDeferral(&deferral));

                auto newAppWindow = new AppWindow(L"");
                newAppWindow->m_isPopupWindow = true;
                newAppWindow->m_onWebViewFirstInitialized = [args, deferral, newAppWindow]() {
                    CHECK_FAILURE(args->put_NewWindow(newAppWindow->m_webView.get()));
                    CHECK_FAILURE(args->put_Handled(TRUE));
                    CHECK_FAILURE(deferral->Complete());
                };

                return S_OK;
            })
            .Get(),
        nullptr));
```

#### remove_NewWindowRequested 

Удалите обработчик событий, добавленный ранее add_NewWindowRequested.

> общедоступные значения HRESULT [remove_NewWindowRequested](#remove_newwindowrequested)(маркер EventRegistrationToken)

#### add_DocumentTitleChanged 

Добавьте обработчик событий для события DocumentTitleChanged.

> общедоступные значения HRESULT [add_DocumentTitleChanged](#add_documenttitlechanged)([ICoreWebView2DocumentTitleChangedEventHandler](ICoreWebView2DocumentTitleChangedEventHandler.md) * eventHandler, EventRegistrationToken * token)

Событие активируется, когда свойство DocumentTitle объекта WebView изменяется и может срабатывать до или после события NavigationCompleted.

```cpp
    // Register a handler for the DocumentTitleChanged event.
    // This handler just announces the new title on the window's title bar.
    CHECK_FAILURE(m_webView->add_DocumentTitleChanged(
        Callback<ICoreWebView2DocumentTitleChangedEventHandler>(
            [this](ICoreWebView2* sender, IUnknown* args) -> HRESULT {
                wil::unique_cotaskmem_string title;
                CHECK_FAILURE(sender->get_DocumentTitle(&title));
                SetWindowText(m_appWindow->GetMainWindow(), title.get());
                return S_OK;
            })
            .Get(),
        &m_documentTitleChangedToken));
```

#### remove_DocumentTitleChanged 

Удалите обработчик событий, добавленный ранее add_DocumentTitleChanged.

> общедоступные значения HRESULT [remove_DocumentTitleChanged](#remove_documenttitlechanged)(маркер EventRegistrationToken)

#### get_DocumentTitle 

Название текущего документа верхнего уровня.

> общедоступные значения HRESULT [get_DocumentTitle](#get_documenttitle)(LPWSTR * Title)

Если документ не имеет явного заголовка или не является пустым, используется значение по умолчанию, которое может быть или не совпадать с URI документа.

#### AddRemoteObject 

Добавьте предоставленный объект узла в сценарий, выполняемый в WebView с указанным именем.

> общедоступные значения HRESULT [AddRemoteObject](#addremoteobject)(имя LPCWSTR, переменная * объект)

Объекты узла предоставляются как прокси удаленных объектов через `window.chrome.webview.remoteObjects.<name>` . Удаленные прокси-объекты являются обещанными и разрешаются в объект, представляющий объект Host. Обещание отклонено, если приложение не добавило объект с именем. Когда код JavaScript обращается к свойству или методу объекта, для него возвращается значение, которое будет обрабатываться в соответствии со значением, возвращенным из хоста для свойства или метода, или отброшено в случае ошибки, например, отсутствие такого свойства или метода для объекта или параметров недопустимым. Например, когда код приложения делает следующее: 

```cpp
VARIANT object;
object.vt = VT_DISPATCH;
object.pdispVal = appObject;
webview->AddRemoteObject(L"host_object", &host);
```

 Код JavaScript в WebView сможет получить доступ к appObject следующим образом, а затем получить доступ к атрибутам и методам appObject: 

```js
let app_object = await window.chrome.webview.remoteObjects.host_object;
let attr1 = await app_object.attr1;
let result = await app_object.method1(parameters);
```

 Обратите внимание, что хотя простые типы, IDispatch и Array поддерживаются, универсальный IUnknown, VT_DECIMAL или VT_RECORD Variant не поддерживается. Удаленные объекты JavaScript, такие как функции обратного вызова, представлены как VT_DISPATCH VARIANT с помощью объекта, реализующего IDispatch. Метод обратного вызова JavaScript можно вызвать с помощью DISPID_VALUE для DISPID. Вложенные массивы поддерживаются до 3 уровней. Массивы по типам ссылок не поддерживаются. VT_EMPTY и VT_NULL сопоставлены в JavaScript как null. В JavaScript NULL и undefine сопоставляются с VT_EMPTY.

Кроме того, все удаленные объекты представляются как `window.chrome.webview.remoteObjects.sync.<name>` . Здесь объекты узла предоставляются как синхронные удаленные прокси-объекты. Эти функции не предназначены для того, чтобы синхронно блокировать выполняемые сценарии, ожидающие общения для запуска кода хоста. Таким образом, это может привести к проблемам с надежностью, поэтому рекомендуется использовать асинхронный API на основе Promise, `window.chrome.webview.remoteObjects.<name>` описанный выше.

Синхронные удаленные прокси-объекты и асинхронные удаленные прокси-объекты могут одновременно выполнять прокси для одного и того же удаленного объекта. Удаленные изменения, внесенные одним прокси-сервером, будут отражаться в любом другом прокси того же удаленного объекта, независимо от того, являются ли они другими прокси-объектами, синхронными или асинхронными.

Несмотря на то, что JavaScript блокируется на синхронный вызов машинного кода, этот машинный код не может снова вызвать JavaScript. При попытке выполнить это действие произойдет сбой с HRESULT_FROM_WIN32 (ERROR_POSSIBLE_DEADLOCK).

Удаленные прокси-объекты — это прокси JavaScript, который перехватывает все вызовы свойств Get, Set и Method. Свойства или методы, которые являются частью прототипа функции или объекта, выполняются локально. Кроме того, любое свойство или метод в массиве `chrome.webview.remoteObjects.options.forceLocalProperties` также будет выполняться локально. Эти значения по умолчанию включают в себя дополнительные методы, которые имеют значение в JavaScript Like `toJSON` и `Symbol.toPrimitive` . При необходимости вы можете добавить в этот массив дополнительные сведения.

Существует метод `chrome.webview.remoteObjects.cleanupSome` , который лучше всего подходит для сборщиков мусора удаленных объектов.

Удаленные прокси-объекты также обладают следующими методами, которые выполняются локально.

* applyRemote,-Remote, setRemote: выполняет вызов метода, свойство get или набор свойств для удаленного объекта. Вы можете использовать их, чтобы явным образом запускать метод или свойство, если существует конфликтующий локальный метод или свойство. Например, `proxy.toString()` будет выполнен локальный метод ToString для прокси-объекта. Но `proxy.applyRemote('toString')` выполняется `toString` на удаленном прокси-объекте.

* "по локальной, setLocal" — выполнение свойства Get или установка свойства локально. Эти методы можно использовать, чтобы принудительно получить или задать свойство в самом удаленном прокси-объекте, а не на удаленном объекте, который он представляет. Например, `proxy.unknownProperty` будет получено свойство с именем `unknownProperty` из удаленного прокси-объекта. Но `proxy.getLocal('unknownProperty')` будет получить значение свойства `unknownProperty` для самого объекта прокси.

* Синхронизация: асинхронные удаленные прокси-объекты предоставляют метод синхронизации, возвращающий обещание для синхронного удаленного объектного прокси для того же удаленного объекта. Например, `chrome.webview.remoteObjects.sample.methodCall()` возвращает асинхронный удаленный прокси-объект. Вы можете использовать этот `sync` метод, чтобы получить для него синхронный удаленный прокси-объект. `const syncProxy = await chrome.webview.remoteObjects.sample.methodCall().sync()`

* Async: синхронные удаленные прокси-объекты предоставляют метод async, который блокирует и возвращает асинхронный удаленный прокси-объект для того же удаленного объекта. Например, `chrome.webview.remoteObjects.sync.sample.methodCall()` возвращает синхронный удаленный прокси-объект. При вызове `async` метода на этих блоках возвращается асинхронный удаленный прокси-объект для того же удаленного объекта: `const asyncProxy = chrome.webview.remoteObjects.sync.sample.methodCall().async()`

* затем: асинхронные удаленные прокси-объекты имеют метод then. Это позволит им доставлять ожидающие. `then` Возвращает обещание, которое разрешается с представлением удаленного объекта. Если прокси представляет литерал JavaScript, то копия, возвращаемая им, будет возвращена локально. Если прокси представляет функцию, возвращается прокси-сервер, не ожидающий ожидания. Если прокси представляет объект JavaScript с сочетанием литеральных свойств и свойств функций, то копия объекта возвращается с некоторыми свойствами в качестве удаленных прокси-объектов.

Все другие вызовы свойств и методов (Кроме описанных выше методов прокси-сервера удаленного объекта, списка forceLocalProperties и свойств прототипов функций и объектов) выполняются удаленно. Асинхронные удаленные прокси-объекты возвращают обещание, представляющее собой асинхронное завершение удаленного вызова метода или получение свойства. Обещание устраняется после завершения удаленных операций, и обещание разрешается в полученное значение операции. Синхронные удаленные прокси-объекты работают точно так же, но блокируют выполнение JavaScript и дождитесь завершения удаленной операции.

Установка свойства для прокси-сервера асинхронного удаленного объекта немного не изменилась. Функция Set возвращает значение немедленно и возвращаемое значение является значением, которое будет задано. Это требование для прокси-объекта JavaScript. Если необходимо асинхронно дождаться завершения установки свойства, используйте метод setRemote, который возвращает обещание, как описано выше. Синхронно заданное свойство свойства объекта для синхронно блокируется, пока не задано свойство.

Например, предположим, что у вас есть COM-объект со следующим интерфейсом

```IDL
    [uuid(3a14c9c0-bc3e-453f-a314-4ce4a0ec81d8), object, local]
    interface IRemoteObjectSample : IUnknown
    {
        // Demonstrate basic method call with some parameters and a return value.
        HRESULT MethodWithParametersAndReturnValue([in] BSTR stringParameter, [in] INT integerParameter, [out, retval] BSTR* stringResult);

        // Demonstrate getting and setting a property.
        [propget] HRESULT Property([out, retval] BSTR* stringResult);
        [propput] HRESULT Property([in] BSTR stringValue);

        // Demonstrate native calling back into JavaScript.
        HRESULT CallCallbackAsynchronously([in] IDispatch* callbackParameter);
    };
```

 Мы можем добавить экземпляр этого интерфейса в наш сценарий JavaScript `AddRemoteObject` . В этом случае мы присвойте ему имя `sample` :

```cpp
            VARIANT remoteObjectAsVariant = {};
            m_remoteObject.query_to<IDispatch>(&remoteObjectAsVariant.pdispVal);
            remoteObjectAsVariant.vt = VT_DISPATCH;

            // We can call AddRemoteObject multiple times in a row without
            // calling RemoveRemoteObject first. This will replace the previous object
            // with the new object. In our case this is the same object and everything
            // is fine.
            CHECK_FAILURE(m_webView->AddRemoteObject(L"sample", &remoteObjectAsVariant));
            remoteObjectAsVariant.pdispVal->Release();
```

 Затем в HTML-документе мы можем использовать этот COM-объект через `chrome.webview.remoteObjects.sample` :

```js
        document.getElementById("getPropertyAsyncButton").addEventListener("click", async () => {
            const propertyValue = await chrome.webview.remoteObjects.sample.property;
            document.getElementById("getPropertyAsyncOutput").textContent = propertyValue;
        });

        document.getElementById("getPropertySyncButton").addEventListener("click", () => {
            const propertyValue = chrome.webview.remoteObjects.sync.sample.property;
            document.getElementById("getPropertySyncOutput").textContent = propertyValue;
        });

        document.getElementById("setPropertyAsyncButton").addEventListener("click", async () => {
            const propertyValue = document.getElementById("setPropertyAsyncInput").value;
            // The following line will work but it will return immediately before the property value has actually been set.
            // If you need to set the property and wait for the property to change value, use the setRemote function.
            chrome.webview.remoteObjects.sample.property = propertyValue;
            document.getElementById("setPropertyAsyncOutput").textContent = "Set";
        });

        document.getElementById("setPropertyExplicitAsyncButton").addEventListener("click", async () => {
            const propertyValue = document.getElementById("setPropertyExplicitAsyncInput").value;
            // If you care about waiting until the property has actually changed value use the setRemote function.
            await chrome.webview.remoteObjects.sample.setRemote("property", propertyValue);
            document.getElementById("setPropertyExplicitAsyncOutput").textContent = "Set";
        });

        document.getElementById("setPropertySyncButton").addEventListener("click", () => {
            const propertyValue = document.getElementById("setPropertySyncInput").value;
            chrome.webview.remoteObjects.sync.sample.property = propertyValue;
            document.getElementById("setPropertySyncOutput").textContent = "Set";
        });

        document.getElementById("invokeMethodAsyncButton").addEventListener("click", async () => {
            const paramValue1 = document.getElementById("invokeMethodAsyncParam1").value;
            const paramValue2 = parseInt(document.getElementById("invokeMethodAsyncParam2").value);
            const resultValue = await chrome.webview.remoteObjects.sample.MethodWithParametersAndReturnValue(paramValue1, paramValue2);
            document.getElementById("invokeMethodAsyncOutput").textContent = resultValue;
        });

        document.getElementById("invokeMethodSyncButton").addEventListener("click", () => {
            const paramValue1 = document.getElementById("invokeMethodSyncParam1").value;
            const paramValue2 = parseInt(document.getElementById("invokeMethodSyncParam2").value);
            const resultValue = chrome.webview.remoteObjects.sync.sample.MethodWithParametersAndReturnValue(paramValue1, paramValue2);
            document.getElementById("invokeMethodSyncOutput").textContent = resultValue;
        });

        let callbackCount = 0;
        document.getElementById("invokeCallbackButton").addEventListener("click", async () => {
            chrome.webview.remoteObjects.sample.CallCallbackAsynchronously(() => {
                document.getElementById("invokeCallbackOutput").textContent = "Native object called the callback " + (++callbackCount) + " time(s).";
            });
        });
```

#### RemoveRemoteObject 

Удалите объект узла, заданный именем, чтобы он больше не будет доступен из кода JavaScript в WebView.

> общедоступное значение HRESULT [RemoveRemoteObject](#removeremoteobject)(имя LPCWSTR)

Несмотря на то что новые попытки доступа будут отвергнуты, если объект уже получен кодом JavaScript в WebView, код JavaScript продолжит получать доступ к этому объекту. Вызов этого метода для имени, которое уже удалено или не было добавлено, завершается сбоем.

#### OpenDevToolsWindow 

Открытие окна DevTools для текущего документа в WebView.

> общедоступные значения HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()

Ничего не происходит, если он вызывается, когда окно DevTools уже открыто

#### add_ContainsFullScreenElementChanged 

Уведомляет об изменении свойства ContainsFullScreenElement.

> общедоступные значения HRESULT [add_ContainsFullScreenElementChanged](#add_containsfullscreenelementchanged)([ICoreWebView2ContainsFullScreenElementChangedEventHandler](ICoreWebView2ContainsFullScreenElementChangedEventHandler.md) * eventHandler, EventRegistrationToken * token)

Это означает, что HTML-элемент, находящиеся внутри WebView, помещается на размер WebView или выходит за экран. Это событие полезно, если, например, элемент видео запрашивается на весь экран. Прослушиватель ContainsFullScreenElementChanged может затем изменить размер WebView в ответе.

```cpp
    // Register a handler for the ContainsFullScreenChanged event.
    CHECK_FAILURE(m_webView->add_ContainsFullScreenElementChanged(
        Callback<ICoreWebView2ContainsFullScreenElementChangedEventHandler>(
            [this](ICoreWebView2* sender, IUnknown* args) -> HRESULT {
                if (m_fullScreenAllowed)
                {
                    CHECK_FAILURE(
                        sender->get_ContainsFullScreenElement(&m_containsFullscreenElement));
                    if (m_containsFullscreenElement)
                    {
                        EnterFullScreen();
                    }
                    else
                    {
                        ExitFullScreen();
                    }
                }
                return S_OK;
            })
            .Get(),
        nullptr));
```

#### remove_ContainsFullScreenElementChanged 

Удалите обработчик событий, добавленный ранее с помощью соответствующего метода события add_.

> общедоступные значения HRESULT [remove_ContainsFullScreenElementChanged](#remove_containsfullscreenelementchanged)(маркер EventRegistrationToken)

#### get_ContainsFullScreenElement 

Указывает, содержит ли WebView элемент HTML на весь экран.

> общедоступные значения HRESULT [get_ContainsFullScreenElement](#get_containsfullscreenelement)(bool * ContainsFullScreenElement)

#### add_WebResourceRequested 

Добавьте обработчик событий для события WebResourceRequested.

> общедоступные значения HRESULT [add_WebResourceRequested](#add_webresourcerequested)([ICoreWebView2WebResourceRequestedEventHandler](ICoreWebView2WebResourceRequestedEventHandler.md) * eventHandler, EventRegistrationToken * token)

Активируется, когда WebView выполняет запрос HTTP к соответствующему URL-адресу и фильтру контекста ресурсов, добавленному с помощью AddWebResourceRequestedFilter. Для срабатывания события необходимо добавить хотя бы один фильтр.

```cpp
        if (m_blockImages)
        {
            m_webView->AddWebResourceRequestedFilter(L"*", CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE);
            CHECK_FAILURE(m_webView->add_WebResourceRequested(
                Callback<ICoreWebView2WebResourceRequestedEventHandler>(
                    [this](
                        ICoreWebView2* sender,
                        ICoreWebView2WebResourceRequestedEventArgs* args) {
                        CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT resourceContext;
                        CHECK_FAILURE(
                            args->get_ResourceContext(&resourceContext));
                        // Ensure that the type is image
                        if (resourceContext != CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE)
                        {
                            return E_INVALIDARG;
                        }
                        // Override the response with an empty one to block the image.
                        // If put_Response is not called, the request will continue as normal.
                        wil::com_ptr<ICoreWebView2WebResourceResponse> response;
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

#### AddWebResourceRequestedFilter 

Добавляет в событие WebResourceRequested код URI и фильтр контекста ресурсов.

> общедоступный HRESULT [AddWebResourceRequestedFilter](#addwebresourcerequestedfilter)(LPCWSTR const uri,[CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context) const разделе ResourceContext)

Параметр URI может быть строкой с подстановочными знаками ("": ноль или больше; "?": только один). nullptr эквивалентен L "". Описание фильтров контекста ресурсов приведено в разделе CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT перечисление.

#### RemoveWebResourceRequestedFilter 

Удаляет соответствующий фильтр веб-ресурсов, который ранее был добавлен для события WebResourceRequested.

> общедоступный HRESULT [RemoveWebResourceRequestedFilter](#removewebresourcerequestedfilter)(LPCWSTR const uri,[CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context) const разделе ResourceContext)

Если один и тот же фильтр был добавлен несколько значений, его необходимо будет удалить столько, сколько вхождений было добавлено для эффективного. Возвращает E_INVALIDARG для фильтра, который еще не был добавлен.

#### add_WindowCloseRequested 

Добавьте обработчик событий для события WindowCloseRequested.

> общедоступные значения HRESULT [add_WindowCloseRequested](#add_windowcloserequested)([ICoreWebView2WindowCloseRequestedEventHandler](ICoreWebView2WindowCloseRequestedEventHandler.md) * eventHandler, EventRegistrationToken * token)

Вызывается, когда содержимое в WebView запрашивает закрытие окна, например после вызова Window. Close. Приложение должно закрыть окно WebView и связанное приложение, если это понятно приложению.

```cpp
    // Register a handler for the WindowCloseRequested event.
    // This handler will close the app window if it is not the main window.
    CHECK_FAILURE(m_webView->add_WindowCloseRequested(
        Callback<ICoreWebView2WindowCloseRequestedEventHandler>(
            [this](ICoreWebView2* sender, IUnknown* args) {
                if (m_isPopupWindow)
                {
                    CloseAppWindow();
                }
                return S_OK;
            })
            .Get(),
        nullptr));
```

#### remove_WindowCloseRequested 

Удалите обработчик событий, добавленный ранее add_WindowCloseRequested.

> общедоступные значения HRESULT [remove_WindowCloseRequested](#remove_windowcloserequested)(маркер EventRegistrationToken)

#### CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT 

Формат изображения, используемый в методе ICoreWebView2:: CapturePreview.

> [CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT](#core_webview2_capture_preview_image_format) перечисления

 Данные                         | Описания
--------------------------------|---------------------------------------------
CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_PNG            | Формат изображения PNG.
CORE_WEBVIEW2_CAPTURE_PREVIEW_IMAGE_FORMAT_JPEG            | Формат изображения JPEG.

#### CORE_WEBVIEW2_SCRIPT_DIALOG_KIND 

Диалоговое окно вида JavaScript, используемое в интерфейсе ICoreWebView2ScriptDialogOpeningEventHandler.

> [CORE_WEBVIEW2_SCRIPT_DIALOG_KIND](#core_webview2_script_dialog_kind) перечисления

 Данные                         | Описания
--------------------------------|---------------------------------------------
CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_ALERT            | Диалоговое окно, вызываемое с помощью функции Window. Alert JavaScript.
CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_CONFIRM            | Диалоговое окно, вызываемое с помощью функции Window. Confirm JavaScript.
CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_PROMPT            | Диалоговое окно, вызываемое с помощью функции Window. prompt JavaScript.
CORE_WEBVIEW2_SCRIPT_DIALOG_KIND_BEFOREUNLOAD            | Диалоговое окно, вызываемое с помощью события JavaScript beforeunload.

#### CORE_WEBVIEW2_PROCESS_FAILED_KIND 

Состояние сбоя процесса, используемого в интерфейсе ICoreWebView2ProcessFailedEventHandler.

> [CORE_WEBVIEW2_PROCESS_FAILED_KIND](#core_webview2_process_failed_kind) перечисления

 Данные                         | Описания
--------------------------------|---------------------------------------------
CORE_WEBVIEW2_PROCESS_FAILED_KIND_BROWSER_PROCESS_EXITED            | Указывает, что процесс браузера неожиданно завершился.
CORE_WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_EXITED            | Указывает, что процесс обработки неожиданно завершился.
CORE_WEBVIEW2_PROCESS_FAILED_KIND_RENDER_PROCESS_UNRESPONSIVE            | Указывает на то, что процесс рендеринга перестает отвечать на запросы.

#### CORE_WEBVIEW2_PERMISSION_KIND 

Тип запроса разрешения.

> [CORE_WEBVIEW2_PERMISSION_KIND](#core_webview2_permission_kind) перечисления

 Данные                         | Описания
--------------------------------|---------------------------------------------
CORE_WEBVIEW2_PERMISSION_KIND_UNKNOWN_PERMISSION            | Неизвестное разрешение.
CORE_WEBVIEW2_PERMISSION_KIND_MICROPHONE            | Разрешение на запись звука.
CORE_WEBVIEW2_PERMISSION_KIND_CAMERA            | Разрешение на захват видео.
CORE_WEBVIEW2_PERMISSION_KIND_GEOLOCATION            | Разрешение на доступ к географической позиции.
CORE_WEBVIEW2_PERMISSION_KIND_NOTIFICATIONS            | Разрешение на отправку веб-уведомлений.
CORE_WEBVIEW2_PERMISSION_KIND_OTHER_SENSORS            | Разрешение на доступ к универсальному датчику.
CORE_WEBVIEW2_PERMISSION_KIND_CLIPBOARD_READ            | Разрешение на чтение системного буфера обмена без жеста пользователя.

#### CORE_WEBVIEW2_PERMISSION_STATE 

Ответ на запрос разрешения.

> [CORE_WEBVIEW2_PERMISSION_STATE](#core_webview2_permission_state) перечисления

 Данные                         | Описания
--------------------------------|---------------------------------------------
CORE_WEBVIEW2_PERMISSION_STATE_DEFAULT            | Используйте поведение браузера по умолчанию, которое обычно запрашивает у пользователей решение.
CORE_WEBVIEW2_PERMISSION_STATE_ALLOW            | Предоставьте разрешение на запрос.
CORE_WEBVIEW2_PERMISSION_STATE_DENY            | Отказ от запроса разрешения.

#### CORE_WEBVIEW2_WEB_ERROR_STATUS 

Значения состояния ошибки для переходов по веб-страницам.

> [CORE_WEBVIEW2_WEB_ERROR_STATUS](#core_webview2_web_error_status) перечисления

 Данные                         | Описания
--------------------------------|---------------------------------------------
CORE_WEBVIEW2_WEB_ERROR_STATUS_UNKNOWN            | Произошла неизвестная ошибка.
CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_COMMON_NAME_IS_INCORRECT            | Общее имя сертификата SSL не совпадает с веб-адресом.
CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_EXPIRED            | Срок действия сертификата SSL истек.
CORE_WEBVIEW2_WEB_ERROR_STATUS_CLIENT_CERTIFICATE_CONTAINS_ERRORS            | SSL-сертификат клиента включает ошибки.
CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_REVOKED            | SSL-сертификат отозван.
CORE_WEBVIEW2_WEB_ERROR_STATUS_CERTIFICATE_IS_INVALID            | Недопустимый сертификат SSL &ndash; это может означать, что сертификат не соответствует ПИН-контактам открытого ключа для имени узла. сертификат подписан недоверенным центром или с использованием слабого алгоритма, который нарушает ограничения на имена, сертификат содержит слабый ключ, срок действия сертификата является слишком длинным, не хватает сведений об отзыве или механизме отзыва, неоднозначное имя узла, отсутствие сведений о прозрачности сертификата, или сертификат связан с [прежним корнем Symantec](https://security.googleblog.com/2018/03/distrust-of-symantec-pki-immediate.html).
CORE_WEBVIEW2_WEB_ERROR_STATUS_SERVER_UNREACHABLE            | Узел недостижим.
CORE_WEBVIEW2_WEB_ERROR_STATUS_TIMEOUT            | Время ожидания соединения истекло.
CORE_WEBVIEW2_WEB_ERROR_STATUS_ERROR_HTTP_INVALID_SERVER_RESPONSE            | Сервер вернул недопустимый или нераспознанный ответ.
CORE_WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_ABORTED            | Соединение было прервано.
CORE_WEBVIEW2_WEB_ERROR_STATUS_CONNECTION_RESET            | Подключение было сброшено.
CORE_WEBVIEW2_WEB_ERROR_STATUS_DISCONNECTED            | Соединение с Интернетом разорвано.
CORE_WEBVIEW2_WEB_ERROR_STATUS_CANNOT_CONNECT            | Не удается подключиться к конечному объекту.
CORE_WEBVIEW2_WEB_ERROR_STATUS_HOST_NAME_NOT_RESOLVED            | Не удалось разрешить указанное имя узла.
CORE_WEBVIEW2_WEB_ERROR_STATUS_OPERATION_CANCELED            | Операция была отменена.
CORE_WEBVIEW2_WEB_ERROR_STATUS_REDIRECT_FAILED            | Перенаправление запроса завершилось сбоем.
CORE_WEBVIEW2_WEB_ERROR_STATUS_UNEXPECTED_ERROR            | Произошла непредвиденная ошибка.

#### CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT 

Перечисление для контекстов запросов веб-ресурсов.

> [CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT](#core_webview2_web_resource_context) перечисления

 Данные                         | Описания
--------------------------------|---------------------------------------------
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_ALL            | Все ресурсы.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_DOCUMENT            | Ресурсы документов.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_STYLESHEET            | Ресурсы CSS.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_IMAGE            | Графические ресурсы.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_MEDIA            | Другие мультимедийные ресурсы, например видео.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_FONT            | Ресурсы шрифта.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_SCRIPT            | Ресурсы сценария.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_XML_HTTP_REQUEST            | HTTP-запросы.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_FETCH            | Получение взаимодействия API.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_TEXT_TRACK            | TextTrack ресурсы.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_EVENT_SOURCE            | Взаимодействие API EventSource.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_WEBSOCKET            | Взаимодействие API WebSocket.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_MANIFEST            | Манифесты веб-приложения.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_SIGNED_EXCHANGE            | Обмен подписанными HTTP-сообщениями.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_PING            | Запросы ping.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_CSP_VIOLATION_REPORT            | Отчеты о нарушениях CSP.
CORE_WEBVIEW2_WEB_RESOURCE_CONTEXT_OTHER            | Другие ресурсы.
