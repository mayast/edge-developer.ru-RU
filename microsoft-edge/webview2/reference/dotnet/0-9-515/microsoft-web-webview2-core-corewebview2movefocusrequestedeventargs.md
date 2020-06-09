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
ms.openlocfilehash: 69835f6fe22246f43e3df9c45a7fde7a674ac0e5
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697646"
---
# <span data-ttu-id="665bb-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2MoveFocusRequestedEventArgs</span><span class="sxs-lookup"><span data-stu-id="665bb-104">Microsoft.Web.WebView2.Core.CoreWebView2MoveFocusRequestedEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="665bb-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="665bb-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="665bb-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="665bb-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="665bb-107">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="665bb-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="665bb-108">Сборка: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="665bb-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="665bb-109">Аргументы события для события MoveFocusRequested.</span><span class="sxs-lookup"><span data-stu-id="665bb-109">Event args for the MoveFocusRequested event.</span></span>

## <span data-ttu-id="665bb-110">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="665bb-110">Summary</span></span>

 <span data-ttu-id="665bb-111">Участников</span><span class="sxs-lookup"><span data-stu-id="665bb-111">Members</span></span>                        | <span data-ttu-id="665bb-112">Описания</span><span class="sxs-lookup"><span data-stu-id="665bb-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="665bb-113">Handled</span><span class="sxs-lookup"><span data-stu-id="665bb-113">Handled</span></span>](#handled) | <span data-ttu-id="665bb-114">Указывает, было ли событие обработано приложением.</span><span class="sxs-lookup"><span data-stu-id="665bb-114">Indicate whether the event has been handled by the app.</span></span>
[<span data-ttu-id="665bb-115">Причина</span><span class="sxs-lookup"><span data-stu-id="665bb-115">Reason</span></span>](#reason) | <span data-ttu-id="665bb-116">Причина, по которой WebView запускает событие "MoveFocus".</span><span class="sxs-lookup"><span data-stu-id="665bb-116">The reason for WebView to fire the MoveFocus Requested event.</span></span>

## <span data-ttu-id="665bb-117">Участников</span><span class="sxs-lookup"><span data-stu-id="665bb-117">Members</span></span>

#### <span data-ttu-id="665bb-118">Handled</span><span class="sxs-lookup"><span data-stu-id="665bb-118">Handled</span></span> 

<span data-ttu-id="665bb-119">Указывает, было ли событие обработано приложением.</span><span class="sxs-lookup"><span data-stu-id="665bb-119">Indicate whether the event has been handled by the app.</span></span>

> <span data-ttu-id="665bb-120">общедоступный логический том [обработан](#handled)</span><span class="sxs-lookup"><span data-stu-id="665bb-120">public bool [Handled](#handled)</span></span>

<span data-ttu-id="665bb-121">Если приложение переместило фокус на нужное место, оно должно установить для свойства Handled значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="665bb-121">If the app has moved the focus to its desired location, it should set Handled property to TRUE.</span></span> <span data-ttu-id="665bb-122">Если свойство Handled имеет значение false после возвращения обработчика событий, будет принято действие по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="665bb-122">When Handled property is false after the event handler returns, default action will be taken.</span></span> <span data-ttu-id="665bb-123">Действие по умолчанию — попытка найти следующую вкладку для дочернего окна позиции табуляции в приложении и попытаться переместить фокус на это окно.</span><span class="sxs-lookup"><span data-stu-id="665bb-123">The default action is to try to find the next tab stop child window in the app and try to move focus to that window.</span></span> <span data-ttu-id="665bb-124">Если для перемещения фокуса не существует другого окна, фокус будет циклически перемещаться в веб-контент WebView.</span><span class="sxs-lookup"><span data-stu-id="665bb-124">If there is no other such window to move focus to, focus will be cycled within the WebView's web content.</span></span>

#### <span data-ttu-id="665bb-125">Причина</span><span class="sxs-lookup"><span data-stu-id="665bb-125">Reason</span></span> 

<span data-ttu-id="665bb-126">Причина, по которой WebView запускает событие "MoveFocus".</span><span class="sxs-lookup"><span data-stu-id="665bb-126">The reason for WebView to fire the MoveFocus Requested event.</span></span>

> <span data-ttu-id="665bb-127">[Причина](#reason) общедоступной CoreWebView2MoveFocusReason</span><span class="sxs-lookup"><span data-stu-id="665bb-127">public CoreWebView2MoveFocusReason [Reason](#reason)</span></span>

