---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.9.430-WebView2 Win32 C++ ICoreWebView2ScriptDialogOpeningEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: cd8f96787d289ab0fe649244ce665445efdbcecf
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884045"
---
# <span data-ttu-id="82b4c-104">0.9.430-Interface ICoreWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="82b4c-104">0.9.430 - interface ICoreWebView2ScriptDialogOpeningEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface ICoreWebView2ScriptDialogOpeningEventArgs
  : public IUnknown
```

<span data-ttu-id="82b4c-105">Аргументы события для события ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="82b4c-105">Event args for the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="82b4c-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="82b4c-106">Summary</span></span>

 <span data-ttu-id="82b4c-107">Участников</span><span class="sxs-lookup"><span data-stu-id="82b4c-107">Members</span></span>                        | <span data-ttu-id="82b4c-108">Описания</span><span class="sxs-lookup"><span data-stu-id="82b4c-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="82b4c-109">get_Uri</span><span class="sxs-lookup"><span data-stu-id="82b4c-109">get_Uri</span></span>](#get_uri) | <span data-ttu-id="82b4c-110">URI страницы, запросившего диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="82b4c-110">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="82b4c-111">get_Kind</span><span class="sxs-lookup"><span data-stu-id="82b4c-111">get_Kind</span></span>](#get_kind) | <span data-ttu-id="82b4c-112">Диалоговое окно "вида JavaScript".</span><span class="sxs-lookup"><span data-stu-id="82b4c-112">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="82b4c-113">get_Message</span><span class="sxs-lookup"><span data-stu-id="82b4c-113">get_Message</span></span>](#get_message) | <span data-ttu-id="82b4c-114">Сообщение в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="82b4c-114">The message of the dialog box.</span></span>
[<span data-ttu-id="82b4c-115">Принять</span><span class="sxs-lookup"><span data-stu-id="82b4c-115">Accept</span></span>](#accept) | <span data-ttu-id="82b4c-116">Основное приложение может вызвать этот метод, чтобы ответить с помощью команды "ОК" для подтверждения, запроса и beforeunload диалоговых окон или вызова этого метода для указания отмены.</span><span class="sxs-lookup"><span data-stu-id="82b4c-116">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="82b4c-117">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="82b4c-117">get_DefaultText</span></span>](#get_defaulttext) | <span data-ttu-id="82b4c-118">Второй параметр, передаваемый диалоговому окну запроса JavaScript.</span><span class="sxs-lookup"><span data-stu-id="82b4c-118">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="82b4c-119">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="82b4c-119">get_ResultText</span></span>](#get_resulttext) | <span data-ttu-id="82b4c-120">Возвращаемое значение функции Prompt для JavaScript при вызове метода "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="82b4c-120">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="82b4c-121">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="82b4c-121">put_ResultText</span></span>](#put_resulttext) | <span data-ttu-id="82b4c-122">Задайте свойство ResultText.</span><span class="sxs-lookup"><span data-stu-id="82b4c-122">Set the ResultText property.</span></span>
[<span data-ttu-id="82b4c-123">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="82b4c-123">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="82b4c-124">Для возврата объекта [ICoreWebView2Deferral](ICoreWebView2Deferral.md) можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="82b4c-124">GetDeferral can be called to return an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object.</span></span>

## <span data-ttu-id="82b4c-125">Участников</span><span class="sxs-lookup"><span data-stu-id="82b4c-125">Members</span></span>

#### <span data-ttu-id="82b4c-126">get_Uri</span><span class="sxs-lookup"><span data-stu-id="82b4c-126">get_Uri</span></span> 

<span data-ttu-id="82b4c-127">URI страницы, запросившего диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="82b4c-127">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="82b4c-128">общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="82b4c-128">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="82b4c-129">get_Kind</span><span class="sxs-lookup"><span data-stu-id="82b4c-129">get_Kind</span></span> 

<span data-ttu-id="82b4c-130">Диалоговое окно "вида JavaScript".</span><span class="sxs-lookup"><span data-stu-id="82b4c-130">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="82b4c-131">общедоступные значения HRESULT [get_Kind](#get_kind)(CORE_WEBVIEW2_SCRIPT_DIALOG_KIND \* видам)</span><span class="sxs-lookup"><span data-stu-id="82b4c-131">public HRESULT [get_Kind](#get_kind)(CORE_WEBVIEW2_SCRIPT_DIALOG_KIND \* kind)</span></span>

<span data-ttu-id="82b4c-132">Приняв, подтвердите, запросите или beforeunload.</span><span class="sxs-lookup"><span data-stu-id="82b4c-132">Accept, confirm, prompt, or beforeunload.</span></span>

#### <span data-ttu-id="82b4c-133">get_Message</span><span class="sxs-lookup"><span data-stu-id="82b4c-133">get_Message</span></span> 

<span data-ttu-id="82b4c-134">Сообщение в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="82b4c-134">The message of the dialog box.</span></span>

> <span data-ttu-id="82b4c-135">общедоступное значение HRESULT [get_Message](#get_message)(LPWSTR \* сообщение)</span><span class="sxs-lookup"><span data-stu-id="82b4c-135">public HRESULT [get_Message](#get_message)(LPWSTR \* message)</span></span>

<span data-ttu-id="82b4c-136">Из JavaScript это первый параметр, передаваемый в Alert, Confirm и Prompt, и он пуст для beforeunload.</span><span class="sxs-lookup"><span data-stu-id="82b4c-136">From JavaScript this is the first parameter passed to alert, confirm, and prompt and is empty for beforeunload.</span></span>

#### <span data-ttu-id="82b4c-137">Принять</span><span class="sxs-lookup"><span data-stu-id="82b4c-137">Accept</span></span> 

<span data-ttu-id="82b4c-138">Основное приложение может вызвать этот метод, чтобы ответить с помощью команды "ОК" для подтверждения, запроса и beforeunload диалоговых окон или вызова этого метода для указания отмены.</span><span class="sxs-lookup"><span data-stu-id="82b4c-138">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="82b4c-139">общедоступное значение HRESULT [принято](#accept)()</span><span class="sxs-lookup"><span data-stu-id="82b4c-139">public HRESULT [Accept](#accept)()</span></span>

<span data-ttu-id="82b4c-140">Из JavaScript это означает, что функция Confirm и beforeunload возвращает значение истина, если вызывается метод принятии.</span><span class="sxs-lookup"><span data-stu-id="82b4c-140">From JavaScript, this means that the confirm and beforeunload function returns true if Accept is called.</span></span> <span data-ttu-id="82b4c-141">И для функции Prompt она возвращает значение ResultText, если вызывается метод допуска, и возвращает значение false в противном случае.</span><span class="sxs-lookup"><span data-stu-id="82b4c-141">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="82b4c-142">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="82b4c-142">get_DefaultText</span></span> 

<span data-ttu-id="82b4c-143">Второй параметр, передаваемый диалоговому окну запроса JavaScript.</span><span class="sxs-lookup"><span data-stu-id="82b4c-143">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="82b4c-144">общедоступные значения HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* DefaultText)</span><span class="sxs-lookup"><span data-stu-id="82b4c-144">public HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* defaultText)</span></span>

<span data-ttu-id="82b4c-145">Это значение по умолчанию, используемое в качестве результата функции JavaScript "prompt".</span><span class="sxs-lookup"><span data-stu-id="82b4c-145">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="82b4c-146">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="82b4c-146">get_ResultText</span></span> 

<span data-ttu-id="82b4c-147">Возвращаемое значение функции Prompt для JavaScript при вызове метода "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="82b4c-147">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="82b4c-148">общедоступные значения HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* ResultText)</span><span class="sxs-lookup"><span data-stu-id="82b4c-148">public HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* resultText)</span></span>

<span data-ttu-id="82b4c-149">Этот тип игнорируется, если диалоговое окно не является запросом.</span><span class="sxs-lookup"><span data-stu-id="82b4c-149">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="82b4c-150">Если параметр "принято" не вызывается, это значение игнорируется, и в командной строке возвращается значение "ложь".</span><span class="sxs-lookup"><span data-stu-id="82b4c-150">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="82b4c-151">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="82b4c-151">put_ResultText</span></span> 

<span data-ttu-id="82b4c-152">Задайте свойство ResultText.</span><span class="sxs-lookup"><span data-stu-id="82b4c-152">Set the ResultText property.</span></span>

> <span data-ttu-id="82b4c-153">общедоступные значения HRESULT [put_ResultText](#put_resulttext)(LPCWSTR ResultText)</span><span class="sxs-lookup"><span data-stu-id="82b4c-153">public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR resultText)</span></span>

#### <span data-ttu-id="82b4c-154">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="82b4c-154">GetDeferral</span></span> 

<span data-ttu-id="82b4c-155">Для возврата объекта [ICoreWebView2Deferral](ICoreWebView2Deferral.md) можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="82b4c-155">GetDeferral can be called to return an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object.</span></span>

> <span data-ttu-id="82b4c-156">общедоступный HRESULT- [РБП](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \* \* РБП)</span><span class="sxs-lookup"><span data-stu-id="82b4c-156">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="82b4c-157">Вы можете использовать этот параметр, чтобы выполнить событие позже.</span><span class="sxs-lookup"><span data-stu-id="82b4c-157">You can use this to complete the event at a later time.</span></span>

