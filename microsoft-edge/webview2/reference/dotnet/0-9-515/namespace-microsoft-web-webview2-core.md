---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: a2a719a12a90f6b1d283ddb10b7513a498cb816d
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697289"
---
# Microsoft.Web.WebView2.Core пространство имен 

> [!NOTE]
> Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515. Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[CoreWebView2CapturePreviewImageFormat](#corewebview2capturepreviewimageformat) | Формат изображения, используемый в методе CoreWebView2CapturePreview.
[CoreWebView2KeyEventKind](#corewebview2keyeventkind) | Тип события клавиши, которое инициировало событие AcceleratorKeyPressed.
[CoreWebView2MoveFocusReason](#corewebview2movefocusreason) | Причина для перемещения фокуса.
[CoreWebView2PermissionKind](#corewebview2permissionkind) | Тип запроса разрешения.
[CoreWebView2PermissionState](#corewebview2permissionstate) | Ответ на запрос разрешения.
[CoreWebView2ProcessFailedKind](#corewebview2processfailedkind) | Состояние сбоя процесса, используемого в классе CoreWebView2ProcessFailedEventHandler.
[CoreWebView2ScriptDialogKind](#corewebview2scriptdialogkind) | Диалоговое окно вида JavaScript, используемое в классе CoreWebView2ScriptDialogOpeningEventHandler.
[CoreWebView2WebErrorStatus](#corewebview2weberrorstatus) | Значения состояния ошибки для переходов по веб-страницам.
[CoreWebView2WebResourceContext](#corewebview2webresourcecontext) | Перечисление для контекстов запросов веб-ресурсов.
CoreWebView2 | WebView2 позволяет размещать веб-содержимое с помощью новейшей технологии веб-браузера.
CoreWebView2AcceleratorKeyPressedEventArgs | Аргументы события для события AcceleratorKeyPressed.
CoreWebView2ContentLoadingEventArgs | Аргументы события для события ContentLoading.
CoreWebView2Controller | Этот класс является владельцем объекта CoreWebView2 и предоставляет поддержку для изменения размеров, отображения и скрытия, фокусировки и других функциональных возможностей, связанных с окнами и композицией.
CoreWebView2Deferral | Этот класс используется для выполнения РБП для аргументов события, которые поддерживают сбор расходов будущих периодов с помощью методаического РБП.
CoreWebView2DevToolsProtocolEventReceivedEventArgs | Аргументы события для события DevToolsProtocolEventReceived.
CoreWebView2DevToolsProtocolEventReceiver | Получатель создается для определенного события протокола DevTools и позволяет подписаться на него и отказаться от него.
CoreWebView2Environment | Представляет среду WebView2.
CoreWebView2EnvironmentOptions | Параметры, используемые для создания среды WebView2.
CoreWebView2MoveFocusRequestedEventArgs | Аргументы события для события MoveFocusRequested.
CoreWebView2NavigationCompletedEventArgs | Аргументы события для события NavigationCompleted.
CoreWebView2NavigationStartingEventArgs | Аргументы события для события NavigationStarting.
CoreWebView2NewWindowRequestedEventArgs | Аргументы события для события NewWindowRequested.
CoreWebView2PermissionRequestedEventArgs | Аргументы события для события PermissionRequested.
CoreWebView2ProcessFailedEventArgs | Аргументы события для события ProcessFailed.
CoreWebView2ScriptDialogOpeningEventArgs | Аргументы события для события ScriptDialogOpening.
CoreWebView2Settings | Определяет свойства, которые включают, отключают или изменяют функции WebView.
CoreWebView2SourceChangedEventArgs | Аргументы события для события SourceChanged.
CoreWebView2WebMessageReceivedEventArgs | Аргументы события для события WebMessageReceived.
CoreWebView2WebResourceRequestedEventArgs | Аргументы события для события WebResourceRequested.
EdgeNotFoundException | Исключение, возникающее при отсутствии установки Edge.
CoreWebView2PhysicalKeyStatus | Структура, представляющая данные, Упакованные в LPARAM, предоставленные событию ключа Win32.

## Участников

#### CoreWebView2CapturePreviewImageFormat 

> Перечисление [CoreWebView2CapturePreviewImageFormat](#corewebview2capturepreviewimageformat)

 Данные                         | Описания
--------------------------------|---------------------------------------------
Формат            | Формат изображения PNG.
JPEG            | Формат изображения JPEG.

Формат изображения, используемый в методе CoreWebView2CapturePreview.

#### CoreWebView2KeyEventKind 

> Перечисление [CoreWebView2KeyEventKind](#corewebview2keyeventkind)

 Данные                         | Описания
--------------------------------|---------------------------------------------
KeyDown            | ВыWM_KEYDOWN сообщение в окне.
KeyUp            | ВыWM_KEYUP сообщение в окне.
SystemKeyDown            | ВыWM_SYSKEYDOWN сообщение в окне.
SystemKeyUp            | ВыWM_SYSKEYUP сообщение в окне.

Тип события клавиши, которое инициировало событие AcceleratorKeyPressed.

#### CoreWebView2MoveFocusReason 

> Перечисление [CoreWebView2MoveFocusReason](#corewebview2movefocusreason)

 Данные                         | Описания
--------------------------------|---------------------------------------------
Методом            | Настройка кода фокуса на WebView.
Next            | Перемещение фокуса из-за прохождения вкладки вперед.
Previous            | Перемещение фокуса из-за перемещения по табуляции назад.

Причина для перемещения фокуса.

#### CoreWebView2PermissionKind 

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

Тип запроса разрешения.

#### CoreWebView2PermissionState 

> Перечисление [CoreWebView2PermissionState](#corewebview2permissionstate)

 Данные                         | Описания
--------------------------------|---------------------------------------------
По умолчанию            | Используйте поведение браузера по умолчанию, которое обычно запрашивает у пользователей решение.
Разрешить            | Предоставьте разрешение на запрос.
Запретить            | Отказ от запроса разрешения.

Ответ на запрос разрешения.

#### CoreWebView2ProcessFailedKind 

> Перечисление [CoreWebView2ProcessFailedKind](#corewebview2processfailedkind)

 Данные                         | Описания
--------------------------------|---------------------------------------------
BrowserProcessExited            | Неожиданное завершение процесса браузера.
RenderProcessExited            | Процесс рендеринга неожиданно завершился.
RenderProcessUnresponsive            | Указывает на то, что процесс рендеринга перестает отвечать на запросы.

Состояние сбоя процесса, используемого в классе CoreWebView2ProcessFailedEventHandler.

#### CoreWebView2ScriptDialogKind 

> Перечисление [CoreWebView2ScriptDialogKind](#corewebview2scriptdialogkind)

 Данные                         | Описания
--------------------------------|---------------------------------------------
Оповещение            | Диалоговое окно, вызываемое с помощью функции Window. Alert JavaScript.
Подтвердить            | Диалоговое окно, вызываемое с помощью функции Window. Confirm JavaScript.
Дачу            | Диалоговое окно, вызываемое с помощью функции Window. prompt JavaScript.
Beforeunload            | Диалоговое окно, вызываемое с помощью функции Window. beforeunload JavaScript.

Диалоговое окно вида JavaScript, используемое в классе CoreWebView2ScriptDialogOpeningEventHandler.

#### CoreWebView2WebErrorStatus 

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

Значения состояния ошибки для переходов по веб-страницам.

#### CoreWebView2WebResourceContext 

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

Перечисление для контекстов запросов веб-ресурсов.

