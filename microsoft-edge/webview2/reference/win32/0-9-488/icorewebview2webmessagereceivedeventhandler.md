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
ms.openlocfilehash: 73af2e217ca645536623eca18ceafad3270529cd
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654911"
---
# <span data-ttu-id="835c5-104">интерфейс ICoreWebView2WebMessageReceivedEventHandler</span><span class="sxs-lookup"><span data-stu-id="835c5-104">interface ICoreWebView2WebMessageReceivedEventHandler</span></span> 

```
interface ICoreWebView2WebMessageReceivedEventHandler
  : public IUnknown
```

<span data-ttu-id="835c5-105">Вызывающий объект реализует этот интерфейс для получения события WebMessageReceived.</span><span class="sxs-lookup"><span data-stu-id="835c5-105">The caller implements this interface to receive the WebMessageReceived event.</span></span>

## <span data-ttu-id="835c5-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="835c5-106">Summary</span></span>

 <span data-ttu-id="835c5-107">Участников</span><span class="sxs-lookup"><span data-stu-id="835c5-107">Members</span></span>                        | <span data-ttu-id="835c5-108">Описания</span><span class="sxs-lookup"><span data-stu-id="835c5-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="835c5-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="835c5-109">Invoke</span></span>](#invoke) | <span data-ttu-id="835c5-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="835c5-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="835c5-111">Участников</span><span class="sxs-lookup"><span data-stu-id="835c5-111">Members</span></span>

#### <span data-ttu-id="835c5-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="835c5-112">Invoke</span></span> 

<span data-ttu-id="835c5-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="835c5-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="835c5-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebMessageReceivedEventArgs](icorewebview2webmessagereceivedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="835c5-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2WebMessageReceivedEventArgs](icorewebview2webmessagereceivedeventargs.md) \* args)</span></span>

