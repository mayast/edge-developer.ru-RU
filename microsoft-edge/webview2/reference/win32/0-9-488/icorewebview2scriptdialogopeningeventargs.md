---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: Microsoft Edge WebView2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/07/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: 33450805c7f5117806feb1fb561cd7e0c364f00e
ms.sourcegitcommit: 8dca1c1367853e45a0a975bc89b1818adb117bd4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/08/2020
ms.locfileid: "10698101"
---
# <span data-ttu-id="4d86a-104">интерфейс ICoreWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="4d86a-104">interface ICoreWebView2ScriptDialogOpeningEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="4d86a-105">Эта ссылка может быть изменена или недоступна для выпусков после версии SDK 0.9.515.</span><span class="sxs-lookup"><span data-stu-id="4d86a-105">This reference may be altered or unavailable for releases after SDK version 0.9.515.</span></span> <span data-ttu-id="4d86a-106">Обратитесь к [Справочнику API WebView2](../../../webview2-api-reference.md) для получения последней ссылки на API.</span><span class="sxs-lookup"><span data-stu-id="4d86a-106">Please refer to [WebView2 API reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface ICoreWebView2ScriptDialogOpeningEventArgs
  : public IUnknown
```

<span data-ttu-id="4d86a-107">Аргументы события для события ScriptDialogOpening.</span><span class="sxs-lookup"><span data-stu-id="4d86a-107">Event args for the ScriptDialogOpening event.</span></span>

## <span data-ttu-id="4d86a-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="4d86a-108">Summary</span></span>

 <span data-ttu-id="4d86a-109">Участников</span><span class="sxs-lookup"><span data-stu-id="4d86a-109">Members</span></span>                        | <span data-ttu-id="4d86a-110">Описания</span><span class="sxs-lookup"><span data-stu-id="4d86a-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="4d86a-111">Принять</span><span class="sxs-lookup"><span data-stu-id="4d86a-111">Accept</span></span>](#accept) | <span data-ttu-id="4d86a-112">Основное приложение может вызвать этот метод, чтобы ответить с помощью команды "ОК" для подтверждения, запроса и beforeunload диалоговых окон или вызова этого метода для указания отмены.</span><span class="sxs-lookup"><span data-stu-id="4d86a-112">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="4d86a-113">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="4d86a-113">get_DefaultText</span></span>](#get_defaulttext) | <span data-ttu-id="4d86a-114">Второй параметр, передаваемый диалоговому окну запроса JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4d86a-114">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="4d86a-115">get_Kind</span><span class="sxs-lookup"><span data-stu-id="4d86a-115">get_Kind</span></span>](#get_kind) | <span data-ttu-id="4d86a-116">Диалоговое окно "вида JavaScript".</span><span class="sxs-lookup"><span data-stu-id="4d86a-116">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="4d86a-117">get_Message</span><span class="sxs-lookup"><span data-stu-id="4d86a-117">get_Message</span></span>](#get_message) | <span data-ttu-id="4d86a-118">Сообщение в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="4d86a-118">The message of the dialog box.</span></span>
[<span data-ttu-id="4d86a-119">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="4d86a-119">get_ResultText</span></span>](#get_resulttext) | <span data-ttu-id="4d86a-120">Возвращаемое значение функции Prompt для JavaScript при вызове метода "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="4d86a-120">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="4d86a-121">get_Uri</span><span class="sxs-lookup"><span data-stu-id="4d86a-121">get_Uri</span></span>](#get_uri) | <span data-ttu-id="4d86a-122">URI страницы, запросившего диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="4d86a-122">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="4d86a-123">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="4d86a-123">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="4d86a-124">Для возврата объекта [ICoreWebView2Deferral](icorewebview2deferral.md) можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="4d86a-124">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>
[<span data-ttu-id="4d86a-125">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="4d86a-125">put_ResultText</span></span>](#put_resulttext) | <span data-ttu-id="4d86a-126">Задайте свойство ResultText.</span><span class="sxs-lookup"><span data-stu-id="4d86a-126">Set the ResultText property.</span></span>

## <span data-ttu-id="4d86a-127">Участников</span><span class="sxs-lookup"><span data-stu-id="4d86a-127">Members</span></span>

#### <span data-ttu-id="4d86a-128">Принять</span><span class="sxs-lookup"><span data-stu-id="4d86a-128">Accept</span></span> 

<span data-ttu-id="4d86a-129">Основное приложение может вызвать этот метод, чтобы ответить с помощью команды "ОК" для подтверждения, запроса и beforeunload диалоговых окон или вызова этого метода для указания отмены.</span><span class="sxs-lookup"><span data-stu-id="4d86a-129">The host may call this to respond with OK to confirm, prompt, and beforeunload dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="4d86a-130">общедоступное значение HRESULT [принято](#accept)()</span><span class="sxs-lookup"><span data-stu-id="4d86a-130">public HRESULT [Accept](#accept)()</span></span>

<span data-ttu-id="4d86a-131">Из JavaScript это означает, что функция Confirm и beforeunload возвращает значение истина, если вызывается метод принятии.</span><span class="sxs-lookup"><span data-stu-id="4d86a-131">From JavaScript, this means that the confirm and beforeunload function returns true if Accept is called.</span></span> <span data-ttu-id="4d86a-132">И для функции Prompt она возвращает значение ResultText, если вызывается метод допуска, и возвращает значение false в противном случае.</span><span class="sxs-lookup"><span data-stu-id="4d86a-132">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="4d86a-133">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="4d86a-133">get_DefaultText</span></span> 

<span data-ttu-id="4d86a-134">Второй параметр, передаваемый диалоговому окну запроса JavaScript.</span><span class="sxs-lookup"><span data-stu-id="4d86a-134">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="4d86a-135">общедоступные значения HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* DefaultText)</span><span class="sxs-lookup"><span data-stu-id="4d86a-135">public HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* defaultText)</span></span>

<span data-ttu-id="4d86a-136">Это значение по умолчанию, используемое в качестве результата функции JavaScript "prompt".</span><span class="sxs-lookup"><span data-stu-id="4d86a-136">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="4d86a-137">get_Kind</span><span class="sxs-lookup"><span data-stu-id="4d86a-137">get_Kind</span></span> 

<span data-ttu-id="4d86a-138">Диалоговое окно "вида JavaScript".</span><span class="sxs-lookup"><span data-stu-id="4d86a-138">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="4d86a-139">общедоступные значения HRESULT [get_Kind](#get_kind)(COREWEBVIEW2_SCRIPT_DIALOG_KIND \* видам)</span><span class="sxs-lookup"><span data-stu-id="4d86a-139">public HRESULT [get_Kind](#get_kind)(COREWEBVIEW2_SCRIPT_DIALOG_KIND \* kind)</span></span>

<span data-ttu-id="4d86a-140">Приняв, подтвердите, запросите или beforeunload.</span><span class="sxs-lookup"><span data-stu-id="4d86a-140">Accept, confirm, prompt, or beforeunload.</span></span>

#### <span data-ttu-id="4d86a-141">get_Message</span><span class="sxs-lookup"><span data-stu-id="4d86a-141">get_Message</span></span> 

<span data-ttu-id="4d86a-142">Сообщение в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="4d86a-142">The message of the dialog box.</span></span>

> <span data-ttu-id="4d86a-143">общедоступное значение HRESULT [get_Message](#get_message)(LPWSTR \* сообщение)</span><span class="sxs-lookup"><span data-stu-id="4d86a-143">public HRESULT [get_Message](#get_message)(LPWSTR \* message)</span></span>

<span data-ttu-id="4d86a-144">Из JavaScript это первый параметр, передаваемый в Alert, Confirm и Prompt, и он пуст для beforeunload.</span><span class="sxs-lookup"><span data-stu-id="4d86a-144">From JavaScript this is the first parameter passed to alert, confirm, and prompt and is empty for beforeunload.</span></span>

#### <span data-ttu-id="4d86a-145">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="4d86a-145">get_ResultText</span></span> 

<span data-ttu-id="4d86a-146">Возвращаемое значение функции Prompt для JavaScript при вызове метода "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="4d86a-146">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="4d86a-147">общедоступные значения HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* ResultText)</span><span class="sxs-lookup"><span data-stu-id="4d86a-147">public HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* resultText)</span></span>

<span data-ttu-id="4d86a-148">Этот тип игнорируется, если диалоговое окно не является запросом.</span><span class="sxs-lookup"><span data-stu-id="4d86a-148">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="4d86a-149">Если параметр "принято" не вызывается, это значение игнорируется, и в командной строке возвращается значение "ложь".</span><span class="sxs-lookup"><span data-stu-id="4d86a-149">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="4d86a-150">get_Uri</span><span class="sxs-lookup"><span data-stu-id="4d86a-150">get_Uri</span></span> 

<span data-ttu-id="4d86a-151">URI страницы, запросившего диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="4d86a-151">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="4d86a-152">общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="4d86a-152">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="4d86a-153">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="4d86a-153">GetDeferral</span></span> 

<span data-ttu-id="4d86a-154">Для возврата объекта [ICoreWebView2Deferral](icorewebview2deferral.md) можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="4d86a-154">GetDeferral can be called to return an [ICoreWebView2Deferral](icorewebview2deferral.md) object.</span></span>

> <span data-ttu-id="4d86a-155">общедоступный HRESULT- [РБП](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \* \* РБП)</span><span class="sxs-lookup"><span data-stu-id="4d86a-155">public HRESULT [GetDeferral](#getdeferral)([ICoreWebView2Deferral](icorewebview2deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="4d86a-156">Вы можете использовать этот параметр, чтобы выполнить событие позже.</span><span class="sxs-lookup"><span data-stu-id="4d86a-156">You can use this to complete the event at a later time.</span></span>

#### <span data-ttu-id="4d86a-157">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="4d86a-157">put_ResultText</span></span> 

<span data-ttu-id="4d86a-158">Задайте свойство ResultText.</span><span class="sxs-lookup"><span data-stu-id="4d86a-158">Set the ResultText property.</span></span>

> <span data-ttu-id="4d86a-159">общедоступные значения HRESULT [put_ResultText](#put_resulttext)(LPCWSTR ResultText)</span><span class="sxs-lookup"><span data-stu-id="4d86a-159">public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR resultText)</span></span>

