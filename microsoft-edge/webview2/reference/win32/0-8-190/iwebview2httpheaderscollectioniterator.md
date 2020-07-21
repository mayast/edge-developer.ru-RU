---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2HttpHeadersCollectionIterator
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: dbcc5b10ce1973df61554f3f27174f600fb25280
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885983"
---
# <span data-ttu-id="62ad8-104">0.8.355-Interface IWebView2HttpHeadersCollectionIterator</span><span class="sxs-lookup"><span data-stu-id="62ad8-104">0.8.355 - interface IWebView2HttpHeadersCollectionIterator</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2HttpHeadersCollectionIterator
  : public IUnknown
```

<span data-ttu-id="62ad8-105">Итератор для коллекции заголовков HTTP.</span><span class="sxs-lookup"><span data-stu-id="62ad8-105">Iterator for a collection of HTTP headers.</span></span>

## <span data-ttu-id="62ad8-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="62ad8-106">Summary</span></span>

 <span data-ttu-id="62ad8-107">Участников</span><span class="sxs-lookup"><span data-stu-id="62ad8-107">Members</span></span>                        | <span data-ttu-id="62ad8-108">Описания</span><span class="sxs-lookup"><span data-stu-id="62ad8-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="62ad8-109">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="62ad8-109">GetCurrentHeader</span></span>](#getcurrentheader) | <span data-ttu-id="62ad8-110">Получите имя и значение текущего HTTP-заголовка итератора.</span><span class="sxs-lookup"><span data-stu-id="62ad8-110">Get the name and value of the current HTTP header of the iterator.</span></span>
[<span data-ttu-id="62ad8-111">MoveNext</span><span class="sxs-lookup"><span data-stu-id="62ad8-111">MoveNext</span></span>](#movenext) | <span data-ttu-id="62ad8-112">Переместите итератор на следующий заголовок HTTP в коллекции.</span><span class="sxs-lookup"><span data-stu-id="62ad8-112">Move the iterator to the next HTTP header in the collection.</span></span>

<span data-ttu-id="62ad8-113">Смотрите [IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) и [IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md).</span><span class="sxs-lookup"><span data-stu-id="62ad8-113">See [IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) and [IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md).</span></span>

## <span data-ttu-id="62ad8-114">Участников</span><span class="sxs-lookup"><span data-stu-id="62ad8-114">Members</span></span>

#### <span data-ttu-id="62ad8-115">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="62ad8-115">GetCurrentHeader</span></span> 

<span data-ttu-id="62ad8-116">Получите имя и значение текущего HTTP-заголовка итератора.</span><span class="sxs-lookup"><span data-stu-id="62ad8-116">Get the name and value of the current HTTP header of the iterator.</span></span>

> <span data-ttu-id="62ad8-117">Public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR \* имя, LPWSTR \* значение)</span><span class="sxs-lookup"><span data-stu-id="62ad8-117">public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR \* name,LPWSTR \* value)</span></span>

<span data-ttu-id="62ad8-118">Этот метод завершается сбоем, если последний вызов MoveNext задает has_next значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="62ad8-118">This method will fail if the last call to MoveNext set has_next to FALSE.</span></span>

#### <span data-ttu-id="62ad8-119">MoveNext</span><span class="sxs-lookup"><span data-stu-id="62ad8-119">MoveNext</span></span> 

<span data-ttu-id="62ad8-120">Переместите итератор на следующий заголовок HTTP в коллекции.</span><span class="sxs-lookup"><span data-stu-id="62ad8-120">Move the iterator to the next HTTP header in the collection.</span></span>

> <span data-ttu-id="62ad8-121">общедоступный HRESULT [MoveNext](#movenext)(BOOL \* has_next)</span><span class="sxs-lookup"><span data-stu-id="62ad8-121">public HRESULT [MoveNext](#movenext)(BOOL \* has_next)</span></span>

<span data-ttu-id="62ad8-122">Для параметра has_next будет задано значение FALSE, если больше нет заголовков HTTP.</span><span class="sxs-lookup"><span data-stu-id="62ad8-122">The has_next parameter will be set to FALSE if there are no more HTTP headers.</span></span> <span data-ttu-id="62ad8-123">После этого метод GetCurrentHeader завершается сбоем, если он вызывается.</span><span class="sxs-lookup"><span data-stu-id="62ad8-123">After this occurs the GetCurrentHeader method will fail if called.</span></span>

