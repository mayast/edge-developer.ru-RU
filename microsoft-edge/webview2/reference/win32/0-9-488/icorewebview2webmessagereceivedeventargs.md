---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/28/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 6e0c20f8763e8895c4b5ebdcdfe9ea7d70aca2b8
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698129"
---
# <span data-ttu-id="28464-104">интерфейс ICoreWebView2WebMessageReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="28464-104">interface ICoreWebView2WebMessageReceivedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="28464-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="28464-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="28464-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="28464-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WebMessageReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="28464-107">Аргументы события для события WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="28464-107">Event args for the WebMessageReceived event.</span></span>

## <span data-ttu-id="28464-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="28464-108">Summary</span></span>

 <span data-ttu-id="28464-109">Участников</span><span class="sxs-lookup"><span data-stu-id="28464-109">Members</span></span>                        | <span data-ttu-id="28464-110">Описания</span><span class="sxs-lookup"><span data-stu-id="28464-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="28464-111">get_Source</span><span class="sxs-lookup"><span data-stu-id="28464-111">get_Source</span></span>](#get_source) | <span data-ttu-id="28464-112">Универсальный код ресурса (URI) документа, отправившего это веб-сообщение.</span><span class="sxs-lookup"><span data-stu-id="28464-112">The URI of the document that sent this web message.</span></span>
[<span data-ttu-id="28464-113">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="28464-113">get_WebMessageAsJson</span></span>](#get_webmessageasjson) | <span data-ttu-id="28464-114">Сообщение, опубликованное из содержимого WebView на узел, преобразованное в строку JSON.</span><span class="sxs-lookup"><span data-stu-id="28464-114">The message posted from the webview content to the host converted to a JSON string.</span></span>
[<span data-ttu-id="28464-115">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="28464-115">TryGetWebMessageAsString</span></span>](#trygetwebmessageasstring) | <span data-ttu-id="28464-116">Если сообщение, опубликованное из содержимого WebView, содержит строковый тип, этот метод возвратит значение этой строки.</span><span class="sxs-lookup"><span data-stu-id="28464-116">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

## <span data-ttu-id="28464-117">Участников</span><span class="sxs-lookup"><span data-stu-id="28464-117">Members</span></span>

#### <span data-ttu-id="28464-118">get_Source</span><span class="sxs-lookup"><span data-stu-id="28464-118">get_Source</span></span> 

<span data-ttu-id="28464-119">Универсальный код ресурса (URI) документа, отправившего это веб-сообщение.</span><span class="sxs-lookup"><span data-stu-id="28464-119">The URI of the document that sent this web message.</span></span>

> <span data-ttu-id="28464-120">общедоступные значения HRESULT [get_Source](#get_source)(LPWSTR \* Source)</span><span class="sxs-lookup"><span data-stu-id="28464-120">public HRESULT [get_Source](#get_source)(LPWSTR \* source)</span></span>

#### <span data-ttu-id="28464-121">get_WebMessageAsJson</span><span class="sxs-lookup"><span data-stu-id="28464-121">get_WebMessageAsJson</span></span> 

<span data-ttu-id="28464-122">Сообщение, опубликованное из содержимого WebView на узел, преобразованное в строку JSON.</span><span class="sxs-lookup"><span data-stu-id="28464-122">The message posted from the webview content to the host converted to a JSON string.</span></span>

> <span data-ttu-id="28464-123">общедоступные значения HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR \* WebMessageAsJson)</span><span class="sxs-lookup"><span data-stu-id="28464-123">public HRESULT [get_WebMessageAsJson](#get_webmessageasjson)(LPWSTR \* webMessageAsJson)</span></span>

<span data-ttu-id="28464-124">Используйте этот способ для обмена данными с помощью объектов JavaScript.</span><span class="sxs-lookup"><span data-stu-id="28464-124">Use this to communicate via JavaScript objects.</span></span>

<span data-ttu-id="28464-125">Например, следующие вызовы в сообщении WebMessageAsJson приводят к следующим значениям:</span><span class="sxs-lookup"><span data-stu-id="28464-125">For example the following postMessage calls result in the following WebMessageAsJson values:</span></span>

```
postMessage({'a': 'b'})      L"{\"a\": \"b\"}"
postMessage(1.2)             L"1.2"
postMessage('example')       L"\"example\""
```

#### <span data-ttu-id="28464-126">TryGetWebMessageAsString</span><span class="sxs-lookup"><span data-stu-id="28464-126">TryGetWebMessageAsString</span></span> 

<span data-ttu-id="28464-127">Если сообщение, опубликованное из содержимого WebView, содержит строковый тип, этот метод возвратит значение этой строки.</span><span class="sxs-lookup"><span data-stu-id="28464-127">If the message posted from the webview content to the host is a string type, this method will return the value of that string.</span></span>

> <span data-ttu-id="28464-128">общедоступные значения HRESULT [TryGetWebMessageAsString](#trygetwebmessageasstring)(LPWSTR \* webMessageAsString)</span><span class="sxs-lookup"><span data-stu-id="28464-128">public HRESULT [TryGetWebMessageAsString](#trygetwebmessageasstring)(LPWSTR \* webMessageAsString)</span></span>

<span data-ttu-id="28464-129">Если сообщение Опубликовано в другом типе JavaScript, этот метод завершается сбоем с E_INVALIDARG.</span><span class="sxs-lookup"><span data-stu-id="28464-129">If the message posted is some other kind of JavaScript type this method will fail with E_INVALIDARG.</span></span> <span data-ttu-id="28464-130">Используйте этот способ для обмена сообщениями через простые строки.</span><span class="sxs-lookup"><span data-stu-id="28464-130">Use this to communicate via simple strings.</span></span>

<span data-ttu-id="28464-131">Например, следующие вызовы в сообщении WebMessageAsString приводят к следующим значениям:</span><span class="sxs-lookup"><span data-stu-id="28464-131">For example the following postMessage calls result in the following WebMessageAsString values:</span></span>

```
postMessage({'a': 'b'})      E_INVALIDARG
postMessage(1.2)             E_INVALIDARG
postMessage('example')       L"example"
```

