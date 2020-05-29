---
ms.assetid: c4043c1e-15ac-4210-8851-3804c7708f49
description: Сведения о том, как локализовать пакет расширения Microsoft Edge таким образом, чтобы он был готов к использованию нескольких языковых стандартов при выпуске.
title: Локализация пакетов расширений
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: EDGE, веб-разработка, HTML, CSS, JavaScript, разработчик
ms.custom: seodec18
ms.openlocfilehash: a6a920b80e915bb14c7ea24abcc54105e5b34eb0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571512"
---
# <span data-ttu-id="378e8-104">Локализация расширений Microsoft Edge для Windows и Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="378e8-104">Localizing Microsoft Edge extensions for Windows and the Microsoft Store</span></span>  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

<span data-ttu-id="378e8-105">Это руководство содержит сведения о том, как локализовать расширение Microsoft EDGE, чтобы оно было готово для нескольких национальных настроек при выпуске.</span><span class="sxs-lookup"><span data-stu-id="378e8-105">This guide walks through how to localize your Microsoft Edge extension so that it's ready for multiple locales upon release.</span></span> <span data-ttu-id="378e8-106">Чтобы полностью локализовать расширение, вам потребуется выполнить действия, описанные как в Windows, так и в Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="378e8-106">To fully localize your extension, you'll need to follow the steps for both Windows and the Microsoft Store.</span></span>

<span data-ttu-id="378e8-107">Если вы хотите локализовать ресурсы расширения для Microsoft EDGE, вы можете научиться использовать платформу i18n в [руководстве по интернационализации](../internationalization.md).</span><span class="sxs-lookup"><span data-stu-id="378e8-107">If you want to localize your extension resources for Microsoft Edge, you can learn how to use the i18n framework in the [Internationalization guide](../internationalization.md).</span></span>


> [!NOTE]
> <span data-ttu-id="378e8-108">Если ваше расширение не поддерживает несколько языков, вы можете перейти к [локализованному имени и описанию в Microsoft Store](#localizing-name-and-description-in-the-microsoft-store).</span><span class="sxs-lookup"><span data-stu-id="378e8-108">If your extension doesn't support multiple languages, you can skip to [Localizing name and description in the Microsoft Store](#localizing-name-and-description-in-the-microsoft-store).</span></span>


## <span data-ttu-id="378e8-109">Общие сведения о процессе локализации</span><span class="sxs-lookup"><span data-stu-id="378e8-109">The localization process overview</span></span>

<span data-ttu-id="378e8-110">Первый шаг к извлечению расширения, доступного для широкой аудитории, — это [Настройка ее appxmanifest](#configuring-the-appxmanifest) для нескольких языков.</span><span class="sxs-lookup"><span data-stu-id="378e8-110">The first step towards getting your extension available to a wide audience is to [configure its AppxManifest](#configuring-the-appxmanifest) for multiple languages.</span></span> <span data-ttu-id="378e8-111">В Microsoft Store пользователи будут показывать языки, поддерживаемые вашим расширением.</span><span class="sxs-lookup"><span data-stu-id="378e8-111">In the Microsoft Store, this will show users what languages your extension supports.</span></span> <span data-ttu-id="378e8-112">Некоторые поля в AppxManifest также нужно изменить, если вы хотите, чтобы имя расширения [локализуется в пользовательском интерфейсе Windows и в Microsoft Store](#localizing-extension-resources-for-windows-and-the-microsoft-store).</span><span class="sxs-lookup"><span data-stu-id="378e8-112">Certain fields in the AppxManifest will also need to be changed if you want the name of your extension to be [localized in the Windows UI and the Microsoft Store](#localizing-extension-resources-for-windows-and-the-microsoft-store).</span></span>


<span data-ttu-id="378e8-113">После настройки AppxManifest вам потребуется [создать строковые ресурсы JSON](#creating-json-string-resources) для языков, которые вы указали как поддерживаемые.</span><span class="sxs-lookup"><span data-stu-id="378e8-113">Once your AppxManifest is configured, you'll need to [create JSON string resources](#creating-json-string-resources) for the languages that you indicated as supported.</span></span> <span data-ttu-id="378e8-114">Для этого требуется создать RESJSON-файл для каждого языка, где в каждом файле есть все строки пользовательского интерфейса на этом языке.</span><span class="sxs-lookup"><span data-stu-id="378e8-114">This requires creating a .resjson file for each language, where each file has all the UI strings of that language within it.</span></span>


<span data-ttu-id="378e8-115">После того как RESJSON файлы для поддерживаемых языков будут сделаны, потребуется [создать файл ресурсов с расширением PRI](#creating-the-resources-file).</span><span class="sxs-lookup"><span data-stu-id="378e8-115">After the .resjson files for the supported languages have been made, a [.pri resource file will need to be created](#creating-the-resources-file).</span></span> <span data-ttu-id="378e8-116">Она будет создана с помощью файла конфигурации для средства **MakePRI** , которое входит в состав [пакета SDK для Windows 10](https://developer.microsoft.com/windows/downloads/windows-10-sdk).</span><span class="sxs-lookup"><span data-stu-id="378e8-116">This will be created by using a configuration file to the **MakePRI** tool that comes with the [Windows 10 SDK](https://developer.microsoft.com/windows/downloads/windows-10-sdk).</span></span> 

> [!NOTE]
> <span data-ttu-id="378e8-117">Если вы загружаете пакет SDK для Windows 10 для использования средства MakePri. exe, вы можете выбрать только "средства подписывания Windows SDK для классических приложений" и "Windows SDK для управляемых приложений UWP", чтобы сделать скачивание более светлым.</span><span class="sxs-lookup"><span data-stu-id="378e8-117">If you are only downloading the Windows 10 SDK to use the MakePri.exe tool, you can select only the "Windows SDK Signing Tools for Desktop Apps" and "Windows SDK for UWP Managed Apps" features to keep the download lighter.</span></span> <span data-ttu-id="378e8-118">Средство MakePri. exe появится во вложенных папках папки C:\Program Files (x86) \Windows Kits\10\bin\10.0.17713.0.</span><span class="sxs-lookup"><span data-stu-id="378e8-118">The MakePri.exe tool will appear in subfolders of C:\Program Files (x86)\Windows Kits\10\bin\10.0.17713.0.</span></span>


<span data-ttu-id="378e8-119">После того как вы загрузили расширение, последний этап — [локализовать название и описание в Microsoft Store](#localizing-name-and-description-in-the-microsoft-store).</span><span class="sxs-lookup"><span data-stu-id="378e8-119">Once you've uploaded your extension, the final step is to [localize the name and description in the Microsoft Store](#localizing-name-and-description-in-the-microsoft-store).</span></span>

> [!NOTE]
> <span data-ttu-id="378e8-120">Отправка расширения Microsoft EDGE в Microsoft Store в настоящее время ограничена возможностями.</span><span class="sxs-lookup"><span data-stu-id="378e8-120">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span> <span data-ttu-id="378e8-121">[Поделитесь с нами](https://aka.ms/extension-request) с помощью ваших запросов на участие в Microsoft Store, и мы поможем вам ознакомиться с будущими обновлениями.</span><span class="sxs-lookup"><span data-stu-id="378e8-121">[Reach out to us](https://aka.ms/extension-request) with your requests to be a part of the Microsoft Store, and we'll consider you for a future update.</span></span>



## <span data-ttu-id="378e8-122">Настройка AppXManifest</span><span class="sxs-lookup"><span data-stu-id="378e8-122">Configuring the AppXManifest</span></span>

<span data-ttu-id="378e8-123">Список поддерживаемых языков расширения в магазине Microsoft Store формируется на основе его значений AppXManifest.</span><span class="sxs-lookup"><span data-stu-id="378e8-123">Your extension's "Supported languages" list in the Microsoft Store is generated based on its AppXManifest values.</span></span> <span data-ttu-id="378e8-124">Этот список указывается с помощью `Resource` элемента.</span><span class="sxs-lookup"><span data-stu-id="378e8-124">This list is specified using the `Resource` element.</span></span>


![изображение параметров](./../../media/language-app-details.png)

<span data-ttu-id="378e8-126">Чтобы задать список языков, которые поддерживаются вашим расширением, вы можете добавить `Resource` элемент в следующем формате (этот `Resource` элемент будет показываться в Microsoft Store на английском, немецком и французском языках):</span><span class="sxs-lookup"><span data-stu-id="378e8-126">To specify the list of languages that are supported by your extension, you can add a `Resource` element in the format seen below (this `Resource` element will show support for English, German, and French in the Microsoft Store):</span></span>

```xml
<Resources>
    <Resource Language="en-us"/>
    <Resource Language="de-de"/>
    <Resource Language="fr-fr"/>
</Resources>
```

<span data-ttu-id="378e8-127">Сведения о языках и кодах языков, поддерживаемых Microsoft Store, можно найти на странице [Поддерживаемые языки](https://msdn.microsoft.com/windows/uwp/publish/supported-languages) .</span><span class="sxs-lookup"><span data-stu-id="378e8-127">See [Supported languages](https://msdn.microsoft.com/windows/uwp/publish/supported-languages) for info on the languages/language codes that the Microsoft Store supports.</span></span>


<span data-ttu-id="378e8-128">Чтобы указать локализованные строки для всех общедоступных элементов, отображаемых в AppxManifest, необходимо использовать идентификатор ресурса в формате `ms-resource:<resource id>` .</span><span class="sxs-lookup"><span data-stu-id="378e8-128">In order to specify localized strings for all publicly visible elements in the AppxManifest, you'll have to use a resource identifier in the format of `ms-resource:<resource id>`.</span></span>

<span data-ttu-id="378e8-129">В приведенных ниже фрагментах кода выводятся полные AppxManifest.</span><span class="sxs-lookup"><span data-stu-id="378e8-129">The snippets below make a complete AppxManifest.</span></span> <span data-ttu-id="378e8-130">Из локализованных файлов ресурсов должны извлекаться следующие значения:</span><span class="sxs-lookup"><span data-stu-id="378e8-130">The following values should be retrieved from localized resource files:</span></span>

- <span data-ttu-id="378e8-131">Properties\DisplayName</span><span class="sxs-lookup"><span data-stu-id="378e8-131">Properties\DisplayName</span></span>
- <span data-ttu-id="378e8-132">Properties\Description</span><span class="sxs-lookup"><span data-stu-id="378e8-132">Properties\Description</span></span>
- <span data-ttu-id="378e8-133">Properties\PublisherDisplayName</span><span class="sxs-lookup"><span data-stu-id="378e8-133">Properties\PublisherDisplayName</span></span>


```xml
<Properties>
    <DisplayName>ms-resource:DisplayName</DisplayName>
    <Description>ms-resource:Description</Description>
    <Logo>Assets\PackageLogo.png</Logo>
    <PublisherDisplayName>ms-resource:PublisherName</PublisherDisplayName>
</Properties>
```

- <span data-ttu-id="378e8-134">Applications\Application\VisualElements\DisplayName</span><span class="sxs-lookup"><span data-stu-id="378e8-134">Applications\Application\VisualElements\DisplayName</span></span>
- <span data-ttu-id="378e8-135">Applications\Application\VisualElements\Description</span><span class="sxs-lookup"><span data-stu-id="378e8-135">Applications\Application\VisualElements\Description</span></span>
- <span data-ttu-id="378e8-136">Applications\Application\Extensions\Extension\AppExtension\DisplayName</span><span class="sxs-lookup"><span data-stu-id="378e8-136">Applications\Application\Extensions\Extension\AppExtension\DisplayName</span></span>

```xml
<Applications>
    <Application Id="App">
      <uap:VisualElements
        AppListEntry="none"
            DisplayName="ms-resource:DisplayName"
       Square150x150Logo="Assets\Square150x150Logo.png"
       Square44x44Logo="Assets\Square44x44Logo.png"
            Description="ms-resource:Description"
        BackgroundColor="transparent">
      </uap:VisualElements>
      <Extensions>
      <uap3:Extension Category="windows.appExtension">
        <uap3:AppExtension Name="com.microsoft.edge.extension"
            Id="MicrosoftTranslate"
            PublicFolder="Extension"
            DisplayName="ms-resource:DisplayName">
        </uap3:AppExtension>
      </uap3:Extension>
      </Extensions>
    </Application>
  </Applications>
```


## <span data-ttu-id="378e8-137">Локализация ресурсов расширений для Windows и Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="378e8-137">Localizing extension resources for Windows and the Microsoft Store</span></span>

<span data-ttu-id="378e8-138">Теперь, когда ваша AppxManifest настроена для нескольких языков, есть несколько ключевых различий, которые необходимо знать между локализацией пользовательского интерфейса в расширении и локализацией расширения для Windows и Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="378e8-138">Now that your AppxManifest is configured for multiple languages, there are some key differences you should know between localizing the UI within your extension and localizing your extension for Windows and the Microsoft Store.</span></span>

<span data-ttu-id="378e8-139">Несмотря на то, что расширения Microsoft EDGE не работают за пределами Microsoft EDGE, управление ими может происходить в Windows.</span><span class="sxs-lookup"><span data-stu-id="378e8-139">While Microsoft Edge extensions don't run outside of Microsoft Edge, the management of them can occur within Windows.</span></span> <span data-ttu-id="378e8-140">Например, пользователи могут управлять своими расширениями в приложении "Параметры".</span><span class="sxs-lookup"><span data-stu-id="378e8-140">For example, users can manage their extensions in the Settings app:</span></span>


![изображение параметров](./../../media/settings.png)



<span data-ttu-id="378e8-142">Имя расширения, которое отображается в приложении "Параметры" в Windows, поступает из AppXManifest.</span><span class="sxs-lookup"><span data-stu-id="378e8-142">The name of the extension that shows up in the Settings app in Windows comes from the AppXManifest.</span></span> <span data-ttu-id="378e8-143">Если это значение жестко на английском языке, английская версия названия будет отображаться на неанглийских устройствах Windows.</span><span class="sxs-lookup"><span data-stu-id="378e8-143">If this value is hardcoded in English, the English version of the name will show up on non-English Windows devices.</span></span> <span data-ttu-id="378e8-144">Если фирменная символика расширения — только на английском языке, это можно сделать без зашиты.</span><span class="sxs-lookup"><span data-stu-id="378e8-144">If the branding of your extension is English only, it's ok to leave it hardcoded.</span></span>


> [!NOTE]
> <span data-ttu-id="378e8-145">Если вы хотите использовать локализованные имена для расширения Microsoft EDGE в Windows, убедитесь, что локализованные имена также [доступны и зарезервированы](./extensions-in-the-windows-dev-center.md#name-reservation) , прежде чем вносить изменения в файл AppXManifest.</span><span class="sxs-lookup"><span data-stu-id="378e8-145">If you want to use localized names for your Microsoft Edge Extension in Windows, make sure the localized names are also [available and reserved](./extensions-in-the-windows-dev-center.md#name-reservation) before you make the changes in the AppXManifest file.</span></span> <span data-ttu-id="378e8-146">Если имена не зарезервированы, при отправке финального пакета в центр разработки для Windows появляется следующее сообщение об ошибке:</span><span class="sxs-lookup"><span data-stu-id="378e8-146">If the names are not reserved, you'll get the following error when you upload the final package to Windows Dev Center:</span></span></br></br>

![Ошибка языка](./../../media/language-error.png)</br></br>


<span data-ttu-id="378e8-148">Инфраструктура локализации на основе i18n, определенная для расширений JavaScript, применима только в среде Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="378e8-148">The i18n based localization infrastructure that's defined for JavaScript extensions is only applicable within the Microsoft Edge environment.</span></span>

<span data-ttu-id="378e8-149">За пределами Microsoft EDGE в Windows и Microsoft Store единственным набором поддерживаемых платформ локализации является платформа для локализации универсальной платформы Windows (UWP).</span><span class="sxs-lookup"><span data-stu-id="378e8-149">Outside of Microsoft Edge, within Windows and the Microsoft Store, the only supported localization framework is based on the Universal Windows Platform (UWP) localization framework.</span></span>

<span data-ttu-id="378e8-150">Несмотря на то что мы поддерживаем ресурсы на основе JSON для приложений для Windows на базе HTML, схема для ресурсов JSON не совпадает с определением для расширений JavaScript.</span><span class="sxs-lookup"><span data-stu-id="378e8-150">While we do support JSON based resources for HTML based Windows apps, the schema for the JSON resources doesn't match the one defined for JavaScript extensions.</span></span>


<span data-ttu-id="378e8-151">Ниже описаны основные отличия в [приложениях для Windows на основе HTML](https://msdn.microsoft.com/library/windows/apps/hh465228.aspx).</span><span class="sxs-lookup"><span data-stu-id="378e8-151">The following are the key differences in [HTML based Windows apps](https://msdn.microsoft.com/library/windows/apps/hh465228.aspx):</span></span>
-    <span data-ttu-id="378e8-152">Ресурсы задаются в файлах RESJSON вместо файлов JSON.</span><span class="sxs-lookup"><span data-stu-id="378e8-152">Resources are specified in .resjson files instead of .json files.</span></span>
-    <span data-ttu-id="378e8-153">Поддерживаемые национальные настройки должны быть указаны в файле AppXManifest, в котором первый язык используется по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="378e8-153">The locales supported should be specified in the AppXManifest file, with the first locale being the default locale.</span></span>
-    <span data-ttu-id="378e8-154">Для использования ресурсов в приложениях для Windows на основе HTML используется следующая схема:</span><span class="sxs-lookup"><span data-stu-id="378e8-154">HTML based Windows apps resources use the following schema:</span></span>
    ```json
    {
        "greeting"              : "Hello",
        "_greeting.comment"     : "A welcome greeting.",

        "farewell"              : "Goodbye",
        "_farewell.comment"     : "A goodbye."
    }
    ```
    <span data-ttu-id="378e8-155">Пара имя/значение, обозначенная подчеркиванием, — это комментарии к соответствующему строковому ресурсу.</span><span class="sxs-lookup"><span data-stu-id="378e8-155">The name/value pair denoted by an underscore are comments for the corresponding string resource.</span></span>
-    <span data-ttu-id="378e8-156">файлы. resjson компилируются в PRI-файлы, которые должны быть включены во время создания пакета AppX.</span><span class="sxs-lookup"><span data-stu-id="378e8-156">.resjson files are compiled into .pri files which must be included during AppX package creation.</span></span>


### <span data-ttu-id="378e8-157">Создание строковых ресурсов JSON</span><span class="sxs-lookup"><span data-stu-id="378e8-157">Creating JSON string resources</span></span>
<span data-ttu-id="378e8-158">После настройки AppxManifest в руки и различий между платформами i18n и для локализации UWP вы можете создавать файлы ресурсов.</span><span class="sxs-lookup"><span data-stu-id="378e8-158">With a configured AppxManifest in hand and the differences between the i18n and UWP localization frameworks highlighted, you're ready to create your resource files.</span></span>

<span data-ttu-id="378e8-159">Только одна строка ресурса в манифесте применима к пакетам расширений Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="378e8-159">Only one resource string in the manifest is applicable to Microsoft Edge extension packages.</span></span> <span data-ttu-id="378e8-160">`DisplayName`Строка обычно локализуется в расширениях JavaScript и может быть легко сопоставлена с файлами. resjson, которые предполагается использовать для Windows.</span><span class="sxs-lookup"><span data-stu-id="378e8-160">The `DisplayName` string is commonly localized in JavaScript extensions, and can be easily mapped to the .resjson files that Windows expects.</span></span> <span data-ttu-id="378e8-161">Предполагается, что это единственный ресурс, который вы хотите локализовать, — образец файла. resjson, который нужно создать:</span><span class="sxs-lookup"><span data-stu-id="378e8-161">Assuming that this is the only resource that you would like to localize, here is a sample .resjson file that should be created:</span></span>

```json
{
    "DisplayName"              : "Jigsaw",
    "_DisplayName.comment"     : "Name of extension."
}
```

<span data-ttu-id="378e8-162">Идентификатор ресурса в каждом файле. resjson должен совпадать с ИДЕНТИФИКАТОРом, используемым в AppXManifest.</span><span class="sxs-lookup"><span data-stu-id="378e8-162">The resource ID in each .resjson file needs to match the ID used in the AppXManifest.</span></span> <span data-ttu-id="378e8-163">С помощью приведенного выше фрагмента example. resjson должна быть указана соответствующая запись AppXManifest:</span><span class="sxs-lookup"><span data-stu-id="378e8-163">Using the example .resjson snippet above, the corresponding AppXManifest entry should be:</span></span>

`DisplayName="ms-resource:DisplayName"`

<span data-ttu-id="378e8-164">Каждый язык, поддерживаемый вашим расширением, должен иметь соответствующий файл Resources. RESJSON и размещаться в следующей структуре папок:</span><span class="sxs-lookup"><span data-stu-id="378e8-164">Each language that your extension supports should have a corresponding resources.resjson file and be placed in the following folder structure:</span></span>

![Структура папок на языке](./../../media/resources-folder.png)


### <span data-ttu-id="378e8-166">Создание файла ресурсов</span><span class="sxs-lookup"><span data-stu-id="378e8-166">Creating the resources file</span></span>
<span data-ttu-id="378e8-167">После создания всех файлов. resjson вы можете создать файл индекса ресурсов пакета (PRI).</span><span class="sxs-lookup"><span data-stu-id="378e8-167">Once you've created all your .resjson files, you're ready to create your package resource index (PRI) file.</span></span> <span data-ttu-id="378e8-168">В этом файле хранятся ресурсы для всех поддерживаемых языков.</span><span class="sxs-lookup"><span data-stu-id="378e8-168">This file stores the resources for all your supported languages.</span></span> <span data-ttu-id="378e8-169">Для этого можно использовать средство **MakePRI** , которое входит в состав пакета SDK для Windows 10.</span><span class="sxs-lookup"><span data-stu-id="378e8-169">To do this you can use the **MakePRI** tool which is included with the Windows 10 SDK.</span></span>


<span data-ttu-id="378e8-170">Сначала необходимо создать файл конфигурации.</span><span class="sxs-lookup"><span data-stu-id="378e8-170">First you'll need to create the configuration file.</span></span> <span data-ttu-id="378e8-171">Это определяет используемые по умолчанию квалификаторы и платформу для ресурсов.</span><span class="sxs-lookup"><span data-stu-id="378e8-171">This defines the default qualifiers and platform for the resources.</span></span> <span data-ttu-id="378e8-172">В этом примере сделайте язык по умолчанию английским (US) и платформой Windows 10.</span><span class="sxs-lookup"><span data-stu-id="378e8-172">For this example, make the default language English (US) and the platform Windows 10.</span></span> <span data-ttu-id="378e8-173">Для этого создайте файл priconfig. XML со следующим содержанием в [корневой каталог]:</span><span class="sxs-lookup"><span data-stu-id="378e8-173">To do this, create a priconfig.xml file with the following content in the [Root folder]:</span></span>

![priconfig в папке](./../../media/priconfig.png)


```xml
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<resources targetOsVersion="10.0.0" majorVersion="1">
    <index root="\" startIndexAt="\">
        <default>
            <qualifier name="Language" value="en-US"/>
            <qualifier name="Contrast" value="standard"/>
            <qualifier name="HomeRegion" value="001"/>
            <qualifier name="TargetSize" value="256"/>
            <qualifier name="LayoutDirection" value="LTR"/>
            <qualifier name="Theme" value="dark"/>
            <qualifier name="AlternateForm" value=""/>
            <qualifier name="DXFeatureLevel" value="DX9"/>
            <qualifier name="Configuration" value=""/>
            <qualifier name="DeviceFamily" value="Universal"/>
            <qualifier name="Custom" value=""/>
        </default>
        <indexer-config type="folder" foldernameAsQualifier="true" filenameAsQualifier="true" qualifierDelimiter="."/>
        <indexer-config type="resw" convertDotsToSlashes="true" initialPath=""/>
        <indexer-config type="resjson" initialPath=""/>
        <indexer-config type="PRI"/>
    </index>
</resources>
```

<span data-ttu-id="378e8-175">Теперь вы можете создать файл Resources. PRI с помощью файла конфигурации и средства MakePRI.</span><span class="sxs-lookup"><span data-stu-id="378e8-175">Now you can use the configuration file and the MakePRI tool to create the resources.pri file.</span></span> <span data-ttu-id="378e8-176">Для этого примера корневой каталог для проекта будет [корневой каталог].</span><span class="sxs-lookup"><span data-stu-id="378e8-176">For this example, the root location for the project will be [Root folder].</span></span>


```cmd
MakePRI new /pr [Root folder] /cf [Root folder]\priconfig.xml /mn [Root folder]\AppxManifest.xml /of [Root folder]\resources.pri /o
```

<span data-ttu-id="378e8-177">Теперь у вас есть один файл Resources. PRI в корневой папке.</span><span class="sxs-lookup"><span data-stu-id="378e8-177">You should now have one resources.pri file in your root folder:</span></span>

![Папка "ресурсы"](./../../media/resources.png)


## <span data-ttu-id="378e8-179">Локализация имени и описания в Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="378e8-179">Localizing name and description in the Microsoft Store</span></span>

<span data-ttu-id="378e8-180">После попытки загрузить полный локализованный пакет центр разработки для Windows обнаружит, что поддерживается несколько языков, и проверьте, есть ли у вас соответствующие локализованные имена и описания для каждого из них.</span><span class="sxs-lookup"><span data-stu-id="378e8-180">Once you try to upload your complete, localized package, the Windows Dev Center will detect that more than one language is supported and check that you have corresponding localized names and descriptions for each.</span></span> <span data-ttu-id="378e8-181">Если хотя бы одно из локализованных значений отсутствует, отправка будет заблокирована до тех пор, пока вы не выдасте нужные значения.</span><span class="sxs-lookup"><span data-stu-id="378e8-181">If any of the localized values are missing, your submission will be blocked until you provide the values.</span></span>

<span data-ttu-id="378e8-182">Если вы хотите предоставить только локализованные имя и описание для Microsoft Store (но не Windows), вы можете сделать это, заполнив [все локализованные имена для вашего расширения](./extensions-in-the-windows-dev-center.md#name-reservation).</span><span class="sxs-lookup"><span data-stu-id="378e8-182">If you are only interested in providing a localized name and description for the Microsoft Store (and not Windows), you can do so by [reserving all the localized names for your extension](./extensions-in-the-windows-dev-center.md#name-reservation).</span></span>


<span data-ttu-id="378e8-183">После того как вы заменили дополнительные локализованные имена, вы можете создать обновленную отправку.</span><span class="sxs-lookup"><span data-stu-id="378e8-183">Once you've reserved additional localized names, you can create an updated submission.</span></span> <span data-ttu-id="378e8-184">В разделе Описание вы можете управлять дополнительными языками для вашего описания в магазине Microsoft Store:</span><span class="sxs-lookup"><span data-stu-id="378e8-184">In the description section you can manage additional languages for your Microsoft Store listing:</span></span>

![Описание приложения на японском языке](./../../media/manage-description-languages.png)

<span data-ttu-id="378e8-186">После того как вы выбрали "Управление дополнительными языками", вам будет предложено выбрать языки, которые нужно добавить в описание Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="378e8-186">Once you've selected "Manage additional languages", you'll get to select which languages you want to add to your Microsoft Store listing.</span></span> <span data-ttu-id="378e8-187">Новый язык будет отображаться как "дополнительный язык описания" в разделе "Описание".</span><span class="sxs-lookup"><span data-stu-id="378e8-187">The new language will show up as 'Additional description language' in the "Description" section.</span></span>

<span data-ttu-id="378e8-188">Вы можете щелкнуть отдельную ссылку в разделе "Описание", чтобы предоставить локализованное название и описание, заметки о выпуске и визуальные ресурсы для каждого языка.</span><span class="sxs-lookup"><span data-stu-id="378e8-188">You can click on the individual link in the "Description" section to provide a localized name and description, release notes, and visual assets for each language.</span></span> <span data-ttu-id="378e8-189">Описание для магазина Microsoft Store не извлекается из AppXManifest.</span><span class="sxs-lookup"><span data-stu-id="378e8-189">The description for the Microsoft Store is not extracted from the AppXManifest.</span></span> <span data-ttu-id="378e8-190">Каждое локализованное описание должно быть введено вручную в центре разработки для Windows:</span><span class="sxs-lookup"><span data-stu-id="378e8-190">Each localized description needs to be manually entered in the Windows Dev Center:</span></span>

![Описание приложения на японском языке](./../../media/japanese-app-description.png)

<span data-ttu-id="378e8-192">После отправки локализованных описаний и публикации расширения любой пользователь, имеющий доступ к локализованной странице расширения в Microsoft Store, будет видеть следующий пользовательский интерфейс:</span><span class="sxs-lookup"><span data-stu-id="378e8-192">Once the localized descriptions are submitted and the extension is published, anyone accessing a localized page of the extension in the Microsoft Store will see the following UI:</span></span>

![Магазин Windows на японском языке](./../../media/japanese-windows-store.png)
 

## <span data-ttu-id="378e8-194">Примеры AppxManifest</span><span class="sxs-lookup"><span data-stu-id="378e8-194">AppxManifest samples</span></span>

### <span data-ttu-id="378e8-195">Нелокализованные AppxManifest</span><span class="sxs-lookup"><span data-stu-id="378e8-195">Non-localized AppxManifest</span></span>
<span data-ttu-id="378e8-196">В следующем примере показан AppxManifest, который не является локализованным, и поддерживает только национальную настройку "en-US".</span><span class="sxs-lookup"><span data-stu-id="378e8-196">The following example shows an AppxManifest that isn't localized, and only supports the "en-us" locale.</span></span>


```xml
<?xml version="1.0" encoding="utf-8"?>
<Package
    xmlns="http://schemas.microsoft.com/appx/manifest/foundation/windows10"
    xmlns:uap="http://schemas.microsoft.com/appx/manifest/uap/windows10"
    xmlns:uap3="http://schemas.microsoft.com/appx/manifest/uap/windows10/3"
    IgnorableNamespaces="uap3">
    <Identity
        Name="63533cct23.Jigsaw"
        Publisher="CN=932A7C4A-0308-4632-9E2F-5931E8F02B7C"
        Version="1.3.0.0" />

    <Properties>
        <DisplayName>Jigsaw</DisplayName>
        <PublisherDisplayName>cct23</PublisherDisplayName>
        <Logo>Assets\icon-50.png</Logo>
    </Properties>

    <Dependencies>
        <TargetDeviceFamily Name="Windows.Desktop" MinVersion="10.0.14393.0" MaxVersionTested="10.0.14800.0" />
    </Dependencies>

    <Resources>
        <Resource Language="en-us" />
    </Resources>

    <Applications>
        <Application Id="App">
            <uap:VisualElements
                AppListEntry="none"
                DisplayName="Jigsaw"
                Square150x150Logo="Assets\icon-150.png"
                Square44x44Logo="Assets\icon-44.png"
                Description="This is a jigsaw puzzle app"
                BackgroundColor="transparent">
            </uap:VisualElements>
            <Extensions>
                <uap3:Extension Category="windows.appExtension">
                    <uap3:AppExtension
                        Name="com.microsoft.edge.extension"
                        Id="EdgeExtension"
                        PublicFolder="Extension"
                        DisplayName="Jigsaw">
                        <uap3:Properties>
                            <Capabilities>
                                <Capability Name="websiteContent"/>
                                <Capability Name="websiteInfo"/>
                                <Capability Name="browserStorage"/>
                            </Capabilities>
                        </uap3:Properties>
                    </uap3:AppExtension>
                </uap3:Extension>
            </Extensions>
        </Application>
    </Applications>
</Package>
```


#### <span data-ttu-id="378e8-197">Локализованные AppxManifest</span><span class="sxs-lookup"><span data-stu-id="378e8-197">Localized AppxManifest</span></span>
<span data-ttu-id="378e8-198">Этот образец AppxManifest локализуется для восьми других языков, кроме en-US.</span><span class="sxs-lookup"><span data-stu-id="378e8-198">This AppxManifest sample is localized for eight other locales besides "en-us".</span></span> <span data-ttu-id="378e8-199">Обратите внимание на `ms-resource:<resource id>` повторения.</span><span class="sxs-lookup"><span data-stu-id="378e8-199">Notice the `ms-resource:<resource id>` occurrences:</span></span>


```xml
<?xml version="1.0" encoding="utf-8"?>
<Package
    xmlns="http://schemas.microsoft.com/appx/manifest/foundation/windows10"
    xmlns:uap="http://schemas.microsoft.com/appx/manifest/uap/windows10"
    xmlns:uap3="http://schemas.microsoft.com/appx/manifest/uap/windows10/3"
    IgnorableNamespaces="uap3">
    <Identity
        Name="63533cct23.Jigsaw"
        Publisher="CN=932A7C4A-0308-4632-9E2F-5931E8F02B7C"
        Version="1.3.0.0" />

    <Properties>
        <DisplayName>ms-resource:DisplayName</DisplayName>
        <PublisherDisplayName>cct23</PublisherDisplayName>
        <Logo>Assets\icon-50.png</Logo>
    </Properties>

    <Dependencies>
        <TargetDeviceFamily Name="Windows.Desktop" MinVersion="10.0.14393.0" MaxVersionTested="10.0.14800.0" />
    </Dependencies>

    <Resources>
        <Resource Language="en-us" />
        <Resource Language="de" />
        <Resource Language="en" />
        <Resource Language="en-gb" />
        <Resource Language="es" />
        <Resource Language="fr" />
        <Resource Language="it" />
        <Resource Language="ja" />
        <Resource Language="zh-cn" />
    </Resources>

    <Applications>
        <Application Id="App">
            <uap:VisualElements
                AppListEntry="none"
                DisplayName="ms-resource:DisplayName"
                Square150x150Logo="Assets\icon-150.png"
                Square44x44Logo="Assets\icon-44.png"
                Description="ms-resource:Description"
                BackgroundColor="transparent">
            </uap:VisualElements>
            <Extensions>
                <uap3:Extension Category="windows.appExtension">
                    <uap3:AppExtension
                        Name="com.microsoft.edge.extension"
                        Id="EdgeExtension"
                        PublicFolder="Extension"
                        DisplayName="ms-resource:DisplayName">
                        <uap3:Properties>
                            <Capabilities>
                                <Capability Name="websiteContent"/>
                                <Capability Name="websiteInfo"/>
                                <Capability Name="browserStorage"/>
                            </Capabilities>
                        </uap3:Properties>
                    </uap3:AppExtension>
                </uap3:Extension>
            </Extensions>
        </Application>
    </Applications>
</Package>
```
