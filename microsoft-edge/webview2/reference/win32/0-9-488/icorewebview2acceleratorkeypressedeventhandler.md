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
ms.openlocfilehash: 5cbf358780d196168976fc0812c9845d0ec59b24
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654732"
---
# <span data-ttu-id="7eec9-104">интерфейс ICoreWebView2AcceleratorKeyPressedEventHandler</span><span class="sxs-lookup"><span data-stu-id="7eec9-104">interface ICoreWebView2AcceleratorKeyPressedEventHandler</span></span> 

```
interface ICoreWebView2AcceleratorKeyPressedEventHandler
  : public IUnknown
```

<span data-ttu-id="7eec9-105">Вызывающий объект реализует этот интерфейс для получения события AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="7eec9-105">The caller implements this interface to receive the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="7eec9-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="7eec9-106">Summary</span></span>

 <span data-ttu-id="7eec9-107">Участников</span><span class="sxs-lookup"><span data-stu-id="7eec9-107">Members</span></span>                        | <span data-ttu-id="7eec9-108">Описания</span><span class="sxs-lookup"><span data-stu-id="7eec9-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7eec9-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="7eec9-109">Invoke</span></span>](#invoke) | <span data-ttu-id="7eec9-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="7eec9-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="7eec9-111">Участников</span><span class="sxs-lookup"><span data-stu-id="7eec9-111">Members</span></span>

#### <span data-ttu-id="7eec9-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="7eec9-112">Invoke</span></span> 

<span data-ttu-id="7eec9-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="7eec9-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="7eec9-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2AcceleratorKeyPressedEventArgs](icorewebview2acceleratorkeypressedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="7eec9-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2AcceleratorKeyPressedEventArgs](icorewebview2acceleratorkeypressedeventargs.md) \* args)</span></span>

