---
ms.assetid: ''
description: Вы можете безопасно экспериментировать в течение определенного периода времени и предоставлять отзыв о новых возможностях платформы.
title: Исходные пробные версии
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 06/29/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: EDGE, веб-разработка, HTML, CSS, пробные версии, разработчик
ms.openlocfilehash: 470896435ab348419749a7de00adcdb83b784df3
ms.sourcegitcommit: 5cbc9237363b3a8ba212ca128aa03c71a33ec86f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/02/2020
ms.locfileid: "10846530"
---
# <span data-ttu-id="a9b6f-104">Использование пробного источника в Microsoft Edge</span><span class="sxs-lookup"><span data-stu-id="a9b6f-104">Use Origin Trials in Microsoft Edge</span></span>  

<span data-ttu-id="a9b6f-105">Разработчики могут использовать пробные версии для пробного использования экспериментальных API на реальных сайтах в течение ограниченного периода времени.</span><span class="sxs-lookup"><span data-stu-id="a9b6f-105">Developers may use Origin Trials to try out experimental APIs on live sites for a limited period of time.</span></span>  <span data-ttu-id="a9b6f-106">Если вы используете пробные версии, пользователи Microsoft EDGE, которые посещает сайт, могут выполнять код, использующий экспериментальные API.</span><span class="sxs-lookup"><span data-stu-id="a9b6f-106">When using Origin Trials, users of Microsoft Edge that visit your site may run code that uses experimental APIs.</span></span>  <span data-ttu-id="a9b6f-107">Для доступа к экспериментальным API-интерфейсам на компьютерах пользователей нет необходимости `edge://flags` включать и отключать флаги компонентов.</span><span class="sxs-lookup"><span data-stu-id="a9b6f-107">To access the experimental APIs on each user machine, you do not need to go to `edge://flags` and turn on feature flags.</span></span>  <span data-ttu-id="a9b6f-108">Дополнительные сведения можно найти в [экспериментальных API-интерфейсах][DeveloperMicrsoftEdgeOriginTrials].</span><span class="sxs-lookup"><span data-stu-id="a9b6f-108">For more information, see [experimental APIs][DeveloperMicrsoftEdgeOriginTrials].</span></span>  <span data-ttu-id="a9b6f-109">Кроме того, вы можете отправить отзыв по проектированию API, вариантов использования или вашего интерфейса, используя API для инженеров браузера и веб-стандартных сообществ.</span><span class="sxs-lookup"><span data-stu-id="a9b6f-109">Additionally, you may provide feedback on the design of the API, your use cases, or your experience using the APIs to browser engineers and the web standard community.</span></span>  

## <span data-ttu-id="a9b6f-110">Приступая к работе с исходными пробными версии</span><span class="sxs-lookup"><span data-stu-id="a9b6f-110">Get started using Origin Trials</span></span>  

<span data-ttu-id="a9b6f-111">Дополнительные сведения о экспериментальных API, доступных в Microsoft EDGE, можно найти в [консоли разработчика бета-версии Microsoft Edge][DeveloperMicrsoftEdgeOriginTrials].</span><span class="sxs-lookup"><span data-stu-id="a9b6f-111">For more information about the experimental APIs available in Microsoft Edge, see [Microsoft Edge Origin Trials Developer Console][DeveloperMicrsoftEdgeOriginTrials].</span></span>  <span data-ttu-id="a9b6f-112">Убедитесь, что вы просматриваете минимальные требования к версиям Microsoft EDGE и Дата окончания срока действия, чтобы оценить пригодность использования экспериментальных API на вашем веб-сайте.</span><span class="sxs-lookup"><span data-stu-id="a9b6f-112">Ensure that you review the minimum version requirements for Microsoft Edge, and the trial end date to assess suitability of using the experimental APIs on your website.</span></span>  

> [!NOTE]
> <span data-ttu-id="a9b6f-113">Эксперименты могут заканчиваться раньше, чем планировалось, если возникает одна из указанных ниже ситуаций.</span><span class="sxs-lookup"><span data-stu-id="a9b6f-113">An experiment may end earlier than planned if any of the following situations occur.</span></span>  
> *   <span data-ttu-id="a9b6f-114">Основной инцидент безопасности.</span><span class="sxs-lookup"><span data-stu-id="a9b6f-114">A major security incident.</span></span>  
> *   <span data-ttu-id="a9b6f-115">Если будет соблюдаться необходимая обратная связь, указывающая на необходимость крупного оформления, чтобы удовлетворить потребности веб-разработчиков.</span><span class="sxs-lookup"><span data-stu-id="a9b6f-115">If sufficient feedback is collected that indicates a major redesign is needed to meet the needs of web developers.</span></span>  
> <span data-ttu-id="a9b6f-116">В обоих случаях для всех разработчиков, которые в настоящее время зарегистрированы в эксперименте, отправляется сообщение электронной почты с уведомлением.</span><span class="sxs-lookup"><span data-stu-id="a9b6f-116">In either case, a notification email is sent to all developers currently enrolled in the experiment.</span></span>  

### <span data-ttu-id="a9b6f-117">Регистрация пробного использования экспериментального API</span><span class="sxs-lookup"><span data-stu-id="a9b6f-117">Register for a trial of an experimental API</span></span>  

<span data-ttu-id="a9b6f-118">Выполните указанные ниже действия, чтобы выполнить регистрацию для пробной версии экспериментального API.</span><span class="sxs-lookup"><span data-stu-id="a9b6f-118">Use the following steps to register for a trial of an experimental API.</span></span>  

1.  <span data-ttu-id="a9b6f-119">Посетите [Консоль разработчика бета-версии Microsoft Edge][DeveloperMicrsoftEdgeOriginTrials] .</span><span class="sxs-lookup"><span data-stu-id="a9b6f-119">Visit the [Microsoft Edge Origin Trials Developer Console][DeveloperMicrsoftEdgeOriginTrials] page.</span></span>  
1.  <span data-ttu-id="a9b6f-120">Нажмите кнопку "зарегистрировать" на любом из доступных экспериментов.</span><span class="sxs-lookup"><span data-stu-id="a9b6f-120">Choose the Register button on any of the available experiments.</span></span>  
1.  <span data-ttu-id="a9b6f-121">Войдите в консоль разработчика с помощью имени пользователя и пароля GitHub.</span><span class="sxs-lookup"><span data-stu-id="a9b6f-121">Sign into the Developer Console using your GitHub username and password.</span></span>  
1.  <span data-ttu-id="a9b6f-122">Выберите **авторизовать MicrosoftEdge**.</span><span class="sxs-lookup"><span data-stu-id="a9b6f-122">Choose **Authorize MicrosoftEdge**.</span></span>  
1.  <span data-ttu-id="a9b6f-123">Заполните форму.</span><span class="sxs-lookup"><span data-stu-id="a9b6f-123">Complete the form.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="a9b6f-124">Чтобы зарегистрировать один или все дочерние домены, выберите `Do you need to match all subdomains for the provided origin?` параметр Задать `Yes` .</span><span class="sxs-lookup"><span data-stu-id="a9b6f-124">To enroll a single or all subdomains, choose set the `Do you need to match all subdomains for the provided origin?` setting to `Yes`.</span></span>  <span data-ttu-id="a9b6f-125">Например, `https://dev.contoso.com` является единственным доменом и `https://*.contoso.com` использует подстановочный знак для представления всех поддоменов.</span><span class="sxs-lookup"><span data-stu-id="a9b6f-125">For example, `https://dev.contoso.com` is a single domain, and `https://*.contoso.com` uses a wildcard to represent all subdomains.</span></span>  
    
    > [!IMPORTANT]
    > <span data-ttu-id="a9b6f-126">Следующие форматы источника не допускаются.</span><span class="sxs-lookup"><span data-stu-id="a9b6f-126">The following origin formats are not allowed.</span></span>  
    > *   <span data-ttu-id="a9b6f-127">Указание вложенной папки в исходном расположении.</span><span class="sxs-lookup"><span data-stu-id="a9b6f-127">Specifying a subfolder on the origin.</span></span>  <span data-ttu-id="a9b6f-128">Например:</span><span class="sxs-lookup"><span data-stu-id="a9b6f-128">For example,</span></span> `https://contoso.com/path/subfolder`  
    > 
    > *   <span data-ttu-id="a9b6f-129">Использование источника с параметрами строки запроса.</span><span class="sxs-lookup"><span data-stu-id="a9b6f-129">Using an origin with query string parameters.</span></span>  <span data-ttu-id="a9b6f-130">Например:</span><span class="sxs-lookup"><span data-stu-id="a9b6f-130">For example,</span></span> `https://contoso.com/path/feature?query_parameter=12345`  
    
1.  <span data-ttu-id="a9b6f-131">Нажмите кнопку **сохранить и зарегистрировать**.</span><span class="sxs-lookup"><span data-stu-id="a9b6f-131">Choose **ACCEPT and REGISTER**.</span></span>  

### <span data-ttu-id="a9b6f-132">Применение маркера</span><span class="sxs-lookup"><span data-stu-id="a9b6f-132">Apply your token</span></span>  

<span data-ttu-id="a9b6f-133">Маркер мгновенно создается и отображается на странице [консоли разработчика бета-версии Microsoft Edge][DeveloperMicrsoftEdgeOriginTrials] .</span><span class="sxs-lookup"><span data-stu-id="a9b6f-133">A token is instantly generated and displayed on the [Microsoft Edge Origin Trials Developer Console][DeveloperMicrsoftEdgeOriginTrials] page.</span></span>  <span data-ttu-id="a9b6f-134">Чтобы начать использовать пробную версию на своем веб-сайте, воспользуйтесь одним из описанных ниже способов применения маркера к странице.</span><span class="sxs-lookup"><span data-stu-id="a9b6f-134">To begin using the trial on your website, use either of the following methods to apply the token to your page.</span></span>  

*   <span data-ttu-id="a9b6f-135">Добавьте `origin-trial` значение атрибута и маркер в `meta` тег на каждой странице, использующей экспериментальный API.</span><span class="sxs-lookup"><span data-stu-id="a9b6f-135">Add the `origin-trial` attribute value and your token to the `meta` tag on every page that uses the experimental API.</span></span>  
    
    ```html
    <meta http-equiv="origin-trial" content="replace-with-your-token">
    ```  
    
*   <span data-ttu-id="a9b6f-136">Добавьте `Origin-Trial` в заголовок HTTP-ответа сервера.</span><span class="sxs-lookup"><span data-stu-id="a9b6f-136">Add `Origin-Trial` to the HTTP response header of your server.</span></span>  
    
    ```json
    Origin-Trial: replace-with-your-token
    ```  
    
> [!NOTE]
> <span data-ttu-id="a9b6f-137">Маркер действителен в течение 6 недель.</span><span class="sxs-lookup"><span data-stu-id="a9b6f-137">Your token is valid for 6 weeks.</span></span>  <span data-ttu-id="a9b6f-138">До окончания срока действия пробной версии вы отправляете напоминания о том, что запросите свое мнение и попросите подтвердить продление пробной версии.</span><span class="sxs-lookup"><span data-stu-id="a9b6f-138">Before your trial ends, reminder emails are sent to you that ask for your feedback and ask you to consider renewing your trial before your token expires.</span></span>  

### <span data-ttu-id="a9b6f-139">Отказ от эксперимента</span><span class="sxs-lookup"><span data-stu-id="a9b6f-139">Opt out of an experiment</span></span>  

<span data-ttu-id="a9b6f-140">Чтобы отказаться от эксперимента, воспользуйтесь одним из описанных ниже способов, чтобы удалить маркер.</span><span class="sxs-lookup"><span data-stu-id="a9b6f-140">To opt out of an experiment, use one of the following methods to remove your token.</span></span>  

*   <span data-ttu-id="a9b6f-141">Удалите `meta` тег с каждой страницы, использующей экспериментальный API.</span><span class="sxs-lookup"><span data-stu-id="a9b6f-141">Remove the `meta` tag from every page that used the experimental API.</span></span>  
    
    ```html
    <meta http-equiv="origin-trial" content="your-token">
    ```  
    
*   <span data-ttu-id="a9b6f-142">Удалите `Origin-Trial` из заголовка HTTP-ответа сервера.</span><span class="sxs-lookup"><span data-stu-id="a9b6f-142">Remove `Origin-Trial` from the HTTP response header of your server.</span></span>  
    
    ```json
    Origin-Trial: your-token
    ```  
    
### <span data-ttu-id="a9b6f-143">Определение экспериментальных функций и предоставление резервного</span><span class="sxs-lookup"><span data-stu-id="a9b6f-143">Detect experimental features and provide a fallback</span></span>  

<span data-ttu-id="a9b6f-144">При использовании экспериментальных API-интерфейсов убедитесь в том, что вы предоставляете рабочие возможности для всех посетителей сайта.</span><span class="sxs-lookup"><span data-stu-id="a9b6f-144">When using experimental APIs, ensure you provide a working experience to all visitors of your website.</span></span>  <span data-ttu-id="a9b6f-145">Посетители могут использовать браузеры, которые не поддерживают экспериментальные API-интерфейсы, добавленные в код.</span><span class="sxs-lookup"><span data-stu-id="a9b6f-145">Visitors may use browsers that do not support the experimental APIs that you added to your code.</span></span>  <span data-ttu-id="a9b6f-146">Кроме того, если срок действия маркера истекает до его возобновления, экспериментальный API будет недоступен, что может привести к ошибкам.</span><span class="sxs-lookup"><span data-stu-id="a9b6f-146">Additionally, if your token expires before you renew it, the experimental API is no longer available which may result in errors.</span></span>  <span data-ttu-id="a9b6f-147">Чтобы избежать такой ситуации, убедитесь в том, что вы определяете возможности, доступные в браузере.</span><span class="sxs-lookup"><span data-stu-id="a9b6f-147">To avoid this situation, ensure you detect features available in your browser.</span></span>  <span data-ttu-id="a9b6f-148">Дополнительные сведения можно найти в разделе [Реализация обнаружения функций][MDNImplementingFeatureDetection].</span><span class="sxs-lookup"><span data-stu-id="a9b6f-148">For more information, see [Implementing feature detection][MDNImplementingFeatureDetection].</span></span>

### <span data-ttu-id="a9b6f-149">Планы для разрешенных источников</span><span class="sxs-lookup"><span data-stu-id="a9b6f-149">Roadmap for Allowed Origins</span></span>  

<span data-ttu-id="a9b6f-150">Сегодня портал бета-версии Microsoft EDGE поддерживает только источники, поддерживающие SSL, а это означает, что веб-сайты должны правильно реализовывать HTTPS, чтобы зарегистрироваться для эксперимента.</span><span class="sxs-lookup"><span data-stu-id="a9b6f-150">The Microsoft Edge Origin Trials portal today only supports SSL Enabled Origins, which means that websites must have HTTPS properly implemented to register for an experiment.</span></span>  <span data-ttu-id="a9b6f-151">В будущем запланированы следующие безопасные источники.</span><span class="sxs-lookup"><span data-stu-id="a9b6f-151">In the future, the following secure origins are planned.</span></span>  

*   <span data-ttu-id="a9b6f-152">Зарегистрируйтесь в `http://localhost` качестве источника экспериментов.</span><span class="sxs-lookup"><span data-stu-id="a9b6f-152">Register `http://localhost` as the origin for your experiments.</span></span>  <span data-ttu-id="a9b6f-153">Чтобы использовать `http://localhost` текущую версию, перейдите к шагу `edge://flags` и установите для него значение **Enabled (включено**).</span><span class="sxs-lookup"><span data-stu-id="a9b6f-153">To use `http://localhost` today, go to `edge://flags` and set the experiment to **Enabled**.</span></span>  
*   <span data-ttu-id="a9b6f-154">Используйте расширения с предварительно `extensions://` фиксированными источниками для регистрации в экспериментах.</span><span class="sxs-lookup"><span data-stu-id="a9b6f-154">Use extensions with `extensions://` prefixed origins to enroll in experiments.</span></span>  
    
<!-- links -->  

[DeveloperMicrsoftEdgeOriginTrials]: https://developer.microsoft.com/microsoft-edge/origin-trials "Консоль разработчика "пробные источники Microsoft Edge" | Документы Microsoft"  

[MDNImplementingFeatureDetection]: https://developer.mozilla.org/docs/learn/tools_and_testing/cross_browser_testing/feature_detection "Реализация обнаружения компонентов | MDN"  
