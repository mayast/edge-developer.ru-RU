---
description: Использование элементов для Microsoft EDGE (Chromium) из кода VS
title: Элементы для Microsoft EDGE (Chromium) из кода VS
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, код VS, код Visual Studio, элементы
ms.openlocfilehash: ef516d8364c68b550f889bcad0fe762a73ce5f99
ms.sourcegitcommit: 652009c5cea9e75c22b077f0cbcdc0d96bd337ac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2020
ms.locfileid: "10694864"
---
# <span data-ttu-id="e610a-104">Элементы расширений Microsoft EDGE и кода</span><span class="sxs-lookup"><span data-stu-id="e610a-104">Elements For Microsoft Edge VS Code Extension</span></span>  

<span data-ttu-id="e610a-105">С помощью [элементов для расширения кода Microsoft Edge][VisualstudioMarketplaceElementsMicrosoftEdgeChromium] VS используйте инструмент "элементы" браузера Microsoft EDGE в [коде Visual Studio][VisualstudioCode].</span><span class="sxs-lookup"><span data-stu-id="e610a-105">With the [Elements for Microsoft Edge][VisualstudioMarketplaceElementsMicrosoftEdgeChromium] VS Code extension, use the Elements tool of the Microsoft Edge browser from within [Visual Studio Code][VisualstudioCode].</span></span>  <span data-ttu-id="e610a-106">Как при запуске, так и при присоединении средство "элементы" подключается к экземпляру Microsoft EDGE, отображает структуру HTML среды выполнения и позволяет изменить макет или проблемы со стилизацией.</span><span class="sxs-lookup"><span data-stu-id="e610a-106">By either launching or attaching, the Elements tool connects to an instance of Microsoft Edge, displays the runtime HTML structure, and allows you to alter the layout or fix styling issues.</span></span>  

:::image type="complex" source="./media/elements-for-edge.gif" alt-text="Элементы для расширения кода EDGE на работе":::
   <span data-ttu-id="e610a-108">Элементы для расширения кода EDGE на работе</span><span class="sxs-lookup"><span data-stu-id="e610a-108">Elements for Edge VS Code extension at work</span></span>  
:::image-end:::

<!--![Elements for Edge VS Code extension at work][ImageGifElementsEdge]  -->  

## <span data-ttu-id="e610a-109">Запуск Microsoft Edge из расширения Elements</span><span class="sxs-lookup"><span data-stu-id="e610a-109">Launching Microsoft Edge From the Elements extension</span></span>  

<span data-ttu-id="e610a-110">Перейдите к элементам на **панели действий**.</span><span class="sxs-lookup"><span data-stu-id="e610a-110">Navigate to Elements in the **Activity Bar**.</span></span>  <span data-ttu-id="e610a-111">Рядом с надписью **элементы для Microsoft Edge: targets** — знак "плюс", который открывает браузер для вашего приложения.</span><span class="sxs-lookup"><span data-stu-id="e610a-111">Next to where it says **Elements for Microsoft Edge: Targets,** there is a plus sign that opens the browser for your app.</span></span>  <span data-ttu-id="e610a-112">Если вы выбрали параметр **about: Blank** , вы должны перейти в браузере, чтобы он отображался на панели элементов в коде vs.</span><span class="sxs-lookup"><span data-stu-id="e610a-112">If you selected the **about:blank** option, you must navigate to your web app in the browser for it to appear in the Elements panel in VS Code.</span></span>  

## <span data-ttu-id="e610a-113">Запуск Microsoft Edge из представления отладки</span><span class="sxs-lookup"><span data-stu-id="e610a-113">Launching Microsoft Edge from the Debug view</span></span>  

<span data-ttu-id="e610a-114">Если вы привыкли использовать представление отладку в коде Visual Studio, вы можете получить доступ к элементам из этого инструмента.</span><span class="sxs-lookup"><span data-stu-id="e610a-114">If you are accustomed to using the Debug view in Visual Studio Code, access Elements from that tool.</span></span>  <span data-ttu-id="e610a-115">Перейдите в представление Отладка \ ( `Ctrl` + `Shift` + `D` в Windows или `Command` + `Shift` + `D` на macOS \).</span><span class="sxs-lookup"><span data-stu-id="e610a-115">Navigate to the Debug view \(`Ctrl`+`Shift`+`D` on Windows or `Command`+`Shift`+`D` on macOS\).</span></span>  

<span data-ttu-id="e610a-116">Если у вас нет каких бы то ни было конфигураций в коде VS, нажмите клавишу `F5` Windows или macOS или нажмите зеленую кнопку **воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="e610a-116">If you do not have any configurations in VS Code, press `F5` on Windows or macOS or select the green **Play** button.</span></span> <span data-ttu-id="e610a-117">Выберите **ребро** в раскрывающемся списке.</span><span class="sxs-lookup"><span data-stu-id="e610a-117">Select **Edge** in the dropdown.</span></span> <span data-ttu-id="e610a-118">Вы увидите `launch.json` файл со следующей конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="e610a-118">You should see a `launch.json` file with the following configuration.</span></span>  

```json
{
    "version": "0.2.0",
    "configurations": [
        {
            
            "name": "Launch Microsoft Edge and open the Elements tool",
            "request": "launch",
            "type": "vscode-edge-devtools.debug",
            "url": "http://localhost:3000"
        
        }
    ]
}
```  

<span data-ttu-id="e610a-119">После того как вы загрузили правильную конфигурацию, нажмите клавишу `F5` Windows или macOS или нажмите зеленую кнопку **воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="e610a-119">Now that you have loaded the correct configuration, either press `F5` on Windows or macOS or select the green **Play** button.</span></span> <span data-ttu-id="e610a-120">С помощью инструмента "элементы", который знаком вам, из браузера Microsoft Edge запускается в коде VS, что позволяет получать доступ к ролика браузера и просматривать компоненты страницы.</span><span class="sxs-lookup"><span data-stu-id="e610a-120">The Elements tool, that is familiar to you, from the Microsoft Edge browser launches in VS Code, allowing you to access a screencast of your browser and examine the components of your page.</span></span>  

## <span data-ttu-id="e610a-121">Присоединение к Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="e610a-121">Attaching to Microsoft Edge</span></span>  

<span data-ttu-id="e610a-122">Чтобы прикрепить код VS к экземпляру Microsoft Edge \ (Chromium \), необходимо запустить браузер, выполнив следующую команду на экране терминала.</span><span class="sxs-lookup"><span data-stu-id="e610a-122">To attach VS Code to an instance of Microsoft Edge\(Chromium\), you must start the browser by running the following command from your terminal.</span></span>  

`start msedge --remote-debugging-port=9222`  

<span data-ttu-id="e610a-123">После запуска приложения добавьте указанную ниже конфигурацию в файл **Launch. JSON** .</span><span class="sxs-lookup"><span data-stu-id="e610a-123">Once the app has launched, add the configuration below to your **launch.json** file:</span></span>  

```json
{
    "type": "vscode-edge-devtools.debug",
    "request": "attach",
    "name": "Attach to Microsoft Edge and open the Elements tool",
    "url": "http://localhost:3000/",
    "webRoot": "${workspaceFolder}/out",
    "port": 9222
}
```  

<span data-ttu-id="e610a-124">Выберите команду **присоединиться к Microsoft EDGE и откройте средство элементы** из раскрывающегося меню отладчик.</span><span class="sxs-lookup"><span data-stu-id="e610a-124">Select **Attach to Microsoft Edge and open the Elements tool** from the Debugger drop-down menu.</span></span>  <span data-ttu-id="e610a-125">Затем либо нажмите `F5` на Windows, либо macOS либо нажмите зеленую кнопку **воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="e610a-125">Next, either press `F5` on Windows or macOS or select the green **Play** button.</span></span>  <span data-ttu-id="e610a-126">Код VS запускает инструмент элементы, позволяя получить доступ к экранной роли браузера, проверить модель DOM и стиль компонентов на странице.</span><span class="sxs-lookup"><span data-stu-id="e610a-126">VS Code launches the Elements tool, allowing you to access a screencast of your browser, inspect the DOM, and the styling of the components on your page.</span></span>  

## <span data-ttu-id="e610a-127">Связь с элементами для группы расширения кода Microsoft Edge VS</span><span class="sxs-lookup"><span data-stu-id="e610a-127">Getting in touch with the Elements for Microsoft Edge VS Code extension team</span></span>  

<span data-ttu-id="e610a-128">Отправьте отзыв, выполнив [архивацию][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] в [репозитории GitHub][GithubMicrosoftVscodeEdgeDevtools] в расширении.</span><span class="sxs-lookup"><span data-stu-id="e610a-128">Send your feedback by [filing an issue][GithubMicrosoftVscodeEdgeDevtoolsNewIssue] against the [GitHub repo][GithubMicrosoftVscodeEdgeDevtools] of the extension.</span></span>  

<span data-ttu-id="e610a-129">Если вы хотите лучше сделать элементы для расширения кода Microsoft EDGE и более, ваши публикации будут рады!</span><span class="sxs-lookup"><span data-stu-id="e610a-129">If you want to help make the Elements for Microsoft Edge VS Code extension better, your contributions are welcome!</span></span>  <span data-ttu-id="e610a-130">Найдите все, что нужно, чтобы начать работу в [репозитории GitHub][GithubMicrosoftVscodeEdgeDevtools] на расширение.</span><span class="sxs-lookup"><span data-stu-id="e610a-130">Find everything you need to get started in the [GitHub repo][GithubMicrosoftVscodeEdgeDevtools] of the extension.</span></span>  

<!-- image links -->  

<!--[ImageGifElementsEdge]: ./media/elements-for-edge.gif "Elements for Edge VS Code extension in action"  -->  
[ImagePngElementsEdge]:./Media/Elements-for-Edge.png "элементы для расширения кода пограничного или более ранней программы в действии"  

<!--links -->  

[VscodeElementsEdge]: ./elements-for-edge.md "Элементы для расширения Microsoft EDGE и кода Документы Microsoft"  

[VisualstudioCode]: https://code.visualstudio.com "Код Visual Studio"  
[VisualStudioCodeDocs]: https://code.visualstudio.com/Docs "Документация | Код Visual Studio"   

[GithubMicrosoftVscodeEdgeDevtools]: https://github.com/Microsoft/vscode-edge-devtools "Microsoft/vscode-Edge-Devtools | GitHub"  
[GithubMicrosoftVscodeEdgeDevtoolsNewIssue]: https://github.com/Microsoft/vscode-edge-devtools/issues/new "Новая ошибка — Microsoft/vscode-Edge-Devtools | GitHub"

[VisualstudioMarketplaceElementsMicrosoftEdgeChromium]: https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools "Элементы для Microsoft EDGE (Chromium) | Visual Studio Marketplace"  
