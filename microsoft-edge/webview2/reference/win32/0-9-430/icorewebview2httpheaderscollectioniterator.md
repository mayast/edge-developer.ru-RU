---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2HttpHeadersCollectionIterator
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 640926481e99c6571c0cbf9c345efa56d97e3f66
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885599"
---
# 0.9.430-Interface ICoreWebView2HttpHeadersCollectionIterator 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2HttpHeadersCollectionIterator
  : public IUnknown
```

Итератор для коллекции заголовков HTTP.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[GetCurrentHeader](#getcurrentheader) | Получите имя и значение текущего HTTP-заголовка итератора.
[get_HasCurrentHeader](#get_hascurrentheader) | Имеет значение true, если итератор не исходил из заголовков.
[MoveNext](#movenext) | Переместите итератор на следующий заголовок HTTP в коллекции.

Смотрите [ICoreWebView2HttpRequestHeaders](ICoreWebView2HttpRequestHeaders.md) и [ICoreWebView2HttpResponseHeaders](ICoreWebView2HttpResponseHeaders.md). 

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

#### GetCurrentHeader 

Получите имя и значение текущего HTTP-заголовка итератора.

> Public HRESULT [GetCurrentHeader](#getcurrentheader)(LPWSTR * имя, LPWSTR * значение)

Этот метод завершается сбоем, если последний вызов MoveNext задает has_next значение FALSE.

#### get_HasCurrentHeader 

Имеет значение true, если итератор не исходил из заголовков.

> общедоступные значения HRESULT [get_HasCurrentHeader](#get_hascurrentheader)(bool * hasCurrent)

Если коллекция, в которой находится итератор, является пустой или, если итератор пропало за ее пределами, это ложный.

#### MoveNext 

Переместите итератор на следующий заголовок HTTP в коллекции.

> общедоступный HRESULT [MoveNext](#movenext)(bool * hasNext)

При отсутствии заголовков HTTP для параметра hasNext будет задано значение FALSE. После этого метод GetCurrentHeader завершается сбоем, если он вызывается.

