---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2MoveFocusRequestedEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: dd141e135275d815458ce66a93dfc9ef3e7b33a8
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878864"
---
# <span data-ttu-id="f8bad-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="f8bad-104">Microsoft.Web.WebView2.Core.CoreWebView2MoveFocusRequestedEventArgs class</span></span> 

<span data-ttu-id="f8bad-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="f8bad-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="f8bad-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="f8bad-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="f8bad-107">Аргументы события для события MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="f8bad-107">Event args for the MoveFocusRequested event.</span></span>

## <span data-ttu-id="f8bad-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="f8bad-108">Summary</span></span>

 <span data-ttu-id="f8bad-109">Участников</span><span class="sxs-lookup"><span data-stu-id="f8bad-109">Members</span></span>                        | <span data-ttu-id="f8bad-110">Описания</span><span class="sxs-lookup"><span data-stu-id="f8bad-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f8bad-111">Handled</span><span class="sxs-lookup"><span data-stu-id="f8bad-111">Handled</span></span>](#handled) | <span data-ttu-id="f8bad-112">Указывает, было ли событие обработано приложением.</span><span class="sxs-lookup"><span data-stu-id="f8bad-112">Indicate whether the event has been handled by the app.</span></span>
[<span data-ttu-id="f8bad-113">Причина</span><span class="sxs-lookup"><span data-stu-id="f8bad-113">Reason</span></span>](#reason) | <span data-ttu-id="f8bad-114">Причина, по которой WebView запускает событие "MoveFocus".</span><span class="sxs-lookup"><span data-stu-id="f8bad-114">The reason for WebView to fire the MoveFocus Requested event.</span></span>

## <span data-ttu-id="f8bad-115">Участников</span><span class="sxs-lookup"><span data-stu-id="f8bad-115">Members</span></span>

#### <span data-ttu-id="f8bad-116">Handled</span><span class="sxs-lookup"><span data-stu-id="f8bad-116">Handled</span></span> 

<span data-ttu-id="f8bad-117">Указывает, было ли событие обработано приложением.</span><span class="sxs-lookup"><span data-stu-id="f8bad-117">Indicate whether the event has been handled by the app.</span></span>

> <span data-ttu-id="f8bad-118">общедоступный логический том [обработан](#handled)</span><span class="sxs-lookup"><span data-stu-id="f8bad-118">public bool [Handled](#handled)</span></span>

<span data-ttu-id="f8bad-119">Если приложение переместило фокус на нужное место, оно должно установить для свойства Handled значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="f8bad-119">If the app has moved the focus to its desired location, it should set Handled property to TRUE.</span></span> <span data-ttu-id="f8bad-120">Если свойство Handled имеет значение false после возвращения обработчика событий, будет принято действие по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f8bad-120">When Handled property is false after the event handler returns, default action will be taken.</span></span> <span data-ttu-id="f8bad-121">Действие по умолчанию — попытка найти следующую вкладку для дочернего окна позиции табуляции в приложении и попытаться переместить фокус на это окно.</span><span class="sxs-lookup"><span data-stu-id="f8bad-121">The default action is to try to find the next tab stop child window in the app and try to move focus to that window.</span></span> <span data-ttu-id="f8bad-122">Если для перемещения фокуса не существует другого окна, фокус будет циклически перемещаться в веб-контент WebView.</span><span class="sxs-lookup"><span data-stu-id="f8bad-122">If there is no other such window to move focus to, focus will be cycled within the WebView's web content.</span></span>

#### <span data-ttu-id="f8bad-123">Причина</span><span class="sxs-lookup"><span data-stu-id="f8bad-123">Reason</span></span> 

<span data-ttu-id="f8bad-124">Причина, по которой WebView запускает событие "MoveFocus".</span><span class="sxs-lookup"><span data-stu-id="f8bad-124">The reason for WebView to fire the MoveFocus Requested event.</span></span>

> <span data-ttu-id="f8bad-125">[Причина](#reason) общедоступной CoreWebView2MoveFocusReason</span><span class="sxs-lookup"><span data-stu-id="f8bad-125">public CoreWebView2MoveFocusReason [Reason](#reason)</span></span>

