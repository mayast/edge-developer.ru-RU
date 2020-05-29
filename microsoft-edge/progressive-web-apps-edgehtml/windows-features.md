---
description: Расширение возможностей PWA для Windows с помощью собственных функций приложения
title: Адаптация PWA для Windows
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/22/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: прогрессивные веб-приложения, PWA, EDGE, Windows, WinRT, UWP, EdgeHTML
ms.openlocfilehash: 5bad708db5b13517fd1887214a5e1d5457796ee2
ms.sourcegitcommit: e07de36ee9fbe20422ffc2c62b98839851e1b02b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2020
ms.locfileid: "10604013"
---
# Адаптация PWA (EdgeHTML) для Windows  

PWAs, установленный в Windows 10, обладает [всеми преимуществами][PwaIndexWindows10] работы в качестве приложений [универсальной платформы Windows (UWP)][WindowsUWPGetStartedGuide] , включая защиту через изолированную платформу приложения для Windows и полный доступ к API [среды выполнения Windows \ (WinRT \))][UwpApiIndex] , в том числе следующие:  

*   Управление функциями устройства (например, Камера, микрофон, GPS)  
*   Доступ к пользовательским ресурсам \ (например, календарь, контакты, документы, музыка и т. д.)  
*   Запуск и Навигация в приложении с помощью голосовых команд Кортаны  
*   Интеграция с ОС Windows \ (через центр уведомлений Windows, панель задач для настольных компьютеров и контекстные меню \)  

... и это лишь некоторые из добавленных возможностей для PWA \ (EdgeHTML \) в Windows!  

В этом руководстве описано, как установить, запустить и усовершенствовать приложение PWA \ (EdgeHTML \) в Windows 10, а также обеспечить совместимость между браузерами и разными платформами.  

## Предварительные условия  

*   Существующий веб-сайт PWA \ (или размещенное приложение) — либо на сайте Live, либо на localhost.  В этом руководстве для [начала работы с прогрессивными веб-приложениями][PwaGetStarted]используется образец PWA.  
*   Скачайте (бесплатное) [Visual Studio Community 2017][MicrosoftVisualStudio|::ref1::|].  Вы также можете использовать выпуски профессионального выпуска, Enterprise или [Preview][MicrosoftVisualStudioPreview] .  В установщике Visual Studio выберите указанные ниже рабочие нагрузки.  
    *   **Разработка универсальной платформы Windows**  

## Настройка и выполнение универсального приложения для Windows  

PWA \ (EdgeHTML \), установленный как приложение Windows 10, запускается независимо от браузера, в отдельном окне \ ( `WWAHost.exe` процесс).  Для этого просто требуется упрощенная оболочка приложения, содержащая размещенное веб-приложение, которое вы можете быстро настроить с помощью `Progressive Web App (Universal Windows)` шаблона проекта Visual Studio.  \ (Все ваши логики приложения, включая отправку запросов API среды выполнения Windows, по-прежнему выполняются в исходном коде веб-приложения.)  

Настройка среды разработки приложений для Windows в Visual Studio.  

1.  В параметрах Windows включите [режим разработчика][WindowsUWPGetStartedEnable].  \ (Введите `developer mode` в searchbar Windows, чтобы найти его. \)  
1.  Запустите Visual Studio и **Создайте новый проект..** .  
1.  Выберите шаблон **проект упаковки приложений для Windows** на C#.  Если вы используете предыдущую версию Visual Studio, найдите соответствующий шаблон в разделе **размещенное веб-приложение (универсальные приложения для Windows)** или **прогрессивное веб-приложение (универсальные приложения для Windows)**.  
1.  Выберите по умолчанию Windows 10 `Target version` \ (самый последний выпуск \) и `Minimum version` \ (сборка 10586 или более поздняя) и нажмите кнопку **ОК**.  

    ![Диалоговое окно "выбор" в Visual Studio для сборок целевых объектов проекта UWP](media/vs-target-min-version.png)  

    Новый проект загружается с открытым конструктором Package. appxmanifest.  Здесь вы настраиваете сведения о приложении, в том числе удостоверение пакета, зависимости пакетов, необходимые возможности, визуальные элементы и точки расширения.  Это легко настраиваемая временная версия манифеста пакета приложения, используемая во время разработки приложения.  
    При построении проекта приложения [Visual Studio создает файл AppxManifest. XML][UwpSchemasAppxpackageUapmanifestschemaGeneratePackageManifest] из этих метаданных, который используется для установки и запуска приложения.  Когда вы обновляете `package.appxmanifest` файл, не забудьте перестроить проект, чтобы оба были отражены во `AppxManifest.xml` время выполнения.  

1.  На панели **приложения** в конструкторе манифестов введите URL-адрес PWA `Start page` .

    > [!NOTE]
    > Сотрудники служб поддерживаются для всех URL-адресов HTTPS \ (Secure, Remote), указанных в `StartPage` .  Сотрудники служб не поддерживаются по умолчанию для веб-приложений, задающих локальную начальную страницу.  Чтобы включить поддержку обслуживания сотрудников для этих случаев, добавьте в манифест явную запись [ApplicationContentUriRules](#set-application-content-uri-rules-acurs) , например: `<uap:Rule Match="http://web-platform.test/" Type="include" uap5:ServiceWorker="true"/>`  
    
    ![Панель приложения в конструкторе Package. appxmanifest](media/vs-manifest-application.png)  
    
    Вы можете изменить и то, `Display name` и другое `Description` .  
1.  Сохраните этот файл \ (или другой 512x512 изображение вашего выбора \) на рабочем столе.  
    Затем на панели **визуальные ресурсы** конструктора манифестов нажмите кнопку `Source` поле **...** , выберите ее в качестве исходного файла и нажмите кнопку **создать**.  \ (Затем нажмите кнопку **ОК** , чтобы перезаписать изображения заполнителей по умолчанию \).  
    
    ![Панель "визуальные ресурсы" в конструкторе Package. appxmanifest](media/vs-manifest-visual-assets.png)  
    
    Это создаст основные визуальные ресурсы для установки, запуска, запуска и распространения вашего приложения в магазине.  
    Если отображаются красные ошибки \ ( `X` \), указывающие на отсутствие изображений, вы можете нажать кнопку ". **..** ", чтобы вручную выбрать файл из созданных изображений.  
1.  На панели **URI содержимого** конструктора манифестов замените на `http://example.com` расположение вашего PWA (например, `Rule`  =  `include` `WinRT Access`  =  `All` "\").  
    Таким образом, вы предоставляете разрешение на доступ к приложению PWA для отправки запросов API для встроенной среды выполнения Windows (WinRT) при запуске в качестве приложения Windows 10, которое рассматривается чуть позже.   Если для вашего фактического доступа к приложению PWA не требуется доступ WinRT, вы можете переключить `WinRT Access` значение на `None` .  В обоих случаях не забудьте вывести строку по умолчанию `http://example.com` с URI для PWA или ваше приложение не сможет правильно загрузиться во время выполнения.  
    Вы готовы запускать и отлаживать PWA как приложение для Windows 10.  Если вы используете сайт localhost для перехода по этому руководству, убедитесь, что он запущен.  Затем  
1.  Выполните сборку \ ( `Ctrl` + `Shift` + `F5` \) и запустите \ ( `F5` \) проект PWA.  После этого ваш веб-сайт должен быть запущен в отдельном окне приложения.  Это размещенное веб-приложение. оно запущено в виде последовательного веб-приложения, установленного в Windows 10!  

    ![PWA запускается в окне WWAHost. exe](media/wwahost.png)  

## Отладка PWA \ (EdgeHTML \) как приложение для Windows  

Поскольку PWA \ (EdgeHTML \) — это просто последовательное, а размещенное веб-приложение, вы можете выполнять отладку кода на стороне сервера так же, как и любое веб-приложение, используя обычную среду IDE и рабочий процесс.  Изменения, которые вы разработали в режиме реального времени, будут отражены в установленном приложении Project Web App при следующем запуске (не требуется повторное развертывание универсального пакета приложения для Windows).

Для отладки на стороне клиента в приложении для Windows 10 необходимо `Microsoft Edge DevTools Preview` приложение.  Это автономное приложение включает все возможности исходного браузера [Microsoft Edge DevTools][DevToolsGuide] \ (в том числе [средств PWA][DevToolsGuideServiceWorkers]), а также основную поддержку [удаленной отладки][DevToolsProtocol01ClientsEdgePreview] и средство [выбора отладочной][DevToolsGuideMicrosoftStoreApp] версии для присоединения к любому запущенному экземпляру обработчика EdgeHTML, в том числе надстроек для Office, кортаны, веб-представлений приложений и, конечно же, PWAs запущено в Windows.  

Вот как можно настроить отладку для PWA \ (EdgeHTML \).  

1.  Установите приложение [Microsoft Edge DevTools Preview][MicrosoftStoreEdgeDevtoolsPreview] из магазина Microsoft Store, если оно еще не установлено.  
1.  Запустив веб-сайт PWA и запускайте приложение DevTools.  
1.  В Visual Studio запустите приложение Windows 10 с помощью `Start Without Debugging` `Ctrl` + `F5` команды ().  \ (Приложение DevTools не прикрепляется должным образом, если активен отладчик Visual Studio. \)  
1.  В приложении DevTools нажмите кнопку **Обновить** в локальной версии средства выбора целевых объектов отладки.  Теперь должен быть указан сайт PWA \ (EdgeHTML \).  \ (Если он также работает в окне браузера, это последний экземпляр этого сайта в списке. \)  
1.  Щелкните ссылку на веб-сайт PWA \ (EdgeHTML \), чтобы открыть новую вкладку экземпляра DevTools и начать отладку.  
    
    ![Средство выбора локальных целей отладки в приложении Microsoft Edge DevTools](media/devtools-local.png)  
    
1.  Вы можете проверить, что DevTools присоединен к веб-приложению PWA, запущенному под управлением Windows.  На **консоли**DevTools введите:  
    
    ```shell
    window.Windows
    ```  
    
    Это возвращает глобальный `Windows Runtime` объект, содержащий все [пространства имен WinRT верхнего уровня](#find-windows-runtime-winrt-apis).  Это ваша входная точка PWA \ (EdgeHTML \) для [универсальной платформы Windows][WindowsUWPIndex], доступная только для веб-приложений, которые выполняются в приложениях Windows 10 (в процессе, запущенном за пределами браузера `WWAHost.exe` ).  
    
## Поиск API-интерфейсов среды выполнения Windows \ (WinRT \)  

Как установленное приложение для Windows, класс [PWA \ (EdgeHTML \) имеет полный доступ к встроенным API среды выполнения Windows][WindowsRuntime]. Определение необходимых данных, получение разрешений для реквизитов и использование функции обнаружения функций для отправки запроса API в поддерживаемых средах.  Пошаговые инструкции по добавлению последовательного расширения для пользователей классического приложения для Windows для настольных систем.  

Существует несколько способов идентификации API универсальной платформы Windows, необходимых для работы с Windows PWA, в том числе поиск в обширных [документах UWP в центре разработки для Windows] [UWP/API/], скачивание и запуск [примеров кода UWP](#uwp-code-samples) в Visual Studio, а также просмотр фрагментов кода для распространенных задач для PWAs в Windows.

Существует несколько способов идентификации API универсальной платформы Windows, которые необходимы для работы с Windows PWA, в том числе поиск в обширных [документах UWP в центре разработки для Windows] [UWP/API/], скачивание и запуск [примеров кода UWP](#uwp-code-samples) в Visual Studio, а также просмотр фрагментов кода для распространенных задач для [PWAs в Windows 10 (EdgeHTML)][PwaIndexWindows10].  

Общие API-интерфейсы WinRT работают в JavaScript так же, как и в C#, поэтому вы можете использовать общие сведения о [платформе универсальной платформы Windows][WindowsUWPIndex] и [Справочник по API-интерфейсам][UwpApiIndex] для использования.  Однако обратите внимание на указанные ниже отличия.  

*   Для функций WinRT в JavaScript используются [различные соглашения о регистре][ScriptingJsinrtUsingWinRTCasingConventions]  
*   [События представлены в виде строковых идентификаторов][ScriptingJsinrtHandlingWinRTEvents] , передаваемых `addEventListener` / `removeEventListener` методам класса.  
*   [Асинхронные методы][ScriptingJsinrtUsingWinRT] используют модель Promise для JavaScript  
*   API-интерфейсы в `Windows.UI.Xaml` пространстве имен не поддерживаются для приложений JavaScript, которые вместо этого используют стек [EdgeHTML][DevGuideWhatsNew] модуля подготовки к просмотру \ (HTML, CSS \).  

Дополнительные сведения можно найти [в разделе Использование среды выполнения Windows в JavaScript][WindowRuntimeUsingJavascript].  

### Примеры кода UWP  

В репозитории [примеров универсальной платформы Windows (UWP)][MicrosoftDeveloperWindowsSamples] можно найти примеры кода JavaScript для распространенных сценариев приложений для Windows 10.  Несмотря на то, что в JS-версиях этих примеров используется библиотека [WinJS][GithubWinjsWinjs] для структурирования шаблона, WinJS не требуется для отправки запросов API WinRT, которые демонстрируются в этих примерах.  

> [!NOTE]
> Если необходимо прослушать [`activated`][UwpApiWindowsUiWebuiWebapplicationActivated] событие для приложения, вы можете сделать это с помощью следующего собственного API WinRT.  
> 
> **Используйте этот**  
> 
> ```javascript
> Windows.UI.WebUI.WebUIApplication.addEventListener("activated", function (activatedEventArgs) {
>     // Check activatedEventArgs.kind and respond as needed
> });
> ```  
> 
> ... в отличие от этого типа WinJS запроса, используемого в примерах:  
> 
> **Это не так**  
> 
> ```javascript
>     var page = WinJS.UI.Pages.define("/html/scenario1-launched.html", {
>         ready: function (element, options) {
>             // Check options.activationKind and respond as needed
>         }
>     });
> ```  

## Отправка запросов API WinRT из PWA (EdgeHTML)  

На этом этапе вы хотите добавить настраиваемое контекстное меню для пользователей Windows на веб-странице PWA \ (EdgeHTML \) и определить необходимые API в пространстве имен [Windows. UI. popups][UwpApiWindowsUiPopups] .  

Чтобы отправить любые запросы API WinRT из нашего PWA \ (EdgeHTML \), необходимо сначала [установить разрешения реквизитов](#set-application-content-uri-rules-acurs) \ (или правила URI содержимого приложения \) в файле манифеста пакета приложения Windows \ ( `.appxmanifest` \).  

Если какой-либо из этих запросов API включает доступ к пользовательским ресурсам, например изображениям и музыке, или к функциям устройств, таким как камера или микрофон, необходимо также добавить [объявления возможностей приложения](#app-capability-declarations) в манифест пакета приложения, чтобы Windows предложит пользователю разрешение.  Если позже вы опубликуете PWA \ (EdgeHTML \) в Microsoft Store, такие разрешения на [доступ к приложениям][MicrosoftSupportWindowsAppPermissions] также будут указаны в вашем списке в магазине.  

#### Настройка правил URI содержимого приложения (Acur)  

С помощью Acur, в противном случае называемого списком разрешенных URL-адресов, вы можете предоставить URL-адреса для прямого доступа к API PWA \ (EdgeHTML \) в интерфейсах среды выполнения Windows.  На уровне операционной системы Windows права на доступ к интерфейсу API платформы разрешаются с помощью кода, размещенного на веб-сервере.  Вы определяете эти границы в файле манифеста пакета приложения, когда вы указываете URL-адреса PWA как `ApplicationContentUriRules` .  

Правила должны включать начальную страницу для вашего приложения и другие страницы, которые нужно добавить в качестве страниц приложения.  Если пользователь переходит по URL-адресу, который не входит в правила, Windows открывает целевой URL-адрес в браузере Microsoft EDGE, а не в отдельном окне PWA \ ( `WWAHost.exe` процесс \).  Вы также можете исключить конкретные URL-адреса.  

Указать URL-адрес `Match` в правилах можно несколькими способами.  

*   Точное имя узла  
*   Имя узла, для которого включен или исключен универсальный код ресурса (URI) со всеми поддоменами этого имени узла  
*   Точный URI  
*   Точный URI, содержащий свойство запроса  
*   Частичный путь и подстановочный знак для указания конкретного расширения файлов  
*   Относительные пути для правил исключения  

Вот несколько примеров Acur в `.appxmanifest` файле:  

```xml
<Application
Id="App"
StartPage="https://contoso.com/home">
<uap:ApplicationContentUriRules>
    <uap:Rule Type="include" Match="https://contoso.com/" WindowsRuntimeAccess="all" />
    <uap:Rule Type="include" Match="https://*.contoso.com/" WindowsRuntimeAccess="all" />
    <uap:Rule Type="exclude" Match="https://contoso.com/excludethispage.aspx" />
</uap:ApplicationContentUriRules>
```  

URL-адреса, определенные в Acur для вашего приложения, могут предоставлять доступ к среде выполнения Windows с помощью `WindowsRuntimeAccess` атрибута, принимающего следующие значения:  

*   `all`: Удаленный код JavaScript имеет доступ ко всем API-интерфейсам WinRT и локальным пакетным компонентам.  В обработчике сценария будет вставлено пространство имен [Windows \ (WinRT \))][UwpApiIndex] .  
*   `allowForWeb`: Удаленный доступ к коду JavaScript ограничен локальными пакетными компонентами, включая пользовательские компоненты C++/C #.  
*   `none`По умолчанию.  Указанный URL-адрес не получает доступ к платформе.  

В этом учебнике вы уже задали единственный ACUR, который вам нужен (шаг 6 предыдущей [настройки и запуск вашего раздела приложения](#set-up-and-run-your-universal-windows-app) ) для вашего приложения на основе одной страницы.  Вы можете подтвердить это с помощью панели **URI содержимого** в `package.appxmanifest` конструкторе Visual Studio.  

![Панель URI содержимого в конструкторе appxmanifest Visual Studio](media/vs-appxmanifest-editor-acurs.png)  

Вы также можете просмотреть необработанный XML-файл манифеста, щелкнув его правой кнопкой мыши `package.appxmanifest` в обозревателе решений Visual Studio и выбрав команду **Просмотреть код** \ ( `F7` \).  Чтобы вернуться в режим конструктора, нажмите кнопку **Конструктор представлений** \ ( `Shift` + `F7` \).  

#### Объявления возможностей приложения  

Если вашему приложению требуется программный доступ к пользовательским ресурсам, например изображениям и музыке, или к устройствам, таким как камера или микрофон, необходимо включить соответствующие [объявления возможностей приложения][WindowsUwpPackagingAppCapabilities] в файл манифеста пакета приложения.  Ниже приводятся три категории объявления возможностей приложения.  

*   [Возможности общего применения][WindowsUwpPackagingAppCapabilitiesGeneralUse], которые используются в большей части сценариев приложений.  
*   [Возможности устройства][WindowsUwpPackagingAppCapabilitiesDevice], которые позволяют вашему приложению получать доступ к периферийным и внутренним устройствам.  
*   [Специальные возможности][WindowsUwpPackagingAppCapabilitiesSpecialRestricted] , поддерживающие сценарии предприятий и требующие использования учетной записи компании Microsoft Store.  Подробнее об учетных записях компаний см. в разделе [Типы, доступность и стоимость учетных записей][WindowsUwpPublishAccountTypesLocationsFees].

На странице приложения Microsoft Store перечислены все возможности, объявленные в манифесте пакета приложения, поэтому не забудьте указать только те возможности, которые используются приложением в действительности.

Некоторые возможности предоставляют приложениям доступ к конфиденциальным ресурсам.  Эти ресурсы считаются конфиденциальными, так как каждый из них может получить доступ к личным данным пользователя или стоить пользователю денег.  Параметры конфиденциальности, управляемые приложением " [Параметры][BingResultsWindows10Settings] " для Windows 10, позволяют пользователю динамически управлять доступом к конфиденциальным ресурсам.  Таким образом, важно, чтобы приложение не считало конфиденциальные ресурсы всегда доступными.  Подробнее о доступе к конфиденциальным ресурсам см. в разделе [Руководство по приложениям, учитывающим требования конфиденциальности][WindowsUwp|::ref2::|Index].  

Вы запрашиваете доступ, объявляя возможности в манифесте пакета для вашего приложения.  В Visual Studio вы можете сделать это на панели " **возможности** " конструктора Package. appxmanifest.  

![Панель "возможности" в конструкторе appxmanifest Visual Studio](media/vs-appxmanifest-editor-capabilities.png)  

В этом учебнике требуется только возможность использования по умолчанию для Интернет-(клиент \), поэтому дальнейших действий не требуется.  

### Использование функции обнаружения компонентов для вызова WinRT  

Чтобы обеспечить оптимальное качество для аудитории PWA на всех платформах, вы можете усовершенствовать интерфейс PWA в Windows с помощью обнаружения компонентов WinRT.  Таким образом, вы можете убедиться, что ваш код для Windows работает только в контексте, в котором доступны и применимы API-интерфейсы WinRT.  

Обнаружение компонентов может быть таким же простым, как поиск `Windows` объекта \ (точка входа в [пространство имен WinRT][UwpApiIndex]\), как показано ниже.  

```javascript
if(window.Windows){
    /*Run code that sends Windows API requests */
}
```  

Тем не менее, если все интерфейсы API Windows доступны не на всех [типах устройств Windows 10][UwpExtensionSdkDeviceFamiliesOverview], лучше квалифицировать пространство имен запроса API, которое вы отправляете, с помощью более детального определения функций.  

```javascript
if(window.Windows && Windows.Media.SpeechRecognition){
    /*Run code that sends Windows API requests */
}
```  

С помощью этого фона вы можете добавить некоторый код WinRT для реализации настраиваемого контекстного меню.  Если вы используете образец PWA [для начала работы с прогрессивными веб-приложениями][PwaGetStarted], выполните указанные ниже действия.

1.  Откройте Visual Studio для проекта сайта PWA.

1.  В обозревателе решений откройте `views\layout.pug` файл и добавьте следующую строку прямо ниже `script` ссылки для сотрудника службы:
    
    ```xml
    script(src='/javascripts/site.js')
    ```  

1.  В обозревателе решений щелкните правой кнопкой мыши `javascripts` папку и выберите команду **Добавить**  >  **новый файл..**..

1.  Присвойте файлу имя: `site.js` и скопируйте его в следующем коде:
    
    ```javascript
    if (window.Windows && Windows.UI.Popups) {
        document.addEventListener('contextmenu', function (e) {

            // Build the context menu
            var menu = new Windows.UI.Popups.PopupMenu();
            menu.commands.append(new Windows.UI.Popups.UICommand("Option 1", null, 1));
            menu.commands.append(new Windows.UI.Popups.UICommandSeparator);
            menu.commands.append(new Windows.UI.Popups.UICommand("Option 2", null, 2));

            // Convert from webpage to WinRT coordinates
            function pageToWinRT(pageX, pageY) {
                var zoomFactor = document.documentElement.msContentZoomFactor;
                return {
                    x: (pageX - window.pageXOffset) * zoomFactor,
                    y: (pageY - window.pageYOffset) * zoomFactor
                };
            }

            // When the menu is invoked, execute the requested command
            menu.showAsync(pageToWinRT(e.pageX, e.pageY)).done(function (invokedCommand) {
                if (invokedCommand !== null) {
                    switch (invokedCommand.id) {
                        case 1:
                            console.log('Option 1 selected');
                            // Invoke code for option 1
                            break;
                        case 2:
                            console.log('Option 2 selected');
                            // Invoke code for option 2
                            break;
                        default:
                            break;
                    }
                } else {
                    // The command is null if no command was invoked.
                    console.log("Context menu dismissed");
                }
            });
        }, false);
    }
    ```

1.  Сравните поведение контекстного меню при запуске PWA в браузере \ ( `F5` из проекта сайта PWA) и в окне приложения Windows \ ( `F5` из проекта универсального приложения для Windows).  При щелчке правой кнопкой мыши в браузере появляется контекстное меню Microsoft Edge по умолчанию, в то время как в `WWAHost.exe` процессе вы можете открыть свое пользовательское меню.  

    | Microsoft Edge | Приложение для Windows 10 |  
    |:--- |:---- |  
    | ![Контекстное меню браузера по умолчанию](media/browser-context-menu.png) | ![Настраиваемое контекстное меню приложения](media/app-context-menu.png) |  

Будем надеяться, что теперь у вас есть надежная основа для постепенного совершенствования PWAs в Windows.  Если вы столкнулись с вопросами или что-то еще не понятно, пожалуйста, отправьте комментарий.  

## Дальнейшая работа

[Центр разработки для Windows][MicrosoftDeveloperWindowsApps] — это полный справочник по всем этапам здания приложений для Windows, от [начала работы][MicrosoftDeveloperWindowsAppsGetStarted]до [проектирования][MicrosoftDeveloperWindowsAppsDesign], [разработки][MicrosoftDeveloperWindowsAppsDevelop]и [публикации][MicrosoftDeveloperStorePublishApps] в Microsoft Store.  

Общие сведения о платформе универсальной платформы Windows (UWP) и о том, как ориентироваться на различные семейства устройств для Windows 10, приведены в статье [Введение для универсальной платформы Windows][WindowsUWPGetStartedGuide].  

Когда вы будете готовы, вот как \ (и почему! \) можно [Отправить PWA в Microsoft Store](./microsoft-store.md).  

<!-- image links -->  

<!-- links -->  

[PwaGetStarted]: ./get-started.md "Приступите к работе с прогрессивными веб-приложениями"  
[PwaIndexWindows10]: ./index.md#pwas-on-windows-10-edgehtml "PWAs в Windows 10 (EdgeHTML) — прогрессивные веб-приложения для Windows"  
[DevToolsGuide]: ../devtools-guide.md "Инструменты разработчика Microsoft EDGE (EdgeHTML)"  
[DevToolsGuideMicrosoftStoreApp]: ../devtools-guide.md#microsoft-store-app "Microsoft Store App-Microsoft EDGE (EdgeHTML) Tools Developer"  
[DevToolsGuideServiceWorkers]: ../devtools-guide/service-workers.md "Обслуживание сотрудников"  
[DevToolsProtocol01ClientsEdgePreview]: ../devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Клиенты Microsoft Edge DevTools Preview-DevTools Protocol"  
[DevGuideWhatsNew]: ../dev-guide/whats-new.md "Новые возможности EdgeHTML"  
[WindowsRuntime]: ../windows-runtime/index.md "Среда выполнения Windows (WinRT) для JavaScript"  
[WindowRuntimeUsingJavascript]: ../windows-runtime/using-the-windows-runtime-in-javascript.md "Использование среды выполнения Windows в JavaScript"  

[ScriptingJsinrtHandlingWinRTEvents]: /scripting/jswinrt/handling-windows-runtime-events-in-javascript "Обработка событий среды выполнения Windows в JavaScript"  
[ScriptingJsinrtUsingWinRT]: /scripting/jswinrt/using-windows-runtime-asynchronous-methods "Использование асинхронных методов среды выполнения Windows"  
[ScriptingJsinrtUsingWinRTCasingConventions]:  /scripting/jswinrt/using-the-windows-runtime-in-javascript#casing-conventions-with-windows-runtime-features "Соглашения с прописными буквами в функциях среды выполнения Windows — использование среды выполнения Windows в JavaScript"  
[UwpApiIndex]: /uwp/api/index "Пространства имен Windows UWP"  
[UwpApiWindowsUiPopups]: /uwp/api/windows.ui.popups "Пространство имен Windows. UI. popups"  
[UwpApiWindowsUiWebuiWebapplicationActivated]: /uwp/api/windows.ui.webui.webuiapplication.activated "Событие WebUIApplication. Activated"  
[UwpExtensionSdkDeviceFamiliesOverview]: /uwp/extension-sdks/device-families-overview "Общие сведения о семействах устройств"  
[UwpSchemasAppxpackageUapmanifestschemaGeneratePackageManifest]: /uwp/schemas/appxpackage/uapmanifestschema/generate-package-manifest "Создание манифеста пакета приложения в Visual Studio"  
[WindowsUWPIndex]: /windows/uwp/index "Документация по универсальной платформе Windows"  
[WindowsUWPGetStartedGuide]: /windows/uwp/get-started/universal-application-platform-guide "Что такое приложение универсальной платформы Windows (UWP)?"  
[WindowsUWPGetStartedEnable]: /windows/uwp/get-started/enable-your-device-for-development "Активация устройства для разработки"  
[WindowsUwpSecurityIndex]: /windows/uwp/security/index "Разрешения"  
[WindowsUwpPublishAccountTypesLocationsFees]: /windows/uwp/publish/account-types-locations-and-fees "Типы счетов, места и сборы"  
[WindowsUwpPackagingAppCapabilitiesSpecialRestricted]: /windows/uwp/packaging/app-capability-declarations#special-and-restricted-capabilities "Ограниченные возможности"  
[WindowsUwpPackagingAppCapabilitiesDevice]: /windows/uwp/packaging/app-capability-declarations#device-capabilities "Возможности устройства"  
[WindowsUwpPackagingAppCapabilitiesGeneralUse]: /windows/uwp/packaging/app-capability-declarations#general-use-capabilities "Возможности общего использования"  
[WindowsUwpPackagingAppCapabilities]: /windows/uwp/packaging/app-capability-declarations "Объявления возможностей приложения"  

[BingResultsWindows10Settings]: https://binged.it/2lOGSH0 "Параметры Windows 10 — Bing"  
[GithubWinjsWinjs]: https://github.com/winjs/winjs "WinJS/WinJS | GitHub"  
[MicrosoftDeveloperStorePublishApps]: https://developer.microsoft.com/store/publish-apps/index "Публикация приложений и игр для Windows"  
[MicrosoftDeveloperWindowsApps]: https://developer.microsoft.com/windows/apps/index "Документация по универсальной платформе Windows"  
[MicrosoftDeveloperWindowsAppsDesign]: https://developer.microsoft.com/windows/apps/design/index "Проектирование и кодирование приложений для Windows"  
[MicrosoftDeveloperWindowsAppsDevelop]: https://developer.microsoft.com/windows/apps/develop/index "Разработка приложений UWP"  
[MicrosoftDeveloperWindowsAppsGetStarted]: https://developer.microsoft.com/windows/apps/getstarted/index "Начало работы с приложениями для Windows 10"  
[MicrosoftDeveloperWindowsSamples]: https://developer.microsoft.com/windows/samples "Примеры кода"  
[MicrosoftStoreEdgeDevtoolsPreview]: https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj "Предварительная версия DevTools Microsoft Edge"  
[MicrosoftSupportWindowsAppPermissions]: https://support.microsoft.com/help/10557/windows-10-app-permissions "Разрешения для приложений"  
[MicrosoftVisualStudioDownloads]: https://visualstudio.microsoft.com/downloads "Загрузки"  
[MicrosoftVisualStudioPreview]: https://visualstudio.microsoft.com/vs/preview "Предварительная версия Visual Studio"  
