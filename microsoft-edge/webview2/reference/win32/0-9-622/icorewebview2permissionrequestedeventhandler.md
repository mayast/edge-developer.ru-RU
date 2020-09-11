---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2PermissionRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2PermissionRequestedEventHandler
ms.openlocfilehash: 5d906c85cf36ccf270d9af342e329e1d969ff494
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012541"
---
# <span data-ttu-id="75ed2-104">интерфейс ICoreWebView2PermissionRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="75ed2-104">interface ICoreWebView2PermissionRequestedEventHandler</span></span> 

```
interface ICoreWebView2PermissionRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="75ed2-105">Вызывающий объект реализует этот интерфейс для получения события PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="75ed2-105">The caller implements this interface to receive the PermissionRequested event.</span></span>

## <span data-ttu-id="75ed2-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="75ed2-106">Summary</span></span>

 <span data-ttu-id="75ed2-107">Участников</span><span class="sxs-lookup"><span data-stu-id="75ed2-107">Members</span></span>                        | <span data-ttu-id="75ed2-108">Описания</span><span class="sxs-lookup"><span data-stu-id="75ed2-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="75ed2-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="75ed2-109">Invoke</span></span>](#invoke) | <span data-ttu-id="75ed2-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="75ed2-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="75ed2-111">Участников</span><span class="sxs-lookup"><span data-stu-id="75ed2-111">Members</span></span>

#### <span data-ttu-id="75ed2-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="75ed2-112">Invoke</span></span> 

<span data-ttu-id="75ed2-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="75ed2-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="75ed2-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2PermissionRequestedEventArgs](icorewebview2permissionrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="75ed2-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2PermissionRequestedEventArgs](icorewebview2permissionrequestedeventargs.md) \* args)</span></span>

