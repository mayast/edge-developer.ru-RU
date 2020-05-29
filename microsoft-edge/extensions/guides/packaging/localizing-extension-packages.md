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
# Локализация расширений Microsoft Edge для Windows и Microsoft Store  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

Это руководство содержит сведения о том, как локализовать расширение Microsoft EDGE, чтобы оно было готово для нескольких национальных настроек при выпуске. Чтобы полностью локализовать расширение, вам потребуется выполнить действия, описанные как в Windows, так и в Microsoft Store.

Если вы хотите локализовать ресурсы расширения для Microsoft EDGE, вы можете научиться использовать платформу i18n в [руководстве по интернационализации](../internationalization.md).


> [!NOTE]
> Если ваше расширение не поддерживает несколько языков, вы можете перейти к [локализованному имени и описанию в Microsoft Store](#localizing-name-and-description-in-the-microsoft-store).


## Общие сведения о процессе локализации

Первый шаг к извлечению расширения, доступного для широкой аудитории, — это [Настройка ее appxmanifest](#configuring-the-appxmanifest) для нескольких языков. В Microsoft Store пользователи будут показывать языки, поддерживаемые вашим расширением. Некоторые поля в AppxManifest также нужно изменить, если вы хотите, чтобы имя расширения [локализуется в пользовательском интерфейсе Windows и в Microsoft Store](#localizing-extension-resources-for-windows-and-the-microsoft-store).


После настройки AppxManifest вам потребуется [создать строковые ресурсы JSON](#creating-json-string-resources) для языков, которые вы указали как поддерживаемые. Для этого требуется создать RESJSON-файл для каждого языка, где в каждом файле есть все строки пользовательского интерфейса на этом языке.


После того как RESJSON файлы для поддерживаемых языков будут сделаны, потребуется [создать файл ресурсов с расширением PRI](#creating-the-resources-file). Она будет создана с помощью файла конфигурации для средства **MakePRI** , которое входит в состав [пакета SDK для Windows 10](https://developer.microsoft.com/windows/downloads/windows-10-sdk). 

> [!NOTE]
> Если вы загружаете пакет SDK для Windows 10 для использования средства MakePri. exe, вы можете выбрать только "средства подписывания Windows SDK для классических приложений" и "Windows SDK для управляемых приложений UWP", чтобы сделать скачивание более светлым. Средство MakePri. exe появится во вложенных папках папки C:\Program Files (x86) \Windows Kits\10\bin\10.0.17713.0.


После того как вы загрузили расширение, последний этап — [локализовать название и описание в Microsoft Store](#localizing-name-and-description-in-the-microsoft-store).

> [!NOTE]
> Отправка расширения Microsoft EDGE в Microsoft Store в настоящее время ограничена возможностями. [Поделитесь с нами](https://aka.ms/extension-request) с помощью ваших запросов на участие в Microsoft Store, и мы поможем вам ознакомиться с будущими обновлениями.



## Настройка AppXManifest

Список поддерживаемых языков расширения в магазине Microsoft Store формируется на основе его значений AppXManifest. Этот список указывается с помощью `Resource` элемента.


![изображение параметров](./../../media/language-app-details.png)

Чтобы задать список языков, которые поддерживаются вашим расширением, вы можете добавить `Resource` элемент в следующем формате (этот `Resource` элемент будет показываться в Microsoft Store на английском, немецком и французском языках):

```xml
<Resources>
    <Resource Language="en-us"/>
    <Resource Language="de-de"/>
    <Resource Language="fr-fr"/>
</Resources>
```

Сведения о языках и кодах языков, поддерживаемых Microsoft Store, можно найти на странице [Поддерживаемые языки](https://msdn.microsoft.com/windows/uwp/publish/supported-languages) .


Чтобы указать локализованные строки для всех общедоступных элементов, отображаемых в AppxManifest, необходимо использовать идентификатор ресурса в формате `ms-resource:<resource id>` .

В приведенных ниже фрагментах кода выводятся полные AppxManifest. Из локализованных файлов ресурсов должны извлекаться следующие значения:

- Properties\DisplayName
- Properties\Description
- Properties\PublisherDisplayName


```xml
<Properties>
    <DisplayName>ms-resource:DisplayName</DisplayName>
    <Description>ms-resource:Description</Description>
    <Logo>Assets\PackageLogo.png</Logo>
    <PublisherDisplayName>ms-resource:PublisherName</PublisherDisplayName>
</Properties>
```

- Applications\Application\VisualElements\DisplayName
- Applications\Application\VisualElements\Description
- Applications\Application\Extensions\Extension\AppExtension\DisplayName

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


## Локализация ресурсов расширений для Windows и Microsoft Store

Теперь, когда ваша AppxManifest настроена для нескольких языков, есть несколько ключевых различий, которые необходимо знать между локализацией пользовательского интерфейса в расширении и локализацией расширения для Windows и Microsoft Store.

Несмотря на то, что расширения Microsoft EDGE не работают за пределами Microsoft EDGE, управление ими может происходить в Windows. Например, пользователи могут управлять своими расширениями в приложении "Параметры".


![изображение параметров](./../../media/settings.png)



Имя расширения, которое отображается в приложении "Параметры" в Windows, поступает из AppXManifest. Если это значение жестко на английском языке, английская версия названия будет отображаться на неанглийских устройствах Windows. Если фирменная символика расширения — только на английском языке, это можно сделать без зашиты.


> [!NOTE]
> Если вы хотите использовать локализованные имена для расширения Microsoft EDGE в Windows, убедитесь, что локализованные имена также [доступны и зарезервированы](./extensions-in-the-windows-dev-center.md#name-reservation) , прежде чем вносить изменения в файл AppXManifest. Если имена не зарезервированы, при отправке финального пакета в центр разработки для Windows появляется следующее сообщение об ошибке:</br></br>

![Ошибка языка](./../../media/language-error.png)</br></br>


Инфраструктура локализации на основе i18n, определенная для расширений JavaScript, применима только в среде Microsoft Edge.

За пределами Microsoft EDGE в Windows и Microsoft Store единственным набором поддерживаемых платформ локализации является платформа для локализации универсальной платформы Windows (UWP).

Несмотря на то что мы поддерживаем ресурсы на основе JSON для приложений для Windows на базе HTML, схема для ресурсов JSON не совпадает с определением для расширений JavaScript.


Ниже описаны основные отличия в [приложениях для Windows на основе HTML](https://msdn.microsoft.com/library/windows/apps/hh465228.aspx).
-    Ресурсы задаются в файлах RESJSON вместо файлов JSON.
-    Поддерживаемые национальные настройки должны быть указаны в файле AppXManifest, в котором первый язык используется по умолчанию.
-    Для использования ресурсов в приложениях для Windows на основе HTML используется следующая схема:
    ```json
    {
        "greeting"              : "Hello",
        "_greeting.comment"     : "A welcome greeting.",

        "farewell"              : "Goodbye",
        "_farewell.comment"     : "A goodbye."
    }
    ```
    Пара имя/значение, обозначенная подчеркиванием, — это комментарии к соответствующему строковому ресурсу.
-    файлы. resjson компилируются в PRI-файлы, которые должны быть включены во время создания пакета AppX.


### Создание строковых ресурсов JSON
После настройки AppxManifest в руки и различий между платформами i18n и для локализации UWP вы можете создавать файлы ресурсов.

Только одна строка ресурса в манифесте применима к пакетам расширений Microsoft Edge. `DisplayName`Строка обычно локализуется в расширениях JavaScript и может быть легко сопоставлена с файлами. resjson, которые предполагается использовать для Windows. Предполагается, что это единственный ресурс, который вы хотите локализовать, — образец файла. resjson, который нужно создать:

```json
{
    "DisplayName"              : "Jigsaw",
    "_DisplayName.comment"     : "Name of extension."
}
```

Идентификатор ресурса в каждом файле. resjson должен совпадать с ИДЕНТИФИКАТОРом, используемым в AppXManifest. С помощью приведенного выше фрагмента example. resjson должна быть указана соответствующая запись AppXManifest:

`DisplayName="ms-resource:DisplayName"`

Каждый язык, поддерживаемый вашим расширением, должен иметь соответствующий файл Resources. RESJSON и размещаться в следующей структуре папок:

![Структура папок на языке](./../../media/resources-folder.png)


### Создание файла ресурсов
После создания всех файлов. resjson вы можете создать файл индекса ресурсов пакета (PRI). В этом файле хранятся ресурсы для всех поддерживаемых языков. Для этого можно использовать средство **MakePRI** , которое входит в состав пакета SDK для Windows 10.


Сначала необходимо создать файл конфигурации. Это определяет используемые по умолчанию квалификаторы и платформу для ресурсов. В этом примере сделайте язык по умолчанию английским (US) и платформой Windows 10. Для этого создайте файл priconfig. XML со следующим содержанием в [корневой каталог]:

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

Теперь вы можете создать файл Resources. PRI с помощью файла конфигурации и средства MakePRI. Для этого примера корневой каталог для проекта будет [корневой каталог].


```cmd
MakePRI new /pr [Root folder] /cf [Root folder]\priconfig.xml /mn [Root folder]\AppxManifest.xml /of [Root folder]\resources.pri /o
```

Теперь у вас есть один файл Resources. PRI в корневой папке.

![Папка "ресурсы"](./../../media/resources.png)


## Локализация имени и описания в Microsoft Store

После попытки загрузить полный локализованный пакет центр разработки для Windows обнаружит, что поддерживается несколько языков, и проверьте, есть ли у вас соответствующие локализованные имена и описания для каждого из них. Если хотя бы одно из локализованных значений отсутствует, отправка будет заблокирована до тех пор, пока вы не выдасте нужные значения.

Если вы хотите предоставить только локализованные имя и описание для Microsoft Store (но не Windows), вы можете сделать это, заполнив [все локализованные имена для вашего расширения](./extensions-in-the-windows-dev-center.md#name-reservation).


После того как вы заменили дополнительные локализованные имена, вы можете создать обновленную отправку. В разделе Описание вы можете управлять дополнительными языками для вашего описания в магазине Microsoft Store:

![Описание приложения на японском языке](./../../media/manage-description-languages.png)

После того как вы выбрали "Управление дополнительными языками", вам будет предложено выбрать языки, которые нужно добавить в описание Microsoft Store. Новый язык будет отображаться как "дополнительный язык описания" в разделе "Описание".

Вы можете щелкнуть отдельную ссылку в разделе "Описание", чтобы предоставить локализованное название и описание, заметки о выпуске и визуальные ресурсы для каждого языка. Описание для магазина Microsoft Store не извлекается из AppXManifest. Каждое локализованное описание должно быть введено вручную в центре разработки для Windows:

![Описание приложения на японском языке](./../../media/japanese-app-description.png)

После отправки локализованных описаний и публикации расширения любой пользователь, имеющий доступ к локализованной странице расширения в Microsoft Store, будет видеть следующий пользовательский интерфейс:

![Магазин Windows на японском языке](./../../media/japanese-windows-store.png)
 

## Примеры AppxManifest

### Нелокализованные AppxManifest
В следующем примере показан AppxManifest, который не является локализованным, и поддерживает только национальную настройку "en-US".


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


#### Локализованные AppxManifest
Этот образец AppxManifest локализуется для восьми других языков, кроме en-US. Обратите внимание на `ms-resource:<resource id>` повторения.


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
