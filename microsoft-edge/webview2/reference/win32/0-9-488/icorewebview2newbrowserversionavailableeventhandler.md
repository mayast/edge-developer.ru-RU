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
ms.openlocfilehash: a6c12669bd90da4861412997818de49626282cb1
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697828"
---
# <span data-ttu-id="4dd87-104">интерфейс ICoreWebView2NewBrowserVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="4dd87-104">interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="4dd87-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="4dd87-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="4dd87-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="4dd87-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NewBrowserVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="4dd87-107">Вызывающий объект реализует этот интерфейс, чтобы получать события NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="4dd87-107">The caller implements this interface to receive NewBrowserVersionAvailable events.</span></span>

## <span data-ttu-id="4dd87-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="4dd87-108">Summary</span></span>

 <span data-ttu-id="4dd87-109">Участников</span><span class="sxs-lookup"><span data-stu-id="4dd87-109">Members</span></span>                        | <span data-ttu-id="4dd87-110">Описания</span><span class="sxs-lookup"><span data-stu-id="4dd87-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4dd87-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="4dd87-111">Invoke</span></span>](#invoke) | <span data-ttu-id="4dd87-112">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="4dd87-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="4dd87-113">Участников</span><span class="sxs-lookup"><span data-stu-id="4dd87-113">Members</span></span>

#### <span data-ttu-id="4dd87-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="4dd87-114">Invoke</span></span> 

<span data-ttu-id="4dd87-115">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="4dd87-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="4dd87-116">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="4dd87-116">public HRESULT [Invoke](#invoke)([ICoreWebView2Environment](icorewebview2environment.md) \* webviewEnvironment, IUnknown \* args)</span></span>

