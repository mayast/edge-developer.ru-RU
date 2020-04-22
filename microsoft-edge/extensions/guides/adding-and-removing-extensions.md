---
description: Сведения о добавлении и удалении расширений, а также о перемещении кнопки расширения рядом с адресной строкой.
title: Добавление и удаление расширений
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/03/2019
ms.topic: article
ms.prod: microsoft-edge
keywords: EDGE, веб-разработка, HTML, CSS, JavaScript, разработчик, расширение
ms.custom: seodec18
localization_priority: Priority
ms.openlocfilehash: fdc6950962e7ce7e0a720d0bafa7e2c63ebd7098
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571565"
---
# <span data-ttu-id="5c22a-104">Добавление, перемещение и удаление расширений для Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="5c22a-104">Adding, moving, and removing extensions for Microsoft Edge</span></span>  

[!INCLUDE [deprecation-note](../includes/deprecation-note.md)]  

<span data-ttu-id="5c22a-105">Поддержка расширений Microsoft Edge была представлена в **обновлении годовщины Windows 10**.</span><span class="sxs-lookup"><span data-stu-id="5c22a-105">Microsoft Edge support for extensions was introduced in the **Windows 10 Anniversary Update**.</span></span> <span data-ttu-id="5c22a-106">Если вы разрабатываете расширение Microsoft EDGE и хотите загрузить его, или если у вас уже есть и хотите удалить его, ознакомьтесь с приведенными ниже инструкциями.</span><span class="sxs-lookup"><span data-stu-id="5c22a-106">If you're developing a Microsoft Edge extension and want to load it up, or if you already have and now want to remove it, check out the steps below.</span></span>
<span data-ttu-id="5c22a-107">Кроме того, в этом разделе приведены сведения о том, как изменить расположение значка расширения в браузере.</span><span class="sxs-lookup"><span data-stu-id="5c22a-107">Also included are details on how to change your extension icon's location in the browser.</span></span>

## <span data-ttu-id="5c22a-108">Добавление расширения</span><span class="sxs-lookup"><span data-stu-id="5c22a-108">Adding an extension</span></span>

1. <span data-ttu-id="5c22a-109">Откройте Microsoft EDGE и введите "about: Flags" в адресную строку.</span><span class="sxs-lookup"><span data-stu-id="5c22a-109">Open Microsoft Edge and type 'about:flags' into the address bar.</span></span>

2. <span data-ttu-id="5c22a-110">Установите флажок **включить компоненты разработчика расширений** .</span><span class="sxs-lookup"><span data-stu-id="5c22a-110">Select the **Enable extension developer features** checkbox.</span></span>

   ![about: flags включение функций разработчика](./../media/sideload-aboutflags.png)
   > [!NOTE]
   > <span data-ttu-id="5c22a-112">Если у вас нет годовщины Windows 10 или более поздней версии, этот параметр будет недоступен.</span><span class="sxs-lookup"><span data-stu-id="5c22a-112">If you don't have the Windows 10 Anniversary Update or later, this option will not be available.</span></span>

3. <span data-ttu-id="5c22a-113">Нажмите кнопку **Дополнительно (...)** , чтобы открыть меню.</span><span class="sxs-lookup"><span data-stu-id="5c22a-113">Select **More (...)** to open the menu.</span></span>

   ![Кнопка "Дополнительно"](./../media/morebutton.png)  

4. <span data-ttu-id="5c22a-115">В меню выберите пункт **расширения** .</span><span class="sxs-lookup"><span data-stu-id="5c22a-115">Select **Extensions** from the menu.</span></span>

5. <span data-ttu-id="5c22a-116">Нажмите кнопку **загрузить расширение** .</span><span class="sxs-lookup"><span data-stu-id="5c22a-116">Select the **Load extension** button.</span></span>

   ![Выбор пункта "загрузить расширение"](./../media/sideload-load-extension.png)

6. <span data-ttu-id="5c22a-118">Перейдите к папке расширения и нажмите кнопку **выбрать папку** .</span><span class="sxs-lookup"><span data-stu-id="5c22a-118">Navigate to your extension's folder and select the  **Select folder** button.</span></span>
   ![Выбор папки расширения для загрузки](./../media/sideload-select-extension.png)
   > [!NOTE]
   > <span data-ttu-id="5c22a-120">Если вы столкнулись с сообщением об ошибке при загрузке расширения, ознакомьтесь со страницей [Устранение неполадок](./../troubleshooting.md) .</span><span class="sxs-lookup"><span data-stu-id="5c22a-120">If you encounter an error message when loading your extension, refer to the [troubleshooting](./../troubleshooting.md) page for guidance.</span></span>


**<span data-ttu-id="5c22a-121">Все готово!</span><span class="sxs-lookup"><span data-stu-id="5c22a-121">You're all set!</span></span> <span data-ttu-id="5c22a-122">Теперь вы увидите расширение, указанное в области расширения Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5c22a-122">You should now see the extension listed in Microsoft Edge's extension pane.</span></span>**

![расширение области «расширение»](./../media/sideload-extension-installed.png)

> [!NOTE]
> <span data-ttu-id="5c22a-124">Неподписанные расширения автоматически отключаются при последующих запусках Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5c22a-124">Unsigned extensions are automatically turned off on subsequent launches of Microsoft Edge.</span></span> <span data-ttu-id="5c22a-125">При переходе браузера в состояние простоя (после примерно 10 секунд бездействия) в нижней части окна отображается следующее уведомление.</span><span class="sxs-lookup"><span data-stu-id="5c22a-125">When the browser enters an idle state (after approximately 10 seconds of inactivity) you will see the following notification at the bottom of the window.</span></span> ![<span data-ttu-id="5c22a-126">опасное](./../media/riskynotification.png) уведомление. чтобы включить неподписанные расширения, нажмите кнопку "включить все равно".</span><span class="sxs-lookup"><span data-stu-id="5c22a-126">risky notification](./../media/riskynotification.png) To turn on the unsigned extensions, click "Turn on anyway".</span></span>



## <span data-ttu-id="5c22a-127">Перемещение кнопки «расширение»</span><span class="sxs-lookup"><span data-stu-id="5c22a-127">Moving the extension button</span></span>
<span data-ttu-id="5c22a-128">В зависимости от параметров расширения оно может отображаться в меню "Дополнительно" **(...)** .</span><span class="sxs-lookup"><span data-stu-id="5c22a-128">Depending on your extension's settings, it could appear in the **More (...)** menu.</span></span>

   ![меню "действия"](./../media/browseraction.png)  


<span data-ttu-id="5c22a-130">Если вы хотите упростить доступ к кнопке, перетащите ее из этого меню.</span><span class="sxs-lookup"><span data-stu-id="5c22a-130">If you want to move the button out of this menu for easier access:</span></span>

1. <span data-ttu-id="5c22a-131">Щелкните правой кнопкой мыши кнопку "расширение".</span><span class="sxs-lookup"><span data-stu-id="5c22a-131">Right-click the extension button.</span></span>

2. <span data-ttu-id="5c22a-132">Нажмите **кнопку Показать рядом с адресной строкой**.</span><span class="sxs-lookup"><span data-stu-id="5c22a-132">Select **Show button next to address bar**.</span></span>

   ![меню "действия"](./../media/browseraction_contextmenu.png)  

<span data-ttu-id="5c22a-134">Кроме того, вы можете сделать это на странице сведения о расширениях.</span><span class="sxs-lookup"><span data-stu-id="5c22a-134">Alternatively, you may do this from the extensions details page:</span></span>

1. <span data-ttu-id="5c22a-135">Нажмите кнопку "расширение".</span><span class="sxs-lookup"><span data-stu-id="5c22a-135">Click on the extension button.</span></span>
2. <span data-ttu-id="5c22a-136">Включите переключатель **Показать рядом с адресной строкой** .</span><span class="sxs-lookup"><span data-stu-id="5c22a-136">Toggle **Show button next to address bar** to on.</span></span>

   ![переключатель "Показать"](./../media/show-button-toggle.png)

> [!NOTE]
> <span data-ttu-id="5c22a-138">Вы всегда можете переместить кнопку назад в меню **Дополнительно (...)** , щелкнув его правой кнопкой мыши и отменив флажок **Показать рядом с адресной строкой** или перейдя на страницу сведений о расширении и нажав **кнопку Показать рядом с пунктом адресная строка** .</span><span class="sxs-lookup"><span data-stu-id="5c22a-138">You can always move the button back to the **More (...)** menu by right-clicking it and unselecting **Show next to address bar** or by going to the extension details page and toggling **Show button next to address bar** to off.</span></span>


## <span data-ttu-id="5c22a-139">Удаление расширения</span><span class="sxs-lookup"><span data-stu-id="5c22a-139">Removing an extension</span></span>

1. <span data-ttu-id="5c22a-140">Откройте Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5c22a-140">Open Microsoft Edge.</span></span>

2. <span data-ttu-id="5c22a-141">Нажмите кнопку **Дополнительно (...)** , чтобы открыть меню.</span><span class="sxs-lookup"><span data-stu-id="5c22a-141">Select **More (...)** to open the menu.</span></span>

3. <span data-ttu-id="5c22a-142">В меню выберите пункт **расширения** .</span><span class="sxs-lookup"><span data-stu-id="5c22a-142">Select **Extensions** from the menu.</span></span>

4. <span data-ttu-id="5c22a-143">Щелкните правой кнопкой мыши расширение, которое вы хотите удалить, и выберите пункт **Удалить**, а затем нажмите кнопку **Удалить** .</span><span class="sxs-lookup"><span data-stu-id="5c22a-143">Right-click the extension you want to remove and select **Remove**, or select the extension and click the **Remove** button.</span></span>

   ![меню "действия"](./../media/remove.png)  

**<span data-ttu-id="5c22a-145">Расширение должно исчезнуть из списка в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="5c22a-145">The extension should disappear from the list in Microsoft Edge.</span></span>**
