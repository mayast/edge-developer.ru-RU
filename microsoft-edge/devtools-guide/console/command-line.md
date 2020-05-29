---
description: Использование командной строки консоли для взаимодействия с запущенной страницей
title: DevTools-Console — Командная строка
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, Командная строка консоли
ms.custom: seodec18
ms.openlocfilehash: c661736e5ea264f60279c89cfa0f9c55361d2288
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572590"
---
# <span data-ttu-id="61841-104">Командная строка консоли</span><span class="sxs-lookup"><span data-stu-id="61841-104">Console command line</span></span>

<span data-ttu-id="61841-105">Используйте командную строку консоли для просмотра и изменения значений на странице, а также для выполнения отладочного кода во всех случаях при использовании [*функции*](/visualstudio/ide/javascript-intellisense) автоматического завершения кода для Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="61841-105">Use the Console command line to view and change values on a page and execute debug code on the fly, all while taking advantage of Visual Studio [*IntelliSense*](/visualstudio/ide/javascript-intellisense) auto code completion.</span></span> 

<span data-ttu-id="61841-106">Просто введите любой допустимый сценарий JavaScript в командной строке и нажмите кнопку `Enter` , чтобы выполнить.</span><span class="sxs-lookup"><span data-stu-id="61841-106">Simply enter any valid JavaScript at the command line prompt and press `Enter` to execute.</span></span> <span data-ttu-id="61841-107">Для `Shift+Enter` добавления разрыва строки с помощью многострочного ввода.</span><span class="sxs-lookup"><span data-stu-id="61841-107">For multi-line input use `Shift+Enter` to add a line-break.</span></span> <span data-ttu-id="61841-108">Используйте `Up` `Down` клавиши со стрелками для перехода к предыдущим командам консоли, которые вы ввели в текущем сеансе DevTools.</span><span class="sxs-lookup"><span data-stu-id="61841-108">Use the `Up` and `Down` arrow keys to navigate through previous console commands you entered during the current  DevTools session.</span></span> <span data-ttu-id="61841-109">В дополнение к стандартным сценариям JavaScript и [API консоли](./console-api.md), консоль также поддерживает следующие команды:</span><span class="sxs-lookup"><span data-stu-id="61841-109">In addition to standard JavaScript and the [Console API](./console-api.md), the Console also supports the following commands for:</span></span>

 - [<span data-ttu-id="61841-110">Выбор объектов DOM</span><span class="sxs-lookup"><span data-stu-id="61841-110">Selecting DOM objects</span></span>](#dom-selectors)
 - [<span data-ttu-id="61841-111">Проверка свойств объекта</span><span class="sxs-lookup"><span data-stu-id="61841-111">Inspecting object properties</span></span>](#object-inspection)
 - [<span data-ttu-id="61841-112">Поиск всех прослушивателей событий для заданного объекта</span><span class="sxs-lookup"><span data-stu-id="61841-112">Finding all the event listeners on a given object</span></span>](#event-listeners)

<span data-ttu-id="61841-113">Сценарий, введенный в командной строке, выполняется в [глобальной области](/scripting/javascript/advanced/variable-scope-javascript) окна, в которой выбрано текущее окно, если эта страница не была приостановлена в точке останова.</span><span class="sxs-lookup"><span data-stu-id="61841-113">Script entered in the command line executes in the [global scope](/scripting/javascript/advanced/variable-scope-javascript) of the currently selected window, unless the page is paused at a breakpoint.</span></span> <span data-ttu-id="61841-114">Команды консоли, введенные при приостановке страницы, будут выполняться в [локальной области](/scripting/javascript/advanced/variable-scope-javascript) текущей функции в стеке вызовов.</span><span class="sxs-lookup"><span data-stu-id="61841-114">Console commands entered while the page is paused will execute in the [local scope](/scripting/javascript/advanced/variable-scope-javascript) of the current function within the call stack.</span></span>

<span data-ttu-id="61841-115">На консоли есть раскрывающийся список **целевых** контекстов выполнения прямо над областью вывода консоли.</span><span class="sxs-lookup"><span data-stu-id="61841-115">The Console has a **Target** execution context drop-down just above the Console output area.</span></span> <span data-ttu-id="61841-116">По умолчанию выбран документ верхнего уровня, **_top**.</span><span class="sxs-lookup"><span data-stu-id="61841-116">The default selection is the top-level document, **_top**.</span></span> <span data-ttu-id="61841-117">Любые элементы IFRAME в документе или запущенных расширениях также отображаются в виде параметров, что позволяет запускать команды в этих областях.</span><span class="sxs-lookup"><span data-stu-id="61841-117">Any iframes in the document or running extensions will also appear as options, allowing you to alternately run commands within those scopes.</span></span>

## <span data-ttu-id="61841-118">Селекторы DOM</span><span class="sxs-lookup"><span data-stu-id="61841-118">DOM selectors</span></span>
<span data-ttu-id="61841-119">Эти консольные селекторы предоставляют простые сокращенные сведения для быстрого доступа к объектам в модели DOM.</span><span class="sxs-lookup"><span data-stu-id="61841-119">These console selectors provide simple shorthands for quickly accessing objects within the DOM:</span></span>

### <span data-ttu-id="61841-120">$ (*Строка выбора CSS*)</span><span class="sxs-lookup"><span data-stu-id="61841-120">$(*CSS selector string*)</span></span>
<span data-ttu-id="61841-121">Возвращает первый элемент в документе, соответствующий указанному [селектору CSS](https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Selectors) (или группе элементов выбора, разделенных запятыми).</span><span class="sxs-lookup"><span data-stu-id="61841-121">Returns the first element within the document matching the specified [CSS selector](https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Selectors)  (or comma-separated group of selectors) string.</span></span> <span data-ttu-id="61841-122">Краткая форма [Document. querySelector ()](https://developer.mozilla.org/docs/Web/API/Document/querySelector).</span><span class="sxs-lookup"><span data-stu-id="61841-122">Shorthand for [document.querySelector()](https://developer.mozilla.org/docs/Web/API/Document/querySelector).</span></span>

<span data-ttu-id="61841-123">Пример: Откройте консоль и введите текст, `$('#main')` который будет возвращать объект div `id='main'` на этой странице.</span><span class="sxs-lookup"><span data-stu-id="61841-123">Example: Open the console and type `$('#main')` to return the div object with `id='main'` on this page.</span></span>

![Пример использования Selector "$"](../media/console_cmd_$.png)

### <span data-ttu-id="61841-125">$ $ (*Строка выбора CSS*)</span><span class="sxs-lookup"><span data-stu-id="61841-125">$$(*CSS selector string*)</span></span>
<span data-ttu-id="61841-126">Возвращает массив элементов в документе, соответствующий указанному [селектору CSS](https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Selectors) (или группе элементов выбора, разделенных запятыми).</span><span class="sxs-lookup"><span data-stu-id="61841-126">Returns an array of elements within the document matching the specified [CSS selector](https://developer.mozilla.org/docs/Learn/CSS/Introduction_to_CSS/Selectors)  (or comma-separated group of selectors) string.</span></span> <span data-ttu-id="61841-127">Краткая форма [Document. querySelectorAll ()](https://developer.mozilla.org/docs/Web/API/Document/querySelectorAll).</span><span class="sxs-lookup"><span data-stu-id="61841-127">Shorthand for [document.querySelectorAll()](https://developer.mozilla.org/docs/Web/API/Document/querySelectorAll).</span></span>

<span data-ttu-id="61841-128">Пример: Откройте консоль и введите текст, `$$('.container')` который будет возвращать все объекты div `class='container'` на этой странице.</span><span class="sxs-lookup"><span data-stu-id="61841-128">Example: Open the console and type `$$('.container')` to return all the div objects with `class='container'` on this page.</span></span>

![Пример использования Selector "$ $"](../media/console_cmd_$$.png)

### <span data-ttu-id="61841-130">$0, $1, $2,...</span><span class="sxs-lookup"><span data-stu-id="61841-130">$0, $1, $2,...</span></span>
<span data-ttu-id="61841-131">Возвращает последние элементы, выделенные на панели [**элементы**](../elements.md) , где `$0` выделен выбранный элемент, `$1` и т. д. — это выбранный элемент.</span><span class="sxs-lookup"><span data-stu-id="61841-131">Returns the last elements selected in the [**Elements**](../elements.md) panel, where `$0` represents the currently selected item, `$1` was the selected item before that, and so on.</span></span>

<span data-ttu-id="61841-132">Пример: Откройте DevTools на вкладке **элементы** , нажмите, `CTRL + B` чтобы активировать инструмент " **Выбор элемента** ", а затем щелкните часть области на этой странице с помощью мыши.</span><span class="sxs-lookup"><span data-stu-id="61841-132">Example: Open  DevTools to the **Elements** tab, press `CTRL + B` to activate the **Select element** tool and click some area on this page with your mouse.</span></span> <span data-ttu-id="61841-133">Теперь откройте консоль и введите текст, `$0` чтобы вернуть элемент, который вы только что открыли.</span><span class="sxs-lookup"><span data-stu-id="61841-133">Now open the Console and type `$0` to return the element you just clicked.</span></span>

![Пример использования средства выбора "$0"](../media/console_cmd_$0.png)

### <span data-ttu-id="61841-135">$x (*выражение XPath*)</span><span class="sxs-lookup"><span data-stu-id="61841-135">$x(*XPath expression*)</span></span>
<span data-ttu-id="61841-136">Возвращает массив элементов, соответствующих указанному выражению [XPath](https://developer.mozilla.org/docs/Introduction_to_using_XPath_in_JavaScript) .</span><span class="sxs-lookup"><span data-stu-id="61841-136">Returns an array of elements matched by the specified [XPath](https://developer.mozilla.org/docs/Introduction_to_using_XPath_in_JavaScript) expression.</span></span> 

<span data-ttu-id="61841-137">Пример: Откройте консоль и введите, `$x('//script[@defer]')` чтобы вернуть все `<script>` элементы на этой странице, содержащие `defer` атрибут.</span><span class="sxs-lookup"><span data-stu-id="61841-137">Example: Open the console and type `$x('//script[@defer]')` to return all the `<script>` elements on this page that contain a `defer` attribute.</span></span>

![Пример использования Selector "$x"](../media/console_cmd_$x.png)

## <span data-ttu-id="61841-139">Проверка объектов</span><span class="sxs-lookup"><span data-stu-id="61841-139">Object inspection</span></span>

<span data-ttu-id="61841-140">Эти команды предоставляют быстрые способы проверки свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="61841-140">These commands provide quick ways to inspect the properties of an object.</span></span> <span data-ttu-id="61841-141">Указанный объект должен быть определен либо в глобальном пространстве имен, либо в текущей области отладчика.</span><span class="sxs-lookup"><span data-stu-id="61841-141">The specified object must either be defined in the global namespace or the current scope of the debugger.</span></span>

### <span data-ttu-id="61841-142">dir (*объект*)</span><span class="sxs-lookup"><span data-stu-id="61841-142">dir(*object*)</span></span>
<span data-ttu-id="61841-143">Возвращает список свойств указанного объекта в виде дерева.</span><span class="sxs-lookup"><span data-stu-id="61841-143">Returns a tree view list of properties for the specified object.</span></span>

<span data-ttu-id="61841-144">Пример: Откройте консоль и введите `dir(document)` сведения о свойствах объекта Document, представляющих эту страницу.</span><span class="sxs-lookup"><span data-stu-id="61841-144">Example: Open the console and type `dir(document)` to see the object properties for the document object representing this page.</span></span>

![Пример использования метода dir](../media/console_cmd_dir.png)

### <span data-ttu-id="61841-146">клавиши (*объект*)</span><span class="sxs-lookup"><span data-stu-id="61841-146">keys(*object*)</span></span>
<span data-ttu-id="61841-147">Возвращает массив имен свойств, вложенных в указанный объект.</span><span class="sxs-lookup"><span data-stu-id="61841-147">Returns an array of property names attached to the specified object.</span></span>

<span data-ttu-id="61841-148">Пример: Откройте консоль и введите `keys(window)` данные, чтобы вернуть все свойства, определенные в глобальном объекте Window.</span><span class="sxs-lookup"><span data-stu-id="61841-148">Example: Open the console and type `keys(window)` to return all of the properties defined on the global window object.</span></span>

![Пример использования метода "Keys"](../media/console_cmd_keys.png)

### <span data-ttu-id="61841-150">значения (*объект*)</span><span class="sxs-lookup"><span data-stu-id="61841-150">values(*object*)</span></span>
<span data-ttu-id="61841-151">Возвращает массив значений свойства, вложенных в указанный объект.</span><span class="sxs-lookup"><span data-stu-id="61841-151">Returns an array of property values attached to the specified object.</span></span>

<span data-ttu-id="61841-152">Пример: Откройте консоль и введите `values(window)` значения всех свойств (ключей), определенных в объекте глобального окна.</span><span class="sxs-lookup"><span data-stu-id="61841-152">Example: Open the console and type `values(window)` to return the values of all the properties (keys) defined on the global window object.</span></span>

![Пример использования метода Values](../media/console_cmd_values.png)

## <span data-ttu-id="61841-154">Прослушиватели событий</span><span class="sxs-lookup"><span data-stu-id="61841-154">Event listeners</span></span>

<span data-ttu-id="61841-155">Эта команда позволяет проверить прослушиватели событий, зарегистрированные для определенного объекта.</span><span class="sxs-lookup"><span data-stu-id="61841-155">This command allows you to inspect the event listeners registered to a given object.</span></span> <span data-ttu-id="61841-156">Указанный объект должен быть определен либо в глобальном пространстве имен, либо в текущей области отладчика.</span><span class="sxs-lookup"><span data-stu-id="61841-156">The specified object must either be defined in the global namespace or the current scope of the  debugger.</span></span>

### <span data-ttu-id="61841-157">getEventListeners (*объект*)</span><span class="sxs-lookup"><span data-stu-id="61841-157">getEventListeners(*object*)</span></span>
<span data-ttu-id="61841-158">Возвращает объект, который содержит ключ для каждого зарегистрированного типа события для заданного объекта.</span><span class="sxs-lookup"><span data-stu-id="61841-158">Returns an object containing a key for each registered event type on the given object.</span></span> <span data-ttu-id="61841-159">Значением каждого ключа является массив прослушивателей событий и связанные с ними сведения.</span><span class="sxs-lookup"><span data-stu-id="61841-159">The value of each key is an array of event listeners and their related info.</span></span> 

<span data-ttu-id="61841-160">Пример: Откройте консоль и введите текст, `getEventListeners(document)` чтобы просмотреть все прослушиватели событий, зарегистрированные на объекте "документ" на этой странице.</span><span class="sxs-lookup"><span data-stu-id="61841-160">Example: Open the console and type `getEventListeners(document)` to see all the event listeners registered on the document object of this page.</span></span>

![Пример использования метода "getEventListeners"](../media/console_cmd_getEventListeners.png)
