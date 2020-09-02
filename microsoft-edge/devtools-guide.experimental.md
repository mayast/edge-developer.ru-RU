---
description: Знакомство со средствами разработчика Microsoft Edge
title: Инструменты разработчика Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/20/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: edgehtml
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
experimental: false
experiment_id: 51fe4b97-3e55-41
ms.openlocfilehash: 3aee2ab67c6e703a0a31b58b5bf985a23fcbb481
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986222"
---
# Инструменты разработчика Microsoft Edge  

> [!NOTE]
> Microsoft Edge DevTools, чтобы веб-разработчики могли создавать и тестировать веб-сайты.  Если вы случайно открыли DevTools, просто нажмите " `F12` Закрыть".  

Microsoft Edge DevTools строится с помощью [TypeScript](https://www.typescriptlang.org/), на платформе [Open Source](https://github.com/Microsoft/ChakraCore), оптимизированных для современных рабочих процессов, и теперь оно доступно как [автономное приложение для Windows 10](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj) в Microsoft Store.

Чтобы узнать больше о последних возможностях, ознакомьтесь с [*DevTools в последнем обновлении Windows 10 (EdgeHTML 17)*](./devtools-guide/whats-new.md).

## Основные средства

![Microsoft Edge DevTools](./devtools-guide/media/devtools.png)

Microsoft Edge DevTools включает следующие возможности:

 - Панель " [**элементы**](./devtools-guide/elements.md) " для редактирования HTML и CSS, проверки свойств специальных возможностей, просмотра прослушивателей событий и установки контрольных точек изменений DOM
 - [**Консоль**](./devtools-guide/console.md) для просмотра и фильтрации сообщений журнала, проверки объектов JavaScript и узлов DOM, а также выполнения JavaScript в контексте выбранного окна или фрейма
 - [**Отладчик**](./devtools-guide/debugger.md) для пошагового использования кода, задания контрольных значений и точек останова, редактирование кода в реальном времени, проверка веб-хранилища и кэша файлов cookie.
 - Панель [**сети**](./devtools-guide/network.md) для мониторинга и проверки запросов и ответов из кэша сети и браузера 
 - Панель [**производительности**](./devtools-guide/performance.md) для профилирования времени и системных ресурсов, необходимых для вашего сайта
 - Панель [**памяти**](./devtools-guide/memory.md) для измерения использования ресурсов памяти и сравнения снимков кучи в разных состояниях выполнения кода
 - Панель [**эмуляции**](./devtools-guide/emulation.md) для проверки сайта с различными профилями браузера, разрешениями экрана и координатами местоположения GPS

Отправляйте [Отзывы и запросы функций](#getting-in-touch-with-the-microsoft-edge-devtools-team).

> [!TIP]
> **[Протестируйте Microsoft Edge бесплатно из любого браузера](https://developer.microsoft.com/microsoft-edge/tools/remote/)**: мы [соBrowserStackся](https://www.browserstack.com/test-on-microsoft-edge-browser#live-cloud) с помощью этого приложения, чтобы предоставить бесплатный Live и автоматизированное тестирование в Microsoft Edge.

## Приложение Microsoft Store

**Microsoft Edge DevTools** [теперь доступен для предварительного просмотра](./devtools-guide/whats-new.md) в виде автономного [приложения для Windows 10 из Microsoft Store](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab), а также с помощью функции "in-browser ( `F12` )". В версии из магазина предусмотрена панель *средства выбора* для подключения к открытым локальным и удаленным конечным объектам страницы и макету с вкладками для удобного переключения между экземплярами Средств разработчика.

### Локальная отладка

Чтобы выполнить отладку страницы локально, просто запустите приложение *Microsoft Edge DevTools* . На **локальной** панели средства выбора отобразятся все активные процессы содержимого EdgeHTML, включая открытые вкладки браузера EDGE, запуск [PWAs](./progressive-web-apps-edgehtml/index.md) (*WWAHost.exe* процессы) и [WebView](./webview.md) элементы управления. Щелкните требуемый конечный объект, чтобы прикрепить и открыть новый экземпляр вкладки DevTools.

![Локальная панель приложения Средства разработчика](./devtools-guide/media/chooser_local.png)

### Удаленная отладка

Приложение *Microsoft Edge DevTools* предоставляет базовую поддержку для отладки страниц на удаленном компьютере с помощью нового [**протокола DevTools**](./devtools-protocol/index.md). В этом выпуске есть удаленный доступ к основным funtionality на панели [**отладчика**](./devtools-guide/debugger.md) , за вычетом проверки кэша (для веб-хранилища, рабочего процесса службы, кэша API и IndexedDB). Удаленная отладка ограничена *Microsoft Edge* для *настольных* компьютеров и поддерживает другие узлы EdgeHTML и устройства под управлением Windows 10, которые появятся в будущих выпусках.

Чтобы приступить к работе, ознакомьтесь с разделом [*Средства разработчика в Microsoft Edge*](./devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview) в документации [Протокол средств разработчика](./devtools-protocol/index.md).

![Удаленная панель приложения Средства разработчика](./devtools-guide/media/chooser_remote.png)

## Общие сочетания клавиш

Эти сочетания клавиш используются для управления основным окном DevTools и/или всеми инструментами.

Действие | Установленное напрямую доверие
:------------ | :-------------
Показать или скрыть DevTools (открывается в последней просмотренной панели) | F12, Ctrl + Shift + I
Переключить закрепление (отстыковать/снизу или справа) | Ctrl + Shift + D 
Отображение не редактируемого открытого исходного HTML-кода в отладчике | Ctrl + U
Показать или скрыть консоль в нижней части любого другого средства  | Ctrl +**`**
Переключиться на элементы (проводник DOM) | Ctrl + 1
Переключиться на Консоль |  Ctrl + 2
Переключиться в режим Отладчика | Ctrl + 3
Переключиться на Сеть | Ctrl + 4
Переключиться на Производительность | Ctrl + 5
Переключиться на Память | CTRL + 6
Переключиться на Эмуляцию | Ctrl + 7
Документ справки | F1
Следующее средство | Ctrl + F6
Предыдущее средство | Ctrl + Shift + F6
Предыдущее средство (из истории) | Ctrl + Shift + [
Следующий инструмент (из истории) | Ctrl + Shift +]
Следующий подкадр    | F6
Предыдущий подкадр | Shift + F6
Следующее соответствие в поле поиска | F3
Предыдущее соответствие в поле поиска | Shift + F3
Поиск в поле поиска | CTRL+F
Перемещение фокуса на консоль в нижней части экрана | Alt + Shift + I
Инструменты закрепления и отстыковки (переключить закрепление) | CTRL+P  
Запуск Средств разработчика на консоли | Ctrl + Shift + J
Обновите страницу. **Примечание.** при отладке и приостановке в точке останова выполняется сначала возобновление выполнения. | Ctrl + Shift + F5 или CTRL + R

## Знакомство с командой Microsoft Edge DevTools  

[!INCLUDE [contact DevTools team note](./devtools-guide-chromium/includes/contact-devtools-team-note.md)]  
