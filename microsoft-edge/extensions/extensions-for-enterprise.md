---
ms.assetid: 8e2f75c4-fb7f-4892-a6c2-23bac081581a
description: Узнайте о различных аспектах расширений Microsoft Edge для предприятий и Узнайте, как они похожи на приложения UWP.
title: Расширения для предприятий
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 03/05/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: EDGE, веб-разработка, HTML, CSS, JavaScript, разработчик
ms.custom: seodec18
ms.openlocfilehash: 8f50c282fce11d2654f990bf135941e0616af3f3
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571588"
---
# Расширения для предприятий  

[!INCLUDE [deprecation-note](includes/deprecation-note.md)]  

У расширений Microsoft Edge есть похожие рабочие процессы по сравнению с другими корпоративными приложениями UWP. Приведенные ниже сведения относятся к определенным аспектам расширений Microsoft Edge.

## Предварительные условия
Следующие элементы предлагаются для разработки, упаковки и развертывания расширения Microsoft Edge для предприятий.

+ Учетная запись портала разработчиков Windows для подписания и освобождения расширения в частном корпоративном магазине. Дополнительные сведения о том [, как открыть учетную запись разработчика,](/windows/uwp/publish/opening-a-developer-account) вы увидите здесь.
+ Microsoft Store для бизнеса или образования, чтобы распространить приложение на корпоративный выпуск. Дополнительные сведения смотрите в [справочной документации Microsoft Store для бизнеса и образовательных учреждений](/microsoft-store/) .
+ Определите, в каких версиях Windows 10 будет работать расширение Microsoft Edge. Список существующих выпусков Windows 10 приведен в разделе [сведения о выпуске Windows 10](https://www.microsoft.com/itpro/windows-10/release-information) .

> [!NOTE]
> Для подписывания выпускного модуля можно использовать портал разработчиков Windows. Для получения дополнительных сведений ознакомьтесь с разрешениями для опубликованных расширений для заведений.

## Windows Information Protection
В настоящее время расширения Microsoft EDGE не учитывают параметры Windows Information Protection (WIP). Если в организации важна защита данных, поддержку расширений для Microsoft Edge включать нельзя.

Чтобы отключить расширения для сотрудников, настройте групповую политику и параметры Microsoft Intune. Дополнительные сведения о политиках для настройки можно найти в разделе [доступные политики для Microsoft Edge](https://technet.microsoft.com/itpro/microsoft-edge/available-policies).

## Расширения пакетов
Прежде чем предприятие сможет распространить расширение между сотрудниками, его необходимо упаковать. Инструкции по использованию расширений пакетов можно найти в руководстве по [упаковке](./guides/packaging.md) .

> [!TIP]
> Обязательно протестируйте установку и запустите расширение для всех версий Windows 10, чтобы убедиться, что оно будет работать надлежащим образом перед распространением.

## Распространение расширений
После того как расширение было упаковано, оно может распространяться между сотрудниками в Microsoft Store, Microsoft Store для бизнеса или в рамках неопубликованных приложений.

Расширения, распределенные по мере того, как Microsoft Store для бизнеса могут быть назначены сотрудникам или добавлены в личное хранилище, где все сотрудники смогут получать к ним доступ. Это можно сделать, выполнив руководство по [распространению бизнес-приложений (LOB) для предприятий](https://msdn.microsoft.com/windows/uwp/publish/distribute-lob-apps-to-enterprises) .

В неопубликованного расширениях, устройствах (неуправляемых или управляемых) необходимо разблокировать для загрузки неопубликованных приложений. Дополнительные сведения о неопубликованного упакованных расширениях можно найти [в бизнес-приложениях неопубликованного в Windows 10](https://technet.microsoft.com/itpro/windows/deploy/sideload-apps-in-windows-10) .

> [!IMPORTANT]
> Если в масштабах предприятия разрабатывается и распространяется внутреннее расширение, для предприятия потребуется как Microsoft Store для бизнеса (или как обучение), так и учетная запись портала разработчиков Windows.

### Поведение расширений неопубликованного
В отличие от расширений, распространяемых через Microsoft Store (или Microsoft Store для бизнеса), расширения неопубликованного в Microsoft Edge обрабатываются по-разному.

Первое отличие влияет на то, как неопубликованного расширения работают после установки. В отличие от расширений из Microsoft Store, расширения неопубликованного не будут немедленно показывать уведомление о том, что у вас есть новое расширение, и нужно вручную включить его пользователем.

Чтобы включить расширение, откройте меню **Дополнительно (...)** , выберите пункт **расширения** , и в списке установленных расширений появится расширение неопубликованного. Щелкните расширение и включите его.

Вторая разница влияет на то, как расширения неопубликованного отображаются в браузере. Например, уведомление о том, что у вас есть новое расширение, и список установленных расширений включают дополнительное предупреждение о том, что расширение из неизвестного источника.

![предупреждение неопубликованного 1](./media/sideload-permissionflyout.PNG)

![предупреждение неопубликованного 2](./media/sideload-l1warning.PNG)

Третья и конечная разница влияют на то, как неопубликованного расширения работают при запуске браузера. Расширения неопубликованного на устройствах, которые либо подключены к домену, либо в случае поддержки MDM будут работать как расширения из Microsoft Store. Однако расширения неопубликованного на устройствах, не присоединенных к домену или не поддерживающих MDM, будут отключены во время запуска браузера и потребуют от пользователя выполнить явное действие.

Вскоре после запуска браузера (после того, как в течение 10 секунд бездействия) в нижней части окна появится следующее уведомление.

![уведомление неопубликованного](./media/sideload-scareUI.PNG)

Каждый раз при запуске Microsoft Edge пользователи должны будут выбрать "включить все в любом случае", чтобы использовать расширение.
