---
description: Автоматизация и тестирование элемента управления WebView2 с помощью драйвера Microsoft Edge
title: Автоматизация и тестирование WebView2 с помощью драйвера Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, EDGE, ICoreWebView2, ICoreWebView2Controller, Selenium, драйвер Microsoft Edge
ms.openlocfilehash: acee8c1f791fdd4a2604b8f3bfa7664548a164d1
ms.sourcegitcommit: 5bdffe91a6594f77eeffa4e864fda90a02784771
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/19/2020
ms.locfileid: "10659717"
---
# Автоматизация и тестирование WebView2 с помощью драйвера Microsoft Edge

Так как WebView2 использует веб-платформу Chromium, WebView2 разработчики могут воспользоваться стандартными веб-средствами для отладки и автоматизации. Одним из таких средств является Selenium, реализующий API [-](https://www.w3.org/TR/webdriver2/) интерфейс консорциума W3C, который можно использовать для создания автоматических тестов, имитирующих взаимодействия с пользователем.

Порядок начала работы:

## Шаг 1: Загрузка образца WebView2API

Если у вас нет проекта WebView2, скачайте наш [пример приложения WebView2API](https://github.com/MicrosoftEdge/WebView2Samples/tree/master/WebView2APISample#webview2-api-sample), который является исчерпывающим примером НОВЕЙШего комплекта SDK для WebView2. Убедитесь в том, что вы удовлетворены [необходимыми условиями](https://github.com/MicrosoftEdge/WebView2Samples/tree/master/WebView2APISample#prerequisites).

Создав точную копию репозитория, создайте проект в Visual Studio. Он должен выглядеть следующим образом:

![замещающий текст](../media/webdriver/sample-app.png)

## Шаг 2: Установка драйвера Microsoft Edge

Следуйте инструкциям, чтобы установить [драйвер Microsoft Edge](https://docs.microsoft.com/microsoft-edge/webdriver-chromium#download-microsoft-edge-driver) , необходимый для автоматизации и тестирования WebView2, который требуется драйверу Selenium для веб-браузера.

Важно убедиться, что версия драйвера Microsoft EDGE соответствует версии Microsoft EDGE, используемой в приложении. Чтобы образец WebView2API работал, убедитесь в том, что ваша версия Microsoft Edge больше или равна поддерживаемой версии последней версии SDK, которую можно найти [в заметках о выпуске](https://docs.microsoft.com/microsoft-edge/hosting/webview2/releasenotes). Чтобы узнать, какая у вас версия Microsoft EDGE уже есть, загрузите ее `edge://settings/help` в браузере.

## Шаг 3: Добавление Selenium в пример WebView2API

На этом этапе у вас должен быть установлен Microsoft EDGE, создан проект WebView2 и установлен драйвер Microsoft Edge. Теперь приступим к работе с Selenium.

> [!NOTE]
> Selenium поддерживает C#, Java, Python, JavaScript и Ruby. Однако это руководство будет отображаться на C#.

1. Начните с создания нового проекта **C# .NET Framework** в **Visual Studio**. Чтобы продолжить, нажмите кнопку **Далее** в правом нижнем углу.

![замещающий текст](../media/webdriver/new-project.png)

2. Введите **имя**проекта, сохраните его в нужном **месте**и нажмите кнопку **создать**.

![замещающий текст](../media/webdriver/app-create.png)

3. Будет создан новый проект. В этом руководстве весь код будет написан в файле **Program.CS** .

![замещающий текст](../media/webdriver/start-app.png)

4. Теперь добавим **Selenium** в проект. Вы можете установить Selenium с помощью **пакета NuGet для Selenium.**

Чтобы скачать **пакет NuGet Selenium...** в **Visual Studio**, наведите указатель мыши на элемент **Project** и выберите пункт **Управление пакетом NuGet**. Появится следующий экран:

![замещающий текст](../media/webdriver/download-nuget.png)

5. Введите **Selenium.** Selenium на панели поиска, щелкните **. стример** из результатов, а затем установите флажок **включить предварительную версию**. В правой части окна убедитесь, что для **версии** установлено значение **4.0.0-alpha04** или более поздней, и нажмите кнопку **установить**. NuGet загрузит Selenium на ваш компьютер.

[Дополнительные сведения о пакете NuGet для Selenium.](https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha04)

![замещающий текст](../media/webdriver/nuget.png)

6. Используйте **OpenQA. Selenium. Edge** , добавив следующий оператор: ```using OpenQA.Selenium.Edge;``` в начале **Program.CS**

```csharp
using OpenQA.Selenium.Edge;

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
```

## Шаг 4: WebView2 диска с Selenium и Microsoft EdgeDriver

1. Сначала создайте `EdgeOptions` объект, скопировав приведенный ниже код.

```csharp
static void Main(string[] args)
{
    // EdgeOptions() requires using OpenQA.Selenium.Edge
    // Construct EdgeOptions with is_legacy = false and the string "webview2"
    EdgeOptions edgeOptions = new EdgeOptions(false, "webview2");
```

`EdgeOptions`Объект принимает два параметра:
\
    **Параметры**
    1. `is_legacy`: значение `false` , указывающее Selenium, что вы управляете новым браузером Microsoft EDGE на основе Chromium.
    2. `"webview2"`: строка, которая указывает Selenium, что вы управляете **WebView2**

2. Затем укажите `edgeOptions.BinaryLocation` путь к файлу исполняемого файла проекта WebView2, создайте строку с именем `msedgedriverDir` , которая содержит путь к файлу, на который установлен [драйвер Microsoft Edge](https://developer.microsoft.com/microsoft-edge/tools/webdriver/#downloads), и создайте строку, которая вызывается `msedgedriverExe` для хранения имени исполняемого файла драйвера Microsoft Edge. По умолчанию вызывается исполняемый файл `"msedgedriver.exe"` . Используйте эти две строки для создания `EdgeDriverService` объекта, как показано ниже. Наконец, создайте `EdgeDriver` объект с помощью `EdgeDriverService` и `EdgeOptions` .

Вы можете скопировать и вставить следующий код под ним `edgeOptions` . Убедитесь, что указаны правильные пути к исполняемому файлу проекта и исполняемому файлу драйвера Microsoft EDGE на вашем компьютере.

```csharp
    //Set the BinaryLocation to the filepath of the WebView2API Sample's executable
    edgeOptions.BinaryLocation = @"C:\path\to\your\webview2\project.exe";

    //Set msedgedriverDir to the filepath of the directory housing msedgedriver.exe
    string msedgedriverDir = @"C:\path\to\your\msededriver.exe's\directory";

    //Set msedgedriverExe to the name of the Edge Driver. By default it is:
    string msedgedriverExe = @"msedgedriver.exe";

    // Construct EdgeDriverService with is_legacy = false  
    EdgeDriverService service = EdgeDriverService.CreateDefaultService(msedgedriverDir, msedgedriverExe, false);

    EdgeDriver e = new EdgeDriver(service, edgeOptions);
```

3. Теперь **EdgeDriver** настроен для настройки **WebView2** в проекте. Например, если вы используете **образец WebView2API**, вы можете **Перейти** <https://microsoft.com> по вызову ```e.Url = @"https://www.microsoft.com";``` . Вы можете просматривать **Selenium** диск **WebView2** , настроив точку останова в этой строке и запуская проект.

```csharp
    //The following will Navigate the WebView2API Sample from bing.com to microsoft.com
    e.Url = @"https://www.microsoft.com";

    //This exits the edge driver
    e.Quit();
}
```

![замещающий текст](../media/webdriver/microsoft.png)

Поздравляем! Вы успешно автоматизируи проект WebView2 и управляемый WebView2 с помощью драйвера Selenium и Microsoft Edge.

## Дальнейшие действия

Дополнительные сведения:

- Ознакомьтесь с [документацией по Selenium](https://www.selenium.dev/documentation/en/webdriver/) и ознакомьтесь с подробным обзором API-интерфейсов Selenium, которые можно использовать для работы с WebView2 или Microsoft EDGE (Chromium).
- Дополнительные сведения об элементе управления [WebView2](https://docs.microsoft.com/microsoft-edge/hosting/webview2) и его использовании при внедрении веб-содержимого в собственное приложение
- Дополнительные сведения об автоматизации Microsoft EDGE (Chromium) можно найти в [документации по Microsoft Edge Driver](https://docs.microsoft.com/microsoft-edge/webdriver-chromium) .

## Связь с командой WebView2  

Помогите нам создать более WebView2ную работу, поделитесь с нами. Посетите наш [репозиторий отзывов](https://github.com/MicrosoftEdge/WebViewFeedback) о функциях или сообщениях об ошибках или поиск известных проблем.
