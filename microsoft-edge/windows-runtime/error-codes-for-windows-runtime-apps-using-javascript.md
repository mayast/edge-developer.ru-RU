---
title: Коды ошибок для приложений среды выполнения Windows, использующих JavaScript
ms.custom: ''
ms.date: 07/29/2020
ms.prod: microsoft-edge
ms.reviewer: ''
ms.suite: ''
ms.technology: windows-integration
ms.tgt_pltfrm: ''
ms.topic: article
f1_keywords:
- JavaScript, Windows Runtime error codes
- VS.WebClient.Help.APPHOST9601
- VS.WebClient.Help.APPHOST9602
- VS.WebClient.Help.APPHOST9603
- VS.WebClient.Help.APPHOST9604
- VS.WebClient.Help.APPHOST9605
- VS.WebClient.Help.APPHOST9606
- VS.WebClient.Help.APPHOST9607
- VS.WebClient.Help.APPHOST9608
- VS.WebClient.Help.APPHOST9610
- VS.WebClient.Help.APPHOST9611
- VS.WebClient.Help.APPHOST9613
- VS.WebClient.Help.APPHOST9614
- VS.WebClient.Help.APPHOST9615
- VS.WebClient.Help.APPHOST9616
- VS.WebClient.Help.APPHOST9617
- VS.WebClient.Help.APPHOST9618
- VS.WebClient.Help.APPHOST9619
- VS.WebClient.Help.APPHOST9620
- VS.WebClient.Help.APPHOST9623
- VS.WebClient.Help.APPHOST9624
- VS.WebClient.Help.APPHOST9626
ms.assetid: 4c6d4e90-602a-4b56-ae74-3458929da442
caps.latest.revision: 1
author: MSEdgeTeam
ms.author: msedgedevrel
manager: ''
ms.openlocfilehash: 7779da61da9f011e55eeb496c7332e5b7cd5a023
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942151"
---
# Коды ошибок для приложений среды выполнения Windows, использующих JavaScript  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

Ниже приведены коды ошибок, отображаемые консолью Microsoft Visual Studio для Windows при разработке приложений среды выполнения Windows с помощью JavaScript.  

| Ошибка | Комментарии |  
|:--- |:--- |  
| APPHOST9601: "Не удается загрузить *удаленный URI.*  Приложение не может загружать удаленный контент веб-контент в локальный контекст". | Дополнительные сведения о том, разрешено ли в контексте веб-контекст, см. в разделе "Функции и [ограничения".][PreviousVersionsWindowsAppsHh465373]  |  
| APPHOST9602: "'javascript:' является недопустимым значением атрибута и пропускается.  Не используйте URI javascript:' в локальном контексте". | По соображениям безопасности в локальном контексте нельзя использовать URI "javascript:".  Дополнительные сведения о разрешениях, разрешенных в локальном контексте, см. в разделе "Функции и [ограничения" в контексте.][PreviousVersionsWindowsAppsHh465373]  |  
| APPHOST9603: "Не удается загрузить подключаемый ActiveX с идентификатором *класса.*  Приложения не могут загружать ActiveX элементы управления". | Приложения Microsoft Runtime с помощью JavaScript не поддерживают пользовательские элементы Microsoft ActiveX controls.  Если вам нужен элемент управления пользовательского пользовательского доступа, используйте стандартный веб-элемент управления, библиотеку элементов управления или создайте собственный настраиваемый элемент управления.  Если вам нужно выполнить настраиваемую логику, создайте собственный объект Windows Runtime.  Сведения о других различиях HTML, CSS и JavaScript см. в [HTML, CSS и JavaScript.][PreviousVersionsWindowsAppsHh465380]  |  
| APPHOST9604: "Не удается найти *Uri,* так как в нем используется недопустимая кодировка символов.  Приложение может перемещаться только к файлам в кодировке UTF8". | Все HTML, JavaScript и CSS, обслуживаемые Windows Runtime, должны быть закодированы как 8-разрядный формат преобразования Юникод (UTF-8).  Сведения о других различиях HTML, CSS и JavaScript см. в [HTML, CSS и JavaScript.][PreviousVersionsWindowsAppsHh465380]  |  
| APPHOST9605: "Не удается перейти к *конечному* *URI,* так как URI находится в зоне безопасности более высокого уровня безопасности.  Вы не сможете перейти от зон, в зоне безопасности которой не нужно перейти от более низкого уровня защиты к зону, если только вы не перейдете к локальному URI контекстного URI из URI контекста и зарегистрировали локальный URI с помощью MSApp.addPublicLocalApplicationUri". | Дополнительные сведения см. в [веб-приложении MSApp.addPublicApplicationUri.][PreviousVersionsHh771917]  |  
| APPHOST9606: "Не удалось загрузить *uri,* так как в нем используется подключение HTTP, а элемент ms-подключений, доступный только по протоколу Ms-подключением).  При использовании элемента ms-подключений с помощью элемента мета-подключений разрешений, доступных только https-connections, разрешается только протокол HTTPS.  Используйте подключение HTTPS или, если безопасное подключение не требуется, удалите элемент метатеги". | Дополнительные сведения см. в [инструкциях по подключению https.][PreviousVersionsWindowsAppsHh452771]  |  
| APPHOST9607: "Приложению не удается запустить URI *на узле из-за* такой ошибки: *failureCode."* | В этой ошибке отсутствуют ресурс или недопустимые файлы.  |  
| APPHOST9608: "Приложению не удалось перейти на страницу о ней:пустая из-за ошибки *Code.* |  |  

| Ошибка | Комментарии |  
|:--- |:--- |  
| APPHOST9610: "Приложение обнаружило ошибку при подготовке к переходу на настраиваемую страницу обработки: *ошибкаCode."* |  |  
| APPHOST9611: "Приложению не удалось перейти на пользовательскую страницу ошибки из-за этой ошибки: *Код ошибки Code".* |  |  
| APPHOST9613: "Приложению не удалось перейти к *uriу,* поскольку в этой ошибке возникает *ошибка Code.* |  |  
| APPHOST9614: "Документ в нравится запрашивал ся в режиме *DOcMode,* но система применяет режим *текущего документа DocMode.*  Iframe будет использовать *текущий документ в режиме docMode".* | Дополнительные сведения об отображении удаленного веб-контента см. в [статье "Ссылки на внешние веб-страницы".][PreviousVersionsWindowsAppsHh780594]  |  
| APPHOST9615: "Приложению не удается скачать файл *на узле,* так как оно было вызвано программным путем за пределами локального контекста". | Это происходит, когда содержимое в контексте веб-контекст пытается скачать файл программно.  |  
| APPHOST9616: "Этот URI не может использовать Географическое расположение.  API географического расположения можно вызвать только из URI, который является частью пакета или включено в элемент ApplicationContentUris манифеста". | Дополнительные сведения о том, разрешено ли в контексте веб-контекст, см. в разделе "Функции и [ограничения".][PreviousVersionsWindowsAppsHh465373]  |  
| APPHOST9617: "Этот URI не льзется использовать API буфера обмена.  API-обмена можно вызвать только из URI, который является частью пакета или включен в элемент ApplicationContentUris манифеста". | Дополнительные сведения о том, разрешено ли в контексте веб-контекст, см. в разделе "Функции и [ограничения".][PreviousVersionsWindowsAppsHh465373]  |  
| APPHOST9618: "Этот URI нельзя использовать окно.dom.  Метод window.close можно вызвать только из упакованного контента, загруженного в схему URI ms-appx URI". | Дополнительные сведения о том, разрешено ли в контексте веб-контекст, см. в разделе "Функции и [ограничения".][PreviousVersionsWindowsAppsHh465373]  |  
| APPHOST9619: "Приложению не удается перейти к *Uri,* так как в контексте веб-контекста не может быть документ верхнего уровня приложения.  Загрузите страницу в конфет". | Перейти к странице верхнего уровня невозможно, но в приложении оно может отображаться в [результатах.][MDNIframe]  Дополнительные сведения об отображении удаленного веб-контента см. в [статье "Ссылки на внешние веб-страницы".][PreviousVersionsWindowsAppsHh780594]  |  

| Ошибка | Комментарии |  
|:--- |:--- |  
| APPHOST9620: "Это приложение закрыто, так как оно использовано подключением http, и элемент meta существует только с помощью значка MS-подключений.  При использовании элемента ms-подключений с помощью элемента мета-подключений разрешений, доступных только https-connections, разрешается только протокол HTTPS.  Используйте подключение HTTPS или, если безопасное подключение не требуется, удалите элемент метатеги". | Дополнительные сведения см. в [инструкциях по подключению https.][PreviousVersionsWindowsAppsHh452771]  |  
| APPHOST9623: "Приложению не удалось *устранить URL-адрес* из-за *ошибки*Code. | Чаще всего эта ошибка возникает из-за отсутствия файла.  |  
| APPHOST9624: "Сценарий не может использовать сценарий для загрузки *URL-адреса,* так как URL-адрес запускает другое приложение.  Запустить другое приложение можно только прямо с помощью действий пользователя". | Приложения не могут запускать другие приложения.  Другие приложения могут запускаться пользователем, когда приложение внедряет определенные контракты.  Дополнительные сведения: [Контракты приложений и расширения][PreviousVersionsWindowsAppsHh464906].  |  
| APPHOST9626: "Обнаружена прямая ссылка на файл `ms-appx://1d33240b-0b00-40e4-a416-a4750c48787f/ja-jp\images\logo.scale-140.png` ресурса.  Эта ссылка приводит к сбоям при использовании вне среды отладки". | Из-за пути к файлу этот PNG-файл счается как локализованный ресурс, из-за чего неудачно возникает `logo.scale-140.png` ошибка непосредственно.  Узнайте [все о глобализации веб-приложения (HTML),][PreviousVersionsWindowsAppsHh465006] если вы планировали использовать этот файл в качестве ресурса.  В противном случае попробуйте переименовать проблемный каталог.  |  

## См. также  

[Использование среды выполнения Windows в JavaScript][WindowsRuntimeJavascript]  

<!-- links -->  

[WindowsRuntimeJavascript]: ./using-the-windows-runtime-in-javascript.md "Использование Windows Runtime в JavaScript | Документы Майкрософт"  

[UwpWindowsGeolocationGeolocatorDevicesPositionChanged]: /uwp/api/Windows.Devices.Geolocation.Geolocator#Windows_Devices_Geolocation_Geolocator_PositionChanged "Геолуокаративный класс | Документы Майкрософт"  

[PreviousVersionsHh771917]: /previous-versions/hh771917(v=vs.85) "addPublicLocalApplicationUri | Документы Майкрософт"  

[PreviousVersionsWindowsAppsHh452771]: /previous-versions/windows/apps/hh452771(v=win.10) "Как подключаться к HTTPS (HTML) | Документы Майкрософт"  
[PreviousVersionsWindowsAppsHh464906]: /previous-versions/windows/apps/hh464906(v=win.10) "Договоры и расширения приложений (приложения Windows Runtime) | Документы Майкрософт"  
[PreviousVersionsWindowsAppsHh465006]: /previous-versions/windows/apps/hh465006(v=win.10) "Глобализация веб-приложения (HTML) | Документы Майкрософт"  
[PreviousVersionsWindowsAppsHh465373]: /previous-versions/windows/apps/hh465373(v=win.10) "Возможности и ограничения по контексту (HTML) | Документы Майкрософт"  
[PreviousVersionsWindowsAppsHh465380]: /previous-versions/windows/apps/hh465380(v=win.10) "Функции и различия (HTML) | Документы Майкрософт"  
[PreviousVersionsWindowsAppsHh780594]: /previous-versions/windows/apps/hh780594(v=win.10) "Как создать ссылку на внешние веб-страницы (HTML) | Документы Майкрософт"  

[MDNIframe]: https://developer.mozilla.org/docs/Web/HTML/Element/iframe "<iframe>: элемент встроенной рамки | MDN"  
