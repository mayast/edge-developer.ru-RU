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
ms.openlocfilehash: f9dcfa996058f4499daff03d8cad033ac61db4c9
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654880"
---
# <span data-ttu-id="5f334-104">интерфейс ICoreWebView2MoveFocusRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="5f334-104">interface ICoreWebView2MoveFocusRequestedEventHandler</span></span> 

```
interface ICoreWebView2MoveFocusRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="5f334-105">Вызывающий объект реализует этот метод для получения события MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="5f334-105">The caller implements this method to receive the MoveFocusRequested event.</span></span>

## <span data-ttu-id="5f334-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="5f334-106">Summary</span></span>

 <span data-ttu-id="5f334-107">Участников</span><span class="sxs-lookup"><span data-stu-id="5f334-107">Members</span></span>                        | <span data-ttu-id="5f334-108">Описания</span><span class="sxs-lookup"><span data-stu-id="5f334-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5f334-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="5f334-109">Invoke</span></span>](#invoke) | <span data-ttu-id="5f334-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="5f334-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="5f334-111">Участников</span><span class="sxs-lookup"><span data-stu-id="5f334-111">Members</span></span>

#### <span data-ttu-id="5f334-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="5f334-112">Invoke</span></span> 

<span data-ttu-id="5f334-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="5f334-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="5f334-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="5f334-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2MoveFocusRequestedEventArgs](icorewebview2movefocusrequestedeventargs.md) \* args)</span></span>

