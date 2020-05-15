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
ms.openlocfilehash: b44724f8e18e11374f88ed2cd22711f06f59f12d
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654859"
---
# <span data-ttu-id="af261-104">интерфейс ICoreWebView2NewBrowserVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="af261-104">interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="af261-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="af261-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="af261-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="af261-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NewBrowserVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="af261-107">Вызывающий объект реализует этот интерфейс, чтобы получать события NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="af261-107">The caller implements this interface to receive NewBrowserVersionAvailable events.</span></span>

## <span data-ttu-id="af261-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="af261-108">Summary</span></span>

 <span data-ttu-id="af261-109">Участников</span><span class="sxs-lookup"><span data-stu-id="af261-109">Members</span></span>                        | <span data-ttu-id="af261-110">Описания</span><span class="sxs-lookup"><span data-stu-id="af261-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="af261-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="af261-111">Invoke</span></span>](#invoke) | <span data-ttu-id="af261-112">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="af261-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="af261-113">Для получения нового номера версии используйте get_NewVersion метод [ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) .</span><span class="sxs-lookup"><span data-stu-id="af261-113">Use the get_NewVersion method of [ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) to get the new version number.</span></span>

## <span data-ttu-id="af261-114">Участников</span><span class="sxs-lookup"><span data-stu-id="af261-114">Members</span></span>

#### <span data-ttu-id="af261-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="af261-115">Invoke</span></span> 

<span data-ttu-id="af261-116">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="af261-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="af261-117">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2Environment](ICoreWebView2Environment.md) \* webviewEnvironment,[ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="af261-117">public HRESULT [Invoke](#invoke)([ICoreWebView2Environment](ICoreWebView2Environment.md) \* webviewEnvironment,[ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) \* args)</span></span>

