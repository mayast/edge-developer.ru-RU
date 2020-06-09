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
ms.openlocfilehash: 4ba3a5acd293b67947622ef4a409319164a23d35
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698031"
---
# <span data-ttu-id="54283-104">интерфейс ICoreWebView2PermissionRequestedEventHandler</span><span class="sxs-lookup"><span data-stu-id="54283-104">interface ICoreWebView2PermissionRequestedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="54283-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="54283-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="54283-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="54283-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2PermissionRequestedEventHandler
  : public IUnknown
```

<span data-ttu-id="54283-107">Вызывающий объект реализует этот интерфейс для получения события PermissionRequested.</span><span class="sxs-lookup"><span data-stu-id="54283-107">The caller implements this interface to receive the PermissionRequested event.</span></span>

## <span data-ttu-id="54283-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="54283-108">Summary</span></span>

 <span data-ttu-id="54283-109">Участников</span><span class="sxs-lookup"><span data-stu-id="54283-109">Members</span></span>                        | <span data-ttu-id="54283-110">Описания</span><span class="sxs-lookup"><span data-stu-id="54283-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="54283-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="54283-111">Invoke</span></span>](#invoke) | <span data-ttu-id="54283-112">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="54283-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="54283-113">Участников</span><span class="sxs-lookup"><span data-stu-id="54283-113">Members</span></span>

#### <span data-ttu-id="54283-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="54283-114">Invoke</span></span> 

<span data-ttu-id="54283-115">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="54283-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="54283-116">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2PermissionRequestedEventArgs](icorewebview2permissionrequestedeventargs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="54283-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* sender, [ICoreWebView2PermissionRequestedEventArgs](icorewebview2permissionrequestedeventargs.md) \* args)</span></span>

