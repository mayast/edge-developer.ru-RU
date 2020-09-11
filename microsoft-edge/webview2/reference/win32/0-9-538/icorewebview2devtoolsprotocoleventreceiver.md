---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: 0.9.579-WebView2 Win32 C++ ICoreWebView2DevToolsProtocolEventReceiver
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2DevToolsProtocolEventReceiver
ms.openlocfilehash: 8b6076842e6670d425be563687c18d312afd69d7
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010259"
---
# <span data-ttu-id="e304a-104">0.9.579-Interface ICoreWebView2DevToolsProtocolEventReceiver</span><span class="sxs-lookup"><span data-stu-id="e304a-104">0.9.579 - interface ICoreWebView2DevToolsProtocolEventReceiver</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2DevToolsProtocolEventReceiver
  : public IUnknown
```

<span data-ttu-id="e304a-105">Получатель создается для определенного события протокола DevTools и позволяет подписаться на него и отказаться от него.</span><span class="sxs-lookup"><span data-stu-id="e304a-105">A Receiver is created for a particular DevTools Protocol event and allows you to subscribe and unsubscribe from that event.</span></span>

## <span data-ttu-id="e304a-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="e304a-106">Summary</span></span>

 <span data-ttu-id="e304a-107">Участников</span><span class="sxs-lookup"><span data-stu-id="e304a-107">Members</span></span>                        | <span data-ttu-id="e304a-108">Описания</span><span class="sxs-lookup"><span data-stu-id="e304a-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="e304a-109">add_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="e304a-109">add_DevToolsProtocolEventReceived</span></span>](#add_devtoolsprotocoleventreceived) | <span data-ttu-id="e304a-110">Подпишитесь на событие DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="e304a-110">Subscribe to a DevToolsProtocol event.</span></span>
[<span data-ttu-id="e304a-111">remove_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="e304a-111">remove_DevToolsProtocolEventReceived</span></span>](#remove_devtoolsprotocoleventreceived) | <span data-ttu-id="e304a-112">Удалите обработчик событий, добавленный ранее add_DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="e304a-112">Remove an event handler previously added with add_DevToolsProtocolEventReceived.</span></span>

<span data-ttu-id="e304a-113">Получить из объекта WebView через GetDevToolsProtocolEventReceiver.</span><span class="sxs-lookup"><span data-stu-id="e304a-113">Obtained from the WebView object via GetDevToolsProtocolEventReceiver.</span></span>

## <span data-ttu-id="e304a-114">Участников</span><span class="sxs-lookup"><span data-stu-id="e304a-114">Members</span></span>

#### <span data-ttu-id="e304a-115">add_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="e304a-115">add_DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="e304a-116">Подпишитесь на событие DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="e304a-116">Subscribe to a DevToolsProtocol event.</span></span>

> <span data-ttu-id="e304a-117">общедоступные значения HRESULT [add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived)(обработчик[ICoreWebView2DevToolsProtocolEventReceivedEventHandler](icorewebview2devtoolsprotocoleventreceivedeventhandler.md) \*, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="e304a-117">public HRESULT [add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived)([ICoreWebView2DevToolsProtocolEventReceivedEventHandler](icorewebview2devtoolsprotocoleventreceivedeventhandler.md) \* handler, EventRegistrationToken \* token)</span></span>

<span data-ttu-id="e304a-118">Метод Invoke обработчика вызывается каждый раз, когда будет срабатывать соответствующее событие DevToolsProtocol.</span><span class="sxs-lookup"><span data-stu-id="e304a-118">The handler's Invoke method will be called whenever the corresponding DevToolsProtocol event fires.</span></span> <span data-ttu-id="e304a-119">Вызов вызывается с помощью объекта аргументов события, содержащего объект Parameter события протокола DevTools в виде строки JSON.</span><span class="sxs-lookup"><span data-stu-id="e304a-119">Invoke will be called with an event args object containing the DevTools Protocol event's parameter object as a JSON string.</span></span>

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

#### <span data-ttu-id="e304a-120">remove_DevToolsProtocolEventReceived</span><span class="sxs-lookup"><span data-stu-id="e304a-120">remove_DevToolsProtocolEventReceived</span></span> 

<span data-ttu-id="e304a-121">Удалите обработчик событий, добавленный ранее add_DevToolsProtocolEventReceived.</span><span class="sxs-lookup"><span data-stu-id="e304a-121">Remove an event handler previously added with add_DevToolsProtocolEventReceived.</span></span>

> <span data-ttu-id="e304a-122">общедоступные значения HRESULT [remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="e304a-122">public HRESULT [remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived)(EventRegistrationToken token)</span></span>

