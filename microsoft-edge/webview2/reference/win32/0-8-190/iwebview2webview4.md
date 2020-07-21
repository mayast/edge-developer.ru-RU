---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView2
title: 0.8.355-WebView2 Win32 C++ IWebView2WebView4
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/20/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE
ms.openlocfilehash: 4e3fdc6283103833526f3c23e12796c78de77261
ms.sourcegitcommit: e0cb9e6f59f222fade6afa4829c59524a9a9b9ff
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/20/2020
ms.locfileid: "10884706"
---
# <span data-ttu-id="eb8f5-104">0.8.355-Interface IWebView2WebView4</span><span class="sxs-lookup"><span data-stu-id="eb8f5-104">0.8.355 - interface IWebView2WebView4</span></span> 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebView4
  : public IWebView2WebView3
```

<span data-ttu-id="eb8f5-105">Дополнительные функции, реализованные основным объектом WebView.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-105">Additional functionality implemented by the primary WebView object.</span></span>

## <span data-ttu-id="eb8f5-106">Краткий обзор</span><span class="sxs-lookup"><span data-stu-id="eb8f5-106">Summary</span></span>

 <span data-ttu-id="eb8f5-107">Участников</span><span class="sxs-lookup"><span data-stu-id="eb8f5-107">Members</span></span>                        | <span data-ttu-id="eb8f5-108">Описания</span><span class="sxs-lookup"><span data-stu-id="eb8f5-108">Descriptions</span></span>
--------------------------------|---------------------------------------------
[<span data-ttu-id="eb8f5-109">AddRemoteObject</span><span class="sxs-lookup"><span data-stu-id="eb8f5-109">AddRemoteObject</span></span>](#addremoteobject) | <span data-ttu-id="eb8f5-110">Добавьте предоставленный объект узла в сценарий, выполняемый в WebView с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-110">Add the provided host object to script running in the WebView with the specified name.</span></span>
[<span data-ttu-id="eb8f5-111">RemoveRemoteObject</span><span class="sxs-lookup"><span data-stu-id="eb8f5-111">RemoveRemoteObject</span></span>](#removeremoteobject) | <span data-ttu-id="eb8f5-112">Удалите объект узла, заданный именем, чтобы он больше не будет доступен из кода JavaScript в WebView.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-112">Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the WebView.</span></span>
[<span data-ttu-id="eb8f5-113">OpenDevToolsWindow</span><span class="sxs-lookup"><span data-stu-id="eb8f5-113">OpenDevToolsWindow</span></span>](#opendevtoolswindow) | <span data-ttu-id="eb8f5-114">Открытие окна DevTools для текущего документа в WebView.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-114">Opens the DevTools window for the current document in the WebView.</span></span>
[<span data-ttu-id="eb8f5-115">add_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="eb8f5-115">add_AcceleratorKeyPressed</span></span>](#add_acceleratorkeypressed) | <span data-ttu-id="eb8f5-116">Добавьте обработчик событий для события AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-116">Add an event handler for the AcceleratorKeyPressed event.</span></span>
[<span data-ttu-id="eb8f5-117">remove_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="eb8f5-117">remove_AcceleratorKeyPressed</span></span>](#remove_acceleratorkeypressed) | <span data-ttu-id="eb8f5-118">Удалите обработчик событий, добавленный ранее add_AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-118">Remove an event handler previously added with add_AcceleratorKeyPressed.</span></span>
[<span data-ttu-id="eb8f5-119">WEBVIEW2_KEY_EVENT_TYPE</span><span class="sxs-lookup"><span data-stu-id="eb8f5-119">WEBVIEW2_KEY_EVENT_TYPE</span></span>](#webview2_key_event_type) | <span data-ttu-id="eb8f5-120">Тип события клавиши, которое инициировало событие AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-120">The type of key event that triggered an AcceleratorKeyPressed event.</span></span>
[<span data-ttu-id="eb8f5-121">WEBVIEW2_PHYSICAL_KEY_STATUS</span><span class="sxs-lookup"><span data-stu-id="eb8f5-121">WEBVIEW2_PHYSICAL_KEY_STATUS</span></span>](#webview2_physical_key_status) | <span data-ttu-id="eb8f5-122">Структура, представляющая данные, Упакованные в LPARAM, предоставленные событию ключа Win32.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-122">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

<span data-ttu-id="eb8f5-123">Вы можете QueryInterface для этого интерфейса из объекта, реализующего [IWebView2WebView](IWebView2WebView.md).</span><span class="sxs-lookup"><span data-stu-id="eb8f5-123">You can QueryInterface for this interface from the object that implements [IWebView2WebView](IWebView2WebView.md).</span></span> <span data-ttu-id="eb8f5-124">Дополнительные сведения вы видите в интерфейсе [IWebView2WebView](IWebView2WebView.md) .</span><span class="sxs-lookup"><span data-stu-id="eb8f5-124">See the [IWebView2WebView](IWebView2WebView.md) interface for more details.</span></span>

## <span data-ttu-id="eb8f5-125">Участников</span><span class="sxs-lookup"><span data-stu-id="eb8f5-125">Members</span></span>

#### <span data-ttu-id="eb8f5-126">AddRemoteObject</span><span class="sxs-lookup"><span data-stu-id="eb8f5-126">AddRemoteObject</span></span> 

<span data-ttu-id="eb8f5-127">Добавьте предоставленный объект узла в сценарий, выполняемый в WebView с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-127">Add the provided host object to script running in the WebView with the specified name.</span></span>

> <span data-ttu-id="eb8f5-128">общедоступные значения HRESULT [AddRemoteObject](#addremoteobject)(имя LPCWSTR, переменная \* объект)</span><span class="sxs-lookup"><span data-stu-id="eb8f5-128">public HRESULT [AddRemoteObject](#addremoteobject)(LPCWSTR name,VARIANT \* object)</span></span>

<span data-ttu-id="eb8f5-129">Объекты узла предоставляются как прокси удаленных объектов через `window.chrome.webview.remoteObjects.<name>` .</span><span class="sxs-lookup"><span data-stu-id="eb8f5-129">Host objects are exposed as remote object proxies via `window.chrome.webview.remoteObjects.<name>`.</span></span> <span data-ttu-id="eb8f5-130">Удаленные прокси-объекты являются обещанными и разрешаются в объект, представляющий объект Host.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-130">Remote object proxies are promises and will resolve to an object representing the host object.</span></span> <span data-ttu-id="eb8f5-131">Обещание отклонено, если приложение не добавило объект с именем.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-131">The promise is rejected if the app has not added an object with the name.</span></span> <span data-ttu-id="eb8f5-132">Когда код JavaScript обращается к свойству или методу объекта, для него возвращается значение, которое будет обрабатываться в соответствии со значением, возвращенным из хоста для свойства или метода, или отброшено в случае ошибки, например, отсутствие такого свойства или метода для объекта или параметров недопустимым.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-132">When JavaScript code access a property or method of the object, a promise is return, which will resolve to the value returned from the host for the property or method, or rejected in case of error such as there is no such property or method on the object or parameters are invalid.</span></span> <span data-ttu-id="eb8f5-133">Например, когда код приложения делает следующее:</span><span class="sxs-lookup"><span data-stu-id="eb8f5-133">For example, when the application code does the following:</span></span> 

```cpp
VARIANT object;
object.vt = VT_DISPATCH;
object.pdispVal = appObject;
webview->AddRemoteObject(L"host_object", &host);
```

 <span data-ttu-id="eb8f5-134">Код JavaScript в WebView сможет получить доступ к appObject следующим образом, а затем получить доступ к атрибутам и методам appObject:</span><span class="sxs-lookup"><span data-stu-id="eb8f5-134">JavaScript code in the WebView will be able to access appObject as following and then access attributes and methods of appObject:</span></span> 

```js
let app_object = await window.chrome.webview.remoteObjects.host_object;
let attr1 = await app_object.attr1;
let result = await app_object.method1(parameters);
```

 <span data-ttu-id="eb8f5-135">Обратите внимание, что хотя простые типы, IDispatch и Array поддерживаются, универсальный IUnknown, VT_DECIMAL или VT_RECORD Variant не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-135">Note that while simple types, IDispatch and array are supported, generic IUnknown, VT_DECIMAL, or VT_RECORD variant is not supported.</span></span> <span data-ttu-id="eb8f5-136">Удаленные объекты JavaScript, такие как функции обратного вызова, представлены как VT_DISPATCH VARIANT с помощью объекта, реализующего IDispatch.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-136">Remote JavaScript objects like callback functions are represented as an VT_DISPATCH VARIANT with the object implementing IDispatch.</span></span> <span data-ttu-id="eb8f5-137">Метод обратного вызова JavaScript можно вызвать с помощью DISPID_VALUE для DISPID.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-137">The JavaScript callback method may be invoked using DISPID_VALUE for the DISPID.</span></span> <span data-ttu-id="eb8f5-138">Вложенные массивы поддерживаются до 3 уровней.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-138">Nested arrays are supported up to a depth of 3.</span></span> <span data-ttu-id="eb8f5-139">Массивы по типам ссылок не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-139">Arrays of by reference types are not supported.</span></span> <span data-ttu-id="eb8f5-140">VT_EMPTY и VT_NULL сопоставлены в JavaScript как null.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-140">VT_EMPTY and VT_NULL are mapped into JavaScript as null.</span></span> <span data-ttu-id="eb8f5-141">В JavaScript NULL и undefine сопоставляются с VT_EMPTY.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-141">In JavaScript null and undefined are mapped to VT_EMPTY.</span></span>

<span data-ttu-id="eb8f5-142">Кроме того, все удаленные объекты представляются как `window.chrome.webview.remoteObjects.sync.<name>` .</span><span class="sxs-lookup"><span data-stu-id="eb8f5-142">Additionally, all remote objects are exposed as `window.chrome.webview.remoteObjects.sync.<name>`.</span></span> <span data-ttu-id="eb8f5-143">Здесь объекты узла предоставляются как синхронные удаленные прокси-объекты.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-143">Here the host objects are exposed as synchronous remote object proxies.</span></span> <span data-ttu-id="eb8f5-144">Эти функции не предназначены для того, чтобы синхронно блокировать выполняемые сценарии, ожидающие общения для запуска кода хоста.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-144">These are not promises and calls to functions or property access synchronously block running script waiting to communicate cross process for the host code to run.</span></span> <span data-ttu-id="eb8f5-145">Таким образом, это может привести к проблемам с надежностью, поэтому рекомендуется использовать асинхронный API на основе Promise, `window.chrome.webview.remoteObjects.<name>` описанный выше.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-145">Accordingly this can result in reliability issues and it is recommended that you use the promise based asynchronous `window.chrome.webview.remoteObjects.<name>` API described above.</span></span>

<span data-ttu-id="eb8f5-146">Синхронные удаленные прокси-объекты и асинхронные удаленные прокси-объекты могут одновременно выполнять прокси для одного и того же удаленного объекта.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-146">Synchronous remote object proxies and asynchronous remote object proxies can both proxy the same remote object.</span></span> <span data-ttu-id="eb8f5-147">Удаленные изменения, внесенные одним прокси-сервером, будут отражаться в любом другом прокси того же удаленного объекта, независимо от того, являются ли они другими прокси-объектами, синхронными или асинхронными.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-147">Remote changes made by one proxy will be reflected in any other proxy of that same remote object whether the other proxies and synchronous or asynchronous.</span></span>

<span data-ttu-id="eb8f5-148">Несмотря на то, что JavaScript блокируется на синхронный вызов машинного кода, этот машинный код не может снова вызвать JavaScript.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-148">While JavaScript is blocked on a synchronous call to native code, that native code is unable to call back to JavaScript.</span></span> <span data-ttu-id="eb8f5-149">При попытке выполнить это действие произойдет сбой с HRESULT_FROM_WIN32 (ERROR_POSSIBLE_DEADLOCK).</span><span class="sxs-lookup"><span data-stu-id="eb8f5-149">Attempts to do so will fail with HRESULT_FROM_WIN32(ERROR_POSSIBLE_DEADLOCK).</span></span>

<span data-ttu-id="eb8f5-150">Удаленные прокси-объекты — это прокси JavaScript, который перехватывает все вызовы свойств Get, Set и Method.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-150">Remote object proxies are JavaScript Proxy objects that intercept all property get, property set, and method invocations.</span></span> <span data-ttu-id="eb8f5-151">Свойства или методы, которые являются частью прототипа функции или объекта, выполняются локально.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-151">Properties or methods that are a part of the Function or Object prototype are run locally.</span></span> <span data-ttu-id="eb8f5-152">Кроме того, любое свойство или метод в массиве `chrome.webview.remoteObjects.options.forceLocalProperties` также будет выполняться локально.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-152">Additionally any property or method in the array `chrome.webview.remoteObjects.options.forceLocalProperties` will also be run locally.</span></span> <span data-ttu-id="eb8f5-153">Эти значения по умолчанию включают в себя дополнительные методы, которые имеют значение в JavaScript Like `toJSON` и `Symbol.toPrimitive` .</span><span class="sxs-lookup"><span data-stu-id="eb8f5-153">This defaults to including optional methods that have meaning in JavaScript like `toJSON` and `Symbol.toPrimitive`.</span></span> <span data-ttu-id="eb8f5-154">При необходимости вы можете добавить в этот массив дополнительные сведения.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-154">You can add more to this array as required.</span></span>

<span data-ttu-id="eb8f5-155">Существует метод `chrome.webview.remoteObjects.cleanupSome` , который лучше всего подходит для сборщиков мусора удаленных объектов.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-155">There's a method `chrome.webview.remoteObjects.cleanupSome` that will best effort garbage collect remote object proxies.</span></span>

<span data-ttu-id="eb8f5-156">Удаленные прокси-объекты также обладают следующими методами, которые выполняются локально.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-156">Remote object proxies additionally have the following methods which run locally:</span></span>

* <span data-ttu-id="eb8f5-157">applyRemote,-Remote, setRemote: выполняет вызов метода, свойство get или набор свойств для удаленного объекта.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-157">applyRemote, getRemote, setRemote: Perform a method invocation, property get, or property set on the remote object.</span></span> <span data-ttu-id="eb8f5-158">Вы можете использовать их, чтобы явным образом запускать метод или свойство, если существует конфликтующий локальный метод или свойство.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-158">You can use these to explicitly force a method or property to run remotely if there is a conflicting local method or property.</span></span> <span data-ttu-id="eb8f5-159">Например, `proxy.toString()` будет выполнен локальный метод ToString для прокси-объекта.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-159">For instance, `proxy.toString()` will run the local toString method on the proxy object.</span></span> <span data-ttu-id="eb8f5-160">Но `proxy.applyRemote('toString')` выполняется `toString` на удаленном прокси-объекте.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-160">But `proxy.applyRemote('toString')` runs `toString` on the remote proxied object instead.</span></span>

* <span data-ttu-id="eb8f5-161">"по локальной, setLocal" — выполнение свойства Get или установка свойства локально.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-161">getLocal, setLocal: Perform property get, or property set locally.</span></span> <span data-ttu-id="eb8f5-162">Эти методы можно использовать, чтобы принудительно получить или задать свойство в самом удаленном прокси-объекте, а не на удаленном объекте, который он представляет.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-162">You can use these methods to force getting or setting a property on the remote object proxy itself rather than on the remote object it represents.</span></span> <span data-ttu-id="eb8f5-163">Например, `proxy.unknownProperty` будет получено свойство с именем `unknownProperty` из удаленного прокси-объекта.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-163">For instance, `proxy.unknownProperty` will get the property named `unknownProperty` from the remote proxied object.</span></span> <span data-ttu-id="eb8f5-164">Но `proxy.getLocal('unknownProperty')` будет получить значение свойства `unknownProperty` для самого объекта прокси.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-164">But `proxy.getLocal('unknownProperty')` will get the value of the property `unknownProperty` on the proxy object itself.</span></span>

* <span data-ttu-id="eb8f5-165">Синхронизация: асинхронные удаленные прокси-объекты предоставляют метод синхронизации, возвращающий обещание для синхронного удаленного объектного прокси для того же удаленного объекта.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-165">sync: Asynchronous remote object proxies expose a sync method which returns a promise for a synchronous remote object proxy for the same remote object.</span></span> <span data-ttu-id="eb8f5-166">Например, `chrome.webview.remoteObjects.sample.methodCall()` возвращает асинхронный удаленный прокси-объект.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-166">For example, `chrome.webview.remoteObjects.sample.methodCall()` returns an asynchronous remote object proxy.</span></span> <span data-ttu-id="eb8f5-167">Вы можете использовать этот `sync` метод, чтобы получить для него синхронный удаленный прокси-объект.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-167">You can use the `sync` method to obtain a synchronous remote object proxy instead:</span></span> `const syncProxy = await chrome.webview.remoteObjects.sample.methodCall().sync()`

* <span data-ttu-id="eb8f5-168">Async: синхронные удаленные прокси-объекты предоставляют метод async, который блокирует и возвращает асинхронный удаленный прокси-объект для того же удаленного объекта.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-168">async: Synchronous remote object proxies expose an async method which blocks and returns an asynchronous remote object proxy for the same remote object.</span></span> <span data-ttu-id="eb8f5-169">Например, `chrome.webview.remoteObjects.sync.sample.methodCall()` возвращает синхронный удаленный прокси-объект.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-169">For example, `chrome.webview.remoteObjects.sync.sample.methodCall()` returns a synchronous remote object proxy.</span></span> <span data-ttu-id="eb8f5-170">При вызове `async` метода на этих блоках возвращается асинхронный удаленный прокси-объект для того же удаленного объекта:</span><span class="sxs-lookup"><span data-stu-id="eb8f5-170">Calling the `async` method on this blocks and then returns an asynchronous remote object proxy for the same remote object:</span></span> `const asyncProxy = chrome.webview.remoteObjects.sync.sample.methodCall().async()`

* <span data-ttu-id="eb8f5-171">затем: асинхронные удаленные прокси-объекты имеют метод then.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-171">then: Asynchronous remote object proxies have a then method.</span></span> <span data-ttu-id="eb8f5-172">Это позволит им доставлять ожидающие.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-172">This allows them to be awaitable.</span></span> `then` <span data-ttu-id="eb8f5-173">Возвращает обещание, которое разрешается с представлением удаленного объекта.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-173">will return a promise that resolves with a representation of the remote object.</span></span> <span data-ttu-id="eb8f5-174">Если прокси представляет литерал JavaScript, то копия, возвращаемая им, будет возвращена локально.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-174">If the proxy represents a JavaScript literal then a copy of that is returned locally.</span></span> <span data-ttu-id="eb8f5-175">Если прокси представляет функцию, возвращается прокси-сервер, не ожидающий ожидания.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-175">If the proxy represents a function then a non-awaitable proxy is returned.</span></span> <span data-ttu-id="eb8f5-176">Если прокси представляет объект JavaScript с сочетанием литеральных свойств и свойств функций, то копия объекта возвращается с некоторыми свойствами в качестве удаленных прокси-объектов.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-176">If the proxy represents a JavaScript object with a mix of literal properties and function properties, then the a copy of the object is returned with some properties as remote object proxies.</span></span>

<span data-ttu-id="eb8f5-177">Все другие вызовы свойств и методов (Кроме описанных выше методов прокси-сервера удаленного объекта, списка forceLocalProperties и свойств прототипов функций и объектов) выполняются удаленно.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-177">All other property and method invocations (other than the above Remote object proxy methods, forceLocalProperties list, and properties on Function and Object prototypes) are run remotely.</span></span> <span data-ttu-id="eb8f5-178">Асинхронные удаленные прокси-объекты возвращают обещание, представляющее собой асинхронное завершение удаленного вызова метода или получение свойства.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-178">Asynchronous remote object proxies return a promise representing asynchronous completion of remotely invoking the method, or getting the property.</span></span> <span data-ttu-id="eb8f5-179">Обещание устраняется после завершения удаленных операций, и обещание разрешается в полученное значение операции.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-179">The promise resolves after the remote operations complete and the promises resolve to the resulting value of the operation.</span></span> <span data-ttu-id="eb8f5-180">Синхронные удаленные прокси-объекты работают точно так же, но блокируют выполнение JavaScript и дождитесь завершения удаленной операции.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-180">Synchronous remote object proxies work similarly but block JavaScript execution and wait for the remote operation to complete.</span></span>

<span data-ttu-id="eb8f5-181">Установка свойства для прокси-сервера асинхронного удаленного объекта немного не изменилась.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-181">Setting a property on an asynchronous remote object proxy works slightly differently.</span></span> <span data-ttu-id="eb8f5-182">Функция Set возвращает значение немедленно и возвращаемое значение является значением, которое будет задано.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-182">The set returns immediately and the return value is the value that will be set.</span></span> <span data-ttu-id="eb8f5-183">Это требование для прокси-объекта JavaScript.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-183">This is a requirement of the JavaScript Proxy object.</span></span> <span data-ttu-id="eb8f5-184">Если необходимо асинхронно дождаться завершения установки свойства, используйте метод setRemote, который возвращает обещание, как описано выше.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-184">If you need to asynchronously wait for the property set to complete, use the setRemote method which returns a promise as described above.</span></span> <span data-ttu-id="eb8f5-185">Синхронно заданное свойство свойства объекта для синхронно блокируется, пока не задано свойство.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-185">Synchronous object property set property synchronously blocks until the property is set.</span></span>

<span data-ttu-id="eb8f5-186">Например, предположим, что у вас есть COM-объект со следующим интерфейсом</span><span class="sxs-lookup"><span data-stu-id="eb8f5-186">For example, suppose you have a COM object with the following interface</span></span>

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

 <span data-ttu-id="eb8f5-187">Мы можем добавить экземпляр этого интерфейса в наш сценарий JavaScript `AddRemoteObject` .</span><span class="sxs-lookup"><span data-stu-id="eb8f5-187">We can add an instance of this interface into our JavaScript with `AddRemoteObject`.</span></span> <span data-ttu-id="eb8f5-188">В этом случае мы присвойте ему имя `sample` :</span><span class="sxs-lookup"><span data-stu-id="eb8f5-188">In this case we name it `sample`:</span></span>

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

 <span data-ttu-id="eb8f5-189">Затем в HTML-документе мы можем использовать этот COM-объект через `chrome.webview.remoteObjects.sample` :</span><span class="sxs-lookup"><span data-stu-id="eb8f5-189">Then in the HTML document we can use this COM object via `chrome.webview.remoteObjects.sample`:</span></span>

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

#### <span data-ttu-id="eb8f5-190">RemoveRemoteObject</span><span class="sxs-lookup"><span data-stu-id="eb8f5-190">RemoveRemoteObject</span></span> 

<span data-ttu-id="eb8f5-191">Удалите объект узла, заданный именем, чтобы он больше не будет доступен из кода JavaScript в WebView.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-191">Remove the host object specified by the name so that it is no longer accessible from JavaScript code in the WebView.</span></span>

> <span data-ttu-id="eb8f5-192">общедоступное значение HRESULT [RemoveRemoteObject](#removeremoteobject)(имя LPCWSTR)</span><span class="sxs-lookup"><span data-stu-id="eb8f5-192">public HRESULT [RemoveRemoteObject](#removeremoteobject)(LPCWSTR name)</span></span>

<span data-ttu-id="eb8f5-193">Несмотря на то что новые попытки доступа будут отвергнуты, если объект уже получен кодом JavaScript в WebView, код JavaScript продолжит получать доступ к этому объекту.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-193">While new access attempts will be denied, if the object is already obtained by JavaScript code in the WebView, the JavaScript code will continue to have access to that object.</span></span> <span data-ttu-id="eb8f5-194">Вызов этого метода для имени, которое уже удалено или не было добавлено, завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-194">Calling this method for a name that is already removed or never added will fail.</span></span>

#### <span data-ttu-id="eb8f5-195">OpenDevToolsWindow</span><span class="sxs-lookup"><span data-stu-id="eb8f5-195">OpenDevToolsWindow</span></span> 

<span data-ttu-id="eb8f5-196">Открытие окна DevTools для текущего документа в WebView.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-196">Opens the DevTools window for the current document in the WebView.</span></span>

> <span data-ttu-id="eb8f5-197">общедоступные значения HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()</span><span class="sxs-lookup"><span data-stu-id="eb8f5-197">public HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()</span></span>

<span data-ttu-id="eb8f5-198">Ничего не происходит, если он вызывается, когда окно DevTools уже открыто</span><span class="sxs-lookup"><span data-stu-id="eb8f5-198">Does nothing if called when the DevTools window is already open</span></span>

#### <span data-ttu-id="eb8f5-199">add_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="eb8f5-199">add_AcceleratorKeyPressed</span></span> 

<span data-ttu-id="eb8f5-200">Добавьте обработчик событий для события AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-200">Add an event handler for the AcceleratorKeyPressed event.</span></span>

> <span data-ttu-id="eb8f5-201">общедоступные значения HRESULT [add_AcceleratorKeyPressed](#add_acceleratorkeypressed)([IWebView2AcceleratorKeyPressedEventHandler](IWebView2AcceleratorKeyPressedEventHandler.md) \* eventHandler, EventRegistrationToken \* token)</span><span class="sxs-lookup"><span data-stu-id="eb8f5-201">public HRESULT [add_AcceleratorKeyPressed](#add_acceleratorkeypressed)([IWebView2AcceleratorKeyPressedEventHandler](IWebView2AcceleratorKeyPressedEventHandler.md) \* eventHandler,EventRegistrationToken \* token)</span></span>

<span data-ttu-id="eb8f5-202">AcceleratorKeyPressed активируется при нажатии или отпускании клавиши сочетания клавиш в том случае, если WebView имеет фокус.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-202">AcceleratorKeyPressed fires when an accelerator key or key combo is pressed or released while the WebView is focused.</span></span> <span data-ttu-id="eb8f5-203">Клавиша считается ускорителем по одной из следующих способов:</span><span class="sxs-lookup"><span data-stu-id="eb8f5-203">A key is considered an accelerator if either:</span></span>

1. <span data-ttu-id="eb8f5-204">В данный момент удерживается клавиша CTRL или ALT;</span><span class="sxs-lookup"><span data-stu-id="eb8f5-204">Ctrl or Alt is currently being held, or</span></span>

1. <span data-ttu-id="eb8f5-205">Нажатая клавиша не сопоставляется с символом.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-205">the pressed key does not map to a character.</span></span> <span data-ttu-id="eb8f5-206">Некоторые неопределенные клавиши никогда не рассматриваются как ускорители, например Shift.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-206">A few specific keys are never considered accelerators, such as Shift.</span></span> <span data-ttu-id="eb8f5-207">Клавиша ESC всегда считается ускорителем.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-207">The Escape key is always considered an accelerator.</span></span>

<span data-ttu-id="eb8f5-208">Событие с автоматическим нажатием клавиши, вызванное удерживанием нажатой клавиши, также срабатывает.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-208">Autorepeated key events caused by holding the key down will also fire this event.</span></span> <span data-ttu-id="eb8f5-209">Чтобы отфильтровать эти данные, Проверьте аргументы события "KeyEventLParam" или "PhysicalKeyStatus".</span><span class="sxs-lookup"><span data-stu-id="eb8f5-209">You can filter these out by checking the event args' KeyEventLParam or PhysicalKeyStatus.</span></span>

<span data-ttu-id="eb8f5-210">В оконном режиме этот обработчик событий вызывается синхронно.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-210">In windowed mode, this event handler is called synchronously.</span></span> <span data-ttu-id="eb8f5-211">До тех пор пока вы не вызываете Handle () для аргументов события или не будет возвращен обработчик событий, процесс браузера будет заблокирован и исходящие межпроцессные вызовы COM не будут работать с RPC_E_CANTCALLOUT_ININPUTSYNCCALL.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-211">Until you call Handle() on the event args or the event handler returns, the browser process will be blocked and outgoing cross-process COM calls will fail with RPC_E_CANTCALLOUT_ININPUTSYNCCALL.</span></span> <span data-ttu-id="eb8f5-212">Однако все методы API WebView2 будут работать.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-212">All WebView2 API methods will work, however.</span></span>

<span data-ttu-id="eb8f5-213">В режиме безоконный обработчик событий вызывается асинхронно.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-213">In windowless mode, the event handler is called asynchronously.</span></span> <span data-ttu-id="eb8f5-214">Дальнейшие входные данные не доходят до браузера, пока обработчик событий не возвратит или не завершит вызов (), но сам процесс браузера не будет заблокирован, а исходящие вызовы COM будут работать нормально.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-214">Further input will not reach the browser until the event handler returns or Handle() is called, but the browser process itself will not be blocked, and outgoing COM calls will work normally.</span></span>

<span data-ttu-id="eb8f5-215">Рекомендуется, чтобы вы могли узнать, что вы хотите обрабатывать клавишу быстрого вызова (TRUE), как и раньше.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-215">It is recommended to call Handle(TRUE) as early as you can know that you want to handle the accelerator key.</span></span>

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

#### <span data-ttu-id="eb8f5-216">remove_AcceleratorKeyPressed</span><span class="sxs-lookup"><span data-stu-id="eb8f5-216">remove_AcceleratorKeyPressed</span></span> 

<span data-ttu-id="eb8f5-217">Удалите обработчик событий, добавленный ранее add_AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-217">Remove an event handler previously added with add_AcceleratorKeyPressed.</span></span>

> <span data-ttu-id="eb8f5-218">общедоступные значения HRESULT [remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed)(маркер EventRegistrationToken)</span><span class="sxs-lookup"><span data-stu-id="eb8f5-218">public HRESULT [remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed)(EventRegistrationToken token)</span></span>

#### <span data-ttu-id="eb8f5-219">WEBVIEW2_KEY_EVENT_TYPE</span><span class="sxs-lookup"><span data-stu-id="eb8f5-219">WEBVIEW2_KEY_EVENT_TYPE</span></span> 

<span data-ttu-id="eb8f5-220">Тип события клавиши, которое инициировало событие AcceleratorKeyPressed.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-220">The type of key event that triggered an AcceleratorKeyPressed event.</span></span>

> <span data-ttu-id="eb8f5-221">[WEBVIEW2_KEY_EVENT_TYPE](#webview2_key_event_type) перечисления</span><span class="sxs-lookup"><span data-stu-id="eb8f5-221">enum [WEBVIEW2_KEY_EVENT_TYPE](#webview2_key_event_type)</span></span>

 <span data-ttu-id="eb8f5-222">Данные</span><span class="sxs-lookup"><span data-stu-id="eb8f5-222">Values</span></span>                         | <span data-ttu-id="eb8f5-223">Описания</span><span class="sxs-lookup"><span data-stu-id="eb8f5-223">Descriptions</span></span>
--------------------------------|---------------------------------------------
<span data-ttu-id="eb8f5-224">WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN</span><span class="sxs-lookup"><span data-stu-id="eb8f5-224">WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN</span></span>            | <span data-ttu-id="eb8f5-225">ВыWM_KEYDOWN сообщение в окне.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-225">Correspond to window message WM_KEYDOWN.</span></span>
<span data-ttu-id="eb8f5-226">WEBVIEW2_KEY_EVENT_TYPE_KEY_UP</span><span class="sxs-lookup"><span data-stu-id="eb8f5-226">WEBVIEW2_KEY_EVENT_TYPE_KEY_UP</span></span>            | <span data-ttu-id="eb8f5-227">ВыWM_KEYUP сообщение в окне.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-227">Correspond to window message WM_KEYUP.</span></span>
<span data-ttu-id="eb8f5-228">WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN</span><span class="sxs-lookup"><span data-stu-id="eb8f5-228">WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN</span></span>            | <span data-ttu-id="eb8f5-229">ВыWM_SYSKEYDOWN сообщение в окне.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-229">Correspond to window message WM_SYSKEYDOWN.</span></span>
<span data-ttu-id="eb8f5-230">WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_UP</span><span class="sxs-lookup"><span data-stu-id="eb8f5-230">WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_UP</span></span>            | <span data-ttu-id="eb8f5-231">ВыWM_SYSKEYUP сообщение в окне.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-231">Correspond to window message WM_SYSKEYUP.</span></span>

#### <span data-ttu-id="eb8f5-232">WEBVIEW2_PHYSICAL_KEY_STATUS</span><span class="sxs-lookup"><span data-stu-id="eb8f5-232">WEBVIEW2_PHYSICAL_KEY_STATUS</span></span> 

<span data-ttu-id="eb8f5-233">Структура, представляющая данные, Упакованные в LPARAM, предоставленные событию ключа Win32.</span><span class="sxs-lookup"><span data-stu-id="eb8f5-233">A structure representing the information packed into the LPARAM given to a Win32 key event.</span></span>

> <span data-ttu-id="eb8f5-234">typedef [WEBVIEW2_PHYSICAL_KEY_STATUS](#webview2_physical_key_status)</span><span class="sxs-lookup"><span data-stu-id="eb8f5-234">typedef [WEBVIEW2_PHYSICAL_KEY_STATUS](#webview2_physical_key_status)</span></span>

<span data-ttu-id="eb8f5-235">Подробные сведения об WM_KEYDOWN вы увидите в документации по адресу[https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)</span><span class="sxs-lookup"><span data-stu-id="eb8f5-235">See the documentation for WM_KEYDOWN for details at [https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)</span></span>

