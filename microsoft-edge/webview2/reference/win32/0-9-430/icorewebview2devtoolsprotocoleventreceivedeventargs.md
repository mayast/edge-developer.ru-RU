---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2DevToolsProtocolEventReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 3fdbe4d978a6a703576dd1135f7b79efad1befa5
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881097"
---
# <span data-ttu-id="b1888-104">0.9.430-Interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="b1888-104">0.9.430 - interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="b1888-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="b1888-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="b1888-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="b1888-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="b1888-107">Аргументы события для события DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="b1888-107">Event args for the DevToolsProtocolEventReceived event.</span></span>

## <span data-ttu-id="b1888-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="b1888-108">Summary</span></span>

 <span data-ttu-id="b1888-109">Участников</span><span class="sxs-lookup"><span data-stu-id="b1888-109">Members</span></span>                        | <span data-ttu-id="b1888-110">Описания</span><span class="sxs-lookup"><span data-stu-id="b1888-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b1888-111">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="b1888-111">get_ParameterObjectAsJson</span></span>](#get_parameterobjectasjson) | <span data-ttu-id="b1888-112">Объект параметра соответствующего события DevToolsProtocol, представленный в виде строки JSON.</span><span class="sxs-lookup"><span data-stu-id="b1888-112">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

## <span data-ttu-id="b1888-113">Участников</span><span class="sxs-lookup"><span data-stu-id="b1888-113">Members</span></span>

#### <span data-ttu-id="b1888-114">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="b1888-114">get_ParameterObjectAsJson</span></span> 

<span data-ttu-id="b1888-115">Объект параметра соответствующего события DevToolsProtocol, представленный в виде строки JSON.</span><span class="sxs-lookup"><span data-stu-id="b1888-115">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

> <span data-ttu-id="b1888-116">общедоступные значения HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* ParameterObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="b1888-116">public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* parameterObjectAsJson)</span></span>

