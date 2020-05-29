---
ms.assetid: 2ecc762c-11a5-4b16-9aed-22606c1d4994
description: Сведения о том, как можно использовать API веб-уведомлений, чтобы разрешить веб-сайтам отправлять уведомления пользователей за пределами контекста браузера Microsoft Edge.
title: 'Руководство для разработчиков: API веб-уведомлений'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 10/18/2017
ms.topic: article
ms.prod: microsoft-edge
keywords: EDGE, веб-разработка, HTML, CSS, JavaScript, разработчик
ms.openlocfilehash: da563a333491ef699925adec6f97b3c21d3e54a0
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571239"
---
# <span data-ttu-id="68619-104">API веб-уведомлений</span><span class="sxs-lookup"><span data-stu-id="68619-104">Web Notifications API</span></span>

<span data-ttu-id="68619-105">API веб-уведомлений позволяет веб-сайтам отправлять уведомления пользователей за пределами контекста веб-страницы в браузере Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="68619-105">The Web Notifications API allows websites to send users notifications outside the context of a webpage within the Microsoft Edge browser.</span></span> <span data-ttu-id="68619-106">Примером этой функции в действии может быть приложение для обмена сообщениями, например Skype.</span><span class="sxs-lookup"><span data-stu-id="68619-106">An example of this feature in action would be with a messaging application like Skype.</span></span> <span data-ttu-id="68619-107">Когда пользователь получит новое сообщение, на его рабочем столе появится уведомление о сообщении.</span><span class="sxs-lookup"><span data-stu-id="68619-107">When a user would receive a new message, a notification would appear on their desktop, alerting them of the message.</span></span> <span data-ttu-id="68619-108">Веб-уведомления полностью интегрированы с платформой уведомлений и центром действий в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="68619-108">Web Notifications are fully integrated with the Notification Platform and the Action Center within Windows 10.</span></span> 

## <span data-ttu-id="68619-109">Создание уведомления</span><span class="sxs-lookup"><span data-stu-id="68619-109">Creating a notification</span></span>

<span data-ttu-id="68619-110">На CodePen рисунке ниже показано, как создать фиктивное уведомление Skype, сделав [`Notification`](https://msdn.microsoft.com/library/mt710818) объект с [`title`](https://msdn.microsoft.com/library/mt710826) [`icon`](https://msdn.microsoft.com/library/mt710814) [`body`](https://msdn.microsoft.com/library/mt710811) установленным флажком "и".</span><span class="sxs-lookup"><span data-stu-id="68619-110">The CodePen below creates a mock Skype notification by making a [`Notification`](https://msdn.microsoft.com/library/mt710818) object with the [`title`](https://msdn.microsoft.com/library/mt710826), [`icon`](https://msdn.microsoft.com/library/mt710814), and [`body`](https://msdn.microsoft.com/library/mt710811) options set:</span></span>


<iframe height='295' scrolling='no' title='<span data-ttu-id="68619-111">Веб-уведомления</span><span class="sxs-lookup"><span data-stu-id="68619-111">Web notifications</span></span>' src='//codepen.io/MicrosoftEdgeDocumentation/embed/RGbxWW/?height=295&theme-id=23761&default-tab=result&embed-version=2&editable=true' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'><span data-ttu-id="68619-112">Ознакомьтесь <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/RGbxWW/'> с веб-уведомлениями о перьях </a> по Microsoft Edge Docs ( <a href='https://codepen.io/MicrosoftEdgeDocumentation'> @MicrosoftEdgeDocumentation </a> ) на <a href='https://codepen.io'> CodePen </a> .</span><span class="sxs-lookup"><span data-stu-id="68619-112">See the Pen <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/RGbxWW/'>Web notifications</a> by Microsoft Edge Docs (<a href='https://codepen.io/MicrosoftEdgeDocumentation'>@MicrosoftEdgeDocumentation</a>) on <a href='https://codepen.io'>CodePen</a>.</span></span>
</iframe>

<span data-ttu-id="68619-113">Настоятельно рекомендуется `icon` указывать для каждого уведомления.</span><span class="sxs-lookup"><span data-stu-id="68619-113">It is strongly recommended that an `icon` be specified for each notification.</span></span> <span data-ttu-id="68619-114">Это не только улучшит уведомления с точки зрения пользовательского интерфейса, но и позволяет оповещать пользователей о том, где отправляются уведомления.</span><span class="sxs-lookup"><span data-stu-id="68619-114">This not only improves a notification from a UI point of view, but also helps alert users of where the notification is being sent from.</span></span>

<span data-ttu-id="68619-115">Посмотрите видеоролик ниже, в котором показано, как создать веб-оповещение и узнать, как это происходит в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="68619-115">Watch the video below for a walkthrough on creating a web notification and to see it's behavior within Windows 10!</span></span>


> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Implementing-Web-Notifications/player]

### <span data-ttu-id="68619-116">Свойства уведомлений</span><span class="sxs-lookup"><span data-stu-id="68619-116">Notification properties</span></span>

<span data-ttu-id="68619-117">Уведомления можно настроить с помощью следующих параметров:</span><span class="sxs-lookup"><span data-stu-id="68619-117">Notifications can be set with the following options:</span></span>

<span data-ttu-id="68619-118">Свойство</span><span class="sxs-lookup"><span data-stu-id="68619-118">Property</span></span> | <span data-ttu-id="68619-119">Описание</span><span class="sxs-lookup"><span data-stu-id="68619-119">Description</span></span>
:-------- | :----------
[<span data-ttu-id="68619-120">body</span><span class="sxs-lookup"><span data-stu-id="68619-120">body</span></span>](https://msdn.microsoft.com/library/mt710811) | <span data-ttu-id="68619-121">Основной текст уведомления.</span><span class="sxs-lookup"><span data-stu-id="68619-121">The body text of the notification.</span></span>
[<span data-ttu-id="68619-122">dir</span><span class="sxs-lookup"><span data-stu-id="68619-122">dir</span></span>](https://msdn.microsoft.com/library/mt710813) | <span data-ttu-id="68619-123">Направление текста уведомления.</span><span class="sxs-lookup"><span data-stu-id="68619-123">The direction of the notification's text.</span></span>
[<span data-ttu-id="68619-124">icon</span><span class="sxs-lookup"><span data-stu-id="68619-124">icon</span></span>](https://msdn.microsoft.com/library/mt710814) | <span data-ttu-id="68619-125">URL-адрес уведомления, который используется для его значка.</span><span class="sxs-lookup"><span data-stu-id="68619-125">The notification's URL that is used for its icon.</span></span>
[<span data-ttu-id="68619-126">файл</span><span class="sxs-lookup"><span data-stu-id="68619-126">lang</span></span>](https://msdn.microsoft.com/library/mt710815) | <span data-ttu-id="68619-127">Язык уведомления.</span><span class="sxs-lookup"><span data-stu-id="68619-127">The language of the notification.</span></span>
[<span data-ttu-id="68619-128">PermissionSet</span><span class="sxs-lookup"><span data-stu-id="68619-128">permission</span></span>](https://msdn.microsoft.com/library/mt670637) | <span data-ttu-id="68619-129">Текущее разрешение на отображение уведомления, предоставленное пользователем для текущего происхождения.</span><span class="sxs-lookup"><span data-stu-id="68619-129">The current notification display permission the user has granted for the current origin.</span></span>
[<span data-ttu-id="68619-130">tag</span><span class="sxs-lookup"><span data-stu-id="68619-130">tag</span></span>](https://msdn.microsoft.com/library/mt710825) | <span data-ttu-id="68619-131">Тег уведомления.</span><span class="sxs-lookup"><span data-stu-id="68619-131">The tag of the notification.</span></span>
[<span data-ttu-id="68619-132">title</span><span class="sxs-lookup"><span data-stu-id="68619-132">title</span></span>](https://msdn.microsoft.com/library/mt710826) | <span data-ttu-id="68619-133">Название уведомления.</span><span class="sxs-lookup"><span data-stu-id="68619-133">The title of the notification.</span></span>

### <span data-ttu-id="68619-134">События уведомления</span><span class="sxs-lookup"><span data-stu-id="68619-134">Notification events</span></span>

<span data-ttu-id="68619-135">С объектом используются следующие события [`Notification`](https://msdn.microsoft.com/library/mt710818) :</span><span class="sxs-lookup"><span data-stu-id="68619-135">The following events are used with the [`Notification`](https://msdn.microsoft.com/library/mt710818) object:</span></span>

<span data-ttu-id="68619-136">Событие</span><span class="sxs-lookup"><span data-stu-id="68619-136">Event</span></span> | <span data-ttu-id="68619-137">Описание</span><span class="sxs-lookup"><span data-stu-id="68619-137">Description</span></span>
:-------- | :----------
[<span data-ttu-id="68619-138">OnClick</span><span class="sxs-lookup"><span data-stu-id="68619-138">onclick</span></span>](https://msdn.microsoft.com/library/mt712180) | <span data-ttu-id="68619-139">Активируется при щелчке уведомления пользователем.</span><span class="sxs-lookup"><span data-stu-id="68619-139">Fires when a notification is clicked by the user.</span></span>
[<span data-ttu-id="68619-140">OnClose (закрыть)</span><span class="sxs-lookup"><span data-stu-id="68619-140">onclose</span></span>](https://msdn.microsoft.com/library/mt712178) | <span data-ttu-id="68619-141">Активируется при закрытии уведомления пользователем или автоматическим тайм-аутам.</span><span class="sxs-lookup"><span data-stu-id="68619-141">Fires when a notification is closed by the user or an auto timeout.</span></span>
[<span data-ttu-id="68619-142">ПриОшибке</span><span class="sxs-lookup"><span data-stu-id="68619-142">onerror</span></span>](https://msdn.microsoft.com/library/mt712181) | <span data-ttu-id="68619-143">Активируется при возникновении ошибки при обработке уведомления.</span><span class="sxs-lookup"><span data-stu-id="68619-143">Fires when an error occurs while handling a notification.</span></span>
[<span data-ttu-id="68619-144">onShow</span><span class="sxs-lookup"><span data-stu-id="68619-144">onshow</span></span>](https://msdn.microsoft.com/library/mt712182) | <span data-ttu-id="68619-145">Активируется при отображении уведомления.</span><span class="sxs-lookup"><span data-stu-id="68619-145">Fires when a notification is displayed.</span></span>

### <span data-ttu-id="68619-146">Способы уведомления</span><span class="sxs-lookup"><span data-stu-id="68619-146">Notification methods</span></span>

<span data-ttu-id="68619-147">С объектом используются следующие методы [`Notification`](https://msdn.microsoft.com/library/mt710818) :</span><span class="sxs-lookup"><span data-stu-id="68619-147">The following methods are used with the [`Notification`](https://msdn.microsoft.com/library/mt710818) object:</span></span>

<span data-ttu-id="68619-148">Метод</span><span class="sxs-lookup"><span data-stu-id="68619-148">Method</span></span> | <span data-ttu-id="68619-149">Описание</span><span class="sxs-lookup"><span data-stu-id="68619-149">Description</span></span>
:-------- | :----------
[<span data-ttu-id="68619-150">close</span><span class="sxs-lookup"><span data-stu-id="68619-150">close</span></span>](https://msdn.microsoft.com/library/mt670636) | <span data-ttu-id="68619-151">Закрывает открытое уведомление.</span><span class="sxs-lookup"><span data-stu-id="68619-151">Closes a displayed notification.</span></span>
[<span data-ttu-id="68619-152">requestPermission</span><span class="sxs-lookup"><span data-stu-id="68619-152">requestPermission</span></span>](https://msdn.microsoft.com/library/mt710824) | <span data-ttu-id="68619-153">Запрашивает разрешение от пользователя, чтобы разрешить отображение уведомлений текущим источником.</span><span class="sxs-lookup"><span data-stu-id="68619-153">Requests permission from the user to allow notifications to be displayed by the current origin.</span></span>

## <span data-ttu-id="68619-154">Разрешения для уведомлений</span><span class="sxs-lookup"><span data-stu-id="68619-154">Notification permissions</span></span>

<span data-ttu-id="68619-155">Microsoft EDGE позволяет пользователям управлять разрешениями уведомлений для каждого определенного домена веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="68619-155">Microsoft Edge allows users to manage notifications permissions for each specific website domain.</span></span> <span data-ttu-id="68619-156">Вы можете выбрать вариант "Да" или "нет" при появлении запроса от домена, чтобы позволить ему показывать уведомления.</span><span class="sxs-lookup"><span data-stu-id="68619-156">It's up to the user to either select "Yes" or "No" when asked by the domain to let it show notifications.</span></span> <span data-ttu-id="68619-157">[`requestPermission`](https://msdn.microsoft.com/library/mt710824)Метод используется, чтобы сообщить состояние разрешения как `granted` , так `denied` и `default` .</span><span class="sxs-lookup"><span data-stu-id="68619-157">The [`requestPermission`](https://msdn.microsoft.com/library/mt710824) method is used to signal the permission state as either `granted`, `denied`, or `default`.</span></span> <span data-ttu-id="68619-158">Значение указывает на то `default` , что пользователь не принял решение, которое рассматривается как эквивалент `denied` .</span><span class="sxs-lookup"><span data-stu-id="68619-158">A value of `default` indicates that the user hasn't made a decision, which is seen as the equivalent of `denied`.</span></span>




## <span data-ttu-id="68619-159">Справочные материалы по API</span><span class="sxs-lookup"><span data-stu-id="68619-159">API reference</span></span>

[<span data-ttu-id="68619-160">Веб-уведомления</span><span class="sxs-lookup"><span data-stu-id="68619-160">Web Notifications</span></span>](https://msdn.microsoft.com/library/mt710827)

## <span data-ttu-id="68619-161">Specification</span><span class="sxs-lookup"><span data-stu-id="68619-161">Specification</span></span>

[<span data-ttu-id="68619-162">Веб-уведомления</span><span class="sxs-lookup"><span data-stu-id="68619-162">Web Notifications</span></span>](https://notifications.spec.whatwg.org)
