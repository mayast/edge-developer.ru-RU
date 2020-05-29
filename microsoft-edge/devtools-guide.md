---
description: Знакомство со средствами разработчика Microsoft EDGE (EdgeHTML)
title: Инструменты разработчика Microsoft EDGE (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/05/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
experimental: true
experiment_id: 51fe4b97-3e55-41
localization_priority: Priority
ms.openlocfilehash: 56edfa3aa39fc20d37d95fb8fde029a702732336
ms.sourcegitcommit: 985cfb79a64951afd5beb7981b26afbed30a8972
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/07/2020
ms.locfileid: "10629506"
---
# <span data-ttu-id="897a0-104">Инструменты разработчика Microsoft EDGE (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="897a0-104">Microsoft Edge (EdgeHTML) Developer Tools</span></span>  

[!INCLUDE [new-devtools-version-note](includes/new-devtools-version-note.md)]  

<span data-ttu-id="897a0-105">DevTools Microsoft Edge \ (EdgeHTML \) создаются с помощью [TypeScript][|::ref1::|Index], на платформе [Open Source][GithubMicrosoftChakracore], оптимизированных для современных серверных рабочих процессов, и теперь доступно как [автономное приложение для Windows 10][MicrosoftStoreEdgeDevtoolsPreview] в Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="897a0-105">The Microsoft Edge \(EdgeHTML\) DevTools are built with [TypeScript][|::ref1::|Index], powered by [open source][GithubMicrosoftChakracore], optimized for modern front-end workflows, and now available as a [standalone Windows 10 app][MicrosoftStoreEdgeDevtoolsPreview] in the Microsoft Store!</span></span>  

<span data-ttu-id="897a0-106">Чтобы узнать больше о последних возможностях, ознакомьтесь с [DevTools в последнем обновлении Windows 10 (EdgeHTML 18)][DevtoolsGuideEdgehtmlWhatsnew].</span><span class="sxs-lookup"><span data-stu-id="897a0-106">For more on the latest features, check out [DevTools in the latest update of Windows 10 (EdgeHTML 18)][DevtoolsGuideEdgehtmlWhatsnew].</span></span>  

## <span data-ttu-id="897a0-107">Основные инструменты</span><span class="sxs-lookup"><span data-stu-id="897a0-107">Core tools</span></span>  

:::image type="complex" source="./devtools-guide/media/devtools.png" alt-text="Microsoft EDGE (EdgeHTML) DevTools":::
   <span data-ttu-id="897a0-109">Microsoft EDGE (EdgeHTML) DevTools</span><span class="sxs-lookup"><span data-stu-id="897a0-109">Microsoft Edge (EdgeHTML) DevTools</span></span>
:::image-end:::

<!--![Microsoft Edge \(EdgeHTML\) DevTools][ImageDevtoolsEdgehtml]  -->  

<span data-ttu-id="897a0-110">Microsoft Edge \ (EdgeHTML \) DevTools включает следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="897a0-110">The Microsoft Edge \(EdgeHTML\) DevTools include:</span></span>  

*   <span data-ttu-id="897a0-111">Панель " [элементы][DevtoolsGuideEdgehtml|::ref2::|] " для редактирования HTML и CSS, проверки свойств специальных возможностей, просмотра прослушивателей событий и установки контрольных точек изменений DOM</span><span class="sxs-lookup"><span data-stu-id="897a0-111">An [Elements][DevtoolsGuideEdgehtml|::ref2::|] panel to edit HTML and CSS, inspect accessibility properties, view event listeners, and set DOM mutation breakpoints</span></span>  
*   <span data-ttu-id="897a0-112">[Консоль][DevtoolsGuideEdgehtml|::ref3::|] для просмотра и фильтрации сообщений журнала, проверки объектов JavaScript и узлов DOM, а также выполнения JavaScript в контексте выбранного окна или фрейма</span><span class="sxs-lookup"><span data-stu-id="897a0-112">A [Console][DevtoolsGuideEdgehtml|::ref3::|] to view and filter log messages, inspect JavaScript objects and DOM nodes, and run JavaScript in the context of the selected window or frame</span></span>  
*   <span data-ttu-id="897a0-113">[Отладчик][DevtoolsGuideEdgehtml|::ref4::|] для пошагового использования кода, задания контрольных значений и точек останова, редактирование кода в реальном времени, проверка веб-хранилища и кэша файлов cookie.</span><span class="sxs-lookup"><span data-stu-id="897a0-113">A [Debugger][DevtoolsGuideEdgehtml|::ref4::|] to step through code, set watches and breakpoints, live edit your code, and inspect your web storage and cookie caches</span></span>  
*   <span data-ttu-id="897a0-114">Панель [сети][DevtoolsGuideEdgehtml|::ref5::|] для мониторинга и проверки запросов и ответов из кэша сети и браузера</span><span class="sxs-lookup"><span data-stu-id="897a0-114">A [Network][DevtoolsGuideEdgehtml|::ref5::|] panel to monitor and inspect requests and responses from the network and browser cache</span></span>  
*   <span data-ttu-id="897a0-115">Панель [производительности][DevtoolsGuideEdgehtml|::ref6::|] для профилирования времени и системных ресурсов, необходимых для вашего сайта</span><span class="sxs-lookup"><span data-stu-id="897a0-115">A [Performance][DevtoolsGuideEdgehtml|::ref6::|] panel to profile the time and system resources required by your site</span></span>  
*   <span data-ttu-id="897a0-116">Панель [памяти][DevtoolsGuideEdgehtml|::ref7::|] для измерения использования ресурсов памяти и сравнения снимков кучи в разных состояниях среды выполнения кода</span><span class="sxs-lookup"><span data-stu-id="897a0-116">A [Memory][DevtoolsGuideEdgehtml|::ref7::|] panel to measure your use of memory resources and compare heap snapshots at different states of code runtime</span></span>  
*   <span data-ttu-id="897a0-117">Панель [хранилища][DevtoolsGuideEdgehtml|::ref8::|] для проверки и управления веб-хранилищем, IndexedDB, cookies и данными кэша</span><span class="sxs-lookup"><span data-stu-id="897a0-117">A [Storage][DevtoolsGuideEdgehtml|::ref8::|] panel for inspecting and managing your web storage, IndexedDB, cookies and cache data</span></span>  
*   <span data-ttu-id="897a0-118">Панель " [сотрудники службы][DevtoolsGuideEdgehtmlServiceworkers] " для управления и отладки сотрудников службы</span><span class="sxs-lookup"><span data-stu-id="897a0-118">A [Service Workers][DevtoolsGuideEdgehtmlServiceworkers] panel for managing and debugging your service workers</span></span>  
*   <span data-ttu-id="897a0-119">Панель [эмуляции][DevtoolsGuideEdgehtml|::ref9::|] для проверки сайта с различными профилями браузера, разрешениями экрана и координатами местоположения GPS</span><span class="sxs-lookup"><span data-stu-id="897a0-119">An [Emulation][DevtoolsGuideEdgehtml|::ref9::|] panel to test your site with different browser profiles, screen resolutions, and GPS location coordinates</span></span>  

<span data-ttu-id="897a0-120">Отправляйте [Отзывы и запросы функций](#feedback)!</span><span class="sxs-lookup"><span data-stu-id="897a0-120">Please keep sending your [feedback and feature requests](#feedback)!</span></span>  

> [!TIP]
> <span data-ttu-id="897a0-121">[Тестирование в Microsoft Edge \ (EdgeHTML \) бесплатно из любого браузера][BrowserstackEdgehtml].</span><span class="sxs-lookup"><span data-stu-id="897a0-121">[Test on Microsoft Edge \(EdgeHTML\) free from any browser][BrowserstackEdgehtml].</span></span>  
> <span data-ttu-id="897a0-122">Группа Microsoft EDGE, сопоставленная с [BrowserStack][BrowserstackEdgehtml] , для предоставления бесплатных и автоматизированных тестов в Microsoft Edge \ (EdgeHTML \).</span><span class="sxs-lookup"><span data-stu-id="897a0-122">The Microsoft Edge team partnered with [BrowserStack][BrowserstackEdgehtml] to provide free live and automated testing on Microsoft Edge \(EdgeHTML\).</span></span>  

## <span data-ttu-id="897a0-123">Приложение Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="897a0-123">Microsoft Store app</span></span>  

<span data-ttu-id="897a0-124">**DevTools Microsoft Edge \ (EdgeHTML \)** [теперь доступны][DevtoolsGuideEdgehtmlWhatsnew] в виде автономного [приложения для Windows 10 из Microsoft Store][MicrosoftStoreEdgeDevtoolsPreview], а также с помощью инструментов "в браузере" и " `F12` \".</span><span class="sxs-lookup"><span data-stu-id="897a0-124">The **Microsoft Edge \(EdgeHTML\) DevTools** are [now available][DevtoolsGuideEdgehtmlWhatsnew] as a standalone [Windows 10 app from the Microsoft Store][MicrosoftStoreEdgeDevtoolsPreview], in addition to the in-browser \(`F12`\) tooling experience.</span></span>  <span data-ttu-id="897a0-125">В версии магазина есть панель **выбора** для присоединения к конечным объектам Open local и Remote Page, а также макет с вкладками для быстрого переключения между экземплярами DevTools.</span><span class="sxs-lookup"><span data-stu-id="897a0-125">With the store version comes a **chooser** panel for attaching to open local and remote page targets and a tabbed layout for easy switching between DevTools instances.</span></span>  

### <span data-ttu-id="897a0-126">Локальная отладка</span><span class="sxs-lookup"><span data-stu-id="897a0-126">Local debugging</span></span>  

<span data-ttu-id="897a0-127">Чтобы выполнить отладку страницы локально, просто запустите приложение Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="897a0-127">To debug a page locally, simply launch the Microsoft Edge DevTools app.</span></span>  <span data-ttu-id="897a0-128">На **локальной** панели средства выбора отображаются все активные процессы содержимого EdgeHTML, включая открытые вкладки браузера EDGE, запуск [PWAs][PwasEdgehtmlIndex] \ ( `WWAHost.exe` процессы \) и [WebView][HostingWebview] элементов управления.</span><span class="sxs-lookup"><span data-stu-id="897a0-128">The **Local** panel of the chooser displays all of the active EdgeHTML content processes, including open Edge browser tabs, running [PWAs][PwasEdgehtmlIndex] \(`WWAHost.exe` processes\), and [webview][HostingWebview] controls.</span></span>  <span data-ttu-id="897a0-129">Выберите требуемый целевой объект, чтобы прикрепить и открыть новый экземпляр вкладки DevTools.</span><span class="sxs-lookup"><span data-stu-id="897a0-129">Select your desired target to attach and open a new tab instance of the DevTools.</span></span>  

:::image type="complex" source="./devtools-guide/media/chooser_local.png" alt-text="Локальная панель приложения DevTools":::
   <span data-ttu-id="897a0-131">Локальная панель приложения DevTools</span><span class="sxs-lookup"><span data-stu-id="897a0-131">DevTools app Local panel</span></span>
:::image-end:::

<!--![DevTools app Local panel][ImageDevtoolsGuideEdgehtmlChooselocal]  -->  

### <span data-ttu-id="897a0-132">Удаленная отладка</span><span class="sxs-lookup"><span data-stu-id="897a0-132">Remote debugging</span></span>  

<span data-ttu-id="897a0-133">Приложение Microsoft Edge DevTools предоставляет базовую поддержку для отладки страниц на удаленном компьютере с помощью нового [протокола DevTools][DevtoolsProtocolEdgehtmlIndex].</span><span class="sxs-lookup"><span data-stu-id="897a0-133">The Microsoft Edge DevTools app introduces basic support for debugging pages on a remote machine via our newly released [DevTools Protocol][DevtoolsProtocolEdgehtmlIndex].</span></span>  <span data-ttu-id="897a0-134">В последнем выпуске есть удаленный доступ к основным функциям в [отладчике][DevtoolsGuideEdgehtml|::ref10::|], [элементах][DevtoolsGuideEdgehtml|::ref11::|] \ (для операций только для чтения, а также на панелях [консоли][DevtoolsGuideEdgehtml|::ref12::|] ).</span><span class="sxs-lookup"><span data-stu-id="897a0-134">With the latest release comes remote access to core functionality in the [Debugger][DevtoolsGuideEdgehtml|::ref10::|], [Elements][DevtoolsGuideEdgehtml|::ref11::|] \(for read-only operations\), and [Console][DevtoolsGuideEdgehtml|::ref12::|] panels.</span></span>  <span data-ttu-id="897a0-135">Удаленная отладка ограничена Microsoft EDGE (EdgeHTML \) на компьютерах, работающих под управлением классических приложений, и поддерживает другие узлы EdgeHTML и устройства с Windows 10, которые появятся в будущих выпусках.</span><span class="sxs-lookup"><span data-stu-id="897a0-135">Remote debugging is limited to Microsoft Edge \(EdgeHTML\) running desktop hosts, with support for other EdgeHTML hosts and Windows 10 devices coming in future releases.</span></span>  

<span data-ttu-id="897a0-136">Чтобы приступить к работе, ознакомьтесь с разделом [*Microsoft Edge DevTools*][DevtoolsProtocolEdgehtmlClientsEdgePreview] в документах [протоколов DevTools][DevtoolsProtocolEdgehtmlIndex] .</span><span class="sxs-lookup"><span data-stu-id="897a0-136">To get started, check out the [*Microsoft Edge DevTools*][DevtoolsProtocolEdgehtmlClientsEdgePreview] section of the [DevTools Protocol][DevtoolsProtocolEdgehtmlIndex] docs.</span></span>  

:::image type="complex" source="./devtools-guide/media/chooser_remote.png" alt-text="Удаленная панель приложения DevTools":::
   <span data-ttu-id="897a0-138">Удаленная панель приложения DevTools</span><span class="sxs-lookup"><span data-stu-id="897a0-138">DevTools app Remote panel</span></span>
:::image-end:::

<!--![DevTools app Remote panel][ImageDevtoolsGuideEdgehtmlRemote]  -->  

## <span data-ttu-id="897a0-139">Общие сочетания клавиш</span><span class="sxs-lookup"><span data-stu-id="897a0-139">General Shortcuts</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="897a0-140">Все сочетания клавиш были проверены в последней версии Windows.</span><span class="sxs-lookup"><span data-stu-id="897a0-140">All shortcuts have been verified in the most recent version of Windows.</span></span>  
> <span data-ttu-id="897a0-141">Если вы не можете использовать ярлык, обновите свою копию Windows.</span><span class="sxs-lookup"><span data-stu-id="897a0-141">If you are unable to use a shortcut, please update your copy of Windows.</span></span>  

<span data-ttu-id="897a0-142">Эти сочетания клавиш управляют основным окном DevTools и должны работать во всех средствах.</span><span class="sxs-lookup"><span data-stu-id="897a0-142">These shortcuts control the main DevTools window and should work across all tools.</span></span>  

| <span data-ttu-id="897a0-143">Действие</span><span class="sxs-lookup"><span data-stu-id="897a0-143">Action</span></span> | <span data-ttu-id="897a0-144">Появивше</span><span class="sxs-lookup"><span data-stu-id="897a0-144">Shortcut</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="897a0-145">Показать или скрыть DevTools \ (открывается в последней просмотренной панели \)</span><span class="sxs-lookup"><span data-stu-id="897a0-145">Show/Hide DevTools \(opens to last viewed panel\)</span></span> | `F12`<span data-ttu-id="897a0-146">, `Ctrl`+`Shift`+</span><span class="sxs-lookup"><span data-stu-id="897a0-146">, `Ctrl`+`Shift`+</span></span>`I` |  
| <span data-ttu-id="897a0-147">Переключить закрепление \ (открепить/снизу или справа \)</span><span class="sxs-lookup"><span data-stu-id="897a0-147">Toggle docking \(Undock/Bottom/Right\)</span></span> | `Ctrl`+`Shift`+`D` |  
| <span data-ttu-id="897a0-148">Открыть файл</span><span class="sxs-lookup"><span data-stu-id="897a0-148">Open file</span></span> | `Ctrl`<span data-ttu-id="897a0-149">+`P`, `Ctrl`+</span><span class="sxs-lookup"><span data-stu-id="897a0-149">+`P`, `Ctrl`+</span></span>`O` |  
| <span data-ttu-id="897a0-150">Отображение нередактируемого исходного кода HTML в отладчике</span><span class="sxs-lookup"><span data-stu-id="897a0-150">Show non-editable HTML source code in Debugger</span></span> | `Ctrl`+`U` |  
| <span data-ttu-id="897a0-151">Отображение и скрытие консоли в нижней части любого другого инструмента</span><span class="sxs-lookup"><span data-stu-id="897a0-151">Show/hide Console at the bottom of any other tool</span></span>  | `Ctrl`+`` ` `` |  
| <span data-ttu-id="897a0-152">Переключение на элементы \ (проводник DOM \)</span><span class="sxs-lookup"><span data-stu-id="897a0-152">Switch to Elements \(DOM Explorer\)</span></span> | `Ctrl`+`1` |  
| <span data-ttu-id="897a0-153">Переключиться на консоль</span><span class="sxs-lookup"><span data-stu-id="897a0-153">Switch to Console</span></span> |  `Ctrl`+`2` |  
| <span data-ttu-id="897a0-154">Переход в режим отладчика</span><span class="sxs-lookup"><span data-stu-id="897a0-154">Switch to Debugger</span></span> | `Ctrl`+`3` |  
| <span data-ttu-id="897a0-155">Переключиться в сеть</span><span class="sxs-lookup"><span data-stu-id="897a0-155">Switch to Network</span></span> | `Ctrl`+`4` |  
| <span data-ttu-id="897a0-156">Переключение на производительность</span><span class="sxs-lookup"><span data-stu-id="897a0-156">Switch to Performance</span></span> | `Ctrl`+`5` |  
| <span data-ttu-id="897a0-157">Переход в память</span><span class="sxs-lookup"><span data-stu-id="897a0-157">Switch to Memory</span></span> | `Ctrl`+`6` |  
| <span data-ttu-id="897a0-158">Переключение на эмуляцию</span><span class="sxs-lookup"><span data-stu-id="897a0-158">Switch to Emulation</span></span> | `Ctrl`+`7` |  
| <span data-ttu-id="897a0-159">Справочный документ</span><span class="sxs-lookup"><span data-stu-id="897a0-159">Help Document</span></span> | `F1` |  
| <span data-ttu-id="897a0-160">Следующий инструмент</span><span class="sxs-lookup"><span data-stu-id="897a0-160">Next tool</span></span> | `Ctrl`+`F6` |  
| <span data-ttu-id="897a0-161">Предыдущее средство</span><span class="sxs-lookup"><span data-stu-id="897a0-161">Previous tool</span></span> | `Ctrl`+`Shift`+`F6` |  
| <span data-ttu-id="897a0-162">Предыдущее средство \ (из истории)</span><span class="sxs-lookup"><span data-stu-id="897a0-162">Previous tool \(from history\)</span></span> | `Ctrl`+`Shift`+`[` |  
| <span data-ttu-id="897a0-163">Следующий инструмент \ (из истории)</span><span class="sxs-lookup"><span data-stu-id="897a0-163">Next tool \(from history\)</span></span> | `Ctrl`+`Shift`+`]` |  
| <span data-ttu-id="897a0-164">Следующий подкадровый</span><span class="sxs-lookup"><span data-stu-id="897a0-164">Next Subframe</span></span> | `F6` |  
| <span data-ttu-id="897a0-165">Предыдущий подкадровый</span><span class="sxs-lookup"><span data-stu-id="897a0-165">Previous Subframe</span></span> | `Shift`+`F6` |  
| <span data-ttu-id="897a0-166">Следующее совпадение в поле поиска</span><span class="sxs-lookup"><span data-stu-id="897a0-166">Next match in Search box</span></span> | `F3` |  
| <span data-ttu-id="897a0-167">Предыдущее совпадение в поле поиска</span><span class="sxs-lookup"><span data-stu-id="897a0-167">Previous match in Search box</span></span> | `Shift`+`F3` |  
| <span data-ttu-id="897a0-168">Поиск в поле поиска</span><span class="sxs-lookup"><span data-stu-id="897a0-168">Find in search box</span></span> | `Ctrl`+`F` |  
| <span data-ttu-id="897a0-169">Перемещение фокуса на консоль в нижней части экрана</span><span class="sxs-lookup"><span data-stu-id="897a0-169">Give focus to console at the bottom</span></span> | `Alt`+`Shift`+`I` |  
| <span data-ttu-id="897a0-170">Запустить DevTools на консоли</span><span class="sxs-lookup"><span data-stu-id="897a0-170">Launch DevTools to Console</span></span> | `Ctrl`+`Shift`+`J` |  
| <span data-ttu-id="897a0-171">Обновить страницу</span><span class="sxs-lookup"><span data-stu-id="897a0-171">Refresh the page</span></span> | `Ctrl`<span data-ttu-id="897a0-172">+`Shift`+`F5`, `Ctrl`+</span><span class="sxs-lookup"><span data-stu-id="897a0-172">+`Shift`+`F5`, `Ctrl`+</span></span>`R` |  

> [!NOTE]
> <span data-ttu-id="897a0-173">При отладке и приостановке в точке останова, при **обновлении действия страницы** сначала возобновляется среда выполнения.</span><span class="sxs-lookup"><span data-stu-id="897a0-173">If you are debugging and paused at a breakpoint, the **Refresh the page** action resumes the runtime first.</span></span>  

## <span data-ttu-id="897a0-174">Отзыв</span><span class="sxs-lookup"><span data-stu-id="897a0-174">Feedback</span></span>  

<span data-ttu-id="897a0-175">Пожалуйста, отправьте свой отзыв, чтобы помочь вам улучшить Microsoft Edge \ (EdgeHTML \) DevTools!</span><span class="sxs-lookup"><span data-stu-id="897a0-175">Please send your feedback to help improve the Microsoft Edge \(EdgeHTML\) DevTools for you!</span></span>  <span data-ttu-id="897a0-176">Просто откройте инструменты \ ( `F12` \) и нажмите кнопку [Отправить отзыв](#microsoft-edge-edgehtml-developer-tools) .</span><span class="sxs-lookup"><span data-stu-id="897a0-176">Simply open the tools \(`F12`\) and select the [Send feedback](#microsoft-edge-edgehtml-developer-tools) button.</span></span>  

<span data-ttu-id="897a0-177">Станьте участником программы [предварительной оценки Windows][WindowsInsiderProgram] , чтобы ознакомиться с [новейшими возможностями, выпущенными в DevTools][DevtoolsGuideEdgehtmlWhatsnew].</span><span class="sxs-lookup"><span data-stu-id="897a0-177">Become a [Windows Insider][WindowsInsiderProgram] to preview the [latest features coming to the DevTools][DevtoolsGuideEdgehtmlWhatsnew].</span></span>  <span data-ttu-id="897a0-178">Используйте приложение центра обратной связи Windows для публикации, отправки по голосованию, отслеживания и получения поддержки общих вариантов и проблем с Windows.</span><span class="sxs-lookup"><span data-stu-id="897a0-178">Use the Windows Feedback Hub app to post, up-vote, track and get support for general Windows suggestions and problems.</span></span>  

<!-- image links  -->  

<!--[ImageDevtoolsEdgehtml]: /microsoft-edge/devtools-guide/media/devtools.png "Microsoft Edge (EdgeHTML) DevTools"  -->  
<!--[ImageDevtoolsGuideEdgehtmlChooselocal]: /microsoft-edge/devtools-guide/media/chooser_local.png "DevTools app Local panel"  -->  
<!--[ImageDevtoolsGuideEdgehtmlRemote]: /microsoft-edge/devtools-guide/media/chooser_remote.png "DevTools app Remote panel"  -->  

<!-- links  -->  

[DevtoolsGuideEdgehtmlConsole]: /microsoft-edge/devtools-guide/console "Консоли"  
[DevtoolsGuideEdgehtmlDebugger]: /microsoft-edge/devtools-guide/debugger "Отладчика"  
[DevtoolsGuideEdgehtmlElements]: /microsoft-edge/devtools-guide/elements "Element"  
[DevtoolsGuideEdgehtmlEmulation]: /microsoft-edge/devtools-guide/emulation "Эмуляции"  
[DevtoolsGuideEdgehtmlMemory]: /microsoft-edge/devtools-guide/memory "Хватки"  
[DevtoolsGuideEdgehtmlNetwork]: /microsoft-edge/devtools-guide/network "Сетью"  
[DevtoolsGuideEdgehtmlPerformance]: /microsoft-edge/devtools-guide/performance "Эффективности"  
[DevtoolsGuideEdgehtmlServiceworkers]: /microsoft-edge/devtools-guide/service-workers "Обслуживание сотрудников"  
[DevtoolsGuideEdgehtmlStorage]: /microsoft-edge/devtools-guide/storage "Склад"  
[DevtoolsGuideEdgehtmlWhatsnew]: /microsoft-edge/devtools-guide/whats-new "DevTools в новейшем обновлении для Windows 10 (EdgeHTML 18)"  
[DevtoolsProtocolEdgehtmlIndex]: /microsoft-edge/devtools-protocol/index "Протокол DevTools Microsoft EDGE (EdgeHTML)"  
[DevtoolsProtocolEdgehtmlClientsEdgePreview]: /microsoft-edge/devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Клиенты Microsoft Edge DevTools Preview-DevTools Protocol"  
[HostingWebview]: /microsoft-edge/hosting/webview "WebView (EdgeHTML) для приложений для Windows 10"  
[PwasEdgehtmlIndex]: /microsoft-edge/progressive-web-apps-edgehtml/index "Прогрессивные веб-приложения (EdgeHTML) в Windows"  

[MicrosoftStoreEdgeDevtoolsPreview]: https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj "Предварительная версия DevTools Microsoft Edge"  

[WindowsInsiderProgram]: https://insider.windows.com "Программа предварительной оценки Windows"  

[BrowserstackEdgehtml]: https://www.browserstack.com/test-on-microsoft-edge-browser "Браузер Microsoft Edge — бесплатное тестирование | BrowserStack"  

[GithubMicrosoftChakracore]: https://github.com/Microsoft/ChakraCore "Microsoft/ChakraCore | GitHub"  

[TypeScriptIndex]: https://www.typescriptlang.org "TypeScript"  
