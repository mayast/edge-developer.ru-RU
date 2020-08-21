---
ms.assetid: 2bc29371-4f2e-4b59-a588-30b107d751f6
description: Узнайте, как Microsoft Edge предоставляет веб-страницы для чтения веб-страниц, чтобы разрешить чтение веб-страниц.
title: Режим чтения — руководство по разработке
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, разработчики, html, css, javascript, разработчики
ms.openlocfilehash: 0d2076a63f97ecf2b4699795b0036736d0f95c9c
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "10941996"
---
# <span data-ttu-id="d3fed-104">Режим чтения</span><span class="sxs-lookup"><span data-stu-id="d3fed-104">Reading view</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="d3fed-105">В Microsoft Edge есть режим чтения, чтобы упростить чтение веб-страниц, как благодаря неотвлекающему нежелательному содержимому на странице.</span><span class="sxs-lookup"><span data-stu-id="d3fed-105">Microsoft Edge provides a reading view for a more streamlined, book-like reading experience of webpages without the distraction of unrelated or other secondary content on the page.</span></span>  <span data-ttu-id="d3fed-106">Режим чтения можно включать и выключать с помощью кнопки **чтения** \(значка книги\) в адресной строке или с `Ctrl` + `Shift` + `R` ней.</span><span class="sxs-lookup"><span data-stu-id="d3fed-106">Reading view can be toggled on or off from the **Reading view** \(book icon\) button on the address bar or with `Ctrl`+`Shift`+`R`.</span></span>  <span data-ttu-id="d3fed-107">При этом извлекаются следующие метаданные со страницы:</span><span class="sxs-lookup"><span data-stu-id="d3fed-107">Reading view extracts the following metadata from a page:</span></span>  

*   <span data-ttu-id="d3fed-108">Title</span><span class="sxs-lookup"><span data-stu-id="d3fed-108">Title</span></span>
*   <span data-ttu-id="d3fed-109">Автор</span><span class="sxs-lookup"><span data-stu-id="d3fed-109">Author</span></span>
*   <span data-ttu-id="d3fed-110">Дата</span><span class="sxs-lookup"><span data-stu-id="d3fed-110">Date</span></span>
*   <span data-ttu-id="d3fed-111">Издатель</span><span class="sxs-lookup"><span data-stu-id="d3fed-111">Publisher</span></span>
*   <span data-ttu-id="d3fed-112">Dominant image\(s\)</span><span class="sxs-lookup"><span data-stu-id="d3fed-112">Dominant image\(s\)</span></span>
*   <span data-ttu-id="d3fed-113">Названия dominant image\(s\)</span><span class="sxs-lookup"><span data-stu-id="d3fed-113">Captions of dominant image\(s\)</span></span>
*   <span data-ttu-id="d3fed-114">Дополнительные изображения</span><span class="sxs-lookup"><span data-stu-id="d3fed-114">Secondary images</span></span>
*   <span data-ttu-id="d3fed-115">Основное содержимое страницы</span><span class="sxs-lookup"><span data-stu-id="d3fed-115">Main text content of the page</span></span>
*   <span data-ttu-id="d3fed-116">Авторские права</span><span class="sxs-lookup"><span data-stu-id="d3fed-116">Copyright</span></span>

<span data-ttu-id="d3fed-117">После этого пользователи смогут настроить контрастность и размер шрифта с панели параметров Microsoft **Edge.**</span><span class="sxs-lookup"><span data-stu-id="d3fed-117">Users can then adjust the page contrast and font size from the Microsoft Edge **Settings** panel.</span></span>  

## <span data-ttu-id="d3fed-118">Извлечение метаданных</span><span class="sxs-lookup"><span data-stu-id="d3fed-118">Metadata extraction</span></span>  

<span data-ttu-id="d3fed-119">Ниже представлены подробные сведения о метаданных страницы, представленных в представлении чтения.</span><span class="sxs-lookup"><span data-stu-id="d3fed-119">Here are details of the page metadata rendered by reading view.</span></span>  

### <span data-ttu-id="d3fed-120">Title</span><span class="sxs-lookup"><span data-stu-id="d3fed-120">Title</span></span>  

<span data-ttu-id="d3fed-121">Чтобы убедиться, что в режиме чтения отображается название статьи:</span><span class="sxs-lookup"><span data-stu-id="d3fed-121">To ensure Reading view renders your article's title:</span></span>  

*   <span data-ttu-id="d3fed-122">Включение `title` элемента в верхний колонтитул</span><span class="sxs-lookup"><span data-stu-id="d3fed-122">Include a `title` element in your header</span></span>  
*   <span data-ttu-id="d3fed-123">Добавление тега метага</span><span class="sxs-lookup"><span data-stu-id="d3fed-123">Include a meta tag with</span></span> `name="title"`  
*   <span data-ttu-id="d3fed-124">Сопоставьте текст заголовка в теле статьи с строкой содержимого тега метаданных.</span><span class="sxs-lookup"><span data-stu-id="d3fed-124">Match the title text in your article body with the content string of your meta tag.</span></span>  <span data-ttu-id="d3fed-125">Pipes \( \) в строке содержимого не должен быть `|` активным, попробуйте использовать вместо него дефисы \( `-` \).</span><span class="sxs-lookup"><span data-stu-id="d3fed-125">Pipes \(`|`\) in your content string prevent the reader view from becoming active, try using hyphens \(`-`\) instead.</span></span>  

### <span data-ttu-id="d3fed-126">Автор</span><span class="sxs-lookup"><span data-stu-id="d3fed-126">Author</span></span>  

<span data-ttu-id="d3fed-127">В режиме чтения будет найден элемент, с которым имеется `class = "byline-name"` выбранный вами режим.</span><span class="sxs-lookup"><span data-stu-id="d3fed-127">Reading View will look for an element with `class = "byline-name"`.</span></span>  <span data-ttu-id="d3fed-128">Рекомендуется поместить имя автора после названия и перед текстом статьи.</span><span class="sxs-lookup"><span data-stu-id="d3fed-128">Best practice is to place the author name after the title and before the article body.</span></span>  

```html
<div class="byline-name">Author name</div>
```  

### <span data-ttu-id="d3fed-129">Дата</span><span class="sxs-lookup"><span data-stu-id="d3fed-129">Date</span></span>  

<span data-ttu-id="d3fed-130">В режиме чтения сведения издателя и даты обрабатываются в одной строке, а дополнительная строка выделить ее.</span><span class="sxs-lookup"><span data-stu-id="d3fed-130">Reading view will render the publisher and date information together on the same line, with additional styling to highlight this information.</span></span>  <span data-ttu-id="d3fed-131">Дата публикации статьи будет отображаться в точности так, как она выглядит в строке.</span><span class="sxs-lookup"><span data-stu-id="d3fed-131">The article's publishing date will render exactly as it appears in the string.</span></span>  <span data-ttu-id="d3fed-132">Режим чтения не преобразуется в определенный формат даты.</span><span class="sxs-lookup"><span data-stu-id="d3fed-132">Reading view does not convert to a specific date format.</span></span>  

<span data-ttu-id="d3fed-133">Если в тексте статьи указана дата и вы хотите, чтобы она отображалась, назначьте элемент, содержащему дату класса: `'dateline'`</span><span class="sxs-lookup"><span data-stu-id="d3fed-133">If you have a date in your article body and would like Reading view to render it, assign the element containing the date with the class `'dateline'`:</span></span>  

```html
<div class="dateline"> Wednesday, September 18, 2013 7:38 AM </div>
```  

<span data-ttu-id="d3fed-134">Если в тексте статьи нет даты, но вы хотите просмотреть дату, используйте тег `name='displaydate'` метага:</span><span class="sxs-lookup"><span data-stu-id="d3fed-134">If you don't have a date in the article body but would like Reading view to render the date, use the meta tag `name='displaydate'`:</span></span>  

```html
<meta name="displaydate" content=" Wednesday, September 18, 2013 7:38 AM ">
```  

### <span data-ttu-id="d3fed-135">Издатель</span><span class="sxs-lookup"><span data-stu-id="d3fed-135">Publisher</span></span>  

<span data-ttu-id="d3fed-136">В режиме чтения найдите протокол Open Graph для `"og:site_name"` отображения сведений издателя.</span><span class="sxs-lookup"><span data-stu-id="d3fed-136">Reading view will look for the Open Graph protocol `"og:site_name"` to render the publisher information.</span></span>  <span data-ttu-id="d3fed-137">Он также ищет и ищет `source_organization` атрибуты во всех HTML-тегах как дополнительный индикатор `publisher` сведений издателя на странице.</span><span class="sxs-lookup"><span data-stu-id="d3fed-137">It also looks for `source_organization` and `publisher` attributes in any html tag as a secondary indicator of publisher information on the page.</span></span>  <span data-ttu-id="d3fed-138">Текст издателя будет гиперссылкой на URL-адрес страницы с использованием стиля страницы режима чтения.</span><span class="sxs-lookup"><span data-stu-id="d3fed-138">The publisher text will be hyperlinked to the URL of page using the Reading view page hyperlink style.</span></span>  

```html
<meta content="Name of organization source" property="og:site_name">
```  

### <span data-ttu-id="d3fed-139">Изображения</span><span class="sxs-lookup"><span data-stu-id="d3fed-139">Images</span></span>  

<span data-ttu-id="d3fed-140">В режиме чтения выводится большинство необработанных изображений, при >= 400 пикселей и пропорции >= 1/3 и =< 3.0.</span><span class="sxs-lookup"><span data-stu-id="d3fed-140">Reading view captures most raw images with width >= 400px and aspect ratio >= 1/3 and =< 3.0.</span></span>  <span data-ttu-id="d3fed-141">Изображения, не удовлетворяемые этим измерениям, могут быть извлечены, например изображения, размеры которых меньше 400 пк с субтитров, но содержат их субтитры.</span><span class="sxs-lookup"><span data-stu-id="d3fed-141">Images that do not meet these dimensions may still be extracted, such as images that are smaller than 400px in width but have captions.</span></span>  <span data-ttu-id="d3fed-142">Первое подходящее изображение становится небольшим изображением статьи.</span><span class="sxs-lookup"><span data-stu-id="d3fed-142">The first eligible image becomes the dominant image of the article.</span></span>  <span data-ttu-id="d3fed-143">Dominant изображение обрабатывается как первый фрагмент содержимого и имеет ширину столбца целий.</span><span class="sxs-lookup"><span data-stu-id="d3fed-143">The dominant image is rendered as the first piece of content and given full column width.</span></span>  <span data-ttu-id="d3fed-144">Все приведенные ниже изображения отображаются как встроенные изображения в статье.</span><span class="sxs-lookup"><span data-stu-id="d3fed-144">All following images are rendered as inline images within the article.</span></span>  

### <span data-ttu-id="d3fed-145">Подписи</span><span class="sxs-lookup"><span data-stu-id="d3fed-145">Captions</span></span>  

<span data-ttu-id="d3fed-146">Рекомендуется разместить изображения на тегах [рисунков,](https://developer.mozilla.org/docs/Web/HTML/Element/figure) не более двух вставленных тегов. [figcaption](https://developer.mozilla.org/docs/Web/HTML/Element/figcaption)</span><span class="sxs-lookup"><span data-stu-id="d3fed-146">Best practice is to place images in [figure](https://developer.mozilla.org/docs/Web/HTML/Element/figure) tags with no more than two nested [figcaption](https://developer.mozilla.org/docs/Web/HTML/Element/figcaption) tags.</span></span>  

### <span data-ttu-id="d3fed-147">Body</span><span class="sxs-lookup"><span data-stu-id="d3fed-147">Body</span></span>  

<span data-ttu-id="d3fed-148">В режиме чтения все содержащийся в документе текст страницы можно хранить в режиме чтения, чтобы все глубоко содержали большинство шрифтов и глубокого текста dom.</span><span class="sxs-lookup"><span data-stu-id="d3fed-148">To ensure that all the body text of your page is captured by Reading view, it helps to keep most of the article text the same font size and DOM depth.</span></span>  <span data-ttu-id="d3fed-149">Алгоритм представления чтения позволяет издателям привлечь к строкам или словам свободы.</span><span class="sxs-lookup"><span data-stu-id="d3fed-149">The reading view algorithm allows for some deviation from this rule so publishers can have the freedom to add emphasis to lines or words.</span></span>  

### <span data-ttu-id="d3fed-150">Авторские права</span><span class="sxs-lookup"><span data-stu-id="d3fed-150">Copyright</span></span>  

<span data-ttu-id="d3fed-151">В режиме чтения отображаются сведения об авторских правах, обозначенные тегами метагами или если отсутствует `name = "copyright"` информация об тегах метатега, текст узла с символом авторского права \( `©` \).</span><span class="sxs-lookup"><span data-stu-id="d3fed-151">Reading view extracts and displays copyright information denoted by meta tags with `name = "copyright"`, or if no meta tag information exists, a text node that contains the copyright \(`©`\) symbol.</span></span>  <span data-ttu-id="d3fed-152">В режиме чтения в конце основного текста статьи выводятся сведения об авторских правах в конце основного текста статьи, если используется меньший размер шрифта, чем основной текст.</span><span class="sxs-lookup"><span data-stu-id="d3fed-152">Reading view displays copyright information at the end of the article main body, styled using a smaller font size than the main body text.</span></span>  

```html
<meta name="copyright" content="Your copyright information">
```  

## <span data-ttu-id="d3fed-153">Выход из режима чтения</span><span class="sxs-lookup"><span data-stu-id="d3fed-153">Opting out of Reading View</span></span>  

<span data-ttu-id="d3fed-154">Если вы хорошо знакомы с содержимым, вы можете отменить эту функцию с помощью следующего тега метага:</span><span class="sxs-lookup"><span data-stu-id="d3fed-154">If you feel your content is not a good fit for Reading view, you can use the following meta tag to opt out of this feature:</span></span>  

```html
<meta name="IE_RM_OFF" content="true">
```  

<span data-ttu-id="d3fed-155">При этом кнопка **режима** чтения не отображается в адресной строке при просмотре страницы пользователями.</span><span class="sxs-lookup"><span data-stu-id="d3fed-155">With this tag, the **Reading view** button will not appear in the address bar when your users view your page.</span></span>  
