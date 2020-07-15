---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2DevToolsProtocolEventReceiver
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 6deff708368b5e8f1229c61cb27654667c7f5026
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10881104"
---
# <span data-ttu-id="7a56b-104">0.9.430-Interface ICoreWebView2DevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="7a56b-104">0.9.430 - interface ICoreWebView2DevToolsProtocolEventReceiver</span></span> 

> [!NOTE]
> <span data-ttu-id="7a56b-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="7a56b-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="7a56b-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="7a56b-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2DevToolsProtocolEventReceiver
  : public IUnknown
```

<span data-ttu-id="7a56b-107">Получатель создается для определенного события протокола DevTools и позволяет подписаться на него и unsubsribe от него.</span><span class="sxs-lookup"><span data-stu-id="7a56b-107">A Receiver is created for a particular DevTools Protocol event and allows you to subscribe and unsubsribe from that event.</span></span>

## <span data-ttu-id="7a56b-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="7a56b-108">Summary</span></span>

 <span data-ttu-id="7a56b-109">Участников</span><span class="sxs-lookup"><span data-stu-id="7a56b-109">Members</span></span>                        | <span data-ttu-id="7a56b-110">Описания</span><span class="sxs-lookup"><span data-stu-id="7a56b-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="7a56b-111">add_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="7a56b-111">add_DevToolsProtocolEventReceived</span></span>](#add_devtoolsprotocoleventreceived) | <span data-ttu-id="7a56b-112">Подпишитесь на событие DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="7a56b-112">Subscribe to a DevToolsProtocol event.</span></span>
[<span data-ttu-id="7a56b-113">remove_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="7a56b-113">remove_DevToolsProtocolEventReceived</span></span>](#remove_devtoolsprotocoleventreceived) | <span data-ttu-id="7a56b-114">Удалите обработчик событий, добавленный ранее add_DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="7a56b-114">Remove an event handler previously added with add_DevToolsProtocolEventReceived.</span></span>

<span data-ttu-id="7a56b-115">Получить из объекта WebView через GetDevToolsProtocolEventReceiver.</span><span class="sxs-lookup"><span data-stu-id="7a56b-115">Obtained from the WebView object via GetDevToolsProtocolEventReceiver.</span></span>

## <span data-ttu-id="7a56b-116">Участников</span><span class="sxs-lookup"><span data-stu-id="7a56b-116">Members</span></span>

#### <span data-ttu-id="7a56b-117">add_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="7a56b-117">add_DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="7a56b-118">Подпишитесь на событие DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="7a56b-118">Subscribe to a DevToolsProtocol event.</span></span>

> <span data-ttu-id="7a56b-119">общедоступные значения HRESULT [add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived)(обработчик[ICoreWebView2DevToolsProtocolEventReceivedEventHandler](ICoreWebView2DevToolsProtocolEventReceivedEventHandler.md) \*, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="7a56b-119">public HRESULT [add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived)([ICoreWebView2DevToolsProtocolEventReceivedEventHandler](ICoreWebView2DevToolsProtocolEventReceivedEventHandler.md) \* handler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="7a56b-120">Метод Invoke обработчика вызывается каждый раз, когда будет срабатывать соответствующее событие DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="7a56b-120">The handler's Invoke method will be called whenever the corresponding DevToolsProtocol event fires.</span></span> <span data-ttu-id="7a56b-121">Вызов вызывается с помощью объекта args события, содержащего объект Parameter события протокола DevTools в виде строки JSON.</span><span class="sxs-lookup"><span data-stu-id="7a56b-121">Invoke will be called with the an event args object containing the DevTools Protocol event's parameter object as a JSON string.</span></span>

```cpp
// Prompt the user to name a CDP event, and then subscribe to that event.
void ScriptComponent::SubscribeToCdpEvent()
{
    TextInputDialog dialog(
        m_appWindow->GetMainWindow(),
        L"Subscribe to CDP Event",
        L"CDP event name:",
        L"Enter the name of the CDP event to subscribe to.\r\n"
            L"You may also have to call the \"enable\" method of the\r\n"
            L"event's domain to receive events (for example \"Log.enable\").\r\n",
        L"Log.entryAdded");
    if (dialog.confirmed)
    {
        std::wstring eventName = dialog.input;
        wil::com_ptr<ICoreWebView2DevToolsProtocolEventReceiver> receiver;
        CHECK_FAILURE(
            m_webView->GetDevToolsProtocolEventReceiver(eventName.c_str(), &receiver));

        // If we are already subscribed to this event, unsubscribe first.
        auto preexistingToken = m_devToolsProtocolEventReceivedTokenMap.find(eventName);
        if (preexistingToken != m_devToolsProtocolEventReceivedTokenMap.end())
        {
            CHECK_FAILURE(receiver->remove_DevToolsProtocolEventReceived(
                preexistingToken->second));
        }

        CHECK_FAILURE(receiver->add_DevToolsProtocolEventReceived(
            Callback<ICoreWebView2DevToolsProtocolEventReceivedEventHandler>(
                [eventName](
                    ICoreWebView2* sender,
                    ICoreWebView2DevToolsProtocolEventReceivedEventArgs* args) -> HRESULT {
                    wil::unique_cotaskmem_string parameterObjectAsJson;
                    CHECK_FAILURE(args->get_ParameterObjectAsJson(&parameterObjectAsJson));
                    MessageBox(
                        nullptr, parameterObjectAsJson.get(),
                        (L"CDP Event Fired: " + eventName).c_str(), MB_OK);
                    return S_OK;
                })
                .Get(),
            &m_devToolsProtocolEventReceivedTokenMap[eventName]));
    }
}
```

#### <span data-ttu-id="7a56b-122">remove_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="7a56b-122">remove_DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="7a56b-123">Удалите обработчик событий, добавленный ранее add_DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="7a56b-123">Remove an event handler previously added with add_DevToolsProtocolEventReceived.</span></span>

> <span data-ttu-id="7a56b-124">общедоступные значения HRESULT [remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="7a56b-124">public HRESULT [remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived)(EventRegistrationToken token)</span></span>

