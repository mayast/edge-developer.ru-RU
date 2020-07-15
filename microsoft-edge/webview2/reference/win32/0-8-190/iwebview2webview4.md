---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2WebView4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/14/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 8b029202843dd006be4d9ecdadc63161bebb6b39
ms.sourcegitcommit: f6764f57aed9ab7229e4eb6cc8851d0cea667403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/15/2020
ms.locfileid: "10878059"
---
# <span data-ttu-id="d2e64-104">0.8.355-Interface IWebView2WebView4</span><span class="sxs-lookup"><span data-stu-id="d2e64-104">0.8.355 - interface IWebView2WebView4</span></span> 

> [!NOTE]
> <span data-ttu-id="d2e64-105">Этот интерфейс может быть изменен или недоступен для выпусков после версии SDK 0.8.355.</span><span class="sxs-lookup"><span data-stu-id="d2e64-105">This interface may be altered or unavailable for releases after SDK version 0.8.355.</span></span> <span data-ttu-id="d2e64-106">Ознакомьтесь со [справочной](../../../webview2-api-reference.md) информацией по последней ссылке на API.</span><span class="sxs-lookup"><span data-stu-id="d2e64-106">Please refer to [Reference](../../../webview2-api-reference.md) for the latest API reference.</span></span>

```
interface IWebView2WebView4
  : public IWebView2WebView3
```

<span data-ttu-id="d2e64-107">Дополнительные функции, реализованные основным объектом WebView.</span><span class="sxs-lookup"><span data-stu-id="d2e64-107">Additional functionality implemented by the primary WebView object.</span></span>

## <span data-ttu-id="d2e64-108">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="d2e64-108">Summary</span></span>

 <span data-ttu-id="d2e64-109">Участников</span><span class="sxs-lookup"><span data-stu-id="d2e64-109">Members</span></span>                        | <span data-ttu-id="d2e64-110">Описания</span><span class="sxs-lookup"><span data-stu-id="d2e64-110">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="d2e64-111">AddRemoteObject</span><span class="sxs-lookup"><span data-stu-id="d2e64-111">AddRemoteObject</span></span>](#addremoteobject) | <span data-ttu-id="d2e64-112">Добавьте предоставленный объект узла в сценарий, выполняемый в WebView с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="d2e64-112">Add the provided host object to script running in the WebView with the specified name.</span></span>
[<span data-ttu-id="d2e64-113">RemoveRemoteObject</span><span class="sxs-lookup"><span data-stu-id="d2e64-113">RemoveRemoteObject</span></span>](#removeremoteobject) | <span data-ttu-id="d2e64-114">Удалите объект узла, заданный именем, чтобы он больше не будет доступен из кода JavaScript в WebView.</span><span class="sxs-lookup"><span data-stu-id="d2e64-114">Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the WebView.</span></span>
[<span data-ttu-id="d2e64-115">OpenDevToolsWindow</span><span class="sxs-lookup"><span data-stu-id="d2e64-115">OpenDevToolsWindow</span></span>](#opendevtoolswindow) | <span data-ttu-id="d2e64-116">Открытие окна DevTools для текущего документа в WebView.</span><span class="sxs-lookup"><span data-stu-id="d2e64-116">Opens the DevTools window for the current document in the WebView.</span></span>
[<span data-ttu-id="d2e64-117">add_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="d2e64-117">add_AcceleratorKeyPressed</span></span>](#add_acceleratorkeypressed) | <span data-ttu-id="d2e64-118">Добавьте обработчик событий для события AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="d2e64-118">Add an event handler for the AcceleratorKeyPressed event.</span></span>
[<span data-ttu-id="d2e64-119">remove_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="d2e64-119">remove_AcceleratorKeyPressed</span></span>](#remove_acceleratorkeypressed) | <span data-ttu-id="d2e64-120">Удалите обработчик событий, добавленный ранее add_AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="d2e64-120">Remove an event handler previously added with add_AcceleratorKeyPressed.</span></span>
[<span data-ttu-id="d2e64-121">WEBVIEW2_KEY_EVENT_TYPE</span><span class="sxs-lookup"><span data-stu-id="d2e64-121">WEBVIEW2_KEY_EVENT_TYPE</span></span>](#webview2_key_event_type) | <span data-ttu-id="d2e64-122">Тип события клавиши, которое инициировало событие AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="d2e64-122">The type of key event that triggered an AcceleratorKeyPressed event.</span></span>
[<span data-ttu-id="d2e64-123">WEBVIEW2_PHYSICAL_KEY_STATUS</span><span class="sxs-lookup"><span data-stu-id="d2e64-123">WEBVIEW2_PHYSICAL_KEY_STATUS</span></span>](#webview2_physical_key_status) | <span data-ttu-id="d2e64-124">Структура, представляющая данные, Упакованные в LPARAM, предоставленные событию ключа Win32.</span><span class="sxs-lookup"><span data-stu-id="d2e64-124">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

<span data-ttu-id="d2e64-125">Вы можете QueryInterface для этого интерфейса из объекта, реализующего [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="d2e64-125">You can QueryInterface for this interface from the object that implements [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="d2e64-126">Дополнительные сведения вы видите в интерфейсе [IWebView2WebView](IWebView2WebView.md) .</span><span class="sxs-lookup"><span data-stu-id="d2e64-126">See the [IWebView2WebView](IWebView2WebView.md) interface for more details.</span></span>

## <span data-ttu-id="d2e64-127">Участников</span><span class="sxs-lookup"><span data-stu-id="d2e64-127">Members</span></span>

#### <span data-ttu-id="d2e64-128">AddRemoteObject</span><span class="sxs-lookup"><span data-stu-id="d2e64-128">AddRemoteObject</span></span> 

<span data-ttu-id="d2e64-129">Добавьте предоставленный объект узла в сценарий, выполняемый в WebView с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="d2e64-129">Add the provided host object to script running in the WebView with the specified name.</span></span>

> <span data-ttu-id="d2e64-130">общедоступные значения HRESULT [AddRemoteObject](#addremoteobject)(имя LPCWSTR, переменная \* объект)</span><span class="sxs-lookup"><span data-stu-id="d2e64-130">public HRESULT [AddRemoteObject](#addremoteobject)(LPCWSTR name,VARIANT \* object)</span></span>

<span data-ttu-id="d2e64-131">Объекты узла предоставляются как прокси удаленных объектов через `window.chrome.webview.remoteObjects.<name>` .</span><span class="sxs-lookup"><span data-stu-id="d2e64-131">Host objects are exposed as remote object proxies via `window.chrome.webview.remoteObjects.<name>`.</span></span> <span data-ttu-id="d2e64-132">Удаленные прокси-объекты являются обещанными и разрешаются в объект, представляющий объект Host.</span><span class="sxs-lookup"><span data-stu-id="d2e64-132">Remote object proxies are promises and will resolve to an object representing the host object.</span></span> <span data-ttu-id="d2e64-133">Обещание отклонено, если приложение не добавило объект с именем.</span><span class="sxs-lookup"><span data-stu-id="d2e64-133">The promise is rejected if the app has not added an object with the name.</span></span> <span data-ttu-id="d2e64-134">Когда код JavaScript обращается к свойству или методу объекта, для него возвращается значение, которое будет обрабатываться в соответствии со значением, возвращенным из хоста для свойства или метода, или отброшено в случае ошибки, например, отсутствие такого свойства или метода для объекта или параметров недопустимым.</span><span class="sxs-lookup"><span data-stu-id="d2e64-134">When JavaScript code access a property or method of the object, a promise is return, which will resolve to the value returned from the host for the property or method, or rejected in case of error such as there is no such property or method on the object or parameters are invalid.</span></span> <span data-ttu-id="d2e64-135">Например, когда код приложения делает следующее:</span><span class="sxs-lookup"><span data-stu-id="d2e64-135">For example, when the application code does the following:</span></span> 

```cpp
VARIANT object;
object.vt = VT_DISPATCH;
object.pdispVal = appObject;
webview->AddRemoteObject(L"host_object", &host);
```

 <span data-ttu-id="d2e64-136">Код JavaScript в WebView сможет получить доступ к appObject следующим образом, а затем получить доступ к атрибутам и методам appObject:</span><span class="sxs-lookup"><span data-stu-id="d2e64-136">JavaScript code in the WebView will be able to access appObject as following and then access attributes and methods of appObject:</span></span> 

```js
let app_object = await window.chrome.webview.remoteObjects.host_object;
let attr1 = await app_object.attr1;
let result = await app_object.method1(parameters);
```

 <span data-ttu-id="d2e64-137">Обратите внимание, что хотя простые типы, IDispatch и Array поддерживаются, универсальный IUnknown, VT_DECIMAL или VT_RECORD Variant не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="d2e64-137">Note that while simple types, IDispatch and array are supported, generic IUnknown, VT_DECIMAL, or VT_RECORD variant is not supported.</span></span> <span data-ttu-id="d2e64-138">Удаленные объекты JavaScript, такие как функции обратного вызова, представлены как VT_DISPATCH VARIANT с помощью объекта, реализующего IDispatch.</span><span class="sxs-lookup"><span data-stu-id="d2e64-138">Remote JavaScript objects like callback functions are represented as an VT_DISPATCH VARIANT with the object implementing IDispatch.</span></span> <span data-ttu-id="d2e64-139">Метод обратного вызова JavaScript можно вызвать с помощью DISPID_VALUE для DISPID.</span><span class="sxs-lookup"><span data-stu-id="d2e64-139">The JavaScript callback method may be invoked using DISPID_VALUE for the DISPID.</span></span> <span data-ttu-id="d2e64-140">Вложенные массивы поддерживаются до 3 уровней.</span><span class="sxs-lookup"><span data-stu-id="d2e64-140">Nested arrays are supported up to a depth of 3.</span></span> <span data-ttu-id="d2e64-141">Массивы по типам ссылок не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="d2e64-141">Arrays of by reference types are not supported.</span></span> <span data-ttu-id="d2e64-142">VT_EMPTY и VT_NULL сопоставлены в JavaScript как null.</span><span class="sxs-lookup"><span data-stu-id="d2e64-142">VT_EMPTY and VT_NULL are mapped into JavaScript as null.</span></span> <span data-ttu-id="d2e64-143">В JavaScript NULL и undefine сопоставляются с VT_EMPTY.</span><span class="sxs-lookup"><span data-stu-id="d2e64-143">In JavaScript null and undefined are mapped to VT_EMPTY.</span></span>

<span data-ttu-id="d2e64-144">Кроме того, все удаленные объекты представляются как `window.chrome.webview.remoteObjects.sync.<name>` .</span><span class="sxs-lookup"><span data-stu-id="d2e64-144">Additionally, all remote objects are exposed as `window.chrome.webview.remoteObjects.sync.<name>`.</span></span> <span data-ttu-id="d2e64-145">Здесь объекты узла предоставляются как синхронные удаленные прокси-объекты.</span><span class="sxs-lookup"><span data-stu-id="d2e64-145">Here the host objects are exposed as synchronous remote object proxies.</span></span> <span data-ttu-id="d2e64-146">Эти функции не предназначены для того, чтобы синхронно блокировать выполняемые сценарии, ожидающие общения для запуска кода хоста.</span><span class="sxs-lookup"><span data-stu-id="d2e64-146">These are not promises and calls to functions or property access synchronously block running script waiting to communicate cross process for the host code to run.</span></span> <span data-ttu-id="d2e64-147">Таким образом, это может привести к проблемам с надежностью, поэтому рекомендуется использовать асинхронный API на основе Promise, `window.chrome.webview.remoteObjects.<name>` описанный выше.</span><span class="sxs-lookup"><span data-stu-id="d2e64-147">Accordingly this can result in reliability issues and it is recommended that you use the promise based asynchronous `window.chrome.webview.remoteObjects.<name>` API described above.</span></span>

<span data-ttu-id="d2e64-148">Синхронные удаленные прокси-объекты и асинхронные удаленные прокси-объекты могут одновременно выполнять прокси для одного и того же удаленного объекта.</span><span class="sxs-lookup"><span data-stu-id="d2e64-148">Synchronous remote object proxies and asynchronous remote object proxies can both proxy the same remote object.</span></span> <span data-ttu-id="d2e64-149">Удаленные изменения, внесенные одним прокси-сервером, будут отражаться в любом другом прокси того же удаленного объекта, независимо от того, являются ли они другими прокси-объектами, синхронными или асинхронными.</span><span class="sxs-lookup"><span data-stu-id="d2e64-149">Remote changes made by one proxy will be reflected in any other proxy of that same remote object whether the other proxies and synchronous or asynchronous.</span></span>

<span data-ttu-id="d2e64-150">Несмотря на то, что JavaScript блокируется на синхронный вызов машинного кода, этот машинный код не может снова вызвать JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d2e64-150">While JavaScript is blocked on a synchronous call to native code, that native code is unable to call back to JavaScript.</span></span> <span data-ttu-id="d2e64-151">При попытке выполнить это действие произойдет сбой с HRESULT_FROM_WIN32 (ERROR_POSSIBLE_DEADLOCK).</span><span class="sxs-lookup"><span data-stu-id="d2e64-151">Attempts to do so will fail with HRESULT_FROM_WIN32(ERROR_POSSIBLE_DEADLOCK).</span></span>

<span data-ttu-id="d2e64-152">Удаленные прокси-объекты — это прокси JavaScript, который перехватывает все вызовы свойств Get, Set и Method.</span><span class="sxs-lookup"><span data-stu-id="d2e64-152">Remote object proxies are JavaScript Proxy objects that intercept all property get, property set, and method invocations.</span></span> <span data-ttu-id="d2e64-153">Свойства или методы, которые являются частью прототипа функции или объекта, выполняются локально.</span><span class="sxs-lookup"><span data-stu-id="d2e64-153">Properties or methods that are a part of the Function or Object prototype are run locally.</span></span> <span data-ttu-id="d2e64-154">Кроме того, любое свойство или метод в массиве `chrome.webview.remoteObjects.options.forceLocalProperties` также будет выполняться локально.</span><span class="sxs-lookup"><span data-stu-id="d2e64-154">Additionally any property or method in the array `chrome.webview.remoteObjects.options.forceLocalProperties` will also be run locally.</span></span> <span data-ttu-id="d2e64-155">Эти значения по умолчанию включают в себя дополнительные методы, которые имеют значение в JavaScript Like `toJSON` и `Symbol.toPrimitive` .</span><span class="sxs-lookup"><span data-stu-id="d2e64-155">This defaults to including optional methods that have meaning in JavaScript like `toJSON` and `Symbol.toPrimitive`.</span></span> <span data-ttu-id="d2e64-156">При необходимости вы можете добавить в этот массив дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="d2e64-156">You can add more to this array as required.</span></span>

<span data-ttu-id="d2e64-157">Существует метод `chrome.webview.remoteObjects.cleanupSome` , который лучше всего подходит для сборщиков мусора удаленных объектов.</span><span class="sxs-lookup"><span data-stu-id="d2e64-157">There's a method `chrome.webview.remoteObjects.cleanupSome` that will best effort garbage collect remote object proxies.</span></span>

<span data-ttu-id="d2e64-158">Удаленные прокси-объекты также обладают следующими методами, которые выполняются локально.</span><span class="sxs-lookup"><span data-stu-id="d2e64-158">Remote object proxies additionally have the following methods which run locally:</span></span>

* <span data-ttu-id="d2e64-159">applyRemote,-Remote, setRemote: выполняет вызов метода, свойство get или набор свойств для удаленного объекта.</span><span class="sxs-lookup"><span data-stu-id="d2e64-159">applyRemote, getRemote, setRemote: Perform a method invocation, property get, or property set on the remote object.</span></span> <span data-ttu-id="d2e64-160">Вы можете использовать их, чтобы явным образом запускать метод или свойство, если существует конфликтующий локальный метод или свойство.</span><span class="sxs-lookup"><span data-stu-id="d2e64-160">You can use these to explicitly force a method or property to run remotely if there is a conflicting local method or property.</span></span> <span data-ttu-id="d2e64-161">Например, `proxy.toString()` будет выполнен локальный метод ToString для прокси-объекта.</span><span class="sxs-lookup"><span data-stu-id="d2e64-161">For instance, `proxy.toString()` will run the local toString method on the proxy object.</span></span> <span data-ttu-id="d2e64-162">Но `proxy.applyRemote('toString')` выполняется `toString` на удаленном прокси-объекте.</span><span class="sxs-lookup"><span data-stu-id="d2e64-162">But `proxy.applyRemote('toString')` runs `toString` on the remote proxied object instead.</span></span>

* <span data-ttu-id="d2e64-163">"по локальной, setLocal" — выполнение свойства Get или установка свойства локально.</span><span class="sxs-lookup"><span data-stu-id="d2e64-163">getLocal, setLocal: Perform property get, or property set locally.</span></span> <span data-ttu-id="d2e64-164">Эти методы можно использовать, чтобы принудительно получить или задать свойство в самом удаленном прокси-объекте, а не на удаленном объекте, который он представляет.</span><span class="sxs-lookup"><span data-stu-id="d2e64-164">You can use these methods to force getting or setting a property on the remote object proxy itself rather than on the remote object it represents.</span></span> <span data-ttu-id="d2e64-165">Например, `proxy.unknownProperty` будет получено свойство с именем `unknownProperty` из удаленного прокси-объекта.</span><span class="sxs-lookup"><span data-stu-id="d2e64-165">For instance, `proxy.unknownProperty` will get the property named `unknownProperty` from the remote proxied object.</span></span> <span data-ttu-id="d2e64-166">Но `proxy.getLocal('unknownProperty')` будет получить значение свойства `unknownProperty` для самого объекта прокси.</span><span class="sxs-lookup"><span data-stu-id="d2e64-166">But `proxy.getLocal('unknownProperty')` will get the value of the property `unknownProperty` on the proxy object itself.</span></span>

* <span data-ttu-id="d2e64-167">Синхронизация: асинхронные удаленные прокси-объекты предоставляют метод синхронизации, возвращающий обещание для синхронного удаленного объектного прокси для того же удаленного объекта.</span><span class="sxs-lookup"><span data-stu-id="d2e64-167">sync: Asynchronous remote object proxies expose a sync method which returns a promise for a synchronous remote object proxy for the same remote object.</span></span> <span data-ttu-id="d2e64-168">Например, `chrome.webview.remoteObjects.sample.methodCall()` возвращает асинхронный удаленный прокси-объект.</span><span class="sxs-lookup"><span data-stu-id="d2e64-168">For example, `chrome.webview.remoteObjects.sample.methodCall()` returns an asynchronous remote object proxy.</span></span> <span data-ttu-id="d2e64-169">Вы можете использовать этот `sync` метод, чтобы получить для него синхронный удаленный прокси-объект.</span><span class="sxs-lookup"><span data-stu-id="d2e64-169">You can use the `sync` method to obtain a synchronous remote object proxy instead:</span></span> `const syncProxy = await chrome.webview.remoteObjects.sample.methodCall().sync()`

* <span data-ttu-id="d2e64-170">Async: синхронные удаленные прокси-объекты предоставляют метод async, который блокирует и возвращает асинхронный удаленный прокси-объект для того же удаленного объекта.</span><span class="sxs-lookup"><span data-stu-id="d2e64-170">async: Synchronous remote object proxies expose an async method which blocks and returns an asynchronous remote object proxy for the same remote object.</span></span> <span data-ttu-id="d2e64-171">Например, `chrome.webview.remoteObjects.sync.sample.methodCall()` возвращает синхронный удаленный прокси-объект.</span><span class="sxs-lookup"><span data-stu-id="d2e64-171">For example, `chrome.webview.remoteObjects.sync.sample.methodCall()` returns a synchronous remote object proxy.</span></span> <span data-ttu-id="d2e64-172">При вызове `async` метода на этих блоках возвращается асинхронный удаленный прокси-объект для того же удаленного объекта:</span><span class="sxs-lookup"><span data-stu-id="d2e64-172">Calling the `async` method on this blocks and then returns an asynchronous remote object proxy for the same remote object:</span></span> `const asyncProxy = chrome.webview.remoteObjects.sync.sample.methodCall().async()`

* <span data-ttu-id="d2e64-173">затем: асинхронные удаленные прокси-объекты имеют метод then.</span><span class="sxs-lookup"><span data-stu-id="d2e64-173">then: Asynchronous remote object proxies have a then method.</span></span> <span data-ttu-id="d2e64-174">Это позволит им доставлять ожидающие.</span><span class="sxs-lookup"><span data-stu-id="d2e64-174">This allows them to be awaitable.</span></span> `then` <span data-ttu-id="d2e64-175">Возвращает обещание, которое разрешается с представлением удаленного объекта.</span><span class="sxs-lookup"><span data-stu-id="d2e64-175">will return a promise that resolves with a representation of the remote object.</span></span> <span data-ttu-id="d2e64-176">Если прокси представляет литерал JavaScript, то копия, возвращаемая им, будет возвращена локально.</span><span class="sxs-lookup"><span data-stu-id="d2e64-176">If the proxy represents a JavaScript literal then a copy of that is returned locally.</span></span> <span data-ttu-id="d2e64-177">Если прокси представляет функцию, возвращается прокси-сервер, не ожидающий ожидания.</span><span class="sxs-lookup"><span data-stu-id="d2e64-177">If the proxy represents a function then a non-awaitable proxy is returned.</span></span> <span data-ttu-id="d2e64-178">Если прокси представляет объект JavaScript с сочетанием литеральных свойств и свойств функций, то копия объекта возвращается с некоторыми свойствами в качестве удаленных прокси-объектов.</span><span class="sxs-lookup"><span data-stu-id="d2e64-178">If the proxy represents a JavaScript object with a mix of literal properties and function properties, then the a copy of the object is returned with some properties as remote object proxies.</span></span>

<span data-ttu-id="d2e64-179">Все другие вызовы свойств и методов (Кроме описанных выше методов прокси-сервера удаленного объекта, списка forceLocalProperties и свойств прототипов функций и объектов) выполняются удаленно.</span><span class="sxs-lookup"><span data-stu-id="d2e64-179">All other property and method invocations (other than the above Remote object proxy methods, forceLocalProperties list, and properties on Function and Object prototypes) are run remotely.</span></span> <span data-ttu-id="d2e64-180">Асинхронные удаленные прокси-объекты возвращают обещание, представляющее собой асинхронное завершение удаленного вызова метода или получение свойства.</span><span class="sxs-lookup"><span data-stu-id="d2e64-180">Asynchronous remote object proxies return a promise representing asynchronous completion of remotely invoking the method, or getting the property.</span></span> <span data-ttu-id="d2e64-181">Обещание устраняется после завершения удаленных операций, и обещание разрешается в полученное значение операции.</span><span class="sxs-lookup"><span data-stu-id="d2e64-181">The promise resolves after the remote operations complete and the promises resolve to the resulting value of the operation.</span></span> <span data-ttu-id="d2e64-182">Синхронные удаленные прокси-объекты работают точно так же, но блокируют выполнение JavaScript и дождитесь завершения удаленной операции.</span><span class="sxs-lookup"><span data-stu-id="d2e64-182">Synchronous remote object proxies work similarly but block JavaScript execution and wait for the remote operation to complete.</span></span>

<span data-ttu-id="d2e64-183">Установка свойства для прокси-сервера асинхронного удаленного объекта немного не изменилась.</span><span class="sxs-lookup"><span data-stu-id="d2e64-183">Setting a property on an asynchronous remote object proxy works slightly differently.</span></span> <span data-ttu-id="d2e64-184">Функция Set возвращает значение немедленно и возвращаемое значение является значением, которое будет задано.</span><span class="sxs-lookup"><span data-stu-id="d2e64-184">The set returns immediately and the return value is the value that will be set.</span></span> <span data-ttu-id="d2e64-185">Это требование для прокси-объекта JavaScript.</span><span class="sxs-lookup"><span data-stu-id="d2e64-185">This is a requirement of the JavaScript Proxy object.</span></span> <span data-ttu-id="d2e64-186">Если необходимо асинхронно дождаться завершения установки свойства, используйте метод setRemote, который возвращает обещание, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="d2e64-186">If you need to asynchronously wait for the property set to complete, use the setRemote method which returns a promise as described above.</span></span> <span data-ttu-id="d2e64-187">Синхронно заданное свойство свойства объекта для синхронно блокируется, пока не задано свойство.</span><span class="sxs-lookup"><span data-stu-id="d2e64-187">Synchronous object property set property synchronously blocks until the property is set.</span></span>

<span data-ttu-id="d2e64-188">Например, предположим, что у вас есть COM-объект со следующим интерфейсом</span><span class="sxs-lookup"><span data-stu-id="d2e64-188">For example, suppose you have a COM object with the following interface</span></span>

```idl
    [uuid(3a14c9c0-bc3e-453f-a314-4ce4a0ec81d8), object, local]
    interface IRemoteObjectSample : IUnknown
    {
        // Demonstrate basic method call with some parameters and a return value.
        HRESULT MethodWithParametersAndReturnValue([in] BSTR stringParameter, [in] INT integerParameter, [out, retval] BSTR* stringResult);

        // Demonstrate getting and setting a property.
        [propget] HRESULT Property([out, retval] BSTR* stringResult);
        [propput] HRESULT Property([in] BSTR stringValue);

        // Demonstrate native calling back into JavaScript.
        HRESULT CallCallbackAsynchronously([in] IDispatch* callbackParameter);
    };
```

 <span data-ttu-id="d2e64-189">Мы можем добавить экземпляр этого интерфейса в наш сценарий JavaScript `AddRemoteObject` .</span><span class="sxs-lookup"><span data-stu-id="d2e64-189">We can add an instance of this interface into our JavaScript with `AddRemoteObject`.</span></span> <span data-ttu-id="d2e64-190">В этом случае мы присвойте ему имя `sample` :</span><span class="sxs-lookup"><span data-stu-id="d2e64-190">In this case we name it `sample`:</span></span>

```cpp
            VARIANT remoteObjectAsVariant = {};
            m_remoteObject.query_to<IDispatch>(&remoteObjectAsVariant.pdispVal);
            remoteObjectAsVariant.vt = VT_DISPATCH;

            // We can call AddRemoteObject multiple times in a row without
            // calling RemoveRemoteObject first. This will replace the previous object
            // with the new object. In our case this is the same object and everything
            // is fine.
            CHECK_FAILURE(m_webView->AddRemoteObject(L"sample", &remoteObjectAsVariant));
            remoteObjectAsVariant.pdispVal->Release();
```

 <span data-ttu-id="d2e64-191">Затем в HTML-документе мы можем использовать этот COM-объект через `chrome.webview.remoteObjects.sample` :</span><span class="sxs-lookup"><span data-stu-id="d2e64-191">Then in the HTML document we can use this COM object via `chrome.webview.remoteObjects.sample`:</span></span>

```js
        document.getElementById("getPropertyAsyncButton").addEventListener("click", async () => {
            const propertyValue = await chrome.webview.remoteObjects.sample.property;
            document.getElementById("getPropertyAsyncOutput").textContent = propertyValue;
        });

        document.getElementById("getPropertySyncButton").addEventListener("click", () => {
            const propertyValue = chrome.webview.remoteObjects.sync.sample.property;
            document.getElementById("getPropertySyncOutput").textContent = propertyValue;
        });

        document.getElementById("setPropertyAsyncButton").addEventListener("click", async () => {
            const propertyValue = document.getElementById("setPropertyAsyncInput").value;
            // The following line will work but it will return immediately before the property value has actually been set.
            // If you need to set the property and wait for the property to change value, use the setRemote function.
            chrome.webview.remoteObjects.sample.property = propertyValue;
            document.getElementById("setPropertyAsyncOutput").textContent = "Set";
        });

        document.getElementById("setPropertyExplicitAsyncButton").addEventListener("click", async () => {
            const propertyValue = document.getElementById("setPropertyExplicitAsyncInput").value;
            // If you care about waiting until the property has actually changed value use the setRemote function.
            await chrome.webview.remoteObjects.sample.setRemote("property", propertyValue);
            document.getElementById("setPropertyExplicitAsyncOutput").textContent = "Set";
        });

        document.getElementById("setPropertySyncButton").addEventListener("click", () => {
            const propertyValue = document.getElementById("setPropertySyncInput").value;
            chrome.webview.remoteObjects.sync.sample.property = propertyValue;
            document.getElementById("setPropertySyncOutput").textContent = "Set";
        });

        document.getElementById("invokeMethodAsyncButton").addEventListener("click", async () => {
            const paramValue1 = document.getElementById("invokeMethodAsyncParam1").value;
            const paramValue2 = parseInt(document.getElementById("invokeMethodAsyncParam2").value);
            const resultValue = await chrome.webview.remoteObjects.sample.MethodWithParametersAndReturnValue(paramValue1, paramValue2);
            document.getElementById("invokeMethodAsyncOutput").textContent = resultValue;
        });

        document.getElementById("invokeMethodSyncButton").addEventListener("click", () => {
            const paramValue1 = document.getElementById("invokeMethodSyncParam1").value;
            const paramValue2 = parseInt(document.getElementById("invokeMethodSyncParam2").value);
            const resultValue = chrome.webview.remoteObjects.sync.sample.MethodWithParametersAndReturnValue(paramValue1, paramValue2);
            document.getElementById("invokeMethodSyncOutput").textContent = resultValue;
        });

        let callbackCount = 0;
        document.getElementById("invokeCallbackButton").addEventListener("click", async () => {
            chrome.webview.remoteObjects.sample.CallCallbackAsynchronously(() => {
                document.getElementById("invokeCallbackOutput").textContent = "Native object called the callback " + (++callbackCount) + " time(s).";
            });
        });
```

#### <span data-ttu-id="d2e64-192">RemoveRemoteObject</span><span class="sxs-lookup"><span data-stu-id="d2e64-192">RemoveRemoteObject</span></span> 

<span data-ttu-id="d2e64-193">Удалите объект узла, заданный именем, чтобы он больше не будет доступен из кода JavaScript в WebView.</span><span class="sxs-lookup"><span data-stu-id="d2e64-193">Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the WebView.</span></span>

> <span data-ttu-id="d2e64-194">общедоступное значение HRESULT [RemoveRemoteObject](#removeremoteobject)(имя LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="d2e64-194">public HRESULT [RemoveRemoteObject](#removeremoteobject)(LPCWSTR name)</span></span>

<span data-ttu-id="d2e64-195">Несмотря на то что новые попытки доступа будут отвергнуты, если объект уже получен кодом JavaScript в WebView, код JavaScript продолжит получать доступ к этому объекту.</span><span class="sxs-lookup"><span data-stu-id="d2e64-195">While new access attempts will be denied, if the object is already obtained by JavaScript code in the WebView, the JavaScript code will continue to have access to that object.</span></span> <span data-ttu-id="d2e64-196">Вызов этого метода для имени, которое уже удалено или не было добавлено, завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="d2e64-196">Calling this method for a name that is already removed or never added will fail.</span></span>

#### <span data-ttu-id="d2e64-197">OpenDevToolsWindow</span><span class="sxs-lookup"><span data-stu-id="d2e64-197">OpenDevToolsWindow</span></span> 

<span data-ttu-id="d2e64-198">Открытие окна DevTools для текущего документа в WebView.</span><span class="sxs-lookup"><span data-stu-id="d2e64-198">Opens the DevTools window for the current document in the WebView.</span></span>

> <span data-ttu-id="d2e64-199">общедоступные значения HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()</span><span class="sxs-lookup"><span data-stu-id="d2e64-199">public HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()</span></span>

<span data-ttu-id="d2e64-200">Ничего не происходит, если он вызывается, когда окно DevTools уже открыто</span><span class="sxs-lookup"><span data-stu-id="d2e64-200">Does nothing if called when the DevTools window is already open</span></span>

#### <span data-ttu-id="d2e64-201">add_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="d2e64-201">add_AcceleratorKeyPressed</span></span> 

<span data-ttu-id="d2e64-202">Добавьте обработчик событий для события AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="d2e64-202">Add an event handler for the AcceleratorKeyPressed event.</span></span>

> <span data-ttu-id="d2e64-203">общедоступные значения HRESULT [add_AcceleratorKeyPressed](#add_acceleratorkeypressed)([IWebView2AcceleratorKeyPressedEventHandler](IWebView2AcceleratorKeyPressedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="d2e64-203">public HRESULT [add_AcceleratorKeyPressed](#add_acceleratorkeypressed)([IWebView2AcceleratorKeyPressedEventHandler](IWebView2AcceleratorKeyPressedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="d2e64-204">AcceleratorKeyPressed активируется при нажатии или отпускании клавиши сочетания клавиш в том случае, если WebView имеет фокус.</span><span class="sxs-lookup"><span data-stu-id="d2e64-204">AcceleratorKeyPressed fires when an accelerator key or key combo is pressed or released while the WebView is focused.</span></span> <span data-ttu-id="d2e64-205">Клавиша считается ускорителем по одной из следующих способов:</span><span class="sxs-lookup"><span data-stu-id="d2e64-205">A key is considered an accelerator if either:</span></span>

1. <span data-ttu-id="d2e64-206">В данный момент удерживается клавиша CTRL или ALT;</span><span class="sxs-lookup"><span data-stu-id="d2e64-206">Ctrl or Alt is currently being held, or</span></span>

1. <span data-ttu-id="d2e64-207">Нажатая клавиша не сопоставляется с символом.</span><span class="sxs-lookup"><span data-stu-id="d2e64-207">the pressed key does not map to a character.</span></span> <span data-ttu-id="d2e64-208">Некоторые неопределенные клавиши никогда не рассматриваются как ускорители, например Shift.</span><span class="sxs-lookup"><span data-stu-id="d2e64-208">A few specific keys are never considered accelerators, such as Shift.</span></span> <span data-ttu-id="d2e64-209">Клавиша ESC всегда считается ускорителем.</span><span class="sxs-lookup"><span data-stu-id="d2e64-209">The Escape key is always considered an accelerator.</span></span>

<span data-ttu-id="d2e64-210">Событие с автоматическим нажатием клавиши, вызванное удерживанием нажатой клавиши, также срабатывает.</span><span class="sxs-lookup"><span data-stu-id="d2e64-210">Autorepeated key events caused by holding the key down will also fire this event.</span></span> <span data-ttu-id="d2e64-211">Чтобы отфильтровать эти данные, Проверьте аргументы события "KeyEventLParam" или "PhysicalKeyStatus".</span><span class="sxs-lookup"><span data-stu-id="d2e64-211">You can filter these out by checking the event args' KeyEventLParam or PhysicalKeyStatus.</span></span>

<span data-ttu-id="d2e64-212">В оконном режиме этот обработчик событий вызывается синхронно.</span><span class="sxs-lookup"><span data-stu-id="d2e64-212">In windowed mode, this event handler is called synchronously.</span></span> <span data-ttu-id="d2e64-213">До тех пор пока вы не вызываете Handle () для аргументов события или не будет возвращен обработчик событий, процесс браузера будет заблокирован и исходящие межпроцессные вызовы COM не будут работать с RPC_E_CANTCALLOUT_ININPUTSYNCCALL.</span><span class="sxs-lookup"><span data-stu-id="d2e64-213">Until you call Handle() on the event args or the event handler returns, the browser process will be blocked and outgoing cross-process COM calls will fail with RPC_E_CANTCALLOUT_ININPUTSYNCCALL.</span></span> <span data-ttu-id="d2e64-214">Однако все методы API WebView2 будут работать.</span><span class="sxs-lookup"><span data-stu-id="d2e64-214">All WebView2 API methods will work, however.</span></span>

<span data-ttu-id="d2e64-215">В режиме безоконный обработчик событий вызывается асинхронно.</span><span class="sxs-lookup"><span data-stu-id="d2e64-215">In windowless mode, the event handler is called asynchronously.</span></span> <span data-ttu-id="d2e64-216">Дальнейшие входные данные не доходят до браузера, пока обработчик событий не возвратит или не завершит вызов (), но сам процесс браузера не будет заблокирован, а исходящие вызовы COM будут работать нормально.</span><span class="sxs-lookup"><span data-stu-id="d2e64-216">Further input will not reach the browser until the event handler returns or Handle() is called, but the browser process itself will not be blocked, and outgoing COM calls will work normally.</span></span>

<span data-ttu-id="d2e64-217">Рекомендуется, чтобы вы могли узнать, что вы хотите обрабатывать клавишу быстрого вызова (TRUE), как и раньше.</span><span class="sxs-lookup"><span data-stu-id="d2e64-217">It is recommended to call Handle(TRUE) as early as you can know that you want to handle the accelerator key.</span></span>

```cpp
    // Register a handler for the AcceleratorKeyPressed event.
    CHECK_FAILURE(m_webView->add_AcceleratorKeyPressed(
        Callback<IWebView2AcceleratorKeyPressedEventHandler>(
            [this](IWebView2WebView* sender, IWebView2AcceleratorKeyPressedEventArgs* args)
                -> HRESULT {
                WEBVIEW2_KEY_EVENT_TYPE type;
                CHECK_FAILURE(args->get_KeyEventType(&type));
                // We only care about key down events.
                if (type == WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN ||
                    type == WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN)
                {
                    UINT key;
                    CHECK_FAILURE(args->get_VirtualKey(&key));
                    // Check if the key is one we want to handle.
                    if (std::function<void()> action =
                            m_appWindow->GetAcceleratorKeyFunction(key))
                    {
                        // Keep the browser from handling this key, whether it's autorepeated or
                        // not.
                        CHECK_FAILURE(args->Handle(TRUE));

                        // Filter out autorepeated keys.
                        WEBVIEW2_PHYSICAL_KEY_STATUS status;
                        CHECK_FAILURE(args->get_PhysicalKeyStatus(&status));
                        if (!status.WasKeyDown)
                        {
                            // Perform the action asynchronously to avoid blocking the
                            // browser process's event queue.
                            m_appWindow->RunAsync(action);
                        }
                    }
                }
                return S_OK;
            })
            .Get(),
        &m_acceleratorKeyPressedToken));
```

#### <span data-ttu-id="d2e64-218">remove_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="d2e64-218">remove_AcceleratorKeyPressed</span></span> 

<span data-ttu-id="d2e64-219">Удалите обработчик событий, добавленный ранее add_AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="d2e64-219">Remove an event handler previously added with add_AcceleratorKeyPressed.</span></span>

> <span data-ttu-id="d2e64-220">общедоступные значения HRESULT [remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="d2e64-220">public HRESULT [remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="d2e64-221">WEBVIEW2_KEY_EVENT_TYPE</span><span class="sxs-lookup"><span data-stu-id="d2e64-221">WEBVIEW2_KEY_EVENT_TYPE</span></span> 

<span data-ttu-id="d2e64-222">Тип события клавиши, которое инициировало событие AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="d2e64-222">The type of key event that triggered an AcceleratorKeyPressed event.</span></span>

> <span data-ttu-id="d2e64-223">[WEBVIEW2_KEY_EVENT_TYPE](#webview2_key_event_type) перечисления</span><span class="sxs-lookup"><span data-stu-id="d2e64-223">enum [WEBVIEW2_KEY_EVENT_TYPE](#webview2_key_event_type)</span></span>

 <span data-ttu-id="d2e64-224">Данные</span><span class="sxs-lookup"><span data-stu-id="d2e64-224">Values</span></span>                         | <span data-ttu-id="d2e64-225">Описания</span><span class="sxs-lookup"><span data-stu-id="d2e64-225">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="d2e64-226">WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN</span><span class="sxs-lookup"><span data-stu-id="d2e64-226">WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN</span></span>            | <span data-ttu-id="d2e64-227">ВыWM_KEYDOWN сообщение в окне.</span><span class="sxs-lookup"><span data-stu-id="d2e64-227">Correspond to window message WM_KEYDOWN.</span></span>
<span data-ttu-id="d2e64-228">WEBVIEW2_KEY_EVENT_TYPE_KEY_UP</span><span class="sxs-lookup"><span data-stu-id="d2e64-228">WEBVIEW2_KEY_EVENT_TYPE_KEY_UP</span></span>            | <span data-ttu-id="d2e64-229">ВыWM_KEYUP сообщение в окне.</span><span class="sxs-lookup"><span data-stu-id="d2e64-229">Correspond to window message WM_KEYUP.</span></span>
<span data-ttu-id="d2e64-230">WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN</span><span class="sxs-lookup"><span data-stu-id="d2e64-230">WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN</span></span>            | <span data-ttu-id="d2e64-231">ВыWM_SYSKEYDOWN сообщение в окне.</span><span class="sxs-lookup"><span data-stu-id="d2e64-231">Correspond to window message WM_SYSKEYDOWN.</span></span>
<span data-ttu-id="d2e64-232">WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_UP</span><span class="sxs-lookup"><span data-stu-id="d2e64-232">WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_UP</span></span>            | <span data-ttu-id="d2e64-233">ВыWM_SYSKEYUP сообщение в окне.</span><span class="sxs-lookup"><span data-stu-id="d2e64-233">Correspond to window message WM_SYSKEYUP.</span></span>

#### <span data-ttu-id="d2e64-234">WEBVIEW2_PHYSICAL_KEY_STATUS</span><span class="sxs-lookup"><span data-stu-id="d2e64-234">WEBVIEW2_PHYSICAL_KEY_STATUS</span></span> 

<span data-ttu-id="d2e64-235">Структура, представляющая данные, Упакованные в LPARAM, предоставленные событию ключа Win32.</span><span class="sxs-lookup"><span data-stu-id="d2e64-235">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

> <span data-ttu-id="d2e64-236">typedef [WEBVIEW2_PHYSICAL_KEY_STATUS](#webview2_physical_key_status)</span><span class="sxs-lookup"><span data-stu-id="d2e64-236">typedef [WEBVIEW2_PHYSICAL_KEY_STATUS](#webview2_physical_key_status)</span></span>

<span data-ttu-id="d2e64-237">Подробные сведения об WM_KEYDOWN вы увидите в документации по адресу[https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)</span><span class="sxs-lookup"><span data-stu-id="d2e64-237">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)</span></span>

