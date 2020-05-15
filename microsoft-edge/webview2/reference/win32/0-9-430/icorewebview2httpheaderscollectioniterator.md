---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 9e94291c55680e03c48a5fbf1b48f9d79a790cb6
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654774"
---
# <span data-ttu-id="23268-104">интерфейс ICoreWebView2HttpHeadersCollectionIterator</span><span class="sxs-lookup"><span data-stu-id="23268-104">interface ICoreWebView2HttpHeadersCollectionIterator</span></span> 

> [!NOTE]
> <span data-ttu-id="23268-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="23268-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="23268-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="23268-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HttpHeadersCollectionIterator
  : public IUnknown
```

<span data-ttu-id="23268-107">Итератор для коллекции заголовков HTTP.</span><span class="sxs-lookup"><span data-stu-id="23268-107">Iterator for a collection of HTTP headers.</span></span>

## <span data-ttu-id="23268-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="23268-108">Summary</span></span>

 <span data-ttu-id="23268-109">Участников</span><span class="sxs-lookup"><span data-stu-id="23268-109">Members</span></span>                        | <span data-ttu-id="23268-110">Описания</span><span class="sxs-lookup"><span data-stu-id="23268-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="23268-111">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="23268-111">GetCurrentHeader</span></span>](#getcurrentheader) | <span data-ttu-id="23268-112">Получите имя и значение текущего HTTP-заголовка итератора.</span><span class="sxs-lookup"><span data-stu-id="23268-112">Get the name and value of the current HTTP header of the iterator.</span></span>
[<span data-ttu-id="23268-113">get_HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="23268-113">get_HasCurrentHeader</span></span>](#get_hascurrentheader) | <span data-ttu-id="23268-114">Имеет значение true, если итератор не исходил из заголовков.</span><span class="sxs-lookup"><span data-stu-id="23268-114">True when the iterator hasn't run out of headers.</span></span>
[<span data-ttu-id="23268-115">MoveNext</span><span class="sxs-lookup"><span data-stu-id="23268-115">MoveNext</span></span>](#movenext) | <span data-ttu-id="23268-116">Переместите итератор на следующий заголовок HTTP в коллекции.</span><span class="sxs-lookup"><span data-stu-id="23268-116">Move the iterator to the next HTTP header in the collection.</span></span>

<span data-ttu-id="23268-117">Смотрите [ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) и [ICoreWebView2HttpResponseHeaders](ICoreWebView2HttpResponseHeaders.md).</span><span class="sxs-lookup"><span data-stu-id="23268-117">See [ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) and [ICoreWebView2HttpResponseHeaders](ICoreWebView2HttpResponseHeaders.md).</span></span> 

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

## <span data-ttu-id="23268-118">Участников</span><span class="sxs-lookup"><span data-stu-id="23268-118">Members</span></span>

#### <span data-ttu-id="23268-119">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="23268-119">GetCurrentHeader</span></span> 

<span data-ttu-id="23268-120">Получите имя и значение текущего HTTP-заголовка итератора.</span><span class="sxs-lookup"><span data-stu-id="23268-120">Get the name and value of the current HTTP header of the iterator.</span></span>

> <span data-ttu-id="23268-121">Public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR \* имя, LPWSTR \* значение)</span><span class="sxs-lookup"><span data-stu-id="23268-121">public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR \* name,LPWSTR \* value)</span></span>

<span data-ttu-id="23268-122">Этот метод завершается сбоем, если последний вызов MoveNext задает has_next значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="23268-122">This method will fail if the last call to MoveNext set has_next to FALSE.</span></span>

#### <span data-ttu-id="23268-123">get_HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="23268-123">get_HasCurrentHeader</span></span> 

<span data-ttu-id="23268-124">Имеет значение true, если итератор не исходил из заголовков.</span><span class="sxs-lookup"><span data-stu-id="23268-124">True when the iterator hasn't run out of headers.</span></span>

> <span data-ttu-id="23268-125">общедоступные значения HRESULT [get_HasCurrentHeader](#get_hascurrentheader)(bool \* hasCurrent)</span><span class="sxs-lookup"><span data-stu-id="23268-125">public HRESULT [get_HasCurrentHeader](#get_hascurrentheader)(BOOL \* hasCurrent)</span></span>

<span data-ttu-id="23268-126">Если коллекция, в которой находится итератор, является пустой или, если итератор пропало за ее пределами, это ложный.</span><span class="sxs-lookup"><span data-stu-id="23268-126">If the collection over which the iterator is iterating is empty or if the iterator has gone past the end of the collection then this is false.</span></span>

#### <span data-ttu-id="23268-127">MoveNext</span><span class="sxs-lookup"><span data-stu-id="23268-127">MoveNext</span></span> 

<span data-ttu-id="23268-128">Переместите итератор на следующий заголовок HTTP в коллекции.</span><span class="sxs-lookup"><span data-stu-id="23268-128">Move the iterator to the next HTTP header in the collection.</span></span>

> <span data-ttu-id="23268-129">общедоступный HRESULT [MoveNext](#movenext)(bool \* hasNext)</span><span class="sxs-lookup"><span data-stu-id="23268-129">public HRESULT [MoveNext](#movenext)(BOOL \* hasNext)</span></span>

<span data-ttu-id="23268-130">При отсутствии заголовков HTTP для параметра hasNext будет задано значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="23268-130">The hasNext parameter will be set to FALSE if there are no more HTTP headers.</span></span> <span data-ttu-id="23268-131">После этого метод GetCurrentHeader завершается сбоем, если он вызывается.</span><span class="sxs-lookup"><span data-stu-id="23268-131">After this occurs the GetCurrentHeader method will fail if called.</span></span>

