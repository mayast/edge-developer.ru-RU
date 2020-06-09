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
ms.openlocfilehash: 05dd401064635a6b20f1936b1efaac025b45749f
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699207"
---
# <span data-ttu-id="8fef6-104">интерфейс ICoreWebView2AcceleratorKeyPressedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8fef6-104">interface ICoreWebView2AcceleratorKeyPressedEventHandler</span></span> 

```
interface ICoreWebView2AcceleratorKeyPressedEventHandler
  : public IUnknown
```

<span data-ttu-id="8fef6-105">Вызывающий объект реализует этот интерфейс для получения события AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="8fef6-105">The caller implements this interface to receive the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="8fef6-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="8fef6-106">Summary</span></span>

 <span data-ttu-id="8fef6-107">Участников</span><span class="sxs-lookup"><span data-stu-id="8fef6-107">Members</span></span>                        | <span data-ttu-id="8fef6-108">Описания</span><span class="sxs-lookup"><span data-stu-id="8fef6-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8fef6-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="8fef6-109">Invoke</span></span>](#invoke) | <span data-ttu-id="8fef6-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="8fef6-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="8fef6-111">Участников</span><span class="sxs-lookup"><span data-stu-id="8fef6-111">Members</span></span>

#### <span data-ttu-id="8fef6-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="8fef6-112">Invoke</span></span> 

<span data-ttu-id="8fef6-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="8fef6-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="8fef6-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2AcceleratorKeyPressedEventArgs](icorewebview2acceleratorkeypressedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="8fef6-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2AcceleratorKeyPressedEventArgs](icorewebview2acceleratorkeypressedeventargs.md) \* args)</span></span>

