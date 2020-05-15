---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 3ac37f7d90fc03214381b991c8becae602bac738
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654857"
---
# <span data-ttu-id="13a25-104">интерфейс ICoreWebView2NewBrowserVersionAvailableEventArgs</span><span class="sxs-lookup"><span data-stu-id="13a25-104">interface ICoreWebView2NewBrowserVersionAvailableEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="13a25-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="13a25-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="13a25-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="13a25-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2NewBrowserVersionAvailableEventArgs
  : public IUnknown
```

<span data-ttu-id="13a25-107">Аргументы события для события NewBrowserVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="13a25-107">Event args for the NewBrowserVersionAvailable event.</span></span>

## <span data-ttu-id="13a25-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="13a25-108">Summary</span></span>

 <span data-ttu-id="13a25-109">Участников</span><span class="sxs-lookup"><span data-stu-id="13a25-109">Members</span></span>                        | <span data-ttu-id="13a25-110">Описания</span><span class="sxs-lookup"><span data-stu-id="13a25-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="13a25-111">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="13a25-111">get_NewVersion</span></span>](#get_newversion) | <span data-ttu-id="13a25-112">Сведения о версии браузера для текущего [ICoreWebView2Environment](ICoreWebView2Environment.md).</span><span class="sxs-lookup"><span data-stu-id="13a25-112">The browser version info of the current [ICoreWebView2Environment](ICoreWebView2Environment.md).</span></span>

## <span data-ttu-id="13a25-113">Участников</span><span class="sxs-lookup"><span data-stu-id="13a25-113">Members</span></span>

#### <span data-ttu-id="13a25-114">get_NewVersion</span><span class="sxs-lookup"><span data-stu-id="13a25-114">get_NewVersion</span></span> 

<span data-ttu-id="13a25-115">Сведения о версии браузера для текущего [ICoreWebView2Environment](ICoreWebView2Environment.md).</span><span class="sxs-lookup"><span data-stu-id="13a25-115">The browser version info of the current [ICoreWebView2Environment](ICoreWebView2Environment.md).</span></span>

> <span data-ttu-id="13a25-116">общедоступные значения HRESULT [get_NewVersion](#get_newversion)(LPWSTR \* NewVersion)</span><span class="sxs-lookup"><span data-stu-id="13a25-116">public HRESULT [get_NewVersion](#get_newversion)(LPWSTR \* newVersion)</span></span>

