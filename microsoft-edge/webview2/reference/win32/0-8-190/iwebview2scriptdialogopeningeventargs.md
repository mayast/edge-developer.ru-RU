---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2ScriptDialogOpeningEventArgs
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: de8c8cc2c6c6f857a2889ad167061d2834c30c02
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10885795"
---
# <span data-ttu-id="40d37-104">0.8.355-Interface IWebView2ScriptDialogOpeningEventArgs</span><span class="sxs-lookup"><span data-stu-id="40d37-104">0.8.355 - interface IWebView2ScriptDialogOpeningEventArgs</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2ScriptDialogOpeningEventArgs
  : public IUnknown
```

<span data-ttu-id="40d37-105">Аргументы события для события [IWebView2WebView:: add_ScriptDialogOpening](IWebView2WebView.md#add_scriptdialogopening) .</span><span class="sxs-lookup"><span data-stu-id="40d37-105">Event args for the [IWebView2WebView::add_ScriptDialogOpening](IWebView2WebView.md#add_scriptdialogopening) event.</span></span>

## <span data-ttu-id="40d37-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="40d37-106">Summary</span></span>

 <span data-ttu-id="40d37-107">Участников</span><span class="sxs-lookup"><span data-stu-id="40d37-107">Members</span></span>                        | <span data-ttu-id="40d37-108">Описания</span><span class="sxs-lookup"><span data-stu-id="40d37-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="40d37-109">get_Uri</span><span class="sxs-lookup"><span data-stu-id="40d37-109">get_Uri</span></span>](#get_uri) | <span data-ttu-id="40d37-110">URI страницы, запросившего диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="40d37-110">The URI of the page that requested the dialog box.</span></span>
[<span data-ttu-id="40d37-111">get_Kind</span><span class="sxs-lookup"><span data-stu-id="40d37-111">get_Kind</span></span>](#get_kind) | <span data-ttu-id="40d37-112">Диалоговое окно "вида JavaScript".</span><span class="sxs-lookup"><span data-stu-id="40d37-112">The kind of JavaScript dialog box.</span></span>
[<span data-ttu-id="40d37-113">get_Message</span><span class="sxs-lookup"><span data-stu-id="40d37-113">get_Message</span></span>](#get_message) | <span data-ttu-id="40d37-114">Сообщение в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="40d37-114">The message of the dialog box.</span></span>
[<span data-ttu-id="40d37-115">Принять</span><span class="sxs-lookup"><span data-stu-id="40d37-115">Accept</span></span>](#accept) | <span data-ttu-id="40d37-116">Основное приложение может вызвать этот метод, чтобы ответить с помощью команды "ОК", чтобы подтвердить и запросить диалоговые окна, или не вызывайте этот способ для обозначения отмены.</span><span class="sxs-lookup"><span data-stu-id="40d37-116">The host may call this to respond with OK to confirm and prompt dialogs or not call this method to indicate cancel.</span></span>
[<span data-ttu-id="40d37-117">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="40d37-117">get_DefaultText</span></span>](#get_defaulttext) | <span data-ttu-id="40d37-118">Второй параметр, передаваемый диалоговому окну запроса JavaScript.</span><span class="sxs-lookup"><span data-stu-id="40d37-118">The second parameter passed to the JavaScript prompt dialog.</span></span>
[<span data-ttu-id="40d37-119">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="40d37-119">get_ResultText</span></span>](#get_resulttext) | <span data-ttu-id="40d37-120">Возвращаемое значение функции Prompt для JavaScript при вызове метода "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="40d37-120">The return value from the JavaScript prompt function if Accept is called.</span></span>
[<span data-ttu-id="40d37-121">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="40d37-121">put_ResultText</span></span>](#put_resulttext) | <span data-ttu-id="40d37-122">Задайте свойство ResultText.</span><span class="sxs-lookup"><span data-stu-id="40d37-122">Set the ResultText property.</span></span>
[<span data-ttu-id="40d37-123">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="40d37-123">GetDeferral</span></span>](#getdeferral) | <span data-ttu-id="40d37-124">Для возврата объекта [IWebView2Deferral](IWebView2Deferral.md) можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="40d37-124">GetDeferral can be called to return an [IWebView2Deferral](IWebView2Deferral.md) object.</span></span>

## <span data-ttu-id="40d37-125">Участников</span><span class="sxs-lookup"><span data-stu-id="40d37-125">Members</span></span>

#### <span data-ttu-id="40d37-126">get_Uri</span><span class="sxs-lookup"><span data-stu-id="40d37-126">get_Uri</span></span> 

<span data-ttu-id="40d37-127">URI страницы, запросившего диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="40d37-127">The URI of the page that requested the dialog box.</span></span>

> <span data-ttu-id="40d37-128">общедоступные значения HRESULT [get_Uri](#get_uri)(LPWSTR \* URI)</span><span class="sxs-lookup"><span data-stu-id="40d37-128">public HRESULT [get_Uri](#get_uri)(LPWSTR \* uri)</span></span>

#### <span data-ttu-id="40d37-129">get_Kind</span><span class="sxs-lookup"><span data-stu-id="40d37-129">get_Kind</span></span> 

<span data-ttu-id="40d37-130">Диалоговое окно "вида JavaScript".</span><span class="sxs-lookup"><span data-stu-id="40d37-130">The kind of JavaScript dialog box.</span></span>

> <span data-ttu-id="40d37-131">общедоступные значения HRESULT [get_Kind](#get_kind)(WEBVIEW2_SCRIPT_DIALOG_KIND \* видам)</span><span class="sxs-lookup"><span data-stu-id="40d37-131">public HRESULT [get_Kind](#get_kind)(WEBVIEW2_SCRIPT_DIALOG_KIND \* kind)</span></span>

#### <span data-ttu-id="40d37-132">get_Message</span><span class="sxs-lookup"><span data-stu-id="40d37-132">get_Message</span></span> 

<span data-ttu-id="40d37-133">Сообщение в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="40d37-133">The message of the dialog box.</span></span>

> <span data-ttu-id="40d37-134">общедоступное значение HRESULT [get_Message](#get_message)(LPWSTR \* сообщение)</span><span class="sxs-lookup"><span data-stu-id="40d37-134">public HRESULT [get_Message](#get_message)(LPWSTR \* message)</span></span>

<span data-ttu-id="40d37-135">Из JavaScript это первый параметр, передаваемый в Alert, Confirm и Prompt.</span><span class="sxs-lookup"><span data-stu-id="40d37-135">From JavaScript this is the first parameter passed to alert, confirm, and prompt.</span></span>

#### <span data-ttu-id="40d37-136">Принять</span><span class="sxs-lookup"><span data-stu-id="40d37-136">Accept</span></span> 

<span data-ttu-id="40d37-137">Основное приложение может вызвать этот метод, чтобы ответить с помощью команды "ОК", чтобы подтвердить и запросить диалоговые окна, или не вызывайте этот способ для обозначения отмены.</span><span class="sxs-lookup"><span data-stu-id="40d37-137">The host may call this to respond with OK to confirm and prompt dialogs or not call this method to indicate cancel.</span></span>

> <span data-ttu-id="40d37-138">общедоступное значение HRESULT [принято](#accept)()</span><span class="sxs-lookup"><span data-stu-id="40d37-138">public HRESULT [Accept](#accept)()</span></span>

<span data-ttu-id="40d37-139">Из JavaScript это означает, что функция Confirm возвращает значение истина, если вызывается метод принятии.</span><span class="sxs-lookup"><span data-stu-id="40d37-139">From JavaScript this means that the confirm function returns true if Accept is called.</span></span> <span data-ttu-id="40d37-140">И для функции Prompt она возвращает значение ResultText, если вызывается метод допуска, и возвращает значение false в противном случае.</span><span class="sxs-lookup"><span data-stu-id="40d37-140">And for the prompt function it returns the value of ResultText if Accept is called and returns false otherwise.</span></span>

#### <span data-ttu-id="40d37-141">get_DefaultText</span><span class="sxs-lookup"><span data-stu-id="40d37-141">get_DefaultText</span></span> 

<span data-ttu-id="40d37-142">Второй параметр, передаваемый диалоговому окну запроса JavaScript.</span><span class="sxs-lookup"><span data-stu-id="40d37-142">The second parameter passed to the JavaScript prompt dialog.</span></span>

> <span data-ttu-id="40d37-143">общедоступные значения HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* DefaultText)</span><span class="sxs-lookup"><span data-stu-id="40d37-143">public HRESULT [get_DefaultText](#get_defaulttext)(LPWSTR \* defaultText)</span></span>

<span data-ttu-id="40d37-144">Это значение по умолчанию, используемое в качестве результата функции JavaScript "prompt".</span><span class="sxs-lookup"><span data-stu-id="40d37-144">This is the default value to use for the result of the prompt JavaScript function.</span></span>

#### <span data-ttu-id="40d37-145">get_ResultText</span><span class="sxs-lookup"><span data-stu-id="40d37-145">get_ResultText</span></span> 

<span data-ttu-id="40d37-146">Возвращаемое значение функции Prompt для JavaScript при вызове метода "Сохранить".</span><span class="sxs-lookup"><span data-stu-id="40d37-146">The return value from the JavaScript prompt function if Accept is called.</span></span>

> <span data-ttu-id="40d37-147">общедоступные значения HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* ResultText)</span><span class="sxs-lookup"><span data-stu-id="40d37-147">public HRESULT [get_ResultText](#get_resulttext)(LPWSTR \* resultText)</span></span>

<span data-ttu-id="40d37-148">Этот тип игнорируется, если диалоговое окно не является запросом.</span><span class="sxs-lookup"><span data-stu-id="40d37-148">This is ignored for dialog kinds other than prompt.</span></span> <span data-ttu-id="40d37-149">Если параметр "принято" не вызывается, это значение игнорируется, и в командной строке возвращается значение "ложь".</span><span class="sxs-lookup"><span data-stu-id="40d37-149">If Accept is not called this value is ignored and false is returned from prompt.</span></span>

#### <span data-ttu-id="40d37-150">put_ResultText</span><span class="sxs-lookup"><span data-stu-id="40d37-150">put_ResultText</span></span> 

<span data-ttu-id="40d37-151">Задайте свойство ResultText.</span><span class="sxs-lookup"><span data-stu-id="40d37-151">Set the ResultText property.</span></span>

> <span data-ttu-id="40d37-152">общедоступные значения HRESULT [put_ResultText](#put_resulttext)(LPCWSTR ResultText)</span><span class="sxs-lookup"><span data-stu-id="40d37-152">public HRESULT [put_ResultText](#put_resulttext)(LPCWSTR resultText)</span></span>

#### <span data-ttu-id="40d37-153">GetDeferral</span><span class="sxs-lookup"><span data-stu-id="40d37-153">GetDeferral</span></span> 

<span data-ttu-id="40d37-154">Для возврата объекта [IWebView2Deferral](IWebView2Deferral.md) можно вызвать методического РБП.</span><span class="sxs-lookup"><span data-stu-id="40d37-154">GetDeferral can be called to return an [IWebView2Deferral](IWebView2Deferral.md) object.</span></span>

> <span data-ttu-id="40d37-155">общедоступный HRESULT- [РБП](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \* \* РБП)</span><span class="sxs-lookup"><span data-stu-id="40d37-155">public HRESULT [GetDeferral](#getdeferral)([IWebView2Deferral](IWebView2Deferral.md) \*\* deferral)</span></span>

<span data-ttu-id="40d37-156">Вы можете использовать этот параметр, чтобы выполнить событие позже.</span><span class="sxs-lookup"><span data-stu-id="40d37-156">You can use this to complete the event at a later time.</span></span>

