---
description: Знакомство со средствами разработчика Microsoft Edge
title: Инструменты разработчика Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: edgehtml
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
experimental: false
experiment_id: 51fe4b97-3e55-41
ms.openlocfilehash: 47b7a3f4f523170f4dfb6f3ef674cecfdc0e157c
ms.sourcegitcommit: 24430258f363b7dd85f7067afd4565bf102b4a1f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2020
ms.locfileid: "10645331"
---
# Инструменты разработчика Microsoft Edge  

> [!NOTE]
> Microsoft Edge DevTools, чтобы веб-разработчики могли создавать и тестировать веб-сайты.  Если вы случайно открыли DevTools, просто нажмите " `F12` Закрыть".  

Microsoft Edge DevTools строится с помощью [TypeScript](https://www.typescriptlang.org/), на платформе [Open Source](https://github.com/Microsoft/ChakraCore), оптимизированных для современных рабочих процессов, и теперь оно доступно как [автономное приложение для Windows 10](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj) в Microsoft Store.

Чтобы узнать больше о последних возможностях, ознакомьтесь с [*DevTools в последнем обновлении Windows 10 (EdgeHTML 17)*](./devtools-guide/whats-new.md).

## Основные инструменты

![Microsoft Edge DevTools](./devtools-guide/media/devtools.png)

Microsoft Edge DevTools включает следующие возможности:

 - Панель " [**элементы**](./devtools-guide/elements.md) " для редактирования HTML и CSS, проверки свойств специальных возможностей, просмотра прослушивателей событий и установки контрольных точек изменений DOM
 - [**Консоль**](./devtools-guide/console.md) для просмотра и фильтрации сообщений журнала, проверки объектов JavaScript и узлов DOM, а также выполнения JavaScript в контексте выбранного окна или фрейма
 - [**Отладчик**](./devtools-guide/debugger.md) для пошагового использования кода, задания контрольных значений и точек останова, редактирование кода в реальном времени, проверка веб-хранилища и кэша файлов cookie.
 - Панель [**сети**](./devtools-guide/network.md) для мониторинга и проверки запросов и ответов из кэша сети и браузера 
 - Панель [**производительности**](./devtools-guide/performance.md) для профилирования времени и системных ресурсов, необходимых для вашего сайта
 - Панель [**памяти**](./devtools-guide/memory.md) для измерения использования ресурсов памяти и сравнения снимков кучи в разных состояниях выполнения кода
 - Панель [**эмуляции**](./devtools-guide/emulation.md) для проверки сайта с различными профилями браузера, разрешениями экрана и координатами местоположения GPS

Отправляйте [Отзывы и запросы функций](#feedback)!

> [!TIP]
> **[Протестируйте Microsoft Edge бесплатно из любого браузера](https://developer.microsoft.com/microsoft-edge/tools/remote/)**: мы [соBrowserStackся](https://www.browserstack.com/test-on-microsoft-edge-browser#live-cloud) с помощью этого приложения, чтобы предоставить бесплатный Live и автоматизированное тестирование в Microsoft Edge.

## Приложение Microsoft Store

**Microsoft Edge DevTools** [теперь доступен для предварительного просмотра](./devtools-guide/whats-new.md) в виде автономного [приложения для Windows 10 из Microsoft Store](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab), а также с помощью функции "in-browser ( `F12` )". В версии магазина есть панель *выбора* для присоединения к конечным объектам Open local и Remote Page, а также макет с вкладками для быстрого переключения между экземплярами DevTools.

### Локальная отладка

Чтобы выполнить отладку страницы локально, просто запустите приложение *Microsoft Edge DevTools* . На **локальной** панели средства выбора отобразятся все активные процессы содержимого EdgeHTML, включая открытые вкладки браузера EDGE, запуск [PWAs](./progressive-web-apps-edgehtml/index.md) (*WWAHost. exe* ) и [WebView](./webview.md) элементов управления. Щелкните требуемый конечный объект, чтобы прикрепить и открыть новый экземпляр вкладки DevTools.

![Локальная панель приложения DevTools](./devtools-guide/media/chooser_local.png)

### Удаленная отладка

Приложение *Microsoft Edge DevTools* предоставляет базовую поддержку для отладки страниц на удаленном компьютере с помощью нового [**протокола DevTools**](./devtools-protocol/index.md). В этом выпуске есть удаленный доступ к основным funtionality на панели [**отладчика**](./devtools-guide/debugger.md) , за вычетом проверки кэша (для веб-хранилища, рабочего процесса службы, кэша API и IndexedDB). Удаленная отладка ограничена *Microsoft Edge* для *настольных* компьютеров и поддерживает другие узлы EdgeHTML и устройства под управлением Windows 10, которые появятся в будущих выпусках.

Чтобы приступить к работе, ознакомьтесь с разделом [*Microsoft Edge DevTools*](./devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview) в документах [протоколов DevTools](./devtools-protocol/index.md) .

![Удаленная панель приложения DevTools](./devtools-guide/media/chooser_remote.png)

## Отзыв

Пожалуйста, отправьте нам свой отзыв, чтобы мы могли дальше усовершенствовать Microsoft Edge DevTools! Просто откройте инструменты ( `F12` ) и нажмите кнопку [**Отправить отзыв**](#microsoft-edge-developer-tools) .

Вы также можете добавлять на наш [форум UserVoice](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer/category/84475-f12-developer-tools) запросы на доступ к инструментам и переголосовать на них и стать участником программы [предварительной оценки Windows](https://insider.windows.com/) , чтобы ознакомиться с [новейшими возможностями,](./devtools-guide/whats-new.md)выпущенными DevTools. Используйте приложение **центра обратной связи** Windows, чтобы опубликовать, проголосовать, отслеживать и получать поддержку общих вариантов и проблем с Windows.

## Общие сочетания клавиш

Эти сочетания клавиш используются для управления основным окном DevTools и/или всеми инструментами.

Действие | Появивше
:------------ | :-------------
Показать или скрыть DevTools (открывается в последней просмотренной панели) | F12, Ctrl + Shift + I
Переключить закрепление (отстыковать/снизу или справа) | Ctrl + Shift + D 
Отображение нередактируемого исходного кода HTML в отладчике | Ctrl + U
Отображение и скрытие консоли в нижней части любого другого инструмента  | Ctrl +**`**
Переключиться на элементы (проводник DOM) | Ctrl + 1
Переключиться на консоль |  Ctrl + 2
Переход в режим отладчика | Ctrl + 3
Переключиться в сеть | Ctrl + 4
Переключение на производительность | Ctrl + 5
Переход в память | CTRL + 6
Переключение на эмуляцию | Ctrl + 7
Справочный документ | F1
Следующий инструмент | Ctrl + F6
Предыдущее средство | Ctrl + Shift + F6
Предыдущее средство (из истории) | Ctrl + Shift + [
Следующий инструмент (из истории) | Ctrl + Shift +]
Следующий подкадровый    | F6
Предыдущий подкадровый | Shift + F6
Следующее совпадение в поле поиска | F3
Предыдущее совпадение в поле поиска | Shift + F3
Поиск в поле поиска | CTRL+F
Перемещение фокуса на консоль в нижней части экрана | Alt + Shift + I
Инструменты закрепления и отстыковки (переключить закрепление) | CTRL+P  
Запустить DevTools на консоли | Ctrl + Shift + J
Обновите страницу. **Примечание.** при отладке и приостановке в точке останова выполняется сначала возобновление выполнения. | Ctrl + Shift + F5 или CTRL + R
