---
description: Автоматизация и тестирование элемента управления WebView2 с помощью драйвера Microsoft Edge
title: Автоматизация и тестирование WebView2 с помощью драйвера Microsoft Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/10/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: IWebView2, IWebView2WebView, webview2, WebView, EDGE, ICoreWebView2, ICoreWebView2Controller, Selenium, драйвер Microsoft Edge
ms.openlocfilehash: a91c01d1ad765dae45061e382daedc2295d70bb8
ms.sourcegitcommit: 4bc904c5d54347185f275bd76441975be471c320
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/12/2020
ms.locfileid: "10926450"
---
# <span data-ttu-id="14e99-104">Автоматизация и тестирование WebView2 с помощью драйвера Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="14e99-104">Automating and testing WebView2 with Microsoft Edge Driver</span></span>

<span data-ttu-id="14e99-105">Так как WebView2 использует веб-платформу Chromium, WebView2 разработчики могут воспользоваться стандартными веб-средствами для отладки и автоматизации.</span><span class="sxs-lookup"><span data-stu-id="14e99-105">Because WebView2 utilizes the Chromium web platform, WebView2 developers can take advantage of standard web tooling for debugging and automation.</span></span> <span data-ttu-id="14e99-106">Одним из таких средств является Selenium, реализующий API [-](https://www.w3.org/TR/webdriver2/) интерфейс консорциума W3C, который можно использовать для создания автоматических тестов, имитирующих взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="14e99-106">One such tool is Selenium, which implements the W3C [WebDriver](https://www.w3.org/TR/webdriver2/) API, which can be used to create automated tests that simulate user interactions.</span></span>

<span data-ttu-id="14e99-107">Порядок начала работы:</span><span class="sxs-lookup"><span data-stu-id="14e99-107">Here's how to get started:</span></span>

## <span data-ttu-id="14e99-108">Шаг 1: Загрузка образца WebView2API</span><span class="sxs-lookup"><span data-stu-id="14e99-108">Step 1: Download WebView2API Sample</span></span>

<span data-ttu-id="14e99-109">Если у вас нет проекта WebView2, скачайте наш [пример приложения WebView2API](https://github.com/MicrosoftEdge/WebView2Samples/tree/master/WebView2APISample#webview2-api-sample), который является исчерпывающим примером НОВЕЙШего комплекта SDK для WebView2.</span><span class="sxs-lookup"><span data-stu-id="14e99-109">If you do not have an existing WebView2 project, download our [WebView2API Sample application](https://github.com/MicrosoftEdge/WebView2Samples/tree/master/WebView2APISample#webview2-api-sample), a comprehensive sample of the latest WebView2 SDK.</span></span> <span data-ttu-id="14e99-110">Убедитесь в том, что вы удовлетворены [необходимыми условиями](https://github.com/MicrosoftEdge/WebView2Samples/tree/master/WebView2APISample#prerequisites).</span><span class="sxs-lookup"><span data-stu-id="14e99-110">Please double check that you have satisfied these [prerequisites](https://github.com/MicrosoftEdge/WebView2Samples/tree/master/WebView2APISample#prerequisites).</span></span>

<span data-ttu-id="14e99-111">Создав точную копию репозитория, создайте проект в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="14e99-111">Once you have cloned the repo, build the project in Visual Studio.</span></span> <span data-ttu-id="14e99-112">Он должен выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="14e99-112">It should look like the following:</span></span>

![замещающий текст](../media/webdriver/sample-app.png)

## <span data-ttu-id="14e99-114">Шаг 2: Установка драйвера Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="14e99-114">Step 2: Install Microsoft Edge Driver</span></span>

<span data-ttu-id="14e99-115">Следуйте инструкциям, чтобы установить [драйвер Microsoft Edge](https://docs.microsoft.com/microsoft-edge/webdriver-chromium#download-microsoft-edge-driver) , необходимый для автоматизации и тестирования WebView2, который требуется драйверу Selenium для веб-браузера.</span><span class="sxs-lookup"><span data-stu-id="14e99-115">Follow the instructions to install [Microsoft Edge Driver](https://docs.microsoft.com/microsoft-edge/webdriver-chromium#download-microsoft-edge-driver) the browser-specific driver required by Selenium to automate and test WebView2.</span></span>

<span data-ttu-id="14e99-116">Важно убедиться, что версия драйвера Microsoft EDGE соответствует версии Microsoft EDGE, используемой в приложении.</span><span class="sxs-lookup"><span data-stu-id="14e99-116">It is important to make sure that the version of Microsoft Edge Driver matches the version of Microsoft Edge that the application uses.</span></span> <span data-ttu-id="14e99-117">Чтобы образец WebView2API работал, убедитесь в том, что ваша версия Microsoft Edge больше или равна поддерживаемой версии последней версии SDK, которую можно найти [в заметках о выпуске](https://docs.microsoft.com/microsoft-edge/hosting/webview2/releasenotes).</span><span class="sxs-lookup"><span data-stu-id="14e99-117">For the WebView2API Sample to work, make sure that your version of Microsoft Edge is greater than or equal to the supported version of our latest SDK release found [in our Release Notes](https://docs.microsoft.com/microsoft-edge/hosting/webview2/releasenotes).</span></span> <span data-ttu-id="14e99-118">Чтобы узнать, какая у вас версия Microsoft EDGE уже есть, загрузите ее `edge://settings/help` в браузере.</span><span class="sxs-lookup"><span data-stu-id="14e99-118">To find out what version of Microsoft Edge you currently have, load `edge://settings/help` in the browser.</span></span>

## <span data-ttu-id="14e99-119">Шаг 3: Добавление Selenium в пример WebView2API</span><span class="sxs-lookup"><span data-stu-id="14e99-119">Step 3: Add Selenium to the WebView2API Sample</span></span>

<span data-ttu-id="14e99-120">На этом этапе у вас должен быть установлен Microsoft EDGE, создан проект WebView2 и установлен драйвер Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="14e99-120">At this point you should have Microsoft Edge installed, built a WebView2 project, and installed Microsoft Edge Driver.</span></span> <span data-ttu-id="14e99-121">Теперь приступим к работе с Selenium.</span><span class="sxs-lookup"><span data-stu-id="14e99-121">Now, let's get started using Selenium.</span></span>

> [!NOTE]
> <span data-ttu-id="14e99-122">Selenium поддерживает C#, Java, Python, JavaScript и Ruby.</span><span class="sxs-lookup"><span data-stu-id="14e99-122">Selenium supports C#, Java, Python, Javascript, and Ruby.</span></span> <span data-ttu-id="14e99-123">Однако это руководство будет отображаться на C#.</span><span class="sxs-lookup"><span data-stu-id="14e99-123">However, this guide will be in C#.</span></span>

1. <span data-ttu-id="14e99-124">Начните с создания нового проекта **C# .NET Framework** в **Visual Studio**.</span><span class="sxs-lookup"><span data-stu-id="14e99-124">Start by creating a new **C# .NET Framework** project in **Visual Studio**.</span></span> <span data-ttu-id="14e99-125">Чтобы продолжить, нажмите кнопку **Далее** в правом нижнем углу.</span><span class="sxs-lookup"><span data-stu-id="14e99-125">Click **Next** on the bottom right-hand corner to continue.</span></span>

![замещающий текст](../media/webdriver/new-project.png)

2. <span data-ttu-id="14e99-127">Введите **имя**проекта, сохраните его в нужном **месте**и нажмите кнопку **создать**.</span><span class="sxs-lookup"><span data-stu-id="14e99-127">Give your project a **name**, save it to your preferred **location**, and click **Create**.</span></span>

![замещающий текст](../media/webdriver/app-create.png)

3. <span data-ttu-id="14e99-129">Будет создан новый проект.</span><span class="sxs-lookup"><span data-stu-id="14e99-129">A new project will be created.</span></span> <span data-ttu-id="14e99-130">В этом руководстве весь код будет написан в файле **Program.CS** .</span><span class="sxs-lookup"><span data-stu-id="14e99-130">In this guide, all code will be written in the **Program.cs** file.</span></span>

![замещающий текст](../media/webdriver/start-app.png)

4. <span data-ttu-id="14e99-132">Теперь добавим **Selenium** в проект.</span><span class="sxs-lookup"><span data-stu-id="14e99-132">Now let's add **Selenium** to the project.</span></span> <span data-ttu-id="14e99-133">Вы можете установить Selenium с помощью **пакета NuGet для Selenium.**</span><span class="sxs-lookup"><span data-stu-id="14e99-133">You can install Selenium via the **Selenium.WebDriver NuGet package**.</span></span>

<span data-ttu-id="14e99-134">Чтобы скачать **пакет NuGet Selenium...** в **Visual Studio**, наведите указатель мыши на элемент **Project** и выберите пункт **Управление пакетом NuGet**.</span><span class="sxs-lookup"><span data-stu-id="14e99-134">To download the **Selenium.WebDriver NuGet package**, in **Visual Studio**, hover over **Project** and select **Manage NuGet Package**.</span></span> <span data-ttu-id="14e99-135">Появится следующий экран:</span><span class="sxs-lookup"><span data-stu-id="14e99-135">The following screen should appear:</span></span>

![замещающий текст](../media/webdriver/download-nuget.png)

5. <span data-ttu-id="14e99-137">Введите **Selenium.** Selenium на панели поиска, щелкните **. стример** из результатов, а затем установите флажок **включить предварительную версию**.</span><span class="sxs-lookup"><span data-stu-id="14e99-137">Enter **Selenium.WebDriver** in the search bar, click **Selenium.WebDriver** from the results, and make sure to checkmark the box next to **include pre-release**.</span></span> <span data-ttu-id="14e99-138">В правой части окна убедитесь, что для **версии** установлено значение **4.0.0-alpha04** или более поздней, и нажмите кнопку **установить**.</span><span class="sxs-lookup"><span data-stu-id="14e99-138">On the right-hand side window, ensure the **Version** is set to **install 4.0.0-alpha04** or later and click **Install**.</span></span> <span data-ttu-id="14e99-139">NuGet загрузит Selenium на ваш компьютер.</span><span class="sxs-lookup"><span data-stu-id="14e99-139">Nuget will download Selenium to your machine.</span></span>

[<span data-ttu-id="14e99-140">Дополнительные сведения о пакете NuGet для Selenium.</span><span class="sxs-lookup"><span data-stu-id="14e99-140">Learn more about the Selenium.WebDriver NuGet package.</span></span>](https://www.nuget.org/packages/Selenium.WebDriver/4.0.0-alpha04)

![замещающий текст](../media/webdriver/nuget.png)

6. <span data-ttu-id="14e99-142">Используйте **OpenQA. Selenium. Edge** , добавив следующий оператор: ```using OpenQA.Selenium.Edge;``` в начале **Program.CS**</span><span class="sxs-lookup"><span data-stu-id="14e99-142">Use **OpenQA.Selenium.Edge** by adding the following statement:```using OpenQA.Selenium.Edge;``` at the beginning of **Program.cs**</span></span>

```csharp
using OpenQA.Selenium.Edge;

using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;
```

## <span data-ttu-id="14e99-143">Шаг 4: WebView2 диска с Selenium и Microsoft EdgeDriver</span><span class="sxs-lookup"><span data-stu-id="14e99-143">Step 4: Drive WebView2 with Selenium and Microsoft EdgeDriver</span></span>

1. <span data-ttu-id="14e99-144">Сначала создайте `EdgeOptions` объект, скопировав приведенный ниже код.</span><span class="sxs-lookup"><span data-stu-id="14e99-144">First, create the `EdgeOptions` object, by copying the code below:</span></span>

```csharp
static void Main(string[] args)
{
    // EdgeOptions() requires using OpenQA.Selenium.Edge
    // Construct EdgeOptions with is_legacy = false and the string "webview2"
    EdgeOptions edgeOptions = new EdgeOptions(false, "webview2");
```

<span data-ttu-id="14e99-145">`EdgeOptions`Объект принимает два параметра:</span><span class="sxs-lookup"><span data-stu-id="14e99-145">The `EdgeOptions` object takes in two parameters:</span></span>
\
    **<span data-ttu-id="14e99-146">Параметры</span><span class="sxs-lookup"><span data-stu-id="14e99-146">Parameters:</span></span>**
    1. `is_legacy`<span data-ttu-id="14e99-147">: значение `false` , указывающее Selenium, что вы управляете новым браузером Microsoft EDGE на основе Chromium.</span><span class="sxs-lookup"><span data-stu-id="14e99-147">: set to `false`, which tells Selenium that you are driving the new Chromium-based Microsoft Edge browser.</span></span>
    2. `"webview2"`<span data-ttu-id="14e99-148">: строка, которая указывает Selenium, что вы управляете **WebView2**</span><span class="sxs-lookup"><span data-stu-id="14e99-148">: a string that tell Selenium you are driving **WebView2**</span></span>

2. <span data-ttu-id="14e99-149">Затем укажите `edgeOptions.BinaryLocation` путь к файлу исполняемого файла проекта WebView2, создайте строку с именем `msedgedriverDir` , которая содержит путь к файлу, на который установлен [драйвер Microsoft Edge](https://developer.microsoft.com/microsoft-edge/tools/webdriver/#downloads), и создайте строку, которая вызывается `msedgedriverExe` для хранения имени исполняемого файла драйвера Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="14e99-149">Next, set `edgeOptions.BinaryLocation` to the file path of your WebView2 project's executable, create a string called `msedgedriverDir` that provides the file path to where you installed [Microsoft Edge Driver](https://developer.microsoft.com/microsoft-edge/tools/webdriver/#downloads), and create a string called `msedgedriverExe` to store the name of the Microsoft Edge Driver executable.</span></span> <span data-ttu-id="14e99-150">По умолчанию вызывается исполняемый файл `"msedgedriver.exe"` .</span><span class="sxs-lookup"><span data-stu-id="14e99-150">By default, the executable is called `"msedgedriver.exe"`.</span></span> <span data-ttu-id="14e99-151">Используйте эти две строки для создания `EdgeDriverService` объекта, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="14e99-151">Use these two strings to construct the `EdgeDriverService` object as shown below.</span></span> <span data-ttu-id="14e99-152">Наконец, создайте `EdgeDriver` объект с помощью `EdgeDriverService` и `EdgeOptions` .</span><span class="sxs-lookup"><span data-stu-id="14e99-152">Finally, create the `EdgeDriver` object using `EdgeDriverService` and `EdgeOptions`.</span></span>

<span data-ttu-id="14e99-153">Вы можете скопировать и вставить следующий код под ним `edgeOptions` .</span><span class="sxs-lookup"><span data-stu-id="14e99-153">You can copy and paste the following code underneath `edgeOptions`.</span></span> <span data-ttu-id="14e99-154">Убедитесь, что указаны правильные пути к исполняемому файлу проекта и исполняемому файлу драйвера Microsoft EDGE на вашем компьютере.</span><span class="sxs-lookup"><span data-stu-id="14e99-154">Make sure to specify the correct file paths to your project's executable and the Microsoft Edge Driver's executable on your machine.</span></span>

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

3. <span data-ttu-id="14e99-155">Теперь **EdgeDriver** настроен для настройки **WebView2** в проекте.</span><span class="sxs-lookup"><span data-stu-id="14e99-155">Now, **EdgeDriver** is configured to drive the **WebView2** in your project.</span></span> <span data-ttu-id="14e99-156">Например, если вы используете **образец WebView2API**, вы можете **Перейти** <https://microsoft.com> по вызову ```e.Url = @"https://www.microsoft.com";``` .</span><span class="sxs-lookup"><span data-stu-id="14e99-156">For example, if you are using the **WebView2API Sample**, you can **Navigate** to <https://microsoft.com> by calling ```e.Url = @"https://www.microsoft.com";```.</span></span> <span data-ttu-id="14e99-157">Вы можете просматривать **Selenium** диск **WebView2** , настроив точку останова в этой строке и запуская проект.</span><span class="sxs-lookup"><span data-stu-id="14e99-157">You can watch **Selenium** drive **WebView2** by setting a breakpoint on this line and running the project.</span></span>

```csharp
    //The following will Navigate the WebView2API Sample from bing.com to microsoft.com
    e.Url = @"https://www.microsoft.com";

    //This exits the edge driver
    e.Quit();
}
```

![замещающий текст](../media/webdriver/microsoft.png)

<span data-ttu-id="14e99-159">Поздравляем!</span><span class="sxs-lookup"><span data-stu-id="14e99-159">Congratulations!</span></span> <span data-ttu-id="14e99-160">Вы успешно автоматизируи проект WebView2 и управляемый WebView2 с помощью драйвера Selenium и Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="14e99-160">You have successfully automated a WebView2 project and driven WebView2 using Selenium and Microsoft Edge Driver.</span></span>

## <span data-ttu-id="14e99-161">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="14e99-161">Next steps</span></span>

<span data-ttu-id="14e99-162">Дополнительные сведения:</span><span class="sxs-lookup"><span data-stu-id="14e99-162">To learn more:</span></span>

- <span data-ttu-id="14e99-163">Ознакомьтесь с [документацией по Selenium](https://www.selenium.dev/documentation/en/webdriver/) и ознакомьтесь с подробным обзором API-интерфейсов Selenium, которые можно использовать для работы с WebView2 или Microsoft EDGE (Chromium).</span><span class="sxs-lookup"><span data-stu-id="14e99-163">Check out [Selenium's documentation](https://www.selenium.dev/documentation/en/webdriver/) for a comprehensive look at the APIs Selenium has available for driving WebView2 or Microsoft Edge (Chromium)</span></span>
- <span data-ttu-id="14e99-164">Дополнительные сведения об элементе управления [WebView2](https://docs.microsoft.com/microsoft-edge/hosting/webview2) и его использовании при внедрении веб-содержимого в собственное приложение</span><span class="sxs-lookup"><span data-stu-id="14e99-164">Learn more about [WebView2](https://docs.microsoft.com/microsoft-edge/hosting/webview2) control and how to use it when embedding web content in your native app</span></span>
- <span data-ttu-id="14e99-165">Дополнительные сведения об автоматизации Microsoft EDGE (Chromium) можно найти в [документации по Microsoft Edge Driver](https://docs.microsoft.com/microsoft-edge/webdriver-chromium) .</span><span class="sxs-lookup"><span data-stu-id="14e99-165">Check out [documentation for Microsoft Edge Driver](https://docs.microsoft.com/microsoft-edge/webdriver-chromium) to learn more about automating Microsoft Edge (Chromium)</span></span>

## <span data-ttu-id="14e99-166">Знакомство с командой Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="14e99-166">Getting in touch with the Microsoft Edge WebView team</span></span>  

[!INCLUDE [contact WebView team note](../includes/contact-webview-team-note.md)]  
