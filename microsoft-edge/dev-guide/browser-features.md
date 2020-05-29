---
ms.assetid: 4d3fa934-4fa8-4c02-b9b5-88506c76baac
description: Руководство по функциям браузера в Microsoft Edge.
title: 'Руководство для разработчиков: браузер'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 11/28/2018
ms.topic: article
ms.prod: microsoft-edge
keywords: EDGE, веб-разработка, HTML, CSS, JavaScript, разработчик
ms.openlocfilehash: e7b13b18048e0a703ca5e2a0e5b52712f41c2101
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10570905"
---
# <span data-ttu-id="97bd1-104">Возможности браузера</span><span class="sxs-lookup"><span data-stu-id="97bd1-104">Browser features</span></span>

## <span data-ttu-id="97bd1-105">Политики автозапуска</span><span class="sxs-lookup"><span data-stu-id="97bd1-105">Autoplay policies</span></span>

 <span data-ttu-id="97bd1-106">Microsoft Edge предоставляет пользователям возможность персонализировать настройки браузера на веб-сайтах, которые перезапускают мультимедиа с помощью звука, чтобы свести к минимуму количество отвлекающих на веб-сайте и экономить пропускную способность.</span><span class="sxs-lookup"><span data-stu-id="97bd1-106">Microsoft Edge provides customers with the ability to personalize their browsing preferences on websites that autoplay media with sound in order to minimize distractions on the web and conserve bandwidth.</span></span> <span data-ttu-id="97bd1-107">Пользователи могут настраивать поведение мультимедиа как для глобальных, так и для отдельных элементов управления автозапуска.</span><span class="sxs-lookup"><span data-stu-id="97bd1-107">Users can customize media behavior with both global and per-site autoplay controls.</span></span> <span data-ttu-id="97bd1-108">Кроме того, Microsoft EDGE автоматически запрещает Автозапуск мультимедиа в закладках на фоне.</span><span class="sxs-lookup"><span data-stu-id="97bd1-108">Additionally, Microsoft Edge automatically suppresses autoplay of media in background tabs.</span></span>

<span data-ttu-id="97bd1-109">Изучите [политики автозапуска](./browser-features/autoplay-policies.md) и ознакомьтесь с подробными сведениями и рекомендациями по обеспечению удобного взаимодействия пользователя с мультимедиа, размещенным на вашем сайте.</span><span class="sxs-lookup"><span data-stu-id="97bd1-109">Check out [Autoplay policies](./browser-features/autoplay-policies.md) for details and best practices to ensure a good user experience with media hosted on your site.</span></span>

## <span data-ttu-id="97bd1-110">Вспышка</span><span class="sxs-lookup"><span data-stu-id="97bd1-110">Flash</span></span>
<span data-ttu-id="97bd1-111">Если на странице используется Flash, но пользователь не включил его, то Microsoft Edge обычно отображает в адресной строке значок "фрагмент головоломки".</span><span class="sxs-lookup"><span data-stu-id="97bd1-111">If Flash is used on your page but the user has not enabled it, Microsoft Edge will normally show a puzzle piece icon in the address bar.</span></span> <span data-ttu-id="97bd1-112">Если вы динамически добавляете элемент управления Flash после загрузки страницы, значок головоломки может не отображаться, в этом случае вы захотите [проверить, загружено ли приложение Flash, и обеспечить корректное](./browser-features/flash.md) использование, если оно не отображается.</span><span class="sxs-lookup"><span data-stu-id="97bd1-112">If you are dynamically adding the Flash control after the page is loaded, the puzzle icon may not display, in which case you'll want to [test if Flash is loaded and provide a graceful fallback experience](./browser-features/flash.md) if its not present.</span></span>

## <span data-ttu-id="97bd1-113">Режим чтения</span><span class="sxs-lookup"><span data-stu-id="97bd1-113">Reading view</span></span>
<span data-ttu-id="97bd1-114">Microsoft Edge предоставляет [представление для чтения](./browser-features/reading-view.md) для более удобной работы с веб-страницами, так же как и без отзыва несвязанных или других вспомогательных материалов на странице.</span><span class="sxs-lookup"><span data-stu-id="97bd1-114">Microsoft Edge provides a [reading view](./browser-features/reading-view.md) for a more streamlined, book-like reading experience of webpages, without the distraction of unrelated or other secondary content on the page.</span></span> <span data-ttu-id="97bd1-115">Здесь вы найдете советы о том, как обеспечить удобную работу с представлением для чтения на сайте, а также инструкции по отказаться от просмотра на вашем сайте из режима чтения.</span><span class="sxs-lookup"><span data-stu-id="97bd1-115">Here are tips on how to ensure a great reading view experience with your site and also instructions for opting your site out of reading view.</span></span>

## <span data-ttu-id="97bd1-116">Обнаружение поставщика поиска</span><span class="sxs-lookup"><span data-stu-id="97bd1-116">Search provider discovery</span></span>

<span data-ttu-id="97bd1-117">Расширенная интеграция поиска встроена в адресную строку Microsoft EDGE, в том числе варианты поиска, результаты из Интернета, журнал браузера и Избранное.</span><span class="sxs-lookup"><span data-stu-id="97bd1-117">Rich search integration is built into the Microsoft Edge address bar, including search suggestions, results from the web, your browsing history, and favorites.</span></span> <span data-ttu-id="97bd1-118">[Ниже приведены дополнительные сведения о службах поиска](./browser-features/search-provider-discovery.md) , которые необходимы для поддержки Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="97bd1-118">[Here's more info for search providers](./browser-features/search-provider-discovery.md) looking to provide support for Microsoft Edge.</span></span>
