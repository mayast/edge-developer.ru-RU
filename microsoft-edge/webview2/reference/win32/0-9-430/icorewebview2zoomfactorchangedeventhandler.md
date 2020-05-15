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
ms.openlocfilehash: dd9365fb8fb0215b3090928c8edb59575c6247fe
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654958"
---
# <span data-ttu-id="5fe33-104">интерфейс ICoreWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="5fe33-104">interface ICoreWebView2ZoomFactorChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="5fe33-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="5fe33-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="5fe33-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="5fe33-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="5fe33-107">Вызывающий объект реализует этот интерфейс, чтобы получать события ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="5fe33-107">The caller implements this interface to receive ZoomFactorChanged events.</span></span>

## <span data-ttu-id="5fe33-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="5fe33-108">Summary</span></span>

 <span data-ttu-id="5fe33-109">Участников</span><span class="sxs-lookup"><span data-stu-id="5fe33-109">Members</span></span>                        | <span data-ttu-id="5fe33-110">Описания</span><span class="sxs-lookup"><span data-stu-id="5fe33-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5fe33-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="5fe33-111">Invoke</span></span>](#invoke) | <span data-ttu-id="5fe33-112">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="5fe33-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="5fe33-113">Используйте свойство ICoreWebView2Host. ZoomFactor, чтобы получить измененный коэффициент масштабирования.</span><span class="sxs-lookup"><span data-stu-id="5fe33-113">Use the ICoreWebView2Host.ZoomFactor property to get the modified zoom factor.</span></span>

## <span data-ttu-id="5fe33-114">Участников</span><span class="sxs-lookup"><span data-stu-id="5fe33-114">Members</span></span>

#### <span data-ttu-id="5fe33-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="5fe33-115">Invoke</span></span> 

<span data-ttu-id="5fe33-116">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="5fe33-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="5fe33-117">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2Host](ICoreWebView2Host.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="5fe33-117">public HRESULT [Invoke](#invoke)([ICoreWebView2Host](ICoreWebView2Host.md) \* sender,IUnknown \* args)</span></span>

<span data-ttu-id="5fe33-118">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="5fe33-118">There are no event args and the args parameter will be null.</span></span>

