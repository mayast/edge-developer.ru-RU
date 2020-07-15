---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2AcceleratorKeyPressedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 8b0d6a4db4a4af6710df54e42b3cddee061a4040
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880964"
---
# <span data-ttu-id="237ac-104">0.9.515-Interface ICoreWebView2AcceleratorKeyPressedEventHandler</span><span class="sxs-lookup"><span data-stu-id="237ac-104">0.9.515 - interface ICoreWebView2AcceleratorKeyPressedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="237ac-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="237ac-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="237ac-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="237ac-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2AcceleratorKeyPressedEventHandler
  : public IUnknown
```

<span data-ttu-id="237ac-107">Вызывающий объект реализует этот интерфейс для получения события AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="237ac-107">The caller implements this interface to receive the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="237ac-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="237ac-108">Summary</span></span>

 <span data-ttu-id="237ac-109">Участников</span><span class="sxs-lookup"><span data-stu-id="237ac-109">Members</span></span>                        | <span data-ttu-id="237ac-110">Описания</span><span class="sxs-lookup"><span data-stu-id="237ac-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="237ac-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="237ac-111">Invoke</span></span>](#invoke) | <span data-ttu-id="237ac-112">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="237ac-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="237ac-113">Участников</span><span class="sxs-lookup"><span data-stu-id="237ac-113">Members</span></span>

#### <span data-ttu-id="237ac-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="237ac-114">Invoke</span></span> 

<span data-ttu-id="237ac-115">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="237ac-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="237ac-116">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2AcceleratorKeyPressedEventArgs](icorewebview2acceleratorkeypressedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="237ac-116">public HRESULT [Invoke](#invoke)([ICoreWebView2Controller](icorewebview2controller.md) \* sender, [ICoreWebView2AcceleratorKeyPressedEventArgs](icorewebview2acceleratorkeypressedeventargs.md) \* args)</span></span>

