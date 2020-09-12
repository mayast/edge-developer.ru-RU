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
ms.openlocfilehash: 61e3b7fc8d25e2a1ce9c60fb84f5f39ba43f281b
ms.sourcegitcommit: efdc6369c48942bfa39e45c713300ed70f0e3655
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/12/2020
ms.locfileid: "11013739"
---
# <span data-ttu-id="9b30f-104">Потоковая модель</span><span class="sxs-lookup"><span data-stu-id="9b30f-104">Threading model</span></span> 

<span data-ttu-id="9b30f-105">Элемент управления WebView2 основывается на [объектной модели компонентов (com)](https://docs.microsoft.com/windows/win32/com/the-component-object-model) и должен выполняться в потоке [однопотоковых апартаментов (STA)](https://docs.microsoft.com/windows/win32/com/single-threaded-apartments) .</span><span class="sxs-lookup"><span data-stu-id="9b30f-105">The WebView2 control is based on the [Component Object Model (COM)](https://docs.microsoft.com/windows/win32/com/the-component-object-model) and must run on a [Single Threaded Apartments (STA)](https://docs.microsoft.com/windows/win32/com/single-threaded-apartments) thread.</span></span>

## <span data-ttu-id="9b30f-106">Безопасность потоков</span><span class="sxs-lookup"><span data-stu-id="9b30f-106">Thread safety</span></span>  

<span data-ttu-id="9b30f-107">WebView2 должен создаваться в потоке пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="9b30f-107">The WebView2 must be created on a UI thread.</span></span>  <span data-ttu-id="9b30f-108">В частности, поток с конвейером сообщений.</span><span class="sxs-lookup"><span data-stu-id="9b30f-108">Specifically a thread with a message pump.</span></span>  <span data-ttu-id="9b30f-109">Все обратные вызовы выполняются в этом потоке и запросы в WebView2 должны выполняться в этом потоке.</span><span class="sxs-lookup"><span data-stu-id="9b30f-109">All callbacks occur on that thread and requests into the WebView2 must be done on that thread.</span></span>  <span data-ttu-id="9b30f-110">Небезопасно использовать WebView2 из другого потока.</span><span class="sxs-lookup"><span data-stu-id="9b30f-110">It is not safe to use the WebView2 from another thread.</span></span>  

<span data-ttu-id="9b30f-111">Единственным исключением является `Content` свойство `CoreWebView2WebResourceRequest` .</span><span class="sxs-lookup"><span data-stu-id="9b30f-111">The only exception is for the `Content` property of `CoreWebView2WebResourceRequest`.</span></span>  <span data-ttu-id="9b30f-112">`Content`Поток свойств читается из фонового потока.</span><span class="sxs-lookup"><span data-stu-id="9b30f-112">The `Content` property stream is read from a background thread.</span></span>  <span data-ttu-id="9b30f-113">Поток должен быть гибким или создаваться из фонового STA, чтобы предотвратить снижение производительности потока пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="9b30f-113">The stream should be agile or be created from a background STA to prevent performance impact to the UI thread.</span></span>  

## <span data-ttu-id="9b30f-114">Повторный вход</span><span class="sxs-lookup"><span data-stu-id="9b30f-114">Reentrancy</span></span>  

<span data-ttu-id="9b30f-115">Обратные вызовы, в том числе обработчики событий и обработчики завершения выполняются последовательно.</span><span class="sxs-lookup"><span data-stu-id="9b30f-115">Callbacks including event handlers and completion handlers run serially.</span></span>  <span data-ttu-id="9b30f-116">Если на вашем компьютере запущен обработчик событий и начинается цикл обработки сообщений, никакие другие обработчики событий и обратные вызовы завершения не смогут начать работу в небезопасном режиме.</span><span class="sxs-lookup"><span data-stu-id="9b30f-116">If you have an event handler running and begin a message loop, no other event handlers or completion callbacks are able to begin running in a reentrant manner.</span></span>  

## <span data-ttu-id="9b30f-117">Отсрочки</span><span class="sxs-lookup"><span data-stu-id="9b30f-117">Deferrals</span></span>  

<span data-ttu-id="9b30f-118">Некоторые события WebView2 считывают значения, заданные для аргументов события, или выполняют некоторые действия после завершения обработчика событий.</span><span class="sxs-lookup"><span data-stu-id="9b30f-118">Some WebView2 events read values set on their event args or perform some action after the event handler completes.</span></span>  <span data-ttu-id="9b30f-119">Если вам также необходимо запустить асинхронную операцию, например обработчик событий, вы можете использовать `GetDeferral` метод для аргументов событий связанных событий.</span><span class="sxs-lookup"><span data-stu-id="9b30f-119">If you also need to run an asynchronous operation such an event handler, you may use the `GetDeferral` method on the event args of the associated events.</span></span>  <span data-ttu-id="9b30f-120">Возвращенный объект РБП гарантирует, что обработчик событий не считается завершенным до тех пор, пока `Complete` `Deferral` не будет запрошен метод.</span><span class="sxs-lookup"><span data-stu-id="9b30f-120">The returned Deferral object ensures the event handler is not considered complete until the `Complete` method of the `Deferral` is requested.</span></span>  

<span data-ttu-id="9b30f-121">Например, вы можете использовать `NewWindowRequested` событие для предоставления `CoreWebView2` соединения в качестве дочернего окна при завершении обработчика событий.</span><span class="sxs-lookup"><span data-stu-id="9b30f-121">For instance, you may use the `NewWindowRequested` event to provide a `CoreWebView2` to connect as a child window when the event handler completes.</span></span>  <span data-ttu-id="9b30f-122">Но если требуется асинхронное создание `CoreWebView2` запроса, запросите `GetDeferral` метод в `NewWindowRequestedEventArgs` .</span><span class="sxs-lookup"><span data-stu-id="9b30f-122">But if you need to asynchronously create the `CoreWebView2`, request the `GetDeferral` method on the `NewWindowRequestedEventArgs`.</span></span>  <span data-ttu-id="9b30f-123">После того как вы создадите асинхронно `CoreWebView2` и установите `NewWindow` свойство в `NewWindowRequestedEventArgs` запросе, что `Complete` `Deferral` необходимо будет вернуть объект с помощью `GetDeferral` метода.</span><span class="sxs-lookup"><span data-stu-id="9b30f-123">After you have asynchronously created the `CoreWebView2` and set the `NewWindow` property on the `NewWindowRequestedEventArgs`, request `Complete` on the `Deferral` object be returned using the `GetDeferral` method.</span></span>  

<!-- links -->  
