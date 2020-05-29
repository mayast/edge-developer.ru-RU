---
description: Используйте панель элементы для проверки HTML, CSS, DOM и специальных возможностей на странице.
title: DevTools-элементы
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, элементы, HTML, CSS, точки останова DOM, события, Специальные возможности
ms.custom: seodec18
ms.openlocfilehash: 8948ddb3291bd122521e0b0800c0113a576d49e4
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572561"
---
# <span data-ttu-id="b0502-104">Элементы</span><span class="sxs-lookup"><span data-stu-id="b0502-104">Elements</span></span>

<span data-ttu-id="b0502-105">С помощью панели **элементы** вы можете выполнять следующие действия:</span><span class="sxs-lookup"><span data-stu-id="b0502-105">The **Elements** panel helps you to:</span></span>

* <span data-ttu-id="b0502-106">[Определение и редактирование элементов в дереве HTML](#html-tree-view) текущей страницы</span><span class="sxs-lookup"><span data-stu-id="b0502-106">[Identify and edit elements in the HTML tree](#html-tree-view) of the current page</span></span>
* <span data-ttu-id="b0502-107">[Проверка и изменение CSS](./elements/styles.md) на странице, включая псевдо-состояния и псевдо-элементы</span><span class="sxs-lookup"><span data-stu-id="b0502-107">[Inspect and modify CSS](./elements/styles.md) on the page, including pseudo-states and pseudo-elements</span></span>
* <span data-ttu-id="b0502-108">[Общие сведения о макете CSS и каскадном стиле](./elements/computed.md) на странице</span><span class="sxs-lookup"><span data-stu-id="b0502-108">[Understand the CSS layout and style cascade](./elements/computed.md) happening on the page</span></span>
* <span data-ttu-id="b0502-109">[Отслеживайте фальшивые обработчики событий](./elements/events.md) , чтобы их можно было отлаживать.</span><span class="sxs-lookup"><span data-stu-id="b0502-109">[Track down rogue event handlers](./elements/events.md) so you can debug them</span></span>
* <span data-ttu-id="b0502-110">[Установка отладочных точек останова для непредвиденных визуальных изменений](./elements/dom-breakpoints.md) для перехода в код, вызывающий их</span><span class="sxs-lookup"><span data-stu-id="b0502-110">[Set debugging breakpoints for unexpected visual changes](./elements/dom-breakpoints.md) to jump into the code causing them</span></span>
* <span data-ttu-id="b0502-111">[Получение подробных сведений о шрифтах, используемых на странице](./elements/fonts.md) , и о том, откуда они загружаются</span><span class="sxs-lookup"><span data-stu-id="b0502-111">[Get detailed information about the fonts used on the page](./elements/fonts.md) and where they're loading from</span></span>
* <span data-ttu-id="b0502-112">[Просмотр страницы с точки зрения средства чтения с экрана](./elements/accessibility.md) для проверки и проверки читаемости</span><span class="sxs-lookup"><span data-stu-id="b0502-112">[View your page from a screen reader's point of view](./elements/accessibility.md) to verify and test accessibility</span></span> 
* <span data-ttu-id="b0502-113">[Просмотр результатов изменения CSS](./elements/changes.md) , внесенных при ОТЛАДКЕ пользовательского интерфейса страницы</span><span class="sxs-lookup"><span data-stu-id="b0502-113">[Review a running diff of the CSS changes](./elements/changes.md) you make as you debug the UI of your page</span></span>

## <span data-ttu-id="b0502-114">Представление в виде дерева HTML</span><span class="sxs-lookup"><span data-stu-id="b0502-114">HTML tree view</span></span>

![Панель "элементы DevTools Microsoft Edge"](./media/elements.png)

1. <span data-ttu-id="b0502-116">С помощью инструмента **Выбор элемента** ( `Ctrl+B` ) найдите элемент в **представлении в виде дерева HTML** , щелкнув его на странице.</span><span class="sxs-lookup"><span data-stu-id="b0502-116">Use the **Select element** (`Ctrl+B`) tool to locate an element in the **HTML tree view** by clicking on it in the page.</span></span>

2. <span data-ttu-id="b0502-117">Используйте инструмент **выделения элементов** ( `Ctrl+Shift+L` ), чтобы найти на странице элемент, наведя на него указатель мыши в представлении в **виде дерева HTML**.</span><span class="sxs-lookup"><span data-stu-id="b0502-117">Use the **Element highlighting** (`Ctrl+Shift+L`) tool to locate an element on the page by hovering over it in the **HTML tree view**.</span></span>

3. <span data-ttu-id="b0502-118">Откройте средство **выбора цвета** ( `Ctrl+K` ), чтобы просмотреть список цветов, используемых на текущей странице.</span><span class="sxs-lookup"><span data-stu-id="b0502-118">Open the **Color picker** (`Ctrl+K`) tool to see a list of the colors in use on the current page.</span></span> <span data-ttu-id="b0502-119">Если щелкнуть цвет в списке, вы получите дополнительные сведения (оттенок, насыщенность, яркость, альфа-канал).</span><span class="sxs-lookup"><span data-stu-id="b0502-119">Clicking on a color on the list will provide further details (Hue, Saturation, Lightness, Alpha).</span></span> <span data-ttu-id="b0502-120">*Палитра цветов* также открывается при щелчке на цветном квадрате рядом с значением цвета в области **стили** , что позволяет редактировать цвет элемента страницы и сразу же просматривать результаты.</span><span class="sxs-lookup"><span data-stu-id="b0502-120">The *Color picker* also opens when you click on the colored square next to a color value in the **Styles** pane, allowing you to edit the color of a page element and immediately see the results.</span></span>

4. <span data-ttu-id="b0502-121">При нажатии кнопки **дерева специальных возможностей** откроется `Ctrl+Shift+A` область [дерева специальных возможностей](./elements/accessibility.md) , в которой отображается структура страницы в том виде, в котором она будет отображаться в специальных возможностях, например Screenreader [экранного диктора Windows](https://support.microsoft.com/help/22798/windows-10-narrator-get-started) .</span><span class="sxs-lookup"><span data-stu-id="b0502-121">The **Accessibility tree** (`Ctrl+Shift+A`) button will open the [Accessibility tree](./elements/accessibility.md) pane showing the structure of your page as it would appear to an assistive technology, such as the [Windows Narrator](https://support.microsoft.com/help/22798/windows-10-narrator-get-started) screenreader.</span></span>

5. <span data-ttu-id="b0502-122">Вы также можете **найти** `Ctrl+F` элемент () в представлении в виде дерева HTML, выполнив поиск имени, атрибутов или текстового содержимого тега.</span><span class="sxs-lookup"><span data-stu-id="b0502-122">You can also **Find** (`Ctrl+F`) an element in the HTML tree view by searching for its tag name, attributes, or text content.</span></span>

### <span data-ttu-id="b0502-123">Редактирование элементов</span><span class="sxs-lookup"><span data-stu-id="b0502-123">Editing elements</span></span>

<span data-ttu-id="b0502-124">Вы можете изменить элемент, щелкнув его правой кнопкой мыши в представлении в виде дерева HTML и выбрав в контекстном меню команду **изменить в виде HTML** .</span><span class="sxs-lookup"><span data-stu-id="b0502-124">You can edit an element by right-clicking on it within the HTML tree view and selecting **Edit as HTML** from the context menu.</span></span> <span data-ttu-id="b0502-125">Контекстное меню также предоставляет параметры для удаления, вырезания, копирования, вставки, настройки псевдо-классов CSS (*: активный*, *: Focus*, *: наведение*, *: Просмотрено*) и добавления атрибутов.</span><span class="sxs-lookup"><span data-stu-id="b0502-125">The context menu also provides options to delete, cut, copy, paste, set CSS pseudo-classes (*:active*, *:focus*, *:hover*, *:visited*) and add attributes.</span></span> <span data-ttu-id="b0502-126">Кроме того, можно изменить атрибут и (или) его значение, дважды щелкнув его в представлении в виде дерева HTML.</span><span class="sxs-lookup"><span data-stu-id="b0502-126">Another way to edit an attribute and/or its value is to double-click it from the HTML tree view.</span></span>

![Контекстное меню представления в виде дерева HTML](./media/elements_html_tree_context.png)

> [!NOTE]
> <span data-ttu-id="b0502-128">Редактирование дерева HTML не влияет на исходную разметку.</span><span class="sxs-lookup"><span data-stu-id="b0502-128">Editing the HTML tree does not affect the underlying source markup.</span></span> <span data-ttu-id="b0502-129">После обновления страницы изменения будут отменены, а только макет, определенный источником страниц.</span><span class="sxs-lookup"><span data-stu-id="b0502-129">Refreshing the page will revert your changes and render only the layout determined by the page source.</span></span> <span data-ttu-id="b0502-130">Вы можете **скопировать** измененный HTML-код в буфер обмена, щелкнув правой кнопкой мыши нужный элемент (или глобальный `html` элемент, если вы хотите, чтобы вся страница была открыта), чтобы открыть контекстное меню.</span><span class="sxs-lookup"><span data-stu-id="b0502-130">You can **Copy** your modified HTML to the clipboard by right-clicking the desired element (or the global `html` element, if you want the entire page) to open up the context menu.</span></span> <span data-ttu-id="b0502-131">(Параметры**вырезания** и **вставки** также доступны).</span><span class="sxs-lookup"><span data-stu-id="b0502-131">(**Cut** and **Paste** options are also available).</span></span>

<span data-ttu-id="b0502-132">В области [стили](./elements/styles.md) вы также можете добавлять и удалять и изменять псевдо-состояния и псевдо-элементы CSS.</span><span class="sxs-lookup"><span data-stu-id="b0502-132">From the [Styles](./elements/styles.md) pane you can also add/delete/edit CSS pseudo-states and pseudo-elements.</span></span>

## <span data-ttu-id="b0502-133">Панели инструментов</span><span class="sxs-lookup"><span data-stu-id="b0502-133">Tool Panes</span></span>

<span data-ttu-id="b0502-134">После того как вы выберете нужный элемент страницы, вы можете использовать области инструментов, чтобы проанализировать различные стили и свойства специальных возможностей, просмотреть прослушиватели событий и настроить точки останова для изменений DOM.</span><span class="sxs-lookup"><span data-stu-id="b0502-134">Once you have selected a page element of interest, you can use the tool panes to further inspect its different styles and accessibility properties, view its event listeners, and set DOM mutation breakpoints.</span></span>

![Панели "Инструменты" на панели "элементы"](./media/elements_toolpanes.png)

1. <span data-ttu-id="b0502-136">[**Стили**](./elements/styles.md): в настоящее время применены стили, упорядоченные по таблицам стилей</span><span class="sxs-lookup"><span data-stu-id="b0502-136">[**Styles**](./elements/styles.md): Currently applied styles organized by stylesheet</span></span>

2. <span data-ttu-id="b0502-137">[**Вычисляемый**](./elements/computed.md): в настоящее время применены стили, упорядоченные по АТРИБУТам CSS</span><span class="sxs-lookup"><span data-stu-id="b0502-137">[**Computed**](./elements/computed.md): Currently applied styles organized by CSS attributes</span></span>

3. <span data-ttu-id="b0502-138">[**События**](./elements/events.md): прослушиватели событий, зарегистрированные для текущего элемента и элементов предков</span><span class="sxs-lookup"><span data-stu-id="b0502-138">[**Events**](./elements/events.md): Event listeners registered on the current element and ancestor elements</span></span>

4. <span data-ttu-id="b0502-139">[**Точки останова DOM**](./elements/dom-breakpoints.md): точки останова, изменяющие DOM</span><span class="sxs-lookup"><span data-stu-id="b0502-139">[**DOM breakpoints**](./elements/dom-breakpoints.md): DOM Mutation Breakpoints</span></span> 

5. <span data-ttu-id="b0502-140">[**Шрифты**](./elements/fonts.md): примененные в данный момент шрифты для выбранного элемента</span><span class="sxs-lookup"><span data-stu-id="b0502-140">[**Fonts**](./elements/fonts.md): Currently applied fonts for a selected element</span></span>

6. <span data-ttu-id="b0502-141">[**Специальные возможности**](./elements/accessibility.md): свойства специальных возможностей</span><span class="sxs-lookup"><span data-stu-id="b0502-141">[**Accessibility**](./elements/accessibility.md):  Accessibility properties</span></span>

7. <span data-ttu-id="b0502-142">[**Изменения**](./elements/changes.md): изменения CSS, внесенные в ходе диагностического сеанса</span><span class="sxs-lookup"><span data-stu-id="b0502-142">[**Changes**](./elements/changes.md): CSS changes made during diagnostic session</span></span>  

## <span data-ttu-id="b0502-143">Горячие</span><span class="sxs-lookup"><span data-stu-id="b0502-143">Shortcuts</span></span>

| <span data-ttu-id="b0502-144">Действие</span><span class="sxs-lookup"><span data-stu-id="b0502-144">Action</span></span>               | <span data-ttu-id="b0502-145">Появивше</span><span class="sxs-lookup"><span data-stu-id="b0502-145">Shortcut</span></span>               |
|:---------------------|:-----------------------|
| <span data-ttu-id="b0502-146">Панель "элементы"</span><span class="sxs-lookup"><span data-stu-id="b0502-146">Elements panel</span></span>       | `Ctrl` + `1`           |
| <span data-ttu-id="b0502-147">Выделение элементов</span><span class="sxs-lookup"><span data-stu-id="b0502-147">Element highlighting</span></span> | `Ctrl` + `Shift` + `L` |
| <span data-ttu-id="b0502-148">Выбор элемента</span><span class="sxs-lookup"><span data-stu-id="b0502-148">Select element</span></span>       | `Ctrl` + `B`           |
| <span data-ttu-id="b0502-149">Палитра</span><span class="sxs-lookup"><span data-stu-id="b0502-149">Color picker</span></span>         | `Ctrl` + `K`           |
| <span data-ttu-id="b0502-150">Дерево специальных возможностей</span><span class="sxs-lookup"><span data-stu-id="b0502-150">Accessibility tree</span></span>   | `Ctrl` + `Shift` + `A` |
