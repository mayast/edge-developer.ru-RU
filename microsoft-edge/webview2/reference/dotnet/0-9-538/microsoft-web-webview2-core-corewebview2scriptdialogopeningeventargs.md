---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: Microsoft. Web. WebView2. Core. CoreWebView2ScriptDialogOpeningEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: Microsoft. Web. WebView2, "ядро", "WebView2", WebView, DotNet, WPF, WinForms, App, EDGE, CoreWebView2, CoreWebView2Controller, браузерный элемент управления, EDGE HTML, Microsoft. Web. WebView2
ms.openlocfilehash: cbff39e9393026f51471bdfb3189600e2d7bf109
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879697"
---
# <span data-ttu-id="5d4c6-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="5d4c6-104">Microsoft.Web.WebView2.Core.CoreWebView2ScriptDialogOpeningEventArgs class</span></span> 

<span data-ttu-id="5d4c6-105">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="5d4c6-105">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="5d4c6-106">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="5d4c6-106">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="5d4c6-107">Аргументы события для события ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="5d4c6-107">Event args for the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="5d4c6-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="5d4c6-108">Summary</span></span>

 <span data-ttu-id="5d4c6-109">Участников</span><span class="sxs-lookup"><span data-stu-id="5d4c6-109">Members</span></span>                        | <span data-ttu-id="5d4c6-110">Описания</span><span class="sxs-lookup"><span data-stu-id="5d4c6-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="5d4c6-111">DefaultText</span><span class="sxs-lookup"><span data-stu-id="5d4c6-111">DefaultText</span></span>](#defaulttext) | <span data-ttu-id="5d4c6-112">Второй параметр, передаваемый диалоговому окну запроса JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5d4c6-112">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="5d4c6-113">Любые</span><span class="sxs-lookup"><span data-stu-id="5d4c6-113">Kind</span></span>](#kind) | <span data-ttu-id="5d4c6-114">Диалоговое окно "вида JavaScript".</span><span class="sxs-lookup"><span data-stu-id="5d4c6-114">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="5d4c6-115">Сообщение</span><span class="sxs-lookup"><span data-stu-id="5d4c6-115">Message</span></span>](#message) | <span data-ttu-id="5d4c6-116">Сообщение в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="5d4c6-116">The message of the dialog box.</span></span>
[<span data-ttu-id="5d4c6-117">ResultText</span><span class="sxs-lookup"><span data-stu-id="5d4c6-117">ResultText</span></span>](#resulttext) | <span data-ttu-id="5d4c6-118">Возвращаемое значение функции Prompt для JavaScript при вызове метода "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="5d4c6-118">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="5d4c6-119">Универсальный код ресурса (URI)</span><span class="sxs-lookup"><span data-stu-id="5d4c6-119">Uri</span></span>](#uri) | <span data-ttu-id="5d4c6-120">URI страницы, запросившего диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="5d4c6-120">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="5d4c6-121">Принять</span><span class="sxs-lookup"><span data-stu-id="5d4c6-121">Accept</span></span>](#accept) | <span data-ttu-id="5d4c6-122">Основное приложение может вызвать этот метод, чтобы ответить с помощью команды "ОК" для подтверждения, запроса и beforeunload диалоговых окон или вызова этого метода для указания отмены.</span><span class="sxs-lookup"><span data-stu-id="5d4c6-122">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="5d4c6-123">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="5d4c6-123">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="5d4c6-124">Для возврата объекта CoreWebView2Deferral можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="5d4c6-124">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

## <span data-ttu-id="5d4c6-125">Участников</span><span class="sxs-lookup"><span data-stu-id="5d4c6-125">Members</span></span>

#### <span data-ttu-id="5d4c6-126">DefaultText</span><span class="sxs-lookup"><span data-stu-id="5d4c6-126">DefaultText</span></span> 

<span data-ttu-id="5d4c6-127">Второй параметр, передаваемый диалоговому окну запроса JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5d4c6-127">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="5d4c6-128">общедоступная строка [DefaultText](#defaulttext)</span><span class="sxs-lookup"><span data-stu-id="5d4c6-128">public string [DefaultText](#defaulttext)</span></span>

<span data-ttu-id="5d4c6-129">Это значение по умолчанию, используемое в качестве результата функции JavaScript "prompt".</span><span class="sxs-lookup"><span data-stu-id="5d4c6-129">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="5d4c6-130">Любые</span><span class="sxs-lookup"><span data-stu-id="5d4c6-130">Kind</span></span> 

<span data-ttu-id="5d4c6-131">Диалоговое окно "вида JavaScript".</span><span class="sxs-lookup"><span data-stu-id="5d4c6-131">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="5d4c6-132">общедоступный [CoreWebView2ScriptDialogKind](#kind)</span><span class="sxs-lookup"><span data-stu-id="5d4c6-132">public CoreWebView2ScriptDialogKind [Kind](#kind)</span></span>

<span data-ttu-id="5d4c6-133">Приняв, подтвердите, запросите или beforeunload.</span><span class="sxs-lookup"><span data-stu-id="5d4c6-133">Accept, confirm, prompt, or beforeunload.</span></span>

#### <span data-ttu-id="5d4c6-134">Сообщение</span><span class="sxs-lookup"><span data-stu-id="5d4c6-134">Message</span></span> 

<span data-ttu-id="5d4c6-135">Сообщение в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="5d4c6-135">The message of the dialog box.</span></span>

> <span data-ttu-id="5d4c6-136">[сообщение](#message) общедоступной строки</span><span class="sxs-lookup"><span data-stu-id="5d4c6-136">public string [Message](#message)</span></span>

<span data-ttu-id="5d4c6-137">Из JavaScript это первый параметр, передаваемый в Alert, Confirm и Prompt, и он пуст для beforeunload.</span><span class="sxs-lookup"><span data-stu-id="5d4c6-137">From JavaScript this is the first parameter passed to alert, confirm, and prompt and is empty for beforeunload.</span></span>

#### <span data-ttu-id="5d4c6-138">ResultText</span><span class="sxs-lookup"><span data-stu-id="5d4c6-138">ResultText</span></span> 

<span data-ttu-id="5d4c6-139">Возвращаемое значение функции Prompt для JavaScript при вызове метода "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="5d4c6-139">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="5d4c6-140">общедоступная строка [ResultText](#resulttext)</span><span class="sxs-lookup"><span data-stu-id="5d4c6-140">public string [ResultText](#resulttext)</span></span>

<span data-ttu-id="5d4c6-141">Этот тип игнорируется, если диалоговое окно не является запросом.</span><span class="sxs-lookup"><span data-stu-id="5d4c6-141">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="5d4c6-142">Если параметр "принято" не вызывается, это значение игнорируется, и в командной строке возвращается значение "ложь".</span><span class="sxs-lookup"><span data-stu-id="5d4c6-142">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="5d4c6-143">Универсальный код ресурса (URI)</span><span class="sxs-lookup"><span data-stu-id="5d4c6-143">Uri</span></span> 

<span data-ttu-id="5d4c6-144">URI страницы, запросившего диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="5d4c6-144">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="5d4c6-145">[URI](#uri) общедоступной строки</span><span class="sxs-lookup"><span data-stu-id="5d4c6-145">public string [Uri](#uri)</span></span>

#### <span data-ttu-id="5d4c6-146">Принять</span><span class="sxs-lookup"><span data-stu-id="5d4c6-146">Accept</span></span> 

<span data-ttu-id="5d4c6-147">Основное приложение может вызвать этот метод, чтобы ответить с помощью команды "ОК" для подтверждения, запроса и beforeunload диалоговых окон или вызова этого метода для указания отмены.</span><span class="sxs-lookup"><span data-stu-id="5d4c6-147">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="5d4c6-148">общедоступная отмена [приема](#accept)()</span><span class="sxs-lookup"><span data-stu-id="5d4c6-148">public void [Accept](#accept)()</span></span>

<span data-ttu-id="5d4c6-149">Из JavaScript это означает, что функция Confirm и beforeunload возвращает значение истина, если вызывается метод принятии.</span><span class="sxs-lookup"><span data-stu-id="5d4c6-149">From JavaScript, this means that the confirm and beforeunload function returns true if Accept is called.</span></span> <span data-ttu-id="5d4c6-150">И для функции Prompt она возвращает значение ResultText, если вызывается метод допуска, и возвращает значение false в противном случае.</span><span class="sxs-lookup"><span data-stu-id="5d4c6-150">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="5d4c6-151">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="5d4c6-151">GetDeferral</span></span> 

<span data-ttu-id="5d4c6-152">Для возврата объекта CoreWebView2Deferral можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="5d4c6-152">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

> <span data-ttu-id="5d4c6-153">общедоступный CoreWebView2Deferral- [РБП](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="5d4c6-153">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="5d4c6-154">Вы можете использовать этот параметр, чтобы выполнить событие позже.</span><span class="sxs-lookup"><span data-stu-id="5d4c6-154">You can use this to complete the event at a later time.</span></span>

