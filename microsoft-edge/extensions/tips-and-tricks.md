---
description: Ознакомьтесь со всеми полезными советами и приемами, относящимися к расширениям Microsoft Edge.
title: Расширения — советы и рекомендации
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/16/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: EDGE, веб-разработка, HTML, CSS, JavaScript, разработчик, расширения
ms.openlocfilehash: db15aa49649432a6c4400b4e6830501c40485a83
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571494"
---
# <span data-ttu-id="c9ca2-104">Советы и рекомендации</span><span class="sxs-lookup"><span data-stu-id="c9ca2-104">Tips and tricks</span></span>  

[!INCLUDE [deprecation-note](includes/deprecation-note.md)]  

<span data-ttu-id="c9ca2-105">Если вы работаете над расширением Microsoft EDGE или уже опубликовали их, может оказаться полезным использование указанных ниже советов и рекомендаций.</span><span class="sxs-lookup"><span data-stu-id="c9ca2-105">Whether you're currently working on a Microsoft Edge extension or have already published one, the following tips and tricks might come in handy.</span></span>

## <span data-ttu-id="c9ca2-106">Получить прямую ссылку на свое расширение в Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="c9ca2-106">Get a direct link to your extension in the Microsoft Store</span></span>
<span data-ttu-id="c9ca2-107">На информационной панели центра разработки для Windows вы можете найти прямую ссылку на свое расширение в Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="c9ca2-107">In the Windows Dev Center dashboard, you can find a direct link to your extension in the Microsoft Store.</span></span> <span data-ttu-id="c9ca2-108">Эта ссылка может быть полезной для рекламы и совместного использования вашего расширения.</span><span class="sxs-lookup"><span data-stu-id="c9ca2-108">This link can be useful for advertising and sharing out your extension.</span></span>


<span data-ttu-id="c9ca2-109">После входа в центр разработки для Windows и навигации по своему расширению через панель мониторинга на странице удостоверение приложения вы найдете ссылку в строке **связь протокола магазина** .</span><span class="sxs-lookup"><span data-stu-id="c9ca2-109">After logging in to the Windows Dev Center and navigating to your extension through the dashboard, on the App identity page you’ll find the link in the **Store protocol link** row:</span></span>

![связь с протоколом магазина](./media/store-link.png)
 
## <span data-ttu-id="c9ca2-111">Убедитесь в том, что вы подписаны на политику Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="c9ca2-111">Make sure you’re following the Microsoft Store Policy</span></span>
<span data-ttu-id="c9ca2-112">При создании расширения следует помнить о том, что вы помните о том, что нужно для отправки в магазин Майкрософт, выделенный в [политике Microsoft Store](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx).</span><span class="sxs-lookup"><span data-stu-id="c9ca2-112">When creating your extension, make sure you keep in mind the guidelines for submitting to the Microsoft Store highlighted in the [Microsoft Store Policy](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx).</span></span> 
 
<span data-ttu-id="c9ca2-113">У расширений Microsoft EDGE также есть дополнительный набор политик, которые нужно отслеживать [здесь](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx#pol_10_12).</span><span class="sxs-lookup"><span data-stu-id="c9ca2-113">Microsoft Edge extensions also have an additional set of policies to follow seen [here](https://msdn.microsoft.com/library/windows/apps/dn764944.aspx#pol_10_12).</span></span>

## <span data-ttu-id="c9ca2-114">Улучшение обнаруживаемости расширения в Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="c9ca2-114">Improve your extension’s discoverability in the Microsoft Store</span></span>

<span data-ttu-id="c9ca2-115">Вы можете добавлять ключевые слова к отправке расширения, чтобы imporove его обнаружение с помощью поиска.</span><span class="sxs-lookup"><span data-stu-id="c9ca2-115">You can add keywords to your extension submission to imporove its discoverability through searches.</span></span> <span data-ttu-id="c9ca2-116">Например, "расширения Microsoft Edge" и "имя расширения".</span><span class="sxs-lookup"><span data-stu-id="c9ca2-116">For example, "Microsoft Edge Extensions" and "name of my extension".</span></span> 

<span data-ttu-id="c9ca2-117">Это можно сделать в центре разработки для Windows в разделе Описание расширения.</span><span class="sxs-lookup"><span data-stu-id="c9ca2-117">This can be done in the Windows Dev Center under the description section of your extension.</span></span> <span data-ttu-id="c9ca2-118">Эти ключевые слова необходимо добавить для каждого языка, поддерживаемого расширением.</span><span class="sxs-lookup"><span data-stu-id="c9ca2-118">These keywords will need to be added for every language your extension supports.</span></span>

![Отправка ответа на рецензию](./media/keywords.png)

## <span data-ttu-id="c9ca2-120">Автоматизация отправки в Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="c9ca2-120">Automate your submission to the Microsoft Store</span></span>
<span data-ttu-id="c9ca2-121">Вы можете автоматизировать и ускорить отправку в Microsoft Store с помощью нового API отправки Microsoft Store, позволяющего обновлять приложения и игры, надстройки (покупки из приложения) и пакеты, которые продаются через API-интерфейс RESTFUL.</span><span class="sxs-lookup"><span data-stu-id="c9ca2-121">You can automate and streamline your submissions to the Microsoft Store by using the new Microsoft Store Submission API, which allows you to update apps/games, add-ons (in-app purchases), and package flights through a REST API.</span></span> <span data-ttu-id="c9ca2-122">Чтобы приступить к работе, ознакомьтесь с [документацией и примерами](https://docs.microsoft.com/windows/uwp/monetize/create-and-manage-submissions-using-windows-store-services) или используйте [расширение API отправки](https://github.com/Microsoft/windows-dev-center-vsts-extension) Open Source.</span><span class="sxs-lookup"><span data-stu-id="c9ca2-122">Check out the [documentation and samples](https://docs.microsoft.com/windows/uwp/monetize/create-and-manage-submissions-using-windows-store-services) or use the open source [Submission API VSTS extension](https://github.com/Microsoft/windows-dev-center-vsts-extension) to get started.</span></span>

## <span data-ttu-id="c9ca2-123">Использование центра обратной связи Windows для сбора запросов на отзыв и рецензии/функции</span><span class="sxs-lookup"><span data-stu-id="c9ca2-123">Use the Windows Feedback Hub to gather feedback/reviews/feature requests</span></span>

<span data-ttu-id="c9ca2-124">Вы можете направить пользователей в подкатегорию центра обратной связи Windows для расширения, внедрив ссылку, указывающую на нее.</span><span class="sxs-lookup"><span data-stu-id="c9ca2-124">You can direct users to the Windows Feedback Hub subcategory for your extension by embedding a link that points to it.</span></span> <span data-ttu-id="c9ca2-125">Эта ссылка должна быть создана в следующем формате:</span><span class="sxs-lookup"><span data-stu-id="c9ca2-125">This link will need to be created using the following format:</span></span> 

`feedback-hub://?tabid=2&appid=<PFN>!App`

<span data-ttu-id="c9ca2-126">Вам потребуется заменить `<PFN>` имя семейства пакетов расширением.</span><span class="sxs-lookup"><span data-stu-id="c9ca2-126">You will need to substitute `<PFN>` with the Package Family Name of you extension.</span></span> <span data-ttu-id="c9ca2-127">Это можно найти в разделе **удостоверение приложения** для вашего расширения в центре разработки для Windows.</span><span class="sxs-lookup"><span data-stu-id="c9ca2-127">This can be found under the **App identity** section for your extension in the Windows Dev Center.</span></span>

## <span data-ttu-id="c9ca2-128">Ознакомьтесь с оценками и рецензированием</span><span class="sxs-lookup"><span data-stu-id="c9ca2-128">Check out your ratings and reviews</span></span>
<span data-ttu-id="c9ca2-129">Регулярно выполняйте вход, чтобы проверить свои отзывы и оценки пользователей.</span><span class="sxs-lookup"><span data-stu-id="c9ca2-129">Log in regularly to check your user reviews and ratings.</span></span> <span data-ttu-id="c9ca2-130">Несмотря на то, что приложение UWP будет иметь только сведения о текущем рынке пользователей, при входе в центр разработки для Windows будет отображаться средняя оценка на всех рынках.</span><span class="sxs-lookup"><span data-stu-id="c9ca2-130">While the UWP app will only have info on the current user market, logging into the Windows Dev Center will display average rating across all markets.</span></span>

## <span data-ttu-id="c9ca2-131">Ответ на отзывы пользователей</span><span class="sxs-lookup"><span data-stu-id="c9ca2-131">Respond to user reviews</span></span>
<span data-ttu-id="c9ca2-132">Вы можете отвечать на отзывы пользователей в Microsoft Store с помощью панели мониторинга центра разработки для Windows.</span><span class="sxs-lookup"><span data-stu-id="c9ca2-132">You can respond to user reviews in the Microsoft Store through the Windows Dev Center's dashboard.</span></span> <span data-ttu-id="c9ca2-133">Перейдите к своему расширению и в разделе Аналитика выберите пункт **Рецензирование**.</span><span class="sxs-lookup"><span data-stu-id="c9ca2-133">Navigate to your extension and under Analytics select **Reviews**.</span></span> <span data-ttu-id="c9ca2-134">После каждой проверки появится ссылка, которая позволит вам отвечать непосредственно на этот клиент.</span><span class="sxs-lookup"><span data-stu-id="c9ca2-134">A link will appear underneath each review that will allow you to respond directly to the customer.</span></span> <span data-ttu-id="c9ca2-135">С помощью этого канала связи вы можете предложить отзыв, устранить проблемы или отправить нам благодарность за отзыв.</span><span class="sxs-lookup"><span data-stu-id="c9ca2-135">This channel of communication enables you to offer feedback, resolutions, or send a thank you for the review!</span></span>

![Отправка ответа на рецензию](./media/reviews.png)
