---
description: Трехмерное представление, интеграция Visual Studio с Microsoft EDGE и многое другое.
title: Новые возможности DevTools (Microsoft Edge 81)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 9dd47a38f345601f2d459d39e3ee7b1728df8971
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993417"
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

# <span data-ttu-id="a4535-104">Новые возможности DevTools (Microsoft Edge 81)</span><span class="sxs-lookup"><span data-stu-id="a4535-104">What's New In DevTools (Microsoft Edge 81)</span></span>  

## <span data-ttu-id="a4535-105">Объявления из группы Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="a4535-105">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="a4535-106">В следующих разделах представлен список извещений, которые вы могли не получить в Microsoft Edge DevTools Teams!</span><span class="sxs-lookup"><span data-stu-id="a4535-106">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team!</span></span> <span data-ttu-id="a4535-107">Узнайте, как использовать новые функции в DevTools, расширения кода VS и многое другое.</span><span class="sxs-lookup"><span data-stu-id="a4535-107">Check them out to try new features in the DevTools, VS Code extensions, and more.</span></span>  <span data-ttu-id="a4535-108">Чтобы оставаться на связи с самыми последними и более свежими возможностями, скачайте на веб – [каналы предварительной версии Microsoft Edge][MicrosoftEdgePreviewChannels] и [следуйте указаниям Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="a4535-108">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <span data-ttu-id="a4535-109">Улучшение специальных возможностей в DevTools</span><span class="sxs-lookup"><span data-stu-id="a4535-109">Accessibility improvements to the DevTools</span></span>  

<span data-ttu-id="a4535-110">Группа DevTools изменила 170 в Chromium для устранения проблем с высокой контрастностью цвета, клавиатуры и средства чтения с экрана в DevTools.</span><span class="sxs-lookup"><span data-stu-id="a4535-110">The DevTools team has contributed 170 changes to Chromium to address high-impact color contrast, keyboard, and screen reader issues in the DevTools.</span></span>  <span data-ttu-id="a4535-111">Каждый разработчик, создающий веб-сайт, должен иметь возможность использовать DevTools.</span><span class="sxs-lookup"><span data-stu-id="a4535-111">Every developer building the web should be able to use the DevTools.</span></span>  

> ##### <span data-ttu-id="a4535-112">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="a4535-112">Figure 1</span></span>  
> <span data-ttu-id="a4535-113">Средство "производительность" в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана</span><span class="sxs-lookup"><span data-stu-id="a4535-113">The Performance tool in the DevTools with the keyboard navigation and screen reader improvements</span></span>  
> ![Средство "производительность" в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана][ImagePerformanceToolKeyboardReaderImprovements]  

<span data-ttu-id="a4535-115">Сведения о том, как сделать веб-страницу доступной для всех пользователей?</span><span class="sxs-lookup"><span data-stu-id="a4535-115">Want to learn how to make your web page accessible to all of your users?</span></span>  <span data-ttu-id="a4535-116">Скачайте [расширения для][WebhintBrowserExtension] Microsoft Edge " [Специальные возможности][AccessibilityInsights] ", чтобы приступить к работе.</span><span class="sxs-lookup"><span data-stu-id="a4535-116">Download the [Accessibility Insights][AccessibilityInsights] and [webhint][WebhintBrowserExtension] extensions for Microsoft Edge to get started.</span></span>  

<span data-ttu-id="a4535-117">Если вы используете средства чтения с экрана или клавиатуру для навигации по DevTools, отправьте нам свой отзыв, выполнив [твит][PostTweetEdgeDevTools] в США или щелкнув значок [Отправить отзыв](#getting-in-touch-with-microsoft-edge-devtools-team) !</span><span class="sxs-lookup"><span data-stu-id="a4535-117">If you use screen readers or the keyboard to navigate around the DevTools, send us your feedback by [tweeting][PostTweetEdgeDevTools] at us or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="a4535-118">[#963183][crbug963183] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="a4535-118">Chromium issue [#963183][crbug963183]</span></span>  

### <span data-ttu-id="a4535-119">Использование DevTools на других языках</span><span class="sxs-lookup"><span data-stu-id="a4535-119">Using the DevTools in other languages</span></span>  

<span data-ttu-id="a4535-120">Многие разработчики используют другие инструменты разработчика, такие как StackOverflow и код VS, на родном языке, а не только на английском языке.</span><span class="sxs-lookup"><span data-stu-id="a4535-120">Many developers use other developer tools, like StackOverflow and VS Code, in their native language, not just in English.</span></span>  <span data-ttu-id="a4535-121">Мы рады объявить локализацию для DevTools, который теперь вы можете использовать на одном из 10 языков, кроме английского.</span><span class="sxs-lookup"><span data-stu-id="a4535-121">We’re excited to announce localization for the DevTools, which you are now able to use in one of 10 languages besides English:</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="a4535-122">Китайский (упрощенное письмо) —  &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span><span class="sxs-lookup"><span data-stu-id="a4535-122">Chinese \(Simplified\) - &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="a4535-123">Китайский (традиционное письмо) —  &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span><span class="sxs-lookup"><span data-stu-id="a4535-123">Chinese \(Traditional\) - &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="a4535-124">Французский — Fran&#231;AIS</span><span class="sxs-lookup"><span data-stu-id="a4535-124">French – fran&#231;ais</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="a4535-125">Немецкий — Deutsch</span><span class="sxs-lookup"><span data-stu-id="a4535-125">German - deutsch</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="a4535-126">Итальянский — Italiano</span><span class="sxs-lookup"><span data-stu-id="a4535-126">Italian - italiano</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="a4535-127">Японская  &#26085;&#26412;&#35486;</span><span class="sxs-lookup"><span data-stu-id="a4535-127">Japanese - &#26085;&#26412;&#35486;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="a4535-128">Корейский —  &#54620;&#44397;&#50612;</span><span class="sxs-lookup"><span data-stu-id="a4535-128">Korean - &#54620;&#44397;&#50612;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="a4535-129">Португальский (portugu&#234;s)</span><span class="sxs-lookup"><span data-stu-id="a4535-129">Portuguese - portugu&#234;s</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="a4535-130">Русский —  &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span><span class="sxs-lookup"><span data-stu-id="a4535-130">Russian – &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="a4535-131">Испанская — ESPA&#241;OL</span><span class="sxs-lookup"><span data-stu-id="a4535-131">Spanish - espa&#241;ol</span></span>
   :::column-end:::
:::row-end:::

<!--  
|  |  |  
|:--- |:--- |  
| Chinese (Simplified) - 中文(简体)（简体）| Chinese (Traditional) - 中文(繁體)（繁體）|  
| French – français | German - deutsch |  
| Italian - italiano | Portuguese - português |  
| Korean - 한국어 | Japanese - 日本語 |  
| Russian – русский | Spanish - español |  
-->  

<span data-ttu-id="a4535-132">DevTools автоматически соответствует языку, который вы используете для Microsoft Edge in `edge://settings/languages` .</span><span class="sxs-lookup"><span data-stu-id="a4535-132">The DevTools automatically match the language you use for Microsoft Edge in `edge://settings/languages`.</span></span>  

<span data-ttu-id="a4535-133">Если вы хотите, чтобы Microsoft Edge выоставался на одном языке, а DevTools на русском языке, нажмите кнопку `F1` DevTools, чтобы открыть вкладку [Параметры][Settings] и отключить **язык браузера**.</span><span class="sxs-lookup"><span data-stu-id="a4535-133">If you want Microsoft Edge to be in one language and your DevTools to remain in English, press `F1` in the DevTools to open [Settings][Settings] and disable **Match browser language**.</span></span>  

> ##### <span data-ttu-id="a4535-134">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="a4535-134">Figure 2</span></span>  
> <span data-ttu-id="a4535-135">DevTools на немецком языке</span><span class="sxs-lookup"><span data-stu-id="a4535-135">The DevTools in German</span></span>  
> ![DevTools на немецком языке][ImageLocalizedGerman]  

<span data-ttu-id="a4535-137">Сообщения **консоли** не локализуются.</span><span class="sxs-lookup"><span data-stu-id="a4535-137">**Console** messages are not localized.</span></span>  <span data-ttu-id="a4535-138">На языке, используемом для Microsoft EDGE, отображаются только строки, используемые в пользовательском интерфейсе DevTools.</span><span class="sxs-lookup"><span data-stu-id="a4535-138">Only the strings used in the DevTools UI are displayed in the language you use for Microsoft Edge.</span></span>  

<span data-ttu-id="a4535-139">Если вы хотите использовать DevTools на языке, отличном от того, на котором они доступны, [твит][PostTweetEdgeDevTools] в США или щелкните значок [Отправить отзыв](#getting-in-touch-with-microsoft-edge-devtools-team) .</span><span class="sxs-lookup"><span data-stu-id="a4535-139">If you want to use the DevTools in a different language than the ones that are available, [tweet][PostTweetEdgeDevTools] at us or click the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon.</span></span>  

<span data-ttu-id="a4535-140">[#941561][crbug941561] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="a4535-140">Chromium issue [#941561][crbug941561]</span></span>  

### <span data-ttu-id="a4535-141">Веб – подсказка с расширением Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a4535-141">webhint Microsoft Edge extension</span></span>  

<span data-ttu-id="a4535-142">Расширение веб-подсказки Microsoft EDGE позволяет легко находить и получать отзывы о специальных возможностях, совместимости с браузерами, безопасности, производительности и других средствах в DevTools.</span><span class="sxs-lookup"><span data-stu-id="a4535-142">The webhint Microsoft Edge extension allows you to easily scan your web page and get feedback on accessibility, browser compatibility, security, performance, and more within the DevTools.</span></span>  <span data-ttu-id="a4535-143">Узнайте больше о [https://webhint.io][Webhint] .</span><span class="sxs-lookup"><span data-stu-id="a4535-143">Read more at [https://webhint.io][Webhint].</span></span>  

> ##### <span data-ttu-id="a4535-144">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="a4535-144">Figure 3</span></span>  
> <span data-ttu-id="a4535-145">Вкладка "Подсказка" в DevTools, если установлено расширение браузера веб.</span><span class="sxs-lookup"><span data-stu-id="a4535-145">The Hints tab in the DevTools when the webhint browser extension is installed</span></span>  
> ![Вкладка "Подсказка" в DevTools, если установлено расширение браузера веб.][ImageHintsTabWebhintExtension]  

<span data-ttu-id="a4535-147">[Попробуйте расширение браузера веб для подсказки в Microsoft Edge][MicrosoftEdgeInsiderAddons].</span><span class="sxs-lookup"><span data-stu-id="a4535-147">[Try the webhint browser extension in Microsoft Edge][MicrosoftEdgeInsiderAddons].</span></span>  <span data-ttu-id="a4535-148">После установки расширения откройте DevTools и перейдите на вкладку подсказки.  В этой статье запустите настраиваемое сканирование сайта.</span><span class="sxs-lookup"><span data-stu-id="a4535-148">Once you install the extension, open the DevTools and select the Hints tab.  From here, run a customizable site scan.</span></span>  <span data-ttu-id="a4535-149">Чтобы получить дополнительные сведения, [заwebhint.IO][WebhintBrowserExtension] в голову.</span><span class="sxs-lookup"><span data-stu-id="a4535-149">Head over to [webhint.io][WebhintBrowserExtension] to learn more.</span></span>  

### <span data-ttu-id="a4535-150">Трехмерное представление</span><span class="sxs-lookup"><span data-stu-id="a4535-150">3D View</span></span>  

<span data-ttu-id="a4535-151">С помощью **трехмерного представления** вы можете выполнять отладку своего веб-приложения, перемещаясь по [объектной модели документов \ (DOM)][MDNDocumentObjectModel] или контексту стека [z-индексов][MDNZIndex] .</span><span class="sxs-lookup"><span data-stu-id="a4535-151">Use the **3D View** to debug your web application by navigating through the [Document Object Model \(DOM\)][MDNDocumentObjectModel] or the [z-index][MDNZIndex] stacking context.</span></span>  

> ##### <span data-ttu-id="a4535-152">Рисунок4</span><span class="sxs-lookup"><span data-stu-id="a4535-152">Figure 4</span></span>  
> <span data-ttu-id="a4535-153">Трехмерное представление в DevTools</span><span class="sxs-lookup"><span data-stu-id="a4535-153">The 3D View in the DevTools</span></span>  
> ![Трехмерное представление в DevTools][Image3DView]  

<span data-ttu-id="a4535-155">Для доступа к трехмерному представлению нажмите клавишу `Ctrl`  +  `Shift`  +  `P` Ввод в **режиме 3D-представления** и выберите **Показать 3D-представление**.</span><span class="sxs-lookup"><span data-stu-id="a4535-155">To access the 3D View, press `Ctrl` + `Shift` + `P`, type in **3D View** and select **Show 3D View**.</span></span>  

<span data-ttu-id="a4535-156">Мы работаем над ИНТЕРФЕЙСом и добавляем дополнительные функции в 3D-представление, поэтому отправьте нам свой [отзыв](#getting-in-touch-with-microsoft-edge-devtools-team).</span><span class="sxs-lookup"><span data-stu-id="a4535-156">We're working on the UI and adding more functionality to the 3D View, so please send us your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team).</span></span>  

<span data-ttu-id="a4535-157">[#987787][crbug987787] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="a4535-157">Chromium issue [#987787][crbug987787]</span></span>  

### <span data-ttu-id="a4535-158">Расширения кода Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a4535-158">Visual Studio Code extensions</span></span>  

<span data-ttu-id="a4535-159">Кроме того, Группа DevTools также выпустила некоторые расширения для [кода Visual Studio \ (код VS)][VisualStudioCode] , которые позволяют использовать возможности DevTools прямо из текстового редактора.</span><span class="sxs-lookup"><span data-stu-id="a4535-159">The DevTools team has also released some extensions for [Visual Studio Code \(VS Code\)][VisualStudioCode] that let you use the power of the DevTools directly from your text editor!</span></span> <span data-ttu-id="a4535-160">Ознакомьтесь с приведенными ниже расширениями.</span><span class="sxs-lookup"><span data-stu-id="a4535-160">Check out the extensions below:</span></span>  

#### <span data-ttu-id="a4535-161">Элементы Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a4535-161">Elements for Microsoft Edge</span></span>  

<span data-ttu-id="a4535-162">С помощью инструмента "элементы" в коде VS добавьте [элементы для расширения кода Microsoft Edge \ (Chromium \)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] vs.</span><span class="sxs-lookup"><span data-stu-id="a4535-162">Use the Elements tool from within VS Code by adding the [Elements for Microsoft Edge \(Chromium\)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] VS Code extension.</span></span>  

> ##### <span data-ttu-id="a4535-163">Рисунок 5</span><span class="sxs-lookup"><span data-stu-id="a4535-163">Figure 5</span></span>  
> <span data-ttu-id="a4535-164">Инструмент "элементы" в коде VS с использованием элементов для расширения Microsoft Edge — ![ инструмент "элементы" в коде VS с использованием элементов для расширения Microsoft Edge][ImageElementsVisualStudioCode]</span><span class="sxs-lookup"><span data-stu-id="a4535-164">The Elements tool in VS Code using the Elements for Microsoft Edge extension ![The Elements tool in VS Code using the Elements for Microsoft Edge extension][ImageElementsVisualStudioCode]</span></span>  

<span data-ttu-id="a4535-165">Для получения дополнительных сведений изучите [элементы для расширения кода Microsoft Edge VS][VisualStudioCodeElementEdgeExtension].</span><span class="sxs-lookup"><span data-stu-id="a4535-165">For more information, check out [Elements for Microsoft Edge VS Code extension][VisualStudioCodeElementEdgeExtension].</span></span>  

#### <span data-ttu-id="a4535-166">Отладчик для Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a4535-166">Debugger for Microsoft Edge</span></span>  

<span data-ttu-id="a4535-167">С помощью [отладчика для расширения кода Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] , Отладка JavaScript выполняется в Microsoft Edge прямо из кода vs.</span><span class="sxs-lookup"><span data-stu-id="a4535-167">With the [Debugger for Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] VS Code extension, debug JavaScript running in Microsoft Edge directly from VS Code!</span></span>  

> ##### <span data-ttu-id="a4535-168">Рисунок6</span><span class="sxs-lookup"><span data-stu-id="a4535-168">Figure 6</span></span>  
> <span data-ttu-id="a4535-169">Отладчик для расширения Microsoft EDGE в коде VS</span><span class="sxs-lookup"><span data-stu-id="a4535-169">The Debugger for Microsoft Edge Extension in VS Code</span></span>  
> ![Отладчик для расширения Microsoft EDGE в коде VS][ImageDebuggerExtensionVisualStudioCode]  

<span data-ttu-id="a4535-171">Дополнительные сведения [об отладке Microsoft Edge из кода VS можно][VisualStudioCodeDebuggerEdgeExtension]найти здесь.</span><span class="sxs-lookup"><span data-stu-id="a4535-171">For more information, check out [how to debug Microsoft Edge from VS Code][VisualStudioCodeDebuggerEdgeExtension].</span></span>  

#### <span data-ttu-id="a4535-172">webhint</span><span class="sxs-lookup"><span data-stu-id="a4535-172">webhint</span></span>  

<span data-ttu-id="a4535-173">Расширение веб- [подсказки][VisualStudioMarketplaceWebhintExtension] и кода используются `webhint` для усовершенствования своей страницы, пока вы пишете ее!</span><span class="sxs-lookup"><span data-stu-id="a4535-173">The [webhint][VisualStudioMarketplaceWebhintExtension] VS Code extension uses `webhint` to improve your web page while you're writing it!</span></span> <span data-ttu-id="a4535-174">Это расширение запускает и сообщает диагностику файлов рабочей области на основе `webhint` анализа.</span><span class="sxs-lookup"><span data-stu-id="a4535-174">This extension runs and reports diagnostics on your workspace files based on `webhint` analysis.</span></span>  

> ##### <span data-ttu-id="a4535-175">Рисунок7</span><span class="sxs-lookup"><span data-stu-id="a4535-175">Figure 7</span></span>  
> <span data-ttu-id="a4535-176">Анализ файла и расширения кода веб-подсказки в коде VS</span><span class="sxs-lookup"><span data-stu-id="a4535-176">The webhint VS Code extension analyzing a .tsx file in VS Code</span></span>  
> ![Анализ файла и расширения кода веб-подсказки в коде VS][ImageWebhintVisualStudioCodeExtensionWorkspace]  

<span data-ttu-id="a4535-178">[Узнайте больше о расширении подсказки кода VS][WebhintVisualStudioCodeExtension].</span><span class="sxs-lookup"><span data-stu-id="a4535-178">[Learn more about the VS Code webhint extension][WebhintVisualStudioCodeExtension].</span></span>  

### <span data-ttu-id="a4535-179">Интеграция с Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a4535-179">Visual Studio integration</span></span>  

<span data-ttu-id="a4535-180">В Visual Studio 2019 версии 16,2 или более поздней Используйте отладчик Visual Studio для отладки JavaScript, который выполняется в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a4535-180">In Visual Studio 2019 version 16.2 or later, use the Visual Studio debugger to debug JavaScript running in Microsoft Edge.</span></span>  <span data-ttu-id="a4535-181">[Загрузите Visual Studio 2019][MicrosoftVisualStudioDownloads] , чтобы попробовать эту функцию!</span><span class="sxs-lookup"><span data-stu-id="a4535-181">[Download Visual Studio 2019][MicrosoftVisualStudioDownloads] to try this feature out!</span></span>  

> ##### <span data-ttu-id="a4535-182">Рисунок8</span><span class="sxs-lookup"><span data-stu-id="a4535-182">Figure 8</span></span>  
> <span data-ttu-id="a4535-183">Visual Studio с возможностью запуска веб-приложения в Microsoft Edge Канарские, dev или Beta</span><span class="sxs-lookup"><span data-stu-id="a4535-183">Visual Studio with the option to launch your web app in Microsoft Edge Canary, Dev, or Beta</span></span>  
> ![Visual Studio с возможностью запуска веб-приложения в Microsoft Edge Канарские, dev или Beta][ImageVisualStudioLaunchWebApp]  

<span data-ttu-id="a4535-185">Дополнительные [сведения об отладке Microsoft Edge из Visual Studio][MicrosoftVisualStudio].</span><span class="sxs-lookup"><span data-stu-id="a4535-185">[Learn more about debugging Microsoft Edge from Visual Studio][MicrosoftVisualStudio].</span></span>  

### <span data-ttu-id="a4535-186">Сообщения консоли предотвращения отслеживания</span><span class="sxs-lookup"><span data-stu-id="a4535-186">Tracking prevention Console messages</span></span>  

<span data-ttu-id="a4535-187">Защита от слежения — это уникальная функция в Microsoft EDGE, которая защищает вас от отслеживания веб-сайтов, которые вы еще не посещаете.</span><span class="sxs-lookup"><span data-stu-id="a4535-187">Tracking prevention is a unique feature in Microsoft Edge that protects you from being tracked by websites you haven't visited before.</span></span>  <span data-ttu-id="a4535-188">Параметр предотвращения отслеживания по умолчанию — это режим балансировки, который блокирует средства отслеживания и известных злоумышленников, чтобы обеспечить баланс конфиденциальности и веб-совместимости.</span><span class="sxs-lookup"><span data-stu-id="a4535-188">The default tracking prevention setting is Balanced mode, which blocks 3rd party trackers and known malicious trackers for an experience that balances privacy and web compatibility.</span></span>  <span data-ttu-id="a4535-189">Чтобы получить более подробную информацию о совместимости веб-страницы, если некоторые средства отслеживания заблокированы, мы также добавили предупреждающие сообщения на консоли, когда средство отслеживания заблокировано.</span><span class="sxs-lookup"><span data-stu-id="a4535-189">To give you more insight into the compatibility of your web page when certain trackers are blocked, we've also added warning messages in the Console when a tracker is blocked.</span></span>  

> ##### <span data-ttu-id="a4535-190">Рисунок9</span><span class="sxs-lookup"><span data-stu-id="a4535-190">Figure 9</span></span>  
> <span data-ttu-id="a4535-191">Сообщения на консоли, когда предотвращение отслеживания блокирует доступ к хранилищу для средства отслеживания</span><span class="sxs-lookup"><span data-stu-id="a4535-191">Messages in the Console when tracking prevention blocks access to storage for a tracker</span></span>  
> ![Сообщения на консоли, когда предотвращение отслеживания блокирует доступ к хранилищу для средства отслеживания][ImageTrackingPrevention]  

<span data-ttu-id="a4535-193">[Узнайте больше о предотвращении отслеживания и балансе между конфиденциальностью и веб-совместимостью][TrackingPrevention].</span><span class="sxs-lookup"><span data-stu-id="a4535-193">[Read more about tracking prevention and the balance between privacy and web compatibility][TrackingPrevention].</span></span>  

## <span data-ttu-id="a4535-194">Объявления из проекта Chromium</span><span class="sxs-lookup"><span data-stu-id="a4535-194">Announcements from the Chromium project</span></span>  

<span data-ttu-id="a4535-195">В следующих разделах описаны дополнительные возможности, доступные в Microsoft Edge 81, которые были задействованы в проекте Open Source Chromium.</span><span class="sxs-lookup"><span data-stu-id="a4535-195">The following sections announce additional features available in Microsoft Edge 81 that were contributed to the open source Chromium project.</span></span>  

### <span data-ttu-id="a4535-196">Поддержка Moto G4 в режиме устройства</span><span class="sxs-lookup"><span data-stu-id="a4535-196">Moto G4 support in Device Mode</span></span>  

<span data-ttu-id="a4535-197">После [включения панели инструментов устройства][DeviceToolbar]имитируйте размеры окна просмотра Moto G4 в списке **устройств** .</span><span class="sxs-lookup"><span data-stu-id="a4535-197">After [enabling the Device Toolbar][DeviceToolbar], simulate the dimensions of a Moto G4 viewport from the **Device** list.</span></span>  

> ##### <span data-ttu-id="a4535-198">Рисунок 10</span><span class="sxs-lookup"><span data-stu-id="a4535-198">Figure 10</span></span>  
> <span data-ttu-id="a4535-199">Имитация окна просмотра Moto G4</span><span class="sxs-lookup"><span data-stu-id="a4535-199">Simulating a Moto G4 viewport</span></span>  
> ![Имитация окна просмотра Moto G4][ImageMotoG4]  

<span data-ttu-id="a4535-201">Щелкните [Показать рамку устройства][DeviceFrame] , чтобы показать аппаратуру Moto G4 в окне просмотра.</span><span class="sxs-lookup"><span data-stu-id="a4535-201">Click [Show Device Frame][DeviceFrame] to show the Moto G4 hardware around the viewport.</span></span>  

> ##### <span data-ttu-id="a4535-202">Рисунок11</span><span class="sxs-lookup"><span data-stu-id="a4535-202">Figure 11</span></span>  
> <span data-ttu-id="a4535-203">Аппаратное обеспечение Moto G4</span><span class="sxs-lookup"><span data-stu-id="a4535-203">Showing the Moto G4 hardware</span></span>  
> ![Аппаратное обеспечение Moto G4][ImageMotoG4Frame]  

<span data-ttu-id="a4535-205">Дополнительные возможности:</span><span class="sxs-lookup"><span data-stu-id="a4535-205">Related features:</span></span>  

*   <span data-ttu-id="a4535-206">Откройте [меню команд][CommandMenu] и выполните команду, `Capture screenshot` чтобы сделать снимок экрана просмотра, включающий оборудование Moto G4 (после включения команды **Показать рамку устройства**).</span><span class="sxs-lookup"><span data-stu-id="a4535-206">Open the [Command Menu][CommandMenu] and run the `Capture screenshot` command to take a screenshot of the viewport that includes the Moto G4 hardware (after enabling **Show Device Frame**).</span></span>  
*   <span data-ttu-id="a4535-207">[Регулирование сети и ЦП][ThrottleNetworkAndCpu] для более точной имитации условий просмотра веб-страниц пользователя на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="a4535-207">[Throttle the network and CPU][ThrottleNetworkAndCpu] to more accurately simulate a mobile user's web browsing conditions.</span></span>  

<span data-ttu-id="a4535-208">[#924693][crbug924693] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="a4535-208">Chromium issue [#924693][crbug924693]</span></span>  

### <span data-ttu-id="a4535-209">Обновления, связанные с файлами cookie</span><span class="sxs-lookup"><span data-stu-id="a4535-209">Cookie-related updates</span></span>  

#### <span data-ttu-id="a4535-210">Заблокированные cookie-файлы в области "cookie"</span><span class="sxs-lookup"><span data-stu-id="a4535-210">Blocked cookies in the Cookies pane</span></span>  

<span data-ttu-id="a4535-211">В области "файлы cookie" на панели приложения теперь отображаются заблокированные файлы cookie с желтым фоном.</span><span class="sxs-lookup"><span data-stu-id="a4535-211">The Cookies pane in the Application panel now displays blocked cookies with a yellow background.</span></span>  

> ##### <span data-ttu-id="a4535-212">Рисунок12</span><span class="sxs-lookup"><span data-stu-id="a4535-212">Figure 12</span></span>  
> <span data-ttu-id="a4535-213">Заблокированные cookie-файлы в области "cookie" на панели приложения</span><span class="sxs-lookup"><span data-stu-id="a4535-213">Blocked cookies in the Cookies pane of the Application panel</span></span>  
> ![Заблокированные cookie-файлы в области "cookie" на панели приложения][ImageBlockedCookies]  

<span data-ttu-id="a4535-215">[#1030258][crbug|::ref1::|] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="a4535-215">Chromium issue [#1030258][crbug|::ref1::|]</span></span>  

#### <span data-ttu-id="a4535-216">Приоритет cookie-файлов в области "cookie"</span><span class="sxs-lookup"><span data-stu-id="a4535-216">Cookie priority in the Cookie pane</span></span>  

<span data-ttu-id="a4535-217">Таблицы cookie на панелях сеть и приложения теперь включают столбец **приоритета** .</span><span class="sxs-lookup"><span data-stu-id="a4535-217">The Cookies tables in the Network and Application panels now include a **Priority** column.</span></span>  

> [!CAUTION]
> <span data-ttu-id="a4535-218">Chromiumные браузеры, такие как Microsoft EDGE, — это единственные браузеры, поддерживающие приоритет cookie-файлов.</span><span class="sxs-lookup"><span data-stu-id="a4535-218">Chromium-based browsers, like Microsoft Edge, are the only browsers that support cookie priority.</span></span>  

<span data-ttu-id="a4535-219">[#1026879][crbug1026879] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="a4535-219">Chromium issue [#1026879][crbug1026879]</span></span>  

#### <span data-ttu-id="a4535-220">Изменение всех значений cookie-файлов</span><span class="sxs-lookup"><span data-stu-id="a4535-220">Edit all cookie values</span></span>  

<span data-ttu-id="a4535-221">Все ячейки в таблицах cookie теперь доступны для редактирования, кроме ячеек в столбце **Размер** , так как этот столбец представляет размер файла cookie в байтах.</span><span class="sxs-lookup"><span data-stu-id="a4535-221">All cells in the Cookie tables are editable now, except cells in the **Size** column because that column represents the network size of the cookie, in bytes.</span></span>  <span data-ttu-id="a4535-222">Просмотрите [поля][CookiesFields] , поясняющие каждый столбец.</span><span class="sxs-lookup"><span data-stu-id="a4535-222">See [Fields][CookiesFields] for an explanation of each column.</span></span>  

> ##### <span data-ttu-id="a4535-223">Рисунок13</span><span class="sxs-lookup"><span data-stu-id="a4535-223">Figure 13</span></span>  
> <span data-ttu-id="a4535-224">Изменение значения cookie-файла</span><span class="sxs-lookup"><span data-stu-id="a4535-224">Editing a cookie value</span></span>  
> ![Изменение значения cookie-файла][ImageEditCookie]  

#### <span data-ttu-id="a4535-226">Копирование как Node.js выбор для включения данных cookie</span><span class="sxs-lookup"><span data-stu-id="a4535-226">Copy as Node.js fetch to include cookie data</span></span>  

<span data-ttu-id="a4535-227">Щелкните правой кнопкой мыши по сетевому запросу и выберите команду **Копировать**  >  **копию как Node.js извлечь** , чтобы получить `fetch` выражение, включающее данные cookie.</span><span class="sxs-lookup"><span data-stu-id="a4535-227">Right-click a network request and select **Copy** > **Copy as Node.js fetch** to get a `fetch` expression that includes cookie data.</span></span>  

> ##### <span data-ttu-id="a4535-228">Рисунок14</span><span class="sxs-lookup"><span data-stu-id="a4535-228">Figure 14</span></span>  
> <span data-ttu-id="a4535-229">Копирование как Node.js выборка</span><span class="sxs-lookup"><span data-stu-id="a4535-229">Copy as Node.js fetch</span></span>  
> ![Копирование как Node.js выборка][ImageCopyFetch]  

<span data-ttu-id="a4535-231">[#1029826][crbug1029826] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="a4535-231">Chromium issue [#1029826][crbug1029826]</span></span>  

### <span data-ttu-id="a4535-232">Более точные значки манифеста веб-приложения</span><span class="sxs-lookup"><span data-stu-id="a4535-232">More accurate web app manifest icons</span></span>  

<span data-ttu-id="a4535-233">Ранее область манифеста на панели приложения отправляет свои собственные запросы для отображения значков манифеста веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="a4535-233">Previously, the Manifest pane in the Application panel sent its own requests in order to display web app manifest icons.</span></span>  <span data-ttu-id="a4535-234">DevTools теперь показывает тот же значок манифеста, который использует Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="a4535-234">DevTools now shows the exact same manifest icon that Microsoft Edge uses.</span></span>  

> ##### <span data-ttu-id="a4535-235">Рисунок15</span><span class="sxs-lookup"><span data-stu-id="a4535-235">Figure 15</span></span>  
> <span data-ttu-id="a4535-236">Значки в области «манифест»</span><span class="sxs-lookup"><span data-stu-id="a4535-236">Icons in the Manifest pane</span></span>  
> ![Значки в области «манифест»][ImageManifestIcon]  

<span data-ttu-id="a4535-238">[#985402][crbug985402] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="a4535-238">Chromium issue [#985402][crbug985402]</span></span>  

### <span data-ttu-id="a4535-239">Наведите указатель мыши на свойства содержимого CSS, чтобы увидеть неэкранированные значения</span><span class="sxs-lookup"><span data-stu-id="a4535-239">Hover over CSS content properties to see unescaped values</span></span>  

<span data-ttu-id="a4535-240">Наведите указатель мыши на значение `content` свойства, чтобы увидеть неэкранированную версию значения.</span><span class="sxs-lookup"><span data-stu-id="a4535-240">Hover over the value of a `content` property to see the unescaped version of the value.</span></span>  

<span data-ttu-id="a4535-241">Например, в этой статье вы узнаете [о том,][CSSContentDemo] что на `p::after` панели Стили отображается строка с escape-символами.</span><span class="sxs-lookup"><span data-stu-id="a4535-241">For example, in this [demo][CSSContentDemo] when you inspect the `p::after` pseudo-element you see an escaped string in the Styles pane:</span></span>  

> ##### <span data-ttu-id="a4535-242">Рисунок16</span><span class="sxs-lookup"><span data-stu-id="a4535-242">Figure 16</span></span>  
> <span data-ttu-id="a4535-243">Строка с escape-символом</span><span class="sxs-lookup"><span data-stu-id="a4535-243">The escaped string</span></span>  
> ![Строка с escape-символом][ImageEscapedString]  

<span data-ttu-id="a4535-245">При наведении указателя мыши на значение, которое `content` отображается в неэкранированном значении:</span><span class="sxs-lookup"><span data-stu-id="a4535-245">When you hover over the `content` value you see the unescaped value:</span></span>  

> ##### <span data-ttu-id="a4535-246">Рисунок17</span><span class="sxs-lookup"><span data-stu-id="a4535-246">Figure 17</span></span>  
> <span data-ttu-id="a4535-247">Неэкранированное значение</span><span class="sxs-lookup"><span data-stu-id="a4535-247">The unescaped value</span></span>  
> ![Неэкранированное значение][ImageUnescapedString]  

### <span data-ttu-id="a4535-249">Дополнительные сведения об ошибках на карте исходного кода на консоли</span><span class="sxs-lookup"><span data-stu-id="a4535-249">More detailed source map errors in the Console</span></span>  

<span data-ttu-id="a4535-250">Теперь консоль содержит более подробные сведения о том, почему не удалось загрузить или проанализировать исходную карту.</span><span class="sxs-lookup"><span data-stu-id="a4535-250">The Console now provides more detail on why a source map failed to load or parse.</span></span>  <span data-ttu-id="a4535-251">Ранее она только что предоставила ошибку, не объясняющую, что пошло не так.</span><span class="sxs-lookup"><span data-stu-id="a4535-251">Previously it just provided an error without explaining what went wrong.</span></span>  

> ##### <span data-ttu-id="a4535-252">Рис. 18</span><span class="sxs-lookup"><span data-stu-id="a4535-252">Figure 18</span></span>  
> <span data-ttu-id="a4535-253">Ошибка при загрузке карты исходного кода на консоли</span><span class="sxs-lookup"><span data-stu-id="a4535-253">A source map loading error in the Console</span></span>  
> ![Ошибка при загрузке карты исходного кода на консоли][ImageSourcemapError]  

### <span data-ttu-id="a4535-255">Настройка отключения прокрутки за пределами файла</span><span class="sxs-lookup"><span data-stu-id="a4535-255">Setting for disabling scrolling past the end of a file</span></span>  

<span data-ttu-id="a4535-256">Откройте [Параметры][Settings] и выберите Отключить **Preferences**  >  **исходные**настройки.  >  **разрешите прокрутку за** пределами файла, чтобы отключить поведение пользовательского интерфейса по умолчанию, позволяющее прокручивать прокрутку за пределами файла на панели « **источники** ».</span><span class="sxs-lookup"><span data-stu-id="a4535-256">Open [Settings][Settings] and then disable **Preferences** > **Sources** > **Allow scrolling past end of file** to disable the default UI behavior that allows you to scroll well past the end of a file in the **Sources** panel.</span></span>  

> ##### <span data-ttu-id="a4535-257">На рисунке 19</span><span class="sxs-lookup"><span data-stu-id="a4535-257">Figure 19</span></span>  
> <span data-ttu-id="a4535-258">Отключение **разрешения на прокрутку за** пределами файла в параметрах</span><span class="sxs-lookup"><span data-stu-id="a4535-258">Disabling **Allow scrolling past end of file** in Settings</span></span>  
> ![Отключение разрешения на прокрутку за пределами файла][ImageSettings]  

> ##### <span data-ttu-id="a4535-260">Рис. 20</span><span class="sxs-lookup"><span data-stu-id="a4535-260">Figure 20</span></span>  
> <span data-ttu-id="a4535-261">Прокрутка за пределами файла теперь отключена на панели «источники»</span><span class="sxs-lookup"><span data-stu-id="a4535-261">Scrolling past the end of a file is now disabled in the Sources panel</span></span>  
> ![Прокрутка за пределами файла теперь отключена на панели «источники»][ImageScroll]  

## <span data-ttu-id="a4535-263">Загрузка каналов предварительной версии Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a4535-263">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="a4535-264">Если вы используете Windows или macOS, рассматривайте в качестве браузера по умолчанию использование [каналов предварительного просмотра Microsoft Edge][MicrosoftEdgePreviewChannels] .</span><span class="sxs-lookup"><span data-stu-id="a4535-264">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="a4535-265">Каналы предварительного просмотра предоставляют доступ к последним функциям DevTools.</span><span class="sxs-lookup"><span data-stu-id="a4535-265">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="a4535-266">Знакомство с Microsoft Edge DevTools Team</span><span class="sxs-lookup"><span data-stu-id="a4535-266">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- <<../../_shared/devtools-feedback.md>>  

<<../../_shared/canary.md>>  

<<../../_shared/discover.md>> -->  

<!-- image links -->  

[ImagePerformanceToolKeyboardReaderImprovements]: ../../images/2020/01/a11y-performance-tool.msft.gif "Рисунок 1: средство "производительность" в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана"  
[ImageLocalizedGerman]: ../../images/2020/01/localized-devtools.msft.png "Рисунок 2: DevTools на немецком языке"  
[ImageHintsTabWebhintExtension]: ../../images/2020/01/webhint-browser-extension.msft.png "Рисунок 3: вкладка "Подсказка" в Microsoft Edge DevTools, когда установлено расширение браузера веб."  
[Image3DView]: ../../images/2020/01/3dview.msft.png "Рисунок 4:3D-представление в Microsoft Edge DevTools"  
[ImageElementsVisualStudioCode]: ../../images/2020/01/elements-for-edge.msft.png "Рисунок 5. инструмент "элементы" в коде VS с использованием элементов для расширения Microsoft Edge"  
[ImageDebuggerExtensionVisualStudioCode]: ../../images/2020/01/vscode-debugger.msft.png "Рисунок 6: отладчик для расширения Microsoft EDGE в коде VS"  
[ImageWebhintVisualStudioCodeExtensionWorkspace]: ../../images/2020/01/webhint-vscode-extension.msft.png "Рис. 7: расширение веб-подсказки и кода анализ целевого файла в коде VS"  
[ImageVisualStudioLaunchWebApp]: ../../images/2020/01/vs.msft.png "Рисунок 8: Visual Studio с возможностью запуска вашего веб-приложения в Microsoft Edge Канарские, dev или Beta"  
[ImageTrackingPrevention]: ../../images/2020/01/tracking-prevention.msft.png "Рис. 9: сообщения на консоли, когда предотвращение отслеживания блокирует доступ к хранилищу для средства отслеживания." 
[ImageMotoG4]: ../../images/2020/01/motog4.msft.png "Рисунок 10: Имитация окна просмотра Moto G4" 
[ImageMotoG4Frame]: ../../images/2020/01/motog4frame.msft.png "Рисунок 11: демонстрация оборудования Moto G4" 
[ImageBlockedCookies]: ../../images/2020/01/blockedcookies.msft.png "Рисунок 12: заблокированные cookie-файлы в области "cookie" на панели приложения"
[ImageEditCookie]: ../../images/2020/01/editcookie.msft.png "Рисунок 13: Редактирование значения cookie-файла"
[ImageCopyFetch]: ../../images/2020/01/fetchcookies.msft.png "Рисунок 14: копирование как Node.js выборка"
[ImageManifestIcon]: ../../images/2020/01/manifesticons.msft.png "Рисунок 15: значки в области манифеста"
[ImageEscapedString]: ../../images/2020/01/escapedstring.msft.png "Рисунок 16: строка с escape-символом"
[ImageUnescapedString]: ../../images/2020/01/unescapedstring.msft.png "Рисунок 17: Неэкранированное значение"
[ImageSourcemapError]: ../../images/2020/01/sourcemap.msft.png "Рисунок 18: ошибка при загрузке карты исходного кода на консоли"
[ImageSettings]: ../../images/2020/01/settings.msft.png "Рисунок 19: отключение режима "Разрешить прокрутку за конец файла" в параметрах"
[ImageScroll]: ../../images/2020/01/scrollingsources.msft.png "Рисунок 20: прокрутка за пределами файла теперь отключена на панели «источники»"

<!-- links -->  

[DeviceToolbar]: ../../../device-mode/index.md#simulate-a-mobile-viewport "Имитация мобильного окна просмотра с помощью режима устройства в Microsoft Edge DevTools"
[DeviceFrame]: ../../../device-mode/index.md#show-device-frame "Нажмите кнопку Показать рамку устройства, чтобы отобразить рамку физического устройства вокруг окна просмотра."
[CommandMenu]: ../../../command-menu/index.md "Выполнение команд с помощью командного меню Microsoft Edge DevTools"  
[ThrottleNetworkAndCpu]: ../../../device-mode/index.md#throttle-the-network-and-cpu "Регулирование сети и ЦП для более точной имитации условий просмотра веб-страниц пользователя на мобильном устройстве."
[crbug924693]: https://crbug.com/924693 "924693: запрос компонента: Добавление Moto G4 в список режимов устройства"
[crbug1030258]: https://crbug.com/1030258 "1030258"
[crbug1026879]: https://crbug.com/1026879 "1026879: вкладка cookie в консоли разработки больше не показывает приоритет"
[CookiesFields]: ../../../storage/cookies.md#fields "Поля в таблице cookie-файлов"
[crbug1029826]: https://crbug.com/1029826 "1029826: вкладка "сеть" — > щелчок правой кнопкой мыши для запроса на > копирование > копирование в качестве выборке не копирует файлы cookie"
[crbug985402]: https://crbug.com/985402 "985402: ошибки значков в манифесте веб-приложения — это запутанная строка"
[CSSContentDemo]: https://mathiasbynens.github.io/css-dbg-stories/css-escapes.html "Демонстрация для без последовательного содержимого CSS"
[Settings]: ../../../customize/index.md#settings "Настройка Microsoft Edge DevTools с помощью параметров"
[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Публикация твита"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Новая ошибка — MicrosoftDocs/Edge-разработчик"  
[TheWebWeWant]: https://aka.ms/webwewant "Требуемый веб-сайт"
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Каналы предварительной версии Microsoft Edge"  
[VisualStudioCodeDebuggerEdgeExtension]: ../../../../visual-studio-code/debugger-for-edge.md "Отладчик для расширения кода Microsoft Edge VS"  
[VisualStudioCodeElementEdgeExtension]: ../../../../visual-studio-code/elements-for-edge.md "Элементы расширений Microsoft EDGE и кода"  
[crbug963183]: https://crbug.com/963183 "963183-DevTools не соответствуют требованиям WCAG"
[crbug941561]: https://crbug.com/941561 "941561 – локализуемость DevTools"
[crbug987787]: https://crbug.com/987787 "987787 – трехмерный вид DOM"
[AccessibilityInsights]: https://aka.ms/a11yinsights "Аналитические сведения о специальных возможностях"  
[MicrosoftEdgeInsiderAddons]: https://aka.ms/webhint/edge-extension "Надстройки Microsoft Edge для участников программы предварительной оценки"  
[MicrosoftVisualStudio]: ../../../../visual-studio/index.md "Visual Studio"  
[MicrosoftVisualStudioDownloads]: https://aka.ms/vs/download "Скачайте Visual Studio 2019 для Windows \ & Mac"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Объектная модель документов (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "z-индекс | MDN"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools учетной записи Twitter"
[VisualStudioCode]: https://aka.ms/vscode "Код Visual Studio"  
[VisualStudioMarketplaceDebuggerEdge]: https://aka.ms/debugger4code "Отладчик для Microsoft Edge-Visual Studio Marketplace"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://aka.ms/elements4code "Элементы для Microsoft Edge \ (Chromium \) — Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://aka.ms/webhint4code ""Подсказка" — Visual Studio Marketplace"
[Webhint]: https://aka.ms/webhint "Подсказка"  
[WebhintBrowserExtension]: https://aka.ms/webhint/browser-extension "Расширение браузеров веб – подсказок | Документация по подсказкам"  
[WebhintVisualStudioCodeExtension]: https://aka.ms/webhint/code-extension "Расширение ссылки и кода Документация по подсказкам"  
[TrackingPrevention]: https://aka.ms/microsoftedge/tracking-prevention-blog "Улучшение защиты от слежения в блоге Microsoft Edge"

> [!NOTE]
> <span data-ttu-id="a4535-323">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a4535-323">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="a4535-324">Исходная страница будет найдена [здесь](https://developers.google.com/web/updates/2020/01/devtools/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="a4535-324">The original page is found [here](https://developers.google.com/web/updates/2020/01/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="a4535-326">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="a4535-326">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  