---
title: Приступая к работе с эмуляторами Lane Surface удаленной отладки
author: zoherghadyali
ms.author: zoghadya
ms.date: 04/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Microsoft EDGE, веб-разработка, средства F12, Devtools, удаленная отладка, Android, Surface Duo
ms.openlocfilehash: af6fa6433b0bc6bba0599e6e9a805235504caadd
ms.sourcegitcommit: 966bfc60040acc794b6ee20eb2084bc8264a4852
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/05/2020
ms.locfileid: "10621504"
---
# Приступая к работе с эмуляторами Lane Surface удаленной отладки

В этой статье описывается процесс удаленной отладки веб-содержимого в [приложении Microsoft Edge][AndroidEdge] на эмуляторе [Duo Surface][SurfaceDuo] из экземпляра [Microsoft Edge][DesktopEdge]. Информация о отладке на устройстве Surface Duo приведена в руководстве по [удаленным отладке устройств с Android][RemoteDebuggingAndroid].

## Подготовка

Перед запуском [эмулятора Surface Duo][DuoEmulator]установите [пакет SDK Surface Duo][DuoSdk] . Дополнительные сведения можно найти [в статьях скачать пакет SDK Surface Duo][DuoSdkdocs].

## Шаг 1: переход в edge://inspect

Откройте классическое [приложение Microsoft Edge][DesktopEdge]и перейдите к нему `edge://inspect` .

> ##### Рис. 1  
> `edge://inspect`Страница в Microsoft EDGE на рабочем столе — ![ страница Edge://inspect в Microsoft EDGE на рабочем столе][ImageEdgeInspect]

> [!NOTE]
> Если `edge://inspect` Страница не распознает [эмулятор Surface Duo][DuoEmulator], перезапустите эмулятор.

## Шаг 2: Запуск эмулятора Surface Duo

Запустите [эмулятор Surface Duo][DuoEmulator]. Обратите внимание, что эмулятор отображает 2 разных экрана, запущенных в эмуляторе.

> ##### Рисунок 2
> Эмулятор Surface Duo ![ , эмулятор Surface Duo][ImageDuoEmulator]  

## Шаг 3. Загружайте веб-содержимое в Microsoft EDGE на эмулятор Surface Duo.

На любом экране проведите пальцем вверх по лотку "Избранное" [эмулятора Surface Duo][DuoEmulator] , чтобы отобразить ящик приложений. Выберите **Edge** , чтобы запустить [приложение Microsoft Edge][AndroidEdge].

> ##### Рисунок3
> Приложение Microsoft EDGE в эмуляторе Lane Duo — ![ приложение Microsoft EDGE в эмуляторе Lane Duo][ImageDuoEmulatorEdge]  

Перейдите на веб-сайт или приложение, которое вы хотите отладить в [приложении Microsoft Edge][AndroidEdge].

## Шаг 4: Отладка содержимого веб-страницы в эмуляторе Duo Surface 

Вернитесь к экземпляру рабочего стола [Microsoft Edge][DesktopEdge]. На `edge://inspect` странице теперь отображается **SurfaceDuoEmulator** со списком открытых вкладок или [PWAs][PwaDocs] , которые выполняются в [эмуляторе Duo Surface][DuoEmulator].

> ##### Рисунок4
> На `edge://inspect` странице отображается список вкладок в приложении Microsoft EDGE, работающем на эмуляторе. на ![ странице Edge://inspect отображается список открытых вкладок приложения Microsoft EDGE, запущенного на эмуляторе.][ImageEdgeInspectTargets]  

> [!NOTE]
> Если вы не видите **SurfaceDuoEmulator** на `edge://inspect` странице, попробуйте открыть или закрыть вкладки в [приложении Microsoft Edge][AndroidEdge] в [эмуляторе Duo Surface][DuoEmulator]. Дополнительные действия по устранению неполадок можно найти в [разделе Устранение неполадок устройств с Android][TroubleshootingAndroid].

В списке открытых вкладок, запущенных в эмуляторе, на вкладке, где находится веб-содержимое для отладки, нажмите кнопку **проверить** . [Приложение Microsoft Edge DevTools][DevToolsDocs] откроется в новом окне. Нажмите **кнопку Переключить** презентацию ![ ][ImageToggleScreencastIcon] , чтобы просмотреть веб-содержимое в [эмуляторе Duo Surface][DuoEmulator] в окне DevTools. Теперь вы можете использовать Microsoft Edge DevTools для отладки вашего веб-содержимого в [эмуляторе Surface Duo][DuoEmulator].

> ##### Рисунок 5
> Использование Microsoft Edge DevTools для отладки Bing в приложении Microsoft EDGE в эмуляторе Surface Duo ![ с помощью Microsoft Edge DevTools для отладки Bing в приложении Microsoft EDGE в эмуляторе Surface Duo][ImageDevTools]  

> [!NOTE]
> Если вы зайдете [приложение Microsoft Edge][AndroidEdge] на обоих экранах эмулятора, она будет показывать новый размер приложения, но не на шарнир. Чтобы понять, как шарнирный элемент влияет на макет вашего веб-содержимого, используйте [эмулятор Surface Duo][DuoEmulator] вместо ролика.

## Дополнительные ресурсы

Интернет — это замечательная платформа для нового класса складная и устройств с двумя экранами, так как вы можете создавать HTML, CSS и JavaScript один раз, чтобы они выглядели хорошо на одном экране, на двух экранах и на складная устройствах. Дополнительные сведения можно найти в разделе Дополнительные ресурсы, чтобы приступить к созданию веб-содержимого для новых устройств.

- [Документация по созданию приложений на устройствах с двумя экранами][DualScreenDocs]
- [Веб-платформа Microsoft Edge для новых API для создания веб-взаимодействия на складная и на устройствах с двумя мониторами][WebPlatformExplainer]
- [Запись рабочего сеанса Microsoft 365 для разработчиков: создание двух экранных возможностей для веб-сайтов и веб-приложений][DeveloperDay]

<!-- image links -->  
[ImageEdgeInspect]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-surface-duo-inspect-page.msft.png "Рисунок 1: страница edge://inspect в Microsoft EDGE на рабочем столе"
[ImageDuoEmulator]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-surface-duo-emulator.msft.png "Рисунок 2: эмулятор Surface Duo"
[ImageDuoEmulatorEdge]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-surface-duo-emulator-edge.msft.png "Рисунок 3: приложение Microsoft EDGE в эмуляторе Lane Duo"
[ImageEdgeInspectTargets]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-surface-duo-inspect-page-with-targets.msft.png "Рисунок 4: страница edge://inspect отображает список открытых вкладок приложения Microsoft EDGE, запущенного на эмуляторе."
[ImageToggleScreencastIcon]: images/toggle-screencast-icon.msft.png
[ImageDevTools]: /microsoft-edge/devtools-guide-chromium/media/remote-debugging-surface-duo-devtools.msft.png "Рисунок 5: использование Microsoft Edge DevTools для отладки Bing в приложении Microsoft EDGE в эмуляторе Lane Duo"

<!-- links -->  
[RemoteDebuggingAndroid]: /microsoft-edge/devtools-guide-chromium/remote-debugging/index "Начало работы с удаленными отладкой устройств с Android"
[PwaDocs]: /microsoft-edge/progressive-web-apps-chromium/index "Прогрессивные веб-приложения для Windows"
[DevToolsDocs]: /microsoft-edge/devtools-guide-chromium "Инструменты разработчика Microsoft EDGE (Chromium)"
[TroubleshootingAndroid]: /microsoft-edge/devtools-guide-chromium/remote-debugging/index#troubleshooting-devtools-is-not-detecting-the-android-device "Устранение неполадок: DevTools не может обнаружить устройство с Android"

[AndroidEdge]: https://play.google.com/store/apps/details?id=com.microsoft.emmx "Приложение Microsoft Edge для Android"
[SurfaceDuo]: https://www.microsoft.com/surface/devices/surface-duo "Знакомство с Surface Duo"
[DesktopEdge]: https://www.microsoft.com/edge/ "Знакомство с новым Microsoft Edge"
[DuoEmulator]: https://docs.microsoft.com/dual-screen/android/use-emulator "Использование эмулятора Surface DUo"
[DuoSdk]: https://www.microsoft.com/download/details.aspx?id=100847 "Предварительная версия SDK Surface Duo"
[DuoSdkDocs]: https://docs.microsoft.com/dual-screen/android/get-duo-sdk "Скачать пакет SDK Surface Duo"
[DualScreenDocs]: https://docs.microsoft.com/dual-screen/ "Создание приложений для устройств с двумя экранами"
[WebPlatformExplainer]: https://github.com/MicrosoftEdge/MSEdgeExplainers/blob/master/Foldables/explainer.md "Примитивы веб-платформ для Грамотногоных функций на складная устройствах"
[DeveloperDay]: https://youtu.be/DXrZWsqXPVc "Создание возможностей двустороннего экрана для веб-сайтов и Интернет-приложений"
