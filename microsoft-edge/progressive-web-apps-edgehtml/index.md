---
description: Прогрессивные веб-приложения работают с родными в Windows 10.  Вот все, что вам нужно знать как веб-разработчик.
title: Прогрессивные веб-приложения (EdgeHTML) в Windows
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 02/28/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: pwa
keywords: прогрессивные веб-приложения, PWA, EDGE, JavaScript, Windows, UWP, Microsoft Store
ms.openlocfilehash: 778502f6db9a89da810b4fb59b10e8fb889fa4b5
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10570848"
---
# Прогрессивные веб-приложения (EdgeHTML) в Windows  

С помощью [последовательного веб-приложения][MDNApps] \ (или просто PWAs \) вам не нужно определять использование открытых веб-технологий для взаимодействия между платформами и предоставление пользователям собственного приложения, такого как приложение, настроенное для их устройства.  Это связано с тем, что PWAs — это только веб-сайты, которые являются [последовательно расширенными][AListApartUnderstandingProgressiveEnhancement] для работы в соответствии с собственными приложениями на платформе поддержки.  В приложениях PWA объединены лучшие качестве веб- и собственных приложения.  

:::row:::
    :::column:::
        ![Значок с возможностью обнаружения][ImageISearch]
        ### [Обнаруживаемым][MDNPwaAdvantagesDiscoverable]
        Из результатов поиска в Интернете и поддержки магазинов приложений
    :::column-end:::
    :::column:::
        ![Устанавливаемый значок][ImageIPackage]
        ### [Устанавливаемый][MDNPwaAdvantagesInstallable]
        Закрепление и запуск на начальном экране  
    :::column-end:::
    :::column:::
        ![Значок повторного запуска][ImageIPushNotification]
        ### [Повторное участие][MDNPwaAdvantagesReEngageable]
        Отправлять push-уведомления, даже если приложение неактивно  
    :::column-end:::
    :::column:::
        ![Значок, не зависящий от сети][ImageIOffline]
        ### [Сетевая независимость][MDNPwaAdvantagesNetworkIndependent]
        Работа в автономном режиме и в условиях низкой сети  
    :::column-end:::
:::row-end:::
:::row:::
    :::column:::
        ![Значок прогрессивной развертки][ImageIProgressive]
        ### [JPEG][MDNPwaAdvantagesProgressive]
        Возможности устройств в масштабах  
    :::column-end:::
    :::column:::
        ![Значок "безопасный"][ImageISecurity]
        ### [Безопасной][MDNPwaAdvantagesSafe]
        Обеспечивает защищенную конечную точку HTTPS и другие меры для защиты от пользователей  
    :::column-end:::
    :::column:::
        ![Значок отклика][ImageIResponsive]
        ### [Хорошая скорость отклика][MDNPwaAdvantagesResponsive]
        Адаптируется к размеру экрана, ориентации и методу ввода для пользователя  
    :::column-end:::
    :::column:::
        ![Значок ссылки][ImageILink]
        ### [Связь][MDNPwaAdvantagesLinkable]
        Предоставление общего доступа к файлу и его запуск с помощью стандартной гиперссылки  
    :::column-end:::
:::row-end:::

Создав или преобразуя существующий веб-сайт в PWA, вы сможете лучше привлекать существующую аудиторию с помощью push-уведомлений и поддержки автономной работы.  В то же время вы можете продолжить создание аудиторий в открытом веб-браузере, так как пользователи будут находить его с помощью поиска и совместного использования ссылок.  

## PWAs в Windows 10 (EdgeHTML)  

> [!NOTE]
> При переходе на Microsoft EDGE (Chromium) из EdgeHTML базовые веб-платформы, используемые PWAs, не совпадают.  Ребро (Chromium) PWAs устанавливаются из браузера и выполняются в нем.  EDGE (EdgeHTML) PWAs работает как приложение универсальной платформы Windows (UWP) и использует старую веб-платформу EdgeHTML.  Если вам нужен доступ к Windows 10 API для PWA, это EdgeHTML документация.  Если ваша цель — поддержка на разных платформах без доступа к API для Windows, обратитесь к [документации по PWA Microsoft EDGE (Chromium)][PwaChromiumIndex].  

Если вы создаете последовательное веб-приложение, чтобы использовать преимущества Windows 10, вы можете распространить его с помощью [Microsoft Store][MicrosoftDeveloperStore], всего одной версии Windows 10, которая составляет 600 и миллион активных пользователей, является потенциальная аудитория приложения.  Приложения, разработанные таким образом, выполняются как приложения [универсальной платформы Windows][WindowsUWPGetStartedGuide] и имеют собственный код, например доступ к API-интерфейсам WinRT.  Обратите внимание на то, что при использовании API-интерфейсов WinRT EdgeHTML используется обнаружение компонентов, поэтому для обеспечения возможности работы PWA между платформами, в которых доступны приложения Microsoft Edge \ (Chromium \), можно использовать функцию обнаружения.  

[Ниже показано, как приступить][PwaEdgehtmlGetStarted] к преобразованию веб-приложения в PWA \ (EdgeHTML \), тестированию его в Windows 10 и распространению в Microsoft Store.  

## Требования  

Для работы в качестве PWA для серверного веб-приложения минимальным требованием должно быть:  

*   [X] [HTTPS][WikiHttps].  Защитите своих пользователей, обеспечив надежную связь между сервером и приложением.  Сотрудники служб и другие технологии PWA работают только с веб-ресурсами, обслуживаемыми в безопасном соединении (или в `localhost` целях отладки).  
  
*   [X] [сотрудников служб][MDNServiceWorkerApi].  Используйте рабочие потоки служб, чтобы выступать в качестве сетевых прокси между сервером и клиентским приложением, чтобы обеспечить поддержку в автономном режиме, кэшировании ресурсов, push-уведомлениях, фоновой синхронизации данных и оптимизации производительности загрузки страниц.  

*   [X] [Манифест веб-приложения][MDNWebAppManifest].  Предоставьте файл метаданных на основе JSON, описывающий ключевые сведения о вашем веб-приложении (например, значки, язык и точку входа URL \), чтобы Windows 10 и другие серверные платформы могли предоставлять пользователям PWA доступ к устанавливаемому исходному приложению.  Связывание сайта с манифестом веб-приложения делает его доступным для [автоматического включения в Microsoft Store][PwaEdgehtmlMicrosoftStoreImportingBing] с помощью службы индексирования Bing.  

Для того чтобы стать прекрасным PWA, вашему приложению также нужны:  

*   [X] [Совместимость с различными браузерами][MDNCrossBrowserTesting].  Убедитесь, что веб-приложение PWA [работает в разных][MicrosoftDeveloperEdgeToolsRemote] браузерах и средах.  В Windows 10 обязательно протестируйте свое приложение как в браузере Microsoft EDGE, так и в полном интерфейсе PWA: как установленное автономное приложение для Windows 10 (на базе ядра EdgeHTML).  
  
*   [X] для [быстрого проектирования][WikiResponsiveWebDesign].  Использование жидкостных макетов и гибких изображений с помощью [сетки][MDNCssGridLayout] каскадных стилей и [/или][MDNCssFlexibleBoxLayout]подаппарата, [запросов мультимедиа][MDNMediaQueries]и [[MDNResponsiveImagesных] изображений для адаптации вашего UX к устройству пользователя.  Используйте [средства эмуляции][DevToolsGuide|::ref1::|] устройства в браузере для проверки на локальном компьютере или настройте [сеанс удаленной отладки][DevToolsProtocolClientsEdgeDevToolsPreview] для проверки непосредственно на целевом устройстве.  В Windows 10 PWAs \ (EdgeHTML \) могут быть также [адаптированы для форм-факторов][WindowsUWPDesignDevicesIndex] за пределами настольных устройств, телефонов и планшетов, в том числе с помощью [Xbox и телевизора][WindowsUWPDesignDevicesDesigningTv], [Surface Hub][MicrosoftDeveloperWindowsSurfaceHub]и устройства [Windows Mixed Reality][MicrosoftDeveloperWindowsMixedReality] .  
  
*   [X] [глубокая компоновка][WikiDeepLinking].  Перенаправление каждой страницы сайта на уникальный URL-адрес, чтобы пользователи могли пользоваться более широкой аудиторией через функцию совместного использования социальных сетей.  

*   [ [X] рекомендации][Webhint].  Используйте средства качества кода, такие как Linter веб – [Подсказка][Webhint] , чтобы оптимизировать эффективность, надежность, безопасность и доступность вашего приложения.  

Чтобы отправить последовательное веб-приложение в [Microsoft Store][MicrosoftDeveloperStore], необходимо:  

*   [X] [учетная запись разработчика Microsoft][WindowsUWPPublishDeveloperAccount]  
*   [X] завершены [шаги для публикации приложения для Windows][WindowsUWPPublishIndex]  

В течение ближайших месяцев существующие PWAs на веб-собраниях с [определенными критериями][PwaEdgehtmlMicrosoftStoreCriteriaAutomaticSubmission] автоматически индексируются с помощью поисковой системы Bing в Microsoft Store \ (там, где разработчики могут напрямую управлять аудиторией Windows 10).  

Для получения дополнительных сведений ознакомьтесь со статьей [PWAs (EdgeHTML) в Microsoft Store][PwaEdgehtmlMicrosoftStore] .  

## Текущая доступность  

Поддержка обработчиком прогрессивных веб-приложений для обработки некоторых архитектурных компонентов, наиболее значительная часть инфраструктуры сети, предоставляемой [API выборки][MDNFetchApi].  Поддержка PWA в ядре EdgeHTML завершена в выпуске Windows 10 1809.  Улучшенные веб-стандарты, так как это время не будет включено в обработчик EdgeHTML, поэтому не забудьте выполнить тесты совместимости и использовать обнаружение компонентов для корректной резервной стратегии: функция, которая нужна для PWA на платформе EdgeHTML, не поддерживается.  

Для предстоящего выпуска Microsoft Edge \ (Chromium \) в 2020 платформа браузера имеет полную поддержку этих функций, которые работают на разных устройствах, поддерживающих браузер Chromium.  

Ниже приведены сведения о текущем состоянии стандартных технологий PWA для EdgeHTML и Windows.  

| Технология | Описание | Доступность | Примечания по использованию |  
|:--- |:--- |:--- |:--- |  
| [Манифест веб-приложения][MDNWebAppManifest] | Предоставляет метаданные приложения для операционной системы, позволяющей включать повышение для установки и магазина приложений.  Требуется для PWAs в Microsoft Store.  | [В разработке][MicrosoftDeveloperEdgePlatformStatusWebApplicationManifest] | Сейчас вы можете использовать [конструктор PWA][|::ref2::|] для создания манифеста JSON, совместимого с W3C, и упаковки приложения для различных платформ ОС.  В Windows конструктор PWA преобразует манифест JSON в `.appxmanifest` Формат \ (XML \), необходимый для приложений Windows 10.  |  
| [API выборки][MDNFetchApi] | Обеспечивает асинхронную сетевую обработку запросов \ (запросы, ответы) для ресурсов страницы |[EdgeHTML 14 + +][DevGuideWhatsNewEdgeHtml14] сборки 14393 + | Синтаксис [API рабочего процесса службы][MDNServiceWorkerApi] основан на API-интерфейсах, использующих выборку данных.  Вы также можете использовать [API FETCH][MDNFetchApi] больше, чем в современной альтернативы `XMLHttpRequest` .  |  
| [API рабочего процесса службы][MDNServiceWorkerApi] | Предоставляет автономно доступную модель веб-приложения или сетевой прокси, в которой сценарии, управляемые событиями, выполняются независимо от веб-страниц.  | [EdgeHTML17][DevGuideWhatsNewEdgeHtml17] /Build 17133 + | Экспериментальная поддержка \ (за `Enable Service Workers` пометкой) в EdgeHTML 16.  По умолчанию в EdgeHTML 17 + сборках.  |  
| [API кэша][MDNCache] | Предоставляет механизм хранения для пар сетевого запроса/ответа | [EdgeHTML17][DevGuideWhatsNewEdgeHtml17] /Build 17133 + | Ознакомьтесь с разделом [API рабочего процесса службы][MDNServiceWorkerApi] выше.  |  
| [API push-уведомлений][MDNPushApi] | Позволяет сотруднику службы подписаться на push-уведомления |[EdgeHTML17][DevGuideWhatsNewEdgeHtml17] /Build 17133 +| Ознакомьтесь с разделом [API рабочего процесса службы][MDNServiceWorkerApi] выше.  Для приложений Windows 10, включая PWAs, требуется [Служба push-уведомлений Windows (WNS)][WindowsUWPControlsPatternTilesNotificationsWns] для доставки push-уведомлений, которые поддерживают [API внедрения][MDNPushApi]W3C.  |  
| [API уведомлений][MDNNotificationsApi] | Разрешает сотрудникам службы отображать системное уведомление для пользователя при Push-сообщении | [EdgeHTML 14 + +][DevGuideWhatsNewEdgeHtml14] сборки 14393 + | Веб-уведомления в EdgeHTML полностью интегрированы с [центром уведомлений][MicrosoftSupportWindowsNotificationSettings]Windows 10, где пользователи смогут управлять уведомлениями о приложениях и настраивать режим " [тихий час][MicrosoftSupportWindowsFocusAssist]".  |  
| [API фоновой синхронизации][MDNSyncManager] | Предоставляет API для уведомления сотрудника службы о том, что пользователь вернулся в сеть и планирует периодические события для синхронизации локальных данных с сервером. | [В разработке][MicrosoftDeveloperEdgePlatformStatusBackgroundSync] | Сейчас вы можете использовать собственный [API WinRT BackgroundTask][WindowsUWPLaunchResumeBackgroundTasks] для реализации фоновых задач для PWA при запуске приложения Windows 10.  |  

Ниже приведено текущее состояние поддержки Microsoft Store для PWAs в Windows 10:  

| Метод отправки из магазина | Состояние | Сведения |  
|:--- |:--- |:--- |  
| Вручную \ (инициировано разработчиком \) | Доступно | Чтобы приступить к работе, ознакомьтесь со статьей ["PWAs" (EdgeHTML) в Microsoft Store][PwaEdgehtmlMicrosoftStore] .  |  
| Автоматически (с автоматическим индексированием с помощью Bing) | Ожидается в ближайшее время | В настоящее время процесс подготовки к работе PWA идет по [пилотному развертыванию][WindowsBlogsWelcomingPWAsEdgeWindows] с ограниченным набором партнеров приложений.  В течение ближайших месяцев Microsoft Store PWAs по всему распространенному веб-каналу.  Изучите [Автоматическое импорт PWA с помощью Bing][PwaEdgehtmlMicrosoftStoreCriteriaAutomaticSubmission] , чтобы узнать больше о требованиях Microsoft Store к автоматически сгенерированным спискам PWA.  |  

<!-- image links -->  

[ImageISearch]: media/i_search.png  
[ImageIPackage]: media/i_package.png  
[ImageIPushNotification]: media/i_push-notification.png  
[ImageIOffline]: media/i_offline.png  
[ImageIProgressive]: media/i_progressive.png  
[ImageISecurity]: media/i_security.png  
[ImageIResponsive]: media/i_responsive.png  
[ImageILink]: media/i_link.png  

<!-- links -->  

[DevToolsProtocolClientsEdgeDevToolsPreview]: ../devtools-protocol/0.1/clients.md#microsoft-edge-devtools-preview "Клиенты Microsoft Edge DevTools Preview-DevTools Protocol"  
[DevToolsGuideEmulation]: ../devtools-guide/emulation.md "Эмуляции"  
[DevGuideWhatsNewEdgeHtml17]: ../dev-guide/whats-new/edgehtml-17.md "Новые возможности EdgeHTML 17"  
[DevGuideWhatsNewEdgeHtml14]: ../dev-guide/whats-new/edgehtml-14.md "Новые возможности EdgeHTML 14"  
[PwaChromiumIndex]: ../progressive-web-apps-chromium/index.md "Прогрессивные веб-приложения (Chromium) в Windows"  
[PwaEdgehtmlGetStarted]: ../progressive-web-apps-edgehtml/get-started.md "Приступая к работе с прогрессивными веб-приложениями (EdgeHTML)"  
[PwaEdgehtmlMicrosoftStore]: ../progressive-web-apps-edgehtml/microsoft-store.md "Прогрессивные веб-приложения в Microsoft Store"
[PwaEdgehtmlMicrosoftStoreCriteriaAutomaticSubmission]: ../progressive-web-apps-edgehtml/microsoft-store.md#criteria-for-automatic-submission "Условия для автоматической отправки последовательного веб-приложения в Microsoft Store"  
[PwaEdgehtmlMicrosoftStoreImportingBing]: microsoft-store.md#automatic-pwa-importing-with-bing "Автоматическое импортирование PWA с помощью веб-приложений с Bing (EdgeHTML) в Microsoft Store"  


[WindowsUWPControlsPatternTilesNotificationsWns]: /windows/uwp/controls-and-patterns/tiles-and-notifications-windows-push-notification-services--wns--overview.md "Общие сведения о службах push-уведомлений Windows \ (WNS \)"  
[WindowsUWPDesignDevicesDesigningTv]: /windows/uwp/design/devices/designing-for-tv.md "Проектирование для Xbox и телевизора"  
[WindowsUWPDesignDevicesIndex]: /windows/uwp/design/devices/index.md "Вопросы пользовательского интерфейса для устройств UWP"  
[WindowsUWPGetStartedGuide]: /windows/uwp/get-started/universal-application-platform-guide.md "Что такое приложение универсальной платформы Windows (UWP)?"  
[WindowsUWPLaunchResumeBackgroundTasks]: /windows/uwp/launch-resume/support-your-app-with-background-tasks.md "Поддержка приложения с помощью фоновых задач"  
[WindowsUWPPublishIndex]: /windows/uwp/publish/index.md "Публикация приложений и игр для Windows"  
[WindowsUWPPublishDeveloperAccount]: /windows/uwp/publish/opening-a-developer-account.md "Открытие учетной записи разработчика"  

[WindowsBlogsWelcomingPWAsEdgeWindows]: https://blogs.windows.com/msedgedev/2018/02/06/welcoming-progressive-web-apps-edge-windows-10/#56z7mJwKsykfbR4I.97 "Welcoming последовательного веб-приложения в Microsoft EDGE и Windows 10 — блоги Windows"  
[MicrosoftDeveloperEdgePlatformStatusBackgroundSync]: https://developer.microsoft.com/microsoft-edge/platform/status/backgroundsyncapi "API фоновой синхронизации — состояние платформы Microsoft Edge"  
[MicrosoftDeveloperEdgePlatformStatusWebApplicationManifest]: https://developer.microsoft.com/microsoft-edge/platform/status/webapplicationmanifest "Манифест веб-приложения — состояние платформы Microsoft Edge"  
[MicrosoftDeveloperEdgeToolsRemote]: https://developer.microsoft.com/microsoft-edge/tools/remote "Мгновенное Тестирование"  
[MicrosoftDeveloperWindowsMixedReality]: https://developer.microsoft.com/windows/mixed-reality "Смешанная реальность для разработчиков"  
[MicrosoftDeveloperWindowsSurfaceHub]: https://developer.microsoft.com/windows/surfacehub "Microsoft Surface HUB"  
[MicrosoftDeveloperStore]: https://developer.microsoft.com/store "Магазин Microsoft Developer"  
[MicrosoftSupportWindowsFocusAssist]: https://support.microsoft.com/help/4026996/windows-10-turn-focus-assist-on-or-off "Включение и отключение фокусной помощи в Windows 10"  
[MicrosoftSupportWindowsNotificationSettings]: https://support.microsoft.com/help/4028678/windows-10-change-notification-settings "Изменение параметров уведомлений в Windows 10"  

[AListApartUnderstandingProgressiveEnhancement]: https://alistapart.com/article/understandingprogressiveenhancement "Раскрывающийся список "последовательное расширение""  

[MDNApps]: https://developer.mozilla.org/Apps/Progressive "приложения | MDN"  
[MDNCache]: https://developer.mozilla.org/docs/Web/API/Cache "Кэш | MDN"  
[MDNCrossBrowserTesting]: https://developer.mozilla.org/docs/Learn/Tools_and_testing/Cross_browser_testing "Тестирование нескольких браузеров | MDN"  
[MDNCssFlexibleBoxLayout]: https://developer.mozilla.org/docs/Web/CSS/CSS_Flexible_Box_Layout "Макет гибких полей CSS | MDN"  
[MDNCssGridLayout]: https://developer.mozilla.org/docs/Web/CSS/CSS_Grid_Layout "Макет сетки CSS | MDN"  
[MDNFetchApi]: https://developer.mozilla.org/docs/Web/API/Fetch_API "Получить API | MDN"  
[MDNMediaQueries]: https://developer.mozilla.org/docs/Web/CSS/Media_Queries "Запросы мультимедиа | MDN"  
[MDNNotificationsApi]: https://developer.mozilla.org/docs/Web/API/Notifications_API "API уведомлений | MDN"  
[MDNPushApi]: https://developer.mozilla.org/docs/Web/API/Push_API "API push-уведомлений | MDN"  
[MDNPwaAdvantagesDiscoverable]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Discoverable "Возможности, которые могут быть обнаружены последовательностью веб-приложения"  
[MDNPwaAdvantagesInstallable]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Installable "Преимущества устанавливаемого веб-приложения с прогрессивным управлением"  
[MDNPwaAdvantagesLinkable]: https://developer.mozilla.org/Apps/Progressive/Advantages#Linkable "Преимущества веб-приложений, поддерживающих связь"  
[MDNPwaAdvantagesNetworkIndependent]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Network_independent "Преимущества независимых от сети веб-приложений"  
[MDNPwaAdvantagesProgressive]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Progressive "Преимущества последовательного веб-приложения"  
[MDNPwaAdvantagesReEngageable]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Re-engageable "Повторное подключение к веб-приложениям с последовательной подобщением"  
[MDNPwaAdvantagesResponsive]: https://developer.mozilla.org/Apps/Progressive/Advantages#Responsive "Преимущества использования веб-приложения с откликом"  
[MDNPwaAdvantagesSafe]: https://developer.mozilla.org/docs/Web/Apps/Progressive/Advantages#Safe "Преимущества надежного веб-приложения"  
[MDNResponsiveImages]: https://developer.mozilla.org/docs/Learn/HTML/Multimedia_and_embedding/Responsive_images "изображения с откликом | MDN"  
[MDNServiceWorkerApi]: https://developer.mozilla.org/docs/Web/API/Service_Worker_API "API рабочего процесса службы | MDN"  
[MDNSyncManager]: https://developer.mozilla.org/docs/Web/API/SyncManager "SyncManager | MDN"  
[MDNWebAppManifest]: https://developer.mozilla.org/docs/Web/Manifest "Манифест веб-приложения | MDN"  

[PWABuilder]: https://www.pwabuilder.com "PWABuilder"  

[Webhint]: https://webhint.io "Подсказка"  

[WikiDeepLinking]: https://en.wikipedia.org/wiki/Deep_linking "Глубокая связь — Википедии"  
[WikiHttps]: https://en.wikipedia.org/wiki/HTTPS "HTTPS-Википедии"  
[WikiResponsiveWebDesign]: https://en.wikipedia.org/wiki/Responsive_web_design "Отклики на веб-дизайн — Википедии"  
