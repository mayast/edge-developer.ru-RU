---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView 2
title: Элемент управления Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/10/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, CoreWebView2, ICoreWebView2Host, элементы управления браузером, EDGE HTML, Windows Forms, WinForms, WPF, .NET
ms.openlocfilehash: bb2287ca854372d9592a3b90c7df6f9a8abf620e
ms.sourcegitcommit: 4bc904c5d54347185f275bd76441975be471c320
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2020
ms.locfileid: "10926472"
---
# <span data-ttu-id="819c1-104">Введение в Microsoft Edge WebView2 (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="819c1-104">Introduction to Microsoft Edge WebView2 (Preview)</span></span>  

<span data-ttu-id="819c1-105">Элемент управления Microsoft Edge WebView2 позволяет внедрять в собственные приложения веб-технологии \ (HTML, CSS и JavaScript).</span><span class="sxs-lookup"><span data-stu-id="819c1-105">The Microsoft Edge WebView2 control enables you to embed web technologies \(HTML, CSS, and JavaScript\) in your native applications.</span></span>  <span data-ttu-id="819c1-106">Элемент управления WebView2 использует [Microsoft EDGE (Chromium)][MicrosoftedgeinsiderMain] в качестве обработчика обработки для отображения веб-содержимого в собственных приложениях.</span><span class="sxs-lookup"><span data-stu-id="819c1-106">The WebView2 control uses [Microsoft Edge (Chromium)][MicrosoftedgeinsiderMain] as the rendering engine to display the web content in native applications.</span></span>  <span data-ttu-id="819c1-107">С помощью WebView2 вы можете внедрить веб-код в различные части собственного приложения или создать для него приложение целиком в рамках одного WebView.</span><span class="sxs-lookup"><span data-stu-id="819c1-107">With WebView2, you may embed web code in different parts of your native application, or build the entire native application within a single WebView.</span></span>  <span data-ttu-id="819c1-108">Сведения о том, как приступить к созданию приложения WebView2, можно найти в разделе Начало [работы](#getting-started).</span><span class="sxs-lookup"><span data-stu-id="819c1-108">For information on how to start building a WebView2 application, see [Get Started](#getting-started).</span></span>  

:::image type="complex" source="./media/WebView2/whatwebview.png" alt-text="Что такое WebView" lightbox="./media/WebView2/whatwebview.png":::
   <span data-ttu-id="819c1-110">Что такое WebView</span><span class="sxs-lookup"><span data-stu-id="819c1-110">What is WebView</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="819c1-111">Предварительная версия WebView2 предназначена для раннего создания прототипов и сбора отзывов, помогающих в создании API.</span><span class="sxs-lookup"><span data-stu-id="819c1-111">The WebView2 Preview is intended for early prototyping and to gather feedback to help shape the API.</span></span>  <span data-ttu-id="819c1-112">Вы не должны использовать предварительный просмотр в производственных приложениях, так как это может привести к коренным изменениям.</span><span class="sxs-lookup"><span data-stu-id="819c1-112">You should not use the preview in your production apps because there may be breaking changes.</span></span>  <span data-ttu-id="819c1-113">Дополнительные сведения можно найти в разделе [Webview2Releasenotes].</span><span class="sxs-lookup"><span data-stu-id="819c1-113">For more information, see [Webview2Releasenotes].</span></span>  

## <span data-ttu-id="819c1-114">Подход к гибридным приложениям</span><span class="sxs-lookup"><span data-stu-id="819c1-114">Hybrid application approach</span></span>  

<span data-ttu-id="819c1-115">Разработчикам часто приходится определять создание веб-приложения или собственного приложения.</span><span class="sxs-lookup"><span data-stu-id="819c1-115">Developers often have to decide between building a web application or a native application.</span></span>  <span data-ttu-id="819c1-116">Решение на основе компромиссов между абонентами и возможностями.</span><span class="sxs-lookup"><span data-stu-id="819c1-116">The decision hinges on the trade-off between reach and power.</span></span>  <span data-ttu-id="819c1-117">Веб-приложения допускают широкий доступ к ним.</span><span class="sxs-lookup"><span data-stu-id="819c1-117">Web applications allow for a broad reach.</span></span>  <span data-ttu-id="819c1-118">Как и веб-разработчик, вы можете использовать больше всего, если не все ваши коды на разных платформах.</span><span class="sxs-lookup"><span data-stu-id="819c1-118">As a Web developer, you may reuse most, if not all of your code, across all different platforms.</span></span>  <span data-ttu-id="819c1-119">Однако в собственных приложениях используются возможности всей платформы машинного кода.</span><span class="sxs-lookup"><span data-stu-id="819c1-119">Native applications, however, utilize the capabilities of the entire native platform.</span></span>  

:::image type="complex" source="./media/WebView2/webnative.png" alt-text="Исходный веб-сайт" lightbox="./media/WebView2/webnative.png":::
   <span data-ttu-id="819c1-121">Исходный веб-сайт</span><span class="sxs-lookup"><span data-stu-id="819c1-121">Web native</span></span>  
:::image-end:::  

<span data-ttu-id="819c1-122">Гибридные приложения позволяют разработчикам использовать преимущества обоих миров.</span><span class="sxs-lookup"><span data-stu-id="819c1-122">Hybrid applications allow developers to enjoy the best of both worlds.</span></span>  <span data-ttu-id="819c1-123">Разработчики гибридных приложений выигрывают от широкого и мощного веб-платформы, а также мощь и полную функциональность собственной платформы.</span><span class="sxs-lookup"><span data-stu-id="819c1-123">Hybrid application developers benefit from the ubiquity and strength of the web platform, and the power and full capabilities of the native platform.</span></span>  

## <span data-ttu-id="819c1-124">Преимущества WebView2</span><span class="sxs-lookup"><span data-stu-id="819c1-124">WebView2 benefits</span></span>   

:::image type="complex" source="./media/WebView2/webviewreasons.png" alt-text="Причины WebView" lightbox="./media/WebView2/webviewreasons.png":::
   <span data-ttu-id="819c1-126">Причины WebView</span><span class="sxs-lookup"><span data-stu-id="819c1-126">WebView reasons</span></span>  
:::image-end:::  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="819c1-127">Веб-экосистема \ "&й навык"</span><span class="sxs-lookup"><span data-stu-id="819c1-127">Web ecosystem \& skillset</span></span>**  
      <span data-ttu-id="819c1-128">Используйте все веб-платформы, библиотеки, Инструментарий и все, что есть в веб-экосистеме.</span><span class="sxs-lookup"><span data-stu-id="819c1-128">Utilize the entire web platform, libraries, tooling, and talent that exists within the web ecosystem.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="819c1-129">Быстрые инновации</span><span class="sxs-lookup"><span data-stu-id="819c1-129">Rapid innovation</span></span>**  
      <span data-ttu-id="819c1-130">Веб-разработки допускают более быстрые развертывание и итерации.</span><span class="sxs-lookup"><span data-stu-id="819c1-130">Web development allows for faster deployment and iteration.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="819c1-131">Поддержка Windows 7, 8, 10</span><span class="sxs-lookup"><span data-stu-id="819c1-131">Windows 7, 8, 10 support</span></span>**  
      <span data-ttu-id="819c1-132">Поддержка согласованного взаимодействия с пользователем в Windows 7, 8 и 10.</span><span class="sxs-lookup"><span data-stu-id="819c1-132">Support for a consistent user experience across Windows 7, 8, and 10.</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      **<span data-ttu-id="819c1-133">Собственные возможности</span><span class="sxs-lookup"><span data-stu-id="819c1-133">Native capabilities</span></span>**  
      <span data-ttu-id="819c1-134">Получить доступ к полному набору API для собственных интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="819c1-134">Access the full set of Native APIs.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="819c1-135">Совместное использование кода</span><span class="sxs-lookup"><span data-stu-id="819c1-135">Code-sharing</span></span>**  
      <span data-ttu-id="819c1-136">Добавление веб-кода в базу кода для более высокой повторной работы на нескольких платформах.</span><span class="sxs-lookup"><span data-stu-id="819c1-136">Add web code to your codebase allows for increased re-use across multiple platforms.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="819c1-137">Служба поддержки Майкрософт</span><span class="sxs-lookup"><span data-stu-id="819c1-137">Microsoft support</span></span>**  
      <span data-ttu-id="819c1-138">Корпорация Майкрософт предоставляет поддержку и добавляет новые запросы на доступ к функциям, когда WebView2 отпущена как завершенный.</span><span class="sxs-lookup"><span data-stu-id="819c1-138">Microsoft provides support and adds new feature requests when WebView2 is release as GA.</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      **<span data-ttu-id="819c1-139">Распространение Evergreen</span><span class="sxs-lookup"><span data-stu-id="819c1-139">Evergreen distribution</span></span>**  
      <span data-ttu-id="819c1-140">Полагаться на обновленную версию Chromium с помощью регулярных обновлений платформы и исправлений для системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="819c1-140">Rely on an up-to-date version of Chromium with regular platform updates and security patches.</span></span>  
   :::column-end:::
   :::column span="1":::
      <span data-ttu-id="819c1-141">**Исправлено** \ (скоро)</span><span class="sxs-lookup"><span data-stu-id="819c1-141">**Fixed** \(coming soon\)</span></span>  
      <span data-ttu-id="819c1-142">Выберите, чтобы упаковать биты Chromium в приложении.</span><span class="sxs-lookup"><span data-stu-id="819c1-142">Choose to package the Chromium bits in your application.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="819c1-143">Добавочное внедрение</span><span class="sxs-lookup"><span data-stu-id="819c1-143">Incremental adoption</span></span>**  
      <span data-ttu-id="819c1-144">Добавление части веб-компонентов в приложение.</span><span class="sxs-lookup"><span data-stu-id="819c1-144">Add web components piece by piece to your application.</span></span>  
   :::column-end:::
:::row-end:::

## <span data-ttu-id="819c1-145">Начало работы</span><span class="sxs-lookup"><span data-stu-id="819c1-145">Getting started</span></span>  

<span data-ttu-id="819c1-146">Чтобы создать и протестировать приложение с помощью элемента управления WebView2, необходимо установить [Microsoft EDGE (Chromium)][MicrosoftedgeinsiderDownload] и [WebView2 SDK][NugetPackagesMicrosoftWebWebView2] .</span><span class="sxs-lookup"><span data-stu-id="819c1-146">To build and test your application using the WebView2 control, you need to have both [Microsoft Edge (Chromium)][MicrosoftedgeinsiderDownload] and the [WebView2 SDK][NugetPackagesMicrosoftWebWebView2] installed.</span></span>  <span data-ttu-id="819c1-147">Чтобы приступить к работе, выберите один из следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="819c1-147">Select one of the following options to get started.</span></span>  

*   [<span data-ttu-id="819c1-148">Начало работы с Win32 C/C++</span><span class="sxs-lookup"><span data-stu-id="819c1-148">Getting Started with Win32 C/C++</span></span>][Webview2GettingstartedWin32]  
*   [<span data-ttu-id="819c1-149">Начало работы с WPF</span><span class="sxs-lookup"><span data-stu-id="819c1-149">Getting Started with WPF</span></span>][Webview2GettingstartedWpf]  
*   [<span data-ttu-id="819c1-150">Приступая к работе с WinForms</span><span class="sxs-lookup"><span data-stu-id="819c1-150">Getting Started with WinForms</span></span>][Webview2GettingstartedWinforms]  
*   [<span data-ttu-id="819c1-151">Начало работы с WinUI3</span><span class="sxs-lookup"><span data-stu-id="819c1-151">Getting Started with WinUI3</span></span>][Webview2GettingstartedWinui]  

<span data-ttu-id="819c1-152">В репозитории [примеров WebView2][GithubMicrosoftedgeWebview2samples] содержатся примеры, демонстрирующие все функции SDK WebView2 и использование API.</span><span class="sxs-lookup"><span data-stu-id="819c1-152">The [WebView2 Samples][GithubMicrosoftedgeWebview2samples] repository contains samples that demonstrate all of the WebView2 SDK features and API usage patterns.</span></span>  <span data-ttu-id="819c1-153">По мере добавления дополнительных функций в пакет SDK для WebView2, образцы приложений будут обновлены.</span><span class="sxs-lookup"><span data-stu-id="819c1-153">As more features are added to the WebView2 SDK, the sample applications will be updated.</span></span>  

## <span data-ttu-id="819c1-154">Поддерживаемые платформы</span><span class="sxs-lookup"><span data-stu-id="819c1-154">Supported platforms</span></span>  

<span data-ttu-id="819c1-155">Предварительный просмотр для разработчиков доступен в следующих средах программирования.</span><span class="sxs-lookup"><span data-stu-id="819c1-155">A developer preview is available on the following programming environments.</span></span>  

*   <span data-ttu-id="819c1-156">Win32 C/C++</span><span class="sxs-lookup"><span data-stu-id="819c1-156">Win32 C/C++</span></span>  
*   <span data-ttu-id="819c1-157">.NET Framework 4.6.2 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="819c1-157">.NET Framework 4.6.2 or later</span></span>  
*   <span data-ttu-id="819c1-158">.NET Core 3,0 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="819c1-158">.NET Core 3.0 or later</span></span>  
*   [<span data-ttu-id="819c1-159">WinUI3.0</span><span class="sxs-lookup"><span data-stu-id="819c1-159">WinUI 3.0</span></span>][UwpToolkitsWinui3]  

<span data-ttu-id="819c1-160">Вы можете запускать приложения WebView2 в следующих версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="819c1-160">You are able to run WebView2 applications on the following versions of Windows.</span></span>  

*   <span data-ttu-id="819c1-161">Windows 10;</span><span class="sxs-lookup"><span data-stu-id="819c1-161">Windows 10</span></span>  
*   <span data-ttu-id="819c1-162">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="819c1-162">Windows 8.1</span></span>  
*   <span data-ttu-id="819c1-163">Windows 8</span><span class="sxs-lookup"><span data-stu-id="819c1-163">Windows 8</span></span>  
*   <span data-ttu-id="819c1-164">Windows 7</span><span class="sxs-lookup"><span data-stu-id="819c1-164">Windows 7</span></span>  
*   <span data-ttu-id="819c1-165">WindowsServer2016</span><span class="sxs-lookup"><span data-stu-id="819c1-165">Windows Server 2016</span></span>  
*   <span data-ttu-id="819c1-166">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="819c1-166">Windows Server 2012</span></span>  
*   <span data-ttu-id="819c1-167">Windows Server 2012R2</span><span class="sxs-lookup"><span data-stu-id="819c1-167">Windows Server 2012R2</span></span>  
*   <span data-ttu-id="819c1-168">Windows Server2008R2</span><span class="sxs-lookup"><span data-stu-id="819c1-168">Windows Server 2008 R2</span></span>  

## <span data-ttu-id="819c1-169">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="819c1-169">Next steps</span></span>  

<span data-ttu-id="819c1-170">Дополнительные сведения о том, как создавать и развертывать приложения WebView2, можно узнать в концептуальной документации и руководствах.</span><span class="sxs-lookup"><span data-stu-id="819c1-170">For more information on how to build and deploy WebView2 applications, review the conceptual documentation and how-to guides.</span></span>  

#### <span data-ttu-id="819c1-171">Понятия</span><span class="sxs-lookup"><span data-stu-id="819c1-171">Concepts</span></span>  

*   [<span data-ttu-id="819c1-172">Общие сведения о версиях SDK для WebView2</span><span class="sxs-lookup"><span data-stu-id="819c1-172">Understand WebView2 SDK versions</span></span>][Webview2ConceptsVersioning]
*   [<span data-ttu-id="819c1-173">Распространение приложений с помощью WebView2</span><span class="sxs-lookup"><span data-stu-id="819c1-173">Distribution of applications using WebView2</span></span>][Webview2ConceptsDistribution]  
*   [<span data-ttu-id="819c1-174">Рекомендации по разработке защищенных приложений WebView2</span><span class="sxs-lookup"><span data-stu-id="819c1-174">Best practices for developing secure WebView2 applications</span></span>][Webview2ConceptsSecurity]
*   [<span data-ttu-id="819c1-175">Управление папкой "данные пользователя" в приложениях WebView2</span><span class="sxs-lookup"><span data-stu-id="819c1-175">Manage User Data Folder in WebView2 Applications</span></span>][Webview2ConceptsUserdatafolder]
 
#### <span data-ttu-id="819c1-176">Практические руководства</span><span class="sxs-lookup"><span data-stu-id="819c1-176">How-To guides</span></span>  

*   [<span data-ttu-id="819c1-177">Отладка с помощью WebView2</span><span class="sxs-lookup"><span data-stu-id="819c1-177">How to Debug with WebView2</span></span>][Webview2HowtoDebug]  
*   [<span data-ttu-id="819c1-178">Автоматизация и тестирование WebView2 с помощью драйвера Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="819c1-178">Automating and testing WebView2 with Microsoft Edge Driver</span></span>][Webview2HowtoWebdriver]  

## <span data-ttu-id="819c1-179">Знакомство с командой Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="819c1-179">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](./includes/contact-webview-team-note.md)]  

> [!NOTE]
> <span data-ttu-id="819c1-180">При предварительном просмотре собранные данные помогают собрать более качественный продукт.</span><span class="sxs-lookup"><span data-stu-id="819c1-180">During the preview, the collected data helps build a better product.</span></span>  <span data-ttu-id="819c1-181">Чтобы отключить сбор данных WebView2, перейдите к `edge://settings/privacy` коллекции данных браузера и отключите ее.</span><span class="sxs-lookup"><span data-stu-id="819c1-181">To turn off WebView2 data collection, go to `edge://settings/privacy` and turn off browser data collection.</span></span>  

<!-- links -->  

[Webview2ConceptsDistribution]: ./concepts/distribution.md "Распространение приложений с помощью WebView2 | Документы Microsoft"  
[Webview2ConceptsSecurity]: ./concepts/security.md "Рекомендации по разработке безопасных приложений WebView2 | Документы Microsoft"  
[Webview2ConceptsUserdatafolder]: ./concepts/userdatafolder.md "Управление папкой "данные пользователя" | Документы Microsoft"  
[Webview2ConceptsVersioning]: ./concepts/versioning.md "Общие сведения о версиях SDK для WebView2 | Документы Microsoft"  
[Webview2GettingstartedWin32]: ./gettingstarted/win32.md "Начало работы с WebView2 (Предварительная версия для разработчиков) | Документы Microsoft"   
[Webview2GettingstartedWinforms]: ./gettingstarted/winforms.md "Начало работы с WebView2 в приложениях для Windows Forms (Предварительная версия) | Документы Microsoft"  
[Webview2GettingstartedWinui]: ./gettingstarted/winui.md "Начало работы с WebView2 в WinUI3 (Предварительная версия) | Документы Microsoft"  
[Webview2GettingstartedWpf]: ./gettingstarted/wpf.md "Начало работы с WebView2 в WPF (Предварительная версия) | Документы Microsoft"  
[Webview2HowtoDebug]: ./howto/debug.md "Отладка с помощью WebView2 | Документы Microsoft"  
[Webview2HowtoWebdriver]: ./howto/webdriver.md "Автоматизация и тестирование WebView2 с помощью драйвера Microsoft Edge | Документы Microsoft"  
[Webview2Releasenotes]: ./releasenotes.md "Заметки о выпуске WEBVIEW2RELEASENOTES для WebView2 SDK | Документы Microsoft"  

[UwpToolkitsWinui3]: ./gettingstarted/winui.md "Библиотека пользовательского интерфейса Windows 3 Preview (2020 июля) | Документы Microsoft"  

[GithubMicrosoftedgeWebview2samples]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeddback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback-MicrosoftEdge/WebViewFeedback | GitHub" 

[MicrosoftedgeinsiderMain]: https://www.microsoftedgeinsider.com "Предварительная оценка Microsoft Edge"  
[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Загрузить программу предварительной оценки Microsoft Edge"  

[NugetPackagesMicrosoftWebWebView2]: https://www.nuget.org/packages/Microsoft.Web.WebView2 "Microsoft. Web. WebView2 | Коллекция NuGet"  
