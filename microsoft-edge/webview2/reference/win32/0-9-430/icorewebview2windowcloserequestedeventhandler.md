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
ms.openlocfilehash: 160395777b2936894001adfff1450d790e8da2c4
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654915"
---
# <span data-ttu-id="b9558-104">интерфейс ICoreWebView2WindowCloseRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="b9558-104">interface ICoreWebView2WindowCloseRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="b9558-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="b9558-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="b9558-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="b9558-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2WindowCloseRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="b9558-107">Вызывающий объект реализует этот интерфейс, чтобы получать события NewWindowRequested.</span><span class="sxs-lookup"><span data-stu-id="b9558-107">The caller implements this interface to receive NewWindowRequested events.</span></span>

## <span data-ttu-id="b9558-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="b9558-108">Summary</span></span>

 <span data-ttu-id="b9558-109">Участников</span><span class="sxs-lookup"><span data-stu-id="b9558-109">Members</span></span>                        | <span data-ttu-id="b9558-110">Описания</span><span class="sxs-lookup"><span data-stu-id="b9558-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b9558-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="b9558-111">Invoke</span></span>](#invoke) | <span data-ttu-id="b9558-112">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="b9558-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="b9558-113">Участников</span><span class="sxs-lookup"><span data-stu-id="b9558-113">Members</span></span>

#### <span data-ttu-id="b9558-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="b9558-114">Invoke</span></span> 

<span data-ttu-id="b9558-115">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="b9558-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="b9558-116">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](ICoreWebView2.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="b9558-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,IUnknown \* args)</span></span>

<span data-ttu-id="b9558-117">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="b9558-117">There are no event args and the args parameter will be null.</span></span>

