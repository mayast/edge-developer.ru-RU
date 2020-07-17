---
description: Протокол Microsoft Edge DevTools версии 0,2 поддерживает следующие конечные точки HTTP.
title: Конечные точки HTTP для протокола Microsoft Edge DevTools версии 0,2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: eb5b29e4d8149f511d8a7cbca3da72391a13e449
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882860"
---
# Конечные точки HTTP для протокола Microsoft Edge DevTools версии 0,2 (EdgeHTML)  

> [!NOTE]
> Версия 0,2 протокола Microsoft Edge DevTools работает только на [обновлениях для Windows 10 октября 2018]() и более поздних сборок для [предварительной оценки Windows](https://insider.windows.com/en-us/getting-started/) .

**Протокол DevTools 0,2** поддерживает следующие конечные точки HTTP. Дополнительные сведения о том, как подключаться к процессу содержимого браузера и по [доменам](domains/index.md) для всех API-интерфейсов Devtools, можно найти в разделе [использование протокола](../index.md#using-the-protocol) .

## /json/version
Сведения о браузере хост-компьютера и версии поддерживаемого им протокола DevTools.

**Параметры**

*Нет*

**Возвращаемый объект**

```json
{
    "Browser":"Edge/18.17763",
    "Protocol-Version":"0.2",
    "User-Agent":"Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/64.0.3282.140 Safari/537.36 Edge/18.17763"
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
