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
# Рекомендации по использованию API среды выполнения Windows  

Вы можете использовать практически каждый элемент API среды выполнения Windows в JavaScript.  Однако есть некоторые аспекты представления JavaScript элементов среды выполнения Windows, которые следует помнить.  

> [!IMPORTANT]
> Сведения о создании компонентов среды выполнения Windows в C++, C# или Visual Basic и их использовании в JavaScript можно найти в разделе [Создание компонентов среды выполнения Windows в c++][WindowsUwpComponentsCreatingCpp] и [Создание компонентов среды выполнения Windows в C# и Visual Basic][WindowsUwpComponentsCreatingCsharpVb].  

## Особые случаи в представлении JavaScript типов среды выполнения Windows  

*   Строки: неинициализированная строка передается методу среды выполнения Windows в качестве строки "uninitial", а строковое значение `null` передается как строка "null".  \ (Это справедливо каждый раз, `null` когда `undefined` какое-либо значение приводится к строке. \) перед передачей строки методу среды выполнения Windows следует инициализировать ее как пустую строку \ ("" \ ").  
*   Интерфейсы: невозможно реализовать интерфейс среды выполнения Windows в JavaScript.  
*   Массивы: массивы среды выполнения Windows не изменяются в размерах, поэтому методы, изменяющие размер массивов в JavaScript, не работают в массивах среды выполнения Windows.  
*   Массивы: Если вы передаете значение массива JavaScript методу среды выполнения Windows, копируется массив.  Метод среды выполнения Windows не может изменить массив или его члены и вернуть его в приложение JavaScript.  Однако вы можете использовать типизированные массивы \ (например, [Int32Array Object][MDNInt32array]\), которые не копируются.  
*   Структуры: структуры среды выполнения Windows — это объекты в JavaScript.  Если вы хотите передать структуру среды выполнения Windows в метод среды выполнения Windows, не создавайте экземпляр структуры с помощью `new` ключевого слова.  Вместо этого создайте объект и добавьте соответствующие члены и их значения.  Имена участников должны быть в стиле Camel: `SomeStruct.firstMember` .  
*   Объекты: объекты JavaScript не совпадают с объектами управляемого кода \ ( `System.Object` \).  Вы не можете передать объект JavaScript методу среды выполнения Windows, для которого требуется `System.Object` .  
*   Идентификация объекта: в большинстве случаев объекты, передаваемые между средой выполнения Windows и JavaScript, не изменяются.  Механизм JavaScript поддерживает схему известных объектов.  Когда объект возвращается из среды выполнения Windows, он сопоставляется с картой и, если он не существует, создается новый объект.  Эти же действия выполняются для объектов, представляющих интерфейсы, возвращаемые методами среды выполнения Windows.  Существует два типа исключений.  

    *   Объекты, возвращаемые при вызове среды выполнения Windows, и новые свойства \ (expando \), не сохраняются при передаче обратно в среду выполнения Windows.  Тем не менее, когда они возвращаются в приложение JavaScript, так как они соответствуют существующему объекту, возвращаемый объект имеет свойства expando.  
    *   Структуры и делегаты в среде выполнения Windows не могут идентифицироваться так же, как и ранее использованные структуры или делегаты.  Каждый раз, когда возвращается функция Structure или делегата, она получает новую ссылку.  

*   Конфликты имен: несколько интерфейсов среды выполнения Windows могут содержать члены с одинаковыми именами.  Если они объединены в один объект JavaScript (который может быть представлением класса среды выполнения или интерфейса), то члены представлены с полными именами.  Чтобы вызвать эти члены, используйте следующий синтаксис:  
    
    ```cpp
    Class["MemberName"](parameter)
    ```  
    
    В следующем коде у двух интерфейсов есть метод Draw, а в классе среды выполнения реализованы оба интерфейса.  
    
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
    
    Вот как можно вызвать вышеприведенный код в JavaScript.  
    
    ```javascript
    var example = new ExampleObject();
    example["CollisionExample.InterfaceA.draw"](12);
    example["CollisionExample.InterfaceB.draw"]("hello");
    ```  
    
*   `Out` параметры: Если метод среды выполнения Windows имеет несколько `out` параметров, в JavaScript этот метод имеет объект JavaScript в качестве возвращаемого значения и объект имеет свойства, соответствующие `out` параметру.  Например, можно использовать следующую подпись среды выполнения Windows в C++.  
    
    ```cpp
    void ExampleMethod(
      [OutAttribute] char^ first,
      [OutAttribute] char^ second
    )
    ```  
    
    Версия JavaScript этой сигнатуры:  
    
    ```javascript
    var returnValue = exampleMethod();
    ```  
    
    В этом примере `returnValue` — объект JavaScript, имеющий два поля: `first` и `second` .  
    
*   Статические члены: среда выполнения Windows определяет статические члены и члены экземпляра.  В JavaScript статические члены добавляются в объект, связанный с классом или интерфейсом среды выполнения Windows.  
    
    ```javascript
    // Static method.
    var accel = Windows.Devices.Sensors.Accelerometer.getDefault();
    // Instance method.
    var reading = accel.getCurrentReading();
    ```  
    
Дополнительные сведения о представлении JavaScript основных типов среды выполнения Windows можно найти в [представлении JavaScript типов среды выполнения Windows][WindowsRuntimeJavascriptTypes].  

<!-- image links -->  

<!-- links -->  
 
[WindowsRuntimeJavascriptTypes]: /microsoft-edge/windows-runtime/javascript-representation-of-windows-runtime-types "Представление типов среды выполнения Windows в JavaScript"

[WindowsUwpComponentsCreatingCpp]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-cpp "Компоненты среды выполнения Windows с C++/CX"  
[WindowsUwpComponentsCreatingCsharpVb]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-csharp-and-visual-basic "Компоненты среды выполнения Windows в C# и Visual Basic"  

[MDNInt32array]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Int32Array "Int32Array | MDN"  