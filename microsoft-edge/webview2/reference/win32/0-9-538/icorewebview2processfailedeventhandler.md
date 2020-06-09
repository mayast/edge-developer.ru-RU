---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 2c109e02de28101c88ea55d849db5701f36795a9
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699154"
---
# <span data-ttu-id="2fd86-104">интерфейс ICoreWebView2ProcessFailedEventHandler</span><span class="sxs-lookup"><span data-stu-id="2fd86-104">interface ICoreWebView2ProcessFailedEventHandler</span></span> 

```
interface ICoreWebView2ProcessFailedEventHandler
  : public IUnknown
```

<span data-ttu-id="2fd86-105">Вызывающий объект реализует этот интерфейс, чтобы получать события ProcessFailed.</span><span class="sxs-lookup"><span data-stu-id="2fd86-105">The caller implements this interface to receive ProcessFailed events.</span></span>

## <span data-ttu-id="2fd86-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="2fd86-106">Summary</span></span>

 <span data-ttu-id="2fd86-107">Участников</span><span class="sxs-lookup"><span data-stu-id="2fd86-107">Members</span></span>                        | <span data-ttu-id="2fd86-108">Описания</span><span class="sxs-lookup"><span data-stu-id="2fd86-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="2fd86-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="2fd86-109">Invoke</span></span>](#invoke) | <span data-ttu-id="2fd86-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="2fd86-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="2fd86-111">Участников</span><span class="sxs-lookup"><span data-stu-id="2fd86-111">Members</span></span>

#### <span data-ttu-id="2fd86-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="2fd86-112">Invoke</span></span> 

<span data-ttu-id="2fd86-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="2fd86-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="2fd86-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2ProcessFailedEventArgs](icorewebview2processfailedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="2fd86-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2ProcessFailedEventArgs](icorewebview2processfailedeventargs.md) \* args)</span></span>

