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
ms.openlocfilehash: 8fd3533d8f479866989f719be6e48c437fae4ddb
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654967"
---
# <span data-ttu-id="2ad65-104">интерфейс ICoreWebView2HistoryChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="2ad65-104">interface ICoreWebView2HistoryChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="2ad65-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="2ad65-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="2ad65-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="2ad65-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HistoryChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="2ad65-107">Вызывающий объект реализует этот интерфейс для получения события HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="2ad65-107">The caller implements this interface to receive the HistoryChanged event.</span></span>

## <span data-ttu-id="2ad65-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="2ad65-108">Summary</span></span>

 <span data-ttu-id="2ad65-109">Участников</span><span class="sxs-lookup"><span data-stu-id="2ad65-109">Members</span></span>                        | <span data-ttu-id="2ad65-110">Описания</span><span class="sxs-lookup"><span data-stu-id="2ad65-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2ad65-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="2ad65-111">Invoke</span></span>](#invoke) | <span data-ttu-id="2ad65-112">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="2ad65-112">There are no event args and the args parameter will be null.</span></span>

## <span data-ttu-id="2ad65-113">Участников</span><span class="sxs-lookup"><span data-stu-id="2ad65-113">Members</span></span>

#### <span data-ttu-id="2ad65-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="2ad65-114">Invoke</span></span> 

<span data-ttu-id="2ad65-115">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="2ad65-115">There are no event args and the args parameter will be null.</span></span>

> <span data-ttu-id="2ad65-116">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](ICoreWebView2.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="2ad65-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* webview,IUnknown \* args)</span></span>

