---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2DevToolsProtocolEventReceiver
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: 155b0ae414d03d7a062b1e3426331307457687ae
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878913"
---
# <span data-ttu-id="b037d-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2DevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="b037d-104">Microsoft.Web.WebView2.Core.CoreWebView2DevToolsProtocolEventReceiver class</span></span> 

<span data-ttu-id="b037d-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="b037d-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="b037d-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="b037d-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="b037d-107">Получатель создается для определенного события протокола DevTools и позволяет подписаться на него и отказаться от него.</span><span class="sxs-lookup"><span data-stu-id="b037d-107">A Receiver is created for a particular DevTools Protocol event and allows you to subscribe and unsubscribe from that event.</span></span>

## <span data-ttu-id="b037d-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="b037d-108">Summary</span></span>

 <span data-ttu-id="b037d-109">Участников</span><span class="sxs-lookup"><span data-stu-id="b037d-109">Members</span></span>                        | <span data-ttu-id="b037d-110">Описания</span><span class="sxs-lookup"><span data-stu-id="b037d-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b037d-111">DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="b037d-111">DevToolsProtocolEventReceived</span></span>](#devtoolsprotocoleventreceived) | <span data-ttu-id="b037d-112">Подпишитесь на событие DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="b037d-112">Subscribe to a DevToolsProtocol event.</span></span>

<span data-ttu-id="b037d-113">Получить из объекта WebView через GetDevToolsProtocolEventReceiver.</span><span class="sxs-lookup"><span data-stu-id="b037d-113">Obtained from the WebView object via GetDevToolsProtocolEventReceiver.</span></span>

## <span data-ttu-id="b037d-114">Участников</span><span class="sxs-lookup"><span data-stu-id="b037d-114">Members</span></span>

#### <span data-ttu-id="b037d-115">DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="b037d-115">DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="b037d-116">Подпишитесь на событие DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="b037d-116">Subscribe to a DevToolsProtocol event.</span></span>

> <span data-ttu-id="b037d-117">событие EventHandler< [CoreWebView2DevToolsProtocolEventReceivedEventArgs](microsoft-web-webview2-core-corewebview2devtoolsprotocoleventreceivedeventargs.md)  >  [DevToolsProtocolEventReceived](#devtoolsprotocoleventreceived)</span><span class="sxs-lookup"><span data-stu-id="b037d-117">public event EventHandler< [CoreWebView2DevToolsProtocolEventReceivedEventArgs](microsoft-web-webview2-core-corewebview2devtoolsprotocoleventreceivedeventargs.md) > [DevToolsProtocolEventReceived](#devtoolsprotocoleventreceived)</span></span>

<span data-ttu-id="b037d-118">Метод Invoke обработчика вызывается каждый раз, когда будет срабатывать соответствующее событие DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="b037d-118">The handler's Invoke method will be called whenever the corresponding DevToolsProtocol event fires.</span></span> <span data-ttu-id="b037d-119">Вызов вызывается с помощью объекта args события, содержащего объект Parameter события протокола DevTools в виде строки JSON.</span><span class="sxs-lookup"><span data-stu-id="b037d-119">Invoke will be called with the an event args object containing the DevTools Protocol event's parameter object as a JSON string.</span></span>

