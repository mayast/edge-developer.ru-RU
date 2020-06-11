---
title: Новые возможности DevTools (Microsoft Edge 83)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/10/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
ms.openlocfilehash: 7651430c581346d1f140f0a5974b8aa9bb809204
ms.sourcegitcommit: f010f43604bd4363af6827f79dbc071b9afcb667
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2020
ms.locfileid: "10709062"
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

# Новые возможности DevTools (Microsoft Edge 83)  

Согласно обновленному календарному плану Chromium мы настраивая наше расписание для предстоящих выпусков Microsoft EDGE и отменив выпуск Microsoft Edge 82. Дополнительные сведения находятся в записи [блога][WindowsBlogStableRelease] .  

Ниже описаны новые возможности, доступные в DevTools в Microsoft Edge 83.  

## Объявления из группы Microsoft Edge DevTools  

В следующих разделах представлен список извещений, которые вы могли не получить в Microsoft Edge DevTools Teams! Узнайте, как использовать новые функции в DevTools, расширения кода VS и многое другое.  Чтобы оставаться на связи с самыми последними и более свежими возможностями, скачайте на веб – [каналы предварительной версии Microsoft Edge][MicrosoftEdgePreviewChannels] и [следуйте указаниям Twitter][EdgeDevToolsTwitterAccount].  

### Удаленная отладка Microsoft EDGE на устройствах с Windows 10  

Приложение [Remote Tools для Microsoft Edge \ (бета-версия)][RemoteTools] теперь доступно в [магазине Microsoft Store][MicrosoftStore].  С помощью этого приложения, которое расширяет [портал устройств Windows][WindowsDevicePortal], вы можете подключаться из экземпляра Microsoft EDGE, запущенного на компьютере разработки, на удаленное устройство с Windows 10, просмотреть список конечных объектов \ (все вкладки в Microsoft EDGE и [PWAs][PWADoc] открыть на устройстве с Windows 10 \) и использовать DevTools на своем компьютере для разработки по отношению к целевому объекту на удаленном устройстве с Windows 10.  

:::image type="complex" source="../../media/2020/03/remote-tools.msft.png" alt-text="Приложение Remote Tools для Microsoft EDGE (бета-версия), доступное в Microsoft Store" lightbox="../../media/2020/03/remote-tools.msft.png":::
   Рисунок 1: приложение [Remote Tools для Microsoft EDGE (Beta)][RemoteTools] , доступное в [Microsoft Store][MicrosoftStore]  
:::image-end:::  

[Ознакомьтесь с руководством по настройке устройства с Windows 10 и компьютера для разработки удаленной отладки][RemoteDebuggingWin10].  Сообщите нам об удаленной отладке, выполнив [твит][PostTweetEdgeDevTools] или щелкнув значок [обратной связи](#feedback) !  

### Новые способы доступа к параметрам  

Существует множество параметров для DevTools, которые можно настроить таким образом, чтобы DevTools внешний вид, оформление и работу. В Microsoft Edge 83 доступ к [параметрам][OverviewSettings] в DevTools теперь стал более простым. Откройте параметры с помощью значка шестеренки рядом с пунктом оповещения консоли и главное меню.  

:::image type="complex" source="../../media/2020/03/settings.msft.png" alt-text="Значок шестеренки, чтобы открыть параметры в DevTools" lightbox="../../media/2020/03/settings.msft.png":::
   Рисунок 2: значок шестеренки открывает **Параметры** в DevTools  
:::image-end:::  

Вы также можете открыть [Параметры][OverviewSettings] из **главного меню** в разделе **Дополнительные инструменты**.

:::image type="complex" source="../../media/2020/03/settings2.msft.png" alt-text="Главное меню > другие инструменты > параметры" lightbox="../../media/2020/03/settings2.msft.png":::
   Рисунок 3: **главное меню**  >  **Дополнительные**  >  **Параметры** инструментов  
:::image-end:::  

[#1050855][crbug1050855] проблем с Chromium

### Новые и улучшенные infobars

В DevTools теперь есть улучшенные возможности, которые появятся на панелях уведомлений \ (infobars \) на информационной панели. В Microsoft Edge 83 infobars более удобны для чтения и предоставляют кнопки, чтобы можно было принять нужное действие прямо сейчас.  

:::image type="complex" source="../../media/2020/03/infobar.msft.png" alt-text="Информационная панель для печати файла minified в Microsoft Edge 83" lightbox="../../media/2020/03/infobar.msft.png":::
   Рисунок 4: информационная панель для печати файла minified в Microsoft Edge версии 83  
:::image-end:::  

[#1056348][crbug1056348] проблем с Chromium

### Навигация в окне выбора цвета с помощью клавиатуры  

[Палитра цветов][ColorPicker] — это графический интерфейс пользователя на [панели «элементы»][ElementsDoc] для изменения `color` и `background-color` объявлений.  В предыдущих версиях Microsoft Edge вы не смогли перемещаться по разделу " **тени** " в [палитре цветов][ColorPicker] с помощью клавиатуры.  

:::image type="complex" source="../../media/2020/03/color-picker.msft.png" alt-text="Теперь вы можете использовать клавиатуру для перемещения селектора в разделе "тени" палитры цветов" lightbox="../../media/2020/03/color-picker.msft.png":::
   На рисунке 5 показано, как использовать клавиатуру для перемещения селектора в разделе " **тени** " [палитры цветов][ColorPicker]  
:::image-end:::  

В Microsoft Edge 83 теперь можно использовать клавиатуру для перемещения селектора в разделе **тени** окна выбора цвета.  

[#963183][crbug963183] проблем с Chromium  

### Вкладка "Свойства" теперь заполняется после обновления страницы  

В Microsoft Edge 81 и более ранних версий **вкладка Свойства** на [панели элементы][ElementsDoc] была разорвана обновлениями страницы.  После обновления страницы на **вкладке Свойства** не заполнятся свойства элемента, выбранного в данный момент.  

:::image type="complex" source="../../media/2020/03/properties-in-81.msft.png" alt-text="В Microsoft Edge 81 и более ранних версий вкладка Свойства была пуста после обновления страницы" lightbox="../../media/2020/03/properties-in-81.msft.png":::
   Рисунок 6: в Microsoft Edge 81 и более ранних версий **вкладка Свойства** была пуста после обновления страницы  
:::image-end:::  

В Microsoft Edge 83 теперь вы можете видеть свойства элемента, выбранного в данный момент, после обновления страницы на **вкладке Свойства**.  

:::image type="complex" source="../../media/2020/03/properties-in-82.msft.png" alt-text="В Microsoft Edge 83 на вкладке Свойства отображаются свойства элемента, выбранного в данный момент, после обновления страницы." lightbox="../../media/2020/03/properties-in-82.msft.png":::
   Рис. 7: в Microsoft Edge 83 на **вкладке Свойства** отображаются свойства элемента, выбранного в данный момент, после обновления страницы.  
:::image-end:::  

[#1050999][crbug1050999] проблем с Chromium  

### Используйте клавиши со стрелками для прокрутки в инструменте "изменения"  

**Средство "изменения** " отслеживает все изменения, внесенные в CSS или JavaScript, в DevTools.  Вы можете использовать **средство "изменения** ", чтобы быстро просмотреть все изменения и вернуть их в редактор или интегрированную среду разработки.  

Откройте **инструмент "изменения** ", нажав `Ctrl` + `Shift` + `P` в DevTools, чтобы открыть [меню команд][DevToolsCommandMenuIndex] и ввести текст `changes` .  Выберите и запустите команду **Показать изменения** , чтобы открыть **средство "изменения** " в DevToolsном ящике.  

После внесения изменений в файл minified **инструмент "изменения** " позволяет выполнить горизонтальную прокрутку для просмотра всего кода minified.  Начиная с Microsoft Edge 83, теперь можно прокручивать по горизонтали с помощью клавиш со стрелками на клавиатуре.  

:::image type="complex" source="../../media/2020/03/changes.msft.png" alt-text="В Microsoft Edge 83 можно выполнить прокрутку по горизонтали с помощью клавиш со стрелками, чтобы просмотреть код minified в инструменте "изменения"." lightbox="../../media/2020/03/changes.msft.png":::
   Рис. 8: в Microsoft Edge 83 вы можете прокручивать текст по горизонтали с помощью клавиш со стрелками, чтобы просмотреть изменения, внесенные в код minified в **инструменте "изменения** ".  
:::image-end:::  

Если вы используете средства чтения с экрана или клавиатуру для навигации по DevTools, отправьте нам свой отзыв, выполнив [твит][PostTweetEdgeDevTools] в США или щелкнув значок [отзыва](#feedback) .  

[#963183][crbug963183] проблем с Chromium  

## Объявления из проекта Chromium  

В следующих разделах описаны дополнительные возможности, доступные в Microsoft Edge 83, которые были задействованы в проекте Open Source Chromium.  

### Эмуляция видения deficiencies  

Откройте [вкладку рендеринг][RenderingDoc] и воспользуйтесь новой функцией **эмуляции deficiencies** , чтобы лучше понять, как люди с разными типами концепций deficienciesют свой сайт.  

:::image type="complex" source="../../media/2020/03/vision.msft.png" alt-text="Имитация размытого видения" lightbox="../../media/2020/03/vision.msft.png":::
   Рисунок 9: Имитация размытого видения  
:::image-end:::  

DevTools может эмулировать размытое видение и следующие [типы концепций цветопередачи deficiencies][ColorBlindnessTypes].  

| Некоторая концепция цвета | Сведения |  
|:--- |:--- |  
| Protanopia | Невозможность воспринимать красный индикатор. |  
| Deuteranopia | Невозможность воспринимать зеленый свет. |  
| Tritanopia | Невозможность воспринимать любой синий индикатор. |  
| Achromatopsia | Невозможность воспринимать любой цвет, за исключением оттенков серого \ (очень редких). |  

Ниже указаны менее экстремальные версии deficiencies, и в действительности они являются более распространенными.  
Например, Protanomaly — это уменьшенная чувствительность к красному свету (в отличие от Protanopia, что является полноценным невозможностью воспринимать красный свет). Тем не менее, omaly концепция deficiencies не так четко: каждый человек, имеющий такой интерес, отличается от того, кто имеет такой же интерес, и может по-разному видеть различные варианты (которые могут выпустить больше или меньше подходящих цветов).  

Благодаря разработке для более экстремальных эмуляций в DevTools веб-приложения будут гарантированно доступны людям с protanomaly, Deuteranomaly, Tritanomaly и achromatomaly.  

Отправьте свой отзыв с помощью [твитов][PostTweetEdgeDevTools] или щелкните значок [отзыва](#feedback) .  

[#1003700][crbug1003700] проблем с Chromium  

### Эмуляция языков  

Эмуляция региональных стандартов путем задания местоположения в **Sensors**  >  **расположениях**датчиков. [Открыть **меню команд** ][DevToolsCommandMenuIndex] и ввести текст `Sensors` для доступа к вкладке **Sensors (датчики** ).  После выполнения этих действий DevTools изменяет текущий языковой стандарт по умолчанию, влияя на приведенный ниже код.  

*   `Intl.*` API, например: `new Intl.NumberFormat().resolvedOptions().locale`  
*   Другие API JavaScript, поддерживающие национальные настройки `String.prototype.localeCompare` , такие как и `*.prototype.toLocaleString` , например: `123_456..toLocaleString()`  
*   API DOM, например `navigator.language` и `navigator.languages`  
*   [`Accept-Language`][MDNAcceptLanguage]Заголовок HTTP-запроса  

> [!NOTE]
> Обновляются `navigator.language` и `navigator.languages` не отображаются немедленно, но только после следующей перезагрузки или перемещения страницы.  Изменения в `Accept-Language` заголовке HTTP отражаются только для последующих запросов.  

:::image type="complex" source="../../media/2020/03/locale.msft.png" alt-text="Эмуляция языкового стандарта" lightbox="../../media/2020/03/locale.msft.png":::
   Рисунок 10: Эмуляция языкового стандарта  
:::image-end:::  

Чтобы попробовать посмотреть демонстрацию, ознакомьтесь с [примером кода, зависящим от языкового стандарта][MathiasByensLocaleDemo].

[#1051822][crbug1051822] проблем с Chromium

### Отладка политики встраивания по началу (COEP)  

На панели Network (сеть) теперь представлена отладочная информация о [политике встраивания][COEP] .  

Столбец **Status** теперь содержит краткое описание причины блокировки запроса, а также ссылку на просмотр заголовков этого запроса для дальнейшей отладки.  

:::image type="complex" source="../../media/2020/03/status.msft.png" alt-text="Заблокированные запросы в столбце * * Состояние * *" lightbox="../../media/2020/03/status.msft.png":::
   Рисунок 11: заблокированные запросы в столбце "состояние"  
:::image-end:::  

В разделе **заголовки ответа** вкладки **заголовки** содержатся дополнительные инструкции по устранению проблем.  

:::image type="complex" source="../../media/2020/03/guidance.msft.png" alt-text="Другие рекомендации в разделе "заголовки ответа"" lightbox="../../media/2020/03/guidance.msft.png":::
   Рисунок 12: дополнительные рекомендации в разделе заголовки ответа  
:::image-end:::  

Отправьте свой отзыв с помощью [твитов][PostTweetEdgeDevTools] или щелкните значок [отзыва](#feedback) .  

[#1051466][crbug1051466] проблем с Chromium  

### Просмотр сетевых запросов, заданных для определенного пути к файлу cookie  

С помощью нового `cookie-path` ключевого слова фильтра на панели **Network (сеть** ) можно сосредоточиться на запросах в сети, которые задают определенный [путь к файлу cookie][MDNCookiePath].  

Изучите [запросы фильтра по свойствам][NetworkProperties] , чтобы найти другие ключевые слова, такие как `cookie-path` .

### Закрепить слева от меню команд  

Откройте [меню команд][DevToolsCommandMenuIndex] и выполните команду, `Dock to left` чтобы переместить DevTools в левой части окна просмотра.  

:::image type="complex" source="../../media/2020/03/dock-to-left.msft.png" alt-text="DevTools закреплен в левой части окна просмотра" lightbox="../../media/2020/03/dock-to-left.msft.png":::
   Рисунок 13: DevTools закреплен в левой части окна просмотра  
:::image-end:::  

> [!NOTE]
> Функция " **прикрепить к левому краю** " была доступна после выпуска Microsoft Edge 75, но ранее она была доступна только в [**главном меню**][MainMenuDoc].  Новая функция в Microsoft Edge 83 — теперь вы можете получить доступ к этой функции в меню команд.  

Отправьте свой отзыв с помощью [твитов][PostTweetEdgeDevTools] или щелкните значок [отзыва](#feedback) .  

[#1011679][crbug1011679] проблем с Chromium  

### Панель "Аудит" теперь является панелью Lighthouse  

Группа DevTools часто получила отзыв от веб-разработчиков, которые могли бы запустить [Lighthouse][GithubGoogleChromeLighthouse] из DevTools, когда они могли бы не найти панель "Lighthouse", и панель **аудиторий** стала на панели " **Lighthouse** ".  

:::image type="complex" source="../../media/2020/03/lighthouse.msft.png" alt-text="Панель Lighthouse" lightbox="../../media/2020/03/lighthouse.msft.png":::
   Рисунок 14: панель Lighthouse  
:::image-end:::  

> [!NOTE]
> Панель **Lighthouse** содержит ссылки на содержимое, размещенное на сторонних веб-сайтах.  Корпорация Майкрософт не несет ответственности за содержимое этих сайтов и любые данные, которые могут быть собраны, и не может управлять ими.  

### Удаление всех локальных переопределений в папке  

После настройки **локальных переопределений** вы можете щелкнуть папку правой кнопкой мыши и выбрать команду создать **все переопределение** для удаления всех локальных переопределений в этой папке.  

:::image type="complex" source="../../media/2020/03/overrides.msft.png" alt-text="Удаление всех переопределений" lightbox="../../media/2020/03/overrides.msft.png":::
   Рисунок 15: удаление всех переопределений  
:::image-end:::  

Отправьте свой отзыв с помощью [твитов][PostTweetEdgeDevTools] или щелкните значок [отзыва](#feedback) .  

[#1016501][crbug1016501] проблем с Chromium  

### Обновленный пользовательский интерфейс длительных задач  

**Длинная задача** — это код JavaScript, который занимает много времени, что приводит к закреплениям веб-страницы.  

На панели производительности вы можете [визуализировать длинные задачи][LongTasksInPerformancePanel] , но в Microsoft Edge 83 пользовательский интерфейс визуализации задач на панели производительности обновлен.  Область задач "Долгая задача" теперь окрашена на красный фон с чередованием.  

:::image type="complex" source="../../media/2020/03/long-task.msft.png" alt-text="Новый пользовательский интерфейс длительной задачи" lightbox="../../media/2020/03/long-task.msft.png":::
   Рисунок 16: новый пользовательский интерфейс длительной задачи  
:::image-end:::  

Отправьте свой отзыв с помощью [твитов][PostTweetEdgeDevTools] или щелкните значок [отзыва](#feedback) .  

[#1054447][crbug1054447] проблем с Chromium  

### Поддержка маскированных значков в области манифеста  

В Oreo Android появились адаптивные значки, которые отображают значки приложений в различных моделях устройств.  **Маскированные значки** — это новый формат значков, поддерживающий адаптивные значки, которые позволяют убедиться, что на устройствах, поддерживающих стандарт маскированных значков, будет хорошо выглядеть значок [PWA][PWADoc] .  

Установите флажок **Показывать только минимальную безопасную область для маскированных значков** в области **манифеста** , чтобы убедиться в том, что маскирующий значок хорошо подходит для устройств с Android Oreo.  

<!-- Check out [Are my current icons ready?] to learn more.  -->  

:::image type="complex" source="../../media/2020/03/maskable-icons.msft.png" alt-text="Флажок Показать только минимальную безопасную область для маскированных значков" lightbox="../../media/2020/03/maskable-icons.msft.png":::
   Рисунок 17: флажок **Показать только минимальную безопасную область для маскированных значков**  
:::image-end:::  

> [!NOTE]
> Этот компонент запущен в Microsoft Edge 81.  Обновления, описанные здесь в Microsoft Edge 83, не были освещены в статье [новые возможности DevTools (Microsoft Edge 81)][WhatsNew81].  

## Отзыв  

Чтобы обсудить новые возможности и изменения в этой записи, а также другие связанные с DevTools, выполните указанные ниже действия.  

*   Отправка отзыва с помощью значка **обратной связи** в DevTools  
*   Твит на [@EdgeDevTools][PostTweetEdgeDevTools]  
*   Отправка предложения в [Вебе][TheWebWeWant]  
*   Ошибки файла в этом документе в репозитории " [Edge — разработчик][GitHubMicrosoftDocsEdgeDeveloperNewIssue] "  

:::image type="complex" source="../../media/2020/03/feedback-icon.msft.png" alt-text="Значок * * Feedback * * в Microsoft Edge DevTools" lightbox="../../media/2020/03/feedback-icon.msft.png":::
   Рисунок 18: значок **обратной связи** в Microsoft Edge DevTools  
:::image-end:::  

## Загрузка каналов предварительной версии Microsoft Edge  

Если вы используете Windows или macOS, рассматривайте в качестве браузера по умолчанию использование [каналов предварительного просмотра Microsoft Edge][MicrosoftEdgePreviewChannels] .  Каналы предварительного просмотра предоставляют доступ к последним функциям DevTools.  

<!-- links -->  

[PostTweetEdgeDevTools]: https://aka.ms/tweet/edgedevtools "@EdgeDevTools | Публикация твита"  
[EdgeDevToolsTwitterAccount]: https://aka.ms/twitter/edgedevtools "@EdgeDevTools учетной записи Twitter"  
[GitHubMicrosoftDocsEdgeDeveloperNewIssue]: https://aka.ms/edgedevtoolsdocs/feedback "Новая ошибка — MicrosoftDocs/Edge-разработчик"  
[MicrosoftEdgePreviewChannels]: https://aka.ms/microsoftedge "Каналы предварительной версии Microsoft Edge"  
[TheWebWeWant]: https://aka.ms/webwewant "Требуемый веб-сайт"  

[WhatsNew81]: /microsoft-edge/devtools-guide-chromium/whats-new/2020/01/devtools "Новые возможности DevTools (Microsoft Edge 81)"  

[DevToolsCommandMenuIndex]: /microsoft-edge/devtools-guide-chromium/command-menu/index "Выполнение команд с помощью командного меню Microsoft Edge DevTools"  
[ColorPicker]: /microsoft-edge/devtools-guide-chromium/css/reference#change-colors-with-the-color-picker "Изменение цвета с помощью палитры цветов"  
[ElementsDoc]: /microsoft-edge/devtools-guide-chromium/css/index "Приступая к просмотру и изменению каскадных таблиц стилей"  
[MainMenuDoc]: /microsoft-edge/devtools-guide-chromium/customize/placement#change-placement-from-the-main-menu "Изменение положения в главном меню"  
[LongTasksInPerformancePanel]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#view-main-thread-activity "Просмотр основного действия потока"  
[RenderingDoc]: /microsoft-edge/devtools-guide-chromium/evaluate-performance/reference#analyze-rendering-performance-with-the-rendering-tab "Анализ производительности отрисовки с помощью вкладки "рендеринг""  
[PWADoc]: /microsoft-edge/progressive-web-apps-chromium/index "Прогрессивные веб-приложения для Windows"  
[RemoteDebuggingWin10]: /microsoft-edge/devtools-guide-chromium/remote-debugging/windows "Начало работы с удаленной отладкой устройств с Windows 10"  
[LineOfCodeBreakpoints]: /microsoft-edge/devtools-guide-chromium/javascript/breakpoints#line-of-code-breakpoints "Точки останова в коде строки"
[NetworkProperties]: /microsoft-edge/devtools-guide-chromium/network/reference#filter-requests-by-properties
[OverviewSettings]: /microsoft-edge/devtools-guide-chromium/customize/#settings

[WindowsDevicePortal]: /windows/uwp/debug-test-perf/device-portal "Общие сведения о портале устройств Windows"  

[RemoteTools]: https://www.microsoft.com/store/apps/9P6CMFV44ZLT "Удаленные инструменты для Microsoft EDGE (бета-версия)"  
[MicrosoftStore]: https://www.microsoft.com/store/apps/windows "Microsoft Store"  
[WindowsBlogStableRelease]: https://blogs.windows.com/msedgedev/2020/03/20/update-stable-channel-releases/ "Обновление в стабильных выпусках канала для Microsoft Edge"

[ColorBlindnessTypes]: http://www.colourblindawareness.org/colour-blindness/types-of-colour-blindness/ "Типы цветовой жалюзи"  
[MDNAcceptLanguage]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Accept-Language "Одобрение и язык"
[MathiasByensLocaleDemo]: https://mathiasbynens.be/demo/locale "Пример кода, зависящий от языкового стандарта"
[MDNCookiePath]: https://developer.mozilla.org/docs/Web/HTTP/Headers/Set-Cookie#Directives

[crbug963183]: https://crbug.com/963183 "Ошибка 963183: DevTools не соответствует требованиям WCAG"  
[crbug1003700]: https://crbug.com/1003700 "Вопрос 1003700: Добавление поддержки DevTools в целях моделирования недостатков для представления цвета"  
[crbug1011679]: https://crbug.com/1011679 "Ошибка 1011679: ввод "закрепить влево" с помощью меню команд"  
[crbug1016501]: https://crbug.com/1016501 "Ошибка 1016501: запрос компонента: кнопка для удаления всех локальных переопределений"  
[crbug1050999]: https://crbug.com/1050999 "Ошибка 1050999: вкладка "Свойства""  
[crbug1051466]: https://crbug.com/1051466 "Ошибка 1051466: поддержка отладки COOP/COEP в DevTools"  
[crbug1054447]: https://crbug.com/1054447 "Ошибка 1054447: обновление метрик производительности на временной шкале DevTools"  
[crbug1051822]: https://crbug.com/1051822 "Ошибка 1051822: DevTools: Добавление пользовательского интерфейса для эмуляции национальной настройки"
[crbug1041830]: https://crbug.com/1041830 "Ошибка 1041830: улучшение цветопередачи для точек останова"
[crbug1050855]: https://crbug.com/1050855 "Неполадка 1050855: Просмотр параметров затрудняет обнаружение"
[crbug1056348]: https://crbug.com/1056348 "Ошибка 1056348: обновление компонента на информационной панели"

[COOP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.tu4hyy6v12wn "Описание COOP и COEP — политика opener для разных источников"  
[COEP]: https://docs.google.com/document/d/1zDlfvfTJ_9e8Jdc8ehuV4zMEu9ySMCiTGMS9y0GU92k/edit#bookmark=id.uo6kivyh0ge2 "Объяснение COOP и COEP — политика для внедрения разных источников"  

[GithubGoogleChromeLighthouse]: https://github.com/GoogleChrome/lighthouse "Репозиторий GitHub Lighthouse"  

> [!NOTE]
> Части этой страницы представляют собой изменения, основанные на работе, созданной и [предоставленной компанией Google][GoogleSitePolicies] и использованными в соответствии с условиями, описанными в [лицензии Creative Commons 4,0 международная лицензия][CCA4IL].  
> Исходная страница будет найдена [здесь](https://developers.google.com/web/updates/2020/03/devtools/index) и была написана с помощью [Kayce Basques][KayceBasques] \ (технический писатель, Chrome DevTools \ & Lighthouse \).  

[![Лицензия Creative Commons][CCby4Image]][CCA4IL]  
Эта работа предоставляется в рамках международной лицензии [Creative Commons Attribution 4.0 International License][CCA4IL].  

[CCA4IL]: https://creativecommons.org/licenses/by/4.0  
[CCby4Image]: https://i.creativecommons.org/l/by/4.0/88x31.png  
[GoogleSitePolicies]: https://developers.google.com/terms/site-policies  
[KayceBasques]: https://developers.google.com/web/resources/contributors/kaycebasques  
