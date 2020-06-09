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
ms.openlocfilehash: 9135ba6bce6b5260413f47531062ea4c96d196cc
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698136"
---
# <span data-ttu-id="a6f0c-104">интерфейс ICoreWebView2SourceChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="a6f0c-104">interface ICoreWebView2SourceChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="a6f0c-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="a6f0c-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="a6f0c-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="a6f0c-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2SourceChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="a6f0c-107">Вызывающий объект реализует этот интерфейс для получения события SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="a6f0c-107">The caller implements this interface to receive the SourceChanged event.</span></span>

## <span data-ttu-id="a6f0c-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="a6f0c-108">Summary</span></span>

 <span data-ttu-id="a6f0c-109">Участников</span><span class="sxs-lookup"><span data-stu-id="a6f0c-109">Members</span></span>                        | <span data-ttu-id="a6f0c-110">Описания</span><span class="sxs-lookup"><span data-stu-id="a6f0c-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a6f0c-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="a6f0c-111">Invoke</span></span>](#invoke) | <span data-ttu-id="a6f0c-112">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="a6f0c-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="a6f0c-113">Участников</span><span class="sxs-lookup"><span data-stu-id="a6f0c-113">Members</span></span>

#### <span data-ttu-id="a6f0c-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="a6f0c-114">Invoke</span></span> 

<span data-ttu-id="a6f0c-115">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="a6f0c-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="a6f0c-116">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* WebView, [ICoreWebView2SourceChangedEventArgs](icorewebview2sourcechangedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="a6f0c-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, [ICoreWebView2SourceChangedEventArgs](icorewebview2sourcechangedeventargs.md) \* args)</span></span>

