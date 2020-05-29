---
title: Новые возможности DevTools (Microsoft Edge 80)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/20/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: ac85f0d9f8a5f112e702968b9c0aeceb05312ac1
ms.sourcegitcommit: 7e3a876ccb1f0ff3d50d4e32f03af98f780e2930
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/24/2020
ms.locfileid: "10591396"
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








# <span data-ttu-id="9185e-103">Новые возможности DevTools (Microsoft Edge 80)</span><span class="sxs-lookup"><span data-stu-id="9185e-103">What's new in DevTools (Microsoft Edge 80)</span></span>   



## <span data-ttu-id="9185e-104">Объявления из группы Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="9185e-104">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="9185e-105">В следующих разделах представлен список извещений, которые вы могли не получить в Microsoft Edge DevTools Teams!</span><span class="sxs-lookup"><span data-stu-id="9185e-105">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team!</span></span> <span data-ttu-id="9185e-106">Узнайте, как использовать новые функции в DevTools, расширения кода VS и многое другое.</span><span class="sxs-lookup"><span data-stu-id="9185e-106">Check them out to try new features in the DevTools, VS Code extensions, and more.</span></span>  <span data-ttu-id="9185e-107">Чтобы оставаться на связи с самыми последними и более свежими возможностями, скачайте на веб – [каналы предварительной версии Microsoft Edge][MicrosoftEdgePreviewChannels] и [следуйте указаниям Twitter][EdgeDevToolsTwitterAccount].</span><span class="sxs-lookup"><span data-stu-id="9185e-107">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <span data-ttu-id="9185e-108">Улучшение специальных возможностей в DevTools</span><span class="sxs-lookup"><span data-stu-id="9185e-108">Accessibility improvements to the DevTools</span></span>  

<span data-ttu-id="9185e-109">Группа DevTools изменила 170 в Chromium для устранения проблем с высокой контрастностью цвета, клавиатуры и средства чтения с экрана в DevTools.</span><span class="sxs-lookup"><span data-stu-id="9185e-109">The DevTools team has contributed 170 changes to Chromium to address high-impact color contrast, keyboard, and screen reader issues in the DevTools.</span></span>  <span data-ttu-id="9185e-110">Каждый разработчик, создающий веб-сайт, должен иметь возможность использовать DevTools.</span><span class="sxs-lookup"><span data-stu-id="9185e-110">Every developer building the web should be able to use the DevTools.</span></span>  

> ##### <span data-ttu-id="9185e-111">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="9185e-111">Figure 1</span></span>  
> <span data-ttu-id="9185e-112">Средство "производительность" в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана</span><span class="sxs-lookup"><span data-stu-id="9185e-112">The Performance tool in the DevTools with the keyboard navigation and screen reader improvements</span></span>  
> ![Средство "производительность" в DevTools с улучшенной навигацией с помощью клавиатуры и средства чтения с экрана][ImagePerformanceToolKeyboardReaderImprovements]  

<span data-ttu-id="9185e-114">Сведения о том, как сделать веб-страницу доступной для всех пользователей?</span><span class="sxs-lookup"><span data-stu-id="9185e-114">Want to learn how to make your web page accessible to all of your users?</span></span>  <span data-ttu-id="9185e-115">Скачайте [расширения для][WebhintBrowserExtension] Microsoft Edge " [Специальные возможности][AccessibilityInsights] ", чтобы приступить к работе.</span><span class="sxs-lookup"><span data-stu-id="9185e-115">Download the [Accessibility Insights][AccessibilityInsights] and [webhint][WebhintBrowserExtension] extensions for Microsoft Edge to get started.</span></span>  

<span data-ttu-id="9185e-116">Если вы используете средства чтения с экрана или клавиатуру для навигации по DevTools, отправьте нам свой отзыв, выполнив [твит][PostTweetEdgeDevTools] в США или щелкнув значок [отзыва](#feedback) .</span><span class="sxs-lookup"><span data-stu-id="9185e-116">If you use screen readers or the keyboard to navigate around the DevTools, send us your feedback by [tweeting][PostTweetEdgeDevTools] at us or clicking the [Feedback](#feedback) icon!</span></span>  

<span data-ttu-id="9185e-117">[#963183][crbug963183] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="9185e-117">Chromium issue [#963183][crbug963183]</span></span>  

### <span data-ttu-id="9185e-118">Использование DevTools на других языках</span><span class="sxs-lookup"><span data-stu-id="9185e-118">Using the DevTools in other languages</span></span>  

<span data-ttu-id="9185e-119">Многие разработчики используют другие инструменты разработчика, такие как StackOverflow и код VS, на родном языке, а не только на английском языке.</span><span class="sxs-lookup"><span data-stu-id="9185e-119">Many developers use other developer tools, like StackOverflow and VS Code, in their native language, not just in English.</span></span>  <span data-ttu-id="9185e-120">Мы рады объявить локализацию для DevTools, который теперь вы можете использовать на одном из 10 языков, кроме английского.</span><span class="sxs-lookup"><span data-stu-id="9185e-120">We’re excited to announce localization for the DevTools, which you are now able to use in one of 10 languages besides English:</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="9185e-121">Китайский (упрощенное письмо) —  &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span><span class="sxs-lookup"><span data-stu-id="9185e-121">Chinese \(Simplified\) - &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="9185e-122">Китайский (традиционное письмо) —  &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span><span class="sxs-lookup"><span data-stu-id="9185e-122">Chinese \(Traditional\) - &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="9185e-123">Французский — Fran&#231;AIS</span><span class="sxs-lookup"><span data-stu-id="9185e-123">French – fran&#231;ais</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="9185e-124">Немецкий — Deutsch</span><span class="sxs-lookup"><span data-stu-id="9185e-124">German - deutsch</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="9185e-125">Итальянский — Italiano</span><span class="sxs-lookup"><span data-stu-id="9185e-125">Italian - italiano</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="9185e-126">Японская  &#26085;&#26412;&#35486;</span><span class="sxs-lookup"><span data-stu-id="9185e-126">Japanese - &#26085;&#26412;&#35486;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="9185e-127">Корейский —  &#54620;&#44397;&#50612;</span><span class="sxs-lookup"><span data-stu-id="9185e-127">Korean - &#54620;&#44397;&#50612;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="9185e-128">Португальский (portugu&#234;s)</span><span class="sxs-lookup"><span data-stu-id="9185e-128">Portuguese - portugu&#234;s</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="9185e-129">Русский —  &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span><span class="sxs-lookup"><span data-stu-id="9185e-129">Russian – &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="9185e-130">Испанская — ESPA&#241;OL</span><span class="sxs-lookup"><span data-stu-id="9185e-130">Spanish - espa&#241;ol</span></span>
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

<span data-ttu-id="9185e-131">Перейдите к разделу `edge://flags` **Включение локализованных средств разработчика** в состояние **включено**и установите для него флажок Включить.</span><span class="sxs-lookup"><span data-stu-id="9185e-131">Navigate to `edge://flags` and set the **Enable localized Developer Tools** flag to **Enabled**.</span></span>  <span data-ttu-id="9185e-132">Также установите флажок **эксперименты со средствами разработчика** для **включения**.</span><span class="sxs-lookup"><span data-stu-id="9185e-132">Also set the **Developer Tools experiments** flag to **Enabled**.</span></span>  <span data-ttu-id="9185e-133">Перезапустите Microsoft EDGE и откройте DevTools.</span><span class="sxs-lookup"><span data-stu-id="9185e-133">Restart Microsoft Edge and open the DevTools.</span></span>  <!-- Press `F1` in the DevTools or go to Settings > Experiments and check the **Match browser language** checkbox.  -->  <span data-ttu-id="9185e-134">DevTools соответствует языку, используемому в Microsoft Edge in `edge://settings/languages` .</span><span class="sxs-lookup"><span data-stu-id="9185e-134">The DevTools match the language you use for Microsoft Edge in `edge://settings/languages`.</span></span>  

> ##### <span data-ttu-id="9185e-135">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="9185e-135">Figure 2</span></span>  
> <span data-ttu-id="9185e-136">DevTools на немецком языке</span><span class="sxs-lookup"><span data-stu-id="9185e-136">The DevTools in German</span></span>  
> ![DevTools на немецком языке][ImageLocalizedGerman]  

<span data-ttu-id="9185e-138">Если вы хотите использовать DevTools на языке, отличном от того, на котором они доступны, [твит][PostTweetEdgeDevTools] в США или щелкните значок [отзыва](#feedback) .</span><span class="sxs-lookup"><span data-stu-id="9185e-138">If you want to use the DevTools in a different language than the ones that are available, [tweet][PostTweetEdgeDevTools] at us or click the [Feedback](#feedback) icon.</span></span>  

<span data-ttu-id="9185e-139">[#941561][crbug941561] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="9185e-139">Chromium issue [#941561][crbug941561]</span></span>  

### <span data-ttu-id="9185e-140">Веб – подсказка с расширением Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9185e-140">webhint Microsoft Edge extension</span></span>  

<span data-ttu-id="9185e-141">Расширение веб-подсказки Microsoft EDGE позволяет легко находить и получать отзывы о специальных возможностях, совместимости с браузерами, безопасности, производительности и других средствах в DevTools.</span><span class="sxs-lookup"><span data-stu-id="9185e-141">The webhint Microsoft Edge extension allows you to easily scan your web page and get feedback on accessibility, browser compatibility, security, performance, and more within the DevTools.</span></span>  <span data-ttu-id="9185e-142">Узнайте больше о [https://webhint.io][Webhint] .</span><span class="sxs-lookup"><span data-stu-id="9185e-142">Read more at [https://webhint.io][Webhint].</span></span>  

> ##### <span data-ttu-id="9185e-143">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="9185e-143">Figure 3</span></span>  
> <span data-ttu-id="9185e-144">Вкладка "Подсказка" в DevTools, если установлено расширение браузера веб.</span><span class="sxs-lookup"><span data-stu-id="9185e-144">The Hints tab in the DevTools when the webhint browser extension is installed</span></span>  
> ![Вкладка "Подсказка" в DevTools, если установлено расширение браузера веб.][ImageHintsTabWebhintExtension]  

<span data-ttu-id="9185e-146">[Попробуйте расширение браузера веб для подсказки в Microsoft Edge][MicrosoftEdgeInsiderAddons].</span><span class="sxs-lookup"><span data-stu-id="9185e-146">[Try the webhint browser extension in Microsoft Edge][MicrosoftEdgeInsiderAddons].</span></span>  <span data-ttu-id="9185e-147">После установки расширения откройте DevTools и перейдите на вкладку подсказки.  В этой статье запустите настраиваемое сканирование сайта.</span><span class="sxs-lookup"><span data-stu-id="9185e-147">Once you install the extension, open the DevTools and select the Hints tab.  From here, run a customizable site scan.</span></span>  <span data-ttu-id="9185e-148">Чтобы получить дополнительные сведения, [заwebhint.IO][WebhintBrowserExtension] в голову.</span><span class="sxs-lookup"><span data-stu-id="9185e-148">Head over to [webhint.io][WebhintBrowserExtension] to learn more.</span></span>

### <span data-ttu-id="9185e-149">Трехмерное представление</span><span class="sxs-lookup"><span data-stu-id="9185e-149">3D View</span></span>  

<span data-ttu-id="9185e-150">С помощью **трехмерного представления** вы можете выполнять отладку своего веб-приложения, перемещаясь по [объектной модели документов \ (DOM)][MDNDocumentObjectModel] или контексту стека [z-индексов][MDNZIndex] .</span><span class="sxs-lookup"><span data-stu-id="9185e-150">Use the **3D View** to debug your web application by navigating through the [Document Object Model \(DOM\)][MDNDocumentObjectModel] or the [z-index][MDNZIndex] stacking context.</span></span>  

> ##### <span data-ttu-id="9185e-151">Рисунок4</span><span class="sxs-lookup"><span data-stu-id="9185e-151">Figure 4</span></span>  
> <span data-ttu-id="9185e-152">Трехмерное представление в DevTools</span><span class="sxs-lookup"><span data-stu-id="9185e-152">The 3D View in the DevTools</span></span>  
> ![Трехмерное представление в DevTools][Image3DView]  

<span data-ttu-id="9185e-154">Чтобы получить доступ к трехмерному представлению, перейдите в раздел `edge://flags` и убедитесь, что флаг **эксперименты со средствами разработчика** установлен в **разрешено**.</span><span class="sxs-lookup"><span data-stu-id="9185e-154">To access the 3D View, navigate to `edge://flags` and ensure that the **Developer Tools experiments** flag is set to **Enabled**.</span></span>  <span data-ttu-id="9185e-155">Перезапустите Microsoft EDGE и откройте DevTools.</span><span class="sxs-lookup"><span data-stu-id="9185e-155">Restart Microsoft Edge and open the DevTools.</span></span>  <span data-ttu-id="9185e-156">Нажмите кнопку `F1` DevTools или выберите **Параметры**, перейдите к разделу " **эксперименты** " и установите флажок **включить трехмерное представление** .</span><span class="sxs-lookup"><span data-stu-id="9185e-156">Press `F1` in the DevTools or go to **Settings**, navigate to **Experiments** section, and check the **Enable 3D View** checkbox.</span></span>  <span data-ttu-id="9185e-157">Теперь нажмите клавишу `Ctrl`  +  `Shift`  +  `P` Ввод в **3D-представление** и выберите **Показать 3D-представление**.</span><span class="sxs-lookup"><span data-stu-id="9185e-157">Now, press `Ctrl` + `Shift` + `P`, type in **3D View** and select **Show 3D View**.</span></span>  

<span data-ttu-id="9185e-158">Мы работаем над ИНТЕРФЕЙСом и добавляем дополнительные функции в представление 3D, поэтому отправьте нам свой [отзыв](#feedback).</span><span class="sxs-lookup"><span data-stu-id="9185e-158">We're working on the UI and adding more functionality to the 3D View so please send us your [feedback](#feedback).</span></span>  

<span data-ttu-id="9185e-159">[#987787][crbug987787] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="9185e-159">Chromium issue [#987787][crbug987787]</span></span>

### <span data-ttu-id="9185e-160">Расширения кода Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9185e-160">Visual Studio Code extensions</span></span>  

<span data-ttu-id="9185e-161">Кроме того, Группа DevTools также выпустила некоторые расширения для [кода Visual Studio \ (код VS)][VisualStudioCode] , которые позволяют использовать возможности DevTools прямо из текстового редактора.</span><span class="sxs-lookup"><span data-stu-id="9185e-161">The DevTools team has also released some extensions for [Visual Studio Code \(VS Code\)][VisualStudioCode] that let you use the power of the DevTools directly from your text editor!</span></span> <span data-ttu-id="9185e-162">Ознакомьтесь с приведенными ниже расширениями.</span><span class="sxs-lookup"><span data-stu-id="9185e-162">Check out the extensions below:</span></span>  

#### <span data-ttu-id="9185e-163">Элементы Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9185e-163">Elements for Microsoft Edge</span></span>  

<span data-ttu-id="9185e-164">С помощью инструмента "элементы" в коде VS добавьте [элементы для расширения кода Microsoft Edge \ (Chromium \)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] vs.</span><span class="sxs-lookup"><span data-stu-id="9185e-164">Use the Elements tool from within VS Code by adding the [Elements for Microsoft Edge \(Chromium\)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] VS Code extension.</span></span>  

> ##### <span data-ttu-id="9185e-165">Рисунок 5</span><span class="sxs-lookup"><span data-stu-id="9185e-165">Figure 5</span></span>  
> <span data-ttu-id="9185e-166">Инструмент "элементы" в коде VS с использованием элементов для расширения Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9185e-166">The Elements tool in VS Code using the Elements for Microsoft Edge extension</span></span>  
> ![Инструмент "элементы" в коде VS с использованием элементов для расширения Microsoft Edge][ImageElementsVisualStudioCode]  

<span data-ttu-id="9185e-168">Для получения дополнительных сведений изучите [элементы для расширения кода Microsoft Edge VS][VisualStudioCodeElementEdgeExtension].</span><span class="sxs-lookup"><span data-stu-id="9185e-168">For more information, check out [Elements for Microsoft Edge VS Code extension][VisualStudioCodeElementEdgeExtension].</span></span>  

#### <span data-ttu-id="9185e-169">Отладчик для Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9185e-169">Debugger for Microsoft Edge</span></span>  

<span data-ttu-id="9185e-170">С помощью [отладчика для расширения кода Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] , Отладка JavaScript выполняется в Microsoft Edge прямо из кода vs.</span><span class="sxs-lookup"><span data-stu-id="9185e-170">With the [Debugger for Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] VS Code extension, debug JavaScript running in Microsoft Edge directly from VS Code!</span></span>  

> ##### <span data-ttu-id="9185e-171">Рисунок6</span><span class="sxs-lookup"><span data-stu-id="9185e-171">Figure 6</span></span>  
> <span data-ttu-id="9185e-172">Отладчик для расширения Microsoft EDGE в коде VS</span><span class="sxs-lookup"><span data-stu-id="9185e-172">The Debugger for Microsoft Edge Extension in VS Code</span></span>  
> ![Отладчик для расширения Microsoft EDGE в коде VS][ImageDebuggerExtensionVisualStudioCode]  

<span data-ttu-id="9185e-174">Дополнительные сведения [об отладке Microsoft Edge из кода VS можно][VisualStudioCodeDebuggerEdgeExtension]найти здесь.</span><span class="sxs-lookup"><span data-stu-id="9185e-174">For more information, check out [how to debug Microsoft Edge from VS Code][VisualStudioCodeDebuggerEdgeExtension].</span></span>  

#### <span data-ttu-id="9185e-175">Подсказка</span><span class="sxs-lookup"><span data-stu-id="9185e-175">webhint</span></span>  

<span data-ttu-id="9185e-176">Расширение веб- [подсказки][VisualStudioMarketplaceWebhintExtension] и кода используются `webhint` для усовершенствования своей страницы, пока вы пишете ее!</span><span class="sxs-lookup"><span data-stu-id="9185e-176">The [webhint][VisualStudioMarketplaceWebhintExtension] VS Code extension uses `webhint` to improve your web page while you're writing it!</span></span> <span data-ttu-id="9185e-177">Это расширение запускает и сообщает диагностику файлов рабочей области на основе `webhint` анализа.</span><span class="sxs-lookup"><span data-stu-id="9185e-177">This extension runs and reports diagnostics on your workspace files based on `webhint` analysis.</span></span>  

> ##### <span data-ttu-id="9185e-178">Рисунок7</span><span class="sxs-lookup"><span data-stu-id="9185e-178">Figure 7</span></span>  
> <span data-ttu-id="9185e-179">Анализ файла и расширения кода веб-подсказки в коде VS</span><span class="sxs-lookup"><span data-stu-id="9185e-179">The webhint VS Code extension analyzing a .tsx file in VS Code</span></span>  
> ![Анализ файла и расширения кода веб-подсказки в коде VS][ImageWebhintVisualStudioCodeExtensionWorkspace]  

<span data-ttu-id="9185e-181">[Узнайте больше о расширении подсказки кода VS][WebhintVisualStudioCodeExtension].</span><span class="sxs-lookup"><span data-stu-id="9185e-181">[Learn more about the VS Code webhint extension][WebhintVisualStudioCodeExtension].</span></span>  

### <span data-ttu-id="9185e-182">Интеграция с Visual Studio</span><span class="sxs-lookup"><span data-stu-id="9185e-182">Visual Studio integration</span></span>
<span data-ttu-id="9185e-183">В Visual Studio 2019 версии 16,2 или более поздней Используйте отладчик Visual Studio для отладки JavaScript, который выполняется в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="9185e-183">In Visual Studio 2019 version 16.2 or later, use the Visual Studio debugger to debug JavaScript running in Microsoft Edge.</span></span>  <span data-ttu-id="9185e-184">[Загрузите Visual Studio 2019][MicrosoftVisualStudioDownloads] , чтобы попробовать эту функцию!</span><span class="sxs-lookup"><span data-stu-id="9185e-184">[Download Visual Studio 2019][MicrosoftVisualStudioDownloads] to try this feature out!</span></span>  

> ##### <span data-ttu-id="9185e-185">Рисунок8</span><span class="sxs-lookup"><span data-stu-id="9185e-185">Figure 8</span></span>  
> <span data-ttu-id="9185e-186">Visual Studio с возможностью запуска веб-приложения в Microsoft Edge Канарские, dev или Beta</span><span class="sxs-lookup"><span data-stu-id="9185e-186">Visual Studio with the option to launch your web app in Microsoft Edge Canary, Dev, or Beta</span></span>  
> ![Visual Studio с возможностью запуска веб-приложения в Microsoft Edge Канарские, dev или Beta][ImageVisualStudioLaunchWebApp]  

<span data-ttu-id="9185e-188">[В этой статье рассказывается о том, как отлаживать Microsoft Edge из Visual Studio][MicrosoftVisualStudioBlogDebugJavascript].</span><span class="sxs-lookup"><span data-stu-id="9185e-188">[Read our blog post to learn how to debug Microsoft Edge from Visual Studio][MicrosoftVisualStudioBlogDebugJavascript].</span></span>  

### <span data-ttu-id="9185e-189">Сообщения консоли предотвращения отслеживания</span><span class="sxs-lookup"><span data-stu-id="9185e-189">Tracking prevention Console messages</span></span>  

<span data-ttu-id="9185e-190">Защита от слежения — это уникальная функция в Microsoft EDGE, которая защищает вас от отслеживания веб-сайтов, которые вы еще не посещаете.</span><span class="sxs-lookup"><span data-stu-id="9185e-190">Tracking prevention is a unique feature in Microsoft Edge that protects you from being tracked by websites you haven't visited before.</span></span>  <span data-ttu-id="9185e-191">Параметр предотвращения отслеживания по умолчанию — это режим балансировки, который блокирует средства отслеживания и известных злоумышленников, чтобы обеспечить баланс конфиденциальности и веб-совместимости.</span><span class="sxs-lookup"><span data-stu-id="9185e-191">The default tracking prevention setting is Balanced mode, which blocks 3rd party trackers and known malicious trackers for an experience that balances privacy and web compatibility.</span></span>  <span data-ttu-id="9185e-192">Чтобы получить более подробную информацию о совместимости веб-страницы, если некоторые средства отслеживания заблокированы, мы также добавили предупреждающие сообщения на консоли, когда средство отслеживания заблокировано.</span><span class="sxs-lookup"><span data-stu-id="9185e-192">To give you more insight into the compatibility of your web page when certain trackers are blocked, we've also added warning messages in the Console when a tracker is blocked.</span></span>  

> ##### <span data-ttu-id="9185e-193">Рисунок9</span><span class="sxs-lookup"><span data-stu-id="9185e-193">Figure 9</span></span>  
> <span data-ttu-id="9185e-194">Сообщения на консоли, когда предотвращение отслеживания блокирует доступ к хранилищу для средства отслеживания</span><span class="sxs-lookup"><span data-stu-id="9185e-194">Messages in the Console when tracking prevention blocks access to storage for a tracker</span></span>  
> ![Сообщения на консоли, когда предотвращение отслеживания блокирует доступ к хранилищу для средства отслеживания][ImageTrackingPrevention]  

<span data-ttu-id="9185e-196">[Узнайте больше о предотвращении отслеживания и балансе между конфиденциальностью и веб-совместимостью][TrackingPrevention].</span><span class="sxs-lookup"><span data-stu-id="9185e-196">[Read more about tracking prevention and the balance between privacy and web compatibility][TrackingPrevention].</span></span>  

## <span data-ttu-id="9185e-197">Объявления из проекта Chromium</span><span class="sxs-lookup"><span data-stu-id="9185e-197">Announcements from the Chromium project</span></span>  

<span data-ttu-id="9185e-198">В следующих разделах описаны дополнительные возможности, доступные в Microsoft Edge 80, которые были задействованы в проекте Open Source Chromium.</span><span class="sxs-lookup"><span data-stu-id="9185e-198">The following sections announce additional features available in Microsoft Edge 80 that were contributed to the open source Chromium project.</span></span>  

### <span data-ttu-id="9185e-199">Поддержка повторной декларации Let и Class на консоли</span><span class="sxs-lookup"><span data-stu-id="9185e-199">Support for let and class redeclarations in the Console</span></span>   

<span data-ttu-id="9185e-200">Теперь консоль поддерживает повторное объявление `let` `class` операторов and.</span><span class="sxs-lookup"><span data-stu-id="9185e-200">The Console now supports redeclarations of `let` and `class` statements.</span></span>  <span data-ttu-id="9185e-201">Невозможность повторного объявления — это распространенный annoyance для веб-разработчиков, использующих консоль для экспериментов с новым кодом JavaScript.</span><span class="sxs-lookup"><span data-stu-id="9185e-201">The inability to redeclare was a common annoyance for web developers who use the Console to experiment with new JavaScript code.</span></span>  

> [!WARNING]
> <span data-ttu-id="9185e-202">При повторном объявлении `let` `class` оператора или в сценарии, находящегося за пределами консоли или при вводе с помощью одного из входных данных в командной консоли возникает проблема `SyntaxError` .</span><span class="sxs-lookup"><span data-stu-id="9185e-202">Redeclaring a `let` or `class` statement in a script outside of the Console or within a single Console input still causes a `SyntaxError`.</span></span>  

<span data-ttu-id="9185e-203">Например, ранее при повторном объявлении локальной переменной `let` консоль вызвала ошибку:</span><span class="sxs-lookup"><span data-stu-id="9185e-203">For example, previously, when redeclaring a local variable with `let`, the Console threw an error:</span></span>  

> ##### <span data-ttu-id="9185e-204">Рисунок 10</span><span class="sxs-lookup"><span data-stu-id="9185e-204">Figure 10</span></span>  
> <span data-ttu-id="9185e-205">Консоль в Microsoft Edge 79 показывает, что повторное объявление Let не выполняется</span><span class="sxs-lookup"><span data-stu-id="9185e-205">The Console in Microsoft Edge 79 showing that the let redeclaration fails</span></span>  
> ![Консоль в Microsoft Edge 79 показывает, что повторное объявление Let не выполняется][ImageConsoleRedeclarationFails]  

<span data-ttu-id="9185e-207">Теперь консоль допускает повторное объявление:</span><span class="sxs-lookup"><span data-stu-id="9185e-207">Now, the Console allows the redeclaration:</span></span>  

> ##### <span data-ttu-id="9185e-208">Рисунок11</span><span class="sxs-lookup"><span data-stu-id="9185e-208">Figure 11</span></span>  
> <span data-ttu-id="9185e-209">Консоль в Microsoft Edge 80, на которой показано, что повторное объявление Let успешно.</span><span class="sxs-lookup"><span data-stu-id="9185e-209">The Console in Microsoft Edge 80 showing that the let redeclaration succeeds</span></span>  
> ![Консоль в Microsoft Edge 80, на которой показано, что повторное объявление Let успешно.][ImageConsoleRedeclarationSucceeds]  

<span data-ttu-id="9185e-211">[#1004193][crbug1004193] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="9185e-211">Chromium issue [#1004193][crbug1004193]</span></span>  

### <span data-ttu-id="9185e-212">Улучшенная Отладка сборок</span><span class="sxs-lookup"><span data-stu-id="9185e-212">Improved WebAssembly debugging</span></span>   

<span data-ttu-id="9185e-213">DevTools начал поддерживать [стандарт отладки dwarf][DwarfHome], что означает увеличение поддержки степпинга кода, установки точек останова и разрешения трассировки стека на исходном языке в DevTools.</span><span class="sxs-lookup"><span data-stu-id="9185e-213">DevTools has started to support the [DWARF Debugging Standard][DwarfHome], which means increased support for stepping over code, setting breakpoints, and resolving stack traces in your source languages within DevTools.</span></span>  

<!-- [TODO: Add this link back] -->  
<!--Check out [Improved WebAssembly debugging in Microsoft Edge DevTools][201912Webassembly] for the full story.  -->  

<!-- [TODO: Replace this image with screenshot in Edge] -->  
<!--
> ##### Figure  
> The new DWARF-powered WebAssembly debugging  
> ![The new DWARF-powered WebAssembly debugging][ImageDwarfPoweredWebAssemblyDebugging]  
-->  

### <span data-ttu-id="9185e-214">Обновления панели сети</span><span class="sxs-lookup"><span data-stu-id="9185e-214">Network panel updates</span></span>   

#### <span data-ttu-id="9185e-215">Цепочки инициаторов запросов на вкладке инициатора</span><span class="sxs-lookup"><span data-stu-id="9185e-215">Request Initiator Chains in the Initiator tab</span></span>   

<span data-ttu-id="9185e-216">Теперь вы можете просмотреть инициаторы и зависимости сетевого запроса как вложенный список.</span><span class="sxs-lookup"><span data-stu-id="9185e-216">You are now able to view the initiators and dependencies of a network request as a nested list.</span></span>  <span data-ttu-id="9185e-217">Это может помочь вам понять, почему был запрошен ресурс, а также о том, какая сетевая активность связана с определенным ресурсом (например, сценарием).</span><span class="sxs-lookup"><span data-stu-id="9185e-217">This may help you understand why a resource was requested, or what network activity a certain resource \(such as a script\) caused.</span></span>  

> ##### <span data-ttu-id="9185e-218">Рисунок12</span><span class="sxs-lookup"><span data-stu-id="9185e-218">Figure 12</span></span>  
> <span data-ttu-id="9185e-219">Цепочка инициаторов запросов на вкладке инициатора</span><span class="sxs-lookup"><span data-stu-id="9185e-219">A Request Initiator Chain in the Initiator tab</span></span>  
> ![Цепочка инициаторов запросов на вкладке инициатора][ImageRequestInitiatorChain]  

<span data-ttu-id="9185e-221">После [входа в сеть на панели Network (сеть][DevToolsNetworkIndex]) выберите ресурс и перейдите на вкладку **инициатор** , чтобы просмотреть **цепочку инициаторов запроса**.</span><span class="sxs-lookup"><span data-stu-id="9185e-221">After [logging network activity in the Network panel][DevToolsNetworkIndex], click a resource and then go to the **Initiator** tab to view the **Request Initiator Chain**:</span></span>  

*   <span data-ttu-id="9185e-222">**Проверенный ресурс** выделяется полужирным шрифтом.</span><span class="sxs-lookup"><span data-stu-id="9185e-222">The **inspected resource** is bold.</span></span>  <span data-ttu-id="9185e-223">На снимке экрана выше `ai.2.min.js` показан проверенный ресурс.</span><span class="sxs-lookup"><span data-stu-id="9185e-223">In the screenshot above, `ai.2.min.js` is the inspected resource.</span></span>  
*   <span data-ttu-id="9185e-224">Ресурсы, расположенные выше проверенного ресурса, являются **инициаторами**.</span><span class="sxs-lookup"><span data-stu-id="9185e-224">The resources above the inspected resource are the **initiators**.</span></span>  <span data-ttu-id="9185e-225">На снимке экрана выше `https://www.microsoftedgeinsider.com` — инициатор `ai.2.min.js` .</span><span class="sxs-lookup"><span data-stu-id="9185e-225">In the screenshot above, `https://www.microsoftedgeinsider.com` is the initiator of `ai.2.min.js`.</span></span>  <span data-ttu-id="9185e-226">Другими словами, `https://www.microsoftedgeinsider.com` это привело к сетевому запросу `ai.2.min.js` .</span><span class="sxs-lookup"><span data-stu-id="9185e-226">In other words, `https://www.microsoftedgeinsider.com` caused the network request for `ai.2.min.js`.</span></span>  
*   <span data-ttu-id="9185e-227">Ресурсы, расположенные под проверенным ресурсом, являются **зависимостями**.</span><span class="sxs-lookup"><span data-stu-id="9185e-227">The resources below the inspected resource are the **dependencies**.</span></span>  <span data-ttu-id="9185e-228">На снимке экрана выше `https://dc.services.visualstudio.com/v2/track` есть зависимость `ai.2.min.js` .</span><span class="sxs-lookup"><span data-stu-id="9185e-228">In the screenshot above, `https://dc.services.visualstudio.com/v2/track` is a dependency of `ai.2.min.js`.</span></span>  <span data-ttu-id="9185e-229">Другими словами, `ai.2.min.js` это привело к сетевому запросу `https://dc.services.visualstudio.com/v2/track` .</span><span class="sxs-lookup"><span data-stu-id="9185e-229">In other words, `ai.2.min.js` caused the network request for `https://dc.services.visualstudio.com/v2/track`.</span></span>  

> [!NOTE]
> <span data-ttu-id="9185e-230">Кроме того, можно получить доступ к сведениям об инициаторе и `Shift` наведении указателя мыши на ресурсы сети.</span><span class="sxs-lookup"><span data-stu-id="9185e-230">Initiator and dependency information may also be accessed by holding `Shift` and then hovering over network resources.</span></span>  <span data-ttu-id="9185e-231">Просмотр [инициаторов и зависимостей][DevToolsNetworkReferenceViewInitiatorsDependencies].</span><span class="sxs-lookup"><span data-stu-id="9185e-231">See [View initiators and dependencies][DevToolsNetworkReferenceViewInitiatorsDependencies].</span></span>  

<span data-ttu-id="9185e-232">[#842488][crbug842488] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="9185e-232">Chromium issue [#842488][crbug842488]</span></span>  

#### <span data-ttu-id="9185e-233">Выделение выбранного сетевого запроса в обзоре</span><span class="sxs-lookup"><span data-stu-id="9185e-233">Highlight the selected network request in the Overview</span></span>   

<span data-ttu-id="9185e-234">После выбора сетевого ресурса для его проверки на панели Network (сеть) размещается синяя рамка вокруг **ресурса.**</span><span class="sxs-lookup"><span data-stu-id="9185e-234">After you click a network resource in order to inspect it, the Network panel now puts a blue border around that resource in the **Overview**.</span></span>  <span data-ttu-id="9185e-235">Это поможет определить, является ли сетевой запрос более ранней или более поздней, чем ожидалось.</span><span class="sxs-lookup"><span data-stu-id="9185e-235">This is able to help you detect if the network request is happening earlier or later than expected.</span></span>  

> ##### <span data-ttu-id="9185e-236">Рисунок13</span><span class="sxs-lookup"><span data-stu-id="9185e-236">Figure 13</span></span>  
> <span data-ttu-id="9185e-237">Область "Обзор", в которой выделяются проверенные ресурсы</span><span class="sxs-lookup"><span data-stu-id="9185e-237">The Overview pane highlighting the inspected resource</span></span>  
> ![Область "Обзор", в которой выделяются проверенные ресурсы][ImageOverviewPaneInspectedResource]  

<span data-ttu-id="9185e-239">[#988253][crbug988253] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="9185e-239">Chromium issue [#988253][crbug988253]</span></span>  

#### <span data-ttu-id="9185e-240">URL-адреса и столбцы "путь" на панели "сеть"</span><span class="sxs-lookup"><span data-stu-id="9185e-240">URL and path columns in the Network panel</span></span>   

<span data-ttu-id="9185e-241">С помощью столбцов «новый **путь** » и « **URL-адрес** » на панели **Network (сеть** ) можно просмотреть абсолютный путь к каждому СЕТЕВОМУ ресурсу или полный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="9185e-241">Use the new **Path** and **URL** columns in the **Network** panel to see the absolute path or full URL of each network resource.</span></span>  

> ##### <span data-ttu-id="9185e-242">Рисунок14</span><span class="sxs-lookup"><span data-stu-id="9185e-242">Figure 14</span></span>  
> <span data-ttu-id="9185e-243">Столбцы "новый путь" и "URL-адрес" на панели "сеть"</span><span class="sxs-lookup"><span data-stu-id="9185e-243">The new Path and URL columns in the Network panel</span></span>  
> ![Столбцы "новый путь" и "URL-адрес" на панели "сеть"][ImagePathNetworkPanel]  

<span data-ttu-id="9185e-245">Щелкните заголовок **каскадной** таблицы правой кнопкой мыши и выберите команду **путь** или **URL-адрес** , чтобы отобразить новые столбцы.</span><span class="sxs-lookup"><span data-stu-id="9185e-245">Right-click the **Waterfall** table header and select **Path** or **URL** to show the new columns.</span></span>  

<span data-ttu-id="9185e-246">[#993366][crbug993366] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="9185e-246">Chromium issue [#993366][crbug993366]</span></span>  

#### <span data-ttu-id="9185e-247">Обновлены строки агента пользователя</span><span class="sxs-lookup"><span data-stu-id="9185e-247">Updated User-Agent strings</span></span>   

<span data-ttu-id="9185e-248">DevTools поддерживает задание пользовательской строки агента пользователя на вкладке **условия сети** .  Строка агента пользователя влияет на `User-Agent` заголовок HTTP, подключенный к сетевым ресурсам, а также на значение `navigator.userAgent` .</span><span class="sxs-lookup"><span data-stu-id="9185e-248">DevTools supports setting a custom User-Agent string through the **Network Conditions** tab.  The User-Agent string affects the `User-Agent` HTTP header attached to network resources, and also the value of `navigator.userAgent`.</span></span>  

<span data-ttu-id="9185e-249">Предопределенные строки агента пользователя обновлены в соответствии с современными версиями браузера.</span><span class="sxs-lookup"><span data-stu-id="9185e-249">The predefined User-Agent strings have been updated to reflect modern browser versions.</span></span>  

> ##### <span data-ttu-id="9185e-250">Рисунок15</span><span class="sxs-lookup"><span data-stu-id="9185e-250">Figure 15</span></span>  
> <span data-ttu-id="9185e-251">Меню агента пользователя на вкладке "условия сети"</span><span class="sxs-lookup"><span data-stu-id="9185e-251">The User Agent menu in the Network Conditions tab</span></span>  
> ![Меню агента пользователя на вкладке "условия сети"][ImageUserAgentNetworkConditionsTab]  

<span data-ttu-id="9185e-253">Чтобы получить доступ к **сетевым условиям**, [откройте меню команд][DevToolsCommandMenuIndex] и выполните `Show Network Conditions` команду.</span><span class="sxs-lookup"><span data-stu-id="9185e-253">To access **Network Conditions**, [open the Command Menu][DevToolsCommandMenuIndex] and run the `Show Network Conditions` command.</span></span>  

> [!NOTE]
> <span data-ttu-id="9185e-254">Вы также можете [задать строки агента пользователя в режиме устройства][DevToolsDeviceModeIndex].</span><span class="sxs-lookup"><span data-stu-id="9185e-254">You may also [set User-Agent strings in Device Mode][DevToolsDeviceModeIndex].</span></span>  

<span data-ttu-id="9185e-255">[#1029031][crbug1029031] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="9185e-255">Chromium issue [#1029031][crbug1029031]</span></span>  

### <span data-ttu-id="9185e-256">Обновления панели аудита</span><span class="sxs-lookup"><span data-stu-id="9185e-256">Audits panel updates</span></span>   

#### <span data-ttu-id="9185e-257">Новый пользовательский интерфейс конфигурации</span><span class="sxs-lookup"><span data-stu-id="9185e-257">New configuration UI</span></span>   

<span data-ttu-id="9185e-258">Пользовательский интерфейс конфигурации имеет новый, реагирующий дизайн и параметры конфигурации регулирования были упрощены.</span><span class="sxs-lookup"><span data-stu-id="9185e-258">The configuration UI has a new, responsive design, and the throttling configuration options have been simplified.</span></span>  <span data-ttu-id="9185e-259">Дополнительные сведения об изменении пользовательского интерфейса для регулирования приведены в разделе [Аудит][GitHubGoogleChromeDevToolsAuditsPanelThrottling] .</span><span class="sxs-lookup"><span data-stu-id="9185e-259">See [Audits Panel Throttling][GitHubGoogleChromeDevToolsAuditsPanelThrottling] for more information on the throttling UI changes.</span></span>  

> ##### <span data-ttu-id="9185e-260">Рисунок16</span><span class="sxs-lookup"><span data-stu-id="9185e-260">Figure 16</span></span>  
> <span data-ttu-id="9185e-261">Новый пользовательский интерфейс конфигурации</span><span class="sxs-lookup"><span data-stu-id="9185e-261">The new configuration UI</span></span>  
> ![Новый пользовательский интерфейс конфигурации][ImageConfigurationUI]  

### <span data-ttu-id="9185e-263">Обновления вкладок покрытия</span><span class="sxs-lookup"><span data-stu-id="9185e-263">Coverage tab updates</span></span>   

#### <span data-ttu-id="9185e-264">Режимы покрытия для отдельных функций или отдельных блоков</span><span class="sxs-lookup"><span data-stu-id="9185e-264">Per-function or per-block coverage modes</span></span>   

<span data-ttu-id="9185e-265">На [вкладке Coverage][DevToolsCoverageIndex] имеется новое раскрывающееся меню, в котором можно указать, нужно ли собирать данные о покрытии кода **для одной функции** или **для каждого блока**.</span><span class="sxs-lookup"><span data-stu-id="9185e-265">The [Coverage tab][DevToolsCoverageIndex] has a new dropdown menu that lets you specify whether code coverage data should be collected **per function** or **per block**.</span></span>  <span data-ttu-id="9185e-266">Покрытие **за блоком** является более подробным, но и более затратным для сбора.</span><span class="sxs-lookup"><span data-stu-id="9185e-266">**Per block** coverage is more detailed but also far more expensive to collect.</span></span>  <span data-ttu-id="9185e-267">DevTools по умолчанию использует **функцию на уровне отдельных функций** .</span><span class="sxs-lookup"><span data-stu-id="9185e-267">DevTools uses **per function** coverage by default now.</span></span>  

> [!CAUTION]
> <span data-ttu-id="9185e-268">В зависимости от того, используется ли **функция** **или режим, в HTML** -файлах могут возблюдаться большие различия в покрытии кода.</span><span class="sxs-lookup"><span data-stu-id="9185e-268">You may see large code coverage differences in HTML files depending on whether you use **per function** or **per block** mode.</span></span>  <span data-ttu-id="9185e-269">При использовании режима " **на функцию** " встроенные сценарии в HTML-файлах рассматриваются как функции.</span><span class="sxs-lookup"><span data-stu-id="9185e-269">When using **per function** mode, inline scripts in HTML files are treated as functions.</span></span>  <span data-ttu-id="9185e-270">Если сценарий выполняется, DevTools помечает весь сценарий как использованный код.</span><span class="sxs-lookup"><span data-stu-id="9185e-270">If the script runs at all then DevTools marks the entire script as used code.</span></span>  <span data-ttu-id="9185e-271">Если сценарий не выполняется вообще, DevTools помечает сценарий как неиспользуемый код.</span><span class="sxs-lookup"><span data-stu-id="9185e-271">Only if the script does not run at all does DevTools mark the script as unused code.</span></span>  

> ##### <span data-ttu-id="9185e-272">Рисунок17</span><span class="sxs-lookup"><span data-stu-id="9185e-272">Figure 17</span></span>  
> <span data-ttu-id="9185e-273">Раскрывающееся меню «режим покрытия»</span><span class="sxs-lookup"><span data-stu-id="9185e-273">The coverage mode dropdown menu</span></span>  
> ![Раскрывающееся меню «режим покрытия»][ImageCoverageMode]  

#### <span data-ttu-id="9185e-275">Теперь покрытие должно быть инициировано перезагрузкой страницы</span><span class="sxs-lookup"><span data-stu-id="9185e-275">Coverage must now be initiated by a page reload</span></span>   

<span data-ttu-id="9185e-276">Переключение покрытия кода без повторной загрузки страницы удалено, так как данные о покрытии были ненадежны.</span><span class="sxs-lookup"><span data-stu-id="9185e-276">Toggling code coverage without a page reload has been removed because the coverage data was unreliable.</span></span>  <span data-ttu-id="9185e-277">Например, функция может быть указана как неиспользуемая, если среда выполнения была длиннее давно, а сборщик мусора V8 удалил его.</span><span class="sxs-lookup"><span data-stu-id="9185e-277">For example, a function may be reported as unused if the runtime was a long time ago and the V8 garbage collector has cleaned it up.</span></span>  

<span data-ttu-id="9185e-278">[#1004203][crbug1004203] проблем с Chromium</span><span class="sxs-lookup"><span data-stu-id="9185e-278">Chromium issue [#1004203][crbug1004203]</span></span>  

## <span data-ttu-id="9185e-279">Отзыв</span><span class="sxs-lookup"><span data-stu-id="9185e-279">Feedback</span></span>   



<span data-ttu-id="9185e-280">Чтобы обсудить новые возможности и изменения в этой записи, а также другие связанные с DevTools, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="9185e-280">To discuss the new features and changes in this post, or anything else related to DevTools:</span></span>  

*   <span data-ttu-id="9185e-281">Отправка отзыва с помощью значка **обратной связи** в DevTools</span><span class="sxs-lookup"><span data-stu-id="9185e-281">Send your feedback using the **Feedback** icon in the DevTools</span></span>  

> ##### <span data-ttu-id="9185e-282">Рис. 18</span><span class="sxs-lookup"><span data-stu-id="9185e-282">Figure 18</span></span>
> <span data-ttu-id="9185e-283">Значок **обратной связи** в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="9185e-283">The **Feedback** icon in the Microsoft Edge DevTools</span></span>  
> ![Значок \* \* Feedback \* \* в Microsoft Edge DevTools][ImageFeedbackIcon]  

*   <span data-ttu-id="9185e-285">Твит на [@EdgeDevTools][PostTweetEdgeDevTools]</span><span class="sxs-lookup"><span data-stu-id="9185e-285">Tweet at [@EdgeDevTools][PostTweetEdgeDevTools]</span></span>  
*   <span data-ttu-id="9185e-286">Отправка предложения в [Вебе][TheWebWeWant]</span><span class="sxs-lookup"><span data-stu-id="9185e-286">Submit a suggestion to [The Web We Want][TheWebWeWant]</span></span>  
*   <span data-ttu-id="9185e-287">Ошибки файла в этом документе в репозитории " [Edge — разработчик][GitHubMicrosoftDocsEdgeDeveloperNewIssue] "</span><span class="sxs-lookup"><span data-stu-id="9185e-287">File bugs on this document in the [edge-developer][GitHubMicrosoftDocsEdgeDeveloperNewIssue] repository</span></span>  

## <span data-ttu-id="9185e-288">Загрузка каналов предварительной версии Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="9185e-288">Download the Microsoft Edge preview channels</span></span>   

<span data-ttu-id="9185e-289">Если вы используете Windows или macOS, рассматривайте в качестве браузера по умолчанию использование [каналов предварительного просмотра Microsoft Edge][MicrosoftEdgePreviewChannels] .</span><span class="sxs-lookup"><span data-stu-id="9185e-289">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="9185e-290">Каналы предварительного просмотра предоставляют доступ к последним функциям DevTools.</span><span class="sxs-lookup"><span data-stu-id="9185e-290">The preview channels give you access to the latest DevTools features.</span></span>  

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
[ImageFeedbackIcon]: ../../images/2019/12/feedback-icon.msft.png "Рисунок 18: значок * * Feedback * * в Microsoft Edge DevTools"

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
> <span data-ttu-id="9185e-348">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9185e-348">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="9185e-349">Исходная страница будет найдена [здесь](https://developers.google.com/web/updates/2019/12/devtools/index) и [Kayce Basques][KayceBasques] \ (технический писатель, хром DevTools & Lighthouse).</span><span class="sxs-lookup"><span data-stu-id="9185e-349">The original page is found [here](https://developers.google.com/web/updates/2019/12/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools & Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="9185e-351">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="9185e-351">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
