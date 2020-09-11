---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2WebMessageReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2WebMessageReceivedEventArgs
ms.openlocfilehash: 58bb4b7f34b2917ec16ead051d1df8d6e6885f6d
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010385"
---
# <span data-ttu-id="5e740-104">0.9.579-Interface ICoreWebView2WebMessageReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="5e740-104">0.9.579 - interface ICoreWebView2WebMessageReceivedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2WebMessageReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="5e740-105">Аргументы события для события WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="5e740-105">Event args for the WebMessageReceived event.</span></span>

## <span data-ttu-id="5e740-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="5e740-106">Summary</span></span>

 <span data-ttu-id="5e740-107">Участников</span><span class="sxs-lookup"><span data-stu-id="5e740-107">Members</span></span>                        | <span data-ttu-id="5e740-108">Описания</span><span class="sxs-lookup"><span data-stu-id="5e740-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5e740-109">get_Source</span><span class="sxs-lookup"><span data-stu-id="5e740-109">get_Source</span></span>](#get_source) | <span data-ttu-id="5e740-110">Универсальный код ресурса (URI) документа, отправившего это веб-сообщение.</span><span class="sxs-lookup"><span data-stu-id="5e740-110">The URI of the document that sent this web message.</span></span>
[<span data-ttu-id="5e740-111">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="5e740-111">get_WebMessageAsJson</span></span>](#get_webmessageasjson) | <span data-ttu-id="5e740-112">Сообщение, опубликованное из содержимого WebView на узел, преобразованное в строку JSON.</span><span class="sxs-lookup"><span data-stu-id="5e740-112">The message posted from the webview content to the host converted to a JSON string.</span></span>
[<span data-ttu-id="5e740-113">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="5e740-113">TryGetWebMessageAsString</span></span>](#trygetwebmessageasstring) | <span data-ttu-id="5e740-114">Если сообщение, опубликованное из содержимого WebView, содержит строковый тип, этот метод возвратит значение этой строки.</span><span class="sxs-lookup"><span data-stu-id="5e740-114">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

## <span data-ttu-id="5e740-115">Участников</span><span class="sxs-lookup"><span data-stu-id="5e740-115">Members</span></span>

#### <span data-ttu-id="5e740-116">get_Source</span><span class="sxs-lookup"><span data-stu-id="5e740-116">get_Source</span></span> 

<span data-ttu-id="5e740-117">Универсальный код ресурса (URI) документа, отправившего это веб-сообщение.</span><span class="sxs-lookup"><span data-stu-id="5e740-117">The URI of the document that sent this web message.</span></span>

> <span data-ttu-id="5e740-118">общедоступные значения HRESULT [get_Source](#get_source)(LPWSTR \* Source)</span><span class="sxs-lookup"><span data-stu-id="5e740-118">public HRESULT [get_Source](#get_source)(LPWSTR \* source)</span></span>

#### <span data-ttu-id="5e740-119">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="5e740-119">get_WebMessageAsJson</span></span> 

<span data-ttu-id="5e740-120">Сообщение, опубликованное из содержимого WebView на узел, преобразованное в строку JSON.</span><span class="sxs-lookup"><span data-stu-id="5e740-120">The message posted from the webview content to the host converted to a JSON string.</span></span>

> <span data-ttu-id="5e740-121">общедоступные значения HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR \* WebMessageAsJson)</span><span class="sxs-lookup"><span data-stu-id="5e740-121">public HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR \* webMessageAsJson)</span></span>

<span data-ttu-id="5e740-122">Используйте этот способ для обмена данными с помощью объектов JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5e740-122">Use this to communicate via JavaScript objects.</span></span>

<span data-ttu-id="5e740-123">Например, следующие вызовы в сообщении WebMessageAsJson приводят к следующим значениям:</span><span class="sxs-lookup"><span data-stu-id="5e740-123">For example the following postMessage calls result in the following WebMessageAsJson values:</span></span>

```
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### <span data-ttu-id="5e740-124">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="5e740-124">TryGetWebMessageAsString</span></span> 

<span data-ttu-id="5e740-125">Если сообщение, опубликованное из содержимого WebView, содержит строковый тип, этот метод возвратит значение этой строки.</span><span class="sxs-lookup"><span data-stu-id="5e740-125">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

> <span data-ttu-id="5e740-126">общедоступные значения HRESULT [TryGetWebMessageAsString](#trygetwebmessageasstring)(LPWSTR \* webMessageAsString)</span><span class="sxs-lookup"><span data-stu-id="5e740-126">public HRESULT [TryGetWebMessageAsString](#trygetwebmessageasstring)(LPWSTR \* webMessageAsString)</span></span>

<span data-ttu-id="5e740-127">Если сообщение Опубликовано в другом типе JavaScript, этот метод завершается сбоем с E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="5e740-127">If the message posted is some other kind of JavaScript type this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="5e740-128">Используйте этот способ для обмена сообщениями через простые строки.</span><span class="sxs-lookup"><span data-stu-id="5e740-128">Use this to communicate via simple strings.</span></span>

<span data-ttu-id="5e740-129">Например, следующие вызовы в сообщении WebMessageAsString приводят к следующим значениям:</span><span class="sxs-lookup"><span data-stu-id="5e740-129">For example the following postMessage calls result in the following WebMessageAsString values:</span></span>

```
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```

