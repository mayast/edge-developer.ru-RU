---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2ZoomFactorChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: d4e565db43e9f528b690ab32a784bfd5e40f787b
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10877289"
---
# <span data-ttu-id="777db-104">0.9.515-Interface ICoreWebView2ZoomFactorChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="777db-104">0.9.515 - interface ICoreWebView2ZoomFactorChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="777db-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="777db-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="777db-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="777db-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ZoomFactorChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="777db-107">Вызывающий объект реализует этот интерфейс, чтобы получать события ZoomFactorChanged.</span><span class="sxs-lookup"><span data-stu-id="777db-107">The caller implements this interface to receive ZoomFactorChanged events.</span></span>

## <span data-ttu-id="777db-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="777db-108">Summary</span></span>

 <span data-ttu-id="777db-109">Участников</span><span class="sxs-lookup"><span data-stu-id="777db-109">Members</span></span>                        | <span data-ttu-id="777db-110">Описания</span><span class="sxs-lookup"><span data-stu-id="777db-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="777db-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="777db-111">Invoke</span></span>](#invoke) | <span data-ttu-id="777db-112">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="777db-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="777db-113">Используйте свойство ICoreWebView2Controller. ZoomFactor, чтобы получить измененный коэффициент масштабирования.</span><span class="sxs-lookup"><span data-stu-id="777db-113">Use the ICoreWebView2Controller.ZoomFactor property to get the modified zoom factor.</span></span>

## <span data-ttu-id="777db-114">Участников</span><span class="sxs-lookup"><span data-stu-id="777db-114">Members</span></span>

#### <span data-ttu-id="777db-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="777db-115">Invoke</span></span> 

<span data-ttu-id="777db-116">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="777db-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="777db-117">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="777db-117">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="777db-118">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="777db-118">There are no event args and the args parameter will be null.</span></span>

