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
ms.openlocfilehash: 4ae58375f0158a3876b284e16a579149dc6db9a5
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699253"
---
# <span data-ttu-id="14cdc-104">интерфейс ICoreWebView2SourceChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="14cdc-104">interface ICoreWebView2SourceChangedEventArgs</span></span> 

```
interface ICoreWebView2SourceChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="14cdc-105">Аргументы события для события SourceChanged.</span><span class="sxs-lookup"><span data-stu-id="14cdc-105">Event args for the SourceChanged event.</span></span>

## <span data-ttu-id="14cdc-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="14cdc-106">Summary</span></span>

 <span data-ttu-id="14cdc-107">Участников</span><span class="sxs-lookup"><span data-stu-id="14cdc-107">Members</span></span>                        | <span data-ttu-id="14cdc-108">Описания</span><span class="sxs-lookup"><span data-stu-id="14cdc-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="14cdc-109">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="14cdc-109">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="14cdc-110">Значение true, если страница, на которую осуществляется переход, является новым документом.</span><span class="sxs-lookup"><span data-stu-id="14cdc-110">True if the page being navigated to is a new document.</span></span>

## <span data-ttu-id="14cdc-111">Участников</span><span class="sxs-lookup"><span data-stu-id="14cdc-111">Members</span></span>

#### <span data-ttu-id="14cdc-112">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="14cdc-112">get_IsNewDocument</span></span> 

<span data-ttu-id="14cdc-113">Значение true, если страница, на которую осуществляется переход, является новым документом.</span><span class="sxs-lookup"><span data-stu-id="14cdc-113">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="14cdc-114">общедоступные значения HRESULT [get_IsNewDocument](#get_isnewdocument)(bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="14cdc-114">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

