---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2DevToolsProtocolEventReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/09/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2DevToolsProtocolEventReceivedEventArgs
ms.openlocfilehash: 079b7840689fbeb2931a22f72ad78c1ce0f590b8
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012569"
---
# <span data-ttu-id="52b67-104">интерфейс ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="52b67-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span></span> 

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="52b67-105">Аргументы события для события DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="52b67-105">Event args for the DevToolsProtocolEventReceived event.</span></span>

## <span data-ttu-id="52b67-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="52b67-106">Summary</span></span>

 <span data-ttu-id="52b67-107">Участников</span><span class="sxs-lookup"><span data-stu-id="52b67-107">Members</span></span>                        | <span data-ttu-id="52b67-108">Описания</span><span class="sxs-lookup"><span data-stu-id="52b67-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="52b67-109">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="52b67-109">get_ParameterObjectAsJson</span></span>](#get_parameterobjectasjson) | <span data-ttu-id="52b67-110">Объект параметра соответствующего события DevToolsProtocol, представленный в виде строки JSON.</span><span class="sxs-lookup"><span data-stu-id="52b67-110">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

## <span data-ttu-id="52b67-111">Участников</span><span class="sxs-lookup"><span data-stu-id="52b67-111">Members</span></span>

#### <span data-ttu-id="52b67-112">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="52b67-112">get_ParameterObjectAsJson</span></span> 

<span data-ttu-id="52b67-113">Объект параметра соответствующего события DevToolsProtocol, представленный в виде строки JSON.</span><span class="sxs-lookup"><span data-stu-id="52b67-113">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

> <span data-ttu-id="52b67-114">общедоступные значения HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* ParameterObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="52b67-114">public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* parameterObjectAsJson)</span></span>

