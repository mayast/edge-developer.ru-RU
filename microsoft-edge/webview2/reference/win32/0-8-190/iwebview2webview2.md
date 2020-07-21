---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 64dac6c56576b618cbdc84da2c8fcbcd0e41028f
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884738"
---
# <span data-ttu-id="096cd-104">0.8.355-Interface IWebView2WebView2</span><span class="sxs-lookup"><span data-stu-id="096cd-104">0.8.355 - interface IWebView2WebView2</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebView2
  : public IUnknown
```

<span data-ttu-id="096cd-105">Дополнительные функции, реализованные основным объектом WebView.</span><span class="sxs-lookup"><span data-stu-id="096cd-105">Additional functionality implemented by the primary WebView object.</span></span>

## <span data-ttu-id="096cd-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="096cd-106">Summary</span></span>

 <span data-ttu-id="096cd-107">Участников</span><span class="sxs-lookup"><span data-stu-id="096cd-107">Members</span></span>                        | <span data-ttu-id="096cd-108">Описания</span><span class="sxs-lookup"><span data-stu-id="096cd-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="096cd-109">Stop</span><span class="sxs-lookup"><span data-stu-id="096cd-109">Stop</span></span>](#stop) | <span data-ttu-id="096cd-110">Остановите все переходы и ожидающие выборки ресурсов.</span><span class="sxs-lookup"><span data-stu-id="096cd-110">Stop all navigations and pending resource fetches.</span></span>

<span data-ttu-id="096cd-111">Вы можете QueryInterface для этого интерфейса из объекта, реализующего [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="096cd-111">You can QueryInterface for this interface from the object that implements [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="096cd-112">Дополнительные сведения вы видите в интерфейсе [IWebView2WebView](IWebView2WebView.md) .</span><span class="sxs-lookup"><span data-stu-id="096cd-112">See the [IWebView2WebView](IWebView2WebView.md) interface for more details.</span></span>

## <span data-ttu-id="096cd-113">Участников</span><span class="sxs-lookup"><span data-stu-id="096cd-113">Members</span></span>

#### <span data-ttu-id="096cd-114">Stop</span><span class="sxs-lookup"><span data-stu-id="096cd-114">Stop</span></span> 

<span data-ttu-id="096cd-115">Остановите все переходы и ожидающие выборки ресурсов.</span><span class="sxs-lookup"><span data-stu-id="096cd-115">Stop all navigations and pending resource fetches.</span></span>

> <span data-ttu-id="096cd-116">открытая [Остановка](#stop)HRESULT ()</span><span class="sxs-lookup"><span data-stu-id="096cd-116">public HRESULT [Stop](#stop)()</span></span>

