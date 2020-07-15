---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2DevToolsProtocolEventReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 0df2ea043a95c8cca24c0b9bbe3091c490b4ea3d
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878605"
---
# <span data-ttu-id="65f14-104">0.8.355-Interface IWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="65f14-104">0.8.355 - interface IWebView2DevToolsProtocolEventReceivedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="65f14-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="65f14-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="65f14-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="65f14-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2DevToolsProtocolEventReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="65f14-107">Аргументы события для события DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="65f14-107">Event args for the DevToolsProtocolEventReceived event.</span></span>

## <span data-ttu-id="65f14-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="65f14-108">Summary</span></span>

 <span data-ttu-id="65f14-109">Участников</span><span class="sxs-lookup"><span data-stu-id="65f14-109">Members</span></span>                        | <span data-ttu-id="65f14-110">Описания</span><span class="sxs-lookup"><span data-stu-id="65f14-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="65f14-111">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="65f14-111">get_ParameterObjectAsJson</span></span>](#get_parameterobjectasjson) | <span data-ttu-id="65f14-112">Объект параметра соответствующего события DevToolsProtocol, представленный в виде строки JSON.</span><span class="sxs-lookup"><span data-stu-id="65f14-112">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

## <span data-ttu-id="65f14-113">Участников</span><span class="sxs-lookup"><span data-stu-id="65f14-113">Members</span></span>

#### <span data-ttu-id="65f14-114">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="65f14-114">get_ParameterObjectAsJson</span></span> 

<span data-ttu-id="65f14-115">Объект параметра соответствующего события DevToolsProtocol, представленный в виде строки JSON.</span><span class="sxs-lookup"><span data-stu-id="65f14-115">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

> <span data-ttu-id="65f14-116">общедоступные значения HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* ParameterObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="65f14-116">public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* parameterObjectAsJson)</span></span>

