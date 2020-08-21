---
title: Специальные свойства ошибок из асинхронных методов среды выполнения Windows.
ms.custom: ''
ms.date: 07/29/2020
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.technology: windows-integration
ms.tgt_pltfrm: ''
ms.topic: article
ms.assetid: 45155584-06d8-4e7f-93a6-8564a93f643d
caps.latest.revision: 4
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: a1fccf1cec811501b94e7da4aa20b69d93754f62
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942067"
---
# Специальные свойства ошибок из асинхронных методов среды выполнения Windows.  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Несовместимость с асинхронными методами выполнения Windows в JavaScript может быть слишком свежий, так как она может вызывать неоднозначно в стеке вызовов.  Объект JavaScript имеет дополнительные свойства, которые отображаются только при наличии ошибки в режиме выполнения `Error` асинхронного метода выполнения Windows при запуске приложения в режиме отладки.  
  
## Специальные свойства ошибки  

Объект ошибки, возникающий из сбоя windows асинхронных операций в режиме отладки, имеет следующие свойства:  

*   `asyncOpSource` \(Object\) Gets information about location where the call that duted that вызывал ошибку.  В свойстве "\(String\)" отображается местовой поиск в коде пользователя, который происходил операция `asyncOpSource.originatingCall` асинхронно.  
*   asyncOpType \(String\) получает имя типа асинхронного типа операции, возвращаемого ошибкой.  
    
Дополнительные сведения об ошибках с асинхронными операциями см. в следующих статьях:  
  
*   [Обработка ошибок с пропущенными минимумами][PreviousVersionsWindowsAppsHh700337]  
*   [Устранение ошибок Windows Runtime][PreviousVersionsWindowsAppsHh974350]  

<!-- links -->  

[PreviousVersionsWindowsAppsHh700337]: /previous-versions/windows/apps/hh700337(v=win.10) "Обработка ошибок с пропущенными HTML-кодами | Документы Майкрософт"  
[PreviousVersionsWindowsAppsHh974350]: /previous-versions/windows/apps/hh974350(v=win.10) "Устранение ошибок среды выполнения Windows (HTML) | Документы Майкрософт"  
