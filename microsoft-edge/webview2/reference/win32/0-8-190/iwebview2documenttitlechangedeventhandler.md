---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 69d8f410c7d9e7c4a8b1dc526babf535a372048f
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654858"
---
# <span data-ttu-id="b0214-104">интерфейс IWebView2DocumentTitleChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="b0214-104">interface IWebView2DocumentTitleChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="b0214-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="b0214-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="b0214-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="b0214-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2DocumentTitleChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="b0214-107">Вызывающий объект реализует этот интерфейс, чтобы получать события DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="b0214-107">The caller implements this interface to receive DocumentTitleChanged events.</span></span>

## <span data-ttu-id="b0214-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="b0214-108">Summary</span></span>

 <span data-ttu-id="b0214-109">Участников</span><span class="sxs-lookup"><span data-stu-id="b0214-109">Members</span></span>                        | <span data-ttu-id="b0214-110">Описания</span><span class="sxs-lookup"><span data-stu-id="b0214-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b0214-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="b0214-111">Invoke</span></span>](#invoke) | <span data-ttu-id="b0214-112">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="b0214-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="b0214-113">Используйте свойство DocumentTitle, чтобы получить измененный заголовок.</span><span class="sxs-lookup"><span data-stu-id="b0214-113">Use the DocumentTitle property to get the modified title.</span></span>

## <span data-ttu-id="b0214-114">Участников</span><span class="sxs-lookup"><span data-stu-id="b0214-114">Members</span></span>

#### <span data-ttu-id="b0214-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="b0214-115">Invoke</span></span> 

<span data-ttu-id="b0214-116">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="b0214-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="b0214-117">Открытый [вызов](#invoke)HRESULT ([IWebView2WebView3](IWebView2WebView3.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="b0214-117">public HRESULT [Invoke](#invoke)([IWebView2WebView3](IWebView2WebView3.md) \* webview,IUnknown \* args)</span></span>

<span data-ttu-id="b0214-118">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="b0214-118">There are no event args and the args parameter will be null.</span></span>

