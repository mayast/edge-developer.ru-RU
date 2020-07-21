---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2ContentLoadingEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 058e29833aa23248b34c7a1e5e5bbc2285a73fa3
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884332"
---
# <span data-ttu-id="35b46-104">0.9.430-Interface ICoreWebView2ContentLoadingEventHandler</span><span class="sxs-lookup"><span data-stu-id="35b46-104">0.9.430 - interface ICoreWebView2ContentLoadingEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ContentLoadingEventHandler
  : public IUnknown
```

<span data-ttu-id="35b46-105">Вызывающий объект реализует этот интерфейс для получения события ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="35b46-105">The caller implements this interface to receive the ContentLoading event.</span></span>

## <span data-ttu-id="35b46-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="35b46-106">Summary</span></span>

 <span data-ttu-id="35b46-107">Участников</span><span class="sxs-lookup"><span data-stu-id="35b46-107">Members</span></span>                        | <span data-ttu-id="35b46-108">Описания</span><span class="sxs-lookup"><span data-stu-id="35b46-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="35b46-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="35b46-109">Invoke</span></span>](#invoke) | <span data-ttu-id="35b46-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="35b46-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="35b46-111">Участников</span><span class="sxs-lookup"><span data-stu-id="35b46-111">Members</span></span>

#### <span data-ttu-id="35b46-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="35b46-112">Invoke</span></span> 

<span data-ttu-id="35b46-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="35b46-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="35b46-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](ICoreWebView2.md) \* WebView,[ICoreWebView2ContentLoadingEventArgs](ICoreWebView2ContentLoadingEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="35b46-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* webview,[ICoreWebView2ContentLoadingEventArgs](ICoreWebView2ContentLoadingEventArgs.md) \* args)</span></span>

