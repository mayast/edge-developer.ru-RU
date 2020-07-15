---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2PermissionRequestedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: d8703ee6bd985d276688901534dadd836aa6c7fc
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877788"
---
# <span data-ttu-id="949c8-104">0.9.430-Interface ICoreWebView2PermissionRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="949c8-104">0.9.430 - interface ICoreWebView2PermissionRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="949c8-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="949c8-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="949c8-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="949c8-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2PermissionRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="949c8-107">Вызывающий объект реализует этот интерфейс для получения события PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="949c8-107">The caller implements this interface to receive the PermissionRequested event.</span></span>

## <span data-ttu-id="949c8-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="949c8-108">Summary</span></span>

 <span data-ttu-id="949c8-109">Участников</span><span class="sxs-lookup"><span data-stu-id="949c8-109">Members</span></span>                        | <span data-ttu-id="949c8-110">Описания</span><span class="sxs-lookup"><span data-stu-id="949c8-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="949c8-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="949c8-111">Invoke</span></span>](#invoke) | <span data-ttu-id="949c8-112">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="949c8-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="949c8-113">Участников</span><span class="sxs-lookup"><span data-stu-id="949c8-113">Members</span></span>

#### <span data-ttu-id="949c8-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="949c8-114">Invoke</span></span> 

<span data-ttu-id="949c8-115">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="949c8-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="949c8-116">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2PermissionRequestedEventArgs](ICoreWebView2PermissionRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="949c8-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2PermissionRequestedEventArgs](ICoreWebView2PermissionRequestedEventArgs.md) \* args)</span></span>

