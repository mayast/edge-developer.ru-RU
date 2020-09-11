---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2ScriptDialogOpeningEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2ScriptDialogOpeningEventHandler
ms.openlocfilehash: fea5ace11a4d1f1ecec9b13382184514d789a308
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010651"
---
# <span data-ttu-id="ed76f-104">0.9.579-Interface ICoreWebView2ScriptDialogOpeningEventHandler</span><span class="sxs-lookup"><span data-stu-id="ed76f-104">0.9.579 - interface ICoreWebView2ScriptDialogOpeningEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ScriptDialogOpeningEventHandler
  : public IUnknown
```

<span data-ttu-id="ed76f-105">Вызывающий объект реализует этот интерфейс для получения события ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="ed76f-105">The caller implements this interface to receive the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="ed76f-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="ed76f-106">Summary</span></span>

 <span data-ttu-id="ed76f-107">Участников</span><span class="sxs-lookup"><span data-stu-id="ed76f-107">Members</span></span>                        | <span data-ttu-id="ed76f-108">Описания</span><span class="sxs-lookup"><span data-stu-id="ed76f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="ed76f-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="ed76f-109">Invoke</span></span>](#invoke) | <span data-ttu-id="ed76f-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="ed76f-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="ed76f-111">Участников</span><span class="sxs-lookup"><span data-stu-id="ed76f-111">Members</span></span>

#### <span data-ttu-id="ed76f-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="ed76f-112">Invoke</span></span> 

<span data-ttu-id="ed76f-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="ed76f-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="ed76f-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2ScriptDialogOpeningEventArgs](icorewebview2scriptdialogopeningeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="ed76f-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2ScriptDialogOpeningEventArgs](icorewebview2scriptdialogopeningeventargs.md) \* args)</span></span>

