---
description: Протокол Microsoft Edge DevTools версии 0,1 поддерживает следующие конечные точки HTTP.
title: Конечные точки HTTP протокола DevTools версии 0,1 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: a9d40772b8175790c034ee67236c4887d0831785
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882872"
---
# Конечные точки HTTP протокола DevTools версии 0,1 (EdgeHTML)  

> [!NOTE]
> Протокол Microsoft Edge DevTools работает только на [Windows 10 2018 апрельского обновления](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) и более поздних сборок для предварительной [оценки Windows](https://insider.windows.com/en-us/getting-started/) .

**Протокол DevTools 0,1** поддерживает следующие конечные точки HTTP. Дополнительные сведения о том, как подключаться к процессу содержимого браузера и по [доменам](domains/index.md) для всех API-интерфейсов Devtools, можно найти в разделе [использование протокола](../index.md#using-the-protocol) .

## /json/version
Сведения о браузере хост-компьютера и версии поддерживаемого им протокола DevTools.

**Параметры**

*Нет*

**Возвращаемый объект**

```json
{
    "Browser":"Edge/17.17627",
    "Protocol-Version":"0.1",
    "User-Agent":"Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/64.0.3282.140 Safari/537.36 Edge/17.17627"
}
```

## /json/protocol

Обеспечивает весь интерфейс API протокола, сериализованный как JSON.

**Параметры**

*Нет*

**Возвращаемый объект**

Объект JSON, который представляет доступную поверхность API для текущей версии протокола.

## /json/list

Список кандидатов на странице для отладки.

**Параметры**

*Нет*

**Возвращаемый объект**

```json
[{
    "id":"000001F5-87EE-4D55-0091-C4C08A1F30C8",
    "title":"Microsoft Edge Developer website - Microsoft Edge Development",
    "type":"Page",
    "url":"https://developer.microsoft.com/microsoft-edge/",
    "webSocketDebuggerUrl":"ws://localhost:9222/target/000001F5-87EE-4D55-0091-C4C08A1F30C8"
}, … ]
```

## /json/close

Закрывает целевой процесс (например, в Microsoft EDGE, закрывает вкладку страницы.)

**Параметры**

Идентификатор целевого объекта 

**Возвращаемый объект**

```
String("Target is closing")
```
