---
ms.assetid: 4d3fa934-4fa8-4c02-b9b5-88506c76baac
description: Руководства по функциям браузера в Microsoft Edge.
title: Браузер — руководство для разработки
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, разработчики, html, css, javascript, разработчики
ms.openlocfilehash: 854b0e8ac057db3cc8b53af6205404d0841dfdb4
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942040"
---
# <span data-ttu-id="6af55-104">Функции браузера</span><span class="sxs-lookup"><span data-stu-id="6af55-104">Browser features</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

## <span data-ttu-id="6af55-105">Политики автозапуска</span><span class="sxs-lookup"><span data-stu-id="6af55-105">Autoplay policies</span></span>  

 <span data-ttu-id="6af55-106">Microsoft Edge предоставляет клиентам возможность персонализировать параметры просмотра на веб-сайтах, которые автоматически воспроизводят мультимедиа, чтобы минимизировать отвлекающую информацию в Интернете и пропускную способность.</span><span class="sxs-lookup"><span data-stu-id="6af55-106">Microsoft Edge provides customers with the ability to personalize their browsing preferences on websites that autoplay media with sound in order to minimize distractions on the web and conserve bandwidth.</span></span>  <span data-ttu-id="6af55-107">Пользователи могут настраивать поведение мультимедиа, используя глобальные элементы управления автозапуском и автозапуска.</span><span class="sxs-lookup"><span data-stu-id="6af55-107">Users can customize media behavior with both global and per-site autoplay controls.</span></span>  <span data-ttu-id="6af55-108">Кроме того, Microsoft Edge автоматически запускает автоматическое воспроизведение мультимедиа на фоновых вкладках.</span><span class="sxs-lookup"><span data-stu-id="6af55-108">Additionally, Microsoft Edge automatically suppresses autoplay of media in background tabs.</span></span>  

<span data-ttu-id="6af55-109">Дополнительные [сведения и рекомендации](./browser-features/autoplay-policies.md) по могут подробно ознакомиться с политиками автопроизведения.</span><span class="sxs-lookup"><span data-stu-id="6af55-109">Check out [Autoplay policies](./browser-features/autoplay-policies.md) for details and best practices to ensure a good user experience with media hosted on your site.</span></span>  

## <span data-ttu-id="6af55-110">Flash</span><span class="sxs-lookup"><span data-stu-id="6af55-110">Flash</span></span>  

<span data-ttu-id="6af55-111">Если на странице используется флэш-память, но пользователь не включил ее, Microsoft Edge обычно отображает значок круговой диаграммы в адресной строке.</span><span class="sxs-lookup"><span data-stu-id="6af55-111">If Flash is used on your page but the user has not enabled it, Microsoft Edge will normally show a puzzle piece icon in the address bar.</span></span>  <span data-ttu-id="6af55-112">Если элемент управления "Мелодия" динамически добавляется после загрузки страницы, значок пузырька может не отображаться, при этом потребуется проверить, загружен ли [Flash, и предоставить его отличное](./browser-features/flash.md) взаимодействие, если она не находится.</span><span class="sxs-lookup"><span data-stu-id="6af55-112">If you are dynamically adding the Flash control after the page is loaded, the puzzle icon may not display, in which case you'll want to [test if Flash is loaded and provide a graceful fallback experience](./browser-features/flash.md) if its not present.</span></span>  

## <span data-ttu-id="6af55-113">Режим чтения</span><span class="sxs-lookup"><span data-stu-id="6af55-113">Reading view</span></span>  

<span data-ttu-id="6af55-114">В Microsoft Edge [reading view](./browser-features/reading-view.md) имеется представление для чтения, чтобы упростить чтение веб-страниц, не отвлекаясь от несвязанных и другого содержимого на странице.</span><span class="sxs-lookup"><span data-stu-id="6af55-114">Microsoft Edge provides a [reading view](./browser-features/reading-view.md) for a more streamlined, book-like reading experience of webpages, without the distraction of unrelated or other secondary content on the page.</span></span>  <span data-ttu-id="6af55-115">Ниже приведены советы о том, как улучшить работу при чтении сайта и инструкции по изменению сайта.</span><span class="sxs-lookup"><span data-stu-id="6af55-115">Here are tips on how to ensure a great reading view experience with your site and also instructions for opting your site out of reading view.</span></span>  

## <span data-ttu-id="6af55-116">Обнаружение службы поиска</span><span class="sxs-lookup"><span data-stu-id="6af55-116">Search provider discovery</span></span>  

<span data-ttu-id="6af55-117">Интеграция с поддержкой поиска встроена в адресную строку Microsoft Edge, включая предложения для поиска, результаты из Интернета, журнал браузера и избранное.</span><span class="sxs-lookup"><span data-stu-id="6af55-117">Rich search integration is built into the Microsoft Edge address bar, including search suggestions, results from the web, your browsing history, and favorites.</span></span>  <span data-ttu-id="6af55-118">[Вот дополнительные сведения о поставщиках поиска, которые](./browser-features/search-provider-discovery.md) ищут службу поддержки Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6af55-118">[Here's more info for search providers](./browser-features/search-provider-discovery.md) looking to provide support for Microsoft Edge.</span></span>  
