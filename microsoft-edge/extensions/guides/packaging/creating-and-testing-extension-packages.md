---
ms.assetid: 5eefa3d8-8626-4486-bd90-1361400d6468
description: Узнайте о том, как упаковать расширение Microsoft Edge вручную и протестировать его, чтобы проверить, правильно ли он упакован.
title: Создание и тестирование пакетов расширений
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: EDGE, веб-разработка, HTML, CSS, JavaScript, разработчик, упаковка
ms.custom: seodec18
ms.openlocfilehash: a76737d76c8f08c8e79992f0804fdbd34d4ed970
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571517"
---
# <span data-ttu-id="532f4-104">Создание и тестирование пакета AppX для расширения Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="532f4-104">Creating and testing a Microsoft Edge extension AppX package</span></span>  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

<span data-ttu-id="532f4-105">Расширения Microsoft Edge упаковываются в AppX и похожи на упаковку универсальных приложений для Windows.</span><span class="sxs-lookup"><span data-stu-id="532f4-105">Microsoft Edge extensions are packaged as AppX, similar to how Universal Windows Apps are packaged.</span></span> <span data-ttu-id="532f4-106">Начиная с обновления годовщины Windows 10, в AppX была добавлена новая схема, которая позволяет AppX включать в качестве содержимого расширение Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="532f4-106">As of Windows 10 Anniversary Update, a new schema has been introduced for AppX that allows an AppX to include a Microsoft Edge extension as its content.</span></span>

<span data-ttu-id="532f4-107">Если вы уже знаете, как создаются расширения Microsoft Edge AppX, вы можете перейти к [использованию ManifoldJS для расширения пакета](./using-manifoldjs-to-package-extensions.md) , чтобы узнать, как использовать средство на основе Node. js для выполнения всех этих действий.</span><span class="sxs-lookup"><span data-stu-id="532f4-107">If you already know how Microsoft Edge extension AppXs are created, you can skip to [Using ManifoldJS to package extension](./using-manifoldjs-to-package-extensions.md) to learn how to use a Node.js based tool to do all of this for you!</span></span>

> [!NOTE]
> <span data-ttu-id="532f4-108">Отправка расширения Microsoft EDGE в Microsoft Store в настоящее время ограничена возможностями.</span><span class="sxs-lookup"><span data-stu-id="532f4-108">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span> <span data-ttu-id="532f4-109">Создав, упакуйте и протестировали расширение, отправьте запрос на [форму отправки расширения](https://aka.ms/extension-request).</span><span class="sxs-lookup"><span data-stu-id="532f4-109">Once you've created, packaged and tested your extension, please submit a request on our [extension submission form](https://aka.ms/extension-request).</span></span>



## <span data-ttu-id="532f4-110">Подготовка папки отправки</span><span class="sxs-lookup"><span data-stu-id="532f4-110">Preparing the submission folder</span></span>

<span data-ttu-id="532f4-111">Чтобы подготовить расширение к отправке, необходимо создать папку со следующей структурой:</span><span class="sxs-lookup"><span data-stu-id="532f4-111">To prepare your extension for submission, you need to create a folder with the following structure:</span></span>

![изображение структуры папок.](./../../media/packaging_folder-structure.png)

<span data-ttu-id="532f4-114">В корневой папке нужно добавить файл AppXManifest. XML.</span><span class="sxs-lookup"><span data-stu-id="532f4-114">At the root of the folder, you should include an AppXManifest.xml file.</span></span> <span data-ttu-id="532f4-115">Этот файл используется для указания содержимого и макета пакета.</span><span class="sxs-lookup"><span data-stu-id="532f4-115">This file is used to specify the contents and layout of the package.</span></span>

<span data-ttu-id="532f4-116">Кроме того, у вас должна быть папка Assets, содержащая ресурсы пользовательского интерфейса, которые будут использоваться в Microsoft Store, и папка расширения, содержащая файлы расширения (сценарии, значки и т. д.).</span><span class="sxs-lookup"><span data-stu-id="532f4-116">You should also have an Assets folder which contains the UI assets to be used in the Microsoft Store, and an Extension folder that contains your extension's files (scripts, icons, etc).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="532f4-117">Вы можете создать другую структуру папок для пакета, но структура папок должна совпадать со значениями AppXManifest.</span><span class="sxs-lookup"><span data-stu-id="532f4-117">You can create a different folder structure for your package, but the folder structure must match the AppXManifest values.</span></span>

### <span data-ttu-id="532f4-118">AppXManifest. XML</span><span class="sxs-lookup"><span data-stu-id="532f4-118">AppXManifest.xml</span></span>
<span data-ttu-id="532f4-119">Файл AppXManifest — это документ XML, содержащий сведения, необходимые системе для развертывания, отображения и обновления приложения для Windows.</span><span class="sxs-lookup"><span data-stu-id="532f4-119">The AppXManifest file is an XML document that contains info the system needs to deploy, display, or update a Windows app.</span></span> <span data-ttu-id="532f4-120">Этот файл содержит также удостоверение пакета, возможности и визуальные элементы.</span><span class="sxs-lookup"><span data-stu-id="532f4-120">This file also includes package identity, capabilities, and visual elements.</span></span> <span data-ttu-id="532f4-121">Каждый пакет приложения должен включать один файл AppXManifest.</span><span class="sxs-lookup"><span data-stu-id="532f4-121">Every app package must include one AppXManifest file.</span></span>

<span data-ttu-id="532f4-122">Разработчики могут использовать следующий шаблон для файла AppXManifest. XML:</span><span class="sxs-lookup"><span data-stu-id="532f4-122">Developers can use the following template for their AppXManifest.xml file:</span></span>

```xml
<?xml version="1.0" encoding="utf-8"?>
<Package
  xmlns="http://schemas.microsoft.com/appx/manifest/foundation/windows10"
  xmlns:uap="http://schemas.microsoft.com/appx/manifest/uap/windows10"
  xmlns:uap3="http://schemas.microsoft.com/appx/manifest/uap/windows10/3"
  IgnorableNamespaces="uap3">

  <Identity
    Name="[REPLACE WITH PACKAGE/IDENTITYNAME]"
    Publisher="[REPLACE WITH PACKAGE/IDENTITY/PUBLISHER]"
    Version="[REPLACE WITH PACKAGE VERSION in the form X.X.X.0]"/>

  <Properties>
    <DisplayName>[REPLACE WITH RESERVED STORE NAME]</DisplayName>
    <PublisherDisplayName>[REPLACE WITH PACKAGE/PROPERTIES/PUBLISHERDISPLAYNAME]</PublisherDisplayName>
    <Logo>[REPLACE WITH RELATIVE PATH TO 50x50 ICON]</Logo>
  </Properties>

  <Dependencies>
    <TargetDeviceFamily Name="Windows.Desktop"
      MinVersion="10.0.14393.0"
      MaxVersionTested="10.0.14800.0" />
  </Dependencies>

  <Resources>
    <Resource Language="en-us"/>
  </Resources>

  <Applications>
    <Application Id="App">
      <uap:VisualElements
        AppListEntry="none"
        DisplayName="[REPLACE WITH RESERVED STORE NAME]"
        Square150x150Logo="[REPLACE WITH RELATIVE PATH TO 150x150 ICON]"
        Square44x44Logo="[REPLACE WITH RELATIVE PATH TO 44x44 ICON]"
        Description="This is the description of the extension"
        BackgroundColor="white">
      </uap:VisualElements>
    <Extensions>
    <uap3:Extension Category="windows.appExtension">
    <uap3:AppExtension Name="com.microsoft.edge.extension"
        Id="EdgeExtension"
        PublicFolder="Extension"
      DisplayName="[REPLACE WITH RESERVED STORE NAME]">
    </uap3:AppExtension>
    </uap3:Extension>
    </Extensions>
 </Application>
</Applications>
</Package>
```

#### <span data-ttu-id="532f4-123">Значения шаблона удостоверения приложения</span><span class="sxs-lookup"><span data-stu-id="532f4-123">App identity template values</span></span>
<span data-ttu-id="532f4-124">После того как вы заменили [имя расширения](./extensions-in-the-windows-dev-center.md#name-reservation) с помощью центра разработки для Windows, вы сможете найти необходимые сведения об удостоверении пакета, необходимые для замены указанных ниже значений в AppXManifest. XML.</span><span class="sxs-lookup"><span data-stu-id="532f4-124">Once you've [reserved the name of your extension](./extensions-in-the-windows-dev-center.md#name-reservation) through the Windows Dev Center, you'll be able to find the necessary package identity information needed to replace the following values in AppXManifest.xml:</span></span>

- `Name`
- `Publisher`
- `DisplayName`
- `PublisherDisplayName`

<span data-ttu-id="532f4-125">Вы можете получить доступ к странице удостоверения приложения, выполнив указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="532f4-125">You can access your App identity page using the following steps:</span></span>

1. <span data-ttu-id="532f4-126">Перейдите в [центр разработки для Windows](https://developer.microsoft.com/windows/).</span><span class="sxs-lookup"><span data-stu-id="532f4-126">Navigate to [Windows Dev Center](https://developer.microsoft.com/windows/).</span></span>
2. <span data-ttu-id="532f4-127">Войдите в свою учетную запись разработчика.</span><span class="sxs-lookup"><span data-stu-id="532f4-127">Sign in to your developer account.</span></span>
3. <span data-ttu-id="532f4-128">Перейдите на панель мониторинга.</span><span class="sxs-lookup"><span data-stu-id="532f4-128">Navigate to the Dashboard.</span></span>
4. <span data-ttu-id="532f4-129">Выберите имя расширения.</span><span class="sxs-lookup"><span data-stu-id="532f4-129">Select the name of your extension.</span></span>

   ![список расширений](./../../media/select-app.png)
5. <span data-ttu-id="532f4-131">Перейдите на страницу удостоверения приложения, которая находится в разделе Управление приложениями (после регистрации приложения).</span><span class="sxs-lookup"><span data-stu-id="532f4-131">Navigate to the App identity page which is under the App management section (after you've registered your app).</span></span>

   ![Страница идентификации приложения](./../../media/app-identity.png)


<span data-ttu-id="532f4-133">Теперь вы можете заполнить шаблон AppXManifest значениями из страницы удостоверение приложения, как показано в шаблоне:</span><span class="sxs-lookup"><span data-stu-id="532f4-133">You can now populate the AppXManifest template with values from the App identity page, as indicated in the template:</span></span>


```xml
<Identity
  Name="37369abigailc.MyExtension"
  Publisher="CN=732F2E5E-B9A6-4243-85F6-A4210F57AA10"
  Version="[REPLACE WITH PACKAGE VERSION in the form X.X.X.0]" />

<Properties>
  <DisplayName>My Extension</DisplayName>
  <PublisherDisplayName>abigailc</PublisherDisplayName>
  <Logo>[REPLACE WITH RELATIVE PATH TO 50x50 ICON]</Logo>
</Properties>
```

#### <span data-ttu-id="532f4-134">Значения шаблона манифеста JSON</span><span class="sxs-lookup"><span data-stu-id="532f4-134">JSON manifest template values</span></span>
<span data-ttu-id="532f4-135">Некоторые значения в AppXManifest должны соответствовать параметрам, определенным в манифесте JSON.</span><span class="sxs-lookup"><span data-stu-id="532f4-135">Some values in the AppXManifest need to match those that are defined in the JSON manifest.</span></span> <span data-ttu-id="532f4-136">Обновите следующие значения в appxmanifest. XML на основе манифеста JSON расширения:</span><span class="sxs-lookup"><span data-stu-id="532f4-136">Please update the following values in appxmanifest.xml based on your extension JSON manifest:</span></span>

- `Version` <span data-ttu-id="532f4-137">— Версия, указанная в манифесте JSON расширения.</span><span class="sxs-lookup"><span data-stu-id="532f4-137">- This is the version listed in your extension's JSON manifest.</span></span> <span data-ttu-id="532f4-138">Строка должна соответствовать формату X. X. X. X, где Последнее целое число должно быть равным 0.</span><span class="sxs-lookup"><span data-stu-id="532f4-138">The string needs to match the X.X.X.X format where the last integer has to be 0.</span></span> <span data-ttu-id="532f4-139">Например:</span><span class="sxs-lookup"><span data-stu-id="532f4-139">E.g.</span></span> <span data-ttu-id="532f4-140">1.2.3.0</span><span class="sxs-lookup"><span data-stu-id="532f4-140">1.2.3.0</span></span>

   ```xml
   <Identity
     Name="37369abigailc.MyExtension"
     Publisher="CN=732F2E5E-B9A6-4243-85F6-A4210F57AA10"
     Version="1.0.0.0" />
   ```

- `Description` <span data-ttu-id="532f4-141">-Это копия описания в манифесте JSON расширения.</span><span class="sxs-lookup"><span data-stu-id="532f4-141">- This is a copy of the description in your extension's JSON manifest.</span></span>

  ```xml
  <uap:VisualElements
    AppListEntry="none"
    DisplayName="My Extension"
    Square150x150Logo="[REPLACE WITH RELATIVE PATH TO 150x150 ICON]"
    Square44x44Logo="[REPLACE WITH RELATIVE PATH TO 44x44 ICON]"
    Description="This extension will allow you to quickly print by clicking the browser action."
    BackgroundColor="white">
  </uap:VisualElements>
  ```


### <span data-ttu-id="532f4-142">Папка "ресурсы"</span><span class="sxs-lookup"><span data-stu-id="532f4-142">Assets folder</span></span>

<span data-ttu-id="532f4-143">В папке Assets вам понадобятся три разных размера значков.</span><span class="sxs-lookup"><span data-stu-id="532f4-143">Within the Assets folder you will need three different icon sizes.</span></span> <span data-ttu-id="532f4-144">Эти значки будут использоваться в Microsoft Store и пользовательском интерфейсе Windows.</span><span class="sxs-lookup"><span data-stu-id="532f4-144">These icons will be used in the Microsoft Store and the Windows UI.</span></span> <span data-ttu-id="532f4-145">Дополнительные сведения об этих значках можно найти в руководстве по [проектированию](./../design.md#icons-for-packaging) .</span><span class="sxs-lookup"><span data-stu-id="532f4-145">For more information on these icons, see the [Design](./../design.md#icons-for-packaging) guide.</span></span>

![Папка «ресурсы» с тремя размерами значков](./../../media/assets-folder.png)

<span data-ttu-id="532f4-147">После создания необходимых ресурсов пользовательского интерфейса обновите AppXManifest. XML, чтобы он указывал на нужные файлы.</span><span class="sxs-lookup"><span data-stu-id="532f4-147">Once you've created the necessary UI assets, update AppXManifest.xml to point to the correct files:</span></span>

- <span data-ttu-id="532f4-148">44 x 44</span><span class="sxs-lookup"><span data-stu-id="532f4-148">44x44</span></span>

   ```xml
   Square44x44Logo="Assets/icon_44.png"
   ```

- <span data-ttu-id="532f4-149">50x50</span><span class="sxs-lookup"><span data-stu-id="532f4-149">50x50</span></span>

  ```xml
   <Logo>Assets/icon_50.png</Logo>
  ```

- <span data-ttu-id="532f4-150">150 x 150</span><span class="sxs-lookup"><span data-stu-id="532f4-150">150x150</span></span>

  ```xml
  Square150x150Logo="Assets/icon_150.png"
  ```


### <span data-ttu-id="532f4-151">Папка "расширение"</span><span class="sxs-lookup"><span data-stu-id="532f4-151">Extension folder</span></span>
<span data-ttu-id="532f4-152">Скопируйте файлы расширений (сохранив структуру папок) в папку "расширение".</span><span class="sxs-lookup"><span data-stu-id="532f4-152">Copy your extension files (keeping the folder structure) into the Extension folder.</span></span> <span data-ttu-id="532f4-153">Убедитесь в `manifest.json` том, что папка расширения находится в корне.</span><span class="sxs-lookup"><span data-stu-id="532f4-153">Make sure `manifest.json` is at the root your Extension folder.</span></span>

![папка расширения со всеми файлами расширений](./../../media/extension-folder.png)


### <span data-ttu-id="532f4-155">Поддержка более чем одной национальной настройки</span><span class="sxs-lookup"><span data-stu-id="532f4-155">Supporting more than one locale</span></span>
<span data-ttu-id="532f4-156">Если ваше расширение поддерживает более одного языка, вы можете настроить пакет AppX так, чтобы в нем отображался правильный локализованный значок и описание.</span><span class="sxs-lookup"><span data-stu-id="532f4-156">If your extension supports more than one language, you may want to configure the AppX package with all the locales that you need so that the correct localized icon and description appear in the Microsoft Store.</span></span> <span data-ttu-id="532f4-157">Дополнительные сведения см. в разделе [Локализация пакетов расширений](./localizing-extension-packages.md) .</span><span class="sxs-lookup"><span data-stu-id="532f4-157">See [Localizing extension packages](./localizing-extension-packages.md) for more information.</span></span>

### <span data-ttu-id="532f4-158">Создание Appx</span><span class="sxs-lookup"><span data-stu-id="532f4-158">Creating an Appx</span></span>

<span data-ttu-id="532f4-159">Чтобы создать appx, вам нужно найти путь для makeappx.</span><span class="sxs-lookup"><span data-stu-id="532f4-159">To create an Appx, you'll need to find the path for makeappx.</span></span> <span data-ttu-id="532f4-160">Обычно это расположение находится в следующем расположении, если вы используете 64-разрядный компьютер.</span><span class="sxs-lookup"><span data-stu-id="532f4-160">This is usually located in the following location if you're on a 64-bit machine.</span></span>

`C:\Program Files (x86)\Windows Kits\10\bin\x64`

<span data-ttu-id="532f4-161">Выполните следующую команду, чтобы создать пакет AppX для вашего расширения.</span><span class="sxs-lookup"><span data-stu-id="532f4-161">Execute the following command to create the AppX package for your extension:</span></span>

`[Path to makeappx] makeappx pack /h SHA256 /d [Path to package folder created in #1] /p [Path to the appx file that you want to create]`

<span data-ttu-id="532f4-162">Это должно выглядеть примерно так, как если бы вы заполнили пути.</span><span class="sxs-lookup"><span data-stu-id="532f4-162">This should look something like this once you've filled in the paths:</span></span>

`C:\Program Files (x86)\Windows Kits\10\bin\x64>makeappx.exe pack /h SHA256 /d "C:\Extension\My Extension" /p C:\Extension\MyExtension.appx`

### <span data-ttu-id="532f4-163">Распаковка Appx</span><span class="sxs-lookup"><span data-stu-id="532f4-163">Unpacking an Appx</span></span>
<span data-ttu-id="532f4-164">Возможно, потребуется распаковать ранее созданный AppX и использовать его в качестве отправной точки для следующей итерации расширения или подтвердить правильность создания AppX.</span><span class="sxs-lookup"><span data-stu-id="532f4-164">You may want to unpack a previously generated AppX and use it as a starting point for the next iteration of your extension or to confirm that the AppX was created correctly.</span></span>

<span data-ttu-id="532f4-165">Для этого вы можете выполнить следующую команду, чтобы распаковать пакет AppX расширения Microsoft Edge:</span><span class="sxs-lookup"><span data-stu-id="532f4-165">To do this, you can execute the following command to unpack the AppX package of your Microsoft Edge extension:</span></span>

`[Path to makeappx] makeappx unpack /v /p [Path to appx file you want to unpack] /d [Path to the location where you want to create the package folder]`

<span data-ttu-id="532f4-166">Это должно выглядеть примерно так, как вы залиты:</span><span class="sxs-lookup"><span data-stu-id="532f4-166">This should look something like this when filled out:</span></span>

`C:\Program Files (x86)\Windows Kits\10\bin\x64>makeappx.exe unpack /v /p "C:\Extension\MyExtension.appx" /d "C:\Extension\My Extension"`





## <span data-ttu-id="532f4-167">Тестирование пакета AppX</span><span class="sxs-lookup"><span data-stu-id="532f4-167">Testing an AppX package</span></span>

<span data-ttu-id="532f4-168">Вы можете протестировать пакет AppX Microsoft Edge с помощью неопубликованных приложений в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="532f4-168">You can test your Microsoft Edge extension AppX package by sideloading it in Microsoft Edge.</span></span> <span data-ttu-id="532f4-169">Неопубликованное приложение-пакет расширений AppX подобен неопубликованному в Skype стандартному приложению для Windows.</span><span class="sxs-lookup"><span data-stu-id="532f4-169">Sideloading the extension AppX package is similar to sideloading a Universal Windows app.</span></span> <span data-ttu-id="532f4-170">Для подписывания пакета вам потребуется создать сертификат, а затем добавить его в Windows.</span><span class="sxs-lookup"><span data-stu-id="532f4-170">You will need to create a certificate for signing the package, and then add the package to Windows.</span></span>

### <span data-ttu-id="532f4-171">Выполняется</span><span class="sxs-lookup"><span data-stu-id="532f4-171">Signing</span></span>

<span data-ttu-id="532f4-172">Узнайте, [как создать сертификат подписи пакета приложения](https://msdn.microsoft.com/library/windows/desktop/jj835832.aspx) и [как подписать пакет приложения с помощью SignTool](https://msdn.microsoft.com/library/windows/desktop/jj835835.aspx) для получения сведений о процессе подписи и сертификации для пакетов.</span><span class="sxs-lookup"><span data-stu-id="532f4-172">See [How to create an app package signing certificate](https://msdn.microsoft.com/library/windows/desktop/jj835832.aspx) and [How to sign an app package using SignTool](https://msdn.microsoft.com/library/windows/desktop/jj835835.aspx) for info on the signing and certification process for packages.</span></span>

> [!NOTE]
> <span data-ttu-id="532f4-173">Перед отправкой пакета расширения в Microsoft Store вам не нужно подписывать его. процесс приема магазина поможет вам!</span><span class="sxs-lookup"><span data-stu-id="532f4-173">You do not need to sign an extension package before submitting it to the Microsoft Store; the Store ingestion process will take care of that for you!</span></span>

<span data-ttu-id="532f4-174">После того как вы подписали пакет с помощью созданного вами сертификата, сертификат по-прежнему не будет доверять локальному компьютеру для развертывания пакетов приложений, пока вы не установите его в хранилище доверенных сертификатов на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="532f4-174">After you've signed the package with the certificate that you created, the certificate is still not trusted by the local machine for deployment of app packages until you install it into the trusted certificates store of the local computer.</span></span> <span data-ttu-id="532f4-175">Для этого можно использовать программу Certutil. exe, которая поставляется вместе с Windows.</span><span class="sxs-lookup"><span data-stu-id="532f4-175">You can use Certutil.exe, which comes with Windows to do this.</span></span>

<span data-ttu-id="532f4-176">Чтобы установить сертификаты с помощью WindowsCertutil. exe, запустите cmd. exe как администратор и выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="532f4-176">To install certificates with WindowsCertutil.exe, run Cmd.exe as administrator and run the following command:</span></span>

`Certutil -addStore TrustedPeople MyKey.cer`

<span data-ttu-id="532f4-177">После того как сертификаты больше не используются, рекомендуется удалить их, выполнив следующую команду в командной строке администратора:</span><span class="sxs-lookup"><span data-stu-id="532f4-177">Once the certificates are no longer in use, it is recommended that you remove them by running the following command from an administrator command prompt:</span></span>

`Certutil -delStore TrustedPeople certID`

<span data-ttu-id="532f4-178">CertID — это серийный номер сертификата.</span><span class="sxs-lookup"><span data-stu-id="532f4-178">The certID is the serial number of the certificate.</span></span> <span data-ttu-id="532f4-179">Чтобы определить серийный номер сертификата, выполните следующую команду:</span><span class="sxs-lookup"><span data-stu-id="532f4-179">To determine the certificate serial number, run the following command:</span></span>

`Certutil -store TrustedPeople`

### <span data-ttu-id="532f4-180">Развертывание</span><span class="sxs-lookup"><span data-stu-id="532f4-180">Deploying</span></span>
<span data-ttu-id="532f4-181">Пакет AppX для расширения Microsoft EDGE можно развернуть, выполнив следующую команду в PowerShell (от имени администратора).</span><span class="sxs-lookup"><span data-stu-id="532f4-181">You can deploy the Microsoft Edge Extension AppX package by running the following command in PowerShell (as administrator):</span></span>

`Add-AppxPackage [path to AppX]`

## <span data-ttu-id="532f4-182">Автоматическое тестирование с помощью фотодисковода</span><span class="sxs-lookup"><span data-stu-id="532f4-182">Automated testing with WebDriver</span></span>

<span data-ttu-id="532f4-183">По мере изменения юбилея вы можете программно неопубликованного свое расширение в Microsoft Edge с помощью веб – дисковода, обеспечивая автоматическое тестирование расширений при запуске Microsoft EDGE в режиме веб – дисковода.</span><span class="sxs-lookup"><span data-stu-id="532f4-183">As of the Anniversary Update, you can programmatically sideload your extension in Microsoft Edge with WebDriver, enabling automated testing of extensions when Microsoft Edge is launched in WebDriver mode.</span></span> <span data-ttu-id="532f4-184">Это позволит вам настроить автоматические тесты для любого расширения, которое управляет контентом на странице, и проверяет правильность поведения.</span><span class="sxs-lookup"><span data-stu-id="532f4-184">This will allow you to set up automated tests for any extension that manipulates content on a page and verify that the correct behavior is exhibited.</span></span>

<span data-ttu-id="532f4-185">Чтобы неопубликованного расширение для автоматического тестирования, необходимо сохранить папку расширения в разделе `%LOCALAPPDATA%\Packages\Microsoft.MicrosoftEdge_8wekyb3d8bbwe\LocalState\` .</span><span class="sxs-lookup"><span data-stu-id="532f4-185">To sideload your extension for automated testing, you'll need to store your extension's folder under `%LOCALAPPDATA%\Packages\Microsoft.MicrosoftEdge_8wekyb3d8bbwe\LocalState\`.</span></span> <span data-ttu-id="532f4-186">После добавления расширения в `LocalState` Каталог вам потребуется создать [`EdgeOptions`](https://seleniumhq.github.io/selenium/docs/api/dotnet/html/T_OpenQA_Selenium_Edge_EdgeOptions.htm) объект и добавить в `extensionPaths` него возможность.</span><span class="sxs-lookup"><span data-stu-id="532f4-186">Once your extension is in the `LocalState` directory, you'll need to create an [`EdgeOptions`](https://seleniumhq.github.io/selenium/docs/api/dotnet/html/T_OpenQA_Selenium_Edge_EdgeOptions.htm) object, and add the `extensionPaths` capability to it.</span></span> <span data-ttu-id="532f4-187">Значение этой возможности — это массив абсолютных путей к расширениям (в `LocalState` каталоге), которые должны быть загружены на стороне, когда Microsoft Edge запускается в режиме веб-накопителя.</span><span class="sxs-lookup"><span data-stu-id="532f4-187">The value of this capability is an array of absolute paths to the extensions (in the `LocalState` directory) you wish to have side loaded when Microsoft Edge starts in WebDriver mode.</span></span>

<span data-ttu-id="532f4-188">Полный пример расширений загрузки сбоку в Microsoft Edge с помощью веб-накопителя вы также ознакомьтесь с приведенными ниже [файлами на C#](https://github.com/scottlow/Ignite2016/blob/master/Ignite%202016%20WebDriver%20Demo/IgniteWebDriverDemo/Program.cs) .</span><span class="sxs-lookup"><span data-stu-id="532f4-188">Check out the following [C# file](https://github.com/scottlow/Ignite2016/blob/master/Ignite%202016%20WebDriver%20Demo/IgniteWebDriverDemo/Program.cs) for a complete sample on side loading extensions in Microsoft Edge with WebDriver.</span></span>
