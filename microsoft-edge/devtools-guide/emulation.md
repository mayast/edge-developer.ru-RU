---
description: Использование панели эмуляции для проверки различных профилей браузера, размеров экрана и разрешения и координат местоположения GPS
title: DevTools — Эмуляция
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools, эмуляция устройств, разработка с откликом, географическое расположение, разрешение
ms.custom: seodec18
ms.openlocfilehash: d66646600aeaac279acaf622527f829c69f33286
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571771"
---
# <span data-ttu-id="6d1c3-104">Эмуляции</span><span class="sxs-lookup"><span data-stu-id="6d1c3-104">Emulation</span></span>

<span data-ttu-id="6d1c3-105">С помощью панели *эмуляции* вы можете выполнять следующие действия:</span><span class="sxs-lookup"><span data-stu-id="6d1c3-105">The *Emulation* panel helps you to:</span></span>
 - <span data-ttu-id="6d1c3-106">Имитировать различные [профили устройств](#device), [браузеры](#browser-profile), [размеры экрана и разрешения](#display)</span><span class="sxs-lookup"><span data-stu-id="6d1c3-106">Simulate various [device profiles](#device), [browsers](#browser-profile), [screen sizes and resolutions](#display)</span></span>
 - <span data-ttu-id="6d1c3-107">Проверка различных [параметров и координат географического положения](#geolocation)</span><span class="sxs-lookup"><span data-stu-id="6d1c3-107">Test different [geolocation settings and coordinates](#geolocation)</span></span>

![Панель эмуляции DevTools Microsoft Edge](./media/emulation.png)

1. <span data-ttu-id="6d1c3-109">Кнопка Сохранить **параметры эмуляции** сохранит все изменения, внесенные в параметры эмуляции рабочего стола по умолчанию, даже если вы закроете и снова откроете DevTools.</span><span class="sxs-lookup"><span data-stu-id="6d1c3-109">The **Persist Emulation settings** button will save any changes you made from the default desktop emulation settings, even when you close and reopen the DevTools.</span></span> 

2. <span data-ttu-id="6d1c3-110">Кнопка **Сброс параметров эмуляции** сбрасывает параметры эмуляции в профиль *рабочего стола* по умолчанию и строку агента пользователя Microsoft Edge с отключенным параметром GPS.</span><span class="sxs-lookup"><span data-stu-id="6d1c3-110">The **Reset Emulation settings** button will reset your emulation settings back to the default *Desktop* browser profile and Microsoft Edge user agent string with GPS turned off.</span></span>

3. <span data-ttu-id="6d1c3-111">Если какие-либо из этих параметров будут изменены по умолчанию, на вкладке **Эмуляция** появится информационное оповещение о том, что некоторые аспекты поведения браузера эмулируется.</span><span class="sxs-lookup"><span data-stu-id="6d1c3-111">When any of these options are changed from the default, the **Emulation** tab will show an informational alert to indicate that some aspect of your browser's behavior is being emulated.</span></span>

## <span data-ttu-id="6d1c3-112">Устройство</span><span class="sxs-lookup"><span data-stu-id="6d1c3-112">Device</span></span>

<span data-ttu-id="6d1c3-113">Выберите стандартный список профилей устройств Windows, которые автоматически настраивают другие параметры эмуляции или определяют собственные *пользовательские* configuation.</span><span class="sxs-lookup"><span data-stu-id="6d1c3-113">Pick from a preset list of Windows device profiles which  automatically configure the other emulation options or specify your own *Custom* configuation.</span></span> <span data-ttu-id="6d1c3-114">Чтобы сбросить все средства эмуляции, вернитесь к параметру *Default* .</span><span class="sxs-lookup"><span data-stu-id="6d1c3-114">Switch back to *Default* to reset all the emulation tools.</span></span>

## <span data-ttu-id="6d1c3-115">Режим</span><span class="sxs-lookup"><span data-stu-id="6d1c3-115">Mode</span></span>

### <span data-ttu-id="6d1c3-116">Профиль браузера</span><span class="sxs-lookup"><span data-stu-id="6d1c3-116">Browser profile</span></span>
<span data-ttu-id="6d1c3-117">Для имитации страницы, работающей на устройстве с Windows Phone, можно быстро изменить параметр **профиля браузера** на *Windows Phone*.</span><span class="sxs-lookup"><span data-stu-id="6d1c3-117">A quick way to simulate your page running on a Windows Phone device is to change the **Browser profile** setting to *Windows Phone*.</span></span>

#### <span data-ttu-id="6d1c3-118">Строка агента пользователя</span><span class="sxs-lookup"><span data-stu-id="6d1c3-118">User agent string</span></span>

<span data-ttu-id="6d1c3-119">Изменение строки агента пользователя для имитации другого браузера — это хороший первый шаг в ошибках отладки, происходящих только в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6d1c3-119">Modifying your user agent string to mimic another browser is a good first step in debugging errors that are only happening in Microsoft Edge.</span></span> 

<span data-ttu-id="6d1c3-120">Кроме того, сценарии переднего плана и/или серверного интерфейса иногда используют строку агента пользователя, чтобы определить, какой браузер вы используете.</span><span class="sxs-lookup"><span data-stu-id="6d1c3-120">Front end and/or back end scripts sometimes use the user agent string  to detect which browser you're using.</span></span> <span data-ttu-id="6d1c3-121">И даже если вы не используете определение браузера в собственном коде, возможно, вы используете библиотеку JavaScript стороннего поставщика или серверный сценарий.</span><span class="sxs-lookup"><span data-stu-id="6d1c3-121">And even when you're not using browser detection in your own code, you may be using a third-party JavaScript library or server-side script that does.</span></span>

<span data-ttu-id="6d1c3-122">Проблема с обнаружением браузеров состоит в том, что она часто используется для изменения масштаба или изменений на веб-странице в зависимости от того, что разработчик может сделать, чтобы ваш браузер мог использовать обнаружение компонентов.</span><span class="sxs-lookup"><span data-stu-id="6d1c3-122">The problem with browser detection is that it's often used to scale back or change the features in a webpage based on what the developer writing the script thinks your browser can do, rather than detecting what your browser can actually do using feature detection.</span></span> <span data-ttu-id="6d1c3-123">Это может привести к неожиданному поведению, поскольку код, предназначенный для Windows Internet Explorer 8, может существенно затруднить работу в Microsoft Edge. или функция, которую браузер вполне способен поддерживать, может быть отключена из-за предположения, сделанного разработчиком.</span><span class="sxs-lookup"><span data-stu-id="6d1c3-123">This can cause unexpected behavior, because code targeted at Windows Internet Explorer 8 can run very differently in Microsoft Edge; or a feature your browser is perfectly capable of supporting might be disabled because of an assumption made by the developer.</span></span>

<span data-ttu-id="6d1c3-124">Если при изменении строки агента пользователя происходит удаление проблемы, обнаружение браузера, возможно, будет заблокировано.</span><span class="sxs-lookup"><span data-stu-id="6d1c3-124">If changing your user agent string clears up the problem, browser detection is likely culprit.</span></span>

## <span data-ttu-id="6d1c3-125">Монитор</span><span class="sxs-lookup"><span data-stu-id="6d1c3-125">Display</span></span>

<span data-ttu-id="6d1c3-126">Эмуляция экрана позволяет предварительно просматривать сайты на разных устройствах и разрешениях: от обычных мониторов до уменьшенных экранов и более современных дисплеев с высоким разрешением.</span><span class="sxs-lookup"><span data-stu-id="6d1c3-126">Display emulation lets you preview your site on different screen sizes and resolutions: from conventional desktop monitors to smaller mobile screens or newer high-resolution displays.</span></span>

<span data-ttu-id="6d1c3-127">Эмуляции приспособлены к попытайтесь и соответствуют физическим измерениям экранов, для которых выполняется эмуляция.</span><span class="sxs-lookup"><span data-stu-id="6d1c3-127">Emulations are adapted to try and match the physical dimensions of the screens being emulated.</span></span> <span data-ttu-id="6d1c3-128">Эмулированные Пиксели могут выглядеть как сжатые или развернутые, а эмуляция не рекомендуется, если необходимо протестировать точечное расположение элементов HTML.</span><span class="sxs-lookup"><span data-stu-id="6d1c3-128">Emulated pixels might appear compressed or expanded, and emulation is not recommended if you need to test pixel-perfect positioning of HTML elements.</span></span> <span data-ttu-id="6d1c3-129">Однако Эмуляция, тем не менее, хорошо подходит для тестирования и выявления более крупных проблем, связанных с размещением элементов.</span><span class="sxs-lookup"><span data-stu-id="6d1c3-129">Emulation is, however, good for testing responsive designs and identifying larger element positioning issues.</span></span>

### <span data-ttu-id="6d1c3-130">Ориентация</span><span class="sxs-lookup"><span data-stu-id="6d1c3-130">Orientation</span></span>

<span data-ttu-id="6d1c3-131">Выберите режим *Альбомная* или *Книжная* .</span><span class="sxs-lookup"><span data-stu-id="6d1c3-131">Choose from *Landscape* or *Portrait* mode.</span></span>

### <span data-ttu-id="6d1c3-132">Разрешение</span><span class="sxs-lookup"><span data-stu-id="6d1c3-132">Resolution</span></span>

<span data-ttu-id="6d1c3-133">Выберите готовый набор разрешений для устройства или укажите собственный *Настраиваемый* файл конфигурации. Поддерживаются разрешения до 80 дюйма и 3820 x 2160.</span><span class="sxs-lookup"><span data-stu-id="6d1c3-133">Choose from a preset list of popular device resolutions, or specify your own *Custom* config. Resolutions of up to 80 inches and 3820 x 2160 are supported.</span></span>

## <span data-ttu-id="6d1c3-134">Геолокация</span><span class="sxs-lookup"><span data-stu-id="6d1c3-134">Geolocation</span></span>

<span data-ttu-id="6d1c3-135">Если ваш веб-сайт использует [API географического расположения](https://developer.mozilla.org/docs/Web/API/Geolocation/Using_geolocation) для предоставления услуг на основе местоположения, вы можете легко проверить различные координаты GPS и состояние датчиков на рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="6d1c3-135">If your site uses the [Geolocation API](https://developer.mozilla.org/docs/Web/API/Geolocation/Using_geolocation) to provide location-based services, you can easily test different GPS coordinates and sensor states from the convenience of your desktop.</span></span> <span data-ttu-id="6d1c3-136">Эти параметры переопределят любые фактические координаты GPS и состояние датчика на компьютерах, которые поддерживают географическое расположение.</span><span class="sxs-lookup"><span data-stu-id="6d1c3-136">These settings will override any actual GPS coordinates and the sensor state on machines that support geolocation.</span></span> 

<span data-ttu-id="6d1c3-137">Как и при использовании личных данных в Интернете, пользователи должны будут предоставлять разрешение на доступ к своему местоположению.</span><span class="sxs-lookup"><span data-stu-id="6d1c3-137">As with any usage of personal data on the web, your users will first need to grant your site permission to use their location.</span></span> <span data-ttu-id="6d1c3-138">Вы можете проверить работу сайта с разрешениями расположения и без него на панели *параметров* Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="6d1c3-138">You can test how your site behaves with and without location permissions from the Microsoft Edge *Settings* panel:</span></span>

<span data-ttu-id="6d1c3-139">**...** >  **Параметры**  >  **Просмотр дополнительных параметров**  >  Разрешения для веб **-сайта**  >  **Управление**</span><span class="sxs-lookup"><span data-stu-id="6d1c3-139">**...** > **Settings** > **View advanced settings** > **Website permissions** > **Manage**</span></span>

![Управление разрешениями веб-сайта с помощью панели "параметры Microsoft Edge"](./media/settings_manage_permissions.png)

## <span data-ttu-id="6d1c3-141">Горячие</span><span class="sxs-lookup"><span data-stu-id="6d1c3-141">Shortcuts</span></span>

| <span data-ttu-id="6d1c3-142">Действие</span><span class="sxs-lookup"><span data-stu-id="6d1c3-142">Action</span></span>                   | <span data-ttu-id="6d1c3-143">Появивше</span><span class="sxs-lookup"><span data-stu-id="6d1c3-143">Shortcut</span></span>               |
|:-------------------------|:-----------------------|
| <span data-ttu-id="6d1c3-144">Сброс параметров эмуляции</span><span class="sxs-lookup"><span data-stu-id="6d1c3-144">Reset Emulation settings</span></span> | `CTRL` + `SHIFT` + `L` |
