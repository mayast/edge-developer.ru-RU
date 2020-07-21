---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2NewVersionAvailableEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 3a9af31477e7b4155bece55ec2faef85efccbd0d
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884983"
---
# <span data-ttu-id="52d66-104">0.8.355-Interface IWebView2NewVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="52d66-104">0.8.355 - interface IWebView2NewVersionAvailableEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2NewVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="52d66-105">Вызывающий объект реализует этот интерфейс, чтобы получать события NewVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="52d66-105">The caller implements this interface to receive NewVersionAvailable events.</span></span>

## <span data-ttu-id="52d66-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="52d66-106">Summary</span></span>

 <span data-ttu-id="52d66-107">Участников</span><span class="sxs-lookup"><span data-stu-id="52d66-107">Members</span></span>                        | <span data-ttu-id="52d66-108">Описания</span><span class="sxs-lookup"><span data-stu-id="52d66-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="52d66-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="52d66-109">Invoke</span></span>](#invoke) | <span data-ttu-id="52d66-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="52d66-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="52d66-111">Для получения нового номера версии используйте get_NewVersion метод [IWebView2NewVersionAvailableEventArgs](IWebView2NewVersionAvailableEventArgs.md) .</span><span class="sxs-lookup"><span data-stu-id="52d66-111">Use the get_NewVersion method of [IWebView2NewVersionAvailableEventArgs](IWebView2NewVersionAvailableEventArgs.md) to get the new version number.</span></span>

## <span data-ttu-id="52d66-112">Участников</span><span class="sxs-lookup"><span data-stu-id="52d66-112">Members</span></span>

#### <span data-ttu-id="52d66-113">Invoke</span><span class="sxs-lookup"><span data-stu-id="52d66-113">Invoke</span></span> 

<span data-ttu-id="52d66-114">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="52d66-114">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="52d66-115">Открытый [вызов](#invoke)HRESULT ([IWebView2Environment](IWebView2Environment.md) \* webviewEnvironment,[IWebView2NewVersionAvailableEventArgs](IWebView2NewVersionAvailableEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="52d66-115">public HRESULT [Invoke](#invoke)([IWebView2Environment](IWebView2Environment.md) \* webviewEnvironment,[IWebView2NewVersionAvailableEventArgs](IWebView2NewVersionAvailableEventArgs.md) \* args)</span></span>

