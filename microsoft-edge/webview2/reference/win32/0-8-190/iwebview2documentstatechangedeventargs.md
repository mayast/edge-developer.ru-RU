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
ms.openlocfilehash: 342716da2cded9c903f1edd13fb3400c779a9b39
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654862"
---
# <span data-ttu-id="30018-104">интерфейс IWebView2DocumentStateChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="30018-104">interface IWebView2DocumentStateChangedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="30018-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="30018-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="30018-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="30018-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2DocumentStateChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="30018-107">Аргументы события для события DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="30018-107">Event args for the DocumentStateChanged event.</span></span>

## <span data-ttu-id="30018-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="30018-108">Summary</span></span>

 <span data-ttu-id="30018-109">Участников</span><span class="sxs-lookup"><span data-stu-id="30018-109">Members</span></span>                        | <span data-ttu-id="30018-110">Описания</span><span class="sxs-lookup"><span data-stu-id="30018-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="30018-111">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="30018-111">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="30018-112">Значение true, если страница, на которую осуществляется переход, является новым документом.</span><span class="sxs-lookup"><span data-stu-id="30018-112">True if the page being navigated to is a new document.</span></span>
[<span data-ttu-id="30018-113">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="30018-113">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="30018-114">Значение true, если загруженное содержимое является страницей ошибки.</span><span class="sxs-lookup"><span data-stu-id="30018-114">True if the loaded content is an error page.</span></span>

## <span data-ttu-id="30018-115">Участников</span><span class="sxs-lookup"><span data-stu-id="30018-115">Members</span></span>

#### <span data-ttu-id="30018-116">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="30018-116">get_IsNewDocument</span></span> 

<span data-ttu-id="30018-117">Значение true, если страница, на которую осуществляется переход, является новым документом.</span><span class="sxs-lookup"><span data-stu-id="30018-117">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="30018-118">общедоступные значения HRESULT [get_IsNewDocument](#get_isnewdocument)(bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="30018-118">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

#### <span data-ttu-id="30018-119">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="30018-119">get_IsErrorPage</span></span> 

<span data-ttu-id="30018-120">Значение true, если загруженное содержимое является страницей ошибки.</span><span class="sxs-lookup"><span data-stu-id="30018-120">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="30018-121">общедоступные значения HRESULT [get_IsErrorPage](#get_iserrorpage)(bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="30018-121">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

