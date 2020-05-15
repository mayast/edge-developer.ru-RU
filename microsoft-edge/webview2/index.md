---
description: Размещение веб-содержимого в приложении Win32 с помощью элемента управления Microsoft Edge WebView 2
title: Microsoft Edge WebView 2 для приложений Win32
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, приложения Win32, Win32, EDGE, ICoreWebView2, ICoreWebView2Controller, элемент управления "веб-браузер", HTML Edge
ms.openlocfilehash: b1ec0c43b57fb107490ddb34b330bb6ec378ac41
ms.sourcegitcommit: 07cda56425e5fdf90eeb3972e17041261bf720cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/14/2020
ms.locfileid: "10654721"
---
# Microsoft Edge WebView2 (Предварительная версия для разработчиков)

Элемент управления Microsoft Edge WebView2 позволяет размещать веб-содержимое в приложении с помощью [Microsoft EDGE (Chromium)](https://www.microsoftedgeinsider.com/) в качестве обработчика визуализации.

Элемент управления WebView2 в настоящее время находится в предварительной версии для разработчиков, в котором вы можете создавать собственные прототипы и обмениваться отзывами с нами, чтобы сослаться на будущее стабильный API. Это может привести к некоторым критическим изменениям, так как мы будем развиваться API во время предварительного просмотра, и в этом случае вам потребуется обновить и WebView2 SDK, и браузер Microsoft EDGE (Chromium). Критические изменения будут отмечены в [заметках о выпуске](./releasenotes.md) SDK. Это заблокируется как WebView2 подходы к бета-версии и стабильным версиям.

## Поддерживаемые платформы

Предварительная версия для разработчиков доступна для Win32 C/C++ и Windows Forms и WPF на платформе .NET Framework 4.6.2 или более поздней версии, а также .NET Core 3,0 или более поздней версии в Windows 10, Windows 8,1, Windows 8, Windows 7, Windows Server 2016, Windows Server 2012 и 2012R2 и Windows Server 2008 R2. [Здесь](https://docs.microsoft.com/uwp/toolkits/winui3/)вы можете найти альфа-версию для WinUI 3,0.

## Начало работы

Чтобы создать и протестировать приложение с помощью элемента управления WebView2, необходимо установить [Microsoft EDGE (Chromium)](https://www.microsoftedgeinsider.com/download/) и [WebView2 SDK](https://aka.ms/webviewnuget) . Выберите один из предложенных ниже вариантов, чтобы приступить к работе.

* [Начало работы с Win32 C/C++](./gettingstarted/win32.md)
* [Начало работы с WPF](./gettingstarted/wpf.md)
* [Начало работы с Windows Forms](./gettingstarted/winforms.md)

Пожалуйста, оставьте свой отзыв в репозитории [обратной связи в WebView2](https://aka.ms/webviewfeedback) .

## Примеры WebView2

В репозитории [примеров WebView2](https://github.com/MicrosoftEdge/WebView2Samples) содержатся примеры, демонстрирующие все возможности SDK WebView2 и их использование API-интерфейсов. По мере добавления дополнительных функций в WebView2 SDK мы регулярно обновляем наши учебные приложения.

## Распространение приложений

Элемент управления WebView2 использует браузер Microsoft EDGE (Chromium). При распространении приложения важно убедиться, что браузер EDGE установлен на всех компьютерах пользователей, на которых будет выполняться приложение. Кроме того, следует учитывать, какая версия и канал установлены, например, стабильный, бета-, для разработчиков или Канарские. Контроллер WebView2 будет использовать самую стабильную версию браузера, установленную на компьютере.

### Будущие запланированные изменения

Мы понимаем, что браузер EDGE может быть недоступен на всех компьютерах пользователей, для которых предназначено приложение, или этот элемент управления процессом установки в браузере Edge может быть очень сложным. Чтобы убедиться, что приложение будет работать на всех компьютерах независимо от состояния установки браузера Microsoft EDGE, мы выпустим среду выполнения Microsoft Edge WebView2. Мы постараемся обновить WebView2, чтобы найти стабильный вариант среды выполнения перед поиском предварительных версий установленного браузера.

Мы также понимаем, что некоторые разработчики приложений работают в ограниченных средах и поэтому должны поддерживать два варианта распространения: Evergreen и фиксированная версия.

Evergreen — Рекомендуемая модель распространения для большинства разработчиков. В этом режиме обновление среды выполнения WebView2 будет полностью поддерживаться корпорацией Майкрософт, так как в этом случае вы будете в состоянии автоматически без дополнительных усилий в приложении. С помощью этой модели самообновления вы можете быть уверены, что ваше приложение использует последние возможности и обновления для системы безопасности для размещенного веб-контента.

Для ограниченных сред также будет поддерживаться модель распространения фиксированной версии. В этой модели приложение выберет и упакуйте определенную версию WebView2. Обновление версии WebView несет ответственность за приложение и будет независимым от любых управляемых механизмов центра обновления Майкрософт. Эту модель следует выбирать в том случае, если важно иметь абсолютный контроль над версией браузера и время обновления, которое использует приложение.

## Среда выполнения Microsoft Edge WebView2

Среда выполнения Microsoft Edge WebView2 — это упаковка двоичных файлов браузера, оптимизированных для использования приложениями WebView2. Он будет работать отдельно или параллельно с помощью веб-браузера клиента Edge. Единая установка времени выполнения будет поддерживать любое количество приложений WebView2. Установка среды выполнения не будет выводиться в качестве браузера для конечных пользователей, то есть без ярлыков на рабочем столе, записи в меню "Пуск" или регистрации протокола.

Приложение, использующий WebView2, должно обеспечивать установку среды выполнения Microsoft Edge WebView2. Во время установки приложения необходимо проверить состояние текущей установки, которое можно определить с помощью [GetAvailableCoreWebView2BrowserVersionString](./reference/win32/0-9-488/webview2-idl.md#getavailablecorewebview2browserversionstring). Если среда выполнения WebView2 недоступна, необходимо связать установщику среды выполнения Microsoft Edge WebView2 с потоком установки.

## Microsoft Edge WebView2 SDK

Чтобы использовать WebView2 в своем приложении, вам потребуется установить [пакет WebView2 SDK](https://aka.ms/webviewnuget) и ссылаться на него в вашем приложении. В наших выпусках NuGet будут включены выпуск и предварительная версия. Окончательная версия включает общедоступные API-интерфейсы, которые в настоящее время планируется выпустить в общем доступе.

Предварительная версия будет содержать дополнительные [экспериментальные API](./reference/win32/0-9-488-reference-webview2.md#experimental). Это API и функциональные возможности, которые мы будем оценивать и которые хотели бы получить [обратную связь](https://aka.ms/webviewfeedback) перед тем, как повысить их до окончательной версии.

## Разработка для будущих версий

Для разработки вы можете использовать бета-версию, разработку или Канарские, чтобы обеспечить работу вашего приложения с предстоящими версиями или воспользоваться преимуществами предстоящих функций. Все предварительно выпущенные каналы предоставляются установленным клиентским браузером Microsoft Edge. Для использования одного из этих каналов убедитесь, что установленный браузер пограничного устройства на компьютере разработчика является вашим каналом. Разработчики могут использовать раздел реестра или переменную среды для изменения WebView2 из самой стабильной версии, обнаруженной для наименее стабильных. Более подробную информацию смотрите в [CreateCoreWebView2EnvironmentWithOptions](./reference/win32/0-9-488/webview2-idl.md#createcorewebview2environmentwithoptions).

## Отладка WebView2

### DevTools

Вы можете использовать [Инструменты разработчика Microsoft EDGE (Chromium)](https://docs.microsoft.com/microsoft-edge/devtools-guide-chromium) для отладки веб-содержимого, отображаемого в WebView, так же, как в браузере. При нахождении фокуса в окне WebView нажмите или `F12` нажмите `Ctrl`  +  `Shift`  +  `I` или щелкните правой кнопкой мыши + выберите, `Inspect` чтобы открыть инструменты разработчика.

:::image type="complex" source="./media/f12.png" alt-text="F12":::
   F12
:::image-end:::  

<!--![F12](./media/f12.png)  -->  

**Обратите внимание, что при отладке приложения в Visual Studio с прикрепленным отладчиком машинного кода `F12` может быть запущен отладчик машинного кода вместо средств разработчика. Используйте `Ctrl`  +  `Shift`  +  `I` или щелкните правой кнопкой мыши, `Inspect` чтобы избежать возможного конфликта сочетаний клавиш.**

### Visual Studio

Вы можете использовать отладчик сценариев в Visual Studio 2019 (минимальный вариант версии 16,4) для отладки сценария в WebView2 прямо из среды разработки. Убедитесь, что компонент **диагностики JavaScript** установлен на **рабочем столе с** рабочей нагрузкой C++.

:::image type="complex" source="./media/vs-js-diagnostics.jpg" alt-text="Диагностика JavaScript в Visual Studio":::
   Диагностика JavaScript в Visual Studio
:::image-end:::  

<!--![vs-js-diagnostics](./media/vs-js-diagnostics.jpg)  -->  

Щелкните проект правой кнопкой мыши и выберите пункт **Свойства**. В разделе **Свойства конфигурации**  >  **Отладка**:  >  **Тип отладчика**выберите параметр **JavaScript (WebView2)** , чтобы включить отладку сценариев WebView2. Дополнительные сведения можно подписаться на ближайшее время.

:::image type="complex" source="./media/vs-script-debugger.jpg" alt-text="Отладчик сценариев Visual Studio":::
   Отладчик сценариев Visual Studio
:::image-end:::  

<!--![vs-script-debugger](./media/vs-script-debugger.jpg)  -->  

### Visual Studio Code

Вы также можете использовать код Visual Studio для отладки сценария в WebView2 прямо из интегрированной среды разработки. Чтобы получить дополнительные сведения, щелкните [здесь](https://github.com/microsoft/vscode-edge-debug2/blob/master/README.md#microsoft-edge-chromium-webview-applications).

## Связь с командой WebView2  

Помогите нам создать более WebView2ную работу, поделитесь с нами. Посетите наш [репозиторий обратной связи](https://aka.ms/webviewfeedback) , чтобы отправить запросы на функцию или отчеты об ошибках.

Кроме того, лучше всего искать известные проблемы.
Во время предварительного просмотра разработчик также будет собирать данные телеметрии, чтобы помочь нам улучшить WebView. Пользователи могут отключить сбор данных WebView, перейдя в edge://settings/privacy в браузере и отключив коллекцию данных браузера.