---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2DocumentTitleChangedEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 0dc9886bc2282d08855ccb40cb8b06b4ffadb659
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886116"
---
# <span data-ttu-id="492a8-104">0.8.355-Interface IWebView2DocumentTitleChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="492a8-104">0.8.355 - interface IWebView2DocumentTitleChangedEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2DocumentTitleChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="492a8-105">Вызывающий объект реализует этот интерфейс, чтобы получать события DocumentTitleChanged.</span><span class="sxs-lookup"><span data-stu-id="492a8-105">The caller implements this interface to receive DocumentTitleChanged events.</span></span>

## <span data-ttu-id="492a8-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="492a8-106">Summary</span></span>

 <span data-ttu-id="492a8-107">Участников</span><span class="sxs-lookup"><span data-stu-id="492a8-107">Members</span></span>                        | <span data-ttu-id="492a8-108">Описания</span><span class="sxs-lookup"><span data-stu-id="492a8-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="492a8-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="492a8-109">Invoke</span></span>](#invoke) | <span data-ttu-id="492a8-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="492a8-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="492a8-111">Используйте свойство DocumentTitle, чтобы получить измененный заголовок.</span><span class="sxs-lookup"><span data-stu-id="492a8-111">Use the DocumentTitle property to get the modified title.</span></span>

## <span data-ttu-id="492a8-112">Участников</span><span class="sxs-lookup"><span data-stu-id="492a8-112">Members</span></span>

#### <span data-ttu-id="492a8-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="492a8-113">Invoke</span></span> 

<span data-ttu-id="492a8-114">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="492a8-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="492a8-115">Открытый [вызов](#invoke)HRESULT ([IWebView2WebView3](IWebView2WebView3.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="492a8-115">public HRESULT [Invoke](#invoke)([IWebView2WebView3](IWebView2WebView3.md) \* webview,IUnknown \* args)</span></span>

<span data-ttu-id="492a8-116">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="492a8-116">There are no event args and the args parameter will be null.</span></span>

