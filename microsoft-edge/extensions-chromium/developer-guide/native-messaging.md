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
# <span data-ttu-id="9e0cb-104">Встроенные сообщения</span><span class="sxs-lookup"><span data-stu-id="9e0cb-104">Native Messaging</span></span>  

<span data-ttu-id="9e0cb-105">Microsoft EDGE теперь допускает расширение, установленное из каталога надстроек Microsoft Edge \ (надстройки Microsoft Edge \), чтобы обмениваться сообщениями с приложением в машинном коде с помощью API передачи сообщений.</span><span class="sxs-lookup"><span data-stu-id="9e0cb-105">Microsoft Edge now allows Extension installed from Microsoft Edge Addons catalog \(Microsoft Edge Addons\) to exchange messages with a native application using message passing APIs.</span></span>  <span data-ttu-id="9e0cb-106">Чтобы включить эту функцию, необходимо выполнить описанные ниже действия при реализации собственного узла сообщений в собственном приложении.</span><span class="sxs-lookup"><span data-stu-id="9e0cb-106">To enable the feature, you need to make sure of following things while implementing native messaging host of your Native Application.</span></span>  

<!--
 > [!NOTE]
> Native messaging is currently not supported on macOS and Linux version of Microsoft Edge.  This feature support is planned to be implemented soon.  -->  

1.  <span data-ttu-id="9e0cb-107">**Собственный узел сообщений**:</span><span class="sxs-lookup"><span data-stu-id="9e0cb-107">**Native messaging host**:</span></span>  
    
    <span data-ttu-id="9e0cb-108">Чтобы зарегистрировать собственный узел сообщений, приложение должно установить файл манифеста, который определяет конфигурацию собственного узла сообщений.</span><span class="sxs-lookup"><span data-stu-id="9e0cb-108">In order to register a native messaging host the application must install a manifest file that defines the native messaging host configuration.</span></span>  <span data-ttu-id="9e0cb-109">Ниже приведен пример файла манифеста.</span><span class="sxs-lookup"><span data-stu-id="9e0cb-109">Below is an example of the manifest file:</span></span>  
    
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
    
<span data-ttu-id="9e0cb-110">Исходный файл манифеста узла сообщений должен быть допустимым JSON и содержать следующие поля:</span><span class="sxs-lookup"><span data-stu-id="9e0cb-110">The native messaging host manifest file must be valid JSON and contains the following fields:</span></span>  

| <span data-ttu-id="9e0cb-111">Имя</span><span class="sxs-lookup"><span data-stu-id="9e0cb-111">Name</span></span> | <span data-ttu-id="9e0cb-112">Описание</span><span class="sxs-lookup"><span data-stu-id="9e0cb-112">Description</span></span> |  
|:--- |:--- |  
| `name` | <span data-ttu-id="9e0cb-113">Имя собственного узла сообщений.</span><span class="sxs-lookup"><span data-stu-id="9e0cb-113">Name of the native messaging host.</span></span> <span data-ttu-id="9e0cb-114">Клиенты передают эту строку `runtime.connectNative` или `runtime.sendNativeMessage` .</span><span class="sxs-lookup"><span data-stu-id="9e0cb-114">Clients pass this string to `runtime.connectNative` or `runtime.sendNativeMessage`.</span></span>  <span data-ttu-id="9e0cb-115">Это имя должно содержать только строчные буквы, цифры, знаки подчеркивания и точки.</span><span class="sxs-lookup"><span data-stu-id="9e0cb-115">This name must only contain lowercase alphanumeric characters, underscores, and dots.</span></span>  <span data-ttu-id="9e0cb-116">Имя не должно начинаться или заканчиваться точкой, а точка после нее не должна быть другой точкой.</span><span class="sxs-lookup"><span data-stu-id="9e0cb-116">The name must not start or end with a dot, and a dot must not be followed by another dot.</span></span> |  
| `description` | <span data-ttu-id="9e0cb-117">Краткое описание приложения.</span><span class="sxs-lookup"><span data-stu-id="9e0cb-117">Short application description.</span></span> |  
| `path` | <span data-ttu-id="9e0cb-118">Путь к двоичному файлу хоста сообщений в машинном коде.</span><span class="sxs-lookup"><span data-stu-id="9e0cb-118">Path to the native messaging host binary.</span></span>  <span data-ttu-id="9e0cb-119">В Windows путь может относиться к каталогу, в котором находится файл манифеста.</span><span class="sxs-lookup"><span data-stu-id="9e0cb-119">On Windows, the path may be relative to the directory in which the manifest file is located.</span></span>  <span data-ttu-id="9e0cb-120">В macOS путь должен быть абсолютным.</span><span class="sxs-lookup"><span data-stu-id="9e0cb-120">On macOS, the path must be absolute.</span></span>  <span data-ttu-id="9e0cb-121">Процесс хоста запустится с текущим набором каталогов и каталогом, содержащим двоичный файл узла.</span><span class="sxs-lookup"><span data-stu-id="9e0cb-121">The host process is started with the current directory set to the directory that contains the host binary.</span></span> <span data-ttu-id="9e0cb-122">Например, если для этого параметра задано значение `C:\Application\nm_host.exe` , двоичный код запускается с текущим каталогом `C:\Application\` .</span><span class="sxs-lookup"><span data-stu-id="9e0cb-122">For example if this parameter is set to `C:\Application\nm_host.exe`, the binary is started using the current directory `C:\Application\`.</span></span> |  
| `type` | <span data-ttu-id="9e0cb-123">Тип интерфейса, используемого для связи с собственным узлом сообщений.</span><span class="sxs-lookup"><span data-stu-id="9e0cb-123">Type of the interface used to communicate with the native messaging host.</span></span>  <span data-ttu-id="9e0cb-124">В настоящее время для этого параметра существует только одно возможное значение: `stdio` .</span><span class="sxs-lookup"><span data-stu-id="9e0cb-124">Currently there is only one possible value for this parameter: `stdio`.</span></span>  <span data-ttu-id="9e0cb-125">Это значение указывает на то, что хром должен использовать `stdin` и `stdout` взаимодействовать с узлом.</span><span class="sxs-lookup"><span data-stu-id="9e0cb-125">This value indicates that Chrome should use `stdin` and `stdout` to communicate with the host.</span></span> |  
| `allowed_origins` |  <span data-ttu-id="9e0cb-126">список расширений, которые должны иметь доступ к собственному узлу сообщений.</span><span class="sxs-lookup"><span data-stu-id="9e0cb-126">list of Extension that should access to the native messaging host.</span></span>  <span data-ttu-id="9e0cb-127">Чтобы разрешить собственное приложение определять и взаимодействовать с расширением надстроек Microsoft EDGE, установите `allowedorigins` для него значение `extension://[Microsoft-Catalog-extensionID]` в файле манифеста собственного узла сообщений.</span><span class="sxs-lookup"><span data-stu-id="9e0cb-127">To enable your Native Application identify and communicate with Microsoft Edge Addons Extension, set `allowedorigins` to `extension://[Microsoft-Catalog-extensionID]` in your native messaging host manifest file.</span></span> |  

1.  **<span data-ttu-id="9e0cb-128">Расположение собственного узла сообщений</span><span class="sxs-lookup"><span data-stu-id="9e0cb-128">Native messaging host location</span></span>**  
    
    <span data-ttu-id="9e0cb-129">Расположение файла манифеста зависит от платформы.</span><span class="sxs-lookup"><span data-stu-id="9e0cb-129">The location of the manifest file depends on the platform.</span></span>  
    
    <span data-ttu-id="9e0cb-130">В Windows файл манифеста может находиться в любом месте файловой системы.</span><span class="sxs-lookup"><span data-stu-id="9e0cb-130">On Windows, the manifest file may be located anywhere in the file system.</span></span>  <span data-ttu-id="9e0cb-131">Установщик приложения должен создать раздел реестра</span><span class="sxs-lookup"><span data-stu-id="9e0cb-131">The application installer must create registry key</span></span>  
    
    `HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application`  
    <span data-ttu-id="9e0cb-132">или</span><span class="sxs-lookup"><span data-stu-id="9e0cb-132">or</span></span>  
    `HKEY_CURRENT_USER\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application`<span data-ttu-id="9e0cb-133">,</span><span class="sxs-lookup"><span data-stu-id="9e0cb-133">,</span></span>  
    
    <span data-ttu-id="9e0cb-134">и задайте в качестве значения по умолчанию для этого ключа полный путь к файлу манифеста.</span><span class="sxs-lookup"><span data-stu-id="9e0cb-134">and set default value of that key to the full path to the manifest file.</span></span>  <span data-ttu-id="9e0cb-135">Например, с помощью следующей команды:</span><span class="sxs-lookup"><span data-stu-id="9e0cb-135">For example, using the following command:</span></span>  
    
    ```shell
    REG ADD "HKCU\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application" /ve /t REG_SZ /d "C:\path\to\nmh-manifest.json" /f
    ```  
    
    <span data-ttu-id="9e0cb-136">или с помощью следующего REG – файла:</span><span class="sxs-lookup"><span data-stu-id="9e0cb-136">or using the following .reg file:</span></span>  
    
    ```shell
    Windows Registry Editor Version 5.00
    [HKEY_CURRENT_USER\Software\Microsoft\Edge\NativeMessagingHosts\com.my_company.my_application]
    @="C:\\path\\to\\nmh-manifest.json"
    ```  
    
    <span data-ttu-id="9e0cb-137">Когда Microsoft Edge выполнит поиск собственных узлов сообщений, сначала запрашивается 32-разрядный реестр, а затем — 64-битовый реестр.</span><span class="sxs-lookup"><span data-stu-id="9e0cb-137">When Microsoft Edge looks for native messaging hosts, the 32-bit registry is queried first, then the 64-bit registry.</span></span>  

<span data-ttu-id="9e0cb-138">В macOS поисковые машинные системы систем обработки сообщений выполняются в определенном расположении, а машинные точки сообщений на уровне пользователя — в подкаталоге в каталоге профиля пользователя с именем `NativeMessagingHosts` .</span><span class="sxs-lookup"><span data-stu-id="9e0cb-138">On macOS, the system-wide native messaging hosts are looked up at a fixed location, while the user-level native messaging hosts are looked up in a subdirectory within the user profile directory called `NativeMessagingHosts`.</span></span>  

<span data-ttu-id="9e0cb-139">Microsoft EDGE на macOS \ (масштаб системы):</span><span class="sxs-lookup"><span data-stu-id="9e0cb-139">Microsoft Edge on macOS \(system-wide\) :</span></span>  
`/Library/Microsoft/Edge/NativeMessagingHosts/com.my_company.my_application.json`  

<span data-ttu-id="9e0cb-140">Microsoft EDGE на macOS \ (для определенного пользователя, путь по умолчанию):</span><span class="sxs-lookup"><span data-stu-id="9e0cb-140">Microsoft Edge on macOS \(user-specific, default path\):</span></span>  
`~/Library/Application Support/Microsoft Edge <ChannelName>/ NativeMessagingHosts/com.my_company.my_application.json`  

`<ChannelName>` <span data-ttu-id="9e0cb-141">может быть Канарские, dev или Beta.</span><span class="sxs-lookup"><span data-stu-id="9e0cb-141">may be Canary, Dev, or Beta.</span></span> <span data-ttu-id="9e0cb-142">Для стабильного канала `Microsoft Edge` следует использовать только `<ChannelName`>"не требуется.</span><span class="sxs-lookup"><span data-stu-id="9e0cb-142">For stable channel, only `Microsoft Edge` should be used, `<ChannelName`>\` is not required.</span></span>

<!-- image links -->  

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="9e0cb-143">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9e0cb-143">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="9e0cb-144">[Здесь](https://developer.chrome.com/extensions/nativeMessaging)будет найдена исходная страница.</span><span class="sxs-lookup"><span data-stu-id="9e0cb-144">The original page is found [here](https://developer.chrome.com/extensions/nativeMessaging).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="9e0cb-146">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9e0cb-146">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
