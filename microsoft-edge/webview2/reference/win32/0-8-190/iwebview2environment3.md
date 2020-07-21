---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2Environment3
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 327a182c5298ed6de6b9e55b407d138857dbe659
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10886096"
---
# <span data-ttu-id="a090e-104">0.8.355-Interface IWebView2Environment3</span><span class="sxs-lookup"><span data-stu-id="a090e-104">0.8.355 - interface IWebView2Environment3</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2Environment3
  : public IWebView2Environment2
```

<span data-ttu-id="a090e-105">Дополнительные функции, реализованные с помощью объекта Environment.</span><span class="sxs-lookup"><span data-stu-id="a090e-105">Additional functionality implemented by the Environment object.</span></span>

## <span data-ttu-id="a090e-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="a090e-106">Summary</span></span>

 <span data-ttu-id="a090e-107">Участников</span><span class="sxs-lookup"><span data-stu-id="a090e-107">Members</span></span>                        | <span data-ttu-id="a090e-108">Описания</span><span class="sxs-lookup"><span data-stu-id="a090e-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="a090e-109">add_NewVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="a090e-109">add_NewVersionAvailable</span></span>](#add_newversionavailable) | <span data-ttu-id="a090e-110">Событие NewVersionAvailable активируется, когда установлена более новая версия браузера EDGE и доступна для использования через WebView2.</span><span class="sxs-lookup"><span data-stu-id="a090e-110">The NewVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>
[<span data-ttu-id="a090e-111">remove_NewVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="a090e-111">remove_NewVersionAvailable</span></span>](#remove_newversionavailable) | <span data-ttu-id="a090e-112">Удалите обработчик событий, добавленный ранее add_NewVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="a090e-112">Remove an event handler previously added with add_NewVersionAvailable.</span></span>

<span data-ttu-id="a090e-113">Дополнительные сведения вы видите в интерфейсе [IWebView2Environment](IWebView2Environment.md) .</span><span class="sxs-lookup"><span data-stu-id="a090e-113">See the [IWebView2Environment](IWebView2Environment.md) interface for more details.</span></span> <span data-ttu-id="a090e-114">Вы можете QueryInterface для этого интерфейса из объекта, реализующего [IWebView2Environment](IWebView2Environment.md).</span><span class="sxs-lookup"><span data-stu-id="a090e-114">You can QueryInterface for this interface from the object that implements [IWebView2Environment](IWebView2Environment.md).</span></span>

## <span data-ttu-id="a090e-115">Участников</span><span class="sxs-lookup"><span data-stu-id="a090e-115">Members</span></span>

#### <span data-ttu-id="a090e-116">add_NewVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="a090e-116">add_NewVersionAvailable</span></span> 

<span data-ttu-id="a090e-117">Событие NewVersionAvailable активируется, когда установлена более новая версия браузера EDGE и доступна для использования через WebView2.</span><span class="sxs-lookup"><span data-stu-id="a090e-117">The NewVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>

> <span data-ttu-id="a090e-118">общедоступные значения HRESULT [add_NewVersionAvailable](#add_newversionavailable)([IWebView2NewVersionAvailableEventHandler](IWebView2NewVersionAvailableEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="a090e-118">public HRESULT [add_NewVersionAvailable](#add_newversionavailable)([IWebView2NewVersionAvailableEventHandler](IWebView2NewVersionAvailableEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="a090e-119">Для использования более новой версии браузера необходимо создать новый [IWebView2Environment](IWebView2Environment.md) и [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="a090e-119">To use the newer version of the browser you must create a new [IWebView2Environment](IWebView2Environment.md) and [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="a090e-120">Событие будет инициировано только для новой версии из того же канала, из которого выполняется код.</span><span class="sxs-lookup"><span data-stu-id="a090e-120">Event will only be fired for new version from the same Edge channel that the code is running from.</span></span> <span data-ttu-id="a090e-121">Если вы не используете установленный EDGE, событие не срабатывает.</span><span class="sxs-lookup"><span data-stu-id="a090e-121">When not running with installed Edge, no event will be fired.</span></span>

<span data-ttu-id="a090e-122">Поскольку папка данных пользователя может использоваться только одним процессом браузера, если вы хотите использовать одну и ту же папку данных пользователя в веб-представлении с помощью новой версии браузера, необходимо сначала закрыть [IWebView2Environment](IWebView2Environment.md) и IWebView2WebViews, которые используют более старую версию браузера.</span><span class="sxs-lookup"><span data-stu-id="a090e-122">Because a user data folder can only be used by one browser process at a time, if you want to use the same user data folder in the WebViews using the new version of the browser, you must close the [IWebView2Environment](IWebView2Environment.md) and IWebView2WebViews that are using the older version of the browser first.</span></span> <span data-ttu-id="a090e-123">Или просто запросите пользователя перезапустить приложение.</span><span class="sxs-lookup"><span data-stu-id="a090e-123">Or simply prompt the user to restart the app.</span></span>

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

#### <span data-ttu-id="a090e-124">remove_NewVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="a090e-124">remove_NewVersionAvailable</span></span> 

<span data-ttu-id="a090e-125">Удалите обработчик событий, добавленный ранее add_NewVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="a090e-125">Remove an event handler previously added with add_NewVersionAvailable.</span></span>

> <span data-ttu-id="a090e-126">общедоступные значения HRESULT [remove_NewVersionAvailable](#remove_newversionavailable)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="a090e-126">public HRESULT [remove_NewVersionAvailable](#remove_newversionavailable)(EventRegistrationToken token)</span></span>

