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
# Рекомендации по использованию API среды выполнения Windows  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Теперь можно использовать практически все элементы API выполнения Windows в JavaScript.  Однако некоторые аспекты элементов во время выполнения JavaScript элементов Windows, которые необходимо помнить.  

> [!IMPORTANT]
> Сведения о создании компонентов среды выполнения Windows в C++, C#или Visual Basic и использовании их в JavaScript см. в статье ["Создание компонентов среды выполнения Windows в C++][WindowsUwpComponentsCreatingCpp] и создание компонентов среды выполнения [в C# и Visual Basic.][WindowsUwpComponentsCreatingCsharpVb]  

## Особые случаи в типах JavaScript для Windows Runtime  

:::row:::
   :::column span="1":::
      Строки  
   :::column-end:::
   :::column span="3":::
      Неинициализированная строка служит методом среды выполнения Windows, а строка "Unsetd" в качестве `null` строки "Null" является строкой "Null".  \(Это значение действительно принадлежат к `null` `undefined` строке.\) Перед аналогичным способом Windows, следует инициализировать ее как пустую строку \("\).  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Интерфейсы  
   :::column-end:::
   :::column span="3":::
      Интерфейс среды выполнения Windows невозможно внедрить в JavaScript.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Массивы  
   :::column-end:::
   :::column span="3":::
      Массивы Windows Runtime не изменяются, поэтому методы изменения размера массивов в JavaScript не работают для массивов Windows Runtime.  
      *   Массивы: при переносе значения массива JavaScript в метод выполнения Windows этот макрос копируется.  Метод среды выполнения Windows не может изменять массив или его элементы и вернуть его в приложение JavaScript.  Однако можно использовать тип \(например, [Int32Array][MDNInt32array]\), которые не копируются.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Структуры  
   :::column-end:::
   :::column span="3":::
      Структуры выполнения Windows являются объектами в JavaScript.  Если вы хотите сделать структуру Windows Runtime методом Windows Runtime, не используйте ключевое `new` слово.  Вместо этого создайте объект и добавьте необходимых участников и их значения.  В отличие от имен участников должны быть названы `SomeStruct.firstMember` так:  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Объекты  
   :::column-end:::
   :::column span="3":::
      Объекты JavaScript отличаются от объектов управляемых кодов \( `System.Object` \).  Объект JavaScript невозможно перенести в метод выполнения Windows, который `System.Object` требуется.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Удостоверение объекта  
   :::column-end:::
   :::column span="3":::
      В большинстве случаев объекты, переданные как в передаче, так и между windows Runtime и JavaScript, не изменяются.  Ядро JavaScript сохраняет карту известных объектов.  Когда объект возвращается из среды выполнения Windows Runtime, он соответствует карте и если он не создан.  Следуйте той же процедуре объектов, которые представляют интерфейсы, возвращаемые методами среды выполнения Windows.  Существует два типа исключений:  
      
      *   Объекты, возвращаемые из вызова Windows выполнения, а затем добавляли новые свойства \(expando\) не сохраняйте их при переносе в среду выполнения Windows Runtime.  Однако при возвращении в приложение JavaScript, так как они совпадают с существующим объектом, свойства возвращаемого объекта имеют свойства развертывания.  
      *   Структуры и делегаты в Windows Runtime не могут быть отличаются от ранее использованных ранее структур и представителей.  Каждый раз, когда возвращаются структура или представителя, получается новая ссылка.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Выделение имен  
   :::column-end:::
   :::column span="3":::
      Несколько интерфейсов Windows Runtime могут иметь одинаковые имена.  Если они объединены в один объект JavaScript (который может представлять класс выполнения или интерфейс), участники представляются с полными именами.  Вы можете позвонить этим членам, используя следующий синтаксис:  
      
      ```cpp
      Class["MemberName"](parameter)
      ```  
      
      В приведенном ниже коде два интерфейса имеет метод рисования, а класс ы выполнения — внедряет оба интерфейса.  
      
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
      
      Вот как можно вызвать приведенный выше код в JavaScript.  
      
      ```javascript
      var example = new ExampleObject();
      example["CollisionExample.InterfaceA.draw"](12);
      example["CollisionExample.InterfaceB.draw"]("hello");
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      `Out` параметры  
   :::column-end:::
   :::column span="3":::
      Если метод выполнения Windows имеет несколько `out` параметров, в JavaScript метод JavaScript в качестве возвращаемого значения объектjaScript выполняется, а объект имеет свойства, соответствующие `out` параметру.  Например, рассмотрим следующее подпись во сеанса Выполнения Windows в C++.  
      
      ```cpp
      void ExampleMethod(
          [OutAttribute] char^ first,
          [OutAttribute] char^ second
      )
      ```  
      
      Для этой подписи используется следующий вид:  
      
      ```javascript
      var returnValue = exampleMethod();
      ```  
      
      В данном `returnValue` примере является объект JavaScript с двумя `first` полями `second` и.  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      Статические члены  
   :::column-end:::
   :::column span="3":::
      Windows Runtime определяет как статические члены, так и участники экземпляра.  В JavaScript статические элементы добавляются к объекту, связанному с классом или интерфейсом выполнения Windows Runtime.  
      
      ```javascript
      // Static method.
      var accel = Windows.Devices.Sensors.Accelerometer.getDefault();
      // Instance method.
      var reading = accel.getCurrentReading();
      ```  
   :::column-end:::
:::row-end:::  
    
Дополнительные сведения о формате JavaScript основных типов Windows Runtime см. в [статье JavaScript, представляющее типы Управляемых типов Windows.][WindowsRuntimeJavascriptTypes]  

<!-- links -->  
 
[WindowsRuntimeJavascriptTypes]: ./javascript-representation-of-windows-runtime-types.md "Представление JavaScript типов среды выполнения Windows | Документы Майкрософт"

[WindowsUwpComponentsCreatingCpp]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-cpp "Компоненты среды выполнения Windows с C+++/CX | Документы Майкрософт"  
[WindowsUwpComponentsCreatingCsharpVb]: /windows/uwp/winrt-components/creating-windows-runtime-components-in-csharp-and-visual-basic "Компоненты среды выполнения Windows с C# и Visual Basic | Документы Майкрософт"  

[MDNInt32array]: https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Int32Array "Int32Array | MDN"  