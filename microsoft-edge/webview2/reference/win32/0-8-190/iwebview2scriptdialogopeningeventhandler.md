---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2ScriptDialogOpeningEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 70f1708d7cc908a761e96d14f25e0f1751d1923d
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878220"
---
# <span data-ttu-id="921fa-104">0.8.355-Interface IWebView2ScriptDialogOpeningEventHandler</span><span class="sxs-lookup"><span data-stu-id="921fa-104">0.8.355 - interface IWebView2ScriptDialogOpeningEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="921fa-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="921fa-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="921fa-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="921fa-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2ScriptDialogOpeningEventHandler
  : public IUnknown
```

<span data-ttu-id="921fa-107">Вызывающий объект реализует этот интерфейс для получения события ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="921fa-107">The caller implements this interface to receive the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="921fa-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="921fa-108">Summary</span></span>

 <span data-ttu-id="921fa-109">Участников</span><span class="sxs-lookup"><span data-stu-id="921fa-109">Members</span></span>                        | <span data-ttu-id="921fa-110">Описания</span><span class="sxs-lookup"><span data-stu-id="921fa-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="921fa-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="921fa-111">Invoke</span></span>](#invoke) | <span data-ttu-id="921fa-112">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="921fa-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="921fa-113">Участников</span><span class="sxs-lookup"><span data-stu-id="921fa-113">Members</span></span>

#### <span data-ttu-id="921fa-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="921fa-114">Invoke</span></span> 

<span data-ttu-id="921fa-115">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="921fa-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="921fa-116">Открытый [вызов](#invoke)HRESULT ([IWebView2WebView](IWebView2WebView.md) \* WebView,[IWebView2ScriptDialogOpeningEventArgs](IWebView2ScriptDialogOpeningEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="921fa-116">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,[IWebView2ScriptDialogOpeningEventArgs](IWebView2ScriptDialogOpeningEventArgs.md) \* args)</span></span>

