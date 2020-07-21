---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2AcceleratorKeyPressedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 2e12f96307b86fe4c3416c4bde2379869b269cb8
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884360"
---
# <span data-ttu-id="ec21a-104">0.9.430-Interface ICoreWebView2AcceleratorKeyPressedEventHandler</span><span class="sxs-lookup"><span data-stu-id="ec21a-104">0.9.430 - interface ICoreWebView2AcceleratorKeyPressedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2AcceleratorKeyPressedEventHandler
  : public IUnknown
```

<span data-ttu-id="ec21a-105">Вызывающий объект реализует этот интерфейс для получения события AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="ec21a-105">The caller implements this interface to receive the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="ec21a-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="ec21a-106">Summary</span></span>

 <span data-ttu-id="ec21a-107">Участников</span><span class="sxs-lookup"><span data-stu-id="ec21a-107">Members</span></span>                        | <span data-ttu-id="ec21a-108">Описания</span><span class="sxs-lookup"><span data-stu-id="ec21a-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ec21a-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="ec21a-109">Invoke</span></span>](#invoke) | <span data-ttu-id="ec21a-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="ec21a-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="ec21a-111">Участников</span><span class="sxs-lookup"><span data-stu-id="ec21a-111">Members</span></span>

#### <span data-ttu-id="ec21a-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="ec21a-112">Invoke</span></span> 

<span data-ttu-id="ec21a-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="ec21a-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="ec21a-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2Host](ICoreWebView2Host.md) \* sender,[ICoreWebView2AcceleratorKeyPressedEventArgs](ICoreWebView2AcceleratorKeyPressedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="ec21a-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Host](ICoreWebView2Host.md) \* sender,[ICoreWebView2AcceleratorKeyPressedEventArgs](ICoreWebView2AcceleratorKeyPressedEventArgs.md) \* args)</span></span>

