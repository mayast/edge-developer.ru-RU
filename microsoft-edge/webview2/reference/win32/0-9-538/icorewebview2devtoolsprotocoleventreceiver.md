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
# 0.9.579-Interface ICoreWebView2DevToolsProtocolEventReceiver 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2DevToolsProtocolEventReceiver
  : public IUnknown
```

Получатель создается для определенного события протокола DevTools и позволяет подписаться на него и отказаться от него.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived) | Подпишитесь на событие DevToolsProtocol.
[remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived) | Удалите обработчик событий, добавленный ранее add_DevToolsProtocolEventReceived.

Получить из объекта WebView через GetDevToolsProtocolEventReceiver.

## Участников

#### add_DevToolsProtocolEventReceived 

Подпишитесь на событие DevToolsProtocol.

> общедоступные значения HRESULT [add_DevToolsProtocolEventReceived](#add_devtoolsprotocoleventreceived)(обработчик[ICoreWebView2DevToolsProtocolEventReceivedEventHandler](icorewebview2devtoolsprotocoleventreceivedeventhandler.md) *, EventRegistrationToken * token)

Метод Invoke обработчика вызывается каждый раз, когда будет срабатывать соответствующее событие DevToolsProtocol. Вызов вызывается с помощью объекта аргументов события, содержащего объект Parameter события протокола DevTools в виде строки JSON.

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

#### remove_DevToolsProtocolEventReceived 

Удалите обработчик событий, добавленный ранее add_DevToolsProtocolEventReceived.

> общедоступные значения HRESULT [remove_DevToolsProtocolEventReceived](#remove_devtoolsprotocoleventreceived)(маркер EventRegistrationToken)

