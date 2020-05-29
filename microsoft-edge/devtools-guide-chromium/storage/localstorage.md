---
title: Просмотр и изменение локального хранилища с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: f7e187662aec8231f2cc4e99baab1b4b8e2048ad
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612013"
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





# <span data-ttu-id="aa45d-103">Просмотр и изменение локального хранилища с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="aa45d-103">View And Edit Local Storage With Microsoft Edge DevTools</span></span>   



<span data-ttu-id="aa45d-104">В этом руководстве описано, как использовать [Microsoft Edge DevTools][MicrosoftEdgeDevTools] для просмотра, изменения и удаления [`localStorage`][MDNWindowsLocalStorage] пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="aa45d-104">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view, edit, and delete [`localStorage`][MDNWindowsLocalStorage] key-value pairs.</span></span>  

## <span data-ttu-id="aa45d-105">Просмотр ключей и значений localStorage</span><span class="sxs-lookup"><span data-stu-id="aa45d-105">View localStorage keys and values</span></span>   

1.  <span data-ttu-id="aa45d-106">Перейдите на вкладку **приложение** , чтобы открыть панель **приложения** .</span><span class="sxs-lookup"><span data-stu-id="aa45d-106">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="aa45d-107">Область **манифеста** отображается по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="aa45d-107">The **Manifest** pane is shown by default.</span></span>  
    
    > ##### <span data-ttu-id="aa45d-108">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="aa45d-108">Figure 1</span></span>  
    > <span data-ttu-id="aa45d-109">Область «манифест»</span><span class="sxs-lookup"><span data-stu-id="aa45d-109">The Manifest pane</span></span>  
    > ![Область «манифест»][ImageManifest]  

1.  <span data-ttu-id="aa45d-111">Разверните меню **Локальное хранилище** .</span><span class="sxs-lookup"><span data-stu-id="aa45d-111">Expand the **Local Storage** menu.</span></span>  
    
    > ##### <span data-ttu-id="aa45d-112">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="aa45d-112">Figure 2</span></span>  
    > <span data-ttu-id="aa45d-113">В меню " **Локальное хранилище** " отображаются два домена: `https://business.bing.com` и</span><span class="sxs-lookup"><span data-stu-id="aa45d-113">The **Local Storage** menu shows two domains: `https://business.bing.com` and</span></span> `https://www.bing.com`  
    > ![Меню «локальное хранилище»][ImageLocalStorageMenu]  

1.  <span data-ttu-id="aa45d-115">Выберите домен, чтобы просмотреть пары "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="aa45d-115">Select a domain to view the key-value pairs.</span></span>  
    
    > ##### <span data-ttu-id="aa45d-116">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="aa45d-116">Figure 3</span></span>  
    > <span data-ttu-id="aa45d-117">`localStorage`Пары "ключ-значение" для `https://www.bing.com` домена</span><span class="sxs-lookup"><span data-stu-id="aa45d-117">The `localStorage` key-value pairs for the `https://www.bing.com` domain</span></span>  
    > ![LocalStorage пары "ключ-значение" для https://www.bing.com домена][ImageLocalStorage]  

1.  <span data-ttu-id="aa45d-119">Выделите строку таблицы, чтобы просмотреть ее значение в представлении под таблицей.</span><span class="sxs-lookup"><span data-stu-id="aa45d-119">Select a row of the table to view the value in the viewer below the table.</span></span>  
    
    > ##### <span data-ttu-id="aa45d-120">Рисунок4</span><span class="sxs-lookup"><span data-stu-id="aa45d-120">Figure 4</span></span>  
    > <span data-ttu-id="aa45d-121">Просмотр значения `eventLogQueue_Online` ключа</span><span class="sxs-lookup"><span data-stu-id="aa45d-121">Viewing the value of the `eventLogQueue_Online` key</span></span>  
    > ![Просмотр значения ключа eventLogQueue_Online][ImageLocalStorageViewer]  

## <span data-ttu-id="aa45d-123">Создание новой `localStorage` пары "ключ-значение"</span><span class="sxs-lookup"><span data-stu-id="aa45d-123">Create a new `localStorage` key-value pair</span></span>   

1.  <span data-ttu-id="aa45d-124">[Просмотр `localStorage` пар "ключ-значение" домена](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="aa45d-124">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="aa45d-125">Дважды щелкните пустую часть таблицы.</span><span class="sxs-lookup"><span data-stu-id="aa45d-125">Double-click the empty part of the table.</span></span>  <span data-ttu-id="aa45d-126">DevTools создает новую строку и нафокусирует указатель мыши на **ключевом** столбце.</span><span class="sxs-lookup"><span data-stu-id="aa45d-126">DevTools creates a new row and focuses your cursor in the **Key** column.</span></span>  
    
    > ##### <span data-ttu-id="aa45d-127">Рисунок 5</span><span class="sxs-lookup"><span data-stu-id="aa45d-127">Figure 5</span></span>  
    > <span data-ttu-id="aa45d-128">Пустая часть таблицы для двойного щелчка, чтобы создать новую пару ключ-значение.</span><span class="sxs-lookup"><span data-stu-id="aa45d-128">The empty part of the table to double-click in order to create a new key-value pair</span></span>  
    > ![Пустая часть таблицы для двойного щелчка, чтобы создать новую пару ключ-значение.][ImageLocalStorageCreate]  

## <span data-ttu-id="aa45d-130">Изменение `localStorage` ключей и значений</span><span class="sxs-lookup"><span data-stu-id="aa45d-130">Edit `localStorage` keys or values</span></span>   

1.  <span data-ttu-id="aa45d-131">[Просмотр `localStorage` пар "ключ-значение" домена](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="aa45d-131">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="aa45d-132">Дважды щелкните ячейку в столбце " **раздел** " или " **значение** ", чтобы изменить этот раздел или значение.</span><span class="sxs-lookup"><span data-stu-id="aa45d-132">Double-click a cell in the **Key** or **Value** column to edit that key or value.</span></span>  
    
    > ##### <span data-ttu-id="aa45d-133">Рисунок6</span><span class="sxs-lookup"><span data-stu-id="aa45d-133">Figure 6</span></span>  
    > <span data-ttu-id="aa45d-134">Редактирование `localStorage` ключа</span><span class="sxs-lookup"><span data-stu-id="aa45d-134">Editing a `localStorage` key</span></span>  
    > ![Редактирование ключа localStorage][ImageLocalStorageEdit]  

## <span data-ttu-id="aa45d-136">Удаление `localStorage` пар "ключ-значение"</span><span class="sxs-lookup"><span data-stu-id="aa45d-136">Delete `localStorage` key-value pairs</span></span>   

1.  <span data-ttu-id="aa45d-137">[Просмотр `localStorage` пар "ключ-значение" домена](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="aa45d-137">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="aa45d-138">Выберите пару "ключ-значение", которую вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="aa45d-138">Select the key-value pair that you want to delete.</span></span>  <span data-ttu-id="aa45d-139">DevTools выделит ее синей, чтобы показать, что она выбрана.</span><span class="sxs-lookup"><span data-stu-id="aa45d-139">DevTools highlights it blue to indicate that it is selected.</span></span>  

1.  <span data-ttu-id="aa45d-140">Нажмите клавишу `Delete` или выберите команду **Удалить выбранное** ![ Удаление ][ImageDeleteIcon] .</span><span class="sxs-lookup"><span data-stu-id="aa45d-140">Press the `Delete` key or click **Delete Selected** ![Delete Selected][ImageDeleteIcon].</span></span>  

## <span data-ttu-id="aa45d-141">Удаление всех `localStorage` пар "ключ-значение" для домена</span><span class="sxs-lookup"><span data-stu-id="aa45d-141">Delete all `localStorage` key-value pairs for a domain</span></span>   

1.  <span data-ttu-id="aa45d-142">[Просмотр `localStorage` пар "ключ-значение" домена](#view-localstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="aa45d-142">[View the `localStorage` key-value pairs of a domain](#view-localstorage-keys-and-values).</span></span>  

1.  <span data-ttu-id="aa45d-143">Нажмите **Очистить все** ![ Очистить все ][ImageClearIcon] .</span><span class="sxs-lookup"><span data-stu-id="aa45d-143">Select **Clear All** ![Clear All][ImageClearIcon].</span></span>  

## <span data-ttu-id="aa45d-144">Взаимодействие с `localStorage` консолью</span><span class="sxs-lookup"><span data-stu-id="aa45d-144">Interact with `localStorage` from the Console</span></span>   

<span data-ttu-id="aa45d-145">Так как вы можете запускать JavaScript на **консоли**, а так как у **консоли** есть доступ к контекстам JavaScript страницы, взаимодействие с `localStorage` **консолью**возможно.</span><span class="sxs-lookup"><span data-stu-id="aa45d-145">Since you are able to run JavaScript in the **Console**, and since the **Console** has access to the JavaScript contexts of the page, it is possible to interact with `localStorage` from the **Console**.</span></span>  

1.  <span data-ttu-id="aa45d-146">Используйте меню "контексты **JavaScript** " для изменения контекста JavaScript на **консоли** , если требуется получить доступ к `localStorage` парам "ключ-значение" домена, отличного от отображаемой страницы.</span><span class="sxs-lookup"><span data-stu-id="aa45d-146">Use the **JavaScript contexts** menu to change the JavaScript context of the **Console** if you want to access the `localStorage` key-value pairs of a domain other than the page that is displayed.</span></span>  
    
    > ##### <span data-ttu-id="aa45d-147">Рисунок7</span><span class="sxs-lookup"><span data-stu-id="aa45d-147">Figure 7</span></span>  
    > <span data-ttu-id="aa45d-148">Изменение контекста JavaScript **консоли**</span><span class="sxs-lookup"><span data-stu-id="aa45d-148">Changing the JavaScript context of the **Console**</span></span>  
    > ![Изменение контекста JavaScript консоли][ImageJSContext]  

1.  <span data-ttu-id="aa45d-150">Выполняйте `localStorage` выражения на консоли так же, как и в JavaScript.</span><span class="sxs-lookup"><span data-stu-id="aa45d-150">Run your `localStorage` expressions in the Console, the same as you do in your JavaScript.</span></span>  
    
    > ##### <span data-ttu-id="aa45d-151">Рисунок8</span><span class="sxs-lookup"><span data-stu-id="aa45d-151">Figure 8</span></span>  
    > <span data-ttu-id="aa45d-152">Взаимодействие с `localStorage` **консолью**</span><span class="sxs-lookup"><span data-stu-id="aa45d-152">Interacting with `localStorage` from the **Console**</span></span>  
    > ![Взаимодействие с localStorage из консоли][ImageLocalStorageConsole]  

 



<!-- image links -->  

[ImageClearIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-icon.msft.png  
[ImageDeleteIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-icon.msft.png  

[ImageManifest]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest.msft.png "Рисунок 1: область манифеста"  
[ImageLocalStorageMenu]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage.msft.png "Рисунок 2: меню "локальное хранилище""  
[ImageLocalStorage]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage-view-key-value.msft.png "Рисунок 3: localStorage пары "ключ-значение" для https://www.bing.com домена"  
[ImageLocalStorageViewer]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage-view-key-value-selected.msft.png "Рисунок 4: Просмотр значения ключа eventLogQueue_Online"  
[ImageLocalStorageCreate]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage-new-key-value.msft.png "Рис. 5: пустая часть таблицы для двойного щелчка, чтобы создать новую пару ключ-значение."  
[ImageLocalStorageEdit]: /microsoft-edge/devtools-guide-chromium/media/storage-application-local-storage-edit-key-value.msft.png "Рисунок 6: Редактирование ключа localStorage"  
[ImageJSContext]: /microsoft-edge/devtools-guide-chromium/media/storage-console-local-storage.msft.png "Рис. 7: изменение контекста JavaScript консоли"  
[ImageLocalStorageConsole]: /microsoft-edge/devtools-guide-chromium/media/storage-console-local-storage-interaction.msft.png "Рисунок 8: взаимодействие с localStorage из консоли"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Инструменты разработчика Microsoft EDGE (Chromium)"  

[MDNWindowsLocalStorage]: https://developer.mozilla.org/docs/Web/API/Window/localStorage "Window. localStorage | MDN"  

> [!NOTE]
> <span data-ttu-id="aa45d-164">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="aa45d-164">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="aa45d-165">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="aa45d-165">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/localstorage) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="aa45d-167">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="aa45d-167">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
