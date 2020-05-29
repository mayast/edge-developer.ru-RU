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
# Создание и тестирование пакета AppX для расширения Microsoft Edge  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

Расширения Microsoft Edge упаковываются в AppX и похожи на упаковку универсальных приложений для Windows. Начиная с обновления годовщины Windows 10, в AppX была добавлена новая схема, которая позволяет AppX включать в качестве содержимого расширение Microsoft Edge.

Если вы уже знаете, как создаются расширения Microsoft Edge AppX, вы можете перейти к [использованию ManifoldJS для расширения пакета](./using-manifoldjs-to-package-extensions.md) , чтобы узнать, как использовать средство на основе Node. js для выполнения всех этих действий.

> [!NOTE]
> Отправка расширения Microsoft EDGE в Microsoft Store в настоящее время ограничена возможностями. Создав, упакуйте и протестировали расширение, отправьте запрос на [форму отправки расширения](https://aka.ms/extension-request).



## Подготовка папки отправки

Чтобы подготовить расширение к отправке, необходимо создать папку со следующей структурой:

![изображение структуры папок. В папке "расширение" находятся папки AppxManifest. XML, "папка расширения" и "ресурсы"](./../../media/packaging_folder-structure.png)

В корневой папке нужно добавить файл AppXManifest. XML. Этот файл используется для указания содержимого и макета пакета.

Кроме того, у вас должна быть папка Assets, содержащая ресурсы пользовательского интерфейса, которые будут использоваться в Microsoft Store, и папка расширения, содержащая файлы расширения (сценарии, значки и т. д.).

> [!IMPORTANT]
> Вы можете создать другую структуру папок для пакета, но структура папок должна совпадать со значениями AppXManifest.

### AppXManifest. XML
Файл AppXManifest — это документ XML, содержащий сведения, необходимые системе для развертывания, отображения и обновления приложения для Windows. Этот файл содержит также удостоверение пакета, возможности и визуальные элементы. Каждый пакет приложения должен включать один файл AppXManifest.

Разработчики могут использовать следующий шаблон для файла AppXManifest. XML:

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

#### Значения шаблона удостоверения приложения
После того как вы заменили [имя расширения](./extensions-in-the-windows-dev-center.md#name-reservation) с помощью центра разработки для Windows, вы сможете найти необходимые сведения об удостоверении пакета, необходимые для замены указанных ниже значений в AppXManifest. XML.

- `Name`
- `Publisher`
- `DisplayName`
- `PublisherDisplayName`

Вы можете получить доступ к странице удостоверения приложения, выполнив указанные ниже действия.

1. Перейдите в [центр разработки для Windows](https://developer.microsoft.com/windows/).
2. Войдите в свою учетную запись разработчика.
3. Перейдите на панель мониторинга.
4. Выберите имя расширения.

   ![список расширений](./../../media/select-app.png)
5. Перейдите на страницу удостоверения приложения, которая находится в разделе Управление приложениями (после регистрации приложения).

   ![Страница идентификации приложения](./../../media/app-identity.png)


Теперь вы можете заполнить шаблон AppXManifest значениями из страницы удостоверение приложения, как показано в шаблоне:


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

#### Значения шаблона манифеста JSON
Некоторые значения в AppXManifest должны соответствовать параметрам, определенным в манифесте JSON. Обновите следующие значения в appxmanifest. XML на основе манифеста JSON расширения:

- `Version` — Версия, указанная в манифесте JSON расширения. Строка должна соответствовать формату X. X. X. X, где Последнее целое число должно быть равным 0. Например: 1.2.3.0

   ```xml
   <Identity
     Name="37369abigailc.MyExtension"
     Publisher="CN=732F2E5E-B9A6-4243-85F6-A4210F57AA10"
     Version="1.0.0.0" />
   ```

- `Description` -Это копия описания в манифесте JSON расширения.

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


### Папка "ресурсы"

В папке Assets вам понадобятся три разных размера значков. Эти значки будут использоваться в Microsoft Store и пользовательском интерфейсе Windows. Дополнительные сведения об этих значках можно найти в руководстве по [проектированию](./../design.md#icons-for-packaging) .

![Папка «ресурсы» с тремя размерами значков](./../../media/assets-folder.png)

После создания необходимых ресурсов пользовательского интерфейса обновите AppXManifest. XML, чтобы он указывал на нужные файлы.

- 44 x 44

   ```xml
   Square44x44Logo="Assets/icon_44.png"
   ```

- 50x50

  ```xml
   <Logo>Assets/icon_50.png</Logo>
  ```

- 150 x 150

  ```xml
  Square150x150Logo="Assets/icon_150.png"
  ```


### Папка "расширение"
Скопируйте файлы расширений (сохранив структуру папок) в папку "расширение". Убедитесь в `manifest.json` том, что папка расширения находится в корне.

![папка расширения со всеми файлами расширений](./../../media/extension-folder.png)


### Поддержка более чем одной национальной настройки
Если ваше расширение поддерживает более одного языка, вы можете настроить пакет AppX так, чтобы в нем отображался правильный локализованный значок и описание. Дополнительные сведения см. в разделе [Локализация пакетов расширений](./localizing-extension-packages.md) .

### Создание Appx

Чтобы создать appx, вам нужно найти путь для makeappx. Обычно это расположение находится в следующем расположении, если вы используете 64-разрядный компьютер.

`C:\Program Files (x86)\Windows Kits\10\bin\x64`

Выполните следующую команду, чтобы создать пакет AppX для вашего расширения.

`[Path to makeappx] makeappx pack /h SHA256 /d [Path to package folder created in #1] /p [Path to the appx file that you want to create]`

Это должно выглядеть примерно так, как если бы вы заполнили пути.

`C:\Program Files (x86)\Windows Kits\10\bin\x64>makeappx.exe pack /h SHA256 /d "C:\Extension\My Extension" /p C:\Extension\MyExtension.appx`

### Распаковка Appx
Возможно, потребуется распаковать ранее созданный AppX и использовать его в качестве отправной точки для следующей итерации расширения или подтвердить правильность создания AppX.

Для этого вы можете выполнить следующую команду, чтобы распаковать пакет AppX расширения Microsoft Edge:

`[Path to makeappx] makeappx unpack /v /p [Path to appx file you want to unpack] /d [Path to the location where you want to create the package folder]`

Это должно выглядеть примерно так, как вы залиты:

`C:\Program Files (x86)\Windows Kits\10\bin\x64>makeappx.exe unpack /v /p "C:\Extension\MyExtension.appx" /d "C:\Extension\My Extension"`





## Тестирование пакета AppX

Вы можете протестировать пакет AppX Microsoft Edge с помощью неопубликованных приложений в Microsoft Edge. Неопубликованное приложение-пакет расширений AppX подобен неопубликованному в Skype стандартному приложению для Windows. Для подписывания пакета вам потребуется создать сертификат, а затем добавить его в Windows.

### Выполняется

Узнайте, [как создать сертификат подписи пакета приложения](https://msdn.microsoft.com/library/windows/desktop/jj835832.aspx) и [как подписать пакет приложения с помощью SignTool](https://msdn.microsoft.com/library/windows/desktop/jj835835.aspx) для получения сведений о процессе подписи и сертификации для пакетов.

> [!NOTE]
> Перед отправкой пакета расширения в Microsoft Store вам не нужно подписывать его. процесс приема магазина поможет вам!

После того как вы подписали пакет с помощью созданного вами сертификата, сертификат по-прежнему не будет доверять локальному компьютеру для развертывания пакетов приложений, пока вы не установите его в хранилище доверенных сертификатов на локальном компьютере. Для этого можно использовать программу Certutil. exe, которая поставляется вместе с Windows.

Чтобы установить сертификаты с помощью WindowsCertutil. exe, запустите cmd. exe как администратор и выполните следующую команду:

`Certutil -addStore TrustedPeople MyKey.cer`

После того как сертификаты больше не используются, рекомендуется удалить их, выполнив следующую команду в командной строке администратора:

`Certutil -delStore TrustedPeople certID`

CertID — это серийный номер сертификата. Чтобы определить серийный номер сертификата, выполните следующую команду:

`Certutil -store TrustedPeople`

### Развертывание
Пакет AppX для расширения Microsoft EDGE можно развернуть, выполнив следующую команду в PowerShell (от имени администратора).

`Add-AppxPackage [path to AppX]`

## Автоматическое тестирование с помощью фотодисковода

По мере изменения юбилея вы можете программно неопубликованного свое расширение в Microsoft Edge с помощью веб – дисковода, обеспечивая автоматическое тестирование расширений при запуске Microsoft EDGE в режиме веб – дисковода. Это позволит вам настроить автоматические тесты для любого расширения, которое управляет контентом на странице, и проверяет правильность поведения.

Чтобы неопубликованного расширение для автоматического тестирования, необходимо сохранить папку расширения в разделе `%LOCALAPPDATA%\Packages\Microsoft.MicrosoftEdge_8wekyb3d8bbwe\LocalState\` . После добавления расширения в `LocalState` Каталог вам потребуется создать [`EdgeOptions`](https://seleniumhq.github.io/selenium/docs/api/dotnet/html/T_OpenQA_Selenium_Edge_EdgeOptions.htm) объект и добавить в `extensionPaths` него возможность. Значение этой возможности — это массив абсолютных путей к расширениям (в `LocalState` каталоге), которые должны быть загружены на стороне, когда Microsoft Edge запускается в режиме веб-накопителя.

Полный пример расширений загрузки сбоку в Microsoft Edge с помощью веб-накопителя вы также ознакомьтесь с приведенными ниже [файлами на C#](https://github.com/scottlow/Ignite2016/blob/master/Ignite%202016%20WebDriver%20Demo/IgniteWebDriverDemo/Program.cs) .
