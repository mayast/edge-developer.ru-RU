---
description: Расширение "Начало работы", часть 1
title: Создавайте простое расширение, которое выталкивает на картину дня в NASA
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge — Chromium, Web Development, HTML, CSS, JavaScript, разработчик, расширения
ms.openlocfilehash: 826401869b98d339e9b156a3727d94bd1182063d
ms.sourcegitcommit: d360e419b5f96f4f691cf7330b0d8dff9126f82e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015767"
---
# <span data-ttu-id="557f9-104">Создавайте простое расширение, которое выталкивает на картину дня в NASA</span><span class="sxs-lookup"><span data-stu-id="557f9-104">Build A Simple Extension That Pops Up NASA Picture Of The Day</span></span> 
 
<!--  
[Completed Extension Package Source for This Part][ArchiveExtensionGettingStartedPart1]  
-->  

## <span data-ttu-id="557f9-105">Обзор</span><span class="sxs-lookup"><span data-stu-id="557f9-105">Overview</span></span>  

<span data-ttu-id="557f9-106">В части 1 цель состоит в том, чтобы создать очень простое расширение Chromium EDGE, начиная с пустого каталога.</span><span class="sxs-lookup"><span data-stu-id="557f9-106">In part 1, the goal is to build a very simple Edge Chromium Extension starting with an empty directory.</span></span>  <span data-ttu-id="557f9-107">Цель этого расширения — выполнить следующие задачи.</span><span class="sxs-lookup"><span data-stu-id="557f9-107">The goal for this Extension is to complete the following tasks.</span></span>  

*   <span data-ttu-id="557f9-108">Создание значков для расширения, которое может использоваться в разных местах и в разных размерах</span><span class="sxs-lookup"><span data-stu-id="557f9-108">Create icons for the Extension that may be used in multiple places and in different sizes</span></span>  
*   <span data-ttu-id="557f9-109">Создание простого `manifest.json` файла</span><span class="sxs-lookup"><span data-stu-id="557f9-109">Create a simple `manifest.json` file</span></span>  
*   <span data-ttu-id="557f9-110">Отображение значка запуска, на котором выводится всплывающее окно с изображением в виде NASA дня</span><span class="sxs-lookup"><span data-stu-id="557f9-110">Display a launch icon that when selected displays a pop-up window containing the NASA picture of the day</span></span>  

## <span data-ttu-id="557f9-111">Основы файла манифеста</span><span class="sxs-lookup"><span data-stu-id="557f9-111">The manifest file basics</span></span>  

<span data-ttu-id="557f9-112">У каждого пакета расширения должен быть `manifest.json` файл в корне.</span><span class="sxs-lookup"><span data-stu-id="557f9-112">Every Extension package must have a `manifest.json` file at the root.</span></span>  <span data-ttu-id="557f9-113">Вы должны представить этот план для расширения.</span><span class="sxs-lookup"><span data-stu-id="557f9-113">You should think of this as the blueprint for the Extension.</span></span>  <span data-ttu-id="557f9-114">Она сообщает обработчику о том, какая версия API расширения ожидает расширений, имя и описание расширения, а также множество других сведений, которые обсуждаются в данном руководстве по началу работы с несколькими компонентами.</span><span class="sxs-lookup"><span data-stu-id="557f9-114">It tells the browser engine what version of the Extension API the Extension expects, the name and description of the Extension, and lots of other details, many of which are discussed in this multi-part Extension Getting Started guide.</span></span>  

<span data-ttu-id="557f9-115">Ниже приведен простой</span><span class="sxs-lookup"><span data-stu-id="557f9-115">Below is the simple</span></span>  `manifest.json`  

```json
{
    "name": "NASA Picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A Chromium Extension to show the NASA Picture of the Day."
}
```  

## <span data-ttu-id="557f9-116">Настройка значков расширений</span><span class="sxs-lookup"><span data-stu-id="557f9-116">Extension icons setup</span></span>  

<span data-ttu-id="557f9-117">Затем добавьте в файл несколько значков `manifest.json` \ (и создайте новый `/icons` каталог с файлами значков \).</span><span class="sxs-lookup"><span data-stu-id="557f9-117">Next add some icons to `manifest.json` file \(and create a new `/icons` directory with the icons files\).</span></span>  <span data-ttu-id="557f9-118">Значки используются для фонового изображения кнопки, которую пользователь выбирает, чтобы запустить расширение \ (если есть), и другие подходящие места.</span><span class="sxs-lookup"><span data-stu-id="557f9-118">The icons are used for the background image of the button the user selects to launch the extension \(if there is one\), and other places that are appropriate.</span></span>  

`PNG` <span data-ttu-id="557f9-119">является рекомендуемым форматом, но вы также можете `BMP` использовать `GIF` , `ICO` и `JPEG` .</span><span class="sxs-lookup"><span data-stu-id="557f9-119">is the recommended format, but you may also use `BMP`, `GIF`, `ICO` and `JPEG`.</span></span>  <span data-ttu-id="557f9-120">Рекомендуется всегда иметь значок размера 128x128 пикселей, и браузер автоматически изменяет их размер по мере необходимости.</span><span class="sxs-lookup"><span data-stu-id="557f9-120">It is recommended to always have at least a 128x128 pixels size icon and the browser automatically resizes it as necessary.</span></span>  

<span data-ttu-id="557f9-121">Структура каталогов должна выглядеть так, как показано на рисунке ниже.</span><span class="sxs-lookup"><span data-stu-id="557f9-121">Your directory structure should look like the following diagram.</span></span>  

<!--  
:::image type="complex" source="./media/part1-heirarchy.png" alt-text="Directory Structure":::
   Directory Structure
:::image-end:::
-->  

<!--![Directory Structure][ImagePart1Heirarchy]  -->  

```shell
└── part1
    ├── _manifest.json
    └── icons
        ├── nasapod16x16.png
        ├── nasapod32x32.png
        ├── nasapod48x48.png
        └── nasapod128x128.png
```  

<span data-ttu-id="557f9-122">Обновленный `manifest.json` файл должен выглядеть следующим образом.</span><span class="sxs-lookup"><span data-stu-id="557f9-122">Your updated `manifest.json` file should appear as follows.</span></span>  

```json
{
    "name": "NASA Picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A chromium extension to show the NASA Picture of the Day.",
    "icons": {
        "16": "icons/nasapod16x16.png",
        "32": "icons/nasapod32x32.png",
        "48": "icons/nasapod48x48.png",
        "128": "icons/nasapod128x128.png"
    }
}
```  

> [!NOTE]
> <span data-ttu-id="557f9-123">Файлы значков, `png` перечисленные в предыдущем коде, находятся в файле с расширением ZIP, упомянутом в верхней части этой страницы.</span><span class="sxs-lookup"><span data-stu-id="557f9-123">The icon `png` files listed previous code are available in the zip download mentioned at the top of this page.</span></span>  

## <span data-ttu-id="557f9-124">Добавление всплывающего окна по умолчанию</span><span class="sxs-lookup"><span data-stu-id="557f9-124">Adding a default pop-up dialog</span></span>  

<span data-ttu-id="557f9-125">Теперь создайте `HTML` файл, который автоматически запускается, когда пользователь выбирает значок расширения.</span><span class="sxs-lookup"><span data-stu-id="557f9-125">Now, create an `HTML` file that is automatically run when the user selects on the extension icon.</span></span>  

:::image type="complex" source="./media/part1-badge1.png" alt-text="Значок значка на панели инструментов":::
   <span data-ttu-id="557f9-127">Значок значка на панели инструментов</span><span class="sxs-lookup"><span data-stu-id="557f9-127">Toolbar Badge Icon</span></span>
:::image-end:::

<!--![Toolbar Badge Icon][ImagePart1Badge1]  -->  

<span data-ttu-id="557f9-128">Имя HTML-файла `popup/popup.html` .</span><span class="sxs-lookup"><span data-stu-id="557f9-128">The HTML file is named `popup/popup.html`.</span></span>  <span data-ttu-id="557f9-129">При выборе значка расширения открывается `popup/popup.html` модальное диалоговое окно, которое остается на месте, пока не выберете его за пределы диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="557f9-129">Selecting the Extension icon launches `popup/popup.html` as modal dialog that stays up until you select outside the dialog.</span></span>  

<span data-ttu-id="557f9-130">Для этого зарегистрируйте файл в качестве всплывающего окна по умолчанию в `manifest.json` разделе в `browser_action` следующем коде.</span><span class="sxs-lookup"><span data-stu-id="557f9-130">For this, register the file as a default pop-up in the `manifest.json` under `browser_action` in the following code.</span></span>  

```json
{
    "name": "NASA Picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A chromium Extension to show the NASA Picture of the Day.",
    "icons": {
        "16": "icons/nasapod16x16.png",
        "32": "icons/nasapod32x32.png",
        "48": "icons/nasapod48x48.png",
        "128": "icons/nasapod128x128.png"
    },
    "browser_action": {
        "default_popup": "popup/popup.html"
    }
}
```  

<span data-ttu-id="557f9-131">В `popup` каталоге добавьте файл, чтобы `popup.html` он отображался на изображении звезд.</span><span class="sxs-lookup"><span data-stu-id="557f9-131">In the `popup` directory , add the file `popup.html` and have it render the stars image.</span></span>  <span data-ttu-id="557f9-132">`popup.html`Файл.</span><span class="sxs-lookup"><span data-stu-id="557f9-132">Here is the `popup.html` file.</span></span>  

```html
<html lang="en">
    <head>
        <meta charset="UTF-8" />
        <title>NASA Picture of the Day</title>
    </head>
    <body>
        <div>
            <img src="/images/stars.jpeg" alt="stars" />
        </div>
    </body>
</html>
```  

 <span data-ttu-id="557f9-133">Кроме того, добавьте файл изображения `images/stars.jpeg` , на который указывает ссылка в `popup.html` файле.</span><span class="sxs-lookup"><span data-stu-id="557f9-133">Also, add an image file `images/stars.jpeg` that is referenced in the `popup.html` file.</span></span>  

<span data-ttu-id="557f9-134">Структура каталогов для примера расширения показана на следующей схеме.</span><span class="sxs-lookup"><span data-stu-id="557f9-134">The directory structure for the example Extension is displayed in the following diagram.</span></span>  

<!--  
:::image type="complex" source="./media/part1-heirarchy1.png" alt-text="Directory Structure for Extension":::
   Directory Structure for Extension
:::image-end:::
-->  

<!--![Directory Structure for Extension][ImagePart1Heirarchy1]  -->  

```shell
└── part1
    ├── _manifest.json
    ├── icons
    │   ├── nasapod16x16.png
    │   ├── nasapod32x32.png
    │   ├── nasapod48x48.png
    │   └── nasapod128x128.png
    ├── images
    │   └── stars.jpeg
    └── popup
        └── popup.html
```  

<!--  
> [!NOTE]
> The `images/stars.jpeg` file listed in the previous image is available in the [zip download][ArchiveExtensionGettingStartedPart1].  
-->  

<span data-ttu-id="557f9-135">Это все, что нужно для того, чтобы создать рабочее расширение.</span><span class="sxs-lookup"><span data-stu-id="557f9-135">That is everything you need to build a working Extension.</span></span>  <span data-ttu-id="557f9-136">Все, что осталось сделать, — это проверить его.</span><span class="sxs-lookup"><span data-stu-id="557f9-136">All that is left to do is test it.</span></span>  

<span data-ttu-id="557f9-137">В следующем разделе объясняется, как загрузить расширение \ (иногда называется загрузкой на боковой панели) в браузер Microsoft Edge \ (Chromium \), чтобы протестировать его.</span><span class="sxs-lookup"><span data-stu-id="557f9-137">The next section explains how to load the Extension \(sometimes called side loading\) into the Microsoft Edge \(Chromium\) browser to test it.</span></span>  

## <span data-ttu-id="557f9-138">Запуск расширения локально в браузере во время его разработки \ (боковая загрузка)</span><span class="sxs-lookup"><span data-stu-id="557f9-138">Run your Extension locally in your browser while developing it \(side-loading\)</span></span>  

<span data-ttu-id="557f9-139">Браузер Microsoft Edge \ (Chromium \) обеспечивает безопасный и простой способ для работы с ними, а также для отладки расширений во время разработки.</span><span class="sxs-lookup"><span data-stu-id="557f9-139">The Microsoft Edge \(Chromium\) browser provides a safe and simple way for you to run as well as debug your Extensions while you are developing.</span></span>  

<span data-ttu-id="557f9-140">Процесс довольно прост.</span><span class="sxs-lookup"><span data-stu-id="557f9-140">The process is quite simple.</span></span>  <span data-ttu-id="557f9-141">Сначала нужно выбрать три точки в верхней части окна браузера.</span><span class="sxs-lookup"><span data-stu-id="557f9-141">You must first select the three dots at the top of your browser.</span></span>  <span data-ttu-id="557f9-142">Затем выберите нужное `Extensions` значение из контекстного меню, как показано на рисунке ниже.</span><span class="sxs-lookup"><span data-stu-id="557f9-142">Next, choose `Extensions` from the context menu as shown in the following image.</span></span>  

:::image type="complex" source="./media/part1-threedots.png" alt-text="Выбор расширений":::
   <span data-ttu-id="557f9-144">Выбор расширений</span><span class="sxs-lookup"><span data-stu-id="557f9-144">Choose Extensions</span></span>
:::image-end:::

<!--![Choose Extensions][ImagePart1Threedots]  -->  

<span data-ttu-id="557f9-145">На странице **Extensions** , как показано на приведенном ниже изображении, включите **режим разработчика** , включив переключатель в нижнюю часть страницы, как показано на рисунке ниже.</span><span class="sxs-lookup"><span data-stu-id="557f9-145">When you are on the **Extensions** page as shown in the following image, enable the **Developer mode** by enabling the toggle at the bottom left of the page as shown in the following image.</span></span>  

:::image type="complex" source="./media/part1-developermode-toggle.png" alt-text="Включение режима разработчика":::
   <span data-ttu-id="557f9-147">Включение режима разработчика</span><span class="sxs-lookup"><span data-stu-id="557f9-147">Enable Developer Mode</span></span>
:::image-end:::

<!--![Enable Developer Mode][ImagePart1DevelopermodeToggle]  -->  

## <span data-ttu-id="557f9-148">Установка и обновление расширений, загруженных в сторону</span><span class="sxs-lookup"><span data-stu-id="557f9-148">Installing and updating side-loaded Extensions</span></span>  

<span data-ttu-id="557f9-149">Когда вы в первый раз хотите установить расширение, вы выбираете параметр, `Load Unpacked` как показано на рисунке ниже.</span><span class="sxs-lookup"><span data-stu-id="557f9-149">The first time you want to install your Extension, you choose the `Load Unpacked` option as shown in the following image.</span></span>  <span data-ttu-id="557f9-150">В этом случае появится запрос на доступ к каталогу, в котором находится файл ресурсов расширения.</span><span class="sxs-lookup"><span data-stu-id="557f9-150">This prompts you for a directory where you have your Extension assets file by file.</span></span>  <span data-ttu-id="557f9-151">Это расширение будет установлено так, как будто вы загрузили его из магазина.</span><span class="sxs-lookup"><span data-stu-id="557f9-151">This installs the Extension as if you had downloaded it from a store.</span></span>  

:::image type="complex" source="./media/part1-installed-extension.png" alt-text="Установленные расширения":::
   <span data-ttu-id="557f9-153">Установленные расширения</span><span class="sxs-lookup"><span data-stu-id="557f9-153">Installed Extensions</span></span>
:::image-end:::

<!--![Installed Extensions][ImagePart1InstalledExtension]  -->  

<span data-ttu-id="557f9-154">После установки расширения вы можете обновить его, нажав `Reload` кнопку под перечнем расширения.</span><span class="sxs-lookup"><span data-stu-id="557f9-154">After you install your Extension, you may update it by selecting the `Reload` button under your Extension listing.</span></span>  

<span data-ttu-id="557f9-155">Чтобы удалить расширение из браузера, нажмите кнопку `Remove` внизу списка расширений.</span><span class="sxs-lookup"><span data-stu-id="557f9-155">To remove the Extension from your browser, click the `Remove` button on the bottom of the Extension listing.</span></span>  

## <span data-ttu-id="557f9-156">Отладка расширений</span><span class="sxs-lookup"><span data-stu-id="557f9-156">Debugging Extensions</span></span>  

<span data-ttu-id="557f9-157">Отладка расширений осуществляется очень просто и поддерживает все функции в EDGE Chromium DevTools.</span><span class="sxs-lookup"><span data-stu-id="557f9-157">Debugging Extensions is quite easy and supports all of the features in Edge Chromium DevTools.</span></span>  <span data-ttu-id="557f9-158">Эти сведения не рассматриваются в этом руководстве по началу работы, но очень важны для успешного построения расширений.</span><span class="sxs-lookup"><span data-stu-id="557f9-158">Those details however are not covered in this getting started guide but are very important to successfully build Extensions.</span></span>  

<!-- image links -->  

<!--[ImagePart1Heirarchy]: ./media/part1-heirarchy.png "Directory Structure"  -->  
<!--[ImagePart1Badge1]: ./media/part1-badge1.png "Toolbar Badge Icon"  -->  
<!--[ImagePart1Heirarchy1]: ./media/part1-heirarchy1.png "Directory Structure for Extension"  -->  
<!--[ImagePart1Threedots]: ./media/part1-threedots.png "Choose Extensions"  -->  
<!--[ImagePart1DevelopermodeToggle]: ./media/part1-developermode-toggle.png "Enable Developer Mode"  -->  
<!--[ImagePart1InstalledExtension]: ./media/part1-installed-extension.png "Installed Extensions"  -->  

<!-- links -->  

[ArchiveExtensionGettingStartedPart1]: ./extension-source/extension-getting-started-part1.zip "Источник пакета расширения для этой части завершен | Документы Microsoft"  
