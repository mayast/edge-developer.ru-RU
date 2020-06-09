---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 2429c519858aa9c55e52d47bea64fc182b6beb73
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699189"
---
# <span data-ttu-id="0aa42-104">интерфейс ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span><span class="sxs-lookup"><span data-stu-id="0aa42-104">interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs</span></span> 

```
interface ICoreWebView2DevToolsProtocolEventReceivedEventArgs
  : public IUnknown
```

<span data-ttu-id="0aa42-105">Аргументы события для события DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="0aa42-105">Event args for the DevToolsProtocolEventReceived event.</span></span>

## <span data-ttu-id="0aa42-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="0aa42-106">Summary</span></span>

 <span data-ttu-id="0aa42-107">Участников</span><span class="sxs-lookup"><span data-stu-id="0aa42-107">Members</span></span>                        | <span data-ttu-id="0aa42-108">Описания</span><span class="sxs-lookup"><span data-stu-id="0aa42-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="0aa42-109">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="0aa42-109">get_ParameterObjectAsJson</span></span>](#get_parameterobjectasjson) | <span data-ttu-id="0aa42-110">Объект параметра соответствующего события DevToolsProtocol, представленный в виде строки JSON.</span><span class="sxs-lookup"><span data-stu-id="0aa42-110">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

## <span data-ttu-id="0aa42-111">Участников</span><span class="sxs-lookup"><span data-stu-id="0aa42-111">Members</span></span>

#### <span data-ttu-id="0aa42-112">get_ParameterObjectAsJson</span><span class="sxs-lookup"><span data-stu-id="0aa42-112">get_ParameterObjectAsJson</span></span> 

<span data-ttu-id="0aa42-113">Объект параметра соответствующего события DevToolsProtocol, представленный в виде строки JSON.</span><span class="sxs-lookup"><span data-stu-id="0aa42-113">The parameter object of the corresponding DevToolsProtocol event represented as a JSON string.</span></span>

> <span data-ttu-id="0aa42-114">общедоступные значения HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* ParameterObjectAsJson)</span><span class="sxs-lookup"><span data-stu-id="0aa42-114">public HRESULT [get_ParameterObjectAsJson](#get_parameterobjectasjson)(LPWSTR \* parameterObjectAsJson)</span></span>

