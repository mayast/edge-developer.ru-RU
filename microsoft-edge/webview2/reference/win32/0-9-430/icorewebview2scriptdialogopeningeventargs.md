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
ms.openlocfilehash: 8ed1a10a65a07fc359deea18b8aadd4df3a7b055
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10655049"
---
# <span data-ttu-id="75cb1-104">интерфейс ICoreWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="75cb1-104">interface ICoreWebView2ScriptDialogOpeningEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="75cb1-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.9.430.</span><span class="sxs-lookup"><span data-stu-id="75cb1-105">This interface may be altered or unavailable for releases after SDK version 0.9.430.</span></span> <span data-ttu-id="75cb1-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="75cb1-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ScriptDialogOpeningEventArgs
  : public IUnknown
```

<span data-ttu-id="75cb1-107">Аргументы события для события ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="75cb1-107">Event args for the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="75cb1-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="75cb1-108">Summary</span></span>

 <span data-ttu-id="75cb1-109">Участников</span><span class="sxs-lookup"><span data-stu-id="75cb1-109">Members</span></span>                        | <span data-ttu-id="75cb1-110">Описания</span><span class="sxs-lookup"><span data-stu-id="75cb1-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="75cb1-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="75cb1-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="75cb1-112">URI страницы, запросившего диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="75cb1-112">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="75cb1-113">get_Kind</span><span class="sxs-lookup"><span data-stu-id="75cb1-113">get_Kind</span></span>](#get_kind) | <span data-ttu-id="75cb1-114">Диалоговое окно "вида JavaScript".</span><span class="sxs-lookup"><span data-stu-id="75cb1-114">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="75cb1-115">get_Message</span><span class="sxs-lookup"><span data-stu-id="75cb1-115">get_Message</span></span>](#get_message) | <span data-ttu-id="75cb1-116">Сообщение в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="75cb1-116">The message of the dialog box.</span></span>
[<span data-ttu-id="75cb1-117">Принять</span><span class="sxs-lookup"><span data-stu-id="75cb1-117">Accept</span></span>](#accept) | <span data-ttu-id="75cb1-118">Основное приложение может вызвать этот метод, чтобы ответить с помощью команды "ОК" для подтверждения, запроса и beforeunload диалоговых окон или вызова этого метода для указания отмены.</span><span class="sxs-lookup"><span data-stu-id="75cb1-118">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="75cb1-119">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="75cb1-119">get_DefaultText</span></span>](#get_defaulttext) | <span data-ttu-id="75cb1-120">Второй параметр, передаваемый диалоговому окну запроса JavaScript.</span><span class="sxs-lookup"><span data-stu-id="75cb1-120">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="75cb1-121">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="75cb1-121">get_ResultText</span></span>](#get_resulttext) | <span data-ttu-id="75cb1-122">Возвращаемое значение функции Prompt для JavaScript при вызове метода "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="75cb1-122">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="75cb1-123">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="75cb1-123">put_ResultText</span></span>](#put_resulttext) | <span data-ttu-id="75cb1-124">Задайте свойство ResultText.</span><span class="sxs-lookup"><span data-stu-id="75cb1-124">Set the ResultText property.</span></span>
[<span data-ttu-id="75cb1-125">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="75cb1-125">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="75cb1-126">Для возврата объекта [ICoreWebView2Deferral](ICoreWebView2Deferral.md) можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="75cb1-126">GetDeferral can be called to return an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object.</span></span>

## <span data-ttu-id="75cb1-127">Участников</span><span class="sxs-lookup"><span data-stu-id="75cb1-127">Members</span></span>

#### <span data-ttu-id="75cb1-128">get_Uri</span><span class="sxs-lookup"><span data-stu-id="75cb1-128">get_Uri</span></span> 

<span data-ttu-id="75cb1-129">URI страницы, запросившего диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="75cb1-129">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="75cb1-130">общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="75cb1-130">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="75cb1-131">get_Kind</span><span class="sxs-lookup"><span data-stu-id="75cb1-131">get_Kind</span></span> 

<span data-ttu-id="75cb1-132">Диалоговое окно "вида JavaScript".</span><span class="sxs-lookup"><span data-stu-id="75cb1-132">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="75cb1-133">общедоступные значения HRESULT [get_Kind](#get_kind)(CORE_WEBVIEW2_SCRIPT_DIALOG_KIND \* видам)</span><span class="sxs-lookup"><span data-stu-id="75cb1-133">public HRESULT [get_Kind](#get_kind)(CORE_WEBVIEW2_SCRIPT_DIALOG_KIND \* kind)</span></span>

<span data-ttu-id="75cb1-134">Приняв, подтвердите, запросите или beforeunload.</span><span class="sxs-lookup"><span data-stu-id="75cb1-134">Accept, confirm, prompt, or beforeunload.</span></span>

#### <span data-ttu-id="75cb1-135">get_Message</span><span class="sxs-lookup"><span data-stu-id="75cb1-135">get_Message</span></span> 

<span data-ttu-id="75cb1-136">Сообщение в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="75cb1-136">The message of the dialog box.</span></span>

> <span data-ttu-id="75cb1-137">общедоступное значение HRESULT [get_Message](#get_message)(LPWSTR \* сообщение)</span><span class="sxs-lookup"><span data-stu-id="75cb1-137">public HRESULT [get_Message](#get_message)(LPWSTR \* message)</span></span>

<span data-ttu-id="75cb1-138">Из JavaScript это первый параметр, передаваемый в Alert, Confirm и Prompt, и он пуст для beforeunload.</span><span class="sxs-lookup"><span data-stu-id="75cb1-138">From JavaScript this is the first parameter passed to alert, confirm, and prompt and is empty for beforeunload.</span></span>

#### <span data-ttu-id="75cb1-139">Принять</span><span class="sxs-lookup"><span data-stu-id="75cb1-139">Accept</span></span> 

<span data-ttu-id="75cb1-140">Основное приложение может вызвать этот метод, чтобы ответить с помощью команды "ОК" для подтверждения, запроса и beforeunload диалоговых окон или вызова этого метода для указания отмены.</span><span class="sxs-lookup"><span data-stu-id="75cb1-140">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="75cb1-141">общедоступное значение HRESULT [принято](#accept)()</span><span class="sxs-lookup"><span data-stu-id="75cb1-141">public HRESULT [Accept](#accept)()</span></span>

<span data-ttu-id="75cb1-142">Из JavaScript это означает, что функция Confirm и beforeunload возвращает значение истина, если вызывается метод принятии.</span><span class="sxs-lookup"><span data-stu-id="75cb1-142">From JavaScript, this means that the confirm and beforeunload function returns true if Accept is called.</span></span> <span data-ttu-id="75cb1-143">И для функции Prompt она возвращает значение ResultText, если вызывается метод допуска, и возвращает значение false в противном случае.</span><span class="sxs-lookup"><span data-stu-id="75cb1-143">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="75cb1-144">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="75cb1-144">get_DefaultText</span></span> 

<span data-ttu-id="75cb1-145">Второй параметр, передаваемый диалоговому окну запроса JavaScript.</span><span class="sxs-lookup"><span data-stu-id="75cb1-145">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="75cb1-146">общедоступные значения HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* DefaultText)</span><span class="sxs-lookup"><span data-stu-id="75cb1-146">public HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* defaultText)</span></span>

<span data-ttu-id="75cb1-147">Это значение по умолчанию, используемое в качестве результата функции JavaScript "prompt".</span><span class="sxs-lookup"><span data-stu-id="75cb1-147">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="75cb1-148">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="75cb1-148">get_ResultText</span></span> 

<span data-ttu-id="75cb1-149">Возвращаемое значение функции Prompt для JavaScript при вызове метода "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="75cb1-149">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="75cb1-150">общедоступные значения HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* ResultText)</span><span class="sxs-lookup"><span data-stu-id="75cb1-150">public HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* resultText)</span></span>

<span data-ttu-id="75cb1-151">Этот тип игнорируется, если диалоговое окно не является запросом.</span><span class="sxs-lookup"><span data-stu-id="75cb1-151">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="75cb1-152">Если параметр "принято" не вызывается, это значение игнорируется, и в командной строке возвращается значение "ложь".</span><span class="sxs-lookup"><span data-stu-id="75cb1-152">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="75cb1-153">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="75cb1-153">put_ResultText</span></span> 

<span data-ttu-id="75cb1-154">Задайте свойство ResultText.</span><span class="sxs-lookup"><span data-stu-id="75cb1-154">Set the ResultText property.</span></span>

> <span data-ttu-id="75cb1-155">общедоступные значения HRESULT [put_ResultText](#put_resulttext)(LPCWSTR ResultText)</span><span class="sxs-lookup"><span data-stu-id="75cb1-155">public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR resultText)</span></span>

#### <span data-ttu-id="75cb1-156">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="75cb1-156">GetDeferral</span></span> 

<span data-ttu-id="75cb1-157">Для возврата объекта [ICoreWebView2Deferral](ICoreWebView2Deferral.md) можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="75cb1-157">GetDeferral can be called to return an [ICoreWebView2Deferral](ICoreWebView2Deferral.md) object.</span></span>

> <span data-ttu-id="75cb1-158">общедоступный HRESULT- [РБП](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \* \* РБП)</span><span class="sxs-lookup"><span data-stu-id="75cb1-158">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](ICoreWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="75cb1-159">Вы можете использовать этот параметр, чтобы выполнить событие позже.</span><span class="sxs-lookup"><span data-stu-id="75cb1-159">You can use this to complete the event at a later time.</span></span>

