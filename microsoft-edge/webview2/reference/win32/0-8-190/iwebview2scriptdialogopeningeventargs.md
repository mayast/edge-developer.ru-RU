---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2ScriptDialogOpeningEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 052f380caadf08814cc9364f3ccfbb5251fa7c7e
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878199"
---
# <span data-ttu-id="fa84d-104">0.8.355-Interface IWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="fa84d-104">0.8.355 - interface IWebView2ScriptDialogOpeningEventArgs</span></span> 

> [!NOTE]
> <span data-ttu-id="fa84d-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="fa84d-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="fa84d-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="fa84d-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2ScriptDialogOpeningEventArgs
  : public IUnknown
```

<span data-ttu-id="fa84d-107">Аргументы события для события [IWebView2WebView:: add_ScriptDialogOpening](IWebView2WebView.md#add_scriptdialogopening) .</span><span class="sxs-lookup"><span data-stu-id="fa84d-107">Event args for the [IWebView2WebView::add_ScriptDialogOpening](IWebView2WebView.md#add_scriptdialogopening) event.</span></span>

## <span data-ttu-id="fa84d-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="fa84d-108">Summary</span></span>

 <span data-ttu-id="fa84d-109">Участников</span><span class="sxs-lookup"><span data-stu-id="fa84d-109">Members</span></span>                        | <span data-ttu-id="fa84d-110">Описания</span><span class="sxs-lookup"><span data-stu-id="fa84d-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="fa84d-111">get_Uri</span><span class="sxs-lookup"><span data-stu-id="fa84d-111">get_Uri</span></span>](#get_uri) | <span data-ttu-id="fa84d-112">URI страницы, запросившего диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="fa84d-112">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="fa84d-113">get_Kind</span><span class="sxs-lookup"><span data-stu-id="fa84d-113">get_Kind</span></span>](#get_kind) | <span data-ttu-id="fa84d-114">Диалоговое окно "вида JavaScript".</span><span class="sxs-lookup"><span data-stu-id="fa84d-114">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="fa84d-115">get_Message</span><span class="sxs-lookup"><span data-stu-id="fa84d-115">get_Message</span></span>](#get_message) | <span data-ttu-id="fa84d-116">Сообщение в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="fa84d-116">The message of the dialog box.</span></span>
[<span data-ttu-id="fa84d-117">Принять</span><span class="sxs-lookup"><span data-stu-id="fa84d-117">Accept</span></span>](#accept) | <span data-ttu-id="fa84d-118">Основное приложение может вызвать этот метод, чтобы ответить с помощью команды "ОК", чтобы подтвердить и запросить диалоговые окна, или не вызывайте этот способ для обозначения отмены.</span><span class="sxs-lookup"><span data-stu-id="fa84d-118">The host may call this to respond with OK to confirm and prompt dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="fa84d-119">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="fa84d-119">get_DefaultText</span></span>](#get_defaulttext) | <span data-ttu-id="fa84d-120">Второй параметр, передаваемый диалоговому окну запроса JavaScript.</span><span class="sxs-lookup"><span data-stu-id="fa84d-120">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="fa84d-121">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="fa84d-121">get_ResultText</span></span>](#get_resulttext) | <span data-ttu-id="fa84d-122">Возвращаемое значение функции Prompt для JavaScript при вызове метода "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="fa84d-122">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="fa84d-123">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="fa84d-123">put_ResultText</span></span>](#put_resulttext) | <span data-ttu-id="fa84d-124">Задайте свойство ResultText.</span><span class="sxs-lookup"><span data-stu-id="fa84d-124">Set the ResultText property.</span></span>
[<span data-ttu-id="fa84d-125">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="fa84d-125">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="fa84d-126">Для возврата объекта [IWebView2Deferral](IWebView2Deferral.md) можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="fa84d-126">GetDeferral can be called to return an [IWebView2Deferral](IWebView2Deferral.md) object.</span></span>

## <span data-ttu-id="fa84d-127">Участников</span><span class="sxs-lookup"><span data-stu-id="fa84d-127">Members</span></span>

#### <span data-ttu-id="fa84d-128">get_Uri</span><span class="sxs-lookup"><span data-stu-id="fa84d-128">get_Uri</span></span> 

<span data-ttu-id="fa84d-129">URI страницы, запросившего диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="fa84d-129">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="fa84d-130">общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="fa84d-130">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="fa84d-131">get_Kind</span><span class="sxs-lookup"><span data-stu-id="fa84d-131">get_Kind</span></span> 

<span data-ttu-id="fa84d-132">Диалоговое окно "вида JavaScript".</span><span class="sxs-lookup"><span data-stu-id="fa84d-132">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="fa84d-133">общедоступные значения HRESULT [get_Kind](#get_kind)(WEBVIEW2_SCRIPT_DIALOG_KIND \* видам)</span><span class="sxs-lookup"><span data-stu-id="fa84d-133">public HRESULT [get_Kind](#get_kind)(WEBVIEW2_SCRIPT_DIALOG_KIND \* kind)</span></span>

#### <span data-ttu-id="fa84d-134">get_Message</span><span class="sxs-lookup"><span data-stu-id="fa84d-134">get_Message</span></span> 

<span data-ttu-id="fa84d-135">Сообщение в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="fa84d-135">The message of the dialog box.</span></span>

> <span data-ttu-id="fa84d-136">общедоступное значение HRESULT [get_Message](#get_message)(LPWSTR \* сообщение)</span><span class="sxs-lookup"><span data-stu-id="fa84d-136">public HRESULT [get_Message](#get_message)(LPWSTR \* message)</span></span>

<span data-ttu-id="fa84d-137">Из JavaScript это первый параметр, передаваемый в Alert, Confirm и Prompt.</span><span class="sxs-lookup"><span data-stu-id="fa84d-137">From JavaScript this is the first parameter passed to alert, confirm, and prompt.</span></span>

#### <span data-ttu-id="fa84d-138">Принять</span><span class="sxs-lookup"><span data-stu-id="fa84d-138">Accept</span></span> 

<span data-ttu-id="fa84d-139">Основное приложение может вызвать этот метод, чтобы ответить с помощью команды "ОК", чтобы подтвердить и запросить диалоговые окна, или не вызывайте этот способ для обозначения отмены.</span><span class="sxs-lookup"><span data-stu-id="fa84d-139">The host may call this to respond with OK to confirm and prompt dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="fa84d-140">общедоступное значение HRESULT [принято](#accept)()</span><span class="sxs-lookup"><span data-stu-id="fa84d-140">public HRESULT [Accept](#accept)()</span></span>

<span data-ttu-id="fa84d-141">Из JavaScript это означает, что функция Confirm возвращает значение истина, если вызывается метод принятии.</span><span class="sxs-lookup"><span data-stu-id="fa84d-141">From JavaScript this means that the confirm function returns true if Accept is called.</span></span> <span data-ttu-id="fa84d-142">И для функции Prompt она возвращает значение ResultText, если вызывается метод допуска, и возвращает значение false в противном случае.</span><span class="sxs-lookup"><span data-stu-id="fa84d-142">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="fa84d-143">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="fa84d-143">get_DefaultText</span></span> 

<span data-ttu-id="fa84d-144">Второй параметр, передаваемый диалоговому окну запроса JavaScript.</span><span class="sxs-lookup"><span data-stu-id="fa84d-144">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="fa84d-145">общедоступные значения HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* DefaultText)</span><span class="sxs-lookup"><span data-stu-id="fa84d-145">public HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* defaultText)</span></span>

<span data-ttu-id="fa84d-146">Это значение по умолчанию, используемое в качестве результата функции JavaScript "prompt".</span><span class="sxs-lookup"><span data-stu-id="fa84d-146">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="fa84d-147">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="fa84d-147">get_ResultText</span></span> 

<span data-ttu-id="fa84d-148">Возвращаемое значение функции Prompt для JavaScript при вызове метода "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="fa84d-148">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="fa84d-149">общедоступные значения HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* ResultText)</span><span class="sxs-lookup"><span data-stu-id="fa84d-149">public HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* resultText)</span></span>

<span data-ttu-id="fa84d-150">Этот тип игнорируется, если диалоговое окно не является запросом.</span><span class="sxs-lookup"><span data-stu-id="fa84d-150">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="fa84d-151">Если параметр "принято" не вызывается, это значение игнорируется, и в командной строке возвращается значение "ложь".</span><span class="sxs-lookup"><span data-stu-id="fa84d-151">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="fa84d-152">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="fa84d-152">put_ResultText</span></span> 

<span data-ttu-id="fa84d-153">Задайте свойство ResultText.</span><span class="sxs-lookup"><span data-stu-id="fa84d-153">Set the ResultText property.</span></span>

> <span data-ttu-id="fa84d-154">общедоступные значения HRESULT [put_ResultText](#put_resulttext)(LPCWSTR ResultText)</span><span class="sxs-lookup"><span data-stu-id="fa84d-154">public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR resultText)</span></span>

#### <span data-ttu-id="fa84d-155">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="fa84d-155">GetDeferral</span></span> 

<span data-ttu-id="fa84d-156">Для возврата объекта [IWebView2Deferral](IWebView2Deferral.md) можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="fa84d-156">GetDeferral can be called to return an [IWebView2Deferral](IWebView2Deferral.md) object.</span></span>

> <span data-ttu-id="fa84d-157">общедоступный HRESULT- [РБП](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \* \* РБП)</span><span class="sxs-lookup"><span data-stu-id="fa84d-157">public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="fa84d-158">Вы можете использовать этот параметр, чтобы выполнить событие позже.</span><span class="sxs-lookup"><span data-stu-id="fa84d-158">You can use this to complete the event at a later time.</span></span>

