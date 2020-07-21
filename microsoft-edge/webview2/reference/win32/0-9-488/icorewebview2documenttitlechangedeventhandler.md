---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2DocumentTitleChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 486218dcb54281da559fb5b5f69314248a0d2cad
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10883821"
---
# <span data-ttu-id="c4407-104">0.9.515-Interface ICoreWebView2DocumentTitleChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="c4407-104">0.9.515 - interface ICoreWebView2DocumentTitleChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2DocumentTitleChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="c4407-105">Вызывающий объект реализует этот интерфейс, чтобы получать события DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="c4407-105">The caller implements this interface to receive DocumentTitleChanged events.</span></span>

## <span data-ttu-id="c4407-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="c4407-106">Summary</span></span>

 <span data-ttu-id="c4407-107">Участников</span><span class="sxs-lookup"><span data-stu-id="c4407-107">Members</span></span>                        | <span data-ttu-id="c4407-108">Описания</span><span class="sxs-lookup"><span data-stu-id="c4407-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c4407-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="c4407-109">Invoke</span></span>](#invoke) | <span data-ttu-id="c4407-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="c4407-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="c4407-111">Используйте свойство DocumentTitle, чтобы получить измененный заголовок.</span><span class="sxs-lookup"><span data-stu-id="c4407-111">Use the DocumentTitle property to get the modified title.</span></span>

## <span data-ttu-id="c4407-112">Участников</span><span class="sxs-lookup"><span data-stu-id="c4407-112">Members</span></span>

#### <span data-ttu-id="c4407-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="c4407-113">Invoke</span></span> 

<span data-ttu-id="c4407-114">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="c4407-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="c4407-115">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="c4407-115">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, IUnknown \* args)</span></span>

<span data-ttu-id="c4407-116">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="c4407-116">There are no event args and the args parameter will be null.</span></span>

