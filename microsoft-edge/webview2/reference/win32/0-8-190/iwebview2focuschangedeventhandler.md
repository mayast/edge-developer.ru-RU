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
ms.openlocfilehash: 23cce166d4ef2d05b6ffe5814c1568f75a72be0e
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654691"
---
# <span data-ttu-id="04655-104">интерфейс IWebView2FocusChangedEventHandler</span><span class="sxs-lookup"><span data-stu-id="04655-104">interface IWebView2FocusChangedEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="04655-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="04655-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="04655-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="04655-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2FocusChangedEventHandler
  : public IUnknown
```

<span data-ttu-id="04655-107">Вызывающий объект реализует этот метод для получения событий GotFocus и LostFocus.</span><span class="sxs-lookup"><span data-stu-id="04655-107">The caller implements this method to receive the GotFocus and LostFocus events.</span></span>

## <span data-ttu-id="04655-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="04655-108">Summary</span></span>

 <span data-ttu-id="04655-109">Участников</span><span class="sxs-lookup"><span data-stu-id="04655-109">Members</span></span>                        | <span data-ttu-id="04655-110">Описания</span><span class="sxs-lookup"><span data-stu-id="04655-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="04655-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="04655-111">Invoke</span></span>](#invoke) | <span data-ttu-id="04655-112">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="04655-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

<span data-ttu-id="04655-113">Аргументы события для этого события отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="04655-113">There are no event args for this event.</span></span>

## <span data-ttu-id="04655-114">Участников</span><span class="sxs-lookup"><span data-stu-id="04655-114">Members</span></span>

#### <span data-ttu-id="04655-115">Invoke</span><span class="sxs-lookup"><span data-stu-id="04655-115">Invoke</span></span> 

<span data-ttu-id="04655-116">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="04655-116">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="04655-117">Открытый [вызов](#invoke)HRESULT ([IWebView2WebView](IWebView2WebView.md) \* WebView, IUnknown \* args)</span><span class="sxs-lookup"><span data-stu-id="04655-117">public HRESULT [Invoke](#invoke)([IWebView2WebView](IWebView2WebView.md) \* webview,IUnknown \* args)</span></span>

<span data-ttu-id="04655-118">Аргументы события отсутствуют, а параметр args — null.</span><span class="sxs-lookup"><span data-stu-id="04655-118">There are no event args and the args parameter will be null.</span></span>

