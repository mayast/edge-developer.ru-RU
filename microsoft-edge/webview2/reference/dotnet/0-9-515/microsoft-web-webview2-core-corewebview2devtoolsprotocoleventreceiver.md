---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2DevToolsProtocolEventReceiver
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 1982c6926d2ed8805433efc4d46ff6f3cac691ce
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885060"
---
# <span data-ttu-id="7b6ce-104">класс 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2DevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="7b6ce-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2DevToolsProtocolEventReceiver class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="7b6ce-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="7b6ce-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="7b6ce-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="7b6ce-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="7b6ce-107">Получатель создается для определенного события протокола DevTools и позволяет подписаться на него и отказаться от него.</span><span class="sxs-lookup"><span data-stu-id="7b6ce-107">A Receiver is created for a particular DevTools Protocol event and allows you to subscribe and unsubscribe from that event.</span></span>

## <span data-ttu-id="7b6ce-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="7b6ce-108">Summary</span></span>

 <span data-ttu-id="7b6ce-109">Участников</span><span class="sxs-lookup"><span data-stu-id="7b6ce-109">Members</span></span>                        | <span data-ttu-id="7b6ce-110">Описания</span><span class="sxs-lookup"><span data-stu-id="7b6ce-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7b6ce-111">DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="7b6ce-111">DevToolsProtocolEventReceived</span></span>](#devtoolsprotocoleventreceived) | <span data-ttu-id="7b6ce-112">Подпишитесь на событие DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="7b6ce-112">Subscribe to a DevToolsProtocol event.</span></span>

<span data-ttu-id="7b6ce-113">Получить из объекта WebView через GetDevToolsProtocolEventReceiver.</span><span class="sxs-lookup"><span data-stu-id="7b6ce-113">Obtained from the WebView object via GetDevToolsProtocolEventReceiver.</span></span>

## <span data-ttu-id="7b6ce-114">Участников</span><span class="sxs-lookup"><span data-stu-id="7b6ce-114">Members</span></span>

#### <span data-ttu-id="7b6ce-115">DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="7b6ce-115">DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="7b6ce-116">Подпишитесь на событие DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="7b6ce-116">Subscribe to a DevToolsProtocol event.</span></span>

> <span data-ttu-id="7b6ce-117">событие EventHandler< [CoreWebView2DevToolsProtocolEventReceivedEventArgs](microsoft-web-webview2-core-corewebview2devtoolsprotocoleventreceivedeventargs.md)  >  [DevToolsProtocolEventReceived](#devtoolsprotocoleventreceived)</span><span class="sxs-lookup"><span data-stu-id="7b6ce-117">public event EventHandler< [CoreWebView2DevToolsProtocolEventReceivedEventArgs](microsoft-web-webview2-core-corewebview2devtoolsprotocoleventreceivedeventargs.md) > [DevToolsProtocolEventReceived](#devtoolsprotocoleventreceived)</span></span>

<span data-ttu-id="7b6ce-118">Метод Invoke обработчика вызывается каждый раз, когда будет срабатывать соответствующее событие DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="7b6ce-118">The handler's Invoke method will be called whenever the corresponding DevToolsProtocol event fires.</span></span> <span data-ttu-id="7b6ce-119">Вызов вызывается с помощью объекта args события, содержащего объект Parameter события протокола DevTools в виде строки JSON.</span><span class="sxs-lookup"><span data-stu-id="7b6ce-119">Invoke will be called with the an event args object containing the DevTools Protocol event's parameter object as a JSON string.</span></span>

