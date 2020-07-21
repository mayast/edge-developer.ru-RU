---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2AcceleratorKeyPressedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 7d510a547e43a4f04ef517c393ceeb3040d914e7
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885033"
---
# <span data-ttu-id="3d627-104">0.8.355-Interface IWebView2AcceleratorKeyPressedEventHandler</span><span class="sxs-lookup"><span data-stu-id="3d627-104">0.8.355 - interface IWebView2AcceleratorKeyPressedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2AcceleratorKeyPressedEventHandler
  : public IUnknown
```

<span data-ttu-id="3d627-105">Вызывающий объект реализует этот интерфейс для получения события AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="3d627-105">The caller implements this interface to receive the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="3d627-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="3d627-106">Summary</span></span>

 <span data-ttu-id="3d627-107">Участников</span><span class="sxs-lookup"><span data-stu-id="3d627-107">Members</span></span>                        | <span data-ttu-id="3d627-108">Описания</span><span class="sxs-lookup"><span data-stu-id="3d627-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3d627-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="3d627-109">Invoke</span></span>](#invoke) | <span data-ttu-id="3d627-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="3d627-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="3d627-111">Участников</span><span class="sxs-lookup"><span data-stu-id="3d627-111">Members</span></span>

#### <span data-ttu-id="3d627-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="3d627-112">Invoke</span></span> 

<span data-ttu-id="3d627-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="3d627-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="3d627-114">Открытый [вызов](#invoke)HRESULT ([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2AcceleratorKeyPressedEventArgs](IWebView2AcceleratorKeyPressedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="3d627-114">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2AcceleratorKeyPressedEventArgs](IWebView2AcceleratorKeyPressedEventArgs.md) \* args)</span></span>

