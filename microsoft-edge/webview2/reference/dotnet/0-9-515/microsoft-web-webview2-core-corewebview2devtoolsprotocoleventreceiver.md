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
ms.openlocfilehash: 9b54f9f519c76440d3556bb67f5ab7ad186ba290
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697667"
---
# <span data-ttu-id="5db11-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2DevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="5db11-104">Microsoft.Web.WebView2.Core.CoreWebView2DevToolsProtocolEventReceiver class</span></span> 

> [!NOTE]
> <span data-ttu-id="5db11-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="5db11-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="5db11-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="5db11-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="5db11-107">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="5db11-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="5db11-108">Сборка: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="5db11-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="5db11-109">Получатель создается для определенного события протокола DevTools и позволяет подписаться на него и отказаться от него.</span><span class="sxs-lookup"><span data-stu-id="5db11-109">A Receiver is created for a particular DevTools Protocol event and allows you to subscribe and unsubscribe from that event.</span></span>

## <span data-ttu-id="5db11-110">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="5db11-110">Summary</span></span>

 <span data-ttu-id="5db11-111">Участников</span><span class="sxs-lookup"><span data-stu-id="5db11-111">Members</span></span>                        | <span data-ttu-id="5db11-112">Описания</span><span class="sxs-lookup"><span data-stu-id="5db11-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5db11-113">DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="5db11-113">DevToolsProtocolEventReceived</span></span>](#devtoolsprotocoleventreceived) | <span data-ttu-id="5db11-114">Подпишитесь на событие DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="5db11-114">Subscribe to a DevToolsProtocol event.</span></span>

<span data-ttu-id="5db11-115">Получить из объекта WebView через GetDevToolsProtocolEventReceiver.</span><span class="sxs-lookup"><span data-stu-id="5db11-115">Obtained from the WebView object via GetDevToolsProtocolEventReceiver.</span></span>

## <span data-ttu-id="5db11-116">Участников</span><span class="sxs-lookup"><span data-stu-id="5db11-116">Members</span></span>

#### <span data-ttu-id="5db11-117">DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="5db11-117">DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="5db11-118">Подпишитесь на событие DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="5db11-118">Subscribe to a DevToolsProtocol event.</span></span>

> <span data-ttu-id="5db11-119">событие EventHandler< [CoreWebView2DevToolsProtocolEventReceivedEventArgs](microsoft-web-webview2-core-corewebview2devtoolsprotocoleventreceivedeventargs.md)  >  [DevToolsProtocolEventReceived](#devtoolsprotocoleventreceived)</span><span class="sxs-lookup"><span data-stu-id="5db11-119">public event EventHandler< [CoreWebView2DevToolsProtocolEventReceivedEventArgs](microsoft-web-webview2-core-corewebview2devtoolsprotocoleventreceivedeventargs.md) > [DevToolsProtocolEventReceived](#devtoolsprotocoleventreceived)</span></span>

<span data-ttu-id="5db11-120">Метод Invoke обработчика вызывается каждый раз, когда будет срабатывать соответствующее событие DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="5db11-120">The handler's Invoke method will be called whenever the corresponding DevToolsProtocol event fires.</span></span> <span data-ttu-id="5db11-121">Вызов вызывается с помощью объекта args события, содержащего объект Parameter события протокола DevTools в виде строки JSON.</span><span class="sxs-lookup"><span data-stu-id="5db11-121">Invoke will be called with the an event args object containing the DevTools Protocol event's parameter object as a JSON string.</span></span>

