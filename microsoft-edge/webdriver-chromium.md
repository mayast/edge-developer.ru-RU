---
description: Сведения о том, как протестировать веб-сайт или приложение в Microsoft EDGE, а также автоматизировать браузер с помощью Web Drive.
title: Chromium
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/18/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft EDGE, веб-разработка, HTML, CSS, сценарий JavaScript, разработчик, веб-дисковод, Selenium, тестирование, инструменты, Автоматизация и тестирование
ms.openlocfilehash: 810c45e1e8d7fb5a6dbefee1c4ae6eccbe573326
ms.sourcegitcommit: f5dc9d3f1e6629120e036c4298f66de636688cb7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/18/2020
ms.locfileid: "10659384"
---
# <span data-ttu-id="68391-104">Chromium</span><span class="sxs-lookup"><span data-stu-id="68391-104">WebDriver (Chromium)</span></span>  

<span data-ttu-id="68391-105">API веб- [накопителей][W3CWebdriver] W3C — это платформа и независимый от языка интерфейс и протокол проводной связи, позволяющая программам и сценариям управлять поведением браузера, например Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="68391-105">The W3C [WebDriver][W3CWebdriver] API is a platform and language-neutral interface and wire protocol allowing programs or scripts to control the behavior of a web browser, like Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="68391-106">С помощью этого устройства разработчики могут создавать автоматические тесты, имитирующие взаимодействие с пользователем.</span><span class="sxs-lookup"><span data-stu-id="68391-106">WebDriver enables developers to create automated tests that simulate user interaction.</span></span>  <span data-ttu-id="68391-107">Тесты и эмуляции веб-дисков отличаются от модульных тестов JavaScript, так как веб-дисководы имеют доступ к функциональным возможностям и сведениям, которые JavaScript запускается в браузере, а также позволяют лучше имитировать события пользователей и события на уровне операционной системы.</span><span class="sxs-lookup"><span data-stu-id="68391-107">WebDriver tests and simulations differ from JavaScript unit tests because WebDriver has access to functionality and information that JavaScript running in the browser does not, and WebDrive is able to more accurately simulate user events or OS-level events.</span></span>  <span data-ttu-id="68391-108">С помощью веб-диска можно управлять тестированием между несколькими окнами, вкладками и страницами в одном тестовом сеансе.</span><span class="sxs-lookup"><span data-stu-id="68391-108">WebDriver is able to manage testing across multiple windows, tabs and webpages in a single test session.</span></span>  

<span data-ttu-id="68391-109">Вот как начать работу с веб-дисководом для Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="68391-109">Here is how to get started with WebDriver for Microsoft Edge \(Chromium\).</span></span>  

## <span data-ttu-id="68391-110">Установка Microsoft EDGE (Chromium)</span><span class="sxs-lookup"><span data-stu-id="68391-110">Install Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="68391-111">[Установите Microsoft EDGE (Chromium)][MicrosoftEdge], если вы еще не сделали этого.</span><span class="sxs-lookup"><span data-stu-id="68391-111">If you have not already, [install Microsoft Edge (Chromium)][MicrosoftEdge].</span></span>  <span data-ttu-id="68391-112">Если вы используете предварительно установленную версию Microsoft EDGE на своем компьютере, убедитесь в том, что у вас есть Microsoft Edge \ (Chromium \), а не Microsoft Edge \ (EdgeHTML \).</span><span class="sxs-lookup"><span data-stu-id="68391-112">If you are using a pre-installed version of Microsoft Edge on your machine, verify that you have Microsoft Edge \(Chromium\) and not Microsoft Edge \(EdgeHTML\).</span></span>  <span data-ttu-id="68391-113">Чтобы быстро проверить, нужно ли загрузить `edge://settings/help` браузер и убедиться, что номер версии — V75 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="68391-113">A quick way to check is to load `edge://settings/help` in the browser and confirm that the version number is v75 or later.</span></span>  

## <span data-ttu-id="68391-114">Скачать драйвер Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="68391-114">Download Microsoft Edge Driver</span></span>  

<span data-ttu-id="68391-115">Для автоматизации каждого браузера для веб-дисковода необходим драйвер, зависящий от браузера.</span><span class="sxs-lookup"><span data-stu-id="68391-115">WebDriver requires a browser-specific driver to automate each browser.</span></span>  <span data-ttu-id="68391-116">Для Microsoft Edge \ (Chromium \) требуется соответствующий [драйвер Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver] для сборки Microsoft EDGE, которую вы хотите протестировать или автоматизировать.</span><span class="sxs-lookup"><span data-stu-id="68391-116">For Microsoft Edge \(Chromium\), WebDriver requires the appropriate [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] for the build of Microsoft Edge you want to test or automate.</span></span>  

<span data-ttu-id="68391-117">Чтобы найти правильный номер сборки, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="68391-117">To find your correct build number, use the following steps.</span></span>  

1.  <span data-ttu-id="68391-118">Запуск Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="68391-118">Launch Microsoft Edge</span></span> 
1.  <span data-ttu-id="68391-119">Просмотреть версию Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="68391-119">View the Microsoft Edge \(Chromium\) version.</span></span>  
    *   <span data-ttu-id="68391-120">Перейдите к</span><span class="sxs-lookup"><span data-stu-id="68391-120">Navigate to</span></span> `edge://settings/help`  
    *   <span data-ttu-id="68391-121">Выберите `...`  >  **Параметры**  >   **о Microsoft Edge**</span><span class="sxs-lookup"><span data-stu-id="68391-121">Select `...` > **Settings** >  **About Microsoft Edge**</span></span>  
1.  <span data-ttu-id="68391-122">Убедитесь в том, что для сборки указана нужная версия, чтобы она правильно выполнялась.</span><span class="sxs-lookup"><span data-stu-id="68391-122">Verify the correct version of WebDriver for your build ensures, so it runs correctly.</span></span>  

:::image type="complex" source="./media/webdriver-chromium/edge-version.png" alt-text="Номер сборки Microsoft Edge Канарские 14 января 2020 г.":::
   <span data-ttu-id="68391-124">Рисунок 1.</span><span class="sxs-lookup"><span data-stu-id="68391-124">Figure 1.</span></span>  <span data-ttu-id="68391-125">Номер сборки Microsoft Edge Канарские 14 января 2020 г.</span><span class="sxs-lookup"><span data-stu-id="68391-125">The build number for Microsoft Edge Canary on January 14, 2020</span></span>  
:::image-end:::  

<span data-ttu-id="68391-126">Теперь [Загрузите соответствующую версию драйвера Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriverDownloads].</span><span class="sxs-lookup"><span data-stu-id="68391-126">Now, [download the matching version of Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriverDownloads].</span></span>  

:::image type="complex" source="./media/webdriver-chromium/edge-driver-install.png" alt-text="Раздел "загружаемые файлы" на странице драйвера Microsoft Edge":::
   <span data-ttu-id="68391-128">Рисунок 2.</span><span class="sxs-lookup"><span data-stu-id="68391-128">Figure 2.</span></span>  <span data-ttu-id="68391-129">Раздел "загружаемые файлы" на странице [драйвера Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriverDownloads]</span><span class="sxs-lookup"><span data-stu-id="68391-129">The Downloads section of the [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriverDownloads] page</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="68391-130">Microsoft Edge \ (EdgeHTML \) не работает с [драйвером Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriverDownloads].</span><span class="sxs-lookup"><span data-stu-id="68391-130">Microsoft Edge \(EdgeHTML\) does not work with [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriverDownloads].</span></span>  <span data-ttu-id="68391-131">Для автоматизации Microsoft Edge \ (EdgeHTML \) необходимо загрузить [Microsoft для Microsoft Edge \ (EdgeHTML \)][Webdriver].</span><span class="sxs-lookup"><span data-stu-id="68391-131">To automate Microsoft Edge \(EdgeHTML\), you must download [Microsoft WebDriver for Microsoft Edge \(EdgeHTML\)][Webdriver].</span></span>  

## <span data-ttu-id="68391-132">Выбор языковой привязки для веб-дисков</span><span class="sxs-lookup"><span data-stu-id="68391-132">Choose a WebDriver language binding</span></span>  

<span data-ttu-id="68391-133">Последним компонентом, который необходимо скачать, является драйвер клиента, зависящий от языка.</span><span class="sxs-lookup"><span data-stu-id="68391-133">The last component you must download is a language-specific client driver.</span></span>  <span data-ttu-id="68391-134">Языковая привязка преобразует код, написанный в Python, Java, C \ #, Ruby и JavaScript, в команды, которые драйвер Microsoft EDGE, [загруженный в предыдущем разделе](#download-microsoft-edge-driver) , может работать в Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="68391-134">The language binding translates the code you write in Python, Java, C\#, Ruby, and JavaScript into commands that the Microsoft Edge Driver you [downloaded in the previous section](#download-microsoft-edge-driver) is able to run in Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="68391-135">[Скачайте выбранную вами языковую привязку веб дисков][SeleniumDownloads].</span><span class="sxs-lookup"><span data-stu-id="68391-135">[Download the WebDriver language binding of your choice][SeleniumDownloads].</span></span>  <span data-ttu-id="68391-136">Группа Microsoft Edge настоятельно рекомендует [Selenium 4,00-alpha05][NugetPackagesSeleniumWebdriver400alpha05] или более поздней версии, так как она содержит встроенную поддержку Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="68391-136">The Microsoft Edge team highly recommends [Selenium 4.00-alpha05][NugetPackagesSeleniumWebdriver400alpha05] or later, since it has built-in support for Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="68391-137">Однако вы можете подключаться к Microsoft Edge \ (Chromium \) во всех более ранних версиях Selenium, включая текущую стабильную версию Selenium 3.</span><span class="sxs-lookup"><span data-stu-id="68391-137">However, you are able to drive Microsoft Edge \(Chromium\) in all older versions of Selenium, including the current stable Selenium 3 release.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="68391-138">Если вы уже выполняли автоматизацию или тестирование Microsoft Edge \ (Chromium \), используя `ChromeDriver` и `ChromeOptions` , код веб-дисковода не запустится в Microsoft Edge V80 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="68391-138">If you were previously automating or testing Microsoft Edge \(Chromium\) by using `ChromeDriver` and `ChromeOptions`, your WebDriver code does not run successfully against Microsoft Edge v80 or later.</span></span>  <span data-ttu-id="68391-139">Это критическое изменение, а Microsoft Edge \ (Chromium \) больше не принимает команды.</span><span class="sxs-lookup"><span data-stu-id="68391-139">This is a breaking change and Microsoft Edge \(Chromium\) no longer accepts the commands.</span></span>  <span data-ttu-id="68391-140">Необходимо изменить тесты, чтобы использовать `EdgeOptions` драйвер класса и [Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver].</span><span class="sxs-lookup"><span data-stu-id="68391-140">You must change your tests to use the `EdgeOptions` class and [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver].</span></span>  

### <span data-ttu-id="68391-141">Использование Selenium 3</span><span class="sxs-lookup"><span data-stu-id="68391-141">Using Selenium 3</span></span>  

<span data-ttu-id="68391-142">[Selenium 3][|::ref1::|] – это новейшая стабильный выпуск Selenium.</span><span class="sxs-lookup"><span data-stu-id="68391-142">[Selenium 3][|::ref1::|] is the latest stable Selenium release.</span></span>  <span data-ttu-id="68391-143">По умолчанию Selenium 3 использует старый Microsoft Edge \ (EdgeHTML \) и не имеет встроенной поддержки Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="68391-143">By default, Selenium 3 drives the old Microsoft Edge \(EdgeHTML\), and does not have built-in support for Microsoft Edge \(Chromium\).</span></span>  <span data-ttu-id="68391-144">Чтобы использовать Selenium 3 с Microsoft Edge \ (Chromium \), установите пакет [инструментов Selenium для Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] .</span><span class="sxs-lookup"><span data-stu-id="68391-144">To use Selenium 3 with Microsoft Edge \(Chromium\), install the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] package.</span></span>  <span data-ttu-id="68391-145">Selenium Tools for Microsoft Edge расширяет Selenium 3 с помощью обновленного драйвера, который поможет вам создавать автоматические тесты для обоих браузеров Microsoft Edge \ (EdgeHTML \) и новых Microsoft Edge \ (Chromium).</span><span class="sxs-lookup"><span data-stu-id="68391-145">The Selenium Tools for Microsoft Edge extend Selenium 3 with an updated driver to help you write automated tests for both the Microsoft Edge \(EdgeHTML\) and new Microsoft Edge \(Chromium\) browsers.</span></span>  

<span data-ttu-id="68391-146">Selenium Tools for Microsoft Edge — это решение для разработчиков, которые хотят оставаться на Selenium 3 и разработчиках с существующими тестами браузера и добавлять покрытие для нового браузера Microsoft Edge \ (Chromium \) без изменения версий Selenium.</span><span class="sxs-lookup"><span data-stu-id="68391-146">Selenium Tools for Microsoft Edge is a solution for developers who prefer to remain on Selenium 3 and developers who have existing browser tests and want to add coverage for the new Microsoft Edge \(Chromium\) browser without changing Selenium versions.</span></span>  <span data-ttu-id="68391-147">`EdgeDriver`Классы и `EdgeDriverService` включенные в них компоненты полностью совместимы с встроенными эквивалентами в Selenium и выполняют Microsoft Edge \ (EdgeHTML \) по умолчанию, поэтому эти средства можно использовать в качестве неполной замены для существующих классов EDGE в Selenium.</span><span class="sxs-lookup"><span data-stu-id="68391-147">The `EdgeDriver` and `EdgeDriverService` classes included in the tools are fully compatible with the built-in equivalents in Selenium, and run Microsoft Edge \(EdgeHTML\) by default so the tools may be used as a seamless drop-in replacement for the existing Edge classes in Selenium.</span></span>  

<span data-ttu-id="68391-148">[Установите средства Selenium для Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] , чтобы приступить к работе с Microsoft Edge \ (Chromium \) с проектом Selenium 3.</span><span class="sxs-lookup"><span data-stu-id="68391-148">[Install Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] to begin using Microsoft Edge \(Chromium\) with your Selenium 3 project.</span></span>  

## <span data-ttu-id="68391-149">Использование веб-накопителя (Microsoft EDGE (Chromium))</span><span class="sxs-lookup"><span data-stu-id="68391-149">Use Microsoft Edge (Chromium) with WebDriver</span></span>

<span data-ttu-id="68391-150">Следующие примеры выполняются с помощью либо Selenium 3, либо 4.</span><span class="sxs-lookup"><span data-stu-id="68391-150">The following examples are runnable using either Selenium 3 or 4.</span></span>  <span data-ttu-id="68391-151">Для использования с Selenium 3 должны быть установлены [средства Selenium для Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] .</span><span class="sxs-lookup"><span data-stu-id="68391-151">To use with Selenium 3, the [Selenium Tools for Microsoft Edge][GithubMicrosoftEdgeSeleniumTools] must be installed.</span></span>  

### <span data-ttu-id="68391-152">Основное использование</span><span class="sxs-lookup"><span data-stu-id="68391-152">Basic Usage</span></span>  

<span data-ttu-id="68391-153">Для использования в Microsoft Edge \ (EdgeHTML \) просто создайте экземпляр класса по умолчанию `EdgeDriver` .</span><span class="sxs-lookup"><span data-stu-id="68391-153">To use with Microsoft Edge \(EdgeHTML\), simply create a default instance of the `EdgeDriver` class.</span></span>

#### [<span data-ttu-id="68391-154">C#</span><span class="sxs-lookup"><span data-stu-id="68391-154">C#</span></span>](#tab/c-sharp/)  

<a id="basic-usage-code" />  

```csharp
var driver = new EdgeDriver();
```  

#### [<span data-ttu-id="68391-155">Языке</span><span class="sxs-lookup"><span data-stu-id="68391-155">Python</span></span>](#tab/python/)  

<a id="basic-usage-code" />  

```python
driver = Edge()
```  

* * *  

### <span data-ttu-id="68391-156">Управление Microsoft EDGE (Chromium)</span><span class="sxs-lookup"><span data-stu-id="68391-156">Driving Microsoft Edge (Chromium)</span></span>  

<span data-ttu-id="68391-157">Для использования с Microsoft Edge \ (Chromium \) вместо этого создайте новый `EdgeDriver` класс и передайте ему `EdgeOptions` объект со `UseChromium` свойством, для которого задано значение `true` .</span><span class="sxs-lookup"><span data-stu-id="68391-157">To use with Microsoft Edge \(Chromium\) instead, create a new `EdgeDriver` class and pass it the `EdgeOptions` object with the `UseChromium` property set to `true`.</span></span>  

#### [<span data-ttu-id="68391-158">C#</span><span class="sxs-lookup"><span data-stu-id="68391-158">C#</span></span>](#tab/c-sharp/)  

<a id="diving-microsoft-edge-chromium-code" />  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;

var driver = new EdgeDriver(options);
```  

#### [<span data-ttu-id="68391-159">Языке</span><span class="sxs-lookup"><span data-stu-id="68391-159">Python</span></span>](#tab/python/)  

<a id="diving-microsoft-edge-chromium-code" />  

```python
options = EdgeOptions()
options.use_chromium = True

driver = Edge(options)
```  

* * *  

### <span data-ttu-id="68391-160">Выбор определенных двоичных файлов браузера (только Chromium)</span><span class="sxs-lookup"><span data-stu-id="68391-160">Choosing Specific Browser Binaries (Chromium-Only)</span></span>  

<span data-ttu-id="68391-161">Используйте этот `EdgeOptions` класс для выбора определенного двоичного файла.</span><span class="sxs-lookup"><span data-stu-id="68391-161">Use the `EdgeOptions` class to choose a specific binary.</span></span>  <span data-ttu-id="68391-162">Это полезно при тестировании [каналов предварительной версии Microsoft Edge][MicrosoftedgeinsiderDownload] , таких как Microsoft Edge Beta.</span><span class="sxs-lookup"><span data-stu-id="68391-162">It is useful for testing [Microsoft Edge preview channels][MicrosoftedgeinsiderDownload] such as Microsoft Edge Beta.</span></span>  

#### [<span data-ttu-id="68391-163">C#</span><span class="sxs-lookup"><span data-stu-id="68391-163">C#</span></span>](#tab/c-sharp/)  

<a id="choosing-specific-browser-binaries-chrome-only-code" />  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.BinaryLocation = @"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe";

var driver = new EdgeDriver(options);
```  

#### [<span data-ttu-id="68391-164">Языке</span><span class="sxs-lookup"><span data-stu-id="68391-164">Python</span></span>](#tab/python/)  

<a id="choosing-specific-browser-binaries-chrome-only-code" />  

```python
options = EdgeOptions()
options.use_chromium = True
options.binary_location = r"C:\Program Files (x86)\Microsoft\Edge Beta\Application\msedge.exe"

driver = Edge(options)
```  

* * *  

### <span data-ttu-id="68391-165">Настройка службы драйвера Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="68391-165">Customizing the Microsoft Edge Driver Service</span></span>  

#### [<span data-ttu-id="68391-166">C#</span><span class="sxs-lookup"><span data-stu-id="68391-166">C#</span></span>](#tab/c-sharp/)  

<a id="customizing-microsoft-edge-driver-services-code" />  

<span data-ttu-id="68391-167">Если `EdgeDriver` экземпляр класса создается с помощью `EdgeOptions` класса, он автоматически создает и запускает соответствующий `EdgeDriverService` класс для Microsoft Edge \ (EdgeHTML \) или Microsoft Edge \ (Chromium \).</span><span class="sxs-lookup"><span data-stu-id="68391-167">When an `EdgeDriver` class instance is created using `EdgeOptions` class, it automatically creates and launches the appropriate `EdgeDriverService` class for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\).</span></span>  

<span data-ttu-id="68391-168">Если вы хотите создать объект `EdgeDriverService` для Microsoft Edge \ (Chromium \) с помощью метода, создайте его `CreateChromiumService()` .</span><span class="sxs-lookup"><span data-stu-id="68391-168">If you want to create an `EdgeDriverService`, create one configured for Microsoft Edge \(Chromium\) using the `CreateChromiumService()` method.</span></span>  <span data-ttu-id="68391-169">Вы можете использовать дополнительные настройки, такие как включение подробного вывода журнала в приведенном ниже коде.</span><span class="sxs-lookup"><span data-stu-id="68391-169">You may find it useful for additional customizations like enabling verbose log output in the following code.</span></span>  

```csharp
using (var service = EdgeDriverService.CreateChromiumService())
{
    service.UseVerboseLogging = true;

    var driver = new EdgeDriver(service);
}
```  

> [!NOTE]
> <span data-ttu-id="68391-170">Вам не нужно предоставлять `EdgeOptions` объект при передаче `EdgeDriver` экземпляра класса `EdgeDriverService` .</span><span class="sxs-lookup"><span data-stu-id="68391-170">You do not need to provide the `EdgeOptions` object when passing the `EdgeDriver` class instance the `EdgeDriverService`.</span></span>  <span data-ttu-id="68391-171">Этот `EdgeDriver` класс использует параметры по умолчанию (Microsoft Edge \ (EdgeHTML \) или Microsoft Edge \ (Chromium \) в зависимости от типа предоставляемой услуги.</span><span class="sxs-lookup"><span data-stu-id="68391-171">The `EdgeDriver` class uses the default options for either Microsoft Edge \(EdgeHTML\) or Microsoft Edge \(Chromium\) depending on what kind of service you provide.</span></span>  
> 
> <span data-ttu-id="68391-172">Тем не менее, если вы хотите предоставить оба `EdgeDriverService` `EdgeOptions` класса и классы, необходимо убедиться, что оба они настроены для одной и той же версии Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="68391-172">However, if you want to provide both an `EdgeDriverService` and `EdgeOptions` classes, you must ensure that both are configured for the same version of Microsoft Edge.</span></span>  <span data-ttu-id="68391-173">Например, невозможно использовать класс по умолчанию Microsoft Edge \ (EdgeHTML \) `EdgeDriverService` и свойства Chromium в `EdgeOptions` классе.</span><span class="sxs-lookup"><span data-stu-id="68391-173">For example, it is not possible to use a default Microsoft Edge \(EdgeHTML\) `EdgeDriverService` class and Chromium properties in the `EdgeOptions` class.</span></span>  <span data-ttu-id="68391-174">`EdgeDriver`Класс вызывает ошибку, чтобы предотвратить использование разных версий.</span><span class="sxs-lookup"><span data-stu-id="68391-174">The `EdgeDriver` class throws an error to prevent using different versions.</span></span>  

#### [<span data-ttu-id="68391-175">Языке</span><span class="sxs-lookup"><span data-stu-id="68391-175">Python</span></span>](#tab/python/)  

<a id="customizing-microsoft-edge-driver-services-code" />  

<span data-ttu-id="68391-176">При использовании Python `Edge` объект создает и управляет `EdgeService` .</span><span class="sxs-lookup"><span data-stu-id="68391-176">When using Python, the `Edge` object creates and manages the `EdgeService`.</span></span>  <span data-ttu-id="68391-177">Чтобы настроить `EdgeService` , передайте объекту дополнительные аргументы `Edge` .</span><span class="sxs-lookup"><span data-stu-id="68391-177">To configure the `EdgeService`, pass additional arguments to the `Edge` object:</span></span>

```python
service_args = ['--verbose']
driver = Edge(service_args = service_args)
```  

* * *  

### <span data-ttu-id="68391-178">Использование параметров, специфичных для Chromium</span><span class="sxs-lookup"><span data-stu-id="68391-178">Using Chromium-Specific Options</span></span>  

<span data-ttu-id="68391-179">Использование `EdgeOptions` класса с `UseChromium` установленным свойством `true` предоставляет доступ ко всем тем же методам и свойствам, которые доступны в классе [ChromeOptions][SeleniumWebDriverChromeoptionsClass] в Selenium.</span><span class="sxs-lookup"><span data-stu-id="68391-179">Using the `EdgeOptions` class with the `UseChromium` property set to `true` gives you access to all of the same methods and properties that are available in the [ChromeOptions][SeleniumWebDriverChromeoptionsClass] class in Selenium.</span></span>  <span data-ttu-id="68391-180">Например, как и в других браузерах Chromium, используйте `EdgeOptions.AddArguments()` метод для запуска Microsoft Edge \ (Chromium \) в [режиме бездисплейного режима][WikiHeadlessBrowser] в приведенном ниже коде.</span><span class="sxs-lookup"><span data-stu-id="68391-180">For example, just like with other Chromium browsers, use the `EdgeOptions.AddArguments()` method to run Microsoft Edge \(Chromium\) in [headless mode][WikiHeadlessBrowser] in the following code.</span></span>  

#### [<span data-ttu-id="68391-181">C#</span><span class="sxs-lookup"><span data-stu-id="68391-181">C#</span></span>](#tab/c-sharp/)  

<a id="using-chromium-specific-options-code" />  

```csharp
var options = new EdgeOptions();
options.UseChromium = true;
options.AddArgument("headless");
options.AddArgument("disable-gpu");
```  

#### [<span data-ttu-id="68391-182">Языке</span><span class="sxs-lookup"><span data-stu-id="68391-182">Python</span></span>](#tab/python/)  

<a id="using-chromium-specific-options-code" />  

```python
options = EdgeOptions()
options.use_chromium = True
options.add_argument('headless')
options.add_argument('disable-gpu')
```  

* * *  

> [!NOTE]
> <span data-ttu-id="68391-183">[Свойства и методы, связанные с Chromium][SeleniumWebDriverChromeoptionsClass] , всегда доступны, но не имеют никакого эффекта, если `UseChromium` свойство не задано `true` .</span><span class="sxs-lookup"><span data-stu-id="68391-183">The [Chromium-specific properties and methods][SeleniumWebDriverChromeoptionsClass] are always available but have no effect if the `UseChromium` property is not set to `true`.</span></span>  <span data-ttu-id="68391-184">Аналогичным образом существующие свойства и методы, предназначенные для Microsoft Edge \ (EdgeHTML \), не применяются, если `UseChromium` для свойства задано значение `true` .</span><span class="sxs-lookup"><span data-stu-id="68391-184">Similarly, existing properties and methods meant for Microsoft Edge \(EdgeHTML\) have no effect if `UseChromium` property is set to `true`.</span></span>  

## <span data-ttu-id="68391-185">Другие способы настройки устройства</span><span class="sxs-lookup"><span data-stu-id="68391-185">Other ways to set up WebDriver</span></span>  

### <span data-ttu-id="68391-186">Шоколад</span><span class="sxs-lookup"><span data-stu-id="68391-186">Chocolatey</span></span>  

<span data-ttu-id="68391-187">Если вы используете [шоколад][Chocolatey] в качестве диспетчера пакетов, установите драйвер Microsoft EDGE, выполнив следующую команду:</span><span class="sxs-lookup"><span data-stu-id="68391-187">If you are using [Chocolatey][Chocolatey] as your package manager, install the Microsoft Edge Driver by running the following command.</span></span>  

```console
choco install selenium-chromium-edge-driver
```  

<span data-ttu-id="68391-188">Дополнительные сведения можно найти [в разделе драйвер Selenium Chromium EDGE на шоколаде][ChocolateyPackagesSeleniumChromiumEdgeDriver].</span><span class="sxs-lookup"><span data-stu-id="68391-188">For more information, see [Selenium Chromium Edge Driver on Chocolatey][ChocolateyPackagesSeleniumChromiumEdgeDriver].</span></span>  

### <span data-ttu-id="68391-189">Docker</span><span class="sxs-lookup"><span data-stu-id="68391-189">Docker</span></span>  

<span data-ttu-id="68391-190">Если вы используете [закрепление][DockerHub], скачайте предварительно настроенное изображение с помощью Microsoft Edge \ (Chromium \) и [Microsoft Edge][MicrosoftDeveloperEdgeToolsWebdriver] , которое уже установлено, выполнив следующую команду:</span><span class="sxs-lookup"><span data-stu-id="68391-190">If you are using [Docker][DockerHub], download a pre-configured image with Microsoft Edge \(Chromium\) and [Microsoft Edge Driver][MicrosoftDeveloperEdgeToolsWebdriver] already installed by running the following command.</span></span>  

```console
docker run -d -p 9515:9515 mcr.microsoft.com/msedge/msedgedriver
```  

<span data-ttu-id="68391-191">Дополнительные сведения можно найти [в разделе контейнер в центре Dock][DockerHubMsedgedriver].</span><span class="sxs-lookup"><span data-stu-id="68391-191">For more information, see [container on Docker Hub][DockerHubMsedgedriver].</span></span>  

## <span data-ttu-id="68391-192">Знакомство с командой Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="68391-192">Getting in touch with the Microsoft Edge DevTools team</span></span>    

<span data-ttu-id="68391-193">Группа Microsoft Edge – это информация о том, как использовать веб – диски, Selenium и Microsoft Edge!</span><span class="sxs-lookup"><span data-stu-id="68391-193">The Microsoft Edge team is eager to hear your feedback about using WebDriver, Selenium, and Microsoft Edge!</span></span>  <span data-ttu-id="68391-194">С помощью значка **обратной связи** в Microsoft Edge DevTools или твит [@EdgeDevTools][TwitterTweetEdgeDevTools] , чтобы команда знала, что вы думаете.</span><span class="sxs-lookup"><span data-stu-id="68391-194">Use the **Feedback** icon in the Microsoft Edge DevTools or tweet [@EdgeDevTools][TwitterTweetEdgeDevTools] to let the team know what you think.</span></span>  


:::image type="complex" source="./devtools-guide-chromium/media/devtools-feedback.png" alt-text="Значок обратной связи в Microsoft Edge DevTools":::
   <span data-ttu-id="68391-196">Значок **обратной связи** в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="68391-196">The **Feedback** icon in the Microsoft Edge DevTools</span></span>  
:::image-end:::  

<!-- image links -->  

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
