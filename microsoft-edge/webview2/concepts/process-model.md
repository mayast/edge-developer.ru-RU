---
description: Модель процесса
title: Модель процесса
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения WPF, WPF, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "браузер", HTML Edge
ms.openlocfilehash: 8548308896815266fbd1e150da979b56cfb268e2
ms.sourcegitcommit: 553957c101f83681b363103cb6af56bf20173f23
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/24/2020
ms.locfileid: "10895563"
---
# <span data-ttu-id="6c019-104">Модель процесса</span><span class="sxs-lookup"><span data-stu-id="6c019-104">Process model</span></span>  

<span data-ttu-id="6c019-105">WebView2 использует ту же модель процессов, что и браузер Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6c019-105">WebView2 uses the same process model as the Microsoft Edge browser.</span></span>  <span data-ttu-id="6c019-106">Дополнительные сведения о модели процесса браузера можно найти в разделе [архитектура браузеров — внутреннее представление в современном веб-браузере][GoogleDeveloperWebUpdates201809InsideBrowserPart1BrowserArchitecture].</span><span class="sxs-lookup"><span data-stu-id="6c019-106">For more information about the browser process model, see [Browser Architecture - Inside look at modern web browser][GoogleDeveloperWebUpdates201809InsideBrowserPart1BrowserArchitecture].</span></span> 

<span data-ttu-id="6c019-107">Один процесс браузера связан с процессами рендеринга и другими служебными процессами, описанными в этой статье.</span><span class="sxs-lookup"><span data-stu-id="6c019-107">One browser process is associated with the renderer processes and other utility processes as described in that article.</span></span>  <span data-ttu-id="6c019-108">Кроме того, в случае WebView2 есть ведущее приложение, запрашивающее процессы с помощью WebView2.</span><span class="sxs-lookup"><span data-stu-id="6c019-108">Additionally, in the case of WebView2, there are host app requesting processes using WebView2.</span></span>  

:::image type="complex" source="../media/process-model-1.png" alt-text="Процесс 1" lightbox="../media/process-model-1.png":::
   <span data-ttu-id="6c019-110">Процесс 1</span><span class="sxs-lookup"><span data-stu-id="6c019-110">Process 1</span></span>  
:::image-end:::  

<span data-ttu-id="6c019-111">Один процесс браузера определяется для папки данных пользователя в сеансе пользователя, который обслуживает любые запросы WebView2, указывающие на папку данных пользователя.</span><span class="sxs-lookup"><span data-stu-id="6c019-111">One browser process is specified per user data folder in a user session that serve any WebView2 requesting process that specifies that user data folder.</span></span>  <span data-ttu-id="6c019-112">Это означает, что один процесс браузера может обслуживать несколько запросов, а один процесс может использовать несколько процессов браузера.</span><span class="sxs-lookup"><span data-stu-id="6c019-112">This means one browser process may be serving multiple requesting processes and one requesting process may be using multiple browser processes.</span></span>  

:::image type="complex" source="../media/process-model-2.png" alt-text="Процесс 2" lightbox="../media/process-model-2.png":::
   <span data-ttu-id="6c019-114">Процесс 2</span><span class="sxs-lookup"><span data-stu-id="6c019-114">Process 2</span></span>  
:::image-end:::  

<span data-ttu-id="6c019-115">Процесс браузера имеет некоторое количество сопоставленных процессов рендеринга.</span><span class="sxs-lookup"><span data-stu-id="6c019-115">A browser process has some number of associated renderer processes.</span></span>  <span data-ttu-id="6c019-116">Процессы браузеров создаются в соответствии с требованиями для обслуживания потенциально нескольких кадров в разных экземплярах WebView2.</span><span class="sxs-lookup"><span data-stu-id="6c019-116">The browser processes are created as required to service potentially multiple frames in different instances of WebView2.</span></span>  <span data-ttu-id="6c019-117">Количество процессов обработки может различаться в зависимости от функции браузера "изоляция сайта" и количества отдельных отключенных относящихся друг от друга экземпляров WebView2.</span><span class="sxs-lookup"><span data-stu-id="6c019-117">The number of renderer processes varies based on the site isolation browser feature and the number of distinct disconnected origins rendered in associated instances of WebView2.</span></span>  <span data-ttu-id="6c019-118">Функция браузера "изоляция сайта" описана в предыдущем содержимом.</span><span class="sxs-lookup"><span data-stu-id="6c019-118">The site isolation browser feature is described in the previous content.</span></span>  

<span data-ttu-id="6c019-119">`CoreWebView2Environment`Представляет папку данных пользователя и процесс браузера.</span><span class="sxs-lookup"><span data-stu-id="6c019-119">The `CoreWebView2Environment` represents a user data folder and browser process.</span></span>  <span data-ttu-id="6c019-120">Этот параметр не `CoreWebView2` соответствует ни одному набору процессов, так как в зависимости от изоляции сайта в соответствии с описанной ниже изоляцией используются различные процессы обработчика.</span><span class="sxs-lookup"><span data-stu-id="6c019-120">The `CoreWebView2` does not directly correspond to any one set of processes since various renderer processes are used by a WebView2 depending on site isolation as previously described.</span></span>  

<span data-ttu-id="6c019-121">Вы можете реагировать на сбои и зависания в таких процессах браузера и отрисовки, использующих `ProcessFailed` событие `CoreWebView2` .</span><span class="sxs-lookup"><span data-stu-id="6c019-121">You are able to react to crashes and hangs in these browser and renderer processes using the `ProcessFailed` event of `CoreWebView2`.</span></span>  

<span data-ttu-id="6c019-122">Вы можете безопасно завершить работу связанных браузеров и процессов отрисовки с помощью `Close` метода `CoreWebView2Controller` .</span><span class="sxs-lookup"><span data-stu-id="6c019-122">You are able to safely shutdown associated browser and renderer processes using the `Close` method of `CoreWebView2Controller`.</span></span>  

<span data-ttu-id="6c019-123">Чтобы открыть окно диспетчера задач браузера из окна **DevTools** экземпляра WebView2, вы можете выбрать `Shift` + `Escape` или навести указатель мыши в заголовке окна DevTools, открыть контекстное меню (щелкнуть правой кнопкой мыши \) и выбрать `Browser task manager` .</span><span class="sxs-lookup"><span data-stu-id="6c019-123">To open the Browser Task Manager window from the **DevTools** window of a WebView2 instance, you are able to select `Shift`+`Escape` or hover on the DevTools window title bar, open the contextual menu \(right-click\), and choose `Browser task manager`.</span></span>  <span data-ttu-id="6c019-124">Будут отображены все процессы, связанные с процессом браузера вашего WebView2, в том числе связанные с ними цели.</span><span class="sxs-lookup"><span data-stu-id="6c019-124">All processes associated with the browser process of your WebView2 are displayed including associated purposes.</span></span>  

<!-- links -->  

[GoogleDeveloperWebUpdates201809InsideBrowserPart1BrowserArchitecture]: https://developers.google.com/web/updates/2018/09/inside-browser-part1#browser-architecture "Архитектура браузера — внутреннее представление в современном веб-браузере (часть 1)"  
