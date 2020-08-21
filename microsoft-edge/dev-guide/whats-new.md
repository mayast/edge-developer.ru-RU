---
description: На этой странице представлен обзор новых возможностей предварительной версии браузера Microsoft EdgeHTML для разработчиков.
title: 'Новые возможности microsoft EdgeHTML для разработчиков: руководство для разработчиков'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, разработка веб-приложений, html, css, javascript, разработчик, разработчики, новые возможности в Edge, новых aPI в Edge, Edgehtml, edgehtml
ms.openlocfilehash: 81973d12f6e66b5e6f1c3cd6a12fee196c4495d7
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "10941962"
---
# <span data-ttu-id="8f43f-104">Что нового в EdgeHTML</span><span class="sxs-lookup"><span data-stu-id="8f43f-104">What's new in EdgeHTML</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="8f43f-105">Получайте новейшие функции и API-интерфейсы, стали участником [программы предварительной оценки Windows!](https://insider.windows.com)</span><span class="sxs-lookup"><span data-stu-id="8f43f-105">Get the latest EdgeHTML features and APIs by becoming a [Windows Insider](https://insider.windows.com)!</span></span>  <span data-ttu-id="8f43f-106">Программа [предварительной оценки Windows предоставляет](https://insider.windows.com) последние сборки Windows 10 сразу после их выхода.</span><span class="sxs-lookup"><span data-stu-id="8f43f-106">The [Windows Insider Program](https://insider.windows.com) provides the latest Windows 10 builds as soon as they're available.</span></span>  

<span data-ttu-id="8f43f-107">Чтобы ознакомиться с новыми функциями и интерфейсами aPI, публикованными в текущем выпуске платформы Microsoft Edge, начните использовать EdgeHTML 18 \(сборка 17763\). [Dev Guide](../dev-guide.md)</span><span class="sxs-lookup"><span data-stu-id="8f43f-107">Head over to the [Dev Guide](../dev-guide.md) to see the new features and APIs shipped in the current release of the Microsoft Edge platform, EdgeHTML 18 \(Build 17763\).</span></span>  

<span data-ttu-id="8f43f-108">Ниже описаны новые и обновленные API Edge HTML в предварительных сборках Для Windows 10.</span><span class="sxs-lookup"><span data-stu-id="8f43f-108">Below are new and updated EdgeHTML APIs in Windows 10 Preview Builds.</span></span> <span data-ttu-id="8f43f-109">Они указаны в `[interface name].[api name]` формате.</span><span class="sxs-lookup"><span data-stu-id="8f43f-109">They are listed in the format of `[interface name].[api name]`.</span></span>  <span data-ttu-id="8f43f-110">Полный список новых возможностей Microsoft Edge и [Changelog](https://developer.microsoft.com/microsoft-edge/platform/changelog) платформ см. в руководстве по разработке, чтобы увидеть новые функции и интерфейс API, публикованный в текущем стабильном выпуске платформы Microsoft Edge и EdgeHTML 18. [Dev Guide](../dev-guide.md)</span><span class="sxs-lookup"><span data-stu-id="8f43f-110">For a full list of new Microsoft Edge and platform features, check out [Changelog](https://developer.microsoft.com/microsoft-edge/platform/changelog) or head over to the [Dev Guide](../dev-guide.md) to see new features and APIs shipped in the current stable release of the Microsoft Edge platform, EdgeHTML 18.</span></span>   

> [!WARNING] 
> <span data-ttu-id="8f43f-111">Некоторые сведения связаны с предварительно опубликованным продуктом, которые могут быть значительно изменены до коммерческого выпуска.</span><span class="sxs-lookup"><span data-stu-id="8f43f-111">Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span>  <span data-ttu-id="8f43f-112">Майкрософт не дает никаких гарантий, явных или подразумеваемых, в отношении предоставленной здесь информации.</span><span class="sxs-lookup"><span data-stu-id="8f43f-112">Microsoft makes no warranties, express or implied, with respect to the information provided here.</span></span>  

## <span data-ttu-id="8f43f-113">Предварительная сборка 18272</span><span class="sxs-lookup"><span data-stu-id="8f43f-113">Preview Build 18272</span></span>  

<span data-ttu-id="8f43f-114">Не изменяется.</span><span class="sxs-lookup"><span data-stu-id="8f43f-114">No API changes.</span></span>  

## <span data-ttu-id="8f43f-115">Сборка 18267</span><span class="sxs-lookup"><span data-stu-id="8f43f-115">Preview Build 18267</span></span>  

<span data-ttu-id="8f43f-116">Не изменяется.</span><span class="sxs-lookup"><span data-stu-id="8f43f-116">No API changes.</span></span>  

## <span data-ttu-id="8f43f-117">Предварительная сборка 18262</span><span class="sxs-lookup"><span data-stu-id="8f43f-117">Preview Build 18262</span></span>  

<span data-ttu-id="8f43f-118">Добавлена поддержка API:</span><span class="sxs-lookup"><span data-stu-id="8f43f-118">Added new API support:</span></span>  

<iframe height='341' scrolling='no' title='<span data-ttu-id="8f43f-119">Сборка EdgeHTML Preview 17682</span><span class="sxs-lookup"><span data-stu-id="8f43f-119">EdgeHTML Preview Build 17682</span></span>' src='//codepen.io/MSEdgeDev/embed/5a691c1840690352f409d3788b8167fa/?height=341&theme-id=23761&default-tab=result&embed-version=2' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'><span data-ttu-id="8f43f-120">См. <a href='https://codepen.io/MSEdgeDev/pen/5a691c1840690352f409d3788b8167fa/'> сборку pen EdgeHTML Preview 17682 </a> на MSEdgeDev <a href='https://codepen.io/MSEdgeDev'> </a> (@MSEdgeDev) на <a href='https://codepen.io'> коде CodePen. </a></span><span class="sxs-lookup"><span data-stu-id="8f43f-120">See the Pen <a href='https://codepen.io/MSEdgeDev/pen/5a691c1840690352f409d3788b8167fa/'>EdgeHTML Preview Build 17682</a> by MSEdgeDev (<a href='https://codepen.io/MSEdgeDev'>@MSEdgeDev</a>) on <a href='https://codepen.io'>CodePen</a>.</span></span>  </iframe>  

## <span data-ttu-id="8f43f-121">Сборка 18252</span><span class="sxs-lookup"><span data-stu-id="8f43f-121">Preview Build 18252</span></span>  

<span data-ttu-id="8f43f-122">Не изменяется.</span><span class="sxs-lookup"><span data-stu-id="8f43f-122">No API changes.</span></span>  

## <span data-ttu-id="8f43f-123">Сборка 18247</span><span class="sxs-lookup"><span data-stu-id="8f43f-123">Preview Build 18247</span></span>  

<span data-ttu-id="8f43f-124">Не изменяется.</span><span class="sxs-lookup"><span data-stu-id="8f43f-124">No API changes.</span></span>  

## <span data-ttu-id="8f43f-125">Предварительная сборка 18242</span><span class="sxs-lookup"><span data-stu-id="8f43f-125">Preview Build 18242</span></span>  

<span data-ttu-id="8f43f-126">Не изменяется.</span><span class="sxs-lookup"><span data-stu-id="8f43f-126">No API changes.</span></span>  
