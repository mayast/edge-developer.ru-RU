---
title: Просмотр и изменение локального хранилища с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 72aee823d3a3143ae7399c7057f3b606bd1078c3
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2020
ms.locfileid: "10983529"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  





# <span data-ttu-id="d1e1e-103">Просмотр и изменение локального хранилища с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="d1e1e-103">View and edit local storage with Microsoft Edge DevTools</span></span>   



<span data-ttu-id="d1e1e-104">В этом руководстве описано, как использовать [Microsoft Edge DevTools][MicrosoftEdgeDevTools] для просмотра, изменения и удаления пар ключ-значение [localStorage][MDNWindowsLocalStorage] .</span><span class="sxs-lookup"><span data-stu-id="d1e1e-104">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view, edit, and delete [localStorage][MDNWindowsLocalStorage] key-value pairs.</span></span>  

## <span data-ttu-id="d1e1e-105">Просмотр ключей и значений localStorage</span><span class="sxs-lookup"><span data-stu-id="d1e1e-105">View localStorage keys and values</span></span>   

1.  <span data-ttu-id="d1e1e-106">Перейдите на вкладку **приложение** , чтобы открыть панель **приложения** .</span><span class="sxs-lookup"><span data-stu-id="d1e1e-106">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="d1e1e-107">Область **манифеста** отображается по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d1e1e-107">The **Manifest** pane is shown by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="d1e1e-109">Область « **Манифест** »</span><span class="sxs-lookup"><span data-stu-id="d1e1e-109">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d1e1e-110">Разверните меню **Локальное хранилище** .</span><span class="sxs-lookup"><span data-stu-id="d1e1e-110">Expand the **Local Storage** menu.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage.msft.png" alt-text="Меню «локальное хранилище»" lightbox="../media/storage-application-local-storage.msft.png":::
       <span data-ttu-id="d1e1e-112">Меню « **Локальное хранилище** »</span><span class="sxs-lookup"><span data-stu-id="d1e1e-112">The **Local Storage** menu</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d1e1e-113">Выберите домен, чтобы просмотреть пары "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="d1e1e-113">Select a domain to view the key-value pairs.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-view-key-value.msft.png" alt-text="LocalStorage пары "ключ-значение" для https://www.bing.com домена" lightbox="../media/storage-application-local-storage-view-key-value.msft.png":::
       <span data-ttu-id="d1e1e-115">`localStorage`Пары "ключ-значение" для `https://www.bing.com` домена</span><span class="sxs-lookup"><span data-stu-id="d1e1e-115">The `localStorage` key-value pairs for the `https://www.bing.com` domain</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d1e1e-116">Выделите строку таблицы, чтобы просмотреть ее значение в представлении под таблицей.</span><span class="sxs-lookup"><span data-stu-id="d1e1e-116">Select a row of the table to view the value in the viewer below the table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-view-key-value-selected.msft.png" alt-text="Просмотр значения ключа eventLogQueue_Online" lightbox="../media/storage-application-local-storage-view-key-value-selected.msft.png":::
       <span data-ttu-id="d1e1e-118">Просмотр значения `eventLogQueue_Online` ключа</span><span class="sxs-lookup"><span data-stu-id="d1e1e-118">View the value of the `eventLogQueue_Online` key</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="d1e1e-119">Создание новой пары "ключ-значение" для localStorage</span><span class="sxs-lookup"><span data-stu-id="d1e1e-119">Create a new localStorage key-value pair</span></span>   

1.  <span data-ttu-id="d1e1e-120">[Просмотр `localStorage` пар "ключ-значение" домена](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="d1e1e-120">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="d1e1e-121">Дважды щелкните пустую часть таблицы.</span><span class="sxs-lookup"><span data-stu-id="d1e1e-121">Double-click the empty part of the table.</span></span>  <span data-ttu-id="d1e1e-122">DevTools создает новую строку и нафокусирует указатель мыши на **ключевом** столбце.</span><span class="sxs-lookup"><span data-stu-id="d1e1e-122">DevTools creates a new row and focuses your cursor in the **Key** column.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-new-key-value.msft.png" alt-text="Пустая часть таблицы для двойного щелчка, чтобы создать новую пару ключ-значение." lightbox="../media/storage-application-local-storage-new-key-value.msft.png":::
       <span data-ttu-id="d1e1e-124">Пустая часть таблицы для двойного щелчка, чтобы создать новую пару ключ-значение.</span><span class="sxs-lookup"><span data-stu-id="d1e1e-124">The empty part of the table to double-click in order to create a new key-value pair</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="d1e1e-125">Изменение ключей и значений localStorage</span><span class="sxs-lookup"><span data-stu-id="d1e1e-125">Edit localStorage keys or values</span></span>   

1.  <span data-ttu-id="d1e1e-126">[Просмотр `localStorage` пар "ключ-значение" домена](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="d1e1e-126">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="d1e1e-127">Дважды щелкните ячейку в столбце " **раздел** " или " **значение** ", чтобы изменить этот раздел или значение.</span><span class="sxs-lookup"><span data-stu-id="d1e1e-127">Double-click a cell in the **Key** or **Value** column to edit that key or value.</span></span>  
    
    :::image type="complex" source="../media/storage-application-local-storage-edit-key-value.msft.png" alt-text="Изменение ключа localStorage" lightbox="../media/storage-application-local-storage-edit-key-value.msft.png":::
       <span data-ttu-id="d1e1e-129">Изменение `localStorage` ключа</span><span class="sxs-lookup"><span data-stu-id="d1e1e-129">Edit a `localStorage` key</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="d1e1e-130">Удаление пар ключ-значение localStorage</span><span class="sxs-lookup"><span data-stu-id="d1e1e-130">Delete localStorage key-value pairs</span></span>   

1.  <span data-ttu-id="d1e1e-131">[Просмотр `localStorage` пар "ключ-значение" домена](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="d1e1e-131">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="d1e1e-132">Выберите пару "ключ-значение", которую вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="d1e1e-132">Select the key-value pair that you want to delete.</span></span>  <span data-ttu-id="d1e1e-133">DevTools выделит ее синей, чтобы показать, что она выбрана.</span><span class="sxs-lookup"><span data-stu-id="d1e1e-133">DevTools highlights it blue to indicate that it is selected.</span></span>  
1.  <span data-ttu-id="d1e1e-134">Нажмите клавишу `Delete` или нажмите кнопку **Удалить выделенные** \ ( ![ Удалить выбранные \ ][ImageDeleteIcon] ).</span><span class="sxs-lookup"><span data-stu-id="d1e1e-134">Press the `Delete` key or click **Delete Selected** \(![Delete Selected][ImageDeleteIcon]\).</span></span>  
    
## <span data-ttu-id="d1e1e-135">Удаление всех `localStorage` пар "ключ-значение" для домена</span><span class="sxs-lookup"><span data-stu-id="d1e1e-135">Delete all `localStorage` key-value pairs for a domain</span></span>   

1.  <span data-ttu-id="d1e1e-136">[Просмотр `localStorage` пар "ключ-значение" домена](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="d1e1e-136">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="d1e1e-137">Нажмите **Очистить все** \ ( ![ Очистить все ][ImageClearIcon] \).</span><span class="sxs-lookup"><span data-stu-id="d1e1e-137">Select **Clear All** \(![Clear All][ImageClearIcon]\).</span></span>  
    
## <span data-ttu-id="d1e1e-138">Взаимодействие с localStorage с помощью консоли</span><span class="sxs-lookup"><span data-stu-id="d1e1e-138">Interact with localStorage from the Console</span></span>   

<span data-ttu-id="d1e1e-139">Так как вы можете запускать JavaScript на **консоли**, а так как у **консоли** есть доступ к контекстам JavaScript страницы, взаимодействие с `localStorage` **консолью**возможно.</span><span class="sxs-lookup"><span data-stu-id="d1e1e-139">Since you are able to run JavaScript in the **Console**, and since the **Console** has access to the JavaScript contexts of the page, it is possible to interact with `localStorage` from the **Console**.</span></span>  

1.  <span data-ttu-id="d1e1e-140">Используйте меню "контексты **JavaScript** " для изменения контекста JavaScript на **консоли** , если требуется получить доступ к `localStorage` парам "ключ-значение" домена, отличного от отображаемой страницы.</span><span class="sxs-lookup"><span data-stu-id="d1e1e-140">Use the **JavaScript contexts** menu to change the JavaScript context of the **Console** if you want to access the `localStorage` key-value pairs of a domain other than the page that is displayed.</span></span>  
    
    :::image type="complex" source="../media/storage-console-local-storage.msft.png" alt-text="Изменение контекста JavaScript консоли" lightbox="../media/storage-console-local-storage.msft.png":::
       <span data-ttu-id="d1e1e-142">Изменение контекста JavaScript консоли</span><span class="sxs-lookup"><span data-stu-id="d1e1e-142">Change the JavaScript context of the Console</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="d1e1e-143">Выполняйте `localStorage` выражения на консоли так же, как и в JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d1e1e-143">Run your `localStorage` expressions in the Console, the same as you do in your JavaScript.</span></span>  
    
    :::image type="complex" source="../media/storage-console-local-storage-interaction.msft.png" alt-text="Взаимодействие с localStorage с помощью консоли" lightbox="../media/storage-console-local-storage-interaction.msft.png":::
       <span data-ttu-id="d1e1e-145">Взаимодействие с `localStorage` **консолью**</span><span class="sxs-lookup"><span data-stu-id="d1e1e-145">Interact with `localStorage` from the **Console**</span></span>  
    :::image-end:::  
    
<!--  
 


-->  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Инструменты разработчика Microsoft EDGE (Chromium) | Документы Microsoft"  

[MDNWindowsLocalStorage]: https://developer.mozilla.org/docs/Web/API/Window/localStorage "Window. localStorage | MDN"  

> [!NOTE]
> <span data-ttu-id="d1e1e-148">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d1e1e-148">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="d1e1e-149">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="d1e1e-149">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="d1e1e-151">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="d1e1e-151">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
