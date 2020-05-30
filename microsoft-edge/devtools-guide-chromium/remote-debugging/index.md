---
title: Начало работы с удаленными отладкой устройств с Android
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: fc7450ba2b088eee8f4005216374980096cbb067
ms.sourcegitcommit: ba9f0ed77e84174b03262b17e62c6a7e26cfeb3d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/30/2020
ms.locfileid: "10688165"
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

# <span data-ttu-id="76e1a-103">Начало работы с удаленными отладкой устройств с Android</span><span class="sxs-lookup"><span data-stu-id="76e1a-103">Get started with remote debugging Android devices</span></span>  

<span data-ttu-id="76e1a-104">Удаленная отладка динамического содержимого на устройстве Android с компьютера Windows или macOS.</span><span class="sxs-lookup"><span data-stu-id="76e1a-104">Remote debug live content on an Android device from your Windows or macOS computer.</span></span>  <span data-ttu-id="76e1a-105">На этой странице учебника вы узнаете, как выполнять указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="76e1a-105">This tutorial page teaches you how to complete the following actions.</span></span>  

*   <span data-ttu-id="76e1a-106">Настройте устройство Android для удаленной отладки и найдите его на компьютере разработчика.</span><span class="sxs-lookup"><span data-stu-id="76e1a-106">Set up your Android device for remote debugging, and discover it from your development machine.</span></span>  
*   <span data-ttu-id="76e1a-107">Изучите и отлаживать динамический контент на устройстве с Android с компьютера для разработки.</span><span class="sxs-lookup"><span data-stu-id="76e1a-107">Inspect and debug live content on your Android device from your development machine.</span></span>  
*   <span data-ttu-id="76e1a-108">Содержимое ролика с устройства Android на экземпляр DevTools на компьютере разработчика.</span><span class="sxs-lookup"><span data-stu-id="76e1a-108">Screencast content from your Android device onto a DevTools instance on your development machine.</span></span>  

<!--  
:::image type="complex" source="../media/remote-debugging--remote-debugging.msft.png" alt-text="Remote Debugging lets you inspect a page running on an Android device from your development machine" lightbox="../media/remote-debugging--remote-debugging.msft.png":::
   old Figure 1.  Remote Debugging lets you inspect a page running on an Android device from your development machine  
:::image-end:::  
-->  

## <span data-ttu-id="76e1a-109">Шаг 1: обнаружение устройства с Android</span><span class="sxs-lookup"><span data-stu-id="76e1a-109">Step 1: Discover your Android device</span></span>  

<span data-ttu-id="76e1a-110">Рабочий процесс, описанный ниже, подходит для большинства пользователей.</span><span class="sxs-lookup"><span data-stu-id="76e1a-110">The workflow below works for most users.</span></span>  <span data-ttu-id="76e1a-111">Дополнительные сведения можно найти в [статье Устранение неполадок: DevTools не удается найти устройство Android](#troubleshooting-devtools-is-not-detecting-the-android-device) .</span><span class="sxs-lookup"><span data-stu-id="76e1a-111">See [Troubleshooting: DevTools is not detecting the Android device](#troubleshooting-devtools-is-not-detecting-the-android-device) for more help.</span></span>  

1.  <span data-ttu-id="76e1a-112">Откройте экран **Параметры разработчика** на устройстве с Android.</span><span class="sxs-lookup"><span data-stu-id="76e1a-112">Open the **Developer Options** screen on your Android.</span></span>  <span data-ttu-id="76e1a-113">Дополнительные сведения можно найти [в разделе Настройка параметров разработчика на устройстве](https://developer.android.com/studio/debug/dev-options.html).</span><span class="sxs-lookup"><span data-stu-id="76e1a-113">For more information, see [Configure On-Device Developer Options](https://developer.android.com/studio/debug/dev-options.html).</span></span>  
1.  <span data-ttu-id="76e1a-114">Выберите **включить отладку USB**.</span><span class="sxs-lookup"><span data-stu-id="76e1a-114">Select **Enable USB Debugging**.</span></span>  
1.  <span data-ttu-id="76e1a-115">На своем компьютере для разработки откройте Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="76e1a-115">On your development machine, open Microsoft Edge.</span></span>  
1.  <span data-ttu-id="76e1a-116">Перейдите на `edge://inspect` страницу в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="76e1a-116">Navigate to the `edge://inspect` page in Microsoft Edge.</span></span>  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-no-targets.msft.png" alt-text="Страница edge://inspect в Microsoft Edge" lightbox="../media/remote-debugging-edge-inspect-no-targets.msft.png":::
       <span data-ttu-id="76e1a-118">Рисунок 1.</span><span class="sxs-lookup"><span data-stu-id="76e1a-118">Figure 1.</span></span>  <span data-ttu-id="76e1a-119">`edge://inspect`Страница в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="76e1a-119">The `edge://inspect` page in Microsoft Edge</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="76e1a-120">Подключите устройство Android непосредственно к компьютеру разработчика с помощью USB-кабеля.</span><span class="sxs-lookup"><span data-stu-id="76e1a-120">Connect your Android device directly to your development machine using a USB cable.</span></span>  <span data-ttu-id="76e1a-121">При первой попытке подключения вы обычно видите сообщение о том, что DevTools обнаруживает неизвестное устройство.</span><span class="sxs-lookup"><span data-stu-id="76e1a-121">The first time you try to connect, you usually see prompt about DevTools detecting an unknown device.</span></span>  <span data-ttu-id="76e1a-122">Подтвердите запрос разрешения на **отладку USB** на устройстве с Android.</span><span class="sxs-lookup"><span data-stu-id="76e1a-122">Accept the **Allow USB Debugging** permission prompt on your Android device.</span></span>  
    
    :::image type="complex" source="../media/remote-debugging-android-permissions-prompt.msft.png" alt-text="Предупреждение о разрешении разрешения на отладку USB на устройстве с Android" lightbox="../media/remote-debugging-android-permissions-prompt.msft.png":::
       <span data-ttu-id="76e1a-124">Рисунок 2.</span><span class="sxs-lookup"><span data-stu-id="76e1a-124">Figure 2.</span></span>  <span data-ttu-id="76e1a-125">Предупреждение о разрешении разрешения на **отладку USB** на устройстве с Android</span><span class="sxs-lookup"><span data-stu-id="76e1a-125">The **Allow USB Debugging** permission prompt on an Android device</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="76e1a-126">Если вы видите название модели устройства с Android, Microsoft Edge успешно установил подключение к устройству.</span><span class="sxs-lookup"><span data-stu-id="76e1a-126">If you see the model name of your Android device, then Microsoft Edge has successfully established the connection to your device.</span></span>  <span data-ttu-id="76e1a-127">Перейдите к [действию 2](#step-2-debug-content-on-your-android-device-from-your-development-machine).</span><span class="sxs-lookup"><span data-stu-id="76e1a-127">Continue to [Step 2](#step-2-debug-content-on-your-android-device-from-your-development-machine).</span></span>  
    
    <!--  
    :::image type="complex" source="../media/remote-debugging--unknown-device.msft.png" alt-text="The Remote Devices tab has successfully detected an unknown device that is pending authorization" lightbox="../media/remote-debugging--unknown-device.msft.png":::
       old Figure 4.  The **Remote Devices** tab has successfully detected an unknown device that is pending authorization  
    :::image-end:::
    -->  
    
### <span data-ttu-id="76e1a-128">Устранение неполадок: DevTools не может обнаружить устройство с Android</span><span class="sxs-lookup"><span data-stu-id="76e1a-128">Troubleshooting: DevTools is not detecting the Android device</span></span>  

<span data-ttu-id="76e1a-129">Ниже приведены советы по устранению неполадок, связанных с правильными параметрами оборудования.</span><span class="sxs-lookup"><span data-stu-id="76e1a-129">Use the following tips to help you troubleshoot the correct settings for your hardware.</span></span>  

*   <span data-ttu-id="76e1a-130">Если вы используете USB-концентратор, попробуйте подключить устройство Android прямо к компьютеру разработчика.</span><span class="sxs-lookup"><span data-stu-id="76e1a-130">If you are using a USB hub, try connecting your Android device directly to your development machine.</span></span>  
*   <span data-ttu-id="76e1a-131">Попробуйте отключить кабель USB между устройством Android и компьютером разработчика, а затем снова подключить USB-кабель.</span><span class="sxs-lookup"><span data-stu-id="76e1a-131">Try unplugging the USB cable between your Android device and development machine, and then re-plugging your USB cable.</span></span>  <span data-ttu-id="76e1a-132">Выполнение задачи во время разблокировки экранов компьютера Android и разработки.</span><span class="sxs-lookup"><span data-stu-id="76e1a-132">Complete the task while your Android and development machine screens are unlocked.</span></span>  
*   <span data-ttu-id="76e1a-133">Убедитесь, что USB-кабель работает.</span><span class="sxs-lookup"><span data-stu-id="76e1a-133">Make sure that your USB cable works.</span></span>  <span data-ttu-id="76e1a-134">Вы должны иметь возможность проверять файлы на устройстве с Android с компьютера, на котором ведется разработка.</span><span class="sxs-lookup"><span data-stu-id="76e1a-134">You should be able to inspect files on your Android device from your development machine.</span></span>  

<span data-ttu-id="76e1a-135">Чтобы убедиться, что программное обеспечение правильно настроено, воспользуйтесь приведенными ниже советами.</span><span class="sxs-lookup"><span data-stu-id="76e1a-135">Use the following tips to help you verify that your software is set up correctly.</span></span>  

*   <span data-ttu-id="76e1a-136">Если на вашем компьютере разработчика установлена операционная система Windows, попробуйте установить драйверы USB для устройства с Android вручную.</span><span class="sxs-lookup"><span data-stu-id="76e1a-136">If your development machine is running Windows, try manually installing the USB drivers for your Android device.</span></span>  <span data-ttu-id="76e1a-137">Дополнительные сведения можно найти в разделе [Установка драйверов USB для OEM][AndroidUSBDrivers].</span><span class="sxs-lookup"><span data-stu-id="76e1a-137">For more information, see [Install OEM USB Drivers][AndroidUSBDrivers].</span></span>  
*   <span data-ttu-id="76e1a-138">Некоторые комбинации устройств Windows и Android (особенно Samsung) требуют дополнительных настроек.</span><span class="sxs-lookup"><span data-stu-id="76e1a-138">Some combinations of Windows and Android devices \(especially Samsung\) require additional settings.</span></span>  <span data-ttu-id="76e1a-139">Дополнительные сведения можно найти в разделе [DevTools Devices не определяет устройство при подключении к сети] [StackOverflowDevicesNotDetected].</span><span class="sxs-lookup"><span data-stu-id="76e1a-139">For more information, see [DevTools Devices does not detect device when plugged in][StackOverflowDevicesNotDetected].</span></span>  

<span data-ttu-id="76e1a-140">Приведенные ниже советы помогут вам устранить неполадки с выводом на экран **разрешение на отладку USB** на устройстве с Android.</span><span class="sxs-lookup"><span data-stu-id="76e1a-140">Use the following tips to help you troubleshoot not seeing the **Allow USB Debugging** prompt on your Android device.</span></span>  

*   <span data-ttu-id="76e1a-141">Отключение кабеля USB и повторное подключение к нему, когда DevTools на компьютере разработки и отображается начальный экран на устройстве с Android.</span><span class="sxs-lookup"><span data-stu-id="76e1a-141">Disconnecting and then re-connecting the USB cable while DevTools is in focus on your development machine and your Android homescreen is showing.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="76e1a-142">Если экраны на устройстве Android или разработчика заблокированы, сообщение может не отображаться.</span><span class="sxs-lookup"><span data-stu-id="76e1a-142">You may not see the prompt if your Android or development machine screens are locked.</span></span>  

*   <span data-ttu-id="76e1a-143">Обновление параметров отображения для устройства Android и компьютера для разработки таким образом, чтобы все они никогда не переходили в спящий режим.</span><span class="sxs-lookup"><span data-stu-id="76e1a-143">Updating the display settings for your Android device and development machine so that each never goes to sleep.</span></span>  
*   <span data-ttu-id="76e1a-144">Установка режима USB для устройства с Android на PTP.</span><span class="sxs-lookup"><span data-stu-id="76e1a-144">Setting the USB mode for Android to PTP.</span></span>  <span data-ttu-id="76e1a-145">Дополнительные сведения можно найти в разделе [Galaxy S4 не показывает диалоговое окно "авторизация USB"][StackExchangeGalaxyS4DoesNotShowDialogBox].</span><span class="sxs-lookup"><span data-stu-id="76e1a-145">For more information, see [Galaxy S4 does not show Authorize USB debugging dialog box][StackExchangeGalaxyS4DoesNotShowDialogBox].</span></span>  
*   <span data-ttu-id="76e1a-146">Выберите **отозвать разрешения на отладку USB** на экране **Параметры разработчика** на устройстве с Android, чтобы сбросить его в новое состояние.</span><span class="sxs-lookup"><span data-stu-id="76e1a-146">Select **Revoke USB Debugging Authorizations** from the **Developer Options** screen on your Android device to reset it to a fresh state.</span></span>  

<span data-ttu-id="76e1a-147">Если вы нашли решение, которое не было упомянуто на этой странице, или в разделе [DevTools Devices не обнаруживает устройство при подключении к сети] [StackOverflowDevicesNotDetected] в области переполнения стека добавьте свое решение на вопрос о переполнении стека.</span><span class="sxs-lookup"><span data-stu-id="76e1a-147">If you find a solution that is not mentioned on this page or in [DevTools Devices does not detect device when plugged in][StackOverflowDevicesNotDetected] on Stack Overflow, please add your solution to the Stack Overflow question</span></span><!--, or [open an issue in the webfundamentals repository][GitHubWebFundamentalsNewIssue]--><span data-ttu-id="76e1a-148">!</span><span class="sxs-lookup"><span data-stu-id="76e1a-148">!</span></span>  

## <span data-ttu-id="76e1a-149">Шаг 2: Отладка содержимого на устройстве с Android с компьютера для разработки</span><span class="sxs-lookup"><span data-stu-id="76e1a-149">Step 2: Debug content on your Android device from your development machine</span></span>  

1.  <span data-ttu-id="76e1a-150">Откройте Microsoft EDGE на устройстве с Android.</span><span class="sxs-lookup"><span data-stu-id="76e1a-150">Open Microsoft Edge on your Android device.</span></span>  
1.  <span data-ttu-id="76e1a-151">На `edge://inspect` странице вы увидите название модели устройства с Android, а затем серийный номер устройства.</span><span class="sxs-lookup"><span data-stu-id="76e1a-151">From the `edge://inspect` page, you see the model name of your Android device, followed by the device serial number.</span></span>  <span data-ttu-id="76e1a-152">Ниже показана версия Microsoft EDGE, установленная на устройстве, с номером версии в круглых скобках.</span><span class="sxs-lookup"><span data-stu-id="76e1a-152">Below that, you should see the version of Microsoft Edge running on the device, with the version number in parentheses.</span></span>  <span data-ttu-id="76e1a-153">Каждая открытая вкладка Microsoft Edge получает уникальный раздел.</span><span class="sxs-lookup"><span data-stu-id="76e1a-153">Each open Microsoft Edge tab gets a unique section.</span></span>  <span data-ttu-id="76e1a-154">Вы можете работать с этой вкладкой в разделе.</span><span class="sxs-lookup"><span data-stu-id="76e1a-154">You may interact with that tab from a section.</span></span>  <!--If there are any apps using WebView, you see a section for each of those apps, too.  --><!--In [**Figure 5**](#figure-5) there are no tabs or WebViews open.  -->  
    
    :::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets.msft.png" alt-text="Подключенное удаленное устройство" lightbox="../media/remote-debugging-edge-inspect-with-targets.msft.png":::
       <span data-ttu-id="76e1a-156">Рисунок 3.</span><span class="sxs-lookup"><span data-stu-id="76e1a-156">Figure 3.</span></span>  <span data-ttu-id="76e1a-157">Подключенное удаленное устройство</span><span class="sxs-lookup"><span data-stu-id="76e1a-157">A connected remote device</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="76e1a-158">В текстовом поле **открыть вкладку с URL-адресом** введите URL-адрес и нажмите кнопку **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="76e1a-158">In the **Open tab with url** text box, enter a URL and then select **Open**.</span></span>  <span data-ttu-id="76e1a-159">Страница откроется на новой вкладке на устройстве с Android.</span><span class="sxs-lookup"><span data-stu-id="76e1a-159">The page opens in a new tab on your Android device.</span></span>  
1.  <span data-ttu-id="76e1a-160">Нажмите кнопку " **проверить** " рядом с URL-адресом, который вы только что открыли.</span><span class="sxs-lookup"><span data-stu-id="76e1a-160">Select **inspect** next to the URL that you just opened.</span></span>  <span data-ttu-id="76e1a-161">Откроется новый экземпляр DevTools.</span><span class="sxs-lookup"><span data-stu-id="76e1a-161">A new DevTools instance opens.</span></span>  

<!-- The version of Microsoft Edge running on your Android device determines the version of DevTools that opens on your development machine.  
    So, if your Android device is running a very old version of Microsoft Edge, the DevTools instance may look very different than what you are used to.   -->

### <span data-ttu-id="76e1a-162">Дополнительные действия: перемещение фокуса, перезагрузка или закрытие вкладки</span><span class="sxs-lookup"><span data-stu-id="76e1a-162">More actions: focus, reload, or close a tab</span></span>  

<span data-ttu-id="76e1a-163">На вкладке **фокус**нажмите кнопку **Перезагрузка**или **Закрыть** рядом с вкладкой, на которую вы хотите установить фокус, перезагрузить или закрыть.</span><span class="sxs-lookup"><span data-stu-id="76e1a-163">Select **focus tab**, **reload**, or **close** next to the tab that you want to focus, reload, or close.</span></span>  

:::image type="complex" source="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png" alt-text="Кнопки для фокусировки, повторной загрузки и закрытия вкладки" lightbox="../media/remote-debugging-edge-inspect-with-targets-buttons.msft.png":::
   <span data-ttu-id="76e1a-165">Рисунок 4.</span><span class="sxs-lookup"><span data-stu-id="76e1a-165">Figure 4.</span></span>  <span data-ttu-id="76e1a-166">Кнопки для фокусировки, повторной загрузки и закрытия вкладки</span><span class="sxs-lookup"><span data-stu-id="76e1a-166">The buttons for focusing, reloading, or closing a tab</span></span>  
:::image-end:::  

### <span data-ttu-id="76e1a-167">Проверка элементов</span><span class="sxs-lookup"><span data-stu-id="76e1a-167">Inspect elements</span></span>  

<span data-ttu-id="76e1a-168">Перейдите на панель **элементы** экземпляра DevTools и наведите указатель мыши на элемент, чтобы выделить его в окне просмотра на устройстве с Android.</span><span class="sxs-lookup"><span data-stu-id="76e1a-168">Go to the **Elements** panel of your DevTools instance, and hover over an element to highlight it in the viewport of your Android device.</span></span>  

<span data-ttu-id="76e1a-169">Вы также можете выбрать элемент на экране устройства с Android, чтобы выбрать его на панели " **элементы** ".</span><span class="sxs-lookup"><span data-stu-id="76e1a-169">You may also select an element on your Android device screen to select it in the **Elements** panel.</span></span>  <span data-ttu-id="76e1a-170">Нажмите кнопку выбрать **элемент** ![ щелкните ][ImageSelectElementIcon] значок выбора элемента в экземпляре DevTools, а затем выберите элемент на экране устройства с Android.</span><span class="sxs-lookup"><span data-stu-id="76e1a-170">Select **Select Element** ![Select Element][ImageSelectElementIcon] icon on your DevTools instance, and then select the element on your Android device screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="76e1a-171">**Элемент "выбрать** " отключается после первого выбора, поэтому для использования этой функции необходимо повторно включить его.</span><span class="sxs-lookup"><span data-stu-id="76e1a-171">**Select Element** is disabled after the first selection, so you must re-enable it every time you want to use the feature.</span></span>  

### <span data-ttu-id="76e1a-172">Демонстрация экрана Android на компьютере разработчика</span><span class="sxs-lookup"><span data-stu-id="76e1a-172">Screencast your Android screen to your development machine</span></span>  

<span data-ttu-id="76e1a-173">Нажмите кнопку "переключить **презентацию** ![ ][ImageToggleScreencastIcon] ", чтобы просмотреть содержимое устройства с Android в экземпляре DevTools.</span><span class="sxs-lookup"><span data-stu-id="76e1a-173">Select **Toggle Screencast** ![Toggle Screencast][ImageToggleScreencastIcon] icon to view the content of your Android device in your DevTools instance.</span></span>  

<span data-ttu-id="76e1a-174">Вы можете взаимодействовать с презентацией следующими способами.</span><span class="sxs-lookup"><span data-stu-id="76e1a-174">You are able to interact with the screencast in the following ways.</span></span>  

*   <span data-ttu-id="76e1a-175">Нажатия клавиш переводятся в касания, и на устройстве обрабатывались соответствующие события сенсорного ввода.</span><span class="sxs-lookup"><span data-stu-id="76e1a-175">Clicks are translated into taps, firing proper touch events on the device.</span></span>  
*   <span data-ttu-id="76e1a-176">Нажатия клавиш на компьютере отправляются на устройство.</span><span class="sxs-lookup"><span data-stu-id="76e1a-176">Keystrokes on your computer are sent to the device.</span></span>  
*   <span data-ttu-id="76e1a-177">Чтобы смоделировать жест сжатия, удерживайте `Shift` при перетаскивании.</span><span class="sxs-lookup"><span data-stu-id="76e1a-177">To simulate a pinch gesture, hold `Shift` while dragging.</span></span>  
*   <span data-ttu-id="76e1a-178">Для прокрутки используйте сенсорной панели, колесико мыши или смахивание с помощью указателя мыши.</span><span class="sxs-lookup"><span data-stu-id="76e1a-178">To scroll, use your trackpad or mouse wheel, or fling with your mouse pointer.</span></span>

> [!NOTE]
> <span data-ttu-id="76e1a-179">Чтобы сделать презентацию более подсказками, воспользуйтесь приведенными ниже советами.</span><span class="sxs-lookup"><span data-stu-id="76e1a-179">Use the following tips to help you screencast.</span></span>  
> 
> *   <span data-ttu-id="76e1a-180">В ролики отображается только содержимое страницы.</span><span class="sxs-lookup"><span data-stu-id="76e1a-180">Screencasts only display page content.</span></span>  <span data-ttu-id="76e1a-181">Прозрачные части презентации представляют интерфейсы устройства, такие как адресная строка Microsoft EDGE, строка состояния Android или клавиатура Android.</span><span class="sxs-lookup"><span data-stu-id="76e1a-181">Transparent portions of the screencast represent device interfaces, such as the Microsoft Edge address bar, the Android status bar, or the Android keyboard.</span></span>  
> *   <span data-ttu-id="76e1a-182">Ролики негативно влияют на частоту кадров.</span><span class="sxs-lookup"><span data-stu-id="76e1a-182">Screencasts negatively affect frame rates.</span></span>  <span data-ttu-id="76e1a-183">Отключите экранную анимацию, изменяя прокрутки или анимации, чтобы получить более точную картину производительности страницы.</span><span class="sxs-lookup"><span data-stu-id="76e1a-183">Disable screencasting while measuring scrolls or animations to get a more accurate picture of the performance of your page.</span></span>  
> *   <span data-ttu-id="76e1a-184">Если экран вашего устройства с Android блокируется, содержимое презентации исчезнет.</span><span class="sxs-lookup"><span data-stu-id="76e1a-184">If your Android device screen locks, the content of your screencast disappears.</span></span>  <span data-ttu-id="76e1a-185">Разблокируйте экран устройства с Android для автоматического возобновления ролика.</span><span class="sxs-lookup"><span data-stu-id="76e1a-185">Unlock your Android device screen to automatically resume the screencast.</span></span>  

<!-- image links -->  

[ImageSelectElementIcon]: /microsoft-edge/devtools-guide-chromium/media/select-element-icon.msft.png  
[ImageToggleScreencastIcon]: /microsoft-edge/devtools-guide-chromium/media/toggle-screencast-icon.msft.png  

<!--[ImageRemoteDebugging]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging--remote-debugging.msft.png "old Figure 1:  Remote Debugging lets you inspect a page running on an Android device from your development machine"  -->  
<!--[ImageEdgeInspect]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-edge-inspect-no-targets.msft.png "Figure 1: The edge://inspect page in Microsoft Edge"  -->  
<!--[ImageAndroidPermissionPrompt]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-android-permissions-prompt.msft.png "Figure 2: The Allow USB Debugging permission prompt on an Android device"  -->  
<!--[ImageConnectedRemoteDevice]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-edge-inspect-with-targets.msft.png "Figure 3: A connected remote device"  -->  
<!-- [ImageReload]:  /microsoft-edge/devtools-guide-chromium/media/remote-debugging-edge-inspect-with-targets-buttons.msft.png "Figure 4: The buttons for focusing, reloading, or closing a tab"  -->  
<!--[ImageUnknownDevice]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging--unknown-device.msft.png "old Figure 4:  The Remote Devices tab has successfully detected an unknown device that is pending authorization"  -->  

<!-- links -->  

[AndroidUSBDrivers]: https://developer.android.com/tools/extras/oem-usb.html "Установка драйверов USB для OEM | Разработчики Android"  

<!-- [GitHubWebFundamentalsNewIssue]: https://github.com/Alphabet/webfundamentals/issues/new?title=[Remote%20Debugging] "GitHub - Web Fundamentals - New Issue"  -->  
[StackOverflowDevicesNotDetected]: https://stackoverflow.com/questions/21925992 "DevTools Devices не обнаруживает устройство при подключении к стеку с переполнением"  

[StackExchangeGalaxyS4DoesNotShowDialogBox]: https://android.stackexchange.com/questions/101933 "ADB — обмен данными в стеке для энтузиастов Android"  

> [!NOTE]
> <span data-ttu-id="76e1a-189">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="76e1a-189">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="76e1a-190">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="76e1a-190">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="76e1a-192">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="76e1a-192">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
