---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: a02a7ac3e31f959e80d5a3bdc41e39f653b9949c
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654955"
---
# <span data-ttu-id="a6962-104">интерфейс IWebView2NewVersionAvailableEventHandler</span><span class="sxs-lookup"><span data-stu-id="a6962-104">interface IWebView2NewVersionAvailableEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="a6962-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="a6962-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="a6962-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="a6962-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2NewVersionAvailableEventHandler
  : public IUnknown
```

<span data-ttu-id="a6962-107">Вызывающий объект реализует этот интерфейс, чтобы получать события NewVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="a6962-107">The caller implements this interface to receive NewVersionAvailable events.</span></span>

## <span data-ttu-id="a6962-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="a6962-108">Summary</span></span>

 <span data-ttu-id="a6962-109">Участников</span><span class="sxs-lookup"><span data-stu-id="a6962-109">Members</span></span>                        | <span data-ttu-id="a6962-110">Описания</span><span class="sxs-lookup"><span data-stu-id="a6962-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a6962-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="a6962-111">Invoke</span></span>](#invoke) | <span data-ttu-id="a6962-112">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="a6962-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="a6962-113">Для получения нового номера версии используйте get_NewVersion метод [IWebView2NewVersionAvailableEventArgs](IWebView2NewVersionAvailableEventArgs.md) .</span><span class="sxs-lookup"><span data-stu-id="a6962-113">Use the get_NewVersion method of [IWebView2NewVersionAvailableEventArgs](IWebView2NewVersionAvailableEventArgs.md) to get the new version number.</span></span>

## <span data-ttu-id="a6962-114">Участников</span><span class="sxs-lookup"><span data-stu-id="a6962-114">Members</span></span>

#### <span data-ttu-id="a6962-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="a6962-115">Invoke</span></span> 

<span data-ttu-id="a6962-116">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="a6962-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="a6962-117">Открытый [вызов](#invoke)HRESULT ([IWebView2Environment](IWebView2Environment.md) \* webviewEnvironment,[IWebView2NewVersionAvailableEventArgs](IWebView2NewVersionAvailableEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="a6962-117">public HRESULT [Invoke](#invoke)([IWebView2Environment](IWebView2Environment.md) \* webviewEnvironment,[IWebView2NewVersionAvailableEventArgs](IWebView2NewVersionAvailableEventArgs.md) \* args)</span></span>

