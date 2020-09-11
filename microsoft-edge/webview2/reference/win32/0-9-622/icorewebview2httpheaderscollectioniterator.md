---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2HttpHeadersCollectionIterator
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2HttpHeadersCollectionIterator
ms.openlocfilehash: 8044b629c5b182d98e4731409301f615a6fba18e
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012545"
---
# интерфейс ICoreWebView2HttpHeadersCollectionIterator 

```
interface ICoreWebView2HttpHeadersCollectionIterator
  : public IUnknown
```

Итератор для коллекции заголовков HTTP.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[get_HasCurrentHeader](#get_hascurrentheader) | Имеет значение true, если итератор не исходил из заголовков.
[GetCurrentHeader](#getcurrentheader) | Получите имя и значение текущего HTTP-заголовка итератора.
[MoveNext](#movenext) | Переместите итератор на следующий заголовок HTTP в коллекции.

Смотрите [ICoreWebView2HttpRequestHeaders](icorewebview2httprequestheaders.md) и [ICoreWebView2HttpResponseHeaders](icorewebview2httpresponseheaders.md).

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

## Участников

#### get_HasCurrentHeader 

Имеет значение true, если итератор не исходил из заголовков.

> общедоступные значения HRESULT [get_HasCurrentHeader](#get_hascurrentheader)(bool * hasCurrent)

Если коллекция, в которой находится итератор, является пустой или, если итератор пропало за ее пределами, это ложный.

#### GetCurrentHeader 

Получите имя и значение текущего HTTP-заголовка итератора.

> Public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR * имя, LPWSTR * значение)

Этот метод завершается сбоем, если последний вызов MoveNext устанавливает для hasNext значение FALSE.

#### MoveNext 

Переместите итератор на следующий заголовок HTTP в коллекции.

> общедоступный HRESULT [MoveNext](#movenext)(bool * hasNext)

При отсутствии заголовков HTTP для параметра hasNext будет задано значение FALSE. После этого метод GetCurrentHeader завершается сбоем, если он вызывается.

