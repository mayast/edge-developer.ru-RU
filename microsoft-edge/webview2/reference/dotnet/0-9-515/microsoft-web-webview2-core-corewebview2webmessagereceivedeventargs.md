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
ms.openlocfilehash: b917f309194316b26ee94aa94dc8289ef4430007
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697541"
---
# <span data-ttu-id="4c75b-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2WebMessageReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="4c75b-104">Microsoft.Web.WebView2.Core.CoreWebView2WebMessageReceivedEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="4c75b-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="4c75b-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="4c75b-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="4c75b-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="4c75b-107">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="4c75b-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="4c75b-108">Сборка: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="4c75b-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="4c75b-109">Аргументы события для события WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="4c75b-109">Event args for the WebMessageReceived event.</span></span>

## <span data-ttu-id="4c75b-110">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="4c75b-110">Summary</span></span>

 <span data-ttu-id="4c75b-111">Участников</span><span class="sxs-lookup"><span data-stu-id="4c75b-111">Members</span></span>                        | <span data-ttu-id="4c75b-112">Описания</span><span class="sxs-lookup"><span data-stu-id="4c75b-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4c75b-113">Источник</span><span class="sxs-lookup"><span data-stu-id="4c75b-113">Source</span></span>](#source) | <span data-ttu-id="4c75b-114">Универсальный код ресурса (URI) документа, отправившего это веб-сообщение.</span><span class="sxs-lookup"><span data-stu-id="4c75b-114">The URI of the document that sent this web message.</span></span>
[<span data-ttu-id="4c75b-115">WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="4c75b-115">WebMessageAsJson</span></span>](#webmessageasjson) | <span data-ttu-id="4c75b-116">Сообщение, опубликованное из содержимого WebView на узел, преобразованное в строку JSON.</span><span class="sxs-lookup"><span data-stu-id="4c75b-116">The message posted from the webview content to the host converted to a JSON string.</span></span>
[<span data-ttu-id="4c75b-117">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="4c75b-117">TryGetWebMessageAsString</span></span>](#trygetwebmessageasstring) | <span data-ttu-id="4c75b-118">Если сообщение, опубликованное из содержимого WebView, содержит строковый тип, этот метод возвратит значение этой строки.</span><span class="sxs-lookup"><span data-stu-id="4c75b-118">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

## <span data-ttu-id="4c75b-119">Участников</span><span class="sxs-lookup"><span data-stu-id="4c75b-119">Members</span></span>

#### <span data-ttu-id="4c75b-120">Источник</span><span class="sxs-lookup"><span data-stu-id="4c75b-120">Source</span></span> 

<span data-ttu-id="4c75b-121">Универсальный код ресурса (URI) документа, отправившего это веб-сообщение.</span><span class="sxs-lookup"><span data-stu-id="4c75b-121">The URI of the document that sent this web message.</span></span>

> <span data-ttu-id="4c75b-122">[источник](#source) общедоступной строки</span><span class="sxs-lookup"><span data-stu-id="4c75b-122">public string [Source](#source)</span></span>

#### <span data-ttu-id="4c75b-123">WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="4c75b-123">WebMessageAsJson</span></span> 

<span data-ttu-id="4c75b-124">Сообщение, опубликованное из содержимого WebView на узел, преобразованное в строку JSON.</span><span class="sxs-lookup"><span data-stu-id="4c75b-124">The message posted from the webview content to the host converted to a JSON string.</span></span>

> <span data-ttu-id="4c75b-125">общедоступная строка [WebMessageAsJson](#webmessageasjson)</span><span class="sxs-lookup"><span data-stu-id="4c75b-125">public string [WebMessageAsJson](#webmessageasjson)</span></span>

<span data-ttu-id="4c75b-126">Используйте этот способ для обмена данными с помощью объектов JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4c75b-126">Use this to communicate via JavaScript objects.</span></span>

<span data-ttu-id="4c75b-127">Например, следующие вызовы в сообщении WebMessageAsJson приводят к следующим значениям:</span><span class="sxs-lookup"><span data-stu-id="4c75b-127">For example the following postMessage calls result in the following WebMessageAsJson values:</span></span>

```
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### <span data-ttu-id="4c75b-128">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="4c75b-128">TryGetWebMessageAsString</span></span> 

<span data-ttu-id="4c75b-129">Если сообщение, опубликованное из содержимого WebView, содержит строковый тип, этот метод возвратит значение этой строки.</span><span class="sxs-lookup"><span data-stu-id="4c75b-129">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

> <span data-ttu-id="4c75b-130">public string [TryGetWebMessageAsString](#trygetwebmessageasstring)()</span><span class="sxs-lookup"><span data-stu-id="4c75b-130">public string [TryGetWebMessageAsString](#trygetwebmessageasstring)()</span></span>

<span data-ttu-id="4c75b-131">Если сообщение Опубликовано в другом типе JavaScript, этот метод завершается сбоем с E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="4c75b-131">If the message posted is some other kind of JavaScript type this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="4c75b-132">Используйте этот способ для обмена сообщениями через простые строки.</span><span class="sxs-lookup"><span data-stu-id="4c75b-132">Use this to communicate via simple strings.</span></span>

<span data-ttu-id="4c75b-133">Например, следующие вызовы в сообщении WebMessageAsString приводят к следующим значениям:</span><span class="sxs-lookup"><span data-stu-id="4c75b-133">For example the following postMessage calls result in the following WebMessageAsString values:</span></span>

```
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```

