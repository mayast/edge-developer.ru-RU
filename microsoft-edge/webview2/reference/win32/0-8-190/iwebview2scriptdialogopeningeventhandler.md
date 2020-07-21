---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2ScriptDialogOpeningEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 58e76c377d8d5709c006cb3a4da2e0edf73ec8fb
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884913"
---
# <span data-ttu-id="fd17d-104">0.8.355-Interface IWebView2ScriptDialogOpeningEventHandler</span><span class="sxs-lookup"><span data-stu-id="fd17d-104">0.8.355 - interface IWebView2ScriptDialogOpeningEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2ScriptDialogOpeningEventHandler
  : public IUnknown
```

<span data-ttu-id="fd17d-105">Вызывающий объект реализует этот интерфейс для получения события ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="fd17d-105">The caller implements this interface to receive the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="fd17d-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="fd17d-106">Summary</span></span>

 <span data-ttu-id="fd17d-107">Участников</span><span class="sxs-lookup"><span data-stu-id="fd17d-107">Members</span></span>                        | <span data-ttu-id="fd17d-108">Описания</span><span class="sxs-lookup"><span data-stu-id="fd17d-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="fd17d-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="fd17d-109">Invoke</span></span>](#invoke) | <span data-ttu-id="fd17d-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="fd17d-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="fd17d-111">Участников</span><span class="sxs-lookup"><span data-stu-id="fd17d-111">Members</span></span>

#### <span data-ttu-id="fd17d-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="fd17d-112">Invoke</span></span> 

<span data-ttu-id="fd17d-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="fd17d-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="fd17d-114">Открытый [вызов](#invoke)HRESULT ([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2ScriptDialogOpeningEventArgs](IWebView2ScriptDialogOpeningEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="fd17d-114">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2ScriptDialogOpeningEventArgs](IWebView2ScriptDialogOpeningEventArgs.md) \* args)</span></span>

