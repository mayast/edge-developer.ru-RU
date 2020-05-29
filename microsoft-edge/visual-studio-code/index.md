---
description: Microsoft EDGE (Chromium) и код Visual Studio
title: Visual Studio Code
author: zoherghadyali
ms.author: zoghadya
ms.date: 03/12/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, код VS, код Visual Studio, отладчик, веб-подсказка
ms.openlocfilehash: 94148864edbd43adbe2dc9f3d0c2fa0c1f7f0b43
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572807"
---
# <span data-ttu-id="3266e-104">Visual Studio Code</span><span class="sxs-lookup"><span data-stu-id="3266e-104">Visual Studio Code</span></span>

<span data-ttu-id="3266e-105">[Код Visual Studio](https://code.visualstudio.com/Docs) — это упрощенный, но мощный редактор исходного кода, который работает на вашем компьютере и доступен для Windows, MacOS и Linux.</span><span class="sxs-lookup"><span data-stu-id="3266e-105">[Visual Studio Code](https://code.visualstudio.com/Docs) is a lightweight but powerful source code editor which runs on your desktop and is available for Windows, macOS and Linux.</span></span> <span data-ttu-id="3266e-106">Она поставляется с встроенной поддержкой JavaScript, TypeScript и Node. js, так что это отличный инструмент для веб-разработчиков прямо из этого поля.</span><span class="sxs-lookup"><span data-stu-id="3266e-106">It comes with built-in support for JavaScript, TypeScript and Node.js so it's a great tool for web developers right out of the box!</span></span> <span data-ttu-id="3266e-107">Заголовку на [эту страницу](https://code.visualstudio.com/) , чтобы загрузить код Visual Studio, если он еще не используется.</span><span class="sxs-lookup"><span data-stu-id="3266e-107">Head to [this page](https://code.visualstudio.com/) to download Visual Studio Code if you aren't using it yet.</span></span>

## <span data-ttu-id="3266e-108">Расширения</span><span class="sxs-lookup"><span data-stu-id="3266e-108">Extensions</span></span>

<!-- We want to put something like the tiles for extensions VS Code uses on this page https://code.visualstudio.com/Docs#top-extensions but I don't think this is a markdown page. I think it's a web page. I couldn't find anything in https://github.com/Microsoft/vscode-docs that looks like this page. In the meantime, here's what I've come up with: -->

<span data-ttu-id="3266e-109">Чтобы получить какое-либо из расширений, выделенных ниже, перейдите в раздел расширения ( `Ctrl`  +  `Shift`  +  `X` в Windows или `Command`  +  `Shift`  +  `X` Mac) в код vs.</span><span class="sxs-lookup"><span data-stu-id="3266e-109">To acquire any of the extensions highlighted below, navigate to Extensions (`Ctrl` + `Shift` + `X` on Windows or `Command` + `Shift` + `X` on Mac) in VS Code.</span></span>

<span data-ttu-id="3266e-110">Найдите нужное расширение рынка и нажмите кнопку **установить**.</span><span class="sxs-lookup"><span data-stu-id="3266e-110">Search the Marketplace for the specific extension and select **Install**.</span></span>

![Установка отладчика для расширения кода Microsoft Edge VS](./media/vscode-debugger-install.png)

## <span data-ttu-id="3266e-112">Отладчик для Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="3266e-112">Debugger for Microsoft Edge</span></span>

<span data-ttu-id="3266e-113">Проведите отладку кода JavaScript на строке по строкам и выведите `console.log()` Операторы прямо в [коде Visual Studio](https://code.visualstudio.com/) с помощью [отладчика для расширения кода Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) vs.</span><span class="sxs-lookup"><span data-stu-id="3266e-113">Debug your front-end JavaScript code line by line and display `console.log()` statements directly in [Visual Studio Code](https://code.visualstudio.com/) using the the [Debugger for Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) VS Code extension!</span></span>

<span data-ttu-id="3266e-114">Используйте [отладчик для расширения кода Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) VS, чтобы запустить и присоединиться к Microsoft EDGE (EdgeHTML) и Microsoft EDGE (Chromium).</span><span class="sxs-lookup"><span data-stu-id="3266e-114">Use the [Debugger for Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=msjsdiag.debugger-for-edge) VS Code extension to launch or attach to both Microsoft Edge (EdgeHTML) and Microsoft Edge (Chromium).</span></span> <span data-ttu-id="3266e-115">Ознакомьтесь со [this page](./debugger-for-edge.md) статьей, пошаговыми инструкциями по отладке Microsoft Edge из кода VS и примерами настроек **Launch. JSON** .</span><span class="sxs-lookup"><span data-stu-id="3266e-115">Check out [this page](./debugger-for-edge.md) for a walkthrough of debugging Microsoft Edge from VS Code and sample **launch.json** configurations.</span></span>

![GIF-файл отладчика для расширения кода пограничного или более ранней версии в действии!](./media/debugger-for-edge.gif)

## <span data-ttu-id="3266e-117">Элементы Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="3266e-117">Elements for Microsoft Edge</span></span>

<span data-ttu-id="3266e-118">Добавляя [элементы для расширения кода Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools) и вы можете использовать средство браузера Elements в коде Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="3266e-118">By adding the [Elements for Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools) VS Code extension, you can use the browser's Elements tool from within Visual Studio Code.</span></span> <span data-ttu-id="3266e-119">При запуске или присоединении средство "элементы" подключится к экземпляру Microsoft EDGE, отобразит HTML-структуру среды выполнения и позволит вам изменить макет или устранить проблемы с стилизацией.</span><span class="sxs-lookup"><span data-stu-id="3266e-119">By either launching or attaching, the Elements tool will connect to an instance of Microsoft Edge, display the runtime HTML structure, and allow you to alter the layout or fix styling issues.</span></span>

<span data-ttu-id="3266e-120">Дополнительные сведения можно найти на [этой странице](./elements-for-edge.md).</span><span class="sxs-lookup"><span data-stu-id="3266e-120">For more information, check out [this page](./elements-for-edge.md).</span></span>

![GIF-файл для расширения кода пограничного элемента в действии!](./media/elements-for-edge.gif)

## <span data-ttu-id="3266e-122">Подсказка</span><span class="sxs-lookup"><span data-stu-id="3266e-122">webhint</span></span>

<span data-ttu-id="3266e-123">Используйте веб- [подсказку](https://webhint.io), настраиваемый инструмент linting, чтобы улучшить доступность, производительность, совместимость с различными браузерами, совместимость с PWA и безопасность сайта.</span><span class="sxs-lookup"><span data-stu-id="3266e-123">Use [webhint](https://webhint.io), a customizable linting tool, to improve the accessibility, performance, cross-browser compatibility, PWA compatibility, and security of your site.</span></span> <span data-ttu-id="3266e-124">Она проверяет ваш код на предмет рекомендаций и распространенных ошибок.</span><span class="sxs-lookup"><span data-stu-id="3266e-124">It checks your code for best practices and common errors.</span></span> <span data-ttu-id="3266e-125">Этот проект с открытым исходным кодом, изначально разработанный группой Microsoft EDGE, теперь является частью [OpenJS Foundation](https://openjsf.org/).</span><span class="sxs-lookup"><span data-stu-id="3266e-125">This open-source project, initially developed by the Microsoft Edge team, is now part of the [OpenJS Foundation](https://openjsf.org/).</span></span> <span data-ttu-id="3266e-126">Группа Microsoft Edge продолжает вносить вклад в веб-подсказку в сообществе в сообщество.</span><span class="sxs-lookup"><span data-stu-id="3266e-126">The Microsoft Edge team continues to contribute to webhint alongside web developers in the community.</span></span>

![Снимок экрана: расширение кода и ссылки на него](./media/webhint-extension.png)

<span data-ttu-id="3266e-128">Выявление и устранение проблем в HTML, CSS, JavaScript, TypeScript и т. д. Добавьте расширение веб- [подсказки для кода VS](https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint).</span><span class="sxs-lookup"><span data-stu-id="3266e-128">Identify and fix problems in your HTML, CSS, JavaScript, TypeScript, and more by adding the [webhint extension for VS Code](https://marketplace.visualstudio.com/items?itemName=webhint.vscode-webhint).</span></span> <span data-ttu-id="3266e-129">Подсказки выводятся в виде встроенных подчеркивания и обобщены на панели "проблемы".</span><span class="sxs-lookup"><span data-stu-id="3266e-129">Hints appear as inline underlines and are summarized in the Problems pane.</span></span>

<span data-ttu-id="3266e-130">Дополнительные сведения можно найти [в разделе Использование подсказки в коде Visual Studio](./webhint.md).</span><span class="sxs-lookup"><span data-stu-id="3266e-130">For more information, see [How to use webhint in Visual Studio Code](./webhint.md).</span></span>
