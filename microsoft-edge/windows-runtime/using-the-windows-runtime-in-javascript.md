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
# Использование среды выполнения Windows в JavaScript  

При написании приложения универсальной платформы Windows (UWP) можно использовать классы, методы и свойства среды выполнения Windows в большинстве тем же способом, что и использование собственных объектов, методов и свойств JavaScript.  Этот раздел содержит сведения о вводе и ссылках на разделы, в которых описаны основные принципы использования API среды выполнения Windows в JavaScript, в том числе сведения о представлениях типов среды выполнения Windows, способах использования асинхронных методов среды выполнения Windows, а также о том, как прослушивать события среды выполнения Windows и обрабатывать их.  

Для общеязыковой документации ознакомьтесь с библиотекой [ссылок JavaScript][MDNJavascriptReference] MDN.  

> [!IMPORTANT]
> Функции среды выполнения Windows недоступны для приложений, работающих в Internet Explorer.  

## Справочная документация по среде выполнения Windows  

Справочная документация приведена в [справочнике среды выполнения Windows][UwpApiIndex].  Примеры кода доступны в JavaScript, а также в C++, C# и Visual Basic.  

## Написание компонентов среды выполнения Windows на C++, C# или Visual Basic  

Инструкции и рекомендации по написанию компонентов среды выполнения Windows, которые можно использовать в JavaScript, приведены в разделе [Создание компонентов среды выполнения Windows в C++][WindowsUwpWinrtCpp] и [Создание компонентов среды выполнения Windows в C# и Visual Basic][WindowsUwpWinrtCsharpVb].  

## Правила использования регистров в функциях среды выполнения Windows  

Соглашения о регистре для функций среды выполнения Windows в JavaScript немного отличаются от используемых в других языках:  

*   Пространства имен и классы находятся в стиле Pascal.  
    
    ```javascript
    Windows.Deployment.PackageInfo;
    ```  
    
*   Члены классов, в том числе методы и свойства, а также члены структур и перечислений, имеют в стиле Camel:  
    
    ```javascript
    Deployment.PackageInfo.createPackage();
    ```  
    
*   Имена событий записываются в строчных буквах:  
    
    ```javascript
    dataTransferManager.ontargetapplicationchosen;
    ```  

## См. также  

[Рекомендации по использованию API среды выполнения Windows][WindowsRuntimeConsiderationsApi]  
[Использование асинхронных методов среды выполнения Windows][WindowsRuntimeAsynchronousMethods]   
[Обработка событий среды выполнения Windows в JavaScript][WindowsRuntimeEventsJavascript]   
[Представление типов среды выполнения Windows в JavaScript][WindowsRuntimeJavascriptTypes]   
[Проекция JavaScript в среде выполнения Windows DateTime и TimeSpan][WindowsRuntimeDatetimeTimespan]  
 
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
