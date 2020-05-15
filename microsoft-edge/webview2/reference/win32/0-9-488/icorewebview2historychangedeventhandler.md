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
ms.openlocfilehash: 42e3767ad2a42a1d9e9931efa8a4fe844ea80dba
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654672"
---
# <span data-ttu-id="7a76e-104">интерфейс ICoreWebView2HistoryChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="7a76e-104">interface ICoreWebView2HistoryChangedEventHandler</span></span> 

```
interface ICoreWebView2HistoryChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="7a76e-105">Вызывающий объект реализует этот интерфейс для получения события HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="7a76e-105">The caller implements this interface to receive the HistoryChanged event.</span></span>

## <span data-ttu-id="7a76e-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="7a76e-106">Summary</span></span>

 <span data-ttu-id="7a76e-107">Участников</span><span class="sxs-lookup"><span data-stu-id="7a76e-107">Members</span></span>                        | <span data-ttu-id="7a76e-108">Описания</span><span class="sxs-lookup"><span data-stu-id="7a76e-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7a76e-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="7a76e-109">Invoke</span></span>](#invoke) | <span data-ttu-id="7a76e-110">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="7a76e-110">There are no event args and the args parameter will be null.</span></span>

## <span data-ttu-id="7a76e-111">Участников</span><span class="sxs-lookup"><span data-stu-id="7a76e-111">Members</span></span>

#### <span data-ttu-id="7a76e-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="7a76e-112">Invoke</span></span> 

<span data-ttu-id="7a76e-113">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="7a76e-113">There are no event args and the args parameter will be null.</span></span>

> <span data-ttu-id="7a76e-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="7a76e-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, IUnknown \* args)</span></span>

