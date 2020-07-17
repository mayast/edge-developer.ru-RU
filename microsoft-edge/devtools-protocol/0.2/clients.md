---
description: Протокол Microsoft Edge DevTools, версия 0,2, поддерживает указанные ниже клиентские средства.
title: Клиенты Microsoft Edge DevTools Protocol версии 0,2 (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 92976de257a73fd7206205622a4c79d1277b3950
ms.sourcegitcommit: a06c86ef7c69e1e400a0be5938449f3c4ba6ec72
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/16/2020
ms.locfileid: "10882893"
---
# Клиенты Microsoft Edge DevTools Protocol версии 0,2 (EdgeHTML)  

> [!NOTE]
> Версия 0,2 протокола Microsoft Edge DevTools работает только на [обновлениях для Windows 10 октября 2018](/windows/uwp/whats-new/windows-10-build-17763) и более поздних сборок для [предварительной оценки Windows](https://insider.windows.com/en-us/getting-started/) .  

**Протокол DevTools 0,2** поддерживает указанные ниже клиентские средства.

[ ![ Microsoft Edge DevTools предварительный просмотр](../media/microsoft-edge-devtools.png)](#microsoft-edge-devtools-preview) [ ![ кода Visual Studio](../media/visual-studio-code.png)](#visual-studio-code) [ ![ Microsoft Visual Studio 15,8](../media/visual-studio-2017.png)](#microsoft-visual-studio)

## Предварительный просмотр средств разработчика в Microsoft Edge

Вы можете использовать автономное приложение [**Microsoft Edge DevTools Preview**](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) из Microsoft Store для удаленной отладки основного устройства под управлением Microsoft EDGE ([EdgeHTML 17](../../dev-guide.md) или более поздней версии).

Версия 0,2 протокола DevTools предоставляет новые домены для отладки стилей и макетов и API консоли в дополнение к функциональным возможностям отладки скриптов, представленным в версии 0,1. В пользовательском интерфейсе DevTools это преобразуется в функциональные возможности, доступные на панелях [**элементы**](../../devtools-guide/elements.md), [**консоль**](../../devtools-guide/console.md) и [**отладчик**](../../devtools-guide/debugger.md) . В настоящее время удаленная отладка Microsoft Edge ограничена для настольных компьютеров, и поддержка других устройств с Windows 10, которые поступают в будущих выпусках.

Вот как можно настроить удаленную отладку с помощью предварительной версии приложения Microsoft Edge DevTools. Протокол DevTools версии 0,2 требует установки [Windows 10 октября 2018](/windows/uwp/whats-new/windows-10-build-17763) или более поздней сборки предварительной оценки для Windows на компьютере Host (отлаживаемого). Приложение DevTools Preview (используется на компьютере отладчика) будет работать в Windows 10 версии 16299 (обновление для Windows 10 для дизайнеров, 10/2017) или более позднюю версию.

**На компьютере с ведущим (отлаживаемого) компьютером...**

1. Если вы находитесь в сети Wi-Fi, убедитесь, что сеть помечена как **domain** или **Private**. Чтобы проверить это, откройте приложение [**Центр безопасности защитника Windows**](/windows/security/threat-protection/windows-defender-security-center/windows-defender-security-center) , щелкните **брандмауэр & защиту сети** и проверьте, указана ли сеть в качестве *доменной сети* или *частной сети*. 

    Если в списке *общедоступный*, перейдите в раздел **Параметры**  >  **& сети**  >  **Wi-Fi**, щелкните свою сеть и переключитесь на кнопку *Network Profile* ( **Частная**).

2. Откройте панель управления " **для разработчиков** " в разделе " *Параметры* Windows" (Найдите для *разработчика* и щелкните " *Использование функций разработчика*"), а также: 

    а. Включить или выключить **режим разработчика**. При этом будет установлен пакет *режима разработчика* , позволяющий удаленное средство для рабочего стола.

    б. Включите [**портал устройств**](/windows/uwp/debug-test-perf/device-portal) (*включите удаленную диагностику через локальную сеть*) и **обнаружение устройств** (*Сделайте устройство видимым для USB-подключений и локальной сети*).

    в. Включите **проверку подлинности** и введите имя пользователя и пароль.

    г. Обратите внимание на экран IP-адрес компьютера и порт подключения (50443).

3. Откройте в Microsoft Edge вкладки, которые вы хотите отладить на клиентском компьютере.

**На клиентском компьютере (отладчике)...**

1.  Установите и запустите автономное приложение [Microsoft Edge DevTools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) из Microsoft Store.

2. Откройте **удаленную** панель и введите сетевое расположение (URL-адрес и порт) хост-компьютера и нажмите кнопку **подключить**.

3. **Установите** сертификат хост-компьютера в появившемся диалоговом окне *недоверенный сертификат* .

4. Укажите имя пользователя и пароль, которые вы определили для проверки подлинности портала устройства.

5. *Удаленная* панель загрузит список целевых объектов страниц, которые могут быть отлажены, на хост-компьютере. Выберите один из них, чтобы запустить отладку.

6. Используйте кнопку " **Обновить** " для обновления и повторной загрузки списка целевых объектов удаленной страницы на хост-компьютере. Нажмите кнопку " **Отключить** ", чтобы вернуться к экрану *Подключение к удаленному устройству* и присоединиться к другому узлу.

## Visual Studio Code

С помощью [отладчика для](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) расширения кода EDGE Вы можете отлаживать сценарий, который выполняется в Microsoft EDGE, прямо в коде Visual Studio. Расширение требует обслуживания веб-приложения с localhost, которое можно начать из командной строки или [задачи](https://code.visualstudio.com/docs/editor/tasks).

Для начала сделайте следующее:

1. Установите [отладчик для](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) расширения кода Edge.

2. Перезапустите программу VS, откройте папку, содержащую проект, для которого вы хотите выполнить отладку, и установите точки останова в коде.

3. Настройте [задачу запуска](https://code.visualstudio.com/docs/editor/debugging#_launch-configurations) localhost, чтобы открыть нужную страницу проекта: **Отладка**  >  **добавления конфигурации..**.. Например:

    ```json
    {
        "version": "0.2.0",
        "configurations": [

            {
                "name": "Launch localhost",
                "type": "edge",
                "request": "launch",
                "url": "http://localhost/mypage.html",
                "webRoot": "${workspaceFolder}/wwwroot"
            }
        ]
    }
    ```

    [*С помощью отладчика*](https://github.com/Microsoft/vscode-edge-debug2#using-the-debugger) больше не заданные параметры настройки запуска. 

4. Запустите сервер на локальном компьютере и нажмите кнопку " **запустить отладку** (воспроизвести)" или `F5` Запустите Microsoft Edge. При попадании в точку останова вы будете прерываться на код VS и проанализировать код от него.

Дополнительные сведения можно найти в руководстве по [отладке кода VS для Microsoft Edge](https://github.com/Microsoft/vscode-edge-debug2#----vs-code---debugger-for-microsoft-edge--) .

## Microsoft Visual Studio

Если вы используете последнюю версию [**Visual Studio**](https://www.visualstudio.com) (visual Studio 15,8 или более поздней версии), которая выполняется в [Windows 10 октября 2018](/windows/uwp/whats-new/windows-10-build-17763)г., вы можете запускать и отлаживать Microsoft Edge из интегрированной среды разработки для любого проекта ASP.NET или .NET.

Вот как можно настроить отладку Microsoft Edge с помощью Visual Studio:

1.  Установите и запустите последнюю версию [**Visual Studio**](https://www.visualstudio.com/) (visual Studio 15,8 или более поздней версии).

2. Открытие существующего основного проекта ASP.NET или .NET или **Создание нового проекта...** использование одного из шаблонов **Visual C#** .NET.

3. В **обозревателе решений**проекта откройте файлы JavaScript, которые вы хотите отладить, и установите точки останова в интерфейсе IDE так же, как и в случае с кодом на стороне сервера.

4. Нажмите `F5` , чтобы запустить Microsoft EDGE, на котором запущен сервер DevTools. При попадании в точку останова вы перейдете в Visual Studio и сможете проанализировать код и прокрутить его.
