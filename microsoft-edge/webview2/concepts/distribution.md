---
description: Варианты распространения при выпуске приложения с помощью Microsoft Edge WebView2
title: Распространение приложения Microsoft Edge WebView2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/10/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения WPF, WPF, EDGE, ICoreWebView2, ICoreWebView2Host, элемент управления "браузер", HTML Edge
ms.openlocfilehash: 3536b749c8a3389b5e247e42f53abf74a9e3281e
ms.sourcegitcommit: 0faf538d5033508af4320b9b89c4ed99872f0574
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/10/2020
ms.locfileid: "11010770"
---
# Распространение приложений с помощью WebView2  

Элемент управления WebView2 использует платформу Microsoft Edge \ (Chromium \).  При упаковке и распространении приложения перед запуском приложения убедитесь в том, что у вас установлена копия платформы или среды выполнения WebView2.  На следующей странице показано, как вы (разработчик) может гарантировать, что среда выполнения WebView2 установлена и использует два режима распространения для вашего приложения WebView2:  [Evergreen](#evergreen-distribution-mode) и [фиксированная версия](#fixed-version-distribution-mode).  

## Режим распространения Evergreen  

Режим распространения Evergreen гарантирует, что ваше приложение использует последние возможности и обновления для системы безопасности.  Режим распространения Evergreen имеет следующие характеристики.  

*   Веб-платформа автоматически обновляется без дополнительных усилий.  
*   Все приложения, которые используют режим распространения Evergreen, используют общую копию двоичных файлов платформы, что экономит место на диске.  

Есть несколько каналов, WebView2, что приложения могут использоваться в качестве веб-платформы.  По умолчанию WebView2 ориентирован на самый стабильный канал, доступный на устройстве, который соответствует минимальным требованиям к версии SDK для WebView2.  Следующие каналы перечислены в порядке от наибольшего к минимуму стабильных каналов.  

1.  Среда выполнения WebView2 \ (Предварительная версия)  
1.  Канал Microsoft Edge Beta  
1.  Канал Microsoft Edge Dev  
1.  Канал Microsoft Edge Canary    

> [!NOTE]
> Для большинства разработчиков рекомендуется использовать модель распространения Evergreen.  

> [!IMPORTANT]
> Стабильный канал Microsoft EDGE не является допустимым целевым объектом для WebView2, поэтому причины описаны ниже.  

Дополнительные сведения об управлении версиями можно найти в разделе [Управление версиями][ConceptsVersioning] и [Globals][ReferenceWin3209622WebviewIdl].  

### Общие сведения о среде выполнения WebView2 и установщике (Предварительная версия)  

Стабильный канал Microsoft Edge может не устанавливаться на всех компьютерах пользователей, на которых запускается приложение.  Вместо того, чтобы обязательно устанавливать Microsoft EDGE, приложение может использовать среду выполнения Evergreen WebView2 и установщик \ (Предварительная версия).  Среда выполнения WebView2 — это настраиваемая копия двоичных файлов Microsoft EDGE, которая используется для запуска приложений WebView2.  После установки исполняющей среды WebView2 пользователи не смогут использовать ее в качестве обычных браузеров.  Например, отсутствует ярлык на рабочем столе, элемент меню "Пуск", пользователи не смогут открывать окно браузера с помощью двоичных файлов среды выполнения и т. д.  Во всех приложениях Evergreen WebView2 на устройстве может использоваться единая установка среды выполнения Evergreen WebView2.  

Сегодня во время предварительного просмотра Evergreen WebView2 и канал разработки Microsoft Edge обновляются одновременно и имеют одинаковое построение.  В будущем в ходе предварительного просмотра WebView2 Teams планирует обновить среду выполнения WebView2 и соответствовать той же сборке, что и канал бета-версии Microsoft Edge.  В будущем, когда WebView2 приступает к общему доступу, Группа WebView2 Teams планирует обновлять среду выполнения WebView2 и соответствовать той же сборке, что и стабильный канал Microsoft Edge.  После завершения работы приложения должны использовать среду выполнения WebView2 в рабочей среде.  

> [!IMPORTANT]
> Не допускайте WebView2 приложения в производство во время предварительного просмотра.  

Разработчикам рекомендуется убедиться, что среда выполнения Evergreen WebView2 установлена перед запуском приложения. Ниже приведен пример рабочего процесса.  

1.  Скачайте последнюю версию [установщика среды выполнения Evergreen WebView2][Webview2Installer].  
1.  Включите установщик в установщик приложения или в средство обновления.  
1.  Во время установки или обновления приложения убедитесь, что среда выполнения Evergreen WebView2 уже установлена на компьютере пользователя, используя API [GetAvailableCoreWebView2BrowserVersionString](../reference/win32/0-9-622/webview2-idl.md#getavailablecorewebview2browserversionstring) и проверяя, имеет ли versionInfo значение null. Если этот параметр не установлен, установщик приложений может автоматически вызвать установщик среды выполнения из процесса с повышенными привилегиями или командной строки с помощью `MicrosoftEdgeWebView2RuntimeInstallerX64.exe /silent /install` . 

В зависимости от вашего сценария вам может потребоваться изменить описанный выше рабочий процесс.  Например, установщик приложения может загрузить установщик Evergreen WebView2 среды выполнения, вместо включения его в пакет приложения.  

> [!NOTE]
> Предварительная версия программы WebView2 Runtime и WebView2 среды выполнения.  Предварительный просмотр имеет ограниченную начальную область и доступен только в автономном режиме для установки на компьютере с Windows 10 на 64-разрядной версии.  В будущем поддержка Windows 7, x86 и ARM64 планируется.  

### Рекомендации по использованию среды выполнения WebView2 и нестабильных каналов Microsoft Edge  

При предварительной версии ознакомьтесь с приведенными ниже рекомендациями.  

*   Убедитесь, что для разработки и тестирования конвейера упаковки и распространителя используется [Среда выполнения Evergreen WebView2 и установщик][Webview2Installer] .  В будущем рабочее приложение должно включать установщик.  
*   Для разработки приложения вы можете использовать среду выполнения Evergreen WebView2.  Несмотря на то, что при переходе среды выполнения с канала разработки на канал Beta или стабильный канал, номер сборки среды выполнения может не соответствовать последним требованиям к предварительной версии SDK WebView2.  Если вы хотите использовать самую последнюю версию пакета SDK, установите канал Microsoft Edge Канарские Channel, чтобы убедиться, что на устройстве доступна совместимая сборка.  Дополнительные сведения об управлении версиями можно найти в разделе [Управление версиями][ConceptsVersioning].  
*   Чтобы протестировать веб-содержимое для обеспечения совместимости с изменениями в платформе, недоступными в стабильном канале, используйте соответствующий нестабильный канал.  

## Режим распространения фиксированной версии  

> [!NOTE]
> Модель распространения фиксированных версий в настоящее время недоступна.  

Для ограниченных сред существуют планы поддержки фиксированной версии (прежнее название — собственный режим распространения).  Режим распространения с фиксированной версией позволяет выбрать и упаковать определенную версию среды выполнения WebView2.  Режим распространения с фиксированной версией позволяет управлять тем, какая версия среды выполнения WebView2 используется приложением, и при обновлении компьютеров пользователей.  Режим распространения фиксированной версии не получает никаких автоматических обновлений, и вы должны запланировать применение обновлений вручную.  

<!-- links -->  

[ConceptsVersioning]: ./versioning.md "Общие сведения о версиях браузеров и WebView2 | Документы Microsoft"  
[ReferenceWin3209622WebviewIdl]: ../reference/win32/0-9-622/webview2-idl.md  "Globals | Документы Microsoft"  

[Webview2Installer]: https://developer.microsoft.com/microsoft-edge/webview2 "Установщик WebView2"  
