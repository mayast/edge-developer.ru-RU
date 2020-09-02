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
# Использование ManifoldJS для создания пакетов AppX расширений  

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]  

ManifoldJS — это инструмент Open Source Node.js, который позволяет быстро и безболезненно создавать пакеты, которые можно использовать для отправки в Microsoft Store.  

Если вы используете собственный обмен сообщениями в расширении, вы должны пропустить следующую статью и перейти к [встроенной службе сообщений в Microsoft Edge](../native-messaging.md#creating-an-extension-with-native-messaging) для инструкции по упаковке.  

Перед тем как приступить к работе, вам по-прежнему придется прочитать статьи, посвященные следующим статьям.  

*   [Расширения в Центре разработки для Windows](./extensions-in-the-windows-dev-center.md)  
*   [Локализация пакетов расширений](./localizing-extension-packages.md)  

> [!NOTE]
> Отправка расширения Microsoft EDGE в Microsoft Store в настоящее время ограничена возможностями.  Создав, упакуйте и протестировали свое расширение, отправьте запрос на [форму отправки расширения](https://developer.microsoft.com/microsoft-edge/extensions/requests).  

## Установка Node.js и ManifoldJS  

Первое, что нужно сделать, — это установить [Node.js LTS](https://nodejs.org/en/download).  
После того как у вас есть узел, в командной строке (предпочтительный PowerShell) выполните следующую команду, чтобы установить ManifoldJS.  

```shell
npm install -g manifoldjs
```  

Чтобы убедиться, что вы правильно установили ManifoldJS, запустите `manifoldjs` из командной строки. Если ManifoldJS не был распознан, добавьте `%APPDATA%\npm` его в ПЕРЕМЕННЫЕ Path.  

## Упаковка с помощью ManifoldJS  

Чтобы начать процесс упаковки, необходимо открыть командную строку и изменить каталоги на папку, которая будет назначена для упакованного расширения.  

Например:

```shell
cd C:\manifoldJSTest
```  

> [!NOTE]
> `manifoldjs`Команда выводит данные из текущего каталога и перезаписывает содержимое.  

Теперь, когда вы используете конечную папку, выполните следующую команду:  

```shell
manifoldjs -l debug -p edgeextension -f edgeextension -m path\to\manifest.json
```  

`mainifoldjs`Команду можно разбить на следующие части.  

:::row:::
   :::column span="1":::
      `-l debug`  
   :::column-end:::
   :::column span="2":::
      Изменение уровня ведения журнала на `debug` полный вывод.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `-p edgeextension`  
   :::column-end:::
   :::column span="2":::
      Задает единственную платформу для выполнения преобразования `edgeextension` .  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `-f edgeextension`  
   :::column-end:::
   :::column span="2":::
      Сообщает программе, что формат манифеста имеет `edgeextension` Формат, и не следует следить за тем, что он не прошел проверку.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `-m \path\to\manifest.json`  
   :::column-end:::
   :::column span="2":::
      Путь к манифесту расширения, который вы хотите преобразовать.  
   :::column-end:::
:::row-end:::  

После завершения работы ManifoldJS вы получите папку со следующим содержимым.  

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

generationInfo.jsдля файла — это журнал, созданный ManifoldJS, и он не будет включен в пакет расширения. `manifest`Будет упаковано только содержимое папки. В папке манифеста в папке Assets содержатся изображения, которые будут использоваться в пользовательском интерфейсе Windows и Microsoft Store, а в папке расширение — содержимое вашего расширения.  

Теперь, когда у вас есть нужные файлы, вам нужно будет изменить созданный файл AppXManifest в `manifest` папке. Если в поле "имя" manifest.jsрасширения указана многоязыковая строка, то после запуска ManifoldJS имя папки верхнего уровня не будет содержать подчеркивания и включать сообщение "MSG".

Например, manifest.jsдля файла с помощью следующего `"name"` поля.  

```shell
"name" : "__MSG_appName__"
```  

у вас есть папка манифеста, в которой она находится `\<CURRENT DIRECTORY>\MSGappName\edgeextension\manifest` .  

В файле AppXManifest вам понадобятся следующие возможности:  

 *   Замените необходимые поля удостоверения и поле PublisherDisplayName, как показано [здесь](./creating-and-testing-extension-packages.md#app-identity-template-values). Обратите внимание, что если вы используете упаковку только для тестирования или для корпоративной рассылки, вы можете использовать значения заполнителей вместо регистрации для учетной записи центра разработки для Windows.  
 *   Замените значки заполнителей в папке Assets значками для расширения тем же размером (150x150, 50x50, 44x44) и именами. Сведения о том, где используются эти значки, можно найти в руководстве по [проектированию](./../design.md#icons-for-packaging) .  
 *   Если ваше расширение локализовано, следуйте инструкциям по [локализации расширений Microsoft Edge](./localizing-extension-packages.md) . Если он не локализован, только прочтите [имя и описание в разделе Microsoft Store](./localizing-extension-packages.md#localizing-name-and-description-in-the-microsoft-store) .  

После того как `appxmanifest.xml` файл будет отсортирован, выполните следующую команду, чтобы создать пакет.  

```shell
manifoldjs -l debug -p edgeextension package <EXTENSION NAME>\edgeextension\manifest\
```  

Теперь пакет будет находиться в папке **пакета** , расположенной в папке edgeextension. Дополнительные сведения о том, как неопубликованного новый пакет, можно найти в разделе [тестирование](./creating-and-testing-extension-packages.md#testing-an-appx-package) раздела Создание и тестирование пакетов расширений.  

После того как пакет будет проверен, вы можете отправить запрос на [форму отправки расширения](https://aka.ms/extension-request) , чтобы стать ее публикацией в Microsoft Store.  
