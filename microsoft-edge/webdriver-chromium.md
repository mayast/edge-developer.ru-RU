---
description: Сведения о том, как протестировать веб-сайт или приложение в Microsoft EDGE, а также автоматизировать браузер с помощью Web Drive.
title: Chromium
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/11/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft EDGE, веб-разработка, HTML, CSS, сценарий JavaScript, разработчик, веб-дисковод, Selenium, тестирование, инструменты, Автоматизация и тестирование
ms.openlocfilehash: 0cb135553b04cd0cf160755eacc0dbae245d13b7
ms.sourcegitcommit: 24430258f363b7dd85f7067afd4565bf102b4a1f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/12/2020
ms.locfileid: "10645317"
---
# Chromium  

API веб- [накопителей][W3CWebdriver] W3C — это платформа и независимый от языка интерфейс и протокол проводной связи, позволяющая программам и сценариям управлять поведением браузера, например Microsoft Edge \ (Chromium \).  

С помощью этого устройства разработчики могут создавать автоматические тесты, имитирующие взаимодействие с пользователем.  Тесты и эмуляции веб-дисков отличаются от модульных тестов JavaScript, так как веб-дисководы имеют доступ к функциональным возможностям и сведениям, которые JavaScript работает в браузере, а также для того, чтобы на устройстве было более точного моделирования событий пользователей и событий на уровне операционной системы.  С помощью веб-диска можно управлять тестированием между несколькими окнами, вкладками и страницами в одном тестовом сеансе.  

Вот как начать работу с веб-дисководом для Microsoft Edge \ (Chromium \).  

## Установка Microsoft EDGE (Chromium)  

[Установите Microsoft EDGE (Chromium)][MicrosoftEdge], если вы еще не сделали этого.  Если вы используете предварительно установленную версию Microsoft EDGE на своем компьютере, убедитесь в том, что у вас есть Microsoft Edge \ (Chromium \), а не Microsoft Edge \ (EdgeHTML \).  Чтобы быстро проверить, нужно ли загрузить `edge://settings/help` браузер и убедиться, что номер версии — V75 или более поздней.  

## Скачать драйвер Microsoft Edge  

Для автоматизации каждого браузера для веб-дисковода необходим драйвер, зависящий от браузера.  Для Microsoft Edge \ (Chromium \) требуется соответствующий [драйвер Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver] для сборки Microsoft EDGE, которую вы хотите протестировать или автоматизировать.  

Чтобы найти правильный номер сборки, выполните указанные ниже действия.  

1.  Запуск Microsoft Edge 
1.  Просмотреть версию Microsoft Edge \ (Chromium \).  
    *   Перейдите к `edge://settings/help`  
    *   Выберите `...`  >  **Параметры**  >   **о Microsoft Edge**  
1.  Убедитесь в том, что для сборки указана нужная версия, чтобы она правильно выполнялась.  

:::image type="complex" source="./media/webdriver-chromium/edge-version.png" alt-text="Номер сборки Microsoft Edge Канарские 14 января 2020 г.":::
   Рисунок 1.  Номер сборки Microsoft Edge Канарские 14 января 2020 г.  
:::image-end:::

<!--  
> ##### Figure 1  
> The build number for Microsoft Edge Canary on January 14, 2020
> ![The build number for Microsoft Edge Canary on January 14, 2020][ImageWebdriverChromiumEdgeVersion]  
-->  

Теперь [Загрузите соответствующую версию драйвера Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriverDownloads].  

:::image type="complex" source="./media/webdriver-chromium/edge-driver-install.png" alt-text="Раздел "загружаемые файлы" на странице драйвера Microsoft Edge":::
   Рисунок 2.  Раздел "загружаемые файлы" на странице [драйвера Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriverDownloads]  
:::image-end:::

<!--  
> ##### Figure 2
> The Downloads section of the [Microsoft Edge Driver page][MicrosoftDeveloperEdgeToolsWebdriverDownloads]
> ![The Downloads section of the Microsoft Edge Driver page][ImageWebdriverChromiumEdgeDriverInstall]  
-->  

> [!NOTE]
> Microsoft Edge \ (EdgeHTML \) не работает с [драйвером Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriverDownloads].  Для автоматизации Microsoft Edge \ (EdgeHTML \) необходимо загрузить [Microsoft для Microsoft Edge \ (EdgeHTML \)][Webdriver].  

## Выбор языковой привязки для веб-дисков  

Последним компонентом, который необходимо скачать, является драйвер клиента, зависящий от языка.  Языковая привязка преобразует код, написанный в Python, Java, C \ #, Ruby и JavaScript, в команды, которые драйвер Microsoft EDGE, загруженный в [предыдущем разделе](#download-microsoft-edge-driver) , может работать в Microsoft Edge \ (Chromium \).  

[Скачайте выбранную вами языковую привязку веб дисков][SeleniumDownloads].  Группа Microsoft Edge настоятельно рекомендует [Selenium 4,00-alpha05][NugetPackagesSeleniumWebdriver400alpha05] или более поздней версии, так как она содержит встроенную поддержку Microsoft Edge \ (Chromium \).  Однако вы можете подключаться к Microsoft Edge \ (Chromium \) во всех более ранних версиях Selenium, включая текущую стабильную версию Selenium 3.  

> [!IMPORTANT]
> Если вы уже выполняли автоматизацию или тестирование Microsoft Edge \ (Chromium \), используя `ChromeDriver` и `ChromeOptions` , код веб-дисковода не запустится в Microsoft Edge V80 или более поздней версии.  Это критическое изменение, а Microsoft Edge \ (Chromium \) больше не принимает эти команды.  Необходимо изменить тесты, чтобы использовать `EdgeOptions` драйвер класса и [Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver].  

### Использование Selenium 3  

[Selenium 3][|::ref1::|] – это новейшая стабильный выпуск Selenium.  По умолчанию Selenium 3 использует старый Microsoft Edge \ (EdgeHTML \) и не имеет встроенной поддержки Microsoft Edge \ (Chromium \).  Чтобы использовать Selenium 3 с Microsoft Edge \ (Chromium \), установите пакет [инструментов Selenium для Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] .  Selenium Tools for Microsoft Edge расширяет Selenium 3 с помощью обновленного драйвера, который поможет вам создавать автоматические тесты для обоих браузеров Microsoft Edge \ (EdgeHTML \) и новых Microsoft Edge \ (Chromium).  

Selenium Tools for Microsoft Edge — это решение для разработчиков, которые хотят оставаться на Selenium 3 и разработчиках с существующими тестами браузера и добавлять покрытие для нового браузера Microsoft Edge \ (Chromium \) без изменения версий Selenium.  `EdgeDriver`Классы и `EdgeDriverService` включенные в них компоненты полностью совместимы с встроенными эквивалентами в Selenium и выполняют Microsoft Edge \ (EdgeHTML \) по умолчанию, поэтому эти средства можно использовать в качестве неполной замены для существующих классов EDGE в Selenium.  

[Установите средства Selenium для Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] , чтобы приступить к работе с Microsoft Edge \ (Chromium \) с проектом Selenium 3.  

## Использование веб-накопителя (Microsoft EDGE (Chromium))

Следующие примеры выполняются с помощью либо Selenium 3, либо 4.  Для использования с Selenium 3 должны быть установлены [средства Selenium для Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] .  

### Основное использование  

Для использования в Microsoft Edge \ (EdgeHTML \) просто создайте экземпляр класса по умолчанию `EdgeDriver` .

#### [C#](#tab/c-sharp/)  

<a id="basic-usage-code" />  

```csharp
var driver = new EdgeDriver();
```  

#### [Языке](#tab/python/)  

<a id="basic-usage-code" />  

```python
driver = Edge()
```  

* * *  

### Управление Microsoft EDGE (Chromium)  

Для использования с Microsoft Edge \ (Chromium \) вместо этого создайте новый `EdgeDriver` класс и передайте ему `EdgeOptions` объект со `UseChromium` свойством, для которого задано значение `true` .  

#### [C#](#tab/c-sharp/)  

<a id="diving-microsoft-edge-chromium-code" />  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### [Языке](#tab/python/)  

<a id="diving-microsoft-edge-chromium-code" />  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options)
```  

* * *  

### Выбор определенных двоичных файлов браузера (только Chromium)  

Используйте этот `EdgeOptions` класс для выбора определенного двоичного файла.  Это полезно при тестировании [каналов предварительной версии Microsoft Edge][MicrosoftedgeinsiderDownload] , таких как Microsoft Edge Beta.  

#### [C#](#tab/c-sharp/)  

<a id="choosing-specific-browser-binaries-chrome-only-code" />  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### [Языке](#tab/python/)  

<a id="choosing-specific-browser-binaries-chrome-only-code" />  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options)
```  

* * *  

### Настройка службы драйвера Microsoft Edge  

#### [C#](#tab/c-sharp/)  

<a id="customizing-microsoft-edge-driver-services-code" />  

Если `EdgeDriver` экземпляр класса создается с помощью `EdgeOptions` класса, он автоматически создает и запускает соответствующий `EdgeDriverService` класс для Microsoft Edge \ (EdgeHTML \) или Microsoft Edge \ (Chromium \).  

Если вы хотите создать объект `EdgeDriverService` для Microsoft Edge \ (Chromium \) с помощью метода, создайте его `CreateChromiumService()` .  Вы можете использовать дополнительные настройки, такие как включение подробного вывода журнала в приведенном ниже коде.  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE]
> Вам не нужно предоставлять `EdgeOptions` объект при передаче `EdgeDriver` экземпляра класса `EdgeDriverService` .  Этот `EdgeDriver` класс использует параметры по умолчанию (Microsoft Edge \ (EdgeHTML \) или Microsoft Edge \ (Chromium \) в зависимости от типа предоставляемой услуги.  
> 
> Тем не менее, если вы хотите предоставить оба `EdgeDriverService` `EdgeOptions` класса и классы, необходимо убедиться, что оба они настроены для одной и той же версии Microsoft Edge.  Например, невозможно использовать класс по умолчанию Microsoft Edge \ (EdgeHTML \) `EdgeDriverService` и свойства Chromium в `EdgeOptions` классе.  `EdgeDriver`Класс вызывает ошибку, чтобы предотвратить использование разных версий.  

#### [Языке](#tab/python/)  

<a id="customizing-microsoft-edge-driver-services-code" />  

При использовании Python `Edge` объект создает и управляет `EdgeService` .  Чтобы настроить `EdgeService` , передайте объекту дополнительные аргументы `Edge` .

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

* * *  

### Использование параметров, специфичных для Chromium  

Использование `EdgeOptions` класса с `UseChromium` установленным свойством `true` предоставляет доступ ко всем тем же методам и свойствам, которые доступны в классе [ChromeOptions][SeleniumWebDriverChromeoptionsClass] в Selenium.  Например, как и в других браузерах Chromium, используйте `EdgeOptions.AddArguments()` метод для запуска Microsoft Edge \ (Chromium \) в [режиме бездисплейного режима][WikiHeadlessBrowser] в приведенном ниже коде.  

#### [C#](#tab/c-sharp/)  

<a id="using-chromium-specific-options-code" />  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

#### [Языке](#tab/python/)  

<a id="using-chromium-specific-options-code" />  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument('headless')
options.add_argument('disable-gpu')
```  

* * *  

> [!NOTE]
> Эти [Свойства и методы Chromium][SeleniumWebDriverChromeoptionsClass] всегда доступны, но не имеют никакого эффекта, если `UseChromium` свойство не задано `true` .  Аналогичным образом существующие свойства и методы, предназначенные для Microsoft Edge \ (EdgeHTML \), не применяются, если `UseChromium` для свойства задано значение `true` .  

<!--  
### [C#](#tab/c-sharp/)  

<a id="selenium-usage" />  

#### Basic Usage  

To use with Microsoft Edge \(EdgeHTML\), simply create a default instance of the `EdgeDriver` class.

```csharp
var driver = new EdgeDriver();
```  

#### Driving Microsoft Edge (Chromium)  

To use with Microsoft Edge \(Chromium\) instead, create a new `EdgeDriver` class and pass it the `EdgeOptions` object with the `UseChromium` property set to `true`.  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### Choosing Specific Browser Binaries (Chromium-Only)  

Use the `EdgeOptions` class to choose a specific binary.  It is useful for testing [Microsoft Edge preview channels][MicrosoftedgeinsiderDownload] such as Microsoft Edge Beta.  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### Customizing the Edge Driver Service  

When an `EdgeDriver` class instance is created using `EdgeOptions` class, it automatically creates and launches the appropriate `EdgeDriverService` class for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\).  

If you want to create an `EdgeDriverService`, create one configured for Microsoft Edge \(Chromium\) using the `CreateChromiumService()` method.  You may find it useful for additional customizations like enabling verbose log output in the following code.  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE]
> You do not need to provide the `EdgeOptions` object when passing the `EdgeDriver` class instance the `EdgeDriverService`.  The `EdgeDriver` class uses the default options for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\) depending on what kind of service you provide.  
> 
> However, if you want to provide both an `EdgeDriverService` and `EdgeOptions` classes, you must ensure that both are configured for the same version of Microsoft Edge.  For example, it is not possible to use a default Microsoft Edge \(EdgeHTML\) `EdgeDriverService` class and Chromium properties in the `EdgeOptions` class.  The `EdgeDriver` class throws an error to prevent using different versions.  

#### Using Chromium-Specific Options  

Using the `EdgeOptions` class with the `UseChromium` property set to `true` gives you access to all of the same methods and properties that are available in the [ChromeOptions][SeleniumWebDriverChromeoptionsClass] class in Selenium.  For example, just like with other Chromium browsers, use the `EdgeOptions.AddArguments()` method to run Microsoft Edge \(Chromium\) in [headless mode][WikiHeadlessBrowser] in the following code.  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

> [!NOTE]
> These [Chromium-specific properties and methods][SeleniumWebDriverChromeoptionsClass] are always available but have no effect if the `UseChromium` property is not set to `true`.  Similarly, existing properties and methods meant for Microsoft Edge \(EdgeHTML\) have no effect if `UseChromium` property is set to `true`.  

### [Python](#tab/python/)  

<a id="selenium-usage" />  

#### Basic Usage  

To use with Microsoft Edge \(EdgeHTML\), simply create a default instance of the `EdgeDriver` class.

```python
driver = Edge()
```  

#### Driving Microsoft Edge (Chromium)  

To use with Microsoft Edge \(Chromium\) instead, create a new `EdgeDriver` class and pass it the `EdgeOptions` object with the `UseChromium` property set to `true`.  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options)
```  

#### Choosing Specific Browser Binaries (Chromium-Only)  

Use the `EdgeOptions` class to choose a specific binary.  It is useful for testing [Microsoft Edge preview channels][MicrosoftedgeinsiderDownload] such as Microsoft Edge Beta.  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options)
```  

#### Customizing the Edge Driver Service  

When an `EdgeDriver` class instance is created using `EdgeOptions` class, it automatically creates and launches the appropriate `EdgeDriverService` class for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\).  

If you want to create an `EdgeDriverService`, create one configured for Microsoft Edge \(Chromium\) using the `CreateChromiumService()` method.  You may find it useful for additional customizations like enabling verbose log output in the following code.  

When using Python, the `Edge` object creates and manages the `EdgeService`.  To configure the `EdgeService`, pass additional arguments to the `Edge` object:

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

#### Using Chromium-Specific Options  

Using the `EdgeOptions` class with the `UseChromium` property set to `true` gives you access to all of the same methods and properties that are available in the [ChromeOptions][SeleniumWebDriverChromeoptionsClass] class in Selenium.  For example, just like with other Chromium browsers, use the `EdgeOptions.AddArguments()` method to run Microsoft Edge \(Chromium\) in [headless mode][WikiHeadlessBrowser] in the following code.  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument('headless')
options.add_argument('disable-gpu')
```  

> [!NOTE]
> These [Chromium-specific properties and methods][SeleniumWebDriverChromeoptionsClass] are always available but have no effect if the `UseChromium` property is not set to `true`.  Similarly, existing properties and methods meant for Microsoft Edge \(EdgeHTML\) have no effect if `UseChromium` property is set to `true`.  

* * *  

-->  

<!--  
### Basic Usage  

To use with Microsoft Edge \(EdgeHTML\), simply create a default instance of the `EdgeDriver` class.

#### C\#  

```csharp
var driver = new EdgeDriver();
```  

#### Python  

```python
driver = Edge()
```  

### Driving Microsoft Edge (Chromium)  

To use with Microsoft Edge \(Chromium\) instead, create a new `EdgeDriver` class and pass it the `EdgeOptions` object with the `UseChromium` property set to `true`.  

#### C\#  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### Python  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options)
```  

### Choosing Specific Browser Binaries (Chromium-Only)  

Use the `EdgeOptions` class to choose a specific binary.  It is useful for testing [Microsoft Edge preview channels][MicrosoftedgeinsiderDownload] such as Microsoft Edge Beta.  

#### C\#  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### Python  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options)
```  

### Customizing the Edge Driver Service  

#### C\#  

When an `EdgeDriver` class instance is created using `EdgeOptions` class, it automatically creates and launches the appropriate `EdgeDriverService` class for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\).  

If you want to create an `EdgeDriverService`, create one configured for Microsoft Edge \(Chromium\) using the `CreateChromiumService()` method.  You may find it useful for additional customizations like enabling verbose log output in the following code.  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE]
> You do not need to provide the `EdgeOptions` object when passing the `EdgeDriver` class instance the `EdgeDriverService`.  The `EdgeDriver` class uses the default options for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\) depending on what kind of service you provide.  
> 
> However, if you want to provide both an `EdgeDriverService` and `EdgeOptions` classes, you must ensure that both are configured for the same version of Microsoft Edge.  For example, it is not possible to use a default Microsoft Edge \(EdgeHTML\) `EdgeDriverService` class and Chromium properties in the `EdgeOptions` class.  The `EdgeDriver` class throws an error to prevent using different versions.  

#### Python  

When using Python, the `Edge` object creates and manages the `EdgeService`.  To configure the `EdgeService`, pass additional arguments to the `Edge` object:

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

### Using Chromium-Specific Options  

Using the `EdgeOptions` class with the `UseChromium` property set to `true` gives you access to all of the same methods and properties that are available in the [ChromeOptions][SeleniumWebDriverChromeoptionsClass] class in Selenium.  For example, just like with other Chromium browsers, use the `EdgeOptions.AddArguments()` method to run Microsoft Edge \(Chromium\) in [headless mode][WikiHeadlessBrowser] in the following code.  

#### C\#  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

#### Python  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument('headless')
options.add_argument('disable-gpu')
```  

> [!NOTE]
> These [Chromium-specific properties and methods][SeleniumWebDriverChromeoptionsClass] are always available but have no effect if the `UseChromium` property is not set to `true`.  Similarly, existing properties and methods meant for Microsoft Edge \(EdgeHTML\) have no effect if `UseChromium` property is set to `true`.  
-->  

## Другие способы настройки устройства  

### Шоколад  

Если вы используете [шоколад][Chocolatey] в качестве диспетчера пакетов, установите драйвер Microsoft EDGE, выполнив следующую команду:  

```console
choco install selenium-chromium-edge-driver
```  

Дополнительные сведения можно найти [в разделе драйвер Selenium Chromium EDGE на шоколаде][ChocolateyPackagesSeleniumChromiumEdgeDriver].  

### Docker  

Если вы используете [закрепление][DockerHub], скачайте предварительно настроенное изображение с помощью Microsoft Edge \ (Chromium \) и [Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver] , которое уже установлено, выполнив следующую команду:  

```console
docker run -d -p 9515:9515 mcr.microsoft.com/msedge/msedgedriver
```  

Дополнительные сведения можно найти [в разделе контейнер в центре Dock][DockerHubMsedgedriver].  

## Знакомство с командой Microsoft Edge DevTools    

Группа Microsoft Edge – это информация о том, как использовать веб – диски, Selenium и Microsoft Edge!  С помощью значка **обратной связи** в Microsoft Edge DevTools или твит [@EdgeDevTools][TwitterTweetEdgeDevTools] , чтобы команда знала, что вы думаете.  


:::image type="complex" source="./devtools-guide-chromium/media/devtools-feedback.png" alt-text="Значок обратной связи в Microsoft Edge DevTools":::
   Значок **обратной связи** в Microsoft Edge DevTools  
:::image-end:::

<!--  
> ##### Figure 3  
> The **Feedback** icon in the Microsoft Edge DevTools  
> ![The example.png file produced by example.js][ImageDevtoolsGuideChromiumMediaDevtoolsFeedback])  
-->  

<!-- image links -->  

<!--[ImageWebdriverChromiumEdgeVersion]: ./media/webdriver-chromium/edge-version.png "Figure 1: The build number for Microsoft Edge Canary on January 14, 2020"  -->  
<!--[ImageWebdriverChromiumEdgeDriverInstall]: ./media/webdriver-chromium/edge-driver-install.png "Figure 2: The Downloads section of the Microsoft Edge Driver page"  -->
<!--[ImageDevtoolsGuideChromiumMediaDevtoolsFeedback]: ./devtools-guide-chromium/media/devtools-feedback.png "Figure 3: The example.png file produced by example.js"  -->  

<!-- links -->  

[Webdriver]: ./webdriver.md "[EdgeHTML) | Документы Microsoft"  

[Chocolatey]: https://chocolatey.org "Шоколад | Шоколадное программное обеспечение"  
[ChocolateyPackagesSeleniumChromiumEdgeDriver]: https://chocolatey.org/packages/selenium-chromium-edge-driver "Драйвер Selenium Chromium Edge | Шоколад"  

[DockerHub]: https://hub.docker.com "Закрепляемый центр"  
[DockerHubMsedgedriver]: https://hub.docker.com/_/microsoft-msedge-msedgedriver?tab=description "msedgedriver | Закрепляемый центр"  

[GithubMicrosoftEdgeSeleniumTools]: https://github.com/microsoft/edge-selenium-tools "Microsoft/Edge-Selenium-Tools | GitHub"  
[GithubSeleniumHq]: https://github.com/SeleniumHQ/selenium "SeleniumHQ/Selenium | GitHub"  

[MicrosoftDeveloperEdgeToolsWebdriver]: https://developer.microsoft.com/microsoft-edge/tools/webdriver "[Стример] | Разработчик Майкрософт"
[MicrosoftDeveloperEdgeToolsWebdriverDownloads]: https://developer.microsoft.com/microsoft-edge/tools/webdriver/#downloads "Загружаемые файлы — "[стример" | Разработчик Майкрософт"  

[MicrosoftEdge]: https://www.microsoft.com/edge "Скачать новый браузер Microsoft Edge"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Скачайте каналы предварительной оценки Microsoft Edge"  

[NugetPackagesMicrosoftEdgeSeleniumtools]: https://www.nuget.org/packages/Microsoft.Edge.SeleniumTools "Microsoft. Edge. SeleniumTools | Коллекция NuGet"  
[NugetPackagesSeleniumWebdriver31410]: https://www.nuget.org/packages/Selenium.WebDriver/3.141.0 "Selenium. 3.141.0 | Коллекция NuGet"  
[NugetPackagesSeleniumWebdriver400alpha05]: https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha05 "Selenium. 4.0.0-alpha05 | Коллекция NuGet"  

[SeleniumHQ]: https://www.selenium.dev "SeleniumHQ"  
[SeleniumDownloads]: https://selenium.dev/downloads "Загрузки | Selenium"  
[SeleniumWebDriverChromeoptionsClass]: https://www.selenium.dev/selenium/docs/api/dotnet/?topic=html/T_OpenQA_Selenium_Chrome_ChromeOptions.htm "Класс ChromeOptions-стример | Selenium"  

[TwitterTweetEdgeDevTools]: https://twitter.com/intent/tweet?text=@EdgeDevTools "@EdgeDevTools | Публикация твита"  

[W3CWebdriver]: https://w3.org/TR/webdriver2 "Довода"  

[WikiHeadlessBrowser]: https://en.wikipedia.org/wiki/Headless_browser "Автономный браузер | Википедии"