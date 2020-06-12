---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 9777a27c1b9252d0d1a5f91a4692b9043fffc569
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10699206"
---
# <span data-ttu-id="b1624-104">интерфейс ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="b1624-104">interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span></span> 

```
interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
  : public IUnknown
```

<span data-ttu-id="b1624-105">Вызывающий объект реализует этот интерфейс, чтобы получить результат метода AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="b1624-105">The caller implements this interface to receive the result of the AddScriptToExecuteOnDocumentCreated method.</span></span>

## <span data-ttu-id="b1624-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="b1624-106">Summary</span></span>

 <span data-ttu-id="b1624-107">Участников</span><span class="sxs-lookup"><span data-stu-id="b1624-107">Members</span></span>                        | <span data-ttu-id="b1624-108">Описания</span><span class="sxs-lookup"><span data-stu-id="b1624-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="b1624-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="b1624-109">Invoke</span></span>](#invoke) | <span data-ttu-id="b1624-110">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="b1624-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="b1624-111">Участников</span><span class="sxs-lookup"><span data-stu-id="b1624-111">Members</span></span>

#### <span data-ttu-id="b1624-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="b1624-112">Invoke</span></span> 

<span data-ttu-id="b1624-113">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="b1624-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="b1624-114">общедоступный [вызов](#invoke)HRESULT (ErrorCode код_ошибки, ИД LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="b1624-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR id)</span></span>
