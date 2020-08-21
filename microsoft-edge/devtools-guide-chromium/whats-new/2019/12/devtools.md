---
title: Новые возможности в DevTools (Microsoft Edge 80)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 03fd78eddf54b68d072ba11401a897ad9f109058
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942143"
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

# <span data-ttu-id="abe2f-103">Новые возможности в DevTools (Microsoft Edge 80)</span><span class="sxs-lookup"><span data-stu-id="abe2f-103">What's new in DevTools (Microsoft Edge 80)</span></span>  

## <span data-ttu-id="abe2f-104">Объявления от команды разработчиков Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="abe2f-104">Announcements from the Microsoft Edge DevTools team</span></span>  

<span data-ttu-id="abe2f-105">В следующих разделах приведен список извещений, которые вы можете пропустить от команды разработчиков Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="abe2f-105">The following sections are a list of announcements you may have missed from the Microsoft Edge DevTools team!</span></span> <span data-ttu-id="abe2f-106">Ознакомьтесь с их новыми возможностями в DevTools, расширениях кодов VS и многом другом.</span><span class="sxs-lookup"><span data-stu-id="abe2f-106">Check them out to try new features in the DevTools, VS Code extensions, and more.</span></span>  <span data-ttu-id="abe2f-107">Чтобы быть в курсе всех последних и полезных функций в средствах разработчика, скачайте [каналы microsoft Edge][MicrosoftEdgePreviewChannels] и [отслеживайте нас в Твиттере.][EdgeDevToolsTwitterAccount]</span><span class="sxs-lookup"><span data-stu-id="abe2f-107">To stay up to date on all the latest and greatest features in your developer tools, download the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] and [follow us on Twitter][EdgeDevToolsTwitterAccount].</span></span>  

### <span data-ttu-id="abe2f-108">Улучшенные специальные возможности в средствах разработчиков</span><span class="sxs-lookup"><span data-stu-id="abe2f-108">Accessibility improvements to the DevTools</span></span>  

<span data-ttu-id="abe2f-109">Меняется 170 на хромомоблю изменилось 170 на Chromium на устранение контрастности цвета, клавиатуры и средства чтения с экрана в средствах разработчиков.</span><span class="sxs-lookup"><span data-stu-id="abe2f-109">The DevTools team has contributed 170 changes to Chromium to address high-impact color contrast, keyboard, and screen reader issues in the DevTools.</span></span>  <span data-ttu-id="abe2f-110">Каждый разработчик, созданный в Интернете, должен использовать DevTools.</span><span class="sxs-lookup"><span data-stu-id="abe2f-110">Every developer building the web should be able to use the DevTools.</span></span>  

> ##### <span data-ttu-id="abe2f-111">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="abe2f-111">Figure 1</span></span>  
> <span data-ttu-id="abe2f-112">Средство для работы с разработчиками с помощью клавиатуры и средства чтения с экрана</span><span class="sxs-lookup"><span data-stu-id="abe2f-112">The Performance tool in the DevTools with the keyboard navigation and screen reader improvements</span></span>  
> ![Средство для работы с разработчиками с помощью клавиатуры и средства чтения с экрана][ImagePerformanceToolKeyboardReaderImprovements]  

<span data-ttu-id="abe2f-114">Хотите узнать, как сделать веб-страницу доступным для всех пользователей?</span><span class="sxs-lookup"><span data-stu-id="abe2f-114">Want to learn how to make your web page accessible to all of your users?</span></span>  <span data-ttu-id="abe2f-115">Скачайте [средство "Аналитика][AccessibilityInsights] специальных возможностей" и [расширения][WebhintBrowserExtension] веб-сайта, касающиеся Microsoft Edge для начала работы.</span><span class="sxs-lookup"><span data-stu-id="abe2f-115">Download the [Accessibility Insights][AccessibilityInsights] and [webhint][WebhintBrowserExtension] extensions for Microsoft Edge to get started.</span></span>  

<span data-ttu-id="abe2f-116">Если вы используете средства чтения с экрана или клавиатуру для навигации по Разработчикам, отправьте нам свой отзыв, [твитирующий][PostTweetEdgeDevTools] нам или щелкнув [значок "Отправить](#getting-in-touch-with-microsoft-edge-devtools-team) отзыв".</span><span class="sxs-lookup"><span data-stu-id="abe2f-116">If you use screen readers or the keyboard to navigate around the DevTools, send us your feedback by [tweeting][PostTweetEdgeDevTools] at us or clicking the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon!</span></span>  

<span data-ttu-id="abe2f-117">Проблема с [#963183][crbug963183]</span><span class="sxs-lookup"><span data-stu-id="abe2f-117">Chromium issue [#963183][crbug963183]</span></span>  

### <span data-ttu-id="abe2f-118">Использование средств разработчиков на других языках</span><span class="sxs-lookup"><span data-stu-id="abe2f-118">Using the DevTools in other languages</span></span>  

<span data-ttu-id="abe2f-119">Многие разработчики используют другие средства разработчика, такие как StackOverflow и VS code, на своем родном языке, а не только на английском языке.</span><span class="sxs-lookup"><span data-stu-id="abe2f-119">Many developers use other developer tools, like StackOverflow and VS Code, in their native language, not just in English.</span></span>  <span data-ttu-id="abe2f-120">Мы рады сообщать локализацию для разработчиков DevTools, который теперь можно использовать на одном из 10 языков, кроме английского:</span><span class="sxs-lookup"><span data-stu-id="abe2f-120">We’re excited to announce localization for the DevTools, which you are now able to use in one of 10 languages besides English:</span></span>  

:::row:::
   :::column span="":::
      <span data-ttu-id="abe2f-121">Китайский \(упрощенное\) -  &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span><span class="sxs-lookup"><span data-stu-id="abe2f-121">Chinese \(Simplified\) - &#20013;&#25991;&#65288;&#31616;&#20307;&#65289;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="abe2f-122">Китайский \(традиционное\) -  &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span><span class="sxs-lookup"><span data-stu-id="abe2f-122">Chinese \(Traditional\) - &#20013;&#25991;&#65288;&#32321;&#39636;&#65289;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="abe2f-123">Французский (француз&#231;оси)</span><span class="sxs-lookup"><span data-stu-id="abe2f-123">French – fran&#231;ais</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="abe2f-124">Немецкий (отладка)</span><span class="sxs-lookup"><span data-stu-id="abe2f-124">German - deutsch</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="abe2f-125">Итальный (курсив)</span><span class="sxs-lookup"><span data-stu-id="abe2f-125">Italian - italiano</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="abe2f-126">Японский ( &#26085;&#26412;&#35486;</span><span class="sxs-lookup"><span data-stu-id="abe2f-126">Japanese - &#26085;&#26412;&#35486;</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="abe2f-127">Корейский ( &#54620;&#44397;&#50612;</span><span class="sxs-lookup"><span data-stu-id="abe2f-127">Korean - &#54620;&#44397;&#50612;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="abe2f-128">Португальский (португалия&#234;s)</span><span class="sxs-lookup"><span data-stu-id="abe2f-128">Portuguese - portugu&#234;s</span></span>
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="":::
      <span data-ttu-id="abe2f-129">Русский ( &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081; русский)</span><span class="sxs-lookup"><span data-stu-id="abe2f-129">Russian – &#1088;&#1091;&#1089;&#1089;&#1082;&#1080;&#1081;</span></span>
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="abe2f-130">Испанский (испания&#241;слишком много</span><span class="sxs-lookup"><span data-stu-id="abe2f-130">Spanish - espa&#241;ol</span></span>
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

<span data-ttu-id="abe2f-131">Перейдите к `edge://flags` пометке **"Включить локализованные средства разработчика" и** установите для него флаг **"Включить локализованные средства разработчика".**</span><span class="sxs-lookup"><span data-stu-id="abe2f-131">Navigate to `edge://flags` and set the **Enable localized Developer Tools** flag to **Enabled**.</span></span>  <span data-ttu-id="abe2f-132">Также задайте **для флага** экспертов разработчика значение **"Включено".**</span><span class="sxs-lookup"><span data-stu-id="abe2f-132">Also set the **Developer Tools experiments** flag to **Enabled**.</span></span>  <span data-ttu-id="abe2f-133">Перезапустите Microsoft Edge и откройте DevTools.</span><span class="sxs-lookup"><span data-stu-id="abe2f-133">Restart Microsoft Edge and open the DevTools.</span></span>  <!-- Press `F1` in the DevTools or go to Settings > Experiments and check the **Match browser language** checkbox.  -->  <span data-ttu-id="abe2f-134">Язык, который вы используете для Microsoft Edge, соответствующего языку, который вы `edge://settings/languages` используете.</span><span class="sxs-lookup"><span data-stu-id="abe2f-134">The DevTools match the language you use for Microsoft Edge in `edge://settings/languages`.</span></span>  

> ##### <span data-ttu-id="abe2f-135">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="abe2f-135">Figure 2</span></span>  
> <span data-ttu-id="abe2f-136">Средства разработчиков на немецком</span><span class="sxs-lookup"><span data-stu-id="abe2f-136">The DevTools in German</span></span>  
> ![Средства разработчиков на немецком][ImageLocalizedGerman]  

<span data-ttu-id="abe2f-138">Если вы хотите использовать разработчики для разработчиков, отличного от того, какие из доступных вам языков вы хотите использовать, [то разговор][PostTweetEdgeDevTools] можно нам или щелкните [значок "Обратная связь".](#getting-in-touch-with-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="abe2f-138">If you want to use the DevTools in a different language than the ones that are available, [tweet][PostTweetEdgeDevTools] at us or click the [Send Feedback](#getting-in-touch-with-microsoft-edge-devtools-team) icon.</span></span>  

<span data-ttu-id="abe2f-139">Проблема с [хромом#941561][crbug941561]</span><span class="sxs-lookup"><span data-stu-id="abe2f-139">Chromium issue [#941561][crbug941561]</span></span>  

### <span data-ttu-id="abe2f-140">расширение microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="abe2f-140">webhint Microsoft Edge extension</span></span>  

<span data-ttu-id="abe2f-141">Расширение веб-сайта Microsoft Edge позволяет легко просматривать веб-страницу и получать отзывы о специальных возможностях, совместимости браузера, безопасности, производительности и т. д. в средствах DevTools.</span><span class="sxs-lookup"><span data-stu-id="abe2f-141">The webhint Microsoft Edge extension allows you to easily scan your web page and get feedback on accessibility, browser compatibility, security, performance, and more within the DevTools.</span></span>  <span data-ttu-id="abe2f-142">Дополнительные сведения [https://webhint.io][Webhint] см. в дополнительных случаях.</span><span class="sxs-lookup"><span data-stu-id="abe2f-142">Read more at [https://webhint.io][Webhint].</span></span>  

> ##### <span data-ttu-id="abe2f-143">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="abe2f-143">Figure 3</span></span>  
> <span data-ttu-id="abe2f-144">Вкладка «Подсказки» в приложении DevTools при установленном расширении браузера</span><span class="sxs-lookup"><span data-stu-id="abe2f-144">The Hints tab in the DevTools when the webhint browser extension is installed</span></span>  
> ![Вкладка «Подсказки» в приложении DevTools при установленном расширении браузера][ImageHintsTabWebhintExtension]  

<span data-ttu-id="abe2f-146">[Попробуйте расширение веб-браузера в Microsoft Edge.][MicrosoftEdgeInsiderAddons]</span><span class="sxs-lookup"><span data-stu-id="abe2f-146">[Try the webhint browser extension in Microsoft Edge][MicrosoftEdgeInsiderAddons].</span></span>  <span data-ttu-id="abe2f-147">После установки расширения откройте вкладку DevTools и выберите вкладку "Подсказки".  В этом окне выполните настраиваемое сканирование сайта.</span><span class="sxs-lookup"><span data-stu-id="abe2f-147">Once you install the extension, open the DevTools and select the Hints tab.  From here, run a customizable site scan.</span></span>  <span data-ttu-id="abe2f-148">Чтобы узнать [больше webhint.io, нажмите][WebhintBrowserExtension] дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="abe2f-148">Head over to [webhint.io][WebhintBrowserExtension] to learn more.</span></span>

### <span data-ttu-id="abe2f-149">Трехмерное представление</span><span class="sxs-lookup"><span data-stu-id="abe2f-149">3D View</span></span>  

<span data-ttu-id="abe2f-150">Используйте **трехмерное** представление для отладки веб-приложения путем перехода к объектной модели [документов \(DOM\)][MDNDocumentObjectModel] или [стопки z-индекса.][MDNZIndex]</span><span class="sxs-lookup"><span data-stu-id="abe2f-150">Use the **3D View** to debug your web application by navigating through the [Document Object Model \(DOM\)][MDNDocumentObjectModel] or the [z-index][MDNZIndex] stacking context.</span></span>  

> ##### <span data-ttu-id="abe2f-151">Рисунок4</span><span class="sxs-lookup"><span data-stu-id="abe2f-151">Figure 4</span></span>  
> <span data-ttu-id="abe2f-152">Трехмерное представление в средствах разработчиков</span><span class="sxs-lookup"><span data-stu-id="abe2f-152">The 3D View in the DevTools</span></span>  
> ![Трехмерное представление в средствах разработчиков][Image3DView]  

<span data-ttu-id="abe2f-154">Для доступа к трехмерному представлению перейдите к трехмерному представлению и убедитесь, что для флага экспертов для `edge://flags` разработчиков **установлено значение "Включено".** **Developer Tools experiments**</span><span class="sxs-lookup"><span data-stu-id="abe2f-154">To access the 3D View, navigate to `edge://flags` and ensure that the **Developer Tools experiments** flag is set to **Enabled**.</span></span>  <span data-ttu-id="abe2f-155">Перезапустите Microsoft Edge и откройте DevTools.</span><span class="sxs-lookup"><span data-stu-id="abe2f-155">Restart Microsoft Edge and open the DevTools.</span></span>  <span data-ttu-id="abe2f-156">Нажмите `F1` в devTools или перейдите в раздел **"Параметры",** перейдите в **раздел "Эксперименты"** и установите **флажок "Включить трехмерное представление".**</span><span class="sxs-lookup"><span data-stu-id="abe2f-156">Press `F1` in the DevTools or go to **Settings**, navigate to **Experiments** section, and check the **Enable 3D View** checkbox.</span></span>  <span data-ttu-id="abe2f-157">Теперь нажмите `Ctrl`  +  `Shift`  +  `P` клавишу ввод в **трехмерном представлении** и выберите **"Показать трехмерное представление".**</span><span class="sxs-lookup"><span data-stu-id="abe2f-157">Now, press `Ctrl` + `Shift` + `P`, type in **3D View** and select **Show 3D View**.</span></span>  

<span data-ttu-id="abe2f-158">Мы работаем над элементом, и мы добавляем дополнительные функции в трехмерное представление, чтобы отправить [нам свой отзыв.](#getting-in-touch-with-microsoft-edge-devtools-team)</span><span class="sxs-lookup"><span data-stu-id="abe2f-158">We're working on the UI and adding more functionality to the 3D View so please send us your [feedback](#getting-in-touch-with-microsoft-edge-devtools-team).</span></span>  

<span data-ttu-id="abe2f-159">[Проблема][crbug987787] с #987787 хромом</span><span class="sxs-lookup"><span data-stu-id="abe2f-159">Chromium issue [#987787][crbug987787]</span></span>

### <span data-ttu-id="abe2f-160">Visual Studio расширения кода</span><span class="sxs-lookup"><span data-stu-id="abe2f-160">Visual Studio Code extensions</span></span>  

<span data-ttu-id="abe2f-161">Команда Разработчиков также выпущена [некоторые расширения для Visual Studio Code \(VS Code\),][VisualStudioCode] которые позволяют использовать возможности DevTools напрямую из текстового редактора!</span><span class="sxs-lookup"><span data-stu-id="abe2f-161">The DevTools team has also released some extensions for [Visual Studio Code \(VS Code\)][VisualStudioCode] that let you use the power of the DevTools directly from your text editor!</span></span> <span data-ttu-id="abe2f-162">Ознакомьтесь с расширениями ниже.</span><span class="sxs-lookup"><span data-stu-id="abe2f-162">Check out the extensions below:</span></span>  

#### <span data-ttu-id="abe2f-163">Элементы Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="abe2f-163">Elements for Microsoft Edge</span></span>  

<span data-ttu-id="abe2f-164">Используйте инструмент "Элементы" в коде VS, добавив расширение ["Элементы" для Microsoft Edge \(Chromium\)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] VS CodeS.</span><span class="sxs-lookup"><span data-stu-id="abe2f-164">Use the Elements tool from within VS Code by adding the [Elements for Microsoft Edge \(Chromium\)][VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension] VS Code extension.</span></span>  

> ##### <span data-ttu-id="abe2f-165">Рисунок 5</span><span class="sxs-lookup"><span data-stu-id="abe2f-165">Figure 5</span></span>  
> <span data-ttu-id="abe2f-166">Инструмент "Элементы" в коде VS с использованием расширения "Элементы" для Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="abe2f-166">The Elements tool in VS Code using the Elements for Microsoft Edge extension</span></span>  
> ![Инструмент "Элементы" в коде VS с использованием расширения "Элементы" для Microsoft Edge][ImageElementsVisualStudioCode]  

<span data-ttu-id="abe2f-168">Дополнительные сведения [см. в статье "Элементы расширения кода Microsoft Edge VS".][VisualStudioCodeElementEdgeExtension]</span><span class="sxs-lookup"><span data-stu-id="abe2f-168">For more information, check out [Elements for Microsoft Edge VS Code extension][VisualStudioCodeElementEdgeExtension].</span></span>  

#### <span data-ttu-id="abe2f-169">Отладка для Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="abe2f-169">Debugger for Microsoft Edge</span></span>  

<span data-ttu-id="abe2f-170">С [расширением][VisualStudioMarketplaceDebuggerEdge] отладки для Microsoft Edge VS отладка JavaScript работает в Microsoft Edge непосредственно из кода VS Code!</span><span class="sxs-lookup"><span data-stu-id="abe2f-170">With the [Debugger for Microsoft Edge][VisualStudioMarketplaceDebuggerEdge] VS Code extension, debug JavaScript running in Microsoft Edge directly from VS Code!</span></span>  

> ##### <span data-ttu-id="abe2f-171">Рисунок6</span><span class="sxs-lookup"><span data-stu-id="abe2f-171">Figure 6</span></span>  
> <span data-ttu-id="abe2f-172">Отладка расширения Microsoft Edge в коде VS</span><span class="sxs-lookup"><span data-stu-id="abe2f-172">The Debugger for Microsoft Edge Extension in VS Code</span></span>  
> ![Отладка расширения Microsoft Edge в коде VS][ImageDebuggerExtensionVisualStudioCode]  

<span data-ttu-id="abe2f-174">Дополнительные сведения см. в [статье о том, как отладить Microsoft Edge от кода VS.][VisualStudioCodeDebuggerEdgeExtension]</span><span class="sxs-lookup"><span data-stu-id="abe2f-174">For more information, check out [how to debug Microsoft Edge from VS Code][VisualStudioCodeDebuggerEdgeExtension].</span></span>  

#### <span data-ttu-id="abe2f-175">webhint</span><span class="sxs-lookup"><span data-stu-id="abe2f-175">webhint</span></span>  

<span data-ttu-id="abe2f-176">[Расширение веб-кода][VisualStudioMarketplaceWebhintExtension] VS используется для `webhint` улучшения веб-страницы во время его письма.</span><span class="sxs-lookup"><span data-stu-id="abe2f-176">The [webhint][VisualStudioMarketplaceWebhintExtension] VS Code extension uses `webhint` to improve your web page while you're writing it!</span></span> <span data-ttu-id="abe2f-177">Это расширение выполняется, а отчеты диагностики для файлов рабочей области на основе `webhint` анализа.</span><span class="sxs-lookup"><span data-stu-id="abe2f-177">This extension runs and reports diagnostics on your workspace files based on `webhint` analysis.</span></span>  

> ##### <span data-ttu-id="abe2f-178">Рисунок7</span><span class="sxs-lookup"><span data-stu-id="abe2f-178">Figure 7</span></span>  
> <span data-ttu-id="abe2f-179">Расширение веб-кода VS с кодом VS</span><span class="sxs-lookup"><span data-stu-id="abe2f-179">The webhint VS Code extension analyzing a .tsx file in VS Code</span></span>  
> ![Расширение веб-кода VS с кодом VS][ImageWebhintVisualStudioCodeExtensionWorkspace]  

<span data-ttu-id="abe2f-181">[Дополнительные сведения о расширении веб-кода VS кода VS.][WebhintVisualStudioCodeExtension]</span><span class="sxs-lookup"><span data-stu-id="abe2f-181">[Learn more about the VS Code webhint extension][WebhintVisualStudioCodeExtension].</span></span>  

### <span data-ttu-id="abe2f-182">Visual Studio интеграции</span><span class="sxs-lookup"><span data-stu-id="abe2f-182">Visual Studio integration</span></span>
<span data-ttu-id="abe2f-183">В Visual Studio 2019 г. и более поздних версий используйте отладку Visual Studio для отладки JavaScript в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="abe2f-183">In Visual Studio 2019 version 16.2 or later, use the Visual Studio debugger to debug JavaScript running in Microsoft Edge.</span></span>  <span data-ttu-id="abe2f-184">[Скачайте Visual Studio 2019 г.,][MicrosoftVisualStudioDownloads] чтобы опробовать эту функцию!</span><span class="sxs-lookup"><span data-stu-id="abe2f-184">[Download Visual Studio 2019][MicrosoftVisualStudioDownloads] to try this feature out!</span></span>  

> ##### <span data-ttu-id="abe2f-185">Рисунок8</span><span class="sxs-lookup"><span data-stu-id="abe2f-185">Figure 8</span></span>  
> <span data-ttu-id="abe2f-186">Visual Studio с возможностью запустить веб-приложение в Microsoft Edge Canary, Dev или бета-версии</span><span class="sxs-lookup"><span data-stu-id="abe2f-186">Visual Studio with the option to launch your web app in Microsoft Edge Canary, Dev, or Beta</span></span>  
> ![Visual Studio с возможностью запустить веб-приложение в Microsoft Edge Canary, Dev или бета-версии][ImageVisualStudioLaunchWebApp]  

<span data-ttu-id="abe2f-188">[Прочтите наш блог, чтобы узнать, как отладку Microsoft Edge отладка Microsoft Edge Visual Studio.][MicrosoftVisualStudioBlogDebugJavascript]</span><span class="sxs-lookup"><span data-stu-id="abe2f-188">[Read our blog post to learn how to debug Microsoft Edge from Visual Studio][MicrosoftVisualStudioBlogDebugJavascript].</span></span>  

### <span data-ttu-id="abe2f-189">Сообщения консоли отслеживания</span><span class="sxs-lookup"><span data-stu-id="abe2f-189">Tracking prevention Console messages</span></span>  

<span data-ttu-id="abe2f-190">Предотвращение отслеживания — это уникальная функция в Microsoft Edge, которая защищает вас при посещении веб-сайтов, которые вы не посещали.</span><span class="sxs-lookup"><span data-stu-id="abe2f-190">Tracking prevention is a unique feature in Microsoft Edge that protects you from being tracked by websites you haven't visited before.</span></span>  <span data-ttu-id="abe2f-191">По умолчанию этот режим предотвращает балансировку сбалансированного отслеживания, который блокирует сторонние средства отслеживания сторонних средств и известные вредоносные отслеживания для обеспечения балансировки конфиденциальности и совместимости веб-сайтов.</span><span class="sxs-lookup"><span data-stu-id="abe2f-191">The default tracking prevention setting is Balanced mode, which blocks 3rd party trackers and known malicious trackers for an experience that balances privacy and web compatibility.</span></span>  <span data-ttu-id="abe2f-192">Чтобы получить более подробные сведения о совместимости веб-страницы, когда заблокированы некоторые средства отслеживания, также мы добавили предупреждения в консоль, если средство отслеживания заблокирован.</span><span class="sxs-lookup"><span data-stu-id="abe2f-192">To give you more insight into the compatibility of your web page when certain trackers are blocked, we've also added warning messages in the Console when a tracker is blocked.</span></span>  

> ##### <span data-ttu-id="abe2f-193">Рисунок9</span><span class="sxs-lookup"><span data-stu-id="abe2f-193">Figure 9</span></span>  
> <span data-ttu-id="abe2f-194">Сообщения в консоли при отслеживании блокируют доступ к хранилищу для отслеживания</span><span class="sxs-lookup"><span data-stu-id="abe2f-194">Messages in the Console when tracking prevention blocks access to storage for a tracker</span></span>  
> ![Сообщения в консоли при отслеживании блокируют доступ к хранилищу для отслеживания][ImageTrackingPrevention]  

<span data-ttu-id="abe2f-196">[Узнайте больше о предотвращении отслеживания и балансе между конфиденциальностью и веб-совместимостью.][TrackingPrevention]</span><span class="sxs-lookup"><span data-stu-id="abe2f-196">[Read more about tracking prevention and the balance between privacy and web compatibility][TrackingPrevention].</span></span>  

## <span data-ttu-id="abe2f-197">Извещения из проекта Chromium</span><span class="sxs-lookup"><span data-stu-id="abe2f-197">Announcements from the Chromium project</span></span>  

<span data-ttu-id="abe2f-198">В следующих разделах описаны дополнительные функции, доступные в Microsoft Edge 80, которые были внесены в проект Chromium.</span><span class="sxs-lookup"><span data-stu-id="abe2f-198">The following sections announce additional features available in Microsoft Edge 80 that were contributed to the open source Chromium project.</span></span>  

### <span data-ttu-id="abe2f-199">Поддержка разрешений и объявлений учебных заводов в консоли</span><span class="sxs-lookup"><span data-stu-id="abe2f-199">Support for let and class redeclarations in the Console</span></span>  

<span data-ttu-id="abe2f-200">Теперь консоль теперь поддерживает объявления и `let` `class` инструкций.</span><span class="sxs-lookup"><span data-stu-id="abe2f-200">The Console now supports redeclarations of `let` and `class` statements.</span></span>  <span data-ttu-id="abe2f-201">Невозможность перестать стать часто объявлений для веб-разработчиков, которые используют консоль для эксперимента с новым кодом JavaScript.</span><span class="sxs-lookup"><span data-stu-id="abe2f-201">The inability to redeclare was a common annoyance for web developers who use the Console to experiment with new JavaScript code.</span></span>  

> [!WARNING]
> <span data-ttu-id="abe2f-202">При объявлении или заполнением отдельных данных консоли или вращения каждого входного `let` консоли по-прежнему `class` приводит к причинам. `SyntaxError`</span><span class="sxs-lookup"><span data-stu-id="abe2f-202">Redeclaring a `let` or `class` statement in a script outside of the Console or within a single Console input still causes a `SyntaxError`.</span></span>  

<span data-ttu-id="abe2f-203">Например, при отключении локальной переменной `let` с помощью консоли состоит из следующей ошибки:</span><span class="sxs-lookup"><span data-stu-id="abe2f-203">For example, previously, when redeclaring a local variable with `let`, the Console threw an error:</span></span>  

> ##### <span data-ttu-id="abe2f-204">Рисунок 10</span><span class="sxs-lookup"><span data-stu-id="abe2f-204">Figure 10</span></span>  
> <span data-ttu-id="abe2f-205">Консоль в Microsoft Edge 79 показывает, что возможность отклонения не удается завершить</span><span class="sxs-lookup"><span data-stu-id="abe2f-205">The Console in Microsoft Edge 79 showing that the let redeclaration fails</span></span>  
> ![Консоль в Microsoft Edge 79 показывает, что возможность отклонения не удается завершить][ImageConsoleRedeclarationFails]  

<span data-ttu-id="abe2f-207">Теперь консоль позволяет отложить перезаку.</span><span class="sxs-lookup"><span data-stu-id="abe2f-207">Now, the Console allows the redeclaration:</span></span>  

> ##### <span data-ttu-id="abe2f-208">Рисунок11</span><span class="sxs-lookup"><span data-stu-id="abe2f-208">Figure 11</span></span>  
> <span data-ttu-id="abe2f-209">Консоль в Microsoft Edge 80 показывает, что разрешение отмены отмены</span><span class="sxs-lookup"><span data-stu-id="abe2f-209">The Console in Microsoft Edge 80 showing that the let redeclaration succeeds</span></span>  
> ![Консоль в Microsoft Edge 80 показывает, что разрешение отмены отмены][ImageConsoleRedeclarationSucceeds]  

<span data-ttu-id="abe2f-211">Проблема с #1004193 chromium [#1004193][crbug1004193]</span><span class="sxs-lookup"><span data-stu-id="abe2f-211">Chromium issue [#1004193][crbug1004193]</span></span>  

### <span data-ttu-id="abe2f-212">Улучшенный отладка веб-сайта</span><span class="sxs-lookup"><span data-stu-id="abe2f-212">Improved WebAssembly debugging</span></span>  

<span data-ttu-id="abe2f-213">DevTools начал поддерживать [стандарт отладки DWARF,][DwarfHome]которая повышает поддержку пошагового кода, настройки остальных точек и устранить расшифровку на локальных языках в разработчиках.</span><span class="sxs-lookup"><span data-stu-id="abe2f-213">DevTools has started to support the [DWARF Debugging Standard][DwarfHome], which means increased support for stepping over code, setting breakpoints, and resolving stack traces in your source languages within DevTools.</span></span>  

<!-- [TODO: Add this link back] -->  
<!--Check out [Improved WebAssembly debugging in Microsoft Edge DevTools][201912Webassembly] for the full story.  -->  

<!-- [TODO: Replace this image with screenshot in Edge] -->  
<!--
> ##### Figure  
> The new DWARF-powered WebAssembly debugging  
> ![The new DWARF-powered WebAssembly debugging][ImageDwarfPoweredWebAssemblyDebugging]  
-->  

### <span data-ttu-id="abe2f-214">Обновления панели сети</span><span class="sxs-lookup"><span data-stu-id="abe2f-214">Network panel updates</span></span>  

#### <span data-ttu-id="abe2f-215">Запрос инициатора китой на вкладке "Инициатор"</span><span class="sxs-lookup"><span data-stu-id="abe2f-215">Request Initiator Chains in the Initiator tab</span></span>  

<span data-ttu-id="abe2f-216">Теперь вы можете просмотреть инициаторы и зависимости сетевого запроса в виде вложенного списка.</span><span class="sxs-lookup"><span data-stu-id="abe2f-216">You are now able to view the initiators and dependencies of a network request as a nested list.</span></span>  <span data-ttu-id="abe2f-217">Это поможет понять, почему был запрашивается запрашиваемый ресурс, и какую активность сети выполнялись определенным ресурсом \(например, сценарий\).</span><span class="sxs-lookup"><span data-stu-id="abe2f-217">This may help you understand why a resource was requested, or what network activity a certain resource \(such as a script\) caused.</span></span>  

> ##### <span data-ttu-id="abe2f-218">Рисунок12</span><span class="sxs-lookup"><span data-stu-id="abe2f-218">Figure 12</span></span>  
> <span data-ttu-id="abe2f-219">Цепочка запросов запроса на вкладке "Инициатор"</span><span class="sxs-lookup"><span data-stu-id="abe2f-219">A Request Initiator Chain in the Initiator tab</span></span>  
> ![Цепочка запросов запроса на вкладке "Инициатор"][ImageRequestInitiatorChain]  

<span data-ttu-id="abe2f-221">После [ведения журнала действий в сети][DevToolsNetworkIndex]на панели "Сеть" щелкните ресурс и перейдите на вкладку **"Инициатор запроса"** для просмотра крайнего **инициатива запроса:**</span><span class="sxs-lookup"><span data-stu-id="abe2f-221">After [logging network activity in the Network panel][DevToolsNetworkIndex], click a resource and then go to the **Initiator** tab to view the **Request Initiator Chain**:</span></span>  

*   <span data-ttu-id="abe2f-222">**Инвертированный ресурс** выделен полужирным начертанием.</span><span class="sxs-lookup"><span data-stu-id="abe2f-222">The **inspected resource** is bold.</span></span>  <span data-ttu-id="abe2f-223">На снимке экрана выше `ai.2.min.js` является проверенный ресурс.</span><span class="sxs-lookup"><span data-stu-id="abe2f-223">In the screenshot above, `ai.2.min.js` is the inspected resource.</span></span>  
*   <span data-ttu-id="abe2f-224">Ресурсами над проверенным ресурсом являются **инициаторы.**</span><span class="sxs-lookup"><span data-stu-id="abe2f-224">The resources above the inspected resource are the **initiators**.</span></span>  <span data-ttu-id="abe2f-225">На снимке экрана выше является `https://www.microsoftedgeinsider.com` инициатор. `ai.2.min.js`</span><span class="sxs-lookup"><span data-stu-id="abe2f-225">In the screenshot above, `https://www.microsoftedgeinsider.com` is the initiator of `ai.2.min.js`.</span></span>  <span data-ttu-id="abe2f-226">Другими словами, `https://www.microsoftedgeinsider.com` вызвано сетевым `ai.2.min.js` запросом.</span><span class="sxs-lookup"><span data-stu-id="abe2f-226">In other words, `https://www.microsoftedgeinsider.com` caused the network request for `ai.2.min.js`.</span></span>  
*   <span data-ttu-id="abe2f-227">Ресурсы, которые не будут проверяться, являются **зависимостями.**</span><span class="sxs-lookup"><span data-stu-id="abe2f-227">The resources below the inspected resource are the **dependencies**.</span></span>  <span data-ttu-id="abe2f-228">На снимке экрана выше `https://dc.services.visualstudio.com/v2/track` представляет собой `ai.2.min.js` зависимость.</span><span class="sxs-lookup"><span data-stu-id="abe2f-228">In the screenshot above, `https://dc.services.visualstudio.com/v2/track` is a dependency of `ai.2.min.js`.</span></span>  <span data-ttu-id="abe2f-229">Другими словами, `ai.2.min.js` вызвано сетевым `https://dc.services.visualstudio.com/v2/track` запросом.</span><span class="sxs-lookup"><span data-stu-id="abe2f-229">In other words, `ai.2.min.js` caused the network request for `https://dc.services.visualstudio.com/v2/track`.</span></span>  

> [!NOTE]
> <span data-ttu-id="abe2f-230">К ним также можно получить доступ к сведениям инициативе и зависимостям, удерживая нажатой кнопку мыши, а затем `Shift` наводя указатель мыши на ресурсы сети.</span><span class="sxs-lookup"><span data-stu-id="abe2f-230">Initiator and dependency information may also be accessed by holding `Shift` and then hovering over network resources.</span></span>  <span data-ttu-id="abe2f-231">[Просмотреть инициативив и зависимости.][DevToolsNetworkReferenceViewInitiatorsDependencies]</span><span class="sxs-lookup"><span data-stu-id="abe2f-231">See [View initiators and dependencies][DevToolsNetworkReferenceViewInitiatorsDependencies].</span></span>  

<span data-ttu-id="abe2f-232">Проблема с chromium [#842488][crbug842488]</span><span class="sxs-lookup"><span data-stu-id="abe2f-232">Chromium issue [#842488][crbug842488]</span></span>  

#### <span data-ttu-id="abe2f-233">Выделение выбранного сетевого запроса в обзоре</span><span class="sxs-lookup"><span data-stu-id="abe2f-233">Highlight the selected network request in the Overview</span></span>  

<span data-ttu-id="abe2f-234">После выбора сетевого ресурса для проверки панель сети панель «Сеть» поместит синюю границу вокруг **него в представлении "Обзор".**</span><span class="sxs-lookup"><span data-stu-id="abe2f-234">After you click a network resource in order to inspect it, the Network panel now puts a blue border around that resource in the **Overview**.</span></span>  <span data-ttu-id="abe2f-235">Это поможет вам определение того, происходит ли сетевое или позднее, чем ожидалось.</span><span class="sxs-lookup"><span data-stu-id="abe2f-235">This is able to help you detect if the network request is happening earlier or later than expected.</span></span>  

> ##### <span data-ttu-id="abe2f-236">Рисунок13</span><span class="sxs-lookup"><span data-stu-id="abe2f-236">Figure 13</span></span>  
> <span data-ttu-id="abe2f-237">Область обзора с проверенным ресурсом</span><span class="sxs-lookup"><span data-stu-id="abe2f-237">The Overview pane highlighting the inspected resource</span></span>  
> ![Область обзора с проверенным ресурсом][ImageOverviewPaneInspectedResource]  

<span data-ttu-id="abe2f-239">[Проблема][crbug988253] с #988253 chromium #988253</span><span class="sxs-lookup"><span data-stu-id="abe2f-239">Chromium issue [#988253][crbug988253]</span></span>  

#### <span data-ttu-id="abe2f-240">Столбцы URL-адресов и путей на панели сети</span><span class="sxs-lookup"><span data-stu-id="abe2f-240">URL and path columns in the Network panel</span></span>  

<span data-ttu-id="abe2f-241">Новые **столбцы "Путь"** **и "URL-адрес"** на панели network (Сетевой ресурс) можно просмотреть абсолютный или полный URL-адрес каждого сетевого ресурса. **Network**</span><span class="sxs-lookup"><span data-stu-id="abe2f-241">Use the new **Path** and **URL** columns in the **Network** panel to see the absolute path or full URL of each network resource.</span></span>  

> ##### <span data-ttu-id="abe2f-242">Рисунок14</span><span class="sxs-lookup"><span data-stu-id="abe2f-242">Figure 14</span></span>  
> <span data-ttu-id="abe2f-243">Новые столбцы путей и URL-адреса на панели «Сетевой сети»</span><span class="sxs-lookup"><span data-stu-id="abe2f-243">The new Path and URL columns in the Network panel</span></span>  
> ![Новые столбцы путей и URL-адреса на панели «Сетевой сети»][ImagePathNetworkPanel]  

<span data-ttu-id="abe2f-245">Щелкните правой кнопкой **мыши заголовок таблицы "Каскадная"** и выберите **путь или** **URL-адрес,** чтобы отобразить новые столбцы.</span><span class="sxs-lookup"><span data-stu-id="abe2f-245">Right-click the **Waterfall** table header and select **Path** or **URL** to show the new columns.</span></span>  

<span data-ttu-id="abe2f-246">Проблема с #993366 chromium [#993366][crbug993366]</span><span class="sxs-lookup"><span data-stu-id="abe2f-246">Chromium issue [#993366][crbug993366]</span></span>  

#### <span data-ttu-id="abe2f-247">Обновленные строки агента пользователя</span><span class="sxs-lookup"><span data-stu-id="abe2f-247">Updated User-Agent strings</span></span>  

<span data-ttu-id="abe2f-248">DevTools поддерживает установку пользовательской строки агента на вкладке **"Условия сети".**  Строка пользователя влияет на заголовок HTTP, прикрепленный `User-Agent` к сетевым ресурсам, а также `navigator.userAgent` значение.</span><span class="sxs-lookup"><span data-stu-id="abe2f-248">DevTools supports setting a custom User-Agent string through the **Network Conditions** tab.  The User-Agent string affects the `User-Agent` HTTP header attached to network resources, and also the value of `navigator.userAgent`.</span></span>  

<span data-ttu-id="abe2f-249">Предопределенные строки пользователя агента были обновлены с учептными версиями с овременными версиями браузера.</span><span class="sxs-lookup"><span data-stu-id="abe2f-249">The predefined User-Agent strings have been updated to reflect modern browser versions.</span></span>  

> ##### <span data-ttu-id="abe2f-250">Рисунок15</span><span class="sxs-lookup"><span data-stu-id="abe2f-250">Figure 15</span></span>  
> <span data-ttu-id="abe2f-251">Меню "Агент пользователя" на вкладке "Сетевые условия"</span><span class="sxs-lookup"><span data-stu-id="abe2f-251">The User Agent menu in the Network Conditions tab</span></span>  
> ![Меню "Агент пользователя" на вкладке "Сетевые условия"][ImageUserAgentNetworkConditionsTab]  

<span data-ttu-id="abe2f-253">Для доступа **к сетевому** [условию откройте меню команд][DevToolsCommandMenuIndex] и выполните `Show Network Conditions` команду.</span><span class="sxs-lookup"><span data-stu-id="abe2f-253">To access **Network Conditions**, [open the Command Menu][DevToolsCommandMenuIndex] and run the `Show Network Conditions` command.</span></span>  

> [!NOTE]
> <span data-ttu-id="abe2f-254">Вы также можете [указать строки пользователя-агенты в режиме устройства.][DevToolsDeviceModeIndex]</span><span class="sxs-lookup"><span data-stu-id="abe2f-254">You may also [set User-Agent strings in Device Mode][DevToolsDeviceModeIndex].</span></span>  

<span data-ttu-id="abe2f-255">Проблема с [#1029031][crbug1029031] хромеум#1029031</span><span class="sxs-lookup"><span data-stu-id="abe2f-255">Chromium issue [#1029031][crbug1029031]</span></span>  

### <span data-ttu-id="abe2f-256">Обновления панели аудита</span><span class="sxs-lookup"><span data-stu-id="abe2f-256">Audits panel updates</span></span>  

#### <span data-ttu-id="abe2f-257">Новый элемент управления конфигурацией</span><span class="sxs-lookup"><span data-stu-id="abe2f-257">New configuration UI</span></span>  

<span data-ttu-id="abe2f-258">В этом окне конфигурации появилась новый, обязательное дизайн, и параметры регулирования упрощены.</span><span class="sxs-lookup"><span data-stu-id="abe2f-258">The configuration UI has a new, responsive design, and the throttling configuration options have been simplified.</span></span>  <span data-ttu-id="abe2f-259">Дополнительные [сведения об][GitHubGoogleChromeDevToolsAuditsPanelThrottling] изменениях в элементе управления регулирования см. в разделе регулирования на панели регулирования.</span><span class="sxs-lookup"><span data-stu-id="abe2f-259">See [Audits Panel Throttling][GitHubGoogleChromeDevToolsAuditsPanelThrottling] for more information on the throttling UI changes.</span></span>  

> ##### <span data-ttu-id="abe2f-260">Рисунок16</span><span class="sxs-lookup"><span data-stu-id="abe2f-260">Figure 16</span></span>  
> <span data-ttu-id="abe2f-261">Новый элемент управления конфигурацией</span><span class="sxs-lookup"><span data-stu-id="abe2f-261">The new configuration UI</span></span>  
> ![Новый элемент управления конфигурацией][ImageConfigurationUI]  

### <span data-ttu-id="abe2f-263">Обновления вкладки по критериев</span><span class="sxs-lookup"><span data-stu-id="abe2f-263">Coverage tab updates</span></span>  

#### <span data-ttu-id="abe2f-264">Режимы охвата для функций или режимы блока на функции</span><span class="sxs-lookup"><span data-stu-id="abe2f-264">Per-function or per-block coverage modes</span></span>  

<span data-ttu-id="abe2f-265">На [вкладке "Утверждения"][DevToolsCoverageIndex] есть новое раскрывающееся меню, в котором можно указать, следует ли собирать данные о покрытии кода для **каждой функции** или **каждого блока.**</span><span class="sxs-lookup"><span data-stu-id="abe2f-265">The [Coverage tab][DevToolsCoverageIndex] has a new dropdown menu that lets you specify whether code coverage data should be collected **per function** or **per block**.</span></span>  <span data-ttu-id="abe2f-266">**Перебор по** блоку более подробно, но и дальнейшее собирать его.</span><span class="sxs-lookup"><span data-stu-id="abe2f-266">**Per block** coverage is more detailed but also far more expensive to collect.</span></span>  <span data-ttu-id="abe2f-267">По умолчанию в DevTools покрывается **функция,** покрывающая функцию на тот или иной.</span><span class="sxs-lookup"><span data-stu-id="abe2f-267">DevTools uses **per function** coverage by default now.</span></span>  

> [!CAUTION]
> <span data-ttu-id="abe2f-268">В HTML-файлах могут зависеть от того, используется ли функция **или** **режим блокирования.**</span><span class="sxs-lookup"><span data-stu-id="abe2f-268">You may see large code coverage differences in HTML files depending on whether you use **per function** or **per block** mode.</span></span>  <span data-ttu-id="abe2f-269">При работе **с функциями** встроенные сценарии HTML-файлы воспринимаются как функции.</span><span class="sxs-lookup"><span data-stu-id="abe2f-269">When using **per function** mode, inline scripts in HTML files are treated as functions.</span></span>  <span data-ttu-id="abe2f-270">Если сценарий выполняется во всех, devTools помечает весь сценарий как использовавшийся код.</span><span class="sxs-lookup"><span data-stu-id="abe2f-270">If the script runs at all then DevTools marks the entire script as used code.</span></span>  <span data-ttu-id="abe2f-271">Только если сценарий выполняется во всех DevTools, помечается сценарием как неиспользуемый код.</span><span class="sxs-lookup"><span data-stu-id="abe2f-271">Only if the script does not run at all does DevTools mark the script as unused code.</span></span>  

> ##### <span data-ttu-id="abe2f-272">Рисунок17</span><span class="sxs-lookup"><span data-stu-id="abe2f-272">Figure 17</span></span>  
> <span data-ttu-id="abe2f-273">Раскрывающееся меню режима перекрытия</span><span class="sxs-lookup"><span data-stu-id="abe2f-273">The coverage mode dropdown menu</span></span>  
> ![Раскрывающееся меню режима перекрытия][ImageCoverageMode]  

#### <span data-ttu-id="abe2f-275">Кoveroverage теперь должен быть инициировано перезагрузкой страницы</span><span class="sxs-lookup"><span data-stu-id="abe2f-275">Coverage must now be initiated by a page reload</span></span>  

<span data-ttu-id="abe2f-276">Переключение кода без перезагрузки страницы была удалена, так как данные покрытия не нарушались.</span><span class="sxs-lookup"><span data-stu-id="abe2f-276">Toggling code coverage without a page reload has been removed because the coverage data was unreliable.</span></span>  <span data-ttu-id="abe2f-277">Например, функция может быть получена как неиспользуемая, если время выполнения была длительное время назад, а сборщик V8 гарбризовала ее.</span><span class="sxs-lookup"><span data-stu-id="abe2f-277">For example, a function may be reported as unused if the runtime was a long time ago and the V8 garbage collector has cleaned it up.</span></span>  

<span data-ttu-id="abe2f-278">Проблема с [хромом#1004203][crbug1004203]</span><span class="sxs-lookup"><span data-stu-id="abe2f-278">Chromium issue [#1004203][crbug1004203]</span></span>  

## <span data-ttu-id="abe2f-279">Скачивание каналов с предварительными версиями Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="abe2f-279">Download the Microsoft Edge preview channels</span></span>  

<span data-ttu-id="abe2f-280">Если вы используете Windows или macOS, рекомендуем использовать каналы [предварительной версии Microsoft Edge][MicrosoftEdgePreviewChannels] в качестве браузера разработки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="abe2f-280">If you are on Windows or macOS, consider using the [Microsoft Edge preview channels][MicrosoftEdgePreviewChannels] as your default development browser.</span></span>  <span data-ttu-id="abe2f-281">Каналы с предварительными версиями доступны новейшие функции Разработчиков.</span><span class="sxs-lookup"><span data-stu-id="abe2f-281">The preview channels give you access to the latest DevTools features.</span></span>  

## <span data-ttu-id="abe2f-282">Совместная работа с помощью команды разработчиков Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="abe2f-282">Getting in touch with Microsoft Edge DevTools team</span></span>  

[!INCLUDE [contact DevTools team note](../../includes/contact-whats-new-note.md)]  

<!--<<../../_shared/devtools-feedback.md>> -->

<!--<<../../_shared/canary.md>> -->

<!--<<../../_shared/discover.md>> -->

<!-- image links -->  

[ImagePerformanceToolKeyboardReaderImprovements]: ../../images/2019/12/a11y-performance-tool.msft.gif "Рис. 1. Средство для работы с разработчиками с помощью клавиатуры и средства чтения с экрана"  
[ImageLocalizedGerman]: ../../images/2019/12/localized-devtools.msft.png "Изображение 2. Разработчики в немецких"  
[ImageHintsTabWebhintExtension]: ../../images/2019/12/webhint-browser-extension.msft.png "Рис. 3. Вкладка "Подсказки" в Microsoft Edge DevTools, если установлено расширение веб-браузера"  
[Image3DView]: ../../images/2019/12/3dview.msft.png "Рис. 4. Трехмерное представление в средствах разработчиков Microsoft Edge"  
[ImageElementsVisualStudioCode]: ../../images/2019/12/elements-for-edge.msft.png "Рис. 5. Инструмент "Элементы" в коде VS с помощью элементов расширения Microsoft Edge"  
[ImageDebuggerExtensionVisualStudioCode]: ../../images/2019/12/vscode-debugger.msft.png "Р. Отладка для Расширения Microsoft Edge в коде VS"  
[ImageWebhintVisualStudioCodeExtensionWorkspace]: ../../images/2019/12/webhint-vscode-extension.msft.png "Рис. Расширение webhint VS-кода VS в коде VS"  
[ImageVisualStudioLaunchWebApp]: ../../images/2019/12/vs.msft.png "Рис. Visual Studio с возможностью запуска веб-приложения в Microsoft Edge Canary, Dev или Бета-версии"  
[ImageTrackingPrevention]: ../../images/2019/12/tracking-prevention.msft.png "Р. Сообщения в консоли при блокировке отслеживания блокируют доступ к хранилищу для отслеживания"  
[ImageConsoleRedeclarationFails]: ../../images/2019/12/letbefore.msft.png "Рис. 10: консоль в Microsoft Edge 79, показывающая, что разрешить отказ отклонения не удается"  
[ImageConsoleRedeclarationSucceeds]: ../../images/2019/12/letafter.msft.png "Рис. 11: консоль в Microsoft Edge 80 показывает, что разрешение отклонения разрешено успешно"  
[ImageRequestInitiatorChain]: ../../images/2019/12/initiators.msft.png "Рис. 12: инициатор запросов на вкладке "Инициатор""  
[ImageOverviewPaneInspectedResource]: ../../images/2019/12/overview.msft.png "Рис. 13: область обзора, на ведущей проверенный ресурс"  
[ImagePathNetworkPanel]: ../../images/2019/12/columns.msft.png "Рис. 14: новые столбцы пути и URL-адреса на панели сети"  
[ImageUserAgentNetworkConditionsTab]: ../../images/2019/12/useragent.msft.png "Рис. 15: меню агента пользователя на вкладке "Сетевые условия""  
[ImageConfigurationUI]: ../../images/2019/12/start.msft.png "Рис. 16: новый элемент управления конфигурацией"  
[ImageCoverageMode]: ../../images/2019/12/modes.msft.png "Рис. 17: раскрывающееся меню режима переключения"  

<!--[ImageDwarfPoweredWebAssemblyDebugging]: ../../images/2019/12/wasm.msft.png "Figure: The new DWARF-powered WebAssembly debugging"  -->

<!-- links -->  

[DevToolsCommandMenuIndex]: ../../../command-menu/index.md "Команды с помощью меню «Средства разработчика» microsoft Edge"  
[DevToolsCoverageIndex]: ../../../coverage/index.md "Поиск кодов JavaScript и CSS с помощью вкладки Coverage в Microsoft Edge DevTools"  
[DevToolsDeviceModeIndex]: ../../../device-mode/index.md#simulate-a-mobile-viewport "Одновременный просмотр для мобильных устройств : одновременный режим устройств с режимом устройств в Microsoft Edge DevTools"  
[DevToolsNetworkIndex]: ../../../network/index.md "Проверка действий с ее сетью в средствах разработчиков Microsoft Edge"  
[DevToolsNetworkReferenceViewInitiatorsDependencies]: ../../../network/reference.md#view-initiators-and-dependencies "Просмотр инициатив и зависимостей — справочник по сетевому анализу"  
[DevGuideEdgeHtmlWhatsNew]: ../../../../dev-guide/whats-new.md "Новые возможности Microsoft EdgeHTML"  
[VisualStudioCodeDebuggerEdgeExtension]: ../../../../visual-studio-code/debugger-for-edge.md "Отладка расширения кода Microsoft Edge VS"  
[VisualStudioCodeElementEdgeExtension]: ../../../../visual-studio-code/elements-for-edge.md "Элементы расширения кода Microsoft Edge VS"  

<!--  [201912Webassembly]: webassembly.md "Improved WebAssembly debugging in Microsoft Edge DevTools"  -->  

[crbug842488]: https://crbug.com/842488 "842488: добавление поля "Инициатор" на вкладку "Заголовки" — "Морели"."  
[crbug988253]: https://crbug.com/988253 "988253 - ошибка DevTools — Без связи между сетевым запросом и графиком "График" — "Транспорт""  
[crbug993366]: https://crbug.com/993366 "993366. Отобразите путь к URL-адресу в списке запросов на сетевую панель ( произвольный"  
[crbug1004193]: https://crbug.com/1004193 "1004193 — режим REPL для V8 — монor"  
[crbug1004203]: https://crbug.com/1004203 "1004203 — Мондия"  
[crbug1029031]: https://crbug.com/1029031 "1029031 — строки США устарели, — монорский" 
[crbug963183]: https://crbug.com/963183 "963183 — средства для разработки не совместимо с WCAG"
[crbug941561]: https://crbug.com/941561 "941561 — локализация средств разработчиков"
[crbug987787]: https://crbug.com/987787 "987787 — Dom 3D View"

[AccessibilityInsights]: https://aka.ms/a11yinsights "Сведения о специальных возможностях"  

[DwarfHome]: https://dwarfstd.org "Домашняя страница Двуха"  
[GitHubGoogleChromeDevToolsAuditsPanelThrottling]: https://github.com/GoogleChrome/lighthouse/blob/master/docs/throttling.md#devtools-audits-panel-throttling "Панель аудита DevTools' на панели регулирования: GoogleChrome/lighthouse | GitHub"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Новая проблема: MicrosoftDocs/edge-разработчики"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Каналы предварительной версии Microsoft Edge"  
[MicrosoftEdgeInsiderAddons]: https://aka.ms/webhint/edge-extension "Microsoft Edge Insider Addons"  
[MicrosoftVisualStudio]: https://aka.ms/vs "Visual Studio"  
[MicrosoftVisualStudioBlogDebugJavascript]: https://aka.ms/vs/debug-edge "Отладка JavaScript в Microsoft Edge с Visual Studio | Visual Studio блог"  
[MicrosoftVisualStudioDownloads]: https://aka.ms/vs/download "Скачивание Visual Studio 2019 для Windows \& для Mac"  
[MDNDocumentObjectModel]: https://developer.mozilla.org/docs/Web/API/Document_Object_Model "Объектная модель документов (DOM) | MDN"  
[MDNZIndex]: https://developer.mozilla.org/docs/Web/CSS/z-index "z-индекс | MDN"  
[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Публикация твита"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools твиттер"
[VisualStudioCode]: https://aka.ms/vscode "Visual Studio код"  
[VisualStudioMarketplaceDebuggerEdge]: https://aka.ms/debugger4code "Отладка для Microsoft Edge — Visual Studio Marketplace"  
[VisualStudioMarketplaceElementsMicrosoftEdgeChromiumExtension]: https://aka.ms/elements4code "Элементы для Microsoft Edge \(Chromium\) — Visual Studio Marketplace"  
[VisualStudioMarketplaceWebhintExtension]: https://aka.ms/webhint4code "webhint — Visual Studio Marketplace"
[Webhint]: https://aka.ms/webhint "webhint"  
[WebhintBrowserExtension]: https://aka.ms/webhint/browser-extension "Расширение Webhint для браузера | документация веб-хинтерской документации"  
[WebhintVisualStudioCodeExtension]: https://aka.ms/webhint/code-extension "Расширение веб-кода VS | документация веб-хинтерской документации"  
[TrackingPrevention]: https://aka.ms/microsoftedge/tracking-prevention-blog "Улучшение отслеживания исправлений в записях блога Microsoft Edge"
[TheWebWeWant]: https://aka.ms/webwewant "Нужный веб-час"

> [!NOTE]
> <span data-ttu-id="abe2f-339">Части этой страницы изменяются на основе работы, созданных google и [предоставлением][GoogleSitePolicies] к ним общего доступа и используются в соответствии с терминами, которые описаны [в лицензии Creative Commons Attribution 4.0.][CCA4IL]</span><span class="sxs-lookup"><span data-stu-id="abe2f-339">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="abe2f-340">Исходная страница [here](https://developers.google.com/web/updates/2019/12/devtools/index) находится на сайте [Kayce Basques][KayceBasques] \(технический автор, Chrome DevTools & Lighthouse\).</span><span class="sxs-lookup"><span data-stu-id="abe2f-340">The original page is found [here](https://developers.google.com/web/updates/2019/12/devtools/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools & Lighthouse\).</span></span>  

[![Creative Commons License][CCby4Image]][CCA4IL]  
<span data-ttu-id="abe2f-342">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="abe2f-342">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
