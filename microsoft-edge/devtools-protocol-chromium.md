---
description: Обновление протокола Microsoft Edge DevTools
title: Обновление протокола Microsoft Edge DevTools
author: zoherghadyali
ms.author: zoghadya
ms.date: 03/11/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: f1936a83f948dd17cc76139b7fd67fc73cd692d0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571701"
---
# Протокол DevTools Microsoft EDGE (Chromium)

При смене базовой веб-платформы Microsoft EDGE на Chromium [протокол DevTools Microsoft EDGE (EdgeHTML)](./devtools-protocol/index.md) не будет получать никаких обновлений. Протокол DevTools Microsoft EDGE (Chromium) будет соответствовать API-интерфейсам протокола Chrome DevTools, пересылаемых вперед. 

Документацию к этим доменам и методам можно найти, обратившись к [средству просмотра протоколов Chrome DevTools](https://chromedevtools.github.io/devtools-protocol/tot/).

> [!NOTE]
> Любые методы с префиксом, заданным `ms` в [протоколе Microsoft EDGE (EdgeHTML) DevTools](./devtools-protocol/index.md) , больше не поддерживаются протоколом Microsoft EDGE (Chromium) DevTools.

## Использование протокола DevTools

Вот как можно прикрепить клиентское средство управления к серверу DevTools в Microsoft EDGE (Chromium).

1. Убедитесь, что все экземпляры Microsoft EDGE (Chromium) закрыты.

2. Запустите Microsoft EDGE (Chromium) с портом удаленной отладки:

    ```
    msedge.exe --remote-debugging-port=9222
    ```

3. При необходимости вы можете при необходимости создать отдельный экземпляр Edge с использованием отдельного профиля пользователя.

    ```
    msedge.exe --user-data-dir=<some directory>
    ```

4. Затем используйте `list` конечную точку HTTP для получения списка конечных объектов страницы.

    ```
    http://localhost:9222/json/list
    ```

5. Наконец, подключитесь к `webSocketDebuggerUrl` нужному целевому объекту и выводите команды и подпишитесь на сообщения о событиях через сервер веб-сокета DevTools.

## Конечные точки HTTP протокола DevTools

Протокол DevTools Microsoft EDGE (Chromium) поддерживает следующие конечные точки HTTP.

## /json/version
Сведения о браузере хост-компьютера и версии поддерживаемого им протокола DevTools.

**Параметры**

*Нет*

**Возвращаемый объект**

```json
{
   "Browser": "Edg/75.0.115.0",
   "Protocol-Version": "1.3",
   "User-Agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/75.0.3739.0 Safari/537.36 Edg/75.0.115.0",
   "V8-Version": "7.5.98",
   "WebKit-Version": "537.36 (@68a98f73c7d0f766fb5a013ea7f8dbb41089bc1b)",
   "webSocketDebuggerUrl": "ws://localhost:9222/devtools/browser/a9d0e8cf-476a-4a89-bba9-0fc27ce691cd"
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
   "description": "",
   "devtoolsFrontendUrl": "/devtools/inspector.html?ws=localhost:9222/devtools/page/AB07C11A262D1EC8634EB12E2DCA4989",
   "id": "AB07C11A262D1EC8634EB12E2DCA4989",
   "title": "localhost:9222/json/protocol",
   "type": "page",
   "url": "http://localhost:9222/json/list",
   "webSocketDebuggerUrl": "ws://localhost:9222/devtools/page/AB07C11A262D1EC8634EB12E2DCA4989"
}, … ]
```

## /json/close

Закрывает целевой процесс (например, в Microsoft EDGE (Chromium), закрывает вкладку Page (страница).

**Параметры**

Идентификатор целевого объекта 

**Возвращаемый объект**

```
String(“Target is closing”)
```

## Удаленные инструменты для Microsoft EDGE (бета-версия)

Теперь вы можете установить [удаленные инструменты для Microsoft EDGE (бета-версия)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) из [Microsoft Store](https://www.microsoft.com/store/apps/windows). Это приложение позволяет осуществлять удаленную отладку Microsoft EDGE (Chromium), работающей на устройстве с Windows 10, с компьютера, на котором ведется разработка.

Чтобы узнать, как настроить устройство с Windows 10 и подключиться к нему с компьютера для разработки, ознакомьтесь с [этим учебником](./devtools-guide-chromium/remote-debugging/windows.md).

[Удаленные инструменты для Microsoft EDGE (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) используют один и тот же протокол DevTools Microsoft EDGE (Chromium) в качестве [DevTools](./devtools-guide-chromium.md) для общения с Microsoft EDGE на устройстве с Windows 10, на котором вы хотите выполнить отладку. Это приложение вставляется только `/msedge/` `pid` перед каждым вызовом к протоколу (в начале), а затем идентификаторе процесса (). Она поддерживает следующие конечные точки HTTP.

### /msedge/json/list

Список кандидатов всех `msedge.exe` процессов (включая [PWAs](./progressive-web-apps-chromium/index.md) и все вкладки во всех экземплярах Microsoft EDGE) на устройстве с Windows 10 для отладки.

**Параметры**

*Нет*

**Возвращаемый объект**

```json
[{
   "description": "",
    "devtoolsFrontendUrl": "http://172.17.75.195:80/msedge/7264/devtools/inspector.html?ws=172.17.75.195:80/msedge/7264/devtools/page/ED4FFDB4529723A0FAFCBDB9B45851BB",
    "faviconUrl": "https://docs.microsoft.com/favicon.ico",
    "id": "ED4FFDB4529723A0FAFCBDB9B45851BB",
    "title": "Get Started with Remote Debugging Windows 10 Devices - Microsoft Edge Development | Microsoft Docs",
    "type": "page",
    "url": "https://docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium/remote-debugging/windows",
    "webSocketDebuggerUrl": "ws://172.17.75.195:80/msedge/7264/devtools/page/ED4FFDB4529723A0FAFCBDB9B45851BB",
    "browserProcessId": 7264
}, … ]
```

### /msedge/

Функционально эквивалентен [/msedge/JSON/List](#msedgejsonlist). 

### /msedge/[PID]/JSON/List

Предоставляет список кандидатов на страницах для экземпляра Microsoft EDGE, соответствующий указанному `[pid]` для отладки.

**Параметры**

*Нет*

**Возвращаемый объект**

```json
[{
    "description": "",
    "devtoolsFrontendUrl": "http://172.17.75.195:80/msedge/7264/devtools/inspector.html?ws=172.17.75.195:80/msedge/7264/devtools/page/ED4FFDB4529723A0FAFCBDB9B45851BB",
    "faviconUrl": "https://docs.microsoft.com/favicon.ico",
    "id": "ED4FFDB4529723A0FAFCBDB9B45851BB",
    "title": "Get Started with Remote Debugging Windows 10 Devices - Microsoft Edge Development | Microsoft Docs",
    "type": "page",
    "url": "https://docs.microsoft.com/en-us/microsoft-edge/devtools-guide-chromium/remote-debugging/windows",
    "webSocketDebuggerUrl": "ws://172.17.75.195:80/msedge/7264/devtools/page/ED4FFDB4529723A0FAFCBDB9B45851BB"
}, … ]
```

### /msedge/[PID]/JSON/Version

Предоставляет сведения о экземпляре Microsoft EDGE, соответствующем предоставленному параметру, `[pid]` и какая версия поддерживаемого им протокола DevTools.

**Параметры**

*Нет*

**Возвращаемый объект**

```json
{
    "Browser": "Edg/82.0.452.0",
    "Protocol-Version": "1.3",
    "User-Agent": "Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/82.0.4080.0 Safari/537.36 Edg/82.0.452.0",
    "V8-Version": "8.2.263",
    "WebKit-Version": "537.36 (@fe0232051787ca94ac8edfc0084c3488b7d9bdb2)",
    "webSocketDebuggerUrl": "172.17.75.195:80/msedge/7264/devtools/browser/7a67c8c4-138b-48e3-bfe0-cb7af34d559a"
}
```

### /msedge/[PID]/JSON/Protocol/

Предоставляет весь интерфейс API протокола, сериализованный как JSON для экземпляра Microsoft EDGE, который соответствует предоставленному `[pid]` .

**Параметры**

*Нет*

**Возвращаемый объект**

Объект JSON, который представляет собой доступную поверхность API для версии протокола, которая используется в качестве экземпляра Microsoft EDGE, соответствующего указанному `[pid]` .
