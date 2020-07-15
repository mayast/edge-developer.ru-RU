---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2ScriptDialogOpeningEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: b7071a312ce1fa3ca006a6805a1f712a51d0dab0
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879116"
---
# <span data-ttu-id="908f6-104">класс 0.9.515-Microsoft. Web. WebView2. Core. CoreWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="908f6-104">0.9.515 - Microsoft.Web.WebView2.Core.CoreWebView2ScriptDialogOpeningEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="908f6-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="908f6-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="908f6-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="908f6-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="908f6-107">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="908f6-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="908f6-108">Сборка: Microsoft.Web.WebView2.Core.dll</span><span class="sxs-lookup"><span data-stu-id="908f6-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="908f6-109">Аргументы события для события ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="908f6-109">Event args for the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="908f6-110">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="908f6-110">Summary</span></span>

 <span data-ttu-id="908f6-111">Участников</span><span class="sxs-lookup"><span data-stu-id="908f6-111">Members</span></span>                        | <span data-ttu-id="908f6-112">Описания</span><span class="sxs-lookup"><span data-stu-id="908f6-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="908f6-113">DefaultText</span><span class="sxs-lookup"><span data-stu-id="908f6-113">DefaultText</span></span>](#defaulttext) | <span data-ttu-id="908f6-114">Второй параметр, передаваемый диалоговому окну запроса JavaScript.</span><span class="sxs-lookup"><span data-stu-id="908f6-114">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="908f6-115">Любые</span><span class="sxs-lookup"><span data-stu-id="908f6-115">Kind</span></span>](#kind) | <span data-ttu-id="908f6-116">Диалоговое окно "вида JavaScript".</span><span class="sxs-lookup"><span data-stu-id="908f6-116">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="908f6-117">Сообщение</span><span class="sxs-lookup"><span data-stu-id="908f6-117">Message</span></span>](#message) | <span data-ttu-id="908f6-118">Сообщение в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="908f6-118">The message of the dialog box.</span></span>
[<span data-ttu-id="908f6-119">ResultText</span><span class="sxs-lookup"><span data-stu-id="908f6-119">ResultText</span></span>](#resulttext) | <span data-ttu-id="908f6-120">Возвращаемое значение функции Prompt для JavaScript при вызове метода "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="908f6-120">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="908f6-121">Универсальный код ресурса (URI)</span><span class="sxs-lookup"><span data-stu-id="908f6-121">Uri</span></span>](#uri) | <span data-ttu-id="908f6-122">URI страницы, запросившего диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="908f6-122">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="908f6-123">Принять</span><span class="sxs-lookup"><span data-stu-id="908f6-123">Accept</span></span>](#accept) | <span data-ttu-id="908f6-124">Основное приложение может вызвать этот метод, чтобы ответить с помощью команды "ОК" для подтверждения, запроса и beforeunload диалоговых окон или вызова этого метода для указания отмены.</span><span class="sxs-lookup"><span data-stu-id="908f6-124">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="908f6-125">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="908f6-125">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="908f6-126">Для возврата объекта CoreWebView2Deferral можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="908f6-126">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

## <span data-ttu-id="908f6-127">Участников</span><span class="sxs-lookup"><span data-stu-id="908f6-127">Members</span></span>

#### <span data-ttu-id="908f6-128">DefaultText</span><span class="sxs-lookup"><span data-stu-id="908f6-128">DefaultText</span></span> 

<span data-ttu-id="908f6-129">Второй параметр, передаваемый диалоговому окну запроса JavaScript.</span><span class="sxs-lookup"><span data-stu-id="908f6-129">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="908f6-130">общедоступная строка [DefaultText](#defaulttext)</span><span class="sxs-lookup"><span data-stu-id="908f6-130">public string [DefaultText](#defaulttext)</span></span>

<span data-ttu-id="908f6-131">Это значение по умолчанию, используемое в качестве результата функции JavaScript "prompt".</span><span class="sxs-lookup"><span data-stu-id="908f6-131">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="908f6-132">Любые</span><span class="sxs-lookup"><span data-stu-id="908f6-132">Kind</span></span> 

<span data-ttu-id="908f6-133">Диалоговое окно "вида JavaScript".</span><span class="sxs-lookup"><span data-stu-id="908f6-133">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="908f6-134">общедоступный [CoreWebView2ScriptDialogKind](#kind)</span><span class="sxs-lookup"><span data-stu-id="908f6-134">public CoreWebView2ScriptDialogKind [Kind](#kind)</span></span>

<span data-ttu-id="908f6-135">Приняв, подтвердите, запросите или beforeunload.</span><span class="sxs-lookup"><span data-stu-id="908f6-135">Accept, confirm, prompt, or beforeunload.</span></span>

#### <span data-ttu-id="908f6-136">Сообщение</span><span class="sxs-lookup"><span data-stu-id="908f6-136">Message</span></span> 

<span data-ttu-id="908f6-137">Сообщение в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="908f6-137">The message of the dialog box.</span></span>

> <span data-ttu-id="908f6-138">[сообщение](#message) общедоступной строки</span><span class="sxs-lookup"><span data-stu-id="908f6-138">public string [Message](#message)</span></span>

<span data-ttu-id="908f6-139">Из JavaScript это первый параметр, передаваемый в Alert, Confirm и Prompt, и он пуст для beforeunload.</span><span class="sxs-lookup"><span data-stu-id="908f6-139">From JavaScript this is the first parameter passed to alert, confirm, and prompt and is empty for beforeunload.</span></span>

#### <span data-ttu-id="908f6-140">ResultText</span><span class="sxs-lookup"><span data-stu-id="908f6-140">ResultText</span></span> 

<span data-ttu-id="908f6-141">Возвращаемое значение функции Prompt для JavaScript при вызове метода "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="908f6-141">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="908f6-142">общедоступная строка [ResultText](#resulttext)</span><span class="sxs-lookup"><span data-stu-id="908f6-142">public string [ResultText](#resulttext)</span></span>

<span data-ttu-id="908f6-143">Этот тип игнорируется, если диалоговое окно не является запросом.</span><span class="sxs-lookup"><span data-stu-id="908f6-143">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="908f6-144">Если параметр "принято" не вызывается, это значение игнорируется, и в командной строке возвращается значение "ложь".</span><span class="sxs-lookup"><span data-stu-id="908f6-144">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="908f6-145">Универсальный код ресурса (URI)</span><span class="sxs-lookup"><span data-stu-id="908f6-145">Uri</span></span> 

<span data-ttu-id="908f6-146">URI страницы, запросившего диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="908f6-146">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="908f6-147">[URI](#uri) общедоступной строки</span><span class="sxs-lookup"><span data-stu-id="908f6-147">public string [Uri](#uri)</span></span>

#### <span data-ttu-id="908f6-148">Принять</span><span class="sxs-lookup"><span data-stu-id="908f6-148">Accept</span></span> 

<span data-ttu-id="908f6-149">Основное приложение может вызвать этот метод, чтобы ответить с помощью команды "ОК" для подтверждения, запроса и beforeunload диалоговых окон или вызова этого метода для указания отмены.</span><span class="sxs-lookup"><span data-stu-id="908f6-149">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="908f6-150">общедоступная отмена [приема](#accept)()</span><span class="sxs-lookup"><span data-stu-id="908f6-150">public void [Accept](#accept)()</span></span>

<span data-ttu-id="908f6-151">Из JavaScript это означает, что функция Confirm и beforeunload возвращает значение истина, если вызывается метод принятии.</span><span class="sxs-lookup"><span data-stu-id="908f6-151">From JavaScript, this means that the confirm and beforeunload function returns true if Accept is called.</span></span> <span data-ttu-id="908f6-152">И для функции Prompt она возвращает значение ResultText, если вызывается метод допуска, и возвращает значение false в противном случае.</span><span class="sxs-lookup"><span data-stu-id="908f6-152">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="908f6-153">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="908f6-153">GetDeferral</span></span> 

<span data-ttu-id="908f6-154">Для возврата объекта CoreWebView2Deferral можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="908f6-154">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

> <span data-ttu-id="908f6-155">общедоступный CoreWebView2Deferral- [РБП](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="908f6-155">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="908f6-156">Вы можете использовать этот параметр, чтобы выполнить событие позже.</span><span class="sxs-lookup"><span data-stu-id="908f6-156">You can use this to complete the event at a later time.</span></span>

