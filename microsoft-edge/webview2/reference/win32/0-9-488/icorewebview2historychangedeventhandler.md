---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 0305517d17bfa812dbaee9b238403f2d9f1fb22d
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697807"
---
# <span data-ttu-id="26263-104">интерфейс ICoreWebView2HistoryChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="26263-104">interface ICoreWebView2HistoryChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="26263-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="26263-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="26263-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="26263-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2HistoryChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="26263-107">Вызывающий объект реализует этот интерфейс для получения события HistoryChanged.</span><span class="sxs-lookup"><span data-stu-id="26263-107">The caller implements this interface to receive the HistoryChanged event.</span></span>

## <span data-ttu-id="26263-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="26263-108">Summary</span></span>

 <span data-ttu-id="26263-109">Участников</span><span class="sxs-lookup"><span data-stu-id="26263-109">Members</span></span>                        | <span data-ttu-id="26263-110">Описания</span><span class="sxs-lookup"><span data-stu-id="26263-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="26263-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="26263-111">Invoke</span></span>](#invoke) | <span data-ttu-id="26263-112">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="26263-112">There are no event args and the args parameter will be null.</span></span>

## <span data-ttu-id="26263-113">Участников</span><span class="sxs-lookup"><span data-stu-id="26263-113">Members</span></span>

#### <span data-ttu-id="26263-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="26263-114">Invoke</span></span> 

<span data-ttu-id="26263-115">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="26263-115">There are no event args and the args parameter will be null.</span></span>

> <span data-ttu-id="26263-116">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](icorewebview2.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="26263-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](icorewebview2.md) \* webview, IUnknown \* args)</span></span>

