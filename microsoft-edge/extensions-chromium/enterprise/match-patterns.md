---
description: Документация по политике предприятия для расширения EDGE (Chromium).
title: Соответствие шаблонам
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/05/2019
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: Edge-Chromium, Разработка расширений, расширения браузера, надстройки, центр партнера, разработчик
ms.openlocfilehash: 16f54fcdc127822e89e050c367a681d886b0c8d0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571646"
---
# Соответствие шаблонам

Разрешения узла и сопоставление сценариев содержимого основаны на наборе URL-адресов, определенных в шаблонах соответствия.  Шаблон соответствия — это URL-адрес, который начинается с разрешенной схемы ( `http` ,, `https` `file` или `ftp` и может содержать `*` символы "").  Особый шаблон `<all_urls>` соответствует любому URL-адресу, который начинается с разрешенной схемы.  Каждый шаблон соответствия состоит из трех частей:  

*   _схема_ (например, или `http` `file` или `*`  

> [!NOTE]
> Доступ к `file` URL-адресам не является автоматическим.  Пользователь должен перейти на страницу управления расширениями и принять участие в `file` доступе к каждому добавочному номеру.  

*   `_host_` (например, `www.google.com` или `*.google.com` или `*` ; Если схема является файлом, часть узла отсутствует.  
*   `_path_` (например,, `/*` `/foo*` или `/foo/bar` .)  Путь должен присутствовать в разрешении узла, но всегда обрабатываются как `/*` .  

Базовый синтаксис:  

```shell
<url-pattern> := <scheme>://<host><path>
<scheme> := '*' | 'http' | 'https' | 'file' | 'ftp'
<host> := '*' | '*.' <any char except '/' and '*'>+
<path> := '/' <any chars>
```  

Значение зависит от `*` того, находится ли оно в части схема, узел или путь.  Если схема указана `*` , она будет соответствовать одному `http` или `https` , а не `file` или `ftp` .  Если узел является просто `*` , он соответствует любому узлу. Если узел установлен `*.hostname` , он соответствует указанному узлу или любому из поддоменов.  В разделе Path каждый из них `*` соответствует 0 или большему числу символов.  В приведенной ниже таблице показаны некоторые допустимые шаблоны.  

| Схеме | Что это такое? | Примеры совпадающих URL-адресов |  
|:--- |:--- |:--- |  
| `http://*/*` | Соответствует любому URL-адресу, использующему схему HTTP | `http://www.google.com` `http://example.org/foo/bar.html` |  
| `http://*/foo*` | Соответствует любому URL-адресу, использующему схему HTTP, на любом узле, если путь начинается с `/foo` | `http://example.com/foo/bar.html` `http://www.google.com/foo` |  
| `https://*.google.com/foo*bar` | Соответствует любому URL-адресу, использующему схему HTTPS, на `google.com` узле \ (например `www.google.com` , `docs.google.com` или `google.com` \), если путь начинается с `/foo` и заканчивается на `bar` | `https://www.google.com/foo/baz/bar` `https://docs.google.com/foobar` |  
| `http://example.org/foo/bar.html` | Соответствует указанному URL-адресу | `http://example.org/foo/bar.html` |  
|`file:///foo*` | Соответствует любому локальному файлу, путь которого начинается с `/foo` | `file:///foo/bar.html` `file:///foo` |  
| `http://127.0.0.1/*` | Соответствует любому URL-адресу, который использует `http` схему и находится на узле. `127.0.0.1` | `http://127.0.0.1` `http://127.0.0.1/foo/bar.html` |  
| `*://mail.google.com/*` | Соответствует любому URL-адресу, который начинается с `http://mail.google.com` OR `https://mail.google.com` . | `http://mail.google.com/foo/baz/bar` `https://mail.google.com/foobar` |  
| `<all_urls>` | Соответствует любому URL-адресу, использующему разрешенную схему. \ (В начале этого раздела вы увидите список разрешенных схем. \) | `http://example.org/foo/bar.html` `file:///bar/baz.html` |  

Ниже приведено несколько примеров `_invalid_` соответствия шаблону.

| Неверный шаблон | Почему это плохо |  
|:--- |:--- |  
| `http://www.foo.com` | Нет `_path_` |  
| `http://*foo/bar` | `*`за "" в узле может следовать только " `.` или `/` " |  
| `http://foo.*.bar/baz` | Если " `*` " находится в поле `_host_` , оно должно быть первым символом |  
| `http:/bar` | Отсутствует `_scheme_` Разделитель \ (' `/` ' должно быть " `//` " \ ") |  
| `foo://*` | Недопустимо `_scheme_` |  

Некоторые схемы не поддерживаются во всех контекстах.

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> [Здесь](https://developer.chrome.com/extensions/match_patterns/)будет найдена исходная страница.  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
