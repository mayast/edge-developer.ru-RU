---
description: Предотвращение работы с контентом мультимедиа на сайте
title: Политики автозапуска — руководство для разработки
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, мультимедиа, видео, звук, автозапуск
ms.custom: seodec18
ms.openlocfilehash: 39c9bd8e9921167dfc3a9ab1a4cc12b2157f0f6f
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "10942061"
---
# <span data-ttu-id="caf38-104">Политики автозапуска</span><span class="sxs-lookup"><span data-stu-id="caf38-104">Autoplay Policies</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="caf38-105">Microsoft Edge предоставляет клиентам возможность персонализировать параметры просмотра на веб-сайтах, которые автоматически воспроизводят мультимедиа, чтобы минимизировать отвлекающую информацию в Интернете и пропускную способность.</span><span class="sxs-lookup"><span data-stu-id="caf38-105">Microsoft Edge provides customers with the ability to personalize their browsing preferences on websites that autoplay media with sound in order to minimize distractions on the web and conserve bandwidth.</span></span>  <span data-ttu-id="caf38-106">Кроме того, Microsoft Edge автоматически запускает автоматическое воспроизведение мультимедиа на фоновых вкладках.</span><span class="sxs-lookup"><span data-stu-id="caf38-106">Additionally, Microsoft Edge automatically suppresses autoplay of media in background tabs.</span></span>  

<span data-ttu-id="caf38-107">Пользователи могут настраивать поведение мультимедиа, используя [глобальные](#global-media-autoplay-settings) элементы управления автозапуском и автозапуска, которые предоставляют следующие параметры: [per-site](#per-site-media-autoplay-settings)</span><span class="sxs-lookup"><span data-stu-id="caf38-107">Users can customize media behavior with both [global](#global-media-autoplay-settings) and [per-site](#per-site-media-autoplay-settings) autoplay controls, which provide the following options:</span></span>  

*   `Allow`  <span data-ttu-id="caf38-108">По умолчанию видео воспроизводятся при первом просмотре вкладки на переднем плане на переднем плане сайта.</span><span class="sxs-lookup"><span data-stu-id="caf38-108">The default and will continue to play videos when a tab is first viewed in the foreground, at the site's discretion.</span></span>  

*   `Limit`  <span data-ttu-id="caf38-109">Функция запретила воспроизведение видео только при отключении звука, поэтому звуковые файлы никогда не удлетворяют.</span><span class="sxs-lookup"><span data-stu-id="caf38-109">Restricts autoplay to only work when videos are muted, so users are never surprised by sound.</span></span>  <span data-ttu-id="caf38-110">Когда пользователь щелкнет в любом месте страницы, функция автозапуска снова включится и будет доступна в этом домене на этой вкладке.</span><span class="sxs-lookup"><span data-stu-id="caf38-110">Once the user clicks anywhere on the page, autoplay is re-enabled, and will continue to be allowed within that domain in that tab.</span></span>  

*   `Block`  <span data-ttu-id="caf38-111">Предотвращайте скорость воспроизведения на всех сайтах, пока пользователи не взаимодействуют с материалами мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="caf38-111">Prevent sautoplay on all sites until users directly interact with the media content.</span></span>  

## <span data-ttu-id="caf38-112">Настройки глобального медианы</span><span class="sxs-lookup"><span data-stu-id="caf38-112">Global media autoplay settings</span></span>  

<span data-ttu-id="caf38-113">Пользователи могут управлять поведением по умолчанию для всех сайтов с помощью функции **автозапуска мультимедиа.**  >  **Media autoplay**</span><span class="sxs-lookup"><span data-stu-id="caf38-113">Users can control the default autoplay behavior for all sites under **Advanced Setting** > **Media autoplay**.</span></span>  

:::image type="complex" source="../media/autoplay_global.png" alt-text="Настройки глобального медианы" lightbox="../media/autoplay_global.png":::
   <span data-ttu-id="caf38-115">Настройки глобального медианы</span><span class="sxs-lookup"><span data-stu-id="caf38-115">Global media autoplay settings</span></span>  
:::image-end:::  

## <span data-ttu-id="caf38-116">Параметры автозапуска мультимедиа на отдельном сайте</span><span class="sxs-lookup"><span data-stu-id="caf38-116">Per-site media autoplay settings</span></span>  

<span data-ttu-id="caf38-117">Пользователи могут управлять автоматическим воспроизведением **Website permissions** для каждого сайта в разделе "Разрешения для веб-сайта" области сведений о веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="caf38-117">Users can control autoplay behavior on a per-site basis under the **Website permissions** section of the website information pane.</span></span>  <span data-ttu-id="caf38-118">Для этого можно щелкнуть значок информации или значок блокировки в левой части адресной строки и выбрать параметры **автозапуска мультимедиа,** чтобы начать работу.</span><span class="sxs-lookup"><span data-stu-id="caf38-118">This setting can be found by clicking the information icon or lock icon on the left side of the address bar and clicking on **Media autoplay settings** to get started.</span></span>  

<span data-ttu-id="caf38-119">Переопределение глобального параметра на отдельном сайте переопределены.</span><span class="sxs-lookup"><span data-stu-id="caf38-119">Per-site settings override the global setting.</span></span>  <span data-ttu-id="caf38-120">Например, если для пользователя задан глобальный `Allow` параметр, но изменяет параметры на отдельном сайте на значение, автозапуск будет `Block` заблокирован.</span><span class="sxs-lookup"><span data-stu-id="caf38-120">For example, if a user has their global setting set to `Allow` but changes a per-site setting to `Block`, autoplay will be blocked for that site.</span></span>  

:::image type="complex" source="../media/autoplay_per-site.png" alt-text="Параметры автозапуска мультимедиа на отдельном сайте" lightbox="../media/autoplay_per-site.png":::
   <span data-ttu-id="caf38-122">Параметры автозапуска мультимедиа на отдельном сайте</span><span class="sxs-lookup"><span data-stu-id="caf38-122">Per-site media autoplay settings</span></span>  
:::image-end:::  

## <span data-ttu-id="caf38-123">Рекомендации по использованию веб-разработчиков</span><span class="sxs-lookup"><span data-stu-id="caf38-123">Best Practices for Web Developers</span></span>  

<span data-ttu-id="caf38-124">Вот как обеспечить удобство работы с мультимедиа, размещенными на сайте:</span><span class="sxs-lookup"><span data-stu-id="caf38-124">Here's how to ensure a good user experience with media hosted on your site:</span></span>  

*   <span data-ttu-id="caf38-125">Предположим, что для каждого использования элемента мультимедиа требуется жест пользователя начинать воспроизведение \(так как пользователи могут заблокировать автозапуск при каждом моменте времени\) и соответствовать планированию соответствует определенному планированию.</span><span class="sxs-lookup"><span data-stu-id="caf38-125">Assume each use of a media element wil require a user gesture to start the playback \(as users can block autoplay at any point in time\) and plan accordingly.</span></span>  <span data-ttu-id="caf38-126">Политики автоиграфики для каждого сайта применяются ко всем и элементам `<audio>` `<video>` независимо от того, как они используются на вашем сайте.</span><span class="sxs-lookup"><span data-stu-id="caf38-126">Global and per-site autoplay policies apply to all `<audio>` and `<video>` elements, regardless of how they are used on your site</span></span>  

*   <span data-ttu-id="caf38-127">Элементы управления мультимедиа всегда находятся на мультимедиа, так и по рекламной адаптации.</span><span class="sxs-lookup"><span data-stu-id="caf38-127">Ensure that media controls are always present on both site media and ad content.</span></span>  <span data-ttu-id="caf38-128">Это позволит пользователям перезапустить воспроизведение, если автозапуск заблокирован.</span><span class="sxs-lookup"><span data-stu-id="caf38-128">This will give users the ability to restart playback if autoplay is blocked on the page.</span></span>  

*   <span data-ttu-id="caf38-129">Оцените, как автоводит пользователей на вашем веб-сайте и воспроизводите их с помощью автозапуска, чтобы свести к минимуму нежелательные функции воспроизведения мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="caf38-129">Evaluate how autoplay may affect users' experience on your website and consider using autoplay in a way that minimizes unwanted media playback.</span></span>  <span data-ttu-id="caf38-130">Если автозапуск является важной частью вашего интерфейса, рекомендуем использовать отключенный контент для запуска и разрешить пользователю включить микрофон.</span><span class="sxs-lookup"><span data-stu-id="caf38-130">If autoplay is a crucial part of your experience, consider using muted content to start and allowing the user to unmute it.</span></span>  <span data-ttu-id="caf38-131">Чтобы содержимое отключено для автозапуска, для автозапуска необходимо явно выключить звук или не включить его.</span><span class="sxs-lookup"><span data-stu-id="caf38-131">For muted content to autoplay, the audio source must be either explicitly muted or not be set.</span></span>  <span data-ttu-id="caf38-132">В противном примере элемент не будет считаться отключенным.</span><span class="sxs-lookup"><span data-stu-id="caf38-132">Otherwise the element will not be considered as muted.</span></span>  

*   <span data-ttu-id="caf38-133">Используйте встроенные элементы управления браузером для воспроизведения мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="caf38-133">Unless absolutely necessary to do otherwise, use the native browser controls for media playback.</span></span>  <span data-ttu-id="caf38-134">Это обеспечит согласованное восприятие пользователей.</span><span class="sxs-lookup"><span data-stu-id="caf38-134">This will ensure a consistent experience for users.</span></span>  <span data-ttu-id="caf38-135">Если вы создаете пользовательские элементы управления мультимедиа, убедитесь, что элементы управления мультимедиа всегда вступили в силу и что элементы управления мультимедиа правильно воспроизводятся.</span><span class="sxs-lookup"><span data-stu-id="caf38-135">If you are building custom controls instead, ensure that media controls are always present and that your controls properly react to autoplay suppression.</span></span>  

### <span data-ttu-id="caf38-136">Делегирование iframe</span><span class="sxs-lookup"><span data-stu-id="caf38-136">Iframe delegation</span></span>  

<span data-ttu-id="caf38-137">Автозапуск в модуле наследующий способ написания разрешений от родительской страницы независимо от `<iframe>` источника контента.</span><span class="sxs-lookup"><span data-stu-id="caf38-137">Autoplay in an `<iframe>` will inherit the autoplay permission from the parent page regardless of content origin.</span></span>  <span data-ttu-id="caf38-138">В сценарии, содержащем каждый файл мультимедиа, размещенным отдельно iframe, пользователю нужно будет использовать воспроизведение для всего списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="caf38-138">In a playlist scenario where each media file is hosted by a separate iframe, the user would only need to initiate playback once for the entire playlist.</span></span>  

### <span data-ttu-id="caf38-139">Обнаружение случаев, когда автозапуск разрешено</span><span class="sxs-lookup"><span data-stu-id="caf38-139">Detecting when autoplay is allowed</span></span>  

<span data-ttu-id="caf38-140">Вы можете настроить элементы управления воспроизведением так, чтобы в нем правильно отображалось состояние, возвращаемое функцией в `play()` элементе мультимедиа:</span><span class="sxs-lookup"><span data-stu-id="caf38-140">You can adjust your playback controls to display the correct state when autoplay is blocked by examining the promise returned by the `play()` function on the media element:</span></span>  

```javascript
var promise = document.querySelector('video').play();

if (promise !== undefined) { 
    promise.catch(_error => { 
        // Autoplay was blocked
        // Show user media controls to manually start playback
    }).then(() => { 
        // Autoplay started
    }); 
}
```  
