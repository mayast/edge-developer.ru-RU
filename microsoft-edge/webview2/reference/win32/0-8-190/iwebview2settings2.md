---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2Settings2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 4ba0299f3afbc6fc2846481f52c1000cd338ecd8
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885788"
---
# <span data-ttu-id="15de6-104">0.8.355-Interface IWebView2Settings2</span><span class="sxs-lookup"><span data-stu-id="15de6-104">0.8.355 - interface IWebView2Settings2</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2Settings2
  : public IWebView2Settings
```

<span data-ttu-id="15de6-105">Определяет свойства, которые включают, отключают или изменяют функции WebView.</span><span class="sxs-lookup"><span data-stu-id="15de6-105">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="15de6-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="15de6-106">Summary</span></span>

 <span data-ttu-id="15de6-107">Участников</span><span class="sxs-lookup"><span data-stu-id="15de6-107">Members</span></span>                        | <span data-ttu-id="15de6-108">Описания</span><span class="sxs-lookup"><span data-stu-id="15de6-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="15de6-109">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="15de6-109">get_AreDefaultContextMenusEnabled</span></span>](#get_aredefaultcontextmenusenabled) | <span data-ttu-id="15de6-110">Свойство AreDefaultContextMenusEnabled используется для предотвращения отображения контекстных меню по умолчанию для пользователя в WebView.</span><span class="sxs-lookup"><span data-stu-id="15de6-110">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>
[<span data-ttu-id="15de6-111">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="15de6-111">put_AreDefaultContextMenusEnabled</span></span>](#put_aredefaultcontextmenusenabled) | <span data-ttu-id="15de6-112">Задайте свойство AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="15de6-112">Set the AreDefaultContextMenusEnabled property.</span></span>

<span data-ttu-id="15de6-113">Изменения, внесенные после события NavigationStarting, будут применены только к следующему элементу навигации верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="15de6-113">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="15de6-114">Участников</span><span class="sxs-lookup"><span data-stu-id="15de6-114">Members</span></span>

#### <span data-ttu-id="15de6-115">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="15de6-115">get_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="15de6-116">Свойство AreDefaultContextMenusEnabled используется для предотвращения отображения контекстных меню по умолчанию для пользователя в WebView.</span><span class="sxs-lookup"><span data-stu-id="15de6-116">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>

> <span data-ttu-id="15de6-117">общедоступные значения HRESULT [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(логический \* включен)</span><span class="sxs-lookup"><span data-stu-id="15de6-117">public HRESULT [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="15de6-118">По умолчанию используется значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="15de6-118">Defaults to TRUE.</span></span>

```cpp
            BOOL allowContextMenus;
            CHECK_FAILURE(m_settings->get_AreDefaultContextMenusEnabled(
                &allowContextMenus));
            if (allowContextMenus) {
                CHECK_FAILURE(m_settings->put_AreDefaultContextMenusEnabled(FALSE));
                MessageBox(nullptr,
                L"Context menus will be disabled after the next navigation.",
                L"Settings change", MB_OK);
            }
            else {
                CHECK_FAILURE(m_settings->put_AreDefaultContextMenusEnabled(TRUE));
                MessageBox(nullptr,
                    L"Context menus will be enabled after the next navigation.",
                    L"Settings change", MB_OK);
            }
```

#### <span data-ttu-id="15de6-119">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="15de6-119">put_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="15de6-120">Задайте свойство AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="15de6-120">Set the AreDefaultContextMenusEnabled property.</span></span>

> <span data-ttu-id="15de6-121">общедоступные значения HRESULT [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(логический параметр включен)</span><span class="sxs-lookup"><span data-stu-id="15de6-121">public HRESULT [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(BOOL enabled)</span></span>

