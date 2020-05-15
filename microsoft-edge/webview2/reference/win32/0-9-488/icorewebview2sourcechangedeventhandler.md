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
ms.openlocfilehash: d808f4b112d3688b4e50a2f6b69db38bbb4808c5
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654961"
---
# <span data-ttu-id="0b1ee-104">интерфейс ICoreWebView2SourceChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="0b1ee-104">interface ICoreWebView2SourceChangedEventHandler</span></span> 

```
interface ICoreWebView2SourceChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="0b1ee-105">Вызывающий объект реализует этот интерфейс для получения события SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="0b1ee-105">The caller implements this interface to receive the SourceChanged event.</span></span>

## <span data-ttu-id="0b1ee-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="0b1ee-106">Summary</span></span>

 <span data-ttu-id="0b1ee-107">Участников</span><span class="sxs-lookup"><span data-stu-id="0b1ee-107">Members</span></span>                        | <span data-ttu-id="0b1ee-108">Описания</span><span class="sxs-lookup"><span data-stu-id="0b1ee-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0b1ee-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="0b1ee-109">Invoke</span></span>](#invoke) | <span data-ttu-id="0b1ee-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="0b1ee-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="0b1ee-111">Участников</span><span class="sxs-lookup"><span data-stu-id="0b1ee-111">Members</span></span>

#### <span data-ttu-id="0b1ee-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="0b1ee-112">Invoke</span></span> 

<span data-ttu-id="0b1ee-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="0b1ee-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="0b1ee-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* WebView, [ICoreWebView2SourceChangedEventArgs](icorewebview2sourcechangedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="0b1ee-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, [ICoreWebView2SourceChangedEventArgs](icorewebview2sourcechangedeventargs.md) \* args)</span></span>

