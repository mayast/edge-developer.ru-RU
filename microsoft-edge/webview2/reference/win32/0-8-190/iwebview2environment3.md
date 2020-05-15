---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/09/2019
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 43becb7f4ec9903557ccd558319e233266ac2ea1
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654696"
---
# <span data-ttu-id="f5dd7-104">интерфейс IWebView2Environment3</span><span class="sxs-lookup"><span data-stu-id="f5dd7-104">interface IWebView2Environment3</span></span> 

> [!NOTE]
> <span data-ttu-id="f5dd7-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="f5dd7-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="f5dd7-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="f5dd7-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2Environment3
  : public IWebView2Environment2
```

<span data-ttu-id="f5dd7-107">Дополнительные функции, реализованные с помощью объекта Environment.</span><span class="sxs-lookup"><span data-stu-id="f5dd7-107">Additional functionality implemented by the Environment object.</span></span>

## <span data-ttu-id="f5dd7-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="f5dd7-108">Summary</span></span>

 <span data-ttu-id="f5dd7-109">Участников</span><span class="sxs-lookup"><span data-stu-id="f5dd7-109">Members</span></span>                        | <span data-ttu-id="f5dd7-110">Описания</span><span class="sxs-lookup"><span data-stu-id="f5dd7-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f5dd7-111">add_NewVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="f5dd7-111">add_NewVersionAvailable</span></span>](#add_newversionavailable) | <span data-ttu-id="f5dd7-112">Событие NewVersionAvailable активируется, когда установлена более новая версия браузера EDGE и доступна для использования через WebView2.</span><span class="sxs-lookup"><span data-stu-id="f5dd7-112">The NewVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>
[<span data-ttu-id="f5dd7-113">remove_NewVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="f5dd7-113">remove_NewVersionAvailable</span></span>](#remove_newversionavailable) | <span data-ttu-id="f5dd7-114">Удалите обработчик событий, добавленный ранее add_NewVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="f5dd7-114">Remove an event handler previously added with add_NewVersionAvailable.</span></span>

<span data-ttu-id="f5dd7-115">Дополнительные сведения вы видите в интерфейсе [IWebView2Environment](IWebView2Environment.md) .</span><span class="sxs-lookup"><span data-stu-id="f5dd7-115">See the [IWebView2Environment](IWebView2Environment.md) interface for more details.</span></span> <span data-ttu-id="f5dd7-116">Вы можете QueryInterface для этого интерфейса из объекта, реализующего [IWebView2Environment](IWebView2Environment.md).</span><span class="sxs-lookup"><span data-stu-id="f5dd7-116">You can QueryInterface for this interface from the object that implements [IWebView2Environment](IWebView2Environment.md).</span></span>

## <span data-ttu-id="f5dd7-117">Участников</span><span class="sxs-lookup"><span data-stu-id="f5dd7-117">Members</span></span>

#### <span data-ttu-id="f5dd7-118">add_NewVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="f5dd7-118">add_NewVersionAvailable</span></span> 

<span data-ttu-id="f5dd7-119">Событие NewVersionAvailable активируется, когда установлена более новая версия браузера EDGE и доступна для использования через WebView2.</span><span class="sxs-lookup"><span data-stu-id="f5dd7-119">The NewVersionAvailable event fires when a newer version of the Edge browser is installed and available to use via WebView2.</span></span>

> <span data-ttu-id="f5dd7-120">общедоступные значения HRESULT [add_NewVersionAvailable](#add_newversionavailable)([IWebView2NewVersionAvailableEventHandler](IWebView2NewVersionAvailableEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="f5dd7-120">public HRESULT [add_NewVersionAvailable](#add_newversionavailable)([IWebView2NewVersionAvailableEventHandler](IWebView2NewVersionAvailableEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="f5dd7-121">Для использования более новой версии браузера необходимо создать новый [IWebView2Environment](IWebView2Environment.md) и [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="f5dd7-121">To use the newer version of the browser you must create a new [IWebView2Environment](IWebView2Environment.md) and [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="f5dd7-122">Событие будет инициировано только для новой версии из того же канала, из которого выполняется код.</span><span class="sxs-lookup"><span data-stu-id="f5dd7-122">Event will only be fired for new version from the same Edge channel that the code is running from.</span></span> <span data-ttu-id="f5dd7-123">Если вы не используете установленный EDGE, событие не срабатывает.</span><span class="sxs-lookup"><span data-stu-id="f5dd7-123">When not running with installed Edge, no event will be fired.</span></span>

<span data-ttu-id="f5dd7-124">Поскольку папка данных пользователя может использоваться только одним процессом браузера, если вы хотите использовать одну и ту же папку данных пользователя в веб-представлении с помощью новой версии браузера, необходимо сначала закрыть [IWebView2Environment](IWebView2Environment.md) и IWebView2WebViews, которые используют более старую версию браузера.</span><span class="sxs-lookup"><span data-stu-id="f5dd7-124">Because a user data folder can only be used by one browser process at a time, if you want to use the same user data folder in the WebViews using the new version of the browser, you must close the [IWebView2Environment](IWebView2Environment.md) and IWebView2WebViews that are using the older version of the browser first.</span></span> <span data-ttu-id="f5dd7-125">Или просто запросите пользователя перезапустить приложение.</span><span class="sxs-lookup"><span data-stu-id="f5dd7-125">Or simply prompt the user to restart the app.</span></span>

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

#### <span data-ttu-id="f5dd7-126">remove_NewVersionAvailable</span><span class="sxs-lookup"><span data-stu-id="f5dd7-126">remove_NewVersionAvailable</span></span> 

<span data-ttu-id="f5dd7-127">Удалите обработчик событий, добавленный ранее add_NewVersionAvailable.</span><span class="sxs-lookup"><span data-stu-id="f5dd7-127">Remove an event handler previously added with add_NewVersionAvailable.</span></span>

> <span data-ttu-id="f5dd7-128">общедоступные значения HRESULT [remove_NewVersionAvailable](#remove_newversionavailable)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="f5dd7-128">public HRESULT [remove_NewVersionAvailable](#remove_newversionavailable)(EventRegistrationToken token)</span></span>

