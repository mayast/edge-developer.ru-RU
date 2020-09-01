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

Нажмите кнопку **Переключить панель инструментов** \ ( ![ Переключить панель инструментов устройства ][ImageDeviceToolbarIcon] ), чтобы открыть пользовательский интерфейс, позволяющий имитировать окно просмотра для мобильных устройств.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Панель инструментов "устройства"" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   Панель инструментов "устройства"  
:::image-end:::  

По умолчанию панель инструментов устройства открывается в режиме отклика окна просмотра.  

### Режим окна просмотра с откликом   

Перетащите маркеры, чтобы изменить размер окна просмотра в соответствии с нужными размерами.  Кроме того, можно ввести значения в полях Ширина и высота.  На приведенном ниже рисунке задана ширина `626` и высота задана `516` .  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png" alt-text="Дескрипторы для изменения размеров окна просмотра в отклике режима просмотра" lightbox="../media/device-mode-toggle-device-toolbar-handles-highlighted.msft.png":::
   Дескрипторы для изменения размеров окна просмотра в отклике режима просмотра  
:::image-end:::  

#### Показать мультимедийные запросы   

Чтобы отобразить точки останова для запросов мультимедиа над окном просмотра, нажмите кнопку **Дополнительные параметры** и выберите пункт **Показать мультимедийные запросы**.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png" alt-text="Показать мультимедийные запросы" lightbox="../media/device-mode-toggle-device-toolbar-more-options-show-media-queries.msft.png":::
   **Показать мультимедийные запросы**  
:::image-end:::  

Щелкните точку останова, чтобы изменить ширину окна просмотра таким образом, чтобы точка останова была инициирована.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png" alt-text="Щелкните точку останова, чтобы изменить ширину окна просмотра" lightbox="../media/device-mode-toggle-device-toolbar-click-breakpoint.msft.png":::
   Щелкните точку останова, чтобы изменить ширину окна просмотра  
:::image-end:::  

#### Настройка типа устройства   

Используйте список **типов устройств** для имитации мобильного устройства или настольного устройства.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png" alt-text="Список типов устройств" lightbox="../media/device-mode-toggle-device-toolbar-device-type-list.msft.png":::
   Список **типов устройств**  
:::image-end:::  

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

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list.msft.png" alt-text="Список устройств" lightbox="../media/device-mode-toggle-device-toolbar-device-list.msft.png":::
   Список **устройств**  
:::image-end:::  

#### Поворот окна просмотра на альбомную ориентацию   

**Rotate** ![ ][ImageRotateIcon] Чтобы повернуть окно просмотра на альбомную ориентацию, нажмите повернуть на (повернуть).  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-landscape.msft.png" alt-text="Альбомная ориентация" lightbox="../media/device-mode-toggle-device-toolbar-landscape.msft.png":::
   Альбомная ориентация  
:::image-end:::  

> [!NOTE]
> Кнопка **повернуть** исчезнет, если **панель инструментов на устройстве** является узкой.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Панель инструментов "устройства"" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   **Панель инструментов "устройства** "  
:::image-end:::  

Смотрите также [Настройка ориентации](#set-orientation).  

#### Показать рамку устройства   

При моделировании размеров определенного мобильного устройства, например iPhone 6, откройте **меню Дополнительные параметры** и выберите пункт **Показать рамку устройства** , чтобы отобразить рамку физического устройства вокруг окна просмотра.  

> [!NOTE]
> Если вы не видите рамку устройства для определенного устройства, скорее всего, это означает, что DevTools просто не имеет иллюстраций для определенного параметра.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png" alt-text="Показать рамку устройства" lightbox="../media/device-mode-toggle-device-toolbar-option-show-device-frame.msft.png":::
         Показать рамку устройства  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png" alt-text="Рамка устройства для iPhone 6" lightbox="../media/device-mode-toggle-device-toolbar-options-device-frame-iphone-6.msft.png":::
         Рамка устройства для iPhone 6  
      :::image-end:::  
   :::column-end:::
:::row-end:::

#### Добавление настраиваемого мобильного устройства   

Чтобы добавить настраиваемое устройство, выполните указанные ниже действия.  

1.  Щелкните список **устройств** и выберите команду **изменить**.  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png" alt-text="Нажмите кнопку Изменить." lightbox="../media/device-mode-toggle-device-toolbar-device-list-edit.msft.png":::
       Нажмите кнопку **изменить** .  
    :::image-end:::  
    
1.  Нажмите кнопку **Добавить настраиваемое устройство**.  
1.  Введите имя, ширину и высоту устройства.  Поля « [отношение к пикселям][MDNWindowDevicePixelRatio]», « [строка агента пользователя][MDNUserAgent]» и « [тип устройства](#set-the-device-type) » являются необязательными.  Поле «Тип устройства» — это список, который по умолчанию имеет значение " **мобильный** ".  
    
    :::image type="complex" source="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png" alt-text="Создание настраиваемого устройства" lightbox="../media/device-mode-toggle-device-toolbar-settings-emulated-devices-add.msft.png":::
       Создание настраиваемого устройства  
    :::image-end:::  

### Отображение линеек   

Нажмите кнопку **Дополнительные параметры** , а затем выберите пункт **Показывать линейки** , чтобы увидеть линейки сверху и слева от окна просмотра.  Единица измерения линеек — Пиксели.  

:::row:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png" alt-text="Отображение линеек" lightbox="../media/device-mode-toggle-device-toolbar-options-show-rulers.msft.png":::
         **Отображение линеек**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-rulers.msft.png" alt-text="Линейки сверху и слева от окна просмотра" lightbox="../media/device-mode-toggle-device-toolbar-rulers.msft.png":::
         Линейки сверху и слева от окна просмотра  
      :::image-end:::  
   :::column-end:::
:::row-end:::

### Изменение масштаба просмотра   

С помощью списка **масштаб** вы можете увеличить или уменьшить масштаб.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-zoom.msft.png" alt-text="Масштаб" lightbox="../media/device-mode-toggle-device-toolbar-zoom.msft.png":::
   **Масштаб**  
:::image-end:::  

## Регулирование сети и ЦП   

Для регулирования сети и ЦП выберите на **мобильном** или **низком мобильном** уровне в списке **регулирования** .  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-throttle.msft.png" alt-text="Список регулирования" lightbox="../media/device-mode-toggle-device-toolbar-throttle.msft.png":::
   Список **регулирования**  
:::image-end:::  

На **мобильном устройстве с уровнем "среднее** " эмулируется быстрое соединение и снижается частота центрального процессора, так как это происходит в течение 4 часов, чем обычно.  На **мобильном** телефоне эмулируется медленная работа сети 3G и снижается частота процессора 6, чем обычно.  Имейте в виду, что регулирование задается относительно нормальной работы ноутбука или рабочего стола.  

> [!NOTE]
> Список **регулирования** скрывается, если **панель инструментов устройства** является узкой.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-highlighted.msft.png" alt-text="Панель инструментов "устройства"" lightbox="../media/device-mode-toggle-device-toolbar-highlighted.msft.png":::
   **Панель инструментов "устройства** "  
:::image-end:::  

### Регулирование только ЦП   

Чтобы перерегулировать только ЦП, а не сеть, перейдите на панель **производительность** , нажмите **Параметры захвата** \ ( ![ Параметры захвата ][ImageCaptureIcon] ), а затем выберите скорость или **6X** **замедление** в списке **ЦП** .  

:::image type="complex" source="../media/device-mode-performance-cpu-throttle.msft.png" alt-text="Список ЦП" lightbox="../media/device-mode-performance-cpu-throttle.msft.png":::
   Список **ЦП**  
:::image-end:::  

### Регулирование сети только   

Для регулирования сети, а не центрального процессора, откройте панель Network ( **сеть** ) и выберите в списке **регулирования** команду **Быстрый 3G** или **низкая 3G** .  

:::image type="complex" source="../media/device-mode-network-throttle.msft.png" alt-text="Список регулирования" lightbox="../media/device-mode-network-throttle.msft.png":::
   Список **регулирования**  
:::image-end:::  

Или нажмите клавиши `Control` + `Shift` + `P` \ (Windows \) или `Command` + `Shift` + `P` \ (macOS \), чтобы открыть **меню команд**, введите `3G` и выберите **включить быстрое регулирование сети 3G** или **включить медленное регулирование сети 3G**.  

:::image type="complex" source="../media/device-mode-command-menu-throttle.msft.png" alt-text="Меню команд" lightbox="../media/device-mode-command-menu-throttle.msft.png":::
   **Меню команд**  
:::image-end:::  

Вы также можете настроить регулирование сети на панели **Performance** .  Нажмите кнопку **захвата параметров** \ ( ![ Параметры ][ImageCaptureIcon] захвата), а затем выберите в списке список **сетей** вариант **Быстрая 3G** или **низкая 3G** .  

:::image type="complex" source="../media/device-mode-performance-network-throttle.msft.png" alt-text="Настройка регулирования сети с помощью панели "производительность"" lightbox="../media/device-mode-performance-network-throttle.msft.png":::
   Настройка регулирования сети с помощью панели " **производительность** "  
:::image-end:::  

## Переопределение географического положения   

Чтобы открыть пользовательский интерфейс переопределения географического положения, нажмите кнопку **Настройка DevTools и** `...` выберите пункт **другие инструменты**  >  **датчики**.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Датчики" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
   **Датчики**  
:::image-end:::  

Или нажмите клавиши `Control` + `Shift` + `P` \ (Windows \) или `Command` + `Shift` + `P` \ (macOS \), чтобы открыть меню команд, введите `Sensors` и выберите пункт **Показать датчики**.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Показать датчики" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
   **Показать датчики**  
:::image-end:::  

Выберите один из стилей из списка **географического расположения** или выберите **другое расположение** , чтобы ввести собственные координаты, или выберите **расположение недоступно** , чтобы проверить, как будет выглядеть страница, когда географическое положение находится в состоянии ошибки.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png" alt-text="Геолокация" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo.msft.png":::
   **Геолокация**  
:::image-end:::  

## Настройка ориентации   

:::row:::
   :::column span="":::
      Чтобы открыть пользовательский интерфейс ориентации, нажмите кнопку **Настройка DevTools** и `...` выберите пункт **другие**  >  **датчики**инструментов.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png" alt-text="Датчики" lightbox="../media/device-mode-toggle-device-toolbar-more-tools-sensors.msft.png":::
         **Датчики**  
      :::image-end:::  
   :::column-end:::
   :::column span="":::
      Или нажмите клавиши `Control` + `Shift` + `P` \ (Windows \) или `Command` + `Shift` + `P` \ (macOS \), чтобы открыть меню команд, введите `Sensors` и выберите пункт **Показать датчики**.  
      
      :::image type="complex" source="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png" alt-text="Показать датчики" lightbox="../media/device-mode-toggle-device-toolbar-command-menu-sensors.msft.png":::
         **Показать датчики**  
      :::image-end:::  
   :::column-end:::
:::row-end:::

Выберите один из наборов параметров в списке **ориентация** или выберите Пользовательский вариант **ориентация** , чтобы задать значения альфа, бета и гамма.  

:::image type="complex" source="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png" alt-text="Ориентация" lightbox="../media/device-mode-toggle-device-toolbar-sensors-tokyo-portrait-upside-down.msft.png":::
   **Ориентация**  
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
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/device-mode/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
