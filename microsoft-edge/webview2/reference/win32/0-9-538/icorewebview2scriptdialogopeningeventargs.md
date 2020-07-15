---
description: Внедрение веб-технологий (HTML, CSS и JavaScript) в собственные приложения с помощью элемента управления Microsoft Edge WebView2
title: WebView2 Win32 C++ ICoreWebView2ScriptDialogOpeningEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/08/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, управление браузером, EDGE HTML, ICoreWebView2ScriptDialogOpeningEventArgs
ms.openlocfilehash: 070e7799111113ab8b4f883df85e505894677a31
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10879046"
---
# <span data-ttu-id="f20e6-104">интерфейс ICoreWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="f20e6-104">interface ICoreWebView2ScriptDialogOpeningEventArgs</span></span> 

```
interface ICoreWebView2ScriptDialogOpeningEventArgs
  : public IUnknown
```

<span data-ttu-id="f20e6-105">Аргументы события для события ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="f20e6-105">Event args for the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="f20e6-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="f20e6-106">Summary</span></span>

 <span data-ttu-id="f20e6-107">Участников</span><span class="sxs-lookup"><span data-stu-id="f20e6-107">Members</span></span>                        | <span data-ttu-id="f20e6-108">Описания</span><span class="sxs-lookup"><span data-stu-id="f20e6-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="f20e6-109">Принять</span><span class="sxs-lookup"><span data-stu-id="f20e6-109">Accept</span></span>](#accept) | <span data-ttu-id="f20e6-110">Основное приложение может вызвать этот метод, чтобы ответить с помощью команды "ОК" для подтверждения, запроса и beforeunload диалоговых окон или вызова этого метода для указания отмены.</span><span class="sxs-lookup"><span data-stu-id="f20e6-110">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="f20e6-111">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="f20e6-111">get_DefaultText</span></span>](#get_defaulttext) | <span data-ttu-id="f20e6-112">Второй параметр, передаваемый диалоговому окну запроса JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f20e6-112">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="f20e6-113">get_Kind</span><span class="sxs-lookup"><span data-stu-id="f20e6-113">get_Kind</span></span>](#get_kind) | <span data-ttu-id="f20e6-114">Диалоговое окно "вида JavaScript".</span><span class="sxs-lookup"><span data-stu-id="f20e6-114">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="f20e6-115">get_Message</span><span class="sxs-lookup"><span data-stu-id="f20e6-115">get_Message</span></span>](#get_message) | <span data-ttu-id="f20e6-116">Сообщение в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="f20e6-116">The message of the dialog box.</span></span>
[<span data-ttu-id="f20e6-117">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="f20e6-117">get_ResultText</span></span>](#get_resulttext) | <span data-ttu-id="f20e6-118">Возвращаемое значение функции Prompt для JavaScript при вызове метода "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="f20e6-118">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="f20e6-119">get_Uri</span><span class="sxs-lookup"><span data-stu-id="f20e6-119">get_Uri</span></span>](#get_uri) | <span data-ttu-id="f20e6-120">URI страницы, запросившего диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f20e6-120">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="f20e6-121">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="f20e6-121">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="f20e6-122">Для возврата объекта [ICoreWebView2Deferral](icorewebview2deferral.md) можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="f20e6-122">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>
[<span data-ttu-id="f20e6-123">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="f20e6-123">put_ResultText</span></span>](#put_resulttext) | <span data-ttu-id="f20e6-124">Задайте свойство ResultText.</span><span class="sxs-lookup"><span data-stu-id="f20e6-124">Set the ResultText property.</span></span>

## <span data-ttu-id="f20e6-125">Участников</span><span class="sxs-lookup"><span data-stu-id="f20e6-125">Members</span></span>

#### <span data-ttu-id="f20e6-126">Принять</span><span class="sxs-lookup"><span data-stu-id="f20e6-126">Accept</span></span> 

<span data-ttu-id="f20e6-127">Основное приложение может вызвать этот метод, чтобы ответить с помощью команды "ОК" для подтверждения, запроса и beforeunload диалоговых окон или вызова этого метода для указания отмены.</span><span class="sxs-lookup"><span data-stu-id="f20e6-127">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="f20e6-128">общедоступное значение HRESULT [принято](#accept)()</span><span class="sxs-lookup"><span data-stu-id="f20e6-128">public HRESULT [Accept](#accept)()</span></span>

<span data-ttu-id="f20e6-129">Из JavaScript это означает, что функция Confirm и beforeunload возвращает значение истина, если вызывается метод принятии.</span><span class="sxs-lookup"><span data-stu-id="f20e6-129">From JavaScript, this means that the confirm and beforeunload function returns true if Accept is called.</span></span> <span data-ttu-id="f20e6-130">И для функции Prompt она возвращает значение ResultText, если вызывается метод допуска, и возвращает значение false в противном случае.</span><span class="sxs-lookup"><span data-stu-id="f20e6-130">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="f20e6-131">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="f20e6-131">get_DefaultText</span></span> 

<span data-ttu-id="f20e6-132">Второй параметр, передаваемый диалоговому окну запроса JavaScript.</span><span class="sxs-lookup"><span data-stu-id="f20e6-132">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="f20e6-133">общедоступные значения HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* DefaultText)</span><span class="sxs-lookup"><span data-stu-id="f20e6-133">public HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* defaultText)</span></span>

<span data-ttu-id="f20e6-134">Это значение по умолчанию, используемое в качестве результата функции JavaScript "prompt".</span><span class="sxs-lookup"><span data-stu-id="f20e6-134">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="f20e6-135">get_Kind</span><span class="sxs-lookup"><span data-stu-id="f20e6-135">get_Kind</span></span> 

<span data-ttu-id="f20e6-136">Диалоговое окно "вида JavaScript".</span><span class="sxs-lookup"><span data-stu-id="f20e6-136">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="f20e6-137">общедоступные значения HRESULT [get_Kind](#get_kind)(COREWEBVIEW2_SCRIPT_DIALOG_KIND \* видам)</span><span class="sxs-lookup"><span data-stu-id="f20e6-137">public HRESULT [get_Kind](#get_kind)(COREWEBVIEW2_SCRIPT_DIALOG_KIND \* kind)</span></span>

<span data-ttu-id="f20e6-138">Приняв, подтвердите, запросите или beforeunload.</span><span class="sxs-lookup"><span data-stu-id="f20e6-138">Accept, confirm, prompt, or beforeunload.</span></span>

#### <span data-ttu-id="f20e6-139">get_Message</span><span class="sxs-lookup"><span data-stu-id="f20e6-139">get_Message</span></span> 

<span data-ttu-id="f20e6-140">Сообщение в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="f20e6-140">The message of the dialog box.</span></span>

> <span data-ttu-id="f20e6-141">общедоступное значение HRESULT [get_Message](#get_message)(LPWSTR \* сообщение)</span><span class="sxs-lookup"><span data-stu-id="f20e6-141">public HRESULT [get_Message](#get_message)(LPWSTR \* message)</span></span>

<span data-ttu-id="f20e6-142">Из JavaScript это первый параметр, передаваемый в Alert, Confirm и Prompt, и он пуст для beforeunload.</span><span class="sxs-lookup"><span data-stu-id="f20e6-142">From JavaScript this is the first parameter passed to alert, confirm, and prompt and is empty for beforeunload.</span></span>

#### <span data-ttu-id="f20e6-143">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="f20e6-143">get_ResultText</span></span> 

<span data-ttu-id="f20e6-144">Возвращаемое значение функции Prompt для JavaScript при вызове метода "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="f20e6-144">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="f20e6-145">общедоступные значения HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* ResultText)</span><span class="sxs-lookup"><span data-stu-id="f20e6-145">public HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* resultText)</span></span>

<span data-ttu-id="f20e6-146">Этот тип игнорируется, если диалоговое окно не является запросом.</span><span class="sxs-lookup"><span data-stu-id="f20e6-146">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="f20e6-147">Если параметр "принято" не вызывается, это значение игнорируется, и в командной строке возвращается значение "ложь".</span><span class="sxs-lookup"><span data-stu-id="f20e6-147">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="f20e6-148">get_Uri</span><span class="sxs-lookup"><span data-stu-id="f20e6-148">get_Uri</span></span> 

<span data-ttu-id="f20e6-149">URI страницы, запросившего диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="f20e6-149">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="f20e6-150">общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="f20e6-150">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="f20e6-151">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="f20e6-151">GetDeferral</span></span> 

<span data-ttu-id="f20e6-152">Для возврата объекта [ICoreWebView2Deferral](icorewebview2deferral.md) можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="f20e6-152">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>

> <span data-ttu-id="f20e6-153">общедоступный HRESULT- [РБП](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* РБП)</span><span class="sxs-lookup"><span data-stu-id="f20e6-153">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="f20e6-154">Вы можете использовать этот параметр, чтобы выполнить событие позже.</span><span class="sxs-lookup"><span data-stu-id="f20e6-154">You can use this to complete the event at a later time.</span></span>

#### <span data-ttu-id="f20e6-155">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="f20e6-155">put_ResultText</span></span> 

<span data-ttu-id="f20e6-156">Задайте свойство ResultText.</span><span class="sxs-lookup"><span data-stu-id="f20e6-156">Set the ResultText property.</span></span>

> <span data-ttu-id="f20e6-157">общедоступные значения HRESULT [put_ResultText](#put_resulttext)(LPCWSTR ResultText)</span><span class="sxs-lookup"><span data-stu-id="f20e6-157">public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR resultText)</span></span>

