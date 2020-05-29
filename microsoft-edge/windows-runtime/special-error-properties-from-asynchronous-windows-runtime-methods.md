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
# <span data-ttu-id="7517b-102">Специальные свойства ошибки из асинхронных методов среды выполнения Windows</span><span class="sxs-lookup"><span data-stu-id="7517b-102">Special Error Properties from Asynchronous Windows Runtime Methods</span></span>  

<span data-ttu-id="7517b-103">Отладка асинхронных методов среды выполнения Windows в JavaScript может быть сложной, так как эта ошибка может возникать в стеке вызовов.</span><span class="sxs-lookup"><span data-stu-id="7517b-103">It can be difficult to debug asynchronous Windows Runtime methods in JavaScript, because the error may be thrown from somewhere deep in the call stack.</span></span> <span data-ttu-id="7517b-104">Объект JavaScript `Error` имеет дополнительные свойства, которые отображаются только в том случае, если ошибка возникает из асинхронного метода среды выполнения Windows, если приложение работает в режиме отладки.</span><span class="sxs-lookup"><span data-stu-id="7517b-104">The JavaScript `Error` object has extra properties that appear only when the error is thrown from an asynchronous Windows Runtime method when the app is running in debug mode.</span></span>  
  
## <span data-ttu-id="7517b-105">Специальные свойства ошибки</span><span class="sxs-lookup"><span data-stu-id="7517b-105">Special Error Properties</span></span>  

<span data-ttu-id="7517b-106">Объект ошибки, являющийся результатом неудачной асинхронной операции среды выполнения Windows в режиме отладки, имеет следующие специальные свойства:</span><span class="sxs-lookup"><span data-stu-id="7517b-106">An error object that results from a failed Windows Runtime asynchronous operation in debug mode has the following special properties:</span></span>  

*   `asyncOpSource` <span data-ttu-id="7517b-107">\ (Объект \) получает сведения о первоначальном расположении, в котором была произведена ошибка вызова.</span><span class="sxs-lookup"><span data-stu-id="7517b-107">\(Object\) Gets information about the original location where the call that produced an error was made.</span></span> <span data-ttu-id="7517b-108">Свойство `asyncOpSource.originatingCall` \ (строка \) отображает расположение в коде пользователя, который является асинхронной операцией.</span><span class="sxs-lookup"><span data-stu-id="7517b-108">The property `asyncOpSource.originatingCall` \(String\) displays the location in the user's code that originated the asynchronous operation.</span></span>  
*   <span data-ttu-id="7517b-109">asyncOpType \ (String \) возвращает имя типа асинхронной операции, который создал ошибку.</span><span class="sxs-lookup"><span data-stu-id="7517b-109">asyncOpType \(String\) Gets the name of the asynchronous operation type that raised the error.</span></span>  
    
<span data-ttu-id="7517b-110">Дополнительные сведения об ошибках при использовании асинхронных операций можно найти в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="7517b-110">For more information about errors with asynchronous operations, see:</span></span>  
  
*   [<span data-ttu-id="7517b-111">Как обрабатывать ошибки с помощью обещает!</span><span class="sxs-lookup"><span data-stu-id="7517b-111">How to handle errors with promises</span></span>][PreviousVersionsWindowsAppsHh700337]  
*   [<span data-ttu-id="7517b-112">Устранение ошибок среды выполнения Windows</span><span class="sxs-lookup"><span data-stu-id="7517b-112">Troubleshooting Windows Runtime errors</span></span>][PreviousVersionsWindowsAppsHh974350]  

<!-- image links -->  

<!-- links -->  

[PreviousVersionsWindowsAppsHh700337]: /previous-versions/windows/apps/hh700337(v=win.10) "Обработка ошибок с помощью обещает (HTML)"  
[PreviousVersionsWindowsAppsHh974350]: /previous-versions/windows/apps/hh974350(v=win.10) "Устранение ошибок среды выполнения Windows (HTML)"  
