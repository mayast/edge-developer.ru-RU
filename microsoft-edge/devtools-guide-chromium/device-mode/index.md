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





# Эмуляция мобильных устройств с помощью режима устройства в Microsoft Edge DevTools   

  

С помощью режима устройства вы можете оценить внешний вид страницы и ее выполнение на мобильном устройстве.  

Режим устройства — это имя для свободной коллекции функций в Microsoft Edge DevTools, которые помогают имитировать мобильные устройства.  К таким функциям относятся:  

*   [Имитация окна просмотра для мобильных устройств](#simulate-a-mobile-viewport)  
*   [Регулирование сети](#throttle-the-network-only)  
*   [Регулирование ЦП](#throttle-the-cpu-only)  
*   [Имитация географического местоположения](#override-geolocation)  
*   [Настройка ориентации](#set-orientation)  

## Ограничения   

Режим устройства облагается [приблизительно][WikiApproximation] так, как выглядит страница на мобильном устройстве.  В режиме устройства вы фактически не запускаете ваш код на мобильном устройстве.  Вы имитируете взаимодействие с пользователем на мобильном устройстве или компьютере.  

Некоторые аспекты мобильных устройств, которые DevTools никогда не смогут имитировать.  Например, архитектура мобильных процессоров очень отличается от архитектуры ноутбука или процессоров для настольных ПК.  Если вы сомневаетесь, лучше использовать страницу на мобильном устройстве.  Использование [удаленной отладки] [DevToolsRemoteDebugging] для просмотра, изменения, отладки и профилирования кода страницы на мобильном устройстве или рабочем столе.  

## Имитация окна просмотра для мобильных устройств   

Нажмите **кнопку** Переключить панель инструментов устройства ![ ][ImageDeviceToolbarIcon] , чтобы открыть пользовательский интерфейс, позволяющий имитировать окно просмотра для мобильных устройств.  

> ##### Рис. 1  
> Панель инструментов "устройства"  
> ![Панель инструментов "устройства"][ImageDeviceToolbar]  

По умолчанию панель инструментов устройства открывается в режиме отклика окна просмотра.  

### Режим окна просмотра с откликом   

Перетащите маркеры, чтобы изменить размер окна просмотра в соответствии с нужными размерами.  Кроме того, можно ввести значения в полях Ширина и высота.  На [рисунке 2](#figure-2)задана ширина `626` и высота задана `516` .  

> ##### Рисунок 2  
> Дескрипторы для изменения размеров окна просмотра в отклике режима просмотра  
> ![Дескрипторы для изменения размеров окна просмотра в отклике режима просмотра][ImageResponsiveHandles]  

#### Показать мультимедийные запросы   

Чтобы отобразить точки останова для запросов мультимедиа над окном просмотра, нажмите кнопку **Дополнительные параметры** и выберите пункт **Показать мультимедийные запросы**.  

> ##### Рисунок3  
> Показать мультимедийные запросы  
> ![Показать мультимедийные запросы][ImageShowMediaQueries]  

Щелкните точку останова, чтобы изменить ширину окна просмотра таким образом, чтобы точка останова была инициирована.  

> ##### Рисунок4  
> Щелкните точку останова, чтобы изменить ширину окна просмотра  
> ![Щелкните точку останова, чтобы изменить ширину окна просмотра][ImageBreakpoint]  

#### Настройка типа устройства   

Используйте список **типов устройств** для имитации мобильного устройства или настольного устройства.  

> ##### Рисунок 5  
> Список **типов устройств**  
> ![Список типов устройств][ImageDeviceType]  

В приведенной ниже таблице описаны различия между параметрами.  **Метод рендеринга** указывает, будет ли Microsoft Edge обрабатывать страницу в виде окна просмотра на мобильном или рабочем столе.  **Значок курсора** указывает на тип курсора, который отображается при наведении указателя мыши на страницу.  **События, созданные** в зависимости от того, срабатывает ли страница `touch` или `click` события при взаимодействии со страницей.  

| Параметр | Метод отрисовки | Значок курсора | События, созданные |  
|:--- |:--- |:--- |:--- |  
| Мобильные устройства | Мобильные устройства | Круг | Сенсорный ввод |  
| Мобильный – (без сенсорных устройств) | Мобильные устройства | Обычный |  нажмите  |  
| Desktop | Desktop | Обычный |  нажмите  |  
| Классическое приложение (касание) | Desktop | Круг | Сенсорный ввод |  

> [!NOTE]
> Если список **тип устройства** не отображается, нажмите кнопку **Дополнительные параметры** и выберите команду **Добавить тип устройства**.  

### Режим просмотра на мобильном устройстве   

Чтобы смоделировать размеры определенного мобильного устройства, выберите нужное устройство из списка **устройств** .  

> ##### Рисунок6  
> Список устройств  
> ![Список устройств][ImageDeviceList]  

#### Поворот окна просмотра на альбомную ориентацию   

Нажмите кнопку **повернуть** ![ поворачивать, ][ImageRotateIcon] чтобы повернуть окно просмотра на альбомную ориентацию.  

> ##### Рисунок7  
> Альбомная ориентация  
> ![Альбомная ориентация][ImageLandscape]  

> [!NOTE]
> Кнопка **повернуть** исчезнет, если **панель инструментов на устройстве** является узкой.  

> ##### Рисунок8  
> Панель инструментов "устройства"  
> ![Панель инструментов "устройства"][ImageDeviceToolbar2]  

Смотрите также [Настройка ориентации](#set-orientation).  

#### Показать рамку устройства   

При моделировании размеров определенного мобильного устройства, например iPhone 6, откройте **меню Дополнительные параметры** и выберите пункт **Показать рамку устройства** , чтобы отобразить рамку физического устройства вокруг окна просмотра.  

> [!NOTE]
> Если вы не видите рамку устройства для определенного устройства, скорее всего, это означает, что DevTools просто не имеет иллюстраций для определенного параметра.  

> ##### Рисунок9  
> Показать рамку устройства  
> ![Показать рамку устройства][ImageShowDeviceFrame]  

> ##### Рисунок 10  
> Рамка устройства для iPhone 6  
> ![Рамка устройства для iPhone 6][ImageIphoneFrame]  

#### Добавление настраиваемого мобильного устройства   

Чтобы добавить настраиваемое устройство, выполните указанные ниже действия.  

1.  Щелкните список **устройств** и выберите команду **изменить**.  

> ##### Рисунок11  
> Выбор **Edit** 
> ![ команды "Изменить"][ImageEdit]  

1.  Нажмите кнопку **Добавить настраиваемое устройство**.  

1.  Введите имя, ширину и высоту устройства.  Поля « [отношение к пикселям][MDNWindowDevicePixelRatio]», « [строка агента пользователя][MDNUserAgent]» и « [тип устройства](#set-the-device-type) » являются необязательными.  Поле «Тип устройства» — это список, который по умолчанию имеет значение " **мобильный** ".  

> ##### Рисунок12  
> Создание настраиваемого устройства  
> ![Создание настраиваемого устройства][ImageAddCustomDevice]  

### Отображение линеек   

Нажмите кнопку **Дополнительные параметры** , а затем выберите пункт **Показывать линейки** , чтобы увидеть линейки сверху и слева от окна просмотра.  Единица измерения линеек — Пиксели.  

> ##### Рисунок13  
> Отображение линеек  
> ![Отображение линеек][ImageShowRulers]  

> ##### Рисунок14  
> Линейки сверху и слева от окна просмотра  
> ![Линейки сверху и слева от окна просмотра][ImageRulers]  

### Изменение масштаба просмотра   

С помощью списка **масштаб** вы можете увеличить или уменьшить масштаб.  

> ##### Рисунок15  
> Масштаб  
> ![Масштаб][ImageZoomViewport]  

## Регулирование сети и ЦП   

Для регулирования сети и ЦП выберите на **мобильном** или **низком мобильном** уровне в списке **регулирования** .  

> ##### Рисунок16  
> Список регулирования  
> ![Список регулирования][ImageThrottling]  

На **мобильном устройстве с уровнем "среднее** " эмулируется быстрое соединение и снижается частота центрального процессора, так как это происходит в течение 4 часов, чем обычно.  На **мобильном** телефоне эмулируется медленная работа сети 3G и снижается частота процессора 6, чем обычно.  Имейте в виду, что регулирование задается относительно нормальной работы ноутбука или рабочего стола.  

> [!NOTE]
> Список **регулирования** будет скрыт, если **панель инструментов устройства** является узкой.  

> ##### Рисунок17  
> Панель инструментов "устройства"  
> ![Панель инструментов "устройства"][ImageDeviceToolbar3]  

### Регулирование только ЦП   

Чтобы перерегулировать только ЦП, а не сеть, перейдите на панель **производительность** , щелкните Параметры захвата **параметров** ![ ][ImageCaptureIcon] , а затем выберите скорость или **6X** **замедление** в списке **ЦП** .  

> ##### Рис. 18  
> Список ЦП  
> ![Список ЦП][ImageCPU]  

### Регулирование сети только   

Для регулирования сети, а не центрального процессора, откройте панель Network ( **сеть** ) и выберите в списке **регулирования** команду **Быстрый 3G** или **низкая 3G** .  

> ##### На рисунке 19  
> Список регулирования  
> ![Список регулирования][ImageNetwork]  

Или нажмите клавиши `Control` + `Shift` + `P` \ (Windows \) или `Command` + `Shift` + `P` \ (macOS \), чтобы открыть меню команд, введите `3G` и выберите **включить быстрое регулирование сети 3G** или **включить медленное регулирование сети 3G**.  

> ##### Рис. 20  
> Меню команд  
> ![Меню команд][ImageCommandMenu]  

Вы также можете настроить регулирование сети на панели **Performance** .  Нажмите **кнопку захват** параметров ![ ][ImageCaptureIcon] , а затем в списке список **сетей** выберите пункт **Быстрая 3G** или **низкая 3G** .  

> ##### Рисунок 21  
> Настройка регулирования сети с помощью панели "производительность"  
> ![Настройка регулирования сети с помощью панели "производительность"][ImageNetwork2]  

## Переопределение географического положения   

Чтобы открыть пользовательский интерфейс переопределения географического расположения, нажмите кнопку **Настройка DevTools** и `...` выберите пункт **другие**  >  **датчики**инструментов.  

> ##### Рис. 22  
> Датчики  
> ![Датчики][ImageSensors]  

Или нажмите клавиши `Control` + `Shift` + `P` \ (Windows \) или `Command` + `Shift` + `P` \ (macOS \), чтобы открыть меню команд, введите `Sensors` и выберите пункт **Показать датчики**.  

> ##### Рис. 23  
> Показать датчики  
> ![Показать датчики][ImageShowSensors]  

Выберите один из стилей из списка **географического расположения** или выберите **другое расположение** , чтобы ввести собственные координаты, или выберите **расположение недоступно** , чтобы проверить, как будет выглядеть страница, когда географическое положение находится в состоянии ошибки.  

> ##### Рисунок 24  
> Геолокация  
> ![Геолокация][ImageGeolocation]  

## Настройка ориентации   

Чтобы открыть пользовательский интерфейс ориентации, нажмите кнопку **Настройка DevTools** и `...` выберите пункт **другие**  >  **датчики**инструментов.  

> ##### Рис. 25  
> Датчики  
> ![Датчики][ImageSensors2]  

Или нажмите клавиши `Control` + `Shift` + `P` \ (Windows \) или `Command` + `Shift` + `P` \ (macOS \), чтобы открыть меню команд, введите `Sensors` и выберите пункт **Показать датчики**.  

> ##### Рис. 26  
> Показать датчики  
> ![Показать датчики][ImageShowSensors2]  

Выберите один из наборов параметров в списке **ориентация** или выберите Пользовательский вариант **ориентация** , чтобы задать значения альфа, бета и гамма.  

> ##### На рисунке 27  
> Ориентация  
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
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
