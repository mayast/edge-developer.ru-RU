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
# <span data-ttu-id="fc0f7-103">Протокол DevTools Microsoft EDGE (Chromium)</span><span class="sxs-lookup"><span data-stu-id="fc0f7-103">Microsoft Edge (Chromium) DevTools Protocol</span></span>

<span data-ttu-id="fc0f7-104">При смене базовой веб-платформы Microsoft EDGE на Chromium [протокол DevTools Microsoft EDGE (EdgeHTML)](./devtools-protocol/index.md) не будет получать никаких обновлений.</span><span class="sxs-lookup"><span data-stu-id="fc0f7-104">With the shift in the underlying web platform of Microsoft Edge to Chromium, the [Microsoft Edge (EdgeHTML) DevTools Protocol](./devtools-protocol/index.md) will not be receiving any further updates.</span></span> <span data-ttu-id="fc0f7-105">Протокол DevTools Microsoft EDGE (Chromium) будет соответствовать API-интерфейсам протокола Chrome DevTools, пересылаемых вперед.</span><span class="sxs-lookup"><span data-stu-id="fc0f7-105">The Microsoft Edge (Chromium) DevTools Protocol will match the APIs of the Chrome DevTools Protocol going forward.</span></span> 

<span data-ttu-id="fc0f7-106">Документацию к этим доменам и методам можно найти, обратившись к [средству просмотра протоколов Chrome DevTools](https://chromedevtools.github.io/devtools-protocol/tot/).</span><span class="sxs-lookup"><span data-stu-id="fc0f7-106">You can find documentation on those domains and methods by referring to the [Chrome DevTools Protocol Viewer](https://chromedevtools.github.io/devtools-protocol/tot/).</span></span>

> [!NOTE]
> <span data-ttu-id="fc0f7-107">Любые методы с префиксом, заданным `ms` в [протоколе Microsoft EDGE (EdgeHTML) DevTools](./devtools-protocol/index.md) , больше не поддерживаются протоколом Microsoft EDGE (Chromium) DevTools.</span><span class="sxs-lookup"><span data-stu-id="fc0f7-107">Any methods that were prefixed with `ms` in the [Microsoft Edge (EdgeHTML) DevTools Protocol](./devtools-protocol/index.md) are no longer supported in the Microsoft Edge (Chromium) DevTools Protocol.</span></span>

## <span data-ttu-id="fc0f7-108">Использование протокола DevTools</span><span class="sxs-lookup"><span data-stu-id="fc0f7-108">Using the DevTools Protocol</span></span>

<span data-ttu-id="fc0f7-109">Вот как можно прикрепить клиентское средство управления к серверу DevTools в Microsoft EDGE (Chromium).</span><span class="sxs-lookup"><span data-stu-id="fc0f7-109">Here's how to attach a custom tooling client to the DevTools Server in Microsoft Edge (Chromium).</span></span>

1. <span data-ttu-id="fc0f7-110">Убедитесь, что все экземпляры Microsoft EDGE (Chromium) закрыты.</span><span class="sxs-lookup"><span data-stu-id="fc0f7-110">Ensure all instances of Microsoft Edge (Chromium) are closed.</span></span>

2. <span data-ttu-id="fc0f7-111">Запустите Microsoft EDGE (Chromium) с портом удаленной отладки:</span><span class="sxs-lookup"><span data-stu-id="fc0f7-111">Launch Microsoft Edge (Chromium) with the remote debugging port:</span></span>

    ```
    msedge.exe --remote-debugging-port=9222
    ```

3. <span data-ttu-id="fc0f7-112">При необходимости вы можете при необходимости создать отдельный экземпляр Edge с использованием отдельного профиля пользователя.</span><span class="sxs-lookup"><span data-stu-id="fc0f7-112">Optionally, you can start a separate instance of Edge using a distinct user profile if desired:</span></span>

    ```
    msedge.exe --user-data-dir=<some directory>
    ```

4. <span data-ttu-id="fc0f7-113">Затем используйте `list` конечную точку HTTP для получения списка конечных объектов страницы.</span><span class="sxs-lookup"><span data-stu-id="fc0f7-113">Next, use the HTTP `list` endpoint to get a list of attachable page targets:</span></span>

    ```
    http://localhost:9222/json/list
    ```

5. <span data-ttu-id="fc0f7-114">Наконец, подключитесь к `webSocketDebuggerUrl` нужному целевому объекту и выводите команды и подпишитесь на сообщения о событиях через сервер веб-сокета DevTools.</span><span class="sxs-lookup"><span data-stu-id="fc0f7-114">Finally, connect to the `webSocketDebuggerUrl` of the desired target and issue commands/subscribe to event messages through the DevTools web socket server.</span></span>

## <span data-ttu-id="fc0f7-115">Конечные точки HTTP протокола DevTools</span><span class="sxs-lookup"><span data-stu-id="fc0f7-115">DevTools Protocol HTTP Endpoints</span></span>

<span data-ttu-id="fc0f7-116">Протокол DevTools Microsoft EDGE (Chromium) поддерживает следующие конечные точки HTTP.</span><span class="sxs-lookup"><span data-stu-id="fc0f7-116">The Microsoft Edge (Chromium) DevTools Protocol supports the following HTTP endpoints.</span></span>

## <span data-ttu-id="fc0f7-117">/json/version</span><span class="sxs-lookup"><span data-stu-id="fc0f7-117">/json/version</span></span>
<span data-ttu-id="fc0f7-118">Сведения о браузере хост-компьютера и версии поддерживаемого им протокола DevTools.</span><span class="sxs-lookup"><span data-stu-id="fc0f7-118">Provides information on the host machine's browser and which version of the DevTools Protocol it supports.</span></span>

**<span data-ttu-id="fc0f7-119">Параметры</span><span class="sxs-lookup"><span data-stu-id="fc0f7-119">Parameters</span></span>**

*<span data-ttu-id="fc0f7-120">Нет</span><span class="sxs-lookup"><span data-stu-id="fc0f7-120">None</span></span>*

**<span data-ttu-id="fc0f7-121">Возвращаемый объект</span><span class="sxs-lookup"><span data-stu-id="fc0f7-121">Return object</span></span>**

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

## <span data-ttu-id="fc0f7-122">/json/protocol</span><span class="sxs-lookup"><span data-stu-id="fc0f7-122">/json/protocol</span></span>

<span data-ttu-id="fc0f7-123">Обеспечивает весь интерфейс API протокола, сериализованный как JSON.</span><span class="sxs-lookup"><span data-stu-id="fc0f7-123">Provides the entire protocol API surface serialized as JSON.</span></span>

**<span data-ttu-id="fc0f7-124">Параметры</span><span class="sxs-lookup"><span data-stu-id="fc0f7-124">Parameters</span></span>**

*<span data-ttu-id="fc0f7-125">Нет</span><span class="sxs-lookup"><span data-stu-id="fc0f7-125">None</span></span>*

**<span data-ttu-id="fc0f7-126">Возвращаемый объект</span><span class="sxs-lookup"><span data-stu-id="fc0f7-126">Return object</span></span>**

<span data-ttu-id="fc0f7-127">Объект JSON, который представляет доступную поверхность API для текущей версии протокола.</span><span class="sxs-lookup"><span data-stu-id="fc0f7-127">JSON object which represents the available API surface for current version of the protocol.</span></span>

## <span data-ttu-id="fc0f7-128">/json/list</span><span class="sxs-lookup"><span data-stu-id="fc0f7-128">/json/list</span></span>

<span data-ttu-id="fc0f7-129">Список кандидатов на странице для отладки.</span><span class="sxs-lookup"><span data-stu-id="fc0f7-129">Provides a candidate list of page targets for debugging.</span></span>

**<span data-ttu-id="fc0f7-130">Параметры</span><span class="sxs-lookup"><span data-stu-id="fc0f7-130">Parameters</span></span>**

*<span data-ttu-id="fc0f7-131">Нет</span><span class="sxs-lookup"><span data-stu-id="fc0f7-131">None</span></span>*

**<span data-ttu-id="fc0f7-132">Возвращаемый объект</span><span class="sxs-lookup"><span data-stu-id="fc0f7-132">Return object</span></span>**

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

## <span data-ttu-id="fc0f7-133">/json/close</span><span class="sxs-lookup"><span data-stu-id="fc0f7-133">/json/close</span></span>

<span data-ttu-id="fc0f7-134">Закрывает целевой процесс (например, в Microsoft EDGE (Chromium), закрывает вкладку Page (страница).</span><span class="sxs-lookup"><span data-stu-id="fc0f7-134">Closes down the target process (e.g., in Microsoft Edge (Chromium), closes the page tab.)</span></span>

**<span data-ttu-id="fc0f7-135">Параметры</span><span class="sxs-lookup"><span data-stu-id="fc0f7-135">Parameters</span></span>**

<span data-ttu-id="fc0f7-136">Идентификатор целевого объекта</span><span class="sxs-lookup"><span data-stu-id="fc0f7-136">Target ID</span></span> 

**<span data-ttu-id="fc0f7-137">Возвращаемый объект</span><span class="sxs-lookup"><span data-stu-id="fc0f7-137">Return object</span></span>**

```
String(“Target is closing”)
```

## <span data-ttu-id="fc0f7-138">Удаленные инструменты для Microsoft EDGE (бета-версия)</span><span class="sxs-lookup"><span data-stu-id="fc0f7-138">Remote Tools for Microsoft Edge (Beta)</span></span>

<span data-ttu-id="fc0f7-139">Теперь вы можете установить [удаленные инструменты для Microsoft EDGE (бета-версия)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) из [Microsoft Store](https://www.microsoft.com/store/apps/windows).</span><span class="sxs-lookup"><span data-stu-id="fc0f7-139">You are now able to install the [Remote Tools for Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) from the [Microsoft Store](https://www.microsoft.com/store/apps/windows).</span></span> <span data-ttu-id="fc0f7-140">Это приложение позволяет осуществлять удаленную отладку Microsoft EDGE (Chromium), работающей на устройстве с Windows 10, с компьютера, на котором ведется разработка.</span><span class="sxs-lookup"><span data-stu-id="fc0f7-140">This app enables you to remotely debug Microsoft Edge (Chromium) running on a Windows 10 device from your development machine.</span></span>

<span data-ttu-id="fc0f7-141">Чтобы узнать, как настроить устройство с Windows 10 и подключиться к нему с компьютера для разработки, ознакомьтесь с [этим учебником](./devtools-guide-chromium/remote-debugging/windows.md).</span><span class="sxs-lookup"><span data-stu-id="fc0f7-141">To learn how to set up your Windows 10 device and connect to it from your development machine, check out [this tutorial](./devtools-guide-chromium/remote-debugging/windows.md).</span></span>

<span data-ttu-id="fc0f7-142">[Удаленные инструменты для Microsoft EDGE (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) используют один и тот же протокол DevTools Microsoft EDGE (Chromium) в качестве [DevTools](./devtools-guide-chromium.md) для общения с Microsoft EDGE на устройстве с Windows 10, на котором вы хотите выполнить отладку.</span><span class="sxs-lookup"><span data-stu-id="fc0f7-142">The [Remote Tools for Microsoft Edge (Beta)](https://www.microsoft.com/store/apps/9P6CMFV44ZLT) uses the same Microsoft Edge (Chromium) DevTools Protocol as the [DevTools](./devtools-guide-chromium.md) to communicate with Microsoft Edge running on the Windows 10 device you want to debug.</span></span> <span data-ttu-id="fc0f7-143">Это приложение вставляется только `/msedge/` `pid` перед каждым вызовом к протоколу (в начале), а затем идентификаторе процесса ().</span><span class="sxs-lookup"><span data-stu-id="fc0f7-143">This app just prepends `/msedge/` and a process ID (`pid`) before each call to the protocol.</span></span> <span data-ttu-id="fc0f7-144">Она поддерживает следующие конечные точки HTTP.</span><span class="sxs-lookup"><span data-stu-id="fc0f7-144">It supports the following HTTP endpoints.</span></span>

### <span data-ttu-id="fc0f7-145">/msedge/json/list</span><span class="sxs-lookup"><span data-stu-id="fc0f7-145">/msedge/json/list</span></span>

<span data-ttu-id="fc0f7-146">Список кандидатов всех `msedge.exe` процессов (включая [PWAs](./progressive-web-apps-chromium/index.md) и все вкладки во всех экземплярах Microsoft EDGE) на устройстве с Windows 10 для отладки.</span><span class="sxs-lookup"><span data-stu-id="fc0f7-146">Provides a candidate list of all `msedge.exe` processes (including [PWAs](./progressive-web-apps-chromium/index.md) and all tabs in all instances of Microsoft Edge) on the Windows 10 device for debugging.</span></span>

**<span data-ttu-id="fc0f7-147">Параметры</span><span class="sxs-lookup"><span data-stu-id="fc0f7-147">Parameters</span></span>**

*<span data-ttu-id="fc0f7-148">Нет</span><span class="sxs-lookup"><span data-stu-id="fc0f7-148">None</span></span>*

**<span data-ttu-id="fc0f7-149">Возвращаемый объект</span><span class="sxs-lookup"><span data-stu-id="fc0f7-149">Return object</span></span>**

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

### <span data-ttu-id="fc0f7-150">/msedge/</span><span class="sxs-lookup"><span data-stu-id="fc0f7-150">/msedge/</span></span>

<span data-ttu-id="fc0f7-151">Функционально эквивалентен [/msedge/JSON/List](#msedgejsonlist).</span><span class="sxs-lookup"><span data-stu-id="fc0f7-151">Functionally equivalent to [/msedge/json/list](#msedgejsonlist).</span></span> 

### <span data-ttu-id="fc0f7-152">/msedge/[PID]/JSON/List</span><span class="sxs-lookup"><span data-stu-id="fc0f7-152">/msedge/[pid]/json/list</span></span>

<span data-ttu-id="fc0f7-153">Предоставляет список кандидатов на страницах для экземпляра Microsoft EDGE, соответствующий указанному `[pid]` для отладки.</span><span class="sxs-lookup"><span data-stu-id="fc0f7-153">Provides a candidate list of page targets for the Microsoft Edge instance that matches the provided `[pid]` for debugging.</span></span>

**<span data-ttu-id="fc0f7-154">Параметры</span><span class="sxs-lookup"><span data-stu-id="fc0f7-154">Parameters</span></span>**

*<span data-ttu-id="fc0f7-155">Нет</span><span class="sxs-lookup"><span data-stu-id="fc0f7-155">None</span></span>*

**<span data-ttu-id="fc0f7-156">Возвращаемый объект</span><span class="sxs-lookup"><span data-stu-id="fc0f7-156">Return object</span></span>**

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

### <span data-ttu-id="fc0f7-157">/msedge/[PID]/JSON/Version</span><span class="sxs-lookup"><span data-stu-id="fc0f7-157">/msedge/[pid]/json/version</span></span>

<span data-ttu-id="fc0f7-158">Предоставляет сведения о экземпляре Microsoft EDGE, соответствующем предоставленному параметру, `[pid]` и какая версия поддерживаемого им протокола DevTools.</span><span class="sxs-lookup"><span data-stu-id="fc0f7-158">Provides information about the Microsoft Edge instance that matches the provided `[pid]` and which version of the DevTools Protocol it supports.</span></span>

**<span data-ttu-id="fc0f7-159">Параметры</span><span class="sxs-lookup"><span data-stu-id="fc0f7-159">Parameters</span></span>**

*<span data-ttu-id="fc0f7-160">Нет</span><span class="sxs-lookup"><span data-stu-id="fc0f7-160">None</span></span>*

**<span data-ttu-id="fc0f7-161">Возвращаемый объект</span><span class="sxs-lookup"><span data-stu-id="fc0f7-161">Return object</span></span>**

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

### <span data-ttu-id="fc0f7-162">/msedge/[PID]/JSON/Protocol/</span><span class="sxs-lookup"><span data-stu-id="fc0f7-162">/msedge/[pid]/json/protocol/</span></span>

<span data-ttu-id="fc0f7-163">Предоставляет весь интерфейс API протокола, сериализованный как JSON для экземпляра Microsoft EDGE, который соответствует предоставленному `[pid]` .</span><span class="sxs-lookup"><span data-stu-id="fc0f7-163">Provides the entire protocol API surface serialized as JSON for the Microsoft Edge instance that matches the provided `[pid]`.</span></span>

**<span data-ttu-id="fc0f7-164">Параметры</span><span class="sxs-lookup"><span data-stu-id="fc0f7-164">Parameters</span></span>**

*<span data-ttu-id="fc0f7-165">Нет</span><span class="sxs-lookup"><span data-stu-id="fc0f7-165">None</span></span>*

**<span data-ttu-id="fc0f7-166">Возвращаемый объект</span><span class="sxs-lookup"><span data-stu-id="fc0f7-166">Return object</span></span>**

<span data-ttu-id="fc0f7-167">Объект JSON, который представляет собой доступную поверхность API для версии протокола, которая используется в качестве экземпляра Microsoft EDGE, соответствующего указанному `[pid]` .</span><span class="sxs-lookup"><span data-stu-id="fc0f7-167">JSON object which represents the available API surface for the version of the protocol that the Microsoft Edge instance that matches the provided `[pid]` is using.</span></span>
