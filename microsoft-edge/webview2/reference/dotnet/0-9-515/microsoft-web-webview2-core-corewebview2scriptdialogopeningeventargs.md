---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 1359e9472455acf2949cc329de4280ad970a3b68
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10697310"
---
# <span data-ttu-id="42d0b-104">Класс Microsoft. Web. WebView2. Core. CoreWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="42d0b-104">Microsoft.Web.WebView2.Core.CoreWebView2ScriptDialogOpeningEventArgs class</span></span> 

> [!NOTE]
> <span data-ttu-id="42d0b-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="42d0b-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="42d0b-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="42d0b-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

<span data-ttu-id="42d0b-107">Пространство имен: Microsoft. Web. WebView2. Core </span><span class="sxs-lookup"><span data-stu-id="42d0b-107">Namespace: Microsoft.Web.WebView2.Core</span></span>\
<span data-ttu-id="42d0b-108">Сборка: Microsoft. Web. WebView2. Core. dll</span><span class="sxs-lookup"><span data-stu-id="42d0b-108">Assembly: Microsoft.Web.WebView2.Core.dll</span></span>

<span data-ttu-id="42d0b-109">Аргументы события для события ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="42d0b-109">Event args for the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="42d0b-110">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="42d0b-110">Summary</span></span>

 <span data-ttu-id="42d0b-111">Участников</span><span class="sxs-lookup"><span data-stu-id="42d0b-111">Members</span></span>                        | <span data-ttu-id="42d0b-112">Описания</span><span class="sxs-lookup"><span data-stu-id="42d0b-112">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="42d0b-113">DefaultText</span><span class="sxs-lookup"><span data-stu-id="42d0b-113">DefaultText</span></span>](#defaulttext) | <span data-ttu-id="42d0b-114">Второй параметр, передаваемый диалоговому окну запроса JavaScript.</span><span class="sxs-lookup"><span data-stu-id="42d0b-114">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="42d0b-115">Любые</span><span class="sxs-lookup"><span data-stu-id="42d0b-115">Kind</span></span>](#kind) | <span data-ttu-id="42d0b-116">Диалоговое окно "вида JavaScript".</span><span class="sxs-lookup"><span data-stu-id="42d0b-116">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="42d0b-117">Сообщение</span><span class="sxs-lookup"><span data-stu-id="42d0b-117">Message</span></span>](#message) | <span data-ttu-id="42d0b-118">Сообщение в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="42d0b-118">The message of the dialog box.</span></span>
[<span data-ttu-id="42d0b-119">ResultText</span><span class="sxs-lookup"><span data-stu-id="42d0b-119">ResultText</span></span>](#resulttext) | <span data-ttu-id="42d0b-120">Возвращаемое значение функции Prompt для JavaScript при вызове метода "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="42d0b-120">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="42d0b-121">Универсальный код ресурса (URI)</span><span class="sxs-lookup"><span data-stu-id="42d0b-121">Uri</span></span>](#uri) | <span data-ttu-id="42d0b-122">URI страницы, запросившего диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="42d0b-122">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="42d0b-123">Принять</span><span class="sxs-lookup"><span data-stu-id="42d0b-123">Accept</span></span>](#accept) | <span data-ttu-id="42d0b-124">Основное приложение может вызвать этот метод, чтобы ответить с помощью команды "ОК" для подтверждения, запроса и beforeunload диалоговых окон или вызова этого метода для указания отмены.</span><span class="sxs-lookup"><span data-stu-id="42d0b-124">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="42d0b-125">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="42d0b-125">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="42d0b-126">Для возврата объекта CoreWebView2Deferral можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="42d0b-126">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

## <span data-ttu-id="42d0b-127">Участников</span><span class="sxs-lookup"><span data-stu-id="42d0b-127">Members</span></span>

#### <span data-ttu-id="42d0b-128">DefaultText</span><span class="sxs-lookup"><span data-stu-id="42d0b-128">DefaultText</span></span> 

<span data-ttu-id="42d0b-129">Второй параметр, передаваемый диалоговому окну запроса JavaScript.</span><span class="sxs-lookup"><span data-stu-id="42d0b-129">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="42d0b-130">общедоступная строка [DefaultText](#defaulttext)</span><span class="sxs-lookup"><span data-stu-id="42d0b-130">public string [DefaultText](#defaulttext)</span></span>

<span data-ttu-id="42d0b-131">Это значение по умолчанию, используемое в качестве результата функции JavaScript "prompt".</span><span class="sxs-lookup"><span data-stu-id="42d0b-131">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="42d0b-132">Любые</span><span class="sxs-lookup"><span data-stu-id="42d0b-132">Kind</span></span> 

<span data-ttu-id="42d0b-133">Диалоговое окно "вида JavaScript".</span><span class="sxs-lookup"><span data-stu-id="42d0b-133">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="42d0b-134">общедоступный [CoreWebView2ScriptDialogKind](#kind)</span><span class="sxs-lookup"><span data-stu-id="42d0b-134">public CoreWebView2ScriptDialogKind [Kind](#kind)</span></span>

<span data-ttu-id="42d0b-135">Приняв, подтвердите, запросите или beforeunload.</span><span class="sxs-lookup"><span data-stu-id="42d0b-135">Accept, confirm, prompt, or beforeunload.</span></span>

#### <span data-ttu-id="42d0b-136">Сообщение</span><span class="sxs-lookup"><span data-stu-id="42d0b-136">Message</span></span> 

<span data-ttu-id="42d0b-137">Сообщение в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="42d0b-137">The message of the dialog box.</span></span>

> <span data-ttu-id="42d0b-138">[сообщение](#message) общедоступной строки</span><span class="sxs-lookup"><span data-stu-id="42d0b-138">public string [Message](#message)</span></span>

<span data-ttu-id="42d0b-139">Из JavaScript это первый параметр, передаваемый в Alert, Confirm и Prompt, и он пуст для beforeunload.</span><span class="sxs-lookup"><span data-stu-id="42d0b-139">From JavaScript this is the first parameter passed to alert, confirm, and prompt and is empty for beforeunload.</span></span>

#### <span data-ttu-id="42d0b-140">ResultText</span><span class="sxs-lookup"><span data-stu-id="42d0b-140">ResultText</span></span> 

<span data-ttu-id="42d0b-141">Возвращаемое значение функции Prompt для JavaScript при вызове метода "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="42d0b-141">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="42d0b-142">общедоступная строка [ResultText](#resulttext)</span><span class="sxs-lookup"><span data-stu-id="42d0b-142">public string [ResultText](#resulttext)</span></span>

<span data-ttu-id="42d0b-143">Этот тип игнорируется, если диалоговое окно не является запросом.</span><span class="sxs-lookup"><span data-stu-id="42d0b-143">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="42d0b-144">Если параметр "принято" не вызывается, это значение игнорируется, и в командной строке возвращается значение "ложь".</span><span class="sxs-lookup"><span data-stu-id="42d0b-144">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="42d0b-145">Универсальный код ресурса (URI)</span><span class="sxs-lookup"><span data-stu-id="42d0b-145">Uri</span></span> 

<span data-ttu-id="42d0b-146">URI страницы, запросившего диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="42d0b-146">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="42d0b-147">[URI](#uri) общедоступной строки</span><span class="sxs-lookup"><span data-stu-id="42d0b-147">public string [Uri](#uri)</span></span>

#### <span data-ttu-id="42d0b-148">Принять</span><span class="sxs-lookup"><span data-stu-id="42d0b-148">Accept</span></span> 

<span data-ttu-id="42d0b-149">Основное приложение может вызвать этот метод, чтобы ответить с помощью команды "ОК" для подтверждения, запроса и beforeunload диалоговых окон или вызова этого метода для указания отмены.</span><span class="sxs-lookup"><span data-stu-id="42d0b-149">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="42d0b-150">общедоступная отмена [приема](#accept)()</span><span class="sxs-lookup"><span data-stu-id="42d0b-150">public void [Accept](#accept)()</span></span>

<span data-ttu-id="42d0b-151">Из JavaScript это означает, что функция Confirm и beforeunload возвращает значение истина, если вызывается метод принятии.</span><span class="sxs-lookup"><span data-stu-id="42d0b-151">From JavaScript, this means that the confirm and beforeunload function returns true if Accept is called.</span></span> <span data-ttu-id="42d0b-152">И для функции Prompt она возвращает значение ResultText, если вызывается метод допуска, и возвращает значение false в противном случае.</span><span class="sxs-lookup"><span data-stu-id="42d0b-152">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="42d0b-153">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="42d0b-153">GetDeferral</span></span> 

<span data-ttu-id="42d0b-154">Для возврата объекта CoreWebView2Deferral можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="42d0b-154">GetDeferral can be called to return a CoreWebView2Deferral object.</span></span>

> <span data-ttu-id="42d0b-155">общедоступный CoreWebView2Deferral- [РБП](#getdeferral)()</span><span class="sxs-lookup"><span data-stu-id="42d0b-155">public CoreWebView2Deferral [GetDeferral](#getdeferral)()</span></span>

<span data-ttu-id="42d0b-156">Вы можете использовать этот параметр, чтобы выполнить событие позже.</span><span class="sxs-lookup"><span data-stu-id="42d0b-156">You can use this to complete the event at a later time.</span></span>

