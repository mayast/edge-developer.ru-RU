---
title: Рекомендации по использованию API среды выполнения Windows
ms.custom: ''
ms.date: 04/01/2020
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.technology: windows-integration
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime API
ms.assetid: 2f56d70c-c80d-4876-8e6a-8ae031d31c22
caps.latest.revision: 8
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 95b082e27c4f247b841a9540e13bd49bd4c8bd67
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572861"
---
# <span data-ttu-id="b4abe-102">Рекомендации по использованию API среды выполнения Windows</span><span class="sxs-lookup"><span data-stu-id="b4abe-102">Considerations when Using the Windows Runtime API</span></span>  

<span data-ttu-id="b4abe-103">Вы можете использовать практически каждый элемент API среды выполнения Windows в JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b4abe-103">You can use nearly every element of the Windows Runtime API in JavaScript.</span></span>  <span data-ttu-id="b4abe-104">Однако есть некоторые аспекты представления JavaScript элементов среды выполнения Windows, которые следует помнить.</span><span class="sxs-lookup"><span data-stu-id="b4abe-104">However, there are some aspects of the JavaScript representation of Windows Runtime elements that you should keep in mind.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="b4abe-105">Сведения о создании компонентов среды выполнения Windows в C++, C# или Visual Basic и их использовании в JavaScript можно найти в разделе [Создание компонентов среды выполнения Windows в c++][WindowsUwpComponentsCreatingCpp] и [Создание компонентов среды выполнения Windows в C# и Visual Basic][WindowsUwpComponentsCreatingCsharpVb].</span><span class="sxs-lookup"><span data-stu-id="b4abe-105">For information about creating Windows Runtime components in C++, C#, or Visual Basic and consuming them in JavaScript, see [Creating Windows Runtime Components in C++][WindowsUwpComponentsCreatingCpp] and [Creating Windows Runtime Components in C# and Visual Basic][WindowsUwpComponentsCreatingCsharpVb].</span></span>  

## <span data-ttu-id="b4abe-106">Особые случаи в представлении JavaScript типов среды выполнения Windows</span><span class="sxs-lookup"><span data-stu-id="b4abe-106">Special Cases in the JavaScript Representation of Windows Runtime Types</span></span>  

*   <span data-ttu-id="b4abe-107">Строки: неинициализированная строка передается методу среды выполнения Windows в качестве строки "uninitial", а строковое значение `null` передается как строка "null".</span><span class="sxs-lookup"><span data-stu-id="b4abe-107">Strings: An uninitialized string is passed to a Windows Runtime method as the string "undefined", and a string set to `null` is passed as the string "null".</span></span>  <span data-ttu-id="b4abe-108">\ (Это справедливо каждый раз, `null` когда `undefined` какое-либо значение приводится к строке. \) перед передачей строки методу среды выполнения Windows следует инициализировать ее как пустую строку \ ("" \ ").</span><span class="sxs-lookup"><span data-stu-id="b4abe-108">\(This is true whenever a `null` or `undefined` value is coerced to a string.\)  Before you pass a string to a Windows Runtime method, you should initialize it as the empty string \(""\).</span></span>  
*   <span data-ttu-id="b4abe-109">Интерфейсы: невозможно реализовать интерфейс среды выполнения Windows в JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b4abe-109">Interfaces: You cannot implement a Windows Runtime interface in JavaScript.</span></span>  
*   <span data-ttu-id="b4abe-110">Массивы: массивы среды выполнения Windows не изменяются в размерах, поэтому методы, изменяющие размер массивов в JavaScript, не работают в массивах среды выполнения Windows.</span><span class="sxs-lookup"><span data-stu-id="b4abe-110">Arrays: Windows Runtime arrays are not resizable, so methods that resize arrays in JavaScript do not work on Windows Runtime arrays.</span></span>  
*   <span data-ttu-id="b4abe-111">Массивы: Если вы передаете значение массива JavaScript методу среды выполнения Windows, копируется массив.</span><span class="sxs-lookup"><span data-stu-id="b4abe-111">Arrays: If you pass a JavaScript array value to a Windows Runtime method, the array is copied.</span></span>  <span data-ttu-id="b4abe-112">Метод среды выполнения Windows не может изменить массив или его члены и вернуть его в приложение JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b4abe-112">The Windows Runtime method is not able to modify the array or its members and return it to your JavaScript app.</span></span>  <span data-ttu-id="b4abe-113">Однако вы можете использовать типизированные массивы \ (например, [Int32Array Object][MDNInt32array]\), которые не копируются.</span><span class="sxs-lookup"><span data-stu-id="b4abe-113">However, you can use typed arrays \(for example, [Int32Array Object][MDNInt32array]\), which are not copied.</span></span>  
*   <span data-ttu-id="b4abe-114">Структуры: структуры среды выполнения Windows — это объекты в JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b4abe-114">Structures: Windows Runtime structures are objects in JavaScript.</span></span>  <span data-ttu-id="b4abe-115">Если вы хотите передать структуру среды выполнения Windows в метод среды выполнения Windows, не создавайте экземпляр структуры с помощью `new` ключевого слова.</span><span class="sxs-lookup"><span data-stu-id="b4abe-115">If you want to pass a Windows Runtime structure to a Windows Runtime method, don't instantiate the structure with the `new` keyword.</span></span>  <span data-ttu-id="b4abe-116">Вместо этого создайте объект и добавьте соответствующие члены и их значения.</span><span class="sxs-lookup"><span data-stu-id="b4abe-116">Instead, create an object and add the relevant members and their values.</span></span>  <span data-ttu-id="b4abe-117">Имена участников должны быть в стиле Camel: `SomeStruct.firstMember` .</span><span class="sxs-lookup"><span data-stu-id="b4abe-117">The names of the members should be in camel case: `SomeStruct.firstMember`.</span></span>  
*   <span data-ttu-id="b4abe-118">Объекты: объекты JavaScript не совпадают с объектами управляемого кода \ ( `System.Object` \).</span><span class="sxs-lookup"><span data-stu-id="b4abe-118">Objects: JavaScript objects aren't the same as managed code objects \(`System.Object`\).</span></span>  <span data-ttu-id="b4abe-119">Вы не можете передать объект JavaScript методу среды выполнения Windows, для которого требуется `System.Object` .</span><span class="sxs-lookup"><span data-stu-id="b4abe-119">You can't pass a JavaScript object to a Windows Runtime method that requires a `System.Object`.</span></span>  
*   <span data-ttu-id="b4abe-120">Идентификация объекта: в большинстве случаев объекты, передаваемые между средой выполнения Windows и JavaScript, не изменяются.</span><span class="sxs-lookup"><span data-stu-id="b4abe-120">Object identity: In most cases, the objects passed back and forth between the Windows Runtime and JavaScript do not change.</span></span>  <span data-ttu-id="b4abe-121">Механизм JavaScript поддерживает схему известных объектов.</span><span class="sxs-lookup"><span data-stu-id="b4abe-121">The JavaScript engine maintains a map of known objects.</span></span>  <span data-ttu-id="b4abe-122">Когда объект возвращается из среды выполнения Windows, он сопоставляется с картой и, если он не существует, создается новый объект.</span><span class="sxs-lookup"><span data-stu-id="b4abe-122">When an object is returned from the Windows Runtime it is matched against the map, and if it does not exist a new object is created.</span></span>  <span data-ttu-id="b4abe-123">Эти же действия выполняются для объектов, представляющих интерфейсы, возвращаемые методами среды выполнения Windows.</span><span class="sxs-lookup"><span data-stu-id="b4abe-123">The same procedure is followed for objects that represent interfaces that are returned by Windows Runtime methods.</span></span>  <span data-ttu-id="b4abe-124">Существует два типа исключений.</span><span class="sxs-lookup"><span data-stu-id="b4abe-124">There are two kinds of exceptions:</span></span>  

    *   <span data-ttu-id="b4abe-125">Объекты, возвращаемые при вызове среды выполнения Windows, и новые свойства \ (expando \), не сохраняются при передаче обратно в среду выполнения Windows.</span><span class="sxs-lookup"><span data-stu-id="b4abe-125">Objects that are returned from a Windows Runtime call, and then have new \(expando\) properties added, don't retain their new properties when they are passed back to the Windows Runtime.</span></span>  <span data-ttu-id="b4abe-126">Тем не менее, когда они возвращаются в приложение JavaScript, так как они соответствуют существующему объекту, возвращаемый объект имеет свойства expando.</span><span class="sxs-lookup"><span data-stu-id="b4abe-126">However, when they are returned to the JavaScript app, because they're matched to the existing object, the returned object does have the expando properties.</span></span>  
    *   <span data-ttu-id="b4abe-127">Структуры и делегаты в среде выполнения Windows не могут идентифицироваться так же, как и ранее использованные структуры или делегаты.</span><span class="sxs-lookup"><span data-stu-id="b4abe-127">Structures and delegates in Windows Runtime can't be identified as identical to previously-used structures or delegates.</span></span>  <span data-ttu-id="b4abe-128">Каждый раз, когда возвращается функция Structure или делегата, она получает новую ссылку.</span><span class="sxs-lookup"><span data-stu-id="b4abe-128">Every time a structure or delegate is returned, it gets a new reference.</span></span>  

*   <span data-ttu-id="b4abe-129">Конфликты имен: несколько интерфейсов среды выполнения Windows могут содержать члены с одинаковыми именами.</span><span class="sxs-lookup"><span data-stu-id="b4abe-129">Name collisions: Multiple Windows Runtime interfaces may have members with the same names.</span></span>  <span data-ttu-id="b4abe-130">Если они объединены в один объект JavaScript (который может быть представлением класса среды выполнения или интерфейса), то члены представлены с полными именами.</span><span class="sxs-lookup"><span data-stu-id="b4abe-130">If they are combined in a single JavaScript object (which can be a representation of a runtime class or an interface), the members are represented with fully-qualified names.</span></span>  <span data-ttu-id="b4abe-131">Чтобы вызвать эти члены, используйте следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="b4abe-131">You can call these members by using the following syntax:</span></span>  
    
    ```cpp
    Class["MemberName"](parameter)
    ```  
    
    <span data-ttu-id="b4abe-132">В следующем коде у двух интерфейсов есть метод Draw, а в классе среды выполнения реализованы оба интерфейса.</span><span class="sxs-lookup"><span data-stu-id="b4abe-132">In the following code, two interfaces have a Draw method, and a runtime class implements both interfaces.</span></span>  
    
    ```cpp
    namespace CollisionExample {
        interface InterfaceA
        {
            HRESULT Draw([in] Int32 a);
        }
        interface InterfaceB
        {
            HRESULT Draw([in] HString a);
        }
        runtimeclass ExampleObject {
          interface InterfaceA
          interface InterfaceB
        }
    }
    ```  
    
    <span data-ttu-id="b4abe-133">Вот как можно вызвать вышеприведенный код в JavaScript.</span><span class="sxs-lookup"><span data-stu-id="b4abe-133">Here is how you can call the above code in JavaScript.</span></span>  
    
    ```javascript
    var example = new ExampleObject();
    example["CollisionExample.InterfaceA.draw"](12);
    example["CollisionExample.InterfaceB.draw"]("hello");
    ```  
    
*   `Out` <span data-ttu-id="b4abe-134">параметры: Если метод среды выполнения Windows имеет несколько `out` параметров, в JavaScript этот метод имеет объект JavaScript в качестве возвращаемого значения и объект имеет свойства, соответствующие `out` параметру.</span><span class="sxs-lookup"><span data-stu-id="b4abe-134">parameters: If a Windows Runtime method has multiple `out` parameters, in JavaScript the method has a JavaScript object as its return value, and the object has properties that correspond to the `out` parameter.</span></span>  <span data-ttu-id="b4abe-135">Например, можно использовать следующую подпись среды выполнения Windows в C++.</span><span class="sxs-lookup"><span data-stu-id="b4abe-135">For example, consider the following Windows Runtime signature in C++.</span></span>  
    
    ```cpp
    void ExampleMethod(
      [OutAttribute] char^ first,
      [OutAttribute] char^ second
    )
    ```  
    
    <span data-ttu-id="b4abe-136">Версия JavaScript этой сигнатуры:</span><span class="sxs-lookup"><span data-stu-id="b4abe-136">The JavaScript version of this signature is:</span></span>  
    
    ```javascript
    var returnValue = exampleMethod();
    ```  
    
    <span data-ttu-id="b4abe-137">В этом примере `returnValue` — объект JavaScript, имеющий два поля: `first` и `second` .</span><span class="sxs-lookup"><span data-stu-id="b4abe-137">In this example, `returnValue` is a JavaScript object that has two fields: `first` and `second`.</span></span>  
    
*   <span data-ttu-id="b4abe-138">Статические члены: среда выполнения Windows определяет статические члены и члены экземпляра.</span><span class="sxs-lookup"><span data-stu-id="b4abe-138">Static members: The Windows Runtime defines both static members and instance members.</span></span>  <span data-ttu-id="b4abe-139">В JavaScript статические члены добавляются в объект, связанный с классом или интерфейсом среды выполнения Windows.</span><span class="sxs-lookup"><span data-stu-id="b4abe-139">In JavaScript, static members are added to the object that is associated with the Windows Runtime class or interface.</span></span>  
    
    ```javascript
    // Static method.
    var accel = Windows.Devices.Sensors.Accelerometer.getDefault();
    // Instance method.
    var reading = accel.getCurrentReading();
    ```  
    
<span data-ttu-id="b4abe-140">Дополнительные сведения о представлении JavaScript основных типов среды выполнения Windows можно найти в [представлении JavaScript типов среды выполнения Windows][WindowsRuntimeJavascriptTypes].</span><span class="sxs-lookup"><span data-stu-id="b4abe-140">For more information about the JavaScript representation of Windows Runtime basic types, see [JavaScript Representation of Windows Runtime Types][WindowsRuntimeJavascriptTypes].</span></span>  

<!-- image links -->  

<!-- links -->  
 
[WindowsRuntimeJavascriptTypes]: /microsoft-edge/windows-runtime/javascript-representation-of-windows-runtime-types "Представление типов среды выполнения Windows в JavaScript"

[WindowsUwpComponentsCreatingCpp]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-cpp "Компоненты среды выполнения Windows с C++/CX"  
[WindowsUwpComponentsCreatingCsharpVb]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-csharp-and-visual-basic "Компоненты среды выполнения Windows в C# и Visual Basic"  

[MDNInt32array]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Int32Array "Int32Array | MDN"  