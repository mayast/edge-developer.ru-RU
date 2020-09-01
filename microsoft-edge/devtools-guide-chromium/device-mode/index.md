---
title: Эмуляция мобильных устройств с помощью режима устройства в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 08/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: microsoft edge, веб-разработка, инструменты f12, средства разработчика
ms.openlocfilehash: 6973f28a0cb530e8928976adb1354fa7471ee343
ms.sourcegitcommit: 1251c555c6b4db8ef8187ed94d8832fdb89d03b8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/31/2020
ms.locfileid: "10985338"
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





# <span data-ttu-id="33068-103">Эмуляция мобильных устройств с помощью режима устройства в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="33068-103">Simulate mobile devices with Device Mode in Microsoft Edge DevTools</span></span>   

  

<span data-ttu-id="33068-104">С помощью режима устройства вы можете оценить внешний вид страницы и ее выполнение на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="33068-104">Use Device Mode to approximate how your page looks and performs on a mobile device.</span></span>  

<span data-ttu-id="33068-105">Режим устройства — это имя для свободной коллекции функций в Microsoft Edge DevTools, которые помогают имитировать мобильные устройства.</span><span class="sxs-lookup"><span data-stu-id="33068-105">Device Mode is the name for the loose collection of features in Microsoft Edge DevTools that help you simulate mobile devices.</span></span>  <span data-ttu-id="33068-106">К таким функциям относятся:</span><span class="sxs-lookup"><span data-stu-id="33068-106">These features include:</span></span>  

*   [<span data-ttu-id="33068-107">Имитация окна просмотра для мобильных устройств</span><span class="sxs-lookup"><span data-stu-id="33068-107">Simulating a mobile viewport</span></span>](#simulate-a-mobile-viewport)  
*   [<span data-ttu-id="33068-108">Регулирование сети</span><span class="sxs-lookup"><span data-stu-id="33068-108">Throttling the network</span></span>](#throttle-the-network-only)  
*   [<span data-ttu-id="33068-109">Регулирование ЦП</span><span class="sxs-lookup"><span data-stu-id="33068-109">Throttling the CPU</span></span>](#throttle-the-cpu-only)  
*   [<span data-ttu-id="33068-110">Имитация географического местоположения</span><span class="sxs-lookup"><span data-stu-id="33068-110">Simulating geolocation</span></span>](#override-geolocation)  
*   [<span data-ttu-id="33068-111">Настройка ориентации</span><span class="sxs-lookup"><span data-stu-id="33068-111">Setting orientation</span></span>](#set-orientation)  

## <span data-ttu-id="33068-112">Ограничения</span><span class="sxs-lookup"><span data-stu-id="33068-112">Limitations</span></span>   

<span data-ttu-id="33068-113">Режим устройства облагается [приблизительно][WikiApproximation] так, как выглядит страница на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="33068-113">Think of Device Mode as a [first-order approximation][WikiApproximation] of how your page looks and feels on a mobile device.</span></span>  <span data-ttu-id="33068-114">В режиме устройства вы фактически не запускаете ваш код на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="33068-114">With Device Mode you do not actually run your code on a mobile device.</span></span>  <span data-ttu-id="33068-115">Вы имитируете взаимодействие с пользователем на мобильном устройстве или компьютере.</span><span class="sxs-lookup"><span data-stu-id="33068-115">You simulate the mobile user experience from your laptop or desktop.</span></span>  

<span data-ttu-id="33068-116">Некоторые аспекты мобильных устройств, которые DevTools никогда не смогут имитировать.</span><span class="sxs-lookup"><span data-stu-id="33068-116">There are some aspects of mobile devices that DevTools will never be able to simulate.</span></span>  <span data-ttu-id="33068-117">Например, архитектура мобильных процессоров очень отличается от архитектуры ноутбука или процессоров для настольных ПК.</span><span class="sxs-lookup"><span data-stu-id="33068-117">For example, the architecture of mobile CPUs is very different than the architecture of laptop or desktop CPUs.</span></span>  <span data-ttu-id="33068-118">Если вы сомневаетесь, лучше использовать страницу на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="33068-118">When in doubt, your best bet is to actually run your page on a mobile device.</span></span>  <span data-ttu-id="33068-119">Использование [удаленной отладки] [DevToolsRemoteDebugging] для просмотра, изменения, отладки и профилирования кода страницы на мобильном устройстве или рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="33068-119">Use [Remote Debugging][DevToolsRemoteDebugging] to view, change, debug, and profile the code of a page from your laptop or desktop while it actually runs on a mobile device.</span></span>  

## <span data-ttu-id="33068-120">Имитация окна просмотра для мобильных устройств</span><span class="sxs-lookup"><span data-stu-id="33068-120">Simulate a mobile viewport</span></span>   

<span data-ttu-id="33068-121">Нажмите кнопку **Переключить панель инструментов** \ ( ![ Переключить панель инструментов устройства ][ImageDeviceToolbarIcon] ), чтобы открыть пользовательский интерфейс, позволяющий имитировать окно просмотра для мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="33068-121">Click **Toggle Device Toolbar** \(![Toggle Device Toolbar][ImageDeviceToolbarIcon]\) to open the UI that enables you to simulate a mobile viewport.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Панель инструментов "устройства"" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   <span data-ttu-id="33068-123">Панель инструментов "устройства"</span><span class="sxs-lookup"><span data-stu-id="33068-123">The Device Toolbar</span></span>  
:::image-end:::  

<span data-ttu-id="33068-124">По умолчанию панель инструментов устройства открывается в режиме отклика окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="33068-124">By default the Device Toolbar opens in Responsive Viewport Mode.</span></span>  

### <span data-ttu-id="33068-125">Режим окна просмотра с откликом</span><span class="sxs-lookup"><span data-stu-id="33068-125">Responsive Viewport Mode</span></span>   

<span data-ttu-id="33068-126">Перетащите маркеры, чтобы изменить размер окна просмотра в соответствии с нужными размерами.</span><span class="sxs-lookup"><span data-stu-id="33068-126">Drag the handles to resize the viewport to whatever dimensions you need.</span></span>  <span data-ttu-id="33068-127">Кроме того, можно ввести значения в полях Ширина и высота.</span><span class="sxs-lookup"><span data-stu-id="33068-127">Or, enter specific values in the width and height boxes.</span></span>  <span data-ttu-id="33068-128">На приведенном ниже рисунке задана ширина `626` и высота задана `516` .</span><span class="sxs-lookup"><span data-stu-id="33068-128">In the following figure, the width is set to `626` and the height is set to `516`.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png" alt-text="Дескрипторы для изменения размеров окна просмотра в отклике режима просмотра" lightbox="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png":::
   <span data-ttu-id="33068-130">Дескрипторы для изменения размеров окна просмотра в отклике режима просмотра</span><span class="sxs-lookup"><span data-stu-id="33068-130">The handles for changing the dimensions of the viewport when in Responsive Viewport Mode</span></span>  
:::image-end:::  

#### <span data-ttu-id="33068-131">Показать мультимедийные запросы</span><span class="sxs-lookup"><span data-stu-id="33068-131">Show media queries</span></span>   

<span data-ttu-id="33068-132">Чтобы отобразить точки останова для запросов мультимедиа над окном просмотра, нажмите кнопку **Дополнительные параметры** и выберите пункт **Показать мультимедийные запросы**.</span><span class="sxs-lookup"><span data-stu-id="33068-132">To show media query breakpoints above your viewport, click **More options** and then select **Show media queries**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png" alt-text="Показать мультимедийные запросы" lightbox="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png":::
   **<span data-ttu-id="33068-134">Показать мультимедийные запросы</span><span class="sxs-lookup"><span data-stu-id="33068-134">Show media queries</span></span>**  
:::image-end:::  

<span data-ttu-id="33068-135">Щелкните точку останова, чтобы изменить ширину окна просмотра таким образом, чтобы точка останова была инициирована.</span><span class="sxs-lookup"><span data-stu-id="33068-135">Click a breakpoint to change the width of the viewport so that the breakpoint gets triggered.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png" alt-text="Щелкните точку останова, чтобы изменить ширину окна просмотра" lightbox="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png":::
   <span data-ttu-id="33068-137">Щелкните точку останова, чтобы изменить ширину окна просмотра</span><span class="sxs-lookup"><span data-stu-id="33068-137">Click a breakpoint to change the width of the viewport</span></span>  
:::image-end:::  

#### <span data-ttu-id="33068-138">Настройка типа устройства</span><span class="sxs-lookup"><span data-stu-id="33068-138">Set the device type</span></span>   

<span data-ttu-id="33068-139">Используйте список **типов устройств** для имитации мобильного устройства или настольного устройства.</span><span class="sxs-lookup"><span data-stu-id="33068-139">Use the **Device Type** list to simulate a mobile device or desktop device.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png" alt-text="Список типов устройств" lightbox="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png":::
   <span data-ttu-id="33068-141">Список **типов устройств**</span><span class="sxs-lookup"><span data-stu-id="33068-141">The **Device Type** list</span></span>  
:::image-end:::  

<span data-ttu-id="33068-142">В приведенной ниже таблице описаны различия между параметрами.</span><span class="sxs-lookup"><span data-stu-id="33068-142">The table below describes the differences between the options.</span></span>  <span data-ttu-id="33068-143">**Метод рендеринга** указывает, будет ли Microsoft Edge обрабатывать страницу в виде окна просмотра на мобильном или рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="33068-143">**Rendering method** refers to whether Microsoft Edge renders the page as a mobile or desktop viewport.</span></span>  <span data-ttu-id="33068-144">**Значок курсора** указывает на тип курсора, который отображается при наведении указателя мыши на страницу.</span><span class="sxs-lookup"><span data-stu-id="33068-144">**Cursor icon** refers to what type of cursor you see when you hover over the page.</span></span>  <span data-ttu-id="33068-145">**События, созданные** в зависимости от того, срабатывает ли страница `touch` или `click` события при взаимодействии со страницей.</span><span class="sxs-lookup"><span data-stu-id="33068-145">**Events fired** refers to whether the page fires `touch` or `click` events when you interact with the page.</span></span>  

| <span data-ttu-id="33068-146">Параметр</span><span class="sxs-lookup"><span data-stu-id="33068-146">Option</span></span> | <span data-ttu-id="33068-147">Метод отрисовки</span><span class="sxs-lookup"><span data-stu-id="33068-147">Rendering method</span></span> | <span data-ttu-id="33068-148">Значок курсора</span><span class="sxs-lookup"><span data-stu-id="33068-148">Cursor icon</span></span> | <span data-ttu-id="33068-149">События, созданные</span><span class="sxs-lookup"><span data-stu-id="33068-149">Events fired</span></span> |  
|:--- |:--- |:--- |:--- |  
| <span data-ttu-id="33068-150">Мобильные устройства</span><span class="sxs-lookup"><span data-stu-id="33068-150">Mobile</span></span> | <span data-ttu-id="33068-151">Мобильные устройства</span><span class="sxs-lookup"><span data-stu-id="33068-151">Mobile</span></span> | <span data-ttu-id="33068-152">Круг</span><span class="sxs-lookup"><span data-stu-id="33068-152">Circle</span></span> | <span data-ttu-id="33068-153">Сенсорный ввод</span><span class="sxs-lookup"><span data-stu-id="33068-153">touch</span></span> |  
| <span data-ttu-id="33068-154">Мобильный – (без сенсорных устройств)</span><span class="sxs-lookup"><span data-stu-id="33068-154">Mobile \(no touch\)</span></span> | <span data-ttu-id="33068-155">Мобильные устройства</span><span class="sxs-lookup"><span data-stu-id="33068-155">Mobile</span></span> | <span data-ttu-id="33068-156">Обычный</span><span class="sxs-lookup"><span data-stu-id="33068-156">Normal</span></span> | <span data-ttu-id="33068-157"> нажмите </span><span class="sxs-lookup"><span data-stu-id="33068-157">click</span></span> |  
| <span data-ttu-id="33068-158">Desktop</span><span class="sxs-lookup"><span data-stu-id="33068-158">Desktop</span></span> | <span data-ttu-id="33068-159">Desktop</span><span class="sxs-lookup"><span data-stu-id="33068-159">Desktop</span></span> | <span data-ttu-id="33068-160">Обычный</span><span class="sxs-lookup"><span data-stu-id="33068-160">Normal</span></span> | <span data-ttu-id="33068-161"> нажмите </span><span class="sxs-lookup"><span data-stu-id="33068-161">click</span></span> |  
| <span data-ttu-id="33068-162">Классическое приложение (касание)</span><span class="sxs-lookup"><span data-stu-id="33068-162">Desktop \(touch\)</span></span> | <span data-ttu-id="33068-163">Desktop</span><span class="sxs-lookup"><span data-stu-id="33068-163">Desktop</span></span> | <span data-ttu-id="33068-164">Круг</span><span class="sxs-lookup"><span data-stu-id="33068-164">Circle</span></span> | <span data-ttu-id="33068-165">Сенсорный ввод</span><span class="sxs-lookup"><span data-stu-id="33068-165">touch</span></span> |  

> [!NOTE]
> <span data-ttu-id="33068-166">Если список **тип устройства** не отображается, нажмите кнопку **Дополнительные параметры** и выберите команду **Добавить тип устройства**.</span><span class="sxs-lookup"><span data-stu-id="33068-166">If you do not see the **Device Type** list, click **More options** and select **Add device type**.</span></span>  

### <span data-ttu-id="33068-167">Режим просмотра на мобильном устройстве</span><span class="sxs-lookup"><span data-stu-id="33068-167">Mobile Device Viewport Mode</span></span>   

<span data-ttu-id="33068-168">Чтобы смоделировать размеры определенного мобильного устройства, выберите нужное устройство из списка **устройств** .</span><span class="sxs-lookup"><span data-stu-id="33068-168">To simulate the dimensions of a specific mobile device, select the device from the **Device** list.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list.msft.png" alt-text="Список устройств" lightbox="../media/device-mode-toggle-device-toolbar-device-list.msft.png":::
   <span data-ttu-id="33068-170">Список **устройств**</span><span class="sxs-lookup"><span data-stu-id="33068-170">The **Device** list</span></span>  
:::image-end:::  

#### <span data-ttu-id="33068-171">Поворот окна просмотра на альбомную ориентацию</span><span class="sxs-lookup"><span data-stu-id="33068-171">Rotate the viewport to landscape orientation</span></span>   

<span data-ttu-id="33068-172">**Rotate** ![ ][ImageRotateIcon] Чтобы повернуть окно просмотра на альбомную ориентацию, нажмите повернуть на (повернуть).</span><span class="sxs-lookup"><span data-stu-id="33068-172">Click **Rotate** \(![Rotate][ImageRotateIcon]\) to rotate the viewport to landscape orientation.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-landscape.msft.png" alt-text="Альбомная ориентация" lightbox="../media/device-mode-toggle-device-toolbar-landscape.msft.png":::
   <span data-ttu-id="33068-174">Альбомная ориентация</span><span class="sxs-lookup"><span data-stu-id="33068-174">Landscape orientation</span></span>  
:::image-end:::  

> [!NOTE]
> <span data-ttu-id="33068-175">Кнопка **повернуть** исчезнет, если **панель инструментов на устройстве** является узкой.</span><span class="sxs-lookup"><span data-stu-id="33068-175">The **Rotate** button disappears if your **Device Toolbar** is narrow.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Панель инструментов "устройства"" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   <span data-ttu-id="33068-177">**Панель инструментов "устройства** "</span><span class="sxs-lookup"><span data-stu-id="33068-177">The **Device Toolbar**</span></span>  
:::image-end:::  

<span data-ttu-id="33068-178">Смотрите также [Настройка ориентации](#set-orientation).</span><span class="sxs-lookup"><span data-stu-id="33068-178">See also [Set orientation](#set-orientation).</span></span>  

#### <span data-ttu-id="33068-179">Показать рамку устройства</span><span class="sxs-lookup"><span data-stu-id="33068-179">Show device frame</span></span>   

<span data-ttu-id="33068-180">При моделировании размеров определенного мобильного устройства, например iPhone 6, откройте **меню Дополнительные параметры** и выберите пункт **Показать рамку устройства** , чтобы отобразить рамку физического устройства вокруг окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="33068-180">When simulating the dimensions of a specific mobile device like an iPhone 6, open **More options** and then select **Show device frame** to show the physical device frame around the viewport.</span></span>  

> [!NOTE]
> <span data-ttu-id="33068-181">Если вы не видите рамку устройства для определенного устройства, скорее всего, это означает, что DevTools просто не имеет иллюстраций для определенного параметра.</span><span class="sxs-lookup"><span data-stu-id="33068-181">If you do not see a device frame for a particular device, it probably means that DevTools just does not have art for that specific option.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png" alt-text="Показать рамку устройства" lightbox="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png":::
         <span data-ttu-id="33068-183">Показать рамку устройства</span><span class="sxs-lookup"><span data-stu-id="33068-183">Show device frame</span></span>  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png" alt-text="Рамка устройства для iPhone 6" lightbox="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png":::
         <span data-ttu-id="33068-185">Рамка устройства для iPhone 6</span><span class="sxs-lookup"><span data-stu-id="33068-185">The device frame for the iPhone 6</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

#### <span data-ttu-id="33068-186">Добавление настраиваемого мобильного устройства</span><span class="sxs-lookup"><span data-stu-id="33068-186">Add a custom mobile device</span></span>   

<span data-ttu-id="33068-187">Чтобы добавить настраиваемое устройство, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="33068-187">To add a custom device:</span></span>  

1.  <span data-ttu-id="33068-188">Щелкните список **устройств** и выберите команду **изменить**.</span><span class="sxs-lookup"><span data-stu-id="33068-188">Click the **Device** list and then select **Edit**.</span></span>  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png" alt-text="Нажмите кнопку Изменить." lightbox="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png":::
       <span data-ttu-id="33068-190">Нажмите кнопку **изменить** .</span><span class="sxs-lookup"><span data-stu-id="33068-190">Select **Edit**</span></span>  
    :::image-end:::  
    
1.  <span data-ttu-id="33068-191">Нажмите кнопку **Добавить настраиваемое устройство**.</span><span class="sxs-lookup"><span data-stu-id="33068-191">Click **Add custom device**.</span></span>  
1.  <span data-ttu-id="33068-192">Введите имя, ширину и высоту устройства.</span><span class="sxs-lookup"><span data-stu-id="33068-192">Enter a name, width, and height for the device.</span></span>  <span data-ttu-id="33068-193">Поля « [отношение к пикселям][MDNWindowDevicePixelRatio]», « [строка агента пользователя][MDNUserAgent]» и « [тип устройства](#set-the-device-type) » являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="33068-193">The [device pixel ratio][MDNWindowDevicePixelRatio], [user agent string][MDNUserAgent], and [device type](#set-the-device-type) fields are optional.</span></span>  <span data-ttu-id="33068-194">Поле «Тип устройства» — это список, который по умолчанию имеет значение " **мобильный** ".</span><span class="sxs-lookup"><span data-stu-id="33068-194">The device type field is the list that is set to **Mobile** by default.</span></span>  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png" alt-text="Создание настраиваемого устройства" lightbox="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png":::
       <span data-ttu-id="33068-196">Создание настраиваемого устройства</span><span class="sxs-lookup"><span data-stu-id="33068-196">Createa custom device</span></span>  
    :::image-end:::  

### <span data-ttu-id="33068-197">Отображение линеек</span><span class="sxs-lookup"><span data-stu-id="33068-197">Show rulers</span></span>   

<span data-ttu-id="33068-198">Нажмите кнопку **Дополнительные параметры** , а затем выберите пункт **Показывать линейки** , чтобы увидеть линейки сверху и слева от окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="33068-198">Click **More options** and then select **Show rulers** to see rulers above and to the left of your viewport.</span></span>  <span data-ttu-id="33068-199">Единица измерения линеек — Пиксели.</span><span class="sxs-lookup"><span data-stu-id="33068-199">The sizing unit of the rulers is pixels.</span></span>  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png" alt-text="Отображение линеек" lightbox="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png":::
         **<span data-ttu-id="33068-201">Отображение линеек</span><span class="sxs-lookup"><span data-stu-id="33068-201">Show rulers</span></span>**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-rulers.msft.png" alt-text="Линейки сверху и слева от окна просмотра" lightbox="../media/device-mode-toggle-device-toolbar-rulers.msft.png":::
         <span data-ttu-id="33068-203">Линейки сверху и слева от окна просмотра</span><span class="sxs-lookup"><span data-stu-id="33068-203">Rulers above and to the left of the viewport</span></span>  
      :::image-end:::  
   :::column-end:::
:::row-end:::

### <span data-ttu-id="33068-204">Изменение масштаба просмотра</span><span class="sxs-lookup"><span data-stu-id="33068-204">Zoom the viewport</span></span>   

<span data-ttu-id="33068-205">С помощью списка **масштаб** вы можете увеличить или уменьшить масштаб.</span><span class="sxs-lookup"><span data-stu-id="33068-205">Use the **Zoom** list to zoom in or out.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-zoom.msft.png" alt-text="Масштаб" lightbox="../media/device-mode-toggle-device-toolbar-zoom.msft.png":::
   **<span data-ttu-id="33068-207">Масштаб</span><span class="sxs-lookup"><span data-stu-id="33068-207">Zoom</span></span>**  
:::image-end:::  

## <span data-ttu-id="33068-208">Регулирование сети и ЦП</span><span class="sxs-lookup"><span data-stu-id="33068-208">Throttle the network and CPU</span></span>   

<span data-ttu-id="33068-209">Для регулирования сети и ЦП выберите на **мобильном** или **низком мобильном** уровне в списке **регулирования** .</span><span class="sxs-lookup"><span data-stu-id="33068-209">To throttle the network and CPU, select **Mid-tier mobile** or **Low-end mobile** from the **Throttle** list.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-throttle.msft.png" alt-text="Список регулирования" lightbox="../media/device-mode-toggle-device-toolbar-throttle.msft.png":::
   <span data-ttu-id="33068-211">Список **регулирования**</span><span class="sxs-lookup"><span data-stu-id="33068-211">The **Throttle** list</span></span>  
:::image-end:::  

<span data-ttu-id="33068-212">На **мобильном устройстве с уровнем "среднее** " эмулируется быстрое соединение и снижается частота центрального процессора, так как это происходит в течение 4 часов, чем обычно.</span><span class="sxs-lookup"><span data-stu-id="33068-212">**Mid-tier mobile** simulates fast 3G and throttles your CPU so that it is 4 times slower than normal.</span></span>  <span data-ttu-id="33068-213">На **мобильном** телефоне эмулируется медленная работа сети 3G и снижается частота процессора 6, чем обычно.</span><span class="sxs-lookup"><span data-stu-id="33068-213">**Low-end mobile** simulates slow 3G and throttles your CPU 6 times slower than normal.</span></span>  <span data-ttu-id="33068-214">Имейте в виду, что регулирование задается относительно нормальной работы ноутбука или рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="33068-214">Keep in mind that the throttling is relative to the normal capability of your laptop or desktop.</span></span>  

> [!NOTE]
> <span data-ttu-id="33068-215">Список **регулирования** скрывается, если **панель инструментов устройства** является узкой.</span><span class="sxs-lookup"><span data-stu-id="33068-215">The **Throttle** list is hidden if your **Device Toolbar** is narrow.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Панель инструментов "устройства"" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   <span data-ttu-id="33068-217">**Панель инструментов "устройства** "</span><span class="sxs-lookup"><span data-stu-id="33068-217">The **Device Toolbar**</span></span>  
:::image-end:::  

### <span data-ttu-id="33068-218">Регулирование только ЦП</span><span class="sxs-lookup"><span data-stu-id="33068-218">Throttle the CPU only</span></span>   

<span data-ttu-id="33068-219">Чтобы перерегулировать только ЦП, а не сеть, перейдите на панель **производительность** , нажмите **Параметры захвата** \ ( ![ Параметры захвата ][ImageCaptureIcon] ), а затем выберите скорость или **6X** **замедление** в списке **ЦП** .</span><span class="sxs-lookup"><span data-stu-id="33068-219">To throttle the CPU only and not the network, go to the **Performance** panel, click **Capture Settings** \(![Capture Settings][ImageCaptureIcon]\), and then select **4x slowdown** or **6x slowdown** from the **CPU** list.</span></span>  

:::image type="complex" source="../media/device-mode-performance-cpu-throttle.msft.png" alt-text="Список ЦП" lightbox="../media/device-mode-performance-cpu-throttle.msft.png":::
   <span data-ttu-id="33068-221">Список **ЦП**</span><span class="sxs-lookup"><span data-stu-id="33068-221">The **CPU** list</span></span>  
:::image-end:::  

### <span data-ttu-id="33068-222">Регулирование сети только</span><span class="sxs-lookup"><span data-stu-id="33068-222">Throttle the network only</span></span>   

<span data-ttu-id="33068-223">Для регулирования сети, а не центрального процессора, откройте панель Network ( **сеть** ) и выберите в списке **регулирования** команду **Быстрый 3G** или **низкая 3G** .</span><span class="sxs-lookup"><span data-stu-id="33068-223">To throttle the network only and not the CPU, go the **Network** panel and select **Fast 3G** or **Slow 3G** from the **Throttle** list.</span></span>  

:::image type="complex" source="../media/device-mode-network-throttle.msft.png" alt-text="Список регулирования" lightbox="../media/device-mode-network-throttle.msft.png":::
   <span data-ttu-id="33068-225">Список **регулирования**</span><span class="sxs-lookup"><span data-stu-id="33068-225">The **Throttle** list</span></span>  
:::image-end:::  

<span data-ttu-id="33068-226">Или нажмите клавиши `Control` + `Shift` + `P` \ (Windows \) или `Command` + `Shift` + `P` \ (macOS \), чтобы открыть **меню команд**, введите `3G` и выберите **включить быстрое регулирование сети 3G** или **включить медленное регулирование сети 3G**.</span><span class="sxs-lookup"><span data-stu-id="33068-226">Or press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the **Command Menu**, type `3G`, and select **Enable fast 3G throttling** or **Enable slow 3G throttling**.</span></span>  

:::image type="complex" source="../media/device-mode-command-menu-throttle.msft.png" alt-text="Меню команд" lightbox="../media/device-mode-command-menu-throttle.msft.png":::
   <span data-ttu-id="33068-228">**Меню команд**</span><span class="sxs-lookup"><span data-stu-id="33068-228">The **Command Menu**</span></span>  
:::image-end:::  

<span data-ttu-id="33068-229">Вы также можете настроить регулирование сети на панели **Performance** .</span><span class="sxs-lookup"><span data-stu-id="33068-229">You can also set network throttling from the **Performance** panel.</span></span>  <span data-ttu-id="33068-230">Нажмите кнопку **захвата параметров** \ ( ![ Параметры ][ImageCaptureIcon] захвата), а затем выберите в списке список **сетей** вариант **Быстрая 3G** или **низкая 3G** .</span><span class="sxs-lookup"><span data-stu-id="33068-230">Click **Capture Settings** \(![Capture Settings][ImageCaptureIcon]\) and then select **Fast 3G** or **Slow 3G** from the **Network** list.</span></span>  

:::image type="complex" source="../media/device-mode-performance-network-throttle.msft.png" alt-text="Настройка регулирования сети с помощью панели "производительность"" lightbox="../media/device-mode-performance-network-throttle.msft.png":::
   <span data-ttu-id="33068-232">Настройка регулирования сети с помощью панели " **производительность** "</span><span class="sxs-lookup"><span data-stu-id="33068-232">Set network throttling from the **Performance** panel</span></span>  
:::image-end:::  

## <span data-ttu-id="33068-233">Переопределение географического положения</span><span class="sxs-lookup"><span data-stu-id="33068-233">Override geolocation</span></span>   

<span data-ttu-id="33068-234">Чтобы открыть пользовательский интерфейс переопределения географического положения, нажмите кнопку **Настройка DevTools и** `...` выберите пункт **другие инструменты**  >  **датчики**.</span><span class="sxs-lookup"><span data-stu-id="33068-234">To open the geolocation overriding UI click **Customize and control DevTools** \(`...`\) and then select **More tools** > **Sensors**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Датчики" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
   **<span data-ttu-id="33068-236">Датчики</span><span class="sxs-lookup"><span data-stu-id="33068-236">Sensors</span></span>**  
:::image-end:::  

<span data-ttu-id="33068-237">Или нажмите клавиши `Control` + `Shift` + `P` \ (Windows \) или `Command` + `Shift` + `P` \ (macOS \), чтобы открыть меню команд, введите `Sensors` и выберите пункт **Показать датчики**.</span><span class="sxs-lookup"><span data-stu-id="33068-237">Or press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, type `Sensors`, and then select **Show Sensors**.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Показать датчики" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
   **<span data-ttu-id="33068-239">Показать датчики</span><span class="sxs-lookup"><span data-stu-id="33068-239">Show Sensors</span></span>**  
:::image-end:::  

<span data-ttu-id="33068-240">Выберите один из стилей из списка **географического расположения** или выберите **другое расположение** , чтобы ввести собственные координаты, или выберите **расположение недоступно** , чтобы проверить, как будет выглядеть страница, когда географическое положение находится в состоянии ошибки.</span><span class="sxs-lookup"><span data-stu-id="33068-240">Select one of the presets from the **Geolocation** list, or select **Custom location** to enter your own coordinates, or select **Location unavailable** to test out how your page behaves when geolocation is in an error state.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png" alt-text="Геолокация" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png":::
   **<span data-ttu-id="33068-242">Геолокация</span><span class="sxs-lookup"><span data-stu-id="33068-242">Geolocation</span></span>**  
:::image-end:::  

## <span data-ttu-id="33068-243">Настройка ориентации</span><span class="sxs-lookup"><span data-stu-id="33068-243">Set orientation</span></span>   

:::row:::
   :::column span="":::
      <span data-ttu-id="33068-244">Чтобы открыть пользовательский интерфейс ориентации, нажмите кнопку **Настройка DevTools** и `...` выберите пункт **другие**  >  **датчики**инструментов.</span><span class="sxs-lookup"><span data-stu-id="33068-244">To open the orientation UI click **Customize and control DevTools** `...` and then select **More tools** > **Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Датчики" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         **<span data-ttu-id="33068-246">Датчики</span><span class="sxs-lookup"><span data-stu-id="33068-246">Sensors</span></span>**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      <span data-ttu-id="33068-247">Или нажмите клавиши `Control` + `Shift` + `P` \ (Windows \) или `Command` + `Shift` + `P` \ (macOS \), чтобы открыть меню команд, введите `Sensors` и выберите пункт **Показать датчики**.</span><span class="sxs-lookup"><span data-stu-id="33068-247">Or press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, type `Sensors`, and then select **Show Sensors**.</span></span>  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Показать датчики" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         **<span data-ttu-id="33068-249">Показать датчики</span><span class="sxs-lookup"><span data-stu-id="33068-249">Show Sensors</span></span>**  
      :::image-end:::  
   :::column-end:::
:::row-end:::

<span data-ttu-id="33068-250">Выберите один из наборов параметров в списке **ориентация** или выберите Пользовательский вариант **ориентация** , чтобы задать значения альфа, бета и гамма.</span><span class="sxs-lookup"><span data-stu-id="33068-250">Select one of the presets from the **Orientation** list or select **Custom orientation** to set your own alpha, beta, and gamma values.</span></span>  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png" alt-text="Ориентация" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png":::
   **<span data-ttu-id="33068-252">Ориентация</span><span class="sxs-lookup"><span data-stu-id="33068-252">Orientation</span></span>**  
:::image-end:::  

<!--  
 


-->  

<!--See [Join the DevTools community][DevToolsCommunity] for other ways to leave feedback.  -->  

<!-- image links -->  

[ImageCaptureIcon]: ../media/capture-settings-icon.msft.png  
[ImageDeviceToolbarIcon]: ../media/toggle-device-toolbar-dark-icon.msft.png  
[ImageRotateIcon]: ../media/rotate-dark-icon.msft.png  

<!-- links -->  

<!--[DevToolsCommunity]: ../index.md#community "Join the DevTools community | Microsoft Docs"  -->
[DevToolsRemoteDebugging]: .. /Remote-Debugging/index.md "Начало работы с удаленными отладочными устройствами Android | Microsoft Docs»  

[MDNWindowDevicePixelRatio]: https://developer.mozilla.org/docs/Web/API/Window/devicePixelRatio "Window. devicePixelRatio | MDN"  
[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "Агент пользователя | MDN"  

[WikiApproximation]: https://en.wikipedia.org/wiki/Order_of_approximation#First-order "Порядок приближения — первый-заказ — Википедии"  

> [!NOTE]
> <span data-ttu-id="33068-257">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="33068-257">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="33068-258">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="33068-258">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="33068-260">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="33068-260">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
