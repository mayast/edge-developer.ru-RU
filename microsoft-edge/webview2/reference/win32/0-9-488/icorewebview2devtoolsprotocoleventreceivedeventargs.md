---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/16/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: e7fbc952a44bdd38e6e59c46adafb8e71b7904b6
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654891"
---
# <span data-ttu-id="10dec-104">интерфейс ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="10dec-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span></span> 

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="10dec-105">Аргументы события для события DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="10dec-105">Event args for the DevToolsProtocolEventReceived event.</span></span>

## <span data-ttu-id="10dec-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="10dec-106">Summary</span></span>

 <span data-ttu-id="10dec-107">Участников</span><span class="sxs-lookup"><span data-stu-id="10dec-107">Members</span></span>                        | <span data-ttu-id="10dec-108">Описания</span><span class="sxs-lookup"><span data-stu-id="10dec-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="10dec-109">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="10dec-109">get_ParameterObjectAsJson</span></span>](#get_parameterobjectasjson) | <span data-ttu-id="10dec-110">Объект параметра соответствующего события DevToolsProtocol, представленный в виде строки JSON.</span><span class="sxs-lookup"><span data-stu-id="10dec-110">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

## <span data-ttu-id="10dec-111">Участников</span><span class="sxs-lookup"><span data-stu-id="10dec-111">Members</span></span>

#### <span data-ttu-id="10dec-112">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="10dec-112">get_ParameterObjectAsJson</span></span> 

<span data-ttu-id="10dec-113">Объект параметра соответствующего события DevToolsProtocol, представленный в виде строки JSON.</span><span class="sxs-lookup"><span data-stu-id="10dec-113">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

> <span data-ttu-id="10dec-114">общедоступные значения HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* ParameterObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="10dec-114">public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* parameterObjectAsJson)</span></span>

