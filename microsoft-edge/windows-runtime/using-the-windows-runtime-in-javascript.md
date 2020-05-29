---
title: Использование среды выполнения Windows в JavaScript
ms.custom: ''
ms.date: 04/01/2020
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
ms.openlocfilehash: bffde93aa973f492189aedcfcaa9c3694d9e61bc
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572846"
---
# <span data-ttu-id="dcee3-102">Использование среды выполнения Windows в JavaScript</span><span class="sxs-lookup"><span data-stu-id="dcee3-102">Using the Windows Runtime in JavaScript</span></span>  

<span data-ttu-id="dcee3-103">При написании приложения универсальной платформы Windows (UWP) можно использовать классы, методы и свойства среды выполнения Windows в большинстве тем же способом, что и использование собственных объектов, методов и свойств JavaScript.</span><span class="sxs-lookup"><span data-stu-id="dcee3-103">When you write a Universal Windows Platform \(UWP\) app, you can use Windows Runtime classes, methods, and properties in much the same way that you would use native JavaScript objects, methods, and properties.</span></span>  <span data-ttu-id="dcee3-104">Этот раздел содержит сведения о вводе и ссылках на разделы, в которых описаны основные принципы использования API среды выполнения Windows в JavaScript, в том числе сведения о представлениях типов среды выполнения Windows, способах использования асинхронных методов среды выполнения Windows, а также о том, как прослушивать события среды выполнения Windows и обрабатывать их.</span><span class="sxs-lookup"><span data-stu-id="dcee3-104">This topic provides introductory information and links to topics that explain the basic concepts of using Windows Runtime APIs in JavaScript, including an explanation of how Windows Runtime types are represented, how to use asynchronous Windows Runtime methods, and how to listen to and handle Windows Runtime events.</span></span>  

<span data-ttu-id="dcee3-105">Для общеязыковой документации ознакомьтесь с библиотекой [ссылок JavaScript][MDNJavascriptReference] MDN.</span><span class="sxs-lookup"><span data-stu-id="dcee3-105">For general language documentation, check out MDN's [JavaScript reference][MDNJavascriptReference] library.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="dcee3-106">Функции среды выполнения Windows недоступны для приложений, работающих в Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="dcee3-106">Windows Runtime features are not available for apps that run in Internet Explorer.</span></span>  

## <span data-ttu-id="dcee3-107">Справочная документация по среде выполнения Windows</span><span class="sxs-lookup"><span data-stu-id="dcee3-107">Windows Runtime Reference Documentation</span></span>  

<span data-ttu-id="dcee3-108">Справочная документация приведена в [справочнике среды выполнения Windows][UwpApiIndex].</span><span class="sxs-lookup"><span data-stu-id="dcee3-108">For reference documentation, see [Windows Runtime Reference][UwpApiIndex].</span></span>  <span data-ttu-id="dcee3-109">Примеры кода доступны в JavaScript, а также в C++, C# и Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="dcee3-109">Code examples are available in JavaScript and also in C++, C#, and Visual Basic.</span></span>  

## <span data-ttu-id="dcee3-110">Написание компонентов среды выполнения Windows на C++, C# или Visual Basic</span><span class="sxs-lookup"><span data-stu-id="dcee3-110">Writing Windows Runtime Components in C++, C#, or Visual Basic</span></span>  

<span data-ttu-id="dcee3-111">Инструкции и рекомендации по написанию компонентов среды выполнения Windows, которые можно использовать в JavaScript, приведены в разделе [Создание компонентов среды выполнения Windows в C++][WindowsUwpWinrtCpp] и [Создание компонентов среды выполнения Windows в C# и Visual Basic][WindowsUwpWinrtCsharpVb].</span><span class="sxs-lookup"><span data-stu-id="dcee3-111">For instructions and guidelines for writing Windows Runtime components that can be consumed in JavaScript, see [Creating Windows Runtime Components in C++][WindowsUwpWinrtCpp] and [Creating Windows Runtime Components in C# and Visual Basic][WindowsUwpWinrtCsharpVb].</span></span>  

## <span data-ttu-id="dcee3-112">Правила использования регистров в функциях среды выполнения Windows</span><span class="sxs-lookup"><span data-stu-id="dcee3-112">Casing Conventions with Windows Runtime Features</span></span>  

<span data-ttu-id="dcee3-113">Соглашения о регистре для функций среды выполнения Windows в JavaScript немного отличаются от используемых в других языках:</span><span class="sxs-lookup"><span data-stu-id="dcee3-113">Casing conventions for Windows Runtime features in JavaScript differ slightly from those for other languages:</span></span>  

*   <span data-ttu-id="dcee3-114">Пространства имен и классы находятся в стиле Pascal.</span><span class="sxs-lookup"><span data-stu-id="dcee3-114">Namespaces and classes are in Pascal case:</span></span>  
    
    ```javascript
    Windows.Deployment.PackageInfo;
    ```  
    
*   <span data-ttu-id="dcee3-115">Члены классов, в том числе методы и свойства, а также члены структур и перечислений, имеют в стиле Camel:</span><span class="sxs-lookup"><span data-stu-id="dcee3-115">Members of classes, including methods and properties, and members of structures and enumerations, are in camel case:</span></span>  
    
    ```javascript
    Deployment.PackageInfo.createPackage();
    ```  
    
*   <span data-ttu-id="dcee3-116">Имена событий записываются в строчных буквах:</span><span class="sxs-lookup"><span data-stu-id="dcee3-116">Event names are in lower case:</span></span>  
    
    ```javascript
    dataTransferManager.ontargetapplicationchosen;
    ```  

## <span data-ttu-id="dcee3-117">См. также</span><span class="sxs-lookup"><span data-stu-id="dcee3-117">See Also</span></span>  

[<span data-ttu-id="dcee3-118">Рекомендации по использованию API среды выполнения Windows</span><span class="sxs-lookup"><span data-stu-id="dcee3-118">Considerations when Using the Windows Runtime API</span></span>][WindowsRuntimeConsiderationsApi]  
[<span data-ttu-id="dcee3-119">Использование асинхронных методов среды выполнения Windows</span><span class="sxs-lookup"><span data-stu-id="dcee3-119">Using Windows Runtime Asynchronous Methods</span></span>][WindowsRuntimeAsynchronousMethods]   
[<span data-ttu-id="dcee3-120">Обработка событий среды выполнения Windows в JavaScript</span><span class="sxs-lookup"><span data-stu-id="dcee3-120">Handling Windows Runtime Events in JavaScript</span></span>][WindowsRuntimeEventsJavascript]   
[<span data-ttu-id="dcee3-121">Представление типов среды выполнения Windows в JavaScript</span><span class="sxs-lookup"><span data-stu-id="dcee3-121">JavaScript Representation of Windows Runtime Types</span></span>][WindowsRuntimeJavascriptTypes]   
[<span data-ttu-id="dcee3-122">Проекция JavaScript в среде выполнения Windows DateTime и TimeSpan</span><span class="sxs-lookup"><span data-stu-id="dcee3-122">JavaScript Projection of Windows Runtime DateTime and TimeSpan</span></span>][WindowsRuntimeDatetimeTimespan]  
 
<!-- image links -->  

<!-- links  -->  

[WindowsRuntimeConsiderationsApi]: /microsoft-edge/windows-runtime/considerations-when-using-the-windows-runtime-api "Рекомендации по использованию API среды выполнения Windows"  
[WindowsRuntimeEventsJavascript]: /microsoft-edge/windows-runtime/handling-windows-runtime-events-in-javascript "Обработка событий среды выполнения Windows в JavaScript"  
[WindowsRuntimeJavascriptTypes]: /microsoft-edge/windows-runtime/javascript-representation-of-windows-runtime-types "Представление типов среды выполнения Windows в JavaScript"  
[WindowsRuntimeAsynchronousMethods]: /microsoft-edge/windows-runtime/using-windows-runtime-asynchronous-methods "Использование асинхронных методов среды выполнения Windows"  
[WindowsRuntimeDatetimeTimespan]: /microsoft-edge/windows-runtime/windows-runtime-datetime-and-timespan-representations "Представления DateTime и TimeSpan среды выполнения Windows"  

[UwpApiIndex]: /uwp/api/index "Пространства имен Windows UWP"  
[WindowsUwpWinrtCpp]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-cpp "Компоненты среды выполнения Windows с C++/CX"  
[WindowsUwpWinrtCsharpVb]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-csharp-and-visual-basic "Компоненты среды выполнения Windows в C# и Visual Basic"  

[MDNJavascriptReference]: https://developer.mozilla.org/docs/Web/JavaScript/Reference "Справочник по JavaScript | MDN"  
