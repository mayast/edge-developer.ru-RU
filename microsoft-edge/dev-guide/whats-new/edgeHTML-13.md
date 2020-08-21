---
description: На этой странице представлен обзор новых возможностей Microsoft EdgeHTML 13.
title: Новые функции и API в Microsoft EdgeHTML 13
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, разработчики, html, css, javascript, разработчики
ms.openlocfilehash: 033b8dacb107492624f3b8c7775a47285c9893dd
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "10941912"
---
# <span data-ttu-id="dd7b0-104">Новые возможности В EdgeHTML 13</span><span class="sxs-lookup"><span data-stu-id="dd7b0-104">What's new in EdgeHTML 13</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="dd7b0-105">Ниже перечислены изменения, пытаемые вместе с Браузером Microsoft Edge HTML 13, технологичным способом, который модуль Microsoft Edge в первом [обновлении](https://blogs.windows.com/windowsexperience/2015/11/12) Windows 10 \(11.11.2015, сборка 10586\).</span><span class="sxs-lookup"><span data-stu-id="dd7b0-105">Here are the changes shipped with EdgeHTML 13, the engine powering the Microsoft Edge browser in the [first major update](https://blogs.windows.com/windowsexperience/2015/11/12) for Windows 10 \(11/2015, Build 10586\).</span></span>  <span data-ttu-id="dd7b0-106">Обзор изменений общего браузера Microsoft Edge см. в статье ["Знакомство с Microsoft EdgeHTML 13, нашем первоначальномплатформе microsoft Edge.](https://blogs.windows.com/msedgedev/2015/11/16)</span><span class="sxs-lookup"><span data-stu-id="dd7b0-106">For an overview of changes to the overall Microsoft Edge browser, see [Introducing EdgeHTML 13, our first platform update for Microsoft Edge](https://blogs.windows.com/msedgedev/2015/11/16).</span></span>  

<span data-ttu-id="dd7b0-107">Вот как и вот такая перечень изменений. [https://aka.ms/devguide_edgehtml_13](./edgehtml-13.md)</span><span class="sxs-lookup"><span data-stu-id="dd7b0-107">Here's the permalink for the following list of changes:  [https://aka.ms/devguide_edgehtml_13](./edgehtml-13.md).</span></span>  

## <span data-ttu-id="dd7b0-108">Возможности</span><span class="sxs-lookup"><span data-stu-id="dd7b0-108">Features</span></span>  

### <span data-ttu-id="dd7b0-109">CSS</span><span class="sxs-lookup"><span data-stu-id="dd7b0-109">CSS</span></span>  

<span data-ttu-id="dd7b0-110">EdgeHTML 13 поддерживает новые возможности CSS, включая следующие:</span><span class="sxs-lookup"><span data-stu-id="dd7b0-110">EdgeHTML 13 supports new CSS features, including:</span></span>  

*   [<span data-ttu-id="dd7b0-111">Классы CSS mutability Pseudo-Class-class-class-classes</span><span class="sxs-lookup"><span data-stu-id="dd7b0-111">CSS Mutability Pseudo-classes</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/cssmutabilitypseudoclasses)  
*   [<span data-ttu-id="dd7b0-112">CSS Range Pseudo-classes</span><span class="sxs-lookup"><span data-stu-id="dd7b0-112">CSS Range Pseudo-classes</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/cssrangepseudoclasses)  
*   <span data-ttu-id="dd7b0-113">При настройке и [избавлении ключевых слов](https://developer.microsoft.com/microsoft-edge/platform/status/cssinitialvalue) CSS [unset](https://developer.microsoft.com/microsoft-edge/platform/status/cssunsetvalue)</span><span class="sxs-lookup"><span data-stu-id="dd7b0-113">CSS [initial](https://developer.microsoft.com/microsoft-edge/platform/status/cssinitialvalue) and [unset](https://developer.microsoft.com/microsoft-edge/platform/status/cssunsetvalue) keywords</span></span>  

### <span data-ttu-id="dd7b0-114">Зашифрованные расширения мультимедиа</span><span class="sxs-lookup"><span data-stu-id="dd7b0-114">Encrypted Media Extensions</span></span>  

<span data-ttu-id="dd7b0-115">Теперь Microsoft Edge теперь поддерживает новые API непрефиксированных зашифрованных оболочки [мультимедиа.](https://w3.org/TR/encrypted-media)</span><span class="sxs-lookup"><span data-stu-id="dd7b0-115">Microsoft Edge now supports the new unprefixed [Encrypted Media Extensions](https://w3.org/TR/encrypted-media) APIs.</span></span>  <span data-ttu-id="dd7b0-116">Зашифрованные расширения мультимедиа \(EME\) расширяют элементы видео и звуковых данных, чтобы включить защиту содержимого без использования подключаемого модуля.  Дополнительные сведения о EME: [зашифрованные расширения мультимедиа.](https://developer.mozilla.org/docs/Web/API/Encrypted_Media_Extensions_API)</span><span class="sxs-lookup"><span data-stu-id="dd7b0-116">Encrypted Media Extensions \(EME\) extends the video and audio elements to enable Digital Rights Management \(DRM\) protected content without using plug-ins.  Read more about EME:  [Encrypted Media Extensions](https://developer.mozilla.org/docs/Web/API/Encrypted_Media_Extensions_API).</span></span>  

### <span data-ttu-id="dd7b0-117">Графика</span><span class="sxs-lookup"><span data-stu-id="dd7b0-117">Graphics</span></span>  

<span data-ttu-id="dd7b0-118">EdgeHTML 13 содержит следующие обновления графических элементов:</span><span class="sxs-lookup"><span data-stu-id="dd7b0-118">EdgeHTML 13 introduces the following graphics updates:</span></span>  

*   [<span data-ttu-id="dd7b0-119">Холлст</span><span class="sxs-lookup"><span data-stu-id="dd7b0-119">Canvas ellipse</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/canvas2dellipse)  
*   [<span data-ttu-id="dd7b0-120">Модели ломаны</span><span class="sxs-lookup"><span data-stu-id="dd7b0-120">Canvas blending modes</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/compositingandblendingincanvas2d)  
*   [<picture> <span data-ttu-id="dd7b0-121">элемент</span><span class="sxs-lookup"><span data-stu-id="dd7b0-121">element</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/pictureelement)  
*   [<span data-ttu-id="dd7b0-122">Внешний контент SVG</span><span class="sxs-lookup"><span data-stu-id="dd7b0-122">SVG external content</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/svgexternalcontent)  

### <span data-ttu-id="dd7b0-123">JavaScript</span><span class="sxs-lookup"><span data-stu-id="dd7b0-123">JavaScript</span></span>  

<span data-ttu-id="dd7b0-124">EdgeHTML 13 содержит основные улучшения и новые возможности поддержки [в Какра,](https://blogs.windows.com/msedgedev/2015/09/30)включая переключатель JavaScript, работает на диске, включая следующие:</span><span class="sxs-lookup"><span data-stu-id="dd7b0-124">EdgeHTML 13 includes [major improvements and new feature support in Chakra](https://blogs.windows.com/msedgedev/2015/09/30), the JavaScript engine powering Microsoft Edge, including:</span></span>  

#### <span data-ttu-id="dd7b0-125">Новые возможности</span><span class="sxs-lookup"><span data-stu-id="dd7b0-125">New features</span></span>  

<span data-ttu-id="dd7b0-126">Включено по умолчанию</span><span class="sxs-lookup"><span data-stu-id="dd7b0-126">On by default</span></span>  

*   <span data-ttu-id="dd7b0-127">[asm.js](https://developer.microsoft.com/microsoft-edge/platform/status/asmjs/?q=asm.js) по умолчанию (запись[блога),](https://blogs.windows.com/msedgedev/2015/11/10) [демонстрация \.](https://dev.windows.com/microsoft-edge/testdrive/demos/chess)</span><span class="sxs-lookup"><span data-stu-id="dd7b0-127">[asm.js](https://developer.microsoft.com/microsoft-edge/platform/status/asmjs/?q=asm.js) enabled by default \([blog post](https://blogs.windows.com/msedgedev/2015/11/10), [demo](https://dev.windows.com/microsoft-edge/testdrive/demos/chess)\)</span></span>  
*   <span data-ttu-id="dd7b0-128">[Классы](https://developer.microsoft.com/microsoft-edge/platform/status/asmjs/?q=classes) \(ES2015\)</span><span class="sxs-lookup"><span data-stu-id="dd7b0-128">[Classes](https://developer.microsoft.com/microsoft-edge/platform/status/asmjs/?q=classes) \(ES2015\)</span></span>  

#### <span data-ttu-id="dd7b0-129">Экспертные функции JavaScript</span><span class="sxs-lookup"><span data-stu-id="dd7b0-129">Experimental JavaScript features</span></span>  

<span data-ttu-id="dd7b0-130">Доступно с</span><span class="sxs-lookup"><span data-stu-id="dd7b0-130">Enabled with</span></span> `about:flags`  

*   <span data-ttu-id="dd7b0-131">[Функции асинхронизации](https://developer.microsoft.com/microsoft-edge/platform/status/asyncfunctions/?q=async%20functions) \(ES2016\)</span><span class="sxs-lookup"><span data-stu-id="dd7b0-131">[Async functions](https://developer.microsoft.com/microsoft-edge/platform/status/asyncfunctions/?q=async%20functions) \(ES2016\)</span></span>  
*   <span data-ttu-id="dd7b0-132">[Оператор экспоненциального оператора](https://developer.microsoft.com/microsoft-edge/platform/status/exponentiationoperatores2016/?q=exponentiation%20operator) \(ES2016\)</span><span class="sxs-lookup"><span data-stu-id="dd7b0-132">[Exponentiation operator](https://developer.microsoft.com/microsoft-edge/platform/status/exponentiationoperatores2016/?q=exponentiation%20operator) \(ES2016\)</span></span>  
*   <span data-ttu-id="dd7b0-133">[Разработка](https://developer.microsoft.com/microsoft-edge/platform/status/destructuringES2015/?q=destructuring) \(ES2015\)</span><span class="sxs-lookup"><span data-stu-id="dd7b0-133">[Destructuring](https://developer.microsoft.com/microsoft-edge/platform/status/destructuringES2015/?q=destructuring) \(ES2015\)</span></span>  

### <span data-ttu-id="dd7b0-134">Ввод пользователя</span><span class="sxs-lookup"><span data-stu-id="dd7b0-134">User Input</span></span>  

<span data-ttu-id="dd7b0-135">В Microsoft EdgeHTML 13 появилась возможность ввода пользователей:</span><span class="sxs-lookup"><span data-stu-id="dd7b0-135">The following features introduced in EdgeHTML 13 improve user input:</span></span>  

*   [<meter> <span data-ttu-id="dd7b0-136">элемент</span><span class="sxs-lookup"><span data-stu-id="dd7b0-136">element</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/meterelement)  
*   [<span data-ttu-id="dd7b0-137">oninvalid event обработчик событий для документа и окна</span><span class="sxs-lookup"><span data-stu-id="dd7b0-137">oninvalid event handler for the element document and window</span></span>](https://developer.microsoft.com/microsoft-edge/platform/status/oninvalideventhandler)  

### <span data-ttu-id="dd7b0-138">Блокировка указате</span><span class="sxs-lookup"><span data-stu-id="dd7b0-138">Pointer Lock</span></span>  

<span data-ttu-id="dd7b0-139">Теперь Microsoft Edge теперь поддерживает API блокировки указателя \(ранее называемая блокировка мыши\) для доступа к неперемещаемому перемещению, блокировке целевого элемента, уберение пределов продолжения перемещения в одном направлении и удаление курсора из вида.</span><span class="sxs-lookup"><span data-stu-id="dd7b0-139">Microsoft Edge now supports the Pointer Lock API \(previously called Mouse Lock\) for access to raw mouse movement, locking the target of mouse events to a single element, eliminating limits of how far mouse movement can go in a single direction, and removing the cursor from view.</span></span>  

## <span data-ttu-id="dd7b0-140">Новые API в Microsoft EdgeHTML 13</span><span class="sxs-lookup"><span data-stu-id="dd7b0-140">New APIs in EdgeHTML 13</span></span>  

<span data-ttu-id="dd7b0-141">Ниже приведен полный список новых aPI в Microsoft EdgeHTML 13.</span><span class="sxs-lookup"><span data-stu-id="dd7b0-141">Here's the full list of new APIs in EdgeHTML 13.</span></span>  <span data-ttu-id="dd7b0-142">Они указаны в `[interface name].[api name]` формате.</span><span class="sxs-lookup"><span data-stu-id="dd7b0-142">They are listed in the format of `[interface name].[api name]`.</span></span>  

<iframe height='584' scrolling='no' title='<span data-ttu-id="dd7b0-143">Новые API в Microsoft EdgeHTML 13</span><span class="sxs-lookup"><span data-stu-id="dd7b0-143">New APIs in EdgeHTML 13</span></span>' src='//codepen.io/MicrosoftEdgeDocumentation/embed/vmzxEY/?height=584&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width:  100%;'><span data-ttu-id="dd7b0-144">См. раздел <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/vmzxEY/'> "Новые API" в Microsoft EdgeHTML 13 </a> с помощью приложений Microsoft Edge <a href='http://codepen.io/MicrosoftEdgeDocumentation'> </a> (@MicrosoftEdgeDocumentation) на <a href='http://codepen.io'> коде </a> кода.</span><span class="sxs-lookup"><span data-stu-id="dd7b0-144">See the Pen <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/vmzxEY/'>New APIs in EdgeHTML 13</a> by Microsoft Edge Docs (<a href='http://codepen.io/MicrosoftEdgeDocumentation'>@MicrosoftEdgeDocumentation</a>) on <a href='http://codepen.io'>CodePen</a>.</span></span></iframe>  
