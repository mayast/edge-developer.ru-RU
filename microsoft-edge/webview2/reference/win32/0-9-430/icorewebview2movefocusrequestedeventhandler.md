---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 5d810b4261d139eb867240a060df76126e70ade4
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655023"
---
# <span data-ttu-id="0d9fa-104">интерфейс ICoreWebView2MoveFocusRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="0d9fa-104">interface ICoreWebView2MoveFocusRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="0d9fa-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="0d9fa-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="0d9fa-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="0d9fa-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2MoveFocusRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="0d9fa-107">Вызывающий объект реализует этот метод для получения события MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="0d9fa-107">The caller implements this method to receive the MoveFocusRequested event.</span></span>

## <span data-ttu-id="0d9fa-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="0d9fa-108">Summary</span></span>

 <span data-ttu-id="0d9fa-109">Участников</span><span class="sxs-lookup"><span data-stu-id="0d9fa-109">Members</span></span>                        | <span data-ttu-id="0d9fa-110">Описания</span><span class="sxs-lookup"><span data-stu-id="0d9fa-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0d9fa-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="0d9fa-111">Invoke</span></span>](#invoke) | <span data-ttu-id="0d9fa-112">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="0d9fa-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="0d9fa-113">Участников</span><span class="sxs-lookup"><span data-stu-id="0d9fa-113">Members</span></span>

#### <span data-ttu-id="0d9fa-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="0d9fa-114">Invoke</span></span> 

<span data-ttu-id="0d9fa-115">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="0d9fa-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="0d9fa-116">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2Host](ICoreWebView2Host.md) \* sender,[ICoreWebView2MoveFocusRequestedEventArgs](ICoreWebView2MoveFocusRequestedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="0d9fa-116">public HRESULT [Invoke](#invoke)([ICoreWebView2Host](ICoreWebView2Host.md) \* sender,[ICoreWebView2MoveFocusRequestedEventArgs](ICoreWebView2MoveFocusRequestedEventArgs.md) \* args)</span></span>

