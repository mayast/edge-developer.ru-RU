---
description: Потоковая модель
title: Потоковая модель
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения WPF, WPF, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "браузер", HTML Edge
ms.openlocfilehash: ad51afee97d3cc3e913ecdd73c4f0c2a99c70564
ms.sourcegitcommit: 553957c101f83681b363103cb6af56bf20173f23
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/24/2020
ms.locfileid: "10895562"
---
# <span data-ttu-id="9d96c-104">Потоковая модель</span><span class="sxs-lookup"><span data-stu-id="9d96c-104">Threading model</span></span>  

## <span data-ttu-id="9d96c-105">Безопасность потоков</span><span class="sxs-lookup"><span data-stu-id="9d96c-105">Thread safety</span></span>  

<span data-ttu-id="9d96c-106">WebView2 должен создаваться в потоке пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="9d96c-106">The WebView2 must be created on a UI thread.</span></span>  <span data-ttu-id="9d96c-107">В частности, поток с конвейером сообщений.</span><span class="sxs-lookup"><span data-stu-id="9d96c-107">Specifically a thread with a message pump.</span></span>  <span data-ttu-id="9d96c-108">Все обратные вызовы выполняются в этом потоке и запросы в WebView2 должны выполняться в этом потоке.</span><span class="sxs-lookup"><span data-stu-id="9d96c-108">All callbacks occur on that thread and requests into the WebView2 must be done on that thread.</span></span>  <span data-ttu-id="9d96c-109">Небезопасно использовать WebView2 из другого потока.</span><span class="sxs-lookup"><span data-stu-id="9d96c-109">It is not safe to use the WebView2 from another thread.</span></span>  

<span data-ttu-id="9d96c-110">Единственным исключением является `Content` свойство `CoreWebView2WebResourceRequest` .</span><span class="sxs-lookup"><span data-stu-id="9d96c-110">The only exception is for the `Content` property of `CoreWebView2WebResourceRequest`.</span></span>  <span data-ttu-id="9d96c-111">`Content`Поток свойств читается из фонового потока.</span><span class="sxs-lookup"><span data-stu-id="9d96c-111">The `Content` property stream is read from a background thread.</span></span>  <span data-ttu-id="9d96c-112">Поток должен быть гибким или создаваться из фонового STA, чтобы предотвратить снижение производительности потока пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="9d96c-112">The stream should be agile or be created from a background STA to prevent performance impact to the UI thread.</span></span>  

## <span data-ttu-id="9d96c-113">Повторный вход</span><span class="sxs-lookup"><span data-stu-id="9d96c-113">Reentrancy</span></span>  

<span data-ttu-id="9d96c-114">Обратные вызовы, в том числе обработчики событий и обработчики завершения выполняются последовательно.</span><span class="sxs-lookup"><span data-stu-id="9d96c-114">Callbacks including event handlers and completion handlers run serially.</span></span>  <span data-ttu-id="9d96c-115">Если на вашем компьютере запущен обработчик событий и начинается цикл обработки сообщений, никакие другие обработчики событий и обратные вызовы завершения не смогут начать работу в небезопасном режиме.</span><span class="sxs-lookup"><span data-stu-id="9d96c-115">If you have an event handler running and begin a message loop, no other event handlers or completion callbacks are able to begin running in a reentrant manner.</span></span>  

## <span data-ttu-id="9d96c-116">Отсрочки</span><span class="sxs-lookup"><span data-stu-id="9d96c-116">Deferrals</span></span>  

<span data-ttu-id="9d96c-117">Некоторые события WebView2 считывают значения, заданные для аргументов события, или выполняют некоторые действия после завершения обработчика событий.</span><span class="sxs-lookup"><span data-stu-id="9d96c-117">Some WebView2 events read values set on their event args or perform some action after the event handler completes.</span></span>  <span data-ttu-id="9d96c-118">Если вам также необходимо запустить асинхронную операцию, например обработчик событий, вы можете использовать `GetDeferral` метод для аргументов событий связанных событий.</span><span class="sxs-lookup"><span data-stu-id="9d96c-118">If you also need to run an asynchronous operation such an event handler, you may use the `GetDeferral` method on the event args of the associated events.</span></span>  <span data-ttu-id="9d96c-119">Возвращенный объект РБП гарантирует, что обработчик событий не считается завершенным до тех пор, пока `Complete` `Deferral` не будет запрошен метод.</span><span class="sxs-lookup"><span data-stu-id="9d96c-119">The returned Deferral object ensures the event handler is not considered complete until the `Complete` method of the `Deferral` is requested.</span></span>  

<span data-ttu-id="9d96c-120">Например, вы можете использовать `NewWindowRequested` событие для предоставления `CoreWebView2` соединения в качестве дочернего окна при завершении обработчика событий.</span><span class="sxs-lookup"><span data-stu-id="9d96c-120">For instance, you may use the `NewWindowRequested` event to provide a `CoreWebView2` to connect as a child window when the event handler completes.</span></span>  <span data-ttu-id="9d96c-121">Но если требуется асинхронное создание `CoreWebView2` запроса, запросите `GetDeferral` метод в `NewWindowRequestedEventArgs` .</span><span class="sxs-lookup"><span data-stu-id="9d96c-121">But if you need to asynchronously create the `CoreWebView2`, request the `GetDeferral` method on the `NewWindowRequestedEventArgs`.</span></span>  <span data-ttu-id="9d96c-122">После того как вы создадите асинхронно `CoreWebView2` и установите `NewWindow` свойство в `NewWindowRequestedEventArgs` запросе, что `Complete` `Deferral` необходимо будет вернуть объект с помощью `GetDeferral` метода.</span><span class="sxs-lookup"><span data-stu-id="9d96c-122">After you have asynchronously created the `CoreWebView2` and set the `NewWindow` property on the `NewWindowRequestedEventArgs`, request `Complete` on the `Deferral` object be returned using the `GetDeferral` method.</span></span>  

<!-- links -->  
