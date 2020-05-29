---
title: Приступая к работе с эмуляторами Lane Surface удаленной отладки
author: zoherghadyali
ms.author: zoghadya
ms.date: 04/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, средства F12, Devtools, удаленная отладка, Android, Surface Duo
ms.openlocfilehash: af6fa6433b0bc6bba0599e6e9a805235504caadd
ms.sourcegitcommit: 966bfc60040acc794b6ee20eb2084bc8264a4852
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/05/2020
ms.locfileid: "10621504"
---
# <span data-ttu-id="f6677-103">Приступая к работе с эмуляторами Lane Surface удаленной отладки</span><span class="sxs-lookup"><span data-stu-id="f6677-103">Get Started with Remote Debugging Surface Duo emulators</span></span>

<span data-ttu-id="f6677-104">В этой статье описывается процесс удаленной отладки веб-содержимого в [приложении Microsoft Edge][AndroidEdge] на эмуляторе [Duo Surface][SurfaceDuo] из экземпляра [Microsoft Edge][DesktopEdge].</span><span class="sxs-lookup"><span data-stu-id="f6677-104">In this article, you walk through the process of remotely debugging your web content in the [Microsoft Edge app][AndroidEdge] on a [Surface Duo][SurfaceDuo] emulator from a desktop instance of [Microsoft Edge][DesktopEdge].</span></span> <span data-ttu-id="f6677-105">Информация о отладке на устройстве Surface Duo приведена в руководстве по [удаленным отладке устройств с Android][RemoteDebuggingAndroid].</span><span class="sxs-lookup"><span data-stu-id="f6677-105">For information on debugging on a Surface Duo device, follow our guide for [remote debugging Android devices][RemoteDebuggingAndroid].</span></span>

## <span data-ttu-id="f6677-106">Подготовка</span><span class="sxs-lookup"><span data-stu-id="f6677-106">Before you Begin</span></span>

<span data-ttu-id="f6677-107">Перед запуском [эмулятора Surface Duo][DuoEmulator]установите [пакет SDK Surface Duo][DuoSdk] .</span><span class="sxs-lookup"><span data-stu-id="f6677-107">Install the [Surface Duo SDK][DuoSdk] before running the [Surface Duo emulator][DuoEmulator].</span></span> <span data-ttu-id="f6677-108">Дополнительные сведения можно найти [в статьях скачать пакет SDK Surface Duo][DuoSdkdocs].</span><span class="sxs-lookup"><span data-stu-id="f6677-108">For more information, see [Get the Surface Duo SDK][DuoSdkdocs].</span></span>

## <span data-ttu-id="f6677-109">Шаг 1: переход в edge://inspect</span><span class="sxs-lookup"><span data-stu-id="f6677-109">Step 1: Navigate to edge://inspect</span></span>

<span data-ttu-id="f6677-110">Откройте классическое [приложение Microsoft Edge][DesktopEdge]и перейдите к нему `edge://inspect` .</span><span class="sxs-lookup"><span data-stu-id="f6677-110">Open a desktop instance of [Microsoft Edge][DesktopEdge], and navigate to `edge://inspect`.</span></span>

> ##### <span data-ttu-id="f6677-111">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="f6677-111">Figure 1</span></span>  
> <span data-ttu-id="f6677-112">`edge://inspect`Страница в Microsoft EDGE на рабочем столе — ![ страница Edge://inspect в Microsoft EDGE на рабочем столе][ImageEdgeInspect]</span><span class="sxs-lookup"><span data-stu-id="f6677-112">The `edge://inspect` page in Microsoft Edge on the desktop ![The edge://inspect page in Microsoft Edge on the desktop][ImageEdgeInspect]</span></span>

> [!NOTE]
> <span data-ttu-id="f6677-113">Если `edge://inspect` Страница не распознает [эмулятор Surface Duo][DuoEmulator], перезапустите эмулятор.</span><span class="sxs-lookup"><span data-stu-id="f6677-113">If the `edge://inspect` page does not recognize the [Surface Duo emulator][DuoEmulator], restart the emulator.</span></span>

## <span data-ttu-id="f6677-114">Шаг 2: Запуск эмулятора Surface Duo</span><span class="sxs-lookup"><span data-stu-id="f6677-114">Step 2: Launch the Surface Duo emulator</span></span>

<span data-ttu-id="f6677-115">Запустите [эмулятор Surface Duo][DuoEmulator].</span><span class="sxs-lookup"><span data-stu-id="f6677-115">Launch the [Surface Duo emulator][DuoEmulator].</span></span> <span data-ttu-id="f6677-116">Обратите внимание, что эмулятор отображает 2 разных экрана, запущенных в эмуляторе.</span><span class="sxs-lookup"><span data-stu-id="f6677-116">Notice that the emulator displays 2 different screens running on the emulator.</span></span>

> ##### <span data-ttu-id="f6677-117">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="f6677-117">Figure 2</span></span>
> <span data-ttu-id="f6677-118">Эмулятор Surface Duo ![ , эмулятор Surface Duo][ImageDuoEmulator]</span><span class="sxs-lookup"><span data-stu-id="f6677-118">The Surface Duo emulator ![The Surface Duo emulator][ImageDuoEmulator]</span></span>  

## <span data-ttu-id="f6677-119">Шаг 3. Загружайте веб-содержимое в Microsoft EDGE на эмулятор Surface Duo.</span><span class="sxs-lookup"><span data-stu-id="f6677-119">Step 3: Load your web content in Microsoft Edge on the Surface Duo emulator</span></span>

<span data-ttu-id="f6677-120">На любом экране проведите пальцем вверх по лотку "Избранное" [эмулятора Surface Duo][DuoEmulator] , чтобы отобразить ящик приложений.</span><span class="sxs-lookup"><span data-stu-id="f6677-120">On either screen, swipe up on the Favorites Tray of the [Surface Duo emulator][DuoEmulator] to display the Apps Drawer.</span></span> <span data-ttu-id="f6677-121">Выберите **Edge** , чтобы запустить [приложение Microsoft Edge][AndroidEdge].</span><span class="sxs-lookup"><span data-stu-id="f6677-121">Choose **Edge** to launch the [Microsoft Edge app][AndroidEdge].</span></span>

> ##### <span data-ttu-id="f6677-122">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="f6677-122">Figure 3</span></span>
> <span data-ttu-id="f6677-123">Приложение Microsoft EDGE в эмуляторе Lane Duo — ![ приложение Microsoft EDGE в эмуляторе Lane Duo][ImageDuoEmulatorEdge]</span><span class="sxs-lookup"><span data-stu-id="f6677-123">The Microsoft Edge app on the Surface Duo emulator ![The Microsoft Edge app on the Surface Duo emulator][ImageDuoEmulatorEdge]</span></span>  

<span data-ttu-id="f6677-124">Перейдите на веб-сайт или приложение, которое вы хотите отладить в [приложении Microsoft Edge][AndroidEdge].</span><span class="sxs-lookup"><span data-stu-id="f6677-124">Navigate to the website or app that you want to debug in the [Microsoft Edge app][AndroidEdge].</span></span>

## <span data-ttu-id="f6677-125">Шаг 4: Отладка содержимого веб-страницы в эмуляторе Duo Surface</span><span class="sxs-lookup"><span data-stu-id="f6677-125">Step 4: Debug your web content from the Surface Duo emulator</span></span> 

<span data-ttu-id="f6677-126">Вернитесь к экземпляру рабочего стола [Microsoft Edge][DesktopEdge].</span><span class="sxs-lookup"><span data-stu-id="f6677-126">Switch back to the desktop instance of [Microsoft Edge][DesktopEdge].</span></span> <span data-ttu-id="f6677-127">На `edge://inspect` странице теперь отображается **SurfaceDuoEmulator** со списком открытых вкладок или [PWAs][PwaDocs] , которые выполняются в [эмуляторе Duo Surface][DuoEmulator].</span><span class="sxs-lookup"><span data-stu-id="f6677-127">The `edge://inspect` page now shows the **SurfaceDuoEmulator** with a list of the open tabs or [PWAs][PwaDocs] that are running on the [Surface Duo emulator][DuoEmulator].</span></span>

> ##### <span data-ttu-id="f6677-128">Рисунок4</span><span class="sxs-lookup"><span data-stu-id="f6677-128">Figure 4</span></span>
> <span data-ttu-id="f6677-129">На `edge://inspect` странице отображается список вкладок в приложении Microsoft EDGE, работающем на эмуляторе. на ![ странице Edge://inspect отображается список открытых вкладок приложения Microsoft EDGE, запущенного на эмуляторе.][ImageEdgeInspectTargets]</span><span class="sxs-lookup"><span data-stu-id="f6677-129">The `edge://inspect` page displays a list of the open tabs in the Microsoft Edge app running on the emulator ![The edge://inspect page displays a list of the open tabs in the Microsoft Edge app running on the emulator][ImageEdgeInspectTargets]</span></span>  

> [!NOTE]
> <span data-ttu-id="f6677-130">Если вы не видите **SurfaceDuoEmulator** на `edge://inspect` странице, попробуйте открыть или закрыть вкладки в [приложении Microsoft Edge][AndroidEdge] в [эмуляторе Duo Surface][DuoEmulator].</span><span class="sxs-lookup"><span data-stu-id="f6677-130">If you do not see **SurfaceDuoEmulator** on the `edge://inspect` page, try opening or closing tabs in the [Microsoft Edge app][AndroidEdge] on the [Surface Duo Emulator][DuoEmulator].</span></span> <span data-ttu-id="f6677-131">Дополнительные действия по устранению неполадок можно найти в [разделе Устранение неполадок устройств с Android][TroubleshootingAndroid].</span><span class="sxs-lookup"><span data-stu-id="f6677-131">For additional troubleshooting steps, see the [troubleshooting section for Android devices][TroubleshootingAndroid].</span></span>

<span data-ttu-id="f6677-132">В списке открытых вкладок, запущенных в эмуляторе, на вкладке, где находится веб-содержимое для отладки, нажмите кнопку **проверить** .</span><span class="sxs-lookup"><span data-stu-id="f6677-132">From the list of open tabs running on the emulator, choose **inspect** on the tab that has the web content to be debugged.</span></span> <span data-ttu-id="f6677-133">[Приложение Microsoft Edge DevTools][DevToolsDocs] откроется в новом окне.</span><span class="sxs-lookup"><span data-stu-id="f6677-133">The [Microsoft Edge DevTools][DevToolsDocs] will open in a new window.</span></span> <span data-ttu-id="f6677-134">Нажмите **кнопку Переключить** презентацию ![ ][ImageToggleScreencastIcon] , чтобы просмотреть веб-содержимое в [эмуляторе Duo Surface][DuoEmulator] в окне DevTools.</span><span class="sxs-lookup"><span data-stu-id="f6677-134">Choose **Toggle Screencast** ![Toggle Screencast][ImageToggleScreencastIcon] to view the web content from your [Surface Duo emulator][DuoEmulator] in the DevTools window.</span></span> <span data-ttu-id="f6677-135">Теперь вы можете использовать Microsoft Edge DevTools для отладки вашего веб-содержимого в [эмуляторе Surface Duo][DuoEmulator].</span><span class="sxs-lookup"><span data-stu-id="f6677-135">You are now able to use the Microsoft Edge DevTools to debug your web content on the [Surface Duo emulator][DuoEmulator].</span></span>

> ##### <span data-ttu-id="f6677-136">Рисунок 5</span><span class="sxs-lookup"><span data-stu-id="f6677-136">Figure 5</span></span>
> <span data-ttu-id="f6677-137">Использование Microsoft Edge DevTools для отладки Bing в приложении Microsoft EDGE в эмуляторе Surface Duo ![ с помощью Microsoft Edge DevTools для отладки Bing в приложении Microsoft EDGE в эмуляторе Surface Duo][ImageDevTools]</span><span class="sxs-lookup"><span data-stu-id="f6677-137">Using the Microsoft Edge DevTools to debug Bing in the Microsoft Edge app on the Surface Duo emulator ![Using the Microsoft Edge DevTools to debug Bing in the Microsoft Edge app on the Surface Duo emulator][ImageDevTools]</span></span>  

> [!NOTE]
> <span data-ttu-id="f6677-138">Если вы зайдете [приложение Microsoft Edge][AndroidEdge] на обоих экранах эмулятора, она будет показывать новый размер приложения, но не на шарнир.</span><span class="sxs-lookup"><span data-stu-id="f6677-138">If you span the [Microsoft Edge app][AndroidEdge] across both screens in the emulator, the screencast will reflect the new size of the app but not the hinge.</span></span> <span data-ttu-id="f6677-139">Чтобы понять, как шарнирный элемент влияет на макет вашего веб-содержимого, используйте [эмулятор Surface Duo][DuoEmulator] вместо ролика.</span><span class="sxs-lookup"><span data-stu-id="f6677-139">To understand how the hinge impacts the layout of your web content, use the [Surface Duo emulator][DuoEmulator] instead of the screencast.</span></span>

## <span data-ttu-id="f6677-140">Дополнительные ресурсы</span><span class="sxs-lookup"><span data-stu-id="f6677-140">Additional Resources</span></span>

<span data-ttu-id="f6677-141">Интернет — это замечательная платформа для нового класса складная и устройств с двумя экранами, так как вы можете создавать HTML, CSS и JavaScript один раз, чтобы они выглядели хорошо на одном экране, на двух экранах и на складная устройствах.</span><span class="sxs-lookup"><span data-stu-id="f6677-141">The web is a great platform for the new class of foldable and dual-screen devices because you can write your HTML, CSS, and JavaScript once and have it look great across single-screen, dual-screen, and foldable devices.</span></span> <span data-ttu-id="f6677-142">Дополнительные сведения можно найти в разделе Дополнительные ресурсы, чтобы приступить к созданию веб-содержимого для новых устройств.</span><span class="sxs-lookup"><span data-stu-id="f6677-142">For more information, see these additional resources to get started building web content for these new devices.</span></span>

- [<span data-ttu-id="f6677-143">Документация по созданию приложений на устройствах с двумя экранами</span><span class="sxs-lookup"><span data-stu-id="f6677-143">Documentation for creating apps on dual-screen devices</span></span>][DualScreenDocs]
- [<span data-ttu-id="f6677-144">Веб-платформа Microsoft Edge для новых API для создания веб-взаимодействия на складная и на устройствах с двумя мониторами</span><span class="sxs-lookup"><span data-stu-id="f6677-144">The Microsoft Edge web platform explainer for new APIs to build web experiences on foldable and dual-screen devices</span></span>][WebPlatformExplainer]
- [<span data-ttu-id="f6677-145">Запись рабочего сеанса Microsoft 365 для разработчиков: создание двух экранных возможностей для веб-сайтов и веб-приложений</span><span class="sxs-lookup"><span data-stu-id="f6677-145">Recording of Microsoft 365 Developer Day session: How to build dual-screen experiences for websites and web apps</span></span>][DeveloperDay]

<!-- image links -->  
[ImageEdgeInspect]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-surface-duo-inspect-page.msft.png "Рисунок 1: страница edge://inspect в Microsoft EDGE на рабочем столе"
[ImageDuoEmulator]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-surface-duo-emulator.msft.png "Рисунок 2: эмулятор Surface Duo"
[ImageDuoEmulatorEdge]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-surface-duo-emulator-edge.msft.png "Рисунок 3: приложение Microsoft EDGE в эмуляторе Lane Duo"
[ImageEdgeInspectTargets]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png "Рисунок 4: страница edge://inspect отображает список открытых вкладок приложения Microsoft EDGE, запущенного на эмуляторе."
[ImageToggleScreencastIcon]: images/toggle-screencast-icon.msft.png
[ImageDevTools]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-surface-duo-devtools.msft.png "Рисунок 5: использование Microsoft Edge DevTools для отладки Bing в приложении Microsoft EDGE в эмуляторе Lane Duo"

<!-- links -->  
[RemoteDebuggingAndroid]: /microsoft-edge/devtools-guide-chromium/remote-debugging/index "Начало работы с удаленными отладкой устройств с Android"
[PwaDocs]: /microsoft-edge/progressive-web-apps-chromium/index "Прогрессивные веб-приложения для Windows"
[DevToolsDocs]: /microsoft-edge/devtools-guide-chromium "Инструменты разработчика Microsoft EDGE (Chromium)"
[TroubleshootingAndroid]: /microsoft-edge/devtools-guide-chromium/remote-debugging/index#troubleshooting-devtools-is-not-detecting-the-android-device "Устранение неполадок: DevTools не может обнаружить устройство с Android"

[AndroidEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Приложение Microsoft Edge для Android"
[SurfaceDuo]: https://www.microsoft.com/surface/devices/surface-duo "Знакомство с Surface Duo"
[DesktopEdge]: https://www.microsoft.com/edge/ "Знакомство с новым Microsoft Edge"
[DuoEmulator]: https://docs.microsoft.com/dual-screen/android/use-emulator "Использование эмулятора Surface DUo"
[DuoSdk]: https://www.microsoft.com/download/details.aspx?id=100847 "Предварительная версия SDK Surface Duo"
[DuoSdkDocs]: https://docs.microsoft.com/dual-screen/android/get-duo-sdk "Скачать пакет SDK Surface Duo"
[DualScreenDocs]: https://docs.microsoft.com/dual-screen/ "Создание приложений для устройств с двумя экранами"
[WebPlatformExplainer]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/master/Foldables/explainer.md "Примитивы веб-платформ для Грамотногоных функций на складная устройствах"
[DeveloperDay]: https://youtu.be/DXrZWsqXPVc "Создание возможностей двустороннего экрана для веб-сайтов и Интернет-приложений"
