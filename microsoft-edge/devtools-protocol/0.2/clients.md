---
description: Протокол Microsoft Edge DevTools, версия 0,2, поддерживает указанные ниже клиентские средства.
title: Клиенты Microsoft Edge DevTools Protocol версии 0,2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.custom: seodec18
ms.openlocfilehash: 657d594b85c47cc1d5c80b8f2ac3ecc4bd4e4502
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571682"
---
# <span data-ttu-id="2a7ce-103">Клиенты протоколов DevTools</span><span class="sxs-lookup"><span data-stu-id="2a7ce-103">DevTools Protocol Clients</span></span>

> [!NOTE]
> <span data-ttu-id="2a7ce-104">Версия 0,2 протокола Microsoft Edge DevTools работает только на [обновлениях для Windows 10 октября 2018](/windows/uwp/whats-new/windows-10-build-17763) и более поздних сборок для [предварительной оценки Windows](https://insider.windows.com/en-us/getting-started/) .</span><span class="sxs-lookup"><span data-stu-id="2a7ce-104">Version 0.2 of the Microsoft Edge DevTools Protocol works only on the [Windows 10 October 2018 Update](/windows/uwp/whats-new/windows-10-build-17763) and later [Windows Insider Preview](https://insider.windows.com/en-us/getting-started/) builds.</span></span>  

<span data-ttu-id="2a7ce-105">**Протокол DevTools 0,2** поддерживает указанные ниже клиентские средства.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-105">**DevTools Protocol 0.2** supports the following tooling clients.</span></span>

<span data-ttu-id="2a7ce-106">[ ![ Microsoft Edge DevTools предварительный просмотр](../media/microsoft-edge-devtools.png)](#microsoft-edge-devtools-preview) [ ![ кода Visual Studio](../media/visual-studio-code.png)](#visual-studio-code) [ ![ Microsoft Visual Studio 15,8](../media/visual-studio-2017.png)](#microsoft-visual-studio)</span><span class="sxs-lookup"><span data-stu-id="2a7ce-106">[![Microsoft Edge DevTools Preview](../media/microsoft-edge-devtools.png)](#microsoft-edge-devtools-preview) [![Visual Studio Code](../media/visual-studio-code.png)](#visual-studio-code) [![Microsoft Visual Studio 15.8](../media/visual-studio-2017.png)](#microsoft-visual-studio)</span></span>

## <span data-ttu-id="2a7ce-107">Предварительная версия DevTools Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="2a7ce-107">Microsoft Edge DevTools Preview</span></span>

<span data-ttu-id="2a7ce-108">Вы можете использовать автономное приложение [**Microsoft Edge DevTools Preview**](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) из Microsoft Store для удаленной отладки основного устройства под управлением Microsoft EDGE ([EdgeHTML 17](../../dev-guide.md) или более поздней версии).</span><span class="sxs-lookup"><span data-stu-id="2a7ce-108">You can use the standalone [**Microsoft Edge DevTools Preview**](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) Windows 10 app from the Microsoft Store to remotely debug a host device running Microsoft Edge ([EdgeHTML 17](../../dev-guide.md) or later).</span></span>

<span data-ttu-id="2a7ce-109">Версия 0,2 протокола DevTools предоставляет новые домены для отладки стилей и макетов и API консоли в дополнение к функциональным возможностям отладки скриптов, представленным в версии 0,1.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-109">Version 0.2 of the DevTools Protocol provides new domains for style and layout debugging and console APIs, in addition to the core script debugging functionality introduced in Version 0.1.</span></span> <span data-ttu-id="2a7ce-110">В пользовательском интерфейсе DevTools это преобразуется в функциональные возможности, доступные на панелях [**элементы**](../../devtools-guide/elements.md), [**консоль**](../../devtools-guide/console.md) и [**отладчик**](../../devtools-guide/debugger.md) .</span><span class="sxs-lookup"><span data-stu-id="2a7ce-110">In the Edge DevTools UI, this translates to functionality available in the [**Elements**](../../devtools-guide/elements.md), [**Console**](../../devtools-guide/console.md) and [**Debugger**](../../devtools-guide/debugger.md) panels.</span></span> <span data-ttu-id="2a7ce-111">В настоящее время удаленная отладка Microsoft Edge ограничена для настольных компьютеров, и поддержка других устройств с Windows 10, которые поступают в будущих выпусках.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-111">Currently Microsoft Edge remote debugging is limited to desktop hosts, with support for other Windows 10 devices coming in future releases.</span></span>

<span data-ttu-id="2a7ce-112">Вот как можно настроить удаленную отладку с помощью предварительной версии приложения Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-112">Here's how to set up remote debugging with the Microsoft Edge DevTools Preview app.</span></span> <span data-ttu-id="2a7ce-113">Протокол DevTools версии 0,2 требует установки [Windows 10 октября 2018](/windows/uwp/whats-new/windows-10-build-17763) или более поздней сборки предварительной оценки для Windows на компьютере Host (отлаживаемого).</span><span class="sxs-lookup"><span data-stu-id="2a7ce-113">The DevTools Protocol version 0.2 requires [Windows 10 October 2018 Update](/windows/uwp/whats-new/windows-10-build-17763) or a later Windows Insider Preview build on the host (debugee) machine.</span></span> <span data-ttu-id="2a7ce-114">Приложение DevTools Preview (используется на компьютере отладчика) будет работать в Windows 10 версии 16299 (обновление для Windows 10 для дизайнеров, 10/2017) или более позднюю версию.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-114">The Edge DevTools Preview app (used on the debugger machine) will run on Windows 10 version 16299 (Windows 10 Fall Creators Update, 10/2017) or higher.</span></span>

**<span data-ttu-id="2a7ce-115">На компьютере с ведущим (отлаживаемого) компьютером...</span><span class="sxs-lookup"><span data-stu-id="2a7ce-115">On the host (debugee) machine...</span></span>**

1. <span data-ttu-id="2a7ce-116">Если вы находитесь в сети Wi-Fi, убедитесь, что сеть помечена как **domain** или **Private**.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-116">If you're on a WiFi network, ensure the network is marked as either **Domain** or **Private**.</span></span> <span data-ttu-id="2a7ce-117">Чтобы проверить это, откройте приложение [**Центр безопасности защитника Windows**](/windows/security/threat-protection/windows-defender-security-center/windows-defender-security-center) , щелкните **брандмауэр & защиту сети** и проверьте, указана ли сеть в качестве *доменной сети* или *частной сети*.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-117">You can verify this by opening the [**Windows Defender Security Center**](/windows/security/threat-protection/windows-defender-security-center/windows-defender-security-center) app, clicking on **Firewall & network protection** and checking if your network is listed as a *Domain network* or *Private network*.</span></span> 

    <span data-ttu-id="2a7ce-118">Если в списке *общедоступный*, перейдите в раздел **Параметры**  >  **& сети**  >  **Wi-Fi**, щелкните свою сеть и переключитесь на кнопку *Network Profile* ( **Частная**).</span><span class="sxs-lookup"><span data-stu-id="2a7ce-118">If its listed as *Public*, go to **Settings** > **Network & Internet** > **Wi-Fi**, click on your network and toggle the *Network profile* button to **Private**.</span></span>

2. <span data-ttu-id="2a7ce-119">Откройте панель управления " **для разработчиков** " в разделе " *Параметры* Windows" (Найдите для *разработчика* и щелкните " *Использование функций разработчика*"), а также:</span><span class="sxs-lookup"><span data-stu-id="2a7ce-119">Open the **For developers** control panel in Windows *Settings* (search for *developer* and click on *Use developer features*), and:</span></span> 

    <span data-ttu-id="2a7ce-120">А.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-120">a.</span></span> <span data-ttu-id="2a7ce-121">Включить или выключить **режим разработчика**.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-121">Toggle on **Developer Mode**.</span></span> <span data-ttu-id="2a7ce-122">При этом будет установлен пакет *режима разработчика* , позволяющий удаленное средство для рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-122">This will install the *Developer Mode* package, enabling remote tooling for desktop.</span></span>

    <span data-ttu-id="2a7ce-123">Б.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-123">b.</span></span> <span data-ttu-id="2a7ce-124">Включите [**портал устройств**](/windows/uwp/debug-test-perf/device-portal) (*включите удаленную диагностику через локальную сеть*) и **обнаружение устройств** (*Сделайте устройство видимым для USB-подключений и локальной сети*).</span><span class="sxs-lookup"><span data-stu-id="2a7ce-124">Enable [**Device Portal**](/windows/uwp/debug-test-perf/device-portal) (*Turn on remote diagnostics over local area network connections*) and **Device discovery** (*Make your device visible to USB connections and your local network*).</span></span>

    <span data-ttu-id="2a7ce-125">в.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-125">c.</span></span> <span data-ttu-id="2a7ce-126">Включите **проверку подлинности** и введите имя пользователя и пароль.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-126">Turn on **Authentication** and supply a username / password.</span></span>

    <span data-ttu-id="2a7ce-127">г.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-127">d.</span></span> <span data-ttu-id="2a7ce-128">Обратите внимание на экран IP-адрес компьютера и порт подключения (50443).</span><span class="sxs-lookup"><span data-stu-id="2a7ce-128">Note the machine IP address and connection port (50443) displayed.</span></span>

3. <span data-ttu-id="2a7ce-129">Откройте в Microsoft Edge вкладки, которые вы хотите отладить на клиентском компьютере.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-129">Open tabs in Microsoft Edge that you wish to debug from the client machine.</span></span>

**<span data-ttu-id="2a7ce-130">На клиентском компьютере (отладчике)...</span><span class="sxs-lookup"><span data-stu-id="2a7ce-130">On the client (debugger) machine...</span></span>**

1.  <span data-ttu-id="2a7ce-131">Установите и запустите автономное приложение [Microsoft Edge DevTools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) из Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-131">Install and launch the standalone [Microsoft Edge DevTools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) app from the Microsoft Store.</span></span>

2. <span data-ttu-id="2a7ce-132">Откройте **удаленную** панель и введите сетевое расположение (URL-адрес и порт) хост-компьютера и нажмите кнопку **подключить**.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-132">Open the **Remote** panel and enter the network location (URL and port) of the host machine and click **Connect**.</span></span>

3. <span data-ttu-id="2a7ce-133">**Установите** сертификат хост-компьютера в появившемся диалоговом окне *недоверенный сертификат* .</span><span class="sxs-lookup"><span data-stu-id="2a7ce-133">**Install** the host machine's certificate from the *Untrusted Certificate* dialog that appears.</span></span>

4. <span data-ttu-id="2a7ce-134">Укажите имя пользователя и пароль, которые вы определили для проверки подлинности портала устройства.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-134">Supply the username/password you designated for Device Portal authentication.</span></span>

5. <span data-ttu-id="2a7ce-135">*Удаленная* панель загрузит список целевых объектов страниц, которые могут быть отлажены, на хост-компьютере.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-135">The *Remote* panel will load a list of debuggable page targets on the host machine.</span></span> <span data-ttu-id="2a7ce-136">Выберите один из них, чтобы запустить отладку.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-136">Select one to start debugging.</span></span>

6. <span data-ttu-id="2a7ce-137">Используйте кнопку " **Обновить** " для обновления и повторной загрузки списка целевых объектов удаленной страницы на хост-компьютере.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-137">Use the **Refresh** button to update and reload the list of remote page targets on the host machine.</span></span> <span data-ttu-id="2a7ce-138">Нажмите кнопку " **Отключить** ", чтобы вернуться к экрану *Подключение к удаленному устройству* и присоединиться к другому узлу.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-138">Click the **Disconnect** button to return to the *Connect to a remote device* screen and attach to a different host.</span></span>

## <span data-ttu-id="2a7ce-139">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="2a7ce-139">Visual Studio Code</span></span>

<span data-ttu-id="2a7ce-140">С помощью [отладчика для](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) расширения кода EDGE Вы можете отлаживать сценарий, который выполняется в Microsoft EDGE, прямо в коде Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-140">With the [Debugger for Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) VS Code extension, you can debug script running in Microsoft Edge directly in Visual Studio Code.</span></span> <span data-ttu-id="2a7ce-141">Расширение требует обслуживания веб-приложения с localhost, которое можно начать из командной строки или [задачи](https://code.visualstudio.com/docs/editor/tasks).</span><span class="sxs-lookup"><span data-stu-id="2a7ce-141">The extension requires you to be serving your web application from localhost, which you can start from either command-line or a [Task](https://code.visualstudio.com/docs/editor/tasks).</span></span>

<span data-ttu-id="2a7ce-142">Для начала сделайте следующее:</span><span class="sxs-lookup"><span data-stu-id="2a7ce-142">To get started:</span></span>

1. <span data-ttu-id="2a7ce-143">Установите [отладчик для](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) расширения кода Edge.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-143">Install the [Debugger for Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) VS Code extension.</span></span>

2. <span data-ttu-id="2a7ce-144">Перезапустите программу VS, откройте папку, содержащую проект, для которого вы хотите выполнить отладку, и установите точки останова в коде.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-144">Restart VS Code, open the folder containing the project you wish to debug and set breakpoints in your code.</span></span>

3. <span data-ttu-id="2a7ce-145">Настройте [задачу запуска](https://code.visualstudio.com/docs/editor/debugging#_launch-configurations) localhost, чтобы открыть нужную страницу проекта: **Отладка**  >  **добавления конфигурации..**.. Например:</span><span class="sxs-lookup"><span data-stu-id="2a7ce-145">Configure a localhost [launch task](https://code.visualstudio.com/docs/editor/debugging#_launch-configurations) to open the desired page of your project: **Debug** > **Add Configuration...**. For example:</span></span>

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

    <span data-ttu-id="2a7ce-146">[*С помощью отладчика*](https://github.com/Microsoft/vscode-edge-debug2#using-the-debugger) больше не заданные параметры настройки запуска.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-146">[*Using the debugger*](https://github.com/Microsoft/vscode-edge-debug2#using-the-debugger) has more on launch configuration settings.</span></span> 

4. <span data-ttu-id="2a7ce-147">Запустите сервер на локальном компьютере и нажмите кнопку " **запустить отладку** (воспроизвести)" или `F5` Запустите Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-147">Start your server on localhost and press the **Start Debugging** (play) button or `F5` to launch Microsoft Edge.</span></span> <span data-ttu-id="2a7ce-148">При попадании в точку останова вы будете прерываться на код VS и проанализировать код от него.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-148">When a breakpoint is hit, you'll break into VS Code and can further inspect and step through code from there.</span></span>

<span data-ttu-id="2a7ce-149">Дополнительные сведения можно найти в руководстве по [отладке кода VS для Microsoft Edge](https://github.com/Microsoft/vscode-edge-debug2#----vs-code---debugger-for-microsoft-edge--) .</span><span class="sxs-lookup"><span data-stu-id="2a7ce-149">For more, check out the [VS Code - Debugger for Microsoft Edge](https://github.com/Microsoft/vscode-edge-debug2#----vs-code---debugger-for-microsoft-edge--) documentation.</span></span>

## <span data-ttu-id="2a7ce-150">Microsoft Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2a7ce-150">Microsoft Visual Studio</span></span>

<span data-ttu-id="2a7ce-151">Если вы используете последнюю версию [**Visual Studio**](https://www.visualstudio.com) (visual Studio 15,8 или более поздней версии), которая выполняется в [Windows 10 октября 2018](/windows/uwp/whats-new/windows-10-build-17763)г., вы можете запускать и отлаживать Microsoft Edge из интегрированной среды разработки для любого проекта ASP.NET или .NET.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-151">Using the latest [**Visual Studio**](https://www.visualstudio.com) version (Visual Studio 15.8 or later) running on [Windows 10 October 2018 Update](/windows/uwp/whats-new/windows-10-build-17763), you can launch and debug Microsoft Edge from the IDE on any ASP.NET or .NET Core project.</span></span>

<span data-ttu-id="2a7ce-152">Вот как можно настроить отладку Microsoft Edge с помощью Visual Studio:</span><span class="sxs-lookup"><span data-stu-id="2a7ce-152">Here's how to set up Microsoft Edge debugging with Visual Studio:</span></span>

1.  <span data-ttu-id="2a7ce-153">Установите и запустите последнюю версию [**Visual Studio**](https://www.visualstudio.com/) (visual Studio 15,8 или более поздней версии).</span><span class="sxs-lookup"><span data-stu-id="2a7ce-153">Install and launch the latest [**Visual Studio**](https://www.visualstudio.com/) (Visual Studio 15.8 or later).</span></span>

2. <span data-ttu-id="2a7ce-154">Открытие существующего основного проекта ASP.NET или .NET или **Создание нового проекта...** использование одного из шаблонов **Visual C#** .NET.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-154">Open an existing ASP.NET or .NET Core project or **Create new project...** using one of the **Visual C#** .NET templates.</span></span>

3. <span data-ttu-id="2a7ce-155">В **обозревателе решений**проекта откройте файлы JavaScript, которые вы хотите отладить, и установите точки останова в интерфейсе IDE так же, как и в случае с кодом на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-155">In the project **Solution Explorer**, open the JavaScript files you wish to debug and set breakpoints within the IDE just as you would with server-side code.</span></span>

4. <span data-ttu-id="2a7ce-156">Нажмите `F5` , чтобы запустить Microsoft EDGE, на котором запущен сервер DevTools.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-156">Press `F5` to launch Microsoft Edge running the DevTools Server.</span></span> <span data-ttu-id="2a7ce-157">При попадании в точку останова вы перейдете в Visual Studio и сможете проанализировать код и прокрутить его.</span><span class="sxs-lookup"><span data-stu-id="2a7ce-157">When a breakpoint is hit, you'll break into Visual Studio and can further inspect and step through the code from there.</span></span>
