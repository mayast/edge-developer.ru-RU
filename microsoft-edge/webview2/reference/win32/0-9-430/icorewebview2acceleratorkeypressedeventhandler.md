---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 8dfb39da070a5c43ce98057830f75f939e86f029
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654797"
---
# <span data-ttu-id="8504e-104">интерфейс ICoreWebView2AcceleratorKeyPressedEventHandler</span><span class="sxs-lookup"><span data-stu-id="8504e-104">interface ICoreWebView2AcceleratorKeyPressedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="8504e-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="8504e-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="8504e-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="8504e-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2AcceleratorKeyPressedEventHandler
  : public IUnknown
```

<span data-ttu-id="8504e-107">Вызывающий объект реализует этот интерфейс для получения события AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="8504e-107">The caller implements this interface to receive the AcceleratorKeyPressed event.</span></span>

## <span data-ttu-id="8504e-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="8504e-108">Summary</span></span>

 <span data-ttu-id="8504e-109">Участников</span><span class="sxs-lookup"><span data-stu-id="8504e-109">Members</span></span>                        | <span data-ttu-id="8504e-110">Описания</span><span class="sxs-lookup"><span data-stu-id="8504e-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8504e-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="8504e-111">Invoke</span></span>](#invoke) | <span data-ttu-id="8504e-112">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="8504e-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="8504e-113">Участников</span><span class="sxs-lookup"><span data-stu-id="8504e-113">Members</span></span>

#### <span data-ttu-id="8504e-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="8504e-114">Invoke</span></span> 

<span data-ttu-id="8504e-115">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="8504e-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="8504e-116">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2Host](ICoreWebView2Host.md) \* sender,[ICoreWebView2AcceleratorKeyPressedEventArgs](ICoreWebView2AcceleratorKeyPressedEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="8504e-116">public HRESULT [Invoke](#invoke)([ICoreWebView2Host](ICoreWebView2Host.md) \* sender,[ICoreWebView2AcceleratorKeyPressedEventArgs](ICoreWebView2AcceleratorKeyPressedEventArgs.md) \* args)</span></span>

