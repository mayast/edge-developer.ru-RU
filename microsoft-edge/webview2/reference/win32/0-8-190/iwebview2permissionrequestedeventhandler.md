---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2PermissionRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: aeb6e2e25ca9f8c454f5dff891f2c488591d2a48
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884934"
---
# <span data-ttu-id="f59a6-104">0.8.355-Interface IWebView2PermissionRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="f59a6-104">0.8.355 - interface IWebView2PermissionRequestedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2PermissionRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="f59a6-105">Вызывающий объект реализует этот интерфейс для получения события PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="f59a6-105">The caller implements this interface to receive the PermissionRequested event.</span></span>

## <span data-ttu-id="f59a6-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="f59a6-106">Summary</span></span>

 <span data-ttu-id="f59a6-107">Участников</span><span class="sxs-lookup"><span data-stu-id="f59a6-107">Members</span></span>                        | <span data-ttu-id="f59a6-108">Описания</span><span class="sxs-lookup"><span data-stu-id="f59a6-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f59a6-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="f59a6-109">Invoke</span></span>](#invoke) | <span data-ttu-id="f59a6-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="f59a6-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="f59a6-111">Участников</span><span class="sxs-lookup"><span data-stu-id="f59a6-111">Members</span></span>

#### <span data-ttu-id="f59a6-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="f59a6-112">Invoke</span></span> 

<span data-ttu-id="f59a6-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="f59a6-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="f59a6-114">Открытый [вызов](#invoke)HRESULT ([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2PermissionRequestedEventArgs](IWebView2PermissionRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="f59a6-114">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2PermissionRequestedEventArgs](IWebView2PermissionRequestedEventArgs.md) \* args)</span></span>

