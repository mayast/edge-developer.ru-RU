---
title: Проверка активности сети в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 267b0113e07085dd565a3ff3437a3fcac2dff9d7
ms.sourcegitcommit: 33663cd7838dddee86228dde469a5e9551bddb02
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611814"
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





# <span data-ttu-id="7ab1e-103">Проверка активности сети в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="7ab1e-103">Inspect Network Activity In Microsoft Edge DevTools</span></span>   



<span data-ttu-id="7ab1e-104">В этом практическом занятии описаны некоторые из наиболее часто используемых функций DevTools, связанных с проанализом активности сети для страницы.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-104">This is a hands-on tutorial of some of the most commonly-used DevTools features related to inspecting network activity for a page.</span></span>  

<span data-ttu-id="7ab1e-105">Для просмотра функциональных возможностей используйте [ссылку сетевая ссылка][DevtoolsNetworkReference] .</span><span class="sxs-lookup"><span data-stu-id="7ab1e-105">See [Network Reference][DevtoolsNetworkReference] if you want to browse features instead.</span></span>  

<!--TODO: This entire section needs a Microsoft Edge DevTools re-write  -->

<!-- Read on, or watch the video version of this tutorial:  -->  

<!--
> [!VIDEO embed/e1gAyQuIFQo]  
-->

## <span data-ttu-id="7ab1e-106">Когда следует использовать панель "сеть"</span><span class="sxs-lookup"><span data-stu-id="7ab1e-106">When to use the Network panel</span></span>   

<span data-ttu-id="7ab1e-107">В общем случае следует использовать панель "сеть", чтобы убедиться в том, что ресурсы загружаются или загружаются должным образом.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-107">In general, use the Network panel when you need to make sure that resources are being downloaded or uploaded as expected.</span></span>  <span data-ttu-id="7ab1e-108">Наиболее распространенными вариантами использования панели "сеть" являются:</span><span class="sxs-lookup"><span data-stu-id="7ab1e-108">The most common use cases for the Network panel are:</span></span>  

*   <span data-ttu-id="7ab1e-109">Убедитесь в том, что ресурсы действительно отправляются или загружаются вообще.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-109">Making sure that resources are actually being uploaded or downloaded at all.</span></span>  
*   <span data-ttu-id="7ab1e-110">Проверка свойств отдельного ресурса, например HTTP-заголовков, содержимого, размера и т. д.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-110">Inspecting the properties of an individual resource, such as the HTTP headers, content, size, and so on.</span></span>  

<span data-ttu-id="7ab1e-111">Если вы ищете способы повышения быстродействия загрузки страниц, **не** начинайте с панели "сеть".</span><span class="sxs-lookup"><span data-stu-id="7ab1e-111">If you are looking for ways to improve page load performance, **do not** start with the Network panel.</span></span>  <span data-ttu-id="7ab1e-112">Существует множество типов проблем с производительностью нагрузки, не связанных с работой сети.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-112">There are many types of load performance issues that are not related to network activity.</span></span>  <span data-ttu-id="7ab1e-113">Начните работу с панели аудита, так как она содержит рекомендации по улучшению страницы.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-113">Start with the Audits panel because it gives you targeted suggestions on how to improve your page.</span></span>  <span data-ttu-id="7ab1e-114">Ознакомьтесь со [скоростью оптимизации веб-сайта][DevtoolsSpeedGetStarted].</span><span class="sxs-lookup"><span data-stu-id="7ab1e-114">See [Optimize Website Speed][DevtoolsSpeedGetStarted].</span></span>  

## <span data-ttu-id="7ab1e-115">Открытие панели "сеть"</span><span class="sxs-lookup"><span data-stu-id="7ab1e-115">Open the Network panel</span></span>   

<span data-ttu-id="7ab1e-116">Чтобы максимально эффективно пользоваться этим учебником, откройте демонстрацию и ознакомьтесь с функциями на странице Demo.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-116">To get the most out of this tutorial, open up the demo and try out the features on the demo page.</span></span>  

1.  <span data-ttu-id="7ab1e-117">Откройте [демонстрацию Приступая к работе][GlitchNetworkGetStarted] .</span><span class="sxs-lookup"><span data-stu-id="7ab1e-117">Open the [Get Started Demo][GlitchNetworkGetStarted] .</span></span>  
    
    > ##### <span data-ttu-id="7ab1e-118">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="7ab1e-118">Figure 1</span></span>  
    > <span data-ttu-id="7ab1e-119">Демонстрация</span><span class="sxs-lookup"><span data-stu-id="7ab1e-119">The demo</span></span>  
    > ![Демонстрация][ImagesTutorialDemo]  
    
    <!--You may prefer to move the demo to a separate window.  -->  
    
    <!--
    > ##### old Figure 2  
    > The demo in one window and this tutorial in a different window  
    > ![The demo in one window and this tutorial in a different window][ImagesTutorialWindows]  -->

1.  <span data-ttu-id="7ab1e-121">[Откройте DevTools][DevToolsOpen] , нажав клавиши `Control` + `Shift` + `J` \ (Windows \) или `Command` + `Option` + `J` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="7ab1e-121">[Open DevTools][DevToolsOpen] by pressing `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\).</span></span>  <span data-ttu-id="7ab1e-122">Откроется панель **консоли** .</span><span class="sxs-lookup"><span data-stu-id="7ab1e-122">The **Console** panel opens.</span></span>  
    
    > ##### <span data-ttu-id="7ab1e-123">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="7ab1e-123">Figure 2</span></span>  
    > <span data-ttu-id="7ab1e-124">На консоли</span><span class="sxs-lookup"><span data-stu-id="7ab1e-124">The Console</span></span>  
    > <span data-ttu-id="7ab1e-125">! [Консоль] [ImagesTutorialConsole]</span><span class="sxs-lookup"><span data-stu-id="7ab1e-125">![The Console][ImagesTutorialConsole]</span></span>  
    
    <span data-ttu-id="7ab1e-126">Вы можете [закрепить DevTools в нижней части окна][DevToolsCustomizePlacement].</span><span class="sxs-lookup"><span data-stu-id="7ab1e-126">You may prefer to [dock DevTools to the bottom of your window][DevToolsCustomizePlacement].</span></span>  
    
    > ##### <span data-ttu-id="7ab1e-127">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="7ab1e-127">Figure 3</span></span>  
    > <span data-ttu-id="7ab1e-128">DevTools закреплено в нижней части окна</span><span class="sxs-lookup"><span data-stu-id="7ab1e-128">DevTools docked to the bottom of the window</span></span>  
    > <span data-ttu-id="7ab1e-129">! [DevTools закреплен в нижней части окна] [ImagesTutorialDocked]</span><span class="sxs-lookup"><span data-stu-id="7ab1e-129">![DevTools docked to the bottom of the window][ImagesTutorialDocked]</span></span>  

1.  <span data-ttu-id="7ab1e-130">Откройте вкладку **сеть** .  Откроется панель Network (сеть).</span><span class="sxs-lookup"><span data-stu-id="7ab1e-130">Select the **Network** tab.  The Network panel opens.</span></span>  
    
    > ##### <span data-ttu-id="7ab1e-131">Рисунок4</span><span class="sxs-lookup"><span data-stu-id="7ab1e-131">Figure 4</span></span>  
    > <span data-ttu-id="7ab1e-132">DevTools закреплено в нижней части окна</span><span class="sxs-lookup"><span data-stu-id="7ab1e-132">DevTools docked to the bottom of the window</span></span>  
    > <span data-ttu-id="7ab1e-133">! [DevTools закреплен в нижней части окна] [ImagesTutorialNetwork]</span><span class="sxs-lookup"><span data-stu-id="7ab1e-133">![DevTools docked to the bottom of the window][ImagesTutorialNetwork]</span></span>  

<span data-ttu-id="7ab1e-134">Прямо сейчас панель Network (сеть) пуста.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-134">Right now the Network panel is empty.</span></span>  <span data-ttu-id="7ab1e-135">DevTools только записывает сетевые активности после того, как вы откроете ее и не произошел никаких сетевых операций после того, как вы открыли DevTools.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-135">DevTools only logs network activity after you open it and no network activity has occurred since you opened DevTools.</span></span>  

## <span data-ttu-id="7ab1e-136">Регистрация активности в сети</span><span class="sxs-lookup"><span data-stu-id="7ab1e-136">Log network activity</span></span>   

<span data-ttu-id="7ab1e-137">Чтобы просмотреть сетевую активность, которая вызывается страницей, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-137">To view the network activity that a page causes:</span></span>  

1.  <span data-ttu-id="7ab1e-138">Перезагрузите страницу.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-138">Reload the page.</span></span>  <span data-ttu-id="7ab1e-139">На панели Network (сеть) регистрируются все сетевые активности в **журнале сети**.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-139">The Network panel logs all network activity in the **Network Log**.</span></span>  
    
    > ##### <span data-ttu-id="7ab1e-140">Рисунок 5</span><span class="sxs-lookup"><span data-stu-id="7ab1e-140">Figure 5</span></span>  
    > <span data-ttu-id="7ab1e-141">Журнал сети</span><span class="sxs-lookup"><span data-stu-id="7ab1e-141">The Network Log</span></span>  
    > <span data-ttu-id="7ab1e-142">! [Журнал сети] [ImagesTutorialLog]</span><span class="sxs-lookup"><span data-stu-id="7ab1e-142">![The Network Log][ImagesTutorialLog]</span></span>  
    
    <span data-ttu-id="7ab1e-143">Каждая строка **журнала сети** представляет ресурс.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-143">Each row of the **Network Log** represents a resource.</span></span>  <span data-ttu-id="7ab1e-144">По умолчанию ресурсы указаны в хронологическом порядке.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-144">By default the resources are listed chronologically.</span></span>  <span data-ttu-id="7ab1e-145">Самый верхний ресурс обычно является основным HTML-документом.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-145">The top resource is usually the main HTML document.</span></span>  <span data-ttu-id="7ab1e-146">Самый нижний ресурс — это тот, который запрашивался последним.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-146">The bottom resource is whatever was requested last.</span></span>  
    
    <span data-ttu-id="7ab1e-147">Каждый столбец представляет сведения о ресурсе.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-147">Each column represents information about a resource.</span></span>  <span data-ttu-id="7ab1e-148">На [**рисунке 6**](#figure-6) показаны столбцы по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-148">[**Figure 6**](#figure-6) shows the default columns:</span></span>  

    *   <span data-ttu-id="7ab1e-149">**Состояние**.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-149">**Status**.</span></span>  <span data-ttu-id="7ab1e-150">Код состояния HTTP для ответа.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-150">The HTTP status code for response.</span></span>  
    *   <span data-ttu-id="7ab1e-151">**Тип**.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-151">**Type**.</span></span>  <span data-ttu-id="7ab1e-152">Тип ресурса.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-152">The resource type.</span></span>  
    *   <span data-ttu-id="7ab1e-153">**Инициатор**.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-153">**Initiator**.</span></span>  <span data-ttu-id="7ab1e-154">Причина запроса ресурса.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-154">The cause of the resource request.</span></span>  <span data-ttu-id="7ab1e-155">При выборе ссылки в столбце инициатора осуществляется переход к исходному коду, вызвавшему запрос.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-155">Selecting a link in the Initiator column takes you to the source code that caused the request.</span></span>  
    *   <span data-ttu-id="7ab1e-156">**Time (время**).</span><span class="sxs-lookup"><span data-stu-id="7ab1e-156">**Time**.</span></span>  <span data-ttu-id="7ab1e-157">Продолжительность запроса.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-157">The duration of the request.</span></span>  
    *   <span data-ttu-id="7ab1e-158">**Каскадом**.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-158">**Waterfall**.</span></span>  <span data-ttu-id="7ab1e-159">Графическое представление различных стадий запроса.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-159">A graphical representation of the different stages of the request.</span></span>  
        <span data-ttu-id="7ab1e-160">Наведите указатель мыши на Каскад, чтобы увидеть разбивку.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-160">Hover over a Waterfall to see a breakdown.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="7ab1e-161">Диаграмма, расположенная над сетевым журналом, называется обзором.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-161">The graph above the Network Log is called the Overview.</span></span>  <span data-ttu-id="7ab1e-162">Вы не будете использовать граф обзора в этом учебнике, поэтому вы можете скрыть его.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-162">You will not use the Overview graph in this tutorial, so you may hide it.</span></span>  <span data-ttu-id="7ab1e-163">Ознакомьтесь [со статьей скрыть область "Общие сведения"][DevtoolsReferenceHideOverview].</span><span class="sxs-lookup"><span data-stu-id="7ab1e-163">See [Hide the Overview pane][DevtoolsReferenceHideOverview].</span></span>
        
1.  <span data-ttu-id="7ab1e-164">После открытия DevTools записывает в журнал сети активность сети.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-164">After you open DevTools, it records network activity in the Network Log.</span></span>  
    <span data-ttu-id="7ab1e-165">Чтобы продемонстрировать это, сначала ознакомьтесь с нижней частью **журнала сети** и запомните о том, что последнее действие будет заглянуть в эту оценку.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-165">To demonstrate this, first look at the bottom of the **Network Log** and make a mental note of the last activity.</span></span>  
1.  <span data-ttu-id="7ab1e-166">Теперь нажмите кнопку " **получить данные** " в демонстрационной версии.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-166">Now, select the **Get Data** button in the demo.</span></span>  
1.  <span data-ttu-id="7ab1e-167">Снова посмотрите на нижнюю часть **сетевого журнала** .</span><span class="sxs-lookup"><span data-stu-id="7ab1e-167">Look at the bottom of the **Network Log** again.</span></span>  <span data-ttu-id="7ab1e-168">Вы должны увидеть новый ресурс под названием "" `getstarted.json` .</span><span class="sxs-lookup"><span data-stu-id="7ab1e-168">You should see a new resource called `getstarted.json`.</span></span>  <span data-ttu-id="7ab1e-169">Нажатие кнопки " **получить данные** " привела к тому, что страница запрашивает этот файл.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-169">Selecting the **Get Data** button caused the page to request this file.</span></span>  
    
    > ##### <span data-ttu-id="7ab1e-170">Рисунок6</span><span class="sxs-lookup"><span data-stu-id="7ab1e-170">Figure 6</span></span>  
    > <span data-ttu-id="7ab1e-171">Новый ресурс в сетевом журнале</span><span class="sxs-lookup"><span data-stu-id="7ab1e-171">A new resource in the Network Log</span></span>  
    > <span data-ttu-id="7ab1e-172">! [Новый ресурс в сетевом журнале] [ImagesTutorialRuntime]</span><span class="sxs-lookup"><span data-stu-id="7ab1e-172">![A new resource in the Network Log][ImagesTutorialRuntime]</span></span>  

## <span data-ttu-id="7ab1e-173">Показать дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="7ab1e-173">Show more information</span></span>   

<span data-ttu-id="7ab1e-174">Столбцы сетевого журнала можно настраивать.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-174">The columns of the Network Log are configurable.</span></span>  <span data-ttu-id="7ab1e-175">Столбцы, которые вы не используете, могут быть скрыты.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-175">You may hide columns that you are not using.</span></span>  
<span data-ttu-id="7ab1e-176">Кроме того, существует множество столбцов, которые по умолчанию скрыты, что может оказаться полезным.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-176">There are also many columns that are hidden by default which you may find useful.</span></span>  

1.  <span data-ttu-id="7ab1e-177">Щелкните правой кнопкой мыши заголовок таблицы журнала сети и выберите команду **Domain (домен**).</span><span class="sxs-lookup"><span data-stu-id="7ab1e-177">Right-click the header of the Network Log table and select **Domain**.</span></span>  <span data-ttu-id="7ab1e-178">Теперь отображается домен каждого ресурса.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-178">The domain of each resource is now shown.</span></span>  
    
    > ##### <span data-ttu-id="7ab1e-179">Рисунок7</span><span class="sxs-lookup"><span data-stu-id="7ab1e-179">Figure 7</span></span>  
    > <span data-ttu-id="7ab1e-180">Включение столбца Domain (домен)</span><span class="sxs-lookup"><span data-stu-id="7ab1e-180">Enabling the Domain column</span></span>  
    > <span data-ttu-id="7ab1e-181">! [Включение столбца domain] [ImagesTutorialDomain]</span><span class="sxs-lookup"><span data-stu-id="7ab1e-181">![Enabling the Domain column][ImagesTutorialDomain]</span></span>  
    
    > [!TIP]
    > <span data-ttu-id="7ab1e-182">Просмотр полного URL-адреса ресурса при наведении указателя мыши на ячейку в столбце **имя** .</span><span class="sxs-lookup"><span data-stu-id="7ab1e-182">See the full URL of a resource by hovering over the cell in the **Name** column.</span></span>  

## <span data-ttu-id="7ab1e-183">Имитация медленных подключений к сети</span><span class="sxs-lookup"><span data-stu-id="7ab1e-183">Simulate a slower network connection</span></span>   

<span data-ttu-id="7ab1e-184">Сетевое подключение компьютера, используемого для создания сайтов, скорее всего быстрее, чем сетевые подключения мобильных устройств ваших пользователей.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-184">The network connection of the computer that you use to build sites is probably faster than the network connections of the mobile devices of your users.</span></span>  <span data-ttu-id="7ab1e-185">Перетаскивая страницу, вы получите более общее представление о том, как долго страница будет загружаться на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-185">By throttling the page, you get a better idea of how long a page takes to load on a mobile device.</span></span>  

1.  <span data-ttu-id="7ab1e-186">Выберите раскрывающийся список **регулирования** , для которого по умолчанию установлено значение в **сети** .</span><span class="sxs-lookup"><span data-stu-id="7ab1e-186">Select the **Throttling** dropdown, which is set to **Online** by default.</span></span>  
    
    > ##### <span data-ttu-id="7ab1e-187">Рисунок8</span><span class="sxs-lookup"><span data-stu-id="7ab1e-187">Figure 8</span></span>  
    > <span data-ttu-id="7ab1e-188">Включение регулирования</span><span class="sxs-lookup"><span data-stu-id="7ab1e-188">Enabling throttling</span></span>  
    > <span data-ttu-id="7ab1e-189">! [Включение регулирования] [ImagesTutorialThrottling]</span><span class="sxs-lookup"><span data-stu-id="7ab1e-189">![Enabling throttling][ImagesTutorialThrottling]</span></span>  
    
1.  <span data-ttu-id="7ab1e-190">Выберите **медленное 3G**.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-190">Select **Slow 3G**.</span></span>  
    
    > ##### <span data-ttu-id="7ab1e-191">Рисунок9</span><span class="sxs-lookup"><span data-stu-id="7ab1e-191">Figure 9</span></span>  
    > <span data-ttu-id="7ab1e-192">Выбор медленной сети 3G</span><span class="sxs-lookup"><span data-stu-id="7ab1e-192">Selecting Slow 3G</span></span>  
    > <span data-ttu-id="7ab1e-193">! [Выберите медленное 3G] [ImagesTutorialSlow3G]</span><span class="sxs-lookup"><span data-stu-id="7ab1e-193">![Selecting Slow 3G][ImagesTutorialSlow3G]</span></span>  
    
1.  <span data-ttu-id="7ab1e-194">Нажмите кнопку Повторная **Загрузка** ![ ][ImageRefreshIcon] и выберите **пустой кэш и нажмите окончательную перезагрузку**.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-194">Long-press **Reload** ![Reload][ImageRefreshIcon] and then select **Empty Cache And Hard Reload**.</span></span>  
    
    > ##### <span data-ttu-id="7ab1e-195">Рисунок 10</span><span class="sxs-lookup"><span data-stu-id="7ab1e-195">Figure 10</span></span>  
    > <span data-ttu-id="7ab1e-196">Пустой кэш и окончательная перезагрузка</span><span class="sxs-lookup"><span data-stu-id="7ab1e-196">Empty Cache And Hard Reload</span></span>  
    > <span data-ttu-id="7ab1e-197">! [Пустой кэш и окончательная перезагрузка] [ImagesTutorialHardReload]</span><span class="sxs-lookup"><span data-stu-id="7ab1e-197">![Empty Cache And Hard Reload][ImagesTutorialHardReload]</span></span>  
    
    <span data-ttu-id="7ab1e-198">При повторном посещении браузер обычно обслуживает некоторые файлы из [кэша][MDNHTTPCache] , что ускоряет загрузку страницы.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-198">On repeat visits, the browser usually serves some files from the [cache][MDNHTTPCache] , which speeds up the page load.</span></span>  <span data-ttu-id="7ab1e-199">**Пустой кэш, и при принудительной перезагрузке** браузер перейдет в сеть для всех ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-199">**Empty Cache And Hard Reload** forces the browser to go the network for all resources.</span></span>  <span data-ttu-id="7ab1e-200">Это полезно, если вы хотите узнать, как в первый раз происходит загрузка страницы посетителем.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-200">This is helpful when you want to see how a first-time visitor experiences a page load.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="7ab1e-201">**Пустой кэш и рабочий процесс повторной загрузки** доступны только в том случае, если открыт DevTools.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-201">The **Empty Cache And Hard Reload** workflow is only available when DevTools is open.</span></span>  

## <span data-ttu-id="7ab1e-202">Захват снимков экрана</span><span class="sxs-lookup"><span data-stu-id="7ab1e-202">Capture screenshots</span></span>   

<span data-ttu-id="7ab1e-203">С помощью снимков экрана можно увидеть, как страница была найдена во время загрузки.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-203">Screenshots let you see how a page looked over time while it was loading.</span></span>  

1.  <span data-ttu-id="7ab1e-204">Нажмите кнопку ![ Параметры сети ][ImageSettingsIcon] и установите флажок **захватить снимки экрана** .</span><span class="sxs-lookup"><span data-stu-id="7ab1e-204">Select ![Network settings][ImageSettingsIcon] and select the **Capture screenshots** checkbox.</span></span>
1.  <span data-ttu-id="7ab1e-205">Снова загрузите страницу с помощью **пустого кэша и окончательной повторной загрузки** .</span><span class="sxs-lookup"><span data-stu-id="7ab1e-205">Reload the page again via the **Empty Cache And Hard Reload** workflow.</span></span>  <span data-ttu-id="7ab1e-206">Если вам нужно напоминание о том, как это сделать, ознакомьтесь [с](#simulate-a-slower-network-connection) разрешениями.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-206">See [Simulate a slower connection](#simulate-a-slower-network-connection) if you need a reminder on how to do this.</span></span>  
    <span data-ttu-id="7ab1e-207">В области снимков экрана представлены эскизы того, как страница рассмотрелась на разных этапах процесса загрузки.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-207">The Screenshots pane provides thumbnails of how the page looked at various points during the loading process.</span></span>  
    
    > ##### <span data-ttu-id="7ab1e-208">Рисунок11</span><span class="sxs-lookup"><span data-stu-id="7ab1e-208">Figure 11</span></span>  
    > <span data-ttu-id="7ab1e-209">Снимки экрана загрузки страницы</span><span class="sxs-lookup"><span data-stu-id="7ab1e-209">Screenshots of the page load</span></span>  
    > <span data-ttu-id="7ab1e-210">! [Снимки экрана загруженной страницы] [ImagesTutorialAllScreenshots]</span><span class="sxs-lookup"><span data-stu-id="7ab1e-210">![Screenshots of the page load][ImagesTutorialAllScreenshots]</span></span>  

1.  <span data-ttu-id="7ab1e-211">Выберите первый эскиз.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-211">Select the first thumbnail.</span></span>  <span data-ttu-id="7ab1e-212">DevTools показывает, какая сетевая активность происходила в данный момент времени.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-212">DevTools shows you what network activity was occurring at that moment in time.</span></span>  
    
    > ##### <span data-ttu-id="7ab1e-213">Рисунок12</span><span class="sxs-lookup"><span data-stu-id="7ab1e-213">Figure 12</span></span>  
    > <span data-ttu-id="7ab1e-214">Сетевая активность, происходящий на первом снимке экрана</span><span class="sxs-lookup"><span data-stu-id="7ab1e-214">The network activity that was happening during the first screenshot</span></span>  
    > <span data-ttu-id="7ab1e-215">! [Сетевая активность, происходящие во время первого снимка экрана] [ImagesTutorialFirstScreenshot]</span><span class="sxs-lookup"><span data-stu-id="7ab1e-215">![The network activity that was happening during the first screenshot][ImagesTutorialFirstScreenshot]</span></span>  

1.  <span data-ttu-id="7ab1e-216">Снова нажмите кнопку ![ Параметры сети ][ImageSettingsIcon] и снимите флажок **захватить снимки экрана** , чтобы закрыть область снимки экрана.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-216">Select ![Network settings][ImageSettingsIcon] again and deselect the **Capture screenshots** checkbox to close the Screenshots pane.</span></span>
1.  <span data-ttu-id="7ab1e-217">Повторно загрузите страницу.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-217">Reload the page again.</span></span>  

## <span data-ttu-id="7ab1e-218">Проверка сведений о ресурсе</span><span class="sxs-lookup"><span data-stu-id="7ab1e-218">Inspect the details of the resource</span></span>   

<span data-ttu-id="7ab1e-219">Выберите ресурс, чтобы получить дополнительные сведения о нем.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-219">Select a resource to learn more information about it.</span></span>  <span data-ttu-id="7ab1e-220">Попробуйте вот так:</span><span class="sxs-lookup"><span data-stu-id="7ab1e-220">Try it now:</span></span>  

1.  <span data-ttu-id="7ab1e-221">Выберите `getstarted.html` .</span><span class="sxs-lookup"><span data-stu-id="7ab1e-221">Select `getstarted.html`.</span></span>  <span data-ttu-id="7ab1e-222">Показана вкладка " **заголовки** ".</span><span class="sxs-lookup"><span data-stu-id="7ab1e-222">The **Headers** tab is shown.</span></span>  <span data-ttu-id="7ab1e-223">Используйте эту вкладку для проверки заголовков HTTP.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-223">Use this tab to inspect HTTP headers.</span></span>  
    
    > ##### <span data-ttu-id="7ab1e-224">Рисунок13</span><span class="sxs-lookup"><span data-stu-id="7ab1e-224">Figure 13</span></span>  
    > <span data-ttu-id="7ab1e-225">Вкладка "заголовки"</span><span class="sxs-lookup"><span data-stu-id="7ab1e-225">The Headers tab</span></span>  
    > <span data-ttu-id="7ab1e-226">! [Вкладка Заголовки] [ImagesTutorialHeaders]</span><span class="sxs-lookup"><span data-stu-id="7ab1e-226">![The Headers tab][ImagesTutorialHeaders]</span></span>  
    
1.  <span data-ttu-id="7ab1e-227">Откройте вкладку **Предварительный просмотр** .  Отобразится основной рендеринг HTML-кода.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-227">Select the **Preview** tab.  A basic rendering of the HTML is shown.</span></span>  
    
    > ##### <span data-ttu-id="7ab1e-228">Рисунок14</span><span class="sxs-lookup"><span data-stu-id="7ab1e-228">Figure 14</span></span>  
    > <span data-ttu-id="7ab1e-229">Вкладка "предварительный просмотр"</span><span class="sxs-lookup"><span data-stu-id="7ab1e-229">The Preview tab</span></span>  
    > <span data-ttu-id="7ab1e-230">! [Вкладка "предварительный просмотр"] [ImagesTutorialPreview]</span><span class="sxs-lookup"><span data-stu-id="7ab1e-230">![The Preview tab][ImagesTutorialPreview]</span></span>  

     <span data-ttu-id="7ab1e-231">Эта вкладка полезна, если API возвращает код ошибки в HTML.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-231">This tab is helpful when an API returns an error code in HTML.</span></span>  <span data-ttu-id="7ab1e-232">Возможно, вам будет проще прочитать обработанный HTML, чем исходный HTML-код или просматривает изображения.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-232">You may find it easier to read the rendered HTML than the HTML source code, or when you inspect images.</span></span>  

1.  <span data-ttu-id="7ab1e-233">Откройте вкладку **ответ** .  Отобразится исходный код HTML.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-233">Select the **Response** tab.  The HTML source code is shown.</span></span>  
    
    > ##### <span data-ttu-id="7ab1e-234">Рисунок15</span><span class="sxs-lookup"><span data-stu-id="7ab1e-234">Figure 15</span></span>  
    > <span data-ttu-id="7ab1e-235">Вкладка "ответ"</span><span class="sxs-lookup"><span data-stu-id="7ab1e-235">The Response tab</span></span>  
    > <span data-ttu-id="7ab1e-236">! [Вкладка "ответ"] [ImagesTutorialResponse]</span><span class="sxs-lookup"><span data-stu-id="7ab1e-236">![The Response tab][ImagesTutorialResponse]</span></span>  
    
    > [!TIP]
    > <span data-ttu-id="7ab1e-237">Если файл minified, то при нажатии кнопки формат **формата** ![ ][ImageFormatIcon] в нижней части вкладки **ответа** повторно форматирует содержимое файла для чтения.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-237">When a file is minified, selecting the **Format** ![Format][ImageFormatIcon] button at the bottom of the **Response** tab re-formats the contents of the file for readability.</span></span>  

1.  <span data-ttu-id="7ab1e-238">Откройте вкладку **время** .  Показана сетевая подразделение активности для этого ресурса.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-238">Select the **Timing** tab.  A breakdown of the network activity for this resource is shown.</span></span>  
    
    > ##### <span data-ttu-id="7ab1e-239">Рисунок16</span><span class="sxs-lookup"><span data-stu-id="7ab1e-239">Figure 16</span></span>  
    > <span data-ttu-id="7ab1e-240">Вкладка время</span><span class="sxs-lookup"><span data-stu-id="7ab1e-240">The Timing tab</span></span>  
    > <span data-ttu-id="7ab1e-241">! [Вкладка время] [ImagesTutorialTiming]</span><span class="sxs-lookup"><span data-stu-id="7ab1e-241">![The Timing tab][ImagesTutorialTiming]</span></span>  

1.  <span data-ttu-id="7ab1e-242">Нажмите кнопку **Закрыть** ![ ][ImageCloseIcon] , чтобы снова просмотреть журнал сети.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-242">Select **Close** ![Close][ImageCloseIcon] to view the Network Log again.</span></span>  
    
    > ##### <span data-ttu-id="7ab1e-243">Рисунок17</span><span class="sxs-lookup"><span data-stu-id="7ab1e-243">Figure 17</span></span>  
    > <span data-ttu-id="7ab1e-244">Кнопка "Закрыть"</span><span class="sxs-lookup"><span data-stu-id="7ab1e-244">The Close button</span></span>  
    > <span data-ttu-id="7ab1e-245">! [Кнопка "Закрыть"] [ImagesTutorialCloseTiming]</span><span class="sxs-lookup"><span data-stu-id="7ab1e-245">![The Close button][ImagesTutorialCloseTiming]</span></span>  

## <span data-ttu-id="7ab1e-246">Поиск заголовков и ответов в сети</span><span class="sxs-lookup"><span data-stu-id="7ab1e-246">Search network headers and responses</span></span>   

<span data-ttu-id="7ab1e-247">Используйте область **поиска** , если вам нужно найти заголовки HTTP и ответы по всем ресурсам для определенной строки или регулярного выражения.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-247">Use the **Search** pane when you need to search the HTTP headers and responses of all resources for a certain string or regular expression.</span></span>  

<span data-ttu-id="7ab1e-248">Например, предположим, что вы хотите убедиться, что ваши ресурсы используют разумные **политики кэширования**.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-248">For example, suppose you want to verify that your resources are using reasonable **cache policies**.</span></span>  

<!--TODO: add cache policies section when available  -->

1.  <span data-ttu-id="7ab1e-249">Выберите **Search** ![ Поиск поиска ][ImageSearchIcon] .</span><span class="sxs-lookup"><span data-stu-id="7ab1e-249">Select **Search** ![Search][ImageSearchIcon].</span></span>  <span data-ttu-id="7ab1e-250">Область поиска откроется слева от сетевого журнала.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-250">The Search pane opens to the left of the Network log.</span></span>  
    
    > ##### <span data-ttu-id="7ab1e-251">Рис. 18</span><span class="sxs-lookup"><span data-stu-id="7ab1e-251">Figure 18</span></span>  
    > <span data-ttu-id="7ab1e-252">Область "Поиск"</span><span class="sxs-lookup"><span data-stu-id="7ab1e-252">The Search pane</span></span>  
    > <span data-ttu-id="7ab1e-253">! [Область поиска] [ImagesTutorialSearch]</span><span class="sxs-lookup"><span data-stu-id="7ab1e-253">![The Search pane][ImagesTutorialSearch]</span></span>  

1.  <span data-ttu-id="7ab1e-254">Введите текст `Cache-Control` и нажмите клавишу `Enter` .</span><span class="sxs-lookup"><span data-stu-id="7ab1e-254">Type `Cache-Control` and press `Enter`.</span></span>  <span data-ttu-id="7ab1e-255">В области поиска перечислены все вхождения `Cache-Control` , найденные в заголовках или содержимом ресурсов.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-255">The Search pane lists all instances of `Cache-Control` that it finds in resource headers or content.</span></span>  
    
    > ##### <span data-ttu-id="7ab1e-256">На рисунке 19</span><span class="sxs-lookup"><span data-stu-id="7ab1e-256">Figure 19</span></span>  
    > <span data-ttu-id="7ab1e-257">Результаты поиска по запросу </span><span class="sxs-lookup"><span data-stu-id="7ab1e-257">Search results for</span></span> `Cache-Control`  
    > <span data-ttu-id="7ab1e-258">! [Результаты поиска для Cache-Control] [ImagesTutorialResults]</span><span class="sxs-lookup"><span data-stu-id="7ab1e-258">![Search results for Cache-Control][ImagesTutorialResults]</span></span>  

1.  <span data-ttu-id="7ab1e-259">Выберите результат, чтобы просмотреть ресурс, в котором был найден результат.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-259">Select a result to view the resource in which the result was found.</span></span>  <span data-ttu-id="7ab1e-260">Если вы видите сведения о ресурсе, выберите результат, чтобы перейти непосредственно к нему.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-260">If you are looking at the details of the resource, select a result to go directly to it.</span></span>  <span data-ttu-id="7ab1e-261">Например, если запрос был найден в заголовке, откроется вкладка Заголовки.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-261">For example, if the query was found in a header, the Headers tab opens.</span></span>   <span data-ttu-id="7ab1e-262">Если запрос найден в содержимом, откроется вкладка **ответ** .</span><span class="sxs-lookup"><span data-stu-id="7ab1e-262">If the query was found in content, the **Response** tab opens.</span></span>  
    
    > ##### <span data-ttu-id="7ab1e-263">Рис. 20</span><span class="sxs-lookup"><span data-stu-id="7ab1e-263">Figure 20</span></span>  
    > <span data-ttu-id="7ab1e-264">Результат поиска, выделенный на вкладке "заголовки"</span><span class="sxs-lookup"><span data-stu-id="7ab1e-264">A search result highlighted in the Headers tab</span></span>  
    > <span data-ttu-id="7ab1e-265">! [Результат поиска, выделенный на вкладке Заголовки] [ImagesTutorialCache]</span><span class="sxs-lookup"><span data-stu-id="7ab1e-265">![A search result highlighted in the Headers tab][ImagesTutorialCache]</span></span>  
    
1.  <span data-ttu-id="7ab1e-266">Закройте область поиска и вкладку заголовки.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-266">Close the Search pane and the Headers tab.</span></span>  
    
    > ##### <span data-ttu-id="7ab1e-267">Рисунок 21</span><span class="sxs-lookup"><span data-stu-id="7ab1e-267">Figure 21</span></span>  
    > <span data-ttu-id="7ab1e-268">Кнопки "Закрыть"</span><span class="sxs-lookup"><span data-stu-id="7ab1e-268">The Close buttons</span></span>  
    > <span data-ttu-id="7ab1e-269">! [Кнопки закрытия] [ImagesTutorialCloseButtons]</span><span class="sxs-lookup"><span data-stu-id="7ab1e-269">![The Close buttons][ImagesTutorialCloseButtons]</span></span>  
    
## <span data-ttu-id="7ab1e-270">Фильтрация ресурсов</span><span class="sxs-lookup"><span data-stu-id="7ab1e-270">Filter resources</span></span>   

<span data-ttu-id="7ab1e-271">DevTools предоставляет множество рабочих процессов для фильтрации ресурсов, не относящихся к поставленной задаче.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-271">DevTools provides numerous workflows for filtering out resources that are not relevant to the task at hand.</span></span>  

> ##### <span data-ttu-id="7ab1e-272">Рис. 22</span><span class="sxs-lookup"><span data-stu-id="7ab1e-272">Figure 22</span></span>  
> <span data-ttu-id="7ab1e-273">Панель инструментов "фильтры"</span><span class="sxs-lookup"><span data-stu-id="7ab1e-273">The Filters toolbar</span></span>  
> <span data-ttu-id="7ab1e-274">! [Панель инструментов "фильтры"] [ImagesTutorialFilters]</span><span class="sxs-lookup"><span data-stu-id="7ab1e-274">![The Filters toolbar][ImagesTutorialFilters]</span></span>  

<span data-ttu-id="7ab1e-275">Панель инструментов " **фильтры** " должна быть включена по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-275">The **Filters** toolbar should be enabled by default.</span></span>  <span data-ttu-id="7ab1e-276">Если не так:</span><span class="sxs-lookup"><span data-stu-id="7ab1e-276">If not:</span></span>  

1.  <span data-ttu-id="7ab1e-277">Щелкните фильтр **фильтра** ![ ][ImageFilterIcon] , чтобы отобразить его.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-277">Select **Filter** ![Filter][ImageFilterIcon] to show it.</span></span>  

### <span data-ttu-id="7ab1e-278">Фильтрация по строке, регулярному выражению или свойству</span><span class="sxs-lookup"><span data-stu-id="7ab1e-278">Filter by string, regular expression, or property</span></span>   

<span data-ttu-id="7ab1e-279">Текстовое поле « **Фильтр** » поддерживает различные типы фильтрации.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-279">The **Filter** text box supports many different types of filtering.</span></span>  

1.  <span data-ttu-id="7ab1e-280">Введите `png` текст в текстовое поле **Фильтр** .</span><span class="sxs-lookup"><span data-stu-id="7ab1e-280">Type `png` into the **Filter** text box.</span></span>  <span data-ttu-id="7ab1e-281">Отображаются только файлы, содержащие текст `png` .</span><span class="sxs-lookup"><span data-stu-id="7ab1e-281">Only the files that contain the text `png` are shown.</span></span>  <span data-ttu-id="7ab1e-282">В этом случае только файлы, соответствующие фильтру, являются изображениями в формате PNG.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-282">In this case the only files that match the filter are the PNG images.</span></span>  
    
    > ##### <span data-ttu-id="7ab1e-283">Рис. 23</span><span class="sxs-lookup"><span data-stu-id="7ab1e-283">Figure 23</span></span>  
    > <span data-ttu-id="7ab1e-284">Строковый фильтр</span><span class="sxs-lookup"><span data-stu-id="7ab1e-284">A string filter</span></span>  
    > <span data-ttu-id="7ab1e-285">! [Строковый фильтр] [ImagesTutorialPNG]</span><span class="sxs-lookup"><span data-stu-id="7ab1e-285">![A string filter][ImagesTutorialPNG]</span></span>  

1.  <span data-ttu-id="7ab1e-286">Введите `/.*\.[cj]s+$/`.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-286">Type `/.*\.[cj]s+$/`.</span></span>  <span data-ttu-id="7ab1e-287">DevTools отфильтровать все ресурсы с именем файла, которое не оканчивается на a, а `j` `c` затем с 1 или более `s` символами.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-287">DevTools filters out any resource with a filename that does not end with a `j` or a `c` followed by 1 or more `s` characters.</span></span>  
    
    > ##### <span data-ttu-id="7ab1e-288">Рисунок 24</span><span class="sxs-lookup"><span data-stu-id="7ab1e-288">Figure 24</span></span>  
    > <span data-ttu-id="7ab1e-289">Фильтр регулярных выражений</span><span class="sxs-lookup"><span data-stu-id="7ab1e-289">A regular expression filter</span></span>  
    > <span data-ttu-id="7ab1e-290">! [Фильтр регулярных выражений] [ImagesTutorialRegEx]</span><span class="sxs-lookup"><span data-stu-id="7ab1e-290">![A regular expression filter][ImagesTutorialRegEx]</span></span>  
    
1.  <span data-ttu-id="7ab1e-291">Введите `-main.css`.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-291">Type `-main.css`.</span></span>  <span data-ttu-id="7ab1e-292">DevTools отфильтровать `main.css` .</span><span class="sxs-lookup"><span data-stu-id="7ab1e-292">DevTools filters out `main.css`.</span></span>  <span data-ttu-id="7ab1e-293">Если какой – либо другой файл соответствует шаблону, он также будет исключен.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-293">If any other file matched the pattern they would also be filtered out.</span></span>  
    
    > ##### <span data-ttu-id="7ab1e-294">Рис. 25</span><span class="sxs-lookup"><span data-stu-id="7ab1e-294">Figure 25</span></span>  
    > <span data-ttu-id="7ab1e-295">Отрицательный фильтр</span><span class="sxs-lookup"><span data-stu-id="7ab1e-295">A negative filter</span></span>  
    > <span data-ttu-id="7ab1e-296">! [Отрицательный фильтр] [ImagesTutorialNegative]</span><span class="sxs-lookup"><span data-stu-id="7ab1e-296">![A negative filter][ImagesTutorialNegative]</span></span>  
    
1.  <span data-ttu-id="7ab1e-297">Введите `domain:cdn.glitch.com` текст в текстовое поле **Фильтр** .</span><span class="sxs-lookup"><span data-stu-id="7ab1e-297">Type `domain:cdn.glitch.com` into the **Filter** text box.</span></span>  <span data-ttu-id="7ab1e-298">DevTools отфильтровать все ресурсы с URL-адресом, который не соответствует этому домену.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-298">DevTools filters out any resource with a URL that does not match this domain.</span></span>  
    
    > ##### <span data-ttu-id="7ab1e-299">Рис. 26</span><span class="sxs-lookup"><span data-stu-id="7ab1e-299">Figure 26</span></span>  
    > <span data-ttu-id="7ab1e-300">Фильтр свойств</span><span class="sxs-lookup"><span data-stu-id="7ab1e-300">A property filter</span></span>  
    > <span data-ttu-id="7ab1e-301">! [Фильтр свойств] [ImagesTutorialProperty]</span><span class="sxs-lookup"><span data-stu-id="7ab1e-301">![A property filter][ImagesTutorialProperty]</span></span>  

    <span data-ttu-id="7ab1e-302">Просмотрите [запросы фильтрации по свойствам][DevtoolsReferenceProperty] для полного списка фильтруемых свойств.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-302">See [Filter requests by properties][DevtoolsReferenceProperty] for the full list of filterable properties.</span></span>  
    
    
1.  <span data-ttu-id="7ab1e-303">Очистите текстовое поле " **Фильтр** " в любом тексте.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-303">Clear the **Filter** text box of any text.</span></span>  

### <span data-ttu-id="7ab1e-304">Фильтрация по типу ресурсов</span><span class="sxs-lookup"><span data-stu-id="7ab1e-304">Filter by resource type</span></span>   

<span data-ttu-id="7ab1e-305">Чтобы сосредоточиться на файле определенного типа, например в таблицах стилей, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-305">To focus in on a certain type of file, such as stylesheets:</span></span>  

1.  <span data-ttu-id="7ab1e-306">Выберите **CSS**.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-306">Select **CSS**.</span></span>  <span data-ttu-id="7ab1e-307">Все остальные типы файлов будут отфильтрованы.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-307">All other file types are filtered out.</span></span>  
    
    > ##### <span data-ttu-id="7ab1e-308">На рисунке 27</span><span class="sxs-lookup"><span data-stu-id="7ab1e-308">Figure 27</span></span>  
    > <span data-ttu-id="7ab1e-309">Отображение только CSS файлов</span><span class="sxs-lookup"><span data-stu-id="7ab1e-309">Showing CSS files only</span></span>  
    > <span data-ttu-id="7ab1e-310">! [Показывать только файлы CSS] [ImagesTutorialCSS]</span><span class="sxs-lookup"><span data-stu-id="7ab1e-310">![Showing CSS files only][ImagesTutorialCSS]</span></span>  
    
1.  <span data-ttu-id="7ab1e-311">Чтобы также просмотреть сценарии, удерживайте клавишу `Control` \ (Windows \) или `Command` \ (macOS \), а затем выберите **JS**.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-311">To also see scripts, hold `Control` \(Windows\) or `Command` \(macOS\) and then select **JS**.</span></span>  
    
    > ##### <span data-ttu-id="7ab1e-312">Рис. 28</span><span class="sxs-lookup"><span data-stu-id="7ab1e-312">Figure 28</span></span>  
    > <span data-ttu-id="7ab1e-313">Отображение только файлов CSS и JS</span><span class="sxs-lookup"><span data-stu-id="7ab1e-313">Showing CSS and JS files only</span></span>  
    > <span data-ttu-id="7ab1e-314">! [Показывать только файлы CSS и JS] [ImagesTutorialCSSJS]</span><span class="sxs-lookup"><span data-stu-id="7ab1e-314">![Showing CSS and JS files only][ImagesTutorialCSSJS]</span></span>  
    
1.  <span data-ttu-id="7ab1e-315">Нажмите кнопку **все** , чтобы удалить фильтры и снова просмотреть все ресурсы.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-315">Select **All** to remove the filters and see all resources again.</span></span>  

<span data-ttu-id="7ab1e-316">Просмотр [запросов фильтрации][DevtoolsNetworkReferenceFilter] для других рабочих процессов фильтрации.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-316">See [Filter requests][DevtoolsNetworkReferenceFilter] for other filtering workflows.</span></span>  

## <span data-ttu-id="7ab1e-317">Блокировать запросы</span><span class="sxs-lookup"><span data-stu-id="7ab1e-317">Block requests</span></span>   

<span data-ttu-id="7ab1e-318">Как выглядит и работает страница при недоступности некоторых ресурсов страницы?</span><span class="sxs-lookup"><span data-stu-id="7ab1e-318">How does a page look and behave when some of the page resources are not available?</span></span>  <span data-ttu-id="7ab1e-319">Не удается полностью завершить его или он по-прежнему работает?</span><span class="sxs-lookup"><span data-stu-id="7ab1e-319">Does it fail completely, or is it still somewhat functional?</span></span>  <span data-ttu-id="7ab1e-320">Блокировка запросов на определение:</span><span class="sxs-lookup"><span data-stu-id="7ab1e-320">Block requests to find out:</span></span>  

1.  <span data-ttu-id="7ab1e-321">`Control` + `Shift` + `P` Чтобы открыть меню команд, нажмите клавиши \ (Windows \) или `Command` + `Shift` + `P` \ ( **Command Menu**macOS \).</span><span class="sxs-lookup"><span data-stu-id="7ab1e-321">Press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**.</span></span>  
    
    > ##### <span data-ttu-id="7ab1e-322">Рис. 29</span><span class="sxs-lookup"><span data-stu-id="7ab1e-322">Figure 29</span></span>  
    > <span data-ttu-id="7ab1e-323">Меню команд</span><span class="sxs-lookup"><span data-stu-id="7ab1e-323">The Command Menu</span></span>  
    > <span data-ttu-id="7ab1e-324">! [Меню команд] [ImagesTutorialCommandMenu]</span><span class="sxs-lookup"><span data-stu-id="7ab1e-324">![The Command Menu][ImagesTutorialCommandMenu]</span></span>  
    
1.  <span data-ttu-id="7ab1e-325">Введите `block` команду **Показать блокировку запросов**и нажмите кнопку `Enter` .</span><span class="sxs-lookup"><span data-stu-id="7ab1e-325">Type `block`, select **Show Request Blocking**, and press `Enter`.</span></span>  
    
    > ##### <span data-ttu-id="7ab1e-326">Рис. 30</span><span class="sxs-lookup"><span data-stu-id="7ab1e-326">Figure 30</span></span>  
    > <span data-ttu-id="7ab1e-327">Показать блокировку запросов</span><span class="sxs-lookup"><span data-stu-id="7ab1e-327">Show Request Blocking</span></span>  
    > <span data-ttu-id="7ab1e-328">! [Показать блокировку запросов] [ImagesTutorialBlock]</span><span class="sxs-lookup"><span data-stu-id="7ab1e-328">![Show Request Blocking][ImagesTutorialBlock]</span></span>  

1.  <span data-ttu-id="7ab1e-329">Нажмите кнопку **Добавить** шаблон ![ Добавить узор ][ImageAddIcon] .</span><span class="sxs-lookup"><span data-stu-id="7ab1e-329">Select **Add Pattern** ![Add Pattern][ImageAddIcon].</span></span>  
1.  <span data-ttu-id="7ab1e-330">Введите `main.css`.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-330">Type `main.css`.</span></span>  
    
    > ##### <span data-ttu-id="7ab1e-331">На рисунке 31</span><span class="sxs-lookup"><span data-stu-id="7ab1e-331">Figure 31</span></span>  
    > <span data-ttu-id="7ab1e-332">Снижающи</span><span class="sxs-lookup"><span data-stu-id="7ab1e-332">Blocking</span></span> `main.css`  
    > <span data-ttu-id="7ab1e-333">! [Блокировка Main. CSS] [ImagesTutorialAddBlock]</span><span class="sxs-lookup"><span data-stu-id="7ab1e-333">![Blocking main.css][ImagesTutorialAddBlock]</span></span>  
    
1.  <span data-ttu-id="7ab1e-334">Нажмите кнопку **Добавить**.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-334">Select **Add**.</span></span>  
1.  <span data-ttu-id="7ab1e-335">Перезагрузите страницу.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-335">Reload the page.</span></span>  <span data-ttu-id="7ab1e-336">Как и предполагалось, стиль страницы немного изменился, так как основная таблица стилей заблокирована.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-336">As expected, the styling of the page is slightly messed up because the main stylesheet has been blocked.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="7ab1e-337">`main.css`Строка в сетевом журнале.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-337">The `main.css` row in the Network Log.</span></span>  <span data-ttu-id="7ab1e-338">Красный текст означает, что ресурс заблокирован.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-338">The red text means that the resource was blocked.</span></span>
    
    > ##### <span data-ttu-id="7ab1e-339">Рисунок 32</span><span class="sxs-lookup"><span data-stu-id="7ab1e-339">Figure 32</span></span>  
    > `main.css` <span data-ttu-id="7ab1e-340">заблокирован</span><span class="sxs-lookup"><span data-stu-id="7ab1e-340">has been blocked</span></span>  
    > <span data-ttu-id="7ab1e-341">! [Main. CSS заблокирована] [ImagesTutorialBlockedStyles]</span><span class="sxs-lookup"><span data-stu-id="7ab1e-341">![main.css has been blocked][ImagesTutorialBlockedStyles]</span></span>  

1.  <span data-ttu-id="7ab1e-342">Снимите флажок **включить блокировку запросов** .</span><span class="sxs-lookup"><span data-stu-id="7ab1e-342">Deselect the **Enable request blocking** checkbox.</span></span>  

## <span data-ttu-id="7ab1e-343">Заключение</span><span class="sxs-lookup"><span data-stu-id="7ab1e-343">Conclusion</span></span>  

<span data-ttu-id="7ab1e-344">Поздравляем, вы завершили обучение.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-344">Congratulations, you have completed the tutorial.</span></span>  <span data-ttu-id="7ab1e-345">Теперь вы знаете, как использовать панель "сеть" в Microsoft Edge DevTools!</span><span class="sxs-lookup"><span data-stu-id="7ab1e-345">You now know how to use the Network panel in the Microsoft Edge DevTools!</span></span>






<span data-ttu-id="7ab1e-346">Обратитесь к [справочной][DevtoolsNetworkReference] информации по сети, чтобы узнать о возможностях DevTools проверки активности сети.</span><span class="sxs-lookup"><span data-stu-id="7ab1e-346">Check out the [Network Reference][DevtoolsNetworkReference] to discover more DevTools features related to inspecting network activity.</span></span>  

 



<!-- image links -->  

[ImageAddIcon]: /microsoft-edge/devtools-guide-chromium/media/add-icon.msft.png  
[ImageCloseIcon]: /microsoft-edge/devtools-guide-chromium/media/close-icon.msft.png  
[ImageFilterIcon]: /microsoft-edge/devtools-guide-chromium/media/filter-icon.msft.png  
[ImageFormatIcon]: /microsoft-edge/devtools-guide-chromium/media/format-icon.msft.png  
[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-icon.msft.png  
[ImageScreenshotsIcon]: /microsoft-edge/devtools-guide-chromium/media/screenshots-icon.msft.png  
[ImageSearchIcon]: /microsoft-edge/devtools-guide-chromium/media/search-icon.msft.png  
[ImageSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/settings-icon.msft.png

[ImagesTutorialDemo]: /microsoft-edge/devtools-guide-chromium/media/network-glitch-inspect-network-activity-demo.msft.png "Рисунок 1: демонстрация"  
<!--[ImagesTutorialWindows]: /microsoft-edge/devtools-guide-chromium/media/network-tutorial/windows.msft.png " old Figure 2: The demo in one window and this tutorial in a different window"  -->  
[ImagesTutorialConsole]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Console.MSFT.png "Рисунок 2: консоль"  
[ImagesTutorialDocked]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Console-Bottom.MSFT.png "Рисунок 3: DevTools закреплено в нижней части окна"  
[ImagesTutorialNetwork]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-Bottom.MSFT.png "Рисунок 4: DevTools закреплены в нижней части окна"  
[ImagesTutorialLog]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network.MSFT.png "Рисунок 5: журнал сети"  
[ImagesTutorialRuntime]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-New-Resource.MSFT.png "Рисунок 6: новый ресурс в сетевом журнале"  
[ImagesTutorialDomain]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-Edit-Column.MSFT.png "Рисунок 7: включение столбца домена"  
[ImagesTutorialThrottling]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-Throttling.MSFT.png "Рисунок 8: Включение регулирования"  
[ImagesTutorialSlow3G]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-Throttling-Slow-3G.MSFT.png "Рисунок 9: выбор медленного 3G"  
[ImagesTutorialHardReload]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Empty-Cache-and-Hard-Reset.MSFT.png "Рисунок 10: пустой кэш и окончательная перезагрузка"  
[ImagesTutorialAllScreenshots]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-screenshots.MSFT.png "Рисунок 11: снимки экрана загрузки страницы"  
[ImagesTutorialFirstScreenshot]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-screenshots-First.MSFT.png "Рисунок 12: сетевое действие, происходящее на первом снимке экрана"  
[ImagesTutorialHeaders]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-Resources-Headers.MSFT.png "Рисунок 13: вкладка" заголовки "  
[ImagesTutorialPreview]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-Resources-Preview.MSFT.png "Рисунок 14: вкладка" предварительный просмотр "  
[ImagesTutorialResponse]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-Resources-Response.MSFT.png "Рисунок 15: вкладка" ответ ""  
[ImagesTutorialTiming]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-Resources-Timing.MSFT.png "Рисунок 16: вкладка" время "  
[ImagesTutorialCloseTiming]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-Resources-Close-tabs.MSFT.png "Рисунок 17: кнопка" Закрыть "  
[ImagesTutorialSearch]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-Search-Empty.MSFT.png "Рисунок 18: область поиска"  
[ImagesTutorialResults]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-Search-Cache-Control.MSFT.png "Рисунок 19: результаты поиска для Cache-Control"  
[ImagesTutorialCache]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-Search-Cache-Control-Headers-Response-Headers.MSFT.png "Рисунок 20: результат поиска, выделенный на вкладке" заголовки "  
[ImagesTutorialCloseButtons]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-Search-Close.MSFT.png "Рисунок 21: кнопки" Закрыть "  
[ImagesTutorialFilters]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-Filter-Empty.MSFT.png "рис. 22: панель инструментов" фильтры "  
[ImagesTutorialPNG]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-Filter-PNG.MSFT.png "Рисунок 23: строковый фильтр"  
[ImagesTutorialRegEx]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-Filter-Regex.MSFT.png "Рисунок 24: фильтр регулярных выражений"  
[ImagesTutorialNegative]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-Filter-Negative-Statement.MSFT.png "Рисунок 25: отрицательный фильтр"  
[ImagesTutorialProperty]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-Filter-property-value.MSFT.png "Рисунок 26: фильтр по свойству"  
[ImagesTutorialCSS]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-Filter-File-Type-CSS.MSFT.png "Рисунок 27: показывать только файлы CSS"  
[ImagesTutorialCSSJS]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-Filter-File-Type-CSS-JS.MSFT.png "Рисунок 28: отображение только файлов CSS и JS"  
[ImagesTutorialCommandMenu]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-CLI-Empty.MSFT.png "Рисунок 29: меню команд"  
[ImagesTutorialBlock]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-CLI-Block.MSFT.png "рис. 30: Показать блокировку запросов"  
[ImagesTutorialAddBlock]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-CLI-Block-Add-pattern.MSFT.png "Рисунок 31: Блокировка Main. CSS"  
[ImagesTutorialBlockedStyles]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-CLI-Block-Main-CSS.MSFT.png "Рисунок 32: Main. CSS заблокирован"  

<!-- links -->  


<!--[CachePolicies]: ../../../web/tools/lighthouse/audits/cache-policy ""  -->  

[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Изменение положения DevTools Microsoft EDGE (Отстыковка, закрепить в нижней части, закрепить слева)"  
[DevtoolsNetworkReference]: /microsoft-edge/devtools-guide-chromium/network/reference "Справочник по анализу сети"
[DevtoolsNetworkReferenceFilter]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests "Запросы фильтрации — Справочник по анализу сети"  
[DevtoolsReferenceHideOverview]: /microsoft-edge/devtools-guide-chromium/network/reference#hide-the-overview-pane "Скрытие области обзора — Справка по анализу сети"
[DevtoolsReferenceProperty]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties "Фильтрация запросов по свойствам — Справочник по анализу сети"
[DevToolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Открыть Microsoft Edge DevTools"  
[DevtoolsSpeedGetStarted]: /microsoft-edge/devtools-guide-chromium/speed/get-started "Оптимизация скорости веб-сайта с помощью Microsoft Edge DevTools"  

[GlitchNetworkGetStarted]: https://microsoft-edge-chromium-devtools.glitch.me/static/network/getstarted.html "Пример проверки активности сети"  

[MDNHTTPCache]: https://developer.mozilla.org/docs/Web/HTTP/Caching "Кэширование HTTP | MDN"  

> [!NOTE]
> <span data-ttu-id="7ab1e-388">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7ab1e-388">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="7ab1e-389">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/network/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="7ab1e-389">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/network/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="7ab1e-391">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="7ab1e-391">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
