---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 5230e4b4c7529924a958779665dd304ec9e6dd45
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699225"
---
# <span data-ttu-id="06bbe-104">интерфейс ICoreWebView2HttpHeadersCollectionIterator</span><span class="sxs-lookup"><span data-stu-id="06bbe-104">interface ICoreWebView2HttpHeadersCollectionIterator</span></span> 

```
interface ICoreWebView2HttpHeadersCollectionIterator
  : public IUnknown
```

<span data-ttu-id="06bbe-105">Итератор для коллекции заголовков HTTP.</span><span class="sxs-lookup"><span data-stu-id="06bbe-105">Iterator for a collection of HTTP headers.</span></span>

## <span data-ttu-id="06bbe-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="06bbe-106">Summary</span></span>

 <span data-ttu-id="06bbe-107">Участников</span><span class="sxs-lookup"><span data-stu-id="06bbe-107">Members</span></span>                        | <span data-ttu-id="06bbe-108">Описания</span><span class="sxs-lookup"><span data-stu-id="06bbe-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="06bbe-109">get_HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="06bbe-109">get_HasCurrentHeader</span></span>](#get_hascurrentheader) | <span data-ttu-id="06bbe-110">Имеет значение true, если итератор не исходил из заголовков.</span><span class="sxs-lookup"><span data-stu-id="06bbe-110">True when the iterator hasn't run out of headers.</span></span>
[<span data-ttu-id="06bbe-111">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="06bbe-111">GetCurrentHeader</span></span>](#getcurrentheader) | <span data-ttu-id="06bbe-112">Получите имя и значение текущего HTTP-заголовка итератора.</span><span class="sxs-lookup"><span data-stu-id="06bbe-112">Get the name and value of the current HTTP header of the iterator.</span></span>
[<span data-ttu-id="06bbe-113">MoveNext</span><span class="sxs-lookup"><span data-stu-id="06bbe-113">MoveNext</span></span>](#movenext) | <span data-ttu-id="06bbe-114">Переместите итератор на следующий заголовок HTTP в коллекции.</span><span class="sxs-lookup"><span data-stu-id="06bbe-114">Move the iterator to the next HTTP header in the collection.</span></span>

<span data-ttu-id="06bbe-115">Смотрите [ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) и [ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md).</span><span class="sxs-lookup"><span data-stu-id="06bbe-115">See [ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) and [ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md).</span></span> 
```cpp
std::wstring RequestHeadersToJsonString(ICoreWebView2HttpRequestHeaders* requestHeaders)
{
    wil::com_ptr<ICoreWebView2HttpHeadersCollectionIterator> iterator;
    CHECK_FAILURE(requestHeaders->GetIterator(&iterator));
    BOOL hasCurrent = FALSE;
    std::wstring result = L"[";

    while (SUCCEEDED(iterator->get_HasCurrentHeader(&hasCurrent)) && hasCurrent)
    {
        wil::unique_cotaskmem_string name;
        wil::unique_cotaskmem_string value;

        CHECK_FAILURE(iterator->GetCurrentHeader(&name, &value));
        result += L"{\"name\": " + EncodeQuote(name.get())
            + L", \"value\": " + EncodeQuote(value.get()) + L"}";

        BOOL hasNext = FALSE;
        CHECK_FAILURE(iterator->MoveNext(&hasNext));
        if (hasNext)
        {
            result += L", ";
        }
    }

    return result + L"]";
}
```

## <span data-ttu-id="06bbe-116">Участников</span><span class="sxs-lookup"><span data-stu-id="06bbe-116">Members</span></span>

#### <span data-ttu-id="06bbe-117">get_HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="06bbe-117">get_HasCurrentHeader</span></span> 

<span data-ttu-id="06bbe-118">Имеет значение true, если итератор не исходил из заголовков.</span><span class="sxs-lookup"><span data-stu-id="06bbe-118">True when the iterator hasn't run out of headers.</span></span>

> <span data-ttu-id="06bbe-119">общедоступные значения HRESULT [get_HasCurrentHeader](#get_hascurrentheader)(bool \* hasCurrent)</span><span class="sxs-lookup"><span data-stu-id="06bbe-119">public HRESULT [get_HasCurrentHeader](#get_hascurrentheader)(BOOL \* hasCurrent)</span></span>

<span data-ttu-id="06bbe-120">Если коллекция, в которой находится итератор, является пустой или, если итератор пропало за ее пределами, это ложный.</span><span class="sxs-lookup"><span data-stu-id="06bbe-120">If the collection over which the iterator is iterating is empty or if the iterator has gone past the end of the collection then this is false.</span></span>

#### <span data-ttu-id="06bbe-121">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="06bbe-121">GetCurrentHeader</span></span> 

<span data-ttu-id="06bbe-122">Получите имя и значение текущего HTTP-заголовка итератора.</span><span class="sxs-lookup"><span data-stu-id="06bbe-122">Get the name and value of the current HTTP header of the iterator.</span></span>

> <span data-ttu-id="06bbe-123">Public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR \* имя, LPWSTR \* значение)</span><span class="sxs-lookup"><span data-stu-id="06bbe-123">public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR \* name, LPWSTR \* value)</span></span>

<span data-ttu-id="06bbe-124">Этот метод завершается сбоем, если последний вызов MoveNext задает has_next значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="06bbe-124">This method will fail if the last call to MoveNext set has_next to FALSE.</span></span>

#### <span data-ttu-id="06bbe-125">MoveNext</span><span class="sxs-lookup"><span data-stu-id="06bbe-125">MoveNext</span></span> 

<span data-ttu-id="06bbe-126">Переместите итератор на следующий заголовок HTTP в коллекции.</span><span class="sxs-lookup"><span data-stu-id="06bbe-126">Move the iterator to the next HTTP header in the collection.</span></span>

> <span data-ttu-id="06bbe-127">общедоступный HRESULT [MoveNext](#movenext)(bool \* hasNext)</span><span class="sxs-lookup"><span data-stu-id="06bbe-127">public HRESULT [MoveNext](#movenext)(BOOL \* hasNext)</span></span>

<span data-ttu-id="06bbe-128">При отсутствии заголовков HTTP для параметра hasNext будет задано значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="06bbe-128">The hasNext parameter will be set to FALSE if there are no more HTTP headers.</span></span> <span data-ttu-id="06bbe-129">После этого метод GetCurrentHeader завершается сбоем, если он вызывается.</span><span class="sxs-lookup"><span data-stu-id="06bbe-129">After this occurs the GetCurrentHeader method will fail if called.</span></span>

