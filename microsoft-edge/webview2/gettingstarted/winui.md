---
description: Размещение веб-содержимого в приложении WinUI с помощью элемента управления Microsoft Edge WebView 2
title: Microsoft Edge WebView2 для приложений WinUI
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/23/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: webview
keywords: WebView2, WebView2, WebView, WebView, winui, winui, EDGE, CoreWebView2, Browser Control, EDGE HTML, Приступая к работе, Приступая к работе, .NET
ms.openlocfilehash: 9960a4411e69f0232ae2d202a61a9beb01c0a631
ms.sourcegitcommit: 553957c101f83681b363103cb6af56bf20173f23
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/24/2020
ms.locfileid: "10895513"
---
# <span data-ttu-id="e5347-104">Начало работы с WebView2 в WinUI3 (Предварительная версия)</span><span class="sxs-lookup"><span data-stu-id="e5347-104">Getting started with WebView2 in WinUI3 (Preview)</span></span>  

<span data-ttu-id="e5347-105">В этой статье приступите к созданию первого приложения WebView2 с помощью WinUI3 и ознакомьтесь с основными возможностями [знакомства с Microsoft Edge WebView2 (Предварительная версия)][Webview2Index].</span><span class="sxs-lookup"><span data-stu-id="e5347-105">In this article, get started creating your first WebView2 app with WinUI3 and learn about the main features of [Introduction to Microsoft Edge WebView2 (Preview)][Webview2Index].</span></span>  <span data-ttu-id="e5347-106">Дополнительные сведения об отдельных API можно найти в [справочнике API][GithubMicrosoftUiXamlSpecsWebview2].</span><span class="sxs-lookup"><span data-stu-id="e5347-106">For more information on individual APIs, see [API reference][GithubMicrosoftUiXamlSpecsWebview2].</span></span>  

## <span data-ttu-id="e5347-107">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="e5347-107">Prerequisites</span></span>  

<span data-ttu-id="e5347-108">Перед переходом к следующей статье убедитесь, что вы установили приведенный ниже список предварительных условий.</span><span class="sxs-lookup"><span data-stu-id="e5347-108">Ensure you install the following list of pre-requisites before proceeding with the following article.</span></span>  

*   <span data-ttu-id="e5347-109">Windows 10 версии 1803 \ (сборка 17134 \) или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="e5347-109">Windows 10 version 1803 \(build 17134\) or later.</span></span>  <span data-ttu-id="e5347-110">Дополнительные сведения можно найти в [центре обновления Windows: вопросы и ответы][MicrosoftSupport12373].</span><span class="sxs-lookup"><span data-stu-id="e5347-110">For more information, see [Windows Update: FAQ][MicrosoftSupport12373].</span></span>  
*   <span data-ttu-id="e5347-111">[Microsoft EDGE (Chromium) Канарские Channel][MicrosoftedgeinsiderDownload] в Windows 10, Windows 8,1 или Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e5347-111">[Microsoft Edge (Chromium) Canary channel][MicrosoftedgeinsiderDownload] on Windows 10, Windows 8.1, or Windows 7.</span></span>  
*   <span data-ttu-id="e5347-112">Visual Studio 2019, версия 16,7 Preview 1.</span><span class="sxs-lookup"><span data-stu-id="e5347-112">Visual Studio 2019, version 16.7 Preview 1.</span></span>  <span data-ttu-id="e5347-113">Дополнительные сведения можно найти в разделе [Библиотека пользовательского интерфейса Windows версии 3 (июль 2020][WindowsAppsWinui3ConfigureYourDevEnvironment]г.).</span><span class="sxs-lookup"><span data-stu-id="e5347-113">For more information, see [Windows UI Library 3 Preview 2 (July 2020)][WindowsAppsWinui3ConfigureYourDevEnvironment].</span></span>  
*   <span data-ttu-id="e5347-114">Версии [x64][WindowsDotnetcliBlobCoreSdk50100Preview4202681X86] и [x86][WindowsDotnetcliBlobCoreSdk50100Preview4202681X64] версии .NET 5 Preview 4.</span><span class="sxs-lookup"><span data-stu-id="e5347-114">Both the [x64][WindowsDotnetcliBlobCoreSdk50100Preview4202681X86] and [x86][WindowsDotnetcliBlobCoreSdk50100Preview4202681X64] versions of .NET 5 Preview 4.</span></span>  
*   <span data-ttu-id="e5347-115">Расширение [шаблонов проектов WinUI 3][VisualstudioMarketplaceWinUiprojecttemplates] для Visual Studio 2019.</span><span class="sxs-lookup"><span data-stu-id="e5347-115">[WinUI 3 Project Templates][VisualstudioMarketplaceWinUiprojecttemplates] extension for Visual Studio 2019.</span></span>  
<span data-ttu-id="e5347-116">Убедитесь, что вы [включите режим разработчика][WindowsUwpGetStartedEnableYourDeviceForDevelopment] , чтобы убедиться в том, что у вас есть доступ ко всем функциям Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="e5347-116">Ensure you [Enable Developer Mode][WindowsUwpGetStartedEnableYourDeviceForDevelopment] to ensure you have access to all Visual Studio features.</span></span>  

## <span data-ttu-id="e5347-117">Шаг 1: Создание проекта</span><span class="sxs-lookup"><span data-stu-id="e5347-117">Step 1 - Create Project</span></span>  

<span data-ttu-id="e5347-118">Начните с базового классического проекта, содержащего одно главное окно.</span><span class="sxs-lookup"><span data-stu-id="e5347-118">Start with a basic desktop project containing a single main window.</span></span>  

1.  <span data-ttu-id="e5347-119">В Visual Studio выберите **создать новый проект**.</span><span class="sxs-lookup"><span data-stu-id="e5347-119">In Visual Studio, select **Create a new project**.</span></span>  
1.  <span data-ttu-id="e5347-120">В раскрывающемся списке Проект выберите **C#**, **Windows**и **WinUI** соответственно.</span><span class="sxs-lookup"><span data-stu-id="e5347-120">In the project drop-down, select **C#**, **Windows**, and **WinUI** respectively.</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-selections.png" alt-text="Диалоговое окно создания проекта Visual Studio для WinUI" lightbox="./media/winui-gettingstarted-selections.png":::
       <span data-ttu-id="e5347-122">Диалоговое окно создания проекта Visual Studio для WinUI</span><span class="sxs-lookup"><span data-stu-id="e5347-122">Visual studio project creation dialog for WinUI</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="e5347-123">Выберите **пустое приложение, упакованное (WinUI на рабочем столе)**, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="e5347-123">Choose **Blank App, Packaged (WinUI in Desktop)**, and then choose **Next**.</span></span>  
1.  <span data-ttu-id="e5347-124">Введите имя проекта, выберите нужные параметры и нажмите кнопку **создать**.</span><span class="sxs-lookup"><span data-stu-id="e5347-124">Enter a project name, choose other options as needed, and then select **Create**.</span></span>  
1.  <span data-ttu-id="e5347-125">В **новом проекте универсальной платформы Windows**выберите указанные ниже значения, а затем нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="e5347-125">In **New Universal Windows Platform Project**, select the following values, and then choose **OK**:</span></span>  
    *   <span data-ttu-id="e5347-126">Целевая версия: **Windows 10, версия 1903 (сборка 18362)** или более поздняя.</span><span class="sxs-lookup"><span data-stu-id="e5347-126">Target version: **Windows 10, version 1903 (build 18362)** or later.</span></span>  
    *   <span data-ttu-id="e5347-127">Минимальная версия: **Windows 10, версия 1803 (сборка 17134)**.</span><span class="sxs-lookup"><span data-stu-id="e5347-127">Minimum version: **Windows 10, version 1803 (build 17134)**.</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-projecttype.png" alt-text="Диалоговое окно создания проекта универсальной платформы Windows с выбранными значениями для целевой версии и минимальной версии." lightbox="./media/winui-gettingstarted-projecttype.png":::
       <span data-ttu-id="e5347-129">Диалоговое окно создания проекта универсальной платформы Windows с выбранными значениями для целевой версии и минимальной версии.</span><span class="sxs-lookup"><span data-stu-id="e5347-129">The New Universal Windows Platform Project dialog with selected values for Target version and Minimum version.</span></span>
    :::image-end:::  
    
1.  <span data-ttu-id="e5347-130">В обозревателе решений создаются два проекта.</span><span class="sxs-lookup"><span data-stu-id="e5347-130">In the Solution Explorer, two projects are generated.</span></span>  
    *   <span data-ttu-id="e5347-131">**Название проекта (классическое приложение)**.</span><span class="sxs-lookup"><span data-stu-id="e5347-131">**Your project name(Desktop)**.</span></span> <span data-ttu-id="e5347-132">Этот проект включает код для вашего приложения.</span><span class="sxs-lookup"><span data-stu-id="e5347-132">This project contains the code for your app.</span></span>  <span data-ttu-id="e5347-133">**App.XAML.CS** определяет `Application` класс, представляющий экземпляр приложения.</span><span class="sxs-lookup"><span data-stu-id="e5347-133">**App.xaml.cs** defines an`Application`class that represents your app instance.</span></span> <span data-ttu-id="e5347-134">**MainWindow.XAML.CS** определяет `MainWindow` класс, представляющий главное окно, которое отображается в экземпляре приложения.</span><span class="sxs-lookup"><span data-stu-id="e5347-134">**MainWindow.xaml.cs** defines a`MainWindow`class that represents the main window displayed by your app instance.</span></span>  <span data-ttu-id="e5347-135">Эти классы являются производными от типов в `Microsoft.UI.Xaml` пространстве имен WinUI.</span><span class="sxs-lookup"><span data-stu-id="e5347-135">These classes derive from types in the`Microsoft.UI.Xaml`namespace of WinUI.</span></span>  
    
    *   <span data-ttu-id="e5347-136">**Имя проекта (пакет)**.</span><span class="sxs-lookup"><span data-stu-id="e5347-136">**Your project name(Package)**.</span></span>  <span data-ttu-id="e5347-137">Этот проект — aWindows пакетов приложений Projectthat настроен для сборки приложения в MSIXный пакет для развертывания.</span><span class="sxs-lookup"><span data-stu-id="e5347-137">This project is aWindows Application Packaging Projectthat is configured to build the app into an MSIX package for deployment.</span></span>  <span data-ttu-id="e5347-138">Проект содержит thepackage manifestfor вашего приложения, и по умолчанию он является запускаемым проектом для вашего решения.</span><span class="sxs-lookup"><span data-stu-id="e5347-138">The project contains thepackage manifestfor your app, and it is the startup project for your solution by default.</span></span> <span data-ttu-id="e5347-139">Дополнительные сведения можно найти [в разделе Настройка классического приложения для MSIX упаковки в Visual Studio][WindowsMsixDesktopToUwpPackagingDotNet] и [Справочник по схеме манифеста пакета для Windows 10][UwpSchemasAppxpackageUapmanifestRoot].</span><span class="sxs-lookup"><span data-stu-id="e5347-139">For more information, see [Set up your desktop application for MSIX packaging in Visual Studio][WindowsMsixDesktopToUwpPackagingDotNet] and [Package manifest schema reference for Windows 10][UwpSchemasAppxpackageUapmanifestRoot].</span></span>
    
1.  <span data-ttu-id="e5347-140">В обозревателе решений откройте окно **MainWindow. XAML** , чтобы отобразить код.</span><span class="sxs-lookup"><span data-stu-id="e5347-140">In the Solution Explorer, open **MainWindow.xaml** to display the code.</span></span>  <span data-ttu-id="e5347-141">Выберите `F5` , чтобы запустить проект и отобразить окно с кнопкой.</span><span class="sxs-lookup"><span data-stu-id="e5347-141">Select `F5` to run your project and show a window with a button.</span></span>  
    
## <span data-ttu-id="e5347-142">Шаг 2: Добавление элемента управления WebView2 в проект</span><span class="sxs-lookup"><span data-stu-id="e5347-142">Step 2 - Add a WebView2 control to your project</span></span>  

<span data-ttu-id="e5347-143">Затем добавьте элемент управления WebView2 в проект.</span><span class="sxs-lookup"><span data-stu-id="e5347-143">Next add a WebView2 control to your project.</span></span>  

1.  <span data-ttu-id="e5347-144">Open (открыть) `MainWindow.xaml` .</span><span class="sxs-lookup"><span data-stu-id="e5347-144">Open `MainWindow.xaml`.</span></span>  <span data-ttu-id="e5347-145">Добавьте пространство имен XAML WebView2 с помощью вставки в тег следующей строки `<Window/>` .</span><span class="sxs-lookup"><span data-stu-id="e5347-145">Add the WebView2 XAML namespace by inserting the following line inside the `<Window/>` tag.</span></span>  
    
    ```xml
    xmlns:controls="using:Microsoft.UI.Xaml.Controls"
    ```  
    
    <span data-ttu-id="e5347-146">Убедитесь, что ваш код `MainWindow.xaml` похож на следующий фрагмент кода.</span><span class="sxs-lookup"><span data-stu-id="e5347-146">Confirm that your code in `MainWindow.xaml` is similar to the following code snippet.</span></span>  
    
    ```xml
    <Window
          x:Class="WinUI_Sample.MainWindow"
          xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
          xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
          xmlns:local="using:WinUI_Sample"
          xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
          xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
          mc:Ignorable="d"
          xmlns:controls="using:Microsoft.UI.Xaml.Controls"
          >
        
          <StackPanel Orientation="Horizontal" HorizontalAlignment="Center" VerticalAlignment="Center">
            <Button x:Name="myButton" Click="myButton_Click">Click Me</Button>
          </StackPanel>
    
    </Window>
    ```  
    
1.  <span data-ttu-id="e5347-147">Чтобы добавить элемент управления WebView2, замените `<StackPanel>` теги на следующий фрагмент кода.</span><span class="sxs-lookup"><span data-stu-id="e5347-147">To add the WebView2 control, replace the `<StackPanel>` tags with the following code snippet.</span></span>  <span data-ttu-id="e5347-148">`Source`Свойство задает начальный URI, отображаемый в элементе управления WebView2.</span><span class="sxs-lookup"><span data-stu-id="e5347-148">The `Source` property sets the initial URI displayed in the WebView2 control.</span></span>  
    
    ```xml  
    <Grid>

        <Grid.RowDefinitions>
            <RowDefinition Height="Auto" />
            <RowDefinition Height="*" />
        </Grid.RowDefinitions>
        <Grid.ColumnDefinitions>
            <ColumnDefinition Width="*" />
            <ColumnDefinition Width="Auto" />
        </Grid.ColumnDefinitions>
        
        <controls:WebView2 x:Name="MyWebView"  Grid.Row="1" Grid.ColumnSpan="2" 
            Source="https://www.microsoft.com" HorizontalAlignment="Stretch" VerticalAlignment="Stretch" />
    
    </Grid>
    ```  
    
1.  <span data-ttu-id="e5347-149">Откройте `MainWindow.xaml.cs` следующую строку и закомментируйте ее.</span><span class="sxs-lookup"><span data-stu-id="e5347-149">Open `MainWindow.xaml.cs` and comment out the following line.</span></span>
    
    ```xml
        // myButton.Content = "Clicked";     
    ```  
    
1.  <span data-ttu-id="e5347-150">Выберите `F5` , чтобы выполнить сборку и запустить проект.</span><span class="sxs-lookup"><span data-stu-id="e5347-150">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="e5347-151">Убедитесь, что ваш элемент управления WebView2 отображается [https://www.microsoft.com][|::ref1::|Main] .</span><span class="sxs-lookup"><span data-stu-id="e5347-151">Confirm that your WebView2 control displays [https://www.microsoft.com][|::ref1::|Main].</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-part3.png" alt-text="Элемент управления WebView2, на котором отображается сайт microsoft.com" lightbox="./media/winui-gettingstarted-part3.png":::
       <span data-ttu-id="e5347-153">Элемент управления WebView2, на котором отображается сайт microsoft.com.</span><span class="sxs-lookup"><span data-stu-id="e5347-153">A WebView2 control displaying the microsoft.com site.</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="e5347-154">Шаг 3: Добавление элементов управления навигацией</span><span class="sxs-lookup"><span data-stu-id="e5347-154">Step 3 - Add navigation controls</span></span>  

<span data-ttu-id="e5347-155">Разрешите пользователям управлять веб-страницей, которая отображается в элементе управления WebView2, добавив адресную строку в приложение.</span><span class="sxs-lookup"><span data-stu-id="e5347-155">Allow users to control the web page that is displayed in your WebView2 control by adding an address bar to your app.</span></span> 

1.  <span data-ttu-id="e5347-156">В файле **MainWindow. XAML**скопируйте и вставьте следующий фрагмент кода внутри `Grid` элемента, содержащего `WebView2` элемент.</span><span class="sxs-lookup"><span data-stu-id="e5347-156">In **MainWindow.xaml**, copy and paste the following code snippet inside the `Grid` element that contains the `WebView2` element.</span></span>  
    
    ```xml
        <TextBox Name="addressBar" Grid.Column="0"/>
        <Button x:Name="myButton" Grid.Column="1" Click="myButton_Click">Go</Button>
    ```  
    
    <span data-ttu-id="e5347-157">Убедитесь, что `Grid` элемент `MainWindow.xaml` похож на следующий фрагмент кода.</span><span class="sxs-lookup"><span data-stu-id="e5347-157">Confirm that your `Grid` element of `MainWindow.xaml` is similar to the following code snippet.</span></span>  
    
    ```xml
    <Grid>
    
        <Grid.RowDefinitions>
            <RowDefinition Height="Auto" />
            <RowDefinition Height="*" />
        </Grid.RowDefinitions>
        <Grid.ColumnDefinitions>
            <ColumnDefinition Width="*" />
            <ColumnDefinition Width="Auto" />
        </Grid.ColumnDefinitions>
    
        <TextBox Name="addressBar" Grid.Column="0"/>
        <Button x:Name="myButton" Grid.Column="1" Click="myButton_Click">Go</Button>
        
        <WebView2 x:Name="MyWebView"  Grid.Row="1" Grid.ColumnSpan="2" 
            Source="https://www.microsoft.com" HorizontalAlignment="Stretch" VerticalAlignment="Stretch" />
    
    </Grid>
    ```  
    
1.  <span data-ttu-id="e5347-158">В **MainWindow.XAML.CS**Скопируйте приведенный ниже фрагмент кода `myButton_Click` , на который будет перемещаться по элементу управления WebView2 на URL-адрес, введенный в адресной строке.</span><span class="sxs-lookup"><span data-stu-id="e5347-158">In **MainWindow.xaml.cs**, copy the following code snippet to `myButton_Click`, which navigates the WebView2 control to the URL entered in the address bar.</span></span>  
    
    ```csharp
    private void myButton_Click(object sender, RoutedEventArgs e)
    {
        try
        {
            Uri targetUri = new Uri(addressBar.Text);
            MyWebView.Source = targetUri;
        }
        catch (FormatException ex)
        {
            // Incorrect address entered.
        }
    }
    ```  
    
    <span data-ttu-id="e5347-159">Выберите `F5` , чтобы выполнить сборку и запустить проект.</span><span class="sxs-lookup"><span data-stu-id="e5347-159">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="e5347-160">Введите новый URL-адрес в адресной строке и нажмите кнопку **Перейти**.</span><span class="sxs-lookup"><span data-stu-id="e5347-160">Enter a new URL in the address bar, and then select **Go**.</span></span>  <span data-ttu-id="e5347-161">Например, введите `https://www.bing.com` .</span><span class="sxs-lookup"><span data-stu-id="e5347-161">For example, enter `https://www.bing.com`.</span></span> 
    
    > [!NOTE]
    > <span data-ttu-id="e5347-162">Убедитесь в том, что в адресной строке используются полные URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="e5347-162">Ensure you use complete URLs in the address bar.</span></span> `ArgumentException` <span data-ttu-id="e5347-163">Если URL-адрес не начинается с or, возникают `http://` исключения `https://` .</span><span class="sxs-lookup"><span data-stu-id="e5347-163">exceptions are thrown if the URL does not start with `http://` or `https://`.</span></span>  
    
    :::image type="complex" source="./media/winui-gettingstarted-bing.png" alt-text="Bing.com" lightbox="./media/winui-gettingstarted-bing.png":::
       <span data-ttu-id="e5347-165">Bing.com</span><span class="sxs-lookup"><span data-stu-id="e5347-165">Bing.com</span></span>  
    :::image-end:::  
    
## <span data-ttu-id="e5347-166">Шаг 4 — события навигации</span><span class="sxs-lookup"><span data-stu-id="e5347-166">Step 4 - Navigation events</span></span>  

<span data-ttu-id="e5347-167">Приложения, на которых размещаются элементы управления WebView2, прослушивают следующие события, возникающие в элементах управления WebView2 на этапе навигации веб-страницы.</span><span class="sxs-lookup"><span data-stu-id="e5347-167">Applications that host WebView2 controls listen for the following events that are raised by WebView2 controls during web page navigation.</span></span>  

*   `NavigationStarting`  
*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
*   `NavigationCompleted`  
> [!NOTE]
> <span data-ttu-id="e5347-168">Переадресация HTTP вызывает несколько `NavigationStarting` событий.</span><span class="sxs-lookup"><span data-stu-id="e5347-168">HTTP redirects raise multiple `NavigationStarting` events.</span></span>  
<span data-ttu-id="e5347-169">Дополнительные сведения можно найти в разделе [события навигации][Webviews2ConceptsNavigationEvents].</span><span class="sxs-lookup"><span data-stu-id="e5347-169">For more information, see [Navigation Events][Webviews2ConceptsNavigationEvents].</span></span>  

<span data-ttu-id="e5347-170">При возникновении ошибок возникают следующие события, которые могут перейти на страницу ошибки.</span><span class="sxs-lookup"><span data-stu-id="e5347-170">When errors occur, the following events are raised and may navigate to an error page.</span></span>  

*   `SourceChanged`  
*   `ContentLoading`  
*   `HistoryChanged`  
    

<span data-ttu-id="e5347-171">В качестве примера использования событий Зарегистрируйте обработчик для `NavigationStarting` него, чтобы отменить все запросы, не ИСПОЛЬЗУЮЩИЕ HTTPS.</span><span class="sxs-lookup"><span data-stu-id="e5347-171">As an example of how to use the events, register a handler for `NavigationStarting` that cancels any requests that don't use HTTPS.</span></span> <span data-ttu-id="e5347-172">`MainWindow.xaml.cs`Измените конструктор, чтобы `EnsureHttps` он регистрировал, и добавьте `EnsureHttps` функцию так, чтобы она соответствовала следующему фрагменту кода.</span><span class="sxs-lookup"><span data-stu-id="e5347-172">In `MainWindow.xaml.cs`, modify the constructor to register `EnsureHttps`, and add the `EnsureHttps` function so that it matches the following code snippet.</span></span>  


```csharp
public MainWindow()
{
    InitializeComponent();
    MyWebView.NavigationStarting += EnsureHttps;
}

private void EnsureHttps(WebView2 sender, WebView2NavigationStartingEventArgs args)
{
    String uri = args.Uri;
    if (!uri.StartsWith("https://"))
    {
        args.Cancel = true;
    }
    else
    {
        addressBar.Text = uri;
    }
}
```  

<span data-ttu-id="e5347-173">Выберите `F5` , чтобы выполнить сборку и запустить проект.</span><span class="sxs-lookup"><span data-stu-id="e5347-173">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="e5347-174">Убедитесь, что Навигация заблокирована на сайтах HTTP и разрешена для HTTPS-сайтов.</span><span class="sxs-lookup"><span data-stu-id="e5347-174">Confirm that navigation is blocked to HTTP sites, and allowed for HTTPS sites.</span></span>  

## <span data-ttu-id="e5347-175">Шаг 5: создание сценариев</span><span class="sxs-lookup"><span data-stu-id="e5347-175">Step 5 - Scripting</span></span>  

<span data-ttu-id="e5347-176">Ведущее приложение может внедрять код JavaScript в элементы управления WebView2 во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="e5347-176">Host applications may inject JavaScript code into WebView2 controls at runtime.</span></span>  <span data-ttu-id="e5347-177">Вставленный JavaScript применяется ко всем новым документам верхнего уровня и дочерним кадрам до тех пор, пока не будет удален JavaScript.</span><span class="sxs-lookup"><span data-stu-id="e5347-177">The injected JavaScript applies to all new top level documents and any child frames until the JavaScript is removed.</span></span>  <span data-ttu-id="e5347-178">Вставленный JavaScript запускается после создания глобального объекта, а также перед запуском любого другого сценария, включенного в документ HTML.</span><span class="sxs-lookup"><span data-stu-id="e5347-178">The injected JavaScript is run after creation of the global object, and before any other script included in the HTML document is run.</span></span>  

<span data-ttu-id="e5347-179">В качестве примера добавьте сценарии, отправляющие предупреждение, когда пользователь переходит на сайты, не поддерживающие HTTPS.</span><span class="sxs-lookup"><span data-stu-id="e5347-179">As an example, add scripts send an alert when a user navigates to non-HTTPS sites.</span></span>  <span data-ttu-id="e5347-180">Измените `EnsureHttps` функцию, чтобы внедрить сценарий в веб-содержимое с помощью [ExecuteScriptAsync][Webviews2ReferenceWpf09515MicrosoftWebExecutescriptasync].</span><span class="sxs-lookup"><span data-stu-id="e5347-180">Modify the `EnsureHttps` function to inject a script into the web content using [ExecuteScriptAsync][Webviews2ReferenceWpf09515MicrosoftWebExecutescriptasync].</span></span>  

```csharp
private void EnsureHttps(WebView2 sender, WebView2NavigationStartingEventArgs args)
{
    String uri = args.Uri;
    if (!uri.StartsWith("https://"))
    {
        MyWebView.ExecuteScriptAsync($"alert('{uri} is not safe, try an https link')");
        args.Cancel = true;
    }
    else
    {
        addressBar.Text = uri;
    }
}
```  

<span data-ttu-id="e5347-181">Выберите `F5` , чтобы выполнить сборку и запустить проект.</span><span class="sxs-lookup"><span data-stu-id="e5347-181">Select `F5` to build and run your project.</span></span>  <span data-ttu-id="e5347-182">Убедитесь, что ваше приложение отображает оповещение при переходе на сайт, который не использует HTTPS.</span><span class="sxs-lookup"><span data-stu-id="e5347-182">Confirm that your application displays an alert when you navigate to a site that does not use HTTPS.</span></span>  

:::image type="complex" source="./media/winui-gettingstarted-script.png" alt-text="Элемент управления WebView2, в котором отображается диалоговое окно оповещения" lightbox="./media/winui-gettingstarted-script.png":::
   <span data-ttu-id="e5347-184">Элемент управления WebView2, в котором отображается диалоговое окно оповещения</span><span class="sxs-lookup"><span data-stu-id="e5347-184">WebView2 control showing an alert dialog</span></span>
:::image-end:::  

<span data-ttu-id="e5347-185">Поздравляем! вы создали первое приложение WebView2.</span><span class="sxs-lookup"><span data-stu-id="e5347-185">Congratulations, you built your first WebView2 app.</span></span>  

## <span data-ttu-id="e5347-186">Дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="e5347-186">Next Steps</span></span>  

<span data-ttu-id="e5347-187">Наша группа в настоящее время использует дополнительные API WebView2.</span><span class="sxs-lookup"><span data-stu-id="e5347-187">Our team is currently building more WebView2 APIs.</span></span>  <span data-ttu-id="e5347-188">Дополнительные сведения о текущем состоянии WebView2 API можно найти в описании [спецификации WebView2][GithubMicrosoftUiXamlSpecsWebview2].</span><span class="sxs-lookup"><span data-stu-id="e5347-188">For more information on the current state of WebView2 APIs, see the [WebView2 spec][GithubMicrosoftUiXamlSpecsWebview2].</span></span>  

> [!NOTE]
> <span data-ttu-id="e5347-189">Объект CoreWebView2 WinRT может быть недоступен на момент отгрузки API WebView2.</span><span class="sxs-lookup"><span data-stu-id="e5347-189">The WinRT CoreWebView2 object may not be available at the time the WebView2 APIs ship.</span></span> <span data-ttu-id="e5347-190">Чтобы узнать, какие API доступны для WebView2 элементов управления, ознакомьтесь со списком доступных API-интерфейсов в [WebView2 спецификации][GithubMicrosoftUiXamlSpecsWebview2] .</span><span class="sxs-lookup"><span data-stu-id="e5347-190">To understand which APIs are available to WebView2 controls, see [WebView2 Spec][GithubMicrosoftUiXamlSpecsWebview2] for a list of the APIs that are available.</span></span> 

<span data-ttu-id="e5347-191">Дополнительные сведения о возможностях WebView2 вы можете найти в статьях [концепции и руководства WebView2][Webview2IndexNextSteps], а также в [репозитории примеров использования WebView2][GithubMicrosoftedgeWebview2samplesMain].</span><span class="sxs-lookup"><span data-stu-id="e5347-191">For more information about WebView2 capabilities, see [WebView2 Concepts and How-To guides][Webview2IndexNextSteps], and the [WebView2 samples repo][GithubMicrosoftedgeWebview2samplesMain].</span></span>  

## <span data-ttu-id="e5347-192">Знакомство с командой Microsoft Edge WebView</span><span class="sxs-lookup"><span data-stu-id="e5347-192">Getting in touch with the Microsoft Edge WebView team</span></span>  

<span data-ttu-id="e5347-193">Помогите вам создать более WebView2ную работу, отправив свой отзыв.</span><span class="sxs-lookup"><span data-stu-id="e5347-193">Help build a richer WebView2 experience by sharing your feedback.</span></span>  <span data-ttu-id="e5347-194">Посетите центр [отзывов и предложений][GithubMicrosoftedgeWebviewfeedback] Microsoft Edge WebView, чтобы отправить запросы функций или отчеты об ошибках или найти известные проблемы.</span><span class="sxs-lookup"><span data-stu-id="e5347-194">Visit the Microsoft Edge WebView [feedback repo][GithubMicrosoftedgeWebviewfeedback] to submit feature requests or bug reports, or to search for known issues.</span></span>  

<!-- links -->  

[Webview2Index]: ../index.md "Введение в Microsoft Edge WebView2 (Предварительная версия) | Документы Microsoft"  
[Webview2IndexNextSteps]: ../index.md#next-steps "Дальнейшие действия — введение в Microsoft Edge WebView2 (Предварительная версия) | Документы Microsoft"  
[Webviews2ConceptsNavigationEvents]: ../concepts/navigation-events.md "События навигации | Документы Microsoft"  
[Webviews2ReferenceWpf09515MicrosoftWebExecutescriptasync]: ../reference/wpf/0-9-515/microsoft-web-webview2-wpf-webview2.md#executescriptasync "Класс ExecuteScriptAsync-Microsoft. Web. WebView2. WPF. WebView2 | Документы Microsoft"  

[UwpSchemasAppxpackageUapmanifestRoot]: /uwp/schemas/appxpackage/uapmanifestschema/schema-root "Справочник по схеме манифеста пакета для Windows 10 | Документы Microsoft"  

[WindowsAppsWinui3ConfigureYourDevEnvironment]: /windows/apps/winui/winui3#configure-your-dev-environment "Настройка среды разработки — библиотеки пользовательского интерфейса Windows 3,0 Preview (Май 2020) | Документы Microsoft"  
[WindowsMsixDesktopToUwpPackagingDotNet]: /windows/msix/desktop/desktop-to-uwp-packaging-dot-net "Настройка классического приложения для MSIX упаковки в Visual Studio | Документы Microsoft"  
[WindowsUwpGetStartedEnableYourDeviceForDevelopment]: /windows/uwp/get-started/enable-your-device-for-development "Активация устройства для разработки | Документы Microsoft"  

[GithubMicrosoftUiXamlSpecsWebview2]: https://github.com/microsoft/microsoft-ui-xaml-specs/blob/master/active/WebView2/WebView2_spec.md "WebView2 Spec-Microsoft/Microsoft-UI-XAML-specs | GitHub"  

[GithubMicrosoftedgeWebview2samplesMain]: https://github.com/MicrosoftEdge/WebView2Samples "WebView2 Samples-MicrosoftEdge/WebView2Samples | GitHub"  
[GithubMicrosoftedgeWebviewfeedback]: https://github.com/MicrosoftEdge/WebViewFeedback "WebView Feedback-MicrosoftEdge/WebViewFeedback | GitHub"  

[MicrosoftMain]: https://www.microsoft.com "SMTP"  

[MicrosoftSupport12373]: https://support.microsoft.com/help/12373 "Обновление Windows: вопросы и ответы"  

[MicrosoftedgeinsiderDownload]: https://www.microsoftedgeinsider.com/download "Скачайте каналы предварительной оценки Microsoft Edge"  

[WindowsDotnetcliBlobCoreSdk50100Preview4202681X86]: https://dotnetcli.blob.core.windows.net/dotnet/Sdk/5.0.100-preview.4.20268.1/dotnet-sdk-5.0.100-preview.4.20268.1-win-x86.exe "Скачать dotnet-sdk-5.0.100-preview.4.20268.1-win-x86.exe"  

[WindowsDotnetcliBlobCoreSdk50100Preview4202681X64]: https://dotnetcli.blob.core.windows.net/dotnet/Sdk/5.0.100-preview.4.20268.1/dotnet-sdk-5.0.100-preview.4.20268.1-win-x64.exe "dotnet-sdk-5.0.100-preview.4.20268.1-win-x64.exe"  

[VisualstudioMarketplaceWinUiprojecttemplates]: https://marketplace.visualstudio.com/items?itemName=Microsoft-WinUI.WinUIProjectTemplates "Шаблоны проектов WinUI 3"  
