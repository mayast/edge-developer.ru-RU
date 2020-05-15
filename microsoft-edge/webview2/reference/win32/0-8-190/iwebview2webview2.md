---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 62daeaab702b431f787bc800ab79664fc183c4ce
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654614"
---
# <span data-ttu-id="54aae-104">интерфейс IWebView2WebView2</span><span class="sxs-lookup"><span data-stu-id="54aae-104">interface IWebView2WebView2</span></span> 

> [!NOTE]
> <span data-ttu-id="54aae-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="54aae-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="54aae-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="54aae-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebView2
  : public IUnknown
```

<span data-ttu-id="54aae-107">Дополнительные функции, реализованные основным объектом WebView.</span><span class="sxs-lookup"><span data-stu-id="54aae-107">Additional functionality implemented by the primary WebView object.</span></span>

## <span data-ttu-id="54aae-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="54aae-108">Summary</span></span>

 <span data-ttu-id="54aae-109">Участников</span><span class="sxs-lookup"><span data-stu-id="54aae-109">Members</span></span>                        | <span data-ttu-id="54aae-110">Описания</span><span class="sxs-lookup"><span data-stu-id="54aae-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="54aae-111">Stop</span><span class="sxs-lookup"><span data-stu-id="54aae-111">Stop</span></span>](#stop) | <span data-ttu-id="54aae-112">Остановите все переходы и ожидающие выборки ресурсов.</span><span class="sxs-lookup"><span data-stu-id="54aae-112">Stop all navigations and pending resource fetches.</span></span>

<span data-ttu-id="54aae-113">Вы можете QueryInterface для этого интерфейса из объекта, реализующего [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="54aae-113">You can QueryInterface for this interface from the object that implements [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="54aae-114">Дополнительные сведения вы видите в интерфейсе [IWebView2WebView](IWebView2WebView.md) .</span><span class="sxs-lookup"><span data-stu-id="54aae-114">See the [IWebView2WebView](IWebView2WebView.md) interface for more details.</span></span>

## <span data-ttu-id="54aae-115">Участников</span><span class="sxs-lookup"><span data-stu-id="54aae-115">Members</span></span>

#### <span data-ttu-id="54aae-116">Stop</span><span class="sxs-lookup"><span data-stu-id="54aae-116">Stop</span></span> 

<span data-ttu-id="54aae-117">Остановите все переходы и ожидающие выборки ресурсов.</span><span class="sxs-lookup"><span data-stu-id="54aae-117">Stop all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="54aae-118">открытая [Остановка](#stop)HRESULT ()</span><span class="sxs-lookup"><span data-stu-id="54aae-118">public HRESULT [Stop](#stop)()</span></span>

