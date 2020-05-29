---
title: Обработка событий среды выполнения Windows в JavaScript
ms.custom: ''
ms.date: 04/01/2017
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.technology: windows-integration
ms.tgt_pltfrm: ''
ms.topic: article
helpviewer_keywords:
- JavaScript, Windows Runtime events
- Windows Runtime events [JavaScript]
ms.assetid: d9436aff-2c30-4846-b8df-eaa3e63fd75c
caps.latest.revision: 6
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: c3db0116a3d464c75fe754e73e41ff1d154f928e
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572857"
---
# Обработка событий среды выполнения Windows в JavaScript  

События среды выполнения Windows не представляются таким же образом в JavaScript, как в C++ или .NET Framework.  Они не являются свойствами класса, а представляют собой строковые идентификаторы (строчные), которые передаются в `addEventListener` методы и классы `removeEventListener` .  Например, вы можете добавить обработчик событий для события [геоPositionChanged][UwpWindowsGeolocationGeolocatorDevicesPositionChanged] , передав методу строку "PositionChanged" `Geolocator.addEventListener` .  

```javascript  
var locator = new Windows.Devices.Geolocation.Geolocator();
locator.addEventListener(
    "positionchanged",
    function (ev) {
        console.log("Got event");
    });
```  

Вы также можете задать `locator.onpositionchanged` свойство:  

```javascript
locator.onpositionchanged =
    function (ev) {
        console.log("Got event");
    };
```  

Еще одна разница между .NET и C++ и JavaScript — количеством параметров, полученных обработчиком событий.  В .NET/C++ обработчик принимает два: отправитель события и данные о событии.  В JavaScript эти два объекта объединены в один `Event` объект.  В приведенном ниже примере `ev` параметр имеет и отправителя события \ ( `target` свойство \), и свойства Data Events \ (здесь, просто `position` \).  Свойства данных события — это те, которые задокументированы для каждого события.  

```javascript
function (ev) {
    console.log("Sender:  " + ev.target);
    console.log("Position:  " +
        ev.position.latitude + "," +
        ev.position.longitude);
};
```  

> [!IMPORTANT]
> Функции среды выполнения Windows недоступны для приложений, работающих в Internet Explorer.  

## См. также  

[Использование среды выполнения Windows в JavaScript][WindowsRuntimeJavascript]  

 <!-- image links -->  

 <!-- links -->  

[WindowsRuntimeJavascript]: /microsoft-edge/windows-runtime/using-the-windows-runtime-in-javascript "Использование среды выполнения Windows в JavaScript"  

[UwpWindowsGeolocationGeolocatorDevicesPositionChanged]: /uwp/api/Windows.Devices.Geolocation.Geolocator#Windows_Devices_Geolocation_Geolocator_PositionChanged "Класс геоуказателей"  
