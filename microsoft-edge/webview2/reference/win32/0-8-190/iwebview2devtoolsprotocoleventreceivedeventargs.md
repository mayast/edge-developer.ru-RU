---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2DevToolsProtocolEventReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 920d95b737a15926e6de33cfed0ee9a98eeade78
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886161"
---
# <span data-ttu-id="4ff99-104">0.8.355-Interface IWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="4ff99-104">0.8.355 - interface IWebView2DevToolsProtocolEventReceivedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2DevToolsProtocolEventReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="4ff99-105">Аргументы события для события DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="4ff99-105">Event args for the DevToolsProtocolEventReceived event.</span></span>

## <span data-ttu-id="4ff99-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="4ff99-106">Summary</span></span>

 <span data-ttu-id="4ff99-107">Участников</span><span class="sxs-lookup"><span data-stu-id="4ff99-107">Members</span></span>                        | <span data-ttu-id="4ff99-108">Описания</span><span class="sxs-lookup"><span data-stu-id="4ff99-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4ff99-109">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="4ff99-109">get_ParameterObjectAsJson</span></span>](#get_parameterobjectasjson) | <span data-ttu-id="4ff99-110">Объект параметра соответствующего события DevToolsProtocol, представленный в виде строки JSON.</span><span class="sxs-lookup"><span data-stu-id="4ff99-110">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

## <span data-ttu-id="4ff99-111">Участников</span><span class="sxs-lookup"><span data-stu-id="4ff99-111">Members</span></span>

#### <span data-ttu-id="4ff99-112">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="4ff99-112">get_ParameterObjectAsJson</span></span> 

<span data-ttu-id="4ff99-113">Объект параметра соответствующего события DevToolsProtocol, представленный в виде строки JSON.</span><span class="sxs-lookup"><span data-stu-id="4ff99-113">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

> <span data-ttu-id="4ff99-114">общедоступные значения HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* ParameterObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="4ff99-114">public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* parameterObjectAsJson)</span></span>

