---
title: Справочник по консоли
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/24/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: bd2a610b48905c6651663d490b9c9f1a0a8c7674
ms.sourcegitcommit: 5cdc1626d5581b79c0f2ac4ea62e7f1974ebfa57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/27/2020
ms.locfileid: "10601789"
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





# <span data-ttu-id="09445-103">Справочник по консоли</span><span class="sxs-lookup"><span data-stu-id="09445-103">Console Reference</span></span>   



<span data-ttu-id="09445-104">Эта страница содержит ссылки на возможности, связанные с консолью Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="09445-104">This page is a reference of features related to the Microsoft Edge DevTools Console.</span></span>  <span data-ttu-id="09445-105">Предполагается, что вы уже знакомы с использованием консоли для просмотра сообщений в журнале и запуска JavaScript.</span><span class="sxs-lookup"><span data-stu-id="09445-105">It assumes that you are already familiar with using the Console to view logged messages and run JavaScript.</span></span>  <span data-ttu-id="09445-106">В противном случае ознакомьтесь [со статьей начало работы с JavaScript на консоли][DevToolsConsoleJavascript] и начните [работу с сообщениями в журнале на консоли][DevToolsConsoleLog].</span><span class="sxs-lookup"><span data-stu-id="09445-106">If not, see [Get Started With Running JavaScript In The Console][DevToolsConsoleJavascript] and [Get Started With Logging Messages In The Console][DevToolsConsoleLog].</span></span>  

<span data-ttu-id="09445-107">Если вы ищете ссылку API на функции, такие как `console.log()` , [Справочник по API консоли][DevToolsConsoleApi].</span><span class="sxs-lookup"><span data-stu-id="09445-107">If you are looking for the API reference on functions like `console.log()` see [Console API Reference][DevToolsConsoleApi].</span></span>  <span data-ttu-id="09445-108">Дополнительные сведения о функциях, таких как `monitorEvents()` [Справка по API для консольных утилит][DevToolsConsoleUtilities].</span><span class="sxs-lookup"><span data-stu-id="09445-108">For the reference on functions like `monitorEvents()` see [Console Utilities API Reference][DevToolsConsoleUtilities].</span></span>  

## <span data-ttu-id="09445-109">Открытие консоли</span><span class="sxs-lookup"><span data-stu-id="09445-109">Open the Console</span></span>   

<span data-ttu-id="09445-110">Вы можете открыть консоль как [панель](#open-the-console-panel) или как [вкладку в ящике](#open-the-console-tab-in-the-drawer).</span><span class="sxs-lookup"><span data-stu-id="09445-110">You may open the Console as a [panel](#open-the-console-panel) or as a [tab in the Drawer](#open-the-console-tab-in-the-drawer).</span></span>  

### <span data-ttu-id="09445-111">Открытие панели консоли</span><span class="sxs-lookup"><span data-stu-id="09445-111">Open the Console panel</span></span>   

<span data-ttu-id="09445-112">Нажмите клавиши `Control` + `Shift` + `J` \ (Windows \) или `Command` + `Option` + `J` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="09445-112">Press `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\).</span></span>  

> ##### <span data-ttu-id="09445-113">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="09445-113">Figure 1</span></span>  
> <span data-ttu-id="09445-114">Панель консоли</span><span class="sxs-lookup"><span data-stu-id="09445-114">The Console panel</span></span>  
> ![Панель консоли][ImageConsolePanel]  

<span data-ttu-id="09445-116">Чтобы открыть панель консоли из [меню команд][DevToolsCommandMenu], начните вводить текст, `Console` а затем запустите команду **Показать консоль** с индикатором **панели** рядом с ним.</span><span class="sxs-lookup"><span data-stu-id="09445-116">To open the Console panel from the [Command Menu][DevToolsCommandMenu], start typing `Console` and then run the **Show Console** command that has the **Panel** badge next to it.</span></span>  

> ##### <span data-ttu-id="09445-117">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="09445-117">Figure 2</span></span>  
> <span data-ttu-id="09445-118">Команда для отображения панели консоли</span><span class="sxs-lookup"><span data-stu-id="09445-118">The command for showing the Console panel</span></span>  
> ![Команда для отображения панели консоли][ImageCommandShowConsole]  

### <span data-ttu-id="09445-120">Открытие вкладки "консоль" в ящике</span><span class="sxs-lookup"><span data-stu-id="09445-120">Open the Console tab in the Drawer</span></span>   

<span data-ttu-id="09445-121">Нажмите `Escape` или щелкните **настроить DevTools** `...` и выберите пункт **Показать входной ящик консоли**.</span><span class="sxs-lookup"><span data-stu-id="09445-121">Press `Escape` or click **Customize And Control DevTools** `...` and then select **Show console drawer**.</span></span>  

> ##### <span data-ttu-id="09445-122">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="09445-122">Figure 3</span></span>  
> <span data-ttu-id="09445-123">Показать консольный ящик</span><span class="sxs-lookup"><span data-stu-id="09445-123">Show console drawer</span></span>  
> ![Показать консольный ящик][ImageShowConsoleDrawer]  

<span data-ttu-id="09445-125">Ящик появляется в нижней части окна DevTools и открывается вкладка **консоли** .</span><span class="sxs-lookup"><span data-stu-id="09445-125">The Drawer pops up at the bottom of your DevTools window, with the **Console** tab open.</span></span>  

> ##### <span data-ttu-id="09445-126">Рисунок4</span><span class="sxs-lookup"><span data-stu-id="09445-126">Figure 4</span></span>  
> <span data-ttu-id="09445-127">Вкладка «консоль» в ящике</span><span class="sxs-lookup"><span data-stu-id="09445-127">The Console tab in the Drawer</span></span>  
> ![Вкладка «консоль» в ящике][ImageDrawerConsole]  

<span data-ttu-id="09445-129">Чтобы открыть вкладку консоль в [меню команд][DevToolsCommandMenu], начните вводить текст, `Console` а затем запустите команду **Показать консоль** с индикатором **ящика** рядом с ним.</span><span class="sxs-lookup"><span data-stu-id="09445-129">To open the Console tab from the [Command Menu][DevToolsCommandMenu], start typing `Console` and then run the **Show Console** command that has the **Drawer** badge next to it.</span></span>  

> ##### <span data-ttu-id="09445-130">Рисунок 5</span><span class="sxs-lookup"><span data-stu-id="09445-130">Figure 5</span></span>  
> <span data-ttu-id="09445-131">Команда для отображения вкладки "консоль" в ящике</span><span class="sxs-lookup"><span data-stu-id="09445-131">The command for showing the Console tab in the Drawer</span></span>  
> ![Команда для отображения вкладки "консоль" в ящике][ImageShowDrawerCommand]  

### <span data-ttu-id="09445-133">Открытие параметров консоли</span><span class="sxs-lookup"><span data-stu-id="09445-133">Open Console Settings</span></span>   

<span data-ttu-id="09445-134">Щелкните Параметры консоли " **Параметры** консоли" ![ ][ImageSettingsButtonIcon] .</span><span class="sxs-lookup"><span data-stu-id="09445-134">Click **Console Settings** ![Console Settings][ImageSettingsButtonIcon].</span></span>  

> ##### <span data-ttu-id="09445-135">Рисунок6</span><span class="sxs-lookup"><span data-stu-id="09445-135">Figure 6</span></span>  
> <span data-ttu-id="09445-136">Параметры консоли</span><span class="sxs-lookup"><span data-stu-id="09445-136">Console Settings</span></span>  
> ![Параметры консоли][ImageConsoleSettings]  

<span data-ttu-id="09445-138">Ниже описаны ссылки для каждого параметра.</span><span class="sxs-lookup"><span data-stu-id="09445-138">The links below explain each setting:</span></span>  

*   [**<span data-ttu-id="09445-139">Скрыть сеть</span><span class="sxs-lookup"><span data-stu-id="09445-139">Hide Network</span></span>**](#hide-network-messages)  
*   [**<span data-ttu-id="09445-140">Сохранить журнал</span><span class="sxs-lookup"><span data-stu-id="09445-140">Preserve Log</span></span>**](#persist-messages-across-page-loads)  
*   [**<span data-ttu-id="09445-141">Только выделенный контекст</span><span class="sxs-lookup"><span data-stu-id="09445-141">Selected Context Only</span></span>**](#filter-out-messages-from-different-contexts)  
*   [**<span data-ttu-id="09445-142">Одинаковая группа</span><span class="sxs-lookup"><span data-stu-id="09445-142">Group Similar</span></span>**](#disable-message-grouping)  
*   [**<span data-ttu-id="09445-143">Запись в журнал XmlHttpRequest</span><span class="sxs-lookup"><span data-stu-id="09445-143">Log XmlHttpRequests</span></span>**](#log-xhr-and-fetch-requests)  
*   [**<span data-ttu-id="09445-144">Упреждающая Оценка</span><span class="sxs-lookup"><span data-stu-id="09445-144">Eager Evaluation</span></span>**](#disable-eager-evaluation)  
*   [**<span data-ttu-id="09445-145">Автозаполнение из истории</span><span class="sxs-lookup"><span data-stu-id="09445-145">Autocomplete From History</span></span>**](#disable-autocomplete-from-history)  

### <span data-ttu-id="09445-146">Открытие боковой панели консоли</span><span class="sxs-lookup"><span data-stu-id="09445-146">Open the Console Sidebar</span></span>   

<span data-ttu-id="09445-147">Нажмите кнопку **Показать боковую панель консоли** ![ ][ImageShowConsoleSidebarIcon] , чтобы показать боковую панель, что бывает полезно для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="09445-147">Click **Show Console Sidebar** ![Show Console Sidebar][ImageShowConsoleSidebarIcon] to show the Sidebar, which is useful for filtering.</span></span>  

> ##### <span data-ttu-id="09445-148">Рисунок7</span><span class="sxs-lookup"><span data-stu-id="09445-148">Figure 7</span></span>  
> <span data-ttu-id="09445-149">Боковая панель консоли</span><span class="sxs-lookup"><span data-stu-id="09445-149">Console Sidebar</span></span>  
> ![Боковая панель консоли][ImageConsoleSidebar]  

## <span data-ttu-id="09445-151">Просмотр сообщений</span><span class="sxs-lookup"><span data-stu-id="09445-151">View messages</span></span>   

<span data-ttu-id="09445-152">В этом разделе описаны возможности, которые позволят изменить способ представления сообщений на консоли.</span><span class="sxs-lookup"><span data-stu-id="09445-152">This section contains features that change how messages are presented in the Console.</span></span>  <span data-ttu-id="09445-153">В этом пошаговом руководстве показано, как [Просмотреть сообщения][DevToolsConsoleViewMessages] .</span><span class="sxs-lookup"><span data-stu-id="09445-153">See [View messages][DevToolsConsoleViewMessages] for a hands-on walkthrough.</span></span>  

### <span data-ttu-id="09445-154">Отключение группировки сообщений</span><span class="sxs-lookup"><span data-stu-id="09445-154">Disable message grouping</span></span>   

<span data-ttu-id="09445-155">[Откройте параметры консоли](#open-console-settings) и отключите **группу, как** отключить поведение группировки сообщений по умолчанию для консоли.</span><span class="sxs-lookup"><span data-stu-id="09445-155">[Open Console Settings](#open-console-settings) and disable **Group similar** to disable the default message grouping behavior of the Console.</span></span>  <span data-ttu-id="09445-156">Посмотрите, как [XHR журнал и](#log-xhr-and-fetch-requests) выводит запросы на получение примера.</span><span class="sxs-lookup"><span data-stu-id="09445-156">See [Log XHR and Fetch requests](#log-xhr-and-fetch-requests) for an example.</span></span>  

### <span data-ttu-id="09445-157">Регистрация запросов XHR и FETCH</span><span class="sxs-lookup"><span data-stu-id="09445-157">Log XHR and Fetch requests</span></span>   

<span data-ttu-id="09445-158">[Откройте параметры консоли](#open-console-settings) и включите в **журнал записи XMLHttpRequest** , чтобы регистрировать все `XMLHttpRequest` и `Fetch` запросы на консоли по мере их появления.</span><span class="sxs-lookup"><span data-stu-id="09445-158">[Open Console Settings](#open-console-settings) and enable **Log XMLHttpRequests** to log all `XMLHttpRequest` and `Fetch` requests to the Console as they happen.</span></span>  

> ##### <span data-ttu-id="09445-159">Рисунок8</span><span class="sxs-lookup"><span data-stu-id="09445-159">Figure 8</span></span>  
> <span data-ttu-id="09445-160">Ведение журнала `XMLHttpRequest` и `Fetch` запросы</span><span class="sxs-lookup"><span data-stu-id="09445-160">Logging `XMLHttpRequest` and `Fetch` requests</span></span>  
> ![Ведение журнала запросов на XMLHttpRequest и выборку][ImageXhrGrouped]  

<span data-ttu-id="09445-162">В верхнем сообщении на [рисунке 8](#figure-8) показано поведение по умолчанию для группировки консоли.</span><span class="sxs-lookup"><span data-stu-id="09445-162">The top message in [Figure 8](#figure-8) shows the default grouping behavior of the Console.</span></span>  <!--  [Figure 9](#figure-9) shows how the same log looks after [disabling message grouping](#disable-message-grouping).  -->  

<!--

> ##### Old Figure 9  
> How the logged `XMLHttpRequest` and `Fetch` requests look after ungrouping  
> ![How the logged XMLHttpRequest and Fetch requests look after ungrouping][ImageXhrUngrouped]  

-->

<!--todo: add example for ungrouping console items  -->  

### <span data-ttu-id="09445-163">Сохранение сообщений на загрузок страниц</span><span class="sxs-lookup"><span data-stu-id="09445-163">Persist messages across page loads</span></span>   

<span data-ttu-id="09445-164">По умолчанию консоль очищается каждый раз, когда вы загружаете новую страницу.</span><span class="sxs-lookup"><span data-stu-id="09445-164">By default the Console clears whenever you load a new page.</span></span>  <span data-ttu-id="09445-165">Чтобы сохранить сообщения на нескольких страницах, [откройте параметры консоли](#open-console-settings) и установите флажок **сохранить журнал** .</span><span class="sxs-lookup"><span data-stu-id="09445-165">To persist messages across page loads, [Open Console Settings](#open-console-settings) and then enable the **Preserve Log** checkbox.</span></span>  

### <span data-ttu-id="09445-166">Скрыть сетевые сообщения</span><span class="sxs-lookup"><span data-stu-id="09445-166">Hide network messages</span></span>   

<span data-ttu-id="09445-167">По умолчанию браузер записывает сетевые сообщения на **консоль**.</span><span class="sxs-lookup"><span data-stu-id="09445-167">By default the browser logs network messages to the **Console**.</span></span>  <span data-ttu-id="09445-168">Например, выбранное сообщение на [рис. 9](#figure-9) представляет код состояния `429` .</span><span class="sxs-lookup"><span data-stu-id="09445-168">For example, the selected message in [Figure 9](#figure-9) represents a status code of `429`.</span></span>  

> ##### <span data-ttu-id="09445-169">Рисунок9</span><span class="sxs-lookup"><span data-stu-id="09445-169">Figure 9</span></span>  
> <span data-ttu-id="09445-170">Сообщение 429 в консоли</span><span class="sxs-lookup"><span data-stu-id="09445-170">A 429 message in the Console</span></span>  
> <span data-ttu-id="09445-171">! [Сообщение 429 в консоли] [Image429Message]</span><span class="sxs-lookup"><span data-stu-id="09445-171">![A 429 message in the Console][Image429Message]</span></span>  

<span data-ttu-id="09445-172">Чтобы скрыть сетевые сообщения, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="09445-172">To hide network messages:</span></span>  

1.  <span data-ttu-id="09445-173">[Откройте параметры консоли](#open-console-settings).</span><span class="sxs-lookup"><span data-stu-id="09445-173">[Open Console Settings](#open-console-settings).</span></span>  
1.  <span data-ttu-id="09445-174">Включите флажок **Скрыть сеть** .</span><span class="sxs-lookup"><span data-stu-id="09445-174">Enable the **Hide Network** checkbox.</span></span>  

## <span data-ttu-id="09445-175">Фильтрация сообщений</span><span class="sxs-lookup"><span data-stu-id="09445-175">Filter messages</span></span>   

<span data-ttu-id="09445-176">Есть несколько способов отфильтровать сообщения на консоли.</span><span class="sxs-lookup"><span data-stu-id="09445-176">There are many ways to filter out messages in the Console.</span></span>  

### <span data-ttu-id="09445-177">Фильтрация сообщений браузера</span><span class="sxs-lookup"><span data-stu-id="09445-177">Filter out browser messages</span></span>   

<span data-ttu-id="09445-178">[Откройте панель консоли](#open-the-console-sidebar) и выберите пункт **сообщения пользователя** , чтобы отображались только те сообщения, которые были получены на странице JavaScript.</span><span class="sxs-lookup"><span data-stu-id="09445-178">[Open the Console Sidebar](#open-the-console-sidebar) and click **User Messages** to only show messages that came from the JavaScript of the page.</span></span>  

> ##### <span data-ttu-id="09445-179">Рисунок 10</span><span class="sxs-lookup"><span data-stu-id="09445-179">Figure 10</span></span>  
> <span data-ttu-id="09445-180">Просмотр сообщений пользователя</span><span class="sxs-lookup"><span data-stu-id="09445-180">Viewing user messages</span></span>  
> <span data-ttu-id="09445-181">! [Просмотр сообщений пользователей] [ImageUserMessages]</span><span class="sxs-lookup"><span data-stu-id="09445-181">![Viewing user messages][ImageUserMessages]</span></span>  

### <span data-ttu-id="09445-182">Фильтрация по уровню ведения журнала</span><span class="sxs-lookup"><span data-stu-id="09445-182">Filter by log level</span></span>   

<span data-ttu-id="09445-183">DevTools назначает каждому `console.*` методу уровень серьезности.</span><span class="sxs-lookup"><span data-stu-id="09445-183">DevTools assigns each `console.*` method a severity level.</span></span>  <span data-ttu-id="09445-184">Существует 4 уровня: `Verbose` ,, `Info` `Warning` , и `Error` .</span><span class="sxs-lookup"><span data-stu-id="09445-184">There are 4 levels: `Verbose`, `Info`, `Warning`, and `Error`.</span></span>  <span data-ttu-id="09445-185">Например, `console.log()` входит в `Info` группу, в то время как `console.error()` она находится в `Error` группе.</span><span class="sxs-lookup"><span data-stu-id="09445-185">For example, `console.log()` is in the `Info` group, whereas `console.error()` is in the `Error` group.</span></span>  <span data-ttu-id="09445-186">[Справочник по API консоли][DevToolsConsoleApi] описывает уровень важности каждого применимого метода.</span><span class="sxs-lookup"><span data-stu-id="09445-186">The [Console API Reference][DevToolsConsoleApi] describes the severity level of each applicable method.</span></span>  <span data-ttu-id="09445-187">Каждое сообщение, которое браузер записывает на консоль, также имеет уровень серьезности.</span><span class="sxs-lookup"><span data-stu-id="09445-187">Every message that the browser logs to the Console has a severity level too.</span></span>  <span data-ttu-id="09445-188">Вы можете скрыть любые ненужные сообщения.</span><span class="sxs-lookup"><span data-stu-id="09445-188">You may hide any level of messages that you are not interested in.</span></span>  <span data-ttu-id="09445-189">Например, если вы заинтересованы в `Error` сообщениях, вы можете скрыть другие три группы.</span><span class="sxs-lookup"><span data-stu-id="09445-189">For example, if you are only interested in `Error` messages, you may hide the other 3 groups.</span></span>  

<span data-ttu-id="09445-190">Щелкните раскрывающийся список **уровни журнала** , чтобы включить или отключить `Verbose` , `Info` `Warning` или `Error` сообщения.</span><span class="sxs-lookup"><span data-stu-id="09445-190">Click the **Log Levels** dropdown to enable or disable `Verbose`, `Info`, `Warning` or `Error` messages.</span></span>  

> ##### <span data-ttu-id="09445-191">Рисунок11</span><span class="sxs-lookup"><span data-stu-id="09445-191">Figure 11</span></span>  
> <span data-ttu-id="09445-192">Раскрывающийся список **уровней журнала**</span><span class="sxs-lookup"><span data-stu-id="09445-192">The **Log Levels** dropdown</span></span>  
> <span data-ttu-id="09445-193">! [Раскрывающийся список уровней журнала] [ImageLogLevels]</span><span class="sxs-lookup"><span data-stu-id="09445-193">![The Log Levels dropdown][ImageLogLevels]</span></span>  

<span data-ttu-id="09445-194">Вы также можете отфильтровать по уровню журнала, [открыв боковую панель консоли](#open-the-console-sidebar) и выбрав пункт **ошибки**, **предупреждения**, **сведения**или **подробный**.</span><span class="sxs-lookup"><span data-stu-id="09445-194">You may also filter by log level by [opening the Console Sidebar](#open-the-console-sidebar) and then clicking **Errors**, **Warnings**, **Info**, or **Verbose**.</span></span>  

> ##### <span data-ttu-id="09445-195">Рисунок12</span><span class="sxs-lookup"><span data-stu-id="09445-195">Figure 12</span></span>  
> <span data-ttu-id="09445-196">Использование боковой панели для просмотра предупреждений</span><span class="sxs-lookup"><span data-stu-id="09445-196">Using the Sidebar to view warnings</span></span>  
> <span data-ttu-id="09445-197">! [Использование боковой панели для просмотра предупреждений] [ImageSidebarWarnings]</span><span class="sxs-lookup"><span data-stu-id="09445-197">![Using the Sidebar to view warnings][ImageSidebarWarnings]</span></span>  

### <span data-ttu-id="09445-198">Фильтрация сообщений по URL-адресу</span><span class="sxs-lookup"><span data-stu-id="09445-198">Filter messages by URL</span></span>   

<span data-ttu-id="09445-199">Введите и `url:` URL-адрес, чтобы просматривать только те сообщения, которые были отправлены из этого URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="09445-199">Type `url:` followed by a URL to only view messages that came from that URL.</span></span>  <span data-ttu-id="09445-200">После ввода `url:` DevTools появятся все нужные URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="09445-200">After you type `url:` DevTools shows all relevant URLs.</span></span>  <span data-ttu-id="09445-201">Домены также работают.</span><span class="sxs-lookup"><span data-stu-id="09445-201">Domains also work.</span></span>  <span data-ttu-id="09445-202">Например, если `https://example.com/a.js` `https://example.com/b.js` сообщения записываются в журнал, `url:https://example.com` вы можете сосредоточиться на сообщениях из этих 2 сценариев.</span><span class="sxs-lookup"><span data-stu-id="09445-202">For example, if `https://example.com/a.js` and `https://example.com/b.js` are logging messages, `url:https://example.com` enables you to focus on the messages from these 2 scripts.</span></span>  

> ##### <span data-ttu-id="09445-203">Рисунок13</span><span class="sxs-lookup"><span data-stu-id="09445-203">Figure 13</span></span>  
> <span data-ttu-id="09445-204">Фильтр URL-адреса</span><span class="sxs-lookup"><span data-stu-id="09445-204">A URL filter</span></span>  
> <span data-ttu-id="09445-205">! [Фильтр URL-адреса] [ImageUrlFilter]</span><span class="sxs-lookup"><span data-stu-id="09445-205">![A URL filter][ImageUrlFilter]</span></span>  

<span data-ttu-id="09445-206">Введите текст `-url:` , чтобы скрыть сообщения от этого URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="09445-206">Type `-url:` to hide messages from that URL.</span></span>  <span data-ttu-id="09445-207">Это называется фильтром отрицательных URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="09445-207">This is called a negative URL filter.</span></span>  

> ##### <span data-ttu-id="09445-208">Рисунок14</span><span class="sxs-lookup"><span data-stu-id="09445-208">Figure 14</span></span>  
> <span data-ttu-id="09445-209">Фильтр отрицательных URL-адресов, который скрывает все сообщения, соответствующие URL-адресу</span><span class="sxs-lookup"><span data-stu-id="09445-209">A negative URL filter that hides all messages matching the URL</span></span> `https://b.wal.co`  
> <span data-ttu-id="09445-210">! [Фильтр по отрицательному URL-адресу, который скрывает все сообщения, соответствующие URL-адресу https://b.wal.co ] [ImageNegativeUrlFilter1]</span><span class="sxs-lookup"><span data-stu-id="09445-210">![A negative URL filter that hides all messages matching the URL https://b.wal.co][ImageNegativeUrlFilter1]</span></span>  

<span data-ttu-id="09445-211">Вы также можете показывать сообщения с одного URL-адреса, [открыв боковую панель консоли](#open-the-console-sidebar), развернув раздел " **пользовательские сообщения** ", а затем щелкнув URL-адрес сценария, содержащего сообщения, на которые нужно обратить внимание.</span><span class="sxs-lookup"><span data-stu-id="09445-211">You may also show messages from a single URL by [opening the Console Sidebar](#open-the-console-sidebar), expanding the **User Messages** section, and then clicking the URL of the script containing the messages on which you want to focus.</span></span>  

> ##### <span data-ttu-id="09445-212">Рисунок15</span><span class="sxs-lookup"><span data-stu-id="09445-212">Figure 15</span></span>  
> <span data-ttu-id="09445-213">Просмотр сообщений, которые были получены</span><span class="sxs-lookup"><span data-stu-id="09445-213">Viewing the messages that came from</span></span> `wp-ad.min.js`  
> <span data-ttu-id="09445-214">! [Просмотр сообщений, поступивших из WP-AD. min. js] [ImageNegativeUrlFilter2]</span><span class="sxs-lookup"><span data-stu-id="09445-214">![Viewing the messages that came from wp-ad.min.js][ImageNegativeUrlFilter2]</span></span>  

### <span data-ttu-id="09445-215">Фильтрация сообщений в разных контекстах</span><span class="sxs-lookup"><span data-stu-id="09445-215">Filter out messages from different contexts</span></span>   

<span data-ttu-id="09445-216">Предположим, что у вас есть реклама \ (AD) на вашей странице.</span><span class="sxs-lookup"><span data-stu-id="09445-216">Suppose that you have an advertisement \(ad\) on your page.</span></span>  <span data-ttu-id="09445-217">Рекламное объявление встраивается в приложение `<iframe>` и создает большое количество сообщений на консоли.</span><span class="sxs-lookup"><span data-stu-id="09445-217">The ad is embedded in an `<iframe>` and is generating a lot of messages in your Console.</span></span>  <span data-ttu-id="09445-218">Так как объявление запущено в другом [контексте JavaScript](#select-javascript-context), один из способов скрыть сообщения — [открыть параметры консоли](#open-console-settings) и установить флажок **только выбранный контекст** .</span><span class="sxs-lookup"><span data-stu-id="09445-218">Because the ad is running in a different [JavaScript context](#select-javascript-context), one way to hide the messages is to [open Console Settings](#open-console-settings) and enable the **Selected Context Only** checkbox.</span></span>  

### <span data-ttu-id="09445-219">Фильтрация сообщений, не соответствующих шаблону регулярного выражения</span><span class="sxs-lookup"><span data-stu-id="09445-219">Filter out messages that do not match a regular expression pattern</span></span>   

<span data-ttu-id="09445-220">Введите регулярное выражение, например `/[gm][ta][mi]/` в текстовое поле **Фильтр** , чтобы отфильтровать сообщения, которые не соответствуют этому шаблону.</span><span class="sxs-lookup"><span data-stu-id="09445-220">Type a regular expression such as `/[gm][ta][mi]/` in the **Filter** text box to filter out any messages that do not match that pattern.</span></span>  <span data-ttu-id="09445-221">DevTools проверяет, найден ли шаблон в тексте сообщения или сценарий, который привел к занесению в журнал сообщения.</span><span class="sxs-lookup"><span data-stu-id="09445-221">DevTools checks if the pattern is found in the message text or the script that caused the message to be logged.</span></span>  

> ##### <span data-ttu-id="09445-222">Рисунок16</span><span class="sxs-lookup"><span data-stu-id="09445-222">Figure 16</span></span>  
> <span data-ttu-id="09445-223">Фильтрация несовпадающих сообщений</span><span class="sxs-lookup"><span data-stu-id="09445-223">Filtering out any messages that do not match</span></span> `/[gm][ta][mi]/`  
> <span data-ttu-id="09445-224">! [Фильтрация сообщений, не соответствующих выражению Regex] [ImageRegExFilter]</span><span class="sxs-lookup"><span data-stu-id="09445-224">![Filtering out any messages that do not match regex expression][ImageRegExFilter]</span></span>  

## <span data-ttu-id="09445-225">Запуск JavaScript</span><span class="sxs-lookup"><span data-stu-id="09445-225">Run JavaScript</span></span>   

<span data-ttu-id="09445-226">В этом разделе описаны возможности, связанные с выполнением JavaScript на консоли.</span><span class="sxs-lookup"><span data-stu-id="09445-226">This section contains features related to running JavaScript in the Console.</span></span>  <span data-ttu-id="09445-227">В этом пошаговом руководстве показано, как [запускать JavaScript][DevToolsConsoleOverviewJavascript] .</span><span class="sxs-lookup"><span data-stu-id="09445-227">See [Run JavaScript][DevToolsConsoleOverviewJavascript] for a hands-on walkthrough.</span></span>  

### <span data-ttu-id="09445-228">Повторное выполнение выражений из истории</span><span class="sxs-lookup"><span data-stu-id="09445-228">Re-run expressions from history</span></span>   

<span data-ttu-id="09445-229">Нажмите клавишу `Up Arrow` для циклического просмотра истории выражений JavaScript, которые выполнялись на консоли раньше.</span><span class="sxs-lookup"><span data-stu-id="09445-229">Press the `Up Arrow` key to cycle through the history of JavaScript expressions that you ran earlier in the Console.</span></span>  <span data-ttu-id="09445-230">Нажмите кнопку `Enter` , чтобы выполнить это выражение еще раз.</span><span class="sxs-lookup"><span data-stu-id="09445-230">Press `Enter` to run that expression again.</span></span>  

### <span data-ttu-id="09445-231">Просмотр значения выражения в режиме реального времени с помощью выражений с реальными данными</span><span class="sxs-lookup"><span data-stu-id="09445-231">Watch the value of an expression in real-time with Live Expressions</span></span>   

<span data-ttu-id="09445-232">Если вы обнаружите, что один и тот же выражение JavaScript будет вводиться повторно в консоль, возможно, вам будет проще создать **выражение в реальном времени**.</span><span class="sxs-lookup"><span data-stu-id="09445-232">If you find yourself typing the same JavaScript expression in the Console repeatedly, you may find it easier to create a **Live Expression**.</span></span>  <span data-ttu-id="09445-233">С помощью **выражений в реальном времени** вы вводите выражение один раз, а затем закрепите его в верхней части консоли.</span><span class="sxs-lookup"><span data-stu-id="09445-233">With **Live Expressions** you type an expression once and then pin it to the top of your Console.</span></span>  <span data-ttu-id="09445-234">Значение выражения обновляется почти в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="09445-234">The value of the expression updates in near real-time.</span></span>  <span data-ttu-id="09445-235">Просмотрите [значения выражений JavaScript в реальном времени с помощью выражений с реальными данными][DevToolsConsoleLiveExpressions].</span><span class="sxs-lookup"><span data-stu-id="09445-235">See [Watch JavaScript Expression Values In Real-Time With Live Expressions][DevToolsConsoleLiveExpressions].</span></span>  

### <span data-ttu-id="09445-236">Отключение безотлагательной оценки</span><span class="sxs-lookup"><span data-stu-id="09445-236">Disable Eager Evaluation</span></span>   

<span data-ttu-id="09445-237">По мере ввода выражений JavaScript в консоли **упреждающая Оценка** показывает предварительный просмотр возвращаемого значения для этого выражения.</span><span class="sxs-lookup"><span data-stu-id="09445-237">As you type JavaScript expressions in the Console, **Eager Evaluation** shows a preview of the return value for that expression.</span></span>  <span data-ttu-id="09445-238">[Откройте параметры консоли](#open-console-settings) и отключите флажок **упреждающая Оценка** , чтобы отключить предварительный просмотр возвращаемых значений.</span><span class="sxs-lookup"><span data-stu-id="09445-238">[Open Console Settings](#open-console-settings) and disable the **Eager Evaluation** checkbox to turn off the return value previews.</span></span>  

### <span data-ttu-id="09445-239">Отключение автозаполнения из истории</span><span class="sxs-lookup"><span data-stu-id="09445-239">Disable autocomplete from history</span></span>   

<span data-ttu-id="09445-240">По мере ввода выражения в всплывающем окне для консоли отображаются выражения, которые были выполнены раньше.</span><span class="sxs-lookup"><span data-stu-id="09445-240">As you type out an expression, the autocomplete popup window for the Console shows expressions that you ran earlier.</span></span>  <span data-ttu-id="09445-241">Эти выражения добавляются в начале `>` символа.</span><span class="sxs-lookup"><span data-stu-id="09445-241">These expressions are prepended with the `>` character.</span></span>  <span data-ttu-id="09445-242">[Откройте меню Параметры консоли](#open-console-settings) и отключите флажок **Автозаполнение из журнала** , чтобы отключить отображение выражений из истории.</span><span class="sxs-lookup"><span data-stu-id="09445-242">[Open Console Settings](#open-console-settings) and disable the **Autocomplete From History** checkbox to stop showing expressions from your history.</span></span>  

> [!NOTE]
> <span data-ttu-id="09445-243">На [рис](#figure-17). 17 `document.querySelector('a')` и `document.querySelector('img')` выражения, которые были оценены ранее.</span><span class="sxs-lookup"><span data-stu-id="09445-243">In [Figure 17](#figure-17), `document.querySelector('a')` and `document.querySelector('img')` are expressions that were evaluated earlier.</span></span>  

> ##### <span data-ttu-id="09445-244">Рисунок17</span><span class="sxs-lookup"><span data-stu-id="09445-244">Figure 17</span></span>  
> <span data-ttu-id="09445-245">Всплывающее окно "Автозаполнение", в котором отображаются выражения из истории</span><span class="sxs-lookup"><span data-stu-id="09445-245">The autocomplete popup showing expressions from history</span></span>  
> <span data-ttu-id="09445-246">! [Всплывающее окно "Автозаполнение", в котором отображаются выражения из истории] [ImageHistoryAutocomplete]</span><span class="sxs-lookup"><span data-stu-id="09445-246">![The autocomplete popup showing expressions from history][ImageHistoryAutocomplete]</span></span>  

### <span data-ttu-id="09445-247">Выбор контекста JavaScript</span><span class="sxs-lookup"><span data-stu-id="09445-247">Select JavaScript context</span></span>   

<span data-ttu-id="09445-248">По умолчанию раскрывающийся список **контекстов JavaScript** имеет значение **Top**, которое представляет [контекст просмотра][MDNBrowsingContext] основного документа.</span><span class="sxs-lookup"><span data-stu-id="09445-248">By default the **JavaScript Context** dropdown is set to **top**, which represents the [browsing context][MDNBrowsingContext] of the main document.</span></span>  

> ##### <span data-ttu-id="09445-249">Рис. 18</span><span class="sxs-lookup"><span data-stu-id="09445-249">Figure 18</span></span>  
> <span data-ttu-id="09445-250">Раскрывающийся список **контекстов JavaScript**</span><span class="sxs-lookup"><span data-stu-id="09445-250">The **JavaScript Context** dropdown</span></span>  
> <span data-ttu-id="09445-251">! [Раскрывающийся список контекстов JavaScript] [ImageJavascriptContext]</span><span class="sxs-lookup"><span data-stu-id="09445-251">![The JavaScript Context dropdown][ImageJavascriptContext]</span></span>  

<span data-ttu-id="09445-252">Предположим, что у вас есть реклама на странице, внедренная в `<iframe>` .</span><span class="sxs-lookup"><span data-stu-id="09445-252">Suppose you have an ad on your page embedded in an `<iframe>`.</span></span>  <span data-ttu-id="09445-253">Вы хотите запустить JavaScript, чтобы настроить модель DOM рекламы.</span><span class="sxs-lookup"><span data-stu-id="09445-253">You want to run JavaScript in order to tweak the DOM of the ad.</span></span>  <span data-ttu-id="09445-254">Сначала необходимо выбрать контекст обзора рекламы из раскрывающегося списка **контекстов JavaScript** .</span><span class="sxs-lookup"><span data-stu-id="09445-254">You should first select the browsing context of the ad from the **JavaScript Context** dropdown.</span></span>  

> ##### <span data-ttu-id="09445-255">На рисунке 19</span><span class="sxs-lookup"><span data-stu-id="09445-255">Figure 19</span></span>  
> <span data-ttu-id="09445-256">Выбор другого контекста JavaScript</span><span class="sxs-lookup"><span data-stu-id="09445-256">Selecting a different JavaScript context</span></span>  
> <span data-ttu-id="09445-257">! [Выбор другого контекста JavaScript] [ImageSelectContext]</span><span class="sxs-lookup"><span data-stu-id="09445-257">![Selecting a different JavaScript context][ImageSelectContext]</span></span>  

## <span data-ttu-id="09445-258">Очистка консоли</span><span class="sxs-lookup"><span data-stu-id="09445-258">Clear the Console</span></span>   

<span data-ttu-id="09445-259">Чтобы очистить консоль, вы можете использовать любой из следующих рабочих процессов:</span><span class="sxs-lookup"><span data-stu-id="09445-259">You may use any of the following workflows to clear the Console:</span></span>  

*   <span data-ttu-id="09445-260">Нажмите кнопку **Очистить консоль** "очистить консоль" ![ ][ImageClearConsoleIcon] .</span><span class="sxs-lookup"><span data-stu-id="09445-260">Click **Clear Console** ![Clear Console][ImageClearConsoleIcon].</span></span>  
*   <span data-ttu-id="09445-261">Щелкните сообщение правой кнопкой мыши и выберите команду **Очистить консоль**.</span><span class="sxs-lookup"><span data-stu-id="09445-261">Right-click a message and then select **Clear Console**.</span></span>  
*   <span data-ttu-id="09445-262">Введите текст `clear()` на консоли и нажмите клавишу `Enter` .</span><span class="sxs-lookup"><span data-stu-id="09445-262">Type `clear()` in the Console and then press `Enter`.</span></span>  
*   <span data-ttu-id="09445-263">Вызов `console.clear()` из JavaScript на веб-странице.</span><span class="sxs-lookup"><span data-stu-id="09445-263">Call `console.clear()` from the JavaScript for your webpage.</span></span>  
*   <span data-ttu-id="09445-264">Нажимайте кнопку, `Control` + `L` пока фокус находится на консоли.</span><span class="sxs-lookup"><span data-stu-id="09445-264">Press `Control`+`L` while the Console is in focus.</span></span>  

 



<!-- image links -->  

[ImageClearConsoleIcon]: /microsoft-edge/devtools-guide-chromium/media/clear-console-button-icon.msft.png  
[ImageSettingsButtonIcon]: /microsoft-edge/devtools-guide-chromium/media/settings-button-icon.msft.png  
[ImageShowConsoleSidebarIcon]: /microsoft-edge/devtools-guide-chromium/media/show-console-sidebar-icon.msft.png  

[ImageConsolePanel]: /microsoft-edge/devtools-guide-chromium/media/console-hello-console.msft.png "Рисунок 1: панель консоли"  
[ImageCommandShowConsole]: /microsoft-edge/devtools-guide-chromium/media/console-command-menu-show-console.msft.png "Рисунок 2: команда для отображения панели консоли"  
[ImageShowConsoleDrawer]: /microsoft-edge/devtools-guide-chromium/media/console-elements-customize-control-devtools-show-console-drawer.msft.png "Рисунок 3: отображение консольного ящика"  
[ImageDrawerConsole]: /microsoft-edge/devtools-guide-chromium/media/console-elements-console-drawer-hello-world.msft.png "Рисунок 4: вкладка «консоль» в ящике"  
[ImageShowDrawerCommand]: /microsoft-edge/devtools-guide-chromium/media/console-command-menu-show-console.msft.png "Рисунок 5: команда для отображения вкладки "консоль" в ящике"  
[ImageConsoleSettings]: /microsoft-edge/devtools-guide-chromium/media/console-settings-group-similar-empty.msft.png "Рисунок 6: параметры консоли"  
[ImageConsoleSidebar]: /microsoft-edge/devtools-guide-chromium/media/console-sidebar-drawer-empty.msft.png "Рисунок 7: Боковая панель консоли"  
[ImageXhrGrouped]: /microsoft-edge/devtools-guide-chromium/media/console-xhr-fetch.msft.png "Рисунок 8: регистрация запросов на XMLHttpRequest и выборку данных"  
<!--[ImageXhrUngrouped]: /microsoft-edge/devtools-guide-chromium/media/console-xhr-fetch-all.msft.png "Figure old 9: How the logged XMLHttpRequest and Fetch requests look after ungrouping"  -->  
[Image429Message]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Console-Show-Network.MSFT.png "Рисунок 9: сообщение 429 в консоли"  
[ImageUserMessages]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Console-sidebar-drawer-User-messages.MSFT.png "Рисунок 10: Просмотр сообщений пользователя"  
[ImageLogLevels]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Console-Log-Level-Default-Levels.MSFT.png "Рисунок 11: раскрывающийся список" уровни журнала ""  
[ImageSidebarWarnings]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Console-sidebar-Warnings.MSFT.png "Рисунок 12: Использование боковой панели для просмотра предупреждений"  
[ImageUrlFilter]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Console-Filter-Text.MSFT.png "Рисунок 13: фильтр URL-адреса"  
[ImageNegativeUrlFilter1]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Console-Negative-Filter-Text.MSFT.png "Рисунок 14: фильтр отрицательных URL-адресов, который скрывает все сообщения, соответствующие URL-адресу https://b.wal.co "  
[ImageNegativeUrlFilter2]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Console-Filter-Text-Specified.MSFT.png "Рисунок 15: Просмотр сообщений, поступивших из WP-AD. min. js"  
[ImageRegExFilter]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Console-Filter-Regex.MSFT.png "Рисунок 16: Фильтрация сообщений, не соответствующих выражению Regex"  
[ImageHistoryAutocomplete]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Console-Filter-Text-AutoFilter-History.MSFT.png "Рисунок 17: всплывающее окно" Автозаполнение ", в котором отображаются выражения из истории"  
[ImageJavascriptContext]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Console-DOM-Level-Top.MSFT.png "Рисунок 18: раскрывающийся список контекстов JavaScript"  
[ImageSelectContext]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Console-DOM-Level-Multiple.MSFT.png "Рисунок 19: выбор другого контекста JavaScript"  

<!-- links -->  

[DevToolsCommandMenu]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Выполнение команд с помощью командного меню Microsoft Edge DevTools"  
[DevToolsConsoleViewMessages]: /microsoft-edge/devtools-guide-chromium/console/index#viewing-logged-messages "Просмотр сообщений с запротоколированием — обзор консоли"  
[DevToolsConsoleApi]: /microsoft-edge/devtools-guide-chromium/console/api "Справочник по API консоли"  
[DevToolsConsoleOverviewJavascript]: /microsoft-edge/devtools-guide-chromium/console/index#running-javascript "Выполнение JavaScript — обзор консоли"  
[DevToolsConsoleJavascript]: /microsoft-edge/devtools-guide-chromium/console/javascript "Начало работы с JavaScript на консоли"  
[DevToolsConsoleLiveExpressions]: /microsoft-edge/devtools-guide-chromium/console/live-expressions "Контроль значений выражений JavaScript в режиме реального времени с помощью выражений в реальном масштабе"  
[DevToolsConsoleLog]: /microsoft-edge/devtools-guide-chromium/console/log "Начало работы с сообщениями журнала на консоли"  
[DevToolsConsoleUtilities]: /microsoft-edge/devtools-guide-chromium/console/utilities "Справочник по API для консольных программ"  

[MDNBrowsingContext]: https://developer.mozilla.org/docs/Glossary/Browsing_context "Контекст просмотра | MDN"  

> [!NOTE]
> <span data-ttu-id="09445-293">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="09445-293">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="09445-294">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/console/reference) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="09445-294">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="09445-296">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="09445-296">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
