---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2NewBrowserVersionAvailableEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 42f63855c97363dab1a19cc784cf654afc40de74
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877849"
---
# <span data-ttu-id="fa594-104">0.9.430-Interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="fa594-104">0.9.430 - interface ICoreWebView2NewBrowserVersionAvailableEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="fa594-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="fa594-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="fa594-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="fa594-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NewBrowserVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="fa594-107">Вызывающий объект реализует этот интерфейс, чтобы получать события NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="fa594-107">The caller implements this interface to receive NewBrowserVersionAvailable events.</span></span>

## <span data-ttu-id="fa594-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="fa594-108">Summary</span></span>

 <span data-ttu-id="fa594-109">Участников</span><span class="sxs-lookup"><span data-stu-id="fa594-109">Members</span></span>                        | <span data-ttu-id="fa594-110">Описания</span><span class="sxs-lookup"><span data-stu-id="fa594-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="fa594-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="fa594-111">Invoke</span></span>](#invoke) | <span data-ttu-id="fa594-112">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="fa594-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="fa594-113">Для получения нового номера версии используйте get_NewVersion метод [ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) .</span><span class="sxs-lookup"><span data-stu-id="fa594-113">Use the get_NewVersion method of [ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) to get the new version number.</span></span>

## <span data-ttu-id="fa594-114">Участников</span><span class="sxs-lookup"><span data-stu-id="fa594-114">Members</span></span>

#### <span data-ttu-id="fa594-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="fa594-115">Invoke</span></span> 

<span data-ttu-id="fa594-116">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="fa594-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="fa594-117">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2Environment](ICoreWebView2Environment.md) \* webviewEnvironment,[ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="fa594-117">public HRESULT [Invoke](#invoke)([ICoreWebView2Environment](ICoreWebView2Environment.md) \* webviewEnvironment,[ICoreWebView2NewBrowserVersionAvailableEventArgs](ICoreWebView2NewBrowserVersionAvailableEventArgs.md) \* args)</span></span>

