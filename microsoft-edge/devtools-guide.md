---
description: Знакомство со средствами разработчика Microsoft EDGE (EdgeHTML)
title: Инструменты разработчика Microsoft EDGE (EdgeHTML)
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 05/05/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: devtools
keywords: Microsoft EDGE, веб-разработка, инструменты для F12, Devtools
experimental: true
experiment_id: 51fe4b97-3e55-41
localization_priority: Priority
ms.openlocfilehash: 56edfa3aa39fc20d37d95fb8fde029a702732336
ms.sourcegitcommit: 985cfb79a64951afd5beb7981b26afbed30a8972
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/07/2020
ms.locfileid: "10629506"
---
# Инструменты разработчика Microsoft EDGE (EdgeHTML)  

[!INCLUDE [new-devtools-version-note](includes/new-devtools-version-note.md)]  

DevTools Microsoft Edge \ (EdgeHTML \) создаются с помощью [TypeScript][|::ref1::|Index], на платформе [Open Source][GithubMicrosoftChakracore], оптимизированных для современных серверных рабочих процессов, и теперь доступно как [автономное приложение для Windows 10][MicrosoftStoreEdgeDevtoolsPreview] в Microsoft Store.  

Чтобы узнать больше о последних возможностях, ознакомьтесь с [DevTools в последнем обновлении Windows 10 (EdgeHTML 18)][DevtoolsGuideEdgehtmlWhatsnew].  

## Основные инструменты  

:::image type="complex" source="./devtools-guide/media/devtools.png" alt-text="Microsoft EDGE (EdgeHTML) DevTools":::
   Microsoft EDGE (EdgeHTML) DevTools
:::image-end:::

<!--![Microsoft Edge \(EdgeHTML\) DevTools][ImageDevtoolsEdgehtml]  -->  

Microsoft Edge \ (EdgeHTML \) DevTools включает следующие возможности:  

*   Панель " [элементы][DevtoolsGuideEdgehtml|::ref2::|] " для редактирования HTML и CSS, проверки свойств специальных возможностей, просмотра прослушивателей событий и установки контрольных точек изменений DOM  
*   [Консоль][DevtoolsGuideEdgehtml|::ref3::|] для просмотра и фильтрации сообщений журнала, проверки объектов JavaScript и узлов DOM, а также выполнения JavaScript в контексте выбранного окна или фрейма  
*   [Отладчик][DevtoolsGuideEdgehtml|::ref4::|] для пошагового использования кода, задания контрольных значений и точек останова, редактирование кода в реальном времени, проверка веб-хранилища и кэша файлов cookie.  
*   Панель [сети][DevtoolsGuideEdgehtml|::ref5::|] для мониторинга и проверки запросов и ответов из кэша сети и браузера  
*   Панель [производительности][DevtoolsGuideEdgehtml|::ref6::|] для профилирования времени и системных ресурсов, необходимых для вашего сайта  
*   Панель [памяти][DevtoolsGuideEdgehtml|::ref7::|] для измерения использования ресурсов памяти и сравнения снимков кучи в разных состояниях среды выполнения кода  
*   Панель [хранилища][DevtoolsGuideEdgehtml|::ref8::|] для проверки и управления веб-хранилищем, IndexedDB, cookies и данными кэша  
*   Панель " [сотрудники службы][DevtoolsGuideEdgehtmlServiceworkers] " для управления и отладки сотрудников службы  
*   Панель [эмуляции][DevtoolsGuideEdgehtml|::ref9::|] для проверки сайта с различными профилями браузера, разрешениями экрана и координатами местоположения GPS  

Отправляйте [Отзывы и запросы функций](#feedback)!  

> [!TIP]
> [Тестирование в Microsoft Edge \ (EdgeHTML \) бесплатно из любого браузера][BrowserstackEdgehtml].  
> Группа Microsoft EDGE, сопоставленная с [BrowserStack][BrowserstackEdgehtml] , для предоставления бесплатных и автоматизированных тестов в Microsoft Edge \ (EdgeHTML \).  

## Приложение Microsoft Store  

**DevTools Microsoft Edge \ (EdgeHTML \)** [теперь доступны][DevtoolsGuideEdgehtmlWhatsnew] в виде автономного [приложения для Windows 10 из Microsoft Store][MicrosoftStoreEdgeDevtoolsPreview], а также с помощью инструментов "в браузере" и " `F12` \".  В версии магазина есть панель **выбора** для присоединения к конечным объектам Open local и Remote Page, а также макет с вкладками для быстрого переключения между экземплярами DevTools.  

### Локальная отладка  

Чтобы выполнить отладку страницы локально, просто запустите приложение Microsoft Edge DevTools.  На **локальной** панели средства выбора отображаются все активные процессы содержимого EdgeHTML, включая открытые вкладки браузера EDGE, запуск [PWAs][PwasEdgehtmlIndex] \ ( `WWAHost.exe` процессы \) и [WebView][HostingWebview] элементов управления.  Выберите требуемый целевой объект, чтобы прикрепить и открыть новый экземпляр вкладки DevTools.  

:::image type="complex" source="./devtools-guide/media/chooser_local.png" alt-text="Локальная панель приложения DevTools":::
   Локальная панель приложения DevTools
:::image-end:::

<!--![DevTools app Local panel][ImageDevtoolsGuideEdgehtmlChooselocal]  -->  

### Удаленная отладка  

Приложение Microsoft Edge DevTools предоставляет базовую поддержку для отладки страниц на удаленном компьютере с помощью нового [протокола DevTools][DevtoolsProtocolEdgehtmlIndex].  В последнем выпуске есть удаленный доступ к основным функциям в [отладчике][DevtoolsGuideEdgehtml|::ref10::|], [элементах][DevtoolsGuideEdgehtml|::ref11::|] \ (для операций только для чтения, а также на панелях [консоли][DevtoolsGuideEdgehtml|::ref12::|] ).  Удаленная отладка ограничена Microsoft EDGE (EdgeHTML \) на компьютерах, работающих под управлением классических приложений, и поддерживает другие узлы EdgeHTML и устройства с Windows 10, которые появятся в будущих выпусках.  

Чтобы приступить к работе, ознакомьтесь с разделом [*Microsoft Edge DevTools*][DevtoolsProtocolEdgehtmlClientsEdgePreview] в документах [протоколов DevTools][DevtoolsProtocolEdgehtmlIndex] .  

:::image type="complex" source="./devtools-guide/media/chooser_remote.png" alt-text="Удаленная панель приложения DevTools":::
   Удаленная панель приложения DevTools
:::image-end:::

<!--![DevTools app Remote panel][ImageDevtoolsGuideEdgehtmlRemote]  -->  

## Общие сочетания клавиш  

> [!IMPORTANT]
> Все сочетания клавиш были проверены в последней версии Windows.  
> Если вы не можете использовать ярлык, обновите свою копию Windows.  

Эти сочетания клавиш управляют основным окном DevTools и должны работать во всех средствах.  

| Действие | Появивше |  
|:--- |:--- |  
| Показать или скрыть DevTools \ (открывается в последней просмотренной панели \) | `F12`, `Ctrl`+`Shift`+`I` |  
| Переключить закрепление \ (открепить/снизу или справа \) | `Ctrl`+`Shift`+`D` |  
| Открыть файл | `Ctrl`+`P`, `Ctrl`+`O` |  
| Отображение нередактируемого исходного кода HTML в отладчике | `Ctrl`+`U` |  
| Отображение и скрытие консоли в нижней части любого другого инструмента  | `Ctrl`+`` ` `` |  
| Переключение на элементы \ (проводник DOM \) | `Ctrl`+`1` |  
| Переключиться на консоль |  `Ctrl`+`2` |  
| Переход в режим отладчика | `Ctrl`+`3` |  
| Переключиться в сеть | `Ctrl`+`4` |  
| Переключение на производительность | `Ctrl`+`5` |  
| Переход в память | `Ctrl`+`6` |  
| Переключение на эмуляцию | `Ctrl`+`7` |  
| Справочный документ | `F1` |  
| Следующий инструмент | `Ctrl`+`F6` |  
| Предыдущее средство | `Ctrl`+`Shift`+`F6` |  
| Предыдущее средство \ (из истории) | `Ctrl`+`Shift`+`[` |  
| Следующий инструмент \ (из истории) | `Ctrl`+`Shift`+`]` |  
| Следующий подкадровый | `F6` |  
| Предыдущий подкадровый | `Shift`+`F6` |  
| Следующее совпадение в поле поиска | `F3` |  
| Предыдущее совпадение в поле поиска | `Shift`+`F3` |  
| Поиск в поле поиска | `Ctrl`+`F` |  
| Перемещение фокуса на консоль в нижней части экрана | `Alt`+`Shift`+`I` |  
| Запустить DevTools на консоли | `Ctrl`+`Shift`+`J` |  
| Обновить страницу | `Ctrl`+`Shift`+`F5`, `Ctrl`+`R` |  

> [!NOTE]
> При отладке и приостановке в точке останова, при **обновлении действия страницы** сначала возобновляется среда выполнения.  

## Отзыв  

Пожалуйста, отправьте свой отзыв, чтобы помочь вам улучшить Microsoft Edge \ (EdgeHTML \) DevTools!  Просто откройте инструменты \ ( `F12` \) и нажмите кнопку [Отправить отзыв](#microsoft-edge-edgehtml-developer-tools) .  

Станьте участником программы [предварительной оценки Windows][WindowsInsiderProgram] , чтобы ознакомиться с [новейшими возможностями, выпущенными в DevTools][DevtoolsGuideEdgehtmlWhatsnew].  Используйте приложение центра обратной связи Windows для публикации, отправки по голосованию, отслеживания и получения поддержки общих вариантов и проблем с Windows.  

<!-- image links  -->  

<!--[ImageDevtoolsEdgehtml]: /microsoft-edge/devtools-guide/media/devtools.png "Microsoft Edge (EdgeHTML) DevTools"  -->  
<!--[ImageDevtoolsGuideEdgehtmlChooselocal]: /microsoft-edge/devtools-guide/media/chooser_local.png "DevTools app Local panel"  -->  
<!--[ImageDevtoolsGuideEdgehtmlRemote]: /microsoft-edge/devtools-guide/media/chooser_remote.png "DevTools app Remote panel"  -->  

<!-- links  -->  

[DevtoolsGuideEdgehtmlConsole]: /microsoft-edge/devtools-guide/console "Консоли"  
[DevtoolsGuideEdgehtmlDebugger]: /microsoft-edge/devtools-guide/debugger "Отладчика"  
[DevtoolsGuideEdgehtmlElements]: /microsoft-edge/devtools-guide/elements "Element"  
[DevtoolsGuideEdgehtmlEmulation]: /microsoft-edge/devtools-guide/emulation "Эмуляции"  
[DevtoolsGuideEdgehtmlMemory]: /microsoft-edge/devtools-guide/memory "Хватки"  
[DevtoolsGuideEdgehtmlNetwork]: /microsoft-edge/devtools-guide/network "Сетью"  
[DevtoolsGuideEdgehtmlPerformance]: /microsoft-edge/devtools-guide/performance "Эффективности"  
[DevtoolsGuideEdgehtmlServiceworkers]: /microsoft-edge/devtools-guide/service-workers "Обслуживание сотрудников"  
[DevtoolsGuideEdgehtmlStorage]: /microsoft-edge/devtools-guide/storage "Склад"  
[DevtoolsGuideEdgehtmlWhatsnew]: /microsoft-edge/devtools-guide/whats-new "DevTools в новейшем обновлении для Windows 10 (EdgeHTML 18)"  
[DevtoolsProtocolEdgehtmlIndex]: /microsoft-edge/devtools-protocol/index "Протокол DevTools Microsoft EDGE (EdgeHTML)"  
[DevtoolsProtocolEdgehtmlClientsEdgePreview]: /microsoft-edge/devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Клиенты Microsoft Edge DevTools Preview-DevTools Protocol"  
[HostingWebview]: /microsoft-edge/hosting/webview "WebView (EdgeHTML) для приложений для Windows 10"  
[PwasEdgehtmlIndex]: /microsoft-edge/progressive-web-apps-edgehtml/index "Прогрессивные веб-приложения (EdgeHTML) в Windows"  

[MicrosoftStoreEdgeDevtoolsPreview]: https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj "Предварительная версия DevTools Microsoft Edge"  

[WindowsInsiderProgram]: https://insider.windows.com "Программа предварительной оценки Windows"  

[BrowserstackEdgehtml]: https://www.browserstack.com/test-on-microsoft-edge-browser "Браузер Microsoft Edge — бесплатное тестирование | BrowserStack"  

[GithubMicrosoftChakracore]: https://github.com/Microsoft/ChakraCore "Microsoft/ChakraCore | GitHub"  

[TypeScriptIndex]: https://www.typescriptlang.org "TypeScript"  
