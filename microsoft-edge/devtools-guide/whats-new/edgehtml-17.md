---
description: Функции, добавленные в Microsoft Edge DevTools в обновлении для Windows 10 от 2018 апреля (EdgeHTML 17)
title: DevTools в EdgeHTML 17
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, edgehtml 17
ms.custom: seodec18
ms.openlocfilehash: cc110071422f858acf840c1eaf100696a6e3cf03
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571702"
---
# DevTools в обновлении для Windows 10 от 2018 апреля (EdgeHTML 17)

Выпуск EdgeHTML 17 DevTools поставляется двумя способами: в качестве традиционных `F12` инструментов для Microsoft EDGE и предварительного просмотра в виде автономного [приложения для Windows 10](#microsoft-edge-devtools-app-preview) из Microsoft Store!

Эти средства были обновлены с учетом ряда основных функций, в том числе базовой поддержки [удаленной отладки](../../devtools-guide.md#remote-debugging) (с помощью нашего нового [протокола DevTools](#devtools-protocol)), [функций отладки PWA](#pwa-debugging), [управления IndexedDB кэша](#indexeddb-inspection), [вертикальной стыковки](#docking-to-the-right-in-microsoft-edge) и других возможностей. Кроме того, мы постараемся, что все операции [рефакторинга](./edgehtml-16.md) , направленные на Последнее уничтожение, были запущены в рамках текущих инвестиций в производительность и надежность.

Ниже приведены последние компоненты Microsoft Edge DevTools, которые были [выпущены в обновлении для Windows 10 от 2018 апреля](/windows/uwp/whats-new/windows-10-build-17134) ([EdgeHTML 17](https://aka.ms/devguide_edgehtml_17)).

## Предварительная версия приложения Microsoft Edge DevTools

![Приложение Microsoft Edge DevTools](../../devtools-protocol/media/microsoft-edge-devtools.png) 

[**Microsoft Edge DevTools**](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) теперь доступен для предварительного просмотра в виде автономного приложения для Windows 10 из Microsoft Store. В версии магазина есть панель *выбора* для присоединения к конечным объектам Open local и Remote Page, а также макет с вкладками для быстрого переключения между экземплярами DevTools. Кроме того, в приложении DevTools можно выполнять отладку веб-содержимого в приложениях (например, надстроек для Office, Кортаны, EdgeHTML [WebView](../../webview.md)и [Windows-Install PWAs](../../progressive-web-apps-edgehtml/windows-features.md)).

Edge DevTools также по-прежнему доступен в `F12` браузере (без панели Chooser).

Отделение DevTools от браузера обеспечивает следующие преимущества UX и архитектуры:

- DevTools работает в отдельной изолированной программной среде контейнера приложения из Microsoft EDGE, обеспечивая более надежную надежность для обоих типов.
- Приложение обеспечивает простой переход между вкладками активных экземпляров DevTools (вместо того чтобы переключаться между открытыми вкладками Microsoft EDGE).
- Мы можем проинструментировать обработчик браузера *EdgeHTML* и открыть его в более крупной экосистеме Devtools с помощью [API-интерфейсов из нескольких браузеров](https://github.com/WICG/devtools-protocol/).
- Мы можем отгрузить обновления DevTools независимо от цикла выпуска Windows (и EdgeHTML).

Дополнительные сведения о [локальной и удаленной отладке с помощью приложения DevTools](../../devtools-guide.md)вы также ознакомьтесь с *руководством по DevTools* .

## Протокол DevTools

Средства разработчика могут использовать [**протокол Microsoft Edge DevTools**](../../devtools-protocol/index.md) для проверки и отладки браузера Microsoft Edge. Она предоставляет набор методов и событий, упорядоченных в разных [доменах](../../devtools-protocol/0.1/domains/index.md) инструментария ядра EdgeHTML.

 Клиенты инструментария могут вызывать эти методы и отслеживать эти события с помощью сообщений веб-сокетов JSON, пересылаемых на *сервер DevTools* , размещенный в Microsoft EDGE или на [портале устройств с Windows](/windows/mixed-reality/using-the-windows-device-portal). 
 
 Microsoft Edge DevTools использует этот протокол для разрешения [удаленной отладки](../../devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview) хост-компьютера, на котором работает Microsoft EDGE, из [автономного клиента DevTools](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj) , доступного из Microsoft Store. В настоящее время поддержка предварительной версии ограничена разделом отладка на другом крае другого настольного устройства или ВМ. С течением времени мы добавим поддержку полного набора DevTools для любого экземпляра EdgeHTML на любом устройстве с Windows 10.  
 
 Последние сборки [**Visual Studio Preview**](https://www.visualstudio.com/vs/preview/) (visual Studio 15,7 Preview 1 или более поздней версии) используйте протокол DevTools, чтобы разрешить запуск и отладку Microsoft EDGE (код JavaScript) в Visual Studio IDE любого базового проекта ASP.NET или .NET.

## Проверка IndexedDB

Новые возможности [**отладчика**](../debugger.md) . Этот выпуск — это [Диспетчер IndexedDB](../storage.md#indexeddb-manager) , который поддерживает проверку и обновление хранилищ объектов и удаление отдельных записей ключа. Ожидается еще больше функций в будущих выпусках.

## Отладка PWA

Поддержка отладки последовательного веб-приложения (PWAs) теперь включена по умолчанию, предоставляя вкладки инструментов для [**сотрудников служб**](../service-workers.md), [**API кэша**](../storage.md#cache-manager)и управления [**IndexedDB**](../storage.md#indexeddb-manager) .

Кроме того, на [панели инструментов "сеть](../network.md#toolbar) " есть кнопка "создать", **обход рабочего процесса для всех сетевых запросов**, чтобы включить или отключить служебные сотрудники как сетевые прокси-серверы:

![Кнопка панели инструментов "сеть": обход рабочего процесса для всех сетевых запросов](../media/network_toolbar_bypass_sw.png)

Вы можете выполнить отладку [PWA как установленное приложение для Windows 10](../../progressive-web-apps-edgehtml/windows-features.md) , выбрав его из списка [**локальных**](../../progressive-web-apps-edgehtml/windows-features.md#debug-your-pwa-edgehtml-as-a-windows-app) целей (вкладка браузера/PWA/WebView) в средстве выбора [автономного приложения DevTools](../../devtools-guide.md#microsoft-store-app).  

## Закрепление справа в Microsoft Edge

Теперь вы можете закрепить DevTools справа от страницы, которую вы отлаживается в Microsoft EDGE, помимо закрепления в нижней части экрана и отстыковки DevTools из окна браузера. Используется `Ctrl+Shift+D` для циклического перехода между положением **Dock**, **наброской вправо**и **откреплением** , а также значками в правом верхнем углу DevTools:

![Параметры стыковки DevTools (в незакрепленном состоянии)](../media/docking_buttons.png) 
