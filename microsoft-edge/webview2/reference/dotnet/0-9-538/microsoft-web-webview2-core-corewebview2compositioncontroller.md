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
ms.openlocfilehash: 33adcccc4174a4ebcbabe4a169cd430942ad8a5a
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699265"
---
# Класс Microsoft. Web. WebView2. Core. CoreWebView2CompositionController 

> [!NOTE]
> Это [экспериментальный API](../../../concepts/versioning.md#experimental-apis) , поставляемый с нашей версией SDK версии [0.9.538-предварительной версии](../../../releasenotes.md#09538).

Пространство имен: Microsoft. Web. WebView2. Core \
Сборка: Microsoft. Web. WebView2. Core. dll

Этот класс является расширением класса CoreWebView2Controller для поддержки визуального размещения.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[Cursor (Курсор)](#cursor) | Текущий курсор, WebView рассчитает, что он должен быть.
[CursorChanged](#cursorchanged) | Событие срабатывает, когда WebView считает, что курсор должен быть изменен.
[RootVisualTarget](#rootvisualtarget) | RootVisualTarget — это визуальный элемент в визуальном дереве размещающего приложения.
[UIAProvider](#uiaprovider) | Возвращает поставщик модели автоматизации пользовательского интерфейса для WebView.
[CreateCoreWebView2PointerInfoFromPointerId](#createcorewebview2pointerinfofrompointerid) | Вспомогательная функция для преобразования pointerId, полученного из системы, в CoreWebView2ExperimentalPointerInfo.
[SendMouseInput](#sendmouseinput) | Если eventKind — CoreWebView2MouseEventKind. HorizontalWheel или CoreWebView2MouseEventKind. Wheel, то mouseData задает величину движения колесика.
[SendPointerInput](#sendpointerinput) | SendPointerInput принимает вводные данные и указатель пера для типов, определенных в CoreWebView2PointerEventKind.

## Участников

#### Cursor (Курсор) 

Текущий курсор, WebView рассчитает, что он должен быть.

> Открытый [курсор](#cursor) IntPtr

Курсор должен быть установлен в WM_SETCURSOR с помощью мыши. SetCursor или установлен на соответствующем родительском элементе/предок WebView через SetClassLongPtr. HCURSOR можно освободить таким образом, чтобы CopyCursor и DestroyCursor, чтобы сохранить собственную копию, если вы еще не настраиваете курсор.

#### CursorChanged 

Событие срабатывает, когда WebView считает, что курсор должен быть изменен.

> событие EventHandler< объект > [CursorChanged](#cursorchanged)

Например, если курсор мыши установлен по умолчанию, но затем перемещается поверх текста, он может попытаться перейти на курсор IBeam.

#### RootVisualTarget 

RootVisualTarget — это визуальный элемент в визуальном дереве размещающего приложения.

> общедоступный объект [RootVisualTarget](#rootvisualtarget)

Этот визуальный элемент — это то, где WebView будет подключаться к визуальному дереву. Приложение использует этот визуальный элемент, чтобы расположить WebView в приложении. Чтобы изменить размер WebView, приложению по-прежнему нужно использовать свойство Boundss. Свойством RootVisualTarget может быть IDCompositionVisual или Windows:: UI:: композиция:: ContainerVisual. WebView подключится к визуальному дереву для предоставленного визуального элемента перед возвратом из метода присваивания свойств. Приложение должно быть зафиксировано на своем устройстве, в котором задано свойство RootVisualTarget. Свойство RootVisualTarget поддерживает значение nullptr, чтобы отключить WebView от визуального дерева приложения.

#### UIAProvider 

Возвращает поставщик модели автоматизации пользовательского интерфейса для WebView.

> общедоступный объект [UIAProvider](#uiaprovider)

#### CreateCoreWebView2PointerInfoFromPointerId 

Вспомогательная функция для преобразования pointerId, полученного из системы, в CoreWebView2ExperimentalPointerInfo.

> общедоступные [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) [CreateCoreWebView2PointerInfoFromPointerId](#createcorewebview2pointerinfofrompointerid)(uint pointerId, IntPtr ParentWindow, Matrix4x4 Transform)

parentWindow — HWND, который содержит WebView. Это может быть любой HWND в дереве HWND, который включает WebView. CoreWebView2Matrix4x4 является преобразованием из HWND в WebView. Возвращенный CoreWebView2ExperimentalPointerInfo используется в SendPointerInfo. Тип указателя должен быть либо пером, либо сенсорным, либо функция завершится сбоем.

#### SendMouseInput 

Если eventKind — CoreWebView2MouseEventKind. HorizontalWheel или CoreWebView2MouseEventKind. Wheel, то mouseData задает величину движения колесика.

> Public void [SendMouseInput](#sendmouseinput)([CoreWebView2MouseEventKind](./namespace-microsoft-web-webview2-core.md) eventKind, [CoreWebView2MouseEventVirtualKeys](./namespace-microsoft-web-webview2-core.md) virtualKeys, uint mouseData, Point Point)

Положительное значение указывает на то, что колесико было повернуто вперед от пользователя; отрицательное значение указывает на то, что колесико было повернуто на обратном направлении к пользователю. Один щелчок мыши определяется как WHEEL_DELTA (120). Если eventKind — CoreWebView2MouseEventKind. XButtonDoubleClick CoreWebView2MouseEventKind. XButtonDown или CoreWebView2MouseEventKind. XButtonUp, mouseData указывает, какие кнопки X были нажаты или отпущены. Это значение должно быть 1, если первая кнопка X нажата/выпущена, и 2 при нажатии или отпускании второй кнопки X. Если eventKind — CoreWebView2MouseEventKind. Leave, virtualKeys, mouseData и Point должны равняться нулю. Если eventKind — любое другое значение, mouseData должно равняться нулю. Ожидается, что точка должна находиться в пространстве координат клиента WebView. Для отслеживания событий мыши, которые запускаются в WebView и потенциально могут перемещаться за пределы WebView и ведущего приложения, рекомендуется использовать вызов SetCapture и ReleaseCapture. Чтобы выйти из всплывающих окон, также рекомендуется отправлять WM_MOUSELEAVE сообщения.

#### SendPointerInput 

SendPointerInput принимает вводные данные и указатель пера для типов, определенных в CoreWebView2PointerEventKind.

> Public void [SendPointerInput](#sendpointerinput)([CoreWebView2PointerEventKind](./namespace-microsoft-web-webview2-core.md) EventType, [CoreWebView2PointerInfo](microsoft-web-webview2-core-corewebview2pointerinfo.md) pointerInfo)

Все входные данные указателя из системы должны быть преобразованы в CoreWebView2ExperimentalPointerInfo первыми.

