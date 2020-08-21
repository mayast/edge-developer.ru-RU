---
ms.assetid: 2ecc762c-11a5-4b16-9aed-22606c1d4994
description: Узнайте, как С помощью API веб-уведомлений можно разрешить отправку уведомлений пользователям за пределами контекста браузера Microsoft Edge.
title: API веб-уведомлений — руководство по разработке
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/28/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge, разработчики, html, css, javascript, разработчики
ms.openlocfilehash: 24b8a7b25fb3e0f0221f6d81b105d5d0374ea423
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "10941800"
---
# <span data-ttu-id="c9a04-104">API веб-уведомлений</span><span class="sxs-lookup"><span data-stu-id="c9a04-104">Web Notifications API</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="c9a04-105">API веб-уведомлений позволяет отправлять пользователям уведомления о них за пределами контекста веб-страницы в браузере Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="c9a04-105">The Web Notifications API allows websites to send users notifications outside the context of a webpage within the Microsoft Edge browser.</span></span>  <span data-ttu-id="c9a04-106">Пример использования этой функции в действии может быть вызвано приложением для обмена сообщениями, например Skype.</span><span class="sxs-lookup"><span data-stu-id="c9a04-106">An example of this feature in action would be with a messaging application like Skype.</span></span>  <span data-ttu-id="c9a04-107">Когда пользователь получит новое сообщение, на рабочем столе появляется уведомление, сообщающее его об отправке.</span><span class="sxs-lookup"><span data-stu-id="c9a04-107">When a user would receive a new message, a notification would appear on their desktop, alerting them of the message.</span></span>  <span data-ttu-id="c9a04-108">Веб-уведомления полностью интегрируются с платформой уведомлений и центром уведомлений в Windows 10.</span><span class="sxs-lookup"><span data-stu-id="c9a04-108">Web Notifications are fully integrated with the Notification Platform and the Action Center within Windows 10.</span></span>  

## <span data-ttu-id="c9a04-109">Создание уведомления</span><span class="sxs-lookup"><span data-stu-id="c9a04-109">Creating a notification</span></span>  

<span data-ttu-id="c9a04-110">Ниже создается уведомление о мехическом коде, создав объект [уведомления](https://msdn.microsoft.com/library/mt710818) [с](https://msdn.microsoft.com/library/mt710826)заголовком, [значком](https://msdn.microsoft.com/library/mt710814)и [набором](https://msdn.microsoft.com/library/mt710811) параметров текста:</span><span class="sxs-lookup"><span data-stu-id="c9a04-110">The CodePen below creates a mock Skype notification by making a [Notification](https://msdn.microsoft.com/library/mt710818) object with the [title](https://msdn.microsoft.com/library/mt710826), [icon](https://msdn.microsoft.com/library/mt710814), and [body](https://msdn.microsoft.com/library/mt710811) options set:</span></span>  

<iframe height='295' scrolling='no' title='<span data-ttu-id="c9a04-111">веб-уведомления</span><span class="sxs-lookup"><span data-stu-id="c9a04-111">Web notifications</span></span>' src='//codepen.io/MicrosoftEdgeDocumentation/embed/RGbxWW/?height=295&theme-id=23761&default-tab=result&embed-version=2&editable=true' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'><span data-ttu-id="c9a04-112">Просматривайте <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/RGbxWW/'> веб-уведомления </a> к аркету с помощью документов на Microsoft Edge <a href='https://codepen.io/MicrosoftEdgeDocumentation'> </a> (@MicrosoftEdgeDocumentation) на <a href='https://codepen.io'> кодировке </a> кода.</span><span class="sxs-lookup"><span data-stu-id="c9a04-112">See the Pen <a href='https://codepen.io/MicrosoftEdgeDocumentation/pen/RGbxWW/'>Web notifications</a> by Microsoft Edge Docs (<a href='https://codepen.io/MicrosoftEdgeDocumentation'>@MicrosoftEdgeDocumentation</a>) on <a href='https://codepen.io'>CodePen</a>.</span></span></iframe>  

<span data-ttu-id="c9a04-113">Настоятельно рекомендуется использовать **значок** для каждого уведомления.</span><span class="sxs-lookup"><span data-stu-id="c9a04-113">It is strongly recommended that an **icon** be specified for each notification.</span></span>  <span data-ttu-id="c9a04-114">Это позволит улучшить уведомление только от точки пользовательского пользовательского пользовательского пользовательского сайта, но и оповещать пользователей о том, с каких лицензий отправляется уведомление.</span><span class="sxs-lookup"><span data-stu-id="c9a04-114">This not only improves a notification from a UI point of view, but also helps alert users of where the notification is being sent from.</span></span>  

<span data-ttu-id="c9a04-115">Просмотрите видеоролик ниже, чтобы узнать, как создавать веб-уведомления, и узнать, как это работает в Windows 10!</span><span class="sxs-lookup"><span data-stu-id="c9a04-115">Watch the video below for a walkthrough on creating a web notification and to see it's behavior within Windows 10!</span></span>  

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Implementing-Web-Notifications/player]  

### <span data-ttu-id="c9a04-116">Свойства уведомления</span><span class="sxs-lookup"><span data-stu-id="c9a04-116">Notification properties</span></span>  

<span data-ttu-id="c9a04-117">Уведомления можно настроить следующими свойствами:</span><span class="sxs-lookup"><span data-stu-id="c9a04-117">Notifications can be set with the following properties:</span></span>  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="c9a04-118">body</span><span class="sxs-lookup"><span data-stu-id="c9a04-118">body</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/body)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="c9a04-119">Текст уведомления.</span><span class="sxs-lookup"><span data-stu-id="c9a04-119">The body text of the notification.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="c9a04-120">dir</span><span class="sxs-lookup"><span data-stu-id="c9a04-120">dir</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/dir)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="c9a04-121">Направление текста уведомления.</span><span class="sxs-lookup"><span data-stu-id="c9a04-121">The direction of the notification's text.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="c9a04-122">icon</span><span class="sxs-lookup"><span data-stu-id="c9a04-122">icon</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/icon)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="c9a04-123">URL-адрес уведомления, используемый для значка своего значка.</span><span class="sxs-lookup"><span data-stu-id="c9a04-123">The notification's URL that is used for its icon.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="c9a04-124">ланг</span><span class="sxs-lookup"><span data-stu-id="c9a04-124">lang</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/lang)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="c9a04-125">Язык уведомления.</span><span class="sxs-lookup"><span data-stu-id="c9a04-125">The language of the notification.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="c9a04-126">разрешение</span><span class="sxs-lookup"><span data-stu-id="c9a04-126">permission</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/permission)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="c9a04-127">В текущем уведомлении отображается разрешение, предоставленное пользователю для текущего оригинала.</span><span class="sxs-lookup"><span data-stu-id="c9a04-127">The current notification display permission the user has granted for the current origin.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="c9a04-128">tag</span><span class="sxs-lookup"><span data-stu-id="c9a04-128">tag</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/tag)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="c9a04-129">Тег уведомления.</span><span class="sxs-lookup"><span data-stu-id="c9a04-129">The tag of the notification.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="c9a04-130">title</span><span class="sxs-lookup"><span data-stu-id="c9a04-130">title</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/title)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="c9a04-131">Название уведомления.</span><span class="sxs-lookup"><span data-stu-id="c9a04-131">The title of the notification.</span></span>  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="c9a04-132">События уведомлений</span><span class="sxs-lookup"><span data-stu-id="c9a04-132">Notification events</span></span>  

<span data-ttu-id="c9a04-133">Следующие события используются в объекте [уведомления:](https://developer.mozilla.org/docs/Web/API/Notification)</span><span class="sxs-lookup"><span data-stu-id="c9a04-133">The following events are used with the [Notification](https://developer.mozilla.org/docs/Web/API/Notification) object:</span></span>  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="c9a04-134">onclick</span><span class="sxs-lookup"><span data-stu-id="c9a04-134">onclick</span></span>](https://developer.mozilla.org/docs/Web/API/Element/click_event)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="c9a04-135">Выбирайте уведомление, нажав ширину.</span><span class="sxs-lookup"><span data-stu-id="c9a04-135">Fires when a notification is clicked by the user.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="c9a04-136">onclose</span><span class="sxs-lookup"><span data-stu-id="c9a04-136">onclose</span></span>](https://developer.mozilla.org/docs/Archive/Mozilla/XUL/Events/close_event)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="c9a04-137">Получайте уведомления, когда пользователь закрывает уведомление или автоматические ожидания.</span><span class="sxs-lookup"><span data-stu-id="c9a04-137">Fires when a notification is closed by the user or an auto timeout.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="c9a04-138">onerror</span><span class="sxs-lookup"><span data-stu-id="c9a04-138">onerror</span></span>](https://developer.mozilla.org/docs/Web/API/Element/error_event)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="c9a04-139">Исчезновение ошибки при обработке уведомления.</span><span class="sxs-lookup"><span data-stu-id="c9a04-139">Fires when an error occurs while handling a notification.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="c9a04-140">onshow</span><span class="sxs-lookup"><span data-stu-id="c9a04-140">onshow</span></span>](https://developer.mozilla.org/docs/Web/API/Element/show_event)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="c9a04-141">Появляются уведомления.</span><span class="sxs-lookup"><span data-stu-id="c9a04-141">Fires when a notification is displayed.</span></span>  
   :::column-end:::
:::row-end:::  

### <span data-ttu-id="c9a04-142">Способы уведомлений</span><span class="sxs-lookup"><span data-stu-id="c9a04-142">Notification methods</span></span>  

<span data-ttu-id="c9a04-143">В объекте Уведомления можно использовать [следующие](https://developer.mozilla.org/docs/Web/API/Notification) способы:</span><span class="sxs-lookup"><span data-stu-id="c9a04-143">The following methods are used with the [Notification](https://developer.mozilla.org/docs/Web/API/Notification) object:</span></span>  

:::row:::
   :::column span="1":::
      [<span data-ttu-id="c9a04-144">close</span><span class="sxs-lookup"><span data-stu-id="c9a04-144">close</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/close)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="c9a04-145">Закрывает отображаемое уведомление.</span><span class="sxs-lookup"><span data-stu-id="c9a04-145">Closes a displayed notification.</span></span>  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      [<span data-ttu-id="c9a04-146">запросразрешения</span><span class="sxs-lookup"><span data-stu-id="c9a04-146">requestPermission</span></span>](https://developer.mozilla.org/docs/Web/API/Notification/requestPermission)  
   :::column-end:::
   :::column span="2":::
      <span data-ttu-id="c9a04-147">Запросы на разрешение пользователя, позволяющие разрешить отображение уведомлений текущим оригиналом.</span><span class="sxs-lookup"><span data-stu-id="c9a04-147">Requests permission from the user to allow notifications to be displayed by the current origin.</span></span>  
   :::column-end:::
:::row-end:::  

## <span data-ttu-id="c9a04-148">Разрешения для уведомлений</span><span class="sxs-lookup"><span data-stu-id="c9a04-148">Notification permissions</span></span>  

<span data-ttu-id="c9a04-149">Microsoft Edge позволяет пользователям управлять разрешениями для каждого отдельного домена веб-сайтов.</span><span class="sxs-lookup"><span data-stu-id="c9a04-149">Microsoft Edge allows users to manage notifications permissions for each specific website domain.</span></span>  <span data-ttu-id="c9a04-150">При появлении сообщения о **Yes** том, что в домене потребуется выбрать "Да" **или "Нет".**</span><span class="sxs-lookup"><span data-stu-id="c9a04-150">It's up to the user to either select **Yes** or **No** when asked by the domain to let it show notifications.</span></span>  <span data-ttu-id="c9a04-151">[Метод запроса Permission](https://developer.mozilla.org/docs/Web/API/Notification/requestPermission) (сигнал из-за параметров разрешений) используется для сигнала в состоянии разрешений. `granted` `denied` `default`</span><span class="sxs-lookup"><span data-stu-id="c9a04-151">The [requestPermission](https://developer.mozilla.org/docs/Web/API/Notification/requestPermission) method is used to signal the permission state as either `granted`, `denied`, or `default`.</span></span>  <span data-ttu-id="c9a04-152">Значение указывает на то, что пользователь не принял `default` решение, которое видно как эквивалент. `denied`</span><span class="sxs-lookup"><span data-stu-id="c9a04-152">A value of `default` indicates that the user hasn't made a decision, which is seen as the equivalent of `denied`.</span></span>  

## <span data-ttu-id="c9a04-153">Справочные материалы по API</span><span class="sxs-lookup"><span data-stu-id="c9a04-153">API reference</span></span>  

[<span data-ttu-id="c9a04-154">Веб-уведомления</span><span class="sxs-lookup"><span data-stu-id="c9a04-154">Web Notifications</span></span>](https://developer.mozilla.org/docs/Web/API/Notifications_API)  

## <span data-ttu-id="c9a04-155">Спецификаци</span><span class="sxs-lookup"><span data-stu-id="c9a04-155">Specification</span></span>  

[<span data-ttu-id="c9a04-156">Веб-уведомления</span><span class="sxs-lookup"><span data-stu-id="c9a04-156">Web Notifications</span></span>](https://notifications.spec.whatwg.org)  
