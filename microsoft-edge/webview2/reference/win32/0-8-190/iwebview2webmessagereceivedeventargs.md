---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2WebMessageReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: d70162803cfb2f9d1f0cfbf7e7397ee1cdbeec0e
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878192"
---
# <span data-ttu-id="1b6c1-104">0.8.355-Interface IWebView2WebMessageReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="1b6c1-104">0.8.355 - interface IWebView2WebMessageReceivedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="1b6c1-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="1b6c1-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="1b6c1-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="1b6c1-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebMessageReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="1b6c1-107">Аргументы события для события WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="1b6c1-107">Event args for the WebMessageReceived event.</span></span>

## <span data-ttu-id="1b6c1-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="1b6c1-108">Summary</span></span>

 <span data-ttu-id="1b6c1-109">Участников</span><span class="sxs-lookup"><span data-stu-id="1b6c1-109">Members</span></span>                        | <span data-ttu-id="1b6c1-110">Описания</span><span class="sxs-lookup"><span data-stu-id="1b6c1-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1b6c1-111">get_Source</span><span class="sxs-lookup"><span data-stu-id="1b6c1-111">get_Source</span></span>](#get_source) | <span data-ttu-id="1b6c1-112">Универсальный код ресурса (URI) документа, отправившего это веб-сообщение.</span><span class="sxs-lookup"><span data-stu-id="1b6c1-112">The URI of the document that sent this web message.</span></span>
[<span data-ttu-id="1b6c1-113">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="1b6c1-113">get_WebMessageAsJson</span></span>](#get_webmessageasjson) | <span data-ttu-id="1b6c1-114">Сообщение, опубликованное из содержимого WebView на узел, преобразованное в строку JSON.</span><span class="sxs-lookup"><span data-stu-id="1b6c1-114">The message posted from the webview content to the host converted to a JSON string.</span></span>
[<span data-ttu-id="1b6c1-115">get_WebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="1b6c1-115">get_WebMessageAsString</span></span>](#get_webmessageasstring) | <span data-ttu-id="1b6c1-116">Если сообщение, опубликованное из содержимого WebView, содержит строковый тип, этот метод возвратит значение этой строки.</span><span class="sxs-lookup"><span data-stu-id="1b6c1-116">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

## <span data-ttu-id="1b6c1-117">Участников</span><span class="sxs-lookup"><span data-stu-id="1b6c1-117">Members</span></span>

#### <span data-ttu-id="1b6c1-118">get_Source</span><span class="sxs-lookup"><span data-stu-id="1b6c1-118">get_Source</span></span> 

<span data-ttu-id="1b6c1-119">Универсальный код ресурса (URI) документа, отправившего это веб-сообщение.</span><span class="sxs-lookup"><span data-stu-id="1b6c1-119">The URI of the document that sent this web message.</span></span>

> <span data-ttu-id="1b6c1-120">общедоступные значения HRESULT [get_Source](#get_source)(LPWSTR \* Source)</span><span class="sxs-lookup"><span data-stu-id="1b6c1-120">public HRESULT [get_Source](#get_source)(LPWSTR \* source)</span></span>

#### <span data-ttu-id="1b6c1-121">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="1b6c1-121">get_WebMessageAsJson</span></span> 

<span data-ttu-id="1b6c1-122">Сообщение, опубликованное из содержимого WebView на узел, преобразованное в строку JSON.</span><span class="sxs-lookup"><span data-stu-id="1b6c1-122">The message posted from the webview content to the host converted to a JSON string.</span></span>

> <span data-ttu-id="1b6c1-123">общедоступные значения HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR \* WebMessageAsJson)</span><span class="sxs-lookup"><span data-stu-id="1b6c1-123">public HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR \* webMessageAsJson)</span></span>

<span data-ttu-id="1b6c1-124">Используйте этот способ для обмена данными с помощью объектов JavaScript.</span><span class="sxs-lookup"><span data-stu-id="1b6c1-124">Use this to communicate via JavaScript objects.</span></span>

<span data-ttu-id="1b6c1-125">Например, следующие вызовы в сообщении WebMessageAsJson приводят к следующим значениям:</span><span class="sxs-lookup"><span data-stu-id="1b6c1-125">For example the following postMessage calls result in the following WebMessageAsJson values:</span></span>

```cpp
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### <span data-ttu-id="1b6c1-126">get_WebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="1b6c1-126">get_WebMessageAsString</span></span> 

<span data-ttu-id="1b6c1-127">Если сообщение, опубликованное из содержимого WebView, содержит строковый тип, этот метод возвратит значение этой строки.</span><span class="sxs-lookup"><span data-stu-id="1b6c1-127">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

> <span data-ttu-id="1b6c1-128">общедоступные значения HRESULT [get_WebMessageAsString](#get_webmessageasstring)(LPWSTR \* WebMessageAsString)</span><span class="sxs-lookup"><span data-stu-id="1b6c1-128">public HRESULT [get_WebMessageAsString](#get_webmessageasstring)(LPWSTR \* webMessageAsString)</span></span>

<span data-ttu-id="1b6c1-129">Если сообщение Опубликовано в другом типе JavaScript, этот метод завершается сбоем с E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="1b6c1-129">If the message posted is some other kind of JavaScript type this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="1b6c1-130">Используйте этот способ для обмена сообщениями через простые строки.</span><span class="sxs-lookup"><span data-stu-id="1b6c1-130">Use this to communicate via simple strings.</span></span>

<span data-ttu-id="1b6c1-131">Например, следующие вызовы в сообщении WebMessageAsString приводят к следующим значениям:</span><span class="sxs-lookup"><span data-stu-id="1b6c1-131">For example the following postMessage calls result in the following WebMessageAsString values:</span></span>

```cpp
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```

