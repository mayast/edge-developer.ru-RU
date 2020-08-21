---
title: Обработка событий среды выполнения Windows в JavaScript
ms.custom: ''
ms.date: 07/29/2020
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
ms.openlocfilehash: fe44457206569c1e32c40514b4b186bec50d1e3c
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942160"
---
# Обработка событий среды выполнения Windows в JavaScript  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

События выполнения Windows Runtime не отражаются иначе в JavaScript, что и в C++ или .NET Framework.  Они не являются занятиями, но в них представлены строки \(нижний регистр\). `addEventListener` `removeEventListener`  Например, можно добавить маркер события для [события Geolocator.PositionChanged,][UwpWindowsGeolocationGeolocatorDevicesPositionChanged] передав `positionchanged` `Geolocator.addEventListener` строку метода.  

```javascript  
var locator = new Windows.Devices.Geolocation.Geolocator();
locator.addEventListener(
    "positionchanged",
    function (ev) {
        console.log("Got event");
    });
```  

Кроме того, свойство можно `locator.onpositionchanged` задать:  

```javascript
locator.onpositionchanged =
    function (ev) {
        console.log("Got event");
    };
```  

Еще одно различие между .NET/C++ и JavaScript — количество параметров, используемых обработчиком события.  В .NET/C+++ обработчик занимает два: отправитель события и данные событий.  В JavaScript два объединяются как один `Event` объект.  В следующем примере параметр может содержать отправитель события `ev` \(свойство\) и `target` свойства события \(здесь, `position` просто \).  Свойства данных события — это те, которые задокументированы для каждого события.  

```javascript
function (ev) {
    console.log("Sender: " + ev.target);
    console.log("Position: " +
        ev.position.latitude + "," +
        ev.position.longitude);
};
```  

> [!IMPORTANT]
> Функции выполнения Windows недоступны для приложений, работающих в Internet Explorer.  

## См. также  

[Использование среды выполнения Windows в JavaScript][WindowsRuntimeJavascript]  

 <!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Использование Windows Runtime в JavaScript | Документы Майкрософт"  

[UwpWindowsGeolocationGeolocatorDevicesPositionChanged]: /uwp/api/Windows.Devices.Geolocation.Geolocator#Windows_Devices_Geolocation_Geolocator_PositionChanged "Геолуокаративный класс | Документы Майкрософт"  
