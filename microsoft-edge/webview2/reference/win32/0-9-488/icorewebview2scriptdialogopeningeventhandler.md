---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ScriptDialogOpeningEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 90721fff94948c632c1bb19d861ffc7d4911faff
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884766"
---
# <span data-ttu-id="aae94-104">0.9.515-Interface ICoreWebView2ScriptDialogOpeningEventHandler</span><span class="sxs-lookup"><span data-stu-id="aae94-104">0.9.515 - interface ICoreWebView2ScriptDialogOpeningEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ScriptDialogOpeningEventHandler
  : public IUnknown
```

<span data-ttu-id="aae94-105">Вызывающий объект реализует этот интерфейс для получения события ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="aae94-105">The caller implements this interface to receive the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="aae94-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="aae94-106">Summary</span></span>

 <span data-ttu-id="aae94-107">Участников</span><span class="sxs-lookup"><span data-stu-id="aae94-107">Members</span></span>                        | <span data-ttu-id="aae94-108">Описания</span><span class="sxs-lookup"><span data-stu-id="aae94-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="aae94-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="aae94-109">Invoke</span></span>](#invoke) | <span data-ttu-id="aae94-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="aae94-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="aae94-111">Участников</span><span class="sxs-lookup"><span data-stu-id="aae94-111">Members</span></span>

#### <span data-ttu-id="aae94-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="aae94-112">Invoke</span></span> 

<span data-ttu-id="aae94-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="aae94-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="aae94-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2ScriptDialogOpeningEventArgs](icorewebview2scriptdialogopeningeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="aae94-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2ScriptDialogOpeningEventArgs](icorewebview2scriptdialogopeningeventargs.md) \* args)</span></span>

