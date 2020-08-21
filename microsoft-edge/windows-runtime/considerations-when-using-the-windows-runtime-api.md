---
title: Рекомендации по использованию API среды выполнения Windows
ms.custom: ''
ms.date: 07/29/2020
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
ms.openlocfilehash: 6b460fe514927590382613b7454a69c89a5a5f8b
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942213"
---
# <span data-ttu-id="bc26b-102">Рекомендации по использованию API среды выполнения Windows</span><span class="sxs-lookup"><span data-stu-id="bc26b-102">Considerations when using the Windows Runtime API</span></span>  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

<span data-ttu-id="bc26b-103">Теперь можно использовать практически все элементы API выполнения Windows в JavaScript.</span><span class="sxs-lookup"><span data-stu-id="bc26b-103">You can use nearly every element of the Windows Runtime API in JavaScript.</span></span>  <span data-ttu-id="bc26b-104">Однако некоторые аспекты элементов во время выполнения JavaScript элементов Windows, которые необходимо помнить.</span><span class="sxs-lookup"><span data-stu-id="bc26b-104">However, there are some aspects of the JavaScript representation of Windows Runtime elements that you should keep in mind.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="bc26b-105">Сведения о создании компонентов среды выполнения Windows в C++, C#или Visual Basic и использовании их в JavaScript см. в статье ["Создание компонентов среды выполнения Windows в C++][WindowsUwpComponentsCreatingCpp] и создание компонентов среды выполнения [в C# и Visual Basic.][WindowsUwpComponentsCreatingCsharpVb]</span><span class="sxs-lookup"><span data-stu-id="bc26b-105">For information about creating Windows Runtime components in C++, C#, or Visual Basic and consuming them in JavaScript, see [Creating Windows Runtime Components in C++][WindowsUwpComponentsCreatingCpp] and [Creating Windows Runtime Components in C# and Visual Basic][WindowsUwpComponentsCreatingCsharpVb].</span></span>  

## <span data-ttu-id="bc26b-106">Особые случаи в типах JavaScript для Windows Runtime</span><span class="sxs-lookup"><span data-stu-id="bc26b-106">Special cases in the JavaScript Representation of Windows Runtime types</span></span>  

:::row:::
   :::column span="1":::
      <span data-ttu-id="bc26b-107">Строки</span><span class="sxs-lookup"><span data-stu-id="bc26b-107">Strings</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="bc26b-108">Неинициализированная строка служит методом среды выполнения Windows, а строка "Unsetd" в качестве `null` строки "Null" является строкой "Null".</span><span class="sxs-lookup"><span data-stu-id="bc26b-108">An uninitialized string is passed to a Windows Runtime method as the string "undefined", and a string set to `null` is passed as the string "null".</span></span>  <span data-ttu-id="bc26b-109">\(Это значение действительно принадлежат к `null` `undefined` строке.\) Перед аналогичным способом Windows, следует инициализировать ее как пустую строку \("\).</span><span class="sxs-lookup"><span data-stu-id="bc26b-109">\(This is true whenever a `null` or `undefined` value is coerced to a string.\)  Before you pass a string to a Windows Runtime method, you should initialize it as the empty string \(""\).</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="bc26b-110">Интерфейсы</span><span class="sxs-lookup"><span data-stu-id="bc26b-110">Interfaces</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="bc26b-111">Интерфейс среды выполнения Windows невозможно внедрить в JavaScript.</span><span class="sxs-lookup"><span data-stu-id="bc26b-111">You cannot implement a Windows Runtime interface in JavaScript.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="bc26b-112">Массивы</span><span class="sxs-lookup"><span data-stu-id="bc26b-112">Arrays</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="bc26b-113">Массивы Windows Runtime не изменяются, поэтому методы изменения размера массивов в JavaScript не работают для массивов Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="bc26b-113">Windows Runtime arrays are not resizable, so methods that resize arrays in JavaScript do not work on Windows Runtime arrays.</span></span>  
      *   <span data-ttu-id="bc26b-114">Массивы: при переносе значения массива JavaScript в метод выполнения Windows этот макрос копируется.</span><span class="sxs-lookup"><span data-stu-id="bc26b-114">Arrays: If you pass a JavaScript array value to a Windows Runtime method, the array is copied.</span></span>  <span data-ttu-id="bc26b-115">Метод среды выполнения Windows не может изменять массив или его элементы и вернуть его в приложение JavaScript.</span><span class="sxs-lookup"><span data-stu-id="bc26b-115">The Windows Runtime method is not able to modify the array or its members and return it to your JavaScript app.</span></span>  <span data-ttu-id="bc26b-116">Однако можно использовать тип \(например, [Int32Array][MDNInt32array]\), которые не копируются.</span><span class="sxs-lookup"><span data-stu-id="bc26b-116">However, you can use typed arrays \(for example, [Int32Array Object][MDNInt32array]\), which are not copied.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="bc26b-117">Структуры</span><span class="sxs-lookup"><span data-stu-id="bc26b-117">Structures</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="bc26b-118">Структуры выполнения Windows являются объектами в JavaScript.</span><span class="sxs-lookup"><span data-stu-id="bc26b-118">Windows Runtime structures are objects in JavaScript.</span></span>  <span data-ttu-id="bc26b-119">Если вы хотите сделать структуру Windows Runtime методом Windows Runtime, не используйте ключевое `new` слово.</span><span class="sxs-lookup"><span data-stu-id="bc26b-119">If you want to pass a Windows Runtime structure to a Windows Runtime method, don't instantiate the structure with the `new` keyword.</span></span>  <span data-ttu-id="bc26b-120">Вместо этого создайте объект и добавьте необходимых участников и их значения.</span><span class="sxs-lookup"><span data-stu-id="bc26b-120">Instead, create an object and add the relevant members and their values.</span></span>  <span data-ttu-id="bc26b-121">В отличие от имен участников должны быть названы `SomeStruct.firstMember` так:</span><span class="sxs-lookup"><span data-stu-id="bc26b-121">The names of the members should be in camel case: `SomeStruct.firstMember`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="bc26b-122">Объекты</span><span class="sxs-lookup"><span data-stu-id="bc26b-122">Objects</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="bc26b-123">Объекты JavaScript отличаются от объектов управляемых кодов \( `System.Object` \).</span><span class="sxs-lookup"><span data-stu-id="bc26b-123">JavaScript objects aren't the same as managed code objects \(`System.Object`\).</span></span>  <span data-ttu-id="bc26b-124">Объект JavaScript невозможно перенести в метод выполнения Windows, который `System.Object` требуется.</span><span class="sxs-lookup"><span data-stu-id="bc26b-124">You can't pass a JavaScript object to a Windows Runtime method that requires a `System.Object`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="bc26b-125">Удостоверение объекта</span><span class="sxs-lookup"><span data-stu-id="bc26b-125">Object identity</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="bc26b-126">В большинстве случаев объекты, переданные как в передаче, так и между windows Runtime и JavaScript, не изменяются.</span><span class="sxs-lookup"><span data-stu-id="bc26b-126">In most cases, the objects passed back and forth between the Windows Runtime and JavaScript do not change.</span></span>  <span data-ttu-id="bc26b-127">Ядро JavaScript сохраняет карту известных объектов.</span><span class="sxs-lookup"><span data-stu-id="bc26b-127">The JavaScript engine maintains a map of known objects.</span></span>  <span data-ttu-id="bc26b-128">Когда объект возвращается из среды выполнения Windows Runtime, он соответствует карте и если он не создан.</span><span class="sxs-lookup"><span data-stu-id="bc26b-128">When an object is returned from the Windows Runtime it is matched against the map, and if it does not exist a new object is created.</span></span>  <span data-ttu-id="bc26b-129">Следуйте той же процедуре объектов, которые представляют интерфейсы, возвращаемые методами среды выполнения Windows.</span><span class="sxs-lookup"><span data-stu-id="bc26b-129">The same procedure is followed for objects that represent interfaces that are returned by Windows Runtime methods.</span></span>  <span data-ttu-id="bc26b-130">Существует два типа исключений:</span><span class="sxs-lookup"><span data-stu-id="bc26b-130">There are two kinds of exceptions:</span></span>  
      
      *   <span data-ttu-id="bc26b-131">Объекты, возвращаемые из вызова Windows выполнения, а затем добавляли новые свойства \(expando\) не сохраняйте их при переносе в среду выполнения Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="bc26b-131">Objects that are returned from a Windows Runtime call, and then have new \(expando\) properties added, don't retain their new properties when they are passed back to the Windows Runtime.</span></span>  <span data-ttu-id="bc26b-132">Однако при возвращении в приложение JavaScript, так как они совпадают с существующим объектом, свойства возвращаемого объекта имеют свойства развертывания.</span><span class="sxs-lookup"><span data-stu-id="bc26b-132">However, when they are returned to the JavaScript app, because they're matched to the existing object, the returned object does have the expando properties.</span></span>  
      *   <span data-ttu-id="bc26b-133">Структуры и делегаты в Windows Runtime не могут быть отличаются от ранее использованных ранее структур и представителей.</span><span class="sxs-lookup"><span data-stu-id="bc26b-133">Structures and delegates in Windows Runtime can't be identified as identical to previously-used structures or delegates.</span></span>  <span data-ttu-id="bc26b-134">Каждый раз, когда возвращаются структура или представителя, получается новая ссылка.</span><span class="sxs-lookup"><span data-stu-id="bc26b-134">Every time a structure or delegate is returned, it gets a new reference.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="bc26b-135">Выделение имен</span><span class="sxs-lookup"><span data-stu-id="bc26b-135">Name collisions</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="bc26b-136">Несколько интерфейсов Windows Runtime могут иметь одинаковые имена.</span><span class="sxs-lookup"><span data-stu-id="bc26b-136">Multiple Windows Runtime interfaces may have members with the same names.</span></span>  <span data-ttu-id="bc26b-137">Если они объединены в один объект JavaScript (который может представлять класс выполнения или интерфейс), участники представляются с полными именами.</span><span class="sxs-lookup"><span data-stu-id="bc26b-137">If they are combined in a single JavaScript object (which can be a representation of a runtime class or an interface), the members are represented with fully-qualified names.</span></span>  <span data-ttu-id="bc26b-138">Вы можете позвонить этим членам, используя следующий синтаксис:</span><span class="sxs-lookup"><span data-stu-id="bc26b-138">You can call these members by using the following syntax:</span></span>  
      
      ```cpp
      Class["MemberName"](parameter)
      ```  
      
      <span data-ttu-id="bc26b-139">В приведенном ниже коде два интерфейса имеет метод рисования, а класс ы выполнения — внедряет оба интерфейса.</span><span class="sxs-lookup"><span data-stu-id="bc26b-139">In the following code, two interfaces have a Draw method, and a runtime class implements both interfaces.</span></span>  
      
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
      
      <span data-ttu-id="bc26b-140">Вот как можно вызвать приведенный выше код в JavaScript.</span><span class="sxs-lookup"><span data-stu-id="bc26b-140">Here is how you can call the above code in JavaScript.</span></span>  
      
      ```javascript
      var example = new ExampleObject();
      example["CollisionExample.InterfaceA.draw"](12);
      example["CollisionExample.InterfaceB.draw"]("hello");
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `Out` <span data-ttu-id="bc26b-141">параметры</span><span class="sxs-lookup"><span data-stu-id="bc26b-141">parameters</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="bc26b-142">Если метод выполнения Windows имеет несколько `out` параметров, в JavaScript метод JavaScript в качестве возвращаемого значения объектjaScript выполняется, а объект имеет свойства, соответствующие `out` параметру.</span><span class="sxs-lookup"><span data-stu-id="bc26b-142">If a Windows Runtime method has multiple `out` parameters, in JavaScript the method has a JavaScript object as its return value, and the object has properties that correspond to the `out` parameter.</span></span>  <span data-ttu-id="bc26b-143">Например, рассмотрим следующее подпись во сеанса Выполнения Windows в C++.</span><span class="sxs-lookup"><span data-stu-id="bc26b-143">For example, consider the following Windows Runtime signature in C++.</span></span>  
      
      ```cpp
      void ExampleMethod(
          [OutAttribute] char^ first,
          [OutAttribute] char^ second
      )
      ```  
      
      <span data-ttu-id="bc26b-144">Для этой подписи используется следующий вид:</span><span class="sxs-lookup"><span data-stu-id="bc26b-144">The JavaScript version of this signature is:</span></span>  
      
      ```javascript
      var returnValue = exampleMethod();
      ```  
      
      <span data-ttu-id="bc26b-145">В данном `returnValue` примере является объект JavaScript с двумя `first` полями `second` и.</span><span class="sxs-lookup"><span data-stu-id="bc26b-145">In this example, `returnValue` is a JavaScript object that has two fields: `first` and `second`.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      <span data-ttu-id="bc26b-146">Статические члены</span><span class="sxs-lookup"><span data-stu-id="bc26b-146">Static members</span></span>  
   :::column-end:::
   :::column span="3":::
      <span data-ttu-id="bc26b-147">Windows Runtime определяет как статические члены, так и участники экземпляра.</span><span class="sxs-lookup"><span data-stu-id="bc26b-147">The Windows Runtime defines both static members and instance members.</span></span>  <span data-ttu-id="bc26b-148">В JavaScript статические элементы добавляются к объекту, связанному с классом или интерфейсом выполнения Windows Runtime.</span><span class="sxs-lookup"><span data-stu-id="bc26b-148">In JavaScript, static members are added to the object that is associated with the Windows Runtime class or interface.</span></span>  
      
      ```javascript
      // Static method.
      var accel = Windows.Devices.Sensors.Accelerometer.getDefault();
      // Instance method.
      var reading = accel.getCurrentReading();
      ```  
   :::column-end:::
:::row-end:::  
    
<span data-ttu-id="bc26b-149">Дополнительные сведения о формате JavaScript основных типов Windows Runtime см. в [статье JavaScript, представляющее типы Управляемых типов Windows.][WindowsRuntimeJavascriptTypes]</span><span class="sxs-lookup"><span data-stu-id="bc26b-149">For more information about the JavaScript representation of Windows Runtime basic types, see [JavaScript Representation of Windows Runtime Types][WindowsRuntimeJavascriptTypes].</span></span>  

<!-- links -->  
 
[WindowsRuntimeJavascriptTypes]: ./javascript-representation-of-windows-runtime-types.md "Представление JavaScript типов среды выполнения Windows | Документы Майкрософт"

[WindowsUwpComponentsCreatingCpp]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-cpp "Компоненты среды выполнения Windows с C+++/CX | Документы Майкрософт"  
[WindowsUwpComponentsCreatingCsharpVb]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-csharp-and-visual-basic "Компоненты среды выполнения Windows с C# и Visual Basic | Документы Майкрософт"  

[MDNInt32array]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Int32Array "Int32Array | MDN"  