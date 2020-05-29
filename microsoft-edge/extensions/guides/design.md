---
description: Узнайте о различных аспектах проектирования и поведении пользовательского интерфейса, которые следует принимать во время создания расширений Microsoft Edge.
title: Расширения-проектирование
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/08/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: EDGE, веб-разработка, JavaScript, дизайн, значки, разработчик
ms.openlocfilehash: 622d72453ea3ecd2897efcf8f67e1b2aa7a0937c
ms.sourcegitcommit: da768193c7ae7b611f4fbb1746f16d9818e42bac
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/28/2020
ms.locfileid: "10684066"
---
# Рекомендации по проектированию для расширений Microsoft Edge  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

На следующей странице содержатся различные аспекты проектирования и поведение пользовательского интерфейса, которые следует принимать во время создания расширений Microsoft Edge.  

## Значки  

С помощью векторного рисунка вы должны сделать значки расширения.  Чтобы упаковать расширение, вы должны создать несколько разных размеров вашего значка и еще три дополнительных размера.  Расширения Microsoft EDGE не поддерживают значки в формате SVG.  

Перед созданием значков расширений следует ознакомиться с руководством по [специальным возможностям][ExtensionsGuidesAccessibility] , чтобы убедиться в том, что значки обладают достаточной контрастностью и отображаются как в светлых, так и в темных темах Microsoft Edge.  

Несмотря на то, что поддерживается любой формат изображения WebKit, рекомендуется использовать значки PNG для поддержки прозрачности.  

### Значки для расширения  

Для расширения вы должны создать один размер значка для действия в браузере или действие страницы, а также один размер значка для области **расширений** .  Для поддержки дисплеев высокого разрешения может быть предусмотрено более одного размера каждого из них.  

Расширение должно иметь значок действия браузера или действия страницы.  При использовании метода [browserAction. setIcon][MSDApiBrowseractionSeticon] или [pageAction. setIcon][MDNApiPageactionSeticon] можно изменить значки действий со страницами и действиями в браузере.  

#### Действие браузера  

Предпочтительные размеры для значков действий браузера и действия страницы:, `20px` `25px` `30px` и `40px` .  Другие поддерживаемые размеры включают `19px` в себя, `35px` и `38px` .  

В следующем фрагменте файла [manifest. JSON][ExtensionsApisupportManifestkeys] показан стандарт и значок действия браузера High Definition, который задается с помощью ключа [browser_action][MDNManifestjsonBrowserAction] .  Тот же синтаксис применяется для ключа [page_action][MDNManifestjsonPageAction] .  

```json
"browser_action": {
    "default_icon": {
        "20": "images/icon_20.png",
        "40": "images/icon_40.png"
    },
    "default_title": "Fetch page info",
    "default_popup": "popup.html"
}
```  

Если действие браузера было установлено с помощью расширения, оно появляется либо в меню действия после выбора команды **Дополнительно (...)**, либо справа от адресной строки, если пользователь отключил **кнопку Показать рядом с адресной строкой** .  

:::row:::
   :::column span="1":::
      :::image type="complex" source="../media/actionmenu-browseraction.png" alt-text="Действие браузера в меню "действие"":::
         Действие браузера в меню "действие" :::image-end:::
      
      <!--![browser action in action menu][ImageActionmenuBrowseraction]  -->  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="../media/browseractionicon.png" alt-text="Действие браузера":::
         Действие браузера :::image-end:::
      
      <!--![browser action][ImageBrowserActionIcon]  -->  
   :::column-end:::
:::row-end:::

#### Действие страницы  

Ключ [page_action][MDNManifestjsonPageAction] имеет тот же синтаксис МАНИФЕСТа JSON, что и ключ [browser_action][MDNManifestjsonBrowserAction] .  Действие страницы также имеет те же требования к размеру значка, что и действие браузера.  

Если в файле [manifest. JSON][ExtensionsApisupportManifestkeys] задано действие Page, оно отображается в адресной строке всякий раз, когда используется метод [pageAction. Show][MDNApiPageactionShow] .  

:::image type="complex" source="../media/pageaction.png" alt-text="Действие страницы":::
   Действие страницы
:::image-end:::

<!--![page action][ImagePageaction]  -->  

##### Пользовательский интерфейс управления  

Когда пользователь переходит на панель расширений, переходя к меню **Дополнительно (...)** , и выбирая **расширения**, рядом с названием расширения отображается значок.  

Вы должны указать следующие размеры значков.  

| Раздел | Сведения |  
|:--- |:--- |  
| `48px` | Значок стандартного разрешения на экран. |  
| `128px` | Значок для дисплеев с высоким разрешением. |  
| `176px` | Значок для отображения еще более высокое разрешение экрана. |  


```json
"icons": {
    "48": "images/icon_48.png",
    "128": "images/icon_128.png",
    "176": "images/icon_176.png"
},
```  

:::image type="complex" source="../media/management-ui.png" alt-text="Пользовательский интерфейс управления":::
   Пользовательский интерфейс управления
:::image-end:::

<!--![management UI][ImageManagementUi]  -->  

### Значки для упаковки  

После того как ваше расширение будет готово к упаковке, вы должны иметь три дополнительных размера значков.  

| Size | Сведения |  
|:--- |:--- |  
| 44px | Используется в пользовательском интерфейсе Windows \ (**список приложений** **,**  \>  приложения**системы**  \>  **& функций**). |  
| 50px | Требования к пакетированию (не отображаются в любом месте). |  
| 150px | Используется в качестве значка для Microsoft Store. |  


Чтобы узнать, где находятся эти значки, просмотрите руководство по [упаковке][ExtensionsGuidesPackagingCreatingTestingPackagesAssetsFolder] или руководство по упаковке [ManifoldJS][ExtensionsGuidesPackagingUsingManifoldjsPackagePackagingManifoldjs] .  Это зависит от того, какой метод упаковки выбран.  

#### Значок Microsoft Store  

Если у значка 150px в Microsoft Store есть прозрачный фон, цвет элемента на устройстве пользователя отображается в качестве цвета фона значка.  

Например, если пользователь выбрал розовый как цвет заливки, прозрачный фон значка вашего магазина будет отображаться как розовый.  

:::row:::
   :::column span="1":::
       :::image type="complex" source="../media/windows-accent-color.png" alt-text="Цвет "контрастные" в Windows":::
          Цвет "контрастные" в Windows :::image-end:::
       
       <!--![Windows accent color][ImageWindowsAccentColor]  -->  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="../media/store-icon-with-transparent-background.png" alt-text="Автоматически выбираемый цвет фона":::
         Автоматически выбираемый цвет фона :::image-end:::
      
      <!--![Background color auto selected][ImageStoreIconTransparencyBackground]  -->  
   :::column-end:::
:::row-end:::

Если вы хотите выбрать собственный цвет фона для Microsoft Store, вы должны сделать фон непрозрачным.  

> [!NOTE]
> Отправка расширения Microsoft EDGE в Microsoft Store в настоящее время ограничена возможностями.  [Свяжитесь с нами][AkaExtensionRequest] с помощью ваших запросов на магазин Microsoft Store, и ваш запрос рассматривается для будущего обновления.  

<!-- image links -->  

<!--[ImageActionmenuBrowseraction]: ../media/actionmenu-browseraction.png "browser action in action menu"  -->  
<!--[ImageBrowserActionIcon]: ../media/browseractionicon.png "browser action"  -->  
<!--[ImagePageaction]: ../media/pageaction.png "page action"  -->  
<!--[ImageManagementUi]: ../media/management-ui.png "management UI"  -->  
<!--[ImageWindowsAccentColor]: ../media/windows-accent-color.png "Windows accent color"  -->  
<!--[ImageStoreIconTransparencyBackground]: ../media/store-icon-with-transparent-background.png "Background color auto selected"  -->  

<!-- links -->  

[ExtensionsGuidesAccessibility]: ./accessibility.md "Специальные возможности | Документы Microsoft"  
[ExtensionsGuidesPackagingCreatingTestingPackagesAssetsFolder]: ./packaging/creating-and-testing-extension-packages.md#assets-folder "Папка Assets — создание и тестирование пакета AppX для расширения Microsoft Edge | Документы Microsoft"  
[ExtensionsGuidesPackagingUsingManifoldjsPackagePackagingManifoldjs]: ./packaging/using-manifoldjs-to-package-extensions.md#packaging-with-manifoldjs "Упаковка в ManifoldJS с помощью ManifoldJS для создания пакетов AppX расширений | Документы Microsoft"  

[ExtensionsApisupportManifestkeys]: ../API-support/supported-manifest-keys.md "Поддерживаемые ключи манифеста | Документы Microsoft"  

[AkaExtensionRequest]: https://aka.ms/extension-request "Доступ к нам"  

[MSDApiBrowseractionSeticon]: https://developer.mozilla.org/Add-ons/WebExtensions/API/browserAction/setIcon "browserAction. setIcon ()-API | MDN"  
[MDNApiPageactionSeticon]: https://developer.mozilla.org/Add-ons/WebExtensions/API/pageAction/setIcon "pageAction. setIcon ()-API | MDN"  
[MDNApiPageactionShow]: https://developer.mozilla.org/Add-ons/WebExtensions/API/pageAction/show "pageAction. Show ()-API | MDN"  
[MDNManifestjsonBrowserAction]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/browser_action "browser_action-manifest. JSON | MDN"  
[MDNManifestjsonPageAction]: https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/page_action "page_action-manifest. JSON | MDN"  
