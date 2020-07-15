---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2Environment2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: d127af61bfdc9bf692fa48489d7982bf2c6cad86
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878549"
---
# <span data-ttu-id="cbc47-104">0.8.355-Interface IWebView2Environment2</span><span class="sxs-lookup"><span data-stu-id="cbc47-104">0.8.355 - interface IWebView2Environment2</span></span> 

> [!NOTE]
> <span data-ttu-id="cbc47-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="cbc47-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="cbc47-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="cbc47-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2Environment2
  : public IWebView2Environment
```

<span data-ttu-id="cbc47-107">Дополнительные функции, реализованные с помощью объекта Environment.</span><span class="sxs-lookup"><span data-stu-id="cbc47-107">Additional functionality implemented by the Environment object.</span></span>

## <span data-ttu-id="cbc47-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="cbc47-108">Summary</span></span>

 <span data-ttu-id="cbc47-109">Участников</span><span class="sxs-lookup"><span data-stu-id="cbc47-109">Members</span></span>                        | <span data-ttu-id="cbc47-110">Описания</span><span class="sxs-lookup"><span data-stu-id="cbc47-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="cbc47-111">get_BrowserVersionInfo</span><span class="sxs-lookup"><span data-stu-id="cbc47-111">get_BrowserVersionInfo</span></span>](#get_browserversioninfo) | <span data-ttu-id="cbc47-112">Сведения о версии браузера для текущего [IWebView2Environment](IWebView2Environment.md), включая имя канала, если он не является стабильным каналом.</span><span class="sxs-lookup"><span data-stu-id="cbc47-112">The browser version info of the current [IWebView2Environment](IWebView2Environment.md), including channel name if it is not the stable channel.</span></span>

<span data-ttu-id="cbc47-113">Дополнительные сведения вы видите в интерфейсе [IWebView2Environment](IWebView2Environment.md) .</span><span class="sxs-lookup"><span data-stu-id="cbc47-113">See the [IWebView2Environment](IWebView2Environment.md) interface for more details.</span></span> <span data-ttu-id="cbc47-114">Вы можете QueryInterface для этого интерфейса из объекта, реализующего [IWebView2Environment](IWebView2Environment.md).</span><span class="sxs-lookup"><span data-stu-id="cbc47-114">You can QueryInterface for this interface from the object that implements [IWebView2Environment](IWebView2Environment.md).</span></span>

## <span data-ttu-id="cbc47-115">Участников</span><span class="sxs-lookup"><span data-stu-id="cbc47-115">Members</span></span>

#### <span data-ttu-id="cbc47-116">get_BrowserVersionInfo</span><span class="sxs-lookup"><span data-stu-id="cbc47-116">get_BrowserVersionInfo</span></span> 

<span data-ttu-id="cbc47-117">Сведения о версии браузера для текущего [IWebView2Environment](IWebView2Environment.md), включая имя канала, если он не является стабильным каналом.</span><span class="sxs-lookup"><span data-stu-id="cbc47-117">The browser version info of the current [IWebView2Environment](IWebView2Environment.md), including channel name if it is not the stable channel.</span></span>

> <span data-ttu-id="cbc47-118">общедоступные значения HRESULT [get_BrowserVersionInfo](#get_browserversioninfo)(LPWSTR \* versionInfo)</span><span class="sxs-lookup"><span data-stu-id="cbc47-118">public HRESULT [get_BrowserVersionInfo](#get_browserversioninfo)(LPWSTR \* versionInfo)</span></span>

<span data-ttu-id="cbc47-119">Это соответствует формату API GetWebView2BrowserVersionInfo.</span><span class="sxs-lookup"><span data-stu-id="cbc47-119">This matches the format of the GetWebView2BrowserVersionInfo API.</span></span> <span data-ttu-id="cbc47-120">Названия каналов: "бета-версия", "Dev" и "Канарские".</span><span class="sxs-lookup"><span data-stu-id="cbc47-120">Channel names are 'beta', 'dev', and 'canary'.</span></span>

```cpp
        wil::unique_cotaskmem_string version_info;
        m_webViewEnvironment->get_BrowserVersionInfo(&version_info);
        MessageBox(
            m_mainWindow, version_info.get(), L"Browser Version Info After WebView Creation",
            MB_OK);
```

