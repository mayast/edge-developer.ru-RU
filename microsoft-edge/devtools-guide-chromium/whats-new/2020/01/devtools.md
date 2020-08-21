---
title: Новые возможности в DevTools (Microsoft Edge 81)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/17/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 8e9e6885d04c7ad15a688b51cee4c16440d3ca1e
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942097"
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

# <span data-ttu-id="c6a52-103">Новые возможности в средствах разработчиков (Microsoft Edge 81)</span><span class="sxs-lookup"><span data-stu-id="c6a52-103">What's New In DevTools (Microsoft Edge 81)</span></span>  

## <span data-ttu-id="c6a52-104">Объявления от команды разработчиков Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c6a52-104">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="c6a52-105">В следующих разделах приведен список извещений, которые вы можете пропустить от команды разработчиков Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c6a52-105">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team!</span></span> <span data-ttu-id="c6a52-106">Ознакомьтесь с их новыми возможностями в DevTools, расширениях кодов VS и многом другом.</span><span class="sxs-lookup"><span data-stu-id="c6a52-106">Check them out to try new features in the DevTools, VS Code extensions, and more.</span></span>  <span data-ttu-id="c6a52-107">Чтобы быть в курсе всех последних и полезных функций в средствах разработчика, скачайте [каналы microsoft Edge][MicrosoftEdgePreviewChannels] и [отслеживайте нас в Твиттере.][EdgeDevToolsTwitterAccount]</span><span class="sxs-lookup"><span data-stu-id="c6a52-107">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <span data-ttu-id="c6a52-108">Улучшенные специальные возможности в средствах разработчиков</span><span class="sxs-lookup"><span data-stu-id="c6a52-108">Accessibility improvements to the DevTools</span></span>  

<span data-ttu-id="c6a52-109">Меняется 170 на хромомоблю изменилось 170 на Chromium на устранение контрастности цвета, клавиатуры и средства чтения с экрана в средствах разработчиков.</span><span class="sxs-lookup"><span data-stu-id="c6a52-109">The DevTools team has contributed 170 changes to Chromium to address high-impact color contrast, keyboard, and screen reader issues in the DevTools.</span></span>  <span data-ttu-id="c6a52-110">Каждый разработчик, созданный в Интернете, должен использовать DevTools.</span><span class="sxs-lookup"><span data-stu-id="c6a52-110">Every developer building the web should be able to use the DevTools.</span></span>  

> ##### <span data-ttu-id="c6a52-111">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="c6a52-111">Figure 1</span></span>  
> <span data-ttu-id="c6a52-112">Средство для работы с разработчиками с помощью клавиатуры и средства чтения с экрана</span><span class="sxs-lookup"><span data-stu-id="c6a52-112">The Performance tool in the DevTools with the keyboard navigation and screen reader improvements</span></span>  
> ![Средство для работы с разработчиками с помощью клавиатуры и средства чтения с экрана][ImagePerformanceToolKeyboardReaderImprovements]  

<span data-ttu-id="c6a52-114">Хотите узнать, как сделать веб-страницу доступным для всех пользователей?</span><span class="sxs-lookup"><span data-stu-id="c6a52-114">Want to learn how to make your web page accessible to all of your users?</span></span>  <span data-ttu-id="c6a52-115">Скачайте [средство "Аналитика][AccessibilityInsights] специальных возможностей" и [расширения][WebhintBrowserExtension] веб-сайта, касающиеся Microsoft Edge для начала работы.</span><span class="sxs-lookup"><span data-stu-id="c6a52-115">Download the [Accessibility Insights][AccessibilityInsights] and [webhint][WebhintBrowserExtension] extensions for Microsoft Edge to get started.</span></span>  

<span data-ttu-id="c6a52-116">Если вы используете средства чтения с экрана или клавиатуру для навигации по Разработчикам, отправьте нам свой отзыв, [твитирую щелкая][PostTweetEdgeDevTools] на мнение или щелкнув [значок "Обратная](#getting-in-touch-with-microsoft-edge-devtools-team) связь!".</span><span class="sxs-lookup"><span data-stu-id="c6a52-116">If you use screen readers or the keyboard to navigate around the DevTools, send us your feedback by [tweeting][PostTweetEdgeDevTools] at us or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="c6a52-117">Проблема с [#963183][crbug963183]</span><span class="sxs-lookup"><span data-stu-id="c6a52-117">Chromium issue [#963183][crbug963183]</span></span>  

### <span data-ttu-id="c6a52-118">Использование средств разработчиков на других языках</span><span class="sxs-lookup"><span data-stu-id="c6a52-118">Using the DevTools in other languages</span></span>  

<span data-ttu-id="c6a52-119">Многие разработчики используют другие средства разработчика, такие как StackOverflow и VS code, на своем родном языке, а не только на английском языке.</span><span class="sxs-lookup"><span data-stu-id="c6a52-119">Many developers use other developer tools, like StackOverflow and VS Code, in their native language, not just in English.</span></span>  <span data-ttu-id="c6a52-120">Мы рады сообщать локализацию для разработчиков Разработчиков, которые теперь можно использовать на одном из 10 языков, кроме английского:</span><span class="sxs-lookup"><span data-stu-id="c6a52-120">We’re excited to announce localization for the DevTools, which you are now able to use in one of 10 languages besides English:</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="c6a52-121">Китайский \(упрощенное\) -  &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span><span class="sxs-lookup"><span data-stu-id="c6a52-121">Chinese \(Simplified\) - &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="c6a52-122">Китайский \(традиционное\) -  &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span><span class="sxs-lookup"><span data-stu-id="c6a52-122">Chinese \(Traditional\) - &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="c6a52-123">Французский (француз&#231;оси)</span><span class="sxs-lookup"><span data-stu-id="c6a52-123">French – fran&#231;ais</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="c6a52-124">Немецкий (отладка)</span><span class="sxs-lookup"><span data-stu-id="c6a52-124">German - deutsch</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="c6a52-125">Итальный (курсив)</span><span class="sxs-lookup"><span data-stu-id="c6a52-125">Italian - italiano</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="c6a52-126">Японский ( &#26085;&#26412;&#35486;</span><span class="sxs-lookup"><span data-stu-id="c6a52-126">Japanese - &#26085;&#26412;&#35486;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="c6a52-127">Корейский ( &#54620;&#44397;&#50612;</span><span class="sxs-lookup"><span data-stu-id="c6a52-127">Korean - &#54620;&#44397;&#50612;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="c6a52-128">Португальский (португалия&#234;s)</span><span class="sxs-lookup"><span data-stu-id="c6a52-128">Portuguese - portugu&#234;s</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="c6a52-129">Русский ( &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081; русский)</span><span class="sxs-lookup"><span data-stu-id="c6a52-129">Russian – &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="c6a52-130">Испанский (испания&#241;слишком много</span><span class="sxs-lookup"><span data-stu-id="c6a52-130">Spanish - espa&#241;ol</span></span>
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

<span data-ttu-id="c6a52-131">Язык, который вы используете в Microsoft Edge, автоматически соответствует языку, который вы `edge://settings/languages` используете.</span><span class="sxs-lookup"><span data-stu-id="c6a52-131">The DevTools automatically match the language you use for Microsoft Edge in `edge://settings/languages`.</span></span>  

<span data-ttu-id="c6a52-132">Если вы хотите, чтобы Microsoft Edge оставался на английском языке и язык с разработчиками остался на английском языке, откройте раздел "Параметры" и отключите `F1` язык **соответствия браузера.** [Settings][Settings]</span><span class="sxs-lookup"><span data-stu-id="c6a52-132">If you want Microsoft Edge to be in one language and your DevTools to remain in English, press `F1` in the DevTools to open [Settings][Settings] and disable **Match browser language**.</span></span>  

> ##### <span data-ttu-id="c6a52-133">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="c6a52-133">Figure 2</span></span>  
> <span data-ttu-id="c6a52-134">Средства разработчиков на немецком</span><span class="sxs-lookup"><span data-stu-id="c6a52-134">The DevTools in German</span></span>  
> ![Средства разработчиков на немецком][ImageLocalizedGerman]  

<span data-ttu-id="c6a52-136">**Сообщения консоли не** локализуются.</span><span class="sxs-lookup"><span data-stu-id="c6a52-136">**Console** messages are not localized.</span></span>  <span data-ttu-id="c6a52-137">На языке, который вы используете в Microsoft Edge, отображаются только строки, используемые в языке.</span><span class="sxs-lookup"><span data-stu-id="c6a52-137">Only the strings used in the DevTools UI are displayed in the language you use for Microsoft Edge.</span></span>  

<span data-ttu-id="c6a52-138">Если вы хотите использовать разработчики для разработчиков, отличного от того, какие из доступных вам языков вы хотите использовать, [то разговор][PostTweetEdgeDevTools] можно нам или щелкните [значок "Обратная связь".](#getting-in-touch-with-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="c6a52-138">If you want to use the DevTools in a different language than the ones that are available, [tweet][PostTweetEdgeDevTools] at us or click the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon.</span></span>  

<span data-ttu-id="c6a52-139">Проблема с [хромом#941561][crbug941561]</span><span class="sxs-lookup"><span data-stu-id="c6a52-139">Chromium issue [#941561][crbug941561]</span></span>  

### <span data-ttu-id="c6a52-140">расширение веб-сайта Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c6a52-140">webhint Microsoft Edge extension</span></span>  

<span data-ttu-id="c6a52-141">Расширение Microsoft Edge позволяет легко просматривать веб-страницу и получать отзывы о специальных возможностях, совместимости браузера, безопасности, производительности и т. д. в средствах DevTools.</span><span class="sxs-lookup"><span data-stu-id="c6a52-141">The webhint Microsoft Edge extension allows you to easily scan your web page and get feedback on accessibility, browser compatibility, security, performance, and more within the DevTools.</span></span>  <span data-ttu-id="c6a52-142">Дополнительные сведения [https://webhint.io][Webhint] см. в дополнительных случаях.</span><span class="sxs-lookup"><span data-stu-id="c6a52-142">Read more at [https://webhint.io][Webhint].</span></span>  

> ##### <span data-ttu-id="c6a52-143">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="c6a52-143">Figure 3</span></span>  
> <span data-ttu-id="c6a52-144">Вкладка «Подсказки» в приложении DevTools при установленном расширении браузера</span><span class="sxs-lookup"><span data-stu-id="c6a52-144">The Hints tab in the DevTools when the webhint browser extension is installed</span></span>  
> ![Вкладка «Подсказки» в приложении DevTools при установленном расширении браузера][ImageHintsTabWebhintExtension]  

<span data-ttu-id="c6a52-146">[Попробуйте расширение веб-браузера в Microsoft Edge.][MicrosoftEdgeInsiderAddons]</span><span class="sxs-lookup"><span data-stu-id="c6a52-146">[Try the webhint browser extension in Microsoft Edge][MicrosoftEdgeInsiderAddons].</span></span>  <span data-ttu-id="c6a52-147">После установки расширения откройте вкладку DevTools и выберите вкладку "Подсказки".  В этом окне выполните настраиваемое сканирование сайта.</span><span class="sxs-lookup"><span data-stu-id="c6a52-147">Once you install the extension, open the DevTools and select the Hints tab.  From here, run a customizable site scan.</span></span>  <span data-ttu-id="c6a52-148">Чтобы узнать [больше webhint.io, нажмите][WebhintBrowserExtension] дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="c6a52-148">Head over to [webhint.io][WebhintBrowserExtension] to learn more.</span></span>  

### <span data-ttu-id="c6a52-149">Трехмерное представление</span><span class="sxs-lookup"><span data-stu-id="c6a52-149">3D View</span></span>  

<span data-ttu-id="c6a52-150">Используйте **трехмерное** представление для отладки веб-приложения путем перехода к объектной модели [документов \(DOM\)][MDNDocumentObjectModel] или [стопки z-индекса.][MDNZIndex]</span><span class="sxs-lookup"><span data-stu-id="c6a52-150">Use the **3D View** to debug your web application by navigating through the [Document Object Model \(DOM\)][MDNDocumentObjectModel] or the [z-index][MDNZIndex] stacking context.</span></span>  

> ##### <span data-ttu-id="c6a52-151">Рисунок4</span><span class="sxs-lookup"><span data-stu-id="c6a52-151">Figure 4</span></span>  
> <span data-ttu-id="c6a52-152">Трехмерное представление в средствах разработчиков</span><span class="sxs-lookup"><span data-stu-id="c6a52-152">The 3D View in the DevTools</span></span>  
> ![Трехмерное представление в средствах разработчиков][Image3DView]  

<span data-ttu-id="c6a52-154">Чтобы открыть трехмерное представление, `Ctrl`  +  `Shift`  +  `P` нажмите клавишу в **трехмерном представлении** и выберите **"Показать трехмерное представление".**</span><span class="sxs-lookup"><span data-stu-id="c6a52-154">To access the 3D View, press `Ctrl` + `Shift` + `P`, type in **3D View** and select **Show 3D View**.</span></span>  

<span data-ttu-id="c6a52-155">Мы работаем над элементом, который мы работаем над новым элементом, поэтому отправьте [нам](#getting-in-touch-with-microsoft-edge-devtools-team)свой отзыв.</span><span class="sxs-lookup"><span data-stu-id="c6a52-155">We're working on the UI and adding more functionality to the 3D View, so please send us your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team).</span></span>  

<span data-ttu-id="c6a52-156">[Проблема][crbug987787] с #987787 chromium #987787</span><span class="sxs-lookup"><span data-stu-id="c6a52-156">Chromium issue [#987787][crbug987787]</span></span>  

### <span data-ttu-id="c6a52-157">Visual Studio расширения кода</span><span class="sxs-lookup"><span data-stu-id="c6a52-157">Visual Studio Code extensions</span></span>  

<span data-ttu-id="c6a52-158">Команда Разработчиков также выпущена [некоторые расширения для Visual Studio Code \(VS Code\),][VisualStudioCode] которые позволяют использовать возможности DevTools напрямую из текстового редактора!</span><span class="sxs-lookup"><span data-stu-id="c6a52-158">The DevTools team has also released some extensions for [Visual Studio Code \(VS Code\)][VisualStudioCode] that let you use the power of the DevTools directly from your text editor!</span></span> <span data-ttu-id="c6a52-159">Ознакомьтесь с расширениями ниже.</span><span class="sxs-lookup"><span data-stu-id="c6a52-159">Check out the extensions below:</span></span>  

#### <span data-ttu-id="c6a52-160">Элементы Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c6a52-160">Elements for Microsoft Edge</span></span>  

<span data-ttu-id="c6a52-161">Используйте инструмент "Элементы" в коде VS, добавив расширение ["Элементы" для Microsoft Edge \(Chromium\)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] VS CodeS.</span><span class="sxs-lookup"><span data-stu-id="c6a52-161">Use the Elements tool from within VS Code by adding the [Elements for Microsoft Edge \(Chromium\)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] VS Code extension.</span></span>  

> ##### <span data-ttu-id="c6a52-162">Рисунок 5</span><span class="sxs-lookup"><span data-stu-id="c6a52-162">Figure 5</span></span>  
> <span data-ttu-id="c6a52-163">Инструмент "Элементы" в коде VS с помощью расширения "Элементы" microsoft Edge для Microsoft Edge с помощью расширения "Элементы" для ![ Microsoft Edge][ImageElementsVisualStudioCode]</span><span class="sxs-lookup"><span data-stu-id="c6a52-163">The Elements tool in VS Code using the Elements for Microsoft Edge extension ![The Elements tool in VS Code using the Elements for Microsoft Edge extension][ImageElementsVisualStudioCode]</span></span>  

<span data-ttu-id="c6a52-164">Дополнительные сведения см. [в статье "Элементы расширения кода Microsoft Edge VS".][VisualStudioCodeElementEdgeExtension]</span><span class="sxs-lookup"><span data-stu-id="c6a52-164">For more information, check out [Elements for Microsoft Edge VS Code extension][VisualStudioCodeElementEdgeExtension].</span></span>  

#### <span data-ttu-id="c6a52-165">Отладка для Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c6a52-165">Debugger for Microsoft Edge</span></span>  

<span data-ttu-id="c6a52-166">С [расширением][VisualStudioMarketplaceDebuggerEdge] отладки для Microsoft Edge VS отладка JavaScript работает в Microsoft Edge непосредственно из кода VS Code!</span><span class="sxs-lookup"><span data-stu-id="c6a52-166">With the [Debugger for Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] VS Code extension, debug JavaScript running in Microsoft Edge directly from VS Code!</span></span>  

> ##### <span data-ttu-id="c6a52-167">Рисунок6</span><span class="sxs-lookup"><span data-stu-id="c6a52-167">Figure 6</span></span>  
> <span data-ttu-id="c6a52-168">Отладка расширения Microsoft Edge в коде VS</span><span class="sxs-lookup"><span data-stu-id="c6a52-168">The Debugger for Microsoft Edge Extension in VS Code</span></span>  
> ![Отладка расширения Microsoft Edge в коде VS][ImageDebuggerExtensionVisualStudioCode]  

<span data-ttu-id="c6a52-170">Дополнительные сведения см. в [статье о том, как отладить Microsoft Edge от кода VS.][VisualStudioCodeDebuggerEdgeExtension]</span><span class="sxs-lookup"><span data-stu-id="c6a52-170">For more information, check out [how to debug Microsoft Edge from VS Code][VisualStudioCodeDebuggerEdgeExtension].</span></span>  

#### <span data-ttu-id="c6a52-171">webhint</span><span class="sxs-lookup"><span data-stu-id="c6a52-171">webhint</span></span>  

<span data-ttu-id="c6a52-172">[Расширение веб-кода][VisualStudioMarketplaceWebhintExtension] VS используется для `webhint` улучшения веб-страницы во время его письма.</span><span class="sxs-lookup"><span data-stu-id="c6a52-172">The [webhint][VisualStudioMarketplaceWebhintExtension] VS Code extension uses `webhint` to improve your web page while you're writing it!</span></span> <span data-ttu-id="c6a52-173">Это расширение выполняется, а отчеты диагностики для файлов рабочей области на основе `webhint` анализа.</span><span class="sxs-lookup"><span data-stu-id="c6a52-173">This extension runs and reports diagnostics on your workspace files based on `webhint` analysis.</span></span>  

> ##### <span data-ttu-id="c6a52-174">Рисунок7</span><span class="sxs-lookup"><span data-stu-id="c6a52-174">Figure 7</span></span>  
> <span data-ttu-id="c6a52-175">Расширение веб-кода VS с кодом VS</span><span class="sxs-lookup"><span data-stu-id="c6a52-175">The webhint VS Code extension analyzing a .tsx file in VS Code</span></span>  
> ![Расширение веб-кода VS с кодом VS][ImageWebhintVisualStudioCodeExtensionWorkspace]  

<span data-ttu-id="c6a52-177">[Дополнительные сведения о расширении веб-кода VS кода VS.][WebhintVisualStudioCodeExtension]</span><span class="sxs-lookup"><span data-stu-id="c6a52-177">[Learn more about the VS Code webhint extension][WebhintVisualStudioCodeExtension].</span></span>  

### <span data-ttu-id="c6a52-178">Visual Studio интеграции</span><span class="sxs-lookup"><span data-stu-id="c6a52-178">Visual Studio integration</span></span>  

<span data-ttu-id="c6a52-179">В Visual Studio 2019 г. и более поздних версий используйте отладку Visual Studio для отладки JavaScript в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c6a52-179">In Visual Studio 2019 version 16.2 or later, use the Visual Studio debugger to debug JavaScript running in Microsoft Edge.</span></span>  <span data-ttu-id="c6a52-180">[Скачайте Visual Studio 2019 г.,][MicrosoftVisualStudioDownloads] чтобы опробовать эту функцию!</span><span class="sxs-lookup"><span data-stu-id="c6a52-180">[Download Visual Studio 2019][MicrosoftVisualStudioDownloads] to try this feature out!</span></span>  

> ##### <span data-ttu-id="c6a52-181">Рисунок8</span><span class="sxs-lookup"><span data-stu-id="c6a52-181">Figure 8</span></span>  
> <span data-ttu-id="c6a52-182">Visual Studio с возможностью запустить веб-приложение в Microsoft Edge Canary, Dev или бета-версии</span><span class="sxs-lookup"><span data-stu-id="c6a52-182">Visual Studio with the option to launch your web app in Microsoft Edge Canary, Dev, or Beta</span></span>  
> ![Visual Studio с возможностью запустить веб-приложение в Microsoft Edge Canary, Dev или бета-версии][ImageVisualStudioLaunchWebApp]  

<span data-ttu-id="c6a52-184">[Подробнее об отладке Microsoft Edge Visual Studio.][MicrosoftVisualStudio]</span><span class="sxs-lookup"><span data-stu-id="c6a52-184">[Learn more about debugging Microsoft Edge from Visual Studio][MicrosoftVisualStudio].</span></span>  

### <span data-ttu-id="c6a52-185">Сообщения консоли отслеживания</span><span class="sxs-lookup"><span data-stu-id="c6a52-185">Tracking prevention Console messages</span></span>  

<span data-ttu-id="c6a52-186">Предотвращение отслеживания — это уникальная функция в Microsoft Edge, которая защищает вас при посещении веб-сайтов, которые вы не посещали.</span><span class="sxs-lookup"><span data-stu-id="c6a52-186">Tracking prevention is a unique feature in Microsoft Edge that protects you from being tracked by websites you haven't visited before.</span></span>  <span data-ttu-id="c6a52-187">По умолчанию этот режим предотвращает балансировку сбалансированного отслеживания, который блокирует сторонние средства отслеживания сторонних поставщиков и известные вредоносные отслеживатели для обеспечения балансировки конфиденциальности и совместимости веб-сайтов.</span><span class="sxs-lookup"><span data-stu-id="c6a52-187">The default tracking prevention setting is Balanced mode, which blocks 3rd party trackers and known malicious trackers for an experience that balances privacy and web compatibility.</span></span>  <span data-ttu-id="c6a52-188">Чтобы получить более подробные сведения о совместимости веб-страницы, когда заблокированы некоторые средства отслеживания, также мы добавили предупреждения в консоль, если средство отслеживания заблокирован.</span><span class="sxs-lookup"><span data-stu-id="c6a52-188">To give you more insight into the compatibility of your web page when certain trackers are blocked, we've also added warning messages in the Console when a tracker is blocked.</span></span>  

> ##### <span data-ttu-id="c6a52-189">Рисунок9</span><span class="sxs-lookup"><span data-stu-id="c6a52-189">Figure 9</span></span>  
> <span data-ttu-id="c6a52-190">Сообщения в консоли при отслеживании блокируют доступ к хранилищу для отслеживания</span><span class="sxs-lookup"><span data-stu-id="c6a52-190">Messages in the Console when tracking prevention blocks access to storage for a tracker</span></span>  
> ![Сообщения в консоли при отслеживании блокируют доступ к хранилищу для отслеживания][ImageTrackingPrevention]  

<span data-ttu-id="c6a52-192">[Узнайте больше о предотвращении отслеживания и балансе между конфиденциальностью и веб-совместимостью.][TrackingPrevention]</span><span class="sxs-lookup"><span data-stu-id="c6a52-192">[Read more about tracking prevention and the balance between privacy and web compatibility][TrackingPrevention].</span></span>  

## <span data-ttu-id="c6a52-193">Извещения из проекта Chromium</span><span class="sxs-lookup"><span data-stu-id="c6a52-193">Announcements from the Chromium project</span></span>  

<span data-ttu-id="c6a52-194">В следующих разделах описаны дополнительные функции, доступные в Браузере Microsoft Edge 81, которые были приняли в проекте открытого калерея Chromium.</span><span class="sxs-lookup"><span data-stu-id="c6a52-194">The following sections announce additional features available in Microsoft Edge 81 that were contributed to the open source Chromium project.</span></span>  

### <span data-ttu-id="c6a52-195">Поддержка Moto G4 в режиме устройства</span><span class="sxs-lookup"><span data-stu-id="c6a52-195">Moto G4 support in Device Mode</span></span>  

<span data-ttu-id="c6a52-196">После [включения панели][DeviceToolbar]инструментов устройств можно оценить размеры представления Moto G4 из **списка устройств.**</span><span class="sxs-lookup"><span data-stu-id="c6a52-196">After [enabling the Device Toolbar][DeviceToolbar], simulate the dimensions of a Moto G4 viewport from the **Device** list.</span></span>  

> ##### <span data-ttu-id="c6a52-197">Рисунок 10</span><span class="sxs-lookup"><span data-stu-id="c6a52-197">Figure 10</span></span>  
> <span data-ttu-id="c6a52-198">Пример окна просмотра модуля G4</span><span class="sxs-lookup"><span data-stu-id="c6a52-198">Simulating a Moto G4 viewport</span></span>  
> ![Пример окна просмотра модуля G4][ImageMotoG4]  

<span data-ttu-id="c6a52-200">Щелкните ["Показать рамку устройства"][DeviceFrame] для отображения оборудования Moto G4 вокруг портала просмотра.</span><span class="sxs-lookup"><span data-stu-id="c6a52-200">Click [Show Device Frame][DeviceFrame] to show the Moto G4 hardware around the viewport.</span></span>  

> ##### <span data-ttu-id="c6a52-201">Рисунок11</span><span class="sxs-lookup"><span data-stu-id="c6a52-201">Figure 11</span></span>  
> <span data-ttu-id="c6a52-202">Аппаратное оборудование Moto G4</span><span class="sxs-lookup"><span data-stu-id="c6a52-202">Showing the Moto G4 hardware</span></span>  
> ![Аппаратное оборудование Moto G4][ImageMotoG4Frame]  

<span data-ttu-id="c6a52-204">Дополнительные возможности</span><span class="sxs-lookup"><span data-stu-id="c6a52-204">Related features:</span></span>  

*   <span data-ttu-id="c6a52-205">Откройте [меню команд и][CommandMenu] запустите команду, чтобы сделать снимок экрана с оборудованием `Capture screenshot` Moto G4 (после включения **показа фрейма**устройства).</span><span class="sxs-lookup"><span data-stu-id="c6a52-205">Open the [Command Menu][CommandMenu] and run the `Capture screenshot` command to take a screenshot of the viewport that includes the Moto G4 hardware (after enabling **Show Device Frame**).</span></span>  
*   <span data-ttu-id="c6a52-206">[Регулирование][ThrottleNetworkAndCpu] сети и цпутивенности цикла, чтобы более тщательно оказались условия просмотра веб-сайта для мобильных устройств пользователей.</span><span class="sxs-lookup"><span data-stu-id="c6a52-206">[Throttle the network and CPU][ThrottleNetworkAndCpu] to more accurately simulate a mobile user's web browsing conditions.</span></span>  

<span data-ttu-id="c6a52-207">Проблема с [#924693][crbug924693]</span><span class="sxs-lookup"><span data-stu-id="c6a52-207">Chromium issue [#924693][crbug924693]</span></span>  

### <span data-ttu-id="c6a52-208">Обновления cookie</span><span class="sxs-lookup"><span data-stu-id="c6a52-208">Cookie-related updates</span></span>  

#### <span data-ttu-id="c6a52-209">Файлы cookie в области "Файлы cookie"</span><span class="sxs-lookup"><span data-stu-id="c6a52-209">Blocked cookies in the Cookies pane</span></span>  

<span data-ttu-id="c6a52-210">В области "Файлы cookie" на панели приложений теперь отображаются файлы cookie, на желтый фон.</span><span class="sxs-lookup"><span data-stu-id="c6a52-210">The Cookies pane in the Application panel now displays blocked cookies with a yellow background.</span></span>  

> ##### <span data-ttu-id="c6a52-211">Рисунок12</span><span class="sxs-lookup"><span data-stu-id="c6a52-211">Figure 12</span></span>  
> <span data-ttu-id="c6a52-212">Файлы cookie в области "Файлы cookie" панели приложения</span><span class="sxs-lookup"><span data-stu-id="c6a52-212">Blocked cookies in the Cookies pane of the Application panel</span></span>  
> ![Файлы cookie в области "Файлы cookie" панели приложения][ImageBlockedCookies]  

<span data-ttu-id="c6a52-214">Проблема с #1030258 chromium [#1030258][crbug|::ref1::|]</span><span class="sxs-lookup"><span data-stu-id="c6a52-214">Chromium issue [#1030258][crbug|::ref1::|]</span></span>  

#### <span data-ttu-id="c6a52-215">Приоритет cookie в области "Файлы cookie"</span><span class="sxs-lookup"><span data-stu-id="c6a52-215">Cookie priority in the Cookie pane</span></span>  

<span data-ttu-id="c6a52-216">Таблицы cookie на панели "Сети" и "Приложения" теперь содержит **столбец приоритета.**</span><span class="sxs-lookup"><span data-stu-id="c6a52-216">The Cookies tables in the Network and Application panels now include a **Priority** column.</span></span>  

> [!CAUTION]
> <span data-ttu-id="c6a52-217">Браузеры cookie, поддерживаемые браузерами Chromium, например Microsoft Edge, — это единое, поддерживающее приоритет файлов cookie.</span><span class="sxs-lookup"><span data-stu-id="c6a52-217">Chromium-based browsers, like Microsoft Edge, are the only browsers that support cookie priority.</span></span>  

<span data-ttu-id="c6a52-218">Проблема с [#1026879][crbug1026879]</span><span class="sxs-lookup"><span data-stu-id="c6a52-218">Chromium issue [#1026879][crbug1026879]</span></span>  

#### <span data-ttu-id="c6a52-219">Изменение всех значений cookie</span><span class="sxs-lookup"><span data-stu-id="c6a52-219">Edit all cookie values</span></span>  

<span data-ttu-id="c6a52-220">На данный момент все ячейки в таблицах Cookie доступны для редактирования, за исключением ячеек в столбце **Size,** так как столбец представляет сетевой размер файла cookie в байтах.</span><span class="sxs-lookup"><span data-stu-id="c6a52-220">All cells in the Cookie tables are editable now, except cells in the **Size** column because that column represents the network size of the cookie, in bytes.</span></span>  <span data-ttu-id="c6a52-221">Просмотрите [поля][CookiesFields] для каждого столбца.</span><span class="sxs-lookup"><span data-stu-id="c6a52-221">See [Fields][CookiesFields] for an explanation of each column.</span></span>  

> ##### <span data-ttu-id="c6a52-222">Рисунок13</span><span class="sxs-lookup"><span data-stu-id="c6a52-222">Figure 13</span></span>  
> <span data-ttu-id="c6a52-223">Изменение значения cookie</span><span class="sxs-lookup"><span data-stu-id="c6a52-223">Editing a cookie value</span></span>  
> ![Изменение значения cookie][ImageEditCookie]  

#### <span data-ttu-id="c6a52-225">Копировать как Node.js лицевой команде для включения данных cookie</span><span class="sxs-lookup"><span data-stu-id="c6a52-225">Copy as Node.js fetch to include cookie data</span></span>  

<span data-ttu-id="c6a52-226">Щелкните сетевой **Copy**запрос правой кнопкой мыши и выберите "Копировать Node.js с помощью лица, чтобы получить выражение с данными  >  **Copy as Node.js fetch** `fetch` cookie".</span><span class="sxs-lookup"><span data-stu-id="c6a52-226">Right-click a network request and select **Copy** > **Copy as Node.js fetch** to get a `fetch` expression that includes cookie data.</span></span>  

> ##### <span data-ttu-id="c6a52-227">Рисунок14</span><span class="sxs-lookup"><span data-stu-id="c6a52-227">Figure 14</span></span>  
> <span data-ttu-id="c6a52-228">Копировать Node.js обновляется из-за лица, обновляемом для обработки данных</span><span class="sxs-lookup"><span data-stu-id="c6a52-228">Copy as Node.js fetch</span></span>  
> ![Копировать Node.js обновляется из-за лица, обновляемом для обработки данных][ImageCopyFetch]  

<span data-ttu-id="c6a52-230">Проблема с хромом [#1029826][crbug1029826]</span><span class="sxs-lookup"><span data-stu-id="c6a52-230">Chromium issue [#1029826][crbug1029826]</span></span>  

### <span data-ttu-id="c6a52-231">Более тщательное виде веб-приложения</span><span class="sxs-lookup"><span data-stu-id="c6a52-231">More accurate web app manifest icons</span></span>  

<span data-ttu-id="c6a52-232">Ранее область манифеста на панели приложения отправила собственные запросы для отображения значков манифеста веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="c6a52-232">Previously, the Manifest pane in the Application panel sent its own requests in order to display web app manifest icons.</span></span>  <span data-ttu-id="c6a52-233">В DevTools теперь отображается точный значок манифеста, который используется в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c6a52-233">DevTools now shows the exact same manifest icon that Microsoft Edge uses.</span></span>  

> ##### <span data-ttu-id="c6a52-234">Рисунок15</span><span class="sxs-lookup"><span data-stu-id="c6a52-234">Figure 15</span></span>  
> <span data-ttu-id="c6a52-235">Значки в области манифеста</span><span class="sxs-lookup"><span data-stu-id="c6a52-235">Icons in the Manifest pane</span></span>  
> ![Значки в области манифеста][ImageManifestIcon]  

<span data-ttu-id="c6a52-237">Проблема с [#985402][crbug985402]</span><span class="sxs-lookup"><span data-stu-id="c6a52-237">Chromium issue [#985402][crbug985402]</span></span>  

### <span data-ttu-id="c6a52-238">Наведите указатель мыши на свойства содержимого CSS, чтобы увидеть несанкцируемые значения</span><span class="sxs-lookup"><span data-stu-id="c6a52-238">Hover over CSS content properties to see unescaped values</span></span>  

<span data-ttu-id="c6a52-239">Наведите указатель мыши на значение свойства, чтобы увидеть `content` необходимую версию значения.</span><span class="sxs-lookup"><span data-stu-id="c6a52-239">Hover over the value of a `content` property to see the unescaped version of the value.</span></span>  

<span data-ttu-id="c6a52-240">Например, в [данном видеоролике,][CSSContentDemo] когда вы просматриваете `p::after` элемент пикоменной элемента, в области "Стили" отображается escaped string:</span><span class="sxs-lookup"><span data-stu-id="c6a52-240">For example, in this [demo][CSSContentDemo] when you inspect the `p::after` pseudo-element you see an escaped string in the Styles pane:</span></span>  

> ##### <span data-ttu-id="c6a52-241">Рисунок16</span><span class="sxs-lookup"><span data-stu-id="c6a52-241">Figure 16</span></span>  
> <span data-ttu-id="c6a52-242">Строка ESCAP</span><span class="sxs-lookup"><span data-stu-id="c6a52-242">The escaped string</span></span>  
> ![Строка ESCAP][ImageEscapedString]  

<span data-ttu-id="c6a52-244">При наведении указателя `content` мыши на необязательное значение:</span><span class="sxs-lookup"><span data-stu-id="c6a52-244">When you hover over the `content` value you see the unescaped value:</span></span>  

> ##### <span data-ttu-id="c6a52-245">Рисунок17</span><span class="sxs-lookup"><span data-stu-id="c6a52-245">Figure 17</span></span>  
> <span data-ttu-id="c6a52-246">Необязательное значение</span><span class="sxs-lookup"><span data-stu-id="c6a52-246">The unescaped value</span></span>  
> ![Необязательное значение][ImageUnescapedString]  

### <span data-ttu-id="c6a52-248">Более подробные ошибки исходной карты в консоли</span><span class="sxs-lookup"><span data-stu-id="c6a52-248">More detailed source map errors in the Console</span></span>  

<span data-ttu-id="c6a52-249">Консоль теперь содержит более подробные сведения о причине загрузки исходной карты или связи источника.</span><span class="sxs-lookup"><span data-stu-id="c6a52-249">The Console now provides more detail on why a source map failed to load or parse.</span></span>  <span data-ttu-id="c6a52-250">Ранее она только что возникает из-за ошибки, в ней не объясняется, почему не так.</span><span class="sxs-lookup"><span data-stu-id="c6a52-250">Previously it just provided an error without explaining what went wrong.</span></span>  

> ##### <span data-ttu-id="c6a52-251">Рисование 18</span><span class="sxs-lookup"><span data-stu-id="c6a52-251">Figure 18</span></span>  
> <span data-ttu-id="c6a52-252">Ошибка загрузки исходной карты в консоли</span><span class="sxs-lookup"><span data-stu-id="c6a52-252">A source map loading error in the Console</span></span>  
> ![Ошибка загрузки исходной карты в консоли][ImageSourcemapError]  

### <span data-ttu-id="c6a52-254">Параметр отмены прокрутки в конце файла</span><span class="sxs-lookup"><span data-stu-id="c6a52-254">Setting for disabling scrolling past the end of a file</span></span>  

<span data-ttu-id="c6a52-255">Откройте [меню "Параметры",][Settings] а затем отключите прокрутку в конце файла, чтобы отключить поведение по умолчанию в списке **Preferences**  >  **Sources**  >  **Allow scrolling past end of file** **"Источники".**</span><span class="sxs-lookup"><span data-stu-id="c6a52-255">Open [Settings][Settings] and then disable **Preferences** > **Sources** > **Allow scrolling past end of file** to disable the default UI behavior that allows you to scroll well past the end of a file in the **Sources** panel.</span></span>  

> ##### <span data-ttu-id="c6a52-256">Рис. 19</span><span class="sxs-lookup"><span data-stu-id="c6a52-256">Figure 19</span></span>  
> <span data-ttu-id="c6a52-257">Выключение функции **прокрутки в** настроек</span><span class="sxs-lookup"><span data-stu-id="c6a52-257">Disabling **Allow scrolling past end of file** in Settings</span></span>  
> ![Выключение функции прокрутки в прошлом конце файла][ImageSettings]  

> ##### <span data-ttu-id="c6a52-259">Рис2 20</span><span class="sxs-lookup"><span data-stu-id="c6a52-259">Figure 20</span></span>  
> <span data-ttu-id="c6a52-260">Прокрутка после окончания файла становится неактивной.</span><span class="sxs-lookup"><span data-stu-id="c6a52-260">Scrolling past the end of a file is now disabled in the Sources panel</span></span>  
> ![Прокрутка после окончания файла становится неактивной.][ImageScroll]  

## <span data-ttu-id="c6a52-262">Загрузить каналы с предварительными версиями Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c6a52-262">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="c6a52-263">Если вы используете Windows или macOS, рекомендуем использовать каналы [предварительной версии Microsoft Edge][MicrosoftEdgePreviewChannels] в качестве браузера разработки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="c6a52-263">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="c6a52-264">Каналы с предварительными версиями доступны новейшие функции Разработчиков.</span><span class="sxs-lookup"><span data-stu-id="c6a52-264">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="c6a52-265">Совместная работа с помощью команды разработчиков Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="c6a52-265">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!-- <<../../_shared/devtools-feedback.md>>  

<<../../_shared/canary.md>>  

<<../../_shared/discover.md>> -->  

<!-- image links -->  

[ImagePerformanceToolKeyboardReaderImprovements]: ../../images/2020/01/a11y-performance-tool.msft.gif "Рис. 1. Средство для работы с разработчиками с помощью клавиатуры и средства чтения с экрана"  
[ImageLocalizedGerman]: ../../images/2020/01/localized-devtools.msft.png "Изображение 2. Разработчики в немецких"  
[ImageHintsTabWebhintExtension]: ../../images/2020/01/webhint-browser-extension.msft.png "Р. Вкладка "Подсказки" в Microsoft Edge DevTools, если установлено расширение веб-браузера"  
[Image3DView]: ../../images/2020/01/3dview.msft.png "Рис. 4. Представление трехмерных моделей в средствах разработчиков Microsoft Edge"  
[ImageElementsVisualStudioCode]: ../../images/2020/01/elements-for-edge.msft.png "Рис. 5. Инструмент "Элементы" в коде VS с помощью элементов расширения Microsoft Edge"  
[ImageDebuggerExtensionVisualStudioCode]: ../../images/2020/01/vscode-debugger.msft.png "Р. Дебугер для расширения Microsoft Edge в коде VS"  
[ImageWebhintVisualStudioCodeExtensionWorkspace]: ../../images/2020/01/webhint-vscode-extension.msft.png "Рис. Расширение webhint VS-кода, анализирующее TSX-файлы в коде VS"  
[ImageVisualStudioLaunchWebApp]: ../../images/2020/01/vs.msft.png "Рис. Visual Studio с возможностью запуска веб-приложения в Microsoft Edge Canary, Dev или Бета-версии"  
[ImageTrackingPrevention]: ../../images/2020/01/tracking-prevention.msft.png "Р. Сообщения в консоли при блокировке отслеживания блокируют доступ к хранилищу для отслеживания" 
[ImageMotoG4]: ../../images/2020/01/motog4.msft.png "Рис. 10: репликация просмотра порта ладони с G4" 
[ImageMotoG4Frame]: ../../images/2020/01/motog4frame.msft.png "Рис. 11: оборудование Moto G4" 
[ImageBlockedCookies]: ../../images/2020/01/blockedcookies.msft.png "Рис. 12: "Заблокированные файлы cookie" в панели приложений"
[ImageEditCookie]: ../../images/2020/01/editcookie.msft.png "Рис. 13: изменение значения cookie"
[ImageCopyFetch]: ../../images/2020/01/fetchcookies.msft.png "Рис. 14: копирование Node.js удаленного доступа"
[ImageManifestIcon]: ../../images/2020/01/manifesticons.msft.png "Рис. 15: значки в области манифеста"
[ImageEscapedString]: ../../images/2020/01/escapedstring.msft.png "Рисование 16: строка escaped"
[ImageUnescapedString]: ../../images/2020/01/unescapedstring.msft.png "Рисование 17: неизвестное значение"
[ImageSourcemapError]: ../../images/2020/01/sourcemap.msft.png "Рисунок 18: ошибка загрузки исходной карты в консоли"
[ImageSettings]: ../../images/2020/01/settings.msft.png "Рис. 19. Выключение прокрутки в прошлом конце файла в параметрах"
[ImageScroll]: ../../images/2020/01/scrollingsources.msft.png "Рис. Прокрутка в конце файла теперь отключена в панели "Источники""

<!-- links -->  

[DeviceToolbar]: ../../../device-mode/index.md#simulate-a-mobile-viewport "Рекламное представление для мобильных устройств с режимом устройства в режиме разработчика Microsoft Edge"
[DeviceFrame]: ../../../device-mode/index.md#show-device-frame "Выберите "Показать рамку устройства" для отображения физического профиля устройства по порту просмотра."
[CommandMenu]: ../../../command-menu/index.md "Команды с помощью меню «Разработчики» microsoft Edge"  
[ThrottleNetworkAndCpu]: ../../../device-mode/index.md#throttle-the-network-and-cpu "Регулирование сети и цпулу веб-университета, чтобы более тщательно оказались условия просмотра веб-сайта для мобильных устройств пользователей."
[crbug924693]: https://crbug.com/924693 "924693: запрос на добавление модуля G4 в список устройств"
[crbug1030258]: https://crbug.com/1030258 "1030258"
[crbug1026879]: https://crbug.com/1026879 "1026879: вкладка Cookie на консоли разработки больше не отображает приоритет"
[CookiesFields]: ../../../storage/cookies.md#fields "Поля в таблице Cookie"
[crbug1029826]: https://crbug.com/1029826 "1029826: вкладка "Сеть" -> щелкните правой кнопкой мыши, чтобы запросить -> копировать > копирования, похожие на копирование, не копируются"
[crbug985402]: https://crbug.com/985402 "985402: строки ошибок манифеста веб-приложения вызывают ошибки в веб-приложении"
[CSSContentDemo]: https://mathiasbynens.github.io/css-dbg-stories/css-escapes.html "Ролик для невольного содержимого CSS"
[Settings]: ../../../customize/index.md#settings "Настройка разработчиков Microsoft Edge с помощью параметров"
[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Публикация твита"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Новая проблема: MicrosoftDocs/edge-разработчики"  
[TheWebWeWant]: https://aka.ms/webwewant "Нужный веб-час"
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Каналы предварительной версии Microsoft Edge"  
[VisualStudioCodeDebuggerEdgeExtension]: ../../../../visual-studio-code/debugger-for-edge.md "Отладка расширения кода Microsoft Edge VS"  
[VisualStudioCodeElementEdgeExtension]: ../../../../visual-studio-code/elements-for-edge.md "Элементы расширения кода Microsoft Edge VS"  
[crbug963183]: https://crbug.com/963183 "963183 — средства для разработки не совместимо с WCAG"
[crbug941561]: https://crbug.com/941561 "941561 — локализация средств разработчиков"
[crbug987787]: https://crbug.com/987787 "987787 — Dom 3D View"
[AccessibilityInsights]: https://aka.ms/a11yinsights "Сведения о специальных возможностях"  
[MicrosoftEdgeInsiderAddons]: https://aka.ms/webhint/edge-extension "Microsoft Edge Insider Addons"  
[MicrosoftVisualStudio]: ../../../../visual-studio/index.md "Visual Studio"  
[MicrosoftVisualStudioDownloads]: https://aka.ms/vs/download "Скачивание Visual Studio 2019 для Windows \& для Mac"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Объектная модель документов (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "z-индекс | MDN"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools твиттер"
[VisualStudioCode]: https://aka.ms/vscode "Visual Studio код"  
[VisualStudioMarketplaceDebuggerEdge]: https://aka.ms/debugger4code "Отладка для Microsoft Edge — Visual Studio Marketplace"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://aka.ms/elements4code "Элементы для Microsoft Edge \(Chromium\) — Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://aka.ms/webhint4code "webhint — Visual Studio Marketplace"
[Webhint]: https://aka.ms/webhint "webhint"  
[WebhintBrowserExtension]: https://aka.ms/webhint/browser-extension "Расширение Webhint для браузера | документация веб-хинтертнера"  
[WebhintVisualStudioCodeExtension]: https://aka.ms/webhint/code-extension "Расширение веб-кода VS | документация веб-хинтертнера"  
[TrackingPrevention]: https://aka.ms/microsoftedge/tracking-prevention-blog "Улучшение отслеживания исправлений в записях блога Microsoft Edge"

> [!NOTE]
> <span data-ttu-id="c6a52-322">Части этой страницы изменяются на основе работы, созданных google и [предоставлением][GoogleSitePolicies] к ним общего доступа и используются в соответствии с терминами, которые описаны [в лицензии Creative Commons Attribution 4.0.][CCA4IL]</span><span class="sxs-lookup"><span data-stu-id="c6a52-322">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="c6a52-323">Исходная страница [here](https://developers.google.com/web/updates/2020/01/devtools/index) находится на сайте [Kayce Basques][KayceBasques] \(технический автор, Chrome DevTools & Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="c6a52-323">The original page is found [here](https://developers.google.com/web/updates/2020/01/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools & Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="c6a52-325">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="c6a52-325">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  