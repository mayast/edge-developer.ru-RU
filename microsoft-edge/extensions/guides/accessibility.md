---
ms.assetid: c4544a19-de78-4c69-a042-c0415726548f
description: Чтобы значок расширения отображался в светлых и темных режимах, следуйте рекомендациям по специальным возможностям.
title: Расширения — специальные возможности
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/16/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: EDGE, веб-разработка, HTML, CSS, JavaScript, разработчик
ms.openlocfilehash: 514e68fc1b797a28c76bda79c8fab88b4ea2216c
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571595"
---
# <span data-ttu-id="01ed1-104">Специальные возможности</span><span class="sxs-lookup"><span data-stu-id="01ed1-104">Accessibility</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

## <span data-ttu-id="01ed1-105">Создание специальных значков расширения для Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="01ed1-105">Creating accessible extension icons for Microsoft Edge</span></span>

<span data-ttu-id="01ed1-106">Сторонним разработчикам расширений рекомендуется использовать ресурсы изображений, которые удовлетворяют требованиям Microsoft к специальным возможностям специальных возможностей, так что значки четко видны как для светлых, так и для темных тем.</span><span class="sxs-lookup"><span data-stu-id="01ed1-106">Third-party extension developers are encouraged to use image assets that meet Microsoft’s strict accessibility requirements so that icons are clearly visible for both light and dark themes.</span></span> <span data-ttu-id="01ed1-107">Рекомендуется, чтобы все значки расширений имели отношение 14:1 между цветом фона значка и главным цветом самого значка.</span><span class="sxs-lookup"><span data-stu-id="01ed1-107">We recommend that all extension icons have a 14:1 ratio between the icon’s background color and the dominant color of the icon itself.</span></span>


<span data-ttu-id="01ed1-108">Расширения, разработанные корпорацией Майкрософт, применяют визуальную обработку наклейок, чтобы удовлетворить этим требованиям.</span><span class="sxs-lookup"><span data-stu-id="01ed1-108">First-party extensions developed by Microsoft apply a “stickering” visual treatment to satisfy these requirements.</span></span>

### <span data-ttu-id="01ed1-109">Примеры "наклейка"</span><span class="sxs-lookup"><span data-stu-id="01ed1-109">Examples of the "stickering"</span></span>

<span data-ttu-id="01ed1-110">Основной задачей "наклейка" является создание визуального доступа к значку на любом цвете фона.</span><span class="sxs-lookup"><span data-stu-id="01ed1-110">The main goal of “stickering” is to make the icon visually accessible on any background color.</span></span> <span data-ttu-id="01ed1-111">Рекомендуемый цветовой коэффициент между белым внешним росчерком и Вашим значком должен быть 14:1 для поддержки высокой контрастности.</span><span class="sxs-lookup"><span data-stu-id="01ed1-111">The recommended color ratio between the white outer stroke and your icon should be 14:1 to support the high contrast requirements.</span></span>

#### <span data-ttu-id="01ed1-112">Значок "хорошо"</span><span class="sxs-lookup"><span data-stu-id="01ed1-112">Good icon</span></span>
<span data-ttu-id="01ed1-113">С помощью наклейки, в основном, значок темного цвета будет отображаться на любом фоне.</span><span class="sxs-lookup"><span data-stu-id="01ed1-113">With stickering, a primarily dark icon will remain visible on any background color.</span></span>


![изображение значка, отображаемого на любом цвете фона](./../media/accessibility-light-to-dark-good.png)

#### <span data-ttu-id="01ed1-115">Неверный значок</span><span class="sxs-lookup"><span data-stu-id="01ed1-115">Bad icon</span></span>
<span data-ttu-id="01ed1-116">Если вы не научитесь работать с наклейками, значок может быть недоступен в фоновом режиме, и его невозможно будет увидеть.</span><span class="sxs-lookup"><span data-stu-id="01ed1-116">Without stickering, an icon could blend in with the background and become impossible to see.</span></span>


![изображение значка, накладываемого на черный фон](./../media/accessibility-light-to-dark-bad.png)

### <span data-ttu-id="01ed1-118">Значок расширения "наклейка"</span><span class="sxs-lookup"><span data-stu-id="01ed1-118">"Stickering" your extension icon</span></span>

<span data-ttu-id="01ed1-119">Следующие пять шагов описывают предлагаемый метод создания значка расширения, который отвечает требованиям Microsoft по специальным возможностям.</span><span class="sxs-lookup"><span data-stu-id="01ed1-119">The following five steps outline the suggested method of creating an extension icon that meets Microsoft’s accessibility requirements:</span></span>


| <span data-ttu-id="01ed1-120">Шаг 1</span><span class="sxs-lookup"><span data-stu-id="01ed1-120">Step 1</span></span>                                       | <span data-ttu-id="01ed1-121">Шаг 2</span><span class="sxs-lookup"><span data-stu-id="01ed1-121">Step 2</span></span>                                       | <span data-ttu-id="01ed1-122">Шаг 3</span><span class="sxs-lookup"><span data-stu-id="01ed1-122">Step 3</span></span>                                                                                 | <span data-ttu-id="01ed1-123">Шаг 4</span><span class="sxs-lookup"><span data-stu-id="01ed1-123">Step 4</span></span>                                                                          | <span data-ttu-id="01ed1-124">Шаг5</span><span class="sxs-lookup"><span data-stu-id="01ed1-124">Step 5</span></span>                                                       |
|:---------------------------------------------|:---------------------------------------------|:---------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------|:-------------------------------------------------------------|
| <span data-ttu-id="01ed1-125">Настройка значка в заданной сетке.</span><span class="sxs-lookup"><span data-stu-id="01ed1-125">Set your icon within your specified grid.</span></span>    | <span data-ttu-id="01ed1-126">Уменьшите размер значка на 2 точки.</span><span class="sxs-lookup"><span data-stu-id="01ed1-126">Reduce your icon size by 2 pixels.</span></span>           | <span data-ttu-id="01ed1-127">Скопируйте значок и вставьте его на место.</span><span class="sxs-lookup"><span data-stu-id="01ed1-127">Copy your icon and paste in place.</span></span> <span data-ttu-id="01ed1-128">Создание внешнего росчерка на 2 пиксела с закругленными углами.</span><span class="sxs-lookup"><span data-stu-id="01ed1-128">Create a 2 pixel outer stroke with rounded corners.</span></span> | <span data-ttu-id="01ed1-129">Обводка, выпустите составной контур и объедините оставшиеся фигуры.</span><span class="sxs-lookup"><span data-stu-id="01ed1-129">Outline your stroke, release the compound path, and merge the remaining shapes.</span></span> | <span data-ttu-id="01ed1-130">Отцветировать внешний росчерк и внутренний значок обводки по своему усмотрению.</span><span class="sxs-lookup"><span data-stu-id="01ed1-130">Color the outer stroke white and the inner icon as you wish.</span></span> |
| ![step1](./../media/accessibility-step1.png) | ![step2](./../media/accessibility-step2.png) | ![step3](./../media/accessibility-step3.png)                                           | ![step4](./../media/accessibility-step4.png)                                    | ![step5](./../media/accessibility-step5.png)                 |

