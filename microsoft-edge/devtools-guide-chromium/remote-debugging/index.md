---
title: Начало работы с удаленными отладкой устройств с Android
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: a9002ca82e6e0dcaf7f174b336e5c640929a561b
ms.sourcegitcommit: 33663cd7838dddee86228dde469a5e9551bddb02
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611821"
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




<!--
<style>
.devtools-inline {
  max-height: 1em;
  vertical-align: middle;
}
</style>
-->  
# <span data-ttu-id="3e3f3-103">Начало работы с удаленными отладкой устройств с Android</span><span class="sxs-lookup"><span data-stu-id="3e3f3-103">Get Started with Remote Debugging Android Devices</span></span>   



<span data-ttu-id="3e3f3-104">Удаленная отладка динамического содержимого на устройстве Android с компьютера Windows или macOS.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-104">Remote debug live content on an Android device from your Windows or macOS computer.</span></span>  <span data-ttu-id="3e3f3-105">В этом учебнике рассказывается о том, как выполнять следующие действия:</span><span class="sxs-lookup"><span data-stu-id="3e3f3-105">This tutorial teaches you how to:</span></span>  

*   <span data-ttu-id="3e3f3-106">Настройте устройство Android для удаленной отладки и найдите его на компьютере разработчика.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-106">Set up your Android device for remote debugging, and discover it from your development machine.</span></span>  
*   <span data-ttu-id="3e3f3-107">Изучите и отлаживать динамический контент на устройстве с Android с компьютера для разработки.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-107">Inspect and debug live content on your Android device from your development machine.</span></span>  
*   <span data-ttu-id="3e3f3-108">Содержимое ролика с устройства Android на экземпляр DevTools на компьютере разработчика.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-108">Screencast content from your Android device onto a DevTools instance on your development machine.</span></span>  

<!--
> ##### Figure 1  
> Remote Debugging lets you inspect a page running on an Android device from your development machine  
> ![Remote Debugging lets you inspect a page running on an Android device from your development machine][ImageRemoteDebugging]  -->

## <span data-ttu-id="3e3f3-109">Шаг 1: обнаружение устройства с Android</span><span class="sxs-lookup"><span data-stu-id="3e3f3-109">Step 1: Discover your Android device</span></span>   

<span data-ttu-id="3e3f3-110">Рабочий процесс, описанный ниже, подходит для большинства пользователей.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-110">The workflow below works for most users.</span></span>  <span data-ttu-id="3e3f3-111">Дополнительные сведения можно найти в [статье Устранение неполадок: DevTools не удается найти устройство Android](#troubleshooting-devtools-is-not-detecting-the-android-device) .</span><span class="sxs-lookup"><span data-stu-id="3e3f3-111">See [Troubleshooting: DevTools is not detecting the Android device](#troubleshooting-devtools-is-not-detecting-the-android-device) for more help.</span></span>  

1.  <span data-ttu-id="3e3f3-112">Откройте экран **Параметры разработчика** на устройстве с Android.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-112">Open the **Developer Options** screen on your Android.</span></span>  <span data-ttu-id="3e3f3-113">Дополнительные сведения [можно найти в разделе Настройка параметров разработчика на устройстве](https://developer.android.com/studio/debug/dev-options.html).</span><span class="sxs-lookup"><span data-stu-id="3e3f3-113">See [Configure On-Device Developer Options](https://developer.android.com/studio/debug/dev-options.html).</span></span>  
1.  <span data-ttu-id="3e3f3-114">Выберите **включить отладку USB**.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-114">Select **Enable USB Debugging**.</span></span>  
1.  <span data-ttu-id="3e3f3-115">На своем компьютере для разработки откройте Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-115">On your development machine, open Microsoft Edge.</span></span>  
1.  <span data-ttu-id="3e3f3-116">[Откройте DevTools][DevToolsOpen].</span><span class="sxs-lookup"><span data-stu-id="3e3f3-116">[Open DevTools][DevToolsOpen].</span></span>  
1.  <span data-ttu-id="3e3f3-117">В DevTools выберите **главное меню** , `...` а затем щелкните **другие инструменты**  >  **Удаленные устройства**.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-117">In DevTools, select the **Main Menu** `...` then select **More tools** > **Remote devices**.</span></span>  
    
    > ##### <span data-ttu-id="3e3f3-118">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="3e3f3-118">Figure 1</span></span>  
    > <span data-ttu-id="3e3f3-119">Открытие вкладки " **Удаленные устройства** " с помощью **главного меню**</span><span class="sxs-lookup"><span data-stu-id="3e3f3-119">Opening the **Remote Devices** tab via the **Main Menu**</span></span>  
    > <span data-ttu-id="3e3f3-120">! [Открытие вкладки удаленные устройства через главное меню] [ImageOpenRemoteDevices]</span><span class="sxs-lookup"><span data-stu-id="3e3f3-120">![Opening the Remote Devices tab via the Main Menu][ImageOpenRemoteDevices]</span></span>  

1.  <span data-ttu-id="3e3f3-121">В DevTools откройте вкладку **Параметры** .</span><span class="sxs-lookup"><span data-stu-id="3e3f3-121">In DevTools, open the **Settings** tab.</span></span>  

1.  <span data-ttu-id="3e3f3-122">Убедитесь, что флажок **обнаружение устройств USB** включен.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-122">Make sure that the **Discover USB devices** checkbox is enabled.</span></span>  
    
    > ##### <span data-ttu-id="3e3f3-123">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="3e3f3-123">Figure 2</span></span>  
    > <span data-ttu-id="3e3f3-124">Флажок " **обнаружение USB-устройств** " включен</span><span class="sxs-lookup"><span data-stu-id="3e3f3-124">The **Discover USB Devices** checkbox is enabled</span></span>  
    > <span data-ttu-id="3e3f3-125">! [Флажок обнаружение USB-устройств установлен] [ImageDiscoverUSBDevices]</span><span class="sxs-lookup"><span data-stu-id="3e3f3-125">![The Discover USB Devices checkbox is enabled][ImageDiscoverUSBDevices]</span></span>  

1.  <span data-ttu-id="3e3f3-126">Подключите устройство Android непосредственно к компьютеру разработчика с помощью USB-кабеля.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-126">Connect your Android device directly to your development machine using a USB cable.</span></span>  <span data-ttu-id="3e3f3-127">Когда вы в первый раз получите это, вы, скорее всего, видите, что DevTools обнаружил неизвестное устройство.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-127">The first time you do this, you usually see that DevTools has detected an unknown device.</span></span>  <span data-ttu-id="3e3f3-128">Если отображается зеленая точка и текст, **связанный** с названием модели устройства с Android, DevTools успешно установил подключение к устройству.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-128">If you see a green dot and the text **Connected** below the model name of your Android device, then DevTools has successfully established the connection to your device.</span></span>  <span data-ttu-id="3e3f3-129">Перейдите к [действию 2](#step-2-debug-content-on-your-android-device-from-your-development-machine).</span><span class="sxs-lookup"><span data-stu-id="3e3f3-129">Continue to [Step 2](#step-2-debug-content-on-your-android-device-from-your-development-machine).</span></span>  
    <!--
    > ##### Figure 4  
    > The **Remote Devices** tab has successfully detected an unknown device that is pending authorization  
    > ![The Remote Devices tab has successfully detected an unknown device that is pending authorization][ImageUnknownDevice]  -->

1.  <span data-ttu-id="3e3f3-130">Если ваше устройство отображается как **неизвестное**, используйте запрос разрешения на **отладку USB** на устройстве с Android.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-130">If your device is showing up as **Unknown**, accept the **Allow USB Debugging** permission prompt on your Android device.</span></span>  

### <span data-ttu-id="3e3f3-131">Устранение неполадок: DevTools не может обнаружить устройство с Android</span><span class="sxs-lookup"><span data-stu-id="3e3f3-131">Troubleshooting: DevTools is not detecting the Android device</span></span>   

<span data-ttu-id="3e3f3-132">Убедитесь, что оборудование настроено правильно.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-132">Make sure that your hardware is set up correctly:</span></span>  

*   <span data-ttu-id="3e3f3-133">Если вы используете USB-концентратор, попробуйте подключить устройство Android прямо к компьютеру разработчика.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-133">If you are using a USB hub, try connecting your Android device directly to your development machine instead.</span></span>  
*   <span data-ttu-id="3e3f3-134">Попробуйте отключить кабель USB между устройством Android и компьютером разработчика, а затем снова подключив его.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-134">Try unplugging the USB cable between your Android device and development machine, and then plugging it back in.</span></span>  <span data-ttu-id="3e3f3-135">Это можно сделать, когда экраны компьютера Android и разработки были разблокированы.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-135">Do it while your Android and development machine screens are unlocked.</span></span>  
*   <span data-ttu-id="3e3f3-136">Убедитесь, что USB-кабель работает.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-136">Make sure that your USB cable works.</span></span>  <span data-ttu-id="3e3f3-137">Вы должны иметь возможность проверять файлы на устройстве с Android с компьютера, на котором ведется разработка.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-137">You should be able to inspect files on your Android device from your development machine.</span></span>  

<span data-ttu-id="3e3f3-138">Убедитесь, что программное обеспечение настроено правильно.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-138">Make sure that your software is set up correctly:</span></span>  

*   <span data-ttu-id="3e3f3-139">Если на вашем компьютере разработчика установлена операционная система Windows, попробуйте установить драйверы USB для устройства с Android вручную.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-139">If your development machine is running Windows, try manually installing the USB drivers for your Android device.</span></span>  <span data-ttu-id="3e3f3-140">Ознакомьтесь с [Разустановочными драйверами USB для OEM][AndroidUSBDrivers].</span><span class="sxs-lookup"><span data-stu-id="3e3f3-140">See [Install OEM USB Drivers][AndroidUSBDrivers].</span></span>  
    
*   <span data-ttu-id="3e3f3-141">Некоторые комбинации устройств Windows и Android (особенно Samsung) требуют дополнительной настройки.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-141">Some combinations of Windows and Android devices (especially Samsung) require extra set up.</span></span>  <span data-ttu-id="3e3f3-142">В разделе [DevTools Devices (устройства) не обнаруживаются устройства, подключенные к сети] [StackOverflowDevicesNotDetected].</span><span class="sxs-lookup"><span data-stu-id="3e3f3-142">See [DevTools Devices does not detect device when plugged in][StackOverflowDevicesNotDetected].</span></span>  
    
<span data-ttu-id="3e3f3-143">Если вы не видите предупреждение **Разрешить отладку USB** на устройстве с Android, попробуйте выполнить указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-143">If you do not see the **Allow USB Debugging** prompt on your Android device try:</span></span>  

*   <span data-ttu-id="3e3f3-144">Отключение кабеля USB и повторное подключение к нему, когда DevTools на компьютере разработки и отображается начальный экран на устройстве с Android.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-144">Disconnecting and then re-connecting the USB cable while DevTools is in focus on your development machine and your Android homescreen is showing.</span></span>  <span data-ttu-id="3e3f3-145">Другими словами, иногда сообщение не отображается, когда экраны компьютера Android или разработчика заблокированы.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-145">In other words, sometimes the prompt does not show up when your Android or development machine screens are locked.</span></span>
*   <span data-ttu-id="3e3f3-146">Обновите параметры отображения для устройства Android и компьютера для разработки, чтобы они никогда не переходят в спящий режим.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-146">Updating the display settings for your Android device and development machine so that they never go to sleep.</span></span>  
*   <span data-ttu-id="3e3f3-147">Установка режима USB для устройства с Android на PTP.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-147">Setting the USB mode for Android to PTP.</span></span>  <span data-ttu-id="3e3f3-148">В разделе [Galaxy S4 не отображается диалоговое окно "авторизация USB"][StackExchangeGalaxyS4DoesNotShowDialogBox].</span><span class="sxs-lookup"><span data-stu-id="3e3f3-148">See [Galaxy S4 does not show Authorize USB debugging dialog box][StackExchangeGalaxyS4DoesNotShowDialogBox].</span></span>  
*   <span data-ttu-id="3e3f3-149">Выберите **отозвать разрешения на отладку USB** на экране **Параметры разработчика** на устройстве с Android, чтобы сбросить его в новое состояние.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-149">Select **Revoke USB Debugging Authorizations** from the **Developer Options** screen on your Android device to reset it to a fresh state.</span></span>  

<span data-ttu-id="3e3f3-150">Если вы нашли решение, которое не упомянуто в этом разделе, или в [DevTools Devices не обнаружит устройство при подключении к сети] [StackOverflowDevicesNotDetected] или добавьте ответ на этот вопрос с переполнением стека.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-150">If you find a solution that is not mentioned in this section or in [DevTools Devices does not detect device when plugged in][StackOverflowDevicesNotDetected] or please add an answer to that Stack Overflow question</span></span><!--, or [open an issue in the webfundamentals repository][GitHubWebFundamentalsNewIssue]--><span data-ttu-id="3e3f3-151">!</span><span class="sxs-lookup"><span data-stu-id="3e3f3-151">!</span></span>  

## <span data-ttu-id="3e3f3-152">Шаг 2: Отладка содержимого на устройстве с Android с компьютера для разработки</span><span class="sxs-lookup"><span data-stu-id="3e3f3-152">Step 2: Debug content on your Android device from your development machine</span></span>   

1.  <span data-ttu-id="3e3f3-153">Откройте Microsoft EDGE на устройстве с Android.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-153">Open Microsoft Edge on your Android device.</span></span>  

1.  <span data-ttu-id="3e3f3-154">На вкладке **Удаленные устройства** выберите вкладку, которая соответствует имени модели устройства Android.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-154">In the **Remote Devices** tab, select the tab that matches your Android device model name.</span></span>  
    <span data-ttu-id="3e3f3-155">В верхней части этой страницы вы увидите название модели устройства с Android, а затем серийный номер.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-155">At the top of this page, you see the model name of your Android device, followed by its serial number.</span></span>  <span data-ttu-id="3e3f3-156">Ниже показана версия Microsoft EDGE, установленная на устройстве, с номером версии в круглых скобках.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-156">Below that, you should see the version of Microsoft Edge running on the device, with the version number in parentheses.</span></span>  <span data-ttu-id="3e3f3-157">Каждая открытая вкладка Microsoft Edge получает собственный раздел.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-157">Each open Microsoft Edge tab gets its own section.</span></span>  <span data-ttu-id="3e3f3-158">Вы можете работать с этой вкладкой в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-158">You may interact with that tab from this section.</span></span>  <!--If there are any apps using WebView, you see a section for each of those apps, too.  --><!--In [**Figure 5**](#figure-5) there are no tabs or WebViews open.  -->
    <!--
    > ##### Figure 5  
    > A connected remote device  
    > ![A connected remote device][ImageConnectedRemoteDevice]  -->

1.  <span data-ttu-id="3e3f3-159">В текстовом поле **Новая вкладка** введите URL-адрес и нажмите кнопку **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-159">In the **New tab** text box, enter a URL and then select **Open**.</span></span>  <span data-ttu-id="3e3f3-160">Страница откроется на новой вкладке на устройстве с Android.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-160">The page opens in a new tab on your Android device.</span></span>  

1.  <span data-ttu-id="3e3f3-161">Нажмите кнопку " **проверить** " рядом с URL-адресом, который вы только что открыли.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-161">Select **Inspect** next to the URL that you just opened.</span></span>  <span data-ttu-id="3e3f3-162">Откроется новый экземпляр DevTools.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-162">A new DevTools instance opens.</span></span>  <span data-ttu-id="3e3f3-163">Версия Microsoft EDGE, установленная на устройстве с Android, определяет версию DevTools, которая открывается на компьютере разработчика.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-163">The version of Microsoft Edge running on your Android device determines the version of DevTools that opens on your development machine.</span></span>  
    <span data-ttu-id="3e3f3-164">Таким образом, если на вашем устройстве Android установлена старая версия Microsoft EDGE, экземпляр DevTools может отличаться от того, с чем вы используете.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-164">So, if your Android device is running a very old version of Microsoft Edge, the DevTools instance may look very different than what you are used to.</span></span>  

### <span data-ttu-id="3e3f3-165">Дополнительные действия: перезагрузка, фокус или закрытие вкладки</span><span class="sxs-lookup"><span data-stu-id="3e3f3-165">More actions: reload, focus, or close a tab</span></span>   

<span data-ttu-id="3e3f3-166">Щелкните значок **Дополнительные параметры** `...` рядом с вкладкой, которую вы хотите перегрузить, сосредоточиться или закрыть.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-166">Select **More Options** `...` next to the tab that you want to reload, focus, or close.</span></span>  
<!--
> ##### Figure 6  
> The menu for reloading, focusing, or closing a tab  
> ![The menu for reloading, focusing, or closing a tab][ImageReload]  -->

### <span data-ttu-id="3e3f3-167">Проверка элементов</span><span class="sxs-lookup"><span data-stu-id="3e3f3-167">Inspect elements</span></span>   

<span data-ttu-id="3e3f3-168">Перейдите на панель **элементы** экземпляра DevTools и наведите указатель мыши на элемент, чтобы выделить его в окне просмотра на устройстве с Android.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-168">Go to the **Elements** panel of your DevTools instance, and hover over an element to highlight it in the viewport of your Android device.</span></span>  

<span data-ttu-id="3e3f3-169">Вы также можете выбрать элемент на экране устройства с Android, чтобы выбрать его на панели " **элементы** ".</span><span class="sxs-lookup"><span data-stu-id="3e3f3-169">You may also select an element on your Android device screen to select it in the **Elements** panel.</span></span>  <span data-ttu-id="3e3f3-170">Выберите пункт выбрать элемент SELECT **элемента** ![ ][ImageSelectElementIcon] в экземпляре DevTools, а затем выберите элемент на экране устройства с Android.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-170">Select **Select Element** ![Select Element][ImageSelectElementIcon] on your DevTools instance, and then select the element on your Android device screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="3e3f3-171">**Элемент "выбрать** " отключается после первого выбора, поэтому при каждом использовании этой функции необходимо повторно включить его.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-171">**Select Element** is disabled after the first selection, so you must re-enable it every time you want to use this feature.</span></span>  

### <span data-ttu-id="3e3f3-172">Демонстрация экрана Android на компьютере разработчика</span><span class="sxs-lookup"><span data-stu-id="3e3f3-172">Screencast your Android screen to your development machine</span></span>   

<span data-ttu-id="3e3f3-173">Нажмите **кнопку Переключить** презентацию, ![ ][ImageToggleScreencastIcon] чтобы просмотреть содержимое устройства с Android в экземпляре DevTools.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-173">Select **Toggle Screencast** ![Toggle Screencast][ImageToggleScreencastIcon] to view the content of your Android device in your DevTools instance.</span></span>  

<span data-ttu-id="3e3f3-174">Вы можете работать с презентацией несколькими способами.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-174">You are able to interact with the screencast in multiple ways:</span></span>  

*   <span data-ttu-id="3e3f3-175">Нажатия клавиш переводятся в касания, и на устройстве обрабатывались соответствующие события сенсорного ввода.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-175">Clicks are translated into taps, firing proper touch events on the device.</span></span>  
*   <span data-ttu-id="3e3f3-176">Нажатия клавиш на компьютере отправляются на устройство.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-176">Keystrokes on your computer are sent to the device.</span></span>  
*   <span data-ttu-id="3e3f3-177">Чтобы смоделировать жест сжатия, удерживайте `Shift` при перетаскивании.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-177">To simulate a pinch gesture, hold `Shift` while dragging.</span></span>  
*   <span data-ttu-id="3e3f3-178">Для прокрутки используйте сенсорной панели, колесико мыши или смахивание с помощью указателя мыши.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-178">To scroll, use your trackpad or mouse wheel, or fling with your mouse pointer.</span></span>

<span data-ttu-id="3e3f3-179">Некоторые заметки для презентаций:</span><span class="sxs-lookup"><span data-stu-id="3e3f3-179">Some notes on screencasts:</span></span>  

*   <span data-ttu-id="3e3f3-180">В ролики отображается только содержимое страницы.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-180">Screencasts only display page content.</span></span>  <span data-ttu-id="3e3f3-181">Прозрачные части презентации представляют интерфейсы устройства, такие как адресная строка Microsoft EDGE, строка состояния Android или клавиатура Android.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-181">Transparent portions of the screencast represent device interfaces, such as the Microsoft Edge address bar, the Android status bar, or the Android keyboard.</span></span>  
*   <span data-ttu-id="3e3f3-182">Ролики негативно влияют на частоту кадров.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-182">Screencasts negatively affect frame rates.</span></span>  <span data-ttu-id="3e3f3-183">Отключите экранную анимацию, изменяя прокрутки или анимации, чтобы получить более точную картину производительности страницы.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-183">Disable screencasting while measuring scrolls or animations to get a more accurate picture of the performance of your page.</span></span>  
*   <span data-ttu-id="3e3f3-184">Если экран вашего устройства с Android блокируется, содержимое презентации исчезнет.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-184">If your Android device screen locks, the content of your screencast disappears.</span></span>  <span data-ttu-id="3e3f3-185">Разблокируйте экран устройства с Android для автоматического возобновления ролика.</span><span class="sxs-lookup"><span data-stu-id="3e3f3-185">Unlock your Android device screen to automatically resume the screencast.</span></span>  





<!-- image links -->  

[ImageSelectElementIcon]: /microsoft-edge/devtools-guide-chromium/media/select-element-icon.msft.png  
[ImageToggleScreencastIcon]: /microsoft-edge/devtools-guide-chromium/media/toggle-screencast-icon.msft.png  

<!--[ImageRemoteDebugging]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging--remote-debugging.msft.png "old Figure 1:  Remote Debugging lets you inspect a page running on an Android device from your development machine"  -->  
[ImageOpenRemoteDevices]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Remote-Debugging-more-Tools-Remote-Devices.MSFT.png "Рисунок 1: Открытие вкладки" Удаленные устройства "через главное меню  
[ImageDiscoverUSBDevices]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Remote-Debugging-Remote-Devices-Tab.MSFT.png "Рисунок 2: флажок" обнаружение USB-устройств "включен.  
<!--[ImageUnknownDevice]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging--unknown-device.msft.png "old Figure 4:  The Remote Devices tab has successfully detected an unknown device that is pending authorization"  -->  
<!--[ImageConnectedRemoteDevice]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging--connected-remote-device.msft.png "old Figure 5:  A connected remote device"  -->
<!--[ImageReload]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging--reload.msft.png "old Figure 6: The menu for reloading, focusing, or closing a tab"  -->

<!-- links -->  

[DevToolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Открыть Microsoft Edge DevTools"  

[AndroidUSBDrivers]: https://developer.android.com/tools/extras/oem-usb.html "Установка драйверов USB для OEM | Разработчики Android"  

<!-- [GitHubWebFundamentalsNewIssue]: https://github.com/Alphabet/webfundamentals/issues/new?title=[Remote%20Debugging] "GitHub - Web Fundamentals - New Issue"  -->  
[StackOverflowDevicesNotDetected]: https://stackoverflow.com/questions/21925992 "DevTools Devices не обнаруживает устройство при подключении к стеку с переполнением"  

[StackExchangeGalaxyS4DoesNotShowDialogBox]: https://android.stackexchange.com/questions/101933 "ADB — обмен данными в стеке для энтузиастов Android"  

> [!NOTE]
> <span data-ttu-id="3e3f3-192">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3e3f3-192">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="3e3f3-193">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="3e3f3-193">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="3e3f3-195">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="3e3f3-195">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
