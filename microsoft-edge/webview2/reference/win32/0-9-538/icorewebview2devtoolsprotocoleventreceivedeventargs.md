---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2DevToolsProtocolEventReceivedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2DevToolsProtocolEventReceivedEventArgs
ms.openlocfilehash: de10adbfe7e74a1679aa8b77cb96775561d87a17
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880131"
---
# <span data-ttu-id="34838-104">интерфейс ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="34838-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span></span> 

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="34838-105">Аргументы события для события DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="34838-105">Event args for the DevToolsProtocolEventReceived event.</span></span>

## <span data-ttu-id="34838-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="34838-106">Summary</span></span>

 <span data-ttu-id="34838-107">Участников</span><span class="sxs-lookup"><span data-stu-id="34838-107">Members</span></span>                        | <span data-ttu-id="34838-108">Описания</span><span class="sxs-lookup"><span data-stu-id="34838-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="34838-109">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="34838-109">get_ParameterObjectAsJson</span></span>](#get_parameterobjectasjson) | <span data-ttu-id="34838-110">Объект параметра соответствующего события DevToolsProtocol, представленный в виде строки JSON.</span><span class="sxs-lookup"><span data-stu-id="34838-110">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

## <span data-ttu-id="34838-111">Участников</span><span class="sxs-lookup"><span data-stu-id="34838-111">Members</span></span>

#### <span data-ttu-id="34838-112">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="34838-112">get_ParameterObjectAsJson</span></span> 

<span data-ttu-id="34838-113">Объект параметра соответствующего события DevToolsProtocol, представленный в виде строки JSON.</span><span class="sxs-lookup"><span data-stu-id="34838-113">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

> <span data-ttu-id="34838-114">общедоступные значения HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* ParameterObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="34838-114">public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* parameterObjectAsJson)</span></span>

