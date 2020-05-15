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
ms.openlocfilehash: 23ee363fd90416d07c76644879a5f4b6cc2acabe
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654935"
---
# <span data-ttu-id="c0c6b-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2DevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="c0c6b-104">Microsoft.Web.WebView2.Core.CoreWebView2DevToolsProtocolEventReceiver class</span></span> 

<span data-ttu-id="c0c6b-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="c0c6b-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="c0c6b-106">Сборка: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="c0c6b-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="c0c6b-107">Получатель создается для определенного события протокола DevTools и позволяет подписаться на него и отказаться от него.</span><span class="sxs-lookup"><span data-stu-id="c0c6b-107">A Receiver is created for a particular DevTools Protocol event and allows you to subscribe and unsubscribe from that event.</span></span>

## <span data-ttu-id="c0c6b-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="c0c6b-108">Summary</span></span>

 <span data-ttu-id="c0c6b-109">Участников</span><span class="sxs-lookup"><span data-stu-id="c0c6b-109">Members</span></span>                        | <span data-ttu-id="c0c6b-110">Описания</span><span class="sxs-lookup"><span data-stu-id="c0c6b-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="c0c6b-111">DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="c0c6b-111">DevToolsProtocolEventReceived</span></span>](#devtoolsprotocoleventreceived) | <span data-ttu-id="c0c6b-112">Подпишитесь на событие DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="c0c6b-112">Subscribe to a DevToolsProtocol event.</span></span>

<span data-ttu-id="c0c6b-113">Получить из объекта WebView через GetDevToolsProtocolEventReceiver.</span><span class="sxs-lookup"><span data-stu-id="c0c6b-113">Obtained from the WebView object via GetDevToolsProtocolEventReceiver.</span></span>

## <span data-ttu-id="c0c6b-114">Участников</span><span class="sxs-lookup"><span data-stu-id="c0c6b-114">Members</span></span>

#### <span data-ttu-id="c0c6b-115">DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="c0c6b-115">DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="c0c6b-116">Подпишитесь на событие DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="c0c6b-116">Subscribe to a DevToolsProtocol event.</span></span>

> <span data-ttu-id="c0c6b-117">событие EventHandler< [CoreWebView2DevToolsProtocolEventReceivedEventArgs](microsoft-web-webview2-core-corewebview2devtoolsprotocoleventreceivedeventargs.md)  >  [DevToolsProtocolEventReceived](#devtoolsprotocoleventreceived)</span><span class="sxs-lookup"><span data-stu-id="c0c6b-117">public event EventHandler< [CoreWebView2DevToolsProtocolEventReceivedEventArgs](microsoft-web-webview2-core-corewebview2devtoolsprotocoleventreceivedeventargs.md) > [DevToolsProtocolEventReceived](#devtoolsprotocoleventreceived)</span></span>

<span data-ttu-id="c0c6b-118">Метод Invoke обработчика вызывается каждый раз, когда будет срабатывать соответствующее событие DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="c0c6b-118">The handler's Invoke method will be called whenever the corresponding DevToolsProtocol event fires.</span></span> <span data-ttu-id="c0c6b-119">Вызов вызывается с помощью объекта args события, содержащего объект Parameter события протокола DevTools в виде строки JSON.</span><span class="sxs-lookup"><span data-stu-id="c0c6b-119">Invoke will be called with the an event args object containing the DevTools Protocol event's parameter object as a JSON string.</span></span>

