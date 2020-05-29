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
# Встроенные сообщения в Microsoft Edge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

## Общие сведения о собственной архитектуре сообщений

С помощью обновления Windows 10 Creators в расширениях Microsoft EDGE можно использовать встроенные сообщения для связи с приложением для универсальной платформы Windows (UWP).  На высоком уровне в расширениях Microsoft Edge используются те же API для собственных сообщений, что и расширения Chrome и Firefox. Тем не менее, собственный узел сообщений необходимо реализовать с помощью универсальной платформы Windows.

> [!NOTE]
> Метод, описанный ниже (подключение к приложению UWP через AppService), является единственным поддерживаемым механизмом включения связи между расширениями Microsoft EDGE и собственными компонентами. Дополнительные сведения о том, как включить связь с устаревшими компонентами Win32, можно найти в разделе [Добавление компонентов рабочего стола в рамках программы Bridge](#adding-a-desktop-bridge-component) . 

 Собственная архитектура сообщений Microsoft Edge использует существующий [`AppService`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.aspx) API в качестве базовой инфраструктуры межпроцессного взаимодействия (IPC). Приложения UWP используют `AppService` API для связи друг с другом. Из-за этого расширения Microsoft EDGE теперь могут взаимодействовать с приложениями UWP.

![собственная архитектура сообщений](./../media/native-messaging-architecture.png)


### Когда и когда не следует использовать собственный обмен сообщениями

Встроенная система обмена сообщениями добавляет к своему расширению новый слой. Реализуя приложение UWP для вашего расширения, вам будут доступны указанные ниже возможности.

* Синхронизируйте данные (например, учетные данные) с сопутствующим приложением UWP.
* Реализуйте более надежные алгоритмы шифрования и расшифровки, недоступные в веб-API.
* Доступ к ресурсам, недоступным с помощью веб-API, например аппаратных средств и устройств USB

В связи с невозможностью использования встроенной системы обмена сообщениями из-за ограничений безопасности или политики есть несколько случаев.

* Изменение параметров пользователя в Microsoft EDGE или Windows, например изменение браузера по умолчанию или поставщика поиска.
* Действия, которые нарушают политики Microsoft Store для приложений и расширений.
* Передача данных в удаленную конечную точку с помощью собственного хоста сообщений.
* Разрешение другим приложениям загружать содержимое, которое изменяет поведение расширения.

## Демонстрационные примеры

Чтобы узнать, что такое собственное расширение почты Microsoft EDGE, которое имеет и сопутствующее приложение UWP, и внешний вид рабочего стола, ознакомьтесь с примерами [SecureInput](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/SecureInput) и [DigitalSigning (C++)](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/tree/master/DigitalSigning) в GitHub.

### Принцип работы

В компоненте расширения Microsoft Edge примера используется сценарий содержимого, чтобы определить, когда пользователь вводит данные, которые должны быть зашифрованы. Это расширение сообщает компоненту моста для настольных систем с помощью встроенного сообщения. После того как пользователь будет готов к отправке данных, расширение вернет зашифрованное значение обратно на веб-сайт.

> [!NOTE]
> Этот пример будет работать только на веб-странице, которая использует пользовательские события для связи с сценарием содержимого расширения. В папке образца есть [HTML-файл](https://github.com/MicrosoftEdge/MicrosoftEdge-Extensions-Demos/blob/master/SecureInput/SecureInput.html) , в котором нужно проверить расширение.

В этом примере приложение UWP используется для передачи ответов из классического моста в Microsoft EDGE, который затем отправляется на расширение Microsoft Edge с помощью обратного вызова. Несмотря на то, что в этом примере запущен собственный узел сообщений в главном приложении, его также можно запускать как фоновую задачу. Для переключения между ними необходимо изменить фоновый сценарий расширения, изменив значение в строке `port = browser.runtime.connectNative("NativeMessagingHostInProcessService");` на `"NativeMessagingHostOutOfProcess"` .

## Реализация хрома в противном случае Microsoft Edge

Несмотря на то, что хром отправляет маршрут с помощью API передачи сообщений для своих расширений для взаимодействия с приложениями, Microsoft Edge использует [`AppService`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.aspx) API-интерфейс, который теперь поддерживает взаимодействие с расширениями Microsoft EDGE и приложениями UWP.

В этом разделе приведены сведения о различиях между хром и Microsoft EDGE, которые обрабатывают встроенную реализацию сообщений.

### Регистрация и манифест узла
Чтобы ваше приложение распознало ваше расширение как собственный узел сообщений, его необходимо зарегистрировать.


Для регистрации [собственного узла сообщений Chrome](https://developer.chrome.com/extensions/nativeMessaging) приложение должно установить файл манифеста в любой точке файловой системы Windows, которая определяет конфигурацию собственного узла сообщений.

В следующем примере показано, как можно настроить файл конфигурации.

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

Чтобы установить этот файл, приложению потребуется:

1. Зарегистрируйте файл манифеста в предварительно определенном расположении в реестре, которое определяет конфигурацию узла:
   - `HKEY_LOCAL_MACHINE\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application`

     или
   - `HKEY_CURRENT_USER\SOFTWARE\Google\Chrome\NativeMessagingHosts\com.my_company.my_application`

2. Задайте в качестве значения по умолчанию для этого ключа полный путь к файлу манифеста, например:  `[HKEY_CURRENT_USER\Software\Google\Chrome\NativeMessagingHosts\com.my_company.my_application] @="C:\\path\\to\\nmh-manifest.json"`




Для Microsoft EDGE, чтобы зарегистрировать [`AppService`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.aspx) (собственный хост-узел сообщений), вам нужно добавить приложение UWP в тот же пакет, что и расширение, и указать [расширение AppService](https://msdn.microsoft.com/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service) в `Package.appxmanifest` файле проекта. `EntryPoint` `Name` Вы можете настроить следующие атрибуты:

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


Кроме того, необходимо указать, какие расширения разрешено подключаться к службе. Так как Microsoft EDGE не имеет эквивалентного `"allowed_origins"` свойства манифеста в его appxmanifest, его необходимо определить и принудительно использовать в среде выполнения с помощью приложения UWP. Поскольку Microsoft Edge будет устанавливать соединение от имени расширения, приложение может найти имя семейства пакетов вызывающего абонента, чтобы определить, есть ли у него соединение с помощью Microsoft EDGE, чтобы управлять вызывающим абонентом или проверять его подлинность. Например: 

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



### Отправка сообщений

Чтобы приложение и расширение могли взаимодействовать друг с другом, сообщения должны быть отправлены и от них.

Расширения Chrome инициируют сообщение, использующее [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) API для доставки сообщения на собственный хост с помощью несохраняемого канала. 

```javascript
chrome.runtime.sendNativeMessage(string application, object message, function responseCallback)
```

Первый параметр — это имя собственного хоста, который хром ищет в реестре для манифеста. Манифест указывает exe-файл, который будет запущен хромом в песочнице, и сообщение будет отправлено с помощью STD i/o. Расширения также могут устанавливать сохраняемый канал с помощью `runtime.connectNative` API-интерфейса, который принимает имя собственного хоста в качестве единственного параметра. 

Microsoft Edge использует ту же конструкцию, что и собственный API сообщений для Chrome, чтобы разрешить расширениям Microsoft Edge указывать, к какой службе приложения нужно подключиться. Первый параметр в разделе `runtime.sendNativeMessage` указывает имя службы приложения. В разделе " [Регистрация и хост манифеста](#registration-and-host-manifest) " `"com.microsoft.inventory"` . Платформа расширения Microsoft Edge ограничивает собственный узел сообщений приложением UWP, упакованным в том же AppX, что и расширение. Это снизит риски безопасности, связанные с вредоносными атаками, которые пытаются подключить Microsoft Edge с другим именем семейства пакетов, изменив элементы манифеста. 

Это означает, что Microsoft Edge будет использовать то же имя семейства пакетов, что и расширение, в дополнение к `AppService` имени, указанному в API, для уникальной идентификации поставщика службы приложений.  

> [!NOTE]
> Это не будет просто преобразовано [набором средств расширения Microsoft Edge](./porting-chrome-extensions.md). Все расширения, указывающие на `"nativeMessaging"` разрешение, помечаются как требующие ручного преобразования для этого компонента.





### Протокол связи

Протокол связи для сообщений в собственном формате определяет способ форматирования сообщений перед отправкой.

Хром запускает каждый машинный хост для обмена сообщениями в отдельном процессе и связывается с ним с помощью стандартного ввода и стандартного вывода. Для отправки сообщений в обоих направлениях используется один и тот же формат: каждое сообщение сериализуется с помощью JSON, UTF-8 кодируется и предшествует 32-разрядной длине сообщений в собственном байтовом порядке.


Для Microsoft Edge приложение, которое реализует службу приложения, будет запущено платформой. При запуске метод фоновой задачи `Run` будет вызываться следующим образом:  

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

Когда ваше расширение отправляет сообщение в приложение UWP, [`onRequestReceived`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appserviceconnection.requestreceived) будет создано событие. Затем это сообщение в формате JSON будет stringified в первую KeyValueую пару [`ValueSet`](https://msdn.microsoft.com/library/windows/apps/dn636131) объекта. :

```csharp
private async void OnRequestReceived(
AppServiceConnection sender,
AppServiceRequestReceivedEventArgs args)
{
    ...
}
```

Когда ваше приложение UWP отправляет ответ обратно на ваше расширение, в него [`KeyValuePair`](https://msdn.microsoft.com/library/windows/apps/5tbh8a42) добавляется объект a `ValueSet` . `Key`Свойство будет игнорироваться Microsoft EDGE, но оно `Value` будет содержать допустимую строку JSON.

### Предусмотрен

Для обратных вызовов используется хром, [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) который позволяет функции обратного вызова обрабатывать любые асинхронные ответы от отправки сообщения.

Microsoft Edge использует [`AppServiceRequest`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appservicerequest) [`SendResponseAsync`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appservicerequest.sendresponseasync) метод объекта, чтобы приложение передавало [`ValueSet`](https://msdn.microsoft.com/library/windows/apps/dn636131) объекту обратное расширение.


### Предельный размер сообщения
Сообщения, которые отправляются между расширением и приложением, имеют разные ограничения на размер сообщений для Chrome и Microsoft Edge.

У Chrome есть следующие ограничения на размер сообщений:
- Ограничение на одно сообщение от собственного узла сообщений: 1 МБ
- Число однозначных сообщений, отправленных на собственный хост сообщений: 4 ГБ

В Microsoft EDGE, в то время как `AppService` ограничение на размер сообщения (зависит от памяти), Microsoft Edge защищает себя от некорректного поведения встроенных приложений, imposing следующие ограничения на размер сообщений.
- Ограничение на одно сообщение от приложения UWP к расширению: 1 МБ
- Ограничение на одно сообщение от расширения приложению UWP: 100 МБ



### Встроенные подключения к сообщениям

Существует два типа подключений для собственных сообщений. Постоянная и не постоянная.
**Постоянное** соединение — это подключение, которое выполняется до тех пор, пока порт не будет удален. **Непостоянное** соединение — это подключение, которое открывается для одного сообщения за один раз и закрывается после доставки.

#### Постоянные правила

Для Chrome постоянное подключение создается путем создания порта сообщений с помощью [`runtime.connectNative`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative) . После того как порт будет сделан, хром запускает собственный хост-процесс для сообщений, который продолжает выполняться до тех пор, пока не будет удален порт.

В Microsoft Edge после создания порта сообщения `runtime.connectNative` Microsoft Edge запускает [`AppServiceConnection`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appserviceconnection) и продолжает работу, пока порт не будет удален. В следующем фрагменте кода показано, как можно установить постоянное соединение в приложении UWP. 

```csharp
this.inventoryService = new AppServiceConnection();  
// Here, we use the app service name provided via the runtime.connectNative API  
this.inventoryService.AppServiceName = "com.microsoft.inventory";  
// Use the same Package Family Name as the extension package
this.inventoryService.PackageFamilyName = "replace with the Package Family Name";  
var status = await
this.inventoryService.OpenAsync();
```

#### Не постоянный

При отправке сообщения с помощью [`runtime.sendNativeMessage`](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/sendNativeMessage) Chrome без создания порта передачи данных хром запускает новый собственный хост-процесс для сообщений. Первое сообщение, созданное ведущим процессом, обрабатывается как ответ на первоначальный запрос, а все остальные сообщения после него пропускаются.

Microsoft Edge прекратит подключение после получения ответа от каждого сообщения. В следующем фрагменте кода показано непостоянное подключение, которое устанавливается вместе с ним, `AppServiceConnection` после получения запроса и его хранения в приложении UWP оно будет завершено [`AppServiceResponse`](https://msdn.microsoft.com/library/windows/apps/windows.applicationmodel.appservice.appserviceresponse) .

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

### Разрешение

Чтобы включить встроенную функцию обмена сообщениями в свое расширение, для Chrome и Microsoft Edge вам нужно объявить это `"nativeMessaging"` разрешение в `manifest.json` файле.


## Услуги для приложений
В этом разделе приведены сведения о том, что службы приложения влияют на встроенную производительность и память сообщений Microsoft Edge.

### Производительность

Службы приложений — это "спонсируемые" приложением переднего плана, вызывающие их, которые предназначены для собственных целей для обмена сообщениями — Microsoft Edge. Это означает, что службы приложений могут выполняться до тех пор, пока запущен Microsoft Edge.

С точки зрения задержки службы приложений используют именованные каналы, после первоначального подключения к ним можно напрямую общаться два приложения. Этот способ обмена данными обеспечивает слабую задержку. После запуска процесса, на котором размещается служба приложений (~ 80ms запускает фоновую задачу на некоторых устройствах), на устройствах с медленными процессорами будет возникать первая задержка. После запуска системы производительность на медленном устройстве ЦП должна быть хорошей. 


### Память
Память, выделенная службе приложений, берется из квоты, выделенной для Microsoft Edge. Это означает, что если Microsoft Edge запускает слишком много служб приложений, возможно, у них недостаточно памяти. Обычно в службах приложений применяются стандартные ограничения памяти фоновой задачи. Например, на устройстве с 512 МБ фоновая задача службы приложений не может быть больше 16 МБАЙТ. Этот номер будет увеличиваться при масштабировании устройств.


## Создание расширения с помощью собственного сообщения

Для проверки собственного обмена сообщениями необходимо, чтобы расширение имело имя семейства пакетов. Microsoft Edge использует это для определения идентификатора собственного узла сообщений, что означает, что расширение должно быть упаковано. 


Чтобы создать расширение с помощью встроенного обмена сообщениями в Visual Studio, выполните указанные ниже действия.

1. Создайте проект UWP в Visual Studio.
2. [Добавьте `AppService` в приложение UWP](https://msdn.microsoft.com/windows/uwp/launch-resume/how-to-create-and-consume-an-app-service).
   - При необходимости вы можете [настроить `AppService` размещение в главном приложении](https://msdn.microsoft.com/windows/uwp/launch-resume/convert-app-service-in-process) , а не в фоновой задаче на этом этапе.
3. Создание и тестирование проекта UWP.
   - При желании вы можете добавить [компонент "мост для настольных систем](#adding-a-desktop-bridge-component)".
4. Создайте расширение Microsoft EDGE, использующее собственный обмен сообщениями для общения с приложением UWP. Файлы расширений можно добавить в папку, указанную `Extension` в проекте UWP. Для всех файлов в этой папке, включая вложенные папки, необходимо настроить их свойства, чтобы `Build Action=Content` и `Copy to Output Directory=Copy Always` . Убедитесь `manifest.json` , что эти свойства также настроены.
5. Измените `package.manifest.xml` файл в проекте, чтобы включить в него метаданные расширения, и преобразуйте его в приложение без монитора, добавив `AppListEntry="none"` :

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

6. Используйте `AppService` имя, заданное для UWP в собственных API для обмена сообщениями.
7. Сборка и [развертывание](#deploying) проекта UWP (с дополнительным компонентом моста для настольных систем).
8. [Упаковка](#packaging) собственного расширения для обмена сообщениями после того, как оно будет готово к отправке в магазине

> [!NOTE]
> Ознакомьтесь с разделом [демонстрационные материалы](#demos) , чтобы получить пример встроенного расширения для обмена сообщениями.


## Добавление компонента Desktop Bridge 
Если вы хотите добавить в пакет компонент Desktop Bridge, вам потребуется создать и построить проект Win32 в Visual Studio. Сведения о том, как преобразовать приложение Win32 в UWP, можно найти в статье [Перенос приложений в Windows 10 через мост для настольных систем](/windows/uwp/porting/desktop-to-uwp-root). После того как вы выстроили в Visual Studio, вы можете добавить исполняемый файл Win32 в пакет, выполнив указанные ниже действия.

1. Добавьте проект Win32 в то же решение, что и проект UWP. 

2. Настройте проект Win32 как зависимый проект для проекта UWP.

    ![Настройка зависимостей проектов](./../media/project-dependencies.PNG)

3. Создайте `Win32` папку в проекте UWP. Скопируйте необходимые двоичные файлы `Win32` проекта в эту папку. Настройте свойства всех двоичных файлов так, чтобы `Build Action=Content` и `Copy to Output Directory=Copy Always` .

    ![папка с файлами приложения Win32 и UWP](./../media/desktop-bridge.png)

4. Измените файл проекта UWP, чтобы скопировать все необходимые двоичные файлы для `Win32` проекта в эту папку с помощью команды Event Build. Это гарантирует, что обновленные двоичные файлы копируются в папку каждый раз при перестроении решения.

    ```xml
    <Target Name="AfterBuild">
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.exe" DestinationFolder="win32" />
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.exe.config" DestinationFolder="win32" />
    <Copy SourceFiles="..\PasswordInputProtection\bin\$(Configuration)\PasswordInputProtection.pdb" DestinationFolder="win32" />
    </Target>
    ```


5. `package.manifest.xml`Для изменения добавьте `<desktop:Extension>` элемент в `<Extensions>` элемент:

    ```xml
    <Extensions>
    <desktop:Extension Category="windows.fullTrustProcess"Executable="Win32\PasswordInputProtection.exe"
    xmlns:desktop="http://schemas.microsoft.com/appx/manifest/desktop/windows10" />
    </Extensions>
    ```

## Развертывание
После того как вы настроили проект UWP (и, при необходимости, проект Win32) как описано выше, вы можете развернуть решение с помощью Visual Studio.

![проект "сборка, процесс сборки"](../media/native-message-uwp-debug.PNG)

После того как решение будет развернуто правильно, вы увидите расширение в Microsoft Edge.

![расширение, показанное в Microsoft Edge](../media/secureextension.png)

## Упакован

> [!NOTE]
> Отправка расширения Microsoft EDGE в Microsoft Store в настоящее время ограничена возможностями. [Поделитесь с нами](https://aka.ms/extension-request) с помощью ваших запросов на участие в Microsoft Store, и мы поможем вам ознакомиться с будущими обновлениями.


Вы можете создать пакет магазина для отправки в центр разработки для Windows с помощью встроенных функций Visual Studio:


![Создание пакета магазина](../media/create-store-package.PNG)

## Отладка
Инструкции по отладке зависят от того, какой компонент нужно протестировать.

### Отладка расширения
После развертывания решения расширение будет установлено в Microsoft Edge. Сведения о том, как отлаживать расширение, можно найти в руководстве по [отладке](./debugging-extensions.md) .


### Отладка приложения UWP
Приложение UWP запускается, когда расширение пытается подключиться к нему с помощью [собственных API для обмена сообщениями](https://developer.mozilla.org/Add-ons/WebExtensions/API/runtime/connectNative). Отладка приложения UWP должна выполняться только после запуска процесса. Это можно настроить с помощью страницы свойств проекта.

1.  В Visual Studio щелкните проект приложения UWP правой кнопкой мыши
2.  Выберите свойства
3.  Флажок "не запускать, но выполнять отладку моего кода при запуске"

    ![Установка флажка "не запускать"](../media/native-message-do-not-launch.png)

В Visual Studio теперь можно установить точки останова в коде, в котором нужно выполнить отладку, а затем запустить отладчик, нажав клавишу F5. После того как вы взаимодействуете с расширением для подключения к приложению UWP, Visual Studio будет автоматически присоединиться к этому процессу.


### Отладка настольного моста
Несмотря на то что существуют различные [методы для отладки моста для настольных систем](https://msdn.microsoft.com/windows/uwp/porting/desktop-to-uwp-debug) (преобразованного приложения Win32), единственным применимым для этих сценариев является параметр PLMDebug. Вы также можете добавить отладочный код в функцию Startup для выполнения ожидания в течение определенного времени, позволяя присоединить Visual Studio к процессу.
