---
ms.assetid: f3560505-e01f-47e5-9ad6-7a419f060fc2
description: Узнайте о том, как использовать встроенные системы обмена сообщениями, чтобы ваше расширение могло взаимодействовать с сопутствующим приложением UWP.
title: Расширения — упаковка
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: EDGE, веб-разработка, HTML, CSS, JavaScript, разработчик
ms.openlocfilehash: 23c97f366db527cae2672d6ad46fa666583f6398
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571526"
---
# <span data-ttu-id="53ae0-104">Упаковка расширений Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="53ae0-104">Packaging Microsoft Edge extensions</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="53ae0-105">Наконец, вы закончите свое расширение и готовы упаковать его.</span><span class="sxs-lookup"><span data-stu-id="53ae0-105">So you've finally completed your extension and are ready to package it up.</span></span> <span data-ttu-id="53ae0-106">Возможно, вам будет интересно узнать, что происходит в ходе выполнения следующих действий в руки потенциальных пользователей.</span><span class="sxs-lookup"><span data-stu-id="53ae0-106">You might be wondering what the next steps are toward getting this in the hands of potential users.</span></span> <span data-ttu-id="53ae0-107">Это руководство предназначено для изучения того, как это сделать.</span><span class="sxs-lookup"><span data-stu-id="53ae0-107">This guide is intended to teach you how to do just that.</span></span>

<span data-ttu-id="53ae0-108">Руководство по упаковке расширений является исчерпывающим в том, что оно охватывает все, что нужно знать о упаковках, даже более детально nitty gritty.</span><span class="sxs-lookup"><span data-stu-id="53ae0-108">The extension packaging guide is comprehensive in that it covers everything you'd want to know about packaging, even the finer, nitty gritty details.</span></span> <span data-ttu-id="53ae0-109">Если вы не хотите изучать все, что нужно знать о том, как упаковать расширение, вы будете в курсе.</span><span class="sxs-lookup"><span data-stu-id="53ae0-109">If you don't want to learn everything there is to know about packaging your extension, you're in luck.</span></span> <span data-ttu-id="53ae0-110">Добавлена поддержка расширений для ManifoldJS — средства Open source node. js, которые занимают большую часть упаковки woes.</span><span class="sxs-lookup"><span data-stu-id="53ae0-110">We've added support for extensions to ManifoldJS, an open source Node.js tool that takes the majority of your packaging woes away.</span></span>

> [!NOTE]
> <span data-ttu-id="53ae0-111">Отправка расширения Microsoft EDGE в Microsoft Store в настоящее время ограничена возможностями.</span><span class="sxs-lookup"><span data-stu-id="53ae0-111">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span> <span data-ttu-id="53ae0-112">[Поделитесь с нами](https://aka.ms/extension-request) с помощью ваших запросов на участие в Microsoft Store, и мы поможем вам ознакомиться с будущими обновлениями.</span><span class="sxs-lookup"><span data-stu-id="53ae0-112">[Reach out to us](https://aka.ms/extension-request) with your requests to be a part of the Microsoft Store, and we’ll consider you for a future update.</span></span>


<span data-ttu-id="53ae0-113">Воспользуйтесь приведенной ниже структурой "процесс" для подключения к упаковке Adventure!</span><span class="sxs-lookup"><span data-stu-id="53ae0-113">Use the process outline below to map out your packaging adventure!</span></span>


## [<span data-ttu-id="53ae0-114">Расширения в центре разработки для Windows</span><span class="sxs-lookup"><span data-stu-id="53ae0-114">Extensions in the Windows Dev Center</span></span>](./packaging/extensions-in-the-windows-dev-center.md)

<span data-ttu-id="53ae0-115">Независимо от того, какой маршрут создания пакетов вы выбрали, вручную или ManifoldJS, первым этапом является регистрация учетной записи разработчика Windows и резервирование имен ваших расширений.</span><span class="sxs-lookup"><span data-stu-id="53ae0-115">No matter which package creation route you choose, manual or ManifoldJS, the first step is registering for a Windows Developer account and reserving the name(s) of your extension.</span></span>

<span data-ttu-id="53ae0-116">После этого вы можете перейти в раздел [Создание и тестирование пакетов расширений](./packaging/creating-and-testing-extension-packages.md) , чтобы выяснить, как создаются appx-пакеты и вы вручную упаковывает свое расширение, либо просто перейдете на него и переходите к [использованию ManifoldJS в расширениях пакетов](./packaging/using-ManifoldJS-to-package-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="53ae0-116">Once you've done this, you can either move on to [Creating and testing extension packages](./packaging/creating-and-testing-extension-packages.md) to learn how AppXs are created and manually package your extension, or go the easier route and jump to [Using ManifoldJS to package extensions](./packaging/using-ManifoldJS-to-package-extensions.md).</span></span>

> [!NOTE]
> <span data-ttu-id="53ae0-117">После того как вы зайдете в США и хотите, чтобы ваше расширение было утверждено в магазине Microsoft Store, ознакомьтесь со [списком для отправки приложения](https://docs.microsoft.com/windows/uwp/publish/app-submissions).</span><span class="sxs-lookup"><span data-stu-id="53ae0-117">Once you've reached out to us and have been approved to have your extension in the Microsoft Store, check out the [app submission checklist](https://docs.microsoft.com/windows/uwp/publish/app-submissions).</span></span>


## [<span data-ttu-id="53ae0-118">Создание и тестирование пакетов расширений</span><span class="sxs-lookup"><span data-stu-id="53ae0-118">Creating and testing extension packages</span></span>](./packaging/creating-and-testing-extension-packages.md)

<span data-ttu-id="53ae0-119">Этот раздел руководства проходит через создание пакета расширения вручную, как только [вы настроили свою учетную запись разработчика Windows и заменили имена расширений (-ов)](./packaging/extensions-in-the-windows-Dev-Center.md).</span><span class="sxs-lookup"><span data-stu-id="53ae0-119">This section of the guide walks through manual extension package creation once [you've set up your Windows Developer account and reserved your extension name(s)](./packaging/extensions-in-the-windows-Dev-Center.md).</span></span> <span data-ttu-id="53ae0-120">Если вы хотите больше узнать о том, как упаковать расширение, дайте это чтение.</span><span class="sxs-lookup"><span data-stu-id="53ae0-120">If you're curious about the finer details of packaging an extension, give this a read.</span></span>

<span data-ttu-id="53ae0-121">Кроме того, в этой статье приведены сведения о том, как [тестировать и распаковать упакованное расширение](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package).</span><span class="sxs-lookup"><span data-stu-id="53ae0-121">Also included is info on how to [test and unpack a packaged extension](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package).</span></span> <span data-ttu-id="53ae0-122">Эта информация важна даже в том случае, если вы проходили маршрут на упаковке ManifoldJS.</span><span class="sxs-lookup"><span data-stu-id="53ae0-122">This info is relevant even if you've gone the ManifoldJS packaging route.</span></span>

## [<span data-ttu-id="53ae0-123">Локализация пакетов расширений</span><span class="sxs-lookup"><span data-stu-id="53ae0-123">Localizing extension packages</span></span>](./packaging/localizing-extension-packages.md)
<span data-ttu-id="53ae0-124">Этап локализации пакета находится между созданием файла appxmanifest. XML и выполнением финальной команды для упаковки расширения.</span><span class="sxs-lookup"><span data-stu-id="53ae0-124">The package localization step falls between creating your appxmanifest.xml file and running the final command to package your extension.</span></span>
<span data-ttu-id="53ae0-125">Это позволяет указать, какие языки поддерживаются в вашем описании в магазине Microsoft Store, а также выбрать язык, на котором будет отображаться имя расширения в Windows.</span><span class="sxs-lookup"><span data-stu-id="53ae0-125">This allows you to indicate which languages your extensions supports in your Microsoft Store listing, and what language your extension's name appears in Windows.</span></span>

<span data-ttu-id="53ae0-126">Вы можете перейти к [локализованному имени и описанию в Microsoft Store](./packaging/localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) в этом разделе руководства, если ваше расширение не поддерживает несколько языков.</span><span class="sxs-lookup"><span data-stu-id="53ae0-126">You can jump to [Localizing name and description for the Microsoft Store](./packaging/localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) in this section of the guide if your extension doesn't support multiple languages.</span></span>

## [<span data-ttu-id="53ae0-127">Использование ManifoldJS для расширения пакетов</span><span class="sxs-lookup"><span data-stu-id="53ae0-127">Using ManifoldJS to package extensions</span></span>](./packaging/using-ManifoldJS-to-package-extensions.md)

<span data-ttu-id="53ae0-128">На маршруте инструмента для упаковки вашего расширения ManifoldJS будет упаковываться расширение в привязке с минимальными усилиями на вашем конечном итоге.</span><span class="sxs-lookup"><span data-stu-id="53ae0-128">The tool route for packaging your extension, ManifoldJS will package up your extension in a snap with minimal effort on your end.</span></span> <span data-ttu-id="53ae0-129">Предоставляя доступ к некоторым ресурсам Windows/Microsoft Store после того, как вы заполните некоторые свойства AppXManifest, и ваше расширение будет упаковано без времени.</span><span class="sxs-lookup"><span data-stu-id="53ae0-129">Provide a few Windows/Microsoft Store assets after filling out some AppXManifest properties and your extension will be packaged in no time.</span></span>

<span data-ttu-id="53ae0-130">После упаковки расширения вы можете ознакомиться с разделом [тестирование](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package) создания и тестирования расширения Microsoft EDGE, чтобы узнать, как неопубликованного или распаковать его.</span><span class="sxs-lookup"><span data-stu-id="53ae0-130">Once your extension is packaged, see the [testing](./packaging/creating-and-testing-extension-packages.md#testing-an-appx-package) section of Creating and testing your Microsoft Edge extension to learn how to sideload or unpack it.</span></span>


## [<span data-ttu-id="53ae0-131">Запуск комплекта сертификации приложений для Windows</span><span class="sxs-lookup"><span data-stu-id="53ae0-131">Running the Windows App Certification Kit</span></span>](./packaging/running-the-windows-app-certification-kit.md)

<span data-ttu-id="53ae0-132">После того как у вас есть упакованное расширение, вы можете запустить его с помощью комплекта сертификации приложений для Windows.</span><span class="sxs-lookup"><span data-stu-id="53ae0-132">Once you have a packaged extension, you can then run it through the Windows App Certification Kit.</span></span> <span data-ttu-id="53ae0-133">Это приведет к тому, что в пакете расширения будет выполняться ряд тестов, чтобы убедиться, что он готов для Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="53ae0-133">Doing so will run a number of tests on your extension package to ensure that it's ready for the Microsoft Store.</span></span>
