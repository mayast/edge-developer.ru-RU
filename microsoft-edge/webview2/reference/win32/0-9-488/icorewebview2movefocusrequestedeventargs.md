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
ms.openlocfilehash: de0319060b6e618c30fc685815bcbcc41e8c3005
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697849"
---
# <span data-ttu-id="9e31a-104">интерфейс ICoreWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="9e31a-104">interface ICoreWebView2MoveFocusRequestedEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="9e31a-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="9e31a-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="9e31a-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="9e31a-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2MoveFocusRequestedEventArgs
  : public IUnknown
```

<span data-ttu-id="9e31a-107">Аргументы события для события MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="9e31a-107">Event args for the MoveFocusRequested event.</span></span>

## <span data-ttu-id="9e31a-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="9e31a-108">Summary</span></span>

 <span data-ttu-id="9e31a-109">Участников</span><span class="sxs-lookup"><span data-stu-id="9e31a-109">Members</span></span>                        | <span data-ttu-id="9e31a-110">Описания</span><span class="sxs-lookup"><span data-stu-id="9e31a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="9e31a-111">get_Handled</span><span class="sxs-lookup"><span data-stu-id="9e31a-111">get_Handled</span></span>](#get_handled) | <span data-ttu-id="9e31a-112">Указывает, было ли событие обработано приложением.</span><span class="sxs-lookup"><span data-stu-id="9e31a-112">Indicate whether the event has been handled by the app.</span></span>
[<span data-ttu-id="9e31a-113">get_Reason</span><span class="sxs-lookup"><span data-stu-id="9e31a-113">get_Reason</span></span>](#get_reason) | <span data-ttu-id="9e31a-114">Причина, по которой WebView запускает событие "MoveFocus".</span><span class="sxs-lookup"><span data-stu-id="9e31a-114">The reason for WebView to fire the MoveFocus Requested event.</span></span>
[<span data-ttu-id="9e31a-115">put_Handled</span><span class="sxs-lookup"><span data-stu-id="9e31a-115">put_Handled</span></span>](#put_handled) | <span data-ttu-id="9e31a-116">Задайте свойство Handled.</span><span class="sxs-lookup"><span data-stu-id="9e31a-116">Set the Handled property.</span></span>

## <span data-ttu-id="9e31a-117">Участников</span><span class="sxs-lookup"><span data-stu-id="9e31a-117">Members</span></span>

#### <span data-ttu-id="9e31a-118">get_Handled</span><span class="sxs-lookup"><span data-stu-id="9e31a-118">get_Handled</span></span> 

<span data-ttu-id="9e31a-119">Указывает, было ли событие обработано приложением.</span><span class="sxs-lookup"><span data-stu-id="9e31a-119">Indicate whether the event has been handled by the app.</span></span>

> <span data-ttu-id="9e31a-120">общедоступные значения HRESULT [get_Handled](#get_handled)(bool \* Value)</span><span class="sxs-lookup"><span data-stu-id="9e31a-120">public HRESULT [get_Handled](#get_handled)(BOOL \* value)</span></span>

<span data-ttu-id="9e31a-121">Если приложение переместило фокус на нужное место, оно должно установить для свойства Handled значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="9e31a-121">If the app has moved the focus to its desired location, it should set Handled property to TRUE.</span></span> <span data-ttu-id="9e31a-122">Если свойство Handled имеет значение false после возвращения обработчика событий, будет принято действие по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9e31a-122">When Handled property is false after the event handler returns, default action will be taken.</span></span> <span data-ttu-id="9e31a-123">Действие по умолчанию — попытка найти следующую вкладку для дочернего окна позиции табуляции в приложении и попытаться переместить фокус на это окно.</span><span class="sxs-lookup"><span data-stu-id="9e31a-123">The default action is to try to find the next tab stop child window in the app and try to move focus to that window.</span></span> <span data-ttu-id="9e31a-124">Если для перемещения фокуса не существует другого окна, фокус будет циклически перемещаться в веб-контент WebView.</span><span class="sxs-lookup"><span data-stu-id="9e31a-124">If there is no other such window to move focus to, focus will be cycled within the WebView's web content.</span></span>

#### <span data-ttu-id="9e31a-125">get_Reason</span><span class="sxs-lookup"><span data-stu-id="9e31a-125">get_Reason</span></span> 

<span data-ttu-id="9e31a-126">Причина, по которой WebView запускает событие "MoveFocus".</span><span class="sxs-lookup"><span data-stu-id="9e31a-126">The reason for WebView to fire the MoveFocus Requested event.</span></span>

> <span data-ttu-id="9e31a-127">общедоступное значение HRESULT [get_Reason](#get_reason)(COREWEBVIEW2_MOVE_FOCUS_REASON \* значение)</span><span class="sxs-lookup"><span data-stu-id="9e31a-127">public HRESULT [get_Reason](#get_reason)(COREWEBVIEW2_MOVE_FOCUS_REASON \* value)</span></span>

#### <span data-ttu-id="9e31a-128">put_Handled</span><span class="sxs-lookup"><span data-stu-id="9e31a-128">put_Handled</span></span> 

<span data-ttu-id="9e31a-129">Задайте свойство Handled.</span><span class="sxs-lookup"><span data-stu-id="9e31a-129">Set the Handled property.</span></span>

> <span data-ttu-id="9e31a-130">общедоступные значения HRESULT [put_Handled](#put_handled)(логическое значение)</span><span class="sxs-lookup"><span data-stu-id="9e31a-130">public HRESULT [put_Handled](#put_handled)(BOOL value)</span></span>

