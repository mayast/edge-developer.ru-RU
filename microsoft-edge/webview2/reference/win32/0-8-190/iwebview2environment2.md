---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2Environment2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: e3177f159ff397ee9d4781936aa32f2715d4af02
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886089"
---
# <span data-ttu-id="8c87f-104">0.8.355-Interface IWebView2Environment2</span><span class="sxs-lookup"><span data-stu-id="8c87f-104">0.8.355 - interface IWebView2Environment2</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2Environment2
  : public IWebView2Environment
```

<span data-ttu-id="8c87f-105">Дополнительные функции, реализованные с помощью объекта Environment.</span><span class="sxs-lookup"><span data-stu-id="8c87f-105">Additional functionality implemented by the Environment object.</span></span>

## <span data-ttu-id="8c87f-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="8c87f-106">Summary</span></span>

 <span data-ttu-id="8c87f-107">Участников</span><span class="sxs-lookup"><span data-stu-id="8c87f-107">Members</span></span>                        | <span data-ttu-id="8c87f-108">Описания</span><span class="sxs-lookup"><span data-stu-id="8c87f-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="8c87f-109">get_BrowserVersionInfo</span><span class="sxs-lookup"><span data-stu-id="8c87f-109">get_BrowserVersionInfo</span></span>](#get_browserversioninfo) | <span data-ttu-id="8c87f-110">Сведения о версии браузера для текущего [IWebView2Environment](IWebView2Environment.md), включая имя канала, если он не является стабильным каналом.</span><span class="sxs-lookup"><span data-stu-id="8c87f-110">The browser version info of the current [IWebView2Environment](IWebView2Environment.md), including channel name if it is not the stable channel.</span></span>

<span data-ttu-id="8c87f-111">Дополнительные сведения вы видите в интерфейсе [IWebView2Environment](IWebView2Environment.md) .</span><span class="sxs-lookup"><span data-stu-id="8c87f-111">See the [IWebView2Environment](IWebView2Environment.md) interface for more details.</span></span> <span data-ttu-id="8c87f-112">Вы можете QueryInterface для этого интерфейса из объекта, реализующего [IWebView2Environment](IWebView2Environment.md).</span><span class="sxs-lookup"><span data-stu-id="8c87f-112">You can QueryInterface for this interface from the object that implements [IWebView2Environment](IWebView2Environment.md).</span></span>

## <span data-ttu-id="8c87f-113">Участников</span><span class="sxs-lookup"><span data-stu-id="8c87f-113">Members</span></span>

#### <span data-ttu-id="8c87f-114">get_BrowserVersionInfo</span><span class="sxs-lookup"><span data-stu-id="8c87f-114">get_BrowserVersionInfo</span></span> 

<span data-ttu-id="8c87f-115">Сведения о версии браузера для текущего [IWebView2Environment](IWebView2Environment.md), включая имя канала, если он не является стабильным каналом.</span><span class="sxs-lookup"><span data-stu-id="8c87f-115">The browser version info of the current [IWebView2Environment](IWebView2Environment.md), including channel name if it is not the stable channel.</span></span>

> <span data-ttu-id="8c87f-116">общедоступные значения HRESULT [get_BrowserVersionInfo](#get_browserversioninfo)(LPWSTR \* versionInfo)</span><span class="sxs-lookup"><span data-stu-id="8c87f-116">public HRESULT [get_BrowserVersionInfo](#get_browserversioninfo)(LPWSTR \* versionInfo)</span></span>

<span data-ttu-id="8c87f-117">Это соответствует формату API GetWebView2BrowserVersionInfo.</span><span class="sxs-lookup"><span data-stu-id="8c87f-117">This matches the format of the GetWebView2BrowserVersionInfo API.</span></span> <span data-ttu-id="8c87f-118">Названия каналов: "бета-версия", "Dev" и "Канарские".</span><span class="sxs-lookup"><span data-stu-id="8c87f-118">Channel names are 'beta', 'dev', and 'canary'.</span></span>

```cpp
        wil::unique_cotaskmem_string version_info;
        m_webViewEnvironment->get_BrowserVersionInfo(&version_info);
        MessageBox(
            m_mainWindow, version_info.get(), L"Browser Version Info After WebView Creation",
            MB_OK);
```

