---
description: Собственная разница в почтовых сообщениях из документации Chrome
title: Встроенные сообщения
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/31/2019
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: Edge-Chromium, Разработка расширений, расширения браузера, надстройки, центр партнера, разработчик
ms.openlocfilehash: 0fe45ea681c54ddea7b27a8d954022b8bda45770
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571648"
---
# Встроенные сообщения  

Microsoft EDGE теперь допускает расширение, установленное из каталога надстроек Microsoft Edge \ (надстройки Microsoft Edge \), чтобы обмениваться сообщениями с приложением в машинном коде с помощью API передачи сообщений.  Чтобы включить эту функцию, необходимо выполнить описанные ниже действия при реализации собственного узла сообщений в собственном приложении.  

<!--
 > [!NOTE]
> Native messaging is currently not supported on macOS and Linux version of Microsoft Edge.  This feature support is planned to be implemented soon.  -->  

1.  **Собственный узел сообщений**:  
    
    Чтобы зарегистрировать собственный узел сообщений, приложение должно установить файл манифеста, который определяет конфигурацию собственного узла сообщений.  Ниже приведен пример файла манифеста.  
    
    ```xml
    {
        "name": "com.my_company.my_application",
        "description": "My Application",
        "path": "C:\\Program Files\\My Application\\chrome_native_messaging_host.exe",
        "type": "stdio",
        "allowed_origins": [
            "chrome-extension://knldjmfmopnpolahpmmgbagdohdnhkik/"
        ]
    }
    ```  
    
Исходный файл манифеста узла сообщений должен быть допустимым JSON и содержать следующие поля:  

| Имя | Описание |  
|:--- |:--- |  
| `name` | Имя собственного узла сообщений. Клиенты передают эту строку `runtime.connectNative` или `runtime.sendNativeMessage` .  Это имя должно содержать только строчные буквы, цифры, знаки подчеркивания и точки.  Имя не должно начинаться или заканчиваться точкой, а точка после нее не должна быть другой точкой. |  
| `description` | Краткое описание приложения. |  
| `path` | Путь к двоичному файлу хоста сообщений в машинном коде.  В Windows путь может относиться к каталогу, в котором находится файл манифеста.  В macOS путь должен быть абсолютным.  Процесс хоста запустится с текущим набором каталогов и каталогом, содержащим двоичный файл узла. Например, если для этого параметра задано значение `C:\Application\nm_host.exe` , двоичный код запускается с текущим каталогом `C:\Application\` . |  
| `type` | Тип интерфейса, используемого для связи с собственным узлом сообщений.  В настоящее время для этого параметра существует только одно возможное значение: `stdio` .  Это значение указывает на то, что хром должен использовать `stdin` и `stdout` взаимодействовать с узлом. |  
| `allowed_origins` |  список расширений, которые должны иметь доступ к собственному узлу сообщений.  Чтобы разрешить собственное приложение определять и взаимодействовать с расширением надстроек Microsoft EDGE, установите `allowedorigins` для него значение `extension://[Microsoft-Catalog-extensionID]` в файле манифеста собственного узла сообщений. |  

1.  **Расположение собственного узла сообщений**  
    
    Расположение файла манифеста зависит от платформы.  
    
    В Windows файл манифеста может находиться в любом месте файловой системы.  Установщик приложения должен создать раздел реестра  
    
    `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application`  
    или  
    `HKEY_CURRENT_USER\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application`,  
    
    и задайте в качестве значения по умолчанию для этого ключа полный путь к файлу манифеста.  Например, с помощью следующей команды:  
    
    ```shell
    REG ADD "HKCU\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application" /ve /t REG_SZ /d "C:\path\to\nmh-manifest.json" /f
    ```  
    
    или с помощью следующего REG – файла:  
    
    ```shell
    Windows Registry Editor Version 5.00
    [HKEY_CURRENT_USER\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application]
    @="C:\\path\\to\\nmh-manifest.json"
    ```  
    
    Когда Microsoft Edge выполнит поиск собственных узлов сообщений, сначала запрашивается 32-разрядный реестр, а затем — 64-битовый реестр.  

В macOS поисковые машинные системы систем обработки сообщений выполняются в определенном расположении, а машинные точки сообщений на уровне пользователя — в подкаталоге в каталоге профиля пользователя с именем `NativeMessagingHosts` .  

Microsoft EDGE на macOS \ (масштаб системы):  
`/Library/Microsoft/Edge/NativeMessagingHosts/com.my_company.my_application.json`  

Microsoft EDGE на macOS \ (для определенного пользователя, путь по умолчанию):  
`~/Library/Application Support/Microsoft Edge <ChannelName>/ NativeMessagingHosts/com.my_company.my_application.json`  

`<ChannelName>` может быть Канарские, dev или Beta. Для стабильного канала `Microsoft Edge` следует использовать только `<ChannelName`>"не требуется.

<!-- image links -->  

<!-- links -->  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> [Здесь](https://developer.chrome.com/extensions/nativeMessaging)будет найдена исходная страница.  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
