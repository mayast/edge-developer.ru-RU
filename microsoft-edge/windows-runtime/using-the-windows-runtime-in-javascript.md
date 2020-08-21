---
title: Использование среды выполнения Windows в JavaScript
ms.custom: ''
ms.date: 07/29/2020
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.technology: windows-integration
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime
ms.assetid: 90658546-f746-4e34-a7d1-71cf9ee322a2
caps.latest.revision: 16
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 444008598a2f7a2f5257544304bed87fbfaa203a
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942171"
---
# <span data-ttu-id="3b85e-102">Использование среды выполнения Windows в JavaScript</span><span class="sxs-lookup"><span data-stu-id="3b85e-102">Using the Windows Runtime in JavaScript</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="3b85e-103">При создании универсальной платформы Windows \(UWP\) вы можете использовать классы Среды выполнения, методы и свойства Windows так же, как и встроенные объекты JavaScript, методы и свойства.</span><span class="sxs-lookup"><span data-stu-id="3b85e-103">When you write a Universal Windows Platform \(UWP\) app, you can use Windows Runtime classes, methods, and properties in much the same way that you would use native JavaScript objects, methods, and properties.</span></span>  <span data-ttu-id="3b85e-104">В этой статье приведены общие сведения об основных понятиях использования API среды выполнения Windows в JavaScript JavaScript, в том числе объяснение типов Windows Runtime, а также обработке методов Windows Runtime и обработке событий Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="3b85e-104">This topic provides introductory information and links to topics that explain the basic concepts of using Windows Runtime APIs in JavaScript, including an explanation of how Windows Runtime types are represented, how to use asynchronous Windows Runtime methods, and how to listen to and handle Windows Runtime events.</span></span>  

<span data-ttu-id="3b85e-105">Для общего языка можно ознакомиться с библиотекой [JavaScript.][MDNJavascriptReference]</span><span class="sxs-lookup"><span data-stu-id="3b85e-105">For general language documentation, check out MDN's [JavaScript reference][MDNJavascriptReference] library.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="3b85e-106">Функции выполнения Windows недоступны для приложений, работающих в Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="3b85e-106">Windows Runtime features are not available for apps that run in Internet Explorer.</span></span>  

## <span data-ttu-id="3b85e-107">Справочная документация windows</span><span class="sxs-lookup"><span data-stu-id="3b85e-107">Windows Runtime reference documentation</span></span>  

<span data-ttu-id="3b85e-108">Сведения для справки см. в [справке по Windows.][UwpApiIndex]</span><span class="sxs-lookup"><span data-stu-id="3b85e-108">For reference documentation, see [Windows Runtime Reference][UwpApiIndex].</span></span>  <span data-ttu-id="3b85e-109">Примеры кодов доступны в JavaScript, а также в C++, C#и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="3b85e-109">Code examples are available in JavaScript and also in C++, C#, and Visual Basic.</span></span>  

## <span data-ttu-id="3b85e-110">Написание компонентов среды выполнения Windows в C++, C#или Visual Basic</span><span class="sxs-lookup"><span data-stu-id="3b85e-110">Writing Windows Runtime components in C++, C#, or Visual Basic</span></span>  

<span data-ttu-id="3b85e-111">Инструкции и рекомендации по созданию компонентов среды выполнения Windows, которые можно использовать в JavaScript, см. в статье ["Создание компонентов среды выполнения Windows в C++ и][WindowsUwpWinrtCpp] [создание компонентов среды выполнения в C# и Visual Basic".][WindowsUwpWinrtCsharpVb]</span><span class="sxs-lookup"><span data-stu-id="3b85e-111">For instructions and guidelines for writing Windows Runtime components that can be consumed in JavaScript, see [Creating Windows Runtime Components in C++][WindowsUwpWinrtCpp] and [Creating Windows Runtime Components in C# and Visual Basic][WindowsUwpWinrtCsharpVb].</span></span>  

## <span data-ttu-id="3b85e-112">Соглашения с возможностями среды выполнения Windows</span><span class="sxs-lookup"><span data-stu-id="3b85e-112">Casing conventions with Windows Runtime features</span></span>  

<span data-ttu-id="3b85e-113">Кассовать соглашения для средств среды выполнения Windows в JavaScript отличаются от языков, доступных на других языках:</span><span class="sxs-lookup"><span data-stu-id="3b85e-113">Casing conventions for Windows Runtime features in JavaScript differ slightly from those for other languages:</span></span>  

*   <span data-ttu-id="3b85e-114">Имена и занятия присутствуют в пассивах:</span><span class="sxs-lookup"><span data-stu-id="3b85e-114">Namespaces and classes are in Pascal case:</span></span>  
    
    ```javascript
    Windows.Deployment.PackageInfo;
    ```  
    
*   <span data-ttu-id="3b85e-115">Участники класса, включая методы и свойства, а также участники структур и перечислений, в камере применяются следующие камеры:</span><span class="sxs-lookup"><span data-stu-id="3b85e-115">Members of classes, including methods and properties, and members of structures and enumerations, are in camel case:</span></span>  
    
    ```javascript
    Deployment.PackageInfo.createPackage();
    ```  
    
*   <span data-ttu-id="3b85e-116">Имена событий отображаются в нижнем регистре.</span><span class="sxs-lookup"><span data-stu-id="3b85e-116">Event names are in lower case:</span></span>  
    
    ```javascript
    dataTransferManager.ontargetapplicationchosen;
    ```  

## <span data-ttu-id="3b85e-117">См. также</span><span class="sxs-lookup"><span data-stu-id="3b85e-117">See also</span></span>  

[<span data-ttu-id="3b85e-118">Рекомендации по использованию API среды выполнения Windows</span><span class="sxs-lookup"><span data-stu-id="3b85e-118">Considerations when Using the Windows Runtime API</span></span>][WindowsRuntimeConsiderationsApi]  
[<span data-ttu-id="3b85e-119">Использование асинхронных методов среды выполнения Windows</span><span class="sxs-lookup"><span data-stu-id="3b85e-119">Using Windows Runtime Asynchronous Methods</span></span>][WindowsRuntimeAsynchronousMethods]   
[<span data-ttu-id="3b85e-120">Обработка событий среды выполнения Windows в JavaScript</span><span class="sxs-lookup"><span data-stu-id="3b85e-120">Handling Windows Runtime Events in JavaScript</span></span>][WindowsRuntimeEventsJavascript]   
[<span data-ttu-id="3b85e-121">Представление типов среды выполнения Windows в JavaScript</span><span class="sxs-lookup"><span data-stu-id="3b85e-121">JavaScript Representation of Windows Runtime Types</span></span>][WindowsRuntimeJavascriptTypes]   
[<span data-ttu-id="3b85e-122">JavaScript Project of Windows Runtime and TimeSpan</span><span class="sxs-lookup"><span data-stu-id="3b85e-122">JavaScript Projection of Windows Runtime DateTime and TimeSpan</span></span>][WindowsRuntimeDatetimeTimespan]  

<!-- links  -->  

[WindowsRuntimeConsiderationsApi]: ./considerations-when-using-the-windows-runtime-api.md "Рекомендации по использованию API среды выполнения Windows | Документы Майкрософт"  
[WindowsRuntimeEventsJavascript]: ./handling-windows-runtime-events-in-javascript.md "Обработка событий windows Runtime в JavaScript | Документы Майкрософт"  
[WindowsRuntimeJavascriptTypes]: ./javascript-representation-of-windows-runtime-types.md "Представление JavaScript типов среды выполнения Windows | Документы Майкрософт"  
[WindowsRuntimeAsynchronousMethods]: ./using-windows-runtime-asynchronous-methods.md "Использование асинхронных методов Windows | Документы Майкрософт"  
[WindowsRuntimeDatetimeTimespan]: ./windows-runtime-datetime-and-timespan-representations.md "Репредставление даты и времени выполнения и TimeSpan | Документы Майкрософт"  

[UwpApiIndex]: /uwp/api/index "Имена пространств Windows UWP | Документы Майкрософт"  
[WindowsUwpWinrtCpp]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-cpp "Компоненты среды выполнения Windows с C+++/CX | Документы Майкрософт"  
[WindowsUwpWinrtCsharpVb]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-csharp-and-visual-basic "Компоненты среды выполнения Windows с C# и Visual Basic | Документы Майкрософт"  

[MDNJavascriptReference]: https://developer.mozilla.org/docs/Web/JavaScript/Reference "Справочник по JavaScript | MDN"  
