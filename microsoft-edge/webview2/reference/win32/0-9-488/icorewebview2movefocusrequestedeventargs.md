---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/28/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 8ca8de3c430eda3bde089ca53501d880f4d8e35e
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654843"
---
# <span data-ttu-id="a7e3a-104">интерфейс ICoreWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="a7e3a-104">interface ICoreWebView2MoveFocusRequestedEventArgs</span></span> 

```
interface ICoreWebView2MoveFocusRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="a7e3a-105">Аргументы события для события MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="a7e3a-105">Event args for the MoveFocusRequested event.</span></span>

## <span data-ttu-id="a7e3a-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="a7e3a-106">Summary</span></span>

 <span data-ttu-id="a7e3a-107">Участников</span><span class="sxs-lookup"><span data-stu-id="a7e3a-107">Members</span></span>                        | <span data-ttu-id="a7e3a-108">Описания</span><span class="sxs-lookup"><span data-stu-id="a7e3a-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a7e3a-109">get_Handled</span><span class="sxs-lookup"><span data-stu-id="a7e3a-109">get_Handled</span></span>](#get_handled) | <span data-ttu-id="a7e3a-110">Указывает, было ли событие обработано приложением.</span><span class="sxs-lookup"><span data-stu-id="a7e3a-110">Indicate whether the event has been handled by the app.</span></span>
[<span data-ttu-id="a7e3a-111">get_Reason</span><span class="sxs-lookup"><span data-stu-id="a7e3a-111">get_Reason</span></span>](#get_reason) | <span data-ttu-id="a7e3a-112">Причина, по которой WebView запускает событие "MoveFocus".</span><span class="sxs-lookup"><span data-stu-id="a7e3a-112">The reason for WebView to fire the MoveFocus Requested event.</span></span>
[<span data-ttu-id="a7e3a-113">put_Handled</span><span class="sxs-lookup"><span data-stu-id="a7e3a-113">put_Handled</span></span>](#put_handled) | <span data-ttu-id="a7e3a-114">Задайте свойство Handled.</span><span class="sxs-lookup"><span data-stu-id="a7e3a-114">Set the Handled property.</span></span>

## <span data-ttu-id="a7e3a-115">Участников</span><span class="sxs-lookup"><span data-stu-id="a7e3a-115">Members</span></span>

#### <span data-ttu-id="a7e3a-116">get_Handled</span><span class="sxs-lookup"><span data-stu-id="a7e3a-116">get_Handled</span></span> 

<span data-ttu-id="a7e3a-117">Указывает, было ли событие обработано приложением.</span><span class="sxs-lookup"><span data-stu-id="a7e3a-117">Indicate whether the event has been handled by the app.</span></span>

> <span data-ttu-id="a7e3a-118">общедоступные значения HRESULT [get_Handled](#get_handled)(bool \* Value)</span><span class="sxs-lookup"><span data-stu-id="a7e3a-118">public HRESULT [get_Handled](#get_handled)(BOOL \* value)</span></span>

<span data-ttu-id="a7e3a-119">Если приложение переместило фокус на нужное место, оно должно установить для свойства Handled значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="a7e3a-119">If the app has moved the focus to its desired location, it should set Handled property to TRUE.</span></span> <span data-ttu-id="a7e3a-120">Если свойство Handled имеет значение false после возвращения обработчика событий, будет принято действие по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a7e3a-120">When Handled property is false after the event handler returns, default action will be taken.</span></span> <span data-ttu-id="a7e3a-121">Действие по умолчанию — попытка найти следующую вкладку для дочернего окна позиции табуляции в приложении и попытаться переместить фокус на это окно.</span><span class="sxs-lookup"><span data-stu-id="a7e3a-121">The default action is to try to find the next tab stop child window in the app and try to move focus to that window.</span></span> <span data-ttu-id="a7e3a-122">Если для перемещения фокуса не существует другого окна, фокус будет циклически перемещаться в веб-контент WebView.</span><span class="sxs-lookup"><span data-stu-id="a7e3a-122">If there is no other such window to move focus to, focus will be cycled within the WebView's web content.</span></span>

#### <span data-ttu-id="a7e3a-123">get_Reason</span><span class="sxs-lookup"><span data-stu-id="a7e3a-123">get_Reason</span></span> 

<span data-ttu-id="a7e3a-124">Причина, по которой WebView запускает событие "MoveFocus".</span><span class="sxs-lookup"><span data-stu-id="a7e3a-124">The reason for WebView to fire the MoveFocus Requested event.</span></span>

> <span data-ttu-id="a7e3a-125">общедоступное значение HRESULT [get_Reason](#get_reason)(COREWEBVIEW2_MOVE_FOCUS_REASON \* значение)</span><span class="sxs-lookup"><span data-stu-id="a7e3a-125">public HRESULT [get_Reason](#get_reason)(COREWEBVIEW2_MOVE_FOCUS_REASON \* value)</span></span>

#### <span data-ttu-id="a7e3a-126">put_Handled</span><span class="sxs-lookup"><span data-stu-id="a7e3a-126">put_Handled</span></span> 

<span data-ttu-id="a7e3a-127">Задайте свойство Handled.</span><span class="sxs-lookup"><span data-stu-id="a7e3a-127">Set the Handled property.</span></span>

> <span data-ttu-id="a7e3a-128">общедоступные значения HRESULT [put_Handled](#put_handled)(логическое значение)</span><span class="sxs-lookup"><span data-stu-id="a7e3a-128">public HRESULT [put_Handled](#put_handled)(BOOL value)</span></span>

