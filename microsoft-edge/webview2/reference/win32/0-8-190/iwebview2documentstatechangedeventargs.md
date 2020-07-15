---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2DocumentStateChangedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 2ef38857b06c14eb9808452a33fa23b24855f055
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878563"
---
# <span data-ttu-id="33915-104">0.8.355-Interface IWebView2DocumentStateChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="33915-104">0.8.355 - interface IWebView2DocumentStateChangedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="33915-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="33915-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="33915-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="33915-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2DocumentStateChangedEventArgs
  : public IUnknown
```

<span data-ttu-id="33915-107">Аргументы события для события DocumentStateChanged.</span><span class="sxs-lookup"><span data-stu-id="33915-107">Event args for the DocumentStateChanged event.</span></span>

## <span data-ttu-id="33915-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="33915-108">Summary</span></span>

 <span data-ttu-id="33915-109">Участников</span><span class="sxs-lookup"><span data-stu-id="33915-109">Members</span></span>                        | <span data-ttu-id="33915-110">Описания</span><span class="sxs-lookup"><span data-stu-id="33915-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="33915-111">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="33915-111">get_IsNewDocument</span></span>](#get_isnewdocument) | <span data-ttu-id="33915-112">Значение true, если страница, на которую осуществляется переход, является новым документом.</span><span class="sxs-lookup"><span data-stu-id="33915-112">True if the page being navigated to is a new document.</span></span>
[<span data-ttu-id="33915-113">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="33915-113">get_IsErrorPage</span></span>](#get_iserrorpage) | <span data-ttu-id="33915-114">Значение true, если загруженное содержимое является страницей ошибки.</span><span class="sxs-lookup"><span data-stu-id="33915-114">True if the loaded content is an error page.</span></span>

## <span data-ttu-id="33915-115">Участников</span><span class="sxs-lookup"><span data-stu-id="33915-115">Members</span></span>

#### <span data-ttu-id="33915-116">get_IsNewDocument</span><span class="sxs-lookup"><span data-stu-id="33915-116">get_IsNewDocument</span></span> 

<span data-ttu-id="33915-117">Значение true, если страница, на которую осуществляется переход, является новым документом.</span><span class="sxs-lookup"><span data-stu-id="33915-117">True if the page being navigated to is a new document.</span></span>

> <span data-ttu-id="33915-118">общедоступные значения HRESULT [get_IsNewDocument](#get_isnewdocument)(bool \* IsNewDocument)</span><span class="sxs-lookup"><span data-stu-id="33915-118">public HRESULT [get_IsNewDocument](#get_isnewdocument)(BOOL \* isNewDocument)</span></span>

#### <span data-ttu-id="33915-119">get_IsErrorPage</span><span class="sxs-lookup"><span data-stu-id="33915-119">get_IsErrorPage</span></span> 

<span data-ttu-id="33915-120">Значение true, если загруженное содержимое является страницей ошибки.</span><span class="sxs-lookup"><span data-stu-id="33915-120">True if the loaded content is an error page.</span></span>

> <span data-ttu-id="33915-121">общедоступные значения HRESULT [get_IsErrorPage](#get_iserrorpage)(bool \* IsErrorPage)</span><span class="sxs-lookup"><span data-stu-id="33915-121">public HRESULT [get_IsErrorPage](#get_iserrorpage)(BOOL \* isErrorPage)</span></span>

