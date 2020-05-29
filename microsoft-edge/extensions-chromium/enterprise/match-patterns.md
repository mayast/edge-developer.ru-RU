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
# <span data-ttu-id="468fa-104">Соответствие шаблонам</span><span class="sxs-lookup"><span data-stu-id="468fa-104">Match Patterns</span></span>

<span data-ttu-id="468fa-105">Разрешения узла и сопоставление сценариев содержимого основаны на наборе URL-адресов, определенных в шаблонах соответствия.</span><span class="sxs-lookup"><span data-stu-id="468fa-105">Host permissions and content script matching are based on a set of URLs defined by match patterns.</span></span>  <span data-ttu-id="468fa-106">Шаблон соответствия — это URL-адрес, который начинается с разрешенной схемы ( `http` ,, `https` `file` или `ftp` и может содержать `*` символы "").</span><span class="sxs-lookup"><span data-stu-id="468fa-106">A match pattern is essentially a URL that begins with a permitted scheme (`http`, `https`, `file`, or `ftp`, and that can contain '`*`' characters.</span></span>  <span data-ttu-id="468fa-107">Особый шаблон `<all_urls>` соответствует любому URL-адресу, который начинается с разрешенной схемы.</span><span class="sxs-lookup"><span data-stu-id="468fa-107">The special pattern `<all_urls>` matches any URL that starts with a permitted scheme.</span></span>  <span data-ttu-id="468fa-108">Каждый шаблон соответствия состоит из трех частей:</span><span class="sxs-lookup"><span data-stu-id="468fa-108">Each match pattern has 3 parts:</span></span>  

*   <span data-ttu-id="468fa-109">_схема_ (например, или `http` `file` или</span><span class="sxs-lookup"><span data-stu-id="468fa-109">_scheme_ — for example, `http` or `file` or</span></span> `*`  

> [!NOTE]
> <span data-ttu-id="468fa-110">Доступ к `file` URL-адресам не является автоматическим.</span><span class="sxs-lookup"><span data-stu-id="468fa-110">Access to `file` URLs is not automatic.</span></span>  <span data-ttu-id="468fa-111">Пользователь должен перейти на страницу управления расширениями и принять участие в `file` доступе к каждому добавочному номеру.</span><span class="sxs-lookup"><span data-stu-id="468fa-111">The user must visit the Extensions management page and opt in to `file` access for each Extension that requests it.</span></span>  

*   `_host_` <span data-ttu-id="468fa-112">(например, `www.google.com` или `*.google.com` или `*` ; Если схема является файлом, часть узла отсутствует.</span><span class="sxs-lookup"><span data-stu-id="468fa-112">— for example, `www.google.com` or `*.google.com` or `*`; if the scheme is file, there is no host part.</span></span>  
*   `_path_` <span data-ttu-id="468fa-113">(например,, `/*` `/foo*` или `/foo/bar` .)</span><span class="sxs-lookup"><span data-stu-id="468fa-113">— for example, `/*`, `/foo*`, or `/foo/bar`.</span></span>  <span data-ttu-id="468fa-114">Путь должен присутствовать в разрешении узла, но всегда обрабатываются как `/*` .</span><span class="sxs-lookup"><span data-stu-id="468fa-114">The path must be present in a host permission, but is always treated as `/*`.</span></span>  

<span data-ttu-id="468fa-115">Базовый синтаксис:</span><span class="sxs-lookup"><span data-stu-id="468fa-115">The basic syntax:</span></span>  

```shell
<url-pattern> := <scheme>://<host><path>
<scheme> := '*' | 'http' | 'https' | 'file' | 'ftp'
<host> := '*' | '*.' <any char except '/' and '*'>+
<path> := '/' <any chars>
```  

<span data-ttu-id="468fa-116">Значение зависит от `*` того, находится ли оно в части схема, узел или путь.</span><span class="sxs-lookup"><span data-stu-id="468fa-116">The meaning of `*` depends on whether it is in the scheme, host, or path part.</span></span>  <span data-ttu-id="468fa-117">Если схема указана `*` , она будет соответствовать одному `http` или `https` , а не `file` или `ftp` .</span><span class="sxs-lookup"><span data-stu-id="468fa-117">If the scheme is `*`, then it matches either `http` or `https`, and not `file`, or `ftp`.</span></span>  <span data-ttu-id="468fa-118">Если узел является просто `*` , он соответствует любому узлу.</span><span class="sxs-lookup"><span data-stu-id="468fa-118">If the host is just `*`, then it matches any host.</span></span> <span data-ttu-id="468fa-119">Если узел установлен `*.hostname` , он соответствует указанному узлу или любому из поддоменов.</span><span class="sxs-lookup"><span data-stu-id="468fa-119">If the host is `*.hostname`, then it matches the specified host or any of the subdomains.</span></span>  <span data-ttu-id="468fa-120">В разделе Path каждый из них `*` соответствует 0 или большему числу символов.</span><span class="sxs-lookup"><span data-stu-id="468fa-120">In the path section, each `*` matches 0 or more characters.</span></span>  <span data-ttu-id="468fa-121">В приведенной ниже таблице показаны некоторые допустимые шаблоны.</span><span class="sxs-lookup"><span data-stu-id="468fa-121">The following table shows some valid patterns.</span></span>  

| <span data-ttu-id="468fa-122">Схеме</span><span class="sxs-lookup"><span data-stu-id="468fa-122">Pattern</span></span> | <span data-ttu-id="468fa-123">Что это такое?</span><span class="sxs-lookup"><span data-stu-id="468fa-123">What it does</span></span> | <span data-ttu-id="468fa-124">Примеры совпадающих URL-адресов</span><span class="sxs-lookup"><span data-stu-id="468fa-124">Examples of matching URLs</span></span> |  
|:--- |:--- |:--- |  
| `http://*/*` | <span data-ttu-id="468fa-125">Соответствует любому URL-адресу, использующему схему HTTP</span><span class="sxs-lookup"><span data-stu-id="468fa-125">Matches any URL that uses the http scheme</span></span> | `http://www.google.com` `http://example.org/foo/bar.html` |  
| `http://*/foo*` | <span data-ttu-id="468fa-126">Соответствует любому URL-адресу, использующему схему HTTP, на любом узле, если путь начинается с</span><span class="sxs-lookup"><span data-stu-id="468fa-126">Matches any URL that uses the http scheme, on any host, as long as the path starts with</span></span> `/foo` | `http://example.com/foo/bar.html` `http://www.google.com/foo` |  
| `https://*.google.com/foo*bar` | <span data-ttu-id="468fa-127">Соответствует любому URL-адресу, использующему схему HTTPS, на `google.com` узле \ (например `www.google.com` , `docs.google.com` или `google.com` \), если путь начинается с `/foo` и заканчивается на</span><span class="sxs-lookup"><span data-stu-id="468fa-127">Matches any URL that uses the https scheme, is on a `google.com` host \(such as `www.google.com`, `docs.google.com`, or `google.com`\), as long as the path starts with `/foo` and ends with</span></span> `bar` | `https://www.google.com/foo/baz/bar` `https://docs.google.com/foobar` |  
| `http://example.org/foo/bar.html` | <span data-ttu-id="468fa-128">Соответствует указанному URL-адресу</span><span class="sxs-lookup"><span data-stu-id="468fa-128">Matches the specified URL</span></span> | `http://example.org/foo/bar.html` |  
|`file:///foo*` | <span data-ttu-id="468fa-129">Соответствует любому локальному файлу, путь которого начинается с</span><span class="sxs-lookup"><span data-stu-id="468fa-129">Matches any local file whose path starts with</span></span> `/foo` | `file:///foo/bar.html` `file:///foo` |  
| `http://127.0.0.1/*` | <span data-ttu-id="468fa-130">Соответствует любому URL-адресу, который использует `http` схему и находится на узле.</span><span class="sxs-lookup"><span data-stu-id="468fa-130">Matches any URL that uses the `http` scheme and is on the host</span></span> `127.0.0.1` | `http://127.0.0.1` `http://127.0.0.1/foo/bar.html` |  
| `*://mail.google.com/*` | <span data-ttu-id="468fa-131">Соответствует любому URL-адресу, который начинается с `http://mail.google.com` OR `https://mail.google.com` .</span><span class="sxs-lookup"><span data-stu-id="468fa-131">Matches any URL that starts with `http://mail.google.com` or `https://mail.google.com`.</span></span> | `http://mail.google.com/foo/baz/bar` `https://mail.google.com/foobar` |  
| `<all_urls>` | <span data-ttu-id="468fa-132">Соответствует любому URL-адресу, использующему разрешенную схему.</span><span class="sxs-lookup"><span data-stu-id="468fa-132">Matches any URL that uses a permitted scheme.</span></span> <span data-ttu-id="468fa-133">\ (В начале этого раздела вы увидите список разрешенных схем. \)</span><span class="sxs-lookup"><span data-stu-id="468fa-133">\(See the beginning of this section for the list of permitted schemes.\)</span></span> | `http://example.org/foo/bar.html` `file:///bar/baz.html` |  

<span data-ttu-id="468fa-134">Ниже приведено несколько примеров `_invalid_` соответствия шаблону.</span><span class="sxs-lookup"><span data-stu-id="468fa-134">Here are some examples of `_invalid_` pattern matches:</span></span>

| <span data-ttu-id="468fa-135">Неверный шаблон</span><span class="sxs-lookup"><span data-stu-id="468fa-135">Bad pattern</span></span> | <span data-ttu-id="468fa-136">Почему это плохо</span><span class="sxs-lookup"><span data-stu-id="468fa-136">Why it is bad</span></span> |  
|:--- |:--- |  
| `http://www.foo.com` | <span data-ttu-id="468fa-137">Нет</span><span class="sxs-lookup"><span data-stu-id="468fa-137">No</span></span> `_path_` |  
| `http://*foo/bar` | <span data-ttu-id="468fa-138">`*`за "" в узле может следовать только " `.` или `/` "</span><span class="sxs-lookup"><span data-stu-id="468fa-138">'`*`' in the host can be followed only by a '`.`' or '`/`'</span></span> |  
| `http://foo.*.bar/baz` | <span data-ttu-id="468fa-139">Если " `*` " находится в поле `_host_` , оно должно быть первым символом</span><span class="sxs-lookup"><span data-stu-id="468fa-139">If '`*`' is in the `_host_`, it must be the first character</span></span> |  
| `http:/bar` | <span data-ttu-id="468fa-140">Отсутствует `_scheme_` Разделитель \ (' `/` ' должно быть " `//` " \ ")</span><span class="sxs-lookup"><span data-stu-id="468fa-140">Missing `_scheme_` separator \('`/`' should be "`//`"\)</span></span> |  
| `foo://*` | <span data-ttu-id="468fa-141">Недопустимо</span><span class="sxs-lookup"><span data-stu-id="468fa-141">Invalid</span></span> `_scheme_` |  

<span data-ttu-id="468fa-142">Некоторые схемы не поддерживаются во всех контекстах.</span><span class="sxs-lookup"><span data-stu-id="468fa-142">Some schemes are not supported in all contexts.</span></span>

> [!NOTE]
> <span data-ttu-id="468fa-143">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="468fa-143">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="468fa-144">[Здесь](https://developer.chrome.com/extensions/match_patterns/)будет найдена исходная страница.</span><span class="sxs-lookup"><span data-stu-id="468fa-144">The original page is found [here](https://developer.chrome.com/extensions/match_patterns/).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="468fa-146">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="468fa-146">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
