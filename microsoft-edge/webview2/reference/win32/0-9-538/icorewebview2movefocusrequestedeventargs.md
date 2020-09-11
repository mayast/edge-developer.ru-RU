---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2MoveFocusRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2MoveFocusRequestedEventArgs
ms.openlocfilehash: 7d86b0129c126b39ae8200550a024819e2004b49
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010028"
---
# <span data-ttu-id="496b9-104">0.9.579-Interface ICoreWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="496b9-104">0.9.579 - interface ICoreWebView2MoveFocusRequestedEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2MoveFocusRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="496b9-105">Аргументы события для события MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="496b9-105">Event args for the MoveFocusRequested event.</span></span>

## <span data-ttu-id="496b9-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="496b9-106">Summary</span></span>

 <span data-ttu-id="496b9-107">Участников</span><span class="sxs-lookup"><span data-stu-id="496b9-107">Members</span></span>                        | <span data-ttu-id="496b9-108">Описания</span><span class="sxs-lookup"><span data-stu-id="496b9-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="496b9-109">get_Handled</span><span class="sxs-lookup"><span data-stu-id="496b9-109">get_Handled</span></span>](#get_handled) | <span data-ttu-id="496b9-110">Указывает, было ли событие обработано приложением.</span><span class="sxs-lookup"><span data-stu-id="496b9-110">Indicate whether the event has been handled by the app.</span></span>
[<span data-ttu-id="496b9-111">get_Reason</span><span class="sxs-lookup"><span data-stu-id="496b9-111">get_Reason</span></span>](#get_reason) | <span data-ttu-id="496b9-112">Причина, по которой WebView запускает событие "MoveFocus".</span><span class="sxs-lookup"><span data-stu-id="496b9-112">The reason for WebView to fire the MoveFocus Requested event.</span></span>
[<span data-ttu-id="496b9-113">put_Handled</span><span class="sxs-lookup"><span data-stu-id="496b9-113">put_Handled</span></span>](#put_handled) | <span data-ttu-id="496b9-114">Задайте свойство Handled.</span><span class="sxs-lookup"><span data-stu-id="496b9-114">Set the Handled property.</span></span>

## <span data-ttu-id="496b9-115">Участников</span><span class="sxs-lookup"><span data-stu-id="496b9-115">Members</span></span>

#### <span data-ttu-id="496b9-116">get_Handled</span><span class="sxs-lookup"><span data-stu-id="496b9-116">get_Handled</span></span> 

<span data-ttu-id="496b9-117">Указывает, было ли событие обработано приложением.</span><span class="sxs-lookup"><span data-stu-id="496b9-117">Indicate whether the event has been handled by the app.</span></span>

> <span data-ttu-id="496b9-118">общедоступные значения HRESULT [get_Handled](#get_handled)(bool \* Value)</span><span class="sxs-lookup"><span data-stu-id="496b9-118">public HRESULT [get_Handled](#get_handled)(BOOL \* value)</span></span>

<span data-ttu-id="496b9-119">Если приложение переместило фокус на нужное место, оно должно установить для свойства Handled значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="496b9-119">If the app has moved the focus to its desired location, it should set Handled property to TRUE.</span></span> <span data-ttu-id="496b9-120">Если свойство Handled имеет значение false после возвращения обработчика событий, будет принято действие по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="496b9-120">When Handled property is false after the event handler returns, default action will be taken.</span></span> <span data-ttu-id="496b9-121">Действие по умолчанию — попытка найти следующую вкладку для дочернего окна позиции табуляции в приложении и попытаться переместить фокус на это окно.</span><span class="sxs-lookup"><span data-stu-id="496b9-121">The default action is to try to find the next tab stop child window in the app and try to move focus to that window.</span></span> <span data-ttu-id="496b9-122">Если для перемещения фокуса не существует другого окна, фокус будет циклически перемещаться в веб-контент WebView.</span><span class="sxs-lookup"><span data-stu-id="496b9-122">If there is no other such window to move focus to, focus will be cycled within the WebView's web content.</span></span>

#### <span data-ttu-id="496b9-123">get_Reason</span><span class="sxs-lookup"><span data-stu-id="496b9-123">get_Reason</span></span> 

<span data-ttu-id="496b9-124">Причина, по которой WebView запускает событие "MoveFocus".</span><span class="sxs-lookup"><span data-stu-id="496b9-124">The reason for WebView to fire the MoveFocus Requested event.</span></span>

> <span data-ttu-id="496b9-125">общедоступное значение HRESULT [get_Reason](#get_reason)(COREWEBVIEW2_MOVE_FOCUS_REASON \* значение)</span><span class="sxs-lookup"><span data-stu-id="496b9-125">public HRESULT [get_Reason](#get_reason)(COREWEBVIEW2_MOVE_FOCUS_REASON \* value)</span></span>

#### <span data-ttu-id="496b9-126">put_Handled</span><span class="sxs-lookup"><span data-stu-id="496b9-126">put_Handled</span></span> 

<span data-ttu-id="496b9-127">Задайте свойство Handled.</span><span class="sxs-lookup"><span data-stu-id="496b9-127">Set the Handled property.</span></span>

> <span data-ttu-id="496b9-128">общедоступные значения HRESULT [put_Handled](#put_handled)(логическое значение)</span><span class="sxs-lookup"><span data-stu-id="496b9-128">public HRESULT [put_Handled](#put_handled)(BOOL value)</span></span>

