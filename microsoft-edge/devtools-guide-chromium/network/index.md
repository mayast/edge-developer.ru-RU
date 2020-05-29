---
title: Проверка активности сети в Microsoft Edge DevTools
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/30/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 267b0113e07085dd565a3ff3437a3fcac2dff9d7
ms.sourcegitcommit: 33663cd7838dddee86228dde469a5e9551bddb02
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/30/2020
ms.locfileid: "10611814"
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





# Проверка активности сети в Microsoft Edge DevTools   



В этом практическом занятии описаны некоторые из наиболее часто используемых функций DevTools, связанных с проанализом активности сети для страницы.  

Для просмотра функциональных возможностей используйте [ссылку сетевая ссылка][DevtoolsNetworkReference] .  

<!--TODO: This entire section needs a Microsoft Edge DevTools re-write  -->

<!-- Read on, or watch the video version of this tutorial:  -->  

<!--
> [!VIDEO embed/e1gAyQuIFQo]  
-->

## Когда следует использовать панель "сеть"   

В общем случае следует использовать панель "сеть", чтобы убедиться в том, что ресурсы загружаются или загружаются должным образом.  Наиболее распространенными вариантами использования панели "сеть" являются:  

*   Убедитесь в том, что ресурсы действительно отправляются или загружаются вообще.  
*   Проверка свойств отдельного ресурса, например HTTP-заголовков, содержимого, размера и т. д.  

Если вы ищете способы повышения быстродействия загрузки страниц, **не** начинайте с панели "сеть".  Существует множество типов проблем с производительностью нагрузки, не связанных с работой сети.  Начните работу с панели аудита, так как она содержит рекомендации по улучшению страницы.  Ознакомьтесь со [скоростью оптимизации веб-сайта][DevtoolsSpeedGetStarted].  

## Открытие панели "сеть"   

Чтобы максимально эффективно пользоваться этим учебником, откройте демонстрацию и ознакомьтесь с функциями на странице Demo.  

1.  Откройте [демонстрацию Приступая к работе][GlitchNetworkGetStarted] .  
    
    > ##### Рис. 1  
    > Демонстрация  
    > ![Демонстрация][ImagesTutorialDemo]  
    
    <!--You may prefer to move the demo to a separate window.  -->  
    
    <!--
    > ##### old Figure 2  
    > The demo in one window and this tutorial in a different window  
    > ![The demo in one window and this tutorial in a different window][ImagesTutorialWindows]  -->

1.  [Откройте DevTools][DevToolsOpen] , нажав клавиши `Control` + `Shift` + `J` \ (Windows \) или `Command` + `Option` + `J` \ (macOS \).  Откроется панель **консоли** .  
    
    > ##### Рисунок 2  
    > На консоли  
    > ! [Консоль] [ImagesTutorialConsole]  
    
    Вы можете [закрепить DevTools в нижней части окна][DevToolsCustomizePlacement].  
    
    > ##### Рисунок3  
    > DevTools закреплено в нижней части окна  
    > ! [DevTools закреплен в нижней части окна] [ImagesTutorialDocked]  

1.  Откройте вкладку **сеть** .  Откроется панель Network (сеть).  
    
    > ##### Рисунок4  
    > DevTools закреплено в нижней части окна  
    > ! [DevTools закреплен в нижней части окна] [ImagesTutorialNetwork]  

Прямо сейчас панель Network (сеть) пуста.  DevTools только записывает сетевые активности после того, как вы откроете ее и не произошел никаких сетевых операций после того, как вы открыли DevTools.  

## Регистрация активности в сети   

Чтобы просмотреть сетевую активность, которая вызывается страницей, выполните указанные ниже действия.  

1.  Перезагрузите страницу.  На панели Network (сеть) регистрируются все сетевые активности в **журнале сети**.  
    
    > ##### Рисунок 5  
    > Журнал сети  
    > ! [Журнал сети] [ImagesTutorialLog]  
    
    Каждая строка **журнала сети** представляет ресурс.  По умолчанию ресурсы указаны в хронологическом порядке.  Самый верхний ресурс обычно является основным HTML-документом.  Самый нижний ресурс — это тот, который запрашивался последним.  
    
    Каждый столбец представляет сведения о ресурсе.  На [**рисунке 6**](#figure-6) показаны столбцы по умолчанию.  

    *   **Состояние**.  Код состояния HTTP для ответа.  
    *   **Тип**.  Тип ресурса.  
    *   **Инициатор**.  Причина запроса ресурса.  При выборе ссылки в столбце инициатора осуществляется переход к исходному коду, вызвавшему запрос.  
    *   **Time (время**).  Продолжительность запроса.  
    *   **Каскадом**.  Графическое представление различных стадий запроса.  
        Наведите указатель мыши на Каскад, чтобы увидеть разбивку.  
    
    > [!NOTE]
    > Диаграмма, расположенная над сетевым журналом, называется обзором.  Вы не будете использовать граф обзора в этом учебнике, поэтому вы можете скрыть его.  Ознакомьтесь [со статьей скрыть область "Общие сведения"][DevtoolsReferenceHideOverview].
        
1.  После открытия DevTools записывает в журнал сети активность сети.  
    Чтобы продемонстрировать это, сначала ознакомьтесь с нижней частью **журнала сети** и запомните о том, что последнее действие будет заглянуть в эту оценку.  
1.  Теперь нажмите кнопку " **получить данные** " в демонстрационной версии.  
1.  Снова посмотрите на нижнюю часть **сетевого журнала** .  Вы должны увидеть новый ресурс под названием "" `getstarted.json` .  Нажатие кнопки " **получить данные** " привела к тому, что страница запрашивает этот файл.  
    
    > ##### Рисунок6  
    > Новый ресурс в сетевом журнале  
    > ! [Новый ресурс в сетевом журнале] [ImagesTutorialRuntime]  

## Показать дополнительные сведения   

Столбцы сетевого журнала можно настраивать.  Столбцы, которые вы не используете, могут быть скрыты.  
Кроме того, существует множество столбцов, которые по умолчанию скрыты, что может оказаться полезным.  

1.  Щелкните правой кнопкой мыши заголовок таблицы журнала сети и выберите команду **Domain (домен**).  Теперь отображается домен каждого ресурса.  
    
    > ##### Рисунок7  
    > Включение столбца Domain (домен)  
    > ! [Включение столбца domain] [ImagesTutorialDomain]  
    
    > [!TIP]
    > Просмотр полного URL-адреса ресурса при наведении указателя мыши на ячейку в столбце **имя** .  

## Имитация медленных подключений к сети   

Сетевое подключение компьютера, используемого для создания сайтов, скорее всего быстрее, чем сетевые подключения мобильных устройств ваших пользователей.  Перетаскивая страницу, вы получите более общее представление о том, как долго страница будет загружаться на мобильном устройстве.  

1.  Выберите раскрывающийся список **регулирования** , для которого по умолчанию установлено значение в **сети** .  
    
    > ##### Рисунок8  
    > Включение регулирования  
    > ! [Включение регулирования] [ImagesTutorialThrottling]  
    
1.  Выберите **медленное 3G**.  
    
    > ##### Рисунок9  
    > Выбор медленной сети 3G  
    > ! [Выберите медленное 3G] [ImagesTutorialSlow3G]  
    
1.  Нажмите кнопку Повторная **Загрузка** ![ ][ImageRefreshIcon] и выберите **пустой кэш и нажмите окончательную перезагрузку**.  
    
    > ##### Рисунок 10  
    > Пустой кэш и окончательная перезагрузка  
    > ! [Пустой кэш и окончательная перезагрузка] [ImagesTutorialHardReload]  
    
    При повторном посещении браузер обычно обслуживает некоторые файлы из [кэша][MDNHTTPCache] , что ускоряет загрузку страницы.  **Пустой кэш, и при принудительной перезагрузке** браузер перейдет в сеть для всех ресурсов.  Это полезно, если вы хотите узнать, как в первый раз происходит загрузка страницы посетителем.  
    
    > [!NOTE]
    > **Пустой кэш и рабочий процесс повторной загрузки** доступны только в том случае, если открыт DevTools.  

## Захват снимков экрана   

С помощью снимков экрана можно увидеть, как страница была найдена во время загрузки.  

1.  Нажмите кнопку ![ Параметры сети ][ImageSettingsIcon] и установите флажок **захватить снимки экрана** .
1.  Снова загрузите страницу с помощью **пустого кэша и окончательной повторной загрузки** .  Если вам нужно напоминание о том, как это сделать, ознакомьтесь [с](#simulate-a-slower-network-connection) разрешениями.  
    В области снимков экрана представлены эскизы того, как страница рассмотрелась на разных этапах процесса загрузки.  
    
    > ##### Рисунок11  
    > Снимки экрана загрузки страницы  
    > ! [Снимки экрана загруженной страницы] [ImagesTutorialAllScreenshots]  

1.  Выберите первый эскиз.  DevTools показывает, какая сетевая активность происходила в данный момент времени.  
    
    > ##### Рисунок12  
    > Сетевая активность, происходящий на первом снимке экрана  
    > ! [Сетевая активность, происходящие во время первого снимка экрана] [ImagesTutorialFirstScreenshot]  

1.  Снова нажмите кнопку ![ Параметры сети ][ImageSettingsIcon] и снимите флажок **захватить снимки экрана** , чтобы закрыть область снимки экрана.
1.  Повторно загрузите страницу.  

## Проверка сведений о ресурсе   

Выберите ресурс, чтобы получить дополнительные сведения о нем.  Попробуйте вот так:  

1.  Выберите `getstarted.html` .  Показана вкладка " **заголовки** ".  Используйте эту вкладку для проверки заголовков HTTP.  
    
    > ##### Рисунок13  
    > Вкладка "заголовки"  
    > ! [Вкладка Заголовки] [ImagesTutorialHeaders]  
    
1.  Откройте вкладку **Предварительный просмотр** .  Отобразится основной рендеринг HTML-кода.  
    
    > ##### Рисунок14  
    > Вкладка "предварительный просмотр"  
    > ! [Вкладка "предварительный просмотр"] [ImagesTutorialPreview]  

     Эта вкладка полезна, если API возвращает код ошибки в HTML.  Возможно, вам будет проще прочитать обработанный HTML, чем исходный HTML-код или просматривает изображения.  

1.  Откройте вкладку **ответ** .  Отобразится исходный код HTML.  
    
    > ##### Рисунок15  
    > Вкладка "ответ"  
    > ! [Вкладка "ответ"] [ImagesTutorialResponse]  
    
    > [!TIP]
    > Если файл minified, то при нажатии кнопки формат **формата** ![ ][ImageFormatIcon] в нижней части вкладки **ответа** повторно форматирует содержимое файла для чтения.  

1.  Откройте вкладку **время** .  Показана сетевая подразделение активности для этого ресурса.  
    
    > ##### Рисунок16  
    > Вкладка время  
    > ! [Вкладка время] [ImagesTutorialTiming]  

1.  Нажмите кнопку **Закрыть** ![ ][ImageCloseIcon] , чтобы снова просмотреть журнал сети.  
    
    > ##### Рисунок17  
    > Кнопка "Закрыть"  
    > ! [Кнопка "Закрыть"] [ImagesTutorialCloseTiming]  

## Поиск заголовков и ответов в сети   

Используйте область **поиска** , если вам нужно найти заголовки HTTP и ответы по всем ресурсам для определенной строки или регулярного выражения.  

Например, предположим, что вы хотите убедиться, что ваши ресурсы используют разумные **политики кэширования**.  

<!--TODO: add cache policies section when available  -->

1.  Выберите **Search** ![ Поиск поиска ][ImageSearchIcon] .  Область поиска откроется слева от сетевого журнала.  
    
    > ##### Рис. 18  
    > Область "Поиск"  
    > ! [Область поиска] [ImagesTutorialSearch]  

1.  Введите текст `Cache-Control` и нажмите клавишу `Enter` .  В области поиска перечислены все вхождения `Cache-Control` , найденные в заголовках или содержимом ресурсов.  
    
    > ##### На рисунке 19  
    > Результаты поиска по запросу  `Cache-Control`  
    > ! [Результаты поиска для Cache-Control] [ImagesTutorialResults]  

1.  Выберите результат, чтобы просмотреть ресурс, в котором был найден результат.  Если вы видите сведения о ресурсе, выберите результат, чтобы перейти непосредственно к нему.  Например, если запрос был найден в заголовке, откроется вкладка Заголовки.   Если запрос найден в содержимом, откроется вкладка **ответ** .  
    
    > ##### Рис. 20  
    > Результат поиска, выделенный на вкладке "заголовки"  
    > ! [Результат поиска, выделенный на вкладке Заголовки] [ImagesTutorialCache]  
    
1.  Закройте область поиска и вкладку заголовки.  
    
    > ##### Рисунок 21  
    > Кнопки "Закрыть"  
    > ! [Кнопки закрытия] [ImagesTutorialCloseButtons]  
    
## Фильтрация ресурсов   

DevTools предоставляет множество рабочих процессов для фильтрации ресурсов, не относящихся к поставленной задаче.  

> ##### Рис. 22  
> Панель инструментов "фильтры"  
> ! [Панель инструментов "фильтры"] [ImagesTutorialFilters]  

Панель инструментов " **фильтры** " должна быть включена по умолчанию.  Если не так:  

1.  Щелкните фильтр **фильтра** ![ ][ImageFilterIcon] , чтобы отобразить его.  

### Фильтрация по строке, регулярному выражению или свойству   

Текстовое поле « **Фильтр** » поддерживает различные типы фильтрации.  

1.  Введите `png` текст в текстовое поле **Фильтр** .  Отображаются только файлы, содержащие текст `png` .  В этом случае только файлы, соответствующие фильтру, являются изображениями в формате PNG.  
    
    > ##### Рис. 23  
    > Строковый фильтр  
    > ! [Строковый фильтр] [ImagesTutorialPNG]  

1.  Введите `/.*\.[cj]s+$/`.  DevTools отфильтровать все ресурсы с именем файла, которое не оканчивается на a, а `j` `c` затем с 1 или более `s` символами.  
    
    > ##### Рисунок 24  
    > Фильтр регулярных выражений  
    > ! [Фильтр регулярных выражений] [ImagesTutorialRegEx]  
    
1.  Введите `-main.css`.  DevTools отфильтровать `main.css` .  Если какой – либо другой файл соответствует шаблону, он также будет исключен.  
    
    > ##### Рис. 25  
    > Отрицательный фильтр  
    > ! [Отрицательный фильтр] [ImagesTutorialNegative]  
    
1.  Введите `domain:cdn.glitch.com` текст в текстовое поле **Фильтр** .  DevTools отфильтровать все ресурсы с URL-адресом, который не соответствует этому домену.  
    
    > ##### Рис. 26  
    > Фильтр свойств  
    > ! [Фильтр свойств] [ImagesTutorialProperty]  

    Просмотрите [запросы фильтрации по свойствам][DevtoolsReferenceProperty] для полного списка фильтруемых свойств.  
    
    
1.  Очистите текстовое поле " **Фильтр** " в любом тексте.  

### Фильтрация по типу ресурсов   

Чтобы сосредоточиться на файле определенного типа, например в таблицах стилей, выполните указанные ниже действия.  

1.  Выберите **CSS**.  Все остальные типы файлов будут отфильтрованы.  
    
    > ##### На рисунке 27  
    > Отображение только CSS файлов  
    > ! [Показывать только файлы CSS] [ImagesTutorialCSS]  
    
1.  Чтобы также просмотреть сценарии, удерживайте клавишу `Control` \ (Windows \) или `Command` \ (macOS \), а затем выберите **JS**.  
    
    > ##### Рис. 28  
    > Отображение только файлов CSS и JS  
    > ! [Показывать только файлы CSS и JS] [ImagesTutorialCSSJS]  
    
1.  Нажмите кнопку **все** , чтобы удалить фильтры и снова просмотреть все ресурсы.  

Просмотр [запросов фильтрации][DevtoolsNetworkReferenceFilter] для других рабочих процессов фильтрации.  

## Блокировать запросы   

Как выглядит и работает страница при недоступности некоторых ресурсов страницы?  Не удается полностью завершить его или он по-прежнему работает?  Блокировка запросов на определение:  

1.  `Control` + `Shift` + `P` Чтобы открыть меню команд, нажмите клавиши \ (Windows \) или `Command` + `Shift` + `P` \ ( **Command Menu**macOS \).  
    
    > ##### Рис. 29  
    > Меню команд  
    > ! [Меню команд] [ImagesTutorialCommandMenu]  
    
1.  Введите `block` команду **Показать блокировку запросов**и нажмите кнопку `Enter` .  
    
    > ##### Рис. 30  
    > Показать блокировку запросов  
    > ! [Показать блокировку запросов] [ImagesTutorialBlock]  

1.  Нажмите кнопку **Добавить** шаблон ![ Добавить узор ][ImageAddIcon] .  
1.  Введите `main.css`.  
    
    > ##### На рисунке 31  
    > Снижающи `main.css`  
    > ! [Блокировка Main. CSS] [ImagesTutorialAddBlock]  
    
1.  Нажмите кнопку **Добавить**.  
1.  Перезагрузите страницу.  Как и предполагалось, стиль страницы немного изменился, так как основная таблица стилей заблокирована.  
    
    > [!NOTE]
    > `main.css`Строка в сетевом журнале.  Красный текст означает, что ресурс заблокирован.
    
    > ##### Рисунок 32  
    > `main.css` заблокирован  
    > ! [Main. CSS заблокирована] [ImagesTutorialBlockedStyles]  

1.  Снимите флажок **включить блокировку запросов** .  

## Заключение  

Поздравляем, вы завершили обучение.  Теперь вы знаете, как использовать панель "сеть" в Microsoft Edge DevTools!






Обратитесь к [справочной][DevtoolsNetworkReference] информации по сети, чтобы узнать о возможностях DevTools проверки активности сети.  

 



<!-- image links -->  

[ImageAddIcon]: /microsoft-edge/devtools-guide-chromium/media/add-icon.msft.png  
[ImageCloseIcon]: /microsoft-edge/devtools-guide-chromium/media/close-icon.msft.png  
[ImageFilterIcon]: /microsoft-edge/devtools-guide-chromium/media/filter-icon.msft.png  
[ImageFormatIcon]: /microsoft-edge/devtools-guide-chromium/media/format-icon.msft.png  
[ImageRefreshIcon]: /microsoft-edge/devtools-guide-chromium/media/refresh-icon.msft.png  
[ImageScreenshotsIcon]: /microsoft-edge/devtools-guide-chromium/media/screenshots-icon.msft.png  
[ImageSearchIcon]: /microsoft-edge/devtools-guide-chromium/media/search-icon.msft.png  
[ImageSettingsIcon]: /microsoft-edge/devtools-guide-chromium/media/settings-icon.msft.png

[ImagesTutorialDemo]: /microsoft-edge/devtools-guide-chromium/media/network-glitch-inspect-network-activity-demo.msft.png "Рисунок 1: демонстрация"  
<!--[ImagesTutorialWindows]: /microsoft-edge/devtools-guide-chromium/media/network-tutorial/windows.msft.png " old Figure 2: The demo in one window and this tutorial in a different window"  -->  
[ImagesTutorialConsole]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Console.MSFT.png "Рисунок 2: консоль"  
[ImagesTutorialDocked]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Console-Bottom.MSFT.png "Рисунок 3: DevTools закреплено в нижней части окна"  
[ImagesTutorialNetwork]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-Bottom.MSFT.png "Рисунок 4: DevTools закреплены в нижней части окна"  
[ImagesTutorialLog]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network.MSFT.png "Рисунок 5: журнал сети"  
[ImagesTutorialRuntime]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-New-Resource.MSFT.png "Рисунок 6: новый ресурс в сетевом журнале"  
[ImagesTutorialDomain]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-Edit-Column.MSFT.png "Рисунок 7: включение столбца домена"  
[ImagesTutorialThrottling]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-Throttling.MSFT.png "Рисунок 8: Включение регулирования"  
[ImagesTutorialSlow3G]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-Throttling-Slow-3G.MSFT.png "Рисунок 9: выбор медленного 3G"  
[ImagesTutorialHardReload]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Empty-Cache-and-Hard-Reset.MSFT.png "Рисунок 10: пустой кэш и окончательная перезагрузка"  
[ImagesTutorialAllScreenshots]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-screenshots.MSFT.png "Рисунок 11: снимки экрана загрузки страницы"  
[ImagesTutorialFirstScreenshot]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-screenshots-First.MSFT.png "Рисунок 12: сетевое действие, происходящее на первом снимке экрана"  
[ImagesTutorialHeaders]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-Resources-Headers.MSFT.png "Рисунок 13: вкладка" заголовки "  
[ImagesTutorialPreview]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-Resources-Preview.MSFT.png "Рисунок 14: вкладка" предварительный просмотр "  
[ImagesTutorialResponse]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-Resources-Response.MSFT.png "Рисунок 15: вкладка" ответ ""  
[ImagesTutorialTiming]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-Resources-Timing.MSFT.png "Рисунок 16: вкладка" время "  
[ImagesTutorialCloseTiming]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-Resources-Close-tabs.MSFT.png "Рисунок 17: кнопка" Закрыть "  
[ImagesTutorialSearch]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-Search-Empty.MSFT.png "Рисунок 18: область поиска"  
[ImagesTutorialResults]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-Search-Cache-Control.MSFT.png "Рисунок 19: результаты поиска для Cache-Control"  
[ImagesTutorialCache]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-Search-Cache-Control-Headers-Response-Headers.MSFT.png "Рисунок 20: результат поиска, выделенный на вкладке" заголовки "  
[ImagesTutorialCloseButtons]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-Search-Close.MSFT.png "Рисунок 21: кнопки" Закрыть "  
[ImagesTutorialFilters]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-Filter-Empty.MSFT.png "рис. 22: панель инструментов" фильтры "  
[ImagesTutorialPNG]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-Filter-PNG.MSFT.png "Рисунок 23: строковый фильтр"  
[ImagesTutorialRegEx]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-Filter-Regex.MSFT.png "Рисунок 24: фильтр регулярных выражений"  
[ImagesTutorialNegative]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-Filter-Negative-Statement.MSFT.png "Рисунок 25: отрицательный фильтр"  
[ImagesTutorialProperty]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-Filter-property-value.MSFT.png "Рисунок 26: фильтр по свойству"  
[ImagesTutorialCSS]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-Filter-File-Type-CSS.MSFT.png "Рисунок 27: показывать только файлы CSS"  
[ImagesTutorialCSSJS]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-Filter-File-Type-CSS-JS.MSFT.png "Рисунок 28: отображение только файлов CSS и JS"  
[ImagesTutorialCommandMenu]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-CLI-Empty.MSFT.png "Рисунок 29: меню команд"  
[ImagesTutorialBlock]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-CLI-Block.MSFT.png "рис. 30: Показать блокировку запросов"  
[ImagesTutorialAddBlock]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-CLI-Block-Add-pattern.MSFT.png "Рисунок 31: Блокировка Main. CSS"  
[ImagesTutorialBlockedStyles]:/Microsoft-Edge/Devtools-Guide-Chromium/Media/Network-Glitch-Network-CLI-Block-Main-CSS.MSFT.png "Рисунок 32: Main. CSS заблокирован"  

<!-- links -->  


<!--[CachePolicies]: ../../../web/tools/lighthouse/audits/cache-policy ""  -->  

[DevToolsCustomizePlacement]: /microsoft-edge/devtools-guide-chromium/customize/placement "Изменение положения DevTools Microsoft EDGE (Отстыковка, закрепить в нижней части, закрепить слева)"  
[DevtoolsNetworkReference]: /microsoft-edge/devtools-guide-chromium/network/reference "Справочник по анализу сети"
[DevtoolsNetworkReferenceFilter]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests "Запросы фильтрации — Справочник по анализу сети"  
[DevtoolsReferenceHideOverview]: /microsoft-edge/devtools-guide-chromium/network/reference#hide-the-overview-pane "Скрытие области обзора — Справка по анализу сети"
[DevtoolsReferenceProperty]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties "Фильтрация запросов по свойствам — Справочник по анализу сети"
[DevToolsOpen]: /microsoft-edge/devtools-guide-chromium/open "Открыть Microsoft Edge DevTools"  
[DevtoolsSpeedGetStarted]: /microsoft-edge/devtools-guide-chromium/speed/get-started "Оптимизация скорости веб-сайта с помощью Microsoft Edge DevTools"  

[GlitchNetworkGetStarted]: https://microsoft-edge-chromium-devtools.glitch.me/static/network/getstarted.html "Пример проверки активности сети"  

[MDNHTTPCache]: https://developer.mozilla.org/docs/Web/HTTP/Caching "Кэширование HTTP | MDN"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/tools/chrome-devtools/network/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
