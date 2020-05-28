---
description: Расширение "Начало работы", часть 1
title: Создавайте простое расширение, которое выталкивает на картину дня в NASA
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/08/2020
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: Edge — Chromium, Web Development, HTML, CSS, JavaScript, разработчик, расширения
ms.openlocfilehash: dd5c1dab0cb9b54b79be7d2728cb9bfde0945185
ms.sourcegitcommit: 0bc1312a1e6a0ac37cf385201db4361fc05184fc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/28/2020
ms.locfileid: "10683625"
---
# Создавайте простое расширение, которое выталкивает на картину дня в NASA  

[Источник пакета расширения для этой части завершен][ArchiveExtensionGettingStartedPart1]  

## Обзор  

В части 1 цель состоит в том, чтобы создать очень простое расширение Chromium EDGE, начиная с пустого каталога.  Цель этого расширения — выполнить следующие задачи.  

*   Создание значков для расширения, которое может использоваться в разных местах и в разных размерах  
*   Создание простого `manifest.json` файла  
*   Отображение значка запуска, на котором выводится всплывающее окно с изображением в виде NASA дня  

## Основы файла манифеста  

У каждого пакета расширения должен быть `manifest.json` файл в корне.  Вы должны представить этот план для расширения.  Она сообщает обработчику о том, какая версия API расширения ожидает расширений, имя и описание расширения, а также множество других сведений, которые обсуждаются в данном руководстве по началу работы с несколькими компонентами.  

Ниже приведен простой  `manifest.json`  

```json
{
    "name": "NASA Picture of the day viewer",
    "version": "0.0.0.1",
    "manifest_version": 2,
    "description": "A Chromium Extension to show the NASA Picture of the Day."
}
```  

## Настройка значков расширений  

Затем добавьте в файл несколько значков `manifest.json` \ (и создайте новый `/icons` каталог с файлами значков \).  Значки используются для фонового изображения кнопки, которую пользователь выбирает, чтобы запустить расширение \ (если есть), и другие подходящие места.  

`PNG` является рекомендуемым форматом, но вы также можете `BMP` использовать `GIF` , `ICO` и `JPEG` .  Рекомендуется всегда иметь значок размера 128x128 пикселей, и браузер автоматически изменяет их размер по мере необходимости.  

Структура каталогов должна выглядеть так, как показано на рисунке ниже.  

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

Обновленный `manifest.json` файл должен выглядеть следующим образом.  

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
> Файлы значков, `png` перечисленные в предыдущем коде, находятся в файле с расширением ZIP, упомянутом в верхней части этой страницы.  

## Добавление всплывающего окна по умолчанию  

Теперь создайте `HTML` файл, который автоматически запускается, когда пользователь выбирает значок расширения.  

:::image type="complex" source="./media/part1-badge1.png" alt-text="Значок значка на панели инструментов":::
   Значок значка на панели инструментов
:::image-end:::

<!--![Toolbar Badge Icon][ImagePart1Badge1]  -->  

Имя HTML-файла `popup/popup.html` .  При выборе значка расширения открывается `popup/popup.html` модальное диалоговое окно, которое остается на месте, пока не выберете его за пределы диалогового окна.  

Для этого зарегистрируйте файл в качестве всплывающего окна по умолчанию в `manifest.json` разделе в `browser_action` следующем коде.  

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

В `popup` каталоге добавьте файл, чтобы `popup.html` он отображался на изображении звезд.  `popup.html`Файл.  

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

 Кроме того, добавьте файл изображения `images/stars.jpeg` , на который указывает ссылка в `popup.html` файле.  

Структура каталогов для примера расширения показана на следующей схеме.  

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

> [!NOTE]
> `images/stars.jpeg`Файл, указанный в предыдущем изображении, доступен в разделе [Загрузка ZIP][ArchiveExtensionGettingStartedPart1].  

Это все, что нужно для того, чтобы создать рабочее расширение.  Все, что осталось для проверки.  

В следующем разделе объясняется, как загрузить расширение \ (иногда называется загрузкой на боковой панели) в браузер Microsoft Edge \ (Chromium \), чтобы протестировать его.  

## Запуск расширения локально в браузере во время его разработки \ (боковая загрузка)  

Браузер Microsoft Edge \ (Chromium \) обеспечивает безопасный и простой способ для работы с ними, а также для отладки расширений во время разработки.  

Процесс довольно прост.  Сначала нужно выбрать три точки в верхней части окна браузера.  Затем выберите нужное `Extensions` значение из контекстного меню, как показано на рисунке ниже.  

:::image type="complex" source="./media/part1-threedots.png" alt-text="Выбор расширений":::
   Выбор расширений
:::image-end:::

<!--![Choose Extensions][ImagePart1Threedots]  -->  

На странице **Extensions** , как показано на приведенном ниже изображении, включите **режим разработчика** , включив переключатель в нижнюю часть страницы, как показано на рисунке ниже.  

:::image type="complex" source="./media/part1-developermode-toggle.png" alt-text="Включение режима разработчика":::
   Включение режима разработчика
:::image-end:::

<!--![Enable Developer Mode][ImagePart1DevelopermodeToggle]  -->  

## Установка и обновление расширений, загруженных в сторону  

Когда вы в первый раз хотите установить расширение, вы выбираете параметр, `Load Unpacked` как показано на рисунке ниже.  В этом случае появится запрос на доступ к каталогу, в котором находится файл ресурсов расширения.  Это расширение будет установлено так, как будто вы загрузили его из магазина.  

:::image type="complex" source="./media/part1-installed-extension.png" alt-text="Установленные расширения":::
   Установленные расширения
:::image-end:::

<!--![Installed Extensions][ImagePart1InstalledExtension]  -->  

После установки расширения вы можете обновить его, нажав `Reload` кнопку под перечнем расширения.  

Чтобы удалить расширение из браузера, нажмите кнопку `Remove` внизу списка расширений.  

## Отладка расширений  

Отладка расширений осуществляется очень просто и поддерживает все функции в EDGE Chromium DevTools.  Эти сведения не рассматриваются в этом руководстве по началу работы, но очень важны для успешного построения расширений.  

<!-- image links -->  

<!--[ImagePart1Heirarchy]: ./media/part1-heirarchy.png "Directory Structure"  -->  
<!--[ImagePart1Badge1]: ./media/part1-badge1.png "Toolbar Badge Icon"  -->  
<!--[ImagePart1Heirarchy1]: ./media/part1-heirarchy1.png "Directory Structure for Extension"  -->  
<!--[ImagePart1Threedots]: ./media/part1-threedots.png "Choose Extensions"  -->  
<!--[ImagePart1DevelopermodeToggle]: ./media/part1-developermode-toggle.png "Enable Developer Mode"  -->  
<!--[ImagePart1InstalledExtension]: ./media/part1-installed-extension.png "Installed Extensions"  -->  

<!-- links -->  

[ArchiveExtensionGettingStartedPart1]: ./extension-source/extension-getting-started-part1.zip "Источник пакета расширения для этой части завершен | Документы Microsoft"  
