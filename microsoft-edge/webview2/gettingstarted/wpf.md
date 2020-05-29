---
description: Размещение веб-содержимого в приложении WPF с помощью элемента управления Microsoft Edge WebView 2
title: Microsoft Edge WebView 2 для приложений WPF
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/12/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, WebView2, WebView, WebView, приложения WPF, WPF, EDGE, CoreWebView2, управление браузером, пограничный HTML, Приступая к работе, начало работы, .NET
ms.openlocfilehash: ebff559a940c54dcea18dec58170bdee1e030e9b
ms.sourcegitcommit: 799fe63d961a37ada455bb36ef3ef0d8076e70bb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2020
ms.locfileid: "10685696"
---
# <span data-ttu-id="5b5e8-104">Начало работы с WebView2 в WPF (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="5b5e8-104">Getting Started with WebView2 in WPF (Preview)</span></span>  

<span data-ttu-id="5b5e8-105">В этой статье приступите к созданию первого приложения WebView2 и ознакомьтесь с основными возможностями [WebView2 (Предварительная версия)](/microsoft-edge/hosting/webview2/index).</span><span class="sxs-lookup"><span data-stu-id="5b5e8-105">In this article, get started creating your first WebView2 app and learn about the main features of [WebView2 (preview)](/microsoft-edge/hosting/webview2/index).</span></span>  <span data-ttu-id="5b5e8-106">Дополнительные сведения об отдельных API можно найти в [справочнике API](../reference/dotnet/0-9-515-reference-webview2.md).</span><span class="sxs-lookup"><span data-stu-id="5b5e8-106">For more information on individual APIs, see [API reference](../reference/dotnet/0-9-515-reference-webview2.md).</span></span>  

## <span data-ttu-id="5b5e8-107">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="5b5e8-107">Prerequisites</span></span>  

<span data-ttu-id="5b5e8-108">Прежде чем продолжить, убедитесь в том, что вы установили следующий список предварительных требований:</span><span class="sxs-lookup"><span data-stu-id="5b5e8-108">Ensure you installed the following list of pre-requisites before proceeding:</span></span>  

* <span data-ttu-id="5b5e8-109">[Канал Канарские Microsoft EDGE (Chromium)](https://www.microsoftedgeinsider.com/download/) , установленный в Windows 10, Windows 8,1 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-109">[Microsoft Edge (Chromium) Canary channel](https://www.microsoftedgeinsider.com/download/) installed on Windows 10, Windows 8.1, or Windows 7.</span></span> 
* <span data-ttu-id="5b5e8-110">[Visual Studio](https://visualstudio.microsoft.com/) 2017 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-110">[Visual Studio](https://visualstudio.microsoft.com/) 2017 or later.</span></span>  

## <span data-ttu-id="5b5e8-111">Шаг 1: создание одного оконного приложения</span><span class="sxs-lookup"><span data-stu-id="5b5e8-111">Step 1 - Create a single window application</span></span>

<span data-ttu-id="5b5e8-112">Начните с базового классического проекта, содержащего одно главное окно.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-112">Start with a basic desktop project containing a single main window.</span></span>  

1. <span data-ttu-id="5b5e8-113">Откройте **Visual Studio.**</span><span class="sxs-lookup"><span data-stu-id="5b5e8-113">Open **Visual Studio.**</span></span>
2. <span data-ttu-id="5b5e8-114">Выберите приложение **WPF .NET Core App** или **WPF .NET Framework**и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-114">Choose **WPF .NET Core App** or **WPF .NET Framework App**, and then choose **Next**.</span></span>  

    :::row:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-wpfcore.png" alt-text="Ядро WPF":::
             <span data-ttu-id="5b5e8-116">Ядро WPF</span><span class="sxs-lookup"><span data-stu-id="5b5e8-116">WPF core</span></span> :::image-end:::
       :::column-end:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-wpffw.png" alt-text="Платформа WPF":::
             <span data-ttu-id="5b5e8-118">Платформа WPF</span><span class="sxs-lookup"><span data-stu-id="5b5e8-118">WPF Framework</span></span> :::image-end:::
       :::column-end:::
    :::row-end:::

3. <span data-ttu-id="5b5e8-119">Введите значения для **имени проекта** и его **местоположения**.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-119">Enter values for **Project name** and **Location**.</span></span>  <span data-ttu-id="5b5e8-120">Выберите .NET Framework 4.6.2 или более поздней версии или .NET Core 3,0 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-120">Select .NET Framework 4.6.2 or later, or .NET Core 3.0 or later.</span></span>  

:::row:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-createcore.png" alt-text="Создание основы":::
             <span data-ttu-id="5b5e8-122">Создание основы</span><span class="sxs-lookup"><span data-stu-id="5b5e8-122">Create core</span></span> :::image-end:::
       :::column-end:::
       :::column span="1":::
          :::image type="complex" source="./media/wpf-gettingstarted-createfw.png" alt-text="Создание платформы":::
             <span data-ttu-id="5b5e8-124">Создание платформы</span><span class="sxs-lookup"><span data-stu-id="5b5e8-124">Create Framework</span></span> :::image-end:::
       :::column-end:::
    :::row-end:::

4. <span data-ttu-id="5b5e8-125">Нажмите кнопку **создать** , чтобы создать проект.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-125">Choose **Create** to create your project.</span></span>  

## <span data-ttu-id="5b5e8-126">Шаг 2. Установка WebView2 SDK</span><span class="sxs-lookup"><span data-stu-id="5b5e8-126">Step 2 - Install WebView2 SDK</span></span>  

<span data-ttu-id="5b5e8-127">Затем добавьте в проект пакет SDK для WebView2.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-127">Next add the WebView2 SDK to the project.</span></span>  <span data-ttu-id="5b5e8-128">Для предварительного просмотра установите пакет SDK WebView2 с помощью NuGet.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-128">For the preview, install the WebView2 SDK using Nuget.</span></span>  

1. <span data-ttu-id="5b5e8-129">Откройте контекстное меню проекта \ (щелкните правой кнопкой мыши \) и выберите пункт **Управление пакетами NuGet..**..</span><span class="sxs-lookup"><span data-stu-id="5b5e8-129">Open the context menu on the project \(right-click\), and choose **Manage NuGet Packages...**.</span></span>  

    :::image type="complex" source="./media/wpf-gettingstarted-mngnuget.png" alt-text="NuGet":::
       <span data-ttu-id="5b5e8-131">NuGet</span><span class="sxs-lookup"><span data-stu-id="5b5e8-131">Nuget</span></span> :::image-end:::

2. <span data-ttu-id="5b5e8-132">Введите `Microsoft.Web.WebView2` строку поиска.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-132">Enter `Microsoft.Web.WebView2` in the search bar.</span></span>  <span data-ttu-id="5b5e8-133">В результатах поиска выберите **Microsoft. Web. WebView2** .</span><span class="sxs-lookup"><span data-stu-id="5b5e8-133">Choose **Microsoft.Web.WebView2** from the search results.</span></span>  <span data-ttu-id="5b5e8-134">Установите **предварительную**версию пакета и нажмите кнопку **установить**.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-134">Set the package version to **pre-release**, and then choose **Install**.</span></span>  

     ![NuGet](./media/installnuget.PNG)

<span data-ttu-id="5b5e8-136">Все готово для начала разработки приложений с помощью API WebView2.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-136">You are all set to start developing applications using the WebView2 API.</span></span>  <span data-ttu-id="5b5e8-137">Нажмите кнопку `F5` , чтобы создать и запустить проект.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-137">Press `F5` to build and run the project.</span></span>  <span data-ttu-id="5b5e8-138">Запущенный проект отобразит пустое окно.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-138">The running project displays an empty window.</span></span>  

:::image type="complex" source="./media/wpf-gettingstarted-blank.png" alt-text="Пустое приложение":::
   <span data-ttu-id="5b5e8-140">Пустое приложение</span><span class="sxs-lookup"><span data-stu-id="5b5e8-140">Empty app</span></span>
:::image-end:::

## <span data-ttu-id="5b5e8-141">Шаг 3: создание отдельного WebView в файле MainWindow. XAML</span><span class="sxs-lookup"><span data-stu-id="5b5e8-141">Step 3 - Create a single WebView in MainWindow.xaml</span></span>  

<span data-ttu-id="5b5e8-142">Далее добавьте WebView в приложение.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-142">Next add a WebView to your application.</span></span>  

1. <span data-ttu-id="5b5e8-143">Open (открыть) `MainWindow.xaml` .</span><span class="sxs-lookup"><span data-stu-id="5b5e8-143">Open `MainWindow.xaml`.</span></span>  <span data-ttu-id="5b5e8-144">Добавьте пространство имен XAML WebView2 с помощью вставки в тег следующей строки `<Window/>` .</span><span class="sxs-lookup"><span data-stu-id="5b5e8-144">Add the WebView2 XAML namespace by inserting the following line inside the `<Window/>` tag.</span></span>  

    ```xml
    xmlns:wv2="clr-namespace:Microsoft.Web.WebView2.Wpf;assembly=Microsoft.Web.WebView2.Wpf"
    ```  

    <span data-ttu-id="5b5e8-145">Убедитесь, что код `MainWindow.xaml` выглядит так, как показано в следующем фрагменте кода.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-145">Confirm that the code in `MainWindow.xaml` looks like the following code snippet.</span></span>  

    ```xml
    <Window x:Class="WPF_Getting_Started.MainWindow"
            xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
            xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
            xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
            xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
            xmlns:local="clr-namespace:{YOUR PROJECT NAME}"
            xmlns:wv2="clr-namespace:Microsoft.Web.WebView2.Wpf;assembly=Microsoft.Web.WebView2.Wpf"
            mc:Ignorable="d"
            Title="MainWindow"
            Height="450"
            Width="800"
        />
        <Grid>

                </Grid>
    </Window>
    ```  

2. <span data-ttu-id="5b5e8-146">Добавьте элемент управления WebView2, заменив `<Grid>` теги, с помощью следующего фрагмента кода.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-146">Add the WebView2 control by replacing the `<Grid>` tags, with the following code snippet.</span></span>  <span data-ttu-id="5b5e8-147">`Source`Свойство задает начальный URI, отображаемый в элементе управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-147">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span>  

    ```xml  
    <DockPanel>
        <wv2:WebView2 Name="webView"
                      Source="https://www.microsoft.com"
        />
    </DockPanel>
    ```  

3. <span data-ttu-id="5b5e8-148">Нажмите `F5` , чтобы создать и запустить проект.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-148">Press `F5` to build and run your project.</span></span>  <span data-ttu-id="5b5e8-149">Убедитесь, что ваш элемент управления WebView2 отображается [https://www.microsoft.com](https://www.microsoft.com) .</span><span class="sxs-lookup"><span data-stu-id="5b5e8-149">Confirm that your WebView2 control displays [https://www.microsoft.com](https://www.microsoft.com).</span></span>  

    :::image type="complex" source="./media/wpf-gettingstarted-microsoft.png" alt-text="Microsoft.com":::
       <span data-ttu-id="5b5e8-151">Microsoft.com</span><span class="sxs-lookup"><span data-stu-id="5b5e8-151">Microsoft.com</span></span> :::image-end:::

## <span data-ttu-id="5b5e8-152">Шаг 4 — Навигация</span><span class="sxs-lookup"><span data-stu-id="5b5e8-152">Step 4 - Navigation</span></span>  

<span data-ttu-id="5b5e8-153">Добавьте в приложение адресную строку, чтобы пользователи могли изменить URL-адрес, который отображается в элементе управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-153">Add the ability to allow users to change the URL that the WebView2 control displays by adding an address bar to the app.</span></span>

1. <span data-ttu-id="5b5e8-154">В файле **MainWindow. XAML**Добавьте адресную строку, скопировав и вставив следующий фрагмент кода в DockPanel, который включает WebView.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-154">In **MainWindow.xaml**, add an address bar by copying and pasting the following code snippet inside the DockPanel that contains the WebView.</span></span>  

```xml
<DockPanel DockPanel.Dock="Top">
    <Button x:Name="ButtonGo"
            DockPanel.Dock="Right"
            Click="ButtonGo_Click"
            Content="Go"
    />
    <TextBox Name="addressBar"/>
</DockPanel>
```  

<span data-ttu-id="5b5e8-155">Убедитесь, что `DockPanel` раздел `MainWindow.xaml` выглядит так, как показано в следующем фрагменте кода.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-155">Confirm that the `DockPanel` section of `MainWindow.xaml` looks like the following code snippet.</span></span>  

```xml
<DockPanel>
    <DockPanel DockPanel.Dock="Top">
        <Button x:Name="ButtonGo" DockPanel.Dock="Right" Click="ButtonGo_Click" Content="Go"/>
        <TextBox Name = "addressBar"/>
    </DockPanel>
    <wv2:WebView2 Name = "webView"
                  Source = "https://www.microsoft.com"
    />
</DockPanel>
```  

2. <span data-ttu-id="5b5e8-156">Откройте `MainWindow.xaml.cs` в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-156">Open `MainWindow.xaml.cs` in Visual Studio.</span></span>  <span data-ttu-id="5b5e8-157">Добавьте `CoreWebView2` пространство имен, вставив следующий фрагмент кода вверху `MainWindow.xaml.cs` .</span><span class="sxs-lookup"><span data-stu-id="5b5e8-157">Add the `CoreWebView2` namespace by inserting the following code snippet at the top of `MainWindow.xaml.cs`.</span></span>  

    ```csharp
    using Microsoft.Web.WebView2.Core;
    ```

3. <span data-ttu-id="5b5e8-158">В **MainWindow.XAML.CS**Скопируйте приведенный ниже фрагмент кода, чтобы создать `ButtonGo_Click` метод, который будет перемещаться по WebView на URL-адрес, введенный в адресной строке.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-158">In **MainWindow.xaml.cs**, copy the following code snippet to create the `ButtonGo_Click` method, which navigates the WebView to the URL entered in the address bar.</span></span>  

    ```csharp
    private void ButtonGo_Click(object sender, RoutedEventArgs e)
    {
        if (webView != null && webView.CoreWebView2 != null)
        {
            webView.CoreWebView2.Navigate(addressBar.Text);
        }
    }
    ```  

<span data-ttu-id="5b5e8-159">Нажмите `F5` , чтобы создать и запустить проект.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-159">Press `F5` to build and run your project.</span></span>  <span data-ttu-id="5b5e8-160">Введите новый URL-адрес в адресной строке и нажмите кнопку **Перейти**.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-160">Enter a new URL in the address bar, and click **Go**.</span></span>  <span data-ttu-id="5b5e8-161">Например, введите `https://www.bing.com` .</span><span class="sxs-lookup"><span data-stu-id="5b5e8-161">For example, enter `https://www.bing.com`.</span></span>  <span data-ttu-id="5b5e8-162">Убедитесь, что элемент управления WebView2 переходит по URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-162">Confirm that the WebView2 control navigates to the URL.</span></span>  

> [!NOTE]
> <span data-ttu-id="5b5e8-163">Убедитесь в том, что в адресной строке введен полный URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-163">Make sure a complete URL is entered in the address bar.</span></span> <span data-ttu-id="5b5e8-164">`ArgumentException`Если URL-адрес не начинается с `http://` или</span><span class="sxs-lookup"><span data-stu-id="5b5e8-164">An `ArgumentException` is thrown if the URL does not start with `http://` or</span></span> `https://`

:::image type="complex" source="./media/wpf-gettingstarted-bing.png" alt-text="Bing":::
   <span data-ttu-id="5b5e8-166">Bing</span><span class="sxs-lookup"><span data-stu-id="5b5e8-166">Bing</span></span>
:::image-end:::

## <span data-ttu-id="5b5e8-167">Шаг 5 — события навигации</span><span class="sxs-lookup"><span data-stu-id="5b5e8-167">Step 5 - Navigation events</span></span>  

<span data-ttu-id="5b5e8-168">Приложение, содержащее элементы управления WebView2, прослушивает следующие события, возникающие при переходе на веб-страницы с помощью элемента управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-168">The application that hosts WebView2 controls listens to the following events that are raised by the WebView2 control during navigation to web pages.</span></span>  

* `NavigationStarting`  
* `SourceChanged`  
* `ContentLoading`  
* `HistoryChanged`  
* `NavigationCompleted`  

<span data-ttu-id="5b5e8-169">Дополнительные сведения можно найти в разделе [события навигации](../reference/win32/0-9-488/icorewebview2.md#navigation-events).</span><span class="sxs-lookup"><span data-stu-id="5b5e8-169">For more information, see [Navigation Events](../reference/win32/0-9-488/icorewebview2.md#navigation-events).</span></span>  

:::image type="complex" source="../media/navigation-events.png" alt-text="События навигации":::
   <span data-ttu-id="5b5e8-171">События навигации</span><span class="sxs-lookup"><span data-stu-id="5b5e8-171">Navigation events</span></span>
:::image-end:::

<span data-ttu-id="5b5e8-172">При возникновении ошибки возникают следующие события, которые могут зависеть от навигации на страницу ошибки.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-172">When an error occurs, the following events are raised and may depend on navigation to an error page.</span></span>  

* `SourceChanged`  
* `ContentLoading`  
* `HistoryChanged`  

<span data-ttu-id="5b5e8-173">При перенаправлении HTTP есть несколько `NavigationStarting` событий.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-173">When there is an HTTP redirect, there are multiple `NavigationStarting` events.</span></span>  

<span data-ttu-id="5b5e8-174">Чтобы продемонстрировать использование этих событий, начните с регистрации обработчика для `NavigationStarting` этого отменяет все запросы, которые не используют HTTPS.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-174">To demonstrate how to use these events, start by registering a handler for `NavigationStarting` that cancels any requests that do not use HTTPS.</span></span>  

<span data-ttu-id="5b5e8-175">`MainWindow.xaml.cs`Измените конструктор, как показано ниже, и добавьте `EnsureHttps` функцию.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-175">In `MainWindow.xaml.cs`, modify the constructor as shown below and add the `EnsureHttps` function.</span></span>  

```csharp
public MainWindow()
{
    InitializeComponent();
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

<span data-ttu-id="5b5e8-176">В конструкторе EnsureHttps регистрируется в качестве обработчика событий для `NavigationStarting` события в элементе управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-176">In the constructor, EnsureHttps is registered as the event handler on the `NavigationStarting` event on the WebView2 control.</span></span>  

<span data-ttu-id="5b5e8-177">Нажмите `F5` , чтобы создать и запустить проект.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-177">Press `F5` to build and run your project.</span></span> <span data-ttu-id="5b5e8-178">Убедитесь, что при переходе на веб-сайт HTTP WebView не **меняется**.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-178">Confirm that when navigating to an HTTP site, the WebView **remains unchanged**.</span></span> <span data-ttu-id="5b5e8-179">Однако WebView будет переходить на сайты HTTPS.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-179">However, the WebView will navigate to HTTPS sites.</span></span>

## <span data-ttu-id="5b5e8-180">Шаг 6-Создание сценариев</span><span class="sxs-lookup"><span data-stu-id="5b5e8-180">Step 6 - Scripting</span></span>  

<span data-ttu-id="5b5e8-181">Вы можете использовать ведущие приложения для вставки кода JavaScript в элементы управления WebView2 во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-181">You may use host applications to inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="5b5e8-182">Вставленный JavaScript применяется ко всем новым документам верхнего уровня и дочерним кадрам до тех пор, пока не будет удален JavaScript.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-182">The injected JavaScript applies to all new top level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="5b5e8-183">Вставленный JavaScript запускается после создания глобального объекта, а также перед запуском любого другого сценария, включенного в документ HTML.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-183">The injected JavaScript is run after creation of the global object, and before any other script included in the HTML document is run.</span></span>  

<span data-ttu-id="5b5e8-184">Вы можете использовать сценарии для оповещения пользователя о переходе на сайт, не поддерживающий HTTPS.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-184">You can use scripting to alert the user when navigating to a non-HTTPS site.</span></span>  <span data-ttu-id="5b5e8-185">Измените `EnsureHttps` функцию таким образом, чтобы она была вставлена в веб-содержимое в виде сценария с помощью метода [ExecuteScriptAsync](../reference/wpf/0-9-515/microsoft-web-webview2-wpf-webview2.md#executescriptasync) .</span><span class="sxs-lookup"><span data-stu-id="5b5e8-185">Modify the `EnsureHttps` function so that it injects script into the web content using the [ExecuteScriptAsync](../reference/wpf/0-9-515/microsoft-web-webview2-wpf-webview2.md#executescriptasync) method.</span></span>  

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

<span data-ttu-id="5b5e8-186">Нажмите `F5` , чтобы создать и запустить проект.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-186">Press `F5` to build and run your project.</span></span>  <span data-ttu-id="5b5e8-187">Убедитесь, что приложение отображает оповещение при переходе на сайт, который не использует HTTPS.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-187">Confirm that the application displays an alert when you navigate to a site that does not use HTTPS.</span></span>  

:::image type="complex" source="./media/wpf-gettingstarted-https.png" alt-text="HTTPS":::
   <span data-ttu-id="5b5e8-189">HTTPS</span><span class="sxs-lookup"><span data-stu-id="5b5e8-189">HTTPS</span></span>
:::image-end:::

## <span data-ttu-id="5b5e8-190">Шаг 7: связь между узлом и веб-контентом</span><span class="sxs-lookup"><span data-stu-id="5b5e8-190">Step 7 - Communication between host and web content</span></span>  

<span data-ttu-id="5b5e8-191">Основное приложение и веб-содержимое могут взаимодействовать друг с другом с помощью `postMessage` следующих параметров:</span><span class="sxs-lookup"><span data-stu-id="5b5e8-191">The host and web content may communicate with each other using `postMessage` as follows:</span></span>  

* <span data-ttu-id="5b5e8-192">Веб-содержимое в элементе управления WebView2 может публиковать сообщение на узле с помощью `window.chrome.webview.postMessage` .</span><span class="sxs-lookup"><span data-stu-id="5b5e8-192">Web content in a WebView2 control may post a message to the host using `window.chrome.webview.postMessage`.</span></span>  <span data-ttu-id="5b5e8-193">Узел обрабатывает сообщение, используя все, что зарегистрировано `WebMessageReceived` на узле.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-193">The host handles the message using any registered `WebMessageReceived` on the host.</span></span>  
* <span data-ttu-id="5b5e8-194">Размещает сообщения на веб-сайте элемента управления WebView2 с помощью `CoreWebView2.PostWebMessageAsString` или `CoreWebView2.PostWebMessageAsJSON` .</span><span class="sxs-lookup"><span data-stu-id="5b5e8-194">Hosts post messages to web content in a WebView2 control using `CoreWebView2.PostWebMessageAsString` or `CoreWebView2.PostWebMessageAsJSON`.</span></span>  <span data-ttu-id="5b5e8-195">Эти сообщения перехватываются обработчиками, добавленными в `window.chrome.webview.addEventListener` .</span><span class="sxs-lookup"><span data-stu-id="5b5e8-195">These messages are caught by handlers added to `window.chrome.webview.addEventListener`.</span></span>  

<span data-ttu-id="5b5e8-196">Этот механизм связи позволяет веб-контенту передавать сообщения ведущему узлу с помощью собственных возможностей.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-196">This communication mechanism allows web content to pass messages to the host using native capabilities.</span></span>  

<span data-ttu-id="5b5e8-197">Когда элемент управления WebView2 переходит по URL-адресу, в проекте отображается URL-адрес в адресной строке и оповещает пользователя об URL-адресе, который отображается в элементе управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-197">In your project, when the WebView2 control navigates to a URL, it displays the URL in the address bar and alerts the user of the URL displayed in the WebView2 control.</span></span>  

1. <span data-ttu-id="5b5e8-198">В **MainWindow.XAML.CS**обновите конструктор и создайте `InitializeAsync` функцию, как показано в следующем фрагменте кода.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-198">In **MainWindow.xaml.cs**, update your constructor and create an `InitializeAsync` function as shown in the following code snippet.</span></span>  <span data-ttu-id="5b5e8-199">`InitializeAsync`Функция ожидает [EnsureCoreWebView2Async](../reference/wpf/0-9-515/microsoft-web-webview2-wpf-webview2.md#ensurecorewebview2async) , так как инициализация `CoreWebView2` является асинхронной.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-199">The `InitializeAsync` function awaits [EnsureCoreWebView2Async](../reference/wpf/0-9-515/microsoft-web-webview2-wpf-webview2.md#ensurecorewebview2async) because the initialization of `CoreWebView2` is asynchronous.</span></span>  

    ```csharp
    public MainWindow()
    {
        InitializeComponent();
        webView.NavigationStarting += EnsureHttps;
        InitializeAsync();
    }

    async void InitializeAsync()
    {
        await webView.EnsureCoreWebView2Async(null);
    }
    ```  

2. <span data-ttu-id="5b5e8-200">После инициализации **CoreWebView2** Зарегистрируйте обработчик событий, на который нужно ответить `WebMessageReceived` .</span><span class="sxs-lookup"><span data-stu-id="5b5e8-200">After **CoreWebView2** is initialized, register an event handler to respond to `WebMessageReceived`.</span></span>  <span data-ttu-id="5b5e8-201">В **MainWindow.XAML.CS** Update `InitializeAsync` и Add `UpdateAddressBar` с помощью следующего фрагмента кода.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-201">In **MainWindow.xaml.cs** update `InitializeAsync` and add `UpdateAddressBar` using the following code snippet.</span></span>  

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

3. <span data-ttu-id="5b5e8-202">Чтобы WebView отсылать и отвечать на веб-сообщение, после `CoreWebView2` инициализации, узел:</span><span class="sxs-lookup"><span data-stu-id="5b5e8-202">In order for the WebView to send and respond to the web message, after `CoreWebView2` is initialized, the host:</span></span>  

    1. <span data-ttu-id="5b5e8-203">Встраивает в веб-содержимое сценарий, регистрирующий обработчик для печати сообщения с узла.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-203">Injects a script to the web content that registers a handler to print message from the host.</span></span>  
    2. <span data-ttu-id="5b5e8-204">Вставляет сценарий в веб-содержимое, которое отправляет URL-адрес узлу.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-204">Injects a script to the web content that posts the URL to the host.</span></span>  

<span data-ttu-id="5b5e8-205">В `MainWindow.xaml.cs` . Обновите `InitializeAsync` следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5b5e8-205">In `MainWindow.xaml.cs`, update `InitializeAsync` as follows:</span></span>  

```csharp
async void InitializeAsync()
{
    await webView.EnsureCoreWebView2Async(null);
    webView.CoreWebView2.WebMessageReceived += UpdateAddressBar;

    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.postMessage(window.document.URL);");
    await webView.CoreWebView2.AddScriptToExecuteOnDocumentCreatedAsync("window.chrome.webview.addEventListener(\'message\', event => alert(event.data));");
}
```  

<span data-ttu-id="5b5e8-206">Нажмите `F5` для сборки и запуска приложения.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-206">Press `F5` to build and run the app.</span></span>  <span data-ttu-id="5b5e8-207">Теперь в адресной строке отображается URI-адрес в WebView и при успешном переходе на новый URI WebView предупреждает пользователя о URI, показанном в WebView.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-207">Now the address bar displays the URI in the WebView and when you successfully navigate to a new URI, the WebView alerts the user of the URI displayed in the WebView.</span></span>  

:::image type="complex" source="./media/wpf-gettingstarted-searchbar.png" alt-text="addressBar":::
   <span data-ttu-id="5b5e8-209">addressBar</span><span class="sxs-lookup"><span data-stu-id="5b5e8-209">addressBar</span></span>
:::image-end:::

<span data-ttu-id="5b5e8-210">Поздравляем! вы создали первое приложение WebView2!</span><span class="sxs-lookup"><span data-stu-id="5b5e8-210">Congratulations, you built your first WebView2 app!</span></span>  

## <span data-ttu-id="5b5e8-211">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="5b5e8-211">Next Steps</span></span>  

* <span data-ttu-id="5b5e8-212">Провлеките [WebView2Samplesный репозиторий](https://github.com/MicrosoftEdge/WebView2Samples) с подробным примером возможностей WebView2's</span><span class="sxs-lookup"><span data-stu-id="5b5e8-212">Checkout the [WebView2Samples repo](https://github.com/MicrosoftEdge/WebView2Samples) for a comprehensive example of WebView2's capabilities</span></span>
* <span data-ttu-id="5b5e8-213">Дополнительные сведения об интерфейсах API для извлечения [справочных](../reference/wpf/0-9-515/microsoft-web-webview2-wpf-webview2) данных</span><span class="sxs-lookup"><span data-stu-id="5b5e8-213">Checkout [API reference](../reference/wpf/0-9-515/microsoft-web-webview2-wpf-webview2) for more detailed information about our APIs</span></span>
* <span data-ttu-id="5b5e8-214">Извлечение списка [ресурсов WebView2](../index.md#next-steps) для получения дополнительных сведений о WebView2</span><span class="sxs-lookup"><span data-stu-id="5b5e8-214">Checkout a list of [WebView2 Resources](../index.md#next-steps) to learn more about WebView2</span></span>

## <span data-ttu-id="5b5e8-215">Знакомство с командой Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="5b5e8-215">Getting in touch with the Microsoft Edge WebView team</span></span>  

<span data-ttu-id="5b5e8-216">Помогите вам создать более широкие возможности WebView2, отправив свой отзыв.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-216">Help build a richer WebView2 experience by sharing your feedback!</span></span>  <span data-ttu-id="5b5e8-217">Посетите центр [отзывов и предложений](https://aka.ms/webviewfeedback) Microsoft Edge WebView, чтобы отправить запросы функций или отчеты об ошибках или найти известные проблемы.</span><span class="sxs-lookup"><span data-stu-id="5b5e8-217">Visit the Microsoft Edge WebView [feedback repo](https://aka.ms/webviewfeedback) to submit feature requests or bug reports or search for known issues.</span></span>  
