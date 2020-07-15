---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2DocumentTitleChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 42031b966f799b788a94938d88d9dec6f4542288
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878542"
---
# <span data-ttu-id="fd4b4-104">0.8.355-Interface IWebView2DocumentTitleChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="fd4b4-104">0.8.355 - interface IWebView2DocumentTitleChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="fd4b4-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="fd4b4-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="fd4b4-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="fd4b4-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2DocumentTitleChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="fd4b4-107">Вызывающий объект реализует этот интерфейс, чтобы получать события DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="fd4b4-107">The caller implements this interface to receive DocumentTitleChanged events.</span></span>

## <span data-ttu-id="fd4b4-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="fd4b4-108">Summary</span></span>

 <span data-ttu-id="fd4b4-109">Участников</span><span class="sxs-lookup"><span data-stu-id="fd4b4-109">Members</span></span>                        | <span data-ttu-id="fd4b4-110">Описания</span><span class="sxs-lookup"><span data-stu-id="fd4b4-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="fd4b4-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="fd4b4-111">Invoke</span></span>](#invoke) | <span data-ttu-id="fd4b4-112">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="fd4b4-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="fd4b4-113">Используйте свойство DocumentTitle, чтобы получить измененный заголовок.</span><span class="sxs-lookup"><span data-stu-id="fd4b4-113">Use the DocumentTitle property to get the modified title.</span></span>

## <span data-ttu-id="fd4b4-114">Участников</span><span class="sxs-lookup"><span data-stu-id="fd4b4-114">Members</span></span>

#### <span data-ttu-id="fd4b4-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="fd4b4-115">Invoke</span></span> 

<span data-ttu-id="fd4b4-116">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="fd4b4-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="fd4b4-117">Открытый [вызов](#invoke)HRESULT ([IWebView2WebView3](IWebView2WebView3.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="fd4b4-117">public HRESULT [Invoke](#invoke)([IWebView2WebView3](IWebView2WebView3.md) \* webview,IUnknown \* args)</span></span>

<span data-ttu-id="fd4b4-118">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="fd4b4-118">There are no event args and the args parameter will be null.</span></span>

