---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2AcceleratorKeyPressedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 13538c0ef14b9517a8a53e00d24ef93819adeb15
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883975"
---
# <span data-ttu-id="70aed-104">0.9.515-Interface ICoreWebView2AcceleratorKeyPressedEventHandler</span><span class="sxs-lookup"><span data-stu-id="70aed-104">0.9.515 - interface ICoreWebView2AcceleratorKeyPressedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2AcceleratorKeyPressedEventHandler
  : public IUnknown
```

<span data-ttu-id="70aed-105">Вызывающий объект реализует этот интерфейс для получения события AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="70aed-105">The caller implements this interface to receive the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="70aed-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="70aed-106">Summary</span></span>

 <span data-ttu-id="70aed-107">Участников</span><span class="sxs-lookup"><span data-stu-id="70aed-107">Members</span></span>                        | <span data-ttu-id="70aed-108">Описания</span><span class="sxs-lookup"><span data-stu-id="70aed-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="70aed-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="70aed-109">Invoke</span></span>](#invoke) | <span data-ttu-id="70aed-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="70aed-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="70aed-111">Участников</span><span class="sxs-lookup"><span data-stu-id="70aed-111">Members</span></span>

#### <span data-ttu-id="70aed-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="70aed-112">Invoke</span></span> 

<span data-ttu-id="70aed-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="70aed-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="70aed-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2AcceleratorKeyPressedEventArgs](icorewebview2acceleratorkeypressedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="70aed-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2AcceleratorKeyPressedEventArgs](icorewebview2acceleratorkeypressedeventargs.md) \* args)</span></span>

