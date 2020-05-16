---
title: Использование манифеста веб-приложения для интеграции последовательного веб-приложения с операционной системой
description: Сведения о том, как использовать манифест веб-приложения для интеграции последовательного веб-приложения с операционной системой.
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/15/2020
ms.topic: conceptual
ms.prod: microsoft-edge
ms.technology: pwa
keywords: прогрессивные веб-приложения, PWA, EDGE, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: f493ae0c3cef3a1950b2207d66fef65055b2d959
ms.sourcegitcommit: d9cc829deb709b0866f6b43a5f4733682ddae5ca
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/16/2020
ms.locfileid: "10659295"
---
# <span data-ttu-id="3f641-104">Использование манифеста веб-приложения для интеграции последовательного веб-приложения с операционной системой</span><span class="sxs-lookup"><span data-stu-id="3f641-104">Use the Web App Manifest to integrate your Progressive Web App into the Operating System</span></span>

<span data-ttu-id="3f641-105">Манифест веб-приложения на веб-сайте влияет на внешний вид и работу последовательного веб-приложения (PWA \) при установке на устройстве.</span><span class="sxs-lookup"><span data-stu-id="3f641-105">A Web App Manifest of a website governs how your Progressive Web App \(PWA\) looks and behaves when installed on a device.</span></span>  <span data-ttu-id="3f641-106">На самом базовом уровне манифест содержит подробные сведения о названии вашего приложения, значках, используемых для представления вашего приложения в системных меню, а также цвета темы, которые используются операционной системой \ (ОС \) в заголовке окна.</span><span class="sxs-lookup"><span data-stu-id="3f641-106">At the most basic level, the Manifest provides details on the name of your app, icons to use to represent your app in system menus, and the theme colors the operating system \(OS\) uses in the title bar.</span></span>  <span data-ttu-id="3f641-107">Кроме того, с помощью манифеста можно разблокирование мощных функций, позволяющих вашему приложению работать как с другими собственными приложениями системы.</span><span class="sxs-lookup"><span data-stu-id="3f641-107">The Manifest also enables you to unlock powerful features that allow your app to behave like other native apps on the system.</span></span>  

## <span data-ttu-id="3f641-108">Быстрый доступ к функциям с помощью сочетаний клавиш</span><span class="sxs-lookup"><span data-stu-id="3f641-108">Use shortcuts to provide quick access to features</span></span>  

<span data-ttu-id="3f641-109">Большинство операционных систем предоставляют быстрый доступ к ключевым функциям приложения с помощью сочетаний клавиш в контекстном меню, подключенном к значку приложения.</span><span class="sxs-lookup"><span data-stu-id="3f641-109">Most operating systems provide quick access to key app features using shortcuts on the context menu connected to the icon of the app.</span></span>  <span data-ttu-id="3f641-110">Для использования сочетаний клавиш в PWA включите `shortcuts` свойство в манифест веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="3f641-110">To use shortcuts in your PWA, include the `shortcuts` property in your Web App Manifest.</span></span>  <span data-ttu-id="3f641-111">В следующем фрагменте кода показано, как определить ярлык в манифесте веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="3f641-111">The following code snippet shows how to define a shortcut in your web app manifest.</span></span>  

```json
"shortcuts": [
    {
        "name": "Play Later",
        "description": "View the list of podcasts you saved for later",
        "url": "/play-later",
        "icons": [
            {
                "src": "/icons/play-later.svg",
                "type": "image/svg+xml",
                "purpose": "any"
            }
        ]
    },
    {
        "name": "Subscriptions",
        "description": "View the list of podcasts available in your subscription",
        "url": "/subscriptions?sort=desc"
    }
]
```  

<span data-ttu-id="3f641-112">При добавлении в полный Манифест веб-приложения Добавление предыдущего фрагмента кода включает два сочетания клавиш в контекстном меню на значке приложения.</span><span class="sxs-lookup"><span data-stu-id="3f641-112">When added to a complete Web App Manifest, adding the previous code snippet enables two shortcuts on the context menu on the icon of the app.</span></span>  <span data-ttu-id="3f641-113">Первый имеет имя `Play Later` и имеет настраиваемый значок.</span><span class="sxs-lookup"><span data-stu-id="3f641-113">The first is named `Play Later` and has a custom icon.</span></span>  <span data-ttu-id="3f641-114">Второй имеет имя `Subscriptions` и не имеет значка, так как `icons` это свойство является необязательным.</span><span class="sxs-lookup"><span data-stu-id="3f641-114">The second is named `Subscriptions` and does not have an icon because the `icons` property is optional.</span></span>  <span data-ttu-id="3f641-115">`description`Свойство также является необязательным и может использоваться для предоставления дополнительной информации о специальных возможностях.</span><span class="sxs-lookup"><span data-stu-id="3f641-115">The `description` property is also optional and may be used to provide additional information for accessibility purposes.</span></span>  

## <span data-ttu-id="3f641-116">Определение приложения в качестве целевого объекта общего доступа</span><span class="sxs-lookup"><span data-stu-id="3f641-116">Identify your app as a Share Target</span></span>

<span data-ttu-id="3f641-117">Многие операционные системы позволяют пользователям быстро предоставлять общий доступ к ссылкам и файлам с помощью собственных приложений.</span><span class="sxs-lookup"><span data-stu-id="3f641-117">Many operating systems enable users to quickly share links and files with native applications.</span></span> <span data-ttu-id="3f641-118">Последовательное веб-приложение может участвовать в этой функции, а также с помощью `share_target` члена манифеста веб-приложения.</span><span class="sxs-lookup"><span data-stu-id="3f641-118">Progressive Web Apps can participate in this feature as well, via the `share_target` member of the Web App Manifest.</span></span> <span data-ttu-id="3f641-119">С помощью share_target вы определяете страницу "действие" (аналогичную форме) и параметры, которые предполагается передать в нее.</span><span class="sxs-lookup"><span data-stu-id="3f641-119">Using share_target, you define the "action" page (similar to a form) and the parameters you expect to be passed into it.</span></span> <span data-ttu-id="3f641-120">В приведенном ниже фрагменте кода показан пример использования `share_target` .</span><span class="sxs-lookup"><span data-stu-id="3f641-120">The following code snippet shows an example of how to use `share_target`.</span></span>

```json
"share_target": {
    "action": "/share.html",
    "params": {
        "title": "name",
        "text": "description",
        "url": "link"
    }
}
```

<span data-ttu-id="3f641-121">При добавлении в манифест веб-приложения это значение определяет "/Share.HTML" в качестве страницы действия для общего доступа.</span><span class="sxs-lookup"><span data-stu-id="3f641-121">When added to the Web App Manifest, this establishes "/share.html" as the action page for a share.</span></span> <span data-ttu-id="3f641-122">Кроме того, он определяет три параметра, которые будут переданы на эту страницу действия: "название", "текст" и "URL".</span><span class="sxs-lookup"><span data-stu-id="3f641-122">Additionally, it defines three parameters that would be passed to that action page: "title", "text", and "url".</span></span> <span data-ttu-id="3f641-123">Эти параметры будут храниться в свойствах "имя", "Описание" и "связь" объекта [ShareData](https://wicg.github.io/web-share#dom-sharedata) .</span><span class="sxs-lookup"><span data-stu-id="3f641-123">These parameters will be stored in the [ShareData](https://wicg.github.io/web-share#dom-sharedata) object’s "name", "description", and "link" properties.</span></span> <span data-ttu-id="3f641-124">По умолчанию на странице действия эти параметры принимаются как часть запроса GET, но вы можете указать запрос `method` и кодировку \ (AS `enctype` \), точно так же, как в веб-форме.</span><span class="sxs-lookup"><span data-stu-id="3f641-124">By default, the action page receives these parameters as part of a GET request, but you can specify the request `method` and encoding \(as `enctype`\), just like you would on a web form.</span></span>

## <span data-ttu-id="3f641-125">См. также</span><span class="sxs-lookup"><span data-stu-id="3f641-125">See also</span></span>  

<span data-ttu-id="3f641-126">Дополнительные сведения о манифестах веб-приложений можно найти в приведенном ниже списке соответствующих тем.</span><span class="sxs-lookup"><span data-stu-id="3f641-126">To learn more about Web App Manifests, see the following list of related topics.</span></span>  

* [<span data-ttu-id="3f641-127">Манифесты веб-приложения</span><span class="sxs-lookup"><span data-stu-id="3f641-127">Web App Manifests</span></span>][MDNWebAppManifests]  
* [<span data-ttu-id="3f641-128">Цель веб-общего доступа</span><span class="sxs-lookup"><span data-stu-id="3f641-128">Web Share Target</span></span>][WICGShareTarget]
* [<span data-ttu-id="3f641-129">Веб-общий доступ</span><span class="sxs-lookup"><span data-stu-id="3f641-129">Web Share</span></span>][WICGShare]

<!-- links -->  

[MDNWebAppManifests]: https://developer.mozilla.org/docs/Web/Manifest "Манифесты веб-приложения | MDN"  
[WICGShareTarget]: https://wicg.github.io/web-share-target/ "Конечный API для веб-общего доступа | WICG"
[WICGShare]: https://w3c.github.io/web-share/ "API для веб-общего доступа | WICG"
