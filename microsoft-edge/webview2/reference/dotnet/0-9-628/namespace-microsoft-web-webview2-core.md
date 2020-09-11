---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2. Core
ms.openlocfilehash: f577cb08bf6029821f9aa3919e73273c82201712
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012423"
---
# Microsoft.Web.WebView2.Core пространство имен 

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[CoreWebView2CapturePreviewImageFormat](#corewebview2capturepreviewimageformat) | Формат изображения, используемый в методе CoreWebView2CapturePreview.
[CoreWebView2KeyEventKind](#corewebview2keyeventkind) | Тип события клавиши, которое инициировало событие AcceleratorKeyPressed.
[CoreWebView2MouseEventKind](#corewebview2mouseeventkind) | Тип событий мыши, используемый функцией SendMouseInput для передачи типа события мыши, отправляемого в WebView.
[CoreWebView2MouseEventVirtualKeys](#corewebview2mouseeventvirtualkeys) | Виртуальные ключи событий мыши, связанные с CoreWebView2MouseEventKind для SendMouseInput.
[CoreWebView2MoveFocusReason](#corewebview2movefocusreason) | Причина для перемещения фокуса.
[CoreWebView2PermissionKind](#corewebview2permissionkind) | Тип запроса разрешения.
[CoreWebView2PermissionState](#corewebview2permissionstate) | Ответ на запрос разрешения.
[CoreWebView2PointerEventKind](#corewebview2pointereventkind) | Тип события указателя, используемый функцией SendPointerInput для передачи типа события указателя, отправляемого в WebView.
[CoreWebView2ProcessFailedKind](#corewebview2processfailedkind) | Состояние сбоя процесса, используемого в классе CoreWebView2ProcessFailedEventHandler.
[CoreWebView2ScriptDialogKind](#corewebview2scriptdialogkind) | Диалоговое окно вида JavaScript, используемое в классе CoreWebView2ScriptDialogOpeningEventHandler.
[CoreWebView2WebErrorStatus](#corewebview2weberrorstatus) | Значения состояния ошибки для переходов по веб-страницам.
[CoreWebView2WebResourceContext](#corewebview2webresourcecontext) | Перечисление для контекстов запросов веб-ресурсов.
CoreWebView2 | WebView2 позволяет размещать веб-содержимое с помощью новейшей технологии веб-браузера.
CoreWebView2AcceleratorKeyPressedEventArgs | Аргументы события для события AcceleratorKeyPressed.
CoreWebView2CompositionController | Этот класс является расширением класса CoreWebView2Controller для поддержки визуального размещения.
CoreWebView2ContentLoadingEventArgs | Аргументы события для события ContentLoading.
CoreWebView2Controller | Этот класс является владельцем объекта CoreWebView2 и предоставляет поддержку для изменения размеров, отображения и скрытия, фокусировки и других функциональных возможностей, связанных с окнами и композицией.
CoreWebView2Deferral | Этот класс используется для выполнения РБП для аргументов события, которые поддерживают сбор расходов будущих периодов с помощью методаического РБП.
CoreWebView2DevToolsProtocolEventReceivedEventArgs | Аргументы события для события DevToolsProtocolEventReceived.
CoreWebView2DevToolsProtocolEventReceiver | Получатель создается для определенного события протокола DevTools и позволяет подписаться на него и отказаться от него.
CoreWebView2Environment | Представляет среду WebView2.
CoreWebView2EnvironmentOptions | Параметры, используемые для создания среды WebView2.
CoreWebView2HttpHeadersCollectionIterator | Итератор для коллекции заголовков HTTP.
CoreWebView2HttpRequestHeaders | Заголовки запросов HTTP.
CoreWebView2HttpResponseHeaders | Заголовки ответа HTTP.
CoreWebView2MoveFocusRequestedEventArgs | Аргументы события для события MoveFocusRequested.
CoreWebView2NavigationCompletedEventArgs | Аргументы события для события NavigationCompleted.
CoreWebView2NavigationStartingEventArgs | Аргументы события для события NavigationStarting.
CoreWebView2NewWindowRequestedEventArgs | Аргументы события для события NewWindowRequested.
CoreWebView2PermissionRequestedEventArgs | Аргументы события для события PermissionRequested.
CoreWebView2PointerInfo | Это преимущественно представляет объединенный объект Win32 POINTER_INFO/POINTER_TOUCH_INFO/POINTER_PEN_INFO.
CoreWebView2ProcessFailedEventArgs | Аргументы события для события ProcessFailed.
CoreWebView2ScriptDialogOpeningEventArgs | Аргументы события для события ScriptDialogOpening.
CoreWebView2Settings | Определяет свойства, которые включают, отключают или изменяют функции WebView.
CoreWebView2SourceChangedEventArgs | Аргументы события для события SourceChanged.
CoreWebView2WebMessageReceivedEventArgs | Аргументы события для события WebMessageReceived.
CoreWebView2WebResourceRequest | HTTP-запрос, используемый для события WebResourceRequested.
CoreWebView2WebResourceRequestedEventArgs | Аргументы события для события WebResourceRequested.
CoreWebView2WebResourceResponse | HTTP-ответ, используемый с событием WebResourceRequested.
CoreWebView2WebResourceResponseReceivedEventArgs | Аргументы события для события WebResourceResponseReceived.
CoreWebView2WindowFeatures | Функции окна для всплывающего окна WebView.
EdgeNotFoundException | Исключение, возникающее при отсутствии установки Edge.
CoreWebView2Matrix4x4 | Это преобразование используется для вычисления правильных координат при вызове CreateCoreWebView2PointerInfoFromPointerId.
CoreWebView2PhysicalKeyStatus | Структура, представляющая данные, Упакованные в LPARAM, предоставленные событию ключа Win32.

## Участников

#### CoreWebView2CapturePreviewImageFormat 

Формат изображения, используемый в методе CoreWebView2CapturePreview.

> Перечисление [CoreWebView2CapturePreviewImageFormat](#corewebview2capturepreviewimageformat)

 Данные                         | Описания
--------------------------------|---------------------------------------------
Формат            | Формат изображения PNG.
JPEG            | Формат изображения JPEG.

#### CoreWebView2KeyEventKind 

Тип события клавиши, которое инициировало событие AcceleratorKeyPressed.

> Перечисление [CoreWebView2KeyEventKind](#corewebview2keyeventkind)

 Данные                         | Описания
--------------------------------|---------------------------------------------
KeyDown            | ВыWM_KEYDOWN сообщение в окне.
KeyUp            | ВыWM_KEYUP сообщение в окне.
SystemKeyDown            | ВыWM_SYSKEYDOWN сообщение в окне.
SystemKeyUp            | ВыWM_SYSKEYUP сообщение в окне.

#### CoreWebView2MouseEventKind 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

Тип событий мыши, используемый функцией SendMouseInput для передачи типа события мыши, отправляемого в WebView.

> Перечисление [CoreWebView2MouseEventKind](#corewebview2mouseeventkind)

 Данные                         | Описания
--------------------------------|---------------------------------------------
HorizontalWheel            | Событие прокрутки колесика мыши по горизонтали WM_MOUSEHWHEEL.
LeftButtonDoubleClick            | Левая кнопка дважды щелкните событие мыши, WM_LBUTTONDBLCLK.
LeftButtonDown            | Левая кнопка вниз события мыши, WM_LBUTTONDOWN.
LeftButtonUp            | Левая кнопка — событие мыши, WM_LBUTTONUP.
Больнич            | Событие выхода из мыши, WM_MOUSELEAVE.
MiddleButtonDoubleClick            | Средняя кнопка дважды щелкните событие мыши, WM_MBUTTONDBLCLK.
MiddleButtonDown            | Средняя кнопка вниз: событие мыши, WM_MBUTTONDOWN.
MiddleButtonUp            | Средняя кнопка: событие мыши, WM_MBUTTONUP.
Move (переместить)            | Событие перемещения мыши, WM_MOUSEMOVE.
RightButtonDoubleClick            | Щелчок правой кнопкой мыши дважды щелкните событие мыши, WM_RBUTTONDBLCLK.
RightButtonDown            | Щелчок правой кнопкой мыши, WM_RBUTTONDOWN.
RightButtonUp            | Щелкните правой кнопкой мыши событие мыши, WM_RBUTTONUP.
Колесо            | Событие прокрутки колесика мыши, WM_MOUSEWHEEL.
XButtonDoubleClick            | Первая или вторая кнопка X дважды щелкните событие мыши, WM_XBUTTONDBLCLK.
XButtonDown            | Первая или вторая кнопка X вниз, WM_XBUTTONDOWN.
XButtonUp            | Первая или вторая кнопка X — событие мыши, WM_XBUTTONUP.

#### CoreWebView2MouseEventVirtualKeys 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

Виртуальные ключи событий мыши, связанные с CoreWebView2MouseEventKind для SendMouseInput.

> Перечисление [CoreWebView2MouseEventVirtualKeys](#corewebview2mouseeventvirtualkeys)

 Данные                         | Описания
--------------------------------|---------------------------------------------
Нет            | Дополнительные клавиши не нажаты.
LeftButton            | Щелчок левой кнопкой мыши не работает, MK_LBUTTON.
RightButton            | Щелчок правой кнопкой мыши не работает, MK_RBUTTON.
Shift            | Клавиша SHIFT нажата вниз, MK_SHIFT.
Элемент управления            | Клавиша CTRL нажата, MK_CONTROL.
MiddleButton            | Средняя нажатие кнопки мыши не работает, MK_MBUTTON.
XButton1            | Первая кнопка X нажата MK_XBUTTON1.
XButton2            | Вторая кнопка X нажата MK_XBUTTON2.

#### CoreWebView2MoveFocusReason 

Причина для перемещения фокуса.

> Перечисление [CoreWebView2MoveFocusReason](#corewebview2movefocusreason)

 Данные                         | Описания
--------------------------------|---------------------------------------------
Методом            | Настройка кода фокуса на WebView.
Next            | Перемещение фокуса из-за прохождения вкладки вперед.
Previous            | Перемещение фокуса из-за перемещения по табуляции назад.

#### CoreWebView2PermissionKind 

Тип запроса разрешения.

> Перечисление [CoreWebView2PermissionKind](#corewebview2permissionkind)

 Данные                         | Описания
--------------------------------|---------------------------------------------
UnknownPermission            | Неизвестное разрешение.
Микрофон            | Разрешение на запись звука.
Камера            | Разрешение на захват видео.
Геолокация            | Разрешение на доступ к географической позиции.
Уведомления            | Разрешение на отправку веб-уведомлений.
OtherSensors            | Разрешение на доступ к универсальному датчику.
ClipboardRead            | Разрешение на чтение системного буфера обмена без жеста пользователя.

#### CoreWebView2PermissionState 

Ответ на запрос разрешения.

> Перечисление [CoreWebView2PermissionState](#corewebview2permissionstate)

 Данные                         | Описания
--------------------------------|---------------------------------------------
По умолчанию            | Используйте поведение браузера по умолчанию, которое обычно запрашивает у пользователей решение.
Разрешить            | Предоставьте разрешение на запрос.
Запретить            | Отказ от запроса разрешения.

#### CoreWebView2PointerEventKind 

[!INCLUDE [prerelease-note](../../includes/prerelease-note.md)]

Тип события указателя, используемый функцией SendPointerInput для передачи типа события указателя, отправляемого в WebView.

> Перечисление [CoreWebView2PointerEventKind](#corewebview2pointereventkind)

 Данные                         | Описания
--------------------------------|---------------------------------------------
Активация            | Соответствует WM_POINTERACTIVATE.
Вниз            | Соответствует WM_POINTERDOWN.
Ввод            | Соответствует WM_POINTERENTER.
Больнич            | Соответствует WM_POINTERLEAVE.
Вверх            | Соответствует WM_POINTERUP.
Update            | Соответствует WM_POINTERUPDATE.

#### CoreWebView2ProcessFailedKind 

Состояние сбоя процесса, используемого в классе CoreWebView2ProcessFailedEventHandler.

> Перечисление [CoreWebView2ProcessFailedKind](#corewebview2processfailedkind)

 Данные                         | Описания
--------------------------------|---------------------------------------------
BrowserProcessExited            | Неожиданное завершение процесса браузера.
RenderProcessExited            | Процесс рендеринга неожиданно завершился.
RenderProcessUnresponsive            | Указывает на то, что процесс рендеринга перестает отвечать на запросы.

#### CoreWebView2ScriptDialogKind 

Диалоговое окно вида JavaScript, используемое в классе CoreWebView2ScriptDialogOpeningEventHandler.

> Перечисление [CoreWebView2ScriptDialogKind](#corewebview2scriptdialogkind)

 Данные                         | Описания
--------------------------------|---------------------------------------------
Оповещение            | Диалоговое окно, вызываемое с помощью функции Window. Alert JavaScript.
Подтвердить            | Диалоговое окно, вызываемое с помощью функции Window. Confirm JavaScript.
Дачу            | Диалоговое окно, вызываемое с помощью функции Window. prompt JavaScript.
Beforeunload            | Диалоговое окно, вызываемое с помощью функции Window. beforeunload JavaScript.

#### CoreWebView2WebErrorStatus 

Значения состояния ошибки для переходов по веб-страницам.

> Перечисление [CoreWebView2WebErrorStatus](#corewebview2weberrorstatus)

 Данные                         | Описания
--------------------------------|---------------------------------------------
Unknown (неизвестно).            | Произошла неизвестная ошибка.
CertificateCommonNameIsIncorrect            | Общее имя сертификата SSL не совпадает с веб-адресом.
CertificateExpired            | Срок действия сертификата SSL истек.
ClientCertificateContainsErrors            | SSL-сертификат клиента включает ошибки.
CertificateRevoked            | SSL-сертификат отозван.
CertificateIsInvalid            | Недопустимый сертификат SSL &ndash; это может означать, что сертификат не соответствует ПИН-контактам открытого ключа для имени узла. сертификат подписан недоверенным центром или с использованием слабого алгоритма, который нарушает ограничения на имена, сертификат содержит слабый ключ, срок действия сертификата является слишком длинным, не хватает сведений об отзыве или механизме отзыва, неоднозначное имя узла, отсутствие сведений о прозрачности сертификата, или сертификат связан с [прежним корнем Symantec](https://security.googleblog.com/2018/03/distrust-of-symantec-pki-immediate.html).
ServerUnreachable            | Узел недостижим.
Превышено время ожидания            | Время ожидания соединения истекло.
ErrorHttpInvalidServerResponse            | Сервер вернул недопустимый или нераспознанный ответ.
ConnectionAborted            | Соединение было прервано.
ConnectionReset            | Подключение было сброшено.
Изолирован            | Соединение с Интернетом разорвано.
CannotConnect            | Не удается подключиться к конечному объекту.
HostNameNotResolved            | Не удалось разрешить указанное имя узла.
OperationCanceled            | Операция была отменена.
RedirectFailed            | Перенаправление запроса завершилось сбоем.
UnexpectedError            | Произошла непредвиденная ошибка.

#### CoreWebView2WebResourceContext 

Перечисление для контекстов запросов веб-ресурсов.

> Перечисление [CoreWebView2WebResourceContext](#corewebview2webresourcecontext)

 Данные                         | Описания
--------------------------------|---------------------------------------------
Все            | Все ресурсы.
Документ            | Ресурсы документов.
Таблицу            | Ресурсы CSS.
Изображение            | Графические ресурсы.
Мультимедиа            | Другие мультимедийные ресурсы, например видео.
Шрифт            | Ресурсы шрифта.
Сценарий            | Ресурсы сценария.
XmlHttpRequest            | HTTP-запросы.
Извлечен            | Получение взаимодействия API.
TextTrack            | TextTrack ресурсы.
EventSource            | Взаимодействие API EventSource.
WebSocket            | Взаимодействие API WebSocket.
Является            | Манифесты веб-приложения.
SignedExchange            | Обмен подписанными HTTP-сообщениями.
Тест            | Запросы ping.
CspViolationReport            | Отчеты о нарушениях CSP.
Other            | Другие ресурсы.

