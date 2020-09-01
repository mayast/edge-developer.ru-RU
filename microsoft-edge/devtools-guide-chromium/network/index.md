---
title: Проверка активности сети в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: cca9a45dae5ee845a219ef3f29c54a99e1ee904a
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2020
ms.locfileid: "10985691"
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





# <span data-ttu-id="31d7f-103">Проверка активности сети в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="31d7f-103">Inspect network activity in Microsoft Edge DevTools</span></span>   



<span data-ttu-id="31d7f-104">В этом практическом занятии описаны некоторые из наиболее часто используемых функций DevTools, связанных с проанализом активности сети для страницы.</span><span class="sxs-lookup"><span data-stu-id="31d7f-104">This is a hands-on tutorial of some of the most commonly-used DevTools features related to inspecting network activity for a page.</span></span>  

<span data-ttu-id="31d7f-105">Для просмотра функциональных возможностей используйте [ссылку сетевая ссылка][DevtoolsNetworkReference] .</span><span class="sxs-lookup"><span data-stu-id="31d7f-105">See [Network Reference][DevtoolsNetworkReference] if you want to browse features instead.</span></span>  

<!--TODO: This entire section needs a Microsoft Edge DevTools re-write  -->

<!-- Read on, or watch the video version of this tutorial:  -->  

<!--
> [!VIDEO embed/e1gAyQuIFQo]  
-->

## <span data-ttu-id="31d7f-106">Когда следует использовать панель "сеть"</span><span class="sxs-lookup"><span data-stu-id="31d7f-106">When to use the Network panel</span></span>   

<span data-ttu-id="31d7f-107">В общем случае следует использовать панель "сеть", чтобы убедиться в том, что ресурсы загружаются или загружаются должным образом.</span><span class="sxs-lookup"><span data-stu-id="31d7f-107">In general, use the Network panel when you need to make sure that resources are being downloaded or uploaded as expected.</span></span>  <span data-ttu-id="31d7f-108">Наиболее распространенными вариантами использования панели "сеть" являются:</span><span class="sxs-lookup"><span data-stu-id="31d7f-108">The most common use cases for the Network panel are:</span></span>  

*   <span data-ttu-id="31d7f-109">Убедитесь в том, что ресурсы действительно отправляются или загружаются вообще.</span><span class="sxs-lookup"><span data-stu-id="31d7f-109">Making sure that resources are actually being uploaded or downloaded at all.</span></span>  
*   <span data-ttu-id="31d7f-110">Проверка свойств отдельного ресурса, например HTTP-заголовков, содержимого, размера и т. д.</span><span class="sxs-lookup"><span data-stu-id="31d7f-110">Inspecting the properties of an individual resource, such as the HTTP headers, content, size, and so on.</span></span>  
    
<span data-ttu-id="31d7f-111">Если вы ищете способы повышения быстродействия загрузки страниц, **не** начинайте с панели "сеть".</span><span class="sxs-lookup"><span data-stu-id="31d7f-111">If you are looking for ways to improve page load performance, **do not** start with the Network panel.</span></span>  <span data-ttu-id="31d7f-112">Существует множество типов проблем с производительностью нагрузки, не связанных с работой сети.</span><span class="sxs-lookup"><span data-stu-id="31d7f-112">There are many types of load performance issues that are not related to network activity.</span></span>  <span data-ttu-id="31d7f-113">Начните работу с панели аудита, так как она содержит рекомендации по улучшению страницы.</span><span class="sxs-lookup"><span data-stu-id="31d7f-113">Start with the Audits panel because it gives you targeted suggestions on how to improve your page.</span></span>  <span data-ttu-id="31d7f-114">Ознакомьтесь со [скоростью оптимизации веб-сайта][DevtoolsSpeedGetStarted].</span><span class="sxs-lookup"><span data-stu-id="31d7f-114">See [Optimize Website Speed][DevtoolsSpeedGetStarted].</span></span>  

## <span data-ttu-id="31d7f-115">Открытие панели "сеть"</span><span class="sxs-lookup"><span data-stu-id="31d7f-115">Open the Network panel</span></span>   

<span data-ttu-id="31d7f-116">Чтобы максимально эффективно пользоваться этим учебником, откройте демонстрацию и ознакомьтесь с функциями на странице Demo.</span><span class="sxs-lookup"><span data-stu-id="31d7f-116">To get the most out of this tutorial, open up the demo and try out the features on the demo page.</span></span>  

1.  <span data-ttu-id="31d7f-117">Откройте [демонстрацию Приступая к работе][GlitchNetworkGetStarted].</span><span class="sxs-lookup"><span data-stu-id="31d7f-117">Open the [Get Started Demo][GlitchNetworkGetStarted].</span></span>  
    
    :::image type="complex" source="../media/network-glitch-inspect-network-activity-demo.msft.png" alt-text="Демонстрация" lightbox="../media/network-glitch-inspect-network-activity-demo.msft.png":::
       <span data-ttu-id="31d7f-119">Демонстрация</span><span class="sxs-lookup"><span data-stu-id="31d7f-119">The demo</span></span>  
    :::image-end:::  
    
    <!--You may prefer to move the demo to a separate window.  -->  
    
    <!--
    :::image type="complex" source="../media/network-tutorial/windows.msft.png" alt-text="The demo in one window and this tutorial in a different window" lightbox="../media/network-tutorial/windows.msft.png":::
       The demo in one window and this tutorial in a different window  
    :::image-end:::  
    -->
    
1.  <span data-ttu-id="31d7f-120">[Откройте DevTools][DevToolsOpen] , нажав клавиши `Control` + `Shift` + `J` \ (Windows \) или `Command` + `Option` + `J` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="31d7f-120">[Open DevTools][DevToolsOpen] by pressing `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\).</span></span>  <span data-ttu-id="31d7f-121">Откроется панель **консоли** .</span><span class="sxs-lookup"><span data-stu-id="31d7f-121">The **Console** panel opens.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-console.msft.png" alt-text="На консоли" lightbox="../media/network-glitch-console.msft.png":::
       <span data-ttu-id="31d7f-123">На **консоли**</span><span class="sxs-lookup"><span data-stu-id="31d7f-123">The **Console**</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="31d7f-124">Вы можете [закрепить DevTools в нижней части окна][DevToolsCustomizePlacement].</span><span class="sxs-lookup"><span data-stu-id="31d7f-124">You may prefer to [dock DevTools to the bottom of your window][DevToolsCustomizePlacement].</span></span>  
    
    :::image type="complex" source="../media/network-glitch-console-bottom.msft.png" alt-text="DevTools закреплено в нижней части окна" lightbox="../media/network-glitch-console-bottom.msft.png":::
       <span data-ttu-id="31d7f-126">DevTools закреплено в нижней части окна</span><span class="sxs-lookup"><span data-stu-id="31d7f-126">DevTools docked to the bottom of the window</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="31d7f-127">Откройте вкладку **сеть** .  Откроется панель Network (сеть).</span><span class="sxs-lookup"><span data-stu-id="31d7f-127">Select the **Network** tab.  The Network panel opens.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-bottom.msft.png" alt-text="DevTools закреплено в нижней части окна" lightbox="../media/network-glitch-network-bottom.msft.png":::
       <span data-ttu-id="31d7f-129">DevTools закреплено в нижней части окна</span><span class="sxs-lookup"><span data-stu-id="31d7f-129">DevTools docked to the bottom of the window</span></span>  
    :::image-end:::  
    
<span data-ttu-id="31d7f-130">Прямо сейчас панель Network (сеть) пуста.</span><span class="sxs-lookup"><span data-stu-id="31d7f-130">Right now the Network panel is empty.</span></span>  <span data-ttu-id="31d7f-131">DevTools только записывает сетевые активности после того, как вы откроете ее и не произошел никаких сетевых операций после того, как вы открыли DevTools.</span><span class="sxs-lookup"><span data-stu-id="31d7f-131">DevTools only logs network activity after you open it and no network activity has occurred since you opened DevTools.</span></span>  

## <span data-ttu-id="31d7f-132">Регистрация активности в сети</span><span class="sxs-lookup"><span data-stu-id="31d7f-132">Log network activity</span></span>   

<span data-ttu-id="31d7f-133">Чтобы просмотреть сетевую активность, которая вызывается страницей, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="31d7f-133">To view the network activity that a page causes:</span></span>  

1.  <span data-ttu-id="31d7f-134">Перезагрузите страницу.</span><span class="sxs-lookup"><span data-stu-id="31d7f-134">Reload the page.</span></span>  <span data-ttu-id="31d7f-135">На панели Network (сеть) регистрируются все сетевые активности в **журнале сети**.</span><span class="sxs-lookup"><span data-stu-id="31d7f-135">The Network panel logs all network activity in the **Network Log**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network.msft.png" alt-text="Журнал сети" lightbox="../media/network-glitch-network.msft.png":::
       <span data-ttu-id="31d7f-137">**Журнал сети**</span><span class="sxs-lookup"><span data-stu-id="31d7f-137">The **Network Log**</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="31d7f-138">Каждая строка **журнала сети** представляет ресурс.</span><span class="sxs-lookup"><span data-stu-id="31d7f-138">Each row of the **Network Log** represents a resource.</span></span>  <span data-ttu-id="31d7f-139">По умолчанию ресурсы указаны в хронологическом порядке.</span><span class="sxs-lookup"><span data-stu-id="31d7f-139">By default the resources are listed chronologically.</span></span>  <span data-ttu-id="31d7f-140">Самый верхний ресурс обычно является основным HTML-документом.</span><span class="sxs-lookup"><span data-stu-id="31d7f-140">The top resource is usually the main HTML document.</span></span>  <span data-ttu-id="31d7f-141">Самый нижний ресурс — это тот, который запрашивался последним.</span><span class="sxs-lookup"><span data-stu-id="31d7f-141">The bottom resource is whatever was requested last.</span></span>  
    
    <span data-ttu-id="31d7f-142">Каждый столбец представляет сведения о ресурсе.</span><span class="sxs-lookup"><span data-stu-id="31d7f-142">Each column represents information about a resource.</span></span>  <span data-ttu-id="31d7f-143">На приведенном выше рисунке отображаются столбцы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="31d7f-143">In the previous figure the default columns are displayed.</span></span>  

    *   <span data-ttu-id="31d7f-144">**Состояние**.</span><span class="sxs-lookup"><span data-stu-id="31d7f-144">**Status**.</span></span>  <span data-ttu-id="31d7f-145">Код состояния HTTP для ответа.</span><span class="sxs-lookup"><span data-stu-id="31d7f-145">The HTTP status code for response.</span></span>  
    *   <span data-ttu-id="31d7f-146">**Тип**.</span><span class="sxs-lookup"><span data-stu-id="31d7f-146">**Type**.</span></span>  <span data-ttu-id="31d7f-147">Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="31d7f-147">The resource type.</span></span>  
    *   <span data-ttu-id="31d7f-148">**Инициатор**.</span><span class="sxs-lookup"><span data-stu-id="31d7f-148">**Initiator**.</span></span>  <span data-ttu-id="31d7f-149">Причина запроса ресурса.</span><span class="sxs-lookup"><span data-stu-id="31d7f-149">The cause of the resource request.</span></span>  <span data-ttu-id="31d7f-150">При выборе ссылки в столбце инициатора осуществляется переход к исходному коду, вызвавшему запрос.</span><span class="sxs-lookup"><span data-stu-id="31d7f-150">Selecting a link in the Initiator column takes you to the source code that caused the request.</span></span>  
    *   <span data-ttu-id="31d7f-151">**Time (время**).</span><span class="sxs-lookup"><span data-stu-id="31d7f-151">**Time**.</span></span>  <span data-ttu-id="31d7f-152">Продолжительность запроса.</span><span class="sxs-lookup"><span data-stu-id="31d7f-152">The duration of the request.</span></span>  
    *   <span data-ttu-id="31d7f-153">**Каскадом**.</span><span class="sxs-lookup"><span data-stu-id="31d7f-153">**Waterfall**.</span></span>  <span data-ttu-id="31d7f-154">Графическое представление различных стадий запроса.</span><span class="sxs-lookup"><span data-stu-id="31d7f-154">A graphical representation of the different stages of the request.</span></span>  <span data-ttu-id="31d7f-155">Наведите указатель мыши на Каскад, чтобы увидеть разбивку.</span><span class="sxs-lookup"><span data-stu-id="31d7f-155">Hover over a Waterfall to see a breakdown.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="31d7f-156">Диаграмма, расположенная над сетевым журналом, называется обзором.</span><span class="sxs-lookup"><span data-stu-id="31d7f-156">The graph above the Network Log is called the Overview.</span></span>  <span data-ttu-id="31d7f-157">Вы не будете использовать граф обзора в этом учебнике, поэтому вы можете скрыть его.</span><span class="sxs-lookup"><span data-stu-id="31d7f-157">You will not use the Overview graph in this tutorial, so you may hide it.</span></span>  <span data-ttu-id="31d7f-158">Ознакомьтесь [со статьей скрыть область "Общие сведения"][DevtoolsReferenceHideOverview].</span><span class="sxs-lookup"><span data-stu-id="31d7f-158">See [Hide the Overview pane][DevtoolsReferenceHideOverview].</span></span>
    
1.  <span data-ttu-id="31d7f-159">После открытия DevTools записывает в журнал сети активность сети.</span><span class="sxs-lookup"><span data-stu-id="31d7f-159">After you open DevTools, it records network activity in the Network Log.</span></span>  
    <span data-ttu-id="31d7f-160">Чтобы продемонстрировать это, сначала ознакомьтесь с нижней частью **журнала сети** и запомните о том, что последнее действие будет заглянуть в эту оценку.</span><span class="sxs-lookup"><span data-stu-id="31d7f-160">To demonstrate this, first look at the bottom of the **Network Log** and make a mental note of the last activity.</span></span>  
1.  <span data-ttu-id="31d7f-161">Теперь нажмите кнопку " **получить данные** " в демонстрационной версии.</span><span class="sxs-lookup"><span data-stu-id="31d7f-161">Now, select the **Get Data** button in the demo.</span></span>  
1.  <span data-ttu-id="31d7f-162">Снова посмотрите на нижнюю часть **сетевого журнала** .</span><span class="sxs-lookup"><span data-stu-id="31d7f-162">Look at the bottom of the **Network Log** again.</span></span>  <span data-ttu-id="31d7f-163">Вы должны увидеть новый ресурс под названием "" `getstarted.json` .</span><span class="sxs-lookup"><span data-stu-id="31d7f-163">You should see a new resource called `getstarted.json`.</span></span>  <span data-ttu-id="31d7f-164">Нажатие кнопки " **получить данные** " привела к тому, что страница запрашивает этот файл.</span><span class="sxs-lookup"><span data-stu-id="31d7f-164">Selecting the **Get Data** button caused the page to request this file.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-new-resource.msft.png" alt-text="Новый ресурс в сетевом журнале" lightbox="../media/network-glitch-network-new-resource.msft.png":::
       <span data-ttu-id="31d7f-166">Новый ресурс в **сетевом журнале**</span><span class="sxs-lookup"><span data-stu-id="31d7f-166">A new resource in the **Network Log**</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="31d7f-167">Показать дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="31d7f-167">Show more information</span></span>   

<span data-ttu-id="31d7f-168">Столбцы сетевого журнала можно настраивать.</span><span class="sxs-lookup"><span data-stu-id="31d7f-168">The columns of the Network Log are configurable.</span></span>  <span data-ttu-id="31d7f-169">Столбцы, которые вы не используете, могут быть скрыты.</span><span class="sxs-lookup"><span data-stu-id="31d7f-169">You may hide columns that you are not using.</span></span>  
<span data-ttu-id="31d7f-170">Кроме того, существует множество столбцов, которые по умолчанию скрыты, что может оказаться полезным.</span><span class="sxs-lookup"><span data-stu-id="31d7f-170">There are also many columns that are hidden by default which you may find useful.</span></span>  

1.  <span data-ttu-id="31d7f-171">Щелкните правой кнопкой мыши заголовок таблицы журнала сети и выберите команду **Domain (домен**).</span><span class="sxs-lookup"><span data-stu-id="31d7f-171">Right-click the header of the Network Log table and select **Domain**.</span></span>  <span data-ttu-id="31d7f-172">Теперь отображается домен каждого ресурса.</span><span class="sxs-lookup"><span data-stu-id="31d7f-172">The domain of each resource is now shown.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-edit-column.msft.png" alt-text="Включение столбца Domain (домен)" lightbox="../media/network-glitch-network-edit-column.msft.png":::
       <span data-ttu-id="31d7f-174">Включение столбца Domain (домен)</span><span class="sxs-lookup"><span data-stu-id="31d7f-174">Enable the Domain column</span></span>  
    :::image-end:::  
    
    > [!TIP]
    > <span data-ttu-id="31d7f-175">Просмотр полного URL-адреса ресурса при наведении указателя мыши на ячейку в столбце **имя** .</span><span class="sxs-lookup"><span data-stu-id="31d7f-175">See the full URL of a resource by hovering over the cell in the **Name** column.</span></span>  
    
## <span data-ttu-id="31d7f-176">Имитация медленных подключений к сети</span><span class="sxs-lookup"><span data-stu-id="31d7f-176">Simulate a slower network connection</span></span>   

<span data-ttu-id="31d7f-177">Сетевое подключение компьютера, используемого для создания сайтов, скорее всего быстрее, чем сетевые подключения мобильных устройств ваших пользователей.</span><span class="sxs-lookup"><span data-stu-id="31d7f-177">The network connection of the computer that you use to build sites is probably faster than the network connections of the mobile devices of your users.</span></span>  <span data-ttu-id="31d7f-178">Перетаскивая страницу, вы получите более общее представление о том, как долго страница будет загружаться на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="31d7f-178">By throttling the page, you get a better idea of how long a page takes to load on a mobile device.</span></span>  

1.  <span data-ttu-id="31d7f-179">Выберите раскрывающийся список **регулирования** , для которого по умолчанию установлено значение в **сети** .</span><span class="sxs-lookup"><span data-stu-id="31d7f-179">Select the **Throttling** dropdown, which is set to **Online** by default.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-throttling.msft.png" alt-text="Включение регулирования" lightbox="../media/network-glitch-network-throttling.msft.png":::
       <span data-ttu-id="31d7f-181">Включение регулирования</span><span class="sxs-lookup"><span data-stu-id="31d7f-181">Enable throttling</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="31d7f-182">Выберите **медленное 3G**.</span><span class="sxs-lookup"><span data-stu-id="31d7f-182">Select **Slow 3G**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-throttling-slow-3g.msft.png" alt-text="Выбор медленной сети 3G" lightbox="../media/network-glitch-network-throttling-slow-3g.msft.png":::
       <span data-ttu-id="31d7f-184">Выбор медленной сети 3G</span><span class="sxs-lookup"><span data-stu-id="31d7f-184">Select Slow 3G</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="31d7f-185">Нажмите кнопку **перезагрузить** ![ ][ImageRefreshIcon] , а затем выберите **пустой кэш и принудительную перезагрузку**.</span><span class="sxs-lookup"><span data-stu-id="31d7f-185">Long-press **Reload** \(![Reload][ImageRefreshIcon]\) and then select **Empty Cache And Hard Reload**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-empty-cache-and-hard-reset.msft.png" alt-text="Пустой кэш и окончательная перезагрузка" lightbox="../media/network-glitch-empty-cache-and-hard-reset.msft.png":::
       **<span data-ttu-id="31d7f-187">Пустой кэш и окончательная перезагрузка</span><span class="sxs-lookup"><span data-stu-id="31d7f-187">Empty Cache And Hard Reload</span></span>**  
    :::image-end:::  
    
    <span data-ttu-id="31d7f-188">При повторном посещении браузер обычно обслуживает некоторые файлы из [кэша][MDNHTTPCache], что ускоряет загрузку страницы.</span><span class="sxs-lookup"><span data-stu-id="31d7f-188">On repeat visits, the browser usually serves some files from the [cache][MDNHTTPCache], which speeds up the page load.</span></span>  <span data-ttu-id="31d7f-189">**Пустой кэш, и при принудительной перезагрузке** браузер перейдет в сеть для всех ресурсов.</span><span class="sxs-lookup"><span data-stu-id="31d7f-189">**Empty Cache And Hard Reload** forces the browser to go the network for all resources.</span></span>  <span data-ttu-id="31d7f-190">Это полезно, если вы хотите узнать, как в первый раз происходит загрузка страницы посетителем.</span><span class="sxs-lookup"><span data-stu-id="31d7f-190">This is helpful when you want to see how a first-time visitor experiences a page load.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="31d7f-191">**Пустой кэш и рабочий процесс повторной загрузки** доступны только в том случае, если открыт DevTools.</span><span class="sxs-lookup"><span data-stu-id="31d7f-191">The **Empty Cache And Hard Reload** workflow is only available when DevTools is open.</span></span>  
    
## <span data-ttu-id="31d7f-192">Захват снимков экрана</span><span class="sxs-lookup"><span data-stu-id="31d7f-192">Capture screenshots</span></span>   

<span data-ttu-id="31d7f-193">С помощью снимков экрана можно увидеть, как страница была найдена во время загрузки.</span><span class="sxs-lookup"><span data-stu-id="31d7f-193">Screenshots let you see how a page looked over time while it was loading.</span></span>  

1.  <span data-ttu-id="31d7f-194">Выберите \ ( ![ Параметры сети ][ImageSettingsIcon] \) и установите флажок **захватить снимки экрана** .</span><span class="sxs-lookup"><span data-stu-id="31d7f-194">Select \(![Network settings][ImageSettingsIcon]\) and select the **Capture screenshots** checkbox.</span></span>
1.  <span data-ttu-id="31d7f-195">Снова загрузите страницу с помощью **пустого кэша и окончательной повторной загрузки** .</span><span class="sxs-lookup"><span data-stu-id="31d7f-195">Reload the page again via the **Empty Cache And Hard Reload** workflow.</span></span>  <span data-ttu-id="31d7f-196">Если вам нужно напоминание о том, как это сделать, ознакомьтесь [с](#simulate-a-slower-network-connection) разрешениями.</span><span class="sxs-lookup"><span data-stu-id="31d7f-196">See [Simulate a slower connection](#simulate-a-slower-network-connection) if you need a reminder on how to do this.</span></span>  
    <span data-ttu-id="31d7f-197">В области снимков экрана представлены эскизы того, как страница рассмотрелась на разных этапах процесса загрузки.</span><span class="sxs-lookup"><span data-stu-id="31d7f-197">The Screenshots pane provides thumbnails of how the page looked at various points during the loading process.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots.msft.png" alt-text="Снимки экрана загрузки страницы" lightbox="../media/network-glitch-network-screenshots.msft.png":::
       <span data-ttu-id="31d7f-199">Снимки экрана загрузки страницы</span><span class="sxs-lookup"><span data-stu-id="31d7f-199">Screenshots of the page load</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="31d7f-200">Выберите первый эскиз.</span><span class="sxs-lookup"><span data-stu-id="31d7f-200">Select the first thumbnail.</span></span>  <span data-ttu-id="31d7f-201">DevTools показывает, какая сетевая активность происходила в данный момент времени.</span><span class="sxs-lookup"><span data-stu-id="31d7f-201">DevTools shows you what network activity was occurring at that moment in time.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-screenshots-first.msft.png" alt-text="Сетевая активность, происходящий на первом снимке экрана" lightbox="../media/network-glitch-network-screenshots-first.msft.png":::
       <span data-ttu-id="31d7f-203">Сетевая активность, происходящий на первом снимке экрана</span><span class="sxs-lookup"><span data-stu-id="31d7f-203">The network activity that was happening during the first screenshot</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="31d7f-204">Нажмите кнопку \ ( ![ Параметры сети ][ImageSettingsIcon] \) еще раз и снимите флажок **захватить снимки экрана** , чтобы закрыть область снимки экрана.</span><span class="sxs-lookup"><span data-stu-id="31d7f-204">Select \(![Network settings][ImageSettingsIcon]\) again and deselect the **Capture screenshots** checkbox to close the Screenshots pane.</span></span>
1.  <span data-ttu-id="31d7f-205">Повторно загрузите страницу.</span><span class="sxs-lookup"><span data-stu-id="31d7f-205">Reload the page again.</span></span>  
    
## <span data-ttu-id="31d7f-206">Проверка сведений о ресурсе</span><span class="sxs-lookup"><span data-stu-id="31d7f-206">Inspect the details of the resource</span></span>   

<span data-ttu-id="31d7f-207">Выберите ресурс, чтобы получить дополнительные сведения о нем.</span><span class="sxs-lookup"><span data-stu-id="31d7f-207">Select a resource to learn more information about it.</span></span>  <span data-ttu-id="31d7f-208">Попробуйте вот так:</span><span class="sxs-lookup"><span data-stu-id="31d7f-208">Try it now:</span></span>  

1.  <span data-ttu-id="31d7f-209">Выберите `getstarted.html` .</span><span class="sxs-lookup"><span data-stu-id="31d7f-209">Select `getstarted.html`.</span></span>  <span data-ttu-id="31d7f-210">Показана вкладка " **заголовки** ".</span><span class="sxs-lookup"><span data-stu-id="31d7f-210">The **Headers** tab is shown.</span></span>  <span data-ttu-id="31d7f-211">Используйте эту вкладку для проверки заголовков HTTP.</span><span class="sxs-lookup"><span data-stu-id="31d7f-211">Use this tab to inspect HTTP headers.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-headers.msft.png" alt-text="Вкладка "заголовки"" lightbox="../media/network-glitch-network-resources-headers.msft.png":::
       <span data-ttu-id="31d7f-213">Вкладка " **заголовки** "</span><span class="sxs-lookup"><span data-stu-id="31d7f-213">The **Headers** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="31d7f-214">Откройте вкладку **Предварительный просмотр** .  Отобразится основной рендеринг HTML-кода.</span><span class="sxs-lookup"><span data-stu-id="31d7f-214">Select the **Preview** tab.  A basic rendering of the HTML is shown.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-preview.msft.png" alt-text="Вкладка "предварительный просмотр"" lightbox="../media/network-glitch-network-resources-preview.msft.png":::
       <span data-ttu-id="31d7f-216">Вкладка " **Предварительный просмотр** "</span><span class="sxs-lookup"><span data-stu-id="31d7f-216">The **Preview** tab</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="31d7f-217">Эта вкладка полезна, если API возвращает код ошибки в HTML.</span><span class="sxs-lookup"><span data-stu-id="31d7f-217">This tab is helpful when an API returns an error code in HTML.</span></span>  <span data-ttu-id="31d7f-218">Возможно, вам будет проще прочитать обработанный HTML, чем исходный HTML-код или просматривает изображения.</span><span class="sxs-lookup"><span data-stu-id="31d7f-218">You may find it easier to read the rendered HTML than the HTML source code, or when you inspect images.</span></span>  

1.  <span data-ttu-id="31d7f-219">Откройте вкладку **ответ** .  Отобразится исходный код HTML.</span><span class="sxs-lookup"><span data-stu-id="31d7f-219">Select the **Response** tab.  The HTML source code is shown.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-response.msft.png" alt-text="Вкладка "ответ"" lightbox="../media/network-glitch-network-resources-response.msft.png":::
       <span data-ttu-id="31d7f-221">Вкладка " **ответ** "</span><span class="sxs-lookup"><span data-stu-id="31d7f-221">The **Response** tab</span></span>  
    :::image-end:::  
    
    > [!TIP]
    > <span data-ttu-id="31d7f-222">Когда файл minified, при нажатии кнопки **Формат** \ ( ![ Формат ][ImageFormatIcon] \) в нижней части вкладки **ответа** повторно форматирует содержимое файла для чтения.</span><span class="sxs-lookup"><span data-stu-id="31d7f-222">When a file is minified, selecting the **Format** \(![Format][ImageFormatIcon]\) button at the bottom of the **Response** tab re-formats the contents of the file for readability.</span></span>  
    
1.  <span data-ttu-id="31d7f-223">Откройте вкладку **время** .  Показана сетевая подразделение активности для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="31d7f-223">Select the **Timing** tab.  A breakdown of the network activity for this resource is shown.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-timing.msft.png" alt-text="Вкладка время" lightbox="../media/network-glitch-network-resources-timing.msft.png":::
       <span data-ttu-id="31d7f-225">Вкладка **время**</span><span class="sxs-lookup"><span data-stu-id="31d7f-225">The **Timing** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="31d7f-226">**Close** ![ ][ImageCloseIcon] Чтобы снова просмотреть журнал сети, нажмите кнопку Закрыть, а затем — закрыть.</span><span class="sxs-lookup"><span data-stu-id="31d7f-226">Select **Close** \(![Close][ImageCloseIcon]\) to view the Network Log again.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-resources-close-tabs.msft.png" alt-text="Кнопка "Закрыть"" lightbox="../media/network-glitch-network-resources-close-tabs.msft.png":::
       <span data-ttu-id="31d7f-228">Кнопка " **Закрыть** "</span><span class="sxs-lookup"><span data-stu-id="31d7f-228">The **Close** button</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="31d7f-229">Поиск заголовков и ответов в сети</span><span class="sxs-lookup"><span data-stu-id="31d7f-229">Search network headers and responses</span></span>   

<span data-ttu-id="31d7f-230">Используйте область **поиска** , если вам нужно найти заголовки HTTP и ответы по всем ресурсам для определенной строки или регулярного выражения.</span><span class="sxs-lookup"><span data-stu-id="31d7f-230">Use the **Search** pane when you need to search the HTTP headers and responses of all resources for a certain string or regular expression.</span></span>  

<span data-ttu-id="31d7f-231">Например, предположим, что вы хотите убедиться, что ваши ресурсы используют разумные **политики кэширования**.</span><span class="sxs-lookup"><span data-stu-id="31d7f-231">For example, suppose you want to verify that your resources are using reasonable **cache policies**.</span></span>  

<!--TODO: add cache policies section when available  -->

1.  <span data-ttu-id="31d7f-232">Нажмите **Поиск** \ ( ![ Поиск ][ImageSearchIcon] \).</span><span class="sxs-lookup"><span data-stu-id="31d7f-232">Select **Search** \(![Search][ImageSearchIcon]\).</span></span>  <span data-ttu-id="31d7f-233">Область поиска откроется слева от сетевого журнала.</span><span class="sxs-lookup"><span data-stu-id="31d7f-233">The Search pane opens to the left of the Network log.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-empty.msft.png" alt-text="Область "Поиск"" lightbox="../media/network-glitch-network-search-empty.msft.png":::
       <span data-ttu-id="31d7f-235">Область " **Поиск** "</span><span class="sxs-lookup"><span data-stu-id="31d7f-235">The **Search** pane</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="31d7f-236">Введите текст `Cache-Control` и нажмите клавишу `Enter` .</span><span class="sxs-lookup"><span data-stu-id="31d7f-236">Type `Cache-Control` and press `Enter`.</span></span>  <span data-ttu-id="31d7f-237">В области поиска перечислены все вхождения `Cache-Control` , найденные в заголовках или содержимом ресурсов.</span><span class="sxs-lookup"><span data-stu-id="31d7f-237">The Search pane lists all instances of `Cache-Control` that it finds in resource headers or content.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control.msft.png" alt-text="Результаты поиска для Cache-Control" lightbox="../media/network-glitch-network-search-cache-control.msft.png":::
       <span data-ttu-id="31d7f-239">Результаты поиска по запросу </span><span class="sxs-lookup"><span data-stu-id="31d7f-239">Search results for</span></span> `Cache-Control`  
    :::image-end:::  
    
1.  <span data-ttu-id="31d7f-240">Выберите результат, чтобы просмотреть ресурс, в котором был найден результат.</span><span class="sxs-lookup"><span data-stu-id="31d7f-240">Select a result to view the resource in which the result was found.</span></span>  <span data-ttu-id="31d7f-241">Если вы видите сведения о ресурсе, выберите результат, чтобы перейти непосредственно к нему.</span><span class="sxs-lookup"><span data-stu-id="31d7f-241">If you are looking at the details of the resource, select a result to go directly to it.</span></span>  <span data-ttu-id="31d7f-242">Например, если запрос был найден в заголовке, откроется вкладка Заголовки.</span><span class="sxs-lookup"><span data-stu-id="31d7f-242">For example, if the query was found in a header, the Headers tab opens.</span></span>   <span data-ttu-id="31d7f-243">Если запрос найден в содержимом, откроется вкладка **ответ** .</span><span class="sxs-lookup"><span data-stu-id="31d7f-243">If the query was found in content, the **Response** tab opens.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png" alt-text="Результат поиска, выделенный на вкладке "заголовки"" lightbox="../media/network-glitch-network-search-cache-control-headers-response-headers.msft.png":::
       <span data-ttu-id="31d7f-245">Результат поиска, выделенный на вкладке " **заголовки** "</span><span class="sxs-lookup"><span data-stu-id="31d7f-245">A search result highlighted in the **Headers** tab</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="31d7f-246">Закройте область поиска и вкладку заголовки.</span><span class="sxs-lookup"><span data-stu-id="31d7f-246">Close the Search pane and the Headers tab.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-search-close.msft.png" alt-text="Кнопки "Закрыть"" lightbox="../media/network-glitch-network-search-close.msft.png":::
       <span data-ttu-id="31d7f-248">Кнопки " **Закрыть** "</span><span class="sxs-lookup"><span data-stu-id="31d7f-248">The **Close** buttons</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="31d7f-249">Фильтрация ресурсов</span><span class="sxs-lookup"><span data-stu-id="31d7f-249">Filter resources</span></span>   

<span data-ttu-id="31d7f-250">DevTools предоставляет множество рабочих процессов для фильтрации ресурсов, не относящихся к поставленной задаче.</span><span class="sxs-lookup"><span data-stu-id="31d7f-250">DevTools provides numerous workflows for filtering out resources that are not relevant to the task at hand.</span></span>  

:::image type="complex" source="../media/network-glitch-network-filter-empty.msft.png" alt-text="Панель инструментов "фильтры"" lightbox="../media/network-glitch-network-filter-empty.msft.png":::
   <span data-ttu-id="31d7f-252">Панель инструментов " **фильтры** "</span><span class="sxs-lookup"><span data-stu-id="31d7f-252">The **Filters** toolbar</span></span>  
:::image-end:::  

<span data-ttu-id="31d7f-253">Панель инструментов " **фильтры** " должна быть включена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="31d7f-253">The **Filters** toolbar should be enabled by default.</span></span>  <span data-ttu-id="31d7f-254">Если не так:</span><span class="sxs-lookup"><span data-stu-id="31d7f-254">If not:</span></span>  

1.  <span data-ttu-id="31d7f-255">Выберите **Фильтр** \ ( ![ фильтр ][ImageFilterIcon] \), чтобы отобразить его.</span><span class="sxs-lookup"><span data-stu-id="31d7f-255">Select **Filter** \(![Filter][ImageFilterIcon]\) to show it.</span></span>  
    
### <span data-ttu-id="31d7f-256">Фильтрация по строке, регулярному выражению или свойству</span><span class="sxs-lookup"><span data-stu-id="31d7f-256">Filter by string, regular expression, or property</span></span>   

<span data-ttu-id="31d7f-257">Текстовое поле « **Фильтр** » поддерживает различные типы фильтрации.</span><span class="sxs-lookup"><span data-stu-id="31d7f-257">The **Filter** text box supports many different types of filtering.</span></span>  

1.  <span data-ttu-id="31d7f-258">Введите `png` текст в текстовое поле **Фильтр** .</span><span class="sxs-lookup"><span data-stu-id="31d7f-258">Type `png` into the **Filter** text box.</span></span>  <span data-ttu-id="31d7f-259">Отображаются только файлы, содержащие текст `png` .</span><span class="sxs-lookup"><span data-stu-id="31d7f-259">Only the files that contain the text `png` are shown.</span></span>  <span data-ttu-id="31d7f-260">В этом случае только файлы, соответствующие фильтру, являются изображениями в формате PNG.</span><span class="sxs-lookup"><span data-stu-id="31d7f-260">In this case the only files that match the filter are the PNG images.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-png.msft.png" alt-text="Строковый фильтр" lightbox="../media/network-glitch-network-filter-png.msft.png":::
       <span data-ttu-id="31d7f-262">Строковый фильтр</span><span class="sxs-lookup"><span data-stu-id="31d7f-262">A string filter</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="31d7f-263">Введите `/.*\.[cj]s+$/`.</span><span class="sxs-lookup"><span data-stu-id="31d7f-263">Type `/.*\.[cj]s+$/`.</span></span>  <span data-ttu-id="31d7f-264">DevTools отфильтровать все ресурсы с именем файла, которое не оканчивается на a, а `j` `c` затем с 1 или более `s` символами.</span><span class="sxs-lookup"><span data-stu-id="31d7f-264">DevTools filters out any resource with a filename that does not end with a `j` or a `c` followed by 1 or more `s` characters.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-regex.msft.png" alt-text="Фильтр регулярных выражений" lightbox="../media/network-glitch-network-filter-regex.msft.png":::
       <span data-ttu-id="31d7f-266">Фильтр регулярных выражений</span><span class="sxs-lookup"><span data-stu-id="31d7f-266">A regular expression filter</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="31d7f-267">Введите `-main.css`.</span><span class="sxs-lookup"><span data-stu-id="31d7f-267">Type `-main.css`.</span></span>  <span data-ttu-id="31d7f-268">DevTools отфильтровать `main.css` .</span><span class="sxs-lookup"><span data-stu-id="31d7f-268">DevTools filters out `main.css`.</span></span>  <span data-ttu-id="31d7f-269">Если какой – либо другой файл соответствует шаблону, он также будет исключен.</span><span class="sxs-lookup"><span data-stu-id="31d7f-269">If any other file matched the pattern they would also be filtered out.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-negative-statement.msft.png" alt-text="Отрицательный фильтр" lightbox="../media/network-glitch-network-filter-negative-statement.msft.png":::
       <span data-ttu-id="31d7f-271">Отрицательный фильтр</span><span class="sxs-lookup"><span data-stu-id="31d7f-271">A negative filter</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="31d7f-272">Введите `domain:cdn.glitch.com` текст в текстовое поле **Фильтр** .</span><span class="sxs-lookup"><span data-stu-id="31d7f-272">Type `domain:cdn.glitch.com` into the **Filter** text box.</span></span>  <span data-ttu-id="31d7f-273">DevTools отфильтровать все ресурсы с URL-адресом, который не соответствует этому домену.</span><span class="sxs-lookup"><span data-stu-id="31d7f-273">DevTools filters out any resource with a URL that does not match this domain.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-property-value.msft.png" alt-text="Фильтр свойств" lightbox="../media/network-glitch-network-filter-property-value.msft.png":::
       <span data-ttu-id="31d7f-275">Фильтр свойств</span><span class="sxs-lookup"><span data-stu-id="31d7f-275">A property filter</span></span>  
    :::image-end:::  
    
    <span data-ttu-id="31d7f-276">Просмотрите [запросы фильтрации по свойствам][DevtoolsReferenceProperty] для полного списка фильтруемых свойств.</span><span class="sxs-lookup"><span data-stu-id="31d7f-276">See [Filter requests by properties][DevtoolsReferenceProperty] for the full list of filterable properties.</span></span>  
    
1.  <span data-ttu-id="31d7f-277">Очистите текстовое поле " **Фильтр** " в любом тексте.</span><span class="sxs-lookup"><span data-stu-id="31d7f-277">Clear the **Filter** text box of any text.</span></span>  
    
### <span data-ttu-id="31d7f-278">Фильтрация по типу ресурсов</span><span class="sxs-lookup"><span data-stu-id="31d7f-278">Filter by resource type</span></span>   

<span data-ttu-id="31d7f-279">Чтобы сосредоточиться на файле определенного типа, например в таблицах стилей, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="31d7f-279">To focus in on a certain type of file, such as stylesheets:</span></span>  

1.  <span data-ttu-id="31d7f-280">Выберите **CSS**.</span><span class="sxs-lookup"><span data-stu-id="31d7f-280">Select **CSS**.</span></span>  <span data-ttu-id="31d7f-281">Все остальные типы файлов будут отфильтрованы.</span><span class="sxs-lookup"><span data-stu-id="31d7f-281">All other file types are filtered out.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css.msft.png" alt-text="Показывать только CSS – файлы" lightbox="../media/network-glitch-network-filter-file-type-css.msft.png":::
       <span data-ttu-id="31d7f-283">Показывать только CSS – файлы</span><span class="sxs-lookup"><span data-stu-id="31d7f-283">Show CSS files only</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="31d7f-284">Чтобы также просмотреть сценарии, удерживайте клавишу `Control` \ (Windows \) или `Command` \ (macOS \), а затем выберите **JS**.</span><span class="sxs-lookup"><span data-stu-id="31d7f-284">To also see scripts, hold `Control` \(Windows\) or `Command` \(macOS\) and then select **JS**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-filter-file-type-css-js.msft.png" alt-text="Показывать только файлы CSS и JS" lightbox="../media/network-glitch-network-filter-file-type-css-js.msft.png":::
       <span data-ttu-id="31d7f-286">Показывать только файлы CSS и JS</span><span class="sxs-lookup"><span data-stu-id="31d7f-286">Show CSS and JS files only</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="31d7f-287">Нажмите кнопку **все** , чтобы удалить фильтры и снова просмотреть все ресурсы.</span><span class="sxs-lookup"><span data-stu-id="31d7f-287">Select **All** to remove the filters and see all resources again.</span></span>  
    
<span data-ttu-id="31d7f-288">Просмотр [запросов фильтрации][DevtoolsNetworkReferenceFilter] для других рабочих процессов фильтрации.</span><span class="sxs-lookup"><span data-stu-id="31d7f-288">See [Filter requests][DevtoolsNetworkReferenceFilter] for other filtering workflows.</span></span>  

## <span data-ttu-id="31d7f-289">Блокировать запросы</span><span class="sxs-lookup"><span data-stu-id="31d7f-289">Block requests</span></span>   

<span data-ttu-id="31d7f-290">Как выглядит и работает страница при недоступности некоторых ресурсов страницы?</span><span class="sxs-lookup"><span data-stu-id="31d7f-290">How does a page look and behave when some of the page resources are not available?</span></span>  <span data-ttu-id="31d7f-291">Не удается полностью завершить его или он по-прежнему работает?</span><span class="sxs-lookup"><span data-stu-id="31d7f-291">Does it fail completely, or is it still somewhat functional?</span></span>  <span data-ttu-id="31d7f-292">Блокировка запросов на определение:</span><span class="sxs-lookup"><span data-stu-id="31d7f-292">Block requests to find out:</span></span>  

1.  <span data-ttu-id="31d7f-293">`Control` + `Shift` + `P` Чтобы открыть меню команд, нажмите клавиши \ (Windows \) или `Command` + `Shift` + `P` \ ( **Command Menu**macOS \).</span><span class="sxs-lookup"><span data-stu-id="31d7f-293">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-cli-empty.msft.png" alt-text="Меню команд" lightbox="../media/network-glitch-network-cli-empty.msft.png":::
       <span data-ttu-id="31d7f-295">**Меню команд**</span><span class="sxs-lookup"><span data-stu-id="31d7f-295">The **Command Menu**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="31d7f-296">Введите `block` команду **Показать блокировку запросов**и нажмите кнопку `Enter` .</span><span class="sxs-lookup"><span data-stu-id="31d7f-296">Type `block`, select **Show Request Blocking**, and press `Enter`.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block.msft.png" alt-text="Показать блокировку запросов" lightbox="../media/network-glitch-network-cli-block.msft.png":::
       **<span data-ttu-id="31d7f-298">Показать блокировку запросов</span><span class="sxs-lookup"><span data-stu-id="31d7f-298">Show Request Blocking</span></span>**  
    :::image-end:::  
    
1.  <span data-ttu-id="31d7f-299">Нажмите кнопку **Добавить узор** \ ( ![ Добавить шаблон ][ImageAddIcon] \).</span><span class="sxs-lookup"><span data-stu-id="31d7f-299">Select **Add Pattern** \(![Add Pattern][ImageAddIcon]\).</span></span>  
1.  <span data-ttu-id="31d7f-300">Введите `main.css`.</span><span class="sxs-lookup"><span data-stu-id="31d7f-300">Type `main.css`.</span></span>  
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-add-pattern.msft.png" alt-text="Блокировка Main. CSS" lightbox="../media/network-glitch-network-cli-block-add-pattern.msft.png":::
       <span data-ttu-id="31d7f-302">Снижающи</span><span class="sxs-lookup"><span data-stu-id="31d7f-302">Blocking</span></span> `main.css`  
    :::image-end:::  
    
1.  <span data-ttu-id="31d7f-303">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="31d7f-303">Select **Add**.</span></span>  
1.  <span data-ttu-id="31d7f-304">Перезагрузите страницу.</span><span class="sxs-lookup"><span data-stu-id="31d7f-304">Reload the page.</span></span>  <span data-ttu-id="31d7f-305">Как и предполагалось, стиль страницы немного изменился, так как основная таблица стилей заблокирована.</span><span class="sxs-lookup"><span data-stu-id="31d7f-305">As expected, the styling of the page is slightly messed up because the main stylesheet has been blocked.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="31d7f-306">`main.css`Строка в сетевом журнале.</span><span class="sxs-lookup"><span data-stu-id="31d7f-306">The `main.css` row in the Network Log.</span></span>  <span data-ttu-id="31d7f-307">Красный текст означает, что ресурс заблокирован.</span><span class="sxs-lookup"><span data-stu-id="31d7f-307">The red text means that the resource was blocked.</span></span>
    
    :::image type="complex" source="../media/network-glitch-network-cli-block-main-css.msft.png" alt-text="Главный. CSS заблокирован" lightbox="../media/network-glitch-network-cli-block-main-css.msft.png":::
       `main.css` <span data-ttu-id="31d7f-309">заблокирован</span><span class="sxs-lookup"><span data-stu-id="31d7f-309">has been blocked</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="31d7f-310">Снимите флажок **включить блокировку запросов** .</span><span class="sxs-lookup"><span data-stu-id="31d7f-310">Deselect the **Enable request blocking** checkbox.</span></span>  

## <span data-ttu-id="31d7f-311">Заключение</span><span class="sxs-lookup"><span data-stu-id="31d7f-311">Conclusion</span></span>  

<span data-ttu-id="31d7f-312">Поздравляем, вы завершили обучение.</span><span class="sxs-lookup"><span data-stu-id="31d7f-312">Congratulations, you have completed the tutorial.</span></span>  <span data-ttu-id="31d7f-313">Теперь вы знаете, как использовать панель " **сеть** " в Microsoft Edge DevTools!</span><span class="sxs-lookup"><span data-stu-id="31d7f-313">You now know how to use the **Network** panel in the Microsoft Edge DevTools!</span></span>

<!--




-->  

<span data-ttu-id="31d7f-314">Обратитесь к [справочной][DevtoolsNetworkReference] информации по сети, чтобы узнать о возможностях DevTools проверки активности сети.</span><span class="sxs-lookup"><span data-stu-id="31d7f-314">Check out the [Network Reference][DevtoolsNetworkReference] to discover more DevTools features related to inspecting network activity.</span></span>  

<!--  
 


-->  

<!-- image links -->  

[ImageAddIcon]: ../media/add-icon.msft.png  
[ImageCloseIcon]: ../media/close-icon.msft.png  
[ImageFilterIcon]: ../media/filter-icon.msft.png  
[ImageFormatIcon]: ../media/format-icon.msft.png  
[ImageRefreshIcon]: ../media/refresh-icon.msft.png  
[ImageScreenshotsIcon]: ../media/screenshots-icon.msft.png  
[ImageSearchIcon]: ../media/search-icon.msft.png  
[ImageSettingsIcon]: ../media/settings-icon.msft.png

<!-- links -->  

<!--[CachePolicies]: ../../../web/tools/lighthouse/audits/cache-policy ""  -->  

[DevToolsCustomizePlacement]: ../customize/placement.md "Изменение положения Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsNetworkReference]: ./reference.md "Справка по анализу сети | Документы Microsoft"
[DevtoolsNetworkReferenceFilter]: ./reference.md#filter-requests "Запросы фильтрации — Справочник по анализу сети | Документы Microsoft"  
[DevtoolsReferenceHideOverview]: ./reference.md#hide-the-overview-pane "Скрыть область обзора — Справка по анализу сети | Документы Microsoft"
[DevtoolsReferenceProperty]: ./reference.md#filter-requests-by-properties "Фильтрация запросов по свойствам-Справка по анализу сети | Документы Microsoft"
[DevToolsOpen]: ../open.md "Открыть Microsoft Edge DevTools | Документы Microsoft"  
[DevtoolsSpeedGetStarted]: ../speed/get-started.md "Оптимизация скорости веб-сайта с помощью Microsoft Edge DevTools | Документы Microsoft"  

[GlitchNetworkGetStarted]: https://microsoft-edge-chromium-devtools.glitch.me/static/network/getstarted.html "Пример проверки активности сети | Цепь"  

[MDNHTTPCache]: https://developer.mozilla.org/docs/Web/HTTP/Caching "Кэширование HTTP | MDN"  

> [!NOTE]
> <span data-ttu-id="31d7f-324">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="31d7f-324">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="31d7f-325">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/network/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="31d7f-325">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="31d7f-327">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="31d7f-327">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
