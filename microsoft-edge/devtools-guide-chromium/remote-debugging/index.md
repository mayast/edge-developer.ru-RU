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
# Начало работы с удаленными отладкой устройств с Android   



Удаленная отладка динамического содержимого на устройстве Android с компьютера Windows или macOS.  В этом учебнике рассказывается о том, как выполнять следующие действия:  

*   Настройте устройство Android для удаленной отладки и найдите его на компьютере разработчика.  
*   Изучите и отлаживать динамический контент на устройстве с Android с компьютера для разработки.  
*   Содержимое ролика с устройства Android на экземпляр DevTools на компьютере разработчика.  

<!--
> ##### Figure 1  
> Remote Debugging lets you inspect a page running on an Android device from your development machine  
> ![Remote Debugging lets you inspect a page running on an Android device from your development machine][ImageRemoteDebugging]  -->

## Шаг 1: обнаружение устройства с Android   

Рабочий процесс, описанный ниже, подходит для большинства пользователей.  Дополнительные сведения можно найти в [статье Устранение неполадок: DevTools не удается найти устройство Android](#troubleshooting-devtools-is-not-detecting-the-android-device) .  

1.  Откройте экран **Параметры разработчика** на устройстве с Android.  Дополнительные сведения [можно найти в разделе Настройка параметров разработчика на устройстве](https://developer.android.com/studio/debug/dev-options.html).  
1.  Выберите **включить отладку USB**.  
1.  На своем компьютере для разработки откройте Microsoft Edge.  
1.  [Откройте DevTools][DevToolsOpen].  
1.  В DevTools выберите **главное меню** , `...` а затем щелкните **другие инструменты**  >  **Удаленные устройства**.  
    
    > ##### Рис. 1  
    > Открытие вкладки " **Удаленные устройства** " с помощью **главного меню**  
    > ! [Открытие вкладки удаленные устройства через главное меню] [ImageOpenRemoteDevices]  

1.  В DevTools откройте вкладку **Параметры** .  

1.  Убедитесь, что флажок **обнаружение устройств USB** включен.  
    
    > ##### Рисунок 2  
    > Флажок " **обнаружение USB-устройств** " включен  
    > ! [Флажок обнаружение USB-устройств установлен] [ImageDiscoverUSBDevices]  

1.  Подключите устройство Android непосредственно к компьютеру разработчика с помощью USB-кабеля.  Когда вы в первый раз получите это, вы, скорее всего, видите, что DevTools обнаружил неизвестное устройство.  Если отображается зеленая точка и текст, **связанный** с названием модели устройства с Android, DevTools успешно установил подключение к устройству.  Перейдите к [действию 2](#step-2-debug-content-on-your-android-device-from-your-development-machine).  
    <!--
    > ##### Figure 4  
    > The **Remote Devices** tab has successfully detected an unknown device that is pending authorization  
    > ![The Remote Devices tab has successfully detected an unknown device that is pending authorization][ImageUnknownDevice]  -->

1.  Если ваше устройство отображается как **неизвестное**, используйте запрос разрешения на **отладку USB** на устройстве с Android.  

### Устранение неполадок: DevTools не может обнаружить устройство с Android   

Убедитесь, что оборудование настроено правильно.  

*   Если вы используете USB-концентратор, попробуйте подключить устройство Android прямо к компьютеру разработчика.  
*   Попробуйте отключить кабель USB между устройством Android и компьютером разработчика, а затем снова подключив его.  Это можно сделать, когда экраны компьютера Android и разработки были разблокированы.  
*   Убедитесь, что USB-кабель работает.  Вы должны иметь возможность проверять файлы на устройстве с Android с компьютера, на котором ведется разработка.  

Убедитесь, что программное обеспечение настроено правильно.  

*   Если на вашем компьютере разработчика установлена операционная система Windows, попробуйте установить драйверы USB для устройства с Android вручную.  Ознакомьтесь с [Разустановочными драйверами USB для OEM][AndroidUSBDrivers].  
    
*   Некоторые комбинации устройств Windows и Android (особенно Samsung) требуют дополнительной настройки.  В разделе [DevTools Devices (устройства) не обнаруживаются устройства, подключенные к сети] [StackOverflowDevicesNotDetected].  
    
Если вы не видите предупреждение **Разрешить отладку USB** на устройстве с Android, попробуйте выполнить указанные ниже действия.  

*   Отключение кабеля USB и повторное подключение к нему, когда DevTools на компьютере разработки и отображается начальный экран на устройстве с Android.  Другими словами, иногда сообщение не отображается, когда экраны компьютера Android или разработчика заблокированы.
*   Обновите параметры отображения для устройства Android и компьютера для разработки, чтобы они никогда не переходят в спящий режим.  
*   Установка режима USB для устройства с Android на PTP.  В разделе [Galaxy S4 не отображается диалоговое окно "авторизация USB"][StackExchangeGalaxyS4DoesNotShowDialogBox].  
*   Выберите **отозвать разрешения на отладку USB** на экране **Параметры разработчика** на устройстве с Android, чтобы сбросить его в новое состояние.  

Если вы нашли решение, которое не упомянуто в этом разделе, или в [DevTools Devices не обнаружит устройство при подключении к сети] [StackOverflowDevicesNotDetected] или добавьте ответ на этот вопрос с переполнением стека.<!--, or [open an issue in the webfundamentals repository][GitHubWebFundamentalsNewIssue]-->!  

## Шаг 2: Отладка содержимого на устройстве с Android с компьютера для разработки   

1.  Откройте Microsoft EDGE на устройстве с Android.  

1.  На вкладке **Удаленные устройства** выберите вкладку, которая соответствует имени модели устройства Android.  
    В верхней части этой страницы вы увидите название модели устройства с Android, а затем серийный номер.  Ниже показана версия Microsoft EDGE, установленная на устройстве, с номером версии в круглых скобках.  Каждая открытая вкладка Microsoft Edge получает собственный раздел.  Вы можете работать с этой вкладкой в этом разделе.  <!--If there are any apps using WebView, you see a section for each of those apps, too.  --><!--In [**Figure 5**](#figure-5) there are no tabs or WebViews open.  -->
    <!--
    > ##### Figure 5  
    > A connected remote device  
    > ![A connected remote device][ImageConnectedRemoteDevice]  -->

1.  В текстовом поле **Новая вкладка** введите URL-адрес и нажмите кнопку **Открыть**.  Страница откроется на новой вкладке на устройстве с Android.  

1.  Нажмите кнопку " **проверить** " рядом с URL-адресом, который вы только что открыли.  Откроется новый экземпляр DevTools.  Версия Microsoft EDGE, установленная на устройстве с Android, определяет версию DevTools, которая открывается на компьютере разработчика.  
    Таким образом, если на вашем устройстве Android установлена старая версия Microsoft EDGE, экземпляр DevTools может отличаться от того, с чем вы используете.  

### Дополнительные действия: перезагрузка, фокус или закрытие вкладки   

Щелкните значок **Дополнительные параметры** `...` рядом с вкладкой, которую вы хотите перегрузить, сосредоточиться или закрыть.  
<!--
> ##### Figure 6  
> The menu for reloading, focusing, or closing a tab  
> ![The menu for reloading, focusing, or closing a tab][ImageReload]  -->

### Проверка элементов   

Перейдите на панель **элементы** экземпляра DevTools и наведите указатель мыши на элемент, чтобы выделить его в окне просмотра на устройстве с Android.  

Вы также можете выбрать элемент на экране устройства с Android, чтобы выбрать его на панели " **элементы** ".  Выберите пункт выбрать элемент SELECT **элемента** ![ ][ImageSelectElementIcon] в экземпляре DevTools, а затем выберите элемент на экране устройства с Android.  

> [!NOTE]
> **Элемент "выбрать** " отключается после первого выбора, поэтому при каждом использовании этой функции необходимо повторно включить его.  

### Демонстрация экрана Android на компьютере разработчика   

Нажмите **кнопку Переключить** презентацию, ![ ][ImageToggleScreencastIcon] чтобы просмотреть содержимое устройства с Android в экземпляре DevTools.  

Вы можете работать с презентацией несколькими способами.  

*   Нажатия клавиш переводятся в касания, и на устройстве обрабатывались соответствующие события сенсорного ввода.  
*   Нажатия клавиш на компьютере отправляются на устройство.  
*   Чтобы смоделировать жест сжатия, удерживайте `Shift` при перетаскивании.  
*   Для прокрутки используйте сенсорной панели, колесико мыши или смахивание с помощью указателя мыши.

Некоторые заметки для презентаций:  

*   В ролики отображается только содержимое страницы.  Прозрачные части презентации представляют интерфейсы устройства, такие как адресная строка Microsoft EDGE, строка состояния Android или клавиатура Android.  
*   Ролики негативно влияют на частоту кадров.  Отключите экранную анимацию, изменяя прокрутки или анимации, чтобы получить более точную картину производительности страницы.  
*   Если экран вашего устройства с Android блокируется, содержимое презентации исчезнет.  Разблокируйте экран устройства с Android для автоматического возобновления ролика.  





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
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/remote-debugging/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
