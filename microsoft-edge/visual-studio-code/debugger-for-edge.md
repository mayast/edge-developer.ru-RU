---
description: Отладка Microsoft EDGE (Chromium) и Microsoft EDGE (EdgeHTML) из кода VS
title: Отладка Microsoft EDGE (Chromium) из кода VS
author: zoherghadyali
ms.author: zoghadya
ms.date: 03/10/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, код VS, код Visual Studio, отладчик
ms.openlocfilehash: 7d8d2f87500b3e81866b49de32db91c0a525baf2
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572804"
---
# <span data-ttu-id="9fbfe-104">Отладчик для расширения кода Microsoft Edge VS</span><span class="sxs-lookup"><span data-stu-id="9fbfe-104">Debugger for Microsoft Edge VS Code extension</span></span>

<span data-ttu-id="9fbfe-105">С помощью [отладчика для расширения кода Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) VS вы можете выполнять отладку клиентского кода JavaScript по строкам и просматривать `console.log()` инструкции прямо из [кода Visual Studio](https://code.visualstudio.com/)!</span><span class="sxs-lookup"><span data-stu-id="9fbfe-105">With the [Debugger for Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) VS Code extension, you can debug your front-end JavaScript code line by line and see `console.log()` statements all directly from [Visual Studio Code](https://code.visualstudio.com/)!</span></span>

![GIF-файл с отладчиком для расширения кода пограничного и на рабочем процессе](./media/debugger-for-edge.gif)

## <span data-ttu-id="9fbfe-107">Запуск Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9fbfe-107">Launching Microsoft Edge</span></span>

<span data-ttu-id="9fbfe-108">Перейдите в представление Отладка ( `Ctrl`  +  `Shift`  +  `D` в Windows или `Command`  +  `Shift`  +  `D` на компьютере Mac) на **панели действий**.</span><span class="sxs-lookup"><span data-stu-id="9fbfe-108">Navigate to the Debug view (`Ctrl` + `Shift` + `D` on Windows or `Command` + `Shift` + `D` on Mac) in the **Activity Bar**.</span></span> <span data-ttu-id="9fbfe-109">Если у вас нет каких-либо конфигураций в коде VS, нажмите клавишу `F5` Windows или Mac или нажмите зеленую кнопку **воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="9fbfe-109">If you do not have any configurations in VS Code, press `F5` on Windows or Mac or click the green **Play** button.</span></span> <span data-ttu-id="9fbfe-110">В раскрывающемся списке выберите пункт "Edge".</span><span class="sxs-lookup"><span data-stu-id="9fbfe-110">Select "Edge" in the dropdown.</span></span> <span data-ttu-id="9fbfe-111">Теперь появится файл **Launch. JSON** со следующими конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="9fbfe-111">You will now see a **launch.json** file with the following configuration:</span></span>

```json
{
    "version": "0.2.0",
    "configurations": [
        {
            "type": "edge",
            "request": "launch",
            "name": "Launch Edge against localhost",
            "url": "http://localhost:8080",
            "webRoot": "${workspaceFolder}"
        }
    ]
}
```

<span data-ttu-id="9fbfe-112">Если вы нажмете `F5` кнопку « **воспроизвести** зеленый» в Windows или Mac или снова нажмите зеленую кнопку воспроизведения, код VS будет запускать Microsoft EDGE (EdgeHTML), и вы сможете выполнять отладку любого веб-проекта, который вы используете на порте **8080** прямо из кода VS!</span><span class="sxs-lookup"><span data-stu-id="9fbfe-112">If you now press `F5` on Windows or Mac or click the green **Play** button again, VS Code will launch Microsoft Edge (EdgeHTML) and you will be able to debug any web project you have running on port **8080** directly from VS Code!</span></span>

### <span data-ttu-id="9fbfe-113">Microsoft Edge (на основе Chromium)</span><span class="sxs-lookup"><span data-stu-id="9fbfe-113">Microsoft Edge (Chromium)</span></span>

<span data-ttu-id="9fbfe-114">Если вы хотите запустить Microsoft EDGE (Chromium), в следующей версии Microsoft EDGE вместо Microsoft EDGE (EdgeHTML) просто добавьте `version` атрибут для существующей конфигурации с версией Microsoft EDGE (Chromium), которую вы хотите запустить ( `dev` `beta` или `canary` ).</span><span class="sxs-lookup"><span data-stu-id="9fbfe-114">If you want to launch Microsoft Edge (Chromium), the next version of Microsoft Edge, instead of Microsoft Edge (EdgeHTML), simply add a `version` attribute to your existing configuration with the version of Microsoft Edge (Chromium) you want to launch (`dev`, `beta`, or `canary`).</span></span> <span data-ttu-id="9fbfe-115">Указанные ниже конфигурации запустят версию Канарские Microsoft EDGE (Chromium):</span><span class="sxs-lookup"><span data-stu-id="9fbfe-115">The configuration below will launch the Canary version of Microsoft Edge (Chromium):</span></span>

```json
{
    "type": "edge",
    "request": "launch",
    "version": "canary",
    "name": "Launch Edge against localhost",
    "url": "http://localhost:8080",
    "webRoot": "${workspaceFolder}"
}
```

## <span data-ttu-id="9fbfe-116">Присоединение к Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9fbfe-116">Attaching to Microsoft Edge</span></span>

<span data-ttu-id="9fbfe-117">Вы также можете прикрепить код VS к Microsoft EDGE (Chromium).</span><span class="sxs-lookup"><span data-stu-id="9fbfe-117">You can also attach VS Code to Microsoft Edge (Chromium).</span></span> <span data-ttu-id="9fbfe-118">На своем терминале выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="9fbfe-118">From your terminal, run the following command:</span></span>

`start msedge --remote-debugging-port=9222`

<span data-ttu-id="9fbfe-119">Добавьте в файл **Launch. JSON** конфигурацию ниже.</span><span class="sxs-lookup"><span data-stu-id="9fbfe-119">Add the configuration below to your **launch.json** file:</span></span>

```json
{
    "type": "edge",
    "request": "attach",
    "name": "Attach to Edge",
    "port": 9222
}
```

<span data-ttu-id="9fbfe-120">Если теперь вы запустите такую конфигурацию, код VS будет подсоединен к Microsoft EDGE (Chromium), и вы сможете начать отладку!</span><span class="sxs-lookup"><span data-stu-id="9fbfe-120">If you now run this configuration, VS Code will attach to Microsoft Edge (Chromium) and you can start debugging!</span></span>

## <span data-ttu-id="9fbfe-121">Отзыв</span><span class="sxs-lookup"><span data-stu-id="9fbfe-121">Feedback</span></span>

<span data-ttu-id="9fbfe-122">Отправьте нам отзыв, выполнив [архивацию](https://github.com/Microsoft/vscode-edge-debug2/issues/new) в [репозитории GitHub](https://github.com/Microsoft/vscode-edge-debug2)для этого расширения.</span><span class="sxs-lookup"><span data-stu-id="9fbfe-122">Send us your feedback by [filing an issue](https://github.com/Microsoft/vscode-edge-debug2/issues/new) against this extension's [GitHub repo](https://github.com/Microsoft/vscode-edge-debug2).</span></span> <span data-ttu-id="9fbfe-123">Добавьте файл журнала адаптера отладки, который создается для каждого запуска в каталоге% TEMP% с именем `vscode-edge-debug2.txt` .</span><span class="sxs-lookup"><span data-stu-id="9fbfe-123">Please include the debug adapter log file, which is created for each run in the %temp% directory with the name `vscode-edge-debug2.txt`.</span></span> <span data-ttu-id="9fbfe-124">Вы можете перетащить этот файл в комментарий вопроса, чтобы отправить его в GitHub.</span><span class="sxs-lookup"><span data-stu-id="9fbfe-124">You can drag this file into an issue comment to upload it to GitHub.</span></span>

<span data-ttu-id="9fbfe-125">Если вы хотите помочь нам улучшить это расширение, мы будем рады вашим публикациям!</span><span class="sxs-lookup"><span data-stu-id="9fbfe-125">If you want to help us make this extension better, we welcome your contributions!</span></span> <span data-ttu-id="9fbfe-126">Вы можете найти все, что вам нужно, чтобы приступить к работе в [нашем репозитории GitHub](https://github.com/Microsoft/vscode-edge-debug2).</span><span class="sxs-lookup"><span data-stu-id="9fbfe-126">You can find everything you need to get started in [our GitHub repo](https://github.com/Microsoft/vscode-edge-debug2).</span></span>