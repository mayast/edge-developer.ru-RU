---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: f9bedb19620b0669d4aac35be4786702940b2a72
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654707"
---
# <span data-ttu-id="6aa25-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2WebMessageReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="6aa25-104">Microsoft.Web.WebView2.Core.CoreWebView2WebMessageReceivedEventArgs class</span></span> 

<span data-ttu-id="6aa25-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="6aa25-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="6aa25-106">Сборка: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="6aa25-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="6aa25-107">Аргументы события для события WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="6aa25-107">Event args for the WebMessageReceived event.</span></span>

## <span data-ttu-id="6aa25-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="6aa25-108">Summary</span></span>

 <span data-ttu-id="6aa25-109">Участников</span><span class="sxs-lookup"><span data-stu-id="6aa25-109">Members</span></span>                        | <span data-ttu-id="6aa25-110">Описания</span><span class="sxs-lookup"><span data-stu-id="6aa25-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6aa25-111">Источник</span><span class="sxs-lookup"><span data-stu-id="6aa25-111">Source</span></span>](#source) | <span data-ttu-id="6aa25-112">Универсальный код ресурса (URI) документа, отправившего это веб-сообщение.</span><span class="sxs-lookup"><span data-stu-id="6aa25-112">The URI of the document that sent this web message.</span></span>
[<span data-ttu-id="6aa25-113">WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="6aa25-113">WebMessageAsJson</span></span>](#webmessageasjson) | <span data-ttu-id="6aa25-114">Сообщение, опубликованное из содержимого WebView на узел, преобразованное в строку JSON.</span><span class="sxs-lookup"><span data-stu-id="6aa25-114">The message posted from the webview content to the host converted to a JSON string.</span></span>
[<span data-ttu-id="6aa25-115">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="6aa25-115">TryGetWebMessageAsString</span></span>](#trygetwebmessageasstring) | <span data-ttu-id="6aa25-116">Если сообщение, опубликованное из содержимого WebView, содержит строковый тип, этот метод возвратит значение этой строки.</span><span class="sxs-lookup"><span data-stu-id="6aa25-116">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

## <span data-ttu-id="6aa25-117">Участников</span><span class="sxs-lookup"><span data-stu-id="6aa25-117">Members</span></span>

#### <span data-ttu-id="6aa25-118">Источник</span><span class="sxs-lookup"><span data-stu-id="6aa25-118">Source</span></span> 

<span data-ttu-id="6aa25-119">Универсальный код ресурса (URI) документа, отправившего это веб-сообщение.</span><span class="sxs-lookup"><span data-stu-id="6aa25-119">The URI of the document that sent this web message.</span></span>

> <span data-ttu-id="6aa25-120">[источник](#source) общедоступной строки</span><span class="sxs-lookup"><span data-stu-id="6aa25-120">public string [Source](#source)</span></span>

#### <span data-ttu-id="6aa25-121">WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="6aa25-121">WebMessageAsJson</span></span> 

<span data-ttu-id="6aa25-122">Сообщение, опубликованное из содержимого WebView на узел, преобразованное в строку JSON.</span><span class="sxs-lookup"><span data-stu-id="6aa25-122">The message posted from the webview content to the host converted to a JSON string.</span></span>

> <span data-ttu-id="6aa25-123">общедоступная строка [WebMessageAsJson](#webmessageasjson)</span><span class="sxs-lookup"><span data-stu-id="6aa25-123">public string [WebMessageAsJson](#webmessageasjson)</span></span>

<span data-ttu-id="6aa25-124">Используйте этот способ для обмена данными с помощью объектов JavaScript.</span><span class="sxs-lookup"><span data-stu-id="6aa25-124">Use this to communicate via JavaScript objects.</span></span>

<span data-ttu-id="6aa25-125">Например, следующие вызовы в сообщении WebMessageAsJson приводят к следующим значениям:</span><span class="sxs-lookup"><span data-stu-id="6aa25-125">For example the following postMessage calls result in the following WebMessageAsJson values:</span></span>

```
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### <span data-ttu-id="6aa25-126">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="6aa25-126">TryGetWebMessageAsString</span></span> 

<span data-ttu-id="6aa25-127">Если сообщение, опубликованное из содержимого WebView, содержит строковый тип, этот метод возвратит значение этой строки.</span><span class="sxs-lookup"><span data-stu-id="6aa25-127">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

> <span data-ttu-id="6aa25-128">public string [TryGetWebMessageAsString](#trygetwebmessageasstring)()</span><span class="sxs-lookup"><span data-stu-id="6aa25-128">public string [TryGetWebMessageAsString](#trygetwebmessageasstring)()</span></span>

<span data-ttu-id="6aa25-129">Если сообщение Опубликовано в другом типе JavaScript, этот метод завершается сбоем с E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="6aa25-129">If the message posted is some other kind of JavaScript type this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="6aa25-130">Используйте этот способ для обмена сообщениями через простые строки.</span><span class="sxs-lookup"><span data-stu-id="6aa25-130">Use this to communicate via simple strings.</span></span>

<span data-ttu-id="6aa25-131">Например, следующие вызовы в сообщении WebMessageAsString приводят к следующим значениям:</span><span class="sxs-lookup"><span data-stu-id="6aa25-131">For example the following postMessage calls result in the following WebMessageAsString values:</span></span>

```
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```

