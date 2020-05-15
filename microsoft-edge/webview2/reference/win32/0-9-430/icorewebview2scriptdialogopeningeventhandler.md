---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/26/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: a9cc4c9e2bd13509c25fa5f5faaa9fe65634b47b
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654851"
---
# <span data-ttu-id="114ee-104">интерфейс ICoreWebView2ScriptDialogOpeningEventHandler</span><span class="sxs-lookup"><span data-stu-id="114ee-104">interface ICoreWebView2ScriptDialogOpeningEventHandler</span></span> 

> [!NOTE]
> <span data-ttu-id="114ee-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="114ee-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="114ee-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="114ee-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ScriptDialogOpeningEventHandler
  : public IUnknown
```

<span data-ttu-id="114ee-107">Вызывающий объект реализует этот интерфейс для получения события ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="114ee-107">The caller implements this interface to receive the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="114ee-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="114ee-108">Summary</span></span>

 <span data-ttu-id="114ee-109">Участников</span><span class="sxs-lookup"><span data-stu-id="114ee-109">Members</span></span>                        | <span data-ttu-id="114ee-110">Описания</span><span class="sxs-lookup"><span data-stu-id="114ee-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="114ee-111">Invoke</span><span class="sxs-lookup"><span data-stu-id="114ee-111">Invoke</span></span>](#invoke) | <span data-ttu-id="114ee-112">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="114ee-112">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="114ee-113">Участников</span><span class="sxs-lookup"><span data-stu-id="114ee-113">Members</span></span>

#### <span data-ttu-id="114ee-114">Invoke</span><span class="sxs-lookup"><span data-stu-id="114ee-114">Invoke</span></span> 

<span data-ttu-id="114ee-115">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="114ee-115">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="114ee-116">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2ScriptDialogOpeningEventArgs](ICoreWebView2ScriptDialogOpeningEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="114ee-116">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2ScriptDialogOpeningEventArgs](ICoreWebView2ScriptDialogOpeningEventArgs.md) \* args)</span></span>

