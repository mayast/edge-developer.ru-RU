---
description: Ознакомьтесь со сведениями о текущих и будущих API, а также известных проблемах и несовместимости с Хромами.
title: API-интерфейсы, поддерживаемые расширениями
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/18/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: EDGE, веб-разработка, HTML, CSS, JavaScript, разработчик
ms.openlocfilehash: fceba67f5fab1a223cfc94abf7f19a0a9d1bcdf0
ms.sourcegitcommit: 0879b205aa88c6b73d84f106b4b435d5a0e8cadc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/18/2020
ms.locfileid: "10937184"
---
# Поддерживаемые API  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Ниже приведен подробный список поддерживаемых членов API. Разработка платформы расширения выполняется, поэтому регулярно проверяйте ее на наличие обновлений.

> [!NOTE]
>  - В Microsoft Edge все API расширений находятся под `browser` пространством имен, например `browser.browserAction.disable()` .
>  - API расширения Microsoft Edge используют обратные вызовы, но не обещает.


## Проблемы с допуском

Следующие известные проблемы занимают на платформе расширения и будут устранены в ближайшем будущем.

- При использовании свойства CSS `url()` абсолютные URL-адреса, использующиеся, `ms-browser-extension://` не будут работать так, как в Chrome. Чтобы обойти эту ошибку, вместо этого используйте относительные пути к ресурсам (начиная с корневого каталога расширения).
- `window.open()` не работает в фоновых сценариях расширения. Взамен рекомендуется использовать `browser.windows.create()` .
- Общие cookie-файлы поддерживаются, но фоновый сценарий расширения не будет иметь доступ к cookie-файлам сеанса, установленным на вкладке до включения расширения. Эта проблема не влияет на постоянные cookie-файлы.
- Если для расширения указаны только неподдерживаемые разрешения, то есть `activeTab`При попытке неопубликованного расширения будет выводиться следующее сообщение: "что-то пошло не так с расширениями, поэтому нам пришлось переустановить их. Вам потребуется снова включить их. "
- При запуске загрузки с помощью скрытого тега привязки в фоновых сценариях произойдет сбой. Это следует делать на странице расширения.


## закладки

`bookmarks`Поддерживаются следующие API:

| API                                   | Известные проблемы                                             | Несовместимость с хромом
|---------------------------------------|----------------------------------------------------------|--------------------------|
| [закладки](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/bookmarks) | | |
| [закладки. Создание](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/bookmarks/create) | | |
| [закладки. Remove](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/bookmarks/remove) | | |
| [закладки. и дерево](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/bookmarks/getTree) |  | |
| [закладки. Move](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/bookmarks/move) | | |
| [закладки. removeTree](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/bookmarks/removeTree) | | |
| [закладки. Update](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/bookmarks/update)            | | |


## browserAction

`browserAction`Поддерживаются следующие API:

| API                                   | Известные проблемы                                             | Несовместимость с хромом
|---------------------------------------|----------------------------------------------------------|--------------------------|
| [browserAction](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction) | | |
| [browserAction. Disable](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/disable) | | |
| [browserAction. Enable](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/enable) | | |
| [browserAction.getBadgeBackgroundColor](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/getBadgeBackgroundColor) |  | |
| [browserAction.setBadgeBackgroundColor](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/setBadgeBackgroundColor) | | |
| [browserAction. onclicks](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/onClicked) | | |
| [browserAction.setBadgeText](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/setBadgeText)            | | |
| [browserAction.setPopup](https://developer.mozilla.org/Add-ons/WebExtensions/API/browserAction/setPopup)  | | |
| [browserAction.getBadgeText](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/getBadgeText)   | | |
| [browserAction.setIcon](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/setIcon) | `browserAction.setIcon` не сохраняется. <br/><br/> `imageData`Параметр не поддерживается. <br/><br/> `path` является обязательным параметром.| |
| [browserAction.](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/getTitle) | | |
| [browserAction.setTitle](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/browserAction/setTitle) | | |

## contextMenu

`contextMenus`Поддерживаются следующие API:

| API                    | Известные проблемы | Несовместимость с хромом
|------------------------|--------------|----------------------|
| [contextMenu](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/contextMenus)  |  | |
| [contextMenu. ContextType](https://developer.mozilla.org/Add-ons/WebExtensions/API/contextMenus/ContextType) | `"page_action"` `ContextType` не отображается в контекстном меню действия страницы.| Microsoft EDGE не поддерживает `"launcher"` `ContextType` .|
| [contextMenu. Create](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/contextMenus/create)    | Если расширения не предоставляют a `contextmenuid` , `id` созданное значение не является уникальным. | |
| [contextMenu. onclickd](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/contextMenus/onClicked) | | |
| [contextMenu. Remove](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/contextMenus/remove) | | |
| [contextMenu. removeAll](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/contextMenus/removeAll) | | |
| [contextMenu. Update](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/contextMenus/update) | | |

## файлах

`cookies`Поддерживаются следующие API:

| API                    | Известные проблемы | Несовместимость с хромом
|------------------------|--------------|----------------------|
| [файлах](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/cookies)  |  | |
| [Cookies. Get](https://developer.mozilla.org/Add-ons/WebExtensions/API/cookies/get)    |  | |
| [Cookies. getAll](https://developer.mozilla.org/Add-ons/WebExtensions/API/cookies/getAll) |   | Если URL-адрес не указан, файлы cookie извлекаются только для URL-адресов в открытых в данный момент вкладках. В Chrome это получает все cookie-файлы на компьютере пользователя. |
| [Cookies. getAllCookieStores](https://developer.mozilla.org/Add-ons/WebExtensions/API/cookies/getAllCookieStores)  | | Всегда возвращает то же хранилище файлов cookie по умолчанию с ИДЕНТИФИКАТОРом "0". Все cookie-файлы входят в этот магазин. |
| [файлы cookie. OnChanged](https://developer.mozilla.org/Add-ons/WebExtensions/API/cookies/onChanged)    | | Не поддерживается. |
| [Cookies. Remove](https://developer.mozilla.org/Add-ons/WebExtensions/API/cookies/remove) |  | |
| [Cookies. Set](https://developer.mozilla.org/Add-ons/WebExtensions/API/cookies/set)    |  | |



## добавоч

`extension`Поддерживаются следующие API:

| API                                   | Известные проблемы | Несовместимость с хромом
|---------------------------------------|----------------------------------------------------------|-------------|
[добавоч](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/extension) | | |
[расширение. getBackgroundPage](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/extension/getBackgroundPage) | | |
[расширение getURL](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/extension/getURL) | | |
[расширение. для просмотра](https://developer.mozilla.org/Add-ons/WebExtensions/API/extension/getViews) | | |
[расширение. isAllowedIncognitoAccess](https://developer.mozilla.org/Add-ons/WebExtensions/API/extension/isAllowedIncognitoAccess) | | | 
[extension.inIncognitoContext](https://developer.mozilla.org/Add-ons/WebExtensions/API/extension/inIncognitoContext) | | | 



## i18n

`i18n`Поддерживаются следующие API:

API | Известные проблемы | Несовместимость с хромом
:------| :-------- | :---------------------
[i18n](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/i18n) | | |
[i18n.getAcceptLanguages](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/i18n/getAcceptLanguages) | | |
[i18n.](https://developer.mozilla.org/Add-ons/WebExtensions/API/i18n/getMessage) | `i18n.getMessage` При использовании недопустимого ключа вместо некорректного сбоя возникает исключение. <br/><br/> `i18n.getMessage` аргумент ожидает строки, но должен также допустить тип int или создать исключение. | |
[i18n.getUILanguage](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/i18n/getUILanguage) | | |

## С3

`idle`Поддерживаются следующие API:

API | Известные проблемы | Несовместимость с хромом
:------| :-------- | :---------------------
[С3](https://developer.mozilla.org/Add-ons/WebExtensions/API/idle) | | |
[Idle. setDetectionInterval](https://developer.mozilla.org/Add-ons/WebExtensions/API/idle/setDetectionInterval) | | |
[Idle. queryState](https://developer.mozilla.org/Add-ons/WebExtensions/API/idle/queryState) | | |

## уведомления

`notifications`Поддерживаются следующие API:

API | Известные проблемы | Несовместимость с хромом
:------| :-------- | :---------------------
[уведомления](https://developer.mozilla.org/Add-ons/WebExtensions/API/notifications) | | |
[Получайте. NotificationOptions](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/NotificationOptions) | | |
[Получайте. TemplateType](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/TemplateType) | | |
[уведомления. Clear](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/clear) | | |
[уведомления. Создание](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/create) | | |
[Notifications. getAll](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/getAll) | | |
[Notifications. Update](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/update) | | |
[Notifications. onButtonClicked](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/onButtonClicked) | | |
[уведомления. onclickd](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/onClicked) | | |
[уведомления. oncloseed](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/notifications/onClosed) | | |
Notifications. onPermissionLevelChanged | | |
Notifications. getPermissionLevel | | |

## pageAction

`pageAction`Поддерживаются следующие API:

API | Известные проблемы | Несовместимость с хромом
:------------ | :------------- | :--------------------
[pageAction](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction) | | |
[pageAction. Popup](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/getPopup) | | |
[pageAction.](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/getTitle) | | |
[pageAction. Hide](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/hide) | | |
[pageAction. onclicks](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/onClicked) | | |
[pageAction.setIcon](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/setIcon) | | `imageData`Параметр не поддерживается. <br/><br/> `path` является обязательным параметром. |
[pageAction.setPopup](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/setPopup) | | |
[pageAction.setTitle](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/setTitle) | | |
[pageAction. Показать](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/pageAction/show) | | |



## язык

`runtime`Поддерживаются следующие API:

API | Известные проблемы | Несовместимость с хромом
:------------ | :------------- | :-------------------
[язык](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime) | | |
[Runtime. Port. Disconnect](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/Port) | | |
[Runtime. Port. OnDisconnection](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/Port) | | |
[Runtime. Port. i](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/Port) | | |
[Runtime. Connect](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connect) | | |
[Runtime. connectNative](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative) | | |
[runtime.id](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime/id) | | |
[Runtime. getBackgroundPage](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/getBackgroundPage) | | |
[Runtime. manifest](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime/getManifest) | | |
[Runtime. getURL](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime/getURL) | | |
[Runtime. lastError](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime/lastError) | | |
[Runtime. Reload](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime/reload) | | |
[Runtime. sendMessage](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendMessage) | Страницы расширений Microsoft Edge могут использоваться `runtime.sendMessage` / `onMessage` для отправки сообщений. <br/><br/> `runtime.sendmessage` не поддерживается на страницах сайта. | Microsoft EDGE не поддерживает этот `options` параметр.|
[Runtime. sendNativeMessage](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) | | |
[Runtime. setUninstallUrl](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/setUninstallUrl) | | |
[Runtime. OnConnect](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/onConnect) | | |
[Runtime. oninstalled](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime/onInstalled) | | |
[Runtime. onmessage](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/runtime/onMessage) | `tab` объект в `runtime.onMessage` событии реализован не полностью. | `MessageSender.tlsChannelId` не поддерживается в Microsoft Edge.|

## хранилище

`storage`Поддерживаются следующие API:

API | Известные проблемы | Несовместимость с хромом
:------------ | :------------- | :------------------------
[хранилище](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/storage) |  | |
[Storage. local. Get](https://developer.mozilla.org/Add-ons/WebExtensions/API/Storage/StorageArea/get)  | | |
[Storage. local. Remove](https://developer.mozilla.org/Add-ons/WebExtensions/API/Storage/StorageArea/remove)  | | |
[Storage. local. Set](https://developer.mozilla.org/Add-ons/WebExtensions/API/Storage/StorageArea/set)  | | |
[Storage. local. Clear](https://developer.mozilla.org/Add-ons/WebExtensions/API/Storage/StorageArea/clear) | | |
[Storage. local. getBytesInUse](https://developer.mozilla.org/Add-ons/WebExtensions/API/Storage/StorageArea/getBytesInUse) | | `storage.local` данные сохраняются в формате, отличном от Chrome, что приводит к возвращению другого значения при вызове `storage.local.getBytesInUse` .  <br/><br/>Пример: `storage.local.set({ "k": { "s": "âas" } }` возвращает 13 в Chrome и 50 в Microsoft Edge.|
[Storage. Sync. Get](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/storage/StorageArea/get) | Если суммарный объем символов в `name` `author` полях и манифесте превышает 31 символ, это `storage.sync` может привести к невозможности работы пространства имен. | |
[Storage. Sync. Remove](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/storage/StorageArea/remove) | | |
[Storage. Sync. Set](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/storage/StorageArea/set) | | |
[хранилище. OnChanged](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/storage/onChanged) | | |

## закладок

`tabs`Поддерживаются следующие API:

API | Известные проблемы | Несовместимость с хромом
:------------ | :------------- | :----------------
[закладок](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs) | | |
[Табуляторы. captureVisibleTab](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/captureVisibleTab) | | |
[Табуляторы. Create](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/create) | | `selected`, `pinned` и `openerTabId` не поддерживаются. |
[Табуляторы. detectLanguage](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/detectLanguage) | | |
[tabs.executeScript](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/executeScript) | `runAt` игнорируется, если флажок установлен. Выполнение сценария в определенном кадре пока не поддерживается. | |
[Табуляторы. Get](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/get) | Страницы параметров. при появлении запроса на табуляции в окне, не вызываемом этим звонком, произошел сбой. | |
[Табуляторы. OnCurrent](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/getCurrent) | | |
[Табуляторы. insertCSS](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/insertCSS) | `runAt` игнорируется, если флажок установлен. | `cssOrigin` не поддерживается. |
[Табуляторы. OnActivated](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/onActivated) | | |
[Табуляторы. onattacheded](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/onAttached) | | |
[Табуляторы. OnCreated](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/onCreated) | | |
[Табуляторы. ondetach.](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs) | | |
[Табуляторы. removed](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/onRemoved) | | |
[Табуляторы. replaced](https://developer.mozilla.org/Add-ons/WebExtensions/API/tabs/onReplaced) | | |
[Табуляторы. OnUpdated](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/onUpdated) | После удаления и повторной установки этот URL-адрес не будет получен до тех пор, пока не будет перезапущена Microsoft Edge. | |
[Вкладка "Табуляция. запрос"](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/query) | `pinned`, `audible` и `muted` пока не поддерживаются. <br/><br/> `"popup"` `windowType` пока не поддерживается. | `highlighted` не поддерживается. <br/><br/> `"panel"`, `"app"` и `"devtools"` `windowType` не поддерживаются. |
[Загружайте символы табуляции](https://developer.mozilla.org/Add-ons/WebExtensions/API/tabs/reload) | | Microsoft EDGE не поддерживает обещаний. |
[Табуляторы. Remove](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/remove) | | |
[Табуляторы. sendMessage](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/sendMessage) | Сообщения с определенным кадром пока не поддерживаются. `tabs.sendMessage` никогда не отправляет ответ после обновления вкладки, если `runtime.onMessage` на вкладке "получение" нет прослушивателей. | |
[закладок. Вкладок](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/Tab) | `audible`,,, `mutedInfo` `inPrivate` `width` и `height` свойства пока не поддерживаются. | `openerTabId`, `selected` а `highlighted` свойства не поддерживаются. |
[Табуляторы. Update](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/tabs/update) | `pinned` и `muted` пока не поддерживаются. | `highlighted` и `selected` не поддерживаются. |


## Навигация

`webNavigation`Поддерживаются следующие API:


| API                                                                                                                                                           | Известные проблемы                                | Несовместимость с хромом                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------|
| [Навигация](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation)                                                     | Неверные идентификаторы вкладок.                      | Фильтрация, TransitionTypes и TransitionQualifiers не поддерживается. <br/><br/> Для вкладки все `processIds` это будет одинаково. |
| [Навигация. getAllFrames](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/getAllFrames)                           | Не включает элементы "объект-iframe". |                                                                                                                             |
| [Навигация. NOFRAMES](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/getFrame)                                   |                                             |                                                                                                                             |
| [Навигация. onBeforeNavigate](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/onBeforeNavigate)                   |                                             |                                                                                                                             |
| [Навигация. oncommittedные](https://developer.mozilla.org/Add-ons/WebExtensions/API/webNavigation/onCommitted)                                           |                                             |                                                                                                                             |
| [Навигация. OnComplete](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/onCompleted)                             |                                             |                                                                                                                             |
| [Навигация. onCreatedNavigationTarget](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/onCreatedNavigationTarget) |                                             |                                                                                                                             |
| [Навигация. onDOMContentLoaded](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/onDOMContentLoaded)               |                                             |                                                                                                                             |
| [Навигация. onErrorOccurred](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/onErrorOccurred)                     |                                             |                                                                                                                             |
| [Навигация. onHistoryStateUpdated](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/onHistoryStateUpdated)         |                                             |                                                                                                                             |
| [Навигация. onReferenceFragmentUpdated](https://developer.mozilla.org/Add-ons/WebExtensions/API/webNavigation/onReferenceFragmentUpdated)            |                                             |                                                                                                                             |
| [Навигация. onTabReplaced](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/onTabReplaced)                         |                                             | Не поддерживается.                                                                                                              |
| [Навигация. TransitionType](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/TransitionType)                       |                                             |                                                                                                                             |
| [Навигация. TransitionQualifier](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/webNavigation/TransitionQualifier)             |                                             |                                                                                                                             |

## WebRequest (запрос)

`webRequest`Поддерживаются следующие API:

API | Известные проблемы | Несовместимость с хромом
:------ | :----- | :-------
[WebRequest (запрос)](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest) | `webRequest` не поддерживается для синхронных `XmlHttpRequests` . | Сетевые запросы из расширений, такие как параметры, фон и всплывающие страницы, не поддерживаются.<br/><br/> Сетевые запросы `<object>` и `<embed>` элементы не поддерживаются.<br/><br/> Невозможно изменить заголовки для кэшированных запросов.  |
[handlerBehaviorChanged](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/handlerBehaviorChanged) | | Изменения обработчика автоматически обрабатываются в Microsoft Edge.<br/><br/>Звонок не действует.  |
[onAuthRequired](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onAuthRequired) | | |
[onBeforeRedirect](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onBeforeRedirect) | | |
[onBeforeRequest](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onBeforeRequest) | | `requestBody` не поддерживается. |
[onBeforeSendHeaders](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onBeforeSendHeaders) | | |
[onCompleted](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onCompleted) | | |
[onErrorOccurred](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onErrorOccurred) | | |
[onHeadersReceived](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onHeadersReceived) | |  |
[onResponseStarted](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onResponseStarted) | |  |
[onSendHeaders](https://developer.mozilla.org/Add-ons/WebExtensions/API/webRequest/onSendHeaders) | | |

## windows

`windows`Поддерживаются следующие API:


| API                                                                                                                               | Известные проблемы                                                   | Несовместимость с хромом                                                                                        |
|:----------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------|
| [windows](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows)                                     |                                                                | `Window` объекты не поддерживают `alwaysOnTop` свойство в Microsoft Edge. <br/><br/>Функция InPrivate не поддерживается. |
| [Windows. CreateType](https://developer.mozilla.org/Add-ons/WebExtensions/API/windows/CreateType)                            |                                                                | `"panel"` и `"detached_panel"` не поддерживаются в Microsoft Edge.                                           |
| [Windows. Create](https://developer.mozilla.org/Add-ons/WebExtensions/API/windows/create)                                    |                                                                | `tabId` параметр для разрыва вкладки не поддерживается.                                                       |
| [Windows. Get](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/get)                             |                                                                |                                                                                                                 |
| [Windows. getAll](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/getAll)                       | `windows.getAll({populate: true})` отсутствует `tabs` свойство. |                                                                                                                 |
| [Windows. на текущий момент](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/getCurrent)               |                                                                |                                                                                                                 |
| [Windows. getLastFocused](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/getLastFocused)       |                                                                |                                                                                                                 |
| [Windows. Update](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/update)                       | Указание положения не поддерживается.                          | `"minimized"`/`"maximized"`/`"fullscreen"` и `drawAttention` не поддерживаются в Microsoft Edge.             |
| [Windows. OnCreated](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/onCreated)                 |                                                                | `WindowType` фильтр не поддерживается.                                                                           |
| [Windows. onFocusChanged](https://developer.mozilla.org/Add-ons/WebExtensions/API/windows/onFocusChanged)                    |                                                                | `WindowType` фильтр не поддерживается.                                                                           |
| [Windows. WindowState](https://developer.mozilla.org/Add-ons/WebExtensions/API/windows/WindowState)                          | `"minimized"`, `"maximized"` `"fullscreen"` не поддерживаются. | `"docked"` не поддерживается в Microsoft Edge.                                                                  |
| [Windows. WindowType](https://developer.mozilla.org/Add-ons/WebExtensions/API/windows/WindowType)                            |                                                                | `"panel"``"app"`и `"devtools"` не поддерживаются в Microsoft Edge.                                       |
| [Windows. WINDOW_ID_CURRENT](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/WINDOW_ID_CURRENT) |                                                                |                                                                                                                 |
| [Windows. WINDOW_ID_NONE](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/API/windows/WINDOW_ID_NONE)       |                                                                |                                                                                                                 |
