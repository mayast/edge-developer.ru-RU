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
# Использование среды выполнения Windows в JavaScript  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

При создании универсальной платформы Windows \(UWP\) вы можете использовать классы Среды выполнения, методы и свойства Windows так же, как и встроенные объекты JavaScript, методы и свойства.  В этой статье приведены общие сведения об основных понятиях использования API среды выполнения Windows в JavaScript JavaScript, в том числе объяснение типов Windows Runtime, а также обработке методов Windows Runtime и обработке событий Windows Runtime.  

Для общего языка можно ознакомиться с библиотекой [JavaScript.][MDNJavascriptReference]  

> [!IMPORTANT]
> Функции выполнения Windows недоступны для приложений, работающих в Internet Explorer.  

## Справочная документация windows  

Сведения для справки см. в [справке по Windows.][UwpApiIndex]  Примеры кодов доступны в JavaScript, а также в C++, C#и Visual Basic.  

## Написание компонентов среды выполнения Windows в C++, C#или Visual Basic  

Инструкции и рекомендации по созданию компонентов среды выполнения Windows, которые можно использовать в JavaScript, см. в статье ["Создание компонентов среды выполнения Windows в C++ и][WindowsUwpWinrtCpp] [создание компонентов среды выполнения в C# и Visual Basic".][WindowsUwpWinrtCsharpVb]  

## Соглашения с возможностями среды выполнения Windows  

Кассовать соглашения для средств среды выполнения Windows в JavaScript отличаются от языков, доступных на других языках:  

*   Имена и занятия присутствуют в пассивах:  
    
    ```javascript
    Windows.Deployment.PackageInfo;
    ```  
    
*   Участники класса, включая методы и свойства, а также участники структур и перечислений, в камере применяются следующие камеры:  
    
    ```javascript
    Deployment.PackageInfo.createPackage();
    ```  
    
*   Имена событий отображаются в нижнем регистре.  
    
    ```javascript
    dataTransferManager.ontargetapplicationchosen;
    ```  

## См. также  

[Рекомендации по использованию API среды выполнения Windows][WindowsRuntimeConsiderationsApi]  
[Использование асинхронных методов среды выполнения Windows][WindowsRuntimeAsynchronousMethods]   
[Обработка событий среды выполнения Windows в JavaScript][WindowsRuntimeEventsJavascript]   
[Представление типов среды выполнения Windows в JavaScript][WindowsRuntimeJavascriptTypes]   
[JavaScript Project of Windows Runtime and TimeSpan][WindowsRuntimeDatetimeTimespan]  

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
