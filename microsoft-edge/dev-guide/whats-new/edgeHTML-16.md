---
ms.assetid: 476c4b7a-be24-434b-a051-83f19d741aaf
description: В этом руководстве представлен обзор функций и стандартов для разработчиков, которые включены в Microsoft Edge.
title: Новые функции и API в EdgeHTML 16
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, разработчики, html, css, javascript, разработчики
ms.openlocfilehash: a15888bc8c1314d61d436759e5d63be942174ea4
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "10941932"
---
# <span data-ttu-id="38484-104">Новые возможности Microsoft EdgeHTML 16</span><span class="sxs-lookup"><span data-stu-id="38484-104">What's new in EdgeHTML 16</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="38484-105">Ниже перечислены новые и обновленные функции, публикуемые в [веб-платформе Microsoft Edge HTML 16,](https://blogs.windows.com/msedgedev/2017/10/17) в [рамках обновления](https://blogs.windows.com/windowsexperience/2017/10/17/whats-new-windows-10-fall-creators-update) \(10.10.2017, сборка 16299\).</span><span class="sxs-lookup"><span data-stu-id="38484-105">Here's a list of the new and updated features shipped in [EdgeHTML 16](https://blogs.windows.com/msedgedev/2017/10/17) web platform, as part of the [Windows 10 Fall Creators Update](https://blogs.windows.com/windowsexperience/2017/10/17/whats-new-windows-10-fall-creators-update) \(10/2017, Build 16299\).</span></span>  <span data-ttu-id="38484-106">Сведения об изменениях в конкретных сборках Windows Insider Preview см. в статье ["Изменение журнала изменений Microsoft Edge"](https://developer.microsoft.com/microsoft-edge/platform/changelog) и ["Новые возможности Microsoft EdgeHTML".](../whats-new.md)</span><span class="sxs-lookup"><span data-stu-id="38484-106">For changes in specific Windows Insider Preview builds, see the [Microsoft Edge Changelog](https://developer.microsoft.com/microsoft-edge/platform/changelog) and [What's New in EdgeHTML](../whats-new.md).</span></span>  

<span data-ttu-id="38484-107">Вот как и вот такая перечень изменений. [https://aka.ms/devguide_edgehtml_16](./edgehtml-16.md)</span><span class="sxs-lookup"><span data-stu-id="38484-107">Here's the permalink for the following list of changes:  [https://aka.ms/devguide_edgehtml_16](./edgehtml-16.md).</span></span>  

## <span data-ttu-id="38484-108">Новые и обновленные функции</span><span class="sxs-lookup"><span data-stu-id="38484-108">New and updated features</span></span>  

### <span data-ttu-id="38484-109">Макет сетки CSS</span><span class="sxs-lookup"><span data-stu-id="38484-109">CSS Grid Layout</span></span>  

<span data-ttu-id="38484-110">Теперь Microsoft Edge теперь поддерживает непрефиксированную реализацию макета [CSS.](https://www.w3.org/TR/css-grid-1)</span><span class="sxs-lookup"><span data-stu-id="38484-110">Microsoft Edge now supports the un-prefixed implementation of [CSS Grid Layout](https://www.w3.org/TR/css-grid-1).</span></span>  <span data-ttu-id="38484-111">[Макет сетки](https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout) определяет двумерную систему макета на основе сетки, которая повышает повышает повышенную четкость макета, чем возможно, расположить с помощью плаваток или сценариев.</span><span class="sxs-lookup"><span data-stu-id="38484-111">[Grid Layout](https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout) defines a two-dimensional grid-based layout system which enables more layout fluidity than possible with positioning using floats or scripts.</span></span>  <span data-ttu-id="38484-112">В примере ниже настроена структура для базовой веб-страницы с помощью макета CSS.</span><span class="sxs-lookup"><span data-stu-id="38484-112">The example below uses CSS Grid Layout to create the structure for a basic web page.</span></span>  

<iframe height='303' scrolling='no' title='<span data-ttu-id="38484-113">Макет сетки CSS</span><span class="sxs-lookup"><span data-stu-id="38484-113">CSS Grid Layout</span></span>' src='//codepen.io/MSEdgeDev/embed/mMQqZX/?height=303&theme-id=23761&default-tab=css,result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'><span data-ttu-id="38484-114">См. <a href='https://codepen.io/MSEdgeDev/pen/mMQqZX/'> сетку пера CSS </a> на mSEdgeDev <a href='https://codepen.io/MSEdgeDev'> </a> (@MSEdgeDev) на <a href='https://codepen.io'> кодировке Кодировки. </a></span><span class="sxs-lookup"><span data-stu-id="38484-114">See the Pen <a href='https://codepen.io/MSEdgeDev/pen/mMQqZX/'>CSS Grid Layout</a>by MSEdgeDev (<a href='https://codepen.io/MSEdgeDev'>@MSEdgeDev</a>) on <a href='https://codepen.io'>CodePen</a>.</span></span></iframe>  

### <span data-ttu-id="38484-115">Положение объекта CSS</span><span class="sxs-lookup"><span data-stu-id="38484-115">CSS object-fit and object-position</span></span>  

<span data-ttu-id="38484-116">Поддержка EdgeHTML 16 предлагает поддержку свойств CSS [`object-fit`](https://developer.mozilla.org/docs/Web/CSS/object-fit) [`object-position`](https://developer.mozilla.org/docs/Web/CSS/object-position) и.</span><span class="sxs-lookup"><span data-stu-id="38484-116">EdgeHTML 16 introduces support for CSS properties [`object-fit`](https://developer.mozilla.org/docs/Web/CSS/object-fit) and [`object-position`](https://developer.mozilla.org/docs/Web/CSS/object-position).</span></span>  <span data-ttu-id="38484-117">Эти свойства определяют положение и размер замещаемого содержимого в поле содержимого.</span><span class="sxs-lookup"><span data-stu-id="38484-117">These properties control the position and size of replaced content within the content box.</span></span>  

### <span data-ttu-id="38484-118">Средства разработчика</span><span class="sxs-lookup"><span data-stu-id="38484-118">Developer Tools</span></span>  

<span data-ttu-id="38484-119">Этот выпуск был начал рефакторского усилий для оценки и производительности, а также добавили набор новых функций, которые можно приступить к [использованию сборок Windows Insider.](https://insider.windows.com)</span><span class="sxs-lookup"><span data-stu-id="38484-119">This release we started a major Microsoft Edge DevTools refactoring effort for improved robustness and performance, and also added a bunch of new features you can start using today on [Windows Insider](https://insider.windows.com) builds.</span></span>  <span data-ttu-id="38484-120">Дополнительные сведения об [изменениях можно](../whats-new.md) найти в руководстве по разработчикам Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="38484-120">Check out the [Microsoft Edge DevTools guide](../whats-new.md) for more on what's changed!</span></span>  

### <span data-ttu-id="38484-121">JavaScript</span><span class="sxs-lookup"><span data-stu-id="38484-121">JavaScript</span></span>  

<span data-ttu-id="38484-122">[Сборки EdgeHTML 16 сборки BavaScript 16 с учетом оптимизации предыдущих выпусков JavaScript](https://blogs.windows.com/msedgedev/2017/10/31) путем расширения возможности обработчика функций для отклонения и повторения, использования повторяющихся кэшей и оптимизации функций `try` / `finally` с блоками.</span><span class="sxs-lookup"><span data-stu-id="38484-122">[EdgeHTML 16 builds on Javascript performance](https://blogs.windows.com/msedgedev/2017/10/31) optimizations of previous releases by expanding the Chakra engine's ability to defer/re-defer functions, use polymorphic inline caches, and optimize functions with `try`/`finally` blocks.</span></span>  

<span data-ttu-id="38484-123">Кроме того, функции, предварительно увидевшие функции в предварительной версии браузера Microsoft EdgeHTML 15, теперь по умолчанию доступны.</span><span class="sxs-lookup"><span data-stu-id="38484-123">Additionally, features first previewed in EdgeHTML 15 are now stable and enabled by default:</span></span>  

#### <span data-ttu-id="38484-124">Новые возможности</span><span class="sxs-lookup"><span data-stu-id="38484-124">New features</span></span>  

<span data-ttu-id="38484-125">Включено по умолчанию</span><span class="sxs-lookup"><span data-stu-id="38484-125">On by default</span></span>  

*   <span data-ttu-id="38484-126">[WebAssembly](https://developer.microsoft.com/microsoft-edge/platform/status/webassemblymvp/?q=WebAssembly) MVP \([демонстрация](https://webassembly.org/demo)\)</span><span class="sxs-lookup"><span data-stu-id="38484-126">[WebAssembly](https://developer.microsoft.com/microsoft-edge/platform/status/webassemblymvp/?q=WebAssembly) MVP \([demo](https://webassembly.org/demo)\)</span></span>  
*   [<span data-ttu-id="38484-127">Общие память и атоминцы</span><span class="sxs-lookup"><span data-stu-id="38484-127">Shared Memory and Atomics</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/sharedmemoryandatomics/?q=Atomics)  

### <span data-ttu-id="38484-128">API запроса оплаты</span><span class="sxs-lookup"><span data-stu-id="38484-128">Payment Request API</span></span>  

<span data-ttu-id="38484-129">[API запросов платежей](../windows-integration/payment-request-api.md) — это открытый aPI-браузера, который позволяет браузерам работать в качестве промежуточного промежуточного предприятия, потребителей и методов оплаты \(например, кредитных карт\).</span><span class="sxs-lookup"><span data-stu-id="38484-129">The [Payment Request API](../windows-integration/payment-request-api.md) is an open, cross-browser standard that enables browsers to act as an intermediary between merchants, consumers, and payment methods \(such as credit cards\) that consumers have stored in the cloud.</span></span>  <span data-ttu-id="38484-130">API в EdgeHTML 16 был обновлен в соответствии с последней [спецификацией API](https://w3c.github.io/payment-request) W3C.</span><span class="sxs-lookup"><span data-stu-id="38484-130">The API in EdgeHTML 16 has been updated to match the latest W3C [Payment Request API](https://w3c.github.io/payment-request) specification.</span></span>  <span data-ttu-id="38484-131">К ним относятся:</span><span class="sxs-lookup"><span data-stu-id="38484-131">This includes:</span></span>  

*   <span data-ttu-id="38484-132">Поддержка `canMakePayment()` метода</span><span class="sxs-lookup"><span data-stu-id="38484-132">Support for the `canMakePayment()` method</span></span>  
*   <span data-ttu-id="38484-133">Поддержка `requestId` свойства</span><span class="sxs-lookup"><span data-stu-id="38484-133">Support for the `requestId` property</span></span>  
*   <span data-ttu-id="38484-134">Поддержка `id` свойства</span><span class="sxs-lookup"><span data-stu-id="38484-134">Support for the `id` property</span></span>  
*   <span data-ttu-id="38484-135">Значение по умолчанию для `complete()` параметра метода `result` изменен с "неизвестно" на "неизвестно"</span><span class="sxs-lookup"><span data-stu-id="38484-135">The default value for the `complete()` method's `result` parameter changed from " " to "unknown"</span></span>  

### <span data-ttu-id="38484-136">Служебные сценарии</span><span class="sxs-lookup"><span data-stu-id="38484-136">Service Workers</span></span>  

<span data-ttu-id="38484-137">[Работники служб — это](https://www.w3.org/TR/service-workers-1) сценарии на основании событий, которые выполняются в фоновом режиме веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="38484-137">[Service Workers](https://www.w3.org/TR/service-workers-1) are event-driven scripts that run in the background of a web page.</span></span>  <span data-ttu-id="38484-138">Сотрудники служб, ранее доступные только с собственными приложениями, такими как перекрестные запросы и обработка запросов из сети, управление фоном и обработкой фонового хранилища, локальное хранилище и push-уведомления.</span><span class="sxs-lookup"><span data-stu-id="38484-138">Service workers enable functionality previously only available with native apps like intercepting and handling requests from the network, managing and handling background sync, local storage, and push notifications.</span></span>  <span data-ttu-id="38484-139">Поддержка для работника по обслуживанию еще работает над разработкой, но вы можете протестировать поддержку PWA в Microsoft Edge с эксперименальными службами, включив `about:flags` функцию.</span><span class="sxs-lookup"><span data-stu-id="38484-139">Support for service worker is still in development, but you can test out your PWA in Microsoft Edge with our experimental service worker support by enabling the service worker feature in `about:flags`.</span></span>  

### <span data-ttu-id="38484-140">WebVR</span><span class="sxs-lookup"><span data-stu-id="38484-140">WebVR</span></span>  

<span data-ttu-id="38484-141">Приложение WebVR для Microsoft Edge добавила поддержку [контроллеров движения.](https://developer.microsoft.com/windows/mixed-reality/motion_controllers)</span><span class="sxs-lookup"><span data-stu-id="38484-141">WebVR for Microsoft Edge has added support for [motion controllers](https://developer.microsoft.com/windows/mixed-reality/motion_controllers).</span></span>  <span data-ttu-id="38484-142">Эти контроллеры имеют тщательное положение пространства, с помощью которой в виртуальной реальности виртуально подходят для взаимодействия с цифровыми объектами.</span><span class="sxs-lookup"><span data-stu-id="38484-142">These controllers have a precise position in space, allowing for fine grained interaction with digital objects in virtual reality.</span></span>  

:::image type="complex" source="../media/MotionControllers.jpg" alt-text="Контроллеры перемещения" lightbox="../media/MotionControllers.jpg":::
   <span data-ttu-id="38484-144">Контроллеры перемещения</span><span class="sxs-lookup"><span data-stu-id="38484-144">Motion controllers</span></span>  
:::image-end:::  

<span data-ttu-id="38484-145">Также был оптимизирован веб-виртуал изменений для поддержки двух разных типов возможностей.</span><span class="sxs-lookup"><span data-stu-id="38484-145">WebVR has also been optimized to support two different types of experiences.</span></span>  

<span data-ttu-id="38484-146">**Компьютеры с Windows Mixed Reality** — настольные компьютеры и ноутбуки с интегрированными графикой.</span><span class="sxs-lookup"><span data-stu-id="38484-146">**Windows Mixed Reality PCs** - Desktops and laptops with integrated graphics.</span></span>  <span data-ttu-id="38484-147">После установки к этим устройствам наши мелодии гарнитуры будут работать в 60 кадров в секунду.</span><span class="sxs-lookup"><span data-stu-id="38484-147">When plugged into these devices, our immersive headsets will run at 60 frames per second.</span></span>  
<span data-ttu-id="38484-148">**Windows Mixed Reality —** компьютеры и ноутбуки с разными графическими объектами.</span><span class="sxs-lookup"><span data-stu-id="38484-148">**Windows Mixed Reality Ultra PCs** - Desktops and laptops with discrete graphics.</span></span>  <span data-ttu-id="38484-149">После установки к этим устройствам наши иммерсивные гарнитуры будут работать в течение 90 кадров в секунду.</span><span class="sxs-lookup"><span data-stu-id="38484-149">When plugged into these devices, our immersive headsets will run at 90 frames per second.</span></span>  

<span data-ttu-id="38484-150">Обе настройки поддерживают одно и то же взаимодействие с видео и играми.</span><span class="sxs-lookup"><span data-stu-id="38484-150">Both setups will support the same immersive video and gaming experiences.</span></span>  

<span data-ttu-id="38484-151">Дополнительные сведения о предстоящих обновлениях Windows Mixed Reality см. в записи блога об обновлениях [windows Mixed Reality.](https://blogs.windows.com/windowsexperience/2017/08/28/windows-mixed-reality-holiday-update)</span><span class="sxs-lookup"><span data-stu-id="38484-151">For more info about the upcoming Windows Mixed Reality updates, check out the [Windows Mixed Reality](https://blogs.windows.com/windowsexperience/2017/08/28/windows-mixed-reality-holiday-update) holiday update blog post.</span></span>  

<span data-ttu-id="38484-152">Для направляющей и демонстраций см. руководство [для разработчиков WebVR.](/microsoft-edge/webvr)</span><span class="sxs-lookup"><span data-stu-id="38484-152">For guides and demos, head over to the [WebVR Developer Guide](/microsoft-edge/webvr).</span></span>  

 > [!NOTE] 
 > <span data-ttu-id="38484-153">Так как речь WebVR еще находится в разработке, реализация Microsoft Edge может измениться ниже строки ниже.</span><span class="sxs-lookup"><span data-stu-id="38484-153">Since the WebVR spec is still in development, Microsoft Edge's implementation may change later down the line.</span></span>  

## <span data-ttu-id="38484-154">Новые API в EdgeHTML 16</span><span class="sxs-lookup"><span data-stu-id="38484-154">New APIs in EdgeHTML 16</span></span>  

<span data-ttu-id="38484-155">Ниже приведен полный список новых aPI в EdgeHTML 16.</span><span class="sxs-lookup"><span data-stu-id="38484-155">Here's the full list of new APIs in EdgeHTML 16.</span></span>  <span data-ttu-id="38484-156">Они указаны в `[interface name].[api name]` формате.</span><span class="sxs-lookup"><span data-stu-id="38484-156">They are listed in the format of `[interface name].[api name]`.</span></span>

> [!NOTE] 
> <span data-ttu-id="38484-157">Хотя в DOM представлены указанные ниже API, конечные советы по могут быть настоящими.</span><span class="sxs-lookup"><span data-stu-id="38484-157">Although the following APIs are exposed in the DOM, the end-to-end behavior of some might still be in development.</span></span>  <span data-ttu-id="38484-158">Сведения о  [том, почему официальное слово](https://developer.microsoft.com/microsoft-edge/platform/status) доступно в поддержке функций, см. в статье о состоянии платформы Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="38484-158">Refer to  [Microsoft Edge platform status](https://developer.microsoft.com/microsoft-edge/platform/status) for the official word on feature support.</span></span>  

---  

<iframe height='559' scrolling='no' title='<span data-ttu-id="38484-159">Новые API в EdgeHTML 16</span><span class="sxs-lookup"><span data-stu-id="38484-159">New APIs in EdgeHTML 16</span></span>' src='//codepen.io/MSEdgeDev/embed/jLGZZY/?height=559&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true'><span data-ttu-id="38484-160">См. раздел <a href='https://codepen.io/MSEdgeDev/pen/jLGZZY/'> "Новый API" в EdgeHTML 16 </a> на MSEdgeDev <a href='https://codepen.io/MSEdgeDev'> </a> (@MSEdgeDev) на <a href='https://codepen.io'> коде CodePen. </a></span><span class="sxs-lookup"><span data-stu-id="38484-160">See the Pen <a href='https://codepen.io/MSEdgeDev/pen/jLGZZY/'>New APIs in EdgeHTML 16</a>by MSEdgeDev (<a href='https://codepen.io/MSEdgeDev'>@MSEdgeDev</a>) on <a href='https://codepen.io'>CodePen</a>.</span></span></iframe>  

---  

## <span data-ttu-id="38484-161">Предыдущие выпуски EdgeHTML</span><span class="sxs-lookup"><span data-stu-id="38484-161">Previous EdgeHTML releases</span></span>  

[<span data-ttu-id="38484-162">EdgeHTML 12/ Windows сборка 10240 (07.07.2015)</span><span class="sxs-lookup"><span data-stu-id="38484-162">EdgeHTML 12 / Windows build 10240 (7/2015)</span></span>](./edgehtml-12.md)  

[<span data-ttu-id="38484-163">EdgeHTML 13 / Windows сборка 10586 (11.11.2015)</span><span class="sxs-lookup"><span data-stu-id="38484-163">EdgeHTML 13 / Windows build 10586 (11/2015)</span></span>](./edgehtml-13.md)  

[<span data-ttu-id="38484-164">EdgeHTML 14/ Windows сборка 14393 (8.08.2016)</span><span class="sxs-lookup"><span data-stu-id="38484-164">EdgeHTML 14 / Windows build 14393 (8/2016)</span></span>](./edgehtml-14.md)  

[<span data-ttu-id="38484-165">EdgeHTML 15 / Windows сборка 15063 (4.04.2017)</span><span class="sxs-lookup"><span data-stu-id="38484-165">EdgeHTML 15 / Windows build 15063 (4/2017)</span></span>](./edgehtml-15.md)  
