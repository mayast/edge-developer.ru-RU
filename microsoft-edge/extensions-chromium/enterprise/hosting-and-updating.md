---
description: Расширениям корпоративной документации для пограничного решения (Chromium).
title: Хранение и обновление
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, Разработка расширений, расширения браузера, надстройки, центр партнера, разработчик
ms.openlocfilehash: d918aec12e56daf66d13488d360a454d736031e8
ms.sourcegitcommit: d360e419b5f96f4f691cf7330b0d8dff9126f82e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015704"
---
# <span data-ttu-id="db701-104">Размещение и обновление веб-магазина</span><span class="sxs-lookup"><span data-stu-id="db701-104">Web Store Hosting and Updating</span></span>  

<span data-ttu-id="db701-105">Большинство расширений размещаются в [каталоге надстроек Microsoft Edge предварительной оценки \ (надстройки Microsoft Edge предварительной оценки \)][MicrosoftStoreExtensions] , чтобы лучше защитить пользователей от вредоносных расширений.</span><span class="sxs-lookup"><span data-stu-id="db701-105">Most Extensions are hosted in the [Microsoft Edge Insider Addons catalog \(Microsoft Edge Insider Addons\)][MicrosoftStoreExtensions] to best protect users from malicious Extensions.</span></span>  

## <span data-ttu-id="db701-106">Размещения</span><span class="sxs-lookup"><span data-stu-id="db701-106">Hosting</span></span>  

<span data-ttu-id="db701-107">Все расширения распространяются на пользователей в виде специального ZIP-файла с суффиксом. CRX.</span><span class="sxs-lookup"><span data-stu-id="db701-107">All Extensions are distributed to users as a special ZIP file with a .crx suffix.</span></span>  <span data-ttu-id="db701-108">Расширения, размещенные в надстройках Microsoft EDGE, загружаются в виде ZIP-файлов.</span><span class="sxs-lookup"><span data-stu-id="db701-108">Extensions hosted in the Microsoft Edge Addons are uploaded as .zip files.</span></span> <span data-ttu-id="db701-109">Процесс публикации автоматически преобразует ZIP-файл в CRX.</span><span class="sxs-lookup"><span data-stu-id="db701-109">The publishing process automatically converts the .zip into a .crx file.</span></span>  

<span data-ttu-id="db701-110">Существует два исключения для правила размещения надстроек Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="db701-110">There are two exceptions to the Microsoft Edge Addons hosting rule:</span></span>  

1.  <span data-ttu-id="db701-111">Расширения, распространяемые с помощью корпоративной политики.</span><span class="sxs-lookup"><span data-stu-id="db701-111">Extensions that are distributed through the Enterprise policy.</span></span>  
1.  <span data-ttu-id="db701-112">В режиме разработчика распакованные каталоги расширений на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="db701-112">Unpacked Extension directories from a local machine while in developer mode.</span></span>  

## <span data-ttu-id="db701-113">Обновление</span><span class="sxs-lookup"><span data-stu-id="db701-113">Updating</span></span>  

<span data-ttu-id="db701-114">Браузер Microsoft Edge периодически проверяет наличие новых версий установленных расширений и обновляет каждый из них без вмешательства пользователя.</span><span class="sxs-lookup"><span data-stu-id="db701-114">The Microsoft Edge browser periodically checks for new versions of installed Extensions and updates each without user intervention.</span></span>  

> [!NOTE]
> <span data-ttu-id="db701-115">Пошаговые инструкции по обновлению расширения в надстройках Microsoft Edge будут добавлены в план.</span><span class="sxs-lookup"><span data-stu-id="db701-115">Steps to update an Extension on Microsoft Edge Addons are planned be added.</span></span>  

<!-- image links -->

<!-- links -->  

[MicrosoftStoreExtensions]: https://microsoftedge.microsoft.com/insider-addons/category/EdgeExtensions "Расширения — надстройки для участников программы предварительной оценки Microsoft Edge"  

> [!NOTE]
> <span data-ttu-id="db701-117">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="db701-117">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="db701-118">[Здесь](https://developer.chrome.com/extensions/hosting)будет найдена исходная страница.</span><span class="sxs-lookup"><span data-stu-id="db701-118">The original page is found [here](https://developer.chrome.com/extensions/hosting).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="db701-120">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="db701-120">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
