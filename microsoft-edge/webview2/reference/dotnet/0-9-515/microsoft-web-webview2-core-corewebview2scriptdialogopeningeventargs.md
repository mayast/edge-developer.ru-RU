---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2ScriptDialogOpeningEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 4e7cd20b982d829be6d304eea1f3f60759cc503f
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884857"
---
# <span data-ttu-id="531f0-104">класс 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="531f0-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2ScriptDialogOpeningEventArgs class</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

<span data-ttu-id="531f0-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="531f0-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="531f0-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="531f0-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="531f0-107">Аргументы события для события ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="531f0-107">Event args for the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="531f0-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="531f0-108">Summary</span></span>

 <span data-ttu-id="531f0-109">Участников</span><span class="sxs-lookup"><span data-stu-id="531f0-109">Members</span></span>                        | <span data-ttu-id="531f0-110">Описания</span><span class="sxs-lookup"><span data-stu-id="531f0-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="531f0-111">DefaultText</span><span class="sxs-lookup"><span data-stu-id="531f0-111">DefaultText</span></span>](#defaulttext) | <span data-ttu-id="531f0-112">Второй параметр, передаваемый диалоговому окну запроса JavaScript.</span><span class="sxs-lookup"><span data-stu-id="531f0-112">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="531f0-113">Любые</span><span class="sxs-lookup"><span data-stu-id="531f0-113">Kind</span></span>](#kind) | <span data-ttu-id="531f0-114">Диалоговое окно "вида JavaScript".</span><span class="sxs-lookup"><span data-stu-id="531f0-114">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="531f0-115">Сообщение</span><span class="sxs-lookup"><span data-stu-id="531f0-115">Message</span></span>](#message) | <span data-ttu-id="531f0-116">Сообщение в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="531f0-116">The message of the dialog box.</span></span>
[<span data-ttu-id="531f0-117">ResultText</span><span class="sxs-lookup"><span data-stu-id="531f0-117">ResultText</span></span>](#resulttext) | <span data-ttu-id="531f0-118">Возвращаемое значение функции Prompt для JavaScript при вызове метода "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="531f0-118">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="531f0-119">Универсальный код ресурса (URI)</span><span class="sxs-lookup"><span data-stu-id="531f0-119">Uri</span></span>](#uri) | <span data-ttu-id="531f0-120">URI страницы, запросившего диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="531f0-120">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="531f0-121">Принять</span><span class="sxs-lookup"><span data-stu-id="531f0-121">Accept</span></span>](#accept) | <span data-ttu-id="531f0-122">Основное приложение может вызвать этот метод, чтобы ответить с помощью команды "ОК" для подтверждения, запроса и beforeunload диалоговых окон или вызова этого метода для указания отмены.</span><span class="sxs-lookup"><span data-stu-id="531f0-122">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="531f0-123">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="531f0-123">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="531f0-124">Для возврата объекта CoreWebView2Deferral можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="531f0-124">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

## <span data-ttu-id="531f0-125">Участников</span><span class="sxs-lookup"><span data-stu-id="531f0-125">Members</span></span>

#### <span data-ttu-id="531f0-126">DefaultText</span><span class="sxs-lookup"><span data-stu-id="531f0-126">DefaultText</span></span> 

<span data-ttu-id="531f0-127">Второй параметр, передаваемый диалоговому окну запроса JavaScript.</span><span class="sxs-lookup"><span data-stu-id="531f0-127">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="531f0-128">общедоступная строка [DefaultText](#defaulttext)</span><span class="sxs-lookup"><span data-stu-id="531f0-128">public string [DefaultText](#defaulttext)</span></span>

<span data-ttu-id="531f0-129">Это значение по умолчанию, используемое в качестве результата функции JavaScript "prompt".</span><span class="sxs-lookup"><span data-stu-id="531f0-129">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="531f0-130">Любые</span><span class="sxs-lookup"><span data-stu-id="531f0-130">Kind</span></span> 

<span data-ttu-id="531f0-131">Диалоговое окно "вида JavaScript".</span><span class="sxs-lookup"><span data-stu-id="531f0-131">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="531f0-132">общедоступный [CoreWebView2ScriptDialogKind](#kind)</span><span class="sxs-lookup"><span data-stu-id="531f0-132">public CoreWebView2ScriptDialogKind [Kind](#kind)</span></span>

<span data-ttu-id="531f0-133">Приняв, подтвердите, запросите или beforeunload.</span><span class="sxs-lookup"><span data-stu-id="531f0-133">Accept, confirm, prompt, or beforeunload.</span></span>

#### <span data-ttu-id="531f0-134">Сообщение</span><span class="sxs-lookup"><span data-stu-id="531f0-134">Message</span></span> 

<span data-ttu-id="531f0-135">Сообщение в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="531f0-135">The message of the dialog box.</span></span>

> <span data-ttu-id="531f0-136">[сообщение](#message) общедоступной строки</span><span class="sxs-lookup"><span data-stu-id="531f0-136">public string [Message](#message)</span></span>

<span data-ttu-id="531f0-137">Из JavaScript это первый параметр, передаваемый в Alert, Confirm и Prompt, и он пуст для beforeunload.</span><span class="sxs-lookup"><span data-stu-id="531f0-137">From JavaScript this is the first parameter passed to alert, confirm, and prompt and is empty for beforeunload.</span></span>

#### <span data-ttu-id="531f0-138">ResultText</span><span class="sxs-lookup"><span data-stu-id="531f0-138">ResultText</span></span> 

<span data-ttu-id="531f0-139">Возвращаемое значение функции Prompt для JavaScript при вызове метода "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="531f0-139">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="531f0-140">общедоступная строка [ResultText](#resulttext)</span><span class="sxs-lookup"><span data-stu-id="531f0-140">public string [ResultText](#resulttext)</span></span>

<span data-ttu-id="531f0-141">Этот тип игнорируется, если диалоговое окно не является запросом.</span><span class="sxs-lookup"><span data-stu-id="531f0-141">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="531f0-142">Если параметр "принято" не вызывается, это значение игнорируется, и в командной строке возвращается значение "ложь".</span><span class="sxs-lookup"><span data-stu-id="531f0-142">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="531f0-143">Универсальный код ресурса (URI)</span><span class="sxs-lookup"><span data-stu-id="531f0-143">Uri</span></span> 

<span data-ttu-id="531f0-144">URI страницы, запросившего диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="531f0-144">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="531f0-145">[URI](#uri) общедоступной строки</span><span class="sxs-lookup"><span data-stu-id="531f0-145">public string [Uri](#uri)</span></span>

#### <span data-ttu-id="531f0-146">Принять</span><span class="sxs-lookup"><span data-stu-id="531f0-146">Accept</span></span> 

<span data-ttu-id="531f0-147">Основное приложение может вызвать этот метод, чтобы ответить с помощью команды "ОК" для подтверждения, запроса и beforeunload диалоговых окон или вызова этого метода для указания отмены.</span><span class="sxs-lookup"><span data-stu-id="531f0-147">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="531f0-148">общедоступная отмена [приема](#accept)()</span><span class="sxs-lookup"><span data-stu-id="531f0-148">public void [Accept](#accept)()</span></span>

<span data-ttu-id="531f0-149">Из JavaScript это означает, что функция Confirm и beforeunload возвращает значение истина, если вызывается метод принятии.</span><span class="sxs-lookup"><span data-stu-id="531f0-149">From JavaScript, this means that the confirm and beforeunload function returns true if Accept is called.</span></span> <span data-ttu-id="531f0-150">И для функции Prompt она возвращает значение ResultText, если вызывается метод допуска, и возвращает значение false в противном случае.</span><span class="sxs-lookup"><span data-stu-id="531f0-150">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="531f0-151">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="531f0-151">GetDeferral</span></span> 

<span data-ttu-id="531f0-152">Для возврата объекта CoreWebView2Deferral можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="531f0-152">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

> <span data-ttu-id="531f0-153">общедоступный CoreWebView2Deferral- [РБП](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="531f0-153">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="531f0-154">Вы можете использовать этот параметр, чтобы выполнить событие позже.</span><span class="sxs-lookup"><span data-stu-id="531f0-154">You can use this to complete the event at a later time.</span></span>

