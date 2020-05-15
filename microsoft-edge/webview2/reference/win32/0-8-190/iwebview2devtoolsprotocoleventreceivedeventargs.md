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
ms.openlocfilehash: cf321ff1091883827b7ce6cda7248a06f1128867
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654868"
---
# <span data-ttu-id="e5d3c-104">интерфейс IWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="e5d3c-104">interface IWebView2DevToolsProtocolEventReceivedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="e5d3c-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="e5d3c-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="e5d3c-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="e5d3c-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2DevToolsProtocolEventReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="e5d3c-107">Аргументы события для события DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="e5d3c-107">Event args for the DevToolsProtocolEventReceived event.</span></span>

## <span data-ttu-id="e5d3c-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="e5d3c-108">Summary</span></span>

 <span data-ttu-id="e5d3c-109">Участников</span><span class="sxs-lookup"><span data-stu-id="e5d3c-109">Members</span></span>                        | <span data-ttu-id="e5d3c-110">Описания</span><span class="sxs-lookup"><span data-stu-id="e5d3c-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e5d3c-111">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="e5d3c-111">get_ParameterObjectAsJson</span></span>](#get_parameterobjectasjson) | <span data-ttu-id="e5d3c-112">Объект параметра соответствующего события DevToolsProtocol, представленный в виде строки JSON.</span><span class="sxs-lookup"><span data-stu-id="e5d3c-112">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

## <span data-ttu-id="e5d3c-113">Участников</span><span class="sxs-lookup"><span data-stu-id="e5d3c-113">Members</span></span>

#### <span data-ttu-id="e5d3c-114">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="e5d3c-114">get_ParameterObjectAsJson</span></span> 

<span data-ttu-id="e5d3c-115">Объект параметра соответствующего события DevToolsProtocol, представленный в виде строки JSON.</span><span class="sxs-lookup"><span data-stu-id="e5d3c-115">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

> <span data-ttu-id="e5d3c-116">общедоступные значения HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* ParameterObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="e5d3c-116">public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* parameterObjectAsJson)</span></span>

