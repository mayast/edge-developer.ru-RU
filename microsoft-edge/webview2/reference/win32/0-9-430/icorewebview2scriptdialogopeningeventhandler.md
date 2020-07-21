---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2ScriptDialogOpeningEventHandler
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 31fea451b377b86eda0055a1074706ea12d9538e
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884024"
---
# <span data-ttu-id="13bbb-104">0.9.430-Interface ICoreWebView2ScriptDialogOpeningEventHandler</span><span class="sxs-lookup"><span data-stu-id="13bbb-104">0.9.430 - interface ICoreWebView2ScriptDialogOpeningEventHandler</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ScriptDialogOpeningEventHandler
  : public IUnknown
```

<span data-ttu-id="13bbb-105">Вызывающий объект реализует этот интерфейс для получения события ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="13bbb-105">The caller implements this interface to receive the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="13bbb-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="13bbb-106">Summary</span></span>

 <span data-ttu-id="13bbb-107">Участников</span><span class="sxs-lookup"><span data-stu-id="13bbb-107">Members</span></span>                        | <span data-ttu-id="13bbb-108">Описания</span><span class="sxs-lookup"><span data-stu-id="13bbb-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="13bbb-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="13bbb-109">Invoke</span></span>](#invoke) | <span data-ttu-id="13bbb-110">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="13bbb-110">Called to provide the implementer with the event args for the corresponding event.</span></span>

## <span data-ttu-id="13bbb-111">Участников</span><span class="sxs-lookup"><span data-stu-id="13bbb-111">Members</span></span>

#### <span data-ttu-id="13bbb-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="13bbb-112">Invoke</span></span> 

<span data-ttu-id="13bbb-113">Вызывается для предоставления средству реализации аргументов события для соответствующего события.</span><span class="sxs-lookup"><span data-stu-id="13bbb-113">Called to provide the implementer with the event args for the corresponding event.</span></span>

> <span data-ttu-id="13bbb-114">Открытый [вызов](#invoke)HRESULT ([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2ScriptDialogOpeningEventArgs](ICoreWebView2ScriptDialogOpeningEventArgs.md) \* args)</span><span class="sxs-lookup"><span data-stu-id="13bbb-114">public HRESULT [Invoke](#invoke)([ICoreWebView2](ICoreWebView2.md) \* sender,[ICoreWebView2ScriptDialogOpeningEventArgs](ICoreWebView2ScriptDialogOpeningEventArgs.md) \* args)</span></span>

