---
title: Коды ошибок для приложений среды выполнения Windows, использующих JavaScript
ms.custom: ''
ms.date: 04/01/2020
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
ms.openlocfilehash: 7aad8577d79bc5612f526e4e2bf1ceb0f2c2929a
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10572858"
---
# Коды ошибок для приложений среды выполнения Windows, использующих JavaScript  

Ниже указаны коды ошибок, которые отображаются на консоли Microsoft Visual Studio при разработке приложений среды выполнения Windows с помощью JavaScript.  

| Ошибка | Комментарии |  
|:--- |:--- |  
| APPHOST9601: "не удается загрузить *remoteURI*.  Приложению не удается загрузить удаленное веб-содержимое в локальном контексте. | Дополнительные сведения о том, какие действия разрешены в веб-контексте, можно найти в разделе [функции и ограничения по контексту][PreviousVersionsWindowsAppsHh465373].  |  
| APPHOST9602: "' JavaScript:" является недопустимым значением атрибута и будет игнорироваться.  Не используйте URI "JavaScript:" в локальном контексте. | По соображениям безопасности нельзя использовать URI "JavaScript:" в локальном контексте.  Дополнительные сведения о том, какие действия разрешены в локальном контексте, можно найти в разделе [функции и ограничения по контексту][PreviousVersionsWindowsAppsHh465373].  |  
| APPHOST9603: "не удается загрузить плагин ActiveX с ИДЕНТИФИКАТОРом класса *classID*.  Приложения не могут загружать элементы ActiveX. " | Приложения среды выполнения Windows с использованием JavaScript не поддерживают пользовательские Microsoft ActiveXcontrols.  Если вам нужен элемент управления пользовательского интерфейса, используйте стандартный веб-элемент управления, библиотеку элементов управления или создайте собственный пользовательский элемент управления.  Если вы хотите выполнить специальную логику, вместо этого создайте настраиваемый объект среды выполнения Windows.  Сведения о других различиях HTML, CSS и JavaScript можно найти в статье как в [HTML, CSS, так и на языке JavaScript и отличиях][PreviousVersionsWindowsAppsHh465380].  |  
| APPHOST9604: "не удается перейти к *URI* , так как он использует недействительную кодировку знаков.  Приложение может переходить только к файлам в кодировке UTF8. | Все HTML, JavaScript и CSS, доступ к которым осуществляется средой выполнения Windows, должны быть закодированы как 8-разрядный формат преобразования Юникод (UTF-8).  Сведения о других различиях HTML, CSS и JavaScript можно найти в статье как в [HTML, CSS, так и на языке JavaScript и отличиях][PreviousVersionsWindowsAppsHh465380].  |  
| APPHOST9605: "не удается перейти к *targetURI* из *sourceUri* из-за того, что конечный URI находится в более высокой зоне безопасности.  Вы не можете переходить от зоны с более низким уровнем безопасности для зоны более высокой безопасности, если только вы не переходите на URI локального контекста из URI веб-контекста, и вы зарегистрировали URI локального контекста с помощью метода MSApp. addPublicLocalApplicationUri. | Дополнительные сведения можно найти в разделе [MSApp. addPublicLocalApplicationUri][PreviousVersionsHh771917].  |  
| APPHOST9606: "не удается загрузить *универсальный код ресурса (URI)* , так как он использует HTTP-соединение и присутствует элемент meta" только по протоколу HTTPS ".  Только HTTPS-соединение разрешено, только если используется элемент meta "только по протоколу HTTPS".  Используйте HTTPS-соединение или, если вам не требуется безопасное соединение, удалите элемент meta. | Дополнительные сведения о том, [как использовать HTTPS, можно найти в разделе требования][PreviousVersionsWindowsAppsHh452771].  |  
| APPHOST9607: "приложению не удается запустить URI на *URI* из-за следующей ошибки: *failureCode*". | Причиной этой ошибки являются отсутствующий ресурс или недопустимый файл.  |  
| APPHOST9608: "приложению не удалось перейти на страницу about: Blank из-за следующей ошибки: *ErrorCode*." |  |  

| Ошибка | Комментарии |  
|:--- |:--- |  
| APPHOST9610: "приложение обнаружило ошибку при подготовке к переходу на настраиваемую страницу ошибки: *ErrorCode*." |  |  
| APPHOST9611: "приложению не удалось перейти на настраиваемую страницу ошибки из-за следующей ошибки: *ErrorCode*." |  |  
| APPHOST9613: "приложению не удалось перейти к *URI* из-за следующей ошибки: *ErrorCode*." |  |  
| APPHOST9614: "документ в IFRAME запросил режим *requestedDocMode* doc, но система принудительно обеспечивает режим *currentDocMode* doc.  IFRAME будет использовать режим *currentDocMode* doc. " | Дополнительные сведения о том, как отображать удаленное веб-содержимое, можно найти [в статье Создание связи с внешними веб-страницами][PreviousVersionsWindowsAppsHh780594].  |  
| APPHOST9615: "приложение не может скачать файл на *URI* , так как оно было вызвано программным образом за пределами локального контекста". | Возникает, когда содержимое в веб-контексте пытается загрузить файл программными средствами.  |  
| APPHOST9616: "Этот универсальный код ресурса (URI) не может использовать API-интерфейсы геоположения.  API геоположения можно вызывать только из URI, который является частью пакета или включен в элемент ApplicationContentUris манифеста. | Дополнительные сведения о том, какие действия разрешены в веб-контексте, можно найти в разделе [функции и ограничения по контексту][PreviousVersionsWindowsAppsHh465373].  |  
| APPHOST9617: "Этот универсальный код ресурса (URI) не может использовать API буфера обмена.  API буфера обмена можно вызывать только из URI, который является частью пакета или включен в элемент ApplicationContentUris манифеста. | Дополнительные сведения о том, какие действия разрешены в веб-контексте, можно найти в разделе [функции и ограничения по контексту][PreviousVersionsWindowsAppsHh465373].  |  
| APPHOST9618: "Этот URI не может использовать Window. Close.  Метод Window. Close может вызываться только из упакованного содержимого, загруженного с помощью схемы URI ms-appx. | Дополнительные сведения о том, какие действия разрешены в веб-контексте, можно найти в разделе [функции и ограничения по контексту][PreviousVersionsWindowsAppsHh465373].  |  
| APPHOST9619: "приложение не может перейти к *URI* , так как страница в веб-контексте не может быть документом верхнего уровня приложения.  Вместо этого загрузите страницу в IFRAME. " | Вы не можете перемещаться по странице верхнего уровня на удаленную веб-страницу, но ваше приложение может отображать веб-страницу в окне [IFRAME][MDNIframe].  Дополнительные сведения о том, как отображать удаленное веб-содержимое, можно найти [в статье Создание связи с внешними веб-страницами][PreviousVersionsWindowsAppsHh780594].  |  

| Ошибка | Комментарии |  
|:--- |:--- |  
| APPHOST9620: "это приложение было закрыто, так как оно использовало HTTP-соединение, а элемент meta" MS-HTTPS-Connections-only "присутствует.  Только HTTPS-соединение разрешено, только если используется элемент meta "только по протоколу HTTPS".  Используйте HTTPS-соединение или, если вам не требуется безопасное соединение, удалите элемент meta. | Дополнительные сведения о том, [как использовать HTTPS, можно найти в разделе требования][PreviousVersionsWindowsAppsHh452771].  |  
| APPHOST9623: сообщение об ошибке "приложению не удалось разрешить *URL-адрес* в результате ошибки: *ErrorCode*". | Распространенной причиной этой ошибки является отсутствующий файл.  |  
| APPHOST9624: "приложение не может использовать сценарий для *загрузки URL URL* -адреса, так как URL-адрес запускает другое приложение.  Запускать другое приложение может только непосредственное взаимодействие с пользователем. | Приложения не могут запускать другие приложения напрямую.  Другие приложения могут запускаться пользователем, когда приложение реализует определенные контракты.  Дополнительные сведения: [Контракты приложений и расширения][PreviousVersionsWindowsAppsHh464906].  |  
| APPHOST9626: обнаружена прямая ссылка на файл ресурсов `ms-appx://1d33240b-0b00-40e4-a416-a4750c48787f/ja-jp\images\logo.scale-140.png` .  Эта ссылка приводит к сбоям при использовании за пределами среды отладки. | Из-за пути к файлу `logo.scale-140.png` этот файл PNG рассматривается как локализованный ресурс, что приводит к неявной ссылке на эти локализованные ресурсы.  Если вы планируете использовать этот файл в качестве языкового ресурса, ознакомьтесь с [разрешениим глобализации вашего приложения (HTML)][PreviousVersionsWindowsAppsHh465006] .  В противном случае попробуйте переименовать каталог с проблемными именами.  |  

## См. также  

[Использование среды выполнения Windows в JavaScript][WindowsRuntimeJavascript]  

<!-- image links -->  

<!-- links -->  

[WindowsRuntimeJavascript]: /microsoft-edge/windows-runtime/using-the-windows-runtime-in-javascript "Использование среды выполнения Windows в JavaScript"  

[UwpWindowsGeolocationGeolocatorDevicesPositionChanged]: /uwp/api/Windows.Devices.Geolocation.Geolocator#Windows_Devices_Geolocation_Geolocator_PositionChanged "Класс геоуказателей"  

[PreviousVersionsHh771917]: /previous-versions/hh771917(v=vs.85) "метод addPublicLocalApplicationUri"  

[PreviousVersionsWindowsAppsHh452771]: /previous-versions/windows/apps/hh452771(v=win.10) "Как сделать обязательным подключение по протоколу HTTPS (HTML)"  
[PreviousVersionsWindowsAppsHh464906]: /previous-versions/windows/apps/hh464906(v=win.10) "Контракты и расширения приложений (приложения среды выполнения Windows)"  
[PreviousVersionsWindowsAppsHh465006]: /previous-versions/windows/apps/hh465006(v=win.10) "Глобализация приложения (HTML)"  
[PreviousVersionsWindowsAppsHh465373]: /previous-versions/windows/apps/hh465373(v=win.10) "Функции и ограничения по контексту (HTML)"  
[PreviousVersionsWindowsAppsHh465380]: /previous-versions/windows/apps/hh465380(v=win.10) "Возможности HTML, CSS и JavaScript и отличия (HTML)"  
[PreviousVersionsWindowsAppsHh780594]: /previous-versions/windows/apps/hh780594(v=win.10) "Связывание с внешними веб-страницами (HTML)"  

[MDNIframe]: https://developer.mozilla.org/docs/Web/HTML/Element/iframe "<> IFRAME: элемент встроенной рамки | MDN"  
