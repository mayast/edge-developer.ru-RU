---
description: Ознакомьтесь со сведениями о поддерживаемых ключах манифеста, а также известных проблемах и несовместимости с Chrome.
title: Ключи манифеста, поддерживаемые расширениями
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: EDGE, веб-разработка, HTML, CSS, JavaScript, разработчик
ms.openlocfilehash: deeff12251d25efaed1b40c98594c616a0d9c99a
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571598"
---
# Поддерживаемые ключи манифеста  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

Каждое расширение имеет файл манифеста в формате JSON, именуемый manifest. JSON. Этот файл содержит важную информацию о расширении в диапазоне от его имени до разрешений. Если не указано в заметке ниже, свойства манифеста Microsoft Edge следуют той же реализации, что и Chrome.

Ниже приведен пример [файла манифеста JSON Microsoft Edge](./supported-manifest-keys/json-manifest-example.md).

## Обязательные ключи

Требуются следующие клавиши:

Раздел | Известные проблемы | Несовместимость с хромом
:------------ | :------------- | :--------------
[созданные](https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/author)  | | 
[name](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/name) | | |
[version](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/version) | | |

## Рекомендуемые клавиши

Рекомендуются следующие клавиши:

Раздел | Известные проблемы | Несовместимость с хромом
:------------ | :------------- | :--------------
browser_specific_settings | | Указывает предпочтительное состояние расширения в браузере. Браузер может, в зависимости от таких факторов, как репутация расширения или общее количество кнопок, уже включенных в адресную строку пользователя, и не может использовать его в будущем выпуске. Это можно использовать для указания положения по умолчанию `browserAction` значка. </br></br> `"browser_specific_settings": {`</br>&nbsp;&nbsp;&nbsp;&nbsp;`"edge": {`</br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`"browser_action_next_to_addressbar": true`</br>&nbsp;&nbsp;&nbsp;&nbsp;`}`</br>`}` </br></br> Не поддерживается в Chrome.|
[default_locale](https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/default_locale)| | |
[description](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/description) | | |
[значки](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/icons) | | |
[manifest_version](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/manifest_version) | | В настоящее время не учитывается в Microsoft Edge.



## browser_actionные и page_actionные ключи

Вы можете добавить только одну из следующих клавиш (или None):

Раздел | Известные проблемы | Несовместимость с хромом
:------------ | :------------- | :--------------
[browser_action](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/browser_action)  | | Microsoft EDGE не поддерживает следующий синтаксис:  `browser_action : {"default_icon" : "icon.png" }`   <br/>Должен быть указан размер значков. <br/>Предпочтительные размеры: 20px, 25px, 30px, 40px. <br/> Другие поддерживаемые размеры: 19px, 35px, 38px.|
[page_action](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/page_action) | | Microsoft EDGE не поддерживает следующий синтаксис:  `page_action : {"default_icon" : "icon.png" }`   <br/>Должен быть указан размер значков. <br/>Предпочтительные размеры: 20px, 25px, 30px, 40px. <br/>Другие поддерживаемые размеры: 19px, 35px, 38px.|

## Необязательные ключи

Следующие клавиши являются необязательными:

Раздел | Известные проблемы | Несовместимость с хромом
:------------ | :------------- | :--------------
[фон](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/background) | | Persistent является обязательным полем для Microsoft Edge.
[content_scripts](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/content_scripts)  | | |
[content_security_policy](https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/content_security_policy)  | В параметрах безопасности содержимого страницы блокируются WebSocket в скриптах содержимого, что создает неопределенное исключение. | Расширения Microsoft EDGE в настоящее время поддерживают [ограничения политики по умолчанию](https://developer.mozilla.org/Add-ons/WebExtensions/Content_Security_Policy#Default_content_security_policy). `script-src 'self'; object-src 'self'` |
[инкогнито](https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/incognito) | | | 
key  | | |
options_page | | |
[правами](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/permissions)  | | |
short_name  | | |
[web_accessible_resources](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/web_accessible_resources) | | |

### Поддерживаемые разрешения
Поддерживаются следующие [разрешения](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/permissions) :


| Разрешение         | Описание                                                                                                                                                                                                                                                                         |
|:-------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \ <all_urls \ >       | Разрешает фоновые и контентные сценарии для взаимодействия со всеми веб-страницами с дополнительными [правами](https://developer.mozilla.org/Add-ons/WebExtensions/manifest.json/permissions#Host_permissions).                                                                                  |
| contextMenu       | Предоставляет доступ к `contextMenus` API. Это позволяет добавлять элементы в контекстное меню Microsoft Edge.                                                                                                                                                                                     |
| файлах            | Предоставляет доступ к `cookies` API. Это позволяет отправлять запросы и изменять файлы cookie, а также получать уведомления об изменениях.                                                                                                                                                           |
| Geolocation        | Разрешите расширению использовать `geolocation` API HTML5 без запроса разрешения пользователя.                                                                                                                                                                                   |
| С3               | Предоставляет доступ к `idle` API. Это позволяет определить, когда изменяется состояние простоя компьютера.                                                                                                                                                                                    |
| хранилище            | Предоставляет доступ к `storage` API. Это позволяет хранить, извлекать и отслеживать изменения, внесенные в пользовательские данные.                                                                                                                                                                             |
| закладок               | Предоставляет доступ к `tabs` API-интерфейсу для взаимодействия с системой вкладок браузера. Это позволяет создавать, изменять и переупорядочение вкладок в браузере, включая URL-адреса, связанные с каждой вкладкой.                                                                                       |
| unlimitedStorage   | Обеспечивает неограниченный объем хранилища (в зависимости от системных ресурсов [), а](https://developer.mozilla.org/Add-ons/WebExtensions/API/storage/local) не 5 МБ. Кроме того, для каждой пары значений "максимум от 5" до неограниченного места в зависимости от системных ресурсов. |
| Навигация      | Предоставляет доступ к `webNavigation` API. Это позволяет получать уведомления о состоянии запросов на переходы.                                                                                                                                                              |
| WebRequest (запрос)         | Предоставляет доступ к `webRequest` API. Это позволяет наблюдать за трафиком, а также перехватывать, блокировать или изменять запрос в ходе проверки.                                                                                                                               |
| webRequestBlocking | Требуется, если расширение использует `webRequest` API в блокирующем режиме.                                                                                                                                                                                                           |

'""'
