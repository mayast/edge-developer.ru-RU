---
description: Знакомство со средствами разработчика Microsoft EDGE (Chromium)
title: Инструменты разработчика Microsoft EDGE (Chromium)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2019
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 178f72fbc47f712882de6f9564478953f4834890
ms.sourcegitcommit: 24430258f363b7dd85f7067afd4565bf102b4a1f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2020
ms.locfileid: "10645310"
---
# <span data-ttu-id="41e44-104">Инструменты разработчика Microsoft EDGE (Chromium)</span><span class="sxs-lookup"><span data-stu-id="41e44-104">Microsoft Edge (Chromium) Developer Tools</span></span>  

<span data-ttu-id="41e44-105">Microsoft Edge использует проект Chromium Open Source для более лучшей веб-совместимости и меньшего разбиения на разные базовые веб-платформы.</span><span class="sxs-lookup"><span data-stu-id="41e44-105">Microsoft Edge has adopted the Chromium open source project to create better web compatibility and less fragmentation of different underlying web platforms.</span></span>  <span data-ttu-id="41e44-106">Это изменение должно облегчить создание и тестирование веб-сайтов в Microsoft EDGE и убедиться в том, что они работают должным образом даже при просмотре в другом браузере на базе Chromium (например, Google Chrome, Vivaldi, Opera или Brave).</span><span class="sxs-lookup"><span data-stu-id="41e44-106">This change should make it easier for you to build and test your websites in Microsoft Edge and ensure that each works as expected even while viewed in a different Chromium-based browser \(such as Google Chrome, Vivaldi, Opera, or Brave\).</span></span>  

<span data-ttu-id="41e44-107">Поскольку веб-сайты увеличили использование в непрерывном массиве типов устройств, сложность и накладные расходы, участвующие в тестировании веб-сайтов, были развернуты.</span><span class="sxs-lookup"><span data-stu-id="41e44-107">As the web has grown in usage across an ever-widening array of device types, the complexity and overhead involved in testing websites has exploded.</span></span> <span data-ttu-id="41e44-108">Поскольку веб-разработчики (особенно те, которые используют небольшие компании \) должны тестироваться в различных системах, вы можете обнаружить, что сайты хорошо подходят для всех типов устройств и для всех браузеров.</span><span class="sxs-lookup"><span data-stu-id="41e44-108">Since web developers \(particularly those at small companies\) must test against so many different systems, you may find it nearly impossible to ensure that sites work well on all device types and all browsers.</span></span>  <span data-ttu-id="41e44-109">Теперь, когда Microsoft Edge базируется на Chromium, группа Microsoft Edge стала упростила матрицу путем выравнивания веб-платформы Microsoft Edge с помощью других браузеров на основе Chromium и предоставила разработчикам средства для создания визуальных средств, как внутри браузера, так и с другими средствами разработчика, которые вы используете каждый день (например, код Visual Studio).</span><span class="sxs-lookup"><span data-stu-id="41e44-109">Now that Microsoft Edge is based on Chromium, the Microsoft Edge team has simplified the matrix by aligning the Microsoft Edge web platform with other Chromium-based browsers and provided a best-in-class developer tooling experience, both inside the browser and with the other developer tools you use every day \(such as Visual Studio Code\).</span></span>  

<span data-ttu-id="41e44-110">Если вы выйдете из Microsoft EDGE и вы в основном разрабатываете в Chromium-браузере, вам нужно прямо дома.</span><span class="sxs-lookup"><span data-stu-id="41e44-110">If you are checking out Microsoft Edge and you mainly develop in a Chromium-based browser, you should feel right at home.</span></span>  <span data-ttu-id="41e44-111">Средства разработчика Microsoft Edge \ (Chromium \) точно так же, как и инструменты разработчика, которые вы уже знаете и используете.</span><span class="sxs-lookup"><span data-stu-id="41e44-111">The Microsoft Edge \(Chromium\) Developer Tools function in the same way as the developer tools you already know and use.</span></span>  <span data-ttu-id="41e44-112">Дополнительные сведения можно найти [в разделе новые возможности DevTools Microsoft EDGE (Chromium)][DevtoolsGuideChromiumWhatsNewIndex].</span><span class="sxs-lookup"><span data-stu-id="41e44-112">For more information, see [What's new in the Microsoft Edge (Chromium) DevTools][DevtoolsGuideChromiumWhatsNewIndex].</span></span>  

:::image type="complex" source="./devtools-guide-chromium/media/devtools.png" alt-text="Microsoft EDGE (Chromium) DevTools":::
   <span data-ttu-id="41e44-114">Microsoft EDGE (Chromium) DevTools</span><span class="sxs-lookup"><span data-stu-id="41e44-114">Microsoft Edge (Chromium) DevTools</span></span>
:::image-end:::

<!--![Microsoft Edge (Chromium) DevTools](./devtools-guide-chromium/media/devtools.png)  -->  

<span data-ttu-id="41e44-115">Если вы выйдете к следующей версии Microsoft EDGE и вы уже разработали в Microsoft Edge \ (EdgeHTML \), у вас появились новые средства, которые помогут вам легко и быстро создавать и тестировать веб-сайты в Microsoft Edge!</span><span class="sxs-lookup"><span data-stu-id="41e44-115">If you are checking out the next version of Microsoft Edge and you previously developed in Microsoft Edge \(EdgeHTML\), you now have some great new tools that should make it easier and faster to build and test your websites in Microsoft Edge!</span></span>  

## <span data-ttu-id="41e44-116">Открытие DevTools</span><span class="sxs-lookup"><span data-stu-id="41e44-116">Open the DevTools</span></span>  

<span data-ttu-id="41e44-117">Если вы никогда раньше не использовали DevTools, инструменты разработчика Microsoft Edge — это набор средств, которые непосредственно встроены в браузер Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="41e44-117">If you have never used the DevTools before, the Microsoft Edge Developer Tools are a set of tools built directly into the Microsoft Edge browser.</span></span>  <span data-ttu-id="41e44-118">С помощью этих DevTools вы можете сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="41e44-118">With these DevTools, you are able to do the following.</span></span>  
*   <span data-ttu-id="41e44-119">Проверка и внесение изменений на веб-сайт HTML</span><span class="sxs-lookup"><span data-stu-id="41e44-119">Inspect and make changes to your HTML website</span></span>  
*   <span data-ttu-id="41e44-120">Редактирование CSS и мгновенное просматривайте просмотр веб-сайта</span><span class="sxs-lookup"><span data-stu-id="41e44-120">Edit CSS and instantly see preview how your website renders</span></span>  
*   <span data-ttu-id="41e44-121">Просмотр всех `console.log()` операторов из кода JavaScript на стороне внешнего пользователя</span><span class="sxs-lookup"><span data-stu-id="41e44-121">See all the `console.log()` statements from your front-end JavaScript code</span></span>  
*   <span data-ttu-id="41e44-122">Отладка сценария с помощью задания точек останова и пошагового прохода по строке</span><span class="sxs-lookup"><span data-stu-id="41e44-122">Debug your script by setting breakpoints and stepping through it line by line</span></span>  

<span data-ttu-id="41e44-123">все прямо в браузере.</span><span class="sxs-lookup"><span data-stu-id="41e44-123">all directly within the browser.</span></span>  <span data-ttu-id="41e44-124">Ниже приведены примеры некоторых функциональных возможностей, предоставляемых DevTools, для облегчения и более быстрой сборки и тестирования веб-сайтов в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="41e44-124">These are just examples of some of the features the DevTools provide to make it easier and faster for you to build and test your websites in Microsoft Edge.</span></span>  

<span data-ttu-id="41e44-125">Открытие DevTools</span><span class="sxs-lookup"><span data-stu-id="41e44-125">To open the DevTools</span></span>  
*   <span data-ttu-id="41e44-126">нажмите клавишу</span><span class="sxs-lookup"><span data-stu-id="41e44-126">press</span></span> `F12` 
*   <span data-ttu-id="41e44-127">нажмите клавишу `Ctrl` + `Shift` + `I` Windows \ ( `Command` + `Option` + `I` на macOS \).</span><span class="sxs-lookup"><span data-stu-id="41e44-127">press `Ctrl`+`Shift`+`I` on Windows \(`Command`+`Option`+`I` on macOS\)</span></span>  

<span data-ttu-id="41e44-128">Если вы хотите просмотреть HTML или CSS для элемента на сайте, щелкните элемент правой кнопкой мыши и выберите команду **проверить** , чтобы перейти на панель элементы.</span><span class="sxs-lookup"><span data-stu-id="41e44-128">If you want to see the HTML or CSS for an element on your site, right-click the element and select **Inspect** to jump into the Elements panel.</span></span>  <span data-ttu-id="41e44-129">Вы также можете нажать клавишу `Ctrl` + `Shift` + `C` Windows \ ( `Command` + `Option` + `C` на macOS \), чтобы открыть DevTools в **режиме проверки элементов** , который позволяет выбрать элемент на сайте и просмотреть HTML и CSS на панели " **элементы** ".</span><span class="sxs-lookup"><span data-stu-id="41e44-129">You may also press `Ctrl`+`Shift`+`C` on Windows \(`Command`+`Option`+`C` on macOS\) to open the DevTools in **Inspect Element Mode** which lets you select an element on the site and see the HTML and CSS in the **Elements** panel.</span></span>  

<span data-ttu-id="41e44-130">Если вы хотите просмотреть журналы из клиентского кода JavaScript или быстро запустить некоторый сценарий, нажмите клавишу `Ctrl` + `Shift` + `J` Windows \ ( `Command` + `Option` + `J` на macOS \), чтобы открыть панель консоли в DevTools.</span><span class="sxs-lookup"><span data-stu-id="41e44-130">If you want to see logs from your front-end JavaScript code or quickly run some script, press `Ctrl`+`Shift`+`J` on Windows \(`Command`+`Option`+`J` on macOS\) to launch the Console panel in the DevTools.</span></span>  

## <span data-ttu-id="41e44-131">Основные инструменты</span><span class="sxs-lookup"><span data-stu-id="41e44-131">Core tools</span></span>  

:::image type="complex" source="./devtools-guide-chromium/media/devtools-core-tools.png" alt-text="Основные инструменты для Microsoft EDGE (Chromium) DevTools":::
   <span data-ttu-id="41e44-133">Основные инструменты для Microsoft EDGE (Chromium) DevTools</span><span class="sxs-lookup"><span data-stu-id="41e44-133">Microsoft Edge (Chromium) DevTools core tools</span></span>
:::image-end:::

<!--![Microsoft Edge \(Chromium\) DevTools core tools](./devtools-guide-chromium/media/devtools-core-tools.png)  -->  

<span data-ttu-id="41e44-134">В Microsoft Edge \ (Chromium \) DevTools включены следующие панели.</span><span class="sxs-lookup"><span data-stu-id="41e44-134">The Microsoft Edge \(Chromium\) DevTools include the following panels.</span></span>  
*   <span data-ttu-id="41e44-135">Панель " **элементы** " для редактирования HTML и CSS, проверки свойств специальных возможностей, просмотра прослушивателей событий и установки контрольных точек изменений DOM</span><span class="sxs-lookup"><span data-stu-id="41e44-135">An **Elements** panel to edit HTML and CSS, inspect accessibility properties, view event listeners, and set DOM mutation breakpoints</span></span>  
*   <span data-ttu-id="41e44-136">**Консоль** для просмотра и фильтрации сообщений журнала, проверки объектов JavaScript и узлов DOM, а также выполнения JavaScript в контексте выбранного окна или фрейма</span><span class="sxs-lookup"><span data-stu-id="41e44-136">A **Console** to view and filter log messages, inspect JavaScript objects and DOM nodes, and run JavaScript in the context of the selected window or frame</span></span>  
*   <span data-ttu-id="41e44-137">Панель « **источники** », в которой можно открывать и редактировать код, задавать точки останова, пошагово прокручивать код и просматривать состояние веб-сайта в одной строке JavaScript за один раз.</span><span class="sxs-lookup"><span data-stu-id="41e44-137">A **Sources** panel to open and live edit your code, set breakpoints, step through code, and see the state of your website one line of JavaScript at a time</span></span>  
*   <span data-ttu-id="41e44-138">Панель **сети** для мониторинга и проверки запросов и ответов из кэша сети и браузера</span><span class="sxs-lookup"><span data-stu-id="41e44-138">A **Network** panel to monitor and inspect requests and responses from the network and browser cache</span></span>   
*   <span data-ttu-id="41e44-139">Панель **производительности** для профилирования времени и системных ресурсов, необходимых для вашего сайта</span><span class="sxs-lookup"><span data-stu-id="41e44-139">A **Performance** panel to profile the time and system resources required by your site</span></span>  
*   <span data-ttu-id="41e44-140">Панель **памяти** для измерения использования ресурсов памяти и сравнения снимков кучи в разных состояниях среды выполнения кода</span><span class="sxs-lookup"><span data-stu-id="41e44-140">A **Memory** panel to measure your use of memory resources and compare heap snapshots at different states of code runtime</span></span>  
*   <span data-ttu-id="41e44-141">Панель **приложения** для проверки, изменения и отладки манифестов веб-приложения, рабочих процессов служб и рабочих процессов служб.</span><span class="sxs-lookup"><span data-stu-id="41e44-141">An **Application** panel to inspect, modify, and debug web app manifests, service workers, and service worker caches.</span></span>  <span data-ttu-id="41e44-142">Вы также можете проверять хранение, базы данных и кэширование на панели **приложения** и управлять ими.</span><span class="sxs-lookup"><span data-stu-id="41e44-142">You may also inspect and manage storage, databases, and caches from the **Application** panel.</span></span>  
*   <span data-ttu-id="41e44-143">Панель **безопасности** для устранения проблем с безопасностью и проверки правильности реализации HTTPS на веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="41e44-143">A **Security** panel to debug security issues and ensure that you have properly implemented HTTPS on your website.</span></span>  <span data-ttu-id="41e44-144">HTTPS обеспечивает безопасность и целостность данных как для вашего сайта, так и для пользователей, которые предоставляют личную информацию на вашем сайте.</span><span class="sxs-lookup"><span data-stu-id="41e44-144">HTTPS provides critical security and data integrity for both your site and your users that provide personal information on your site.</span></span>  
*   <span data-ttu-id="41e44-145">Панель **аудитов** \ (теперь переименовывает **Lighthouse**\), чтобы запустить аудит веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="41e44-145">An **Audits** panel \(now renamed **Lighthouse**\) to run an audit of your website.</span></span>  <span data-ttu-id="41e44-146">Результаты аудита помогают улучшить качество сайта следующими способами.</span><span class="sxs-lookup"><span data-stu-id="41e44-146">The results of the audit help you improve the quality of your site in the following ways.</span></span>  
    *   <span data-ttu-id="41e44-147">Перехватывать распространенные ошибки, связанные с обеспечением доступности веб-сайта, его безопасности, выполнения и т. д.</span><span class="sxs-lookup"><span data-stu-id="41e44-147">Catch common errors related to making your website accessible, secure, performant, and so on.</span></span>  
    *   <span data-ttu-id="41e44-148">Устраните все ошибки.</span><span class="sxs-lookup"><span data-stu-id="41e44-148">Fix each error.</span></span>  
    *   <span data-ttu-id="41e44-149">Создание PWA.</span><span class="sxs-lookup"><span data-stu-id="41e44-149">Build a PWA.</span></span>  

[!INCLUDE [audits-panel-note](./devtools-guide-chromium/includes/audits-panel-note.md)]  

<span data-ttu-id="41e44-150">Пожалуйста, отправляйте [Отзывы и запросы функций](#getting-in-touch-with-the-microsoft-edge-devtools-team)!</span><span class="sxs-lookup"><span data-stu-id="41e44-150">Please send your [feedback and feature requests](#getting-in-touch-with-the-microsoft-edge-devtools-team)!</span></span>  

## <span data-ttu-id="41e44-151">Расширения</span><span class="sxs-lookup"><span data-stu-id="41e44-151">Extensions</span></span>  

<span data-ttu-id="41e44-152">Возможно, вы использовали расширения для DevTools, которые помогут вам диагностировать и отлаживать проблемы при создании веб-сайтов или приложений.</span><span class="sxs-lookup"><span data-stu-id="41e44-152">You may have used extensions to the DevTools to help you diagnose and debug issues when building your websites or apps.</span></span>  <span data-ttu-id="41e44-153">Вы можете получить расширения для Microsoft EDGE на странице [надстроек Microsoft Edge][MicrosoftEdgeAddonsExtensions] .</span><span class="sxs-lookup"><span data-stu-id="41e44-153">You may acquire extensions for Microsoft Edge from the [Microsoft Edge Addons][MicrosoftEdgeAddonsExtensions] page.</span></span>  <span data-ttu-id="41e44-154">На странице [надстроек Microsoft Edge][MicrosoftEdgeAddonsExtensions] вы можете просматривать расширения DevTools из категории " **средства разработчика** " или поиска по определенному расширению.</span><span class="sxs-lookup"><span data-stu-id="41e44-154">From the [Microsoft Edge Addons][MicrosoftEdgeAddonsExtensions] page, you may browse DevTools extensions from the **Developer tools** category or search for a specific extension.</span></span>  

<span data-ttu-id="41e44-155">Вы также можете добавлять расширения из [веб-магазина Chrome][GoogleChromeWebstoreExtensions].</span><span class="sxs-lookup"><span data-stu-id="41e44-155">You may also add extensions from the [Chrome Web Store][GoogleChromeWebstoreExtensions].</span></span>  

:::image type="complex" source="./devtools-guide-chromium/media/allow-extensions-from-stores.png" alt-text="Веб-магазин Chrome в Microsoft Edge":::
   <span data-ttu-id="41e44-157">Веб-магазин Chrome в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="41e44-157">Chrome Web Store in Microsoft Edge</span></span>
:::image-end:::

<!--![Chrome Web Store in Microsoft Edge](./devtools-guide-chromium/media/allow-extensions-from-stores.png)  -->

<span data-ttu-id="41e44-158">В верхней части экрана выберите **Разрешить расширения из других магазинов** и нажмите кнопку **Разрешить** в появившемся диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="41e44-158">At the top, select **Allow extensions from other stores** and then select **Allow** in the dialog that appears.</span></span>  

> [!NOTE]
> <span data-ttu-id="41e44-159">Расширения, установленные из источников, отличных от Microsoft Store, не проверяются и могут повлиять на производительность браузера.</span><span class="sxs-lookup"><span data-stu-id="41e44-159">Extensions installed from sources other than the Microsoft Store are unverified, and may affect browser performance.</span></span>  

<span data-ttu-id="41e44-160">Нажмите кнопку **Добавить в хром** , чтобы добавить расширение DevTools в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="41e44-160">Select **Add to Chrome** to add your DevTools extension to Microsoft Edge!</span></span>  

:::image type="complex" source="./devtools-guide-chromium/media/install-extension-from-chrome-store.png" alt-text="Добавление расширения из веб-магазина Chrome в Microsoft Edge":::
   <span data-ttu-id="41e44-162">Добавление расширения из веб-магазина Chrome в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="41e44-162">Adding extension from Chrome Web Store to Microsoft Edge</span></span>
:::image-end:::

<!--![Adding extension from Chrome Web Store to Microsoft Edge](./devtools-guide-chromium/media/install-extension-from-chrome-store.png)  -->  

## <span data-ttu-id="41e44-163">Горячие</span><span class="sxs-lookup"><span data-stu-id="41e44-163">Shortcuts</span></span>  

<span data-ttu-id="41e44-164">Эти сочетания клавиш управляют основным окном DevTools, работают во всех инструментах или оба.</span><span class="sxs-lookup"><span data-stu-id="41e44-164">These shortcuts control the main DevTools window, work across all tools, or both.</span></span>  

| <span data-ttu-id="41e44-165">Действие</span><span class="sxs-lookup"><span data-stu-id="41e44-165">Action</span></span> | <span data-ttu-id="41e44-166">Windows</span><span class="sxs-lookup"><span data-stu-id="41e44-166">Windows</span></span> | <span data-ttu-id="41e44-167">macOS</span><span class="sxs-lookup"><span data-stu-id="41e44-167">macOS</span></span> |  
|:--- |:--- | :--- |  
| <span data-ttu-id="41e44-168">Показать или скрыть DevTools \ (открывается в последней просмотренной панели \)</span><span class="sxs-lookup"><span data-stu-id="41e44-168">Show/Hide DevTools \(opens to last viewed panel\)</span></span> | `F12` <span data-ttu-id="41e44-169">/`Ctrl`+`Shift`+</span><span class="sxs-lookup"><span data-stu-id="41e44-169">or `Ctrl`+`Shift`+</span></span>`I` | `Command`+`Option`+`I` |  
| <span data-ttu-id="41e44-170">Отображение панели консоли</span><span class="sxs-lookup"><span data-stu-id="41e44-170">Show the Console panel</span></span> | `Ctrl`+`Shift`+`J` | `Command`+`Option`+`J` |  
| <span data-ttu-id="41e44-171">Показать DevTools в **режиме проверки элемента** , который позволяет выбрать элемент на сайте и просмотреть HTML и CSS на панели " **элементы** "</span><span class="sxs-lookup"><span data-stu-id="41e44-171">Show the DevTools in **Inspect Element Mode** which lets you select an element on the site and see the HTML and CSS in the **Elements** panel</span></span> | `Ctrl`+`Shift`+`C` | `Command`+`Option`+`C` |  
| <span data-ttu-id="41e44-172">Показать параметры</span><span class="sxs-lookup"><span data-stu-id="41e44-172">Show Settings</span></span> | `?` <span data-ttu-id="41e44-173">/`Fn`+</span><span class="sxs-lookup"><span data-stu-id="41e44-173">or `Fn`+</span></span>`F1` | `?` <span data-ttu-id="41e44-174">/`Fn`+</span><span class="sxs-lookup"><span data-stu-id="41e44-174">or `Fn`+</span></span>`F1` |  
| <span data-ttu-id="41e44-175">Переход к следующей панели</span><span class="sxs-lookup"><span data-stu-id="41e44-175">Show the next panel</span></span> | `Ctrl`+`]` | `Command`+`]` |  
| <span data-ttu-id="41e44-176">Показать предыдущую панель</span><span class="sxs-lookup"><span data-stu-id="41e44-176">Show the previous panel</span></span> | `Ctrl`+`[` | `Command`+`[` |  
| <span data-ttu-id="41e44-177">Закрепите DevTools в последней использованной вакансии.</span><span class="sxs-lookup"><span data-stu-id="41e44-177">Dock the DevTools in the last position used.</span></span>  <span data-ttu-id="41e44-178">Если DevTools остается в положении по умолчанию для всего сеанса, этот ярлык отсоединяет DevTools в отдельном окне.</span><span class="sxs-lookup"><span data-stu-id="41e44-178">If the DevTools remain in the default position for the entire session, this shortcut undocks the DevTools into a separate window</span></span> | `Ctrl`+`Shift`+`D` | `Command`+`Shift`+`D` |  
| <span data-ttu-id="41e44-179">Переключение **режима устройства**</span><span class="sxs-lookup"><span data-stu-id="41e44-179">Toggle **Device Mode**</span></span> | `Ctrl`+`Shift`+`M` | `Command`+`Shift`+`M` |  
| <span data-ttu-id="41e44-180">Переключение **режима проверки элемента** , который позволяет выбрать элемент на сайте и просмотреть HTML и CSS на панели " **элементы** "</span><span class="sxs-lookup"><span data-stu-id="41e44-180">Toggle **Inspect Element Mode** which lets you select an element on the site and see the HTML and CSS in the **Elements** panel</span></span> | `Ctrl`+`Shift`+`C` | `Command`+`Shift`+`C` |  
| <span data-ttu-id="41e44-181">Показать меню команд</span><span class="sxs-lookup"><span data-stu-id="41e44-181">Show the Command Menu</span></span> | `Ctrl`+`Shift`+`P` | `Command`+`Shift`+`P` |  
| <span data-ttu-id="41e44-182">Показать или скрыть денежный ящик</span><span class="sxs-lookup"><span data-stu-id="41e44-182">Show/Hide the Drawer</span></span> | `Esc` | `Esc` |  
| <span data-ttu-id="41e44-183">Обновлен.</span><span class="sxs-lookup"><span data-stu-id="41e44-183">Refresh.</span></span>  <span data-ttu-id="41e44-184">Страница будет обновлена с помощью кэша.</span><span class="sxs-lookup"><span data-stu-id="41e44-184">This refreshes the page using the cache.</span></span>  | `F5` <span data-ttu-id="41e44-185">/`Ctrl`+</span><span class="sxs-lookup"><span data-stu-id="41e44-185">or `Ctrl`+</span></span>`R` | `Command`+`R` |  
| <span data-ttu-id="41e44-186">Жесткое обновление.</span><span class="sxs-lookup"><span data-stu-id="41e44-186">Hard Refresh.</span></span>  <span data-ttu-id="41e44-187">Это заставляет Microsoft Edge загрузить ресурсы еще раз и перезагрузить.</span><span class="sxs-lookup"><span data-stu-id="41e44-187">This forces Microsoft Edge to download resources again and reload.</span></span>  <span data-ttu-id="41e44-188">Возможно, используемые ресурсы могут поступать из кэшированной версии.</span><span class="sxs-lookup"><span data-stu-id="41e44-188">It is possible that the used resources may come from a cached version</span></span> | `Ctrl`<span data-ttu-id="41e44-189">+`F5`/`Ctrl`+`Shift`+</span><span class="sxs-lookup"><span data-stu-id="41e44-189">+`F5` or `Ctrl`+`Shift`+</span></span>`R` | `Command`+`Shift`+`R` |  
| <span data-ttu-id="41e44-190">Поиск текста на текущей панели.</span><span class="sxs-lookup"><span data-stu-id="41e44-190">Search for text within the current panel.</span></span>  <span data-ttu-id="41e44-191">Не поддерживается в панелях аудит, приложения и безопасность</span><span class="sxs-lookup"><span data-stu-id="41e44-191">Not supported in the Audits, Application, and Security panels</span></span> | `Ctrl`+`F` | `Command`+`F` |  
| <span data-ttu-id="41e44-192">Отображение панели поиска в ящике, позволяющей искать текст во всех загруженных ресурсах</span><span class="sxs-lookup"><span data-stu-id="41e44-192">Show the Search panel in the Drawer, which lets you search for text across all loaded resources</span></span> | `Ctrl`+`Shift`+`F` | `Command`+`Option`+`F` |  
| <span data-ttu-id="41e44-193">Открытие файла на панели «источники»</span><span class="sxs-lookup"><span data-stu-id="41e44-193">Open a file in the Sources panel</span></span> | `Ctrl`<span data-ttu-id="41e44-194">+`O`/`Ctrl`+</span><span class="sxs-lookup"><span data-stu-id="41e44-194">+`O` or `Ctrl`+</span></span>`P` | `Command`<span data-ttu-id="41e44-195">+`O`/`Command`+</span><span class="sxs-lookup"><span data-stu-id="41e44-195">+`O` or `Command`+</span></span>`P` |  
| <span data-ttu-id="41e44-196">Увеличить масштаб</span><span class="sxs-lookup"><span data-stu-id="41e44-196">Zoom in</span></span> | `Ctrl`+`Shift`+`+` | `Command`+`Shift`+`+` |  
| <span data-ttu-id="41e44-197">Уменьшить</span><span class="sxs-lookup"><span data-stu-id="41e44-197">Zoom out</span></span> | `Ctrl`+`-` | `Command`+`-` |  
| <span data-ttu-id="41e44-198">Восстановление масштаба по умолчанию</span><span class="sxs-lookup"><span data-stu-id="41e44-198">Restore default zoom level</span></span> | `Ctrl`+`0` | `Command`+`0` |  
| <span data-ttu-id="41e44-199">Выполнить сниппет</span><span class="sxs-lookup"><span data-stu-id="41e44-199">Run snippet</span></span> | `Ctrl`<span data-ttu-id="41e44-200">+`O`или `Ctrl` + `P` введите `!` имя сценария, а затем нажмите клавишу</span><span class="sxs-lookup"><span data-stu-id="41e44-200">+`O` or `Ctrl`+`P`, type `!` followed by the name of the script, then press</span></span> `Enter` | <span data-ttu-id="41e44-201">Нажмите клавишу `Command` + `O` или `Command` + `P` , введите `!` имя сценария, а затем нажмите клавишу</span><span class="sxs-lookup"><span data-stu-id="41e44-201">Press `Command`+`O` or `Command`+`P`, type `!` followed by the name of the script, then press</span></span> `Enter` |  
| <span data-ttu-id="41e44-202">Отображение нередактируемого исходного кода HTML на новой вкладке</span><span class="sxs-lookup"><span data-stu-id="41e44-202">Show non-editable HTML source code in a new tab</span></span> | `Ctrl`+`U` | <span data-ttu-id="41e44-203">Н/Д</span><span class="sxs-lookup"><span data-stu-id="41e44-203">N/A</span></span> |  

> [!NOTE]
> <span data-ttu-id="41e44-204">При отладке и приостановке в точке останова сначала восстанавливается ярлык **обновления**.</span><span class="sxs-lookup"><span data-stu-id="41e44-204">If you are debugging and paused at a breakpoint, the **Refresh**shortcut resumes the runtime first.</span></span>  

## <span data-ttu-id="41e44-205">См. также</span><span class="sxs-lookup"><span data-stu-id="41e44-205">See also</span></span>  

*   [<span data-ttu-id="41e44-206">DevTools для начинающих: Приступая к работе с HTML и моделью DOM</span><span class="sxs-lookup"><span data-stu-id="41e44-206">DevTools for Beginners: Get Started with HTML and the DOM</span></span>][DevtoolsGuideChromiumBeginnersHtml]  
*   [<span data-ttu-id="41e44-207">Протокол DevTools Microsoft EDGE (Chromium)</span><span class="sxs-lookup"><span data-stu-id="41e44-207">Microsoft Edge (Chromium) DevTools Protocol</span></span>][DevtoolsProtocolChromiumIndex]  

## <span data-ttu-id="41e44-208">Знакомство с командой Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="41e44-208">Getting in touch with the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="41e44-209">Отправьте свой отзыв, чтобы команда Microsoft Edge продолжала улучшать Microsoft Edge DevTools.</span><span class="sxs-lookup"><span data-stu-id="41e44-209">Please send your feedback, so the Microsoft Edge team continues improving the Microsoft Edge DevTools for you!</span></span>  <span data-ttu-id="41e44-210">Просто щелкните значок **обратной связи** в DevTools или нажмите `Alt` + `Shift` + `I` на Windows \ ( `Option` + `Shift` + `I` в macOS \) и введите любые отзывы или предложения по функциям для DevTools.</span><span class="sxs-lookup"><span data-stu-id="41e44-210">Simply select the **Feedback** icon in the DevTools or press `Alt`+`Shift`+`I` on Windows \(`Option`+`Shift`+`I` on macOS\) and enter any feedback or feature requests you have for the DevTools.</span></span>  

:::image type="complex" source="./devtools-guide-chromium/media/devtools-feedback.png" alt-text="Обратная связь в Microsoft Edge":::
   <span data-ttu-id="41e44-212">Обратная связь в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="41e44-212">Give feedback on Microsoft Edge</span></span>
:::image-end:::

<!--![Give feedback on Microsoft Edge](./devtools-guide-chromium/media/devtools-feedback.png)  -->  

<span data-ttu-id="41e44-213">Если вы хотите просмотреть [последние функции DevTools][DevtoolsGuideChromiumWhatsNewIndex], скачайте [Microsoft Edge Канарские][MicrosoftedgeinsiderDownload], который строится на ночь.</span><span class="sxs-lookup"><span data-stu-id="41e44-213">If you want to preview the [latest features coming to the DevTools][DevtoolsGuideChromiumWhatsNewIndex], download [Microsoft Edge Canary][MicrosoftedgeinsiderDownload], which builds nightly.</span></span>  

<!-- image links -->  

<!-- links -->  

[DevtoolsGuideChromiumBeginnersHtml]: /microsoft-edge/devtools-guide-chromium/beginners/html "DevTools для начинающих: Приступая к работе с HTML и моделью DOM | Документы Microsoft"  
[DevtoolsGuideChromiumWhatsNewIndex]: ./devtools-guide-chromium/whats-new.md "Новые возможности Microsoft EDGE (Chromium) DevTools | Документы Microsoft"  
[DevtoolsProtocolChromiumIndex]: /microsoft-edge/devtools-protocol-chromium "Протокол Microsoft EDGE (Chromium) DevTools Protocol | Документы Microsoft"  

[MicrosoftEdgeAddonsExtensions]: https://microsoftedge.microsoft.com/addons/category/Edge-Extensions "Надстройки Microsoft Edge"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Скачайте каналы предварительной оценки Microsoft Edge"  

[GoogleChromeWebstoreExtensions]: https://chrome.google.com/webstore/category/extensions "Расширения | Веб-магазин Chrome"  
