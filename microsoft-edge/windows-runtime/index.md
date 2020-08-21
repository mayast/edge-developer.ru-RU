---
description: Используйте среду выполнения Windows Runtime (WinRT), чтобы звонить из приложения JavaScript.
title: Среда выполнения Windows (WinRT) для JavaScript
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/29/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: windows-integration
keywords: Среда выполнения Windows, WinRT, PWA, JavaScript
ms.openlocfilehash: e4b6eab4ecfbd26ccda8ef1c6e51a7a30dfaecfc
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942206"
---
# Среда выполнения Windows (WinRT) для JavaScript  

[!INCLUDE [deprecation-note](../includes/legacy-edge-note.md)]  

[Среда выполнения Windows Runtime](/windows/uwp/get-started/universal-application-platform-guide#how-the-universal-windows-platform-relates-to-windows-runtime-apis) \(или просто WinRT\) — это набор встроенных API, которые демонстрируют [Windows 10 device families](/uwp/extension-sdks/device-families-overview) [универсальные приложения платформы Windows](/windows/uwp/get-started/universal-application-platform-guide) \(UWP\).  API WinRT проегул на ряд различных языков, включая C#, C++, Visual Basic и JavaScript.  

Веб-разработчик может запросить эти собственные API Windows от JavaScript при запуске приложения [как установленное приложение Windows 10](../progressive-web-apps-edgehtml/windows-features.md#set-up-and-run-your-universal-windows-app) \(запущено из процесса, а не `wwahost.exe` через\браузер\).  Кроме того, на вашем веб-сайте, запущенном как приложение Для Windows 10, также могут использовать элемент управления [веб-образной](#webview) книги Microsoft Edge для отображения удаленного и локального веб-контента и API [MSApp](#msapp) для обработки BLOB-объектов и потоковой обработки потоковой загрузки.  

Ниже перечислены области имен WinRT верхнего уровня, доступные во всех приложениях windows 10:  

| WinRT Namespace | Описание |  
|:--- |:--- |  
| [AI](/uwp/api/windows.AI.MachineLearning.Preview) \(Preview\) | Содержит классы, которые могут загружать модели обучения, привязку данных к данным и оценки результатов.  |  
| [Модель приложения](/uwp/api/windows.applicationmodel) | Приложение с доступом к базовым функциям системы и сведениям о пакете приложения и обработке операций приостановки приостановки.  |  
| [Данные](/uwp/api/windows.data.html) | Служит классом служебной программы для работы с различными форматами данных, включая HTML, JSON, PDF, текст и XML.  |  
| [Устройства](/uwp/api/windows.devices) | Это пространство имен обеспечивает доступ к небольшим поставщикам устройств, включая ADC, GPIO, I2 C, PWM и SPI.  |  
| [Foundation](/uwp/api/windows.foundation) | Включает финансовые функции среды выполнения Windows, втом числе управление асинхронными операциями и доступ к хранилищам свойств.  Это пространство имен определяет распространенные типы значений, представляющие идентификатор ресурса \(URI\), даты и времени, двухмерные значения и другие базовые значения.  |  
| [Игры](/uwp/api/windows.gaming.input) |В этом режиме представлены ввод данных для контроллера, меню игры, мониторинга игри и чата.  |  
| [Globalization](/uwp/api/windows.globalization) | Поддержка глобализации профилей языков, географических регионов и международных календарей.  |  
| [Графика](/uwp/api/windows.graphics) | Предоставляет основные типы данных, содержащие сведения о том, как рисовать графические объекты.  Эти структуры данных обычно используются для определения того, каким образом применяются крупные поверхности при использовании класса CompositionVirtualDrawingSurface.  |  
| [Управление](/uwp/api/windows.management) | Предоставляет возможности принудительно синхронизировать синхронизацию с устройства управления мобильными устройствами \(MDM\) с сервером.  Этот протокол синхронизации MDM основан на стандарте управления мобильными устройствами.  |  
| [Мультимедиа](/uwp/api/windows.media) | Содержит классы для создания мультимедиа, таких как фотографии, аудиозаписи и видео.  |  
| [Сеть](/uwp/api/windows.networking) | Предоставлен доступ к хозям и конечным точкам, используемым сетевыми приложениями.  |  
| [Процентная скучность](/uwp/api/windows.perception) | Содержит классы для идеального проведения пользователей, позволяя приложениям находить и принудительно находить приложения относительно устройства относительно поверхности и голограмм, окружающей голограммы.  |  
| [Безопасность](/uwp/api/windows.security.authentication.identity) | В этой статье описано, как управлять проверкой подлинности пользователей, управление учетными данными, широкими возможностями и функциями защиты корпоративных данных.  |  
| [Службы](/uwp/api/windows.services.cortana) | Предоставлен доступ к службам Майкрософт для Кортаны, Карт, Microsoft Store и Targeted \(subscription\).  |  
| [Хранилище](/uwp/api/windows.storage) | В шаблоне разрешается управление файлами, папками и параметрами приложения.  |  
| [System](/uwp/api/windows.system) | Включает функции системы, такие как запуск приложений, получить сведения о пользователе и прибыть о памяти.  |  
| [Пользовательский интерфейс](/uwp/api/windows.ui) | Приложение с доступом к базовым функциям системы и сведениям о системе.  **ПРИМЕЧАНИЕ.** API в пространстве имен недоступны для `Windows.UI.Xaml` приложений JavaScript \(которые могут использовать эквивалентные веб-стандарты\).  |  
| [Интернет](/uwp/api/windows.web) | Сведения об ошибках, возникающих из операций веб-службы.  |  

Дополнительные сведения об использовании см. в [использовании среды выполнения Windows в JavaScript.](./using-the-windows-runtime-in-javascript.md)  Чтобы узнать, как запустить веб-сайт как приложение для Windows, воспользуйтесь научным учебнием по работе с [PWA](../progressive-web-apps/windows-features.md) для Windows.  

## Веб-представление  

С [помощью элемента управления Microsoft Edge WebView](../webview.md) можно размещать веб-контент в приложении для Windows 10.  Это точно так же, как и `<iframe>` при работе, но обеспечивает [больше](../hosting/webview.md#webview-versus-iframe) возможностей и возможностей управления процессом.  

## MSApp  

Глобальный объект [MSAppal](./reference/msapp.md) \( \) предоставляет функции с сортируемыми `window.MSApp` функциями справки для приложений JavaScript для приложений JavaScript, например служебных программ для преобразования между стандартами и эквивалентными типами объектов WinRT.  
