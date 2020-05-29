---
ms.assetid: 2bc29371-4f2e-4b59-a588-30b107d751f6
description: Узнайте о том, как Microsoft Edge предлагает представление для чтения веб-страниц, позволяющее бесплатно читать дополнительные возможности чтения.
title: 'Руководство для разработчиков: режим чтения'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: EDGE, веб-разработка, HTML, CSS, JavaScript, разработчик
ms.openlocfilehash: e84edb5cc29b644939895f2996c50f3b4ec23379
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10570900"
---
# <span data-ttu-id="0ec38-104">Режим чтения</span><span class="sxs-lookup"><span data-stu-id="0ec38-104">Reading view</span></span>

<span data-ttu-id="0ec38-105">Microsoft Edge предоставляет *представление для чтения* для более удобной работы с веб-страницами, так же как и без отзыва несвязанных или других вспомогательных материалов на странице.</span><span class="sxs-lookup"><span data-stu-id="0ec38-105">Microsoft Edge provides a *reading view* for a more streamlined, book-like reading experience of webpages without the distraction of unrelated or other secondary content on the page.</span></span> <span data-ttu-id="0ec38-106">Режим чтения можно включить или отключить из **режима чтения** (значка книги) в **адресной строке** (или с помощью **сочетания клавиш CTRL**  +  **+**  +  **R**).</span><span class="sxs-lookup"><span data-stu-id="0ec38-106">Reading view can be toggled on or off from the **Reading view** (book icon) button on the **address bar** (or with **Ctrl** + **Shift** + **R**).</span></span> <span data-ttu-id="0ec38-107">В режиме чтения на странице извлекаются следующие метаданные:</span><span class="sxs-lookup"><span data-stu-id="0ec38-107">Reading view extracts the following metadata from a page:</span></span>

* <span data-ttu-id="0ec38-108">Title</span><span class="sxs-lookup"><span data-stu-id="0ec38-108">Title</span></span>
* <span data-ttu-id="0ec38-109">Созданные</span><span class="sxs-lookup"><span data-stu-id="0ec38-109">Author</span></span>
* <span data-ttu-id="0ec38-110">Дата</span><span class="sxs-lookup"><span data-stu-id="0ec38-110">Date</span></span>
* <span data-ttu-id="0ec38-111">Издатель</span><span class="sxs-lookup"><span data-stu-id="0ec38-111">Publisher</span></span>
* <span data-ttu-id="0ec38-112">Доминирующее изображение (-ов)</span><span class="sxs-lookup"><span data-stu-id="0ec38-112">Dominant image(s)</span></span>
* <span data-ttu-id="0ec38-113">Заголовки доминирующего изображения (-ов)</span><span class="sxs-lookup"><span data-stu-id="0ec38-113">Captions of dominant image(s)</span></span>
* <span data-ttu-id="0ec38-114">Дополнительные изображения</span><span class="sxs-lookup"><span data-stu-id="0ec38-114">Secondary images</span></span>
* <span data-ttu-id="0ec38-115">Основное текстовое содержимое страницы</span><span class="sxs-lookup"><span data-stu-id="0ec38-115">Main text content of the page</span></span>
* <span data-ttu-id="0ec38-116">Авторские права</span><span class="sxs-lookup"><span data-stu-id="0ec38-116">Copyright</span></span>

<span data-ttu-id="0ec38-117">Пользователи могут настроить контрастность страницы и размер шрифта на панели " **Параметры** Microsoft Edge".</span><span class="sxs-lookup"><span data-stu-id="0ec38-117">Users can then adjust the page contrast and font size from the Microsoft Edge **Settings** panel.</span></span>

## <span data-ttu-id="0ec38-118">Извлечение метаданных</span><span class="sxs-lookup"><span data-stu-id="0ec38-118">Metadata extraction</span></span>


<span data-ttu-id="0ec38-119">Ниже приведены подробные сведения о метаданных страницы, отображаемых в режиме чтения.</span><span class="sxs-lookup"><span data-stu-id="0ec38-119">Here are details of the page metadata rendered by reading view.</span></span>

### <span data-ttu-id="0ec38-120">Title</span><span class="sxs-lookup"><span data-stu-id="0ec38-120">Title</span></span>

<span data-ttu-id="0ec38-121">Чтобы убедиться в том, что в режиме чтения отображается название статьи, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="0ec38-121">To ensure Reading view renders your article's title:</span></span>

* <span data-ttu-id="0ec38-122">Добавление элемента **заголовка** в верхний колонтитул</span><span class="sxs-lookup"><span data-stu-id="0ec38-122">Include a **title** element in your header</span></span>
* <span data-ttu-id="0ec38-123">Включение тега meta с</span><span class="sxs-lookup"><span data-stu-id="0ec38-123">Include a meta tag with</span></span> `name="title"`
* <span data-ttu-id="0ec38-124">Поиск текста заголовка в тексте статьи с помощью строки содержимого тега meta.</span><span class="sxs-lookup"><span data-stu-id="0ec38-124">Match the title text in your article body with the content string of your meta tag.</span></span> <span data-ttu-id="0ec38-125">Каналы `|` в строке контента не допускают, что представление "читатель" становится активным, попробуйте использовать hypens `-` .</span><span class="sxs-lookup"><span data-stu-id="0ec38-125">Pipes `|` in your content string prevent the reader view from becoming active, try using hypens `-` instead.</span></span>

### <span data-ttu-id="0ec38-126">Созданные</span><span class="sxs-lookup"><span data-stu-id="0ec38-126">Author</span></span>

<span data-ttu-id="0ec38-127">В режиме чтения будет искаться элемент `class = "byline-name"` .</span><span class="sxs-lookup"><span data-stu-id="0ec38-127">Reading View will look for an element with `class = "byline-name"`.</span></span> <span data-ttu-id="0ec38-128">Рекомендуется размещать имя автора после названия и перед текстом статьи.</span><span class="sxs-lookup"><span data-stu-id="0ec38-128">Best practice is to place the author name after the title and before the article body.</span></span>

```html
<div class="byline-name">Author name</div>
```

### <span data-ttu-id="0ec38-129">Дата</span><span class="sxs-lookup"><span data-stu-id="0ec38-129">Date</span></span>

<span data-ttu-id="0ec38-130">В режиме чтения сведения о издателе и дате отображаются в одной строке с дополнительными стилями, чтобы выделить эти сведения.</span><span class="sxs-lookup"><span data-stu-id="0ec38-130">Reading view will render the publisher and date information together on the same line, with additional styling to highlight this information.</span></span> <span data-ttu-id="0ec38-131">Дата публикации статьи будет отображаться точно так же, как в строке.</span><span class="sxs-lookup"><span data-stu-id="0ec38-131">The article's publishing date will render exactly as it appears in the string.</span></span> <span data-ttu-id="0ec38-132">Режим чтения не преобразуется в определенный формат даты.</span><span class="sxs-lookup"><span data-stu-id="0ec38-132">Reading view does not convert to a specific date format.</span></span>

<span data-ttu-id="0ec38-133">Если у вас есть дата в тексте статьи и вы хотите, чтобы режим чтения отображался, назначьте элемент, содержащий дату, на этот класс `'dateline'` :</span><span class="sxs-lookup"><span data-stu-id="0ec38-133">If you have a date in your article body and would like Reading view to render it, assign the element containing the date with the class `'dateline'`:</span></span>

```html
<div class="dateline"> Wednesday, September 18, 2013 7:38 AM </div>
```

<span data-ttu-id="0ec38-134">Если у вас нет даты в тексте статьи, но вы хотите, чтобы в режиме чтения отображалась Дата, используйте тег META `name='displaydate'` :</span><span class="sxs-lookup"><span data-stu-id="0ec38-134">If you don't have a date in the article body but would like Reading view to render the date, use the meta tag `name='displaydate'`:</span></span>

```html
<meta name="displaydate" content=" Wednesday, September 18, 2013 7:38 AM ">
```

### <span data-ttu-id="0ec38-135">Издатель</span><span class="sxs-lookup"><span data-stu-id="0ec38-135">Publisher</span></span>

<span data-ttu-id="0ec38-136">Режим чтения будет искать протокол *Open Graph* `"og:site_name"` для отрисовки данных издателя.</span><span class="sxs-lookup"><span data-stu-id="0ec38-136">Reading view will look for the *Open Graph* protocol `"og:site_name"` to render the publisher information.</span></span> <span data-ttu-id="0ec38-137">Он также ищет `source_organization` и `publisher` атрибуты в любом HTML-теге как дополнительный индикатор сведений об издателе на странице.</span><span class="sxs-lookup"><span data-stu-id="0ec38-137">It also looks for `source_organization` and `publisher` attributes in any html tag as a secondary indicator of publisher information on the page.</span></span> <span data-ttu-id="0ec38-138">Текст издателя будет гиперссылкой на URL-адрес страницы с помощью стиля "гиперссылка" на странице "режим чтения".</span><span class="sxs-lookup"><span data-stu-id="0ec38-138">The publisher text will be hyperlinked to the URL of page using the Reading view page hyperlink style.</span></span>

```html
<meta content="Name of organization source" property="og:site_name">
```

### <span data-ttu-id="0ec38-139">Изображения</span><span class="sxs-lookup"><span data-stu-id="0ec38-139">Images</span></span>

<span data-ttu-id="0ec38-140">В режиме чтения захватывается большинство необработанных изображений с Width >= 400px и пропорции >= 1/3 и =< 3,0.</span><span class="sxs-lookup"><span data-stu-id="0ec38-140">Reading view captures most raw images with width >= 400px and aspect ratio >= 1/3 and =< 3.0.</span></span> <span data-ttu-id="0ec38-141">Изображения, которые не соответствуют этим измерениям, могут по-прежнему извлекаться, например изображения, размер которых меньше 400px в ширину, но субтитры.</span><span class="sxs-lookup"><span data-stu-id="0ec38-141">Images that do not meet these dimensions may still be extracted, such as images that are smaller than 400px in width but have captions.</span></span> <span data-ttu-id="0ec38-142">Первое подходящего изображения становится главным изображением статьи.</span><span class="sxs-lookup"><span data-stu-id="0ec38-142">The first eligible image becomes the dominant image of the article.</span></span> <span data-ttu-id="0ec38-143">Доминирующее изображение визуализируется как первый фрагмент содержимого и задается полная ширина столбца.</span><span class="sxs-lookup"><span data-stu-id="0ec38-143">The dominant image is rendered as the first piece of content and given full column width.</span></span> <span data-ttu-id="0ec38-144">Все приведенные ниже изображения отображаются как встроенные изображения в статье.</span><span class="sxs-lookup"><span data-stu-id="0ec38-144">All following images are rendered as inline images within the article.</span></span>

### <span data-ttu-id="0ec38-145">Подписи</span><span class="sxs-lookup"><span data-stu-id="0ec38-145">Captions</span></span>

<span data-ttu-id="0ec38-146">Лучше размещайте изображения на [рисунках](https://msdn.microsoft.com/library/gg593038(v=vs.85).aspx) с помощью тегов, не имеющих более двух вложенных тегов [figcaption](https://msdn.microsoft.com/library/gg593037(v=vs.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="0ec38-146">Best practice is to place images in [figure](https://msdn.microsoft.com/library/gg593038(v=vs.85).aspx) tags with no more than two nested [figcaption](https://msdn.microsoft.com/library/gg593037(v=vs.85).aspx) tags.</span></span>

### <span data-ttu-id="0ec38-147">Body</span><span class="sxs-lookup"><span data-stu-id="0ec38-147">Body</span></span>

<span data-ttu-id="0ec38-148">Чтобы убедиться в том, что весь основной текст страницы захватывается режимом чтения, это позволяет хранить в большей части текста статьи одинаковый размер шрифта и глубину DOM.</span><span class="sxs-lookup"><span data-stu-id="0ec38-148">To ensure that all the body text of your page is captured by Reading view, it helps to keep most of the article text the same font size and DOM depth.</span></span> <span data-ttu-id="0ec38-149">Алгоритм представления для чтения допускает некоторое отклонение от этого правила, чтобы издатели могли использовать свободу выделения для линий или слов.</span><span class="sxs-lookup"><span data-stu-id="0ec38-149">The reading view algorithm allows for some deviation from this rule so publishers can have the freedom to add emphasis to lines or words.</span></span>

### <span data-ttu-id="0ec38-150">Авторские права</span><span class="sxs-lookup"><span data-stu-id="0ec38-150">Copyright</span></span>

<span data-ttu-id="0ec38-151">В режиме чтения извлекаются и отображаются сведения об авторских правах, обозначающие теги META `name = "copyright"` , или если сведения о тегах meta отсутствуют, текстовый узел, содержащий символ авторского права (**©**).</span><span class="sxs-lookup"><span data-stu-id="0ec38-151">Reading view extracts and displays copyright information denoted by meta tags with `name = "copyright"`, or if no meta tag information exists, a text node that contains the copyright (**©**) symbol.</span></span> <span data-ttu-id="0ec38-152">В режиме чтения сведения об авторских правах отображаются в конце основного текста статьи, в стиле которого используется меньший размер шрифта, чем у основного основного текста.</span><span class="sxs-lookup"><span data-stu-id="0ec38-152">Reading view displays copyright information at the end of the article main body, styled using a smaller font size than the main body text.</span></span>

```html
<meta name="copyright" content="Your copyright information">
```

## <span data-ttu-id="0ec38-153">Выход из режима чтения</span><span class="sxs-lookup"><span data-stu-id="0ec38-153">Opting out of Reading View</span></span>


<span data-ttu-id="0ec38-154">Если вы считаете, что содержимое не подходит для просмотра в режиме чтения, вы можете использовать следующий тег META для отказа от этой функции:</span><span class="sxs-lookup"><span data-stu-id="0ec38-154">If you feel your content is not a good fit for Reading view, you can use the following meta tag to opt out of this feature:</span></span>

```html
<meta name="IE_RM_OFF" content="true">
```

<span data-ttu-id="0ec38-155">При использовании этого тега кнопка " **режим чтения** " не отображается в адресной строке, когда пользователи просматривают страницу.</span><span class="sxs-lookup"><span data-stu-id="0ec38-155">With this tag, the **Reading view** button will not appear in the address bar when your users view your page.</span></span>
