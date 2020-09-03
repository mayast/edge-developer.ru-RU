---
description: Улучшения специальных возможностей, использование DevTools на других языках и многое другое.
title: Новые возможности DevTools (Microsoft Edge 80)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/01/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: dcc6c97cfb355d654c596f4be29de6507174bebd
ms.sourcegitcommit: 63e6d34ff483f3b419a0e271a3513874e6ce6c79
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/02/2020
ms.locfileid: "10993403"
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

# <span data-ttu-id="f1989-104">Новые возможности DevTools (Microsoft Edge 80)</span><span class="sxs-lookup"><span data-stu-id="f1989-104">What's new in DevTools (Microsoft Edge 80)</span></span>  

## <span data-ttu-id="f1989-105">Объявления из группы Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="f1989-105">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="f1989-106">В следующих разделах представлен список извещений, которые вы могли не получить в Microsoft Edge DevTools Teams!</span><span class="sxs-lookup"><span data-stu-id="f1989-106">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team!</span></span> <span data-ttu-id="f1989-107">Узнайте, как использовать новые функции в DevTools, расширения кода VS и многое другое.</span><span class="sxs-lookup"><span data-stu-id="f1989-107">Check them out to try new features in the DevTools, VS Code extensions, and more.</span></span>  <span data-ttu-id="f1989-108">Чтобы оставаться на связи с самыми последними и более свежими возможностями, скачайте на веб – [каналы предварительной версии Microsoft Edge][MicrosoftEdgePreviewChannels] и [следуйте указаниям Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="f1989-108">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <span data-ttu-id="f1989-109">Улучшение специальных возможностей в DevTools</span><span class="sxs-lookup"><span data-stu-id="f1989-109">Accessibility improvements to the DevTools</span></span>  

<span data-ttu-id="f1989-110">Группа DevTools изменила 170 в Chromium для устранения проблем с высокой контрастностью цвета, клавиатуры и средства чтения с экрана в DevTools.</span><span class="sxs-lookup"><span data-stu-id="f1989-110">The DevTools team has contributed 170 changes to Chromium to address high-impact color contrast, keyboard, and screen reader issues in the DevTools.</span></span>  <span data-ttu-id="f1989-111">Каждый разработчик, создающий веб-сайт, должен иметь возможность использовать DevTools.</span><span class="sxs-lookup"><span data-stu-id="f1989-111">Every developer building the web should be able to use the DevTools.</span></span>  

> ##### <span data-ttu-id="f1989-112">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="f1989-112">Figure 1</span></span>  
> <span data-ttu-id="f1989-113">Средство "производительность" в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана</span><span class="sxs-lookup"><span data-stu-id="f1989-113">The Performance tool in the DevTools with the keyboard navigation and screen reader improvements</span></span>  
> ![Средство "производительность" в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана][ImagePerformanceToolKeyboardReaderImprovements]  

<span data-ttu-id="f1989-115">Сведения о том, как сделать веб-страницу доступной для всех пользователей?</span><span class="sxs-lookup"><span data-stu-id="f1989-115">Want to learn how to make your web page accessible to all of your users?</span></span>  <span data-ttu-id="f1989-116">Скачайте [расширения для][WebhintBrowserExtension] Microsoft Edge " [Специальные возможности][AccessibilityInsights] ", чтобы приступить к работе.</span><span class="sxs-lookup"><span data-stu-id="f1989-116">Download the [Accessibility Insights][AccessibilityInsights] and [webhint][WebhintBrowserExtension] extensions for Microsoft Edge to get started.</span></span>  

<span data-ttu-id="f1989-117">Если вы используете средства чтения с экрана или клавиатуру для навигации по DevTools, отправьте нам свой отзыв, выполнив [твит][PostTweetEdgeDevTools] в США или щелкнув значок [Отправить отзыв](#getting-in-touch-with-microsoft-edge-devtools-team) !</span><span class="sxs-lookup"><span data-stu-id="f1989-117">If you use screen readers or the keyboard to navigate around the DevTools, send us your feedback by [tweeting][PostTweetEdgeDevTools] at us or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="f1989-118">[#963183][crbug963183] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="f1989-118">Chromium issue [#963183][crbug963183]</span></span>  

### <span data-ttu-id="f1989-119">Использование DevTools на других языках</span><span class="sxs-lookup"><span data-stu-id="f1989-119">Using the DevTools in other languages</span></span>  

<span data-ttu-id="f1989-120">Многие разработчики используют другие инструменты разработчика, такие как StackOverflow и код VS, на родном языке, а не только на английском языке.</span><span class="sxs-lookup"><span data-stu-id="f1989-120">Many developers use other developer tools, like StackOverflow and VS Code, in their native language, not just in English.</span></span>  <span data-ttu-id="f1989-121">Мы рады объявить локализацию для DevTools, который теперь вы можете использовать на одном из 10 языков, кроме английского.</span><span class="sxs-lookup"><span data-stu-id="f1989-121">We’re excited to announce localization for the DevTools, which you are now able to use in one of 10 languages besides English:</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="f1989-122">Китайский (упрощенное письмо) —  &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span><span class="sxs-lookup"><span data-stu-id="f1989-122">Chinese \(Simplified\) - &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="f1989-123">Китайский (традиционное письмо) —  &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span><span class="sxs-lookup"><span data-stu-id="f1989-123">Chinese \(Traditional\) - &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="f1989-124">Французский — Fran&#231;AIS</span><span class="sxs-lookup"><span data-stu-id="f1989-124">French – fran&#231;ais</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="f1989-125">Немецкий — Deutsch</span><span class="sxs-lookup"><span data-stu-id="f1989-125">German - deutsch</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="f1989-126">Итальянский — Italiano</span><span class="sxs-lookup"><span data-stu-id="f1989-126">Italian - italiano</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="f1989-127">Японская  &#26085;&#26412;&#35486;</span><span class="sxs-lookup"><span data-stu-id="f1989-127">Japanese - &#26085;&#26412;&#35486;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="f1989-128">Корейский —  &#54620;&#44397;&#50612;</span><span class="sxs-lookup"><span data-stu-id="f1989-128">Korean - &#54620;&#44397;&#50612;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="f1989-129">Португальский (portugu&#234;s)</span><span class="sxs-lookup"><span data-stu-id="f1989-129">Portuguese - portugu&#234;s</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="f1989-130">Русский —  &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span><span class="sxs-lookup"><span data-stu-id="f1989-130">Russian – &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="f1989-131">Испанская — ESPA&#241;OL</span><span class="sxs-lookup"><span data-stu-id="f1989-131">Spanish - espa&#241;ol</span></span>
   :::column-end:::
:::row-end:::

<!--  
|  |  |  
|:--- |:--- |  
| Chinese (Simplified) - 中文（简体）| Chinese (Traditional) - 中文（繁體）|  
| French – français | German - deutsch |  
| Italian - italiano | Portuguese - português |  
| Korean - 한국어 | Japanese - 日本語 |  
| Russian – русский | Spanish - español |  
-->  

<span data-ttu-id="f1989-132">Перейдите к разделу `edge://flags` **Включение локализованных средств разработчика** в состояние **включено**и установите для него флажок Включить.</span><span class="sxs-lookup"><span data-stu-id="f1989-132">Navigate to `edge://flags` and set the **Enable localized Developer Tools** flag to **Enabled**.</span></span>  <span data-ttu-id="f1989-133">Также установите флажок **эксперименты со средствами разработчика** для **включения**.</span><span class="sxs-lookup"><span data-stu-id="f1989-133">Also set the **Developer Tools experiments** flag to **Enabled**.</span></span>  <span data-ttu-id="f1989-134">Перезапустите Microsoft EDGE и откройте DevTools.</span><span class="sxs-lookup"><span data-stu-id="f1989-134">Restart Microsoft Edge and open the DevTools.</span></span>  <!-- Press `F1` in the DevTools or go to Settings > Experiments and check the **Match browser language** checkbox.  -->  <span data-ttu-id="f1989-135">DevTools соответствует языку, используемому в Microsoft Edge in `edge://settings/languages` .</span><span class="sxs-lookup"><span data-stu-id="f1989-135">The DevTools match the language you use for Microsoft Edge in `edge://settings/languages`.</span></span>  

> ##### <span data-ttu-id="f1989-136">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="f1989-136">Figure 2</span></span>  
> <span data-ttu-id="f1989-137">DevTools на немецком языке</span><span class="sxs-lookup"><span data-stu-id="f1989-137">The DevTools in German</span></span>  
> ![DevTools на немецком языке][ImageLocalizedGerman]  

<span data-ttu-id="f1989-139">Если вы хотите использовать DevTools на языке, отличном от того, на котором они доступны, [твит][PostTweetEdgeDevTools] в США или щелкните значок [Отправить отзыв](#getting-in-touch-with-microsoft-edge-devtools-team) .</span><span class="sxs-lookup"><span data-stu-id="f1989-139">If you want to use the DevTools in a different language than the ones that are available, [tweet][PostTweetEdgeDevTools] at us or click the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon.</span></span>  

<span data-ttu-id="f1989-140">[#941561][crbug941561] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="f1989-140">Chromium issue [#941561][crbug941561]</span></span>  

### <span data-ttu-id="f1989-141">Веб – подсказка с расширением Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f1989-141">webhint Microsoft Edge extension</span></span>  

<span data-ttu-id="f1989-142">Расширение веб-подсказки Microsoft EDGE позволяет легко находить и получать отзывы о специальных возможностях, совместимости с браузерами, безопасности, производительности и других средствах в DevTools.</span><span class="sxs-lookup"><span data-stu-id="f1989-142">The webhint Microsoft Edge extension allows you to easily scan your web page and get feedback on accessibility, browser compatibility, security, performance, and more within the DevTools.</span></span>  <span data-ttu-id="f1989-143">Узнайте больше о [https://webhint.io][Webhint] .</span><span class="sxs-lookup"><span data-stu-id="f1989-143">Read more at [https://webhint.io][Webhint].</span></span>  

> ##### <span data-ttu-id="f1989-144">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="f1989-144">Figure 3</span></span>  
> <span data-ttu-id="f1989-145">Вкладка "Подсказка" в DevTools, если установлено расширение браузера веб.</span><span class="sxs-lookup"><span data-stu-id="f1989-145">The Hints tab in the DevTools when the webhint browser extension is installed</span></span>  
> ![Вкладка "Подсказка" в DevTools, если установлено расширение браузера веб.][ImageHintsTabWebhintExtension]  

<span data-ttu-id="f1989-147">[Попробуйте расширение браузера веб для подсказки в Microsoft Edge][MicrosoftEdgeInsiderAddons].</span><span class="sxs-lookup"><span data-stu-id="f1989-147">[Try the webhint browser extension in Microsoft Edge][MicrosoftEdgeInsiderAddons].</span></span>  <span data-ttu-id="f1989-148">После установки расширения откройте DevTools и перейдите на вкладку подсказки.  В этой статье запустите настраиваемое сканирование сайта.</span><span class="sxs-lookup"><span data-stu-id="f1989-148">Once you install the extension, open the DevTools and select the Hints tab.  From here, run a customizable site scan.</span></span>  <span data-ttu-id="f1989-149">Чтобы получить дополнительные сведения, [заwebhint.IO][WebhintBrowserExtension] в голову.</span><span class="sxs-lookup"><span data-stu-id="f1989-149">Head over to [webhint.io][WebhintBrowserExtension] to learn more.</span></span>

### <span data-ttu-id="f1989-150">Трехмерное представление</span><span class="sxs-lookup"><span data-stu-id="f1989-150">3D View</span></span>  

<span data-ttu-id="f1989-151">С помощью **трехмерного представления** вы можете выполнять отладку своего веб-приложения, перемещаясь по [объектной модели документов \ (DOM)][MDNDocumentObjectModel] или контексту стека [z-индексов][MDNZIndex] .</span><span class="sxs-lookup"><span data-stu-id="f1989-151">Use the **3D View** to debug your web application by navigating through the [Document Object Model \(DOM\)][MDNDocumentObjectModel] or the [z-index][MDNZIndex] stacking context.</span></span>  

> ##### <span data-ttu-id="f1989-152">Рисунок4</span><span class="sxs-lookup"><span data-stu-id="f1989-152">Figure 4</span></span>  
> <span data-ttu-id="f1989-153">Трехмерное представление в DevTools</span><span class="sxs-lookup"><span data-stu-id="f1989-153">The 3D View in the DevTools</span></span>  
> ![Трехмерное представление в DevTools][Image3DView]  

<span data-ttu-id="f1989-155">Чтобы получить доступ к трехмерному представлению, перейдите в раздел `edge://flags` и убедитесь, что флаг **эксперименты со средствами разработчика** установлен в **разрешено**.</span><span class="sxs-lookup"><span data-stu-id="f1989-155">To access the 3D View, navigate to `edge://flags` and ensure that the **Developer Tools experiments** flag is set to **Enabled**.</span></span>  <span data-ttu-id="f1989-156">Перезапустите Microsoft EDGE и откройте DevTools.</span><span class="sxs-lookup"><span data-stu-id="f1989-156">Restart Microsoft Edge and open the DevTools.</span></span>  <span data-ttu-id="f1989-157">Нажмите кнопку `F1` DevTools или выберите **Параметры**, перейдите к разделу " **эксперименты** " и установите флажок **включить трехмерное представление** .</span><span class="sxs-lookup"><span data-stu-id="f1989-157">Press `F1` in the DevTools or go to **Settings**, navigate to **Experiments** section, and check the **Enable 3D View** checkbox.</span></span>  <span data-ttu-id="f1989-158">Теперь нажмите клавишу `Ctrl`  +  `Shift`  +  `P` Ввод в **3D-представление** и выберите **Показать 3D-представление**.</span><span class="sxs-lookup"><span data-stu-id="f1989-158">Now, press `Ctrl` + `Shift` + `P`, type in **3D View** and select **Show 3D View**.</span></span>  

<span data-ttu-id="f1989-159">Мы работаем над ИНТЕРФЕЙСом и добавляем дополнительные функции в представление 3D, поэтому отправьте нам свой [отзыв](#getting-in-touch-with-microsoft-edge-devtools-team).</span><span class="sxs-lookup"><span data-stu-id="f1989-159">We're working on the UI and adding more functionality to the 3D View so please send us your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team).</span></span>  

<span data-ttu-id="f1989-160">[#987787][crbug987787] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="f1989-160">Chromium issue [#987787][crbug987787]</span></span>

### <span data-ttu-id="f1989-161">Расширения кода Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f1989-161">Visual Studio Code extensions</span></span>  

<span data-ttu-id="f1989-162">Кроме того, Группа DevTools также выпустила некоторые расширения для [кода Visual Studio \ (код VS)][VisualStudioCode] , которые позволяют использовать возможности DevTools прямо из текстового редактора.</span><span class="sxs-lookup"><span data-stu-id="f1989-162">The DevTools team has also released some extensions for [Visual Studio Code \(VS Code\)][VisualStudioCode] that let you use the power of the DevTools directly from your text editor!</span></span> <span data-ttu-id="f1989-163">Ознакомьтесь с приведенными ниже расширениями.</span><span class="sxs-lookup"><span data-stu-id="f1989-163">Check out the extensions below:</span></span>  

#### <span data-ttu-id="f1989-164">Элементы Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f1989-164">Elements for Microsoft Edge</span></span>  

<span data-ttu-id="f1989-165">С помощью инструмента "элементы" в коде VS добавьте [элементы для расширения кода Microsoft Edge \ (Chromium \)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] vs.</span><span class="sxs-lookup"><span data-stu-id="f1989-165">Use the Elements tool from within VS Code by adding the [Elements for Microsoft Edge \(Chromium\)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] VS Code extension.</span></span>  

> ##### <span data-ttu-id="f1989-166">Рисунок 5</span><span class="sxs-lookup"><span data-stu-id="f1989-166">Figure 5</span></span>  
> <span data-ttu-id="f1989-167">Инструмент "элементы" в коде VS с использованием элементов для расширения Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f1989-167">The Elements tool in VS Code using the Elements for Microsoft Edge extension</span></span>  
> ![Инструмент "элементы" в коде VS с использованием элементов для расширения Microsoft Edge][ImageElementsVisualStudioCode]  

<span data-ttu-id="f1989-169">Для получения дополнительных сведений изучите [элементы для расширения кода Microsoft Edge VS][VisualStudioCodeElementEdgeExtension].</span><span class="sxs-lookup"><span data-stu-id="f1989-169">For more information, check out [Elements for Microsoft Edge VS Code extension][VisualStudioCodeElementEdgeExtension].</span></span>  

#### <span data-ttu-id="f1989-170">Отладчик для Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f1989-170">Debugger for Microsoft Edge</span></span>  

<span data-ttu-id="f1989-171">С помощью [отладчика для расширения кода Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] , Отладка JavaScript выполняется в Microsoft Edge прямо из кода vs.</span><span class="sxs-lookup"><span data-stu-id="f1989-171">With the [Debugger for Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] VS Code extension, debug JavaScript running in Microsoft Edge directly from VS Code!</span></span>  

> ##### <span data-ttu-id="f1989-172">Рисунок6</span><span class="sxs-lookup"><span data-stu-id="f1989-172">Figure 6</span></span>  
> <span data-ttu-id="f1989-173">Отладчик для расширения Microsoft EDGE в коде VS</span><span class="sxs-lookup"><span data-stu-id="f1989-173">The Debugger for Microsoft Edge Extension in VS Code</span></span>  
> ![Отладчик для расширения Microsoft EDGE в коде VS][ImageDebuggerExtensionVisualStudioCode]  

<span data-ttu-id="f1989-175">Дополнительные сведения [об отладке Microsoft Edge из кода VS можно][VisualStudioCodeDebuggerEdgeExtension]найти здесь.</span><span class="sxs-lookup"><span data-stu-id="f1989-175">For more information, check out [how to debug Microsoft Edge from VS Code][VisualStudioCodeDebuggerEdgeExtension].</span></span>  

#### <span data-ttu-id="f1989-176">webhint</span><span class="sxs-lookup"><span data-stu-id="f1989-176">webhint</span></span>  

<span data-ttu-id="f1989-177">Расширение веб- [подсказки][VisualStudioMarketplaceWebhintExtension] и кода используются `webhint` для усовершенствования своей страницы, пока вы пишете ее!</span><span class="sxs-lookup"><span data-stu-id="f1989-177">The [webhint][VisualStudioMarketplaceWebhintExtension] VS Code extension uses `webhint` to improve your web page while you're writing it!</span></span> <span data-ttu-id="f1989-178">Это расширение запускает и сообщает диагностику файлов рабочей области на основе `webhint` анализа.</span><span class="sxs-lookup"><span data-stu-id="f1989-178">This extension runs and reports diagnostics on your workspace files based on `webhint` analysis.</span></span>  

> ##### <span data-ttu-id="f1989-179">Рисунок7</span><span class="sxs-lookup"><span data-stu-id="f1989-179">Figure 7</span></span>  
> <span data-ttu-id="f1989-180">Анализ файла и расширения кода веб-подсказки в коде VS</span><span class="sxs-lookup"><span data-stu-id="f1989-180">The webhint VS Code extension analyzing a .tsx file in VS Code</span></span>  
> ![Анализ файла и расширения кода веб-подсказки в коде VS][ImageWebhintVisualStudioCodeExtensionWorkspace]  

<span data-ttu-id="f1989-182">[Узнайте больше о расширении подсказки кода VS][WebhintVisualStudioCodeExtension].</span><span class="sxs-lookup"><span data-stu-id="f1989-182">[Learn more about the VS Code webhint extension][WebhintVisualStudioCodeExtension].</span></span>  

### <span data-ttu-id="f1989-183">Интеграция с Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f1989-183">Visual Studio integration</span></span>
<span data-ttu-id="f1989-184">В Visual Studio 2019 версии 16,2 или более поздней Используйте отладчик Visual Studio для отладки JavaScript, который выполняется в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="f1989-184">In Visual Studio 2019 version 16.2 or later, use the Visual Studio debugger to debug JavaScript running in Microsoft Edge.</span></span>  <span data-ttu-id="f1989-185">[Загрузите Visual Studio 2019][MicrosoftVisualStudioDownloads] , чтобы попробовать эту функцию!</span><span class="sxs-lookup"><span data-stu-id="f1989-185">[Download Visual Studio 2019][MicrosoftVisualStudioDownloads] to try this feature out!</span></span>  

> ##### <span data-ttu-id="f1989-186">Рисунок8</span><span class="sxs-lookup"><span data-stu-id="f1989-186">Figure 8</span></span>  
> <span data-ttu-id="f1989-187">Visual Studio с возможностью запуска веб-приложения в Microsoft Edge Канарские, dev или Beta</span><span class="sxs-lookup"><span data-stu-id="f1989-187">Visual Studio with the option to launch your web app in Microsoft Edge Canary, Dev, or Beta</span></span>  
> ![Visual Studio с возможностью запуска веб-приложения в Microsoft Edge Канарские, dev или Beta][ImageVisualStudioLaunchWebApp]  

<span data-ttu-id="f1989-189">[В этой статье рассказывается о том, как отлаживать Microsoft Edge из Visual Studio][MicrosoftVisualStudioBlogDebugJavascript].</span><span class="sxs-lookup"><span data-stu-id="f1989-189">[Read our blog post to learn how to debug Microsoft Edge from Visual Studio][MicrosoftVisualStudioBlogDebugJavascript].</span></span>  

### <span data-ttu-id="f1989-190">Сообщения консоли предотвращения отслеживания</span><span class="sxs-lookup"><span data-stu-id="f1989-190">Tracking prevention Console messages</span></span>  

<span data-ttu-id="f1989-191">Защита от слежения — это уникальная функция в Microsoft EDGE, которая защищает вас от отслеживания веб-сайтов, которые вы еще не посещаете.</span><span class="sxs-lookup"><span data-stu-id="f1989-191">Tracking prevention is a unique feature in Microsoft Edge that protects you from being tracked by websites you haven't visited before.</span></span>  <span data-ttu-id="f1989-192">Параметр предотвращения отслеживания по умолчанию — это режим балансировки, который блокирует средства отслеживания и известных злоумышленников, чтобы обеспечить баланс конфиденциальности и веб-совместимости.</span><span class="sxs-lookup"><span data-stu-id="f1989-192">The default tracking prevention setting is Balanced mode, which blocks 3rd party trackers and known malicious trackers for an experience that balances privacy and web compatibility.</span></span>  <span data-ttu-id="f1989-193">Чтобы получить более подробную информацию о совместимости веб-страницы, если некоторые средства отслеживания заблокированы, мы также добавили предупреждающие сообщения на консоли, когда средство отслеживания заблокировано.</span><span class="sxs-lookup"><span data-stu-id="f1989-193">To give you more insight into the compatibility of your web page when certain trackers are blocked, we've also added warning messages in the Console when a tracker is blocked.</span></span>  

> ##### <span data-ttu-id="f1989-194">Рисунок9</span><span class="sxs-lookup"><span data-stu-id="f1989-194">Figure 9</span></span>  
> <span data-ttu-id="f1989-195">Сообщения на консоли, когда предотвращение отслеживания блокирует доступ к хранилищу для средства отслеживания</span><span class="sxs-lookup"><span data-stu-id="f1989-195">Messages in the Console when tracking prevention blocks access to storage for a tracker</span></span>  
> ![Сообщения на консоли, когда предотвращение отслеживания блокирует доступ к хранилищу для средства отслеживания][ImageTrackingPrevention]  

<span data-ttu-id="f1989-197">[Узнайте больше о предотвращении отслеживания и балансе между конфиденциальностью и веб-совместимостью][TrackingPrevention].</span><span class="sxs-lookup"><span data-stu-id="f1989-197">[Read more about tracking prevention and the balance between privacy and web compatibility][TrackingPrevention].</span></span>  

## <span data-ttu-id="f1989-198">Объявления из проекта Chromium</span><span class="sxs-lookup"><span data-stu-id="f1989-198">Announcements from the Chromium project</span></span>  

<span data-ttu-id="f1989-199">В следующих разделах описаны дополнительные возможности, доступные в Microsoft Edge 80, которые были задействованы в проекте Open Source Chromium.</span><span class="sxs-lookup"><span data-stu-id="f1989-199">The following sections announce additional features available in Microsoft Edge 80 that were contributed to the open source Chromium project.</span></span>  

### <span data-ttu-id="f1989-200">Поддержка повторной декларации Let и Class на консоли</span><span class="sxs-lookup"><span data-stu-id="f1989-200">Support for let and class redeclarations in the Console</span></span>  

<span data-ttu-id="f1989-201">Теперь консоль поддерживает повторное объявление `let` `class` операторов and.</span><span class="sxs-lookup"><span data-stu-id="f1989-201">The Console now supports redeclarations of `let` and `class` statements.</span></span>  <span data-ttu-id="f1989-202">Невозможность повторного объявления — это распространенный annoyance для веб-разработчиков, использующих консоль для экспериментов с новым кодом JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f1989-202">The inability to redeclare was a common annoyance for web developers who use the Console to experiment with new JavaScript code.</span></span>  

> [!WARNING]
> <span data-ttu-id="f1989-203">При повторном объявлении `let` `class` оператора или в сценарии, находящегося за пределами консоли или при вводе с помощью одного из входных данных в командной консоли возникает проблема `SyntaxError` .</span><span class="sxs-lookup"><span data-stu-id="f1989-203">Redeclaring a `let` or `class` statement in a script outside of the Console or within a single Console input still causes a `SyntaxError`.</span></span>  

<span data-ttu-id="f1989-204">Например, ранее при повторном объявлении локальной переменной `let` консоль вызвала ошибку:</span><span class="sxs-lookup"><span data-stu-id="f1989-204">For example, previously, when redeclaring a local variable with `let`, the Console threw an error:</span></span>  

> ##### <span data-ttu-id="f1989-205">Рисунок 10</span><span class="sxs-lookup"><span data-stu-id="f1989-205">Figure 10</span></span>  
> <span data-ttu-id="f1989-206">Консоль в Microsoft Edge 79 показывает, что повторное объявление Let не выполняется</span><span class="sxs-lookup"><span data-stu-id="f1989-206">The Console in Microsoft Edge 79 showing that the let redeclaration fails</span></span>  
> ![Консоль в Microsoft Edge 79 показывает, что повторное объявление Let не выполняется][ImageConsoleRedeclarationFails]  

<span data-ttu-id="f1989-208">Теперь консоль допускает повторное объявление:</span><span class="sxs-lookup"><span data-stu-id="f1989-208">Now, the Console allows the redeclaration:</span></span>  

> ##### <span data-ttu-id="f1989-209">Рисунок11</span><span class="sxs-lookup"><span data-stu-id="f1989-209">Figure 11</span></span>  
> <span data-ttu-id="f1989-210">Консоль в Microsoft Edge 80, на которой показано, что повторное объявление Let успешно.</span><span class="sxs-lookup"><span data-stu-id="f1989-210">The Console in Microsoft Edge 80 showing that the let redeclaration succeeds</span></span>  
> ![Консоль в Microsoft Edge 80, на которой показано, что повторное объявление Let успешно.][ImageConsoleRedeclarationSucceeds]  

<span data-ttu-id="f1989-212">[#1004193][crbug1004193] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="f1989-212">Chromium issue [#1004193][crbug1004193]</span></span>  

### <span data-ttu-id="f1989-213">Улучшенная Отладка сборок</span><span class="sxs-lookup"><span data-stu-id="f1989-213">Improved WebAssembly debugging</span></span>  

<span data-ttu-id="f1989-214">DevTools начал поддерживать [стандарт отладки dwarf][DwarfHome], что означает увеличение поддержки степпинга кода, установки точек останова и разрешения трассировки стека на исходном языке в DevTools.</span><span class="sxs-lookup"><span data-stu-id="f1989-214">DevTools has started to support the [DWARF Debugging Standard][DwarfHome], which means increased support for stepping over code, setting breakpoints, and resolving stack traces in your source languages within DevTools.</span></span>  

<!-- [TODO: Add this link back] -->  
<!--Check out [Improved WebAssembly debugging in Microsoft Edge DevTools][201912Webassembly] for the full story.  -->  

<!-- [TODO: Replace this image with screenshot in Edge] -->  
<!--
> ##### Figure  
> The new DWARF-powered WebAssembly debugging  
> ![The new DWARF-powered WebAssembly debugging][ImageDwarfPoweredWebAssemblyDebugging]  
-->  

### <span data-ttu-id="f1989-215">Обновления панели сети</span><span class="sxs-lookup"><span data-stu-id="f1989-215">Network panel updates</span></span>  

#### <span data-ttu-id="f1989-216">Цепочки инициаторов запросов на вкладке инициатора</span><span class="sxs-lookup"><span data-stu-id="f1989-216">Request Initiator Chains in the Initiator tab</span></span>  

<span data-ttu-id="f1989-217">Теперь вы можете просмотреть инициаторы и зависимости сетевого запроса как вложенный список.</span><span class="sxs-lookup"><span data-stu-id="f1989-217">You are now able to view the initiators and dependencies of a network request as a nested list.</span></span>  <span data-ttu-id="f1989-218">Это может помочь вам понять, почему был запрошен ресурс, а также о том, какая сетевая активность связана с определенным ресурсом (например, сценарием).</span><span class="sxs-lookup"><span data-stu-id="f1989-218">This may help you understand why a resource was requested, or what network activity a certain resource \(such as a script\) caused.</span></span>  

> ##### <span data-ttu-id="f1989-219">Рисунок12</span><span class="sxs-lookup"><span data-stu-id="f1989-219">Figure 12</span></span>  
> <span data-ttu-id="f1989-220">Цепочка инициаторов запросов на вкладке инициатора</span><span class="sxs-lookup"><span data-stu-id="f1989-220">A Request Initiator Chain in the Initiator tab</span></span>  
> ![Цепочка инициаторов запросов на вкладке инициатора][ImageRequestInitiatorChain]  

<span data-ttu-id="f1989-222">После [входа в сеть на панели Network (сеть][DevToolsNetworkIndex]) выберите ресурс и перейдите на вкладку **инициатор** , чтобы просмотреть **цепочку инициаторов запроса**.</span><span class="sxs-lookup"><span data-stu-id="f1989-222">After [logging network activity in the Network panel][DevToolsNetworkIndex], click a resource and then go to the **Initiator** tab to view the **Request Initiator Chain**:</span></span>  

*   <span data-ttu-id="f1989-223">**Проверенный ресурс** выделяется полужирным шрифтом.</span><span class="sxs-lookup"><span data-stu-id="f1989-223">The **inspected resource** is bold.</span></span>  <span data-ttu-id="f1989-224">На снимке экрана выше `ai.2.min.js` показан проверенный ресурс.</span><span class="sxs-lookup"><span data-stu-id="f1989-224">In the screenshot above, `ai.2.min.js` is the inspected resource.</span></span>  
*   <span data-ttu-id="f1989-225">Ресурсы, расположенные выше проверенного ресурса, являются **инициаторами**.</span><span class="sxs-lookup"><span data-stu-id="f1989-225">The resources above the inspected resource are the **initiators**.</span></span>  <span data-ttu-id="f1989-226">На снимке экрана выше `https://www.microsoftedgeinsider.com` — инициатор `ai.2.min.js` .</span><span class="sxs-lookup"><span data-stu-id="f1989-226">In the screenshot above, `https://www.microsoftedgeinsider.com` is the initiator of `ai.2.min.js`.</span></span>  <span data-ttu-id="f1989-227">Другими словами, `https://www.microsoftedgeinsider.com` это привело к сетевому запросу `ai.2.min.js` .</span><span class="sxs-lookup"><span data-stu-id="f1989-227">In other words, `https://www.microsoftedgeinsider.com` caused the network request for `ai.2.min.js`.</span></span>  
*   <span data-ttu-id="f1989-228">Ресурсы, расположенные под проверенным ресурсом, являются **зависимостями**.</span><span class="sxs-lookup"><span data-stu-id="f1989-228">The resources below the inspected resource are the **dependencies**.</span></span>  <span data-ttu-id="f1989-229">На снимке экрана выше `https://dc.services.visualstudio.com/v2/track` есть зависимость `ai.2.min.js` .</span><span class="sxs-lookup"><span data-stu-id="f1989-229">In the screenshot above, `https://dc.services.visualstudio.com/v2/track` is a dependency of `ai.2.min.js`.</span></span>  <span data-ttu-id="f1989-230">Другими словами, `ai.2.min.js` это привело к сетевому запросу `https://dc.services.visualstudio.com/v2/track` .</span><span class="sxs-lookup"><span data-stu-id="f1989-230">In other words, `ai.2.min.js` caused the network request for `https://dc.services.visualstudio.com/v2/track`.</span></span>  

> [!NOTE]
> <span data-ttu-id="f1989-231">Кроме того, можно получить доступ к сведениям об инициаторе и `Shift` наведении указателя мыши на ресурсы сети.</span><span class="sxs-lookup"><span data-stu-id="f1989-231">Initiator and dependency information may also be accessed by holding `Shift` and then hovering over network resources.</span></span>  <span data-ttu-id="f1989-232">Просмотр [инициаторов и зависимостей][DevToolsNetworkReferenceViewInitiatorsDependencies].</span><span class="sxs-lookup"><span data-stu-id="f1989-232">See [View initiators and dependencies][DevToolsNetworkReferenceViewInitiatorsDependencies].</span></span>  

<span data-ttu-id="f1989-233">[#842488][crbug842488] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="f1989-233">Chromium issue [#842488][crbug842488]</span></span>  

#### <span data-ttu-id="f1989-234">Выделение выбранного сетевого запроса в обзоре</span><span class="sxs-lookup"><span data-stu-id="f1989-234">Highlight the selected network request in the Overview</span></span>  

<span data-ttu-id="f1989-235">После выбора сетевого ресурса для его проверки на панели Network (сеть) размещается синяя рамка вокруг **ресурса.**</span><span class="sxs-lookup"><span data-stu-id="f1989-235">After you click a network resource in order to inspect it, the Network panel now puts a blue border around that resource in the **Overview**.</span></span>  <span data-ttu-id="f1989-236">Это поможет определить, является ли сетевой запрос более ранней или более поздней, чем ожидалось.</span><span class="sxs-lookup"><span data-stu-id="f1989-236">This is able to help you detect if the network request is happening earlier or later than expected.</span></span>  

> ##### <span data-ttu-id="f1989-237">Рисунок13</span><span class="sxs-lookup"><span data-stu-id="f1989-237">Figure 13</span></span>  
> <span data-ttu-id="f1989-238">Область "Обзор", в которой выделяются проверенные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f1989-238">The Overview pane highlighting the inspected resource</span></span>  
> ![Область "Обзор", в которой выделяются проверенные ресурсы][ImageOverviewPaneInspectedResource]  

<span data-ttu-id="f1989-240">[#988253][crbug988253] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="f1989-240">Chromium issue [#988253][crbug988253]</span></span>  

#### <span data-ttu-id="f1989-241">URL-адреса и столбцы "путь" на панели "сеть"</span><span class="sxs-lookup"><span data-stu-id="f1989-241">URL and path columns in the Network panel</span></span>  

<span data-ttu-id="f1989-242">С помощью столбцов «новый **путь** » и « **URL-адрес** » на панели **Network (сеть** ) можно просмотреть абсолютный путь к каждому СЕТЕВОМУ ресурсу или полный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="f1989-242">Use the new **Path** and **URL** columns in the **Network** panel to see the absolute path or full URL of each network resource.</span></span>  

> ##### <span data-ttu-id="f1989-243">Рисунок14</span><span class="sxs-lookup"><span data-stu-id="f1989-243">Figure 14</span></span>  
> <span data-ttu-id="f1989-244">Столбцы "новый путь" и "URL-адрес" на панели "сеть"</span><span class="sxs-lookup"><span data-stu-id="f1989-244">The new Path and URL columns in the Network panel</span></span>  
> ![Столбцы "новый путь" и "URL-адрес" на панели "сеть"][ImagePathNetworkPanel]  

<span data-ttu-id="f1989-246">Щелкните заголовок **каскадной** таблицы правой кнопкой мыши и выберите команду **путь** или **URL-адрес** , чтобы отобразить новые столбцы.</span><span class="sxs-lookup"><span data-stu-id="f1989-246">Right-click the **Waterfall** table header and select **Path** or **URL** to show the new columns.</span></span>  

<span data-ttu-id="f1989-247">[#993366][crbug993366] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="f1989-247">Chromium issue [#993366][crbug993366]</span></span>  

#### <span data-ttu-id="f1989-248">Обновлены строки агента пользователя</span><span class="sxs-lookup"><span data-stu-id="f1989-248">Updated User-Agent strings</span></span>  

<span data-ttu-id="f1989-249">DevTools поддерживает задание пользовательской строки агента пользователя на вкладке **условия сети** .  Строка агента пользователя влияет на `User-Agent` заголовок HTTP, подключенный к сетевым ресурсам, а также на значение `navigator.userAgent` .</span><span class="sxs-lookup"><span data-stu-id="f1989-249">DevTools supports setting a custom User-Agent string through the **Network Conditions** tab.  The User-Agent string affects the `User-Agent` HTTP header attached to network resources, and also the value of `navigator.userAgent`.</span></span>  

<span data-ttu-id="f1989-250">Предопределенные строки агента пользователя обновлены в соответствии с современными версиями браузера.</span><span class="sxs-lookup"><span data-stu-id="f1989-250">The predefined User-Agent strings have been updated to reflect modern browser versions.</span></span>  

> ##### <span data-ttu-id="f1989-251">Рисунок15</span><span class="sxs-lookup"><span data-stu-id="f1989-251">Figure 15</span></span>  
> <span data-ttu-id="f1989-252">Меню агента пользователя на вкладке "условия сети"</span><span class="sxs-lookup"><span data-stu-id="f1989-252">The User Agent menu in the Network Conditions tab</span></span>  
> ![Меню агента пользователя на вкладке "условия сети"][ImageUserAgentNetworkConditionsTab]  

<span data-ttu-id="f1989-254">Чтобы получить доступ к **сетевым условиям**, [откройте меню команд][DevToolsCommandMenuIndex] и выполните `Show Network Conditions` команду.</span><span class="sxs-lookup"><span data-stu-id="f1989-254">To access **Network Conditions**, [open the Command Menu][DevToolsCommandMenuIndex] and run the `Show Network Conditions` command.</span></span>  

> [!NOTE]
> <span data-ttu-id="f1989-255">Вы также можете [задать строки агента пользователя в режиме устройства][DevToolsDeviceModeIndex].</span><span class="sxs-lookup"><span data-stu-id="f1989-255">You may also [set User-Agent strings in Device Mode][DevToolsDeviceModeIndex].</span></span>  

<span data-ttu-id="f1989-256">[#1029031][crbug1029031] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="f1989-256">Chromium issue [#1029031][crbug1029031]</span></span>  

### <span data-ttu-id="f1989-257">Обновления панели аудита</span><span class="sxs-lookup"><span data-stu-id="f1989-257">Audits panel updates</span></span>  

#### <span data-ttu-id="f1989-258">Новый пользовательский интерфейс конфигурации</span><span class="sxs-lookup"><span data-stu-id="f1989-258">New configuration UI</span></span>  

<span data-ttu-id="f1989-259">Пользовательский интерфейс конфигурации имеет новый, реагирующий дизайн и параметры конфигурации регулирования были упрощены.</span><span class="sxs-lookup"><span data-stu-id="f1989-259">The configuration UI has a new, responsive design, and the throttling configuration options have been simplified.</span></span>  <span data-ttu-id="f1989-260">Дополнительные сведения об изменении пользовательского интерфейса для регулирования приведены в разделе [Аудит][GitHubGoogleChromeDevToolsAuditsPanelThrottling] .</span><span class="sxs-lookup"><span data-stu-id="f1989-260">See [Audits Panel Throttling][GitHubGoogleChromeDevToolsAuditsPanelThrottling] for more information on the throttling UI changes.</span></span>  

> ##### <span data-ttu-id="f1989-261">Рисунок16</span><span class="sxs-lookup"><span data-stu-id="f1989-261">Figure 16</span></span>  
> <span data-ttu-id="f1989-262">Новый пользовательский интерфейс конфигурации</span><span class="sxs-lookup"><span data-stu-id="f1989-262">The new configuration UI</span></span>  
> ![Новый пользовательский интерфейс конфигурации][ImageConfigurationUI]  

### <span data-ttu-id="f1989-264">Обновления вкладок покрытия</span><span class="sxs-lookup"><span data-stu-id="f1989-264">Coverage tab updates</span></span>  

#### <span data-ttu-id="f1989-265">Режимы покрытия для отдельных функций или отдельных блоков</span><span class="sxs-lookup"><span data-stu-id="f1989-265">Per-function or per-block coverage modes</span></span>  

<span data-ttu-id="f1989-266">На [вкладке Coverage][DevToolsCoverageIndex] имеется новое раскрывающееся меню, в котором можно указать, нужно ли собирать данные о покрытии кода **для одной функции** или **для каждого блока**.</span><span class="sxs-lookup"><span data-stu-id="f1989-266">The [Coverage tab][DevToolsCoverageIndex] has a new dropdown menu that lets you specify whether code coverage data should be collected **per function** or **per block**.</span></span>  <span data-ttu-id="f1989-267">Покрытие **за блоком** является более подробным, но и более затратным для сбора.</span><span class="sxs-lookup"><span data-stu-id="f1989-267">**Per block** coverage is more detailed but also far more expensive to collect.</span></span>  <span data-ttu-id="f1989-268">DevTools по умолчанию использует **функцию на уровне отдельных функций** .</span><span class="sxs-lookup"><span data-stu-id="f1989-268">DevTools uses **per function** coverage by default now.</span></span>  

> [!CAUTION]
> <span data-ttu-id="f1989-269">В зависимости от того, используется ли **функция** **или режим, в HTML** -файлах могут возблюдаться большие различия в покрытии кода.</span><span class="sxs-lookup"><span data-stu-id="f1989-269">You may see large code coverage differences in HTML files depending on whether you use **per function** or **per block** mode.</span></span>  <span data-ttu-id="f1989-270">При использовании режима " **на функцию** " встроенные сценарии в HTML-файлах рассматриваются как функции.</span><span class="sxs-lookup"><span data-stu-id="f1989-270">When using **per function** mode, inline scripts in HTML files are treated as functions.</span></span>  <span data-ttu-id="f1989-271">Если сценарий выполняется, DevTools помечает весь сценарий как использованный код.</span><span class="sxs-lookup"><span data-stu-id="f1989-271">If the script runs at all then DevTools marks the entire script as used code.</span></span>  <span data-ttu-id="f1989-272">Если сценарий не выполняется вообще, DevTools помечает сценарий как неиспользуемый код.</span><span class="sxs-lookup"><span data-stu-id="f1989-272">Only if the script does not run at all does DevTools mark the script as unused code.</span></span>  

> ##### <span data-ttu-id="f1989-273">Рисунок17</span><span class="sxs-lookup"><span data-stu-id="f1989-273">Figure 17</span></span>  
> <span data-ttu-id="f1989-274">Раскрывающееся меню «режим покрытия»</span><span class="sxs-lookup"><span data-stu-id="f1989-274">The coverage mode dropdown menu</span></span>  
> ![Раскрывающееся меню «режим покрытия»][ImageCoverageMode]  

#### <span data-ttu-id="f1989-276">Теперь покрытие должно быть инициировано перезагрузкой страницы</span><span class="sxs-lookup"><span data-stu-id="f1989-276">Coverage must now be initiated by a page reload</span></span>  

<span data-ttu-id="f1989-277">Переключение покрытия кода без повторной загрузки страницы удалено, так как данные о покрытии были ненадежны.</span><span class="sxs-lookup"><span data-stu-id="f1989-277">Toggling code coverage without a page reload has been removed because the coverage data was unreliable.</span></span>  <span data-ttu-id="f1989-278">Например, функция может быть указана как неиспользуемая, если среда выполнения была длиннее давно, а сборщик мусора V8 удалил его.</span><span class="sxs-lookup"><span data-stu-id="f1989-278">For example, a function may be reported as unused if the runtime was a long time ago and the V8 garbage collector has cleaned it up.</span></span>  

<span data-ttu-id="f1989-279">[#1004203][crbug1004203] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="f1989-279">Chromium issue [#1004203][crbug1004203]</span></span>  

## <span data-ttu-id="f1989-280">Загрузка каналов предварительной версии Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="f1989-280">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="f1989-281">Если вы используете Windows или macOS, рассматривайте в качестве браузера по умолчанию использование [каналов предварительного просмотра Microsoft Edge][MicrosoftEdgePreviewChannels] .</span><span class="sxs-lookup"><span data-stu-id="f1989-281">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="f1989-282">Каналы предварительного просмотра предоставляют доступ к последним функциям DevTools.</span><span class="sxs-lookup"><span data-stu-id="f1989-282">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="f1989-283">Знакомство с Microsoft Edge DevTools Team</span><span class="sxs-lookup"><span data-stu-id="f1989-283">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!--<<../../_shared/devtools-feedback.md>> -->

<!--<<../../_shared/canary.md>> -->

<!--<<../../_shared/discover.md>> -->

<!-- image links -->  

[ImagePerformanceToolKeyboardReaderImprovements]: ../../images/2019/12/a11y-performance-tool.msft.gif "Рисунок 1: средство "производительность" в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана"  
[ImageLocalizedGerman]: ../../images/2019/12/localized-devtools.msft.png "Рисунок 2: DevTools на немецком языке"  
[ImageHintsTabWebhintExtension]: ../../images/2019/12/webhint-browser-extension.msft.png "Рисунок 3: вкладка "Подсказка" в Microsoft Edge DevTools, когда установлено расширение браузера веб."  
[Image3DView]: ../../images/2019/12/3dview.msft.png "Рисунок 4:3D-представление в Microsoft Edge DevTools"  
[ImageElementsVisualStudioCode]: ../../images/2019/12/elements-for-edge.msft.png "Рисунок 5. инструмент "элементы" в коде VS с использованием элементов для расширения Microsoft Edge"  
[ImageDebuggerExtensionVisualStudioCode]: ../../images/2019/12/vscode-debugger.msft.png "Рисунок 6: отладчик для расширения Microsoft EDGE в коде VS"  
[ImageWebhintVisualStudioCodeExtensionWorkspace]: ../../images/2019/12/webhint-vscode-extension.msft.png "Рис. 7: расширение веб-подсказки и кода анализ целевого файла в коде VS"  
[ImageVisualStudioLaunchWebApp]: ../../images/2019/12/vs.msft.png "Рисунок 8: Visual Studio с возможностью запуска вашего веб-приложения в Microsoft Edge Канарские, dev или Beta"  
[ImageTrackingPrevention]: ../../images/2019/12/tracking-prevention.msft.png "Рис. 9: сообщения на консоли, когда предотвращение отслеживания блокирует доступ к хранилищу для средства отслеживания."  
[ImageConsoleRedeclarationFails]: ../../images/2019/12/letbefore.msft.png "Рис. 10: консоль в Microsoft Edge 79 показывает, что повторное объявление Let не выполняется"  
[ImageConsoleRedeclarationSucceeds]: ../../images/2019/12/letafter.msft.png "На рисунке 11: консоль в Microsoft Edge 80 показывает, что повторное объявление Let успешно."  
[ImageRequestInitiatorChain]: ../../images/2019/12/initiators.msft.png "Рисунок 12: цепочка инициаторов запросов на вкладке инициатора"  
[ImageOverviewPaneInspectedResource]: ../../images/2019/12/overview.msft.png "Рисунок 13: область "Обзор", в которой выделяются проверенные ресурсы"  
[ImagePathNetworkPanel]: ../../images/2019/12/columns.msft.png "Рисунок 14: столбцы "новый путь" и "URL-адрес" на панели "сеть""  
[ImageUserAgentNetworkConditionsTab]: ../../images/2019/12/useragent.msft.png "Рисунок 15: меню агента пользователя на вкладке условия сети"  
[ImageConfigurationUI]: ../../images/2019/12/start.msft.png "Рисунок 16: новый пользовательский интерфейс конфигурации"  
[ImageCoverageMode]: ../../images/2019/12/modes.msft.png "Рисунок 17: раскрывающееся меню «режим покрытия»"  

<!--[ImageDwarfPoweredWebAssemblyDebugging]: ../../images/2019/12/wasm.msft.png "Figure: The new DWARF-powered WebAssembly debugging"  -->

<!-- links -->  

[DevToolsCommandMenuIndex]: ../../../command-menu/index.md "Выполнение команд с помощью командного меню Microsoft Edge DevTools"  
[DevToolsCoverageIndex]: ../../../coverage/index.md "Поиск неиспользуемых кодов JavaScript и CSS с помощью вкладки "покрытие" в Microsoft Edge DevTools"  
[DevToolsDeviceModeIndex]: ../../../device-mode/index.md#simulate-a-mobile-viewport "Имитация мобильного просмотра экрана — Эмуляция мобильных устройств с помощью режима устройства в Microsoft Edge DevTools"  
[DevToolsNetworkIndex]: ../../../network/index.md "Проверка активности сети в Microsoft Edge DevTools"  
[DevToolsNetworkReferenceViewInitiatorsDependencies]: ../../../network/reference.md#view-initiators-and-dependencies "Просмотр инициаторов и зависимостей — справочные материалы по анализу сети"  
[DevGuideEdgeHtmlWhatsNew]: ../../../../dev-guide/whats-new.md "Новые возможности EdgeHTML"  
[VisualStudioCodeDebuggerEdgeExtension]: ../../../../visual-studio-code/debugger-for-edge.md "Отладчик для расширения кода Microsoft Edge VS"  
[VisualStudioCodeElementEdgeExtension]: ../../../../visual-studio-code/elements-for-edge.md "Элементы расширений Microsoft EDGE и кода"  

<!--  [201912Webassembly]: webassembly.md "Improved WebAssembly debugging in Microsoft Edge DevTools"  -->  

[crbug842488]: https://crbug.com/842488 "842488 — Добавление поля инициатора на вкладку заголовки — Monorail"  
[crbug988253]: https://crbug.com/988253 "988253 — ошибка DevTools — отсутствует связь между сетевым запросом и графом временной шкалы — Monorail"  
[crbug993366]: https://crbug.com/993366 "993366 — часть URL-адреса в списке запросов на панели "сеть" — monorail."  
[crbug1004193]: https://crbug.com/1004193 "1004193-режим REPL для V8-Monorail"  
[crbug1004203]: https://crbug.com/1004203 "1004203-Monorail"  
[crbug1029031]: https://crbug.com/1029031 "Строки 1029031-UA устарели — Monorail" 
[crbug963183]: https://crbug.com/963183 "963183-DevTools не соответствуют требованиям WCAG"
[crbug941561]: https://crbug.com/941561 "941561 – локализуемость DevTools"
[crbug987787]: https://crbug.com/987787 "987787 – трехмерный вид DOM"

[AccessibilityInsights]: https://aka.ms/a11yinsights "Аналитические сведения о специальных возможностях"  

[DwarfHome]: https://dwarfstd.org "Домашняя страница dwarf"  
[GitHubGoogleChromeDevToolsAuditsPanelThrottling]: https://github.com/GoogleChrome/lighthouse/blob/master/docs/throttling.md#devtools-audits-panel-throttling "DevTools ' Аудит регулирования панели — GoogleChrome/Lighthouse | GitHub"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Новая ошибка — MicrosoftDocs/Edge-разработчик"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Каналы предварительной версии Microsoft Edge"  
[MicrosoftEdgeInsiderAddons]: https://aka.ms/webhint/edge-extension "Надстройки Microsoft Edge для участников программы предварительной оценки"  
[MicrosoftVisualStudio]: https://aka.ms/vs "Visual Studio"  
[MicrosoftVisualStudioBlogDebugJavascript]: https://aka.ms/vs/debug-edge "Отладка JavaScript в Microsoft Edge из Visual Studio | Блог Visual Studio"  
[MicrosoftVisualStudioDownloads]: https://aka.ms/vs/download "Скачайте Visual Studio 2019 для Windows \ & Mac"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Объектная модель документов (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "z-индекс | MDN"  
[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Публикация твита"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools учетной записи Twitter"
[VisualStudioCode]: https://aka.ms/vscode "Код Visual Studio"  
[VisualStudioMarketplaceDebuggerEdge]: https://aka.ms/debugger4code "Отладчик для Microsoft Edge-Visual Studio Marketplace"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://aka.ms/elements4code "Элементы для Microsoft Edge \ (Chromium \) — Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://aka.ms/webhint4code ""Подсказка" — Visual Studio Marketplace"
[Webhint]: https://aka.ms/webhint "Подсказка"  
[WebhintBrowserExtension]: https://aka.ms/webhint/browser-extension "Расширение браузеров веб – подсказок | Документация по подсказкам"  
[WebhintVisualStudioCodeExtension]: https://aka.ms/webhint/code-extension "Расширение ссылки и кода Документация по подсказкам"  
[TrackingPrevention]: https://aka.ms/microsoftedge/tracking-prevention-blog "Улучшение защиты от слежения в блоге Microsoft Edge"
[TheWebWeWant]: https://aka.ms/webwewant "Требуемый веб-сайт"

> [!NOTE]
> <span data-ttu-id="f1989-340">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f1989-340">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="f1989-341">Исходная страница будет найдена [здесь](https://developers.google.com/web/updates/2019/12/devtools/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="f1989-341">The original page is found [here](https://developers.google.com/web/updates/2019/12/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="f1989-343">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="f1989-343">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
