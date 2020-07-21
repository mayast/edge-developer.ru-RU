---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-WebView2 Win32 C++ ICoreWebView2DevToolsProtocolEventReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 2ed75f2a12387b6b8de628ac27ef536cf43fb8b1
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885410"
---
# <span data-ttu-id="8b790-104">0.9.515-Interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="8b790-104">0.9.515 - interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="8b790-105">Аргументы события для события DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="8b790-105">Event args for the DevToolsProtocolEventReceived event.</span></span>

## <span data-ttu-id="8b790-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="8b790-106">Summary</span></span>

 <span data-ttu-id="8b790-107">Участников</span><span class="sxs-lookup"><span data-stu-id="8b790-107">Members</span></span>                        | <span data-ttu-id="8b790-108">Описания</span><span class="sxs-lookup"><span data-stu-id="8b790-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8b790-109">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="8b790-109">get_ParameterObjectAsJson</span></span>](#get_parameterobjectasjson) | <span data-ttu-id="8b790-110">Объект параметра соответствующего события DevToolsProtocol, представленный в виде строки JSON.</span><span class="sxs-lookup"><span data-stu-id="8b790-110">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

## <span data-ttu-id="8b790-111">Участников</span><span class="sxs-lookup"><span data-stu-id="8b790-111">Members</span></span>

#### <span data-ttu-id="8b790-112">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="8b790-112">get_ParameterObjectAsJson</span></span> 

<span data-ttu-id="8b790-113">Объект параметра соответствующего события DevToolsProtocol, представленный в виде строки JSON.</span><span class="sxs-lookup"><span data-stu-id="8b790-113">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

> <span data-ttu-id="8b790-114">общедоступные значения HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* ParameterObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="8b790-114">public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* parameterObjectAsJson)</span></span>

