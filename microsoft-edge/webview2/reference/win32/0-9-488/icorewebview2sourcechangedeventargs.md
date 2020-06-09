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
ms.openlocfilehash: 8ea9437530a7f64cc045bfbaa1cc3cc55da77732
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698143"
---
# <span data-ttu-id="14ede-104">интерфейс ICoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="14ede-104">interface ICoreWebView2SourceChangedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="14ede-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="14ede-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="14ede-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="14ede-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="14ede-107">Аргументы события для события SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="14ede-107">Event args for the SourceChanged event.</span></span>

## <span data-ttu-id="14ede-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="14ede-108">Summary</span></span>

 <span data-ttu-id="14ede-109">Участников</span><span class="sxs-lookup"><span data-stu-id="14ede-109">Members</span></span>                        | <span data-ttu-id="14ede-110">Описания</span><span class="sxs-lookup"><span data-stu-id="14ede-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="14ede-111">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="14ede-111">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="14ede-112">Значение true, если страница, на которую осуществляется переход, является новым документом.</span><span class="sxs-lookup"><span data-stu-id="14ede-112">True if the page being navigated to is a new document.</span></span>

## <span data-ttu-id="14ede-113">Участников</span><span class="sxs-lookup"><span data-stu-id="14ede-113">Members</span></span>

#### <span data-ttu-id="14ede-114">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="14ede-114">get_IsNewDocument</span></span> 

<span data-ttu-id="14ede-115">Значение true, если страница, на которую осуществляется переход, является новым документом.</span><span class="sxs-lookup"><span data-stu-id="14ede-115">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="14ede-116">общедоступные значения HRESULT [get_IsNewDocument](#get_isnewdocument)(bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="14ede-116">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

