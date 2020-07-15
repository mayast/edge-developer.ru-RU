---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2HttpHeadersCollectionIterator
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 7abc6119d893cd1e9432d255969549f07d7e3a00
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878465"
---
# <span data-ttu-id="0b038-104">0.8.355-Interface IWebView2HttpHeadersCollectionIterator</span><span class="sxs-lookup"><span data-stu-id="0b038-104">0.8.355 - interface IWebView2HttpHeadersCollectionIterator</span></span> 

> [!NOTE]
> <span data-ttu-id="0b038-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="0b038-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="0b038-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="0b038-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2HttpHeadersCollectionIterator
  : public IUnknown
```

<span data-ttu-id="0b038-107">Итератор для коллекции заголовков HTTP.</span><span class="sxs-lookup"><span data-stu-id="0b038-107">Iterator for a collection of HTTP headers.</span></span>

## <span data-ttu-id="0b038-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="0b038-108">Summary</span></span>

 <span data-ttu-id="0b038-109">Участников</span><span class="sxs-lookup"><span data-stu-id="0b038-109">Members</span></span>                        | <span data-ttu-id="0b038-110">Описания</span><span class="sxs-lookup"><span data-stu-id="0b038-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0b038-111">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="0b038-111">GetCurrentHeader</span></span>](#getcurrentheader) | <span data-ttu-id="0b038-112">Получите имя и значение текущего HTTP-заголовка итератора.</span><span class="sxs-lookup"><span data-stu-id="0b038-112">Get the name and value of the current HTTP header of the iterator.</span></span>
[<span data-ttu-id="0b038-113">MoveNext</span><span class="sxs-lookup"><span data-stu-id="0b038-113">MoveNext</span></span>](#movenext) | <span data-ttu-id="0b038-114">Переместите итератор на следующий заголовок HTTP в коллекции.</span><span class="sxs-lookup"><span data-stu-id="0b038-114">Move the iterator to the next HTTP header in the collection.</span></span>

<span data-ttu-id="0b038-115">Смотрите [IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) и [IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md).</span><span class="sxs-lookup"><span data-stu-id="0b038-115">See [IWebView2HttpRequestHeaders](IWebView2HttpRequestHeaders.md) and [IWebView2HttpResponseHeaders](IWebView2HttpResponseHeaders.md).</span></span>

## <span data-ttu-id="0b038-116">Участников</span><span class="sxs-lookup"><span data-stu-id="0b038-116">Members</span></span>

#### <span data-ttu-id="0b038-117">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="0b038-117">GetCurrentHeader</span></span> 

<span data-ttu-id="0b038-118">Получите имя и значение текущего HTTP-заголовка итератора.</span><span class="sxs-lookup"><span data-stu-id="0b038-118">Get the name and value of the current HTTP header of the iterator.</span></span>

> <span data-ttu-id="0b038-119">Public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR \* имя, LPWSTR \* значение)</span><span class="sxs-lookup"><span data-stu-id="0b038-119">public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR \* name,LPWSTR \* value)</span></span>

<span data-ttu-id="0b038-120">Этот метод завершается сбоем, если последний вызов MoveNext задает has_next значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="0b038-120">This method will fail if the last call to MoveNext set has_next to FALSE.</span></span>

#### <span data-ttu-id="0b038-121">MoveNext</span><span class="sxs-lookup"><span data-stu-id="0b038-121">MoveNext</span></span> 

<span data-ttu-id="0b038-122">Переместите итератор на следующий заголовок HTTP в коллекции.</span><span class="sxs-lookup"><span data-stu-id="0b038-122">Move the iterator to the next HTTP header in the collection.</span></span>

> <span data-ttu-id="0b038-123">общедоступный HRESULT [MoveNext](#movenext)(BOOL \* has_next)</span><span class="sxs-lookup"><span data-stu-id="0b038-123">public HRESULT [MoveNext](#movenext)(BOOL \* has_next)</span></span>

<span data-ttu-id="0b038-124">Для параметра has_next будет задано значение FALSE, если больше нет заголовков HTTP.</span><span class="sxs-lookup"><span data-stu-id="0b038-124">The has_next parameter will be set to FALSE if there are no more HTTP headers.</span></span> <span data-ttu-id="0b038-125">После этого метод GetCurrentHeader завершается сбоем, если он вызывается.</span><span class="sxs-lookup"><span data-stu-id="0b038-125">After this occurs the GetCurrentHeader method will fail if called.</span></span>

