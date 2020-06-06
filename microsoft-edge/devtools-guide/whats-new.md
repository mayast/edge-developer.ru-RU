---
description: Узнайте о новых возможностях Microsoft Edge DevTools в обновлении для Windows 10 от 2018 октября
title: Новые возможности Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, edgehtml 18
ms.custom: RS5, seodec18
ms.openlocfilehash: 604419f4c77ccaaf2dfd3179273be803cde86fc8
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571708"
---
# DevTools в новейшем обновлении для Windows 10 (EdgeHTML 18)

Последнее обновление Microsoft Edge DevTools позволяет получить ряд специальных возможностей в пользовательском интерфейсе и, в частности, новые специальные панели для [*рабочих процессов*](#service-workers-panel) и [*хранения*](#storage-panel), средства [поиска файлов](#source-file-search-tools) исходного кода в отладчике и новые [домены протоколов пограничного DevTools](#edge-devtools-protocol-updates) для отладки стиля и макета и API консоли.

Ниже приведены последние компоненты Microsoft Edge DevTools, доступные в обновлении для [Windows 10 от 2018 октября](/windows/uwp/whats-new/windows-10-build-17763) ([EdgeHTML 18](https://aka.ms/devguide_edgehtml_18)). Кроме того, мы также исправлены некоторые ошибки, связанные со специальными возможностями, надежностью и производительностью, для улучшения основ!

## Приложение DevTools

Мы обновили отдельное [приложение Microsoft Edge DevTools Preview](../devtools-guide.md#microsoft-store-app). Последний выпуск включает в себя доступ для удаленной отладки к основным funtionality в [**отладчике**](./debugger.md), [**элементах**](./elements.md) (для операций только для чтения) и на панелях [**консоли**](./console.md) .

## Панель "работники обслуживания"

Теперь на экране выделена область [**сотрудников службы**](./service-workers.md) для проверки, управления и отладки рабочих процессов сайта. Это обеспечивает те же функциональные возможности, что и ранее в панели *отладчика* (теперь с меньшим пределами пользовательского интерфейса!).

![Панель "работники обслуживания"](./media/service_worker.png)

## Панель "хранилище"

Мы также переместили все локальные инспекторы хранилища (*локальные и Sesion хранилище, IndexedDB, cookie-файлы*), которые ранее находятся в *отладчике* , на собственную выделенную панель [**хранилища**](./storage.md) .

![Панель "хранилище"](./media/storage_cache.png)

## Средства поиска файлов исходного кода

В [**отладчике**](./debugger.md) теперь есть область [поиска файлов исходного кода](./debugger.md#file-search) . Откройте файл с помощью команды *найти в файлах* ( `Ctrl` + `Shift` + `F` ), если вы пытаетесь найти в исходном коде определенную строку. На панели инструментов находятся различные параметры поиска, в том числе регулярные выражения. 

![Поиск файлов отладчика](./media/debugger_file_search.png)

Кроме того, вы можете быстро открыть любой загруженный исходный файл с помощью команды *Открыть файл* ( `Ctrl` + `P` ).

![Открытие файла отладчика](./media/debugger_open_file.png)

## Обновления протокола DevTools Edge

[Версия 0,2](../devtools-protocol/0.2/index.md) протокола DevTools предоставляет новые домены для работы со стилями и разметкой (только для чтения) и консольными API в дополнение к основным функциям отладки скриптов, представленным в [версии 0,1](../devtools-protocol/0.1/index.md). В пользовательском интерфейсе Edge DevTools это преобразуется в функции, доступные в [**элементах**](../devtools-guide/elements.md) (для операций только на чтение), [**консоли**](../devtools-guide/console.md) и панели [**отладчика**](../devtools-guide/debugger.md) .