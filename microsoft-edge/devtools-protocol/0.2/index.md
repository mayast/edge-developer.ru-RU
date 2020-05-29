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
# <span data-ttu-id="1a8aa-103">Протокол DevTools версии 0,2 заметки о выпуске</span><span class="sxs-lookup"><span data-stu-id="1a8aa-103">DevTools Protocol Version 0.2 Release Notes</span></span>

> [!NOTE]
> <span data-ttu-id="1a8aa-104">Версия 0,2 протокола Microsoft Edge DevTools работает только на [обновлениях для Windows 10 октября 2018](/windows/uwp/whats-new/windows-10-build-17763) и более поздних сборок для [предварительной оценки Windows](https://insider.windows.com/getting-started/) .</span><span class="sxs-lookup"><span data-stu-id="1a8aa-104">Version 0.2 of the Microsoft Edge DevTools Protocol works only on the [Windows 10 October 2018 Update](/windows/uwp/whats-new/windows-10-build-17763) and later [Windows Insider Preview](https://insider.windows.com/getting-started/) builds.</span></span>

<span data-ttu-id="1a8aa-105">Версия 0,2 **протокола Microsoft Edge DevTools** обеспечивает предварительный просмотр для проверки инструментальных средств EdgeHTML и Basic Remote Debugging в новом отдельном приложении [Microsoft Edge DevTools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) .</span><span class="sxs-lookup"><span data-stu-id="1a8aa-105">Version 0.2 of the Microsoft **Edge DevTools Protocol** provides a preview for testing EdgeHTML instrumentation and basic remote debugging in the new standalone [Microsoft Edge DevTools Preview](https://www.microsoft.com/store/p/microsoft-edge-devtools-preview/9mzbfrmz0mnj?activetab=pivot%3aoverviewtab) app.</span></span> <span data-ttu-id="1a8aa-106">Для этого требуется, чтобы на компьютере была установлена версия [Windows 10 октябрь 2018](/windows/uwp/whats-new/windows-10-build-17763) или более поздняя сборка предварительной [оценки для Windows](https://insider.windows.com/getting-started/) .</span><span class="sxs-lookup"><span data-stu-id="1a8aa-106">As such, it requires you to be running the [Windows 10 October 2018 Update](/windows/uwp/whats-new/windows-10-build-17763) or a later [Windows Insider Preview](https://insider.windows.com/getting-started/) build.</span></span>

<span data-ttu-id="1a8aa-107">Цели протокола DevTools — это три части:</span><span class="sxs-lookup"><span data-stu-id="1a8aa-107">The goals behind the DevTools Protocol are three-fold:</span></span>

 - <span data-ttu-id="1a8aa-108">Предоставьте общедоступный API для нашего приложения DevTools, чтобы присоединиться к Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1a8aa-108">Provide a public API for our DevTools app to attach to Microsoft Edge</span></span>
 - <span data-ttu-id="1a8aa-109">Расширение доступа к функциональным возможностям DevTools с помощью внешних клиентов</span><span class="sxs-lookup"><span data-stu-id="1a8aa-109">Expand access of DevTools functionality to external tooling clients</span></span>
 - <span data-ttu-id="1a8aa-110">Разрешите удаленную отладку в диапазоне устройств с Windows 10, работающих в Micrsoft Edge</span><span class="sxs-lookup"><span data-stu-id="1a8aa-110">Enable remote debugging across the range of Windows 10 devices running Micrsoft Edge</span></span> 

<span data-ttu-id="1a8aa-111">Версия 0,2 протокола DevTools включает новые домены для стиля и макета (только для чтения) и API консоли в дополнение к основным функциям отладки сценария, представленным в версии 0,1.</span><span class="sxs-lookup"><span data-stu-id="1a8aa-111">Version 0.2 of the DevTools Protocol includes new domains for style and layout (read-only) debugging and console APIs, in addition to the core script debugging functionality introduced in Version 0.1.</span></span> <span data-ttu-id="1a8aa-112">В пользовательском интерфейсе DevTools это преобразуется в функциональные возможности, доступные на панелях [**элементы**](../../devtools-guide/elements.md), [**консоль**](../../devtools-guide/console.md) и [**отладчик**](../../devtools-guide/debugger.md) .</span><span class="sxs-lookup"><span data-stu-id="1a8aa-112">In the Edge DevTools UI, this translates to functionality available in the [**Elements**](../../devtools-guide/elements.md), [**Console**](../../devtools-guide/console.md) and [**Debugger**](../../devtools-guide/debugger.md)  panels.</span></span>
