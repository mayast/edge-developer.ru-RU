---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 3c88108f0e1df89c62c8713ff37f35d0c759cf6c
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654994"
---
# <span data-ttu-id="5509a-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="5509a-104">Microsoft.Web.WebView2.Core.CoreWebView2MoveFocusRequestedEventArgs class</span></span> 

<span data-ttu-id="5509a-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="5509a-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="5509a-106">Сборка: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="5509a-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="5509a-107">Аргументы события для события MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="5509a-107">Event args for the MoveFocusRequested event.</span></span>

## <span data-ttu-id="5509a-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="5509a-108">Summary</span></span>

 <span data-ttu-id="5509a-109">Участников</span><span class="sxs-lookup"><span data-stu-id="5509a-109">Members</span></span>                        | <span data-ttu-id="5509a-110">Описания</span><span class="sxs-lookup"><span data-stu-id="5509a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5509a-111">Handled</span><span class="sxs-lookup"><span data-stu-id="5509a-111">Handled</span></span>](#handled) | <span data-ttu-id="5509a-112">Указывает, было ли событие обработано приложением.</span><span class="sxs-lookup"><span data-stu-id="5509a-112">Indicate whether the event has been handled by the app.</span></span>
[<span data-ttu-id="5509a-113">Причина</span><span class="sxs-lookup"><span data-stu-id="5509a-113">Reason</span></span>](#reason) | <span data-ttu-id="5509a-114">Причина, по которой WebView запускает событие "MoveFocus".</span><span class="sxs-lookup"><span data-stu-id="5509a-114">The reason for WebView to fire the MoveFocus Requested event.</span></span>

## <span data-ttu-id="5509a-115">Участников</span><span class="sxs-lookup"><span data-stu-id="5509a-115">Members</span></span>

#### <span data-ttu-id="5509a-116">Handled</span><span class="sxs-lookup"><span data-stu-id="5509a-116">Handled</span></span> 

<span data-ttu-id="5509a-117">Указывает, было ли событие обработано приложением.</span><span class="sxs-lookup"><span data-stu-id="5509a-117">Indicate whether the event has been handled by the app.</span></span>

> <span data-ttu-id="5509a-118">общедоступный логический том [обработан](#handled)</span><span class="sxs-lookup"><span data-stu-id="5509a-118">public bool [Handled](#handled)</span></span>

<span data-ttu-id="5509a-119">Если приложение переместило фокус на нужное место, оно должно установить для свойства Handled значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="5509a-119">If the app has moved the focus to its desired location, it should set Handled property to TRUE.</span></span> <span data-ttu-id="5509a-120">Если свойство Handled имеет значение false после возвращения обработчика событий, будет принято действие по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5509a-120">When Handled property is false after the event handler returns, default action will be taken.</span></span> <span data-ttu-id="5509a-121">Действие по умолчанию — попытка найти следующую вкладку для дочернего окна позиции табуляции в приложении и попытаться переместить фокус на это окно.</span><span class="sxs-lookup"><span data-stu-id="5509a-121">The default action is to try to find the next tab stop child window in the app and try to move focus to that window.</span></span> <span data-ttu-id="5509a-122">Если для перемещения фокуса не существует другого окна, фокус будет циклически перемещаться в веб-контент WebView.</span><span class="sxs-lookup"><span data-stu-id="5509a-122">If there is no other such window to move focus to, focus will be cycled within the WebView's web content.</span></span>

#### <span data-ttu-id="5509a-123">Причина</span><span class="sxs-lookup"><span data-stu-id="5509a-123">Reason</span></span> 

<span data-ttu-id="5509a-124">Причина, по которой WebView запускает событие "MoveFocus".</span><span class="sxs-lookup"><span data-stu-id="5509a-124">The reason for WebView to fire the MoveFocus Requested event.</span></span>

> <span data-ttu-id="5509a-125">[Причина](#reason) общедоступной CoreWebView2MoveFocusReason</span><span class="sxs-lookup"><span data-stu-id="5509a-125">public CoreWebView2MoveFocusReason [Reason](#reason)</span></span>

