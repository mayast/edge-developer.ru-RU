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
ms.openlocfilehash: 2e3afec26b0e09a80182118f74b6f50733b0c71a
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654809"
---
# <span data-ttu-id="b56cc-104">интерфейс IWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="b56cc-104">interface IWebView2MoveFocusRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="b56cc-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="b56cc-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="b56cc-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="b56cc-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2MoveFocusRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="b56cc-107">Аргументы события для события MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="b56cc-107">Event args for the MoveFocusRequested event.</span></span>

## <span data-ttu-id="b56cc-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="b56cc-108">Summary</span></span>

 <span data-ttu-id="b56cc-109">Участников</span><span class="sxs-lookup"><span data-stu-id="b56cc-109">Members</span></span>                        | <span data-ttu-id="b56cc-110">Описания</span><span class="sxs-lookup"><span data-stu-id="b56cc-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b56cc-111">get_Reason</span><span class="sxs-lookup"><span data-stu-id="b56cc-111">get_Reason</span></span>](#get_reason) | <span data-ttu-id="b56cc-112">Причина, по которой WebView запускает событие "MoveFocus".</span><span class="sxs-lookup"><span data-stu-id="b56cc-112">The reason for WebView to fire the MoveFocus Requested event.</span></span>
[<span data-ttu-id="b56cc-113">get_Handled</span><span class="sxs-lookup"><span data-stu-id="b56cc-113">get_Handled</span></span>](#get_handled) | <span data-ttu-id="b56cc-114">Указывает, было ли событие обработано приложением.</span><span class="sxs-lookup"><span data-stu-id="b56cc-114">Indicate whether the event has been handled by the app.</span></span>
[<span data-ttu-id="b56cc-115">put_Handled</span><span class="sxs-lookup"><span data-stu-id="b56cc-115">put_Handled</span></span>](#put_handled) | <span data-ttu-id="b56cc-116">Задайте свойство Handled.</span><span class="sxs-lookup"><span data-stu-id="b56cc-116">Set the Handled property.</span></span>

## <span data-ttu-id="b56cc-117">Участников</span><span class="sxs-lookup"><span data-stu-id="b56cc-117">Members</span></span>

#### <span data-ttu-id="b56cc-118">get_Reason</span><span class="sxs-lookup"><span data-stu-id="b56cc-118">get_Reason</span></span> 

<span data-ttu-id="b56cc-119">Причина, по которой WebView запускает событие "MoveFocus".</span><span class="sxs-lookup"><span data-stu-id="b56cc-119">The reason for WebView to fire the MoveFocus Requested event.</span></span>

> <span data-ttu-id="b56cc-120">общедоступное значение HRESULT [get_Reason](#get_reason)(WEBVIEW2_MOVE_FOCUS_REASON \* значение)</span><span class="sxs-lookup"><span data-stu-id="b56cc-120">public HRESULT [get_Reason](#get_reason)(WEBVIEW2_MOVE_FOCUS_REASON \* value)</span></span>

#### <span data-ttu-id="b56cc-121">get_Handled</span><span class="sxs-lookup"><span data-stu-id="b56cc-121">get_Handled</span></span> 

<span data-ttu-id="b56cc-122">Указывает, было ли событие обработано приложением.</span><span class="sxs-lookup"><span data-stu-id="b56cc-122">Indicate whether the event has been handled by the app.</span></span>

> <span data-ttu-id="b56cc-123">общедоступные значения HRESULT [get_Handled](#get_handled)(bool \* Value)</span><span class="sxs-lookup"><span data-stu-id="b56cc-123">public HRESULT [get_Handled](#get_handled)(BOOL \* value)</span></span>

<span data-ttu-id="b56cc-124">Если приложение переместило фокус на нужное место, оно должно установить для свойства Handled значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="b56cc-124">If the app has moved the focus to its desired location, it should set Handled property to TRUE.</span></span> <span data-ttu-id="b56cc-125">Если свойство Handled имеет значение false после возвращения обработчика событий, будет принято действие по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b56cc-125">When Handled property is false after the event handler returns, default action will be taken.</span></span> <span data-ttu-id="b56cc-126">Действие по умолчанию — попытка найти следующую вкладку для дочернего окна позиции табуляции в приложении и попытаться переместить фокус на это окно.</span><span class="sxs-lookup"><span data-stu-id="b56cc-126">The default action is to try to find the next tab stop child window in the app and try to move focus to that window.</span></span> <span data-ttu-id="b56cc-127">Если для перемещения фокуса не существует другого окна, фокус будет циклически перемещаться в веб-контент WebView.</span><span class="sxs-lookup"><span data-stu-id="b56cc-127">If there is no other such window to move focus to, focus will be cycled within the WebView's web content.</span></span>

#### <span data-ttu-id="b56cc-128">put_Handled</span><span class="sxs-lookup"><span data-stu-id="b56cc-128">put_Handled</span></span> 

<span data-ttu-id="b56cc-129">Задайте свойство Handled.</span><span class="sxs-lookup"><span data-stu-id="b56cc-129">Set the Handled property.</span></span>

> <span data-ttu-id="b56cc-130">общедоступные значения HRESULT [put_Handled](#put_handled)(логическое значение)</span><span class="sxs-lookup"><span data-stu-id="b56cc-130">public HRESULT [put_Handled](#put_handled)(BOOL value)</span></span>

