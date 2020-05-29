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
# <span data-ttu-id="6a655-104">Рекомендации по проектированию для расширений Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="6a655-104">Design Guidelines For Microsoft Edge Extensions</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="6a655-105">На следующей странице содержатся различные аспекты проектирования и поведение пользовательского интерфейса, которые следует принимать во время создания расширений Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6a655-105">The following page contains various design aspects and UI behavior to consider when creating Microsoft Edge extensions.</span></span>  

## <span data-ttu-id="6a655-106">Значки</span><span class="sxs-lookup"><span data-stu-id="6a655-106">Icons</span></span>  

<span data-ttu-id="6a655-107">С помощью векторного рисунка вы должны сделать значки расширения.</span><span class="sxs-lookup"><span data-stu-id="6a655-107">You should make the icons of your extension using a vector graphic.</span></span>  <span data-ttu-id="6a655-108">Чтобы упаковать расширение, вы должны создать несколько разных размеров вашего значка и еще три дополнительных размера.</span><span class="sxs-lookup"><span data-stu-id="6a655-108">You must create a few different sizes of your icon for your extension, and three additional sizes if you want to package your extension.</span></span>  <span data-ttu-id="6a655-109">Расширения Microsoft EDGE не поддерживают значки в формате SVG.</span><span class="sxs-lookup"><span data-stu-id="6a655-109">Microsoft Edge extensions do not support .svg icons.</span></span>  

<span data-ttu-id="6a655-110">Перед созданием значков расширений следует ознакомиться с руководством по [специальным возможностям][ExtensionsGuidesAccessibility] , чтобы убедиться в том, что значки обладают достаточной контрастностью и отображаются как в светлых, так и в темных темах Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6a655-110">Before you create your extension icons, you should review the [accessibility][ExtensionsGuidesAccessibility] guide to ensure that your icons have high enough contrast and are visible in both the light and dark themes of Microsoft Edge.</span></span>  

<span data-ttu-id="6a655-111">Несмотря на то, что поддерживается любой формат изображения WebKit, рекомендуется использовать значки PNG для поддержки прозрачности.</span><span class="sxs-lookup"><span data-stu-id="6a655-111">While any webkit image format is supported, .png icons are recommended for transparency support.</span></span>  

### <span data-ttu-id="6a655-112">Значки для расширения</span><span class="sxs-lookup"><span data-stu-id="6a655-112">Icons for your extension</span></span>  

<span data-ttu-id="6a655-113">Для расширения вы должны создать один размер значка для действия в браузере или действие страницы, а также один размер значка для области **расширений** .</span><span class="sxs-lookup"><span data-stu-id="6a655-113">For your extension, you must create one icon size for the browser action or page action, and one icon size for the **Extensions** pane.</span></span>  <span data-ttu-id="6a655-114">Для поддержки дисплеев высокого разрешения может быть предусмотрено более одного размера каждого из них.</span><span class="sxs-lookup"><span data-stu-id="6a655-114">More than one size for each may be provided to support high resolution displays.</span></span>  

<span data-ttu-id="6a655-115">Расширение должно иметь значок действия браузера или действия страницы.</span><span class="sxs-lookup"><span data-stu-id="6a655-115">An extension should have a browser action or page action icon.</span></span>  <span data-ttu-id="6a655-116">При использовании метода [browserAction. setIcon][MSDApiBrowseractionSeticon] или [pageAction. setIcon][MDNApiPageactionSeticon] можно изменить значки действий со страницами и действиями в браузере.</span><span class="sxs-lookup"><span data-stu-id="6a655-116">The browser action and page action icons may be changed at runtime using the [browserAction.setIcon][MSDApiBrowseractionSeticon] method or [pageAction.setIcon][MDNApiPageactionSeticon] method.</span></span>  

#### <span data-ttu-id="6a655-117">Действие браузера</span><span class="sxs-lookup"><span data-stu-id="6a655-117">Browser action</span></span>  

<span data-ttu-id="6a655-118">Предпочтительные размеры для значков действий браузера и действия страницы:, `20px` `25px` `30px` и `40px` .</span><span class="sxs-lookup"><span data-stu-id="6a655-118">The preferred sizes for browser action and page action icons are `20px`, `25px`, `30px`, and `40px`.</span></span>  <span data-ttu-id="6a655-119">Другие поддерживаемые размеры включают `19px` в себя, `35px` и `38px` .</span><span class="sxs-lookup"><span data-stu-id="6a655-119">Other supported sizes include `19px`, `35px`, and `38px`.</span></span>  

<span data-ttu-id="6a655-120">В следующем фрагменте файла [manifest. JSON][ExtensionsApisupportManifestkeys] показан стандарт и значок действия браузера High Definition, который задается с помощью ключа [browser_action][MDNManifestjsonBrowserAction] .</span><span class="sxs-lookup"><span data-stu-id="6a655-120">The following [manifest.json][ExtensionsApisupportManifestkeys] file snippet shows a standard and high definition browser action icon being specified using the [browser_action][MDNManifestjsonBrowserAction] key.</span></span>  <span data-ttu-id="6a655-121">Тот же синтаксис применяется для ключа [page_action][MDNManifestjsonPageAction] .</span><span class="sxs-lookup"><span data-stu-id="6a655-121">The same syntax applies for the [page_action][MDNManifestjsonPageAction] key.</span></span>  

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

<span data-ttu-id="6a655-122">Если действие браузера было установлено с помощью расширения, оно появляется либо в меню действия после выбора команды **Дополнительно (...)**, либо справа от адресной строки, если пользователь отключил **кнопку Показать рядом с адресной строкой** .</span><span class="sxs-lookup"><span data-stu-id="6a655-122">If the browser action has been set by the extension, it appears either in the Actions menu after selecting **More(...)**,  or to the right of the address bar if **Show button next to the address bar** has been toggled on by the user.</span></span>  

:::row:::
   :::column span="1":::
      :::image type="complex" source="../media/actionmenu-browseraction.png" alt-text="Действие браузера в меню "действие"":::
         <span data-ttu-id="6a655-124">Действие браузера в меню "действие"</span><span class="sxs-lookup"><span data-stu-id="6a655-124">Browser action in action menu</span></span> :::image-end:::
      
      <!--![browser action in action menu][ImageActionmenuBrowseraction]  -->  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="../media/browseractionicon.png" alt-text="Действие браузера":::
         <span data-ttu-id="6a655-126">Действие браузера</span><span class="sxs-lookup"><span data-stu-id="6a655-126">Browser action</span></span> :::image-end:::
      
      <!--![browser action][ImageBrowserActionIcon]  -->  
   :::column-end:::
:::row-end:::

#### <span data-ttu-id="6a655-127">Действие страницы</span><span class="sxs-lookup"><span data-stu-id="6a655-127">Page action</span></span>  

<span data-ttu-id="6a655-128">Ключ [page_action][MDNManifestjsonPageAction] имеет тот же синтаксис МАНИФЕСТа JSON, что и ключ [browser_action][MDNManifestjsonBrowserAction] .</span><span class="sxs-lookup"><span data-stu-id="6a655-128">The [page_action][MDNManifestjsonPageAction] key has the same JSON manifest syntax as the [browser_action][MDNManifestjsonBrowserAction] key.</span></span>  <span data-ttu-id="6a655-129">Действие страницы также имеет те же требования к размеру значка, что и действие браузера.</span><span class="sxs-lookup"><span data-stu-id="6a655-129">Page action also has the same icon size requirements as browser action.</span></span>  

<span data-ttu-id="6a655-130">Если в файле [manifest. JSON][ExtensionsApisupportManifestkeys] задано действие Page, оно отображается в адресной строке всякий раз, когда используется метод [pageAction. Show][MDNApiPageactionShow] .</span><span class="sxs-lookup"><span data-stu-id="6a655-130">If page action is specified in the [manifest.json][ExtensionsApisupportManifestkeys] file, it appears within the address bar whenever the [pageAction.show][MDNApiPageactionShow] method is used.</span></span>  

:::image type="complex" source="../media/pageaction.png" alt-text="Действие страницы":::
   <span data-ttu-id="6a655-132">Действие страницы</span><span class="sxs-lookup"><span data-stu-id="6a655-132">Page action</span></span>
:::image-end:::

<!--![page action][ImagePageaction]  -->  

##### <span data-ttu-id="6a655-133">Пользовательский интерфейс управления</span><span class="sxs-lookup"><span data-stu-id="6a655-133">Management UI</span></span>  

<span data-ttu-id="6a655-134">Когда пользователь переходит на панель расширений, переходя к меню **Дополнительно (...)** , и выбирая **расширения**, рядом с названием расширения отображается значок.</span><span class="sxs-lookup"><span data-stu-id="6a655-134">When users navigate to the extensions pane by going to the **More(...)** menu and selecting **Extensions**, an icon is displayed next to the name of the extension.</span></span>  

<span data-ttu-id="6a655-135">Вы должны указать следующие размеры значков.</span><span class="sxs-lookup"><span data-stu-id="6a655-135">You should specify the following icon sizes.</span></span>  

| <span data-ttu-id="6a655-136">Раздел</span><span class="sxs-lookup"><span data-stu-id="6a655-136">Key</span></span> | <span data-ttu-id="6a655-137">Сведения</span><span class="sxs-lookup"><span data-stu-id="6a655-137">Details</span></span> |  
|:--- |:--- |  
| `48px` | <span data-ttu-id="6a655-138">Значок стандартного разрешения на экран.</span><span class="sxs-lookup"><span data-stu-id="6a655-138">Icon for standard resolution displays.</span></span> |  
| `128px` | <span data-ttu-id="6a655-139">Значок для дисплеев с высоким разрешением.</span><span class="sxs-lookup"><span data-stu-id="6a655-139">Icon for high resolution displays.</span></span> |  
| `176px` | <span data-ttu-id="6a655-140">Значок для отображения еще более высокое разрешение экрана.</span><span class="sxs-lookup"><span data-stu-id="6a655-140">Icon for even higher resolution displays.</span></span> |  


```json
"icons": {
    "48": "images/icon_48.png",
    "128": "images/icon_128.png",
    "176": "images/icon_176.png"
},
```  

:::image type="complex" source="../media/management-ui.png" alt-text="Пользовательский интерфейс управления":::
   <span data-ttu-id="6a655-142">Пользовательский интерфейс управления</span><span class="sxs-lookup"><span data-stu-id="6a655-142">Management UI</span></span>
:::image-end:::

<!--![management UI][ImageManagementUi]  -->  

### <span data-ttu-id="6a655-143">Значки для упаковки</span><span class="sxs-lookup"><span data-stu-id="6a655-143">Icons for packaging</span></span>  

<span data-ttu-id="6a655-144">После того как ваше расширение будет готово к упаковке, вы должны иметь три дополнительных размера значков.</span><span class="sxs-lookup"><span data-stu-id="6a655-144">Once your extension is ready for packaging, you must have three additional icon sizes ready.</span></span>  

| <span data-ttu-id="6a655-145">Size</span><span class="sxs-lookup"><span data-stu-id="6a655-145">Size</span></span> | <span data-ttu-id="6a655-146">Сведения</span><span class="sxs-lookup"><span data-stu-id="6a655-146">Details</span></span> |  
|:--- |:--- |  
| <span data-ttu-id="6a655-147">44px</span><span class="sxs-lookup"><span data-stu-id="6a655-147">44px</span></span> | <span data-ttu-id="6a655-148">Используется в пользовательском интерфейсе Windows \ (**список приложений** **,**  \>  приложения**системы**  \>  **& функций**).</span><span class="sxs-lookup"><span data-stu-id="6a655-148">Used in the Windows UI \(**App List**, **Settings** \> **System** \> **Apps & features**\).</span></span> |  
| <span data-ttu-id="6a655-149">50px</span><span class="sxs-lookup"><span data-stu-id="6a655-149">50px</span></span> | <span data-ttu-id="6a655-150">Требования к пакетированию (не отображаются в любом месте).</span><span class="sxs-lookup"><span data-stu-id="6a655-150">Packaging requirement \(not visible anywhere\).</span></span> |  
| <span data-ttu-id="6a655-151">150px</span><span class="sxs-lookup"><span data-stu-id="6a655-151">150px</span></span> | <span data-ttu-id="6a655-152">Используется в качестве значка для Microsoft Store.</span><span class="sxs-lookup"><span data-stu-id="6a655-152">Used as the icon for the Microsoft Store.</span></span> |  


<span data-ttu-id="6a655-153">Чтобы узнать, где находятся эти значки, просмотрите руководство по [упаковке][ExtensionsGuidesPackagingCreatingTestingPackagesAssetsFolder] или руководство по упаковке [ManifoldJS][ExtensionsGuidesPackagingUsingManifoldjsPackagePackagingManifoldjs] .</span><span class="sxs-lookup"><span data-stu-id="6a655-153">See either the [manual packaging guide][ExtensionsGuidesPackagingCreatingTestingPackagesAssetsFolder] or the [ManifoldJS packaging guide][ExtensionsGuidesPackagingUsingManifoldjsPackagePackagingManifoldjs] to determine where these icons is placed.</span></span>  <span data-ttu-id="6a655-154">Это зависит от того, какой метод упаковки выбран.</span><span class="sxs-lookup"><span data-stu-id="6a655-154">This depends upon which packaging method you choose.</span></span>  

#### <span data-ttu-id="6a655-155">Значок Microsoft Store</span><span class="sxs-lookup"><span data-stu-id="6a655-155">Microsoft Store icon</span></span>  

<span data-ttu-id="6a655-156">Если у значка 150px в Microsoft Store есть прозрачный фон, цвет элемента на устройстве пользователя отображается в качестве цвета фона значка.</span><span class="sxs-lookup"><span data-stu-id="6a655-156">If the 150px icon for the Microsoft Store has a transparent background, the accent color of the user's device appears as the background color of the icon.</span></span>  

<span data-ttu-id="6a655-157">Например, если пользователь выбрал розовый как цвет заливки, прозрачный фон значка вашего магазина будет отображаться как розовый.</span><span class="sxs-lookup"><span data-stu-id="6a655-157">For example, if a user has selected pink as the accent color, the transparent background of your store icon is displayed as pink.</span></span>  

:::row:::
   :::column span="1":::
       :::image type="complex" source="../media/windows-accent-color.png" alt-text="Цвет "контрастные" в Windows":::
          <span data-ttu-id="6a655-159">Цвет "контрастные" в Windows</span><span class="sxs-lookup"><span data-stu-id="6a655-159">Windows accent color</span></span> :::image-end:::
       
       <!--![Windows accent color][ImageWindowsAccentColor]  -->  
   :::column-end:::
   :::column span="1":::
      :::image type="complex" source="../media/store-icon-with-transparent-background.png" alt-text="Автоматически выбираемый цвет фона":::
         <span data-ttu-id="6a655-161">Автоматически выбираемый цвет фона</span><span class="sxs-lookup"><span data-stu-id="6a655-161">Background color auto selected</span></span> :::image-end:::
      
      <!--![Background color auto selected][ImageStoreIconTransparencyBackground]  -->  
   :::column-end:::
:::row-end:::

<span data-ttu-id="6a655-162">Если вы хотите выбрать собственный цвет фона для Microsoft Store, вы должны сделать фон непрозрачным.</span><span class="sxs-lookup"><span data-stu-id="6a655-162">If you want to pick your own background color for your Microsoft Store, you must make the background opaque.</span></span>  

> [!NOTE]
> <span data-ttu-id="6a655-163">Отправка расширения Microsoft EDGE в Microsoft Store в настоящее время ограничена возможностями.</span><span class="sxs-lookup"><span data-stu-id="6a655-163">Submitting a Microsoft Edge extension to the Microsoft Store is currently a restricted capability.</span></span>  <span data-ttu-id="6a655-164">[Свяжитесь с нами][AkaExtensionRequest] с помощью ваших запросов на магазин Microsoft Store, и ваш запрос рассматривается для будущего обновления.</span><span class="sxs-lookup"><span data-stu-id="6a655-164">[Contact us][AkaExtensionRequest] with your requests for the Microsoft Store, and your request is considered for a future update.</span></span>  

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
