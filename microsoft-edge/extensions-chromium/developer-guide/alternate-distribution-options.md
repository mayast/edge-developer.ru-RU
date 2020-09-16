---
description: Процесс распространения расширения по механизму, отличному от проверенных хранилищ
title: Альтернативный способ распространения расширения
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, Разработка расширений, расширения браузера, надстройки, центр партнера, разработчик
ms.openlocfilehash: e28a84fd75ad1ac0be2000a22c26371ca73d0293
ms.sourcegitcommit: d360e419b5f96f4f691cf7330b0d8dff9126f82e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015697"
---
# <span data-ttu-id="d25ae-104">Альтернативный способ распространения расширения</span><span class="sxs-lookup"><span data-stu-id="d25ae-104">Alternate Method of Distributing Extension</span></span>  

<span data-ttu-id="d25ae-105">Если вы являетесь разработчиком, которому нужно распространить расширение в рамках процесса установки другого программного обеспечения или администратор сети, которому нужно распространить расширение по всей Организации, Microsoft EDGE поддерживает следующие методы установки расширения:</span><span class="sxs-lookup"><span data-stu-id="d25ae-105">If you are a developer who wants to distribute an Extension as part of the installation process for other software, or a network admin that want to distribute an Extension throughout their organization, Microsoft Edge supports the following Extension installation methods:</span></span>  

*   **<span data-ttu-id="d25ae-106">Использование реестра Windows \ (только для Windows)</span><span class="sxs-lookup"><span data-stu-id="d25ae-106">Using the Windows registry \(Windows only\)</span></span>**  

<span data-ttu-id="d25ae-107">Microsoft EDGE поддерживает установку расширения, размещенного на `update_URL` .</span><span class="sxs-lookup"><span data-stu-id="d25ae-107">Microsoft Edge supports installing an Extension hosted at an `update_URL`.</span></span>  <span data-ttu-id="d25ae-108">В Windows `update_URL` необходимо указывать на каталог надстроек Microsoft Edge \ (надстройки Microsoft EDGE), где должно быть размещено расширение.</span><span class="sxs-lookup"><span data-stu-id="d25ae-108">On Windows, the `update_URL` must point to the Microsoft Edge Addons catalog \(Microsoft Edge Addons\) where the Extension must be hosted.</span></span>  

> [!NOTE]
> <span data-ttu-id="d25ae-109">Внешняя Установка расширения с помощью JSON-файла настроек для macOS</span><span class="sxs-lookup"><span data-stu-id="d25ae-109">External installation of Extension via a preferences json file for macOS</span></span> <!--and Linux--> <span data-ttu-id="d25ae-110">еще не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="d25ae-110">are not supported yet.</span></span>  <span data-ttu-id="d25ae-111">Поддержка этих функций скоро будет доступна.</span><span class="sxs-lookup"><span data-stu-id="d25ae-111">This feature support will soon be available.</span></span>

## <span data-ttu-id="d25ae-112">Использование реестра Windows</span><span class="sxs-lookup"><span data-stu-id="d25ae-112">Using the Windows registry</span></span>  

<span data-ttu-id="d25ae-113">Сначала опубликуйте расширение в надстройках Microsoft EDGE или упакуйте файл a. CRX и убедитесь, что он успешно установлен.</span><span class="sxs-lookup"><span data-stu-id="d25ae-113">First, publish the Extension in the Microsoft Edge Addons, or package a .crx file and make sure that it installs successfully.</span></span>  

<span data-ttu-id="d25ae-114">Для установки расширения через реестр в Windows можно выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="d25ae-114">The steps to install Extension via registry in windows are:</span></span>  

*   <span data-ttu-id="d25ae-115">Найдите или создайте в реестре следующий раздел:</span><span class="sxs-lookup"><span data-stu-id="d25ae-115">Find or create the following key in the registry:</span></span>  
    *   <span data-ttu-id="d25ae-116">32 — разрядная версия Windows:</span><span class="sxs-lookup"><span data-stu-id="d25ae-116">32-bit Windows:</span></span>  `HKEY_LOCAL_MACHINE\Software\Microsoft\Edge\Extensions`  
    *   <span data-ttu-id="d25ae-117">64 — разрядная версия Windows:</span><span class="sxs-lookup"><span data-stu-id="d25ae-117">64-bit Windows:</span></span>  `HKEY_LOCAL_MACHINE\Software\Wow6432Node\Microsoft\Edge\Extensions`  
*   <span data-ttu-id="d25ae-118">Создайте новый ключ \ (Folder \) в разделе Extensions с тем же именем, что и идентификатор расширения, (например, `aaaaaaaaaabbbbbbbbbbcccccccccc` \).</span><span class="sxs-lookup"><span data-stu-id="d25ae-118">Create a new key \(folder\) under the Extensions key with the same name as the ID of your Extension \(for example, `aaaaaaaaaabbbbbbbbbbcccccccccc`\).</span></span>  
*   <span data-ttu-id="d25ae-119">В ключе расширения создайте свойство `update_url` и задайте для него значение: `https://edge.microsoft.com/extensionwebstorebase/v1/crx` , \ (это указывает на CRX расширения в надстройках Microsoft Edge \).</span><span class="sxs-lookup"><span data-stu-id="d25ae-119">In your Extension key, create a property, `update_url`, and set it to the value: `https://edge.microsoft.com/extensionwebstorebase/v1/crx`,  \(this points to the crx of your extension in the Microsoft Edge Addons\).</span></span> <span data-ttu-id="d25ae-120">Если вы хотите установить расширение из веб-магазина Chrome, укажите URL-адрес веб-магазина Chrome Update `https://clients2.google.com/service/update2/crx` .</span><span class="sxs-lookup"><span data-stu-id="d25ae-120">If you want to install an extension from the Chrome Web Store, please provide the Chrome Web Store update URL, `https://clients2.google.com/service/update2/crx`.</span></span>  
    
    ```javascript
    {
        "update_url": "https://edge.microsoft.com/extensionwebstorebase/v1/crx"
    }
    ```  
    
*   <span data-ttu-id="d25ae-121">Запустите браузер и перейдите к нему, и `edge://extensions` вы увидите расширение в списке.</span><span class="sxs-lookup"><span data-stu-id="d25ae-121">Launch the browser and go to `edge://extensions`; you should see the extension listed.</span></span>  

## <span data-ttu-id="d25ae-122">Обновление и удаление</span><span class="sxs-lookup"><span data-stu-id="d25ae-122">Updating and uninstalling</span></span>  

<span data-ttu-id="d25ae-123">Microsoft Edge проверяет записи метаданных в реестре каждый раз при запуске браузера и вносит необходимые изменения во внешние расширения.</span><span class="sxs-lookup"><span data-stu-id="d25ae-123">Microsoft Edge scans the metadata entries in the registry each time the browser starts, and makes any necessary changes to the installed external extensions.</span></span>  

<span data-ttu-id="d25ae-124">Чтобы обновить расширение до новой версии, обновите файл и обновите версию в реестре.</span><span class="sxs-lookup"><span data-stu-id="d25ae-124">To update your extension to a new version, update the file, and then update the version in the registry.</span></span>  

<span data-ttu-id="d25ae-125">Чтобы удалить расширение (например, если оно удалено), удалите файл параметров \ ( `aaaaaaaaaabbbbbbbbbbcccccccccc.json` \) или метаданные из реестра.</span><span class="sxs-lookup"><span data-stu-id="d25ae-125">To uninstall your extension \(for example, if your software is uninstalled\), remove your preference file \(`aaaaaaaaaabbbbbbbbbbcccccccccc.json`\) or the metadata from the registry.</span></span>  

<!-- image links -->  

<!-- links -->  

> [!NOTE]
> <span data-ttu-id="d25ae-126">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d25ae-126">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="d25ae-127">[Здесь](https://developer.chrome.com/apps/external_extensions)будет найдена исходная страница.</span><span class="sxs-lookup"><span data-stu-id="d25ae-127">The original page is found [here](https://developer.chrome.com/apps/external_extensions).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="d25ae-129">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d25ae-129">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies
