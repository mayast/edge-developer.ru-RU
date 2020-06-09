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
ms.openlocfilehash: 84ff41eeb30d5c3561666a71f989e02163419152
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697968"
---
# <span data-ttu-id="a2903-104">интерфейс ICoreWebView2DocumentTitleChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="a2903-104">interface ICoreWebView2DocumentTitleChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="a2903-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="a2903-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="a2903-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="a2903-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2DocumentTitleChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="a2903-107">Вызывающий объект реализует этот интерфейс, чтобы получать события DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="a2903-107">The caller implements this interface to receive DocumentTitleChanged events.</span></span>

## <span data-ttu-id="a2903-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="a2903-108">Summary</span></span>

 <span data-ttu-id="a2903-109">Участников</span><span class="sxs-lookup"><span data-stu-id="a2903-109">Members</span></span>                        | <span data-ttu-id="a2903-110">Описания</span><span class="sxs-lookup"><span data-stu-id="a2903-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a2903-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="a2903-111">Invoke</span></span>](#invoke) | <span data-ttu-id="a2903-112">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="a2903-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="a2903-113">Используйте свойство DocumentTitle, чтобы получить измененный заголовок.</span><span class="sxs-lookup"><span data-stu-id="a2903-113">Use the DocumentTitle property to get the modified title.</span></span>

## <span data-ttu-id="a2903-114">Участников</span><span class="sxs-lookup"><span data-stu-id="a2903-114">Members</span></span>

#### <span data-ttu-id="a2903-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="a2903-115">Invoke</span></span> 

<span data-ttu-id="a2903-116">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="a2903-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="a2903-117">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="a2903-117">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="a2903-118">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="a2903-118">There are no event args and the args parameter will be null.</span></span>

