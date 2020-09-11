---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2HistoryChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2HistoryChangedEventHandler
ms.openlocfilehash: 909b055af0f9594bb3c85b215cb8e02f13606aa0
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012498"
---
# <span data-ttu-id="ecf17-104">интерфейс ICoreWebView2HistoryChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="ecf17-104">interface ICoreWebView2HistoryChangedEventHandler</span></span> 

```
interface ICoreWebView2HistoryChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="ecf17-105">Вызывающий объект реализует этот интерфейс для получения события HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="ecf17-105">The caller implements this interface to receive the HistoryChanged event.</span></span>

## <span data-ttu-id="ecf17-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="ecf17-106">Summary</span></span>

 <span data-ttu-id="ecf17-107">Участников</span><span class="sxs-lookup"><span data-stu-id="ecf17-107">Members</span></span>                        | <span data-ttu-id="ecf17-108">Описания</span><span class="sxs-lookup"><span data-stu-id="ecf17-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ecf17-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="ecf17-109">Invoke</span></span>](#invoke) | <span data-ttu-id="ecf17-110">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="ecf17-110">There are no event args and the args parameter will be null.</span></span>

## <span data-ttu-id="ecf17-111">Участников</span><span class="sxs-lookup"><span data-stu-id="ecf17-111">Members</span></span>

#### <span data-ttu-id="ecf17-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="ecf17-112">Invoke</span></span> 

<span data-ttu-id="ecf17-113">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="ecf17-113">There are no event args and the args parameter will be null.</span></span>

> <span data-ttu-id="ecf17-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="ecf17-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

