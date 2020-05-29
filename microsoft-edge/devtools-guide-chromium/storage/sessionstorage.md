---
title: Просмотр и изменение хранилища сеанса с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: d90d4bd7ec9b8927b713a744fb067cc5e96a1fe6
ms.sourcegitcommit: ad68bfbb355f6cfdaaf6612b77ea3985d4d6a58b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/01/2020
ms.locfileid: "10612083"
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





# <span data-ttu-id="2cf7c-103">Просмотр и изменение хранилища сеанса с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="2cf7c-103">View And Edit Session Storage With Microsoft Edge DevTools</span></span>   

  

<span data-ttu-id="2cf7c-104">В этом руководстве описано, как использовать [Microsoft Edge DevTools][MicrosoftEdgeDevTools] для просмотра, изменения и удаления [`sessionStorage`][MDNSessionStorage] пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="2cf7c-104">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view, edit, and delete [`sessionStorage`][MDNSessionStorage] key-value pairs.</span></span>  

## <span data-ttu-id="2cf7c-105">Просмотр ключей и значений sessionStorage</span><span class="sxs-lookup"><span data-stu-id="2cf7c-105">View sessionStorage keys and values</span></span>   

1.  <span data-ttu-id="2cf7c-106">Перейдите на вкладку **приложение** , чтобы открыть панель **приложения** .</span><span class="sxs-lookup"><span data-stu-id="2cf7c-106">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="2cf7c-107">Область **манифеста** отображается по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2cf7c-107">The **Manifest** pane is shown by default.</span></span>  
    
    > ##### <span data-ttu-id="2cf7c-108">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="2cf7c-108">Figure 1</span></span>  
    > <span data-ttu-id="2cf7c-109">Область «манифест»</span><span class="sxs-lookup"><span data-stu-id="2cf7c-109">The Manifest pane</span></span>  
    > ![Область «манифест»][ImageManifest]  

1.  <span data-ttu-id="2cf7c-111">Разверните меню **хранилище сеанса** .</span><span class="sxs-lookup"><span data-stu-id="2cf7c-111">Expand the **Session Storage** menu.</span></span>  
    
    > ##### <span data-ttu-id="2cf7c-112">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="2cf7c-112">Figure 2</span></span>  
    > <span data-ttu-id="2cf7c-113">Меню « **хранилище сеанса** »</span><span class="sxs-lookup"><span data-stu-id="2cf7c-113">The **Session Storage** Menu</span></span>  
    > ![Меню «хранилище сеанса»][ImageSessionStorageMenu]  

1.  <span data-ttu-id="2cf7c-115">Выберите домен, чтобы просмотреть пары "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="2cf7c-115">Select a domain to view the key-value pairs.</span></span>  
    
    > ##### <span data-ttu-id="2cf7c-116">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="2cf7c-116">Figure 3</span></span>  
    > <span data-ttu-id="2cf7c-117">SessionStorage пары "ключ-значение"</span><span class="sxs-lookup"><span data-stu-id="2cf7c-117">The sessionStorage key-value pairs</span></span>  
    > ![Пары "sessionStorage" "ключ-значение"][ImageSessionStorage]  

1.  <span data-ttu-id="2cf7c-119">Выделите строку таблицы, чтобы просмотреть ее значение в представлении под таблицей.</span><span class="sxs-lookup"><span data-stu-id="2cf7c-119">Select a row of the table to view the value in the viewer below the table.</span></span>  
    
    > ##### <span data-ttu-id="2cf7c-120">Рисунок4</span><span class="sxs-lookup"><span data-stu-id="2cf7c-120">Figure 4</span></span>  
    > <span data-ttu-id="2cf7c-121">Просмотр значения `x-sid` ключа</span><span class="sxs-lookup"><span data-stu-id="2cf7c-121">Viewing the value of the `x-sid` key</span></span>  
    > ![Просмотр значения ключа x-SID][ImageSessionStorageViewer]  

## <span data-ttu-id="2cf7c-123">Создание новой пары "ключ-значение" для sessionStorage</span><span class="sxs-lookup"><span data-stu-id="2cf7c-123">Create a new sessionStorage key-value pair</span></span>   

1.  <span data-ttu-id="2cf7c-124">[Просмотр `sessionStorage` пар "ключ-значение" домена](#view-sessionstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="2cf7c-124">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="2cf7c-125">Дважды щелкните пустую часть таблицы.</span><span class="sxs-lookup"><span data-stu-id="2cf7c-125">Double-click the empty part of the table.</span></span>  <span data-ttu-id="2cf7c-126">DevTools создает новую строку и нафокусирует указатель мыши на **ключевом** столбце.</span><span class="sxs-lookup"><span data-stu-id="2cf7c-126">DevTools creates a new row and focuses your cursor in the **Key** column.</span></span>  
    
    > ##### <span data-ttu-id="2cf7c-127">Рисунок 5</span><span class="sxs-lookup"><span data-stu-id="2cf7c-127">Figure 5</span></span>  
    > <span data-ttu-id="2cf7c-128">Пустая часть таблицы для двойного щелчка, чтобы создать новую пару ключ-значение.</span><span class="sxs-lookup"><span data-stu-id="2cf7c-128">The empty part of the table to double-click in order to create a new key-value pair</span></span>  
    > ![Пустая часть таблицы для двойного щелчка, чтобы создать новую пару ключ-значение.][ImageSessionStorageCreate]  

## <span data-ttu-id="2cf7c-130">Изменение ключей и значений sessionStorage</span><span class="sxs-lookup"><span data-stu-id="2cf7c-130">Edit sessionStorage keys or values</span></span>   

1.  <span data-ttu-id="2cf7c-131">[Просмотр `sessionStorage` пар "ключ-значение" домена](#view-sessionstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="2cf7c-131">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="2cf7c-132">Дважды щелкните ячейку в столбце " **раздел** " или " **значение** ", чтобы изменить этот раздел или значение.</span><span class="sxs-lookup"><span data-stu-id="2cf7c-132">Double-click a cell in the **Key** or **Value** column to edit that key or value.</span></span>  
    
    > ##### <span data-ttu-id="2cf7c-133">Рисунок6</span><span class="sxs-lookup"><span data-stu-id="2cf7c-133">Figure 6</span></span>  
    > <span data-ttu-id="2cf7c-134">Редактирование `sessionStorage` ключа</span><span class="sxs-lookup"><span data-stu-id="2cf7c-134">Editing a `sessionStorage` key</span></span>  
    > ![Редактирование ключа sessionStorage][ImageSessionStorageEdit]  

## <span data-ttu-id="2cf7c-136">Удаление пар ключ-значение sessionStorage</span><span class="sxs-lookup"><span data-stu-id="2cf7c-136">Delete sessionStorage key-value pairs</span></span>   

1.  <span data-ttu-id="2cf7c-137">[Просмотр `sessionStorage` пар "ключ-значение" домена](#view-sessionstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="2cf7c-137">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="2cf7c-138">Выберите пару "ключ-значение", которую вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="2cf7c-138">Select the key-value pair that you want to delete.</span></span>  <span data-ttu-id="2cf7c-139">DevTools выделит ее синей, чтобы показать, что она выбрана.</span><span class="sxs-lookup"><span data-stu-id="2cf7c-139">DevTools highlights it blue to indicate that it is selected.</span></span>  

1.  <span data-ttu-id="2cf7c-140">Нажмите клавишу `Delete` или выберите команду **Удалить выбранное** ![ Удаление ][ImageDeleteIcon] .</span><span class="sxs-lookup"><span data-stu-id="2cf7c-140">Press the `Delete` key or click **Delete Selected** ![Delete Selected][ImageDeleteIcon].</span></span>  

## <span data-ttu-id="2cf7c-141">Удаление всех пар ключ-значение sessionStorage для домена</span><span class="sxs-lookup"><span data-stu-id="2cf7c-141">Delete all sessionStorage key-value pairs for a domain</span></span>   

1.  <span data-ttu-id="2cf7c-142">[Просмотр `sessionStorage` пар "ключ-значение" домена](#view-sessionstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="2cf7c-142">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  

1.  <span data-ttu-id="2cf7c-143">Нажмите **Очистить все** ![ Очистить все ][ImageClearIcon] .</span><span class="sxs-lookup"><span data-stu-id="2cf7c-143">Select **Clear All** ![Clear All][ImageClearIcon].</span></span>  

## <span data-ttu-id="2cf7c-144">Взаимодействие с sessionStorage с помощью консоли</span><span class="sxs-lookup"><span data-stu-id="2cf7c-144">Interact with sessionStorage from the Console</span></span>   

<span data-ttu-id="2cf7c-145">Так как вы можете запустить JavaScript на **консоли**, и так как **консоль** имеет доступ к контекстам JavaScript на странице, можно взаимодействовать с `sessionStorage` ней из **консоли**.</span><span class="sxs-lookup"><span data-stu-id="2cf7c-145">Since you can run JavaScript in the **Console**, and since the **Console** has access to the JavaScript contexts of the page, it is possible to interact with `sessionStorage` from the **Console**.</span></span>  

1.  <span data-ttu-id="2cf7c-146">Используйте меню "контексты **JavaScript** " для изменения контекста JavaScript на **консоли** , если вы хотите получить доступ к `sessionStorage` парам "ключ-значение" домена, отличного от страницы, на которой вы являетесь.</span><span class="sxs-lookup"><span data-stu-id="2cf7c-146">Use the **JavaScript contexts** menu to change the JavaScript context of the **Console** if you want to access the `sessionStorage` key-value pairs of a domain other than the page you are on.</span></span>  
    
    > ##### <span data-ttu-id="2cf7c-147">Рисунок7</span><span class="sxs-lookup"><span data-stu-id="2cf7c-147">Figure 7</span></span>  
    > <span data-ttu-id="2cf7c-148">Изменение контекста JavaScript **консоли**</span><span class="sxs-lookup"><span data-stu-id="2cf7c-148">Changing the JavaScript context of the **Console**</span></span>  
    > ![Изменение контекста JavaScript консоли][ImageJSContext]  

1.  <span data-ttu-id="2cf7c-150">Выполняйте `sessionStorage` выражения на консоли так же, как и в JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2cf7c-150">Run your `sessionStorage` expressions in the Console, the same as you would in your JavaScript.</span></span>  
    
    > ##### <span data-ttu-id="2cf7c-151">Рисунок8</span><span class="sxs-lookup"><span data-stu-id="2cf7c-151">Figure 8</span></span>  
    > <span data-ttu-id="2cf7c-152">Взаимодействие с `sessionStorage` **консолью**</span><span class="sxs-lookup"><span data-stu-id="2cf7c-152">Interacting with `sessionStorage` from the **Console**</span></span>  
    > ![Взаимодействие с sessionStorage из консоли][ImageSessionStorageConsole]  

   

  

<!-- image links -->  

[ImageClearIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-icon.msft.png  
[ImageDeleteIcon]: /microsoft-edge/devtools-guide-chromium/media/delete-icon.msft.png  

[ImageManifest]: /microsoft-edge/devtools-guide-chromium/media/storage-application-manifest.msft.png "Рисунок 1: область манифеста"  
[ImageSessionStorageMenu]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-session-storage.msft.png "Рисунок 2: меню «хранилище сеанса»"  
[ImageSessionStorage]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-session-storage-domain.msft.png "Рисунок 3: пары "ключ-значение" sessionStorage"  
[ImageSessionStorageViewer]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-session-storage-domain-key-value-selected.msft.png "Рисунок 4: Просмотр значения ключа x-SID"  
[ImageSessionStorageCreate]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-session-storage-domain-key-value-new.msft.png "Рис. 5: пустая часть таблицы для двойного щелчка, чтобы создать новую пару ключ-значение."  
[ImageSessionStorageEdit]: /microsoft-edge/devtools-guide-chromium/media/storage-application-storage-session-storage-domain-key-value-edit.msft.png "Рисунок 6: Редактирование ключа sessionStorage"  
[ImageJSContext]: /microsoft-edge/devtools-guide-chromium/media/storage-console-domain-selection.msft.png "Рис. 7: изменение контекста JavaScript консоли"  
[ImageSessionStorageConsole]: /microsoft-edge/devtools-guide-chromium/media/storage-console-session-storage-keys.msft.png "Рисунок 8: взаимодействие с sessionStorage из консоли"  

<!-- links -->  

[MicrosoftEdgeDevTools]: /microsoft-edge/devtools-guide-chromium "Инструменты разработчика Microsoft EDGE (Chromium)"  

[MDNSessionStorage]: https://developer.mozilla.org/docs/Web/API/Window/sessionStorage "Window. sessionStorage | MDN"  

> [!NOTE]
> <span data-ttu-id="2cf7c-164">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2cf7c-164">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="2cf7c-165">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/storage/sessionstorage) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="2cf7c-165">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/sessionstorage) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="2cf7c-167">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2cf7c-167">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
