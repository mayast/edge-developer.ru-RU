---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2MoveFocusRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 5d8d447bced6bbbb51ae33220e74ebcf47f11ce5
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885929"
---
# <span data-ttu-id="41b0a-104">0.8.355-Interface IWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="41b0a-104">0.8.355 - interface IWebView2MoveFocusRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2MoveFocusRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="41b0a-105">Аргументы события для события MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="41b0a-105">Event args for the MoveFocusRequested event.</span></span>

## <span data-ttu-id="41b0a-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="41b0a-106">Summary</span></span>

 <span data-ttu-id="41b0a-107">Участников</span><span class="sxs-lookup"><span data-stu-id="41b0a-107">Members</span></span>                        | <span data-ttu-id="41b0a-108">Описания</span><span class="sxs-lookup"><span data-stu-id="41b0a-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="41b0a-109">get_Reason</span><span class="sxs-lookup"><span data-stu-id="41b0a-109">get_Reason</span></span>](#get_reason) | <span data-ttu-id="41b0a-110">Причина, по которой WebView запускает событие "MoveFocus".</span><span class="sxs-lookup"><span data-stu-id="41b0a-110">The reason for WebView to fire the MoveFocus Requested event.</span></span>
[<span data-ttu-id="41b0a-111">get_Handled</span><span class="sxs-lookup"><span data-stu-id="41b0a-111">get_Handled</span></span>](#get_handled) | <span data-ttu-id="41b0a-112">Указывает, было ли событие обработано приложением.</span><span class="sxs-lookup"><span data-stu-id="41b0a-112">Indicate whether the event has been handled by the app.</span></span>
[<span data-ttu-id="41b0a-113">put_Handled</span><span class="sxs-lookup"><span data-stu-id="41b0a-113">put_Handled</span></span>](#put_handled) | <span data-ttu-id="41b0a-114">Задайте свойство Handled.</span><span class="sxs-lookup"><span data-stu-id="41b0a-114">Set the Handled property.</span></span>

## <span data-ttu-id="41b0a-115">Участников</span><span class="sxs-lookup"><span data-stu-id="41b0a-115">Members</span></span>

#### <span data-ttu-id="41b0a-116">get_Reason</span><span class="sxs-lookup"><span data-stu-id="41b0a-116">get_Reason</span></span> 

<span data-ttu-id="41b0a-117">Причина, по которой WebView запускает событие "MoveFocus".</span><span class="sxs-lookup"><span data-stu-id="41b0a-117">The reason for WebView to fire the MoveFocus Requested event.</span></span>

> <span data-ttu-id="41b0a-118">общедоступное значение HRESULT [get_Reason](#get_reason)(WEBVIEW2_MOVE_FOCUS_REASON \* значение)</span><span class="sxs-lookup"><span data-stu-id="41b0a-118">public HRESULT [get_Reason](#get_reason)(WEBVIEW2_MOVE_FOCUS_REASON \* value)</span></span>

#### <span data-ttu-id="41b0a-119">get_Handled</span><span class="sxs-lookup"><span data-stu-id="41b0a-119">get_Handled</span></span> 

<span data-ttu-id="41b0a-120">Указывает, было ли событие обработано приложением.</span><span class="sxs-lookup"><span data-stu-id="41b0a-120">Indicate whether the event has been handled by the app.</span></span>

> <span data-ttu-id="41b0a-121">общедоступные значения HRESULT [get_Handled](#get_handled)(bool \* Value)</span><span class="sxs-lookup"><span data-stu-id="41b0a-121">public HRESULT [get_Handled](#get_handled)(BOOL \* value)</span></span>

<span data-ttu-id="41b0a-122">Если приложение переместило фокус на нужное место, оно должно установить для свойства Handled значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="41b0a-122">If the app has moved the focus to its desired location, it should set Handled property to TRUE.</span></span> <span data-ttu-id="41b0a-123">Если свойство Handled имеет значение false после возвращения обработчика событий, будет принято действие по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="41b0a-123">When Handled property is false after the event handler returns, default action will be taken.</span></span> <span data-ttu-id="41b0a-124">Действие по умолчанию — попытка найти следующую вкладку для дочернего окна позиции табуляции в приложении и попытаться переместить фокус на это окно.</span><span class="sxs-lookup"><span data-stu-id="41b0a-124">The default action is to try to find the next tab stop child window in the app and try to move focus to that window.</span></span> <span data-ttu-id="41b0a-125">Если для перемещения фокуса не существует другого окна, фокус будет циклически перемещаться в веб-контент WebView.</span><span class="sxs-lookup"><span data-stu-id="41b0a-125">If there is no other such window to move focus to, focus will be cycled within the WebView's web content.</span></span>

#### <span data-ttu-id="41b0a-126">put_Handled</span><span class="sxs-lookup"><span data-stu-id="41b0a-126">put_Handled</span></span> 

<span data-ttu-id="41b0a-127">Задайте свойство Handled.</span><span class="sxs-lookup"><span data-stu-id="41b0a-127">Set the Handled property.</span></span>

> <span data-ttu-id="41b0a-128">общедоступные значения HRESULT [put_Handled](#put_handled)(логическое значение)</span><span class="sxs-lookup"><span data-stu-id="41b0a-128">public HRESULT [put_Handled](#put_handled)(BOOL value)</span></span>

