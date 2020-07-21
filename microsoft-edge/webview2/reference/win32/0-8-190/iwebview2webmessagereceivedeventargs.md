---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2WebMessageReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 4dfe2296312ac3ff3e9c67667c660aafcea38211
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885760"
---
# <span data-ttu-id="82c34-104">0.8.355-Interface IWebView2WebMessageReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="82c34-104">0.8.355 - interface IWebView2WebMessageReceivedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebMessageReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="82c34-105">Аргументы события для события WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="82c34-105">Event args for the WebMessageReceived event.</span></span>

## <span data-ttu-id="82c34-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="82c34-106">Summary</span></span>

 <span data-ttu-id="82c34-107">Участников</span><span class="sxs-lookup"><span data-stu-id="82c34-107">Members</span></span>                        | <span data-ttu-id="82c34-108">Описания</span><span class="sxs-lookup"><span data-stu-id="82c34-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="82c34-109">get_Source</span><span class="sxs-lookup"><span data-stu-id="82c34-109">get_Source</span></span>](#get_source) | <span data-ttu-id="82c34-110">Универсальный код ресурса (URI) документа, отправившего это веб-сообщение.</span><span class="sxs-lookup"><span data-stu-id="82c34-110">The URI of the document that sent this web message.</span></span>
[<span data-ttu-id="82c34-111">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="82c34-111">get_WebMessageAsJson</span></span>](#get_webmessageasjson) | <span data-ttu-id="82c34-112">Сообщение, опубликованное из содержимого WebView на узел, преобразованное в строку JSON.</span><span class="sxs-lookup"><span data-stu-id="82c34-112">The message posted from the webview content to the host converted to a JSON string.</span></span>
[<span data-ttu-id="82c34-113">get_WebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="82c34-113">get_WebMessageAsString</span></span>](#get_webmessageasstring) | <span data-ttu-id="82c34-114">Если сообщение, опубликованное из содержимого WebView, содержит строковый тип, этот метод возвратит значение этой строки.</span><span class="sxs-lookup"><span data-stu-id="82c34-114">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

## <span data-ttu-id="82c34-115">Участников</span><span class="sxs-lookup"><span data-stu-id="82c34-115">Members</span></span>

#### <span data-ttu-id="82c34-116">get_Source</span><span class="sxs-lookup"><span data-stu-id="82c34-116">get_Source</span></span> 

<span data-ttu-id="82c34-117">Универсальный код ресурса (URI) документа, отправившего это веб-сообщение.</span><span class="sxs-lookup"><span data-stu-id="82c34-117">The URI of the document that sent this web message.</span></span>

> <span data-ttu-id="82c34-118">общедоступные значения HRESULT [get_Source](#get_source)(LPWSTR \* Source)</span><span class="sxs-lookup"><span data-stu-id="82c34-118">public HRESULT [get_Source](#get_source)(LPWSTR \* source)</span></span>

#### <span data-ttu-id="82c34-119">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="82c34-119">get_WebMessageAsJson</span></span> 

<span data-ttu-id="82c34-120">Сообщение, опубликованное из содержимого WebView на узел, преобразованное в строку JSON.</span><span class="sxs-lookup"><span data-stu-id="82c34-120">The message posted from the webview content to the host converted to a JSON string.</span></span>

> <span data-ttu-id="82c34-121">общедоступные значения HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR \* WebMessageAsJson)</span><span class="sxs-lookup"><span data-stu-id="82c34-121">public HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR \* webMessageAsJson)</span></span>

<span data-ttu-id="82c34-122">Используйте этот способ для обмена данными с помощью объектов JavaScript.</span><span class="sxs-lookup"><span data-stu-id="82c34-122">Use this to communicate via JavaScript objects.</span></span>

<span data-ttu-id="82c34-123">Например, следующие вызовы в сообщении WebMessageAsJson приводят к следующим значениям:</span><span class="sxs-lookup"><span data-stu-id="82c34-123">For example the following postMessage calls result in the following WebMessageAsJson values:</span></span>

```cpp
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### <span data-ttu-id="82c34-124">get_WebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="82c34-124">get_WebMessageAsString</span></span> 

<span data-ttu-id="82c34-125">Если сообщение, опубликованное из содержимого WebView, содержит строковый тип, этот метод возвратит значение этой строки.</span><span class="sxs-lookup"><span data-stu-id="82c34-125">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

> <span data-ttu-id="82c34-126">общедоступные значения HRESULT [get_WebMessageAsString](#get_webmessageasstring)(LPWSTR \* WebMessageAsString)</span><span class="sxs-lookup"><span data-stu-id="82c34-126">public HRESULT [get_WebMessageAsString](#get_webmessageasstring)(LPWSTR \* webMessageAsString)</span></span>

<span data-ttu-id="82c34-127">Если сообщение Опубликовано в другом типе JavaScript, этот метод завершается сбоем с E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="82c34-127">If the message posted is some other kind of JavaScript type this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="82c34-128">Используйте этот способ для обмена сообщениями через простые строки.</span><span class="sxs-lookup"><span data-stu-id="82c34-128">Use this to communicate via simple strings.</span></span>

<span data-ttu-id="82c34-129">Например, следующие вызовы в сообщении WebMessageAsString приводят к следующим значениям:</span><span class="sxs-lookup"><span data-stu-id="82c34-129">For example the following postMessage calls result in the following WebMessageAsString values:</span></span>

```cpp
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```

