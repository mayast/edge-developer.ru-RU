---
description: Использование вычисляемой области для понимания того, как вычисляются каскадные и вычисляемые элементы CSS в элементах страницы
title: DevTools-вычисляемые элементы
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/10/2017
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, элементы, CSS, вычисляемое значение, модель Box
ms.custom: seodec18
ms.openlocfilehash: c7b1b7c86f30e6947442c9b3d0e8856074ce4c8e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572549"
---
# <span data-ttu-id="8fb84-104">Вычисленное</span><span class="sxs-lookup"><span data-stu-id="8fb84-104">Computed</span></span>

<span data-ttu-id="8fb84-105">Просмотр схемы модели полей (ширина, заполнение, границы, поля и смещение) выбранного элемента.</span><span class="sxs-lookup"><span data-stu-id="8fb84-105">See a box model diagram (width, padding, border, margin and offset values) of the selected element.</span></span> <span data-ttu-id="8fb84-106">Если вы включите инструмент **выделения элементов** ( `Ctrl+Shift+L` ), то те же цветовые области на схеме (для ширины, заполнения и т. д.) будут накладываться на отображаемый элемент, когда вы выбираете его на странице.</span><span class="sxs-lookup"><span data-stu-id="8fb84-106">If you turn on the **Element highlighting** tool (`Ctrl+Shift+L`), the same colored regions in the diagram (for width, padding, etc.) that will overlay the rendered element when you select it on the page.</span></span> <span data-ttu-id="8fb84-107">Вы можете изменить любое значение на диаграмме, щелкнув его.</span><span class="sxs-lookup"><span data-stu-id="8fb84-107">You can edit any value in the diagram by clicking it.</span></span> 

<span data-ttu-id="8fb84-108">Под схемой модель Box можно создать фильтруемый и редактируемый список свойств вычисляемого стиля.</span><span class="sxs-lookup"><span data-stu-id="8fb84-108">Below the box model diagram is a filterable and editable list of computed style properties.</span></span> <span data-ttu-id="8fb84-109">Отключение активного в данный момент свойства активирует свойство Next в Cascade, если оно существует.</span><span class="sxs-lookup"><span data-stu-id="8fb84-109">Turning off a currently active property activates the next property in the cascade, if one exists.</span></span> <span data-ttu-id="8fb84-110">Вы можете просматривать изменения на панели " [**изменения**](./changes.md) ".</span><span class="sxs-lookup"><span data-stu-id="8fb84-110">You can view your changes in the [**Changes**](./changes.md) pane.</span></span>

<span data-ttu-id="8fb84-111">По умолчанию кнопка **Показать только стили пользователей** включена.</span><span class="sxs-lookup"><span data-stu-id="8fb84-111">The **Display user styles only** button is on by default.</span></span> <span data-ttu-id="8fb84-112">При нажатии кнопки будут вычислены стили из *стандартной таблицы стилей* Microsoft EDGE в списке "вычисляемые стили".</span><span class="sxs-lookup"><span data-stu-id="8fb84-112">Depressing the button will include styles from the *default stylesheet* of Microsoft Edge in the computed styles list.</span></span>

![Вычисляемая область](../media/elements_computed.png)