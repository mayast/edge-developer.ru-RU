---
title: Специальные свойства ошибки из асинхронных методов среды выполнения Windows
ms.custom: ''
ms.date: 04/01/2020
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
ms.openlocfilehash: 5cf2604e26c84e769cf44e0879ee137cbfbe8b90
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572848"
---
# Специальные свойства ошибки из асинхронных методов среды выполнения Windows  

Отладка асинхронных методов среды выполнения Windows в JavaScript может быть сложной, так как эта ошибка может возникать в стеке вызовов. Объект JavaScript `Error` имеет дополнительные свойства, которые отображаются только в том случае, если ошибка возникает из асинхронного метода среды выполнения Windows, если приложение работает в режиме отладки.  
  
## Специальные свойства ошибки  

Объект ошибки, являющийся результатом неудачной асинхронной операции среды выполнения Windows в режиме отладки, имеет следующие специальные свойства:  

*   `asyncOpSource` \ (Объект \) получает сведения о первоначальном расположении, в котором была произведена ошибка вызова. Свойство `asyncOpSource.originatingCall` \ (строка \) отображает расположение в коде пользователя, который является асинхронной операцией.  
*   asyncOpType \ (String \) возвращает имя типа асинхронной операции, который создал ошибку.  
    
Дополнительные сведения об ошибках при использовании асинхронных операций можно найти в следующих статьях:  
  
*   [Как обрабатывать ошибки с помощью обещает!][PreviousVersionsWindowsAppsHh700337]  
*   [Устранение ошибок среды выполнения Windows][PreviousVersionsWindowsAppsHh974350]  

<!-- image links -->  

<!-- links -->  

[PreviousVersionsWindowsAppsHh700337]: /previous-versions/windows/apps/hh700337(v=win.10) "Обработка ошибок с помощью обещает (HTML)"  
[PreviousVersionsWindowsAppsHh974350]: /previous-versions/windows/apps/hh974350(v=win.10) "Устранение ошибок среды выполнения Windows (HTML)"  
