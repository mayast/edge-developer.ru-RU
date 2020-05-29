---
description: Используйте протокол Microsoft Edge DevTools для проверки и отладки браузера Microsoft EDGE (EdgeHTML).
title: Протокол Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/11/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: 8bef24c98dae284f2111f6a16fca4a6f27c89dc4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571659"
---
# Протокол DevTools Microsoft EDGE (EdgeHTML)

> [!NOTE]
> Протокол DevTools Microsoft EDGE (EdgeHTML) работает только в [Windows 10 апрель 2018](https://blogs.windows.com/windowsexperience/2018/04/30/how-to-get-the-windows-10-april-2018-update/#5VXkQMU41CJzZPER.97) и более поздних сборках.

Средства разработчика могут использовать **протокол DevTools Microsoft EDGE (EdgeHTML)** для проверки и отладки браузера Microsoft EDGE (EdgeHTML). Она предоставляет набор методов и событий, упорядоченных в разных [доменах](0.2/domains/index.md) инструментария ядра EdgeHTML.

 Клиенты с поддержкой инструментария могут вызывать эти методы и отслеживать эти события с помощью сообщений веб-сокетов JSON, пересылаемых на *сервер DevTools* , размещенный в Microsoft EDGE (EdgeHTML) или на портале устройств с Windows. Microsoft EDGE (EdgeHTML) DevTools использует этот протокол для разрешения [удаленной отладки](0.2/clients.md#microsoft-edge-devtools-preview) хост-компьютера, на котором работает Microsoft EDGE (EdgeHTML), из автономного клиента DevTools, доступного из [Microsoft Store](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj).

Протокол DevTools Microsoft EDGE (EdgeHTML) предназначен для тесного выравнивания по протоколу Chrome DevTools ( [для протоколов WICG в DevTools](https://github.com/WICG/devtools-protocol/)), хотя в этом выпуске есть известные промежутки между взаимозаменяемостью.

## Использование протокола

Вот как можно прикрепить клиентское средство управления к серверу DevTools в Microsoft EDGE (EdgeHTML). Если вы используете Microsoft Edge DevTools в качестве клиента, ознакомьтесь с инструкциями по [удаленной отладке](0.2/clients.md#microsoft-edge-devtools-preview) .

1. Запустите Microsoft EDGE (EdgeHTML) с открытым портом удаленной отладки, указав URL-адрес, который вы хотите открыть. Пример

    ```
    MicrosoftEdge.exe --devtools-server-port 9222 https://www.bing.com
    ```

    Если элемент EDGE уже запущен, параметр URL-адрес является необязательным. Рядом с адресной строкой браузера появится кнопка, указывающая на то, что **сервер средств разработчика** запущен.

    ![Сервер средств разработчика](media/developer-tools-server.png) 

2. Используйте эту [конечную точку HTTP](0.2/http.md) для получения списка целевых объектов страниц:

    ```
    http://localhost:9222/json/list
    ```

3. Подключитесь к списку `webSocketDebuggerUrl` нужной страницы, чтобы выполнить дальнейшие [команды протокола](0.2/domains/index.md) и получать сообщения о событиях через сокет-сервер Devtools.

## Состояние и отзывы

[Версия 0,2](0.2/index.md) протокола DevTools предоставляет новые домены для работы со стилями и разметкой (только для чтения) и консольными API в дополнение к основным функциям отладки скриптов, представленным в [версии 0,1](0.1/index.md). В пользовательском интерфейсе Microsoft Edge DevTools это преобразуется в функциональные возможности, доступные на панелях [**элементы**](../devtools-guide/elements.md), [**консоль**](../devtools-guide/console.md) и [**отладчик**](../devtools-guide/debugger.md) .

Благодарим вас за то, что поedge DevTools Protocol! Мы будем рады узнать ваше мнение по адресу:

 - [**Разработчик Microsoft Edge для разработчиков UserVoice**](https://wpdev.uservoice.com/forums/257854-microsoft-edge-developer?category_id=84475): идеи и запросы по функциям DevTools

 - [**Средство отслеживания проблем EdgeHTML**](https://developer.microsoft.com/microsoft-edge/platform/issues/): протокол, DevTools и EdgeHTML ошибки и проблемы с платформой.

 - [**Центр отзывов Microsoft Edge DevTools**](feedback-hub:?referrer=microsoftEdge&tabID=2&newFeedback=true&ContextId=344): проблемы с протоколом и DevTools и предложениями в приложении "центр отзывов"

## Вопросы и ответы

#### Может ли несколько клиентов подключаться к одному и тому же серверу DevTools?
Нет, не одновременно, когда клиенты находятся в процессе отладки. Последний клиент для подключения будет отключаться из предыдущего. В будущем при поддержке дополнительных средств они могут поддерживать одновременные подключения клиентов.

#### Нужно ли использовать 9222 в качестве порта сервера DevTools?
Нет. Вы можете указать любой порт, но не забудьте выбрать тот, который еще не используется. Порт 9222 для удаленной отладки используется в соответствии с соглашением.

#### Как подключить клиентское средство управления к Microsoft EDGE (EdgeHTML), на котором работает сервер DevTools?
Чтобы присоединиться к Microsoft EDGE (EdgeHTML), работающей на локальном компьютере, ознакомьтесь с инструкциями по [*протоколу,*](#using-the-protocol) описанным выше. Если вы собираетесь поддерживать удаленную отладку, вам потребуется обменять рабочий процесс для установки SSL-сертификата узла на клиентском компьютере, например, с помощью диалогового окна установки, как [Microsoft Edge DevTools в предварительной версии](./0.2/clients.md#microsoft-edge-devtools-preview) .

#### Если я использую удаленную отладку с помощью EDGE DevTools, нужно запустить процесс хост-браузера с помощью переключателя *командной строки DevTools-Port (сервер-порт* ). 
Нет. Если вы настраиваете [удаленную отладку с помощью Microsoft Edge DevTools Preview](./0.2/clients.md#microsoft-edge-devtools-preview), `--devtools-server-port` параметр командной строки не нужен для начального края. В этом случае на *портале устройств* Windows размещается сервер DevTools от имени браузера.

#### Можно ли использовать протокол Edge DevTools для удаленной отладки процесса WWAHost. exe или WebView?
Протокол Edge DevTools в настоящее время поддерживает только вкладки браузера. Процессы WWAHost. exe и WebView не поддерживаются.
