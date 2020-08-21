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
# <span data-ttu-id="1a8a9-102">Специальные свойства ошибок из асинхронных методов среды выполнения Windows.</span><span class="sxs-lookup"><span data-stu-id="1a8a9-102">Special error properties from asynchronous Windows Runtime methods</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="1a8a9-103">Несовместимость с асинхронными методами выполнения Windows в JavaScript может быть слишком свежий, так как она может вызывать неоднозначно в стеке вызовов.</span><span class="sxs-lookup"><span data-stu-id="1a8a9-103">It can be difficult to debug asynchronous Windows Runtime methods in JavaScript, because the error may be thrown from somewhere deep in the call stack.</span></span>  <span data-ttu-id="1a8a9-104">Объект JavaScript имеет дополнительные свойства, которые отображаются только при наличии ошибки в режиме выполнения `Error` асинхронного метода выполнения Windows при запуске приложения в режиме отладки.</span><span class="sxs-lookup"><span data-stu-id="1a8a9-104">The JavaScript `Error` object has extra properties that appear only when the error is thrown from an asynchronous Windows Runtime method when the app is running in debug mode.</span></span>  
  
## <span data-ttu-id="1a8a9-105">Специальные свойства ошибки</span><span class="sxs-lookup"><span data-stu-id="1a8a9-105">Special error properties</span></span>  

<span data-ttu-id="1a8a9-106">Объект ошибки, возникающий из сбоя windows асинхронных операций в режиме отладки, имеет следующие свойства:</span><span class="sxs-lookup"><span data-stu-id="1a8a9-106">An error object that results from a failed Windows Runtime asynchronous operation in debug mode has the following special properties:</span></span>  

*   `asyncOpSource` <span data-ttu-id="1a8a9-107">\(Object\) Gets information about location where the call that duted that вызывал ошибку.</span><span class="sxs-lookup"><span data-stu-id="1a8a9-107">\(Object\) Gets information about the original location where the call that produced an error was made.</span></span>  <span data-ttu-id="1a8a9-108">В свойстве "\(String\)" отображается местовой поиск в коде пользователя, который происходил операция `asyncOpSource.originatingCall` асинхронно.</span><span class="sxs-lookup"><span data-stu-id="1a8a9-108">The property `asyncOpSource.originatingCall` \(String\) displays the location in the user's code that originated the asynchronous operation.</span></span>  
*   <span data-ttu-id="1a8a9-109">asyncOpType \(String\) получает имя типа асинхронного типа операции, возвращаемого ошибкой.</span><span class="sxs-lookup"><span data-stu-id="1a8a9-109">asyncOpType \(String\) Gets the name of the asynchronous operation type that raised the error.</span></span>  
    
<span data-ttu-id="1a8a9-110">Дополнительные сведения об ошибках с асинхронными операциями см. в следующих статьях:</span><span class="sxs-lookup"><span data-stu-id="1a8a9-110">For more information about errors with asynchronous operations, see:</span></span>  
  
*   [<span data-ttu-id="1a8a9-111">Обработка ошибок с пропущенными минимумами</span><span class="sxs-lookup"><span data-stu-id="1a8a9-111">How to handle errors with promises</span></span>][PreviousVersionsWindowsAppsHh700337]  
*   [<span data-ttu-id="1a8a9-112">Устранение ошибок Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="1a8a9-112">Troubleshooting Windows Runtime errors</span></span>][PreviousVersionsWindowsAppsHh974350]  

<!-- links -->  

[PreviousVersionsWindowsAppsHh700337]: /previous-versions/windows/apps/hh700337(v=win.10) "Обработка ошибок с пропущенными HTML-кодами | Документы Майкрософт"  
[PreviousVersionsWindowsAppsHh974350]: /previous-versions/windows/apps/hh974350(v=win.10) "Устранение ошибок среды выполнения Windows (HTML) | Документы Майкрософт"  
