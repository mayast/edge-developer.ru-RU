---
title: Эмуляция мобильных устройств с помощью режима устройства в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 10c1ee12777965778ebec2d257399dc231e2a01a
ms.sourcegitcommit: 531ec8aa1f89b28bc4d271e8e995f846f2392bc3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/29/2020
ms.locfileid: "10607428"
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





# <span data-ttu-id="2c5d3-103">Эмуляция мобильных устройств с помощью режима устройства в Microsoft Edge DevTools</span><span class="sxs-lookup"><span data-stu-id="2c5d3-103">Simulate Mobile Devices with Device Mode in Microsoft Edge DevTools</span></span>   

  

<span data-ttu-id="2c5d3-104">С помощью режима устройства вы можете оценить внешний вид страницы и ее выполнение на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="2c5d3-104">Use Device Mode to approximate how your page looks and performs on a mobile device.</span></span>  

<span data-ttu-id="2c5d3-105">Режим устройства — это имя для свободной коллекции функций в Microsoft Edge DevTools, которые помогают имитировать мобильные устройства.</span><span class="sxs-lookup"><span data-stu-id="2c5d3-105">Device Mode is the name for the loose collection of features in Microsoft Edge DevTools that help you simulate mobile devices.</span></span>  <span data-ttu-id="2c5d3-106">К таким функциям относятся:</span><span class="sxs-lookup"><span data-stu-id="2c5d3-106">These features include:</span></span>  

*   [<span data-ttu-id="2c5d3-107">Имитация окна просмотра для мобильных устройств</span><span class="sxs-lookup"><span data-stu-id="2c5d3-107">Simulating a mobile viewport</span></span>](#simulate-a-mobile-viewport)  
*   [<span data-ttu-id="2c5d3-108">Регулирование сети</span><span class="sxs-lookup"><span data-stu-id="2c5d3-108">Throttling the network</span></span>](#throttle-the-network-only)  
*   [<span data-ttu-id="2c5d3-109">Регулирование ЦП</span><span class="sxs-lookup"><span data-stu-id="2c5d3-109">Throttling the CPU</span></span>](#throttle-the-cpu-only)  
*   [<span data-ttu-id="2c5d3-110">Имитация географического местоположения</span><span class="sxs-lookup"><span data-stu-id="2c5d3-110">Simulating geolocation</span></span>](#override-geolocation)  
*   [<span data-ttu-id="2c5d3-111">Настройка ориентации</span><span class="sxs-lookup"><span data-stu-id="2c5d3-111">Setting orientation</span></span>](#set-orientation)  

## <span data-ttu-id="2c5d3-112">Ограничения</span><span class="sxs-lookup"><span data-stu-id="2c5d3-112">Limitations</span></span>   

<span data-ttu-id="2c5d3-113">Режим устройства облагается [приблизительно][WikiApproximation] так, как выглядит страница на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="2c5d3-113">Think of Device Mode as a [first-order approximation][WikiApproximation] of how your page looks and feels on a mobile device.</span></span>  <span data-ttu-id="2c5d3-114">В режиме устройства вы фактически не запускаете ваш код на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="2c5d3-114">With Device Mode you do not actually run your code on a mobile device.</span></span>  <span data-ttu-id="2c5d3-115">Вы имитируете взаимодействие с пользователем на мобильном устройстве или компьютере.</span><span class="sxs-lookup"><span data-stu-id="2c5d3-115">You simulate the mobile user experience from your laptop or desktop.</span></span>  

<span data-ttu-id="2c5d3-116">Некоторые аспекты мобильных устройств, которые DevTools никогда не смогут имитировать.</span><span class="sxs-lookup"><span data-stu-id="2c5d3-116">There are some aspects of mobile devices that DevTools will never be able to simulate.</span></span>  <span data-ttu-id="2c5d3-117">Например, архитектура мобильных процессоров очень отличается от архитектуры ноутбука или процессоров для настольных ПК.</span><span class="sxs-lookup"><span data-stu-id="2c5d3-117">For example, the architecture of mobile CPUs is very different than the architecture of laptop or desktop CPUs.</span></span>  <span data-ttu-id="2c5d3-118">Если вы сомневаетесь, лучше использовать страницу на мобильном устройстве.</span><span class="sxs-lookup"><span data-stu-id="2c5d3-118">When in doubt, your best bet is to actually run your page on a mobile device.</span></span>  <span data-ttu-id="2c5d3-119">Использование [удаленной отладки] [DevToolsRemoteDebugging] для просмотра, изменения, отладки и профилирования кода страницы на мобильном устройстве или рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="2c5d3-119">Use [Remote Debugging][DevToolsRemoteDebugging] to view, change, debug, and profile the code of a page from your laptop or desktop while it actually runs on a mobile device.</span></span>  

## <span data-ttu-id="2c5d3-120">Имитация окна просмотра для мобильных устройств</span><span class="sxs-lookup"><span data-stu-id="2c5d3-120">Simulate a mobile viewport</span></span>   

<span data-ttu-id="2c5d3-121">Нажмите **кнопку** Переключить панель инструментов устройства ![ ][ImageDeviceToolbarIcon] , чтобы открыть пользовательский интерфейс, позволяющий имитировать окно просмотра для мобильных устройств.</span><span class="sxs-lookup"><span data-stu-id="2c5d3-121">Click **Toggle Device Toolbar** ![Toggle Device Toolbar][ImageDeviceToolbarIcon] to open the UI that enables you to simulate a mobile viewport.</span></span>  

> ##### <span data-ttu-id="2c5d3-122">Рис. 1</span><span class="sxs-lookup"><span data-stu-id="2c5d3-122">Figure 1</span></span>  
> <span data-ttu-id="2c5d3-123">Панель инструментов "устройства"</span><span class="sxs-lookup"><span data-stu-id="2c5d3-123">The Device Toolbar</span></span>  
> ![Панель инструментов "устройства"][ImageDeviceToolbar]  

<span data-ttu-id="2c5d3-125">По умолчанию панель инструментов устройства открывается в режиме отклика окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="2c5d3-125">By default the Device Toolbar opens in Responsive Viewport Mode.</span></span>  

### <span data-ttu-id="2c5d3-126">Режим окна просмотра с откликом</span><span class="sxs-lookup"><span data-stu-id="2c5d3-126">Responsive Viewport Mode</span></span>   

<span data-ttu-id="2c5d3-127">Перетащите маркеры, чтобы изменить размер окна просмотра в соответствии с нужными размерами.</span><span class="sxs-lookup"><span data-stu-id="2c5d3-127">Drag the handles to resize the viewport to whatever dimensions you need.</span></span>  <span data-ttu-id="2c5d3-128">Кроме того, можно ввести значения в полях Ширина и высота.</span><span class="sxs-lookup"><span data-stu-id="2c5d3-128">Or, enter specific values in the width and height boxes.</span></span>  <span data-ttu-id="2c5d3-129">На [рисунке 2](#figure-2)задана ширина `626` и высота задана `516` .</span><span class="sxs-lookup"><span data-stu-id="2c5d3-129">In [Figure 2](#figure-2), the width is set to `626` and the height is set to `516`.</span></span>  

> ##### <span data-ttu-id="2c5d3-130">Рисунок 2</span><span class="sxs-lookup"><span data-stu-id="2c5d3-130">Figure 2</span></span>  
> <span data-ttu-id="2c5d3-131">Дескрипторы для изменения размеров окна просмотра в отклике режима просмотра</span><span class="sxs-lookup"><span data-stu-id="2c5d3-131">The handles for changing the dimensions of the viewport when in Responsive Viewport Mode</span></span>  
> ![Дескрипторы для изменения размеров окна просмотра в отклике режима просмотра][ImageResponsiveHandles]  

#### <span data-ttu-id="2c5d3-133">Показать мультимедийные запросы</span><span class="sxs-lookup"><span data-stu-id="2c5d3-133">Show media queries</span></span>   

<span data-ttu-id="2c5d3-134">Чтобы отобразить точки останова для запросов мультимедиа над окном просмотра, нажмите кнопку **Дополнительные параметры** и выберите пункт **Показать мультимедийные запросы**.</span><span class="sxs-lookup"><span data-stu-id="2c5d3-134">To show media query breakpoints above your viewport, click **More options** and then select **Show media queries**.</span></span>  

> ##### <span data-ttu-id="2c5d3-135">Рисунок3</span><span class="sxs-lookup"><span data-stu-id="2c5d3-135">Figure 3</span></span>  
> <span data-ttu-id="2c5d3-136">Показать мультимедийные запросы</span><span class="sxs-lookup"><span data-stu-id="2c5d3-136">Show media queries</span></span>  
> ![Показать мультимедийные запросы][ImageShowMediaQueries]  

<span data-ttu-id="2c5d3-138">Щелкните точку останова, чтобы изменить ширину окна просмотра таким образом, чтобы точка останова была инициирована.</span><span class="sxs-lookup"><span data-stu-id="2c5d3-138">Click a breakpoint to change the width of the viewport so that the breakpoint gets triggered.</span></span>  

> ##### <span data-ttu-id="2c5d3-139">Рисунок4</span><span class="sxs-lookup"><span data-stu-id="2c5d3-139">Figure 4</span></span>  
> <span data-ttu-id="2c5d3-140">Щелкните точку останова, чтобы изменить ширину окна просмотра</span><span class="sxs-lookup"><span data-stu-id="2c5d3-140">Click a breakpoint to change the width of the viewport</span></span>  
> ![Щелкните точку останова, чтобы изменить ширину окна просмотра][ImageBreakpoint]  

#### <span data-ttu-id="2c5d3-142">Настройка типа устройства</span><span class="sxs-lookup"><span data-stu-id="2c5d3-142">Set the device type</span></span>   

<span data-ttu-id="2c5d3-143">Используйте список **типов устройств** для имитации мобильного устройства или настольного устройства.</span><span class="sxs-lookup"><span data-stu-id="2c5d3-143">Use the **Device Type** list to simulate a mobile device or desktop device.</span></span>  

> ##### <span data-ttu-id="2c5d3-144">Рисунок 5</span><span class="sxs-lookup"><span data-stu-id="2c5d3-144">Figure 5</span></span>  
> <span data-ttu-id="2c5d3-145">Список **типов устройств**</span><span class="sxs-lookup"><span data-stu-id="2c5d3-145">The **Device Type** list</span></span>  
> ![Список типов устройств][ImageDeviceType]  

<span data-ttu-id="2c5d3-147">В приведенной ниже таблице описаны различия между параметрами.</span><span class="sxs-lookup"><span data-stu-id="2c5d3-147">The table below describes the differences between the options.</span></span>  <span data-ttu-id="2c5d3-148">**Метод рендеринга** указывает, будет ли Microsoft Edge обрабатывать страницу в виде окна просмотра на мобильном или рабочем столе.</span><span class="sxs-lookup"><span data-stu-id="2c5d3-148">**Rendering method** refers to whether Microsoft Edge renders the page as a mobile or desktop viewport.</span></span>  <span data-ttu-id="2c5d3-149">**Значок курсора** указывает на тип курсора, который отображается при наведении указателя мыши на страницу.</span><span class="sxs-lookup"><span data-stu-id="2c5d3-149">**Cursor icon** refers to what type of cursor you see when you hover over the page.</span></span>  <span data-ttu-id="2c5d3-150">**События, созданные** в зависимости от того, срабатывает ли страница `touch` или `click` события при взаимодействии со страницей.</span><span class="sxs-lookup"><span data-stu-id="2c5d3-150">**Events fired** refers to whether the page fires `touch` or `click` events when you interact with the page.</span></span>  

| <span data-ttu-id="2c5d3-151">Параметр</span><span class="sxs-lookup"><span data-stu-id="2c5d3-151">Option</span></span> | <span data-ttu-id="2c5d3-152">Метод отрисовки</span><span class="sxs-lookup"><span data-stu-id="2c5d3-152">Rendering method</span></span> | <span data-ttu-id="2c5d3-153">Значок курсора</span><span class="sxs-lookup"><span data-stu-id="2c5d3-153">Cursor icon</span></span> | <span data-ttu-id="2c5d3-154">События, созданные</span><span class="sxs-lookup"><span data-stu-id="2c5d3-154">Events fired</span></span> |  
|:--- |:--- |:--- |:--- |  
| <span data-ttu-id="2c5d3-155">Мобильные устройства</span><span class="sxs-lookup"><span data-stu-id="2c5d3-155">Mobile</span></span> | <span data-ttu-id="2c5d3-156">Мобильные устройства</span><span class="sxs-lookup"><span data-stu-id="2c5d3-156">Mobile</span></span> | <span data-ttu-id="2c5d3-157">Круг</span><span class="sxs-lookup"><span data-stu-id="2c5d3-157">Circle</span></span> | <span data-ttu-id="2c5d3-158">Сенсорный ввод</span><span class="sxs-lookup"><span data-stu-id="2c5d3-158">touch</span></span> |  
| <span data-ttu-id="2c5d3-159">Мобильный – (без сенсорных устройств)</span><span class="sxs-lookup"><span data-stu-id="2c5d3-159">Mobile \(no touch\)</span></span> | <span data-ttu-id="2c5d3-160">Мобильные устройства</span><span class="sxs-lookup"><span data-stu-id="2c5d3-160">Mobile</span></span> | <span data-ttu-id="2c5d3-161">Обычный</span><span class="sxs-lookup"><span data-stu-id="2c5d3-161">Normal</span></span> | <span data-ttu-id="2c5d3-162"> нажмите </span><span class="sxs-lookup"><span data-stu-id="2c5d3-162">click</span></span> |  
| <span data-ttu-id="2c5d3-163">Desktop</span><span class="sxs-lookup"><span data-stu-id="2c5d3-163">Desktop</span></span> | <span data-ttu-id="2c5d3-164">Desktop</span><span class="sxs-lookup"><span data-stu-id="2c5d3-164">Desktop</span></span> | <span data-ttu-id="2c5d3-165">Обычный</span><span class="sxs-lookup"><span data-stu-id="2c5d3-165">Normal</span></span> | <span data-ttu-id="2c5d3-166"> нажмите </span><span class="sxs-lookup"><span data-stu-id="2c5d3-166">click</span></span> |  
| <span data-ttu-id="2c5d3-167">Классическое приложение (касание)</span><span class="sxs-lookup"><span data-stu-id="2c5d3-167">Desktop \(touch\)</span></span> | <span data-ttu-id="2c5d3-168">Desktop</span><span class="sxs-lookup"><span data-stu-id="2c5d3-168">Desktop</span></span> | <span data-ttu-id="2c5d3-169">Круг</span><span class="sxs-lookup"><span data-stu-id="2c5d3-169">Circle</span></span> | <span data-ttu-id="2c5d3-170">Сенсорный ввод</span><span class="sxs-lookup"><span data-stu-id="2c5d3-170">touch</span></span> |  

> [!NOTE]
> <span data-ttu-id="2c5d3-171">Если список **тип устройства** не отображается, нажмите кнопку **Дополнительные параметры** и выберите команду **Добавить тип устройства**.</span><span class="sxs-lookup"><span data-stu-id="2c5d3-171">If you do not see the **Device Type** list, click **More options** and select **Add device type**.</span></span>  

### <span data-ttu-id="2c5d3-172">Режим просмотра на мобильном устройстве</span><span class="sxs-lookup"><span data-stu-id="2c5d3-172">Mobile Device Viewport Mode</span></span>   

<span data-ttu-id="2c5d3-173">Чтобы смоделировать размеры определенного мобильного устройства, выберите нужное устройство из списка **устройств** .</span><span class="sxs-lookup"><span data-stu-id="2c5d3-173">To simulate the dimensions of a specific mobile device, select the device from the **Device** list.</span></span>  

> ##### <span data-ttu-id="2c5d3-174">Рисунок6</span><span class="sxs-lookup"><span data-stu-id="2c5d3-174">Figure 6</span></span>  
> <span data-ttu-id="2c5d3-175">Список устройств</span><span class="sxs-lookup"><span data-stu-id="2c5d3-175">The Device list</span></span>  
> ![Список устройств][ImageDeviceList]  

#### <span data-ttu-id="2c5d3-177">Поворот окна просмотра на альбомную ориентацию</span><span class="sxs-lookup"><span data-stu-id="2c5d3-177">Rotate the viewport to landscape orientation</span></span>   

<span data-ttu-id="2c5d3-178">Нажмите кнопку **повернуть** ![ поворачивать, ][ImageRotateIcon] чтобы повернуть окно просмотра на альбомную ориентацию.</span><span class="sxs-lookup"><span data-stu-id="2c5d3-178">Click **Rotate** ![Rotate][ImageRotateIcon] to rotate the viewport to landscape orientation.</span></span>  

> ##### <span data-ttu-id="2c5d3-179">Рисунок7</span><span class="sxs-lookup"><span data-stu-id="2c5d3-179">Figure 7</span></span>  
> <span data-ttu-id="2c5d3-180">Альбомная ориентация</span><span class="sxs-lookup"><span data-stu-id="2c5d3-180">Landscape orientation</span></span>  
> ![Альбомная ориентация][ImageLandscape]  

> [!NOTE]
> <span data-ttu-id="2c5d3-182">Кнопка **повернуть** исчезнет, если **панель инструментов на устройстве** является узкой.</span><span class="sxs-lookup"><span data-stu-id="2c5d3-182">The **Rotate** button disappears if your **Device Toolbar** is narrow.</span></span>  

> ##### <span data-ttu-id="2c5d3-183">Рисунок8</span><span class="sxs-lookup"><span data-stu-id="2c5d3-183">Figure 8</span></span>  
> <span data-ttu-id="2c5d3-184">Панель инструментов "устройства"</span><span class="sxs-lookup"><span data-stu-id="2c5d3-184">The Device Toolbar</span></span>  
> ![Панель инструментов "устройства"][ImageDeviceToolbar2]  

<span data-ttu-id="2c5d3-186">Смотрите также [Настройка ориентации](#set-orientation).</span><span class="sxs-lookup"><span data-stu-id="2c5d3-186">See also [Set orientation](#set-orientation).</span></span>  

#### <span data-ttu-id="2c5d3-187">Показать рамку устройства</span><span class="sxs-lookup"><span data-stu-id="2c5d3-187">Show device frame</span></span>   

<span data-ttu-id="2c5d3-188">При моделировании размеров определенного мобильного устройства, например iPhone 6, откройте **меню Дополнительные параметры** и выберите пункт **Показать рамку устройства** , чтобы отобразить рамку физического устройства вокруг окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="2c5d3-188">When simulating the dimensions of a specific mobile device like an iPhone 6, open **More options** and then select **Show device frame** to show the physical device frame around the viewport.</span></span>  

> [!NOTE]
> <span data-ttu-id="2c5d3-189">Если вы не видите рамку устройства для определенного устройства, скорее всего, это означает, что DevTools просто не имеет иллюстраций для определенного параметра.</span><span class="sxs-lookup"><span data-stu-id="2c5d3-189">If you do not see a device frame for a particular device, it probably means that DevTools just does not have art for that specific option.</span></span>  

> ##### <span data-ttu-id="2c5d3-190">Рисунок9</span><span class="sxs-lookup"><span data-stu-id="2c5d3-190">Figure 9</span></span>  
> <span data-ttu-id="2c5d3-191">Показать рамку устройства</span><span class="sxs-lookup"><span data-stu-id="2c5d3-191">Show device frame</span></span>  
> ![Показать рамку устройства][ImageShowDeviceFrame]  

> ##### <span data-ttu-id="2c5d3-193">Рисунок 10</span><span class="sxs-lookup"><span data-stu-id="2c5d3-193">Figure 10</span></span>  
> <span data-ttu-id="2c5d3-194">Рамка устройства для iPhone 6</span><span class="sxs-lookup"><span data-stu-id="2c5d3-194">The device frame for the iPhone 6</span></span>  
> ![Рамка устройства для iPhone 6][ImageIphoneFrame]  

#### <span data-ttu-id="2c5d3-196">Добавление настраиваемого мобильного устройства</span><span class="sxs-lookup"><span data-stu-id="2c5d3-196">Add a custom mobile device</span></span>   

<span data-ttu-id="2c5d3-197">Чтобы добавить настраиваемое устройство, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="2c5d3-197">To add a custom device:</span></span>  

1.  <span data-ttu-id="2c5d3-198">Щелкните список **устройств** и выберите команду **изменить**.</span><span class="sxs-lookup"><span data-stu-id="2c5d3-198">Click the **Device** list and then select **Edit**.</span></span>  

> ##### <span data-ttu-id="2c5d3-199">Рисунок11</span><span class="sxs-lookup"><span data-stu-id="2c5d3-199">Figure 11</span></span>  
> <span data-ttu-id="2c5d3-200">Выбор **Edit** 
> ![ команды "Изменить"][ImageEdit]</span><span class="sxs-lookup"><span data-stu-id="2c5d3-200">Selecting **Edit**
![Selecting Edit][ImageEdit]</span></span>  

1.  <span data-ttu-id="2c5d3-201">Нажмите кнопку **Добавить настраиваемое устройство**.</span><span class="sxs-lookup"><span data-stu-id="2c5d3-201">Click **Add custom device**.</span></span>  

1.  <span data-ttu-id="2c5d3-202">Введите имя, ширину и высоту устройства.</span><span class="sxs-lookup"><span data-stu-id="2c5d3-202">Enter a name, width, and height for the device.</span></span>  <span data-ttu-id="2c5d3-203">Поля « [отношение к пикселям][MDNWindowDevicePixelRatio]», « [строка агента пользователя][MDNUserAgent]» и « [тип устройства](#set-the-device-type) » являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="2c5d3-203">The [device pixel ratio][MDNWindowDevicePixelRatio], [user agent string][MDNUserAgent], and [device type](#set-the-device-type) fields are optional.</span></span>  <span data-ttu-id="2c5d3-204">Поле «Тип устройства» — это список, который по умолчанию имеет значение " **мобильный** ".</span><span class="sxs-lookup"><span data-stu-id="2c5d3-204">The device type field is the list that is set to **Mobile** by default.</span></span>  

> ##### <span data-ttu-id="2c5d3-205">Рисунок12</span><span class="sxs-lookup"><span data-stu-id="2c5d3-205">Figure 12</span></span>  
> <span data-ttu-id="2c5d3-206">Создание настраиваемого устройства</span><span class="sxs-lookup"><span data-stu-id="2c5d3-206">Creating a custom device</span></span>  
> ![Создание настраиваемого устройства][ImageAddCustomDevice]  

### <span data-ttu-id="2c5d3-208">Отображение линеек</span><span class="sxs-lookup"><span data-stu-id="2c5d3-208">Show rulers</span></span>   

<span data-ttu-id="2c5d3-209">Нажмите кнопку **Дополнительные параметры** , а затем выберите пункт **Показывать линейки** , чтобы увидеть линейки сверху и слева от окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="2c5d3-209">Click **More options** and then select **Show rulers** to see rulers above and to the left of your viewport.</span></span>  <span data-ttu-id="2c5d3-210">Единица измерения линеек — Пиксели.</span><span class="sxs-lookup"><span data-stu-id="2c5d3-210">The sizing unit of the rulers is pixels.</span></span>  

> ##### <span data-ttu-id="2c5d3-211">Рисунок13</span><span class="sxs-lookup"><span data-stu-id="2c5d3-211">Figure 13</span></span>  
> <span data-ttu-id="2c5d3-212">Отображение линеек</span><span class="sxs-lookup"><span data-stu-id="2c5d3-212">Show rulers</span></span>  
> ![Отображение линеек][ImageShowRulers]  

> ##### <span data-ttu-id="2c5d3-214">Рисунок14</span><span class="sxs-lookup"><span data-stu-id="2c5d3-214">Figure 14</span></span>  
> <span data-ttu-id="2c5d3-215">Линейки сверху и слева от окна просмотра</span><span class="sxs-lookup"><span data-stu-id="2c5d3-215">Rulers above and to the left of the viewport</span></span>  
> ![Линейки сверху и слева от окна просмотра][ImageRulers]  

### <span data-ttu-id="2c5d3-217">Изменение масштаба просмотра</span><span class="sxs-lookup"><span data-stu-id="2c5d3-217">Zoom the viewport</span></span>   

<span data-ttu-id="2c5d3-218">С помощью списка **масштаб** вы можете увеличить или уменьшить масштаб.</span><span class="sxs-lookup"><span data-stu-id="2c5d3-218">Use the **Zoom** list to zoom in or out.</span></span>  

> ##### <span data-ttu-id="2c5d3-219">Рисунок15</span><span class="sxs-lookup"><span data-stu-id="2c5d3-219">Figure 15</span></span>  
> <span data-ttu-id="2c5d3-220">Масштаб</span><span class="sxs-lookup"><span data-stu-id="2c5d3-220">Zoom</span></span>  
> ![Масштаб][ImageZoomViewport]  

## <span data-ttu-id="2c5d3-222">Регулирование сети и ЦП</span><span class="sxs-lookup"><span data-stu-id="2c5d3-222">Throttle the network and CPU</span></span>   

<span data-ttu-id="2c5d3-223">Для регулирования сети и ЦП выберите на **мобильном** или **низком мобильном** уровне в списке **регулирования** .</span><span class="sxs-lookup"><span data-stu-id="2c5d3-223">To throttle the network and CPU, select **Mid-tier mobile** or **Low-end mobile** from the **Throttle** list.</span></span>  

> ##### <span data-ttu-id="2c5d3-224">Рисунок16</span><span class="sxs-lookup"><span data-stu-id="2c5d3-224">Figure 16</span></span>  
> <span data-ttu-id="2c5d3-225">Список регулирования</span><span class="sxs-lookup"><span data-stu-id="2c5d3-225">The Throttle list</span></span>  
> ![Список регулирования][ImageThrottling]  

<span data-ttu-id="2c5d3-227">На **мобильном устройстве с уровнем "среднее** " эмулируется быстрое соединение и снижается частота центрального процессора, так как это происходит в течение 4 часов, чем обычно.</span><span class="sxs-lookup"><span data-stu-id="2c5d3-227">**Mid-tier mobile** simulates fast 3G and throttles your CPU so that it is 4 times slower than normal.</span></span>  <span data-ttu-id="2c5d3-228">На **мобильном** телефоне эмулируется медленная работа сети 3G и снижается частота процессора 6, чем обычно.</span><span class="sxs-lookup"><span data-stu-id="2c5d3-228">**Low-end mobile** simulates slow 3G and throttles your CPU 6 times slower than normal.</span></span>  <span data-ttu-id="2c5d3-229">Имейте в виду, что регулирование задается относительно нормальной работы ноутбука или рабочего стола.</span><span class="sxs-lookup"><span data-stu-id="2c5d3-229">Keep in mind that the throttling is relative to the normal capability of your laptop or desktop.</span></span>  

> [!NOTE]
> <span data-ttu-id="2c5d3-230">Список **регулирования** будет скрыт, если **панель инструментов устройства** является узкой.</span><span class="sxs-lookup"><span data-stu-id="2c5d3-230">The **Throttle** list will be hidden if your **Device Toolbar** is narrow.</span></span>  

> ##### <span data-ttu-id="2c5d3-231">Рисунок17</span><span class="sxs-lookup"><span data-stu-id="2c5d3-231">Figure 17</span></span>  
> <span data-ttu-id="2c5d3-232">Панель инструментов "устройства"</span><span class="sxs-lookup"><span data-stu-id="2c5d3-232">The Device Toolbar</span></span>  
> ![Панель инструментов "устройства"][ImageDeviceToolbar3]  

### <span data-ttu-id="2c5d3-234">Регулирование только ЦП</span><span class="sxs-lookup"><span data-stu-id="2c5d3-234">Throttle the CPU only</span></span>   

<span data-ttu-id="2c5d3-235">Чтобы перерегулировать только ЦП, а не сеть, перейдите на панель **производительность** , щелкните Параметры захвата **параметров** ![ ][ImageCaptureIcon] , а затем выберите скорость или **6X** **замедление** в списке **ЦП** .</span><span class="sxs-lookup"><span data-stu-id="2c5d3-235">To throttle the CPU only and not the network, go to the **Performance** panel, click **Capture Settings** ![Capture Settings][ImageCaptureIcon], and then select **4x slowdown** or **6x slowdown** from the **CPU** list.</span></span>  

> ##### <span data-ttu-id="2c5d3-236">Рис. 18</span><span class="sxs-lookup"><span data-stu-id="2c5d3-236">Figure 18</span></span>  
> <span data-ttu-id="2c5d3-237">Список ЦП</span><span class="sxs-lookup"><span data-stu-id="2c5d3-237">The CPU list</span></span>  
> ![Список ЦП][ImageCPU]  

### <span data-ttu-id="2c5d3-239">Регулирование сети только</span><span class="sxs-lookup"><span data-stu-id="2c5d3-239">Throttle the network only</span></span>   

<span data-ttu-id="2c5d3-240">Для регулирования сети, а не центрального процессора, откройте панель Network ( **сеть** ) и выберите в списке **регулирования** команду **Быстрый 3G** или **низкая 3G** .</span><span class="sxs-lookup"><span data-stu-id="2c5d3-240">To throttle the network only and not the CPU, go the **Network** panel and select **Fast 3G** or **Slow 3G** from the **Throttle** list.</span></span>  

> ##### <span data-ttu-id="2c5d3-241">На рисунке 19</span><span class="sxs-lookup"><span data-stu-id="2c5d3-241">Figure 19</span></span>  
> <span data-ttu-id="2c5d3-242">Список регулирования</span><span class="sxs-lookup"><span data-stu-id="2c5d3-242">The Throttle list</span></span>  
> ![Список регулирования][ImageNetwork]  

<span data-ttu-id="2c5d3-244">Или нажмите клавиши `Control` + `Shift` + `P` \ (Windows \) или `Command` + `Shift` + `P` \ (macOS \), чтобы открыть меню команд, введите `3G` и выберите **включить быстрое регулирование сети 3G** или **включить медленное регулирование сети 3G**.</span><span class="sxs-lookup"><span data-stu-id="2c5d3-244">Or press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, type `3G`, and select **Enable fast 3G throttling** or **Enable slow 3G throttling**.</span></span>  

> ##### <span data-ttu-id="2c5d3-245">Рис. 20</span><span class="sxs-lookup"><span data-stu-id="2c5d3-245">Figure 20</span></span>  
> <span data-ttu-id="2c5d3-246">Меню команд</span><span class="sxs-lookup"><span data-stu-id="2c5d3-246">The Command Menu</span></span>  
> ![Меню команд][ImageCommandMenu]  

<span data-ttu-id="2c5d3-248">Вы также можете настроить регулирование сети на панели **Performance** .</span><span class="sxs-lookup"><span data-stu-id="2c5d3-248">You can also set network throttling from the **Performance** panel.</span></span>  <span data-ttu-id="2c5d3-249">Нажмите **кнопку захват** параметров ![ ][ImageCaptureIcon] , а затем в списке список **сетей** выберите пункт **Быстрая 3G** или **низкая 3G** .</span><span class="sxs-lookup"><span data-stu-id="2c5d3-249">Click **Capture Settings** ![Capture Settings][ImageCaptureIcon] and then select **Fast 3G** or **Slow 3G** from the **Network** list.</span></span>  

> ##### <span data-ttu-id="2c5d3-250">Рисунок 21</span><span class="sxs-lookup"><span data-stu-id="2c5d3-250">Figure 21</span></span>  
> <span data-ttu-id="2c5d3-251">Настройка регулирования сети с помощью панели "производительность"</span><span class="sxs-lookup"><span data-stu-id="2c5d3-251">Setting network throttling from the Performance panel</span></span>  
> ![Настройка регулирования сети с помощью панели "производительность"][ImageNetwork2]  

## <span data-ttu-id="2c5d3-253">Переопределение географического положения</span><span class="sxs-lookup"><span data-stu-id="2c5d3-253">Override geolocation</span></span>   

<span data-ttu-id="2c5d3-254">Чтобы открыть пользовательский интерфейс переопределения географического расположения, нажмите кнопку **Настройка DevTools** и `...` выберите пункт **другие**  >  **датчики**инструментов.</span><span class="sxs-lookup"><span data-stu-id="2c5d3-254">To open the geolocation overriding UI click **Customize and control DevTools** `...` and then select **More tools** > **Sensors**.</span></span>  

> ##### <span data-ttu-id="2c5d3-255">Рис. 22</span><span class="sxs-lookup"><span data-stu-id="2c5d3-255">Figure 22</span></span>  
> <span data-ttu-id="2c5d3-256">Датчики</span><span class="sxs-lookup"><span data-stu-id="2c5d3-256">Sensors</span></span>  
> ![Датчики][ImageSensors]  

<span data-ttu-id="2c5d3-258">Или нажмите клавиши `Control` + `Shift` + `P` \ (Windows \) или `Command` + `Shift` + `P` \ (macOS \), чтобы открыть меню команд, введите `Sensors` и выберите пункт **Показать датчики**.</span><span class="sxs-lookup"><span data-stu-id="2c5d3-258">Or press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, type `Sensors`, and then select **Show Sensors**.</span></span>  

> ##### <span data-ttu-id="2c5d3-259">Рис. 23</span><span class="sxs-lookup"><span data-stu-id="2c5d3-259">Figure 23</span></span>  
> <span data-ttu-id="2c5d3-260">Показать датчики</span><span class="sxs-lookup"><span data-stu-id="2c5d3-260">Show Sensors</span></span>  
> ![Показать датчики][ImageShowSensors]  

<span data-ttu-id="2c5d3-262">Выберите один из стилей из списка **географического расположения** или выберите **другое расположение** , чтобы ввести собственные координаты, или выберите **расположение недоступно** , чтобы проверить, как будет выглядеть страница, когда географическое положение находится в состоянии ошибки.</span><span class="sxs-lookup"><span data-stu-id="2c5d3-262">Select one of the presets from the **Geolocation** list, or select **Custom location** to enter your own coordinates, or select **Location unavailable** to test out how your page behaves when geolocation is in an error state.</span></span>  

> ##### <span data-ttu-id="2c5d3-263">Рисунок 24</span><span class="sxs-lookup"><span data-stu-id="2c5d3-263">Figure 24</span></span>  
> <span data-ttu-id="2c5d3-264">Геолокация</span><span class="sxs-lookup"><span data-stu-id="2c5d3-264">Geolocation</span></span>  
> ![Геолокация][ImageGeolocation]  

## <span data-ttu-id="2c5d3-266">Настройка ориентации</span><span class="sxs-lookup"><span data-stu-id="2c5d3-266">Set orientation</span></span>   

<span data-ttu-id="2c5d3-267">Чтобы открыть пользовательский интерфейс ориентации, нажмите кнопку **Настройка DevTools** и `...` выберите пункт **другие**  >  **датчики**инструментов.</span><span class="sxs-lookup"><span data-stu-id="2c5d3-267">To open the orientation UI click **Customize and control DevTools** `...` and then select **More tools** > **Sensors**.</span></span>  

> ##### <span data-ttu-id="2c5d3-268">Рис. 25</span><span class="sxs-lookup"><span data-stu-id="2c5d3-268">Figure 25</span></span>  
> <span data-ttu-id="2c5d3-269">Датчики</span><span class="sxs-lookup"><span data-stu-id="2c5d3-269">Sensors</span></span>  
> ![Датчики][ImageSensors2]  

<span data-ttu-id="2c5d3-271">Или нажмите клавиши `Control` + `Shift` + `P` \ (Windows \) или `Command` + `Shift` + `P` \ (macOS \), чтобы открыть меню команд, введите `Sensors` и выберите пункт **Показать датчики**.</span><span class="sxs-lookup"><span data-stu-id="2c5d3-271">Or press `Control`+`Shift`+`P` \(Windows\) or `Command`+`Shift`+`P` \(macOS\) to open the Command Menu, type `Sensors`, and then select **Show Sensors**.</span></span>  

> ##### <span data-ttu-id="2c5d3-272">Рис. 26</span><span class="sxs-lookup"><span data-stu-id="2c5d3-272">Figure 26</span></span>  
> <span data-ttu-id="2c5d3-273">Показать датчики</span><span class="sxs-lookup"><span data-stu-id="2c5d3-273">Show Sensors</span></span>  
> ![Показать датчики][ImageShowSensors2]  

<span data-ttu-id="2c5d3-275">Выберите один из наборов параметров в списке **ориентация** или выберите Пользовательский вариант **ориентация** , чтобы задать значения альфа, бета и гамма.</span><span class="sxs-lookup"><span data-stu-id="2c5d3-275">Select one of the presets from the **Orientation** list or select **Custom orientation** to set your own alpha, beta, and gamma values.</span></span>  

> ##### <span data-ttu-id="2c5d3-276">На рисунке 27</span><span class="sxs-lookup"><span data-stu-id="2c5d3-276">Figure 27</span></span>  
> <span data-ttu-id="2c5d3-277">Ориентация</span><span class="sxs-lookup"><span data-stu-id="2c5d3-277">Orientation</span></span>  
> ![Ориентация][ImageOrientation]  

 



<!--See [Join the DevTools community][DevToolsCommunity] for other ways to leave feedback.  -->  

<!-- image links -->  

[ImageCaptureIcon]: /microsoft-edge/devtools-guide-chromium/media/capture-settings-icon.msft.png  
[ImageCustomizeIcon]: /microsoft-edge/devtools-guide-chromium/media/customize-and-control-devtools-icon.msft.png  
[ImageDeviceToolbarIcon]: /microsoft-edge/devtools-guide-chromium/media/toggle-device-toolbar-dark-icon.msft.png  
[ImageRotateIcon]: /microsoft-edge/devtools-guide-chromium/media/rotate-dark-icon.msft.png  

[ImageDeviceToolbar]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-highlighted.msft.png "Рисунок 1: панель инструментов "устройства""  
[ImageResponsiveHandles]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png "Рисунок 2: маркеры изменения размеров окна просмотра в отклике режима просмотра"  
[ImageShowMediaQueries]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png "Рисунок 3: отображение запросов мультимедиа"  
[ImageBreakpoint]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png "Рисунок 4: щелкните точку останова, чтобы изменить ширину окна просмотра."  
[ImageDeviceType]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-device-type-list.msft.png "Рисунок 5: список типов устройств"  
[ImageDeviceList]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-device-list.msft.png "Рисунок 6: список устройств"  
[ImageLandscape]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-landscape.msft.png "Рисунок 7: альбомная ориентация"  
[ImageDeviceToolbar2]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-highlighted.msft.png "Рисунок 8: панель инструментов устройства"  
[ImageShowDeviceFrame]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png "Рис. 9: Показать рамку устройства"  
[ImageIphoneFrame]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png "Рисунок 10: кадр устройства для iPhone 6"  
[ImageEdit]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-device-list-edit.msft.png "Рисунок 11: выбор пункта "Изменить""  
[ImageAddCustomDevice]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png "Рисунок 12: Создание настраиваемого устройства"  
[ImageShowRulers]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png "Рисунок 13: отображение линеек"  
[ImageRulers]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-rulers.msft.png "Рисунок 14: линейки выше и слева от окна просмотра"  
[ImageZoomViewport]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-zoom.msft.png "Рисунок 15: масштаб"  
[ImageThrottling]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-throttle.msft.png "Рисунок 16: список регулирования"  
[ImageDeviceToolbar3]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-highlighted.msft.png "Рисунок 17: панель инструментов "устройства""  
[ImageCPU]: /microsoft-edge/devtools-guide-chromium/media/device-mode-performance-cpu-throttle.msft.png "Рисунок 18: список ЦП"  
[ImageNetwork]: /microsoft-edge/devtools-guide-chromium/media/device-mode-network-throttle.msft.png "На рисунке 19: список регулирования"  
[ImageCommandMenu]: /microsoft-edge/devtools-guide-chromium/media/device-mode-command-menu-throttle.msft.png "Рисунок 20: меню команд"  
[ImageNetwork2]: /microsoft-edge/devtools-guide-chromium/media/device-mode-performance-network-throttle.msft.png "Рисунок 21: Настройка регулирования сети с помощью панели "производительность""  
[ImageSensors]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png "Рисунок 22: датчики"  
[ImageShowSensors]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png "Рисунок 23: отображение датчиков"  
[ImageGeolocation]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png "Рисунок 24: географическое положение"  
[ImageSensors2]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png "Рисунок 25: датчики"  
[ImageShowSensors2]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png "Рис. 26: отображение датчиков"  
[ImageOrientation]: /microsoft-edge/devtools-guide-chromium/media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png "Рисунок 27: ориентация"  

<!-- links -->  

<!--[DevToolsCommunity]: ../index.md#community "Join the DevTools community"  -->
[DevToolsRemoteDebugging]:/Microsoft-Edge/Devtools-Guide-Chromium/Remote-Debugging/index "Начало работы с удаленными отладочными устройствами Android"  

[MDNWindowDevicePixelRatio]: https://developer.mozilla.org/docs/Web/API/Window/devicePixelRatio "Window. devicePixelRatio | MDN"  
[MDNUserAgent]: https://developer.mozilla.org/docs/Glossary/User_agent "Агент пользователя | MDN"  

[WikiApproximation]: https://en.wikipedia.org/wiki/Order_of_approximation#First-order "Порядок приближения — первый-заказ — Википедии"  

> [!NOTE]
> <span data-ttu-id="2c5d3-310">Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2c5d3-310">Portions of this page are modifications based on work created and [shared by Google][GoogleSitePolicies] and used according to terms described in the [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  
> <span data-ttu-id="2c5d3-311">Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).</span><span class="sxs-lookup"><span data-stu-id="2c5d3-311">The original page is found [here](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) and is authored by [Kayce Basques][KayceBasques] \(Technical Writer, Chrome DevTools \& Lighthouse\).</span></span>  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
<span data-ttu-id="2c5d3-313">Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].</span><span class="sxs-lookup"><span data-stu-id="2c5d3-313">This work is licensed under a [Creative Commons Attribution 4.0 International License][CCA4IL].</span></span>  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
