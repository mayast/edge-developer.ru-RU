---
title: Представления DateTime и TimeSpan среды выполнения Windows
ms.custom: ''
ms.date: 04/01/2020
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
ms.openlocfilehash: d3e138493b80face1238118a99c03f6015a6a8ef
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572842"
---
# Представления DateTime и TimeSpan среды выполнения Windows  

Представление даты и времени в JavaScript отличается от версии среды выполнения Windows.  Структура [DateTime][UwpWindowsFoundationDatetime] среды выполнения Windows представлена в JavaScript как [дату][MDNDate] с резервным хранилищем, которое соответствует `DateTime` данным \ (и имеет другой диапазон и точность из JavaScript `Date` ).  Если изменить этот настраиваемый `Date` объект, он становится стандартным сценарием JavaScript `Date` и теряет точность.  `Date`Значения JavaScript можно передать в среду выполнения Windows `DateTime` и будет проверяться по диапазону, что может привести к возникновению исключений для маршалирования.  

 Структура [TimeSpan][UwpWindowsFoundationTimespan] среды выполнения Windows преобразуется в миллисекунды и возвращается в виде номера JavaScript.  

## См. также  

[Использование среды выполнения Windows в JavaScript][WindowsRuntimeJavascript]  

<!-- image links -->  

<!-- links -->  

[WindowsRuntimeJavascript]: /microsoft-edge/windows-runtime/using-the-windows-runtime-in-javascript "Использование среды выполнения Windows в JavaScript"  

[UwpWindowsFoundationDatetime]: /uwp/api/Windows.Foundation.DateTime "Структура DateTime"  
[UwpWindowsFoundationTimespan]: /uwp/api/windows.foundation.timespan "Структура TimeSpan"  

[MDNDate]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Date "Дата | MDN"  
