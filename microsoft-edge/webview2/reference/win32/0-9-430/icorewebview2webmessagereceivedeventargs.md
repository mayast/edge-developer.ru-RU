---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2WebMessageReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: c619c066151941f1177d55c973569c89f03daa2e
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880166"
---
# <span data-ttu-id="c0c7b-104">0.9.430-Interface ICoreWebView2WebMessageReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="c0c7b-104">0.9.430 - interface ICoreWebView2WebMessageReceivedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="c0c7b-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="c0c7b-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="c0c7b-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="c0c7b-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebMessageReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="c0c7b-107">Аргументы события для события WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="c0c7b-107">Event args for the WebMessageReceived event.</span></span>

## <span data-ttu-id="c0c7b-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="c0c7b-108">Summary</span></span>

 <span data-ttu-id="c0c7b-109">Участников</span><span class="sxs-lookup"><span data-stu-id="c0c7b-109">Members</span></span>                        | <span data-ttu-id="c0c7b-110">Описания</span><span class="sxs-lookup"><span data-stu-id="c0c7b-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c0c7b-111">get_Source</span><span class="sxs-lookup"><span data-stu-id="c0c7b-111">get_Source</span></span>](#get_source) | <span data-ttu-id="c0c7b-112">Универсальный код ресурса (URI) документа, отправившего это веб-сообщение.</span><span class="sxs-lookup"><span data-stu-id="c0c7b-112">The URI of the document that sent this web message.</span></span>
[<span data-ttu-id="c0c7b-113">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="c0c7b-113">get_WebMessageAsJson</span></span>](#get_webmessageasjson) | <span data-ttu-id="c0c7b-114">Сообщение, опубликованное из содержимого WebView на узел, преобразованное в строку JSON.</span><span class="sxs-lookup"><span data-stu-id="c0c7b-114">The message posted from the webview content to the host converted to a JSON string.</span></span>
[<span data-ttu-id="c0c7b-115">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="c0c7b-115">TryGetWebMessageAsString</span></span>](#trygetwebmessageasstring) | <span data-ttu-id="c0c7b-116">Если сообщение, опубликованное из содержимого WebView, содержит строковый тип, этот метод возвратит значение этой строки.</span><span class="sxs-lookup"><span data-stu-id="c0c7b-116">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

## <span data-ttu-id="c0c7b-117">Участников</span><span class="sxs-lookup"><span data-stu-id="c0c7b-117">Members</span></span>

#### <span data-ttu-id="c0c7b-118">get_Source</span><span class="sxs-lookup"><span data-stu-id="c0c7b-118">get_Source</span></span> 

<span data-ttu-id="c0c7b-119">Универсальный код ресурса (URI) документа, отправившего это веб-сообщение.</span><span class="sxs-lookup"><span data-stu-id="c0c7b-119">The URI of the document that sent this web message.</span></span>

> <span data-ttu-id="c0c7b-120">общедоступные значения HRESULT [get_Source](#get_source)(LPWSTR \* Source)</span><span class="sxs-lookup"><span data-stu-id="c0c7b-120">public HRESULT [get_Source](#get_source)(LPWSTR \* source)</span></span>

#### <span data-ttu-id="c0c7b-121">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="c0c7b-121">get_WebMessageAsJson</span></span> 

<span data-ttu-id="c0c7b-122">Сообщение, опубликованное из содержимого WebView на узел, преобразованное в строку JSON.</span><span class="sxs-lookup"><span data-stu-id="c0c7b-122">The message posted from the webview content to the host converted to a JSON string.</span></span>

> <span data-ttu-id="c0c7b-123">общедоступные значения HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR \* WebMessageAsJson)</span><span class="sxs-lookup"><span data-stu-id="c0c7b-123">public HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR \* webMessageAsJson)</span></span>

<span data-ttu-id="c0c7b-124">Используйте этот способ для обмена данными с помощью объектов JavaScript.</span><span class="sxs-lookup"><span data-stu-id="c0c7b-124">Use this to communicate via JavaScript objects.</span></span>

<span data-ttu-id="c0c7b-125">Например, следующие вызовы в сообщении WebMessageAsJson приводят к следующим значениям:</span><span class="sxs-lookup"><span data-stu-id="c0c7b-125">For example the following postMessage calls result in the following WebMessageAsJson values:</span></span>

```cpp
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### <span data-ttu-id="c0c7b-126">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="c0c7b-126">TryGetWebMessageAsString</span></span> 

<span data-ttu-id="c0c7b-127">Если сообщение, опубликованное из содержимого WebView, содержит строковый тип, этот метод возвратит значение этой строки.</span><span class="sxs-lookup"><span data-stu-id="c0c7b-127">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

> <span data-ttu-id="c0c7b-128">общедоступные значения HRESULT [TryGetWebMessageAsString](#trygetwebmessageasstring)(LPWSTR \* webMessageAsString)</span><span class="sxs-lookup"><span data-stu-id="c0c7b-128">public HRESULT [TryGetWebMessageAsString](#trygetwebmessageasstring)(LPWSTR \* webMessageAsString)</span></span>

<span data-ttu-id="c0c7b-129">Если сообщение Опубликовано в другом типе JavaScript, этот метод завершается сбоем с E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="c0c7b-129">If the message posted is some other kind of JavaScript type this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="c0c7b-130">Используйте этот способ для обмена сообщениями через простые строки.</span><span class="sxs-lookup"><span data-stu-id="c0c7b-130">Use this to communicate via simple strings.</span></span>

<span data-ttu-id="c0c7b-131">Например, следующие вызовы в сообщении WebMessageAsString приводят к следующим значениям:</span><span class="sxs-lookup"><span data-stu-id="c0c7b-131">For example the following postMessage calls result in the following WebMessageAsString values:</span></span>

```cpp
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```

