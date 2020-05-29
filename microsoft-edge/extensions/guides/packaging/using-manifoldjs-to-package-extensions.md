---
ms.assetid: c4397525-b978-4dc2-89bc-2198b3069742
description: Узнайте, как упаковать расширение Microsoft EDGE в привязке с помощью ManifoldJS, с помощью средства Node. js Open Source.
title: Использование ManifoldJS для расширения пакетов
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: EDGE, веб-разработка, HTML, CSS, JavaScript, разработчик
ms.custom: seodec18
ms.openlocfilehash: cca83a26c9f80eca6454e3b5b329f72a7491b6e2
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571508"
---
# <span data-ttu-id="9918f-104">Использование ManifoldJS для создания пакетов AppX расширений</span><span class="sxs-lookup"><span data-stu-id="9918f-104">Using ManifoldJS to create extension AppX packages</span></span>  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

<span data-ttu-id="9918f-105">ManifoldJS — это инструмент Open source node. js, который позволяет быстро и безболезненно создавать пакеты, которые можно использовать для отправки в Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="9918f-105">ManifoldJS is an open source Node.js tool that allows you to quickly and painlessly create a package that you can then use for submission to the Microsoft Store.</span></span>

<span data-ttu-id="9918f-106">Если вы используете собственный обмен сообщениями в расширении, вы должны пропустить этот параметр и перейти к [встроенной службе сообщений в Microsoft Edge](../native-messaging.md#creating-an-extension-with-native-messaging) для инструкции по упаковке.</span><span class="sxs-lookup"><span data-stu-id="9918f-106">If you use native messaging in your extension, you should skip this and go to [Native messaging in Microsoft Edge](../native-messaging.md#creating-an-extension-with-native-messaging) for packaging instruction.</span></span> 

<span data-ttu-id="9918f-107">Прежде чем приступить к работе, вам по-прежнему придется прочитать следующие статьи:</span><span class="sxs-lookup"><span data-stu-id="9918f-107">Before getting started, you will still need to read up on the following articles:</span></span>

- [<span data-ttu-id="9918f-108">Расширения в центре разработки для Windows</span><span class="sxs-lookup"><span data-stu-id="9918f-108">Extensions in the Windows Dev Center</span></span>](./extensions-in-the-windows-dev-center.md)
- [<span data-ttu-id="9918f-109">Локализация пакетов расширений</span><span class="sxs-lookup"><span data-stu-id="9918f-109">Localizing extension packages</span></span>](./localizing-extension-packages.md)

> [!NOTE]
> <span data-ttu-id="9918f-110">Отправка расширения Microsoft EDGE в Microsoft Store в настоящее время ограничена возможностями.</span><span class="sxs-lookup"><span data-stu-id="9918f-110">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span> <span data-ttu-id="9918f-111">Создав, упакуйте и протестировали расширение, отправьте запрос на [форму отправки расширения](https://aka.ms/extension-request).</span><span class="sxs-lookup"><span data-stu-id="9918f-111">Once you've created, packaged and tested your extension, please submit a request on our [extension submission form](https://aka.ms/extension-request).</span></span>


## <span data-ttu-id="9918f-112">Установка Nodes. js и ManifoldJS</span><span class="sxs-lookup"><span data-stu-id="9918f-112">Installing Node.js and ManifoldJS</span></span>

<span data-ttu-id="9918f-113">Прежде всего необходимо установить [node. js LTS](https://nodejs.org/en/download/).</span><span class="sxs-lookup"><span data-stu-id="9918f-113">The first things you'll need to do is install [Node.js LTS](https://nodejs.org/en/download/).</span></span>
<span data-ttu-id="9918f-114">После того как у вас есть узел, в командной строке (предпочтительный PowerShell) выполните следующую команду, чтобы установить ManifoldJS:</span><span class="sxs-lookup"><span data-stu-id="9918f-114">Once you have Node, from a command line (preferably PowerShell), run the following command to install ManifoldJS:</span></span>

`npm install -g manifoldjs`

<span data-ttu-id="9918f-115">Чтобы убедиться, что вы правильно установили ManifoldJS, запустите `manifoldjs` из командной строки.</span><span class="sxs-lookup"><span data-stu-id="9918f-115">To verify that you've correctly installed ManifoldJS, run `manifoldjs` from the command line.</span></span> <span data-ttu-id="9918f-116">Если ManifoldJS не распознается, добавьте `%APPDATA%\npm` его в ПЕРЕМЕННЫЕ Path.</span><span class="sxs-lookup"><span data-stu-id="9918f-116">If ManifoldJS wasn't recognized, add `%APPDATA%\npm` to your PATH variables.</span></span>

## <span data-ttu-id="9918f-117">Упаковка с помощью ManifoldJS</span><span class="sxs-lookup"><span data-stu-id="9918f-117">Packaging with ManifoldJS</span></span>

<span data-ttu-id="9918f-118">Чтобы начать процесс упаковки, необходимо открыть командную строку и изменить каталоги на папку, которая будет назначена для упакованного расширения.</span><span class="sxs-lookup"><span data-stu-id="9918f-118">To start the packaging process, you'll need to open a command line and change directories to a folder that will be the destination for your packaged extension.</span></span>

<span data-ttu-id="9918f-119">Пример</span><span class="sxs-lookup"><span data-stu-id="9918f-119">For example:</span></span>

`cd C:\manifoldJSTest`

> [!NOTE]
> <span data-ttu-id="9918f-120">ManifoldJS будет выводиться в текущем каталоге и может перезаписывать содержимое.</span><span class="sxs-lookup"><span data-stu-id="9918f-120">ManifoldJS will output in the current directory and can overwrite content.</span></span>



<span data-ttu-id="9918f-121">Теперь, когда вы находитесь в конечной папке, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="9918f-121">Now that you're in your destination folder, run the following command:</span></span>

`manifoldjs -l debug -p edgeextension -f edgeextension -m <EXTENSION LOCATION>\manifest.json`


<span data-ttu-id="9918f-122">Эту команду можно разделить на следующие части:</span><span class="sxs-lookup"><span data-stu-id="9918f-122">This command can be broken down into the following parts:</span></span>
 -    <span data-ttu-id="9918f-123">**-l Отладка**: меняет уровень ведения журнала на "Отладка", чтобы получить полную распечатку.</span><span class="sxs-lookup"><span data-stu-id="9918f-123">**-l debug**: Changes the log level to "debug" to get a full print out.</span></span>
 -    <span data-ttu-id="9918f-124">**-p edgeextension**: задает единственную платформу для выполнения преобразования в edgeextension.</span><span class="sxs-lookup"><span data-stu-id="9918f-124">**-p edgeextension**: Sets the only platform to run the conversion on to edgeextension.</span></span>
 -    <span data-ttu-id="9918f-125">**-f edgeextension**: сообщает программе, что формат манифеста является форматом edgeextension, и не следует следить за тем, что он не прошел проверку.</span><span class="sxs-lookup"><span data-stu-id="9918f-125">**-f edgeextension**: Tells the program that the format of the manifest is an edgeextension format and not to care if it fails validation.</span></span>
 -    <span data-ttu-id="9918f-126">**-m \ < расположение расширения > \manifest.JSON**: путь к манифесту расширения, который вы хотите преобразовать.</span><span class="sxs-lookup"><span data-stu-id="9918f-126">**-m \<EXTENSION LOCATION>\manifest.json**: The path to the extension manifest that you want to convert.</span></span>


<span data-ttu-id="9918f-127">После завершения работы ManifoldJS вы получите папку со следующим содержанием:</span><span class="sxs-lookup"><span data-stu-id="9918f-127">After ManifoldJS has finished running, you'll have a folder with the following contents:</span></span>

    My Extension
        edgeextension
            generationInfo.json
            manifest
                   appxmanifest.xml
                Assets
                    Square150x150Logo.png
                    Square44x44Logo.png
                    StoreLogo.png    
                Extension
                    manifest.json
                    popup.html
                    ...
                ...

<span data-ttu-id="9918f-128">Файл generationInfo. JSON — это журнал, созданный ManifoldJS, и он не будет включен в пакет расширения.</span><span class="sxs-lookup"><span data-stu-id="9918f-128">The generationInfo.json file is a log produced by running ManifoldJS and won't be included in your extension package.</span></span> <span data-ttu-id="9918f-129">Будет упаковано только содержимое папки **манифеста** .</span><span class="sxs-lookup"><span data-stu-id="9918f-129">Only the contents of the **manifest** folder will be packaged.</span></span> <span data-ttu-id="9918f-130">В папке манифеста в папке Assets содержатся изображения, которые будут использоваться в пользовательском интерфейсе Windows и Microsoft Store, а в папке расширение — содержимое вашего расширения.</span><span class="sxs-lookup"><span data-stu-id="9918f-130">Within the manifest folder, the Assets folder contains the images that will be used in the Windows and Microsoft Store UI, while the Extension folder has the contents of your extension within it.</span></span>


<span data-ttu-id="9918f-131">Теперь, когда у вас есть нужные файлы, вам нужно будет изменить созданный файл AppXManifest в папке **манифеста** .</span><span class="sxs-lookup"><span data-stu-id="9918f-131">Now that you have the correct files, you'll need to edit the generated AppXManifest file within the **manifest** folder.</span></span> <span data-ttu-id="9918f-132">Если в файле Extension. JSON есть Международная строка для поля "имя", то после запуска ManifoldJS имя папки верхнего уровня не будет содержать подчеркивания и включать сообщение "MSG".</span><span class="sxs-lookup"><span data-stu-id="9918f-132">If the extension’s manifest.json file has an internationalized string for the "name" field, once ManifoldJS is run, the most top layer folder’s name will have no underscores and include "MSG".</span></span>

<span data-ttu-id="9918f-133">Например, файл manifest. JSON со следующим `"name"` полем:</span><span class="sxs-lookup"><span data-stu-id="9918f-133">For example, a manifest.json file with the following `"name"` field:</span></span>

`"name" : "__MSG_appName__"`

<span data-ttu-id="9918f-134">у вас есть папка манифеста, в которой она находится `\<CURRENT DIRECTORY>\MSGappName\edgeextension\manifest` .</span><span class="sxs-lookup"><span data-stu-id="9918f-134">will have a manifest folder that lives in `\<CURRENT DIRECTORY>\MSGappName\edgeextension\manifest`.</span></span>

<span data-ttu-id="9918f-135">В файле AppXManifest необходимо:</span><span class="sxs-lookup"><span data-stu-id="9918f-135">In the AppXManifest file, you'll need to:</span></span>
 -    <span data-ttu-id="9918f-136">Замените необходимые поля удостоверения и поле PublisherDisplayName, как показано [здесь](./creating-and-testing-extension-packages.md#app-identity-template-values).</span><span class="sxs-lookup"><span data-stu-id="9918f-136">Replace the required Identity fields and PublisherDisplayName field as outlined [here](./creating-and-testing-extension-packages.md#app-identity-template-values).</span></span> <span data-ttu-id="9918f-137">Обратите внимание, что если вы используете только упаковку для тестирования или корпоративное распространение, вы можете использовать значения заполнителей вместо регистрации для учетной записи центра разработки для Windows.</span><span class="sxs-lookup"><span data-stu-id="9918f-137">Note that if you're only packaging for testing purposes or for enterprise distribution, you can use placeholder values instead of registering for a Windows Dev Center account.</span></span>
 -    <span data-ttu-id="9918f-138">Замените значки заполнителей в папке Assets значками для расширения тем же размером (150x150, 50x50, 44x44) и именами.</span><span class="sxs-lookup"><span data-stu-id="9918f-138">Replace the placeholder icons in the Assets folder with icons for your extension with the same sizes (150x150, 50x50, 44x44) and names.</span></span> <span data-ttu-id="9918f-139">Сведения о том, где используются эти значки, можно найти в руководстве по [проектированию](./../design.md#icons-for-packaging) .</span><span class="sxs-lookup"><span data-stu-id="9918f-139">See the [Design](./../design.md#icons-for-packaging) guide for information about where these icons are used.</span></span>
 - <span data-ttu-id="9918f-140">Если ваше расширение локализовано, следуйте инструкциям по [локализации расширений Microsoft Edge](./localizing-extension-packages.md) .</span><span class="sxs-lookup"><span data-stu-id="9918f-140">If your extension is localized, follow the entire [Localizing Microsoft Edge extensions](./localizing-extension-packages.md) guide.</span></span> <span data-ttu-id="9918f-141">Если он не локализован, только прочтите [имя и описание в разделе Microsoft Store](./localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) .</span><span class="sxs-lookup"><span data-stu-id="9918f-141">If it isn't localized, only read the [Localizing name and description in the Microsoft Store](./localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) section.</span></span>

<span data-ttu-id="9918f-142">После того как файл AppxManifest. XML будет отсортирован, выполните следующую команду, чтобы создать пакет.</span><span class="sxs-lookup"><span data-stu-id="9918f-142">Once your appxmanifest.xml file is sorted out, run the following command to create your package:</span></span>

`manifoldjs -l debug -p edgeextension package <EXTENSION NAME>\edgeextension\manifest\`

<span data-ttu-id="9918f-143">Теперь пакет будет находиться в папке **пакета** , расположенной в папке edgeextension.</span><span class="sxs-lookup"><span data-stu-id="9918f-143">Your package will now be in the **package** folder located within the edgeextension folder.</span></span> <span data-ttu-id="9918f-144">Сведения о том, как неопубликованного новый пакет, можно найти [в разделе Создание и тестирование пакетов](./creating-and-testing-extension-packages.md#testing-an-appx-package) расширений.</span><span class="sxs-lookup"><span data-stu-id="9918f-144">See Creating and testing extension packages' [testing](./creating-and-testing-extension-packages.md#testing-an-appx-package) section for info on how to sideload your new package.</span></span>

<span data-ttu-id="9918f-145">После того как пакет будет проверен, вы можете отправить запрос на [форму отправки расширения](https://aka.ms/extension-request) , чтобы стать ее публикацией в Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="9918f-145">Once your package has been tested, feel free to submit a request on our [extension submission form](https://aka.ms/extension-request) in order to be considered for publication to the Microsoft Store.</span></span>
