---
description: Размещение веб-содержимого в приложении Windows Forms с помощью элемента управления Microsoft Edge WebView 2
title: Microsoft Edge WebView 2 для приложений Windows Forms
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, WebView2, WebView, WebView, приложения WinForms, WinForms, EDGE, CoreWebView2, браузер, край HTML, Приступая к работе, Приступая к работе, .NET, Windows Forms
ms.openlocfilehash: 6c53b66dd9f849384f24c2ae879f28231a25f481
ms.sourcegitcommit: 799fe63d961a37ada455bb36ef3ef0d8076e70bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2020
ms.locfileid: "10685689"
---
# <span data-ttu-id="1f109-104">Начало работы с WebView2 в приложениях для Windows Forms (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="1f109-104">Getting Started with WebView2 in Windows Forms apps (Preview)</span></span>  

<span data-ttu-id="1f109-105">В этой статье приступите к созданию первого приложения WebView2 и ознакомьтесь с основными возможностями [WebView2 (Предварительная версия)](/microsoft-edge/hosting/webview2/index).</span><span class="sxs-lookup"><span data-stu-id="1f109-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2 (preview)](/microsoft-edge/hosting/webview2/index).</span></span>  <span data-ttu-id="1f109-106">Дополнительные сведения об отдельных API можно найти в [справочнике API](../reference/dotnet/0-9-515-reference-webview2.md).</span><span class="sxs-lookup"><span data-stu-id="1f109-106">For more information on individual APIs, see [API reference](../reference/dotnet/0-9-515-reference-webview2.md).</span></span>  

## <span data-ttu-id="1f109-107">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="1f109-107">Prerequisites</span></span>  

<span data-ttu-id="1f109-108">Прежде чем продолжить, убедитесь в том, что вы установили следующий список предварительных требований:</span><span class="sxs-lookup"><span data-stu-id="1f109-108">Ensure you installed the following list of pre-requisites before proceeding:</span></span>  

* <span data-ttu-id="1f109-109">[Канал Канарские Microsoft EDGE (Chromium)](https://www.microsoftedgeinsider.com/download/) , установленный в Windows 10, Windows 8,1 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="1f109-109">[Microsoft Edge (Chromium) Canary channel](https://www.microsoftedgeinsider.com/download/) installed on Windows 10, Windows 8.1, or Windows 7.</span></span> 
* <span data-ttu-id="1f109-110">[Visual Studio](https://visualstudio.microsoft.com/) 2017 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="1f109-110">[Visual Studio](https://visualstudio.microsoft.com/) 2017 or later.</span></span>

> [!NOTE]
> <span data-ttu-id="1f109-111">Если вы разрабатываете **Microsoft Forms .NET Core 3,0 или .NET 5**, скачайте [Visual Studio (Предварительная версия)](https://visualstudio.microsoft.com/vs/preview/)</span><span class="sxs-lookup"><span data-stu-id="1f109-111">If developing with **Windows Forms .NET Core 3.0 or .NET 5**, download [Visual Studio (Preview)](https://visualstudio.microsoft.com/vs/preview/)</span></span>

## <span data-ttu-id="1f109-112">Шаг 1: создание одного оконного приложения</span><span class="sxs-lookup"><span data-stu-id="1f109-112">Step 1 - Create a single window application</span></span>

<span data-ttu-id="1f109-113">Начните с базового классического проекта, содержащего одно главное окно.</span><span class="sxs-lookup"><span data-stu-id="1f109-113">Start with a basic desktop project containing a single main window.</span></span>  

1. <span data-ttu-id="1f109-114">Откройте **Visual Studio.**</span><span class="sxs-lookup"><span data-stu-id="1f109-114">Open **Visual Studio.**</span></span>

2. <span data-ttu-id="1f109-115">Выберите **приложение Windows Forms .NET Framework** или **основное приложение Windows Forms .NET**и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="1f109-115">Choose **Windows Forms .NET Framework App** or **Windows Forms .NET Core App**, and then choose **Next**.</span></span>

    ![newproject](./media/winforms-newproject.png)

3. <span data-ttu-id="1f109-117">Введите значения для **имени проекта** и его **местоположения**.</span><span class="sxs-lookup"><span data-stu-id="1f109-117">Enter values for **Project name** and **Location**.</span></span>  <span data-ttu-id="1f109-118">Выберите **.NET Framework 4.6.2** или более поздней версии или **.NET Core 3,0** или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="1f109-118">Select **.NET Framework 4.6.2** or later, or **.NET Core 3.0** or later.</span></span>  

    ![startproject](./media/winforms-startproj.png)

4. <span data-ttu-id="1f109-120">Нажмите кнопку **создать** , чтобы создать проект.</span><span class="sxs-lookup"><span data-stu-id="1f109-120">Choose **Create** to create your project.</span></span>

## <span data-ttu-id="1f109-121">Шаг 2. Установка WebView2 SDK</span><span class="sxs-lookup"><span data-stu-id="1f109-121">Step 2 - Install WebView2 SDK</span></span>

<span data-ttu-id="1f109-122">Затем добавьте в проект пакет SDK для WebView2.</span><span class="sxs-lookup"><span data-stu-id="1f109-122">Next add the WebView2 SDK to the project.</span></span>  <span data-ttu-id="1f109-123">Для предварительного просмотра установите пакет SDK WebView2 с помощью NuGet.</span><span class="sxs-lookup"><span data-stu-id="1f109-123">For the preview, install the WebView2 SDK using Nuget.</span></span>  

1. <span data-ttu-id="1f109-124">Откройте контекстное меню проекта \ (щелкните правой кнопкой мыши \) и выберите пункт **Управление пакетами NuGet..**..</span><span class="sxs-lookup"><span data-stu-id="1f109-124">Open the context menu on the project \(right-click\), and choose **Manage NuGet Packages...**.</span></span>  

    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="NuGet":::
       <span data-ttu-id="1f109-126">NuGet</span><span class="sxs-lookup"><span data-stu-id="1f109-126">Nuget</span></span> :::image-end:::

2. <span data-ttu-id="1f109-127">Введите `Microsoft.Web.WebView2` строку поиска.</span><span class="sxs-lookup"><span data-stu-id="1f109-127">Enter `Microsoft.Web.WebView2` in the search bar.</span></span>  <span data-ttu-id="1f109-128">В результатах поиска выберите **Microsoft. Web. WebView2** .</span><span class="sxs-lookup"><span data-stu-id="1f109-128">Choose **Microsoft.Web.WebView2** from the search results.</span></span>  <span data-ttu-id="1f109-129">Установите **предварительную**версию пакета и нажмите кнопку **установить**.</span><span class="sxs-lookup"><span data-stu-id="1f109-129">Set the package version to **pre-release**, and then choose **Install**.</span></span>  

    ![NuGet](./media/installnuget.png)

<span data-ttu-id="1f109-131">Все готово для начала разработки приложений с помощью API WebView2.</span><span class="sxs-lookup"><span data-stu-id="1f109-131">You are all set to start developing applications using the WebView2 API.</span></span>  <span data-ttu-id="1f109-132">Выберите `F5` для сборки и запуска проекта.</span><span class="sxs-lookup"><span data-stu-id="1f109-132">Select `F5` to build and run the project.</span></span>  <span data-ttu-id="1f109-133">Запущенный проект отобразит пустое окно.</span><span class="sxs-lookup"><span data-stu-id="1f109-133">The running project displays an empty window.</span></span>  

![emptyApp](./media/winforms-emptyApp.png)

## <span data-ttu-id="1f109-135">Шаг 3: создание единого WebView</span><span class="sxs-lookup"><span data-stu-id="1f109-135">Step 3 - Create a single WebView</span></span>  

<span data-ttu-id="1f109-136">Далее добавьте WebView в приложение.</span><span class="sxs-lookup"><span data-stu-id="1f109-136">Next add a WebView to your application.</span></span>  

1. <span data-ttu-id="1f109-137">Откройте **конструктор Windows Forms**.</span><span class="sxs-lookup"><span data-stu-id="1f109-137">Open the **Windows Forms Designer**.</span></span>  
2. <span data-ttu-id="1f109-138">Найдите **WebView2** на **панели элементов**.</span><span class="sxs-lookup"><span data-stu-id="1f109-138">Search for **WebView2** in the **Toolbox**.</span></span> <span data-ttu-id="1f109-139">Перетаскивание элемента управления **WebView2** в приложение Windows Forms</span><span class="sxs-lookup"><span data-stu-id="1f109-139">Drag and drop the **WebView2** control into the Windows Forms App</span></span>

    ![элементов](./media/winforms-toolbox.png)

3. <span data-ttu-id="1f109-141">Измените `Name` свойство на `webView` .</span><span class="sxs-lookup"><span data-stu-id="1f109-141">Change the `Name` property to `webView`.</span></span>

    ![элементов](./media/winforms-properties.png)

4. <span data-ttu-id="1f109-143">`Source`Свойство задает начальный URI, отображаемый в элементе управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="1f109-143">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span> <span data-ttu-id="1f109-144">Установите для свойства Source значение</span><span class="sxs-lookup"><span data-stu-id="1f109-144">Set the Source property to</span></span> <https://www.microsoft.com>

    ![элементов](./media/winforms-source.png)

<span data-ttu-id="1f109-146">Выберите `F5` , чтобы выполнить сборку и запустить проект.</span><span class="sxs-lookup"><span data-stu-id="1f109-146">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="1f109-147">Убедитесь, что ваш элемент управления WebView2 отображается [https://www.microsoft.com](https://www.microsoft.com) .</span><span class="sxs-lookup"><span data-stu-id="1f109-147">Confirm that your WebView2 control displays [https://www.microsoft.com](https://www.microsoft.com).</span></span>

![hellowebview](./media/winforms-hellowebview.png)

> [!NOTE]
> <span data-ttu-id="1f109-149">Если вы работаете с монитором с высоким разрешением, может потребоваться [настроить поддержку высокого разрешения для приложения Windows Forms](https://docs.microsoft.com/dotnet/framework/winforms/high-dpi-support-in-windows-forms#configuring-your-windows-forms-app-for-high-dpi-support).</span><span class="sxs-lookup"><span data-stu-id="1f109-149">If you are working on a high DPI monitor, you may have to [configure your Windows Forms app for high DPI support](https://docs.microsoft.com/dotnet/framework/winforms/high-dpi-support-in-windows-forms#configuring-your-windows-forms-app-for-high-dpi-support).</span></span>

## <span data-ttu-id="1f109-150">Шаг 4: обработка событий изменения размера окна</span><span class="sxs-lookup"><span data-stu-id="1f109-150">Step 4 - Handle Window Resize Events</span></span>

<span data-ttu-id="1f109-151">Добавьте еще несколько элементов управления в формы Windows Forms с панели элементов, а затем обработайте события изменения размера окна соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="1f109-151">Add a few more controls to your Windows Forms from the toolbox, and then handle window resize events appropriately.</span></span>

1. <span data-ttu-id="1f109-152">Открытие **панели элементов** в **конструкторе Windows Forms**</span><span class="sxs-lookup"><span data-stu-id="1f109-152">In the **Windows Forms Designer** open the **Toolbox**</span></span>
2. <span data-ttu-id="1f109-153">Перетащите **текстовое поле** в приложение Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="1f109-153">Drag and Drop a **TextBox** into the Windows Forms App.</span></span> <span data-ttu-id="1f109-154">Назовите **поле TextBox** `addressBar` на **вкладке Свойства**.</span><span class="sxs-lookup"><span data-stu-id="1f109-154">Name the **TextBox** `addressBar` in the **Properties Tab**.</span></span>
3. <span data-ttu-id="1f109-155">Перетащите **кнопку** в приложение Windows Forms.</span><span class="sxs-lookup"><span data-stu-id="1f109-155">Drag and Drop a **Button** into the Windows Forms App.</span></span> <span data-ttu-id="1f109-156">Измените текст **кнопки** `Go!` и назовите **кнопку** на `goButton` **вкладке Свойства**.</span><span class="sxs-lookup"><span data-stu-id="1f109-156">Change the text in the **Button** to `Go!` and name the **Button** `goButton` in the **Properties Tab**.</span></span>

<span data-ttu-id="1f109-157">Приложение должно выглядеть так, как показано в конструкторе:</span><span class="sxs-lookup"><span data-stu-id="1f109-157">The app should look like the following in the designer:</span></span>

![Проектировщик](./media/winforms-designer.png)

4. <span data-ttu-id="1f109-159">В **Form1.CS** определите, `Form_Resize` нужно ли сохранять элементы управления при изменении размера окна приложения.</span><span class="sxs-lookup"><span data-stu-id="1f109-159">In **Form1.cs** define `Form_Resize` to keep the controls in place when the App Window is resized.</span></span>

```csharp
public Form1()
{
    InitializeComponent();
    this.Resize += new System.EventHandler(this.Form_Resize);
}

private void Form_Resize(object sender, EventArgs e)
{
    webView.Size = this.ClientSize - new System.Drawing.Size(webView.Location);
    goButton.Left = this.ClientSize.Width - goButton.Width;
    addressBar.Width = goButton.Left - addressBar.Left;
}
```

<span data-ttu-id="1f109-160">Выберите `F5` , чтобы выполнить сборку и запустить проект.</span><span class="sxs-lookup"><span data-stu-id="1f109-160">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="1f109-161">Убедитесь, что приложение отображается примерно так, как показано на следующем снимке экрана.</span><span class="sxs-lookup"><span data-stu-id="1f109-161">Confirm that the app displays similar to the following screenshot.</span></span>

![приложение](./media/winforms-app.png)

## <span data-ttu-id="1f109-163">Шаг 5 — Навигация</span><span class="sxs-lookup"><span data-stu-id="1f109-163">Step 5 - Navigation</span></span>

<span data-ttu-id="1f109-164">Добавьте в приложение адресную строку, чтобы пользователи могли изменить URL-адрес, который отображается в элементе управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="1f109-164">Add the ability to allow users to change the URL that the WebView2 control displays by adding an address bar to the app.</span></span>

1. <span data-ttu-id="1f109-165">В поле `Form1.cs` Добавить `CoreWebView2` пространство имен вставьте следующий фрагмент кода вверху `Form1.cs` .</span><span class="sxs-lookup"><span data-stu-id="1f109-165">In `Form1.cs` add the `CoreWebView2` namespace by inserting the following code snippet at the top of `Form1.cs`.</span></span>  

    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```

2. <span data-ttu-id="1f109-166">В **конструкторе Windows Forms**дважды щелкните `Go!` кнопку, чтобы создать `goButton_Click` метод `Form1.cs` .</span><span class="sxs-lookup"><span data-stu-id="1f109-166">In the **Windows Forms Designer**, double-click on the `Go!` button to create the `goButton_Click` method in `Form1.cs`.</span></span> <span data-ttu-id="1f109-167">Скопируйте и вставьте следующий фрагмент в функцию.</span><span class="sxs-lookup"><span data-stu-id="1f109-167">Copy and paste the following snippet inside the function.</span></span> <span data-ttu-id="1f109-168">Теперь `goButton_Click` функция переходит по WebView на URL-адрес, введенный в адресной строке.</span><span class="sxs-lookup"><span data-stu-id="1f109-168">Now, the `goButton_Click` function navigates the WebView to the URL entered in the address bar.</span></span>

    ```csharp
    private void goButton_Click(object sender, EventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  

<span data-ttu-id="1f109-169">Выберите `F5` , чтобы выполнить сборку и запустить проект.</span><span class="sxs-lookup"><span data-stu-id="1f109-169">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="1f109-170">Введите новый URL-адрес в адресной строке и нажмите кнопку **Перейти**.</span><span class="sxs-lookup"><span data-stu-id="1f109-170">Enter a new URL in the address bar, and click **Go**.</span></span>  <span data-ttu-id="1f109-171">Например, введите `https://www.bing.com` .</span><span class="sxs-lookup"><span data-stu-id="1f109-171">For example, enter `https://www.bing.com`.</span></span>  <span data-ttu-id="1f109-172">Убедитесь, что элемент управления WebView2 переходит по URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="1f109-172">Confirm that the WebView2 control navigates to the URL.</span></span>  

> [!NOTE]
> <span data-ttu-id="1f109-173">Убедитесь в том, что в адресной строке введен полный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="1f109-173">Ensure a complete URL is entered in the address bar.</span></span> <span data-ttu-id="1f109-174">`ArgumentException`Если URL-адрес не начинается с `http://` или</span><span class="sxs-lookup"><span data-stu-id="1f109-174">An `ArgumentException` is thrown if the URL does not start with `http://` or</span></span> `https://`

![bing](./media/winforms-bing.png)

## <span data-ttu-id="1f109-176">Шаг 6 — события навигации</span><span class="sxs-lookup"><span data-stu-id="1f109-176">Step 6 - Navigation events</span></span>  

<span data-ttu-id="1f109-177">Приложение, содержащее элементы управления WebView2, прослушивает следующие события, возникающие при переходе на веб-страницы с помощью элемента управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="1f109-177">The application that hosts WebView2 controls listens to the following events that are raised by the WebView2 control during navigation to web pages.</span></span>  

* `NavigationStarting`  
* `SourceChanged`  
* `ContentLoading`  
* `HistoryChanged`  
* `NavigationCompleted`  

<span data-ttu-id="1f109-178">Дополнительные сведения можно найти в разделе [события навигации](../reference/win32/0-9-488/icorewebview2.md#navigation-events).</span><span class="sxs-lookup"><span data-stu-id="1f109-178">For more information, see [Navigation Events](../reference/win32/0-9-488/icorewebview2.md#navigation-events).</span></span>  

:::image type="complex" source="../media/navigation-events.png" alt-text="События навигации":::
   <span data-ttu-id="1f109-180">События навигации</span><span class="sxs-lookup"><span data-stu-id="1f109-180">Navigation events</span></span>
:::image-end:::

<span data-ttu-id="1f109-181">При возникновении ошибки возникают следующие события, которые могут зависеть от навигации на страницу ошибки.</span><span class="sxs-lookup"><span data-stu-id="1f109-181">When an error occurs, the following events are raised and may depend on navigation to an error page.</span></span>  

* `SourceChanged`  
* `ContentLoading`  
* `HistoryChanged`  

<span data-ttu-id="1f109-182">При перенаправлении HTTP есть несколько `NavigationStarting` событий.</span><span class="sxs-lookup"><span data-stu-id="1f109-182">When there is an HTTP redirect, there are multiple `NavigationStarting` events.</span></span>  

<span data-ttu-id="1f109-183">Чтобы продемонстрировать использование этих событий, начните с регистрации обработчика для `NavigationStarting` этого отменяет все запросы, которые не используют HTTPS.</span><span class="sxs-lookup"><span data-stu-id="1f109-183">To demonstrate how to use these events, start by registering a handler for `NavigationStarting` that cancels any requests that do not use HTTPS.</span></span>  

<span data-ttu-id="1f109-184">`Form1.cs`Измените конструктор, как показано ниже, и добавьте `EnsureHttps` функцию.</span><span class="sxs-lookup"><span data-stu-id="1f109-184">In `Form1.cs`, modify the constructor as shown below and add the `EnsureHttps` function.</span></span>  

```csharp
public Form1()
{
    InitializeComponent();
    this.Resize += new System.EventHandler(this.Form_Resize);

    webView.NavigationStarting += EnsureHttps;
}

void EnsureHttps(object sender, CoreWebView2NavigationStartingEventArgs args)
{
    String uri = args.Uri;
    if (!uri.StartsWith("https://"))
    {
        args.Cancel = true;
    }
}
```

<span data-ttu-id="1f109-185">В конструкторе EnsureHttps регистрируется в качестве обработчика событий для `NavigationStarting` события в элементе управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="1f109-185">In the constructor, EnsureHttps is registered as the event handler on the `NavigationStarting` event on the WebView2 control.</span></span>  

<span data-ttu-id="1f109-186">Выберите `F5` , чтобы выполнить сборку и запустить проект.</span><span class="sxs-lookup"><span data-stu-id="1f109-186">Select `F5` to build and run your project.</span></span> <span data-ttu-id="1f109-187">Убедитесь, что при переходе на веб-сайт HTTP WebView не меняется.</span><span class="sxs-lookup"><span data-stu-id="1f109-187">Confirm that when navigating to an HTTP site, the WebView remains unchanged.</span></span> <span data-ttu-id="1f109-188">Однако WebView будет переходить на сайты HTTPS.</span><span class="sxs-lookup"><span data-stu-id="1f109-188">However, the WebView will navigate to HTTPS sites.</span></span>

## <span data-ttu-id="1f109-189">Шаг 7: создание сценариев</span><span class="sxs-lookup"><span data-stu-id="1f109-189">Step 7 - Scripting</span></span>  

<span data-ttu-id="1f109-190">Вы можете использовать ведущие приложения для вставки кода JavaScript в элементы управления WebView2 во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="1f109-190">You may use host applications to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="1f109-191">Вставленный JavaScript применяется ко всем новым документам верхнего уровня и дочерним кадрам до тех пор, пока не будет удален JavaScript.</span><span class="sxs-lookup"><span data-stu-id="1f109-191">The injected JavaScript applies to all new top level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="1f109-192">Вставленный JavaScript запускается после создания глобального объекта, а также перед запуском любого другого сценария, включенного в документ HTML.</span><span class="sxs-lookup"><span data-stu-id="1f109-192">The injected JavaScript is run after creation of the global object, and before any other script included in the HTML document is run.</span></span>  

<span data-ttu-id="1f109-193">Вы можете использовать сценарии для оповещения пользователя о переходе на сайт, не поддерживающий HTTPS.</span><span class="sxs-lookup"><span data-stu-id="1f109-193">You can use scripting to alert the user when navigating to a non-HTTPS site.</span></span>  <span data-ttu-id="1f109-194">Измените `EnsureHttps` функцию таким образом, чтобы она была вставлена в веб-содержимое в виде сценария с помощью метода [ExecuteScriptAsync]() .</span><span class="sxs-lookup"><span data-stu-id="1f109-194">Modify the `EnsureHttps` function so that it injects script into the web content using the [ExecuteScriptAsync]() method.</span></span>  

```csharp
void EnsureHttps(object sender, CoreWebView2NavigationStartingEventArgs args)
{
    String uri = args.Uri;
    if (!uri.StartsWith("https://"))
    {
        webView.CoreWebView2.ExecuteScriptAsync($"alert('{uri} is not safe, try an https link')");
        args.Cancel = true;
    }
}
```  

<span data-ttu-id="1f109-195">Выберите `F5` , чтобы выполнить сборку и запустить проект.</span><span class="sxs-lookup"><span data-stu-id="1f109-195">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="1f109-196">Убедитесь, что приложение отображает оповещение при переходе на сайт, который не использует HTTPS.</span><span class="sxs-lookup"><span data-stu-id="1f109-196">Confirm that the application displays an alert when you navigate to a site that does not use HTTPS.</span></span>  

![https](./media/winforms-https.png)

## <span data-ttu-id="1f109-198">Шаг 8-связь между узлом и веб-контентом</span><span class="sxs-lookup"><span data-stu-id="1f109-198">Step 8 - Communication between host and web content</span></span>  

<span data-ttu-id="1f109-199">Основное приложение и веб-содержимое могут взаимодействовать друг с другом с помощью `postMessage` следующих параметров:</span><span class="sxs-lookup"><span data-stu-id="1f109-199">The host and web content may communicate with each other using `postMessage` as follows:</span></span>  

* <span data-ttu-id="1f109-200">Веб-содержимое в элементе управления WebView2 может публиковать сообщение на узле с помощью `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="1f109-200">Web content in a WebView2 control may post a message to the host using `window.chrome.webview.postMessage`.</span></span>  <span data-ttu-id="1f109-201">Узел обрабатывает сообщение, используя все, что зарегистрировано `WebMessageReceived` на узле.</span><span class="sxs-lookup"><span data-stu-id="1f109-201">The host handles the message using any registered `WebMessageReceived` on the host.</span></span>  
* <span data-ttu-id="1f109-202">Размещает сообщения на веб-сайте элемента управления WebView2 с помощью `CoreWebView2.PostWebMessageAsString` или `CoreWebView2.PostWebMessageAsJSON` .</span><span class="sxs-lookup"><span data-stu-id="1f109-202">Hosts post messages to web content in a WebView2 control using `CoreWebView2.PostWebMessageAsString` or `CoreWebView2.PostWebMessageAsJSON`.</span></span>  <span data-ttu-id="1f109-203">Эти сообщения перехватываются обработчиками, добавленными в `window.chrome.webview.addEventListener` .</span><span class="sxs-lookup"><span data-stu-id="1f109-203">These messages are caught by handlers added to `window.chrome.webview.addEventListener`.</span></span>  

<span data-ttu-id="1f109-204">Этот механизм связи позволяет веб-контенту передавать сообщения ведущему узлу с помощью собственных возможностей.</span><span class="sxs-lookup"><span data-stu-id="1f109-204">This communication mechanism allows web content to pass messages to the host using native capabilities.</span></span>  

<span data-ttu-id="1f109-205">Когда элемент управления WebView2 переходит по URL-адресу, в проекте отображается URL-адрес в адресной строке и оповещает пользователя об URL-адресе, который отображается в элементе управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="1f109-205">In your project, when the WebView2 control navigates to a URL, it displays the URL in the address bar and alerts the user of the URL displayed in the WebView2 control.</span></span>  

1. <span data-ttu-id="1f109-206">В **Form1.CS**обновите конструктор и создайте `InitializeAsync` функцию, как показано в следующем фрагменте кода.</span><span class="sxs-lookup"><span data-stu-id="1f109-206">In **Form1.cs**, update your constructor and create an `InitializeAsync` function as shown in the following code snippet.</span></span>  <span data-ttu-id="1f109-207">`InitializeAsync`Функция ожидает [EnsureCoreWebView2Async]() , так как инициализация `CoreWebView2` является асинхронной.</span><span class="sxs-lookup"><span data-stu-id="1f109-207">The `InitializeAsync` function awaits [EnsureCoreWebView2Async]() because the initialization of `CoreWebView2` is asynchronous.</span></span>  

    ```csharp
    public Form1()
    {
        InitializeComponent();
        this.Resize += new System.EventHandler(this.Form_Resize);
        webView.NavigationStarting += EnsureHttps;
        InitializeAsync();
    }

    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
    }
    ```  

2. <span data-ttu-id="1f109-208">После инициализации **CoreWebView2** Зарегистрируйте обработчик событий, на который нужно ответить `WebMessageReceived` .</span><span class="sxs-lookup"><span data-stu-id="1f109-208">After **CoreWebView2** is initialized, register an event handler to respond to `WebMessageReceived`.</span></span>  <span data-ttu-id="1f109-209">В разделе `Form1.cs` Update `InitializeAsync` и Add `UpdateAddressBar` (добавить с помощью следующего фрагмента кода).</span><span class="sxs-lookup"><span data-stu-id="1f109-209">In `Form1.cs` update `InitializeAsync` and add `UpdateAddressBar` using the following code snippet.</span></span>  

    ```csharp
    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
        webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;
    }

    void UpdateAddressBar(object sender, CoreWebView2WebMessageReceivedEventArgs args)
    {
        String uri = args.TryGetWebMessageAsString();
        addressBar.Text = uri;
        webView.CoreWebView2.PostWebMessageAsString(uri);
    }
    ```  

3. <span data-ttu-id="1f109-210">Чтобы WebView отсылать и отвечать на веб-сообщение, после его `CoreWebView2` инициализации ведущее приложение вставляет сценарий в веб-содержимое в:</span><span class="sxs-lookup"><span data-stu-id="1f109-210">In order for the WebView to send and respond to the web message, after `CoreWebView2` is initialized, the host injects a script in the web content to:</span></span>  

    1. <span data-ttu-id="1f109-211">Отправьте URL-адрес узлу с помощью `postMessage` .</span><span class="sxs-lookup"><span data-stu-id="1f109-211">Send the URL to the host using `postMessage`.</span></span>
    2. <span data-ttu-id="1f109-212">Зарегистрируйте обработчик событий, чтобы напечатать сообщение, отправленное с узла.</span><span class="sxs-lookup"><span data-stu-id="1f109-212">Register an event handler to print a message sent from the host.</span></span>  

<span data-ttu-id="1f109-213">В `Form1.cs` Обновите, `InitializeAsync` как показано в следующем фрагменте кода.</span><span class="sxs-lookup"><span data-stu-id="1f109-213">In `Form1.cs`, update `InitializeAsync` as shown in the following code snippet.</span></span>  

```csharp
async void InitializeAsync()
{
    await webView.EnsureCoreWebView2Async(null);
    webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;

    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
}
```  

<span data-ttu-id="1f109-214">Выберите `F5` , чтобы выполнить сборку и запустить приложение.</span><span class="sxs-lookup"><span data-stu-id="1f109-214">Select `F5` to build and run the app.</span></span>  <span data-ttu-id="1f109-215">Убедитесь в том, что в адресной строке отображается URL-адрес сайта, отображаемого в WebView.</span><span class="sxs-lookup"><span data-stu-id="1f109-215">Confirm that the address bar displays the URL of the site displayed in the WebView.</span></span> <span data-ttu-id="1f109-216">Кроме того, при успешном переходе к новому URL-адресу WebView предупреждает пользователя об URL-адресе, показанном в WebView.</span><span class="sxs-lookup"><span data-stu-id="1f109-216">Also, when you successfully navigate to a new URL, the WebView alerts the user of the URL displayed in the WebView.</span></span>  

![finalapp](./media/winforms-finalapp.png)

<span data-ttu-id="1f109-218">Поздравляем! вы создали первое приложение WebView2!</span><span class="sxs-lookup"><span data-stu-id="1f109-218">Congratulations, you built your first WebView2 app!</span></span>  

## <span data-ttu-id="1f109-219">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="1f109-219">Next Steps</span></span> 

* <span data-ttu-id="1f109-220">Провлеките [WebView2Samplesный репозиторий](https://github.com/MicrosoftEdge/WebView2Samples) с подробным примером возможностей WebView2's</span><span class="sxs-lookup"><span data-stu-id="1f109-220">Checkout the [WebView2Samples repo](https://github.com/MicrosoftEdge/WebView2Samples) for a comprehensive example of WebView2's capabilities</span></span>
* <span data-ttu-id="1f109-221">Дополнительные сведения об интерфейсах API для извлечения [справочных](../reference/winforms/0-9-515/microsoft-web-webview2-winforms-webview2.md) данных</span><span class="sxs-lookup"><span data-stu-id="1f109-221">Checkout [API reference](../reference/winforms/0-9-515/microsoft-web-webview2-winforms-webview2.md) for more detailed information about our APIs</span></span>
* <span data-ttu-id="1f109-222">Извлечение списка [ресурсов WebView2](../index.md#next-steps) для получения дополнительных сведений о WebView2</span><span class="sxs-lookup"><span data-stu-id="1f109-222">Checkout a list of [WebView2 Resources](../index.md#next-steps) to learn more about WebView2</span></span>


## <span data-ttu-id="1f109-223">Знакомство с командой Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="1f109-223">Getting in touch with the Microsoft Edge WebView team</span></span>  

<span data-ttu-id="1f109-224">Помогите вам создать более широкие возможности WebView2, отправив свой отзыв.</span><span class="sxs-lookup"><span data-stu-id="1f109-224">Help build a richer WebView2 experience by sharing your feedback!</span></span>  <span data-ttu-id="1f109-225">Посетите центр [отзывов и предложений](https://aka.ms/webviewfeedback) Microsoft Edge WebView, чтобы отправить запросы функций или отчеты об ошибках или найти известные проблемы.</span><span class="sxs-lookup"><span data-stu-id="1f109-225">Visit the Microsoft Edge WebView [feedback repo](https://aka.ms/webviewfeedback) to submit feature requests or bug reports or search for known issues.</span></span>  
