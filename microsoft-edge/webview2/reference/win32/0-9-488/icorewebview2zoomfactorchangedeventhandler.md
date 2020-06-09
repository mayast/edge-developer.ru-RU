---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 64211bf99873ef2e2a41aaf2fb9453e892f6536a
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698108"
---
# <span data-ttu-id="1340e-104">интерфейс ICoreWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="1340e-104">interface ICoreWebView2ZoomFactorChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="1340e-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="1340e-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="1340e-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="1340e-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="1340e-107">Вызывающий объект реализует этот интерфейс, чтобы получать события ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="1340e-107">The caller implements this interface to receive ZoomFactorChanged events.</span></span>

## <span data-ttu-id="1340e-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="1340e-108">Summary</span></span>

 <span data-ttu-id="1340e-109">Участников</span><span class="sxs-lookup"><span data-stu-id="1340e-109">Members</span></span>                        | <span data-ttu-id="1340e-110">Описания</span><span class="sxs-lookup"><span data-stu-id="1340e-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="1340e-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="1340e-111">Invoke</span></span>](#invoke) | <span data-ttu-id="1340e-112">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="1340e-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="1340e-113">Используйте свойство ICoreWebView2Controller. ZoomFactor, чтобы получить измененный коэффициент масштабирования.</span><span class="sxs-lookup"><span data-stu-id="1340e-113">Use the ICoreWebView2Controller.ZoomFactor property to get the modified zoom factor.</span></span>

## <span data-ttu-id="1340e-114">Участников</span><span class="sxs-lookup"><span data-stu-id="1340e-114">Members</span></span>

#### <span data-ttu-id="1340e-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="1340e-115">Invoke</span></span> 

<span data-ttu-id="1340e-116">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="1340e-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="1340e-117">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="1340e-117">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="1340e-118">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="1340e-118">There are no event args and the args parameter will be null.</span></span>

