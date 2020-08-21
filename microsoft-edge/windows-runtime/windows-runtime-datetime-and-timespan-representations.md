---
title: Представления DateTime и TimeSpan среды выполнения Windows
ms.custom: ''
ms.date: 07/29/2020
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.technology: windows-integration
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime dates and times
- TimeSpan [JavaScript]
- DateTime [JavaScript]
ms.assetid: 9743e9ac-9054-463e-8264-427183e4905f
caps.latest.revision: 9
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 1c51bba74bb7e5182eb25342badcae848eeba339
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942057"
---
# <span data-ttu-id="06c81-102">Представления DateTime и TimeSpan среды выполнения Windows</span><span class="sxs-lookup"><span data-stu-id="06c81-102">Windows Runtime DateTime and TimeSpan representations</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="06c81-103">Представление JavaScript для дат ы и времени отличается от версии Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="06c81-103">The JavaScript representation of dates and times is different from the Windows Runtime version.</span></span>  <span data-ttu-id="06c81-104">Структура [даты и времени][UwpWindowsFoundationDatetime] выполнения Windows представлена в javaScript как [дата,][MDNDate] в котором в строгом хранилище входит в обратный хранилище, соответствующий `DateTime` данным \(и имеет другой диапазон и точности JavaScript `Date` \).</span><span class="sxs-lookup"><span data-stu-id="06c81-104">The Windows Runtime [DateTime][UwpWindowsFoundationDatetime] structure is represented in JavaScript as a [Date][MDNDate] that has a backing store that matches the `DateTime` data \(and has a different range and precision from the JavaScript `Date`\).</span></span>  <span data-ttu-id="06c81-105">При изменении `Date` настраиваемого объекта он становится стандартной точности JavaScript и `Date` потери.</span><span class="sxs-lookup"><span data-stu-id="06c81-105">If you modify this custom `Date` object, it becomes a standard JavaScript `Date` and loses precision.</span></span>  <span data-ttu-id="06c81-106">Значения JavaScript можно перенести в windows Runtime и проверяться диапазоном, что может приводить к возникновению исключений `Date` `DateTime` в полях.</span><span class="sxs-lookup"><span data-stu-id="06c81-106">JavaScript `Date` values can be passed to a Windows Runtime `DateTime` and will be range-checked, which might result in marshaling exceptions.</span></span>  

 <span data-ttu-id="06c81-107">Структура Windows Runtime [TimeSpan][UwpWindowsFoundationTimespan] преобразуется в миллисекунды и возвращается как номер JavaScript.</span><span class="sxs-lookup"><span data-stu-id="06c81-107">The Windows Runtime [TimeSpan][UwpWindowsFoundationTimespan] structure is converted to milliseconds and returned as a JavaScript number.</span></span>  

## <span data-ttu-id="06c81-108">См. также</span><span class="sxs-lookup"><span data-stu-id="06c81-108">See also</span></span>  

[<span data-ttu-id="06c81-109">Использование среды выполнения Windows в JavaScript</span><span class="sxs-lookup"><span data-stu-id="06c81-109">Using the Windows Runtime in JavaScript</span></span>][WindowsRuntimeJavascript]  

<!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Использование Windows Runtime в JavaScript | Документы Майкрософт"  

[UwpWindowsFoundationDatetime]: /uwp/api/Windows.Foundation.DateTime "DateTime Struct | Документы Майкрософт"  
[UwpWindowsFoundationTimespan]: /uwp/api/windows.foundation.timespan "Структура TimeSpan Struct | Документы Майкрософт"  

[MDNDate]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Date "Дата | MDN"  
