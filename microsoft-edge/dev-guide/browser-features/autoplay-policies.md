---
description: Убедитесь в том, что содержимое мультимедиа на вашем сайте является предполагаемым.
title: 'Руководство по разработке: политики автозапуска'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 9/17/2018
ms.topic: article
ms.prod: microsoft-edge
keywords: EDGE, мультимедиа, видео, звук, автозапуск
ms.custom: seodec18
ms.openlocfilehash: 397c6f0a22359dbfab7c44370b0429147b7c9834
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10570902"
---
# <span data-ttu-id="7415c-104">Политики автозапуска</span><span class="sxs-lookup"><span data-stu-id="7415c-104">Autoplay Policies</span></span>

<span data-ttu-id="7415c-105">Microsoft Edge предоставляет пользователям возможность персонализировать настройки браузера на веб-сайтах, которые перезапускают мультимедиа с помощью звука, чтобы свести к минимуму количество отвлекающих на веб-сайте и экономить пропускную способность.</span><span class="sxs-lookup"><span data-stu-id="7415c-105">Microsoft Edge provides customers with the ability to personalize their browsing preferences on websites that autoplay media with sound in order to minimize distractions on the web and conserve bandwidth.</span></span> <span data-ttu-id="7415c-106">Дополнительно Microsoft EDGE автоматически запрещает Автозапуск мультимедиа в закладках на фоне.</span><span class="sxs-lookup"><span data-stu-id="7415c-106">Additionaly, Microsoft Edge automatically suppresses autoplay of media in background tabs.</span></span>

<span data-ttu-id="7415c-107">Пользователи могут настраивать параметры поведения мультимедиа как для [глобальных](#global-media-autoplay-settings) , так и [для отдельных](#per-site-media-autoplay-settings) элементов управления, которые предоставляют следующие возможности.</span><span class="sxs-lookup"><span data-stu-id="7415c-107">Users can customize media behavior with both [global](#global-media-autoplay-settings) and [per-site](#per-site-media-autoplay-settings) autoplay controls, which provide the following options:</span></span>

- <span data-ttu-id="7415c-108">" **Разрешить** " — используется по умолчанию и продолжает воспроизводить видео при первом просмотре вкладки на переднем плане на усмотрение сайта.</span><span class="sxs-lookup"><span data-stu-id="7415c-108">**Allow**  is the default and will continue to play videos when a tab is first viewed in the foreground, at the site’s discretion.</span></span>

- <span data-ttu-id="7415c-109">" **Ограничить** ", чтобы автозапуск работал только при выключенном видеоролике, так что пользователи не будут удивлены звуковым сигналом.</span><span class="sxs-lookup"><span data-stu-id="7415c-109">**Limit** will restrict autoplay to only work when videos are muted, so users are never surprised by sound.</span></span> <span data-ttu-id="7415c-110">Когда пользователь щелкает на странице в любом месте, автозапуск повторно включается, и на этой вкладке он по-прежнему будет разрешен в этом домене.</span><span class="sxs-lookup"><span data-stu-id="7415c-110">Once the user clicks anywhere on the page, autoplay is re-enabled, and will continue to be allowed within that domain in that tab.</span></span>

- <span data-ttu-id="7415c-111">**Запрещает** автозапуск на всех сайтах, пока пользователи не будут напрямую взаимодействовать с содержимым мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7415c-111">**Block** will prevent autoplay on all sites until users directly interact with the media content.</span></span>

## <span data-ttu-id="7415c-112">Параметры автозапуска для глобальных файлов мультимедиа</span><span class="sxs-lookup"><span data-stu-id="7415c-112">Global media autoplay settings</span></span>

<span data-ttu-id="7415c-113">Пользователи могут управлять поведением автоматического запуска по умолчанию для всех сайтов в разделе **Дополнительные параметры**  >  **автозапуска мультимедиа**.</span><span class="sxs-lookup"><span data-stu-id="7415c-113">Users can control the default autoplay behavior for all sites under **Advanced Setting** > **Media autoplay**.</span></span>

![Параметры автозапуска для глобальных файлов мультимедиа](../media/autoplay_global.png)

## <span data-ttu-id="7415c-115">Параметры автозапуска мультимедиа для отдельных сайтов</span><span class="sxs-lookup"><span data-stu-id="7415c-115">Per-site media autoplay settings</span></span>

<span data-ttu-id="7415c-116">Пользователи могут управлять поведением автозапуск на уровне отдельных сайтов в разделе " **разрешения** для веб-сайта" в области "сведения о веб-сайте".</span><span class="sxs-lookup"><span data-stu-id="7415c-116">Users can control autoplay behavior on a per-site basis under the **Website permissions** section of the website information pane.</span></span> <span data-ttu-id="7415c-117">Этот параметр можно найти, щелкнув значок "сведения" или значок замка в левой части адресной строки и выбрав пункт "Параметры автозапуска мультимедиа", чтобы приступить к работе.</span><span class="sxs-lookup"><span data-stu-id="7415c-117">This setting can be found by clicking the information icon or lock icon on the left side of the address bar and clicking on “Media autoplay settings” to get started.</span></span>

<span data-ttu-id="7415c-118">Параметры на уровне сайта переопределяют глобальный параметр.</span><span class="sxs-lookup"><span data-stu-id="7415c-118">Per-site settings override the global setting.</span></span> <span data-ttu-id="7415c-119">Например, если для пользователя задано значение "разрешить", но для параметра "на уровне сайта" выбрано значение "блокировать", автозапуск будет заблокирован для этого сайта.</span><span class="sxs-lookup"><span data-stu-id="7415c-119">For example, if a user has their global setting set to “Allow” but changes a per-site setting to “Block”, autoplay will be blocked for that site.</span></span>

![Параметры автозапуска мультимедиа для отдельных сайтов](../media/autoplay_per-site.png)
 
## <span data-ttu-id="7415c-121">Рекомендации для веб-разработчиков</span><span class="sxs-lookup"><span data-stu-id="7415c-121">Best Practices for Web Developers</span></span>

<span data-ttu-id="7415c-122">Ниже показано, как обеспечить оптимальное взаимодействие пользователей с мультимедиа на вашем сайте.</span><span class="sxs-lookup"><span data-stu-id="7415c-122">Here's how to ensure a good user experience with media hosted on your site:</span></span>

- <span data-ttu-id="7415c-123">Предположим, что для каждого использования мультимедийного элемента будет требуется жест пользователя, чтобы начать воспроизведение (поскольку пользователи могут блокировать Автозапуск в любой момент времени) и планировать соответствующим образом.</span><span class="sxs-lookup"><span data-stu-id="7415c-123">Assume  each use of a media element wil require a user gesture to start the playback (as users can block autoplay at any point in time) and plan accordingly.</span></span>  <span data-ttu-id="7415c-124">Глобальные политики для автозапуска и включения на уровне сайта применяются ко всем `<audio>` и `<video>` элементам независимо от того, как они используются на вашем сайте.</span><span class="sxs-lookup"><span data-stu-id="7415c-124">Global and per-site autoplay policies apply to all `<audio>` and `<video>` elements, regardless of how they are used on your site</span></span>

- <span data-ttu-id="7415c-125">Убедитесь, что элементы управления мультимедиа всегда присутствуют на обоих носителях сайта и рекламном контенте.</span><span class="sxs-lookup"><span data-stu-id="7415c-125">Ensure that media controls are always present on both site media and ad content.</span></span> <span data-ttu-id="7415c-126">Таким образом пользователи смогут перезапустить воспроизведение, если на странице заблокирован автозапуск.</span><span class="sxs-lookup"><span data-stu-id="7415c-126">This will give users the ability to restart playback if autoplay is blocked on the page.</span></span>

- <span data-ttu-id="7415c-127">Определите, как автозапуск может повлиять на работу пользователей на вашем веб-сайте, и используйте автозапуск таким образом, чтобы свести к минимуму воспроизведение нежелательного мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7415c-127">Evaluate how autoplay may affect users’ experience on your website and consider using autoplay in a way that minimizes unwanted media playback.</span></span> <span data-ttu-id="7415c-128">Если функция "Автозапуск" является важной частью вашего опыта, вы можете использовать отключенное содержимое, чтобы включить его и разрешить пользователю включать микрофон.</span><span class="sxs-lookup"><span data-stu-id="7415c-128">If autoplay is a crucial part of your experience, consider using muted content to start and allowing the user to unmute it.</span></span> <span data-ttu-id="7415c-129">Чтобы отключить автозапуск содержимого для автозапуска, источник звука должен быть либо явно отключен, либо не был установлен.</span><span class="sxs-lookup"><span data-stu-id="7415c-129">For muted content to autoplay, the audio source must be either explicitly muted or not be set.</span></span> <span data-ttu-id="7415c-130">В противном случае элемент не будет рассматриваться как отключенный.</span><span class="sxs-lookup"><span data-stu-id="7415c-130">Otherwise the element will not be considered as muted.</span></span>

- <span data-ttu-id="7415c-131">Если нет необходимости в других случаях, используйте собственные элементы управления браузера для воспроизведения мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="7415c-131">Unless absolutely necessary to do otherwise, use the native browser controls for media playback.</span></span> <span data-ttu-id="7415c-132">Это обеспечит постоянную работу пользователей.</span><span class="sxs-lookup"><span data-stu-id="7415c-132">This will ensure a consistent experience for users.</span></span> <span data-ttu-id="7415c-133">Если вы собираетесь создать пользовательские элементы управления, убедитесь в том, что элементы управления мультимедиа всегда присутствуют и что элементы управления правильно реагируют на отключение автозапуска.</span><span class="sxs-lookup"><span data-stu-id="7415c-133">If you are building custom controls instead, ensure that media controls are always present and that your controls properly react to autoplay suppression.</span></span>

### <span data-ttu-id="7415c-134">Делегирование IFRAME</span><span class="sxs-lookup"><span data-stu-id="7415c-134">Iframe delegation</span></span>

<span data-ttu-id="7415c-135">Автозапуск в интерфейсе `<iframe>` будет наследовать разрешение на автозапуск от родительской страницы независимо от происхождения содержимого.</span><span class="sxs-lookup"><span data-stu-id="7415c-135">Autoplay in an `<iframe>` will inherit the autoplay permission from the parent page regardless of content origin.</span></span> <span data-ttu-id="7415c-136">В сценарии воспроизведения, в котором каждый файл мультимедиа размещается на отдельном интернет-кадре, пользователю потребуется только один раз запустить воспроизведение для всего списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="7415c-136">In a playlist scenario where each media file is hosted by a separate iframe, the user would only need to initiate playback once for the entire playlist.</span></span>

### <span data-ttu-id="7415c-137">Определение того, разрешено ли автозапуск</span><span class="sxs-lookup"><span data-stu-id="7415c-137">Detecting when autoplay is allowed</span></span>

<span data-ttu-id="7415c-138">Вы можете настроить элементы управления воспроизведением так, чтобы оно отображало правильное состояние, когда автозапуск заблокирован, проверив обещание, возвращенное `play()` функцией на мультимедийном элементе:</span><span class="sxs-lookup"><span data-stu-id="7415c-138">You can adjust your playback controls to display the correct state when autoplay is blocked by examining the promise returned by the `play()` function on the media element:</span></span>

```Javascript

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
