---
title: Просмотр и изменение хранилища сеанса с помощью Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: d0631f69a082a2a73c51e4359c21cf94636d665e
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2020
ms.locfileid: "10983585"
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





# <span data-ttu-id="2d46d-103">Просмотр и изменение хранилища сеанса с помощью Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="2d46d-103">View and edit Session Storage with Microsoft Edge DevTools</span></span>   

  

<span data-ttu-id="2d46d-104">В этом руководстве описано, как использовать [Microsoft Edge DevTools][MicrosoftEdgeDevTools] для просмотра, изменения и удаления [`sessionStorage`][MDNSessionStorage] пар "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="2d46d-104">This guide shows you how to use [Microsoft Edge DevTools][MicrosoftEdgeDevTools] to view, edit, and delete [`sessionStorage`][MDNSessionStorage] key-value pairs.</span></span>  

## <span data-ttu-id="2d46d-105">Просмотр ключей и значений sessionStorage</span><span class="sxs-lookup"><span data-stu-id="2d46d-105">View sessionStorage keys and values</span></span>   

1.  <span data-ttu-id="2d46d-106">Перейдите на вкладку **приложение** , чтобы открыть панель **приложения** .</span><span class="sxs-lookup"><span data-stu-id="2d46d-106">Select the **Application** tab to open the **Application** panel.</span></span>  <span data-ttu-id="2d46d-107">Область **манифеста** отображается по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2d46d-107">The **Manifest** pane is shown by default.</span></span>  
    
    :::image type="complex" source="../media/storage-application-manifest.msft.png" alt-text="Область «манифест»" lightbox="../media/storage-application-manifest.msft.png":::
       <span data-ttu-id="2d46d-109">Область « **Манифест** »</span><span class="sxs-lookup"><span data-stu-id="2d46d-109">The **Manifest** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2d46d-110">Разверните меню **хранилище сеанса** .</span><span class="sxs-lookup"><span data-stu-id="2d46d-110">Expand the **Session Storage** menu.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage.msft.png" alt-text="Меню «хранилище сеанса»" lightbox="../media/storage-application-storage-session-storage.msft.png":::
       <span data-ttu-id="2d46d-112">Меню « **хранилище сеанса** »</span><span class="sxs-lookup"><span data-stu-id="2d46d-112">The **Session Storage** Menu</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2d46d-113">Выберите домен, чтобы просмотреть пары "ключ-значение".</span><span class="sxs-lookup"><span data-stu-id="2d46d-113">Select a domain to view the key-value pairs.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain.msft.png" alt-text="Пары "sessionStorage" "ключ-значение"" lightbox="../media/storage-application-storage-session-storage-domain.msft.png":::
       <span data-ttu-id="2d46d-115">`sessionStorage`Пары "ключ-значение"</span><span class="sxs-lookup"><span data-stu-id="2d46d-115">The `sessionStorage` key-value pairs</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2d46d-116">Выделите строку таблицы, чтобы просмотреть ее значение в представлении под таблицей.</span><span class="sxs-lookup"><span data-stu-id="2d46d-116">Select a row of the table to view the value in the viewer below the table.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-selected.msft.png" alt-text="Просмотр значения ключа x-SID" lightbox="../media/storage-application-storage-session-storage-domain-key-value-selected.msft.png":::
       <span data-ttu-id="2d46d-118">Просмотр значения `x-sid` ключа</span><span class="sxs-lookup"><span data-stu-id="2d46d-118">View the value of the `x-sid` key</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="2d46d-119">Создание новой пары "ключ-значение" для sessionStorage</span><span class="sxs-lookup"><span data-stu-id="2d46d-119">Create a new sessionStorage key-value pair</span></span>   

1.  <span data-ttu-id="2d46d-120">[Просмотр `sessionStorage` пар "ключ-значение" домена](#view-sessionstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="2d46d-120">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="2d46d-121">Дважды щелкните пустую часть таблицы.</span><span class="sxs-lookup"><span data-stu-id="2d46d-121">Double-click the empty part of the table.</span></span>  <span data-ttu-id="2d46d-122">DevTools создает новую строку и нафокусирует указатель мыши на **ключевом** столбце.</span><span class="sxs-lookup"><span data-stu-id="2d46d-122">DevTools creates a new row and focuses your cursor in the **Key** column.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-new.msft.png" alt-text="Пустая часть таблицы для двойного щелчка, чтобы создать новую пару ключ-значение." lightbox="../media/storage-application-storage-session-storage-domain-key-value-new.msft.png":::
       <span data-ttu-id="2d46d-124">Пустая часть таблицы для двойного щелчка, чтобы создать новую пару ключ-значение.</span><span class="sxs-lookup"><span data-stu-id="2d46d-124">The empty part of the table to double-click in order to create a new key-value pair</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="2d46d-125">Изменение ключей и значений sessionStorage</span><span class="sxs-lookup"><span data-stu-id="2d46d-125">Edit sessionStorage keys or values</span></span>   

1.  <span data-ttu-id="2d46d-126">[Просмотр `sessionStorage` пар "ключ-значение" домена](#view-sessionstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="2d46d-126">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="2d46d-127">Дважды щелкните ячейку в столбце " **раздел** " или " **значение** ", чтобы изменить этот раздел или значение.</span><span class="sxs-lookup"><span data-stu-id="2d46d-127">Double-click a cell in the **Key** or **Value** column to edit that key or value.</span></span>  
    
    :::image type="complex" source="../media/storage-application-storage-session-storage-domain-key-value-edit.msft.png" alt-text="Изменение ключа sessionStorage" lightbox="../media/storage-application-storage-session-storage-domain-key-value-edit.msft.png":::
       <span data-ttu-id="2d46d-129">Изменение `sessionStorage` ключа</span><span class="sxs-lookup"><span data-stu-id="2d46d-129">Edit a `sessionStorage` key</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="2d46d-130">Удаление пар ключ-значение sessionStorage</span><span class="sxs-lookup"><span data-stu-id="2d46d-130">Delete sessionStorage key-value pairs</span></span>   

1.  <span data-ttu-id="2d46d-131">[Просмотр `sessionStorage` пар "ключ-значение" домена](#view-sessionstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="2d46d-131">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="2d46d-132">Выберите пару "ключ-значение", которую вы хотите удалить.</span><span class="sxs-lookup"><span data-stu-id="2d46d-132">Select the key-value pair that you want to delete.</span></span>  <span data-ttu-id="2d46d-133">DevTools выделит ее синей, чтобы показать, что она выбрана.</span><span class="sxs-lookup"><span data-stu-id="2d46d-133">DevTools highlights it blue to indicate that it is selected.</span></span>  
1.  <span data-ttu-id="2d46d-134">Нажмите клавишу `Delete` или нажмите кнопку **Удалить выделенные** \ ( ![ Удалить выбранные \ ][ImageDeleteIcon] ).</span><span class="sxs-lookup"><span data-stu-id="2d46d-134">Press the `Delete` key or click **Delete Selected** \(![Delete Selected][ImageDeleteIcon]\).</span></span>  
    
## <span data-ttu-id="2d46d-135">Удаление всех пар ключ-значение sessionStorage для домена</span><span class="sxs-lookup"><span data-stu-id="2d46d-135">Delete all sessionStorage key-value pairs for a domain</span></span>   

1.  <span data-ttu-id="2d46d-136">[Просмотр `sessionStorage` пар "ключ-значение" домена](#view-sessionstorage-keys-and-values).</span><span class="sxs-lookup"><span data-stu-id="2d46d-136">[View the `sessionStorage` key-value pairs of a domain](#view-sessionstorage-keys-and-values).</span></span>  
1.  <span data-ttu-id="2d46d-137">Нажмите **Очистить все** \ ( ![ Очистить все ][ImageClearIcon] \).</span><span class="sxs-lookup"><span data-stu-id="2d46d-137">Select **Clear All** \(![Clear All][ImageClearIcon]\).</span></span>  
    
## <span data-ttu-id="2d46d-138">Взаимодействие с sessionStorage с помощью консоли</span><span class="sxs-lookup"><span data-stu-id="2d46d-138">Interact with sessionStorage from the Console</span></span>   

<span data-ttu-id="2d46d-139">Так как вы можете запустить JavaScript на **консоли**, и так как **консоль** имеет доступ к контекстам JavaScript на странице, можно взаимодействовать с `sessionStorage` ней из **консоли**.</span><span class="sxs-lookup"><span data-stu-id="2d46d-139">Since you can run JavaScript in the **Console**, and since the **Console** has access to the JavaScript contexts of the page, it is possible to interact with `sessionStorage` from the **Console**.</span></span>  

1.  <span data-ttu-id="2d46d-140">Используйте меню "контексты **JavaScript** " для изменения контекста JavaScript на **консоли** , если вы хотите получить доступ к `sessionStorage` парам "ключ-значение" домена, отличного от страницы, на которой вы являетесь.</span><span class="sxs-lookup"><span data-stu-id="2d46d-140">Use the **JavaScript contexts** menu to change the JavaScript context of the **Console** if you want to access the `sessionStorage` key-value pairs of a domain other than the page you are on.</span></span>  
    
    :::image type="complex" source="../media/storage-console-domain-selection.msft.png" alt-text="Изменение контекста JavaScript консоли" lightbox="../media/storage-console-domain-selection.msft.png":::
       <span data-ttu-id="2d46d-142">Изменение контекста JavaScript консоли</span><span class="sxs-lookup"><span data-stu-id="2d46d-142">Change the JavaScript context of the Console</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="2d46d-143">Выполняйте `sessionStorage` выражения на консоли так же, как и в JavaScript.</span><span class="sxs-lookup"><span data-stu-id="2d46d-143">Run your `sessionStorage` expressions in the Console, the same as you would in your JavaScript.</span></span>  
    
    :::image type="complex" source="../media/storage-console-session-storage-keys.msft.png" alt-text="Взаимодействие с sessionStorage с помощью консоли" lightbox="../media/storage-console-session-storage-keys.msft.png":::
       <span data-ttu-id="2d46d-145">Взаимодействие с `sessionStorage` **консолью**</span><span class="sxs-lookup"><span data-stu-id="2d46d-145">Interact with `sessionStorage` from the **Console**</span></span>  
    :::image-end:::  
    
<!--  
   

  
-->  

<!-- image links -->  

[ImageClearIcon]: ../media/clear-icon.msft.png  
[ImageDeleteIcon]: ../media/delete-icon.msft.png  

<!-- links -->  

[MicrosoftEdgeDevTools]: ../../devtools-guide-chromium.md "Инструменты разработчика Microsoft EDGE (Chromium) | Документы Microsoft"  

[MDNSessionStorage]: https://developer.mozilla.org/docs/Web/API/Window/sessionStorage "Window. sessionStorage | MDN"  

> [!NOTE]
> <span data-ttu-id="2d46d-148">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2d46d-148">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="2d46d-149">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/storage/sessionstorage) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="2d46d-149">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/storage/sessionstorage) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="2d46d-151">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2d46d-151">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
