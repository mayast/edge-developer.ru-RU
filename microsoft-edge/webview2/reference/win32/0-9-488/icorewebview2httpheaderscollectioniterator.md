---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 2f0a41c72c6ac6f7bcfbf7a5cbd5eef61ffa3a68
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697268"
---
# <span data-ttu-id="e10f6-104">интерфейс ICoreWebView2HttpHeadersCollectionIterator</span><span class="sxs-lookup"><span data-stu-id="e10f6-104">interface ICoreWebView2HttpHeadersCollectionIterator</span></span> 

> [!NOTE]
> <span data-ttu-id="e10f6-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="e10f6-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="e10f6-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="e10f6-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HttpHeadersCollectionIterator
  : public IUnknown
```

<span data-ttu-id="e10f6-107">Итератор для коллекции заголовков HTTP.</span><span class="sxs-lookup"><span data-stu-id="e10f6-107">Iterator for a collection of HTTP headers.</span></span>

## <span data-ttu-id="e10f6-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="e10f6-108">Summary</span></span>

 <span data-ttu-id="e10f6-109">Участников</span><span class="sxs-lookup"><span data-stu-id="e10f6-109">Members</span></span>                        | <span data-ttu-id="e10f6-110">Описания</span><span class="sxs-lookup"><span data-stu-id="e10f6-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e10f6-111">get_HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="e10f6-111">get_HasCurrentHeader</span></span>](#get_hascurrentheader) | <span data-ttu-id="e10f6-112">Имеет значение true, если итератор не исходил из заголовков.</span><span class="sxs-lookup"><span data-stu-id="e10f6-112">True when the iterator hasn't run out of headers.</span></span>
[<span data-ttu-id="e10f6-113">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="e10f6-113">GetCurrentHeader</span></span>](#getcurrentheader) | <span data-ttu-id="e10f6-114">Получите имя и значение текущего HTTP-заголовка итератора.</span><span class="sxs-lookup"><span data-stu-id="e10f6-114">Get the name and value of the current HTTP header of the iterator.</span></span>
[<span data-ttu-id="e10f6-115">MoveNext</span><span class="sxs-lookup"><span data-stu-id="e10f6-115">MoveNext</span></span>](#movenext) | <span data-ttu-id="e10f6-116">Переместите итератор на следующий заголовок HTTP в коллекции.</span><span class="sxs-lookup"><span data-stu-id="e10f6-116">Move the iterator to the next HTTP header in the collection.</span></span>

<span data-ttu-id="e10f6-117">Смотрите [ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) и [ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md).</span><span class="sxs-lookup"><span data-stu-id="e10f6-117">See [ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) and [ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md).</span></span> 
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

## <span data-ttu-id="e10f6-118">Участников</span><span class="sxs-lookup"><span data-stu-id="e10f6-118">Members</span></span>

#### <span data-ttu-id="e10f6-119">get_HasCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="e10f6-119">get_HasCurrentHeader</span></span> 

<span data-ttu-id="e10f6-120">Имеет значение true, если итератор не исходил из заголовков.</span><span class="sxs-lookup"><span data-stu-id="e10f6-120">True when the iterator hasn't run out of headers.</span></span>

> <span data-ttu-id="e10f6-121">общедоступные значения HRESULT [get_HasCurrentHeader](#get_hascurrentheader)(bool \* hasCurrent)</span><span class="sxs-lookup"><span data-stu-id="e10f6-121">public HRESULT [get_HasCurrentHeader](#get_hascurrentheader)(BOOL \* hasCurrent)</span></span>

<span data-ttu-id="e10f6-122">Если коллекция, в которой находится итератор, является пустой или, если итератор пропало за ее пределами, это ложный.</span><span class="sxs-lookup"><span data-stu-id="e10f6-122">If the collection over which the iterator is iterating is empty or if the iterator has gone past the end of the collection then this is false.</span></span>

#### <span data-ttu-id="e10f6-123">GetCurrentHeader</span><span class="sxs-lookup"><span data-stu-id="e10f6-123">GetCurrentHeader</span></span> 

<span data-ttu-id="e10f6-124">Получите имя и значение текущего HTTP-заголовка итератора.</span><span class="sxs-lookup"><span data-stu-id="e10f6-124">Get the name and value of the current HTTP header of the iterator.</span></span>

> <span data-ttu-id="e10f6-125">Public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR \* имя, LPWSTR \* значение)</span><span class="sxs-lookup"><span data-stu-id="e10f6-125">public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR \* name, LPWSTR \* value)</span></span>

<span data-ttu-id="e10f6-126">Этот метод завершается сбоем, если последний вызов MoveNext задает has_next значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="e10f6-126">This method will fail if the last call to MoveNext set has_next to FALSE.</span></span>

#### <span data-ttu-id="e10f6-127">MoveNext</span><span class="sxs-lookup"><span data-stu-id="e10f6-127">MoveNext</span></span> 

<span data-ttu-id="e10f6-128">Переместите итератор на следующий заголовок HTTP в коллекции.</span><span class="sxs-lookup"><span data-stu-id="e10f6-128">Move the iterator to the next HTTP header in the collection.</span></span>

> <span data-ttu-id="e10f6-129">общедоступный HRESULT [MoveNext](#movenext)(bool \* hasNext)</span><span class="sxs-lookup"><span data-stu-id="e10f6-129">public HRESULT [MoveNext](#movenext)(BOOL \* hasNext)</span></span>

<span data-ttu-id="e10f6-130">При отсутствии заголовков HTTP для параметра hasNext будет задано значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="e10f6-130">The hasNext parameter will be set to FALSE if there are no more HTTP headers.</span></span> <span data-ttu-id="e10f6-131">После этого метод GetCurrentHeader завершается сбоем, если он вызывается.</span><span class="sxs-lookup"><span data-stu-id="e10f6-131">After this occurs the GetCurrentHeader method will fail if called.</span></span>

