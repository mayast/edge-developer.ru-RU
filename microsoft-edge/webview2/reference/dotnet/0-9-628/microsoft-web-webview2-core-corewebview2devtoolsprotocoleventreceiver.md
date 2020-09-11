---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2DevToolsProtocolEventReceiver
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: 42ea3beb51dc315ed7ab3b7b0c04c7414adab2db
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11012410"
---
# <span data-ttu-id="67750-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2DevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="67750-104">Microsoft.Web.WebView2.Core.CoreWebView2DevToolsProtocolEventReceiver class</span></span> 

<span data-ttu-id="67750-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="67750-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="67750-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="67750-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="67750-107">Получатель создается для определенного события протокола DevTools и позволяет подписаться на него и отказаться от него.</span><span class="sxs-lookup"><span data-stu-id="67750-107">A Receiver is created for a particular DevTools Protocol event and allows you to subscribe and unsubscribe from that event.</span></span>

## <span data-ttu-id="67750-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="67750-108">Summary</span></span>

 <span data-ttu-id="67750-109">Участников</span><span class="sxs-lookup"><span data-stu-id="67750-109">Members</span></span>                        | <span data-ttu-id="67750-110">Описания</span><span class="sxs-lookup"><span data-stu-id="67750-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="67750-111">DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="67750-111">DevToolsProtocolEventReceived</span></span>](#devtoolsprotocoleventreceived) | <span data-ttu-id="67750-112">Подпишитесь на событие DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="67750-112">Subscribe to a DevToolsProtocol event.</span></span>

<span data-ttu-id="67750-113">Получить из объекта WebView через GetDevToolsProtocolEventReceiver.</span><span class="sxs-lookup"><span data-stu-id="67750-113">Obtained from the WebView object via GetDevToolsProtocolEventReceiver.</span></span>

## <span data-ttu-id="67750-114">Участников</span><span class="sxs-lookup"><span data-stu-id="67750-114">Members</span></span>

#### <span data-ttu-id="67750-115">DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="67750-115">DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="67750-116">Подпишитесь на событие DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="67750-116">Subscribe to a DevToolsProtocol event.</span></span>

> <span data-ttu-id="67750-117">событие EventHandler< [CoreWebView2DevToolsProtocolEventReceivedEventArgs](microsoft-web-webview2-core-corewebview2devtoolsprotocoleventreceivedeventargs.md)  >  [DevToolsProtocolEventReceived](#devtoolsprotocoleventreceived)</span><span class="sxs-lookup"><span data-stu-id="67750-117">public event EventHandler< [CoreWebView2DevToolsProtocolEventReceivedEventArgs](microsoft-web-webview2-core-corewebview2devtoolsprotocoleventreceivedeventargs.md) > [DevToolsProtocolEventReceived](#devtoolsprotocoleventreceived)</span></span>

<span data-ttu-id="67750-118">Метод Invoke обработчика вызывается каждый раз, когда будет срабатывать соответствующее событие DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="67750-118">The handler's Invoke method will be called whenever the corresponding DevToolsProtocol event fires.</span></span> <span data-ttu-id="67750-119">Вызов вызывается с помощью объекта аргументов события, содержащего объект Parameter события протокола DevTools в виде строки JSON.</span><span class="sxs-lookup"><span data-stu-id="67750-119">Invoke will be called with an event args object containing the DevTools Protocol event's parameter object as a JSON string.</span></span>

