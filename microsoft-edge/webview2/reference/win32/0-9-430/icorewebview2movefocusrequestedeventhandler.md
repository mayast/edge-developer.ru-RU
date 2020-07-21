---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2MoveFocusRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: d50f84edeb532d90a1268f553b38e4cbf256556a
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884089"
---
# <span data-ttu-id="8484f-104">0.9.430-Interface ICoreWebView2MoveFocusRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8484f-104">0.9.430 - interface ICoreWebView2MoveFocusRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2MoveFocusRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="8484f-105">Вызывающий объект реализует этот метод для получения события MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="8484f-105">The caller implements this method to receive the MoveFocusRequested event.</span></span>

## <span data-ttu-id="8484f-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="8484f-106">Summary</span></span>

 <span data-ttu-id="8484f-107">Участников</span><span class="sxs-lookup"><span data-stu-id="8484f-107">Members</span></span>                        | <span data-ttu-id="8484f-108">Описания</span><span class="sxs-lookup"><span data-stu-id="8484f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8484f-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="8484f-109">Invoke</span></span>](#invoke) | <span data-ttu-id="8484f-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="8484f-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="8484f-111">Участников</span><span class="sxs-lookup"><span data-stu-id="8484f-111">Members</span></span>

#### <span data-ttu-id="8484f-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="8484f-112">Invoke</span></span> 

<span data-ttu-id="8484f-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="8484f-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="8484f-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2Host](ICoreWebView2Host.md) \* sender,[ICoreWebView2MoveFocusRequestedEventArgs](ICoreWebView2MoveFocusRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="8484f-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Host](ICoreWebView2Host.md) \* sender,[ICoreWebView2MoveFocusRequestedEventArgs](ICoreWebView2MoveFocusRequestedEventArgs.md) \* args)</span></span>

