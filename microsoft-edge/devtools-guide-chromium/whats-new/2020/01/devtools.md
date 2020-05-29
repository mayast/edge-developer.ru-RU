---
title: Новые возможности DevTools (Microsoft Edge 81)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/20/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 6de8f7b11edb476f2656dd6f16e02413b1873ed8
ms.sourcegitcommit: a5392ab44133d742c0e1fa500ad9a872989b7c3f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/28/2020
ms.locfileid: "10684715"
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







# <span data-ttu-id="618d4-103">Новые возможности DevTools (Microsoft Edge 81)</span><span class="sxs-lookup"><span data-stu-id="618d4-103">What's New In DevTools (Microsoft Edge 81)</span></span>   



## <span data-ttu-id="618d4-104">Объявления из группы Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="618d4-104">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="618d4-105">В следующих разделах представлен список извещений, которые вы могли не получить в Microsoft Edge DevTools Teams!</span><span class="sxs-lookup"><span data-stu-id="618d4-105">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team!</span></span> <span data-ttu-id="618d4-106">Узнайте, как использовать новые функции в DevTools, расширения кода VS и многое другое.</span><span class="sxs-lookup"><span data-stu-id="618d4-106">Check them out to try new features in the DevTools, VS Code extensions, and more.</span></span>  <span data-ttu-id="618d4-107">Чтобы оставаться на связи с самыми последними и более свежими возможностями, скачайте на веб – [каналы предварительной версии Microsoft Edge][MicrosoftEdgePreviewChannels] и [следуйте указаниям Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="618d4-107">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <span data-ttu-id="618d4-108">Улучшение специальных возможностей в DevTools</span><span class="sxs-lookup"><span data-stu-id="618d4-108">Accessibility improvements to the DevTools</span></span>  

<span data-ttu-id="618d4-109">Группа DevTools изменила 170 в Chromium для устранения проблем с высокой контрастностью цвета, клавиатуры и средства чтения с экрана в DevTools.</span><span class="sxs-lookup"><span data-stu-id="618d4-109">The DevTools team has contributed 170 changes to Chromium to address high-impact color contrast, keyboard, and screen reader issues in the DevTools.</span></span>  <span data-ttu-id="618d4-110">Каждый разработчик, создающий веб-сайт, должен иметь возможность использовать DevTools.</span><span class="sxs-lookup"><span data-stu-id="618d4-110">Every developer building the web should be able to use the DevTools.</span></span>  

> ##### <span data-ttu-id="618d4-111">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="618d4-111">Figure 1</span></span>  
> <span data-ttu-id="618d4-112">Средство "производительность" в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана</span><span class="sxs-lookup"><span data-stu-id="618d4-112">The Performance tool in the DevTools with the keyboard navigation and screen reader improvements</span></span>  
> ![Средство "производительность" в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана][ImagePerformanceToolKeyboardReaderImprovements]  

<span data-ttu-id="618d4-114">Сведения о том, как сделать веб-страницу доступной для всех пользователей?</span><span class="sxs-lookup"><span data-stu-id="618d4-114">Want to learn how to make your web page accessible to all of your users?</span></span>  <span data-ttu-id="618d4-115">Скачайте [расширения для][WebhintBrowserExtension] Microsoft Edge " [Специальные возможности][AccessibilityInsights] ", чтобы приступить к работе.</span><span class="sxs-lookup"><span data-stu-id="618d4-115">Download the [Accessibility Insights][AccessibilityInsights] and [webhint][WebhintBrowserExtension] extensions for Microsoft Edge to get started.</span></span>  

<span data-ttu-id="618d4-116">Если вы используете средства чтения с экрана или клавиатуру для навигации по DevTools, отправьте нам свой отзыв, выполнив [твит][PostTweetEdgeDevTools] в США или щелкнув значок [отзыва](#feedback) .</span><span class="sxs-lookup"><span data-stu-id="618d4-116">If you use screen readers or the keyboard to navigate around the DevTools, send us your feedback by [tweeting][PostTweetEdgeDevTools] at us or clicking the [Feedback](#feedback) icon!</span></span>  

<span data-ttu-id="618d4-117">[#963183][crbug963183] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="618d4-117">Chromium issue [#963183][crbug963183]</span></span>  

### <span data-ttu-id="618d4-118">Использование DevTools на других языках</span><span class="sxs-lookup"><span data-stu-id="618d4-118">Using the DevTools in other languages</span></span>  

<span data-ttu-id="618d4-119">Многие разработчики используют другие инструменты разработчика, такие как StackOverflow и код VS, на родном языке, а не только на английском языке.</span><span class="sxs-lookup"><span data-stu-id="618d4-119">Many developers use other developer tools, like StackOverflow and VS Code, in their native language, not just in English.</span></span>  <span data-ttu-id="618d4-120">Мы рады объявить локализацию для DevTools, который теперь вы можете использовать на одном из 10 языков, кроме английского.</span><span class="sxs-lookup"><span data-stu-id="618d4-120">We’re excited to announce localization for the DevTools, which you are now able to use in one of 10 languages besides English:</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="618d4-121">Китайский (упрощенное письмо) —  &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span><span class="sxs-lookup"><span data-stu-id="618d4-121">Chinese \(Simplified\) - &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="618d4-122">Китайский (традиционное письмо) —  &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span><span class="sxs-lookup"><span data-stu-id="618d4-122">Chinese \(Traditional\) - &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="618d4-123">Французский — Fran&#231;AIS</span><span class="sxs-lookup"><span data-stu-id="618d4-123">French – fran&#231;ais</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="618d4-124">Немецкий — Deutsch</span><span class="sxs-lookup"><span data-stu-id="618d4-124">German - deutsch</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="618d4-125">Итальянский — Italiano</span><span class="sxs-lookup"><span data-stu-id="618d4-125">Italian - italiano</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="618d4-126">Японская  &#26085;&#26412;&#35486;</span><span class="sxs-lookup"><span data-stu-id="618d4-126">Japanese - &#26085;&#26412;&#35486;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="618d4-127">Корейский —  &#54620;&#44397;&#50612;</span><span class="sxs-lookup"><span data-stu-id="618d4-127">Korean - &#54620;&#44397;&#50612;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="618d4-128">Португальский (portugu&#234;s)</span><span class="sxs-lookup"><span data-stu-id="618d4-128">Portuguese - portugu&#234;s</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="618d4-129">Русский —  &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span><span class="sxs-lookup"><span data-stu-id="618d4-129">Russian – &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="618d4-130">Испанская — ESPA&#241;OL</span><span class="sxs-lookup"><span data-stu-id="618d4-130">Spanish - espa&#241;ol</span></span>
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

<span data-ttu-id="618d4-131">DevTools автоматически соответствует языку, который вы используете для Microsoft Edge in `edge://settings/languages` .</span><span class="sxs-lookup"><span data-stu-id="618d4-131">The DevTools automatically match the language you use for Microsoft Edge in `edge://settings/languages`.</span></span>  

<span data-ttu-id="618d4-132">Если вы хотите, чтобы Microsoft Edge выоставался на одном языке, а DevTools на русском языке, нажмите кнопку `F1` DevTools, чтобы открыть вкладку [Параметры][Settings] и отключить **язык браузера**.</span><span class="sxs-lookup"><span data-stu-id="618d4-132">If you want Microsoft Edge to be in one language and your DevTools to remain in English, press `F1` in the DevTools to open [Settings][Settings] and disable **Match browser language**.</span></span>  

> ##### <span data-ttu-id="618d4-133">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="618d4-133">Figure 2</span></span>  
> <span data-ttu-id="618d4-134">DevTools на немецком языке</span><span class="sxs-lookup"><span data-stu-id="618d4-134">The DevTools in German</span></span>  
> ![DevTools на немецком языке][ImageLocalizedGerman]  

<span data-ttu-id="618d4-136">Сообщения **консоли** не локализуются.</span><span class="sxs-lookup"><span data-stu-id="618d4-136">**Console** messages are not localized.</span></span>  <span data-ttu-id="618d4-137">На языке, используемом для Microsoft EDGE, отображаются только строки, используемые в пользовательском интерфейсе DevTools.</span><span class="sxs-lookup"><span data-stu-id="618d4-137">Only the strings used in the DevTools UI are displayed in the language you use for Microsoft Edge.</span></span>  

<span data-ttu-id="618d4-138">Если вы хотите использовать DevTools на языке, отличном от того, на котором они доступны, [твит][PostTweetEdgeDevTools] в США или щелкните значок [отзыва](#feedback) .</span><span class="sxs-lookup"><span data-stu-id="618d4-138">If you want to use the DevTools in a different language than the ones that are available, [tweet][PostTweetEdgeDevTools] at us or click the [Feedback](#feedback) icon.</span></span>  

<span data-ttu-id="618d4-139">[#941561][crbug941561] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="618d4-139">Chromium issue [#941561][crbug941561]</span></span>  

### <span data-ttu-id="618d4-140">Веб – подсказка с расширением Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="618d4-140">webhint Microsoft Edge extension</span></span>  

<span data-ttu-id="618d4-141">Расширение веб-подсказки Microsoft EDGE позволяет легко находить и получать отзывы о специальных возможностях, совместимости с браузерами, безопасности, производительности и других средствах в DevTools.</span><span class="sxs-lookup"><span data-stu-id="618d4-141">The webhint Microsoft Edge extension allows you to easily scan your web page and get feedback on accessibility, browser compatibility, security, performance, and more within the DevTools.</span></span>  <span data-ttu-id="618d4-142">Узнайте больше о [https://webhint.io][Webhint] .</span><span class="sxs-lookup"><span data-stu-id="618d4-142">Read more at [https://webhint.io][Webhint].</span></span>  

> ##### <span data-ttu-id="618d4-143">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="618d4-143">Figure 3</span></span>  
> <span data-ttu-id="618d4-144">Вкладка "Подсказка" в DevTools, если установлено расширение браузера веб.</span><span class="sxs-lookup"><span data-stu-id="618d4-144">The Hints tab in the DevTools when the webhint browser extension is installed</span></span>  
> ![Вкладка "Подсказка" в DevTools, если установлено расширение браузера веб.][ImageHintsTabWebhintExtension]  

<span data-ttu-id="618d4-146">[Попробуйте расширение браузера веб для подсказки в Microsoft Edge][MicrosoftEdgeInsiderAddons].</span><span class="sxs-lookup"><span data-stu-id="618d4-146">[Try the webhint browser extension in Microsoft Edge][MicrosoftEdgeInsiderAddons].</span></span>  <span data-ttu-id="618d4-147">После установки расширения откройте DevTools и перейдите на вкладку подсказки.  В этой статье запустите настраиваемое сканирование сайта.</span><span class="sxs-lookup"><span data-stu-id="618d4-147">Once you install the extension, open the DevTools and select the Hints tab.  From here, run a customizable site scan.</span></span>  <span data-ttu-id="618d4-148">Чтобы получить дополнительные сведения, [заwebhint.IO][WebhintBrowserExtension] в голову.</span><span class="sxs-lookup"><span data-stu-id="618d4-148">Head over to [webhint.io][WebhintBrowserExtension] to learn more.</span></span>  

### <span data-ttu-id="618d4-149">Трехмерное представление</span><span class="sxs-lookup"><span data-stu-id="618d4-149">3D View</span></span>  

<span data-ttu-id="618d4-150">С помощью **трехмерного представления** вы можете выполнять отладку своего веб-приложения, перемещаясь по [объектной модели документов \ (DOM)][MDNDocumentObjectModel] или контексту стека [z-индексов][MDNZIndex] .</span><span class="sxs-lookup"><span data-stu-id="618d4-150">Use the **3D View** to debug your web application by navigating through the [Document Object Model \(DOM\)][MDNDocumentObjectModel] or the [z-index][MDNZIndex] stacking context.</span></span>  

> ##### <span data-ttu-id="618d4-151">Рисунок4</span><span class="sxs-lookup"><span data-stu-id="618d4-151">Figure 4</span></span>  
> <span data-ttu-id="618d4-152">Трехмерное представление в DevTools</span><span class="sxs-lookup"><span data-stu-id="618d4-152">The 3D View in the DevTools</span></span>  
> ![Трехмерное представление в DevTools][Image3DView]  

<span data-ttu-id="618d4-154">Для доступа к трехмерному представлению нажмите клавишу `Ctrl`  +  `Shift`  +  `P` Ввод в **режиме 3D-представления** и выберите **Показать 3D-представление**.</span><span class="sxs-lookup"><span data-stu-id="618d4-154">To access the 3D View, press `Ctrl` + `Shift` + `P`, type in **3D View** and select **Show 3D View**.</span></span>  

<span data-ttu-id="618d4-155">Мы работаем над ИНТЕРФЕЙСом и добавляем дополнительные функции в 3D-представление, поэтому отправьте нам свой [отзыв](#feedback).</span><span class="sxs-lookup"><span data-stu-id="618d4-155">We're working on the UI and adding more functionality to the 3D View, so please send us your [feedback](#feedback).</span></span>  

<span data-ttu-id="618d4-156">[#987787][crbug987787] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="618d4-156">Chromium issue [#987787][crbug987787]</span></span>  

### <span data-ttu-id="618d4-157">Расширения кода Visual Studio</span><span class="sxs-lookup"><span data-stu-id="618d4-157">Visual Studio Code extensions</span></span>  

<span data-ttu-id="618d4-158">Кроме того, Группа DevTools также выпустила некоторые расширения для [кода Visual Studio \ (код VS)][VisualStudioCode] , которые позволяют использовать возможности DevTools прямо из текстового редактора.</span><span class="sxs-lookup"><span data-stu-id="618d4-158">The DevTools team has also released some extensions for [Visual Studio Code \(VS Code\)][VisualStudioCode] that let you use the power of the DevTools directly from your text editor!</span></span> <span data-ttu-id="618d4-159">Ознакомьтесь с приведенными ниже расширениями.</span><span class="sxs-lookup"><span data-stu-id="618d4-159">Check out the extensions below:</span></span>  

#### <span data-ttu-id="618d4-160">Элементы Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="618d4-160">Elements for Microsoft Edge</span></span>  

<span data-ttu-id="618d4-161">С помощью инструмента "элементы" в коде VS добавьте [элементы для расширения кода Microsoft Edge \ (Chromium \)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] vs.</span><span class="sxs-lookup"><span data-stu-id="618d4-161">Use the Elements tool from within VS Code by adding the [Elements for Microsoft Edge \(Chromium\)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] VS Code extension.</span></span>  

> ##### <span data-ttu-id="618d4-162">Рисунок 5</span><span class="sxs-lookup"><span data-stu-id="618d4-162">Figure 5</span></span>  
> <span data-ttu-id="618d4-163">Инструмент "элементы" в коде VS с использованием элементов для расширения Microsoft Edge — ![ инструмент "элементы" в коде VS с использованием элементов для расширения Microsoft Edge][ImageElementsVisualStudioCode]</span><span class="sxs-lookup"><span data-stu-id="618d4-163">The Elements tool in VS Code using the Elements for Microsoft Edge extension ![The Elements tool in VS Code using the Elements for Microsoft Edge extension][ImageElementsVisualStudioCode]</span></span>  

<span data-ttu-id="618d4-164">Для получения дополнительных сведений изучите [элементы для расширения кода Microsoft Edge VS][VisualStudioCodeElementEdgeExtension].</span><span class="sxs-lookup"><span data-stu-id="618d4-164">For more information, check out [Elements for Microsoft Edge VS Code extension][VisualStudioCodeElementEdgeExtension].</span></span>  

#### <span data-ttu-id="618d4-165">Отладчик для Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="618d4-165">Debugger for Microsoft Edge</span></span>  

<span data-ttu-id="618d4-166">С помощью [отладчика для расширения кода Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] , Отладка JavaScript выполняется в Microsoft Edge прямо из кода vs.</span><span class="sxs-lookup"><span data-stu-id="618d4-166">With the [Debugger for Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] VS Code extension, debug JavaScript running in Microsoft Edge directly from VS Code!</span></span>  

> ##### <span data-ttu-id="618d4-167">Рисунок6</span><span class="sxs-lookup"><span data-stu-id="618d4-167">Figure 6</span></span>  
> <span data-ttu-id="618d4-168">Отладчик для расширения Microsoft EDGE в коде VS</span><span class="sxs-lookup"><span data-stu-id="618d4-168">The Debugger for Microsoft Edge Extension in VS Code</span></span>  
> ![Отладчик для расширения Microsoft EDGE в коде VS][ImageDebuggerExtensionVisualStudioCode]  

<span data-ttu-id="618d4-170">Дополнительные сведения [об отладке Microsoft Edge из кода VS можно][VisualStudioCodeDebuggerEdgeExtension]найти здесь.</span><span class="sxs-lookup"><span data-stu-id="618d4-170">For more information, check out [how to debug Microsoft Edge from VS Code][VisualStudioCodeDebuggerEdgeExtension].</span></span>  

#### <span data-ttu-id="618d4-171">Подсказка</span><span class="sxs-lookup"><span data-stu-id="618d4-171">webhint</span></span>  

<span data-ttu-id="618d4-172">Расширение веб- [подсказки][VisualStudioMarketplaceWebhintExtension] и кода используются `webhint` для усовершенствования своей страницы, пока вы пишете ее!</span><span class="sxs-lookup"><span data-stu-id="618d4-172">The [webhint][VisualStudioMarketplaceWebhintExtension] VS Code extension uses `webhint` to improve your web page while you're writing it!</span></span> <span data-ttu-id="618d4-173">Это расширение запускает и сообщает диагностику файлов рабочей области на основе `webhint` анализа.</span><span class="sxs-lookup"><span data-stu-id="618d4-173">This extension runs and reports diagnostics on your workspace files based on `webhint` analysis.</span></span>  

> ##### <span data-ttu-id="618d4-174">Рисунок7</span><span class="sxs-lookup"><span data-stu-id="618d4-174">Figure 7</span></span>  
> <span data-ttu-id="618d4-175">Анализ файла и расширения кода веб-подсказки в коде VS</span><span class="sxs-lookup"><span data-stu-id="618d4-175">The webhint VS Code extension analyzing a .tsx file in VS Code</span></span>  
> ![Анализ файла и расширения кода веб-подсказки в коде VS][ImageWebhintVisualStudioCodeExtensionWorkspace]  

<span data-ttu-id="618d4-177">[Узнайте больше о расширении подсказки кода VS][WebhintVisualStudioCodeExtension].</span><span class="sxs-lookup"><span data-stu-id="618d4-177">[Learn more about the VS Code webhint extension][WebhintVisualStudioCodeExtension].</span></span>  

### <span data-ttu-id="618d4-178">Интеграция с Visual Studio</span><span class="sxs-lookup"><span data-stu-id="618d4-178">Visual Studio integration</span></span>  

<span data-ttu-id="618d4-179">В Visual Studio 2019 версии 16,2 или более поздней Используйте отладчик Visual Studio для отладки JavaScript, который выполняется в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="618d4-179">In Visual Studio 2019 version 16.2 or later, use the Visual Studio debugger to debug JavaScript running in Microsoft Edge.</span></span>  <span data-ttu-id="618d4-180">[Загрузите Visual Studio 2019][MicrosoftVisualStudioDownloads] , чтобы попробовать эту функцию!</span><span class="sxs-lookup"><span data-stu-id="618d4-180">[Download Visual Studio 2019][MicrosoftVisualStudioDownloads] to try this feature out!</span></span>  

> ##### <span data-ttu-id="618d4-181">Рисунок8</span><span class="sxs-lookup"><span data-stu-id="618d4-181">Figure 8</span></span>  
> <span data-ttu-id="618d4-182">Visual Studio с возможностью запуска веб-приложения в Microsoft Edge Канарские, dev или Beta</span><span class="sxs-lookup"><span data-stu-id="618d4-182">Visual Studio with the option to launch your web app in Microsoft Edge Canary, Dev, or Beta</span></span>  
> ![Visual Studio с возможностью запуска веб-приложения в Microsoft Edge Канарские, dev или Beta][ImageVisualStudioLaunchWebApp]  

<span data-ttu-id="618d4-184">Дополнительные [сведения об отладке Microsoft Edge из Visual Studio][MicrosoftVisualStudio].</span><span class="sxs-lookup"><span data-stu-id="618d4-184">[Learn more about debugging Microsoft Edge from Visual Studio][MicrosoftVisualStudio].</span></span>  

### <span data-ttu-id="618d4-185">Сообщения консоли предотвращения отслеживания</span><span class="sxs-lookup"><span data-stu-id="618d4-185">Tracking prevention Console messages</span></span>  

<span data-ttu-id="618d4-186">Защита от слежения — это уникальная функция в Microsoft EDGE, которая защищает вас от отслеживания веб-сайтов, которые вы еще не посещаете.</span><span class="sxs-lookup"><span data-stu-id="618d4-186">Tracking prevention is a unique feature in Microsoft Edge that protects you from being tracked by websites you haven't visited before.</span></span>  <span data-ttu-id="618d4-187">Параметр предотвращения отслеживания по умолчанию — это режим балансировки, который блокирует средства отслеживания и известных злоумышленников, чтобы обеспечить баланс конфиденциальности и веб-совместимости.</span><span class="sxs-lookup"><span data-stu-id="618d4-187">The default tracking prevention setting is Balanced mode, which blocks 3rd party trackers and known malicious trackers for an experience that balances privacy and web compatibility.</span></span>  <span data-ttu-id="618d4-188">Чтобы получить более подробную информацию о совместимости веб-страницы, если некоторые средства отслеживания заблокированы, мы также добавили предупреждающие сообщения на консоли, когда средство отслеживания заблокировано.</span><span class="sxs-lookup"><span data-stu-id="618d4-188">To give you more insight into the compatibility of your web page when certain trackers are blocked, we've also added warning messages in the Console when a tracker is blocked.</span></span>  

> ##### <span data-ttu-id="618d4-189">Рисунок9</span><span class="sxs-lookup"><span data-stu-id="618d4-189">Figure 9</span></span>  
> <span data-ttu-id="618d4-190">Сообщения на консоли, когда предотвращение отслеживания блокирует доступ к хранилищу для средства отслеживания</span><span class="sxs-lookup"><span data-stu-id="618d4-190">Messages in the Console when tracking prevention blocks access to storage for a tracker</span></span>  
> ![Сообщения на консоли, когда предотвращение отслеживания блокирует доступ к хранилищу для средства отслеживания][ImageTrackingPrevention]  

<span data-ttu-id="618d4-192">[Узнайте больше о предотвращении отслеживания и балансе между конфиденциальностью и веб-совместимостью][TrackingPrevention].</span><span class="sxs-lookup"><span data-stu-id="618d4-192">[Read more about tracking prevention and the balance between privacy and web compatibility][TrackingPrevention].</span></span>



## <span data-ttu-id="618d4-193">Объявления из проекта Chromium</span><span class="sxs-lookup"><span data-stu-id="618d4-193">Announcements from the Chromium project</span></span>  

<span data-ttu-id="618d4-194">В следующих разделах описаны дополнительные возможности, доступные в Microsoft Edge 81, которые были задействованы в проекте Open Source Chromium.</span><span class="sxs-lookup"><span data-stu-id="618d4-194">The following sections announce additional features available in Microsoft Edge 81 that were contributed to the open source Chromium project.</span></span>  

### <span data-ttu-id="618d4-195">Поддержка Moto G4 в режиме устройства</span><span class="sxs-lookup"><span data-stu-id="618d4-195">Moto G4 support in Device Mode</span></span> 

<span data-ttu-id="618d4-196">После [включения панели инструментов устройства][DeviceToolbar]имитируйте размеры окна просмотра Moto G4 в списке **устройств** .</span><span class="sxs-lookup"><span data-stu-id="618d4-196">After [enabling the Device Toolbar][DeviceToolbar], simulate the dimensions of a Moto G4 viewport from the **Device** list.</span></span>  

> ##### <span data-ttu-id="618d4-197">Рисунок 10</span><span class="sxs-lookup"><span data-stu-id="618d4-197">Figure 10</span></span>  
> <span data-ttu-id="618d4-198">Имитация окна просмотра Moto G4</span><span class="sxs-lookup"><span data-stu-id="618d4-198">Simulating a Moto G4 viewport</span></span>  
> ![Имитация окна просмотра Moto G4][ImageMotoG4]  

<span data-ttu-id="618d4-200">Щелкните [Показать рамку устройства][DeviceFrame] , чтобы показать аппаратуру Moto G4 в окне просмотра.</span><span class="sxs-lookup"><span data-stu-id="618d4-200">Click [Show Device Frame][DeviceFrame] to show the Moto G4 hardware around the viewport.</span></span>  

> ##### <span data-ttu-id="618d4-201">Рисунок11</span><span class="sxs-lookup"><span data-stu-id="618d4-201">Figure 11</span></span>  
> <span data-ttu-id="618d4-202">Аппаратное обеспечение Moto G4</span><span class="sxs-lookup"><span data-stu-id="618d4-202">Showing the Moto G4 hardware</span></span>  
> ![Аппаратное обеспечение Moto G4][ImageMotoG4Frame]  

<span data-ttu-id="618d4-204">Дополнительные возможности:</span><span class="sxs-lookup"><span data-stu-id="618d4-204">Related features:</span></span>  

*   <span data-ttu-id="618d4-205">Откройте [меню команд][CommandMenu] и выполните команду, `Capture screenshot` чтобы сделать снимок экрана просмотра, включающий оборудование Moto G4 (после включения команды **Показать рамку устройства**).</span><span class="sxs-lookup"><span data-stu-id="618d4-205">Open the [Command Menu][CommandMenu] and run the `Capture screenshot` command to take a screenshot of the viewport that includes the Moto G4 hardware (after enabling **Show Device Frame**).</span></span>  
*   <span data-ttu-id="618d4-206">[Регулирование сети и ЦП][ThrottleNetworkAndCpu] для более точной имитации условий просмотра веб-страниц пользователя на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="618d4-206">[Throttle the network and CPU][ThrottleNetworkAndCpu] to more accurately simulate a mobile user's web browsing conditions.</span></span>  

<span data-ttu-id="618d4-207">[#924693][crbug924693] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="618d4-207">Chromium issue [#924693][crbug924693]</span></span>  

### <span data-ttu-id="618d4-208">Обновления, связанные с файлами cookie</span><span class="sxs-lookup"><span data-stu-id="618d4-208">Cookie-related updates</span></span>   

#### <span data-ttu-id="618d4-209">Заблокированные cookie-файлы в области "cookie"</span><span class="sxs-lookup"><span data-stu-id="618d4-209">Blocked cookies in the Cookies pane</span></span>   

<span data-ttu-id="618d4-210">В области "файлы cookie" на панели приложения теперь отображаются заблокированные файлы cookie с желтым фоном.</span><span class="sxs-lookup"><span data-stu-id="618d4-210">The Cookies pane in the Application panel now displays blocked cookies with a yellow background.</span></span>  

> ##### <span data-ttu-id="618d4-211">Рисунок12</span><span class="sxs-lookup"><span data-stu-id="618d4-211">Figure 12</span></span>  
> <span data-ttu-id="618d4-212">Заблокированные cookie-файлы в области "cookie" на панели приложения</span><span class="sxs-lookup"><span data-stu-id="618d4-212">Blocked cookies in the Cookies pane of the Application panel</span></span>  
> ![Заблокированные cookie-файлы в области "cookie" на панели приложения][ImageBlockedCookies]  

<span data-ttu-id="618d4-214">[#1030258][crbug|::ref1::|] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="618d4-214">Chromium issue [#1030258][crbug|::ref1::|]</span></span>  

#### <span data-ttu-id="618d4-215">Приоритет cookie-файлов в области "cookie"</span><span class="sxs-lookup"><span data-stu-id="618d4-215">Cookie priority in the Cookie pane</span></span>   

<span data-ttu-id="618d4-216">Таблицы cookie на панелях сеть и приложения теперь включают столбец **приоритета** .</span><span class="sxs-lookup"><span data-stu-id="618d4-216">The Cookies tables in the Network and Application panels now include a **Priority** column.</span></span>  

> [!CAUTION]
> <span data-ttu-id="618d4-217">Chromiumные браузеры, такие как Microsoft EDGE, — это единственные браузеры, поддерживающие приоритет cookie-файлов.</span><span class="sxs-lookup"><span data-stu-id="618d4-217">Chromium-based browsers, like Microsoft Edge, are the only browsers that support cookie priority.</span></span>  

<span data-ttu-id="618d4-218">[#1026879][crbug1026879] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="618d4-218">Chromium issue [#1026879][crbug1026879]</span></span>  

#### <span data-ttu-id="618d4-219">Изменение всех значений cookie-файлов</span><span class="sxs-lookup"><span data-stu-id="618d4-219">Edit all cookie values</span></span>   

<span data-ttu-id="618d4-220">Все ячейки в таблицах cookie теперь доступны для редактирования, кроме ячеек в столбце **Размер** , так как этот столбец представляет размер файла cookie в байтах.</span><span class="sxs-lookup"><span data-stu-id="618d4-220">All cells in the Cookie tables are editable now, except cells in the **Size** column because that column represents the network size of the cookie, in bytes.</span></span>  <span data-ttu-id="618d4-221">Просмотрите [поля][CookiesFields] , поясняющие каждый столбец.</span><span class="sxs-lookup"><span data-stu-id="618d4-221">See [Fields][CookiesFields] for an explanation of each column.</span></span>  

> ##### <span data-ttu-id="618d4-222">Рисунок13</span><span class="sxs-lookup"><span data-stu-id="618d4-222">Figure 13</span></span>  
> <span data-ttu-id="618d4-223">Изменение значения cookie-файла</span><span class="sxs-lookup"><span data-stu-id="618d4-223">Editing a cookie value</span></span>  
> ![Изменение значения cookie-файла][ImageEditCookie]  

#### <span data-ttu-id="618d4-225">Копировать как Node. js выборка для включения данных cookie</span><span class="sxs-lookup"><span data-stu-id="618d4-225">Copy as Node.js fetch to include cookie data</span></span>   

<span data-ttu-id="618d4-226">Щелкните сетевой запрос правой кнопкой мыши и выберите команду **Копировать**  >  **копию как Node. js** , чтобы получить `fetch` выражение, включающее данные cookie.</span><span class="sxs-lookup"><span data-stu-id="618d4-226">Right-click a network request and select **Copy** > **Copy as Node.js fetch** to get a `fetch` expression that includes cookie data.</span></span>  

> ##### <span data-ttu-id="618d4-227">Рисунок14</span><span class="sxs-lookup"><span data-stu-id="618d4-227">Figure 14</span></span>  
> <span data-ttu-id="618d4-228">Выборка "Копировать как Node. js"</span><span class="sxs-lookup"><span data-stu-id="618d4-228">Copy as Node.js fetch</span></span>  
> ![Выборка "Копировать как Node. js"][ImageCopyFetch]  

<span data-ttu-id="618d4-230">[#1029826][crbug1029826] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="618d4-230">Chromium issue [#1029826][crbug1029826]</span></span>  

### <span data-ttu-id="618d4-231">Более точные значки манифеста веб-приложения</span><span class="sxs-lookup"><span data-stu-id="618d4-231">More accurate web app manifest icons</span></span>   

<span data-ttu-id="618d4-232">Ранее область манифеста на панели приложения отправляет свои собственные запросы для отображения значков манифеста веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="618d4-232">Previously, the Manifest pane in the Application panel sent its own requests in order to display web app manifest icons.</span></span>  <span data-ttu-id="618d4-233">DevTools теперь показывает тот же значок манифеста, который использует Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="618d4-233">DevTools now shows the exact same manifest icon that Microsoft Edge uses.</span></span>  

> ##### <span data-ttu-id="618d4-234">Рисунок15</span><span class="sxs-lookup"><span data-stu-id="618d4-234">Figure 15</span></span>  
> <span data-ttu-id="618d4-235">Значки в области «манифест»</span><span class="sxs-lookup"><span data-stu-id="618d4-235">Icons in the Manifest pane</span></span>  
> ![Значки в области «манифест»][ImageManifestIcon]   

<span data-ttu-id="618d4-237">[#985402][crbug985402] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="618d4-237">Chromium issue [#985402][crbug985402]</span></span>  

### <span data-ttu-id="618d4-238">Наведите указатель мыши на свойства содержимого CSS, чтобы увидеть неэкранированные значения</span><span class="sxs-lookup"><span data-stu-id="618d4-238">Hover over CSS content properties to see unescaped values</span></span>   

<span data-ttu-id="618d4-239">Наведите указатель мыши на значение `content` свойства, чтобы увидеть неэкранированную версию значения.</span><span class="sxs-lookup"><span data-stu-id="618d4-239">Hover over the value of a `content` property to see the unescaped version of the value.</span></span>  

<span data-ttu-id="618d4-240">Например, в этой статье вы узнаете [о том,][CSSContentDemo] что на `p::after` панели Стили отображается строка с escape-символами.</span><span class="sxs-lookup"><span data-stu-id="618d4-240">For example, in this [demo][CSSContentDemo] when you inspect the `p::after` pseudo-element you see an escaped string in the Styles pane:</span></span>  

> ##### <span data-ttu-id="618d4-241">Рисунок16</span><span class="sxs-lookup"><span data-stu-id="618d4-241">Figure 16</span></span>  
> <span data-ttu-id="618d4-242">Строка с escape-символом</span><span class="sxs-lookup"><span data-stu-id="618d4-242">The escaped string</span></span>  
> ![Строка с escape-символом][ImageEscapedString]   

<span data-ttu-id="618d4-244">При наведении указателя мыши на значение, которое `content` отображается в неэкранированном значении:</span><span class="sxs-lookup"><span data-stu-id="618d4-244">When you hover over the `content` value you see the unescaped value:</span></span>  

> ##### <span data-ttu-id="618d4-245">Рисунок17</span><span class="sxs-lookup"><span data-stu-id="618d4-245">Figure 17</span></span>  
> <span data-ttu-id="618d4-246">Неэкранированное значение</span><span class="sxs-lookup"><span data-stu-id="618d4-246">The unescaped value</span></span>  
> ![Неэкранированное значение][ImageUnescapedString]   

### <span data-ttu-id="618d4-248">Дополнительные сведения об ошибках на карте исходного кода на консоли</span><span class="sxs-lookup"><span data-stu-id="618d4-248">More detailed source map errors in the Console</span></span>   

<span data-ttu-id="618d4-249">Теперь консоль содержит более подробные сведения о том, почему не удалось загрузить или проанализировать исходную карту.</span><span class="sxs-lookup"><span data-stu-id="618d4-249">The Console now provides more detail on why a source map failed to load or parse.</span></span>  <span data-ttu-id="618d4-250">Ранее она только что предоставила ошибку, не объясняющую, что пошло не так.</span><span class="sxs-lookup"><span data-stu-id="618d4-250">Previously it just provided an error without explaining what went wrong.</span></span>  

> ##### <span data-ttu-id="618d4-251">Рис. 18</span><span class="sxs-lookup"><span data-stu-id="618d4-251">Figure 18</span></span>  
> <span data-ttu-id="618d4-252">Ошибка при загрузке карты исходного кода на консоли</span><span class="sxs-lookup"><span data-stu-id="618d4-252">A source map loading error in the Console</span></span>  
> ![Ошибка при загрузке карты исходного кода на консоли][ImageSourcemapError]  

### <span data-ttu-id="618d4-254">Настройка отключения прокрутки за пределами файла</span><span class="sxs-lookup"><span data-stu-id="618d4-254">Setting for disabling scrolling past the end of a file</span></span>   

<span data-ttu-id="618d4-255">Откройте [Параметры][Settings] и выберите Отключить **Preferences**  >  **исходные**настройки.  >  **разрешите прокрутку за** пределами файла, чтобы отключить поведение пользовательского интерфейса по умолчанию, позволяющее прокручивать прокрутку за пределами файла на панели « **источники** ».</span><span class="sxs-lookup"><span data-stu-id="618d4-255">Open [Settings][Settings] and then disable **Preferences** > **Sources** > **Allow scrolling past end of file** to disable the default UI behavior that allows you to scroll well past the end of a file in the **Sources** panel.</span></span>  

> ##### <span data-ttu-id="618d4-256">На рисунке 19</span><span class="sxs-lookup"><span data-stu-id="618d4-256">Figure 19</span></span>  
> <span data-ttu-id="618d4-257">Отключение **разрешения на прокрутку за** пределами файла в параметрах</span><span class="sxs-lookup"><span data-stu-id="618d4-257">Disabling **Allow scrolling past end of file** in Settings</span></span>  
> ![Отключение разрешения на прокрутку за пределами файла][ImageSettings]  

> ##### <span data-ttu-id="618d4-259">Рис. 20</span><span class="sxs-lookup"><span data-stu-id="618d4-259">Figure 20</span></span>  
> <span data-ttu-id="618d4-260">Прокрутка за пределами файла теперь отключена на панели «источники»</span><span class="sxs-lookup"><span data-stu-id="618d4-260">Scrolling past the end of a file is now disabled in the Sources panel</span></span>  
> ![Прокрутка за пределами файла теперь отключена на панели «источники»][ImageScroll]  

## <span data-ttu-id="618d4-262">Отзыв</span><span class="sxs-lookup"><span data-stu-id="618d4-262">Feedback</span></span>   



<span data-ttu-id="618d4-263">Чтобы обсудить новые возможности и изменения в этой записи, а также другие связанные с DevTools, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="618d4-263">To discuss the new features and changes in this post, or anything else related to DevTools:</span></span>  

*   <span data-ttu-id="618d4-264">Отправка отзыва с помощью значка **обратной связи** в DevTools</span><span class="sxs-lookup"><span data-stu-id="618d4-264">Send your feedback using the **Feedback** icon in the DevTools</span></span>  

> ##### <span data-ttu-id="618d4-265">Рисунок 21</span><span class="sxs-lookup"><span data-stu-id="618d4-265">Figure 21</span></span>  
> <span data-ttu-id="618d4-266">Значок **обратной связи** в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="618d4-266">The **Feedback** icon in the Microsoft Edge DevTools</span></span>  
> ![Значок \* \* Feedback \* \* в Microsoft Edge DevTools][ImageFeedbackIcon]  

*   <span data-ttu-id="618d4-268">Твит на [@EdgeDevTools][PostTweetEdgeDevTools]</span><span class="sxs-lookup"><span data-stu-id="618d4-268">Tweet at [@EdgeDevTools][PostTweetEdgeDevTools]</span></span>  
*   <span data-ttu-id="618d4-269">Отправка предложения в [Вебе][TheWebWeWant]</span><span class="sxs-lookup"><span data-stu-id="618d4-269">Submit a suggestion to [The Web We Want][TheWebWeWant]</span></span>  
*   <span data-ttu-id="618d4-270">Ошибки файла в этом документе в репозитории " [Edge — разработчик][GitHubMicrosoftDocsEdgeDeveloperNewIssue] "</span><span class="sxs-lookup"><span data-stu-id="618d4-270">File bugs on this document in the [edge-developer][GitHubMicrosoftDocsEdgeDeveloperNewIssue] repository</span></span>  

## <span data-ttu-id="618d4-271">Загрузка каналов предварительной версии Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="618d4-271">Download the Microsoft Edge preview channels</span></span>   

<span data-ttu-id="618d4-272">Если вы используете Windows или macOS, рассматривайте в качестве браузера по умолчанию использование [каналов предварительного просмотра Microsoft Edge][MicrosoftEdgePreviewChannels] .</span><span class="sxs-lookup"><span data-stu-id="618d4-272">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="618d4-273">Каналы предварительного просмотра предоставляют доступ к последним функциям DevTools.</span><span class="sxs-lookup"><span data-stu-id="618d4-273">The preview channels give you access to the latest DevTools features.</span></span>  

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
[ImageCopyFetch]: ../../images/2020/01/fetchcookies.msft.png "Рисунок 14: Копировать как Node. js"
[ImageManifestIcon]: ../../images/2020/01/manifesticons.msft.png "Рисунок 15: значки в области манифеста"
[ImageEscapedString]: ../../images/2020/01/escapedstring.msft.png "Рисунок 16: строка с escape-символом"
[ImageUnescapedString]: ../../images/2020/01/unescapedstring.msft.png "Рисунок 17: Неэкранированное значение"
[ImageSourcemapError]: ../../images/2020/01/sourcemap.msft.png "Рисунок 18: ошибка при загрузке карты исходного кода на консоли"
[ImageSettings]: ../../images/2020/01/settings.msft.png "Рисунок 19: отключение режима "Разрешить прокрутку за конец файла" в параметрах"
[ImageScroll]: ../../images/2020/01/scrollingsources.msft.png "Рисунок 20: прокрутка за пределами файла теперь отключена на панели «источники»"
[ImageFeedbackIcon]: ../../images/2020/01/feedback-icon.msft.png "Рисунок 21: значок * * Feedback * * в Microsoft Edge DevTools"


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
> <span data-ttu-id="618d4-331">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="618d4-331">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="618d4-332">Исходная страница будет найдена [здесь](https://developers.google.com/web/updates/2020/01/devtools/index) и [Kayce Basques][KayceBasques] \ (технический писатель, хром DevTools & Lighthouse).</span><span class="sxs-lookup"><span data-stu-id="618d4-332">The original page is found [here](https://developers.google.com/web/updates/2020/01/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools & Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="618d4-334">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="618d4-334">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  