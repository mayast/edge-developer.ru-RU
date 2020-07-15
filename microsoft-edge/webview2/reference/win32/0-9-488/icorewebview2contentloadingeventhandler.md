---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ContentLoadingEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 6f817fd5e602582c47c2785459d2a3987174a7b8
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880775"
---
# <span data-ttu-id="47df0-104">0.9.515-Interface ICoreWebView2ContentLoadingEventHandler</span><span class="sxs-lookup"><span data-stu-id="47df0-104">0.9.515 - interface ICoreWebView2ContentLoadingEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="47df0-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="47df0-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="47df0-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="47df0-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ContentLoadingEventHandler
  : public IUnknown
```

<span data-ttu-id="47df0-107">Вызывающий объект реализует этот интерфейс для получения события ContentLoading.</span><span class="sxs-lookup"><span data-stu-id="47df0-107">The caller implements this interface to receive the ContentLoading event.</span></span>

## <span data-ttu-id="47df0-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="47df0-108">Summary</span></span>

 <span data-ttu-id="47df0-109">Участников</span><span class="sxs-lookup"><span data-stu-id="47df0-109">Members</span></span>                        | <span data-ttu-id="47df0-110">Описания</span><span class="sxs-lookup"><span data-stu-id="47df0-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="47df0-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="47df0-111">Invoke</span></span>](#invoke) | <span data-ttu-id="47df0-112">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="47df0-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="47df0-113">Участников</span><span class="sxs-lookup"><span data-stu-id="47df0-113">Members</span></span>

#### <span data-ttu-id="47df0-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="47df0-114">Invoke</span></span> 

<span data-ttu-id="47df0-115">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="47df0-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="47df0-116">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* WebView, [ICoreWebView2ContentLoadingEventArgs](icorewebview2contentloadingeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="47df0-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, [ICoreWebView2ContentLoadingEventArgs](icorewebview2contentloadingeventargs.md) \* args)</span></span>

