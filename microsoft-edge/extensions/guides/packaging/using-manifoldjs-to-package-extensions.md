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
# Использование ManifoldJS для создания пакетов AppX расширений  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

ManifoldJS — это инструмент Open source node. js, который позволяет быстро и безболезненно создавать пакеты, которые можно использовать для отправки в Microsoft Store.

Если вы используете собственный обмен сообщениями в расширении, вы должны пропустить этот параметр и перейти к [встроенной службе сообщений в Microsoft Edge](../native-messaging.md#creating-an-extension-with-native-messaging) для инструкции по упаковке. 

Прежде чем приступить к работе, вам по-прежнему придется прочитать следующие статьи:

- [Расширения в центре разработки для Windows](./extensions-in-the-windows-dev-center.md)
- [Локализация пакетов расширений](./localizing-extension-packages.md)

> [!NOTE]
> Отправка расширения Microsoft EDGE в Microsoft Store в настоящее время ограничена возможностями. Создав, упакуйте и протестировали расширение, отправьте запрос на [форму отправки расширения](https://aka.ms/extension-request).


## Установка Nodes. js и ManifoldJS

Прежде всего необходимо установить [node. js LTS](https://nodejs.org/en/download/).
После того как у вас есть узел, в командной строке (предпочтительный PowerShell) выполните следующую команду, чтобы установить ManifoldJS:

`npm install -g manifoldjs`

Чтобы убедиться, что вы правильно установили ManifoldJS, запустите `manifoldjs` из командной строки. Если ManifoldJS не распознается, добавьте `%APPDATA%\npm` его в ПЕРЕМЕННЫЕ Path.

## Упаковка с помощью ManifoldJS

Чтобы начать процесс упаковки, необходимо открыть командную строку и изменить каталоги на папку, которая будет назначена для упакованного расширения.

Пример

`cd C:\manifoldJSTest`

> [!NOTE]
> ManifoldJS будет выводиться в текущем каталоге и может перезаписывать содержимое.



Теперь, когда вы находитесь в конечной папке, выполните следующую команду:

`manifoldjs -l debug -p edgeextension -f edgeextension -m <EXTENSION LOCATION>\manifest.json`


Эту команду можно разделить на следующие части:
 -    **-l Отладка**: меняет уровень ведения журнала на "Отладка", чтобы получить полную распечатку.
 -    **-p edgeextension**: задает единственную платформу для выполнения преобразования в edgeextension.
 -    **-f edgeextension**: сообщает программе, что формат манифеста является форматом edgeextension, и не следует следить за тем, что он не прошел проверку.
 -    **-m \ < расположение расширения > \manifest.JSON**: путь к манифесту расширения, который вы хотите преобразовать.


После завершения работы ManifoldJS вы получите папку со следующим содержанием:

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

Файл generationInfo. JSON — это журнал, созданный ManifoldJS, и он не будет включен в пакет расширения. Будет упаковано только содержимое папки **манифеста** . В папке манифеста в папке Assets содержатся изображения, которые будут использоваться в пользовательском интерфейсе Windows и Microsoft Store, а в папке расширение — содержимое вашего расширения.


Теперь, когда у вас есть нужные файлы, вам нужно будет изменить созданный файл AppXManifest в папке **манифеста** . Если в файле Extension. JSON есть Международная строка для поля "имя", то после запуска ManifoldJS имя папки верхнего уровня не будет содержать подчеркивания и включать сообщение "MSG".

Например, файл manifest. JSON со следующим `"name"` полем:

`"name" : "__MSG_appName__"`

у вас есть папка манифеста, в которой она находится `\<CURRENT DIRECTORY>\MSGappName\edgeextension\manifest` .

В файле AppXManifest необходимо:
 -    Замените необходимые поля удостоверения и поле PublisherDisplayName, как показано [здесь](./creating-and-testing-extension-packages.md#app-identity-template-values). Обратите внимание, что если вы используете только упаковку для тестирования или корпоративное распространение, вы можете использовать значения заполнителей вместо регистрации для учетной записи центра разработки для Windows.
 -    Замените значки заполнителей в папке Assets значками для расширения тем же размером (150x150, 50x50, 44x44) и именами. Сведения о том, где используются эти значки, можно найти в руководстве по [проектированию](./../design.md#icons-for-packaging) .
 - Если ваше расширение локализовано, следуйте инструкциям по [локализации расширений Microsoft Edge](./localizing-extension-packages.md) . Если он не локализован, только прочтите [имя и описание в разделе Microsoft Store](./localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) .

После того как файл AppxManifest. XML будет отсортирован, выполните следующую команду, чтобы создать пакет.

`manifoldjs -l debug -p edgeextension package <EXTENSION NAME>\edgeextension\manifest\`

Теперь пакет будет находиться в папке **пакета** , расположенной в папке edgeextension. Сведения о том, как неопубликованного новый пакет, можно найти [в разделе Создание и тестирование пакетов](./creating-and-testing-extension-packages.md#testing-an-appx-package) расширений.

После того как пакет будет проверен, вы можете отправить запрос на [форму отправки расширения](https://aka.ms/extension-request) , чтобы стать ее публикацией в Microsoft Store.
