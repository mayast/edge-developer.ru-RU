---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2Environment3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: d16a12aae823c48b7dd4b0b5e8225cdd40c1dafc
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878528"
---
# <span data-ttu-id="3344a-104">0.8.355-Interface IWebView2Environment3</span><span class="sxs-lookup"><span data-stu-id="3344a-104">0.8.355 - interface IWebView2Environment3</span></span> 

> [!NOTE]
> <span data-ttu-id="3344a-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="3344a-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="3344a-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="3344a-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2Environment3
  : public IWebView2Environment2
```

<span data-ttu-id="3344a-107">Дополнительные функции, реализованные с помощью объекта Environment.</span><span class="sxs-lookup"><span data-stu-id="3344a-107">Additional functionality implemented by the Environment object.</span></span>

## <span data-ttu-id="3344a-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="3344a-108">Summary</span></span>

 <span data-ttu-id="3344a-109">Участников</span><span class="sxs-lookup"><span data-stu-id="3344a-109">Members</span></span>                        | <span data-ttu-id="3344a-110">Описания</span><span class="sxs-lookup"><span data-stu-id="3344a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="3344a-111">add_NewVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="3344a-111">add_NewVersionAvailable</span></span>](#add_newversionavailable) | <span data-ttu-id="3344a-112">Событие NewVersionAvailable активируется, когда установлена более новая версия браузера EDGE и доступна для использования через WebView2.</span><span class="sxs-lookup"><span data-stu-id="3344a-112">The NewVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>
[<span data-ttu-id="3344a-113">remove_NewVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="3344a-113">remove_NewVersionAvailable</span></span>](#remove_newversionavailable) | <span data-ttu-id="3344a-114">Удалите обработчик событий, добавленный ранее add_NewVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="3344a-114">Remove an event handler previously added with add_NewVersionAvailable.</span></span>

<span data-ttu-id="3344a-115">Дополнительные сведения вы видите в интерфейсе [IWebView2Environment](IWebView2Environment.md) .</span><span class="sxs-lookup"><span data-stu-id="3344a-115">See the [IWebView2Environment](IWebView2Environment.md) interface for more details.</span></span> <span data-ttu-id="3344a-116">Вы можете QueryInterface для этого интерфейса из объекта, реализующего [IWebView2Environment](IWebView2Environment.md).</span><span class="sxs-lookup"><span data-stu-id="3344a-116">You can QueryInterface for this interface from the object that implements [IWebView2Environment](IWebView2Environment.md).</span></span>

## <span data-ttu-id="3344a-117">Участников</span><span class="sxs-lookup"><span data-stu-id="3344a-117">Members</span></span>

#### <span data-ttu-id="3344a-118">add_NewVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="3344a-118">add_NewVersionAvailable</span></span> 

<span data-ttu-id="3344a-119">Событие NewVersionAvailable активируется, когда установлена более новая версия браузера EDGE и доступна для использования через WebView2.</span><span class="sxs-lookup"><span data-stu-id="3344a-119">The NewVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>

> <span data-ttu-id="3344a-120">общедоступные значения HRESULT [add_NewVersionAvailable](#add_newversionavailable)([IWebView2NewVersionAvailableEventHandler](IWebView2NewVersionAvailableEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="3344a-120">public HRESULT [add_NewVersionAvailable](#add_newversionavailable)([IWebView2NewVersionAvailableEventHandler](IWebView2NewVersionAvailableEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="3344a-121">Для использования более новой версии браузера необходимо создать новый [IWebView2Environment](IWebView2Environment.md) и [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="3344a-121">To use the newer version of the browser you must create a new [IWebView2Environment](IWebView2Environment.md) and [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="3344a-122">Событие будет инициировано только для новой версии из того же канала, из которого выполняется код.</span><span class="sxs-lookup"><span data-stu-id="3344a-122">Event will only be fired for new version from the same Edge channel that the code is running from.</span></span> <span data-ttu-id="3344a-123">Если вы не используете установленный EDGE, событие не срабатывает.</span><span class="sxs-lookup"><span data-stu-id="3344a-123">When not running with installed Edge, no event will be fired.</span></span>

<span data-ttu-id="3344a-124">Поскольку папка данных пользователя может использоваться только одним процессом браузера, если вы хотите использовать одну и ту же папку данных пользователя в веб-представлении с помощью новой версии браузера, необходимо сначала закрыть [IWebView2Environment](IWebView2Environment.md) и IWebView2WebViews, которые используют более старую версию браузера.</span><span class="sxs-lookup"><span data-stu-id="3344a-124">Because a user data folder can only be used by one browser process at a time, if you want to use the same user data folder in the WebViews using the new version of the browser, you must close the [IWebView2Environment](IWebView2Environment.md) and IWebView2WebViews that are using the older version of the browser first.</span></span> <span data-ttu-id="3344a-125">Или просто запросите пользователя перезапустить приложение.</span><span class="sxs-lookup"><span data-stu-id="3344a-125">Or simply prompt the user to restart the app.</span></span>

```cpp
    // After the environment is successfully created,
    // register a handler for the NewVersionAvailable event.
    // This handler tells when there is a new Edge version available on the machine.
    CHECK_FAILURE(m_webViewEnvironment->add_NewVersionAvailable(
        Callback<IWebView2NewVersionAvailableEventHandler>(
            [this](IWebView2Environment* sender, IWebView2NewVersionAvailableEventArgs* args)
                -> HRESULT {
                // Get the version value from args
                wil::unique_cotaskmem_string newVersion;
                CHECK_FAILURE(args->get_NewVersion(&newVersion));
                std::wstring message = L"We detected there is a new version for the browser.";
                message += L"\n\nVersion number: ";
                message += newVersion.get();
                message += L"\n\n";
                if (m_webView)
                {
                    message += L"Do you want to restart the app? \n\n";
                    message += L"Click No if you only want to re-create the webviews. \n";
                    message += L"Click Cancel for no action. \n";
                }
                int response = MessageBox(
                    m_mainWindow, message.c_str(), L"New available version",
                    m_webView ? MB_YESNOCANCEL : MB_OK);

                if (response == IDYES)
                {
                    RestartApp();
                }
                else if (response == IDNO)
                {
                    ReinitializeWebViewWithNewBrowser();
                }
                else
                {
                    // do nothing
                }

                return S_OK;
            })
            .Get(),
        nullptr));
```

#### <span data-ttu-id="3344a-126">remove_NewVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="3344a-126">remove_NewVersionAvailable</span></span> 

<span data-ttu-id="3344a-127">Удалите обработчик событий, добавленный ранее add_NewVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="3344a-127">Remove an event handler previously added with add_NewVersionAvailable.</span></span>

> <span data-ttu-id="3344a-128">общедоступные значения HRESULT [remove_NewVersionAvailable](#remove_newversionavailable)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="3344a-128">public HRESULT [remove_NewVersionAvailable](#remove_newversionavailable)(EventRegistrationToken token)</span></span>

