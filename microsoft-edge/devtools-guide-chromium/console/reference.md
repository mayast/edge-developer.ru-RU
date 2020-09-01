---
title: Справочник по консоли
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 51a85c3dad121dcb42633390de9b4e817074546e
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2020
ms.locfileid: "10982500"
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





# <span data-ttu-id="17282-103">Справочник по консоли</span><span class="sxs-lookup"><span data-stu-id="17282-103">Console Reference</span></span>   



<span data-ttu-id="17282-104">Эта страница содержит ссылки на возможности, связанные с консолью Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="17282-104">This page is a reference of features related to the Microsoft Edge DevTools Console.</span></span>  <span data-ttu-id="17282-105">Предполагается, что вы уже знакомы с использованием консоли для просмотра сообщений в журнале и запуска JavaScript.</span><span class="sxs-lookup"><span data-stu-id="17282-105">It assumes that you are already familiar with using the Console to view logged messages and run JavaScript.</span></span>  <span data-ttu-id="17282-106">В противном случае ознакомьтесь [со статьей начало работы с JavaScript на консоли][DevToolsConsoleJavascript] и начните [работу с сообщениями в журнале на консоли][DevToolsConsoleLog].</span><span class="sxs-lookup"><span data-stu-id="17282-106">If not, see [Get Started With Running JavaScript In The Console][DevToolsConsoleJavascript] and [Get Started With Logging Messages In The Console][DevToolsConsoleLog].</span></span>  

<span data-ttu-id="17282-107">Если вы ищете ссылку API на функции, такие как `console.log()` , [Справочник по API консоли][DevToolsConsoleApi].</span><span class="sxs-lookup"><span data-stu-id="17282-107">If you are looking for the API reference on functions like `console.log()` see [Console API Reference][DevToolsConsoleApi].</span></span>  <span data-ttu-id="17282-108">Справку по функциям, например `monitorEvents()` , можно найти в [справочнике API для консольных утилит][DevToolsConsoleUtilities].</span><span class="sxs-lookup"><span data-stu-id="17282-108">For the reference on functions like `monitorEvents()`, see [Console Utilities API Reference][DevToolsConsoleUtilities].</span></span>  

## <span data-ttu-id="17282-109">Открытие консоли</span><span class="sxs-lookup"><span data-stu-id="17282-109">Open the Console</span></span>   

<span data-ttu-id="17282-110">Вы можете открыть консоль как [панель](#open-the-console-panel) или как [вкладку в ящике](#open-the-console-tab-in-the-drawer).</span><span class="sxs-lookup"><span data-stu-id="17282-110">You may open the Console as a [panel](#open-the-console-panel) or as a [tab in the Drawer](#open-the-console-tab-in-the-drawer).</span></span>  

### <span data-ttu-id="17282-111">Открытие панели консоли</span><span class="sxs-lookup"><span data-stu-id="17282-111">Open the Console panel</span></span>   

<span data-ttu-id="17282-112">Нажмите клавиши `Control` + `Shift` + `J` \ (Windows \) или `Command` + `Option` + `J` \ (macOS \).</span><span class="sxs-lookup"><span data-stu-id="17282-112">Press `Control`+`Shift`+`J` \(Windows\) or `Command`+`Option`+`J` \(macOS\).</span></span>  

:::image type="complex" source="../media/console-hello-console.msft.png" alt-text="Панель консоли" lightbox="../media/console-hello-console.msft.png":::
   <span data-ttu-id="17282-114">Панель **консоли**</span><span class="sxs-lookup"><span data-stu-id="17282-114">The **Console** panel</span></span>  
:::image-end:::  

<span data-ttu-id="17282-115">Чтобы открыть панель консоли из [меню команд][DevToolsCommandMenu], начните вводить текст, `Console` а затем запустите команду **Показать консоль** с индикатором **панели** рядом с ним.</span><span class="sxs-lookup"><span data-stu-id="17282-115">To open the Console panel from the [Command Menu][DevToolsCommandMenu], start typing `Console` and then run the **Show Console** command that has the **Panel** badge next to it.</span></span>  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Команда для отображения панели консоли" lightbox="../media/console-command-menu-show-console.msft.png":::
   <span data-ttu-id="17282-117">Команда для отображения панели **консоли**</span><span class="sxs-lookup"><span data-stu-id="17282-117">The command to show the **Console** panel</span></span>  
:::image-end:::  

### <span data-ttu-id="17282-118">Открытие вкладки "консоль" в ящике</span><span class="sxs-lookup"><span data-stu-id="17282-118">Open the Console tab in the Drawer</span></span>   

<span data-ttu-id="17282-119">Нажмите `Escape` или щелкните **настроить DevTools** \ ( `...` \) и выберите пункт **Показать входной ящик консоли**.</span><span class="sxs-lookup"><span data-stu-id="17282-119">Press `Escape` or click **Customize And Control DevTools** \(`...`\) and then select **Show console drawer**.</span></span>  

:::image type="complex" source="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png" alt-text="Показать консольный ящик" lightbox="../media/console-elements-customize-control-devtools-show-console-drawer.msft.png":::
   **<span data-ttu-id="17282-121">Показать консольный ящик</span><span class="sxs-lookup"><span data-stu-id="17282-121">Show console drawer</span></span>**  
:::image-end:::  

<span data-ttu-id="17282-122">Ящик появляется в нижней части окна DevTools и открывается вкладка **консоли** .</span><span class="sxs-lookup"><span data-stu-id="17282-122">The Drawer pops up at the bottom of your DevTools window, with the **Console** tab open.</span></span>  

:::image type="complex" source="../media/console-elements-console-drawer-hello-world.msft.png" alt-text="Вкладка «консоль» в ящике" lightbox="../media/console-elements-console-drawer-hello-world.msft.png":::
   <span data-ttu-id="17282-124">Вкладка « **консоль** » в **ящике**</span><span class="sxs-lookup"><span data-stu-id="17282-124">The **Console** tab in the **Drawer**</span></span>  
:::image-end:::  

<span data-ttu-id="17282-125">Чтобы открыть вкладку консоль в [меню команд][DevToolsCommandMenu], начните вводить текст, `Console` а затем запустите команду **Показать консоль** с индикатором **ящика** рядом с ним.</span><span class="sxs-lookup"><span data-stu-id="17282-125">To open the Console tab from the [Command Menu][DevToolsCommandMenu], start typing `Console` and then run the **Show Console** command that has the **Drawer** badge next to it.</span></span>  

:::image type="complex" source="../media/console-command-menu-show-console.msft.png" alt-text="Команда для отображения вкладки "консоль" в ящике" lightbox="../media/console-command-menu-show-console.msft.png":::
   <span data-ttu-id="17282-127">Команда для отображения вкладки " **консоль** " в **ящике**</span><span class="sxs-lookup"><span data-stu-id="17282-127">The command to show the **Console** tab in the **Drawer**</span></span>  
:::image-end:::  

### <span data-ttu-id="17282-128">Открытие параметров консоли</span><span class="sxs-lookup"><span data-stu-id="17282-128">Open Console Settings</span></span>   

<span data-ttu-id="17282-129">Нажмите кнопку **Параметры консоли** \ ( ![ Параметры консоли ][ImageSettingsButtonIcon] \).</span><span class="sxs-lookup"><span data-stu-id="17282-129">Click **Console Settings** \(![Console Settings][ImageSettingsButtonIcon]\).</span></span>  

:::image type="complex" source="../media/console-settings-group-similar-empty.msft.png" alt-text="Параметры консоли" lightbox="../media/console-settings-group-similar-empty.msft.png":::
   **<span data-ttu-id="17282-131">Параметры консоли</span><span class="sxs-lookup"><span data-stu-id="17282-131">Console Settings</span></span>**  
:::image-end:::  

<span data-ttu-id="17282-132">Ниже описаны ссылки для каждого параметра.</span><span class="sxs-lookup"><span data-stu-id="17282-132">The links below explain each setting:</span></span>  

*   [**<span data-ttu-id="17282-133">Скрыть сеть</span><span class="sxs-lookup"><span data-stu-id="17282-133">Hide Network</span></span>**](#hide-network-messages)  
*   [**<span data-ttu-id="17282-134">Сохранить журнал</span><span class="sxs-lookup"><span data-stu-id="17282-134">Preserve Log</span></span>**](#persist-messages-across-page-loads)  
*   [**<span data-ttu-id="17282-135">Только выделенный контекст</span><span class="sxs-lookup"><span data-stu-id="17282-135">Selected Context Only</span></span>**](#filter-out-messages-from-different-contexts)  
*   [**<span data-ttu-id="17282-136">Одинаковая группа</span><span class="sxs-lookup"><span data-stu-id="17282-136">Group Similar</span></span>**](#disable-message-grouping)  
*   [**<span data-ttu-id="17282-137">Запись в журнал XmlHttpRequest</span><span class="sxs-lookup"><span data-stu-id="17282-137">Log XmlHttpRequests</span></span>**](#log-xhr-and-fetch-requests)  
*   [**<span data-ttu-id="17282-138">Упреждающая Оценка</span><span class="sxs-lookup"><span data-stu-id="17282-138">Eager Evaluation</span></span>**](#disable-eager-evaluation)  
*   [**<span data-ttu-id="17282-139">Автозаполнение из истории</span><span class="sxs-lookup"><span data-stu-id="17282-139">Autocomplete From History</span></span>**](#disable-autocomplete-from-history)  
    
### <span data-ttu-id="17282-140">Открытие боковой панели консоли</span><span class="sxs-lookup"><span data-stu-id="17282-140">Open the Console Sidebar</span></span>   

<span data-ttu-id="17282-141">Нажмите кнопку **Показать боковую панель консоли** \ ( ![ Показать боковую панель консоли ][ImageShowConsoleSidebarIcon] ), чтобы отобразить боковую панель, которая удобна для фильтрации.</span><span class="sxs-lookup"><span data-stu-id="17282-141">Click **Show Console Sidebar** \(![Show Console Sidebar][ImageShowConsoleSidebarIcon]\) to show the Sidebar, which is useful for filtering.</span></span>  

:::image type="complex" source="../media/console-sidebar-drawer-empty.msft.png" alt-text="Боковая панель консоли" lightbox="../media/console-sidebar-drawer-empty.msft.png":::
   <span data-ttu-id="17282-143">**Console (консоль** ) Врезка</span><span class="sxs-lookup"><span data-stu-id="17282-143">**Console** Sidebar</span></span>  
:::image-end:::  

## <span data-ttu-id="17282-144">Просмотр сообщений</span><span class="sxs-lookup"><span data-stu-id="17282-144">View messages</span></span>   

<span data-ttu-id="17282-145">В этом разделе описаны возможности, которые позволят изменить способ представления сообщений на консоли.</span><span class="sxs-lookup"><span data-stu-id="17282-145">This section contains features that change how messages are presented in the Console.</span></span>  <span data-ttu-id="17282-146">В этом пошаговом руководстве показано, как [Просмотреть сообщения][DevToolsConsoleViewMessages] .</span><span class="sxs-lookup"><span data-stu-id="17282-146">See [View messages][DevToolsConsoleViewMessages] for a hands-on walkthrough.</span></span>  

### <span data-ttu-id="17282-147">Отключение группировки сообщений</span><span class="sxs-lookup"><span data-stu-id="17282-147">Disable message grouping</span></span>   

<span data-ttu-id="17282-148">[Откройте параметры консоли](#open-console-settings) и отключите **группу, как** отключить поведение группировки сообщений по умолчанию для консоли.</span><span class="sxs-lookup"><span data-stu-id="17282-148">[Open Console Settings](#open-console-settings) and disable **Group similar** to disable the default message grouping behavior of the Console.</span></span>  <span data-ttu-id="17282-149">Посмотрите, как [XHR журнал и](#log-xhr-and-fetch-requests) выводит запросы на получение примера.</span><span class="sxs-lookup"><span data-stu-id="17282-149">See [Log XHR and Fetch requests](#log-xhr-and-fetch-requests) for an example.</span></span>  

### <span data-ttu-id="17282-150">Регистрация запросов XHR и FETCH</span><span class="sxs-lookup"><span data-stu-id="17282-150">Log XHR and Fetch requests</span></span>   

<span data-ttu-id="17282-151">[Откройте параметры консоли](#open-console-settings) и включите в **журнал записи XMLHttpRequest** , чтобы регистрировать все `XMLHttpRequest` и `Fetch` запросы на консоли по мере их появления.</span><span class="sxs-lookup"><span data-stu-id="17282-151">[Open Console Settings](#open-console-settings) and enable **Log XMLHttpRequests** to log all `XMLHttpRequest` and `Fetch` requests to the Console as they happen.</span></span>  

:::image type="complex" source="../media/console-xhr-fetch.msft.png" alt-text="Запись запросов на XMLHttpRequest и выборке" lightbox="../media/console-xhr-fetch.msft.png":::
   <span data-ttu-id="17282-153">Журналы `XMLHttpRequest` и `Fetch` запросы</span><span class="sxs-lookup"><span data-stu-id="17282-153">Log `XMLHttpRequest` and `Fetch` requests</span></span>  
:::image-end:::  
<span data-ttu-id="17282-154">Верхнее сообщение на предыдущем рисунке показывает поведение группировки по умолчанию для **консоли**.</span><span class="sxs-lookup"><span data-stu-id="17282-154">The top message in previous figure displays the default grouping behavior of the **Console**.</span></span>  <!--  In the following figure, the same log is displayed after [disabling message grouping](#disable-message-grouping).  -->  

<!--  
> ##### Old Figure 9  
> How the logged `XMLHttpRequest` and `Fetch` requests look after ungrouping  
> :::image type="complex" source="../media/console-xhr-fetch-all.msft.png" alt-text="How the logged XMLHttpRequest and Fetch requests look after ungrouping" lightbox="../media/console-xhr-fetch-all.msft.png":::
>    How the logged XMLHttpRequest and Fetch requests look after ungrouping  
> :::image-end:::  
-->  

<!--todo: add example for ungrouping console items  -->  

### <span data-ttu-id="17282-155">Сохранение сообщений на загрузок страниц</span><span class="sxs-lookup"><span data-stu-id="17282-155">Persist messages across page loads</span></span>   

<span data-ttu-id="17282-156">По умолчанию консоль очищается каждый раз, когда вы загружаете новую страницу.</span><span class="sxs-lookup"><span data-stu-id="17282-156">By default the Console clears whenever you load a new page.</span></span>  <span data-ttu-id="17282-157">Чтобы сохранить сообщения на нескольких страницах, [откройте параметры консоли](#open-console-settings) и установите флажок **сохранить журнал** .</span><span class="sxs-lookup"><span data-stu-id="17282-157">To persist messages across page loads, [Open Console Settings](#open-console-settings) and then enable the **Preserve Log** checkbox.</span></span>  

### <span data-ttu-id="17282-158">Скрыть сетевые сообщения</span><span class="sxs-lookup"><span data-stu-id="17282-158">Hide network messages</span></span>   

<span data-ttu-id="17282-159">По умолчанию браузер записывает сетевые сообщения на **консоль**.</span><span class="sxs-lookup"><span data-stu-id="17282-159">By default the browser logs network messages to the **Console**.</span></span>  <span data-ttu-id="17282-160">На приведенном ниже рисунке выбранное сообщение представляет код состояния HTTP `429` .</span><span class="sxs-lookup"><span data-stu-id="17282-160">In the following figure, the selected message represents an HTTP status code of `429`.</span></span>  

:::image type="complex" source="../media/console-show-network.msft.png" alt-text="Сообщение 429 в консоли" lightbox="../media/console-show-network.msft.png":::
   <span data-ttu-id="17282-162">`429`Сообщение на **консоли**</span><span class="sxs-lookup"><span data-stu-id="17282-162">A `429` message in the **Console**</span></span>  
:::image-end:::  
<span data-ttu-id="17282-163">Чтобы скрыть сетевые сообщения, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="17282-163">To hide network messages:</span></span>  

1.  <span data-ttu-id="17282-164">[Откройте параметры консоли](#open-console-settings).</span><span class="sxs-lookup"><span data-stu-id="17282-164">[Open Console Settings](#open-console-settings).</span></span>  
1.  <span data-ttu-id="17282-165">Включите флажок **Скрыть сеть** .</span><span class="sxs-lookup"><span data-stu-id="17282-165">Enable the **Hide Network** checkbox.</span></span>  
    
## <span data-ttu-id="17282-166">Фильтрация сообщений</span><span class="sxs-lookup"><span data-stu-id="17282-166">Filter messages</span></span>   

<span data-ttu-id="17282-167">Есть несколько способов отфильтровать сообщения на консоли.</span><span class="sxs-lookup"><span data-stu-id="17282-167">There are many ways to filter out messages in the Console.</span></span>  

### <span data-ttu-id="17282-168">Фильтрация сообщений браузера</span><span class="sxs-lookup"><span data-stu-id="17282-168">Filter out browser messages</span></span>   

<span data-ttu-id="17282-169">[Откройте панель консоли](#open-the-console-sidebar) и выберите пункт **сообщения пользователя** , чтобы отображались только те сообщения, которые были получены на странице JavaScript.</span><span class="sxs-lookup"><span data-stu-id="17282-169">[Open the Console Sidebar](#open-the-console-sidebar) and click **User Messages** to only show messages that came from the JavaScript of the page.</span></span>  

:::image type="complex" source="../media/console-sidebar-drawer-user-messages.msft.png" alt-text="Просмотр сообщений пользователя" lightbox="../media/console-sidebar-drawer-user-messages.msft.png":::
   <span data-ttu-id="17282-171">Просмотр сообщений пользователя</span><span class="sxs-lookup"><span data-stu-id="17282-171">View user messages</span></span>  
:::image-end:::  

### <span data-ttu-id="17282-172">Фильтрация по уровню ведения журнала</span><span class="sxs-lookup"><span data-stu-id="17282-172">Filter by log level</span></span>   

<span data-ttu-id="17282-173">DevTools назначает каждому `console.*` методу уровень серьезности.</span><span class="sxs-lookup"><span data-stu-id="17282-173">DevTools assigns each `console.*` method a severity level.</span></span>  <span data-ttu-id="17282-174">Существует 4 уровня: `Verbose` ,, `Info` `Warning` , и `Error` .</span><span class="sxs-lookup"><span data-stu-id="17282-174">There are 4 levels: `Verbose`, `Info`, `Warning`, and `Error`.</span></span>  <span data-ttu-id="17282-175">Например, `console.log()` входит в `Info` группу, в то время как `console.error()` она находится в `Error` группе.</span><span class="sxs-lookup"><span data-stu-id="17282-175">For example, `console.log()` is in the `Info` group, whereas `console.error()` is in the `Error` group.</span></span>  <span data-ttu-id="17282-176">[Справочник по API консоли][DevToolsConsoleApi] описывает уровень важности каждого применимого метода.</span><span class="sxs-lookup"><span data-stu-id="17282-176">The [Console API Reference][DevToolsConsoleApi] describes the severity level of each applicable method.</span></span>  <span data-ttu-id="17282-177">Каждое сообщение, которое браузер записывает на консоль, также имеет уровень серьезности.</span><span class="sxs-lookup"><span data-stu-id="17282-177">Every message that the browser logs to the Console has a severity level too.</span></span>  <span data-ttu-id="17282-178">Вы можете скрыть любые ненужные сообщения.</span><span class="sxs-lookup"><span data-stu-id="17282-178">You may hide any level of messages that you are not interested in.</span></span>  <span data-ttu-id="17282-179">Например, если вы заинтересованы в `Error` сообщениях, вы можете скрыть другие три группы.</span><span class="sxs-lookup"><span data-stu-id="17282-179">For example, if you are only interested in `Error` messages, you may hide the other 3 groups.</span></span>  

<span data-ttu-id="17282-180">Щелкните раскрывающийся список **уровни журнала** , чтобы включить или отключить `Verbose` , `Info` `Warning` или `Error` сообщения.</span><span class="sxs-lookup"><span data-stu-id="17282-180">Click the **Log Levels** dropdown to enable or disable `Verbose`, `Info`, `Warning` or `Error` messages.</span></span>  

:::image type="complex" source="../media/console-log-level-default-levels.msft.png" alt-text="Раскрывающийся список уровней журнала" lightbox="../media/console-log-level-default-levels.msft.png":::
   <span data-ttu-id="17282-182">Раскрывающийся список **уровней журнала**</span><span class="sxs-lookup"><span data-stu-id="17282-182">The **Log Levels** dropdown</span></span>  
:::image-end:::  

<span data-ttu-id="17282-183">Вы также можете отфильтровать по уровню журнала, [открыв боковую панель консоли](#open-the-console-sidebar) и выбрав пункт **ошибки**, **предупреждения**, **сведения**или **подробный**.</span><span class="sxs-lookup"><span data-stu-id="17282-183">You may also filter by log level by [opening the Console Sidebar](#open-the-console-sidebar) and then clicking **Errors**, **Warnings**, **Info**, or **Verbose**.</span></span>  

:::image type="complex" source="../media/console-sidebar-warnings.msft.png" alt-text="Использование боковой панели для просмотра предупреждений" lightbox="../media/console-sidebar-warnings.msft.png":::
   <span data-ttu-id="17282-185">Использование боковой панели для просмотра предупреждений</span><span class="sxs-lookup"><span data-stu-id="17282-185">Use the Sidebar to view warnings</span></span>  
:::image-end:::  

### <span data-ttu-id="17282-186">Фильтрация сообщений по URL-адресу</span><span class="sxs-lookup"><span data-stu-id="17282-186">Filter messages by URL</span></span>   

<span data-ttu-id="17282-187">Введите и `url:` URL-адрес, чтобы просматривать только те сообщения, которые были отправлены из этого URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="17282-187">Type `url:` followed by a URL to only view messages that came from that URL.</span></span>  <span data-ttu-id="17282-188">После ввода `url:` DevTools появятся все нужные URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="17282-188">After you type `url:` DevTools shows all relevant URLs.</span></span>  <span data-ttu-id="17282-189">Домены также работают.</span><span class="sxs-lookup"><span data-stu-id="17282-189">Domains also work.</span></span>  <span data-ttu-id="17282-190">Например, если `https://example.com/a.js` `https://example.com/b.js` сообщения записываются в журнал, `url:https://example.com` вы можете сосредоточиться на сообщениях из этих 2 сценариев.</span><span class="sxs-lookup"><span data-stu-id="17282-190">For example, if `https://example.com/a.js` and `https://example.com/b.js` are logging messages, `url:https://example.com` enables you to focus on the messages from these 2 scripts.</span></span>  

:::image type="complex" source="../media/console-filter-text.msft.png" alt-text="Фильтр URL-адреса" lightbox="../media/console-filter-text.msft.png":::
   <span data-ttu-id="17282-192">Фильтр URL-адреса</span><span class="sxs-lookup"><span data-stu-id="17282-192">A URL filter</span></span>  
:::image-end:::  

<span data-ttu-id="17282-193">Введите текст `-url:` , чтобы скрыть сообщения от этого URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="17282-193">Type `-url:` to hide messages from that URL.</span></span>  <span data-ttu-id="17282-194">Это называется фильтром отрицательных URL-адресов.</span><span class="sxs-lookup"><span data-stu-id="17282-194">This is called a negative URL filter.</span></span>  

:::image type="complex" source="../media/console-negative-filter-text.msft.png" alt-text="Фильтр отрицательных URL-адресов, в котором скрываются все сообщения, соответствующие https://b.wal.co URL-адресу." lightbox="../media/console-negative-filter-text.msft.png":::
   <span data-ttu-id="17282-196">Фильтр отрицательных URL-адресов, в котором скрываются все сообщения, соответствующие `https://b.wal.co` URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="17282-196">A negative URL filter that hides all messages that match the `https://b.wal.co` URL</span></span>
:::image-end:::  

<span data-ttu-id="17282-197">Вы также можете показывать сообщения с одного URL-адреса, [открыв боковую панель консоли](#open-the-console-sidebar), развернув раздел " **пользовательские сообщения** ", а затем щелкнув URL-адрес сценария, содержащего сообщения, на которые нужно обратить внимание.</span><span class="sxs-lookup"><span data-stu-id="17282-197">You may also show messages from a single URL by [opening the Console Sidebar](#open-the-console-sidebar), expanding the **User Messages** section, and then clicking the URL of the script containing the messages on which you want to focus.</span></span>  

:::image type="complex" source="../media/console-filter-text-specified.msft.png" alt-text="Просмотр сообщений, которые поставляются с wp-ad.min.js" lightbox="../media/console-filter-text-specified.msft.png":::
   <span data-ttu-id="17282-199">Просмотр сообщений, которые были получены</span><span class="sxs-lookup"><span data-stu-id="17282-199">View the messages that came from</span></span> `wp-ad.min.js`  
:::image-end:::  

### <span data-ttu-id="17282-200">Фильтрация сообщений в разных контекстах</span><span class="sxs-lookup"><span data-stu-id="17282-200">Filter out messages from different contexts</span></span>   

<span data-ttu-id="17282-201">Предположим, что у вас есть реклама \ (AD) на вашей странице.</span><span class="sxs-lookup"><span data-stu-id="17282-201">Suppose that you have an advertisement \(ad\) on your page.</span></span>  <span data-ttu-id="17282-202">Рекламное объявление встраивается в приложение `<iframe>` и создает большое количество сообщений на консоли.</span><span class="sxs-lookup"><span data-stu-id="17282-202">The ad is embedded in an `<iframe>` and is generating a lot of messages in your Console.</span></span>  <span data-ttu-id="17282-203">Так как объявление запущено в другом [контексте JavaScript](#select-javascript-context), один из способов скрыть сообщения — [открыть параметры консоли](#open-console-settings) и установить флажок **только выбранный контекст** .</span><span class="sxs-lookup"><span data-stu-id="17282-203">Because the ad is running in a different [JavaScript context](#select-javascript-context), one way to hide the messages is to [open Console Settings](#open-console-settings) and enable the **Selected Context Only** checkbox.</span></span>  

### <span data-ttu-id="17282-204">Фильтрация сообщений, не соответствующих шаблону регулярного выражения</span><span class="sxs-lookup"><span data-stu-id="17282-204">Filter out messages that do not match a regular expression pattern</span></span>   

<span data-ttu-id="17282-205">Введите регулярное выражение, например `/[gm][ta][mi]/` в текстовое поле **Фильтр** , чтобы отфильтровать сообщения, которые не соответствуют этому шаблону.</span><span class="sxs-lookup"><span data-stu-id="17282-205">Type a regular expression such as `/[gm][ta][mi]/` in the **Filter** text box to filter out any messages that do not match that pattern.</span></span>  <span data-ttu-id="17282-206">DevTools проверяет, найден ли шаблон в тексте сообщения или сценарий, который привел к занесению в журнал сообщения.</span><span class="sxs-lookup"><span data-stu-id="17282-206">DevTools checks if the pattern is found in the message text or the script that caused the message to be logged.</span></span>  

:::image type="complex" source="../media/console-filter-regex.msft.png" alt-text="Фильтрация сообщений, не соответствующих выражению Regex" lightbox="../media/console-filter-regex.msft.png":::
   <span data-ttu-id="17282-208">Фильтрация сообщений, не соответствующих `/[gm][ta][mi]/` выражению регулярного выражения</span><span class="sxs-lookup"><span data-stu-id="17282-208">Filter out any messages that do not match the `/[gm][ta][mi]/` regex expression</span></span>  
:::image-end:::  

## <span data-ttu-id="17282-209">Запуск JavaScript</span><span class="sxs-lookup"><span data-stu-id="17282-209">Run JavaScript</span></span>   

<span data-ttu-id="17282-210">В этом разделе описаны возможности, связанные с выполнением JavaScript на консоли.</span><span class="sxs-lookup"><span data-stu-id="17282-210">This section contains features related to running JavaScript in the Console.</span></span>  <span data-ttu-id="17282-211">В этом пошаговом руководстве показано, как [запускать JavaScript][DevToolsConsoleOverviewJavascript] .</span><span class="sxs-lookup"><span data-stu-id="17282-211">See [Run JavaScript][DevToolsConsoleOverviewJavascript] for a hands-on walkthrough.</span></span>  

### <span data-ttu-id="17282-212">Повторное выполнение выражений из истории</span><span class="sxs-lookup"><span data-stu-id="17282-212">Re-run expressions from history</span></span>   

<span data-ttu-id="17282-213">Нажмите клавишу `Up Arrow` для циклического просмотра истории выражений JavaScript, которые выполнялись на консоли раньше.</span><span class="sxs-lookup"><span data-stu-id="17282-213">Press the `Up Arrow` key to cycle through the history of JavaScript expressions that you ran earlier in the Console.</span></span>  <span data-ttu-id="17282-214">Нажмите кнопку `Enter` , чтобы выполнить это выражение еще раз.</span><span class="sxs-lookup"><span data-stu-id="17282-214">Press `Enter` to run that expression again.</span></span>  

### <span data-ttu-id="17282-215">Просмотр значения выражения в режиме реального времени с помощью выражений с реальными данными</span><span class="sxs-lookup"><span data-stu-id="17282-215">Watch the value of an expression in real-time with Live Expressions</span></span>   

<span data-ttu-id="17282-216">Если вы обнаружите, что один и тот же выражение JavaScript будет вводиться повторно в консоль, возможно, вам будет проще создать **выражение в реальном времени**.</span><span class="sxs-lookup"><span data-stu-id="17282-216">If you find yourself typing the same JavaScript expression in the Console repeatedly, you may find it easier to create a **Live Expression**.</span></span>  <span data-ttu-id="17282-217">С помощью **выражений в реальном времени** вы вводите выражение один раз, а затем закрепите его в верхней части консоли.</span><span class="sxs-lookup"><span data-stu-id="17282-217">With **Live Expressions** you type an expression once and then pin it to the top of your Console.</span></span>  <span data-ttu-id="17282-218">Значение выражения обновляется почти в режиме реального времени.</span><span class="sxs-lookup"><span data-stu-id="17282-218">The value of the expression updates in near real-time.</span></span>  <span data-ttu-id="17282-219">Просмотрите [значения выражений JavaScript в реальном времени с помощью выражений с реальными данными][DevToolsConsoleLiveExpressions].</span><span class="sxs-lookup"><span data-stu-id="17282-219">See [Watch JavaScript Expression Values In Real-Time With Live Expressions][DevToolsConsoleLiveExpressions].</span></span>  

### <span data-ttu-id="17282-220">Отключение безотлагательной оценки</span><span class="sxs-lookup"><span data-stu-id="17282-220">Disable Eager Evaluation</span></span>   

<span data-ttu-id="17282-221">По мере ввода выражений JavaScript в консоли **упреждающая Оценка** показывает предварительный просмотр возвращаемого значения для этого выражения.</span><span class="sxs-lookup"><span data-stu-id="17282-221">As you type JavaScript expressions in the Console, **Eager Evaluation** shows a preview of the return value for that expression.</span></span>  <span data-ttu-id="17282-222">[Откройте параметры консоли](#open-console-settings) и отключите флажок **упреждающая Оценка** , чтобы отключить предварительный просмотр возвращаемых значений.</span><span class="sxs-lookup"><span data-stu-id="17282-222">[Open Console Settings](#open-console-settings) and disable the **Eager Evaluation** checkbox to turn off the return value previews.</span></span>  

### <span data-ttu-id="17282-223">Отключение автозаполнения из истории</span><span class="sxs-lookup"><span data-stu-id="17282-223">Disable autocomplete from history</span></span>   

<span data-ttu-id="17282-224">По мере ввода выражения в всплывающем окне для консоли отображаются выражения, которые были выполнены раньше.</span><span class="sxs-lookup"><span data-stu-id="17282-224">As you type out an expression, the autocomplete popup window for the Console shows expressions that you ran earlier.</span></span>  <span data-ttu-id="17282-225">Эти выражения добавляются в начале `>` символа.</span><span class="sxs-lookup"><span data-stu-id="17282-225">These expressions are prepended with the `>` character.</span></span>  <span data-ttu-id="17282-226">[Откройте меню Параметры консоли](#open-console-settings) и отключите флажок **Автозаполнение из журнала** , чтобы отключить отображение выражений из истории.</span><span class="sxs-lookup"><span data-stu-id="17282-226">[Open Console Settings](#open-console-settings) and disable the **Autocomplete From History** checkbox to stop showing expressions from your history.</span></span>  

> [!NOTE]
> <span data-ttu-id="17282-227">На приведенном ниже рисунке, `document.querySelector('a')` а `document.querySelector('img')` также выражения, которые были оценены ранее.</span><span class="sxs-lookup"><span data-stu-id="17282-227">In the following figure, `document.querySelector('a')` and `document.querySelector('img')` are expressions that were evaluated earlier.</span></span>  

:::image type="complex" source="../media/console-filter-text-autofilter-history.msft.png" alt-text="В всплывающем окне "Автозаполнение" отображаются выражения из истории" lightbox="../media/console-filter-text-autofilter-history.msft.png":::
   <span data-ttu-id="17282-229">В всплывающем окне "Автозаполнение" отображаются выражения из истории</span><span class="sxs-lookup"><span data-stu-id="17282-229">The autocomplete popup displays expressions from history</span></span>  
:::image-end:::  

### <span data-ttu-id="17282-230">Выбор контекста JavaScript</span><span class="sxs-lookup"><span data-stu-id="17282-230">Select JavaScript context</span></span>   

<span data-ttu-id="17282-231">По умолчанию раскрывающийся список **контекстов JavaScript** имеет значение **Top**, которое представляет [контекст просмотра][MDNBrowsingContext] основного документа.</span><span class="sxs-lookup"><span data-stu-id="17282-231">By default the **JavaScript Context** dropdown is set to **top**, which represents the [browsing context][MDNBrowsingContext] of the main document.</span></span>  

:::image type="complex" source="../media/console-dom-level-top.msft.png" alt-text="Раскрывающийся список контекстов JavaScript" lightbox="../media/console-dom-level-top.msft.png":::
   <span data-ttu-id="17282-233">Раскрывающийся список **контекстов JavaScript**</span><span class="sxs-lookup"><span data-stu-id="17282-233">The **JavaScript Context** dropdown</span></span>  
:::image-end:::  

<span data-ttu-id="17282-234">Предположим, что у вас есть реклама на странице, внедренная в `<iframe>` .</span><span class="sxs-lookup"><span data-stu-id="17282-234">Suppose you have an ad on your page embedded in an `<iframe>`.</span></span>  <span data-ttu-id="17282-235">Вы хотите запустить JavaScript, чтобы настроить модель DOM рекламы.</span><span class="sxs-lookup"><span data-stu-id="17282-235">You want to run JavaScript in order to tweak the DOM of the ad.</span></span>  <span data-ttu-id="17282-236">Сначала необходимо выбрать контекст обзора рекламы из раскрывающегося списка **контекстов JavaScript** .</span><span class="sxs-lookup"><span data-stu-id="17282-236">You should first select the browsing context of the ad from the **JavaScript Context** dropdown.</span></span>  

:::image type="complex" source="../media/console-dom-level-multiple.msft.png" alt-text="Выбор другого контекста JavaScript" lightbox="../media/console-dom-level-multiple.msft.png":::
   <span data-ttu-id="17282-238">Выбор другого контекста JavaScript</span><span class="sxs-lookup"><span data-stu-id="17282-238">Select a different JavaScript context</span></span>  
:::image-end:::  

## <span data-ttu-id="17282-239">Очистка консоли</span><span class="sxs-lookup"><span data-stu-id="17282-239">Clear the Console</span></span>   

<span data-ttu-id="17282-240">Чтобы очистить консоль, вы можете использовать любой из следующих рабочих процессов:</span><span class="sxs-lookup"><span data-stu-id="17282-240">You may use any of the following workflows to clear the Console:</span></span>  

*   <span data-ttu-id="17282-241">Нажмите **Очистить консоль** \ ( ![ Очистить консоль ][ImageClearConsoleIcon] ).</span><span class="sxs-lookup"><span data-stu-id="17282-241">Click **Clear Console** \(![Clear Console][ImageClearConsoleIcon]\).</span></span>  
*   <span data-ttu-id="17282-242">Щелкните сообщение правой кнопкой мыши и выберите команду **Очистить консоль**.</span><span class="sxs-lookup"><span data-stu-id="17282-242">Right-click a message and then select **Clear Console**.</span></span>  
*   <span data-ttu-id="17282-243">Введите текст `clear()` на консоли и нажмите клавишу `Enter` .</span><span class="sxs-lookup"><span data-stu-id="17282-243">Type `clear()` in the Console and then press `Enter`.</span></span>  
*   <span data-ttu-id="17282-244">Вызов `console.clear()` из JavaScript на веб-странице.</span><span class="sxs-lookup"><span data-stu-id="17282-244">Call `console.clear()` from the JavaScript for your webpage.</span></span>  
*   <span data-ttu-id="17282-245">Нажимайте кнопку, `Control` + `L` пока фокус находится на консоли.</span><span class="sxs-lookup"><span data-stu-id="17282-245">Press `Control`+`L` while the Console is in focus.</span></span>  
    
<!--
 

  
-->  

<!-- image links -->  

[ImageClearConsoleIcon]: ../media/clear-console-button-icon.msft.png  
[ImageSettingsButtonIcon]: ../media/settings-button-icon.msft.png  
[ImageShowConsoleSidebarIcon]: ../media/show-console-sidebar-icon.msft.png  

<!-- links -->  

[DevToolsCommandMenu]: ../command-menu/index.md "Выполнение команд с помощью командного меню Microsoft Edge DevTools | Документы Microsoft"  
[DevToolsConsoleViewMessages]: ./index.md#viewing-logged-messages "Просмотр сообщений с запротоколированием — обзор консоли | Документы Microsoft"  
[DevToolsConsoleApi]: ./api.md "Справочник по API консоли | Документы Microsoft"  
[DevToolsConsoleOverviewJavascript]: ./index.md#running-javascript "Выполнение JavaScript: обзор консоли | Документы Microsoft"  
[DevToolsConsoleJavascript]: ./javascript.md "Начало работы с JavaScript на консоли | Документы Microsoft"  
[DevToolsConsoleLiveExpressions]: ./live-expressions.md "Просмотр значений выражений JavaScript в режиме реального времени с помощью выражений в реальном масштабе | Документы Microsoft"  
[DevToolsConsoleLog]: ./log.md "Начало работы с сообщениями в журнале на консоли | Документы Microsoft"  
[DevToolsConsoleUtilities]: ./utilities.md "Справочник по API служебных программ для консоли | Документы Microsoft"  

[MDNBrowsingContext]: https://developer.mozilla.org/docs/Glossary/Browsing_context "Контекст просмотра | MDN"  

> [!NOTE]
> <span data-ttu-id="17282-255">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="17282-255">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="17282-256">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/console/reference) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="17282-256">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/console/reference) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="17282-258">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="17282-258">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
