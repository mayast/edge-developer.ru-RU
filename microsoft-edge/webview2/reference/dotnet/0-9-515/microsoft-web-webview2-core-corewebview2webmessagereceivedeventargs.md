---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2WebMessageReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: a3d1f899cb270f9a44d92d647ab2f5a4d5c3b02a
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886369"
---
# <span data-ttu-id="09f90-104">класс 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2WebMessageReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="09f90-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2WebMessageReceivedEventArgs class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="09f90-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="09f90-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="09f90-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="09f90-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="09f90-107">Аргументы события для события WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="09f90-107">Event args for the WebMessageReceived event.</span></span>

## <span data-ttu-id="09f90-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="09f90-108">Summary</span></span>

 <span data-ttu-id="09f90-109">Участников</span><span class="sxs-lookup"><span data-stu-id="09f90-109">Members</span></span>                        | <span data-ttu-id="09f90-110">Описания</span><span class="sxs-lookup"><span data-stu-id="09f90-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="09f90-111">Источник</span><span class="sxs-lookup"><span data-stu-id="09f90-111">Source</span></span>](#source) | <span data-ttu-id="09f90-112">Универсальный код ресурса (URI) документа, отправившего это веб-сообщение.</span><span class="sxs-lookup"><span data-stu-id="09f90-112">The URI of the document that sent this web message.</span></span>
[<span data-ttu-id="09f90-113">WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="09f90-113">WebMessageAsJson</span></span>](#webmessageasjson) | <span data-ttu-id="09f90-114">Сообщение, опубликованное из содержимого WebView на узел, преобразованное в строку JSON.</span><span class="sxs-lookup"><span data-stu-id="09f90-114">The message posted from the webview content to the host converted to a JSON string.</span></span>
[<span data-ttu-id="09f90-115">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="09f90-115">TryGetWebMessageAsString</span></span>](#trygetwebmessageasstring) | <span data-ttu-id="09f90-116">Если сообщение, опубликованное из содержимого WebView, содержит строковый тип, этот метод возвратит значение этой строки.</span><span class="sxs-lookup"><span data-stu-id="09f90-116">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

## <span data-ttu-id="09f90-117">Участников</span><span class="sxs-lookup"><span data-stu-id="09f90-117">Members</span></span>

#### <span data-ttu-id="09f90-118">Источник</span><span class="sxs-lookup"><span data-stu-id="09f90-118">Source</span></span> 

<span data-ttu-id="09f90-119">Универсальный код ресурса (URI) документа, отправившего это веб-сообщение.</span><span class="sxs-lookup"><span data-stu-id="09f90-119">The URI of the document that sent this web message.</span></span>

> <span data-ttu-id="09f90-120">[источник](#source) общедоступной строки</span><span class="sxs-lookup"><span data-stu-id="09f90-120">public string [Source](#source)</span></span>

#### <span data-ttu-id="09f90-121">WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="09f90-121">WebMessageAsJson</span></span> 

<span data-ttu-id="09f90-122">Сообщение, опубликованное из содержимого WebView на узел, преобразованное в строку JSON.</span><span class="sxs-lookup"><span data-stu-id="09f90-122">The message posted from the webview content to the host converted to a JSON string.</span></span>

> <span data-ttu-id="09f90-123">общедоступная строка [WebMessageAsJson](#webmessageasjson)</span><span class="sxs-lookup"><span data-stu-id="09f90-123">public string [WebMessageAsJson](#webmessageasjson)</span></span>

<span data-ttu-id="09f90-124">Используйте этот способ для обмена данными с помощью объектов JavaScript.</span><span class="sxs-lookup"><span data-stu-id="09f90-124">Use this to communicate via JavaScript objects.</span></span>

<span data-ttu-id="09f90-125">Например, следующие вызовы в сообщении WebMessageAsJson приводят к следующим значениям:</span><span class="sxs-lookup"><span data-stu-id="09f90-125">For example the following postMessage calls result in the following WebMessageAsJson values:</span></span>

```
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### <span data-ttu-id="09f90-126">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="09f90-126">TryGetWebMessageAsString</span></span> 

<span data-ttu-id="09f90-127">Если сообщение, опубликованное из содержимого WebView, содержит строковый тип, этот метод возвратит значение этой строки.</span><span class="sxs-lookup"><span data-stu-id="09f90-127">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

> <span data-ttu-id="09f90-128">public string [TryGetWebMessageAsString](#trygetwebmessageasstring)()</span><span class="sxs-lookup"><span data-stu-id="09f90-128">public string [TryGetWebMessageAsString](#trygetwebmessageasstring)()</span></span>

<span data-ttu-id="09f90-129">Если сообщение Опубликовано в другом типе JavaScript, этот метод завершается сбоем с E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="09f90-129">If the message posted is some other kind of JavaScript type this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="09f90-130">Используйте этот способ для обмена сообщениями через простые строки.</span><span class="sxs-lookup"><span data-stu-id="09f90-130">Use this to communicate via simple strings.</span></span>

<span data-ttu-id="09f90-131">Например, следующие вызовы в сообщении WebMessageAsString приводят к следующим значениям:</span><span class="sxs-lookup"><span data-stu-id="09f90-131">For example the following postMessage calls result in the following WebMessageAsString values:</span></span>

```
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```

