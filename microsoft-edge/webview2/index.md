---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView 2
title: Элемент управления Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/21/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, CoreWebView2, ICoreWebView2Host, элементы управления браузером, EDGE HTML, Windows Forms, WinForms, WPF, .NET
ms.openlocfilehash: 1b140d9f644c7a864cac4966bb4cfdd400feeb0d
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697744"
---
# <span data-ttu-id="d5596-104">Введение в Microsoft Edge WebView2 (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="d5596-104">Introduction to Microsoft Edge WebView2 (Preview)</span></span>  

<span data-ttu-id="d5596-105">Элемент управления Microsoft Edge WebView2 позволяет внедрять в собственные приложения веб-технологии \ (HTML, CSS и JavaScript).</span><span class="sxs-lookup"><span data-stu-id="d5596-105">The Microsoft Edge WebView2 control enables you to embed web technologies \(HTML, CSS, and JavaScript\) in your native applications.</span></span>  <span data-ttu-id="d5596-106">Элемент управления WebView2 использует [Microsoft EDGE (Chromium)](https://www.microsoftedgeinsider.com) в качестве обработчика обработки для отображения веб-содержимого в собственных приложениях.</span><span class="sxs-lookup"><span data-stu-id="d5596-106">The WebView2 control uses [Microsoft Edge (Chromium)](https://www.microsoftedgeinsider.com) as the rendering engine to display the web content in native applications.</span></span>  <span data-ttu-id="d5596-107">С помощью WebView2 вы можете внедрить веб-код в различные части собственного приложения или создать для него приложение целиком в рамках одного WebView.</span><span class="sxs-lookup"><span data-stu-id="d5596-107">With WebView2, you may embed web code in different parts of your native application, or build the entire native application within a single WebView.</span></span>  <span data-ttu-id="d5596-108">Сведения о том, как приступить к созданию приложения WebView2, можно найти в разделе Начало [работы](./index.md#getting-started).</span><span class="sxs-lookup"><span data-stu-id="d5596-108">For information on how to start building a WebView2 application, see [Get Started](./index.md#getting-started).</span></span>  

:::image type="complex" source="./media/WebView2/whatwebview.png" alt-text="Что такое WebView":::
   <span data-ttu-id="d5596-110">Что такое WebView</span><span class="sxs-lookup"><span data-stu-id="d5596-110">What is WebView</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="d5596-111">Предварительная версия WebView2 предназначена для раннего создания прототипов и сбора отзывов, помогающих в создании API.</span><span class="sxs-lookup"><span data-stu-id="d5596-111">The WebView2 Preview is intended for early prototyping and to gather feedback to help to shape the API.</span></span>  <span data-ttu-id="d5596-112">Группа Microsoft Edge WebView не рекомендует использовать предварительный просмотр в производственных приложениях, так как это может привести к [коренным изменениям](./releasenotes.md).</span><span class="sxs-lookup"><span data-stu-id="d5596-112">The Microsoft Edge WebView team does not recommend that you use the preview in your production apps because there may be [breaking changes](./releasenotes.md).</span></span>  

## <span data-ttu-id="d5596-113">Подход к гибридным приложениям</span><span class="sxs-lookup"><span data-stu-id="d5596-113">Hybrid application approach</span></span>  

<span data-ttu-id="d5596-114">Разработчикам часто приходится выбирать между созданием веб-приложения или собственного приложения.</span><span class="sxs-lookup"><span data-stu-id="d5596-114">Developers often have to choose between building a web application or a native application.</span></span>  <span data-ttu-id="d5596-115">Решение на основе компромиссов между абонентами и возможностями.</span><span class="sxs-lookup"><span data-stu-id="d5596-115">The decision hinges on the trade-off between reach and power.</span></span>  <span data-ttu-id="d5596-116">Веб-приложения допускают широкий доступ к ним.</span><span class="sxs-lookup"><span data-stu-id="d5596-116">Web applications allow for a broad reach.</span></span>  <span data-ttu-id="d5596-117">Как и веб-разработчик, вы можете использовать больше всего, если не все ваши коды на разных платформах.</span><span class="sxs-lookup"><span data-stu-id="d5596-117">As a Web developer, you may reuse most, if not all of your code, across all different platforms.</span></span>  <span data-ttu-id="d5596-118">Однако в собственных приложениях используются возможности всей платформы машинного кода.</span><span class="sxs-lookup"><span data-stu-id="d5596-118">Native applications, however, utilize the capabilities of the entire native platform.</span></span>  

:::image type="complex" source="./media/WebView2/webnative.png" alt-text="Исходный веб-сайт":::
   <span data-ttu-id="d5596-120">Исходный веб-сайт</span><span class="sxs-lookup"><span data-stu-id="d5596-120">Web native</span></span>  
:::image-end:::  

<span data-ttu-id="d5596-121">Гибридные приложения позволяют разработчикам использовать преимущества обоих миров.</span><span class="sxs-lookup"><span data-stu-id="d5596-121">Hybrid applications allow developers to enjoy the best of both worlds.</span></span>  <span data-ttu-id="d5596-122">Разработчики гибридных приложений выигрывают от широкого и мощного веб-платформы, а также мощь и полную функциональность собственной платформы.</span><span class="sxs-lookup"><span data-stu-id="d5596-122">Hybrid application developers benefit from the ubiquity and strength of the web platform, and the power and full capabilities of the native platform.</span></span>  

## <span data-ttu-id="d5596-123">Преимущества WebView2</span><span class="sxs-lookup"><span data-stu-id="d5596-123">WebView2 benefits</span></span>   

:::image type="complex" source="./media/WebView2/webviewreasons.png" alt-text="Причины WebView":::
   <span data-ttu-id="d5596-125">Причины WebView</span><span class="sxs-lookup"><span data-stu-id="d5596-125">WebView reasons</span></span>  
:::image-end:::  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="d5596-126">Веб-экосистема \ "&й навык"</span><span class="sxs-lookup"><span data-stu-id="d5596-126">Web ecosystem \& skillset</span></span>**  
      <span data-ttu-id="d5596-127">Используйте все веб-платформы, библиотеки, Инструментарий и все, что есть в веб-экосистеме.</span><span class="sxs-lookup"><span data-stu-id="d5596-127">Utilize the entire web platform, libraries, tooling, and talent that exists within the web ecosystem.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="d5596-128">Быстрые инновации</span><span class="sxs-lookup"><span data-stu-id="d5596-128">Rapid innovation</span></span>**  
      <span data-ttu-id="d5596-129">Веб-разработки допускают более быстрые развертывание и итерации.</span><span class="sxs-lookup"><span data-stu-id="d5596-129">Web development allows for faster deployment and iteration.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="d5596-130">Поддержка Windows 7, 8, 10</span><span class="sxs-lookup"><span data-stu-id="d5596-130">Windows 7, 8, 10 support</span></span>**  
      <span data-ttu-id="d5596-131">Поддержка согласованного взаимодействия с пользователем в Windows 7, 8 и 10.</span><span class="sxs-lookup"><span data-stu-id="d5596-131">Support for a consistent user experience across Windows 7, 8, and 10.</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      **<span data-ttu-id="d5596-132">Собственные возможности</span><span class="sxs-lookup"><span data-stu-id="d5596-132">Native capabilities</span></span>**  
      <span data-ttu-id="d5596-133">Получить доступ к полному набору API для собственных интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="d5596-133">Access the full set of Native APIs.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="d5596-134">Совместное использование кода</span><span class="sxs-lookup"><span data-stu-id="d5596-134">Code-sharing</span></span>**  
      <span data-ttu-id="d5596-135">Добавление веб-кода в базу кода для более высокой повторной работы на нескольких платформах.</span><span class="sxs-lookup"><span data-stu-id="d5596-135">Add web code to your codebase allows for increased re-use across multiple platforms.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="d5596-136">Служба поддержки Майкрософт</span><span class="sxs-lookup"><span data-stu-id="d5596-136">Microsoft support</span></span>**  
      <span data-ttu-id="d5596-137">Корпорация Майкрософт предоставляет поддержку и добавляет новые запросы на доступ к функциям, когда WebView2 отпущена как завершенный.</span><span class="sxs-lookup"><span data-stu-id="d5596-137">Microsoft provides support and adds new feature requests when WebView2 is release as GA.</span></span>  
   :::column-end:::
:::row-end:::
:::row:::
   :::column span="1":::
      **<span data-ttu-id="d5596-138">Распространение Evergreen</span><span class="sxs-lookup"><span data-stu-id="d5596-138">Evergreen distribution</span></span>**  
      <span data-ttu-id="d5596-139">Полагаться на обновленную версию Chromium с помощью регулярных обновлений платформы и исправлений для системы безопасности.</span><span class="sxs-lookup"><span data-stu-id="d5596-139">Rely on an up-to-date version of Chromium with regular platform updates and security patches.</span></span>  
   :::column-end:::
   :::column span="1":::
      <span data-ttu-id="d5596-140">**Исправлено** \ (скоро)</span><span class="sxs-lookup"><span data-stu-id="d5596-140">**Fixed** \(coming soon\)</span></span>  
      <span data-ttu-id="d5596-141">Выберите, чтобы упаковать биты Chromium в приложении.</span><span class="sxs-lookup"><span data-stu-id="d5596-141">Choose to package the Chromium bits in your application.</span></span>  
   :::column-end:::
   :::column span="1":::
      **<span data-ttu-id="d5596-142">Добавочное внедрение</span><span class="sxs-lookup"><span data-stu-id="d5596-142">Incremental adoption</span></span>**  
      <span data-ttu-id="d5596-143">Добавление части веб-компонентов в приложение.</span><span class="sxs-lookup"><span data-stu-id="d5596-143">Add web components piece by piece to your application.</span></span>  
   :::column-end:::
:::row-end:::

## <span data-ttu-id="d5596-144">Начало работы</span><span class="sxs-lookup"><span data-stu-id="d5596-144">Getting started</span></span>  

<span data-ttu-id="d5596-145">Чтобы создать и протестировать приложение с помощью элемента управления WebView2, необходимо установить [Microsoft EDGE (Chromium)](https://www.microsoftedgeinsider.com/download) и [WebView2 SDK](https://aka.ms/webviewnuget) .</span><span class="sxs-lookup"><span data-stu-id="d5596-145">To build and test your application using the WebView2 control, you need to have both [Microsoft Edge (Chromium)](https://www.microsoftedgeinsider.com/download) and the [WebView2 SDK](https://aka.ms/webviewnuget) installed.</span></span>  <span data-ttu-id="d5596-146">Чтобы приступить к работе, выберите один из следующих параметров.</span><span class="sxs-lookup"><span data-stu-id="d5596-146">Select one of the following options to get started.</span></span>  

*   [<span data-ttu-id="d5596-147">Начало работы с Win32 C/C++</span><span class="sxs-lookup"><span data-stu-id="d5596-147">Getting Started with Win32 C/C++</span></span>](./gettingstarted/win32.md)  
*   [<span data-ttu-id="d5596-148">Начало работы с WPF</span><span class="sxs-lookup"><span data-stu-id="d5596-148">Getting Started with WPF</span></span>](./gettingstarted/wpf.md)  
*   [<span data-ttu-id="d5596-149">Приступая к работе с WinForms</span><span class="sxs-lookup"><span data-stu-id="d5596-149">Getting Started with WinForms</span></span>](./gettingstarted/winforms.md)  

<span data-ttu-id="d5596-150">В репозитории [примеров WebView2](https://github.com/MicrosoftEdge/WebView2Samples) содержатся примеры, демонстрирующие все функции WebView2 SDK и модели использования API.</span><span class="sxs-lookup"><span data-stu-id="d5596-150">The [WebView2 Samples](https://github.com/MicrosoftEdge/WebView2Samples) repository contains samples that demonstrate all of the WebView2 SDKs features and API usage patterns.</span></span> <span data-ttu-id="d5596-151">По мере добавления дополнительных функций в пакет SDK для WebView2, образцы приложений будут обновлены.</span><span class="sxs-lookup"><span data-stu-id="d5596-151">As more features are added to the WebView2 SDK, the sample applications will be updated.</span></span>   

## <span data-ttu-id="d5596-152">Поддерживаемые платформы</span><span class="sxs-lookup"><span data-stu-id="d5596-152">Supported platforms</span></span>  

<span data-ttu-id="d5596-153">Предварительный просмотр для разработчиков доступен в следующих средах программирования.</span><span class="sxs-lookup"><span data-stu-id="d5596-153">A developer preview is available on the following programming environments.</span></span>  

*   <span data-ttu-id="d5596-154">Win32 C/C++</span><span class="sxs-lookup"><span data-stu-id="d5596-154">Win32 C/C++</span></span>  
*   <span data-ttu-id="d5596-155">.NET Framework 4.6.2 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="d5596-155">.NET Framework 4.6.2 or later</span></span>  
*   <span data-ttu-id="d5596-156">.NET Core 3,0 или более поздняя версия</span><span class="sxs-lookup"><span data-stu-id="d5596-156">.NET Core 3.0 or later</span></span>  
*   [<span data-ttu-id="d5596-157">WinUI 3,0</span><span class="sxs-lookup"><span data-stu-id="d5596-157">WinUI 3.0</span></span>](/uwp/toolkits/winui3/)  

<span data-ttu-id="d5596-158">Вы можете запускать приложения WebView2 в следующих версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="d5596-158">You are able to run WebView2 applications on the following versions of Windows.</span></span>  

*   <span data-ttu-id="d5596-159">Windows 10;</span><span class="sxs-lookup"><span data-stu-id="d5596-159">Windows 10</span></span>  
*   <span data-ttu-id="d5596-160">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="d5596-160">Windows 8.1</span></span>  
*   <span data-ttu-id="d5596-161">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d5596-161">Windows 8</span></span>  
*   <span data-ttu-id="d5596-162">Windows 7</span><span class="sxs-lookup"><span data-stu-id="d5596-162">Windows 7</span></span>  
*   <span data-ttu-id="d5596-163">WindowsServer2016</span><span class="sxs-lookup"><span data-stu-id="d5596-163">Windows Server 2016</span></span>  
*   <span data-ttu-id="d5596-164">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d5596-164">Windows Server 2012</span></span>  
*   <span data-ttu-id="d5596-165">Windows Server 2012R2</span><span class="sxs-lookup"><span data-stu-id="d5596-165">Windows Server 2012R2</span></span>  
*   <span data-ttu-id="d5596-166">Windows Server2008R2</span><span class="sxs-lookup"><span data-stu-id="d5596-166">Windows Server 2008 R2</span></span>  

## <span data-ttu-id="d5596-167">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="d5596-167">Next steps</span></span>  

<span data-ttu-id="d5596-168">Более подробную информацию о том, как создавать и развертывать приложения WebView2, вывлекать концептуальную документацию и практические руководства.</span><span class="sxs-lookup"><span data-stu-id="d5596-168">For more detailed information on how to build and deploy WebView2 applications, checkout the conceptual documentation and how-to guides.</span></span>  

#### <span data-ttu-id="d5596-169">Понятия</span><span class="sxs-lookup"><span data-stu-id="d5596-169">Concepts</span></span>  

*   [<span data-ttu-id="d5596-170">WebView2 SDK и Microsoft Edge Versions</span><span class="sxs-lookup"><span data-stu-id="d5596-170">WebView2 SDK and Microsoft Edge versioning</span></span>](./concepts/versioning.md)
*   [<span data-ttu-id="d5596-171">Распространение приложений WebView2</span><span class="sxs-lookup"><span data-stu-id="d5596-171">Distributing WebView2 applications</span></span>](./concepts/distribution.md)  
 
#### <span data-ttu-id="d5596-172">Практические руководства</span><span class="sxs-lookup"><span data-stu-id="d5596-172">How-To guides</span></span>  

*   [<span data-ttu-id="d5596-173">Отладка WebView2 с помощью DevTools и Visual Studio, отладка скриптов</span><span class="sxs-lookup"><span data-stu-id="d5596-173">Debugging WebView2 with DevTools and Visual Studio script debugging</span></span>](./howto/debug.md)  
*   [<span data-ttu-id="d5596-174">Автоматизация и отладка WebView2 с помощью Microsoft EdgeDriver</span><span class="sxs-lookup"><span data-stu-id="d5596-174">Automating and debugging WebView2 with Microsoft EdgeDriver</span></span>](./howto/webdriver.md)  

<!--todo: add how-tos when available  -->  

## <span data-ttu-id="d5596-175">Связь с командой WebView2</span><span class="sxs-lookup"><span data-stu-id="d5596-175">Getting in touch with the WebView2 team</span></span>  

<span data-ttu-id="d5596-176">Помогите вам создать более WebView2ную работу, отправив свой отзыв.</span><span class="sxs-lookup"><span data-stu-id="d5596-176">Help build a richer WebView2 experience by sharing your feedback.</span></span>  <span data-ttu-id="d5596-177">Чтобы отправить запросы на функции или отчеты об ошибках, посетите [репозиторий обратной связи](https://aka.ms/webviewfeedback) WebView.</span><span class="sxs-lookup"><span data-stu-id="d5596-177">Visit the WebView [feedback repo](https://aka.ms/webviewfeedback) to submit feature requests or bug reports.</span></span>  <span data-ttu-id="d5596-178">Кроме того, лучше всего искать известные проблемы.</span><span class="sxs-lookup"><span data-stu-id="d5596-178">It is also a good place to search for known issues.</span></span>  

> [!NOTE]
> <span data-ttu-id="d5596-179">В предварительной версии для разработчиков группа Microsoft Edge WebView также собирает данные, которые помогут вам создать более подWebView.</span><span class="sxs-lookup"><span data-stu-id="d5596-179">During developer preview, the Microsoft Edge WebView team also collects data to help build a better WebView.</span></span>  <span data-ttu-id="d5596-180">Пользователи могут отключить сбор данных WebView, перейдя `edge://settings/privacy` в браузер Microsoft EDGE и отключив коллекцию данных браузера.</span><span class="sxs-lookup"><span data-stu-id="d5596-180">Users may turn off WebView data collection by navigating to `edge://settings/privacy` in the Microsoft Edge browser and turning off browser data collection.</span></span>  
