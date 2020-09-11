---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2AcceleratorKeyPressedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2AcceleratorKeyPressedEventHandler
ms.openlocfilehash: 15ad3a4afb76ea8068066097340af204b45fe416
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012549"
---
# <span data-ttu-id="870f2-104">интерфейс ICoreWebView2AcceleratorKeyPressedEventHandler</span><span class="sxs-lookup"><span data-stu-id="870f2-104">interface ICoreWebView2AcceleratorKeyPressedEventHandler</span></span> 

```
interface ICoreWebView2AcceleratorKeyPressedEventHandler
  : public IUnknown
```

<span data-ttu-id="870f2-105">Вызывающий объект реализует этот интерфейс для получения события AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="870f2-105">The caller implements this interface to receive the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="870f2-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="870f2-106">Summary</span></span>

 <span data-ttu-id="870f2-107">Участников</span><span class="sxs-lookup"><span data-stu-id="870f2-107">Members</span></span>                        | <span data-ttu-id="870f2-108">Описания</span><span class="sxs-lookup"><span data-stu-id="870f2-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="870f2-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="870f2-109">Invoke</span></span>](#invoke) | <span data-ttu-id="870f2-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="870f2-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="870f2-111">Участников</span><span class="sxs-lookup"><span data-stu-id="870f2-111">Members</span></span>

#### <span data-ttu-id="870f2-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="870f2-112">Invoke</span></span> 

<span data-ttu-id="870f2-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="870f2-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="870f2-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2AcceleratorKeyPressedEventArgs](icorewebview2acceleratorkeypressedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="870f2-114">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2AcceleratorKeyPressedEventArgs](icorewebview2acceleratorkeypressedeventargs.md) \* args)</span></span>

