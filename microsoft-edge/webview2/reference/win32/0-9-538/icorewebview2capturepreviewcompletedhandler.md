---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2CapturePreviewCompletedHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2CapturePreviewCompletedHandler
ms.openlocfilehash: 96fff3ab67331bf5a8cf8323af5dddbca04f9e0e
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010567"
---
# <span data-ttu-id="23f70-104">0.9.579-Interface ICoreWebView2CapturePreviewCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="23f70-104">0.9.579 - interface ICoreWebView2CapturePreviewCompletedHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2CapturePreviewCompletedHandler
  : public IUnknown
```

<span data-ttu-id="23f70-105">Вызывающий объект реализует этот метод, чтобы получить результат метода CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="23f70-105">The caller implements this method to receive the result of the CapturePreview method.</span></span>

## <span data-ttu-id="23f70-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="23f70-106">Summary</span></span>

 <span data-ttu-id="23f70-107">Участников</span><span class="sxs-lookup"><span data-stu-id="23f70-107">Members</span></span>                        | <span data-ttu-id="23f70-108">Описания</span><span class="sxs-lookup"><span data-stu-id="23f70-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="23f70-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="23f70-109">Invoke</span></span>](#invoke) | <span data-ttu-id="23f70-110">Вызывается для предоставления разработчику состояния завершения соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="23f70-110">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

<span data-ttu-id="23f70-111">Результат записывается в поток, указанный в вызове метода CapturePreview.</span><span class="sxs-lookup"><span data-stu-id="23f70-111">The result is written to the stream provided in the CapturePreview method call.</span></span>

## <span data-ttu-id="23f70-112">Участников</span><span class="sxs-lookup"><span data-stu-id="23f70-112">Members</span></span>

#### <span data-ttu-id="23f70-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="23f70-113">Invoke</span></span> 

<span data-ttu-id="23f70-114">Вызывается для предоставления разработчику состояния завершения соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="23f70-114">Called to provide the implementer with the completion status of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="23f70-115">общедоступный [вызов](#invoke)HRESULT (результат HRESULT)</span><span class="sxs-lookup"><span data-stu-id="23f70-115">public HRESULT [Invoke](#invoke)(HRESULT result)</span></span>

