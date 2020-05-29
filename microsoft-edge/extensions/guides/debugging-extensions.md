---
description: С помощью средств разработчика F12 вы узнаете, как выполнять отладку фонового сценария расширения, сценариев содержимого и страниц расширений.
title: Расширения — Отладка
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 12/16/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: EDGE, веб-разработка, HTML, JavaScript, разработчик, отладка, отладка
ms.custom: seodec18
ms.openlocfilehash: 34488870cb4e4a92a9d57859509ce7d1176cf284
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571569"
---
# <span data-ttu-id="83a1f-104">Отладка расширений</span><span class="sxs-lookup"><span data-stu-id="83a1f-104">Debugging extensions</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="83a1f-105">Вы можете выполнять отладку расширений в Microsoft Edge с помощью средств разработчика F12.</span><span class="sxs-lookup"><span data-stu-id="83a1f-105">You can debug your extensions in Microsoft Edge by using F12 Developer Tools.</span></span>

<span data-ttu-id="83a1f-106">Следующий видеоролик проходит через расширение Microsoft Edge Buggy, проследуя каждый из сценариев отладки и устранит его.</span><span class="sxs-lookup"><span data-stu-id="83a1f-106">The following video goes through a buggy Microsoft Edge extension, walking though each debugging scenario and fixing it up along the way.</span></span> <span data-ttu-id="83a1f-107">Для получения дополнительных сведений ознакомьтесь с пошаговыми инструкциями, приведенными ниже.</span><span class="sxs-lookup"><span data-stu-id="83a1f-107">See the step-by-step instructions below for more info.</span></span>

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Debugging-Microsoft-Edge-Extensions/player]


> [!NOTE]
> <span data-ttu-id="83a1f-108">Чтобы воспользоваться преимуществами отладки расширений с помощью F12, необходимо сначала включить функции разработчика в: flags.</span><span class="sxs-lookup"><span data-stu-id="83a1f-108">In order to take advantage of extension debugging with F12, you must first turn on developer features in about:flags.</span></span> <span data-ttu-id="83a1f-109">Дополнительные сведения о том, как это сделать, можно найти в разделе [Добавление и удаление расширений](./adding-and-removing-extensions.md) .</span><span class="sxs-lookup"><span data-stu-id="83a1f-109">See [Adding and removing extensions](./adding-and-removing-extensions.md) for details on how to do this.</span></span>


## <span data-ttu-id="83a1f-110">Отладка фонового сценария</span><span class="sxs-lookup"><span data-stu-id="83a1f-110">Background script debugging</span></span>
<span data-ttu-id="83a1f-111">Чтобы начать отладку фонового сценария расширения, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="83a1f-111">To start debugging the background script of your extension:</span></span>

1. <span data-ttu-id="83a1f-112">Нажмите кнопку **Дополнительно (...)** , а затем — **расширения** , чтобы перейти в область "расширение".</span><span class="sxs-lookup"><span data-stu-id="83a1f-112">Click on **More (...)** followed by **Extensions** to go into the extension pane.</span></span>  
 ![Кнопка "Дополнительно"](./../media/morebutton.png)
2. <span data-ttu-id="83a1f-114">Выберите расширение, которое вы хотите отладить.</span><span class="sxs-lookup"><span data-stu-id="83a1f-114">Click on the extension that you want to debug.</span></span>
3. <span data-ttu-id="83a1f-115">Щелкните ссылку **Фоновая страница** , чтобы открыть клавишу F12 для фонового процесса.</span><span class="sxs-lookup"><span data-stu-id="83a1f-115">Click on the **Background page** link to bring up F12 for the background process.</span></span>  
 ![выбранное расширение Просмотр параметров с помощью ссылки для проверки](./../media/debug-inspect.png)
4. <span data-ttu-id="83a1f-117">Выберите вкладку **Debugger (отладчик** ) в F12.</span><span class="sxs-lookup"><span data-stu-id="83a1f-117">Select the **Debugger** tab in F12.</span></span>
5. <span data-ttu-id="83a1f-118">Перейдите к фоновому сценарию расширения и выберите его.</span><span class="sxs-lookup"><span data-stu-id="83a1f-118">Navigate to and select your extension's background script.</span></span>
6. <span data-ttu-id="83a1f-119">Размещайте точки останова для отладки, щелкая слева от номера строки исходного кода.</span><span class="sxs-lookup"><span data-stu-id="83a1f-119">Place breakpoints for debugging by clicking to the left of the source code line number.</span></span>  
 ![консоль F12, на которой показан фоновый сценарий с точками разрыва](./../media/debug-f12-background.png)
7. <span data-ttu-id="83a1f-121">Откройте вкладку **консоль** и выполните команду " `location.reload()` ".</span><span class="sxs-lookup"><span data-stu-id="83a1f-121">Select the **Console** tab and execute the command "`location.reload()`".</span></span> <span data-ttu-id="83a1f-122">Это приведет к повторному выполнению фонового сценария, который позволит вам пройти код.</span><span class="sxs-lookup"><span data-stu-id="83a1f-122">This will re-execute the background script, allowing you to step through your code.</span></span>  
 ![консоль с расположением. Перезагрузка введена](./../media/debug-f12-background-console.png)


## <span data-ttu-id="83a1f-124">Отладка скриптов содержимого</span><span class="sxs-lookup"><span data-stu-id="83a1f-124">Content script debugging</span></span>
<span data-ttu-id="83a1f-125">Чтобы приступить к отладке сценария содержимого расширения, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="83a1f-125">To start debugging the content script of your extension:</span></span>

1. <span data-ttu-id="83a1f-126">Запустите F12, перейдя на кнопку **Дополнительно (...)** и выбрав пункт **"средства разработчика F12"** или нажав клавишу F12 на клавиатуре.</span><span class="sxs-lookup"><span data-stu-id="83a1f-126">Launch F12 by either navigating to the **More (...)** button and selecting **"F12 Developer Tools"** or by pressing F12 on your keyboard.</span></span>
2. <span data-ttu-id="83a1f-127">Перейдите к скрипту содержимого расширения и выберите его.</span><span class="sxs-lookup"><span data-stu-id="83a1f-127">Navigate to and select your extension's content script.</span></span> <span data-ttu-id="83a1f-128">Скрипты содержимого для выполняемых в настоящее время расширений будут отображаться в разных папках для каждого из этих расширений.</span><span class="sxs-lookup"><span data-stu-id="83a1f-128">Content scripts for extensions currently running will be depicted by a different folder for each extension.</span></span>

    > [!NOTE]
    > <span data-ttu-id="83a1f-129">Отобразятся только сценарии для запуска содержимого.</span><span class="sxs-lookup"><span data-stu-id="83a1f-129">Only running content scripts will appear.</span></span>

3. <span data-ttu-id="83a1f-130">Размещайте точки останова для отладки, щелкая слева от номера строки исходного кода.</span><span class="sxs-lookup"><span data-stu-id="83a1f-130">Place breakpoints for debugging by clicking to the left of the source code line number.</span></span>  
 ![F12 с отлаживаемым сценарием содержимого](./../media/debug-content-f12.png)
4. <span data-ttu-id="83a1f-132">Обновите вкладку браузера, чтобы начать пошаговую отладку кода.</span><span class="sxs-lookup"><span data-stu-id="83a1f-132">Refresh the browser tab to begin stepping though your code.</span></span>




## <span data-ttu-id="83a1f-133">Отладка страницы расширения</span><span class="sxs-lookup"><span data-stu-id="83a1f-133">Extension page debugging</span></span>

<span data-ttu-id="83a1f-134">Существует два метода, которые можно использовать для доступа к исходному коду страницы расширения для отладки.</span><span class="sxs-lookup"><span data-stu-id="83a1f-134">There are two methods that can be used for accessing the source code of your extension page for debugging.</span></span> <span data-ttu-id="83a1f-135">Один из способов применяется к различным страницам, а другая — только для всплывающих страниц.</span><span class="sxs-lookup"><span data-stu-id="83a1f-135">One method applies to a variety of pages while the other only works for popup pages.</span></span>

### <span data-ttu-id="83a1f-136">Отладка любой страницы расширения</span><span class="sxs-lookup"><span data-stu-id="83a1f-136">Debugging any extension page</span></span>
<span data-ttu-id="83a1f-137">Следующий метод работает для всех страниц расширения, таких как страница параметров и всплывающие окна.</span><span class="sxs-lookup"><span data-stu-id="83a1f-137">The following method works for all extension pages like the options page and popups:</span></span>


1. <span data-ttu-id="83a1f-138">Щелкните правой кнопкой мыши фон страницы.</span><span class="sxs-lookup"><span data-stu-id="83a1f-138">Right-click on the background of your page.</span></span>
2. <span data-ttu-id="83a1f-139">Нажмите кнопку **"Просмотр исходного кода"**.</span><span class="sxs-lookup"><span data-stu-id="83a1f-139">Select **"View source"**.</span></span>

   ![Отладка всплывающих окон с помощью F12](./../media/debug-popup-select.png)

3. <span data-ttu-id="83a1f-141">После открытия F12 разместите точки останова в файле, который вы хотите отладить.</span><span class="sxs-lookup"><span data-stu-id="83a1f-141">Once F12 opens, place breakpoints within the file you want to debug.</span></span>

   ![Отладка всплывающих окон с помощью F12](./../media/debug-popup-f12.png)
4. <span data-ttu-id="83a1f-143">Откройте вкладку **консоль** и выполните команду `location.reload()` .</span><span class="sxs-lookup"><span data-stu-id="83a1f-143">Select the **Console** tab and execute the command `location.reload()`.</span></span> <span data-ttu-id="83a1f-144">Это приведет к повторному выполнению сценария страницы, что позволит вам пройти код.</span><span class="sxs-lookup"><span data-stu-id="83a1f-144">This will re-execute the page script, allowing you to step through your code.</span></span>  

   ![консоль с расположением. Перезагрузка введена](./../media/debug-f12-background-console.png)

### <span data-ttu-id="83a1f-146">Отладка страницы расширения всплывающего окна</span><span class="sxs-lookup"><span data-stu-id="83a1f-146">Debugging a popup extension page</span></span>
<span data-ttu-id="83a1f-147">Несмотря на то, что метод для отладки страниц расширений также применяется к страницам расширений всплывающих окон, ниже описаны другие способы отладки всплывающего окна.</span><span class="sxs-lookup"><span data-stu-id="83a1f-147">While the method for debugging extension pages also applies to popup extension pages, the following steps outline another way to debug your popup:</span></span>

1. <span data-ttu-id="83a1f-148">Щелкните правой кнопкой мыши значок расширения.</span><span class="sxs-lookup"><span data-stu-id="83a1f-148">Right-click your extension's icon.</span></span>
2. <span data-ttu-id="83a1f-149">Выберите **"проверить всплывающее окно"**.</span><span class="sxs-lookup"><span data-stu-id="83a1f-149">Select **"Inspect popup"**.</span></span>

   ![Проверка отладки всплывающего окна](./../media/debug-popup-inspect.png)
3. <span data-ttu-id="83a1f-151">Выполните действия 3 и 4, описанные выше, для размещения точек останова и повторной загрузки всплывающего окна.</span><span class="sxs-lookup"><span data-stu-id="83a1f-151">Follow steps 3 and 4 above for placing breakpoints and reloading the popup.</span></span>
