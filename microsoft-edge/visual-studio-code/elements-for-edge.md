---
description: Использование элементов для Microsoft EDGE (Chromium) из кода VS
title: Элементы для Microsoft EDGE (Chromium) из кода VS
author: erdraud
ms.author: erdraud
ms.date: 08/08/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, код VS, код Visual Studio, элементы
ms.openlocfilehash: 4875a4665fe1561ecf587a050bbd44e116d9ce5e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572808"
---
# <span data-ttu-id="33c3a-104">Элементы расширений Microsoft EDGE и кода</span><span class="sxs-lookup"><span data-stu-id="33c3a-104">Elements for Microsoft Edge VS Code extension</span></span>

<span data-ttu-id="33c3a-105">Добавляя [элементы для расширения кода Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools) и вы можете использовать средство браузера Elements в [коде Visual Studio](https://code.visualstudio.com/).</span><span class="sxs-lookup"><span data-stu-id="33c3a-105">By adding the [Elements for Microsoft Edge](https://marketplace.visualstudio.com/items?itemName=ms-edgedevtools.vscode-edge-devtools) VS Code extension, you can use the browser's Elements tool from within [Visual Studio Code](https://code.visualstudio.com/).</span></span> <span data-ttu-id="33c3a-106">При запуске или присоединении средство "элементы" подключится к экземпляру Microsoft EDGE, отобразит HTML-структуру среды выполнения и позволит вам изменить макет или устранить проблемы с стилизацией.</span><span class="sxs-lookup"><span data-stu-id="33c3a-106">By either launching or attaching, the Elements tool will connect to an instance of Microsoft Edge, display the runtime HTML structure, and allow you to alter the layout or fix styling issues.</span></span>

![GIF-файл с элементами для расширения кода пограничного и на рабочем процессе](./media/elements-for-edge.gif)

## <span data-ttu-id="33c3a-108">Запуск Microsoft Edge из расширения Elements</span><span class="sxs-lookup"><span data-stu-id="33c3a-108">Launching Microsoft Edge From the Elements extension</span></span> 

<span data-ttu-id="33c3a-109">Перейдите к элементам на **панели действий**.</span><span class="sxs-lookup"><span data-stu-id="33c3a-109">Navigate to Elements in the **Activity Bar**.</span></span> <span data-ttu-id="33c3a-110">Рядом с надписью "элементы для Microsoft Edge: targets" есть знак "плюс", который будет открывать браузер для вашего приложения.</span><span class="sxs-lookup"><span data-stu-id="33c3a-110">Next to where it says "Elements for Microsoft Edge: Targets," there is a plus sign that will open the browser for your app.</span></span> <span data-ttu-id="33c3a-111">Если вы выбрали параметр *about: Blank* , вам придется перейти к веб-приложению в браузере, чтобы оно отображалось на панели элементы в коде vs.</span><span class="sxs-lookup"><span data-stu-id="33c3a-111">If you selected the *about:blank* option, you will have to navigate to your web app in the browser for it to appear in the Elements panel in VS Code.</span></span>

## <span data-ttu-id="33c3a-112">Запуск Microsoft Edge из представления отладки</span><span class="sxs-lookup"><span data-stu-id="33c3a-112">Launching Microsoft Edge from the Debug view</span></span>

<span data-ttu-id="33c3a-113">Если вы привыкли использовать представление отладку в коде Visual Studio, вы можете получить доступ к элементам этого средства.</span><span class="sxs-lookup"><span data-stu-id="33c3a-113">If you are accustomed to using the Debug view in Visual Studio Code, you can access Elements from that tool.</span></span> <span data-ttu-id="33c3a-114">Перейдите в представление Отладка ( `Ctrl`  +  `Shift`  +  `D` в Windows или `Command`  +  `Shift`  +  `D` на компьютере Mac).</span><span class="sxs-lookup"><span data-stu-id="33c3a-114">Navigate to the Debug view (`Ctrl` + `Shift` + `D` on Windows or `Command` + `Shift` + `D` on Mac).</span></span> 

<span data-ttu-id="33c3a-115">Если у вас нет каких-либо конфигураций в коде VS, нажмите клавишу `F5` Windows или Mac или нажмите зеленую кнопку **воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="33c3a-115">If you do not have any configurations in VS Code, press `F5` on Windows or Mac or click the green **Play** button.</span></span> <span data-ttu-id="33c3a-116">В раскрывающемся списке выберите пункт "Edge".</span><span class="sxs-lookup"><span data-stu-id="33c3a-116">Select "Edge" in the dropdown.</span></span> <span data-ttu-id="33c3a-117">Теперь появится файл **Launch. JSON** со следующими конфигурацией.</span><span class="sxs-lookup"><span data-stu-id="33c3a-117">You will now see a **launch.json** file with the following configuration:</span></span>

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

<span data-ttu-id="33c3a-118">После того как вы загрузили правильную конфигурацию, нажмите клавишу `F5` Windows или Mac или нажмите зеленую кнопку **воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="33c3a-118">Now that you have loaded the correct configuration, either press `F5` on Windows or Mac or click the green **Play** button.</span></span> <span data-ttu-id="33c3a-119">Инструмент элементы, знакомый с обозревателем Microsoft EDGE, теперь будет запущен в рамках кода VS, что позволит вам получить доступ к ролика браузера и проверить компоненты страницы.</span><span class="sxs-lookup"><span data-stu-id="33c3a-119">The Elements tool you are familiar with from the Microsoft Edge browser will now launch in VS Code, allowing you to access a screencast of your browser and examine the components of your page.</span></span>

## <span data-ttu-id="33c3a-120">Присоединение к Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="33c3a-120">Attaching to Microsoft Edge</span></span>
<span data-ttu-id="33c3a-121">Если вы хотите прикрепить код VS к экземпляру Microsoft EDGE (Chromium), необходимо запустить браузер, выполнив следующую команду из teminal:</span><span class="sxs-lookup"><span data-stu-id="33c3a-121">If you'd like to attach VS Code to an instance of Microsoft Edge (Chromium), you must start the browser by running the following command from your teminal:</span></span>

`start msedge --remote-debugging-port=9222`

<span data-ttu-id="33c3a-122">После запуска приложения добавьте указанную ниже конфигурацию в файл **Launch. JSON** .</span><span class="sxs-lookup"><span data-stu-id="33c3a-122">Once the app has launched, add the configuration below to your **launch.json** file:</span></span>

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

<span data-ttu-id="33c3a-123">Выберите "присоединиться к Microsoft Edge" и откройте инструмент "элементы" в раскрывающемся меню "отладчик".</span><span class="sxs-lookup"><span data-stu-id="33c3a-123">Select "Attach to Microsoft Edge and open the Elements tool" from the Debugger drop-down menu.</span></span> <span data-ttu-id="33c3a-124">После этого нажмите `F5` на Windows или Mac или нажмите зеленую кнопку **воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="33c3a-124">Next, either press `F5` on Windows or Mac or click the green **Play** button.</span></span> <span data-ttu-id="33c3a-125">Код VS запустит инструмент элементы, что позволит вам получить доступ к экранной роли браузера, проверить модель DOM и стиль компонентов на странице.</span><span class="sxs-lookup"><span data-stu-id="33c3a-125">VS Code will launch the Elements tool, allowing you to access a screencast of your browser, inspect the DOM, and the styling of the components on your page.</span></span>

## <span data-ttu-id="33c3a-126">Отзыв</span><span class="sxs-lookup"><span data-stu-id="33c3a-126">Feedback</span></span>
<span data-ttu-id="33c3a-127">Отправьте нам отзыв, выполнив [архивацию](https://github.com/microsoft/vscode-edge-devtools/issues/new) в [репозитории GitHub](https://github.com/microsoft/vscode-edge-devtools)для этого расширения.</span><span class="sxs-lookup"><span data-stu-id="33c3a-127">Send us your feedback by [filing an issue](https://github.com/microsoft/vscode-edge-devtools/issues/new) against this extension's [GitHub repo](https://github.com/microsoft/vscode-edge-devtools).</span></span> 

<span data-ttu-id="33c3a-128">Если вы хотите помочь нам улучшить это расширение, мы будем рады вашим публикациям!</span><span class="sxs-lookup"><span data-stu-id="33c3a-128">If you want to help us make this extension better, we welcome your contributions!</span></span> <span data-ttu-id="33c3a-129">Вы можете найти все, что вам нужно, чтобы приступить к работе в [нашем репозитории GitHub](https://github.com/microsoft/vscode-edge-devtools).</span><span class="sxs-lookup"><span data-stu-id="33c3a-129">You can find everything you need to get started in [our GitHub repo](https://github.com/microsoft/vscode-edge-devtools).</span></span>