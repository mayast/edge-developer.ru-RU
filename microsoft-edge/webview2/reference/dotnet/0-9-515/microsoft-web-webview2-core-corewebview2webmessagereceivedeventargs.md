---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2WebMessageReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: ff4ebd8dc3a1c78424d57f6c7b5e6f7fc8e99049
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879319"
---
# <span data-ttu-id="6656c-104">класс 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2WebMessageReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="6656c-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2WebMessageReceivedEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="6656c-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="6656c-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="6656c-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="6656c-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="6656c-107">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="6656c-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="6656c-108">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="6656c-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="6656c-109">Аргументы события для события WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="6656c-109">Event args for the WebMessageReceived event.</span></span>

## <span data-ttu-id="6656c-110">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="6656c-110">Summary</span></span>

 <span data-ttu-id="6656c-111">Участников</span><span class="sxs-lookup"><span data-stu-id="6656c-111">Members</span></span>                        | <span data-ttu-id="6656c-112">Описания</span><span class="sxs-lookup"><span data-stu-id="6656c-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="6656c-113">Источник</span><span class="sxs-lookup"><span data-stu-id="6656c-113">Source</span></span>](#source) | <span data-ttu-id="6656c-114">Универсальный код ресурса (URI) документа, отправившего это веб-сообщение.</span><span class="sxs-lookup"><span data-stu-id="6656c-114">The URI of the document that sent this web message.</span></span>
[<span data-ttu-id="6656c-115">WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="6656c-115">WebMessageAsJson</span></span>](#webmessageasjson) | <span data-ttu-id="6656c-116">Сообщение, опубликованное из содержимого WebView на узел, преобразованное в строку JSON.</span><span class="sxs-lookup"><span data-stu-id="6656c-116">The message posted from the webview content to the host converted to a JSON string.</span></span>
[<span data-ttu-id="6656c-117">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="6656c-117">TryGetWebMessageAsString</span></span>](#trygetwebmessageasstring) | <span data-ttu-id="6656c-118">Если сообщение, опубликованное из содержимого WebView, содержит строковый тип, этот метод возвратит значение этой строки.</span><span class="sxs-lookup"><span data-stu-id="6656c-118">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

## <span data-ttu-id="6656c-119">Участников</span><span class="sxs-lookup"><span data-stu-id="6656c-119">Members</span></span>

#### <span data-ttu-id="6656c-120">Источник</span><span class="sxs-lookup"><span data-stu-id="6656c-120">Source</span></span> 

<span data-ttu-id="6656c-121">Универсальный код ресурса (URI) документа, отправившего это веб-сообщение.</span><span class="sxs-lookup"><span data-stu-id="6656c-121">The URI of the document that sent this web message.</span></span>

> <span data-ttu-id="6656c-122">[источник](#source) общедоступной строки</span><span class="sxs-lookup"><span data-stu-id="6656c-122">public string [Source](#source)</span></span>

#### <span data-ttu-id="6656c-123">WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="6656c-123">WebMessageAsJson</span></span> 

<span data-ttu-id="6656c-124">Сообщение, опубликованное из содержимого WebView на узел, преобразованное в строку JSON.</span><span class="sxs-lookup"><span data-stu-id="6656c-124">The message posted from the webview content to the host converted to a JSON string.</span></span>

> <span data-ttu-id="6656c-125">общедоступная строка [WebMessageAsJson](#webmessageasjson)</span><span class="sxs-lookup"><span data-stu-id="6656c-125">public string [WebMessageAsJson](#webmessageasjson)</span></span>

<span data-ttu-id="6656c-126">Используйте этот способ для обмена данными с помощью объектов JavaScript.</span><span class="sxs-lookup"><span data-stu-id="6656c-126">Use this to communicate via JavaScript objects.</span></span>

<span data-ttu-id="6656c-127">Например, следующие вызовы в сообщении WebMessageAsJson приводят к следующим значениям:</span><span class="sxs-lookup"><span data-stu-id="6656c-127">For example the following postMessage calls result in the following WebMessageAsJson values:</span></span>

```
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### <span data-ttu-id="6656c-128">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="6656c-128">TryGetWebMessageAsString</span></span> 

<span data-ttu-id="6656c-129">Если сообщение, опубликованное из содержимого WebView, содержит строковый тип, этот метод возвратит значение этой строки.</span><span class="sxs-lookup"><span data-stu-id="6656c-129">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

> <span data-ttu-id="6656c-130">public string [TryGetWebMessageAsString](#trygetwebmessageasstring)()</span><span class="sxs-lookup"><span data-stu-id="6656c-130">public string [TryGetWebMessageAsString](#trygetwebmessageasstring)()</span></span>

<span data-ttu-id="6656c-131">Если сообщение Опубликовано в другом типе JavaScript, этот метод завершается сбоем с E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="6656c-131">If the message posted is some other kind of JavaScript type this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="6656c-132">Используйте этот способ для обмена сообщениями через простые строки.</span><span class="sxs-lookup"><span data-stu-id="6656c-132">Use this to communicate via simple strings.</span></span>

<span data-ttu-id="6656c-133">Например, следующие вызовы в сообщении WebMessageAsString приводят к следующим значениям:</span><span class="sxs-lookup"><span data-stu-id="6656c-133">For example the following postMessage calls result in the following WebMessageAsString values:</span></span>

```
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```

