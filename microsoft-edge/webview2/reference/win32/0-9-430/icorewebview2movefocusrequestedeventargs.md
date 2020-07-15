---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2MoveFocusRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: fe0c0fae0ec33cbc5ba50ca163b3f4fc8baa61b9
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10880957"
---
# <span data-ttu-id="a1c2c-104">0.9.430-Interface ICoreWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="a1c2c-104">0.9.430 - interface ICoreWebView2MoveFocusRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="a1c2c-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="a1c2c-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="a1c2c-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="a1c2c-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2MoveFocusRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="a1c2c-107">Аргументы события для события MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="a1c2c-107">Event args for the MoveFocusRequested event.</span></span>

## <span data-ttu-id="a1c2c-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="a1c2c-108">Summary</span></span>

 <span data-ttu-id="a1c2c-109">Участников</span><span class="sxs-lookup"><span data-stu-id="a1c2c-109">Members</span></span>                        | <span data-ttu-id="a1c2c-110">Описания</span><span class="sxs-lookup"><span data-stu-id="a1c2c-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a1c2c-111">get_Reason</span><span class="sxs-lookup"><span data-stu-id="a1c2c-111">get_Reason</span></span>](#get_reason) | <span data-ttu-id="a1c2c-112">Причина, по которой WebView запускает событие "MoveFocus".</span><span class="sxs-lookup"><span data-stu-id="a1c2c-112">The reason for WebView to fire the MoveFocus Requested event.</span></span>
[<span data-ttu-id="a1c2c-113">get_Handled</span><span class="sxs-lookup"><span data-stu-id="a1c2c-113">get_Handled</span></span>](#get_handled) | <span data-ttu-id="a1c2c-114">Указывает, было ли событие обработано приложением.</span><span class="sxs-lookup"><span data-stu-id="a1c2c-114">Indicate whether the event has been handled by the app.</span></span>
[<span data-ttu-id="a1c2c-115">put_Handled</span><span class="sxs-lookup"><span data-stu-id="a1c2c-115">put_Handled</span></span>](#put_handled) | <span data-ttu-id="a1c2c-116">Задайте свойство Handled.</span><span class="sxs-lookup"><span data-stu-id="a1c2c-116">Set the Handled property.</span></span>

## <span data-ttu-id="a1c2c-117">Участников</span><span class="sxs-lookup"><span data-stu-id="a1c2c-117">Members</span></span>

#### <span data-ttu-id="a1c2c-118">get_Reason</span><span class="sxs-lookup"><span data-stu-id="a1c2c-118">get_Reason</span></span> 

<span data-ttu-id="a1c2c-119">Причина, по которой WebView запускает событие "MoveFocus".</span><span class="sxs-lookup"><span data-stu-id="a1c2c-119">The reason for WebView to fire the MoveFocus Requested event.</span></span>

> <span data-ttu-id="a1c2c-120">общедоступное значение HRESULT [get_Reason](#get_reason)(CORE_WEBVIEW2_MOVE_FOCUS_REASON \* значение)</span><span class="sxs-lookup"><span data-stu-id="a1c2c-120">public HRESULT [get_Reason](#get_reason)(CORE_WEBVIEW2_MOVE_FOCUS_REASON \* value)</span></span>

#### <span data-ttu-id="a1c2c-121">get_Handled</span><span class="sxs-lookup"><span data-stu-id="a1c2c-121">get_Handled</span></span> 

<span data-ttu-id="a1c2c-122">Указывает, было ли событие обработано приложением.</span><span class="sxs-lookup"><span data-stu-id="a1c2c-122">Indicate whether the event has been handled by the app.</span></span>

> <span data-ttu-id="a1c2c-123">общедоступные значения HRESULT [get_Handled](#get_handled)(bool \* Value)</span><span class="sxs-lookup"><span data-stu-id="a1c2c-123">public HRESULT [get_Handled](#get_handled)(BOOL \* value)</span></span>

<span data-ttu-id="a1c2c-124">Если приложение переместило фокус на нужное место, оно должно установить для свойства Handled значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="a1c2c-124">If the app has moved the focus to its desired location, it should set Handled property to TRUE.</span></span> <span data-ttu-id="a1c2c-125">Если свойство Handled имеет значение false после возвращения обработчика событий, будет принято действие по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a1c2c-125">When Handled property is false after the event handler returns, default action will be taken.</span></span> <span data-ttu-id="a1c2c-126">Действие по умолчанию — попытка найти следующую вкладку для дочернего окна позиции табуляции в приложении и попытаться переместить фокус на это окно.</span><span class="sxs-lookup"><span data-stu-id="a1c2c-126">The default action is to try to find the next tab stop child window in the app and try to move focus to that window.</span></span> <span data-ttu-id="a1c2c-127">Если для перемещения фокуса не существует другого окна, фокус будет циклически перемещаться в веб-контент WebView.</span><span class="sxs-lookup"><span data-stu-id="a1c2c-127">If there is no other such window to move focus to, focus will be cycled within the WebView's web content.</span></span>

#### <span data-ttu-id="a1c2c-128">put_Handled</span><span class="sxs-lookup"><span data-stu-id="a1c2c-128">put_Handled</span></span> 

<span data-ttu-id="a1c2c-129">Задайте свойство Handled.</span><span class="sxs-lookup"><span data-stu-id="a1c2c-129">Set the Handled property.</span></span>

> <span data-ttu-id="a1c2c-130">общедоступные значения HRESULT [put_Handled](#put_handled)(логическое значение)</span><span class="sxs-lookup"><span data-stu-id="a1c2c-130">public HRESULT [put_Handled](#put_handled)(BOOL value)</span></span>

