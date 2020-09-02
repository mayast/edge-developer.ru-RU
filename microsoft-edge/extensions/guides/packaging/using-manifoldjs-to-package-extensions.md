---
ms.assetid: c4397525-b978-4dc2-89bc-2198b3069742
description: Узнайте, как упаковать расширение Microsoft EDGE в привязке с помощью ManifoldJS — средства для работы с открытыми источниками Node.js.
title: Использование ManifoldJS для расширений пакетов
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/20/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: EDGE, веб-разработка, HTML, CSS, JavaScript, разработчик
ms.custom: seodec18
ms.openlocfilehash: 83aa57ae0e4ae302b1360be50e5158782b6fbb76
ms.sourcegitcommit: b88d2a55a59db8373ff2bac275d3730977bf19c9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/01/2020
ms.locfileid: "10986208"
---
# <span data-ttu-id="85f2f-104">Использование ManifoldJS для создания пакетов AppX расширений</span><span class="sxs-lookup"><span data-stu-id="85f2f-104">Using ManifoldJS to create extension AppX packages</span></span>  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

<span data-ttu-id="85f2f-105">ManifoldJS — это инструмент Open Source Node.js, который позволяет быстро и безболезненно создавать пакеты, которые можно использовать для отправки в Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="85f2f-105">ManifoldJS is an open source Node.js tool that allows you to quickly and painlessly create a package that you can then use for submission to the Microsoft Store.</span></span>  

<span data-ttu-id="85f2f-106">Если вы используете собственный обмен сообщениями в расширении, вы должны пропустить следующую статью и перейти к [встроенной службе сообщений в Microsoft Edge](../native-messaging.md#creating-an-extension-with-native-messaging) для инструкции по упаковке.</span><span class="sxs-lookup"><span data-stu-id="85f2f-106">If you use native messaging in your extension, you should skip the following article and go to [Native messaging in Microsoft Edge](../native-messaging.md#creating-an-extension-with-native-messaging) for packaging instruction.</span></span>  

<span data-ttu-id="85f2f-107">Перед тем как приступить к работе, вам по-прежнему придется прочитать статьи, посвященные следующим статьям.</span><span class="sxs-lookup"><span data-stu-id="85f2f-107">Before getting started, you will still need to read up on the following articles.</span></span>  

*   [<span data-ttu-id="85f2f-108">Расширения в Центре разработки для Windows</span><span class="sxs-lookup"><span data-stu-id="85f2f-108">Extensions in the Windows Dev Center</span></span>](./extensions-in-the-windows-dev-center.md)  
*   [<span data-ttu-id="85f2f-109">Локализация пакетов расширений</span><span class="sxs-lookup"><span data-stu-id="85f2f-109">Localizing extension packages</span></span>](./localizing-extension-packages.md)  

> [!NOTE]
> <span data-ttu-id="85f2f-110">Отправка расширения Microsoft EDGE в Microsoft Store в настоящее время ограничена возможностями.</span><span class="sxs-lookup"><span data-stu-id="85f2f-110">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span>  <span data-ttu-id="85f2f-111">Создав, упакуйте и протестировали свое расширение, отправьте запрос на [форму отправки расширения](https://developer.microsoft.com/microsoft-edge/extensions/requests).</span><span class="sxs-lookup"><span data-stu-id="85f2f-111">Once you have created, packaged and tested your extension, please submit a request on our [extension submission form](https://developer.microsoft.com/microsoft-edge/extensions/requests).</span></span>  

## <span data-ttu-id="85f2f-112">Установка Node.js и ManifoldJS</span><span class="sxs-lookup"><span data-stu-id="85f2f-112">Installing Node.js and ManifoldJS</span></span>  

<span data-ttu-id="85f2f-113">Первое, что нужно сделать, — это установить [Node.js LTS](https://nodejs.org/en/download).</span><span class="sxs-lookup"><span data-stu-id="85f2f-113">The first things you will need to do is install [Node.js LTS](https://nodejs.org/en/download).</span></span>  
<span data-ttu-id="85f2f-114">После того как у вас есть узел, в командной строке (предпочтительный PowerShell) выполните следующую команду, чтобы установить ManifoldJS.</span><span class="sxs-lookup"><span data-stu-id="85f2f-114">Once you have Node, from a command line (preferably PowerShell), run the following command to install ManifoldJS.</span></span>  

```shell
npm install -g manifoldjs
```  

<span data-ttu-id="85f2f-115">Чтобы убедиться, что вы правильно установили ManifoldJS, запустите `manifoldjs` из командной строки.</span><span class="sxs-lookup"><span data-stu-id="85f2f-115">To verify that you have correctly installed ManifoldJS, run `manifoldjs` from the command line.</span></span> <span data-ttu-id="85f2f-116">Если ManifoldJS не был распознан, добавьте `%APPDATA%\npm` его в ПЕРЕМЕННЫЕ Path.</span><span class="sxs-lookup"><span data-stu-id="85f2f-116">If ManifoldJS was not recognized, add `%APPDATA%\npm` to your PATH variables.</span></span>  

## <span data-ttu-id="85f2f-117">Упаковка с помощью ManifoldJS</span><span class="sxs-lookup"><span data-stu-id="85f2f-117">Packaging with ManifoldJS</span></span>  

<span data-ttu-id="85f2f-118">Чтобы начать процесс упаковки, необходимо открыть командную строку и изменить каталоги на папку, которая будет назначена для упакованного расширения.</span><span class="sxs-lookup"><span data-stu-id="85f2f-118">To start the packaging process, you will need to open a command line and change directories to a folder that will be the destination for your packaged extension.</span></span>  

<span data-ttu-id="85f2f-119">Например:</span><span class="sxs-lookup"><span data-stu-id="85f2f-119">For example:</span></span>

```shell
cd C:\manifoldJSTest
```  

> [!NOTE]
> <span data-ttu-id="85f2f-120">`manifoldjs`Команда выводит данные из текущего каталога и перезаписывает содержимое.</span><span class="sxs-lookup"><span data-stu-id="85f2f-120">The `manifoldjs` command outputs in the current directory and overwrites content.</span></span>  

<span data-ttu-id="85f2f-121">Теперь, когда вы используете конечную папку, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="85f2f-121">Now that you are in your destination folder, run the following command.</span></span>  

```shell
manifoldjs -l debug -p edgeextension -f edgeextension -m path\to\manifest.json
```  

<span data-ttu-id="85f2f-122">`mainifoldjs`Команду можно разбить на следующие части.</span><span class="sxs-lookup"><span data-stu-id="85f2f-122">The `mainifoldjs` command can be broken down into the following parts.</span></span>  

:::row:::
   :::column span="1":::
      `-l debug`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="85f2f-123">Изменение уровня ведения журнала на `debug` полный вывод.</span><span class="sxs-lookup"><span data-stu-id="85f2f-123">Changes the log level to `debug` to get a full print out.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `-p edgeextension`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="85f2f-124">Задает единственную платформу для выполнения преобразования `edgeextension` .</span><span class="sxs-lookup"><span data-stu-id="85f2f-124">Sets the only platform to run the conversion on to `edgeextension`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `-f edgeextension`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="85f2f-125">Сообщает программе, что формат манифеста имеет `edgeextension` Формат, и не следует следить за тем, что он не прошел проверку.</span><span class="sxs-lookup"><span data-stu-id="85f2f-125">Tells the program that the format of the manifest is an `edgeextension` format and not to care if it fails validation.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `-m \path\to\manifest.json`  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="85f2f-126">Путь к манифесту расширения, который вы хотите преобразовать.</span><span class="sxs-lookup"><span data-stu-id="85f2f-126">The path to the extension manifest that you want to convert.</span></span>  
   :::column-end:::
:::row-end:::  

<span data-ttu-id="85f2f-127">После завершения работы ManifoldJS вы получите папку со следующим содержимым.</span><span class="sxs-lookup"><span data-stu-id="85f2f-127">After ManifoldJS has finished running, you will have a folder with the following contents.</span></span>  

```text
┌ My Extension
└┬ edgeextension
 ├- generationInfo.json
 └┬ manifest
  ├- appxmanifest.xml
  ├┬ Assets
  |├- Square150x150Logo.png
  |├- Square44x44Logo.png
  |└- StoreLogo.png    
  └┬ Extension
   ├- manifest.json
   └- popup.html
```  
<!-- 
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
-->  

<span data-ttu-id="85f2f-128">generationInfo.jsдля файла — это журнал, созданный ManifoldJS, и он не будет включен в пакет расширения.</span><span class="sxs-lookup"><span data-stu-id="85f2f-128">The generationInfo.json file is a log produced by running ManifoldJS and will not be included in your extension package.</span></span> <span data-ttu-id="85f2f-129">`manifest`Будет упаковано только содержимое папки.</span><span class="sxs-lookup"><span data-stu-id="85f2f-129">Only the contents of the `manifest` folder will be packaged.</span></span> <span data-ttu-id="85f2f-130">В папке манифеста в папке Assets содержатся изображения, которые будут использоваться в пользовательском интерфейсе Windows и Microsoft Store, а в папке расширение — содержимое вашего расширения.</span><span class="sxs-lookup"><span data-stu-id="85f2f-130">Within the manifest folder, the Assets folder contains the images that will be used in the Windows and Microsoft Store UI, while the Extension folder has the contents of your extension within it.</span></span>  

<span data-ttu-id="85f2f-131">Теперь, когда у вас есть нужные файлы, вам нужно будет изменить созданный файл AppXManifest в `manifest` папке.</span><span class="sxs-lookup"><span data-stu-id="85f2f-131">Now that you have the correct files, you will need to edit the generated AppXManifest file within the `manifest` folder.</span></span> <span data-ttu-id="85f2f-132">Если в поле "имя" manifest.jsрасширения указана многоязыковая строка, то после запуска ManifoldJS имя папки верхнего уровня не будет содержать подчеркивания и включать сообщение "MSG".</span><span class="sxs-lookup"><span data-stu-id="85f2f-132">If the extension’s manifest.json file has an internationalized string for the "name" field, once ManifoldJS is run, the most top layer folder’s name will have no underscores and include "MSG".</span></span>

<span data-ttu-id="85f2f-133">Например, manifest.jsдля файла с помощью следующего `"name"` поля.</span><span class="sxs-lookup"><span data-stu-id="85f2f-133">For example, a manifest.json file with the following `"name"` field.</span></span>  

```shell
"name" : "__MSG_appName__"
```  

<span data-ttu-id="85f2f-134">у вас есть папка манифеста, в которой она находится `\<CURRENT DIRECTORY>\MSGappName\edgeextension\manifest` .</span><span class="sxs-lookup"><span data-stu-id="85f2f-134">will have a manifest folder that lives in `\<CURRENT DIRECTORY>\MSGappName\edgeextension\manifest`.</span></span>  

<span data-ttu-id="85f2f-135">В файле AppXManifest вам понадобятся следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="85f2f-135">In the AppXManifest file, you will need to:</span></span>  

 *   <span data-ttu-id="85f2f-136">Замените необходимые поля удостоверения и поле PublisherDisplayName, как показано [здесь](./creating-and-testing-extension-packages.md#app-identity-template-values).</span><span class="sxs-lookup"><span data-stu-id="85f2f-136">Replace the required Identity fields and PublisherDisplayName field as outlined [here](./creating-and-testing-extension-packages.md#app-identity-template-values).</span></span> <span data-ttu-id="85f2f-137">Обратите внимание, что если вы используете упаковку только для тестирования или для корпоративной рассылки, вы можете использовать значения заполнителей вместо регистрации для учетной записи центра разработки для Windows.</span><span class="sxs-lookup"><span data-stu-id="85f2f-137">Note that if you are only packaging for testing purposes or for enterprise distribution, you can use placeholder values instead of registering for a Windows Dev Center account.</span></span>  
 *   <span data-ttu-id="85f2f-138">Замените значки заполнителей в папке Assets значками для расширения тем же размером (150x150, 50x50, 44x44) и именами.</span><span class="sxs-lookup"><span data-stu-id="85f2f-138">Replace the placeholder icons in the Assets folder with icons for your extension with the same sizes (150x150, 50x50, 44x44) and names.</span></span> <span data-ttu-id="85f2f-139">Сведения о том, где используются эти значки, можно найти в руководстве по [проектированию](./../design.md#icons-for-packaging) .</span><span class="sxs-lookup"><span data-stu-id="85f2f-139">See the [Design](./../design.md#icons-for-packaging) guide for information about where these icons are used.</span></span>  
 *   <span data-ttu-id="85f2f-140">Если ваше расширение локализовано, следуйте инструкциям по [локализации расширений Microsoft Edge](./localizing-extension-packages.md) .</span><span class="sxs-lookup"><span data-stu-id="85f2f-140">If your extension is localized, follow the entire [Localizing Microsoft Edge extensions](./localizing-extension-packages.md) guide.</span></span> <span data-ttu-id="85f2f-141">Если он не локализован, только прочтите [имя и описание в разделе Microsoft Store](./localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) .</span><span class="sxs-lookup"><span data-stu-id="85f2f-141">If it is not localized, only read the [Localizing name and description in the Microsoft Store](./localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) section.</span></span>  

<span data-ttu-id="85f2f-142">После того как `appxmanifest.xml` файл будет отсортирован, выполните следующую команду, чтобы создать пакет.</span><span class="sxs-lookup"><span data-stu-id="85f2f-142">Once your `appxmanifest.xml` file is sorted out, run the following command to create your package.</span></span>  

```shell
manifoldjs -l debug -p edgeextension package <EXTENSION NAME>\edgeextension\manifest\
```  

<span data-ttu-id="85f2f-143">Теперь пакет будет находиться в папке **пакета** , расположенной в папке edgeextension.</span><span class="sxs-lookup"><span data-stu-id="85f2f-143">Your package will now be in the **package** folder located within the edgeextension folder.</span></span> <span data-ttu-id="85f2f-144">Дополнительные сведения о том, как неопубликованного новый пакет, можно найти в разделе [тестирование](./creating-and-testing-extension-packages.md#testing-an-appx-package) раздела Создание и тестирование пакетов расширений.</span><span class="sxs-lookup"><span data-stu-id="85f2f-144">For more information about how to sideload your new package, see [testing](./creating-and-testing-extension-packages.md#testing-an-appx-package) section of Creating and testing extension packages.</span></span>  

<span data-ttu-id="85f2f-145">После того как пакет будет проверен, вы можете отправить запрос на [форму отправки расширения](https://aka.ms/extension-request) , чтобы стать ее публикацией в Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="85f2f-145">Once your package has been tested, feel free to submit a request on our [extension submission form](https://aka.ms/extension-request) in order to be considered for publication to the Microsoft Store.</span></span>  
