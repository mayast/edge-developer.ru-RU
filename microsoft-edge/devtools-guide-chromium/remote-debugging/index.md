---
title: Начало работы с удаленными отладкой устройств с Android
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: c77633c4844f0e576b7dff6574000a78c8c083da
ms.sourcegitcommit: f010f43604bd4363af6827f79dbc071b9afcb667
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2020
ms.locfileid: "10708538"
---
<!-- Copyright Kayce Basques 

   Licensed under the Apache License, Version 2.0 (the "License");
   you may not use this file except in compliance with the License.
   You may obtain a copy of the License at

       https://www.apache.org/licenses/LICENSE-2.0

   Unless required by applicable law or agreed to in writing, software
   distributed under the License is distributed on an "AS IS" BASIS,
   WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
   See the License for the specific language governing permissions and
   limitations under the License.  -->  

# <span data-ttu-id="5e29d-103">Начало работы с удаленными отладкой устройств с Android</span><span class="sxs-lookup"><span data-stu-id="5e29d-103">Get started with remote debugging Android devices</span></span>  

<span data-ttu-id="5e29d-104">Удаленная отладка динамического содержимого на устройстве Android с компьютера Windows или macOS.</span><span class="sxs-lookup"><span data-stu-id="5e29d-104">Remote debug live content on an Android device from your Windows or macOS computer.</span></span>  <span data-ttu-id="5e29d-105">На следующей странице учебника вы узнаете, как выполнять указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="5e29d-105">The following tutorial page teaches you how to complete the following actions.</span></span>  

*   <span data-ttu-id="5e29d-106">Настройте устройство Android для удаленной отладки и найдите его на компьютере разработчика.</span><span class="sxs-lookup"><span data-stu-id="5e29d-106">Set up your Android device for remote debugging, and discover it from your development machine.</span></span>  
*   <span data-ttu-id="5e29d-107">Изучите и отлаживать динамический контент на устройстве с Android с компьютера для разработки.</span><span class="sxs-lookup"><span data-stu-id="5e29d-107">Inspect and debug live content on your Android device from your development machine.</span></span>  
*   <span data-ttu-id="5e29d-108">Содержимое ролика с устройства Android на экземпляр DevTools на компьютере разработчика.</span><span class="sxs-lookup"><span data-stu-id="5e29d-108">Screencast content from your Android device onto a DevTools instance on your development machine.</span></span>  

<!--  
:::image type="complex" source="../media/remote-debugging--remote-debugging.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging--remote-debugging.msft.png":::
   old Figure 1.  Remote Debugging lets you inspect a page running on an Android device from your development machine  
:::image-end:::  
-->  

> [!NOTE]
> <span data-ttu-id="5e29d-109">Удаленная отладка приложения Microsoft EDGE на устройствах с iOS в настоящее время не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="5e29d-109">Remote debugging the Microsoft Edge app on iOS devices is not currently supported.</span></span>  <span data-ttu-id="5e29d-110">Следующее руководство специально ориентировано на удаленную отладку Microsoft EDGE на устройствах с Android.</span><span class="sxs-lookup"><span data-stu-id="5e29d-110">The following guide is specifically focused on remote debugging Microsoft Edge on Android devices.</span></span>
> <span data-ttu-id="5e29d-111">Если у вас есть устройство macOS, следуйте инструкциям [по отладке Brightcove][BrightcoveSupportDebuggingMobileDevices] для удаленной отладки Microsoft EDGE на устройстве с iOS с помощью Safari.</span><span class="sxs-lookup"><span data-stu-id="5e29d-111">If you have a macOS device, follow the [Brightcove Debugging guide][BrightcoveSupportDebuggingMobileDevices] to remotely debug Microsoft Edge on an iOS device using Safari.</span></span>  <span data-ttu-id="5e29d-112">Дополнительные сведения о средстве веб-инспектора в Safari можно найти в разделе [средства разработки веб-сайтов Safari][AppleDeveloperSafariTools].</span><span class="sxs-lookup"><span data-stu-id="5e29d-112">For more information about the Web Inspector tool in Safari, see [Safari Web Development Tools][AppleDeveloperSafariTools].</span></span>  

## <span data-ttu-id="5e29d-113">Шаг 1: обнаружение устройства с Android</span><span class="sxs-lookup"><span data-stu-id="5e29d-113">Step 1: Discover your Android device</span></span>  

<span data-ttu-id="5e29d-114">Рабочий процесс, описанный ниже, подходит для большинства пользователей.</span><span class="sxs-lookup"><span data-stu-id="5e29d-114">The workflow below works for most users.</span></span>  <span data-ttu-id="5e29d-115">Дополнительные сведения можно найти в разделе [Устранение неполадок: DevTools не удается найти раздел устройства Android](#troubleshooting-devtools-is-not-detecting-the-android-device) .</span><span class="sxs-lookup"><span data-stu-id="5e29d-115">For more help, see the [Troubleshooting: DevTools is not detecting the Android device](#troubleshooting-devtools-is-not-detecting-the-android-device) section.</span></span>  

1.  <span data-ttu-id="5e29d-116">Откройте экран **Параметры разработчика** на устройстве с Android.</span><span class="sxs-lookup"><span data-stu-id="5e29d-116">Open the **Developer Options** screen on your Android.</span></span>  <span data-ttu-id="5e29d-117">Дополнительные сведения можно найти [в разделе Настройка параметров разработчика на устройстве][AndroidDeveloperStudioDevOptions].</span><span class="sxs-lookup"><span data-stu-id="5e29d-117">For more information, see [Configure On-Device Developer Options][AndroidDeveloperStudioDevOptions].</span></span>  
1.  <span data-ttu-id="5e29d-118">Выберите **включить отладку USB**.</span><span class="sxs-lookup"><span data-stu-id="5e29d-118">Select **Enable USB Debugging**.</span></span>  
1.  <span data-ttu-id="5e29d-119">На своем компьютере для разработки откройте Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5e29d-119">On your development machine, open Microsoft Edge.</span></span>  
1.  <span data-ttu-id="5e29d-120">Перейдите на `edge://inspect` страницу в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5e29d-120">Navigate to the `edge://inspect` page in Microsoft Edge.</span></span>  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-no-targets.msft.png" alt-text="Страница edge://inspect в Microsoft Edge" lightbox="../media/remote-debugging-edge-inspect-no-targets.msft.png":::
       <span data-ttu-id="5e29d-122">Рисунок 1.</span><span class="sxs-lookup"><span data-stu-id="5e29d-122">Figure 1.</span></span>  <span data-ttu-id="5e29d-123">`edge://inspect`Страница в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="5e29d-123">The `edge://inspect` page in Microsoft Edge</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="5e29d-124">Подключите устройство Android непосредственно к компьютеру разработчика с помощью USB-кабеля.</span><span class="sxs-lookup"><span data-stu-id="5e29d-124">Connect your Android device directly to your development machine using a USB cable.</span></span>  <span data-ttu-id="5e29d-125">При первой попытке подключения вы обычно видите сообщение о том, что DevTools обнаруживает неизвестное устройство.</span><span class="sxs-lookup"><span data-stu-id="5e29d-125">The first time you try to connect, you usually see prompt about DevTools detecting an unknown device.</span></span>  <span data-ttu-id="5e29d-126">Подтвердите запрос разрешения на **отладку USB** на устройстве с Android.</span><span class="sxs-lookup"><span data-stu-id="5e29d-126">Accept the **Allow USB Debugging** permission prompt on your Android device.</span></span>  
    
    :::image type="complex" source="../media/remote-debugging-android-permissions-prompt.msft.png" alt-text="Предупреждение о разрешении разрешения на отладку USB на устройстве с Android" lightbox="../media/remote-debugging-android-permissions-prompt.msft.png":::
       <span data-ttu-id="5e29d-128">Рисунок 2.</span><span class="sxs-lookup"><span data-stu-id="5e29d-128">Figure 2.</span></span>  <span data-ttu-id="5e29d-129">Предупреждение о разрешении разрешения на **отладку USB** на устройстве с Android</span><span class="sxs-lookup"><span data-stu-id="5e29d-129">The **Allow USB Debugging** permission prompt on an Android device</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="5e29d-130">Если вы видите название модели устройства с Android, Microsoft Edge успешно установил подключение к устройству.</span><span class="sxs-lookup"><span data-stu-id="5e29d-130">If you see the model name of your Android device, then Microsoft Edge has successfully established the connection to your device.</span></span>  <span data-ttu-id="5e29d-131">Перейдите к разделу [этап 2](#step-2-debug-content-on-your-android-device-from-your-development-machine) .</span><span class="sxs-lookup"><span data-stu-id="5e29d-131">Continue to the [Step 2](#step-2-debug-content-on-your-android-device-from-your-development-machine) section.</span></span>  
    
    <!--  
    :::image type="complex" source="../media/remote-debugging--unknown-device.msft.png" alt-text="The Remote Devices tab has successfully detected an unknown device that is pending authorization" lightbox="../media/remote-debugging--unknown-device.msft.png":::
       old Figure 4.  The **Remote Devices** tab has successfully detected an unknown device that is pending authorization  
    :::image-end:::
    -->  
    
### <span data-ttu-id="5e29d-132">Устранение неполадок: DevTools не может обнаружить устройство с Android</span><span class="sxs-lookup"><span data-stu-id="5e29d-132">Troubleshooting: DevTools is not detecting the Android device</span></span>  

<span data-ttu-id="5e29d-133">Ниже приведены советы по устранению неполадок, связанных с правильными параметрами оборудования.</span><span class="sxs-lookup"><span data-stu-id="5e29d-133">Use the following tips to help you troubleshoot the correct settings for your hardware.</span></span>  

*   <span data-ttu-id="5e29d-134">Если вы используете USB-концентратор, попробуйте подключить устройство Android прямо к компьютеру разработчика.</span><span class="sxs-lookup"><span data-stu-id="5e29d-134">If you are using a USB hub, try connecting your Android device directly to your development machine.</span></span>  
*   <span data-ttu-id="5e29d-135">Попробуйте отключить кабель USB между устройством Android и компьютером разработчика, а затем снова подключить USB-кабель.</span><span class="sxs-lookup"><span data-stu-id="5e29d-135">Try unplugging the USB cable between your Android device and development machine, and then re-plugging your USB cable.</span></span>  <span data-ttu-id="5e29d-136">Выполнение задачи во время разблокировки экранов компьютера Android и разработки.</span><span class="sxs-lookup"><span data-stu-id="5e29d-136">Complete the task while your Android and development machine screens are unlocked.</span></span>  
*   <span data-ttu-id="5e29d-137">Убедитесь, что USB-кабель работает.</span><span class="sxs-lookup"><span data-stu-id="5e29d-137">Make sure that your USB cable works.</span></span>  <span data-ttu-id="5e29d-138">Вы должны иметь возможность проверять файлы на устройстве с Android с компьютера, на котором ведется разработка.</span><span class="sxs-lookup"><span data-stu-id="5e29d-138">You should be able to inspect files on your Android device from your development machine.</span></span>  

<span data-ttu-id="5e29d-139">Чтобы убедиться, что программное обеспечение правильно настроено, воспользуйтесь приведенными ниже советами.</span><span class="sxs-lookup"><span data-stu-id="5e29d-139">Use the following tips to help you verify that your software is set up correctly.</span></span>  

*   <span data-ttu-id="5e29d-140">Если на вашем компьютере разработчика установлена операционная система Windows, попробуйте установить драйверы USB для устройства с Android вручную.</span><span class="sxs-lookup"><span data-stu-id="5e29d-140">If your development machine is running Windows, try manually installing the USB drivers for your Android device.</span></span>  <span data-ttu-id="5e29d-141">Дополнительные сведения можно найти в разделе [Установка драйверов USB для OEM][AndroidDeveloperToolsOemUsb].</span><span class="sxs-lookup"><span data-stu-id="5e29d-141">For more information, see [Install OEM USB Drivers][AndroidDeveloperToolsOemUsb].</span></span>  
*   <span data-ttu-id="5e29d-142">Некоторые комбинации устройств Windows и Android (особенно Samsung) требуют дополнительных настроек.</span><span class="sxs-lookup"><span data-stu-id="5e29d-142">Some combinations of Windows and Android devices \(especially Samsung\) require additional settings.</span></span>  <span data-ttu-id="5e29d-143">Дополнительные сведения можно найти в разделе [устройства DevTools не обнаруживают устройства при подключении к сети][Stackoverflow21925992].</span><span class="sxs-lookup"><span data-stu-id="5e29d-143">For more information, see [DevTools Devices does not detect device when plugged in][Stackoverflow21925992].</span></span>  

<span data-ttu-id="5e29d-144">Приведенные ниже советы помогут вам устранить неполадки с выводом на экран **разрешение на отладку USB** на устройстве с Android.</span><span class="sxs-lookup"><span data-stu-id="5e29d-144">Use the following tips to help you troubleshoot not seeing the **Allow USB Debugging** prompt on your Android device.</span></span>  

*   <span data-ttu-id="5e29d-145">Отключение кабеля USB и повторное подключение к нему, когда DevTools на компьютере разработки и отображается начальный экран на устройстве с Android.</span><span class="sxs-lookup"><span data-stu-id="5e29d-145">Disconnecting and then re-connecting the USB cable while DevTools is in focus on your development machine and your Android homescreen is showing.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="5e29d-146">Если экраны на устройстве Android или разработчика заблокированы, сообщение может не отображаться.</span><span class="sxs-lookup"><span data-stu-id="5e29d-146">You may not see the prompt if your Android or development machine screens are locked.</span></span>  

*   <span data-ttu-id="5e29d-147">Обновление параметров отображения для устройства Android и компьютера для разработки таким образом, чтобы все они никогда не переходили в спящий режим.</span><span class="sxs-lookup"><span data-stu-id="5e29d-147">Updating the display settings for your Android device and development machine so that each never goes to sleep.</span></span>  
*   <span data-ttu-id="5e29d-148">Установка режима USB для устройства с Android на PTP.</span><span class="sxs-lookup"><span data-stu-id="5e29d-148">Setting the USB mode for Android to PTP.</span></span>  <span data-ttu-id="5e29d-149">Дополнительные сведения можно найти в разделе [Galaxy S4 не показывает диалоговое окно "авторизация USB"][StackexchangeAndroid101933].</span><span class="sxs-lookup"><span data-stu-id="5e29d-149">For more information, see [Galaxy S4 does not show Authorize USB debugging dialog box][StackexchangeAndroid101933].</span></span>  
*   <span data-ttu-id="5e29d-150">Выберите **отозвать разрешения на отладку USB** на экране **Параметры разработчика** на устройстве с Android, чтобы сбросить его в новое состояние.</span><span class="sxs-lookup"><span data-stu-id="5e29d-150">Select **Revoke USB Debugging Authorizations** from the **Developer Options** screen on your Android device to reset it to a fresh state.</span></span>  

<span data-ttu-id="5e29d-151">Если вы нашли решение, которое не было упомянуто на этой странице, или на [DevTools устройствах не обнаружите устройства при подключении][Stackoverflow21925992] к переполнению стека, добавьте свое решение на вопрос о переполнении стека.</span><span class="sxs-lookup"><span data-stu-id="5e29d-151">If you find a solution that is not mentioned on this page or in [DevTools Devices does not detect device when plugged in][Stackoverflow21925992] on Stack Overflow, please add your solution to the Stack Overflow question</span></span><!--, or [open an issue in the webfundamentals repository][GitHubWebFundamentalsNewIssue]--><span data-ttu-id="5e29d-152">!</span><span class="sxs-lookup"><span data-stu-id="5e29d-152">!</span></span>  

## <span data-ttu-id="5e29d-153">Шаг 2: Отладка содержимого на устройстве с Android с компьютера для разработки</span><span class="sxs-lookup"><span data-stu-id="5e29d-153">Step 2: Debug content on your Android device from your development machine</span></span>  

1.  <span data-ttu-id="5e29d-154">Откройте Microsoft EDGE на устройстве с Android.</span><span class="sxs-lookup"><span data-stu-id="5e29d-154">Open Microsoft Edge on your Android device.</span></span>  
1.  <span data-ttu-id="5e29d-155">На `edge://inspect` странице вы увидите название модели устройства с Android, а затем серийный номер устройства.</span><span class="sxs-lookup"><span data-stu-id="5e29d-155">From the `edge://inspect` page, you see the model name of your Android device, followed by the device serial number.</span></span>  <span data-ttu-id="5e29d-156">Ниже показана версия Microsoft EDGE, установленная на устройстве, с номером версии в круглых скобках.</span><span class="sxs-lookup"><span data-stu-id="5e29d-156">Below that, you should see the version of Microsoft Edge running on the device, with the version number in parentheses.</span></span>  <span data-ttu-id="5e29d-157">Каждая открытая вкладка Microsoft Edge получает уникальный раздел.</span><span class="sxs-lookup"><span data-stu-id="5e29d-157">Each open Microsoft Edge tab gets a unique section.</span></span>  <span data-ttu-id="5e29d-158">Вы можете работать с этой вкладкой в разделе.</span><span class="sxs-lookup"><span data-stu-id="5e29d-158">You may interact with that tab from a section.</span></span>  <!--If there are any apps using WebView, you see a section for each of those apps, too.  --><!--In [**Figure 5**](#figure-5) there are no tabs or WebViews open.  -->  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets.msft.png" alt-text="Подключенное удаленное устройство" lightbox="../media/remote-debugging-edge-inspect-with-targets.msft.png":::
       <span data-ttu-id="5e29d-160">Рисунок 3.</span><span class="sxs-lookup"><span data-stu-id="5e29d-160">Figure 3.</span></span>  <span data-ttu-id="5e29d-161">Подключенное удаленное устройство</span><span class="sxs-lookup"><span data-stu-id="5e29d-161">A connected remote device</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="5e29d-162">В текстовом поле **открыть вкладку с URL-адресом** введите URL-адрес и нажмите кнопку **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="5e29d-162">In the **Open tab with url** text box, enter a URL and then select **Open**.</span></span>  <span data-ttu-id="5e29d-163">Страница откроется на новой вкладке на устройстве с Android.</span><span class="sxs-lookup"><span data-stu-id="5e29d-163">The page opens in a new tab on your Android device.</span></span>  
1.  <span data-ttu-id="5e29d-164">Нажмите кнопку " **проверить** " рядом с URL-адресом, который вы только что открыли.</span><span class="sxs-lookup"><span data-stu-id="5e29d-164">Select **inspect** next to the URL that you just opened.</span></span>  <span data-ttu-id="5e29d-165">Откроется новый экземпляр DevTools.</span><span class="sxs-lookup"><span data-stu-id="5e29d-165">A new DevTools instance opens.</span></span>  

<!-- The version of Microsoft Edge running on your Android device determines the version of DevTools that opens on your development machine.  
    So, if your Android device is running a very old version of Microsoft Edge, the DevTools instance may look very different than what you are used to.   -->

### <span data-ttu-id="5e29d-166">Дополнительные действия: перемещение фокуса, перезагрузка или закрытие вкладки</span><span class="sxs-lookup"><span data-stu-id="5e29d-166">More actions: focus, reload, or close a tab</span></span>  

<span data-ttu-id="5e29d-167">На вкладке **фокус**нажмите кнопку **Перезагрузка**или **Закрыть** рядом с вкладкой, на которую вы хотите установить фокус, перезагрузить или закрыть.</span><span class="sxs-lookup"><span data-stu-id="5e29d-167">Select **focus tab**, **reload**, or **close** next to the tab that you want to focus, reload, or close.</span></span>  

:::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png" alt-text="Кнопки для фокусировки, повторной загрузки и закрытия вкладки" lightbox="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png":::
   <span data-ttu-id="5e29d-169">Рисунок 4.</span><span class="sxs-lookup"><span data-stu-id="5e29d-169">Figure 4.</span></span>  <span data-ttu-id="5e29d-170">Кнопки для фокусировки, повторной загрузки и закрытия вкладки</span><span class="sxs-lookup"><span data-stu-id="5e29d-170">The buttons for focusing, reloading, or closing a tab</span></span>  
:::image-end:::  

### <span data-ttu-id="5e29d-171">Проверка элементов</span><span class="sxs-lookup"><span data-stu-id="5e29d-171">Inspect elements</span></span>  

<span data-ttu-id="5e29d-172">Перейдите на панель **элементы** экземпляра DevTools и наведите указатель мыши на элемент, чтобы выделить его в окне просмотра на устройстве с Android.</span><span class="sxs-lookup"><span data-stu-id="5e29d-172">Go to the **Elements** panel of your DevTools instance, and hover over an element to highlight it in the viewport of your Android device.</span></span>  

<span data-ttu-id="5e29d-173">Вы также можете выбрать элемент на экране устройства с Android, чтобы выбрать его на панели " **элементы** ".</span><span class="sxs-lookup"><span data-stu-id="5e29d-173">You may also select an element on your Android device screen to select it in the **Elements** panel.</span></span>  <span data-ttu-id="5e29d-174">Нажмите кнопку выбрать **элемент** ![ щелкните ][ImageSelectElementIcon] значок выбора элемента в экземпляре DevTools, а затем выберите элемент на экране устройства с Android.</span><span class="sxs-lookup"><span data-stu-id="5e29d-174">Select **Select Element** ![Select Element][ImageSelectElementIcon] icon on your DevTools instance, and then select the element on your Android device screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="5e29d-175">**Элемент "выбрать** " отключается после первого выбора, поэтому для использования этой функции необходимо повторно включить его.</span><span class="sxs-lookup"><span data-stu-id="5e29d-175">**Select Element** is disabled after the first selection, so you must re-enable it every time you want to use the feature.</span></span>  

### <span data-ttu-id="5e29d-176">Демонстрация экрана Android на компьютере разработчика</span><span class="sxs-lookup"><span data-stu-id="5e29d-176">Screencast your Android screen to your development machine</span></span>  

<span data-ttu-id="5e29d-177">Нажмите кнопку "переключить **презентацию** ![ ][ImageToggleScreencastIcon] ", чтобы просмотреть содержимое устройства с Android в экземпляре DevTools.</span><span class="sxs-lookup"><span data-stu-id="5e29d-177">Select **Toggle Screencast** ![Toggle Screencast][ImageToggleScreencastIcon] icon to view the content of your Android device in your DevTools instance.</span></span>  

<span data-ttu-id="5e29d-178">Вы можете взаимодействовать с презентацией следующими способами.</span><span class="sxs-lookup"><span data-stu-id="5e29d-178">You are able to interact with the screencast in the following ways.</span></span>  

*   <span data-ttu-id="5e29d-179">Нажатия клавиш переводятся в касания, и на устройстве обрабатывались соответствующие события сенсорного ввода.</span><span class="sxs-lookup"><span data-stu-id="5e29d-179">Clicks are translated into taps, firing proper touch events on the device.</span></span>  
*   <span data-ttu-id="5e29d-180">Нажатия клавиш на компьютере отправляются на устройство.</span><span class="sxs-lookup"><span data-stu-id="5e29d-180">Keystrokes on your computer are sent to the device.</span></span>  
*   <span data-ttu-id="5e29d-181">Чтобы смоделировать жест сжатия, удерживайте `Shift` при перетаскивании.</span><span class="sxs-lookup"><span data-stu-id="5e29d-181">To simulate a pinch gesture, hold `Shift` while dragging.</span></span>  
*   <span data-ttu-id="5e29d-182">Для прокрутки используйте сенсорной панели, колесико мыши или смахивание с помощью указателя мыши.</span><span class="sxs-lookup"><span data-stu-id="5e29d-182">To scroll, use your trackpad or mouse wheel, or fling with your mouse pointer.</span></span>

> [!NOTE]
> <span data-ttu-id="5e29d-183">Чтобы сделать презентацию более подсказками, воспользуйтесь приведенными ниже советами.</span><span class="sxs-lookup"><span data-stu-id="5e29d-183">Use the following tips to help you screencast.</span></span>  
> 
> *   <span data-ttu-id="5e29d-184">В ролики отображается только содержимое страницы.</span><span class="sxs-lookup"><span data-stu-id="5e29d-184">Screencasts only display page content.</span></span>  <span data-ttu-id="5e29d-185">Прозрачные части презентации представляют интерфейсы устройства, такие как адресная строка Microsoft EDGE, строка состояния Android или клавиатура Android.</span><span class="sxs-lookup"><span data-stu-id="5e29d-185">Transparent portions of the screencast represent device interfaces, such as the Microsoft Edge address bar, the Android status bar, or the Android keyboard.</span></span>  
> *   <span data-ttu-id="5e29d-186">Ролики негативно влияют на частоту кадров.</span><span class="sxs-lookup"><span data-stu-id="5e29d-186">Screencasts negatively affect frame rates.</span></span>  <span data-ttu-id="5e29d-187">Отключите экранную анимацию, изменяя прокрутки или анимации, чтобы получить более точную картину производительности страницы.</span><span class="sxs-lookup"><span data-stu-id="5e29d-187">Disable screencasting while measuring scrolls or animations to get a more accurate picture of the performance of your page.</span></span>  
> *   <span data-ttu-id="5e29d-188">Если экран вашего устройства с Android блокируется, содержимое презентации исчезнет.</span><span class="sxs-lookup"><span data-stu-id="5e29d-188">If your Android device screen locks, the content of your screencast disappears.</span></span>  <span data-ttu-id="5e29d-189">Разблокируйте экран устройства с Android для автоматического возобновления ролика.</span><span class="sxs-lookup"><span data-stu-id="5e29d-189">Unlock your Android device screen to automatically resume the screencast.</span></span>  

<!-- image links -->  

[ImageSelectElementIcon]: /microsoft-edge/devtools-guide-chromium/media/select-element-icon.msft.png  
[ImageToggleScreencastIcon]: /microsoft-edge/devtools-guide-chromium/media/toggle-screencast-icon.msft.png  

<!-- links -->  

[AndroidDeveloperStudioDevOptions]: https://developer.android.com/studio/debug/dev-options "Настройка параметров разработчика на устройстве | Разработчик Android"  
[AndroidDeveloperToolsOemUsb]: https://developer.android.com/tools/extras/oem-usb.html "Установка драйверов USB для OEM | Разработчики Android"  

[AppleDeveloperSafariTools]: https://developer.apple.com/safari/tools "Средства разработки веб-браузера Safari | Разработчик Apple"  

[BrightcoveSupportDebuggingMobileDevices]: https://support.brightcove.com/debugging-mobile-devices "Отладка на мобильных устройствах | Поддержка Brightcove"  

<!-- [GitHubWebFundamentalsNewIssue]: https://github.com/Alphabet/webfundamentals/issues/new?title=[Remote%20Debugging] "GitHub - Web Fundamentals - New Issue"  -->  

[StackexchangeAndroid101933]: https://android.stackexchange.com/questions/101933 "ADB — обмен данными в стеке для энтузиастов Android"  

[Stackoverflow21925992]: https://stackoverflow.com/questions/21925992 "Устройства DevTools не обнаруживают устройства при подключении к стеку с переполнением"  

> [!NOTE]
> <span data-ttu-id="5e29d-196">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5e29d-196">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="5e29d-197">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="5e29d-197">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="5e29d-199">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="5e29d-199">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
