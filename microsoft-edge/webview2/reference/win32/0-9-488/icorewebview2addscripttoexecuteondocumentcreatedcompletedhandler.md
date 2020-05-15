---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/28/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: e9f98b43463fe5259d2f9f723b62b78c1d1a4758
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654916"
---
# <span data-ttu-id="86e57-104">интерфейс ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span><span class="sxs-lookup"><span data-stu-id="86e57-104">interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler</span></span> 

```
interface ICoreWebView2AddScriptToExecuteOnDocumentCreatedCompletedHandler
  : public IUnknown
```

<span data-ttu-id="86e57-105">Вызывающий объект реализует этот интерфейс, чтобы получить результат метода AddScriptToExecuteOnDocumentCreated.</span><span class="sxs-lookup"><span data-stu-id="86e57-105">The caller implements this interface to receive the result of the AddScriptToExecuteOnDocumentCreated method.</span></span>

## <span data-ttu-id="86e57-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="86e57-106">Summary</span></span>

 <span data-ttu-id="86e57-107">Участников</span><span class="sxs-lookup"><span data-stu-id="86e57-107">Members</span></span>                        | <span data-ttu-id="86e57-108">Описания</span><span class="sxs-lookup"><span data-stu-id="86e57-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="86e57-109">Invoke</span><span class="sxs-lookup"><span data-stu-id="86e57-109">Invoke</span></span>](#invoke) | <span data-ttu-id="86e57-110">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="86e57-110">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

## <span data-ttu-id="86e57-111">Участников</span><span class="sxs-lookup"><span data-stu-id="86e57-111">Members</span></span>

#### <span data-ttu-id="86e57-112">Invoke</span><span class="sxs-lookup"><span data-stu-id="86e57-112">Invoke</span></span> 

<span data-ttu-id="86e57-113">Вызывается для предоставления разработчику состояния завершения и результата соответствующего асинхронного вызова метода.</span><span class="sxs-lookup"><span data-stu-id="86e57-113">Called to provide the implementer with the completion status and result of the corresponding asynchronous method call.</span></span>

> <span data-ttu-id="86e57-114">общедоступный [вызов](#invoke)HRESULT (ErrorCode код_ошибки, ИД LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="86e57-114">public HRESULT [Invoke](#invoke)(HRESULT errorCode, LPCWSTR id)</span></span>

