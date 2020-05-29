---
description: Узнайте о том, как использовать встроенные системы обмена сообщениями, чтобы ваше расширение могло взаимодействовать с сопутствующим приложением UWP.
title: Расширения-собственная система обмена сообщениями
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: EDGE, веб-разработка, HTML, CSS, JavaScript, разработчик, собственный, Обмен сообщениями, UWP
ms.openlocfilehash: 83f80e112180317c38763225c1cdd015da4238b0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571544"
---
# <span data-ttu-id="7d532-104">Встроенные сообщения в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7d532-104">Native messaging in Microsoft Edge</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

## <span data-ttu-id="7d532-105">Общие сведения о собственной архитектуре сообщений</span><span class="sxs-lookup"><span data-stu-id="7d532-105">Native messaging architecture overview</span></span>

<span data-ttu-id="7d532-106">С помощью обновления Windows 10 Creators в расширениях Microsoft EDGE можно использовать встроенные сообщения для связи с приложением для универсальной платформы Windows (UWP).</span><span class="sxs-lookup"><span data-stu-id="7d532-106">With the Windows 10 Creators Update, Microsoft Edge extensions are able to use native messaging to communicate with a companion Universal Windows Platform (UWP) app.</span></span>  <span data-ttu-id="7d532-107">На высоком уровне в расширениях Microsoft Edge используются те же API для собственных сообщений, что и расширения Chrome и Firefox.</span><span class="sxs-lookup"><span data-stu-id="7d532-107">At a high level, Microsoft Edge extensions use the same APIs for native messaging as Chrome and Firefox extensions.</span></span> <span data-ttu-id="7d532-108">Тем не менее, собственный узел сообщений необходимо реализовать с помощью универсальной платформы Windows.</span><span class="sxs-lookup"><span data-stu-id="7d532-108">However, the native messaging host will need to be implemented using the Universal Windows Platform.</span></span>

> [!NOTE]
> <span data-ttu-id="7d532-109">Метод, описанный ниже (подключение к приложению UWP через AppService), является единственным поддерживаемым механизмом включения связи между расширениями Microsoft EDGE и собственными компонентами.</span><span class="sxs-lookup"><span data-stu-id="7d532-109">The method outlined below (connecting to a UWP app via AppService) is the only supported mechanism for enabling communication between Microsoft Edge extensions and native components.</span></span> <span data-ttu-id="7d532-110">Дополнительные сведения о том, как включить связь с устаревшими компонентами Win32, можно найти в разделе [Добавление компонентов рабочего стола в рамках программы Bridge](#adding-a-desktop-bridge-component) .</span><span class="sxs-lookup"><span data-stu-id="7d532-110">Please see the [Adding a Desktop Bridge component](#adding-a-desktop-bridge-component) section of this guide for more information on how to enable communication with legacy Win32 components.</span></span> 

 <span data-ttu-id="7d532-111">Собственная архитектура сообщений Microsoft Edge использует существующий [`AppService`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.aspx) API в качестве базовой инфраструктуры межпроцессного взаимодействия (IPC).</span><span class="sxs-lookup"><span data-stu-id="7d532-111">Microsoft Edge's native messaging architecture leverages the existing [`AppService`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.aspx) API as the underlying inter-process communication (IPC) infrastructure.</span></span> <span data-ttu-id="7d532-112">Приложения UWP используют `AppService` API для связи друг с другом.</span><span class="sxs-lookup"><span data-stu-id="7d532-112">UWP apps use the `AppService` API to communicate with one another.</span></span> <span data-ttu-id="7d532-113">Из-за этого расширения Microsoft EDGE теперь могут взаимодействовать с приложениями UWP.</span><span class="sxs-lookup"><span data-stu-id="7d532-113">Because of this, Microsoft Edge extensions can now communicate with UWP apps.</span></span>

![собственная архитектура сообщений](./../media/native-messaging-architecture.png)


### <span data-ttu-id="7d532-115">Когда и когда не следует использовать собственный обмен сообщениями</span><span class="sxs-lookup"><span data-stu-id="7d532-115">When and when not to use native messaging</span></span>

<span data-ttu-id="7d532-116">Встроенная система обмена сообщениями добавляет к своему расширению новый слой.</span><span class="sxs-lookup"><span data-stu-id="7d532-116">Native messaging adds a whole new layer to your extension.</span></span> <span data-ttu-id="7d532-117">Реализуя приложение UWP для вашего расширения, вам будут доступны указанные ниже возможности.</span><span class="sxs-lookup"><span data-stu-id="7d532-117">By implementing a UWP companion app for your extension, the following possibilities become available to you:</span></span>

* <span data-ttu-id="7d532-118">Синхронизируйте данные (например, учетные данные) с сопутствующим приложением UWP.</span><span class="sxs-lookup"><span data-stu-id="7d532-118">Synchronize data (e.g. credentials) with a companion UWP app.</span></span>
* <span data-ttu-id="7d532-119">Реализуйте более надежные алгоритмы шифрования и расшифровки, недоступные в веб-API.</span><span class="sxs-lookup"><span data-stu-id="7d532-119">Implement stronger encryption/decryption algorithms not available in web APIs.</span></span>
* <span data-ttu-id="7d532-120">Доступ к ресурсам, недоступным с помощью веб-API, например аппаратных средств и устройств USB</span><span class="sxs-lookup"><span data-stu-id="7d532-120">Access resources that are not accessible through web APIs, e.g. hardware or USB devices</span></span>

<span data-ttu-id="7d532-121">В связи с невозможностью использования встроенной системы обмена сообщениями из-за ограничений безопасности или политики есть несколько случаев.</span><span class="sxs-lookup"><span data-stu-id="7d532-121">There are a few instances where native messaging can't be used due to security or policy restrictions:</span></span>

* <span data-ttu-id="7d532-122">Изменение параметров пользователя в Microsoft EDGE или Windows, например изменение браузера по умолчанию или поставщика поиска.</span><span class="sxs-lookup"><span data-stu-id="7d532-122">Modifying user settings in either Microsoft Edge or Windows, e.g. changing the default browser or search provider.</span></span>
* <span data-ttu-id="7d532-123">Действия, которые нарушают политики Microsoft Store для приложений и расширений.</span><span class="sxs-lookup"><span data-stu-id="7d532-123">Actions that violate Microsoft Store policies for both apps and extensions.</span></span>
* <span data-ttu-id="7d532-124">Передача данных в удаленную конечную точку с помощью собственного хоста сообщений.</span><span class="sxs-lookup"><span data-stu-id="7d532-124">Transferring data to remote endpoint via native message host.</span></span>
* <span data-ttu-id="7d532-125">Разрешение другим приложениям загружать содержимое, которое изменяет поведение расширения.</span><span class="sxs-lookup"><span data-stu-id="7d532-125">Allowing other apps to download content that changes extension behavior.</span></span>

## <span data-ttu-id="7d532-126">Демонстрационные примеры</span><span class="sxs-lookup"><span data-stu-id="7d532-126">Demos</span></span>

<span data-ttu-id="7d532-127">Чтобы узнать, что такое собственное расширение почты Microsoft EDGE, которое имеет и сопутствующее приложение UWP, и внешний вид рабочего стола, ознакомьтесь с примерами [SecureInput](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/SecureInput) и [DigitalSigning (C++)](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/DigitalSigning) в GitHub.</span><span class="sxs-lookup"><span data-stu-id="7d532-127">To get a feel for what an Microsoft Edge native messaging extension that has both a companion UWP app and a Desktop Bridge looks like, check out the [SecureInput](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/SecureInput) and [DigitalSigning (C++)](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/DigitalSigning) examples on GitHub.</span></span>

### <span data-ttu-id="7d532-128">Принцип работы</span><span class="sxs-lookup"><span data-stu-id="7d532-128">How it works</span></span>

<span data-ttu-id="7d532-129">В компоненте расширения Microsoft Edge примера используется сценарий содержимого, чтобы определить, когда пользователь вводит данные, которые должны быть зашифрованы.</span><span class="sxs-lookup"><span data-stu-id="7d532-129">The Microsoft Edge extension component of the sample uses its content script to detect when a user is typing in information that should be encrypted.</span></span> <span data-ttu-id="7d532-130">Это расширение сообщает компоненту моста для настольных систем с помощью встроенного сообщения.</span><span class="sxs-lookup"><span data-stu-id="7d532-130">The extension communicates this to the Desktop Bridge component via native messaging.</span></span> <span data-ttu-id="7d532-131">После того как пользователь будет готов к отправке данных, расширение вернет зашифрованное значение обратно на веб-сайт.</span><span class="sxs-lookup"><span data-stu-id="7d532-131">When the user is ready to submit the data, the extension will return an encrypted value back to the website.</span></span>

> [!NOTE]
> <span data-ttu-id="7d532-132">Этот пример будет работать только на веб-странице, которая использует пользовательские события для связи с сценарием содержимого расширения.</span><span class="sxs-lookup"><span data-stu-id="7d532-132">This sample will only work on a webpage that uses custom events to communicate with the extension's content script.</span></span> <span data-ttu-id="7d532-133">В папке образца есть [HTML-файл](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/blob/master/SecureInput/SecureInput.html) , в котором нужно проверить расширение.</span><span class="sxs-lookup"><span data-stu-id="7d532-133">The sample folder includes a [.html file](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/blob/master/SecureInput/SecureInput.html) to test the extension with.</span></span>

<span data-ttu-id="7d532-134">В этом примере приложение UWP используется для передачи ответов из классического моста в Microsoft EDGE, который затем отправляется на расширение Microsoft Edge с помощью обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="7d532-134">In this example, the UWP app is used to pass responses from the Desktop Bridge to Microsoft Edge, which then gets sent to the Microsoft Edge extension via callback.</span></span> <span data-ttu-id="7d532-135">Несмотря на то, что в этом примере запущен собственный узел сообщений в главном приложении, его также можно запускать как фоновую задачу.</span><span class="sxs-lookup"><span data-stu-id="7d532-135">While this example has the native messaging host run in the main app, it's also able to run as a background task.</span></span> <span data-ttu-id="7d532-136">Для переключения между ними необходимо изменить фоновый сценарий расширения, изменив значение в строке `port = browser.runtime.connectNative("NativeMessagingHostInProcessService");` на `"NativeMessagingHostOutOfProcess"` .</span><span class="sxs-lookup"><span data-stu-id="7d532-136">Switching between the two requires editing the extension's background script, changing the string within `port = browser.runtime.connectNative("NativeMessagingHostInProcessService");` to `"NativeMessagingHostOutOfProcess"`.</span></span>

## <span data-ttu-id="7d532-137">Реализация хрома в противном случае Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="7d532-137">Chrome vs Microsoft Edge implementation</span></span>

<span data-ttu-id="7d532-138">Несмотря на то, что хром отправляет маршрут с помощью API передачи сообщений для своих расширений для взаимодействия с приложениями, Microsoft Edge использует [`AppService`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.aspx) API-интерфейс, который теперь поддерживает взаимодействие с расширениями Microsoft EDGE и приложениями UWP.</span><span class="sxs-lookup"><span data-stu-id="7d532-138">While Chrome goes the route of using message passing APIs for their extensions to communicate with apps, Microsoft Edge utilizes the [`AppService`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.aspx) API which now enables Microsoft Edge extensions and UWP apps to communicate.</span></span>

<span data-ttu-id="7d532-139">В этом разделе приведены сведения о различиях между хром и Microsoft EDGE, которые обрабатывают встроенную реализацию сообщений.</span><span class="sxs-lookup"><span data-stu-id="7d532-139">This section details the differences between how Chrome and Microsoft Edge handle native messaging implementation.</span></span>

### <span data-ttu-id="7d532-140">Регистрация и манифест узла</span><span class="sxs-lookup"><span data-stu-id="7d532-140">Registration and host manifest</span></span>
<span data-ttu-id="7d532-141">Чтобы ваше приложение распознало ваше расширение как собственный узел сообщений, его необходимо зарегистрировать.</span><span class="sxs-lookup"><span data-stu-id="7d532-141">In order for your app to be recognized by your extension as a native messaging host, it will need to be registered.</span></span>


<span data-ttu-id="7d532-142">Для регистрации [собственного узла сообщений Chrome](https://developer.chrome.com/extensions/nativeMessaging) приложение должно установить файл манифеста в любой точке файловой системы Windows, которая определяет конфигурацию собственного узла сообщений.</span><span class="sxs-lookup"><span data-stu-id="7d532-142">For [Chrome native messaging](https://developer.chrome.com/extensions/nativeMessaging) host registration, your app needs to install a manifest file anywhere in the Windows file system that defines the native messaging host configuration.</span></span>

<span data-ttu-id="7d532-143">В следующем примере показано, как можно настроить файл конфигурации.</span><span class="sxs-lookup"><span data-stu-id="7d532-143">The following JSON is an example of how the config file can be set up:</span></span>

```json
{
   "name": "com.my_company.my_application",
   "description": "My Application",
   "path": "C:\\ProgramFiles\\MyApplication\\chrome_native_messaging_host.exe",
   "type": "stdio",
   "allowed_origins": [
      "chrome-extension://knldjmfmopnpolahpmmgbagdohdnhkik/"
    ]
}
```

<span data-ttu-id="7d532-144">Чтобы установить этот файл, приложению потребуется:</span><span class="sxs-lookup"><span data-stu-id="7d532-144">To install this file, the app would need to:</span></span>

1. <span data-ttu-id="7d532-145">Зарегистрируйте файл манифеста в предварительно определенном расположении в реестре, которое определяет конфигурацию узла:</span><span class="sxs-lookup"><span data-stu-id="7d532-145">Register the manifest file in a predefined location in the registry that defines the host configuration:</span></span>
   - `HKEY_LOCAL_MACHINE\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application`

     <span data-ttu-id="7d532-146">или</span><span class="sxs-lookup"><span data-stu-id="7d532-146">or</span></span>
   - `HKEY_CURRENT_USER\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application`

2. <span data-ttu-id="7d532-147">Задайте в качестве значения по умолчанию для этого ключа полный путь к файлу манифеста, например:</span><span class="sxs-lookup"><span data-stu-id="7d532-147">Set the default value of that key to the full path to the manifest file, e.g.</span></span>  `[HKEY_CURRENT_USER\Software\Google\Chrome\NativeMessagingHosts\com.my_company.my_application] @="C:\\path\\to\\nmh-manifest.json"`




<span data-ttu-id="7d532-148">Для Microsoft EDGE, чтобы зарегистрировать [`AppService`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.aspx) (собственный хост-узел сообщений), вам нужно добавить приложение UWP в тот же пакет, что и расширение, и указать [расширение AppService](https://msdn.microsoft.com/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service) в `Package.appxmanifest` файле проекта.</span><span class="sxs-lookup"><span data-stu-id="7d532-148">For Microsoft Edge, in order to register an [`AppService`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.aspx)(native messaging host) you'll need to include the UWP companion app in the same package as your extension and specify the [AppService extension](https://msdn.microsoft.com/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service) in your project's `Package.appxmanifest` file.</span></span> <span data-ttu-id="7d532-149">`EntryPoint` `Name` Вы можете настроить следующие атрибуты:</span><span class="sxs-lookup"><span data-stu-id="7d532-149">The `EntryPoint` and `Name` attributes can be configured by you:</span></span>

```xml
...
<Applications>    
    <Application Id="App"         
        <Extensions>        
            <uap:Extension Category="windows.appService" EntryPoint="MyAppService.Inventory">          
            <uap:AppService Name="com.microsoft.inventory"/>        
            </uap:Extension>      
        </Extensions>      
        ...    
    </Application>
</Applications>
```


<span data-ttu-id="7d532-150">Кроме того, необходимо указать, какие расширения разрешено подключаться к службе.</span><span class="sxs-lookup"><span data-stu-id="7d532-150">You'll also need to set which extension(s) are allowed to connect to the service.</span></span> <span data-ttu-id="7d532-151">Так как Microsoft EDGE не имеет эквивалентного `"allowed_origins"` свойства манифеста в его appxmanifest, его необходимо определить и принудительно использовать в среде выполнения с помощью приложения UWP.</span><span class="sxs-lookup"><span data-stu-id="7d532-151">Because Microsoft Edge doesn't have an equivalent `"allowed_origins"` manifest property in its AppxManifest, this will need to be determined and enforced at runtime by your UWP app.</span></span> <span data-ttu-id="7d532-152">Поскольку Microsoft Edge будет устанавливать соединение от имени расширения, приложение может найти имя семейства пакетов вызывающего абонента, чтобы определить, есть ли у него соединение с помощью Microsoft EDGE, чтобы управлять вызывающим абонентом или проверять его подлинность.</span><span class="sxs-lookup"><span data-stu-id="7d532-152">Since Microsoft Edge will be establishing the connection on behalf of the extension, the app can look up the caller's Package Family Name to determine if they're being connected by Microsoft Edge to control or authenticate the caller.</span></span> <span data-ttu-id="7d532-153">Например:</span><span class="sxs-lookup"><span data-stu-id="7d532-153">E.g.</span></span> 

```csharp
protected async override void
OnBackgroundActivated(BackgroundActivatedEventArgs args)
{
    IBackgroundTaskInstance taskInstance = args.TaskInstance;
    if (taskInstance.TriggerDetails is AppServiceTriggerDetails)
    {
        AppServiceTriggerDetails appService = taskInstance.TriggerDetails as AppServiceTriggerDetails;
        if (appService.CallerPackageFamilyName == EdgePFN)
        {
            // Establish the connection
        }
        else
        {
            // Reject the connection
        }
    }
}
```



### <span data-ttu-id="7d532-154">Отправка сообщений</span><span class="sxs-lookup"><span data-stu-id="7d532-154">Message sending</span></span>

<span data-ttu-id="7d532-155">Чтобы приложение и расширение могли взаимодействовать друг с другом, сообщения должны быть отправлены и от них.</span><span class="sxs-lookup"><span data-stu-id="7d532-155">For an app and an extension to communicate with one another, messages need to be sent to and from them.</span></span>

<span data-ttu-id="7d532-156">Расширения Chrome инициируют сообщение, использующее [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) API для доставки сообщения на собственный хост с помощью несохраняемого канала.</span><span class="sxs-lookup"><span data-stu-id="7d532-156">Chrome extensions initiate a message using the [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) API to deliver a message to the native host using a non-persistent channel.</span></span> 

```javascript
chrome.runtime.sendNativeMessage(string application, object message, function responseCallback)
```

<span data-ttu-id="7d532-157">Первый параметр — это имя собственного хоста, который хром ищет в реестре для манифеста.</span><span class="sxs-lookup"><span data-stu-id="7d532-157">The first parameter is the name of the native host, which Chrome looks up in the registry for the manifest.</span></span> <span data-ttu-id="7d532-158">Манифест указывает exe-файл, который будет запущен хромом в песочнице, и сообщение будет отправлено с помощью STD i/o.</span><span class="sxs-lookup"><span data-stu-id="7d532-158">The manifest specifies the .exe that Chrome will launch in a sandbox, and the message is sent using std i/o.</span></span> <span data-ttu-id="7d532-159">Расширения также могут устанавливать сохраняемый канал с помощью `runtime.connectNative` API-интерфейса, который принимает имя собственного хоста в качестве единственного параметра.</span><span class="sxs-lookup"><span data-stu-id="7d532-159">Extensions can also establish a persistent channel using the `runtime.connectNative` API, which takes the name of the native host as the only parameter.</span></span> 

<span data-ttu-id="7d532-160">Microsoft Edge использует ту же конструкцию, что и собственный API сообщений для Chrome, чтобы разрешить расширениям Microsoft Edge указывать, к какой службе приложения нужно подключиться.</span><span class="sxs-lookup"><span data-stu-id="7d532-160">Microsoft Edge uses the same construct as Chrome's native messaging API to allow Microsoft Edge extensions to specify which app service to connect to.</span></span> <span data-ttu-id="7d532-161">Первый параметр в разделе `runtime.sendNativeMessage` указывает имя службы приложения.</span><span class="sxs-lookup"><span data-stu-id="7d532-161">The first parameter in `runtime.sendNativeMessage` specifies the app service name.</span></span> <span data-ttu-id="7d532-162">В разделе " [Регистрация и хост манифеста](#registration-and-host-manifest) " `"com.microsoft.inventory"` .</span><span class="sxs-lookup"><span data-stu-id="7d532-162">In the [Registration and host manifest](#registration-and-host-manifest) section, this is `"com.microsoft.inventory"`.</span></span> <span data-ttu-id="7d532-163">Платформа расширения Microsoft Edge ограничивает собственный узел сообщений приложением UWP, упакованным в том же AppX, что и расширение.</span><span class="sxs-lookup"><span data-stu-id="7d532-163">The Microsoft Edge extension platform restricts the native messaging host to being a UWP app that is packaged in the same AppX as the extension.</span></span> <span data-ttu-id="7d532-164">Это снизит риски безопасности, связанные с вредоносными атаками, которые пытаются подключить Microsoft Edge с другим именем семейства пакетов, изменив элементы манифеста.</span><span class="sxs-lookup"><span data-stu-id="7d532-164">This mitigates any security risks associated with malicious attacks that try to connect Microsoft Edge with another Package Family Name by tampering with manifest entries.</span></span> 

<span data-ttu-id="7d532-165">Это означает, что Microsoft Edge будет использовать то же имя семейства пакетов, что и расширение, в дополнение к `AppService` имени, указанному в API, для уникальной идентификации поставщика службы приложений.</span><span class="sxs-lookup"><span data-stu-id="7d532-165">This means that Microsoft Edge will use the same Package Family Name as the extension, in addition to the `AppService` name specified in the API, to uniquely identify the provider of the app service.</span></span>  

> [!NOTE]
> <span data-ttu-id="7d532-166">Это не будет просто преобразовано [набором средств расширения Microsoft Edge](./porting-chrome-extensions.md).</span><span class="sxs-lookup"><span data-stu-id="7d532-166">This will not be easily converted by the [Microsoft Edge Extension Toolkit](./porting-chrome-extensions.md).</span></span> <span data-ttu-id="7d532-167">Все расширения, указывающие на `"nativeMessaging"` разрешение, помечаются как требующие ручного преобразования для этого компонента.</span><span class="sxs-lookup"><span data-stu-id="7d532-167">Any extensions that specifies the `"nativeMessaging"` permission will be flagged as requiring manual conversion for this component.</span></span>





### <span data-ttu-id="7d532-168">Протокол связи</span><span class="sxs-lookup"><span data-stu-id="7d532-168">Communication protocol</span></span>

<span data-ttu-id="7d532-169">Протокол связи для сообщений в собственном формате определяет способ форматирования сообщений перед отправкой.</span><span class="sxs-lookup"><span data-stu-id="7d532-169">Communication protocol for native messaging determines how messages are formatted before sending.</span></span>

<span data-ttu-id="7d532-170">Хром запускает каждый машинный хост для обмена сообщениями в отдельном процессе и связывается с ним с помощью стандартного ввода и стандартного вывода.</span><span class="sxs-lookup"><span data-stu-id="7d532-170">Chrome starts each native messaging host in a separate process and communicates with it using standard input and standard output.</span></span> <span data-ttu-id="7d532-171">Для отправки сообщений в обоих направлениях используется один и тот же формат: каждое сообщение сериализуется с помощью JSON, UTF-8 кодируется и предшествует 32-разрядной длине сообщений в собственном байтовом порядке.</span><span class="sxs-lookup"><span data-stu-id="7d532-171">The same format is used to send messages in both directions: each message is serialized using JSON, UTF-8 encoded and is preceded with 32-bit message length in native byte order.</span></span>


<span data-ttu-id="7d532-172">Для Microsoft Edge приложение, которое реализует службу приложения, будет запущено платформой.</span><span class="sxs-lookup"><span data-stu-id="7d532-172">For Microsoft Edge, the background task/main app that implements the app service will be started by the platform.</span></span> <span data-ttu-id="7d532-173">При запуске метод фоновой задачи `Run` будет вызываться следующим образом:</span><span class="sxs-lookup"><span data-stu-id="7d532-173">On startup, the background task's `Run` method will be invoked:</span></span>  

```csharp
public void Run(IBackgroundTaskInstance taskInstance)    
{
    this.backgroundTaskDeferral = taskInstance.GetDeferral();
    // Get a deferral so that the service isn't terminated.
    taskInstance.Canceled += OnTaskCanceled;
    // Associate a cancellation handler with the background task.
    // Retrieve the app service connection and set up a listener for incoming app service requests.
    var details = taskInstance.TriggerDetails as AppServiceTriggerDetails;
    appServiceconnection = details.AppServiceConnection;
    appServiceconnection.RequestReceived += OnRequestReceived;
}
```

<span data-ttu-id="7d532-174">Когда ваше расширение отправляет сообщение в приложение UWP, [`onRequestReceived`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appserviceconnection.requestreceived) будет создано событие.</span><span class="sxs-lookup"><span data-stu-id="7d532-174">When your extension sends a message to your UWP app, the [`onRequestReceived`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appserviceconnection.requestreceived) event will be raised.</span></span> <span data-ttu-id="7d532-175">Затем это сообщение в формате JSON будет stringified в первую KeyValueую пару [`ValueSet`](https://msdn.microsoft.com/library/windows/apps/dn636131) объекта.</span><span class="sxs-lookup"><span data-stu-id="7d532-175">This JSON formatted message will then be stringified into the first KeyValue pair of a [`ValueSet`](https://msdn.microsoft.com/library/windows/apps/dn636131) object.</span></span> <span data-ttu-id="7d532-176">:</span><span class="sxs-lookup"><span data-stu-id="7d532-176">:</span></span>

```csharp
private async void OnRequestReceived(
AppServiceConnection sender,
AppServiceRequestReceivedEventArgs args)
{
    ...
}
```

<span data-ttu-id="7d532-177">Когда ваше приложение UWP отправляет ответ обратно на ваше расширение, в него [`KeyValuePair`](https://msdn.microsoft.com/library/windows/apps/5tbh8a42) добавляется объект a `ValueSet` .</span><span class="sxs-lookup"><span data-stu-id="7d532-177">When your UWP app sends a response back to your extension, a [`KeyValuePair`](https://msdn.microsoft.com/library/windows/apps/5tbh8a42) will be added to the `ValueSet` object.</span></span> <span data-ttu-id="7d532-178">`Key`Свойство будет игнорироваться Microsoft EDGE, но оно `Value` будет содержать допустимую строку JSON.</span><span class="sxs-lookup"><span data-stu-id="7d532-178">The `Key` property will be ignored by Microsoft Edge, but the `Value` property will contain a valid JSON string.</span></span>

### <span data-ttu-id="7d532-179">Предусмотрен</span><span class="sxs-lookup"><span data-stu-id="7d532-179">Callback</span></span>

<span data-ttu-id="7d532-180">Для обратных вызовов используется хром, [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) который позволяет функции обратного вызова обрабатывать любые асинхронные ответы от отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="7d532-180">For callbacks, Chrome uses [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) which allows a callback function to handle any asynchronous response from sending a message.</span></span>

<span data-ttu-id="7d532-181">Microsoft Edge использует [`AppServiceRequest`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appservicerequest) [`SendResponseAsync`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appservicerequest.sendresponseasync) метод объекта, чтобы приложение передавало [`ValueSet`](https://msdn.microsoft.com/library/windows/apps/dn636131) объекту обратное расширение.</span><span class="sxs-lookup"><span data-stu-id="7d532-181">Microsoft Edge uses the [`AppServiceRequest`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appservicerequest) object's [`SendResponseAsync`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appservicerequest.sendresponseasync) method to let the app send a [`ValueSet`](https://msdn.microsoft.com/library/windows/apps/dn636131) object back to the extension.</span></span>


### <span data-ttu-id="7d532-182">Предельный размер сообщения</span><span class="sxs-lookup"><span data-stu-id="7d532-182">Message size limit</span></span>
<span data-ttu-id="7d532-183">Сообщения, которые отправляются между расширением и приложением, имеют разные ограничения на размер сообщений для Chrome и Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7d532-183">Messages that are sent back and forth between an extension and an app have different message size limitations in place for Chrome and Microsoft Edge.</span></span>

<span data-ttu-id="7d532-184">У Chrome есть следующие ограничения на размер сообщений:</span><span class="sxs-lookup"><span data-stu-id="7d532-184">Chrome has the following message size limitations:</span></span>
- <span data-ttu-id="7d532-185">Ограничение на одно сообщение от собственного узла сообщений: 1 МБ</span><span class="sxs-lookup"><span data-stu-id="7d532-185">Single message limit from native messaging host: 1 MB</span></span>
- <span data-ttu-id="7d532-186">Число однозначных сообщений, отправленных на собственный хост сообщений: 4 ГБ</span><span class="sxs-lookup"><span data-stu-id="7d532-186">Single message limit sent to native messaging host: 4 GB</span></span>

<span data-ttu-id="7d532-187">В Microsoft EDGE, в то время как `AppService` ограничение на размер сообщения (зависит от памяти), Microsoft Edge защищает себя от некорректного поведения встроенных приложений, imposing следующие ограничения на размер сообщений.</span><span class="sxs-lookup"><span data-stu-id="7d532-187">For Microsoft Edge, while `AppService` has no limit on message size (dependent on memory), Microsoft Edge protects itself against misbehaving native apps by imposing the following message size limits:</span></span>
- <span data-ttu-id="7d532-188">Ограничение на одно сообщение от приложения UWP к расширению: 1 МБ</span><span class="sxs-lookup"><span data-stu-id="7d532-188">Single message limit from UWP app to extension: 1 MB</span></span>
- <span data-ttu-id="7d532-189">Ограничение на одно сообщение от расширения приложению UWP: 100 МБ</span><span class="sxs-lookup"><span data-stu-id="7d532-189">Single message limit from extension to UWP app: 100 MB</span></span>



### <span data-ttu-id="7d532-190">Встроенные подключения к сообщениям</span><span class="sxs-lookup"><span data-stu-id="7d532-190">Native messaging connections</span></span>

<span data-ttu-id="7d532-191">Существует два типа подключений для собственных сообщений. Постоянная и не постоянная.</span><span class="sxs-lookup"><span data-stu-id="7d532-191">There are two types of connections for native messaging; persistent and non-persistent.</span></span>
<span data-ttu-id="7d532-192">**Постоянное** соединение — это подключение, которое выполняется до тех пор, пока порт не будет удален.</span><span class="sxs-lookup"><span data-stu-id="7d532-192">A **persistent** connection is a connection that is kept running until the port is destroyed.</span></span> <span data-ttu-id="7d532-193">**Непостоянное** соединение — это подключение, которое открывается для одного сообщения за один раз и закрывается после доставки.</span><span class="sxs-lookup"><span data-stu-id="7d532-193">A **non-persistent** connection is a connection that is opened for one message at a time and closes after delivery.</span></span>

#### <span data-ttu-id="7d532-194">Постоянные правила</span><span class="sxs-lookup"><span data-stu-id="7d532-194">Persistent</span></span>

<span data-ttu-id="7d532-195">Для Chrome постоянное подключение создается путем создания порта сообщений с помощью [`runtime.connectNative`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative) .</span><span class="sxs-lookup"><span data-stu-id="7d532-195">For Chrome, a persistent connection is made by creating a messaging port using [`runtime.connectNative`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative).</span></span> <span data-ttu-id="7d532-196">После того как порт будет сделан, хром запускает собственный хост-процесс для сообщений, который продолжает выполняться до тех пор, пока не будет удален порт.</span><span class="sxs-lookup"><span data-stu-id="7d532-196">Once the port is made, Chrome starts a native messaging host process that keeps running until the port it destroyed.</span></span>

<span data-ttu-id="7d532-197">В Microsoft Edge после создания порта сообщения `runtime.connectNative` Microsoft Edge запускает [`AppServiceConnection`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appserviceconnection) и продолжает работу, пока порт не будет удален.</span><span class="sxs-lookup"><span data-stu-id="7d532-197">For Microsoft Edge, once a messaging port is created using `runtime.connectNative`, Microsoft Edge starts the [`AppServiceConnection`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appserviceconnection) and keeps it running until the port is destroyed.</span></span> <span data-ttu-id="7d532-198">В следующем фрагменте кода показано, как можно установить постоянное соединение в приложении UWP.</span><span class="sxs-lookup"><span data-stu-id="7d532-198">The following snippet shows how a persistent connection is established from within a UWP app.</span></span> 

```csharp
this.inventoryService = new AppServiceConnection();  
// Here, we use the app service name provided via the runtime.connectNative API  
this.inventoryService.AppServiceName = "com.microsoft.inventory";  
// Use the same Package Family Name as the extension package
this.inventoryService.PackageFamilyName = "replace with the Package Family Name";  
var status = await
this.inventoryService.OpenAsync();
```

#### <span data-ttu-id="7d532-199">Не постоянный</span><span class="sxs-lookup"><span data-stu-id="7d532-199">Non-persistent</span></span>

<span data-ttu-id="7d532-200">При отправке сообщения с помощью [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) Chrome без создания порта передачи данных хром запускает новый собственный хост-процесс для сообщений.</span><span class="sxs-lookup"><span data-stu-id="7d532-200">When a message is sent using [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) in Chrome, without creating a messaging port, Chrome starts a new native messaging host process for each message.</span></span> <span data-ttu-id="7d532-201">Первое сообщение, созданное ведущим процессом, обрабатывается как ответ на первоначальный запрос, а все остальные сообщения после него пропускаются.</span><span class="sxs-lookup"><span data-stu-id="7d532-201">The first message generated by the host process is handled as a response to the original request, and all other messages after it are ignored.</span></span>

<span data-ttu-id="7d532-202">Microsoft Edge прекратит подключение после получения ответа от каждого сообщения.</span><span class="sxs-lookup"><span data-stu-id="7d532-202">Microsoft Edge will terminate the connection after every messages' response has been received.</span></span> <span data-ttu-id="7d532-203">В следующем фрагменте кода показано непостоянное подключение, которое устанавливается вместе с ним, `AppServiceConnection` после получения запроса и его хранения в приложении UWP оно будет завершено [`AppServiceResponse`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appserviceresponse) .</span><span class="sxs-lookup"><span data-stu-id="7d532-203">The following snippet shows a non-persistent connection that is established with `AppServiceConnection` that will then be terminated within the UWP app after a request has been received and stored as an [`AppServiceResponse`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appserviceresponse).</span></span>

```csharp
using (var connection = new AppServiceConnection())
{    
    //Set up a new app service connection
    connection.AppServiceName = "com.microsoft.randomnumbergenerator";
    connection.PackageFamilyName = "Microsoft.SDKSamples.AppServicesProvider.CS_8wekyb3d8bbwe";
    AppServiceConnectionStatus status = await connection.OpenAsync();
    AppServiceResponse response = await connection.SendMessageAsync(inputs);
}
```

### <span data-ttu-id="7d532-204">Разрешение</span><span class="sxs-lookup"><span data-stu-id="7d532-204">Permission</span></span>

<span data-ttu-id="7d532-205">Чтобы включить встроенную функцию обмена сообщениями в свое расширение, для Chrome и Microsoft Edge вам нужно объявить это `"nativeMessaging"` разрешение в `manifest.json` файле.</span><span class="sxs-lookup"><span data-stu-id="7d532-205">In order to enable native messaging use with your extension, for both Chrome and Microsoft Edge you'll need to declare the `"nativeMessaging"` permission in you `manifest.json` file.</span></span>


## <span data-ttu-id="7d532-206">Услуги для приложений</span><span class="sxs-lookup"><span data-stu-id="7d532-206">App services</span></span>
<span data-ttu-id="7d532-207">В этом разделе приведены сведения о том, что службы приложения влияют на встроенную производительность и память сообщений Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7d532-207">This section details the impact app services has on Microsoft Edge native messaging performance and memory.</span></span>

### <span data-ttu-id="7d532-208">Производительность</span><span class="sxs-lookup"><span data-stu-id="7d532-208">Performance</span></span>

<span data-ttu-id="7d532-209">Службы приложений — это "спонсируемые" приложением переднего плана, вызывающие их, которые предназначены для собственных целей для обмена сообщениями — Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7d532-209">App services are "sponsored" by the foreground app that calls them which for native messaging purposes is Microsoft Edge.</span></span> <span data-ttu-id="7d532-210">Это означает, что службы приложений могут выполняться до тех пор, пока запущен Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7d532-210">This means that app services can run as long as Microsoft Edge is running.</span></span>

<span data-ttu-id="7d532-211">С точки зрения задержки службы приложений используют именованные каналы, после первоначального подключения к ним можно напрямую общаться два приложения.</span><span class="sxs-lookup"><span data-stu-id="7d532-211">In regards to latency, app services use named pipes that, after initial connection, allow two apps to directly communicate.</span></span> <span data-ttu-id="7d532-212">Этот способ обмена данными обеспечивает слабую задержку.</span><span class="sxs-lookup"><span data-stu-id="7d532-212">This method of communication produces low latency.</span></span> <span data-ttu-id="7d532-213">После запуска процесса, на котором размещается служба приложений (~ 80ms запускает фоновую задачу на некоторых устройствах), на устройствах с медленными процессорами будет возникать первая задержка.</span><span class="sxs-lookup"><span data-stu-id="7d532-213">Devices with slow CPUs will experience some initial latency after starting up the process that hosts the app service (~80ms to startup the background task on some devices).</span></span> <span data-ttu-id="7d532-214">После запуска системы производительность на медленном устройстве ЦП должна быть хорошей.</span><span class="sxs-lookup"><span data-stu-id="7d532-214">After start-up, performance on slow CPU devices should be good.</span></span> 


### <span data-ttu-id="7d532-215">Память</span><span class="sxs-lookup"><span data-stu-id="7d532-215">Memory</span></span>
<span data-ttu-id="7d532-216">Память, выделенная службе приложений, берется из квоты, выделенной для Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7d532-216">The memory allocated to an app service is taken out of the quota allocated to Microsoft Edge.</span></span> <span data-ttu-id="7d532-217">Это означает, что если Microsoft Edge запускает слишком много служб приложений, возможно, у них недостаточно памяти.</span><span class="sxs-lookup"><span data-stu-id="7d532-217">This means that if Microsoft Edge starts too many app services there is a possibility that they could run out of memory.</span></span> <span data-ttu-id="7d532-218">Обычно в службах приложений применяются стандартные ограничения памяти фоновой задачи.</span><span class="sxs-lookup"><span data-stu-id="7d532-218">The usual background task memory caps are enforced on app services.</span></span> <span data-ttu-id="7d532-219">Например, на устройстве с 512 МБ фоновая задача службы приложений не может быть больше 16 МБАЙТ.</span><span class="sxs-lookup"><span data-stu-id="7d532-219">For instance, on a 512MB device an app service background task can be no larger than 16MB.</span></span> <span data-ttu-id="7d532-220">Этот номер будет увеличиваться при масштабировании устройств.</span><span class="sxs-lookup"><span data-stu-id="7d532-220">This number goes up as the devices scale up.</span></span>


## <span data-ttu-id="7d532-221">Создание расширения с помощью собственного сообщения</span><span class="sxs-lookup"><span data-stu-id="7d532-221">Creating an extension with native messaging</span></span>

<span data-ttu-id="7d532-222">Для проверки собственного обмена сообщениями необходимо, чтобы расширение имело имя семейства пакетов.</span><span class="sxs-lookup"><span data-stu-id="7d532-222">In order to test native messaging, your extension needs a Package Family Name.</span></span> <span data-ttu-id="7d532-223">Microsoft Edge использует это для определения идентификатора собственного узла сообщений, что означает, что расширение должно быть упаковано.</span><span class="sxs-lookup"><span data-stu-id="7d532-223">Microsoft Edge uses this to determine the native message host identity, which means your extension should be packaged.</span></span> 


<span data-ttu-id="7d532-224">Чтобы создать расширение с помощью встроенного обмена сообщениями в Visual Studio, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="7d532-224">To create your extension with native messaging in Visual Studio:</span></span>

1. <span data-ttu-id="7d532-225">Создайте проект UWP в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="7d532-225">Create a UWP project in Visual Studio.</span></span>
2. <span data-ttu-id="7d532-226">[Добавьте `AppService` в приложение UWP](https://msdn.microsoft.com/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service).</span><span class="sxs-lookup"><span data-stu-id="7d532-226">[Add `AppService` to your UWP app](https://msdn.microsoft.com/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service).</span></span>
   - <span data-ttu-id="7d532-227">При необходимости вы можете [настроить `AppService` размещение в главном приложении](https://msdn.microsoft.com/windows/uwp/launch-resume/convert-app-service-in-process) , а не в фоновой задаче на этом этапе.</span><span class="sxs-lookup"><span data-stu-id="7d532-227">You can optionally [configure `AppService` to be hosted in the main app](https://msdn.microsoft.com/windows/uwp/launch-resume/convert-app-service-in-process) instead of as a background task at this point.</span></span>
3. <span data-ttu-id="7d532-228">Создание и тестирование проекта UWP.</span><span class="sxs-lookup"><span data-stu-id="7d532-228">Build and test your UWP project.</span></span>
   - <span data-ttu-id="7d532-229">При желании вы можете добавить [компонент "мост для настольных систем](#adding-a-desktop-bridge-component)".</span><span class="sxs-lookup"><span data-stu-id="7d532-229">You can optionally add a [Desktop Bridge component](#adding-a-desktop-bridge-component).</span></span>
4. <span data-ttu-id="7d532-230">Создайте расширение Microsoft EDGE, использующее собственный обмен сообщениями для общения с приложением UWP.</span><span class="sxs-lookup"><span data-stu-id="7d532-230">Create a Microsoft Edge extension that uses native messaging to communicate with the UWP companion app.</span></span> <span data-ttu-id="7d532-231">Файлы расширений можно добавить в папку, указанную `Extension` в проекте UWP.</span><span class="sxs-lookup"><span data-stu-id="7d532-231">The extension files can be added into a folder named `Extension` in the UWP project.</span></span> <span data-ttu-id="7d532-232">Для всех файлов в этой папке, включая вложенные папки, необходимо настроить их свойства, чтобы `Build Action=Content` и `Copy to Output Directory=Copy Always` .</span><span class="sxs-lookup"><span data-stu-id="7d532-232">All of the files underneath this folder, including subfolders, need to have their properties configured such that `Build Action=Content` and `Copy to Output Directory=Copy Always`.</span></span> <span data-ttu-id="7d532-233">Убедитесь `manifest.json` , что эти свойства также настроены.</span><span class="sxs-lookup"><span data-stu-id="7d532-233">Make sure `manifest.json` is also configured with these properties.</span></span>
5. <span data-ttu-id="7d532-234">Измените `package.manifest.xml` файл в проекте, чтобы включить в него метаданные расширения, и преобразуйте его в приложение без монитора, добавив `AppListEntry="none"` :</span><span class="sxs-lookup"><span data-stu-id="7d532-234">Modify the `package.manifest.xml` file in the project to include extension metadata and convert it to a headless app by adding `AppListEntry="none"`:</span></span>

    ```xml
    <Package
    xmlns="http://schemas.microsoft.com/appx/manifest/foundation/windows10" 
    xmlns:rescap="http://schemas.microsoft.com/appx/manifest/foundation/windows10/restrictedcapabilities" 
    xmlns:mp="http://schemas.microsoft.com/appx/2014/phone/manifest" 
    xmlns:uap="http://schemas.microsoft.com/appx/manifest/uap/windows10" 
    xmlns:uap3="http://schemas.microsoft.com/appx/manifest/uap/windows10/3"
    IgnorableNamespaces="uap uap3 mp rescap build" 
    xmlns:build="http://schemas.microsoft.com/developer/appx/2015/build">

    <Dependencies>
        <TargetDeviceFamily Name="Windows.Desktop" MinVersion="10.0.15063.0" MaxVersionTested="10.0.15063.0" />
    </Dependencies>

       <Application Id="App" Executable="$targetnametoken$.exe" EntryPoint="NativeMessagingHostInProcess.App">
          <uap:VisualElements AppListEntry="none"
            DisplayName="SecureInput"
            Square150x150Logo="Assets\Square150x150Logo.png"
            Square44x44Logo="Assets\Square44x44Logo.png"
            Description="NativeMessagingHostInProcess"
            BackgroundColor="transparent">
          </uap:VisualElements>
          <Extensions>
            <uap3:Extension Category="windows.appExtension">
                <uap3:AppExtension
                    Name="com.microsoft.edge.extension"
                    Id="EdgeExtension"
                    PublicFolder="Extension"
                    DisplayName="ms-resource:DisplayName">
                </uap3:AppExtension>
            </uap3:Extension>
          </Extensions>
    </Application>
    ```

6. <span data-ttu-id="7d532-235">Используйте `AppService` имя, заданное для UWP в собственных API для обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="7d532-235">Use the `AppService` name configured for the UWP in the native messaging APIs.</span></span>
7. <span data-ttu-id="7d532-236">Сборка и [развертывание](#deploying) проекта UWP (с дополнительным компонентом моста для настольных систем).</span><span class="sxs-lookup"><span data-stu-id="7d532-236">Build and [deploy](#deploying) the UWP project (with the optional Desktop Bridge component).</span></span>
8. <span data-ttu-id="7d532-237">[Упаковка](#packaging) собственного расширения для обмена сообщениями после того, как оно будет готово к отправке в магазине</span><span class="sxs-lookup"><span data-stu-id="7d532-237">[Package](#packaging) your native messaging extension once it's ready for Store submission</span></span>

> [!NOTE]
> <span data-ttu-id="7d532-238">Ознакомьтесь с разделом [демонстрационные материалы](#demos) , чтобы получить пример встроенного расширения для обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="7d532-238">Reference the [Demos](#demos) section for an example of a complete native messaging extension.</span></span>


## <span data-ttu-id="7d532-239">Добавление компонента Desktop Bridge</span><span class="sxs-lookup"><span data-stu-id="7d532-239">Adding a Desktop Bridge component</span></span> 
<span data-ttu-id="7d532-240">Если вы хотите добавить в пакет компонент Desktop Bridge, вам потребуется создать и построить проект Win32 в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="7d532-240">If you want to add a Desktop Bridge component to your package, you'll need to create and build your Win32 project in Visual Studio.</span></span> <span data-ttu-id="7d532-241">Сведения о том, как преобразовать приложение Win32 в UWP, можно найти в статье [Перенос приложений в Windows 10 через мост для настольных систем](/windows/uwp/porting/desktop-to-uwp-root).</span><span class="sxs-lookup"><span data-stu-id="7d532-241">For info on how to convert your win32 app to UWP, see [Porting apps to Windows 10 via Desktop Bridge](/windows/uwp/porting/desktop-to-uwp-root).</span></span> <span data-ttu-id="7d532-242">После того как вы выстроили в Visual Studio, вы можете добавить исполняемый файл Win32 в пакет, выполнив указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="7d532-242">Once built in Visual Studio, you can add the Win32 executable to the package by doing the following steps:</span></span>

1. <span data-ttu-id="7d532-243">Добавьте проект Win32 в то же решение, что и проект UWP.</span><span class="sxs-lookup"><span data-stu-id="7d532-243">Add the Win32 project to the same solution as the UWP project.</span></span> 

2. <span data-ttu-id="7d532-244">Настройте проект Win32 как зависимый проект для проекта UWP.</span><span class="sxs-lookup"><span data-stu-id="7d532-244">Set the Win32 project as a dependent project for the UWP project:</span></span>

    ![Настройка зависимостей проектов](./../media/project-dependencies.PNG)

3. <span data-ttu-id="7d532-246">Создайте `Win32` папку в проекте UWP.</span><span class="sxs-lookup"><span data-stu-id="7d532-246">Create a `Win32` folder within the UWP project.</span></span> <span data-ttu-id="7d532-247">Скопируйте необходимые двоичные файлы `Win32` проекта в эту папку.</span><span class="sxs-lookup"><span data-stu-id="7d532-247">Copy the necessary binaries for the `Win32` project to this folder.</span></span> <span data-ttu-id="7d532-248">Настройте свойства всех двоичных файлов так, чтобы `Build Action=Content` и `Copy to Output Directory=Copy Always` .</span><span class="sxs-lookup"><span data-stu-id="7d532-248">Configure the properties of all the binaries such that `Build Action=Content` and `Copy to Output Directory=Copy Always`.</span></span>

    ![папка с файлами приложения Win32 и UWP](./../media/desktop-bridge.png)

4. <span data-ttu-id="7d532-250">Измените файл проекта UWP, чтобы скопировать все необходимые двоичные файлы для `Win32` проекта в эту папку с помощью команды Event Build.</span><span class="sxs-lookup"><span data-stu-id="7d532-250">Modify the UWP project file to copy all the necessary binaries for the `Win32` project into this folder using PostBuild event command.</span></span> <span data-ttu-id="7d532-251">Это гарантирует, что обновленные двоичные файлы копируются в папку каждый раз при перестроении решения.</span><span class="sxs-lookup"><span data-stu-id="7d532-251">This ensures that the updated binaries are being copied to the folder every time the solution is rebuilt.</span></span>

    ```xml
    <Target Name="AfterBuild">
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.exe" DestinationFolder="win32" />
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.exe.config" DestinationFolder="win32" />
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.pdb" DestinationFolder="win32" />
    </Target>
    ```


5. <span data-ttu-id="7d532-252">`package.manifest.xml`Для изменения добавьте `<desktop:Extension>` элемент в `<Extensions>` элемент:</span><span class="sxs-lookup"><span data-stu-id="7d532-252">Modify `package.manifest.xml` by adding the `<desktop:Extension>` element to the `<Extensions>` element:</span></span>

    ```xml
    <Extensions>
    <desktop:Extension Category="windows.fullTrustProcess"Executable="Win32\PasswordInputProtection.exe"
    xmlns:desktop="http://schemas.microsoft.com/appx/manifest/desktop/windows10" />
    </Extensions>
    ```

## <span data-ttu-id="7d532-253">Развертывание</span><span class="sxs-lookup"><span data-stu-id="7d532-253">Deploying</span></span>
<span data-ttu-id="7d532-254">После того как вы настроили проект UWP (и, при необходимости, проект Win32) как описано выше, вы можете развернуть решение с помощью Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="7d532-254">Once you have configured your UWP project (and optionally Win32 project) as outlined above, you are ready to deploy the solution using Visual Studio.</span></span>

![проект "сборка, процесс сборки"](../media/native-message-uwp-debug.PNG)

<span data-ttu-id="7d532-256">После того как решение будет развернуто правильно, вы увидите расширение в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7d532-256">Once the solution is correctly deployed, you should see your extension in Microsoft Edge.</span></span>

![расширение, показанное в Microsoft Edge](../media/secureextension.png)

## <span data-ttu-id="7d532-258">Упакован</span><span class="sxs-lookup"><span data-stu-id="7d532-258">Packaging</span></span>

> [!NOTE]
> <span data-ttu-id="7d532-259">Отправка расширения Microsoft EDGE в Microsoft Store в настоящее время ограничена возможностями.</span><span class="sxs-lookup"><span data-stu-id="7d532-259">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span> <span data-ttu-id="7d532-260">[Поделитесь с нами](https://aka.ms/extension-request) с помощью ваших запросов на участие в Microsoft Store, и мы поможем вам ознакомиться с будущими обновлениями.</span><span class="sxs-lookup"><span data-stu-id="7d532-260">[Reach out to us](https://aka.ms/extension-request) with your requests to be a part of the Microsoft Store, and we'll consider you for a future update.</span></span>


<span data-ttu-id="7d532-261">Вы можете создать пакет магазина для отправки в центр разработки для Windows с помощью встроенных функций Visual Studio:</span><span class="sxs-lookup"><span data-stu-id="7d532-261">You can generate a Store package for submission to the Windows Dev Center using built-in Visual Studio functionality:</span></span>


![Создание пакета магазина](../media/create-store-package.PNG)

## <span data-ttu-id="7d532-263">Отладка</span><span class="sxs-lookup"><span data-stu-id="7d532-263">Debugging</span></span>
<span data-ttu-id="7d532-264">Инструкции по отладке зависят от того, какой компонент нужно протестировать.</span><span class="sxs-lookup"><span data-stu-id="7d532-264">The instructions for debugging vary depending on which component you want to test out:</span></span>

### <span data-ttu-id="7d532-265">Отладка расширения</span><span class="sxs-lookup"><span data-stu-id="7d532-265">Debugging the extension</span></span>
<span data-ttu-id="7d532-266">После развертывания решения расширение будет установлено в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="7d532-266">Once the solution is deployed, the extension will be installed in Microsoft Edge.</span></span> <span data-ttu-id="7d532-267">Сведения о том, как отлаживать расширение, можно найти в руководстве по [отладке](./debugging-extensions.md) .</span><span class="sxs-lookup"><span data-stu-id="7d532-267">Check out the [Debugging](./debugging-extensions.md) guide for info on how to debug an extension.</span></span>


### <span data-ttu-id="7d532-268">Отладка приложения UWP</span><span class="sxs-lookup"><span data-stu-id="7d532-268">Debugging the UWP app</span></span>
<span data-ttu-id="7d532-269">Приложение UWP запускается, когда расширение пытается подключиться к нему с помощью [собственных API для обмена сообщениями](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative).</span><span class="sxs-lookup"><span data-stu-id="7d532-269">The UWP app will launch when the extension tries to connect to it using [native messaging APIs](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative).</span></span> <span data-ttu-id="7d532-270">Отладка приложения UWP должна выполняться только после запуска процесса.</span><span class="sxs-lookup"><span data-stu-id="7d532-270">You'll need to debug the UWP app only once the process starts.</span></span> <span data-ttu-id="7d532-271">Это можно настроить с помощью страницы свойств проекта.</span><span class="sxs-lookup"><span data-stu-id="7d532-271">This can be configured via the project's Property page:</span></span>

1.  <span data-ttu-id="7d532-272">В Visual Studio щелкните проект приложения UWP правой кнопкой мыши</span><span class="sxs-lookup"><span data-stu-id="7d532-272">In Visual Studio, right click your UWP app project</span></span>
2.  <span data-ttu-id="7d532-273">Выберите свойства</span><span class="sxs-lookup"><span data-stu-id="7d532-273">Select Properties</span></span>
3.  <span data-ttu-id="7d532-274">Флажок "не запускать, но выполнять отладку моего кода при запуске"</span><span class="sxs-lookup"><span data-stu-id="7d532-274">Check "Do not launch, but debug my code when it starts"</span></span>

    ![Установка флажка "не запускать"](../media/native-message-do-not-launch.png)

<span data-ttu-id="7d532-276">В Visual Studio теперь можно установить точки останова в коде, в котором нужно выполнить отладку, а затем запустить отладчик, нажав клавишу F5.</span><span class="sxs-lookup"><span data-stu-id="7d532-276">In Visual Studio you can now set breakpoints in the code where you want to debug, then launch the debugger by pressing F5.</span></span> <span data-ttu-id="7d532-277">После того как вы взаимодействуете с расширением для подключения к приложению UWP, Visual Studio будет автоматически присоединиться к этому процессу.</span><span class="sxs-lookup"><span data-stu-id="7d532-277">Once you interact with the extension to connect to the UWP app, Visual Studio will automatically attach to the process.</span></span>


### <span data-ttu-id="7d532-278">Отладка настольного моста</span><span class="sxs-lookup"><span data-stu-id="7d532-278">Debugging the Desktop Bridge</span></span>
<span data-ttu-id="7d532-279">Несмотря на то что существуют различные [методы для отладки моста для настольных систем](https://msdn.microsoft.com/windows/uwp/porting/desktop-to-uwp-debug) (преобразованного приложения Win32), единственным применимым для этих сценариев является параметр PLMDebug.</span><span class="sxs-lookup"><span data-stu-id="7d532-279">Even though there are various [methods for debugging a Desktop Bridge](https://msdn.microsoft.com/windows/uwp/porting/desktop-to-uwp-debug) (converted Win32 app), the only one applicable for this scenarios is the PLMDebug option.</span></span> <span data-ttu-id="7d532-280">Вы также можете добавить отладочный код в функцию Startup для выполнения ожидания в течение определенного времени, позволяя присоединить Visual Studio к процессу.</span><span class="sxs-lookup"><span data-stu-id="7d532-280">You could also add debugging code to the startup function to perform a wait for a specific time, allowing you to attach Visual Studio to the process.</span></span>
