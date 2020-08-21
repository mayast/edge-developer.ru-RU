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
# Представления DateTime и TimeSpan среды выполнения Windows  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Представление JavaScript для дат ы и времени отличается от версии Windows Runtime.  Структура [даты и времени][UwpWindowsFoundationDatetime] выполнения Windows представлена в javaScript как [дата,][MDNDate] в котором в строгом хранилище входит в обратный хранилище, соответствующий `DateTime` данным \(и имеет другой диапазон и точности JavaScript `Date` \).  При изменении `Date` настраиваемого объекта он становится стандартной точности JavaScript и `Date` потери.  Значения JavaScript можно перенести в windows Runtime и проверяться диапазоном, что может приводить к возникновению исключений `Date` `DateTime` в полях.  

 Структура Windows Runtime [TimeSpan][UwpWindowsFoundationTimespan] преобразуется в миллисекунды и возвращается как номер JavaScript.  

## См. также  

[Использование среды выполнения Windows в JavaScript][WindowsRuntimeJavascript]  

<!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Использование Windows Runtime в JavaScript | Документы Майкрософт"  

[UwpWindowsFoundationDatetime]: /uwp/api/Windows.Foundation.DateTime "DateTime Struct | Документы Майкрософт"  
[UwpWindowsFoundationTimespan]: /uwp/api/windows.foundation.timespan "Структура TimeSpan Struct | Документы Майкрософт"  

[MDNDate]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Date "Дата | MDN"  
