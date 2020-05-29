---
description: Заметки о выпуске Microsoft Edge DevTools Protocol версии 0,2
title: Заметки о выпуске протокола Microsoft Edge DevTools версии 0,2
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: reference
ms.prod: microsoft-edge
ms.openlocfilehash: c4c54273d123c605181ee4b53aa441768a8711bf
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571658"
---
# Протокол DevTools версии 0,2 заметки о выпуске

> [!NOTE]
> Версия 0,2 протокола Microsoft Edge DevTools работает только на [обновлениях для Windows 10 октября 2018](/windows/uwp/whats-new/windows-10-build-17763) и более поздних сборок для [предварительной оценки Windows](https://insider.windows.com/getting-started/) .

Версия 0,2 **протокола Microsoft Edge DevTools** обеспечивает предварительный просмотр для проверки инструментальных средств EdgeHTML и Basic Remote Debugging в новом отдельном приложении [Microsoft Edge DevTools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) . Для этого требуется, чтобы на компьютере была установлена версия [Windows 10 октябрь 2018](/windows/uwp/whats-new/windows-10-build-17763) или более поздняя сборка предварительной [оценки для Windows](https://insider.windows.com/getting-started/) .

Цели протокола DevTools — это три части:

 - Предоставьте общедоступный API для нашего приложения DevTools, чтобы присоединиться к Microsoft Edge
 - Расширение доступа к функциональным возможностям DevTools с помощью внешних клиентов
 - Разрешите удаленную отладку в диапазоне устройств с Windows 10, работающих в Micrsoft Edge 

Версия 0,2 протокола DevTools включает новые домены для стиля и макета (только для чтения) и API консоли в дополнение к основным функциям отладки сценария, представленным в версии 0,1. В пользовательском интерфейсе DevTools это преобразуется в функциональные возможности, доступные на панелях [**элементы**](../../devtools-guide/elements.md), [**консоль**](../../devtools-guide/console.md) и [**отладчик**](../../devtools-guide/debugger.md) .
