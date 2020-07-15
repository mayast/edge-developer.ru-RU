---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2Settings2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 4e9f1d7baadcb20774bd4816f043f71a1a8b50b8
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878206"
---
# <span data-ttu-id="65736-104">0.8.355-Interface IWebView2Settings2</span><span class="sxs-lookup"><span data-stu-id="65736-104">0.8.355 - interface IWebView2Settings2</span></span> 

> [!NOTE]
> <span data-ttu-id="65736-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="65736-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="65736-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="65736-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2Settings2
  : public IWebView2Settings
```

<span data-ttu-id="65736-107">Определяет свойства, которые включают, отключают или изменяют функции WebView.</span><span class="sxs-lookup"><span data-stu-id="65736-107">Defines properties that enable, disable, or modify WebView features.</span></span>

## <span data-ttu-id="65736-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="65736-108">Summary</span></span>

 <span data-ttu-id="65736-109">Участников</span><span class="sxs-lookup"><span data-stu-id="65736-109">Members</span></span>                        | <span data-ttu-id="65736-110">Описания</span><span class="sxs-lookup"><span data-stu-id="65736-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="65736-111">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="65736-111">get_AreDefaultContextMenusEnabled</span></span>](#get_aredefaultcontextmenusenabled) | <span data-ttu-id="65736-112">Свойство AreDefaultContextMenusEnabled используется для предотвращения отображения контекстных меню по умолчанию для пользователя в WebView.</span><span class="sxs-lookup"><span data-stu-id="65736-112">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>
[<span data-ttu-id="65736-113">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="65736-113">put_AreDefaultContextMenusEnabled</span></span>](#put_aredefaultcontextmenusenabled) | <span data-ttu-id="65736-114">Задайте свойство AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="65736-114">Set the AreDefaultContextMenusEnabled property.</span></span>

<span data-ttu-id="65736-115">Изменения, внесенные после события NavigationStarting, будут применены только к следующему элементу навигации верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="65736-115">Setting changes made after NavigationStarting event will not apply until the next top level navigation.</span></span>

## <span data-ttu-id="65736-116">Участников</span><span class="sxs-lookup"><span data-stu-id="65736-116">Members</span></span>

#### <span data-ttu-id="65736-117">get_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="65736-117">get_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="65736-118">Свойство AreDefaultContextMenusEnabled используется для предотвращения отображения контекстных меню по умолчанию для пользователя в WebView.</span><span class="sxs-lookup"><span data-stu-id="65736-118">The AreDefaultContextMenusEnabled property is used to prevent default context menus from being shown to user in webview.</span></span>

> <span data-ttu-id="65736-119">общедоступные значения HRESULT [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(логический \* включен)</span><span class="sxs-lookup"><span data-stu-id="65736-119">public HRESULT [get_AreDefaultContextMenusEnabled](#get_aredefaultcontextmenusenabled)(BOOL \* enabled)</span></span>

<span data-ttu-id="65736-120">По умолчанию используется значение TRUE.</span><span class="sxs-lookup"><span data-stu-id="65736-120">Defaults to TRUE.</span></span>

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

#### <span data-ttu-id="65736-121">put_AreDefaultContextMenusEnabled</span><span class="sxs-lookup"><span data-stu-id="65736-121">put_AreDefaultContextMenusEnabled</span></span> 

<span data-ttu-id="65736-122">Задайте свойство AreDefaultContextMenusEnabled.</span><span class="sxs-lookup"><span data-stu-id="65736-122">Set the AreDefaultContextMenusEnabled property.</span></span>

> <span data-ttu-id="65736-123">общедоступные значения HRESULT [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(логический параметр включен)</span><span class="sxs-lookup"><span data-stu-id="65736-123">public HRESULT [put_AreDefaultContextMenusEnabled](#put_aredefaultcontextmenusenabled)(BOOL enabled)</span></span>

