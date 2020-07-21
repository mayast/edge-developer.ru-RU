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
# 0.8.355-Interface IWebView2WebView4 

[!INCLUDE [deprecation-note](../../includes/deprecation-note.md)]

```
interface IWebView2WebView4
  : public IWebView2WebView3
```

Дополнительные функции, реализованные основным объектом WebView.

## Краткий обзор

 Участников                        | Описания
--------------------------------|---------------------------------------------
[AddRemoteObject](#addremoteobject) | Добавьте предоставленный объект узла в сценарий, выполняемый в WebView с указанным именем.
[RemoveRemoteObject](#removeremoteobject) | Удалите объект узла, заданный именем, чтобы он больше не будет доступен из кода JavaScript в WebView.
[OpenDevToolsWindow](#opendevtoolswindow) | Открытие окна DevTools для текущего документа в WebView.
[add_AcceleratorKeyPressed](#add_acceleratorkeypressed) | Добавьте обработчик событий для события AcceleratorKeyPressed.
[remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed) | Удалите обработчик событий, добавленный ранее add_AcceleratorKeyPressed.
[WEBVIEW2_KEY_EVENT_TYPE](#webview2_key_event_type) | Тип события клавиши, которое инициировало событие AcceleratorKeyPressed.
[WEBVIEW2_PHYSICAL_KEY_STATUS](#webview2_physical_key_status) | Структура, представляющая данные, Упакованные в LPARAM, предоставленные событию ключа Win32.

Вы можете QueryInterface для этого интерфейса из объекта, реализующего [IWebView2WebView](IWebView2WebView.md). Дополнительные сведения вы видите в интерфейсе [IWebView2WebView](IWebView2WebView.md) .

## Участников

#### AddRemoteObject 

Добавьте предоставленный объект узла в сценарий, выполняемый в WebView с указанным именем.

> общедоступные значения HRESULT [AddRemoteObject](#addremoteobject)(имя LPCWSTR, переменная * объект)

Объекты узла предоставляются как прокси удаленных объектов через `window.chrome.webview.remoteObjects.<name>` . Удаленные прокси-объекты являются обещанными и разрешаются в объект, представляющий объект Host. Обещание отклонено, если приложение не добавило объект с именем. Когда код JavaScript обращается к свойству или методу объекта, для него возвращается значение, которое будет обрабатываться в соответствии со значением, возвращенным из хоста для свойства или метода, или отброшено в случае ошибки, например, отсутствие такого свойства или метода для объекта или параметров недопустимым. Например, когда код приложения делает следующее: 

```cpp
VARIANT object;
object.vt = VT_DISPATCH;
object.pdispVal = appObject;
webview->AddRemoteObject(L"host_object", &host);
```

 Код JavaScript в WebView сможет получить доступ к appObject следующим образом, а затем получить доступ к атрибутам и методам appObject: 

```js
let app_object = await window.chrome.webview.remoteObjects.host_object;
let attr1 = await app_object.attr1;
let result = await app_object.method1(parameters);
```

 Обратите внимание, что хотя простые типы, IDispatch и Array поддерживаются, универсальный IUnknown, VT_DECIMAL или VT_RECORD Variant не поддерживается. Удаленные объекты JavaScript, такие как функции обратного вызова, представлены как VT_DISPATCH VARIANT с помощью объекта, реализующего IDispatch. Метод обратного вызова JavaScript можно вызвать с помощью DISPID_VALUE для DISPID. Вложенные массивы поддерживаются до 3 уровней. Массивы по типам ссылок не поддерживаются. VT_EMPTY и VT_NULL сопоставлены в JavaScript как null. В JavaScript NULL и undefine сопоставляются с VT_EMPTY.

Кроме того, все удаленные объекты представляются как `window.chrome.webview.remoteObjects.sync.<name>` . Здесь объекты узла предоставляются как синхронные удаленные прокси-объекты. Эти функции не предназначены для того, чтобы синхронно блокировать выполняемые сценарии, ожидающие общения для запуска кода хоста. Таким образом, это может привести к проблемам с надежностью, поэтому рекомендуется использовать асинхронный API на основе Promise, `window.chrome.webview.remoteObjects.<name>` описанный выше.

Синхронные удаленные прокси-объекты и асинхронные удаленные прокси-объекты могут одновременно выполнять прокси для одного и того же удаленного объекта. Удаленные изменения, внесенные одним прокси-сервером, будут отражаться в любом другом прокси того же удаленного объекта, независимо от того, являются ли они другими прокси-объектами, синхронными или асинхронными.

Несмотря на то, что JavaScript блокируется на синхронный вызов машинного кода, этот машинный код не может снова вызвать JavaScript. При попытке выполнить это действие произойдет сбой с HRESULT_FROM_WIN32 (ERROR_POSSIBLE_DEADLOCK).

Удаленные прокси-объекты — это прокси JavaScript, который перехватывает все вызовы свойств Get, Set и Method. Свойства или методы, которые являются частью прототипа функции или объекта, выполняются локально. Кроме того, любое свойство или метод в массиве `chrome.webview.remoteObjects.options.forceLocalProperties` также будет выполняться локально. Эти значения по умолчанию включают в себя дополнительные методы, которые имеют значение в JavaScript Like `toJSON` и `Symbol.toPrimitive` . При необходимости вы можете добавить в этот массив дополнительные сведения.

Существует метод `chrome.webview.remoteObjects.cleanupSome` , который лучше всего подходит для сборщиков мусора удаленных объектов.

Удаленные прокси-объекты также обладают следующими методами, которые выполняются локально.

* applyRemote,-Remote, setRemote: выполняет вызов метода, свойство get или набор свойств для удаленного объекта. Вы можете использовать их, чтобы явным образом запускать метод или свойство, если существует конфликтующий локальный метод или свойство. Например, `proxy.toString()` будет выполнен локальный метод ToString для прокси-объекта. Но `proxy.applyRemote('toString')` выполняется `toString` на удаленном прокси-объекте.

* "по локальной, setLocal" — выполнение свойства Get или установка свойства локально. Эти методы можно использовать, чтобы принудительно получить или задать свойство в самом удаленном прокси-объекте, а не на удаленном объекте, который он представляет. Например, `proxy.unknownProperty` будет получено свойство с именем `unknownProperty` из удаленного прокси-объекта. Но `proxy.getLocal('unknownProperty')` будет получить значение свойства `unknownProperty` для самого объекта прокси.

* Синхронизация: асинхронные удаленные прокси-объекты предоставляют метод синхронизации, возвращающий обещание для синхронного удаленного объектного прокси для того же удаленного объекта. Например, `chrome.webview.remoteObjects.sample.methodCall()` возвращает асинхронный удаленный прокси-объект. Вы можете использовать этот `sync` метод, чтобы получить для него синхронный удаленный прокси-объект. `const syncProxy = await chrome.webview.remoteObjects.sample.methodCall().sync()`

* Async: синхронные удаленные прокси-объекты предоставляют метод async, который блокирует и возвращает асинхронный удаленный прокси-объект для того же удаленного объекта. Например, `chrome.webview.remoteObjects.sync.sample.methodCall()` возвращает синхронный удаленный прокси-объект. При вызове `async` метода на этих блоках возвращается асинхронный удаленный прокси-объект для того же удаленного объекта: `const asyncProxy = chrome.webview.remoteObjects.sync.sample.methodCall().async()`

* затем: асинхронные удаленные прокси-объекты имеют метод then. Это позволит им доставлять ожидающие. `then` Возвращает обещание, которое разрешается с представлением удаленного объекта. Если прокси представляет литерал JavaScript, то копия, возвращаемая им, будет возвращена локально. Если прокси представляет функцию, возвращается прокси-сервер, не ожидающий ожидания. Если прокси представляет объект JavaScript с сочетанием литеральных свойств и свойств функций, то копия объекта возвращается с некоторыми свойствами в качестве удаленных прокси-объектов.

Все другие вызовы свойств и методов (Кроме описанных выше методов прокси-сервера удаленного объекта, списка forceLocalProperties и свойств прототипов функций и объектов) выполняются удаленно. Асинхронные удаленные прокси-объекты возвращают обещание, представляющее собой асинхронное завершение удаленного вызова метода или получение свойства. Обещание устраняется после завершения удаленных операций, и обещание разрешается в полученное значение операции. Синхронные удаленные прокси-объекты работают точно так же, но блокируют выполнение JavaScript и дождитесь завершения удаленной операции.

Установка свойства для прокси-сервера асинхронного удаленного объекта немного не изменилась. Функция Set возвращает значение немедленно и возвращаемое значение является значением, которое будет задано. Это требование для прокси-объекта JavaScript. Если необходимо асинхронно дождаться завершения установки свойства, используйте метод setRemote, который возвращает обещание, как описано выше. Синхронно заданное свойство свойства объекта для синхронно блокируется, пока не задано свойство.

Например, предположим, что у вас есть COM-объект со следующим интерфейсом

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

 Мы можем добавить экземпляр этого интерфейса в наш сценарий JavaScript `AddRemoteObject` . В этом случае мы присвойте ему имя `sample` :

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

 Затем в HTML-документе мы можем использовать этот COM-объект через `chrome.webview.remoteObjects.sample` :

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

#### RemoveRemoteObject 

Удалите объект узла, заданный именем, чтобы он больше не будет доступен из кода JavaScript в WebView.

> общедоступное значение HRESULT [RemoveRemoteObject](#removeremoteobject)(имя LPCWSTR)

Несмотря на то что новые попытки доступа будут отвергнуты, если объект уже получен кодом JavaScript в WebView, код JavaScript продолжит получать доступ к этому объекту. Вызов этого метода для имени, которое уже удалено или не было добавлено, завершается сбоем.

#### OpenDevToolsWindow 

Открытие окна DevTools для текущего документа в WebView.

> общедоступные значения HRESULT [OpenDevToolsWindow](#opendevtoolswindow)()

Ничего не происходит, если он вызывается, когда окно DevTools уже открыто

#### add_AcceleratorKeyPressed 

Добавьте обработчик событий для события AcceleratorKeyPressed.

> общедоступные значения HRESULT [add_AcceleratorKeyPressed](#add_acceleratorkeypressed)([IWebView2AcceleratorKeyPressedEventHandler](IWebView2AcceleratorKeyPressedEventHandler.md) * eventHandler, EventRegistrationToken * token)

AcceleratorKeyPressed активируется при нажатии или отпускании клавиши сочетания клавиш в том случае, если WebView имеет фокус. Клавиша считается ускорителем по одной из следующих способов:

1. В данный момент удерживается клавиша CTRL или ALT;

1. Нажатая клавиша не сопоставляется с символом. Некоторые неопределенные клавиши никогда не рассматриваются как ускорители, например Shift. Клавиша ESC всегда считается ускорителем.

Событие с автоматическим нажатием клавиши, вызванное удерживанием нажатой клавиши, также срабатывает. Чтобы отфильтровать эти данные, Проверьте аргументы события "KeyEventLParam" или "PhysicalKeyStatus".

В оконном режиме этот обработчик событий вызывается синхронно. До тех пор пока вы не вызываете Handle () для аргументов события или не будет возвращен обработчик событий, процесс браузера будет заблокирован и исходящие межпроцессные вызовы COM не будут работать с RPC_E_CANTCALLOUT_ININPUTSYNCCALL. Однако все методы API WebView2 будут работать.

В режиме безоконный обработчик событий вызывается асинхронно. Дальнейшие входные данные не доходят до браузера, пока обработчик событий не возвратит или не завершит вызов (), но сам процесс браузера не будет заблокирован, а исходящие вызовы COM будут работать нормально.

Рекомендуется, чтобы вы могли узнать, что вы хотите обрабатывать клавишу быстрого вызова (TRUE), как и раньше.

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

#### remove_AcceleratorKeyPressed 

Удалите обработчик событий, добавленный ранее add_AcceleratorKeyPressed.

> общедоступные значения HRESULT [remove_AcceleratorKeyPressed](#remove_acceleratorkeypressed)(маркер EventRegistrationToken)

#### WEBVIEW2_KEY_EVENT_TYPE 

Тип события клавиши, которое инициировало событие AcceleratorKeyPressed.

> [WEBVIEW2_KEY_EVENT_TYPE](#webview2_key_event_type) перечисления

 Данные                         | Описания
--------------------------------|---------------------------------------------
WEBVIEW2_KEY_EVENT_TYPE_KEY_DOWN            | ВыWM_KEYDOWN сообщение в окне.
WEBVIEW2_KEY_EVENT_TYPE_KEY_UP            | ВыWM_KEYUP сообщение в окне.
WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_DOWN            | ВыWM_SYSKEYDOWN сообщение в окне.
WEBVIEW2_KEY_EVENT_TYPE_SYSTEM_KEY_UP            | ВыWM_SYSKEYUP сообщение в окне.

#### WEBVIEW2_PHYSICAL_KEY_STATUS 

Структура, представляющая данные, Упакованные в LPARAM, предоставленные событию ключа Win32.

> typedef [WEBVIEW2_PHYSICAL_KEY_STATUS](#webview2_physical_key_status)

Подробные сведения об WM_KEYDOWN вы увидите в документации по адресу[https://docs.microsoft.com/windows/win32/inputdev/wm-keydown](https://docs.microsoft.com/windows/win32/inputdev/wm-keydown)

