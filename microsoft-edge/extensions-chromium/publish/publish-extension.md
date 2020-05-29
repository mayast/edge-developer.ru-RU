---
description: Пошаговое руководство по публикации расширений EDGE (Chromium) в Microsoft Store.
title: Публикация расширения
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 04/21/2020
ms.topic: article
ms.prod: microsoft-edge-chromium
keywords: Edge-Chromium, Разработка расширений, расширения браузера, надстройки, центр партнера, разработчик
ms.openlocfilehash: 7b5be511af1e81efd5da4fc4bc0691f317437f94
ms.sourcegitcommit: 531ec8aa1f89b28bc4d271e8e995f846f2392bc3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/29/2020
ms.locfileid: "10607380"
---
# <span data-ttu-id="23fd2-104">Публикация расширения</span><span class="sxs-lookup"><span data-stu-id="23fd2-104">Publish An Extension</span></span>  

<span data-ttu-id="23fd2-105">Опубликуйте расширение в каталоге надстроек Microsoft Edge \ (надстройки Microsoft Edge \).</span><span class="sxs-lookup"><span data-stu-id="23fd2-105">Publish your Extension on Microsoft Edge Addons catalog \(Microsoft Edge Addons\).</span></span>  <span data-ttu-id="23fd2-106">Вы должны сначала создать отправку в [центре партнера][MicrosoftPartnerCenter] и отправить его.</span><span class="sxs-lookup"><span data-stu-id="23fd2-106">You must first create a submission on [Partner Center][MicrosoftPartnerCenter] and submit it.</span></span>  <span data-ttu-id="23fd2-107">В этом документе перечислены все сведения, которые необходимо предоставить для создания отправки расширения.</span><span class="sxs-lookup"><span data-stu-id="23fd2-107">This document lists all the details that you must provide to create an Extension submission.</span></span>  

## <span data-ttu-id="23fd2-108">Подготовка</span><span class="sxs-lookup"><span data-stu-id="23fd2-108">Before You Begin</span></span>  

*   <span data-ttu-id="23fd2-109">Вы должны иметь активную учетную запись разработчика в [центре партнера][MicrosoftPartnerCenter] , чтобы отправить свое расширение в надстройки Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="23fd2-109">You must have an active developer account on [Partner Center][MicrosoftPartnerCenter] to submit your Extension in Microsoft Edge Addons.</span></span>  <span data-ttu-id="23fd2-110">Если у вас его нет, [Создайте новую учетную запись разработчика][MicrosoftPartnerCenter].</span><span class="sxs-lookup"><span data-stu-id="23fd2-110">If you do not have one, [create a new developer account][MicrosoftPartnerCenter].</span></span>  
*   <span data-ttu-id="23fd2-111">Создайте ZIP-файл пакета расширения и убедитесь, что он включает следующие файлы:</span><span class="sxs-lookup"><span data-stu-id="23fd2-111">Create a zip file of your Extension package and ensure that it contains these files:</span></span>  
    *   <span data-ttu-id="23fd2-112">Файл манифеста и его версия должны определять имя и версию расширения.</span><span class="sxs-lookup"><span data-stu-id="23fd2-112">The manifest file and it must define the name and version of your Extension.</span></span>  
    *   <span data-ttu-id="23fd2-113">Изображения и другие файлы, необходимые для вашего расширения.</span><span class="sxs-lookup"><span data-stu-id="23fd2-113">The images and other files that are required for your Extension.</span></span>  


<span data-ttu-id="23fd2-114">Если вы еще не начали создание расширения, вы можете обратиться к учебнику [Приступая к работе][ExtensionsGettingStarted] для создания расширения Microsoft Edge Chromium.</span><span class="sxs-lookup"><span data-stu-id="23fd2-114">If you have not started building an Extension, you may refer to the [Getting Started][ExtensionsGettingStarted] tutorial for building a Microsoft Edge Chromium extension.</span></span>  

<span data-ttu-id="23fd2-115">Чтобы создать отправку расширения в [центре партнера][MicrosoftPartnerCenter], выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="23fd2-115">To create an Extension submission on [Partner Center][MicrosoftPartnerCenter], follow these steps.</span></span>  

## <span data-ttu-id="23fd2-116">Шаг 1: начало новой отправки</span><span class="sxs-lookup"><span data-stu-id="23fd2-116">Step 1: Start a New Submission</span></span>  

<span data-ttu-id="23fd2-117">Перейдите на [панель мониторинга разработчика][MicrosoftPartnerCenter].</span><span class="sxs-lookup"><span data-stu-id="23fd2-117">Go to your [developer dashboard][MicrosoftPartnerCenter].</span></span>  <span data-ttu-id="23fd2-118">На странице Overview (обзор) нажмите кнопку **создать новое расширение**.</span><span class="sxs-lookup"><span data-stu-id="23fd2-118">From the Overview page, click **Create new extension**.</span></span>  

## <span data-ttu-id="23fd2-119">Шаг 2: отправка Zip-файла расширения</span><span class="sxs-lookup"><span data-stu-id="23fd2-119">Step 2: Upload Your Extension Zip File</span></span>  

<span data-ttu-id="23fd2-120">На странице **пакета** вы отправляете ZIP-файл для отправки расширения.</span><span class="sxs-lookup"><span data-stu-id="23fd2-120">The **Package** page is where you upload the zip file for your Extension submission.</span></span>  <span data-ttu-id="23fd2-121">Вы можете добавить только один пакет за раз, поэтому, если ваше расширение не завершено, вы можете отправить его в любое время, прежде чем публиковать его.</span><span class="sxs-lookup"><span data-stu-id="23fd2-121">You may only upload one package at a time, so if your Extension is not complete you may upload a work-in-progress package and update at any time before you publish it.</span></span>  <span data-ttu-id="23fd2-122">Перед загрузкой убедитесь, что ваш пакет содержит `manifest.json` файл и прекрасно работает в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="23fd2-122">Be sure that your package contains the `manifest.json` file and is working fine on Microsoft Edge prior to uploading.</span></span>  
<span data-ttu-id="23fd2-123">Добавьте пакет, перетащив его в поле Отправить, или выберите команду **Обзор файлов**.</span><span class="sxs-lookup"><span data-stu-id="23fd2-123">Upload the package by dragging it into the upload field or by selecting **Browse your files**.</span></span>  <span data-ttu-id="23fd2-124">На странице "пакет" проверяется ZIP-файл расширений и отображается сообщение о том, что **Отправка завершена или**завершилась сбоем.</span><span class="sxs-lookup"><span data-stu-id="23fd2-124">The Package page validates the Extensions zip file and displays that **success or failure status of your upload**.</span></span>  <span data-ttu-id="23fd2-125">Если пакет проходит проверку подлинности; Она успешно загружена, и вы увидите сообщение об успешном завершении.</span><span class="sxs-lookup"><span data-stu-id="23fd2-125">If the package passes validation; it is uploaded successfully and you see a success message.</span></span>  <span data-ttu-id="23fd2-126">Если пакет не прошел проверку подлинности; пакет не принят, и появляется сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="23fd2-126">If the package fails validation; the package is not accepted and you see an error message.</span></span>  <span data-ttu-id="23fd2-127">Если в пакете есть ошибки, устраните проблемы и попробуйте загрузить ее еще раз.</span><span class="sxs-lookup"><span data-stu-id="23fd2-127">If there are errors in the package, resolve the issues and try uploading it again.</span></span>  

<span data-ttu-id="23fd2-128">После успешной отправки ознакомьтесь со сведениями о расширении и нажмите кнопку **Далее** , чтобы продолжить.</span><span class="sxs-lookup"><span data-stu-id="23fd2-128">After successful upload, review your Extension details and click **Next** to proceed.</span></span>  

## <span data-ttu-id="23fd2-129">Шаг 3: предоставление сведений о доступности</span><span class="sxs-lookup"><span data-stu-id="23fd2-129">Step 3: Provide Availability details</span></span>  

### <span data-ttu-id="23fd2-130">Определение видимости</span><span class="sxs-lookup"><span data-stu-id="23fd2-130">Define Visibility</span></span>  

<span data-ttu-id="23fd2-131">Выберите параметр **видимости** , чтобы определить аудиторию, которая может найти и получить расширение.</span><span class="sxs-lookup"><span data-stu-id="23fd2-131">Select a **Visibility** option to define the audience who may discover and acquire your Extension.</span></span>  <span data-ttu-id="23fd2-132">Здесь вы можете указать, должны ли пользователи найти свое расширение в надстройках Microsoft EDGE или вообще ознакомиться со списком.</span><span class="sxs-lookup"><span data-stu-id="23fd2-132">This gives you the option to specify whether users should find your Extension in Microsoft Edge Addons or see the listing at all.</span></span>  <span data-ttu-id="23fd2-133">В настоящее время у вас есть два параметра в разделе Visibility (видимость).</span><span class="sxs-lookup"><span data-stu-id="23fd2-133">Currently, you have two options under visibility:</span></span>  

*   `Public`  
    <span data-ttu-id="23fd2-134">Это параметр по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="23fd2-134">This is the default option.</span></span>  
    <span data-ttu-id="23fd2-135">Если выбрать `Public` , ваше расширение доступно и может быть обнаруживаемым для всех пользователей в надстройках Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="23fd2-135">If you select `Public`, your Extension is available and discoverable to everyone in Microsoft Edge Addons.</span></span>  <span data-ttu-id="23fd2-136">Оставьте этот параметр, если вы хотите, чтобы расширение было указано в надстройках Microsoft Edge для пользователей с помощью поиска, просмотра и прямой ссылки на свое расширение.</span><span class="sxs-lookup"><span data-stu-id="23fd2-136">Leave this option selected if you want your Extension to be listed in Microsoft Edge Addons for users to find via searching, browsing, and the direct link of your Extension.</span></span>  

*   `Hidden`  
    <span data-ttu-id="23fd2-137">Если выбрать `Hidden` это расширение, оно будет скрыто в надстройках Microsoft Edge для пользователей, которые просматривают Поиск или просмотрев; вы должны поделиться URL-адресом вашего списка, чтобы распространить расширение.</span><span class="sxs-lookup"><span data-stu-id="23fd2-137">If you select `Hidden`, your Extension is hidden in Microsoft Edge Addons from users searching or browsing; you must share your listing URL to distribute your Extension.</span></span>  <span data-ttu-id="23fd2-138">Пользователи, у которых есть прямая ссылка на этот список, могут скачать его в Microsoft Edge \ (вы можете найти URL-адрес списка на странице " **Обзор расширения** " для отправки расширения).</span><span class="sxs-lookup"><span data-stu-id="23fd2-138">Users who have the direct link to the listing may download it on Microsoft Edge \(you may find your listing URL under **Extension Overview** page of Extension submission\).</span></span>  

> [!NOTE]
> <span data-ttu-id="23fd2-139">Если вы отправили расширение как **общедоступное** и в дальнейшем измените его на **частный**, пользователи, которые установили расширение, когда сохранится, смогут получить доступ и получать обновления в будущем.</span><span class="sxs-lookup"><span data-stu-id="23fd2-139">If you submit an Extension as **Public** and later change it to **Private**, Users who installed the Extension when it was public continue to have access and receive future updates.</span></span>  

### <span data-ttu-id="23fd2-140">Определение рынков</span><span class="sxs-lookup"><span data-stu-id="23fd2-140">Define markets</span></span>  

<span data-ttu-id="23fd2-141">Вы должны определить конкретные рынки, на которых вы предлагаете расширение, и выбрать **Показать параметры** в разделе **рынки** на странице **доступность** .</span><span class="sxs-lookup"><span data-stu-id="23fd2-141">You must define the specific markets in which you are offering your Extension, select **Show options** in the **Markets** section on the **Availability** page.</span></span>  <span data-ttu-id="23fd2-142">Откроется всплывающее окно выбора рынка, в котором нужно выбрать рынки.</span><span class="sxs-lookup"><span data-stu-id="23fd2-142">The Market selection pop-up window is displayed, where you should choose the markets.</span></span>  <span data-ttu-id="23fd2-143">По умолчанию выделены все рынки, включая все **будущие рынки** , которые могут быть добавлены позже.</span><span class="sxs-lookup"><span data-stu-id="23fd2-143">By default, all markets are selected, including any **future markets** that may be added later.</span></span>  <span data-ttu-id="23fd2-144">Вы можете отменить выбор отдельных рынков, чтобы исключить их, или нажать кнопку **снять все** , а затем добавить индивидуальные рынки по своему выбору.</span><span class="sxs-lookup"><span data-stu-id="23fd2-144">You may deselect individual markets to exclude them, or you may click **Unselect all** and then add individual markets of your choice.</span></span>  

> [!NOTE]
> <span data-ttu-id="23fd2-145">Если у пользователей уже есть расширение на определенном рынке, и вы позже удалите этот рынок, пользователи, у которых уже есть расширение на этом рынке, смогут продолжать использовать его, но они не получат последующих обновлений.</span><span class="sxs-lookup"><span data-stu-id="23fd2-145">If users already have your Extension in a certain market, and you later remove that market, users who already has the Extension in that market may continue to use it, but they do not get the later updates you submit.</span></span>  

<span data-ttu-id="23fd2-146">Нажмите кнопку **сохранить** , чтобы перейти к разделу **свойства** .</span><span class="sxs-lookup"><span data-stu-id="23fd2-146">Click **Save** to proceed to **Properties** section.</span></span>  

## <span data-ttu-id="23fd2-147">Шаг 4: Выбор свойств расширения</span><span class="sxs-lookup"><span data-stu-id="23fd2-147">Step 4: Select Properties for Your Extension</span></span>  

### <span data-ttu-id="23fd2-148">Свойства расширения</span><span class="sxs-lookup"><span data-stu-id="23fd2-148">Extension properties</span></span>  

*   [<span data-ttu-id="23fd2-149">Категория</span><span class="sxs-lookup"><span data-stu-id="23fd2-149">Category</span></span>](#category)  
*   [<span data-ttu-id="23fd2-150">Требования к политике конфиденциальности</span><span class="sxs-lookup"><span data-stu-id="23fd2-150">Privacy policy requirements</span></span>](#privacy-policy-requirements)  
*   [<span data-ttu-id="23fd2-151">URL-адрес с политикой конфиденциальности</span><span class="sxs-lookup"><span data-stu-id="23fd2-151">Privacy policy URL</span></span>](#privacy-policy-url)  
*   [<span data-ttu-id="23fd2-152">URL-адрес сайта</span><span class="sxs-lookup"><span data-stu-id="23fd2-152">Website URL</span></span>](#website-url)  
*   [<span data-ttu-id="23fd2-153">URL-адрес или адрес электронной почты службы поддержки</span><span class="sxs-lookup"><span data-stu-id="23fd2-153">Support URL/email address</span></span>](#support-urlemail-address)  
*   [<span data-ttu-id="23fd2-154">Оценка расширения</span><span class="sxs-lookup"><span data-stu-id="23fd2-154">Extension Rating</span></span>](#extension-rating)  

#### <span data-ttu-id="23fd2-155">Категория</span><span class="sxs-lookup"><span data-stu-id="23fd2-155">Category</span></span>  

<span data-ttu-id="23fd2-156">Если вы задаете свое расширение в категории справа, пользователи смогут легко найти свое расширение и узнать больше о нем.</span><span class="sxs-lookup"><span data-stu-id="23fd2-156">Listing your Extension in the right category helps users find your Extension easily and understand more about it.</span></span>  <span data-ttu-id="23fd2-157">Выберите категорию, которая лучше описывает расширение.</span><span class="sxs-lookup"><span data-stu-id="23fd2-157">Select a Category that best describes your Extension.</span></span>  

<span data-ttu-id="23fd2-158">**Возможные значения**:</span><span class="sxs-lookup"><span data-stu-id="23fd2-158">**Possible Values**:</span></span>  

*   `Accessibility`  
*   `Blogging`  
*   `Developer Tools`  
*   `Fun`  
*   `News & Weather`  
*   `Photos`  
*   `Productivity`  
*   `Search Tools`  
*   `Shopping`  
*   `Social & Communication`  
*   `Sports`  

#### <span data-ttu-id="23fd2-159">Требования к политике конфиденциальности</span><span class="sxs-lookup"><span data-stu-id="23fd2-159">Privacy policy requirements</span></span>  

<span data-ttu-id="23fd2-160">Указывает, будет ли расширение получать доступ к своим личным данным, собирает данные или передает их.</span><span class="sxs-lookup"><span data-stu-id="23fd2-160">Indicate whether your Extension accesses, collects, or transmits any personal information.</span></span>  

> [!NOTE]
> <span data-ttu-id="23fd2-161">Если расширение требует наличия политики конфиденциальности и вы не указали его, возможно, ваша отправка не проходит сертификацию.</span><span class="sxs-lookup"><span data-stu-id="23fd2-161">If your Extension requires a privacy policy and you have not provided one, your submission may fail certification.</span></span>  

<span data-ttu-id="23fd2-162">**Возможные значения**:</span><span class="sxs-lookup"><span data-stu-id="23fd2-162">**Possible Values**:</span></span>  

*   `No`<span data-ttu-id="23fd2-163">: URL-адрес политики конфиденциальности является необязательным.</span><span class="sxs-lookup"><span data-stu-id="23fd2-163">:  A privacy policy URL is optional.</span></span>  
*   `Yes`<span data-ttu-id="23fd2-164">: Требуется URL-адрес политики конфиденциальности.</span><span class="sxs-lookup"><span data-stu-id="23fd2-164">:  A privacy policy URL is required.</span></span>  

#### <span data-ttu-id="23fd2-165">URL-адрес с политикой конфиденциальности</span><span class="sxs-lookup"><span data-stu-id="23fd2-165">Privacy policy URL</span></span>  

<span data-ttu-id="23fd2-166">Вы несете ответственность за то, чтобы ваше расширение отвечало законам о конфиденциальности и положениям, а для предоставления действительного URL-адреса политики конфиденциальности (если это необходимо).</span><span class="sxs-lookup"><span data-stu-id="23fd2-166">You are responsible for ensuring your Extension complies with privacy laws and regulations, and for providing a valid privacy policy URL, if required.</span></span>  <span data-ttu-id="23fd2-167">Вы должны указать URL-адрес политики конфиденциальности, если вы обращаетесь к личным сведениям, передаете или собираетесь своему расширению.</span><span class="sxs-lookup"><span data-stu-id="23fd2-167">You must provide a privacy policy URL if any personal information is being accessed, transmitted, or collected by your Extension.</span></span>  
<span data-ttu-id="23fd2-168">Чтобы определить, требуется ли для расширения политика конфиденциальности, ознакомьтесь с [условиями разработчика Microsoft Edge][MicrosoftAppDeveloperAgreement] и [документом политики разработчика каталог надстроек Microsoft Edge][MicrosoftEdgeAddonsCatalogDeveloperPolicies].</span><span class="sxs-lookup"><span data-stu-id="23fd2-168">To determine if your Extension requires a privacy policy, review the [Microsoft Edge Developer Agreement][MicrosoftAppDeveloperAgreement] and the [Microsoft Edge Addons Catalog Developer Policies document][MicrosoftEdgeAddonsCatalogDeveloperPolicies].</span></span>  

<span data-ttu-id="23fd2-169">**Возможные значения**:</span><span class="sxs-lookup"><span data-stu-id="23fd2-169">**Possible Values**:</span></span>  

*   `{url}`  

#### <span data-ttu-id="23fd2-170">URL-адрес сайта</span><span class="sxs-lookup"><span data-stu-id="23fd2-170">Website URL</span></span>  

<span data-ttu-id="23fd2-171">Это свойство является необязательным.</span><span class="sxs-lookup"><span data-stu-id="23fd2-171">This property is Optional.</span></span>  
<span data-ttu-id="23fd2-172">URL-адрес страницы расширения.</span><span class="sxs-lookup"><span data-stu-id="23fd2-172">The URL of the web page for your Extension.</span></span>  <span data-ttu-id="23fd2-173">Этот URL-адрес должен указывать на страницу на своем веб-сайте, а не в веб-списке расширения в надстройках Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="23fd2-173">This URL must point to a page on your own website, not the web listing for your Extension in Microsoft Edge Addons.</span></span>  

<span data-ttu-id="23fd2-174">**Возможные значения**:</span><span class="sxs-lookup"><span data-stu-id="23fd2-174">**Possible Values**:</span></span>  

*   `{url}`  

#### <span data-ttu-id="23fd2-175">URL-адрес или адрес электронной почты службы поддержки</span><span class="sxs-lookup"><span data-stu-id="23fd2-175">Support URL/email address</span></span>  

<span data-ttu-id="23fd2-176">Это свойство является необязательным.</span><span class="sxs-lookup"><span data-stu-id="23fd2-176">This property is Optional.</span></span>  
<span data-ttu-id="23fd2-177">URL-адрес страницы, на которой размещаются пользователи для поддержки расширения, или адрес электронной почты, по которому вы можете обратиться за поддержкой.</span><span class="sxs-lookup"><span data-stu-id="23fd2-177">The URL of the web page where users go for support with your Extension, or an email address to contact you for support.</span></span>  <span data-ttu-id="23fd2-178">Вы включаете сведения о поддержке для всех отправленных сообщений, чтобы пользователи знали, как получить поддержку от вас.</span><span class="sxs-lookup"><span data-stu-id="23fd2-178">You include support information for all submissions, so that your users know how to get support from you.</span></span>  

<span data-ttu-id="23fd2-179">**Возможные значения**:</span><span class="sxs-lookup"><span data-stu-id="23fd2-179">**Possible Values**:</span></span>  

*   `{email_address}`  
*   `{url}`  

#### <span data-ttu-id="23fd2-180">Оценка расширения</span><span class="sxs-lookup"><span data-stu-id="23fd2-180">Extension Rating</span></span>  

<span data-ttu-id="23fd2-181">Оценка расширения помогает нам определить возраст целевой аудитории расширения.</span><span class="sxs-lookup"><span data-stu-id="23fd2-181">Extension rating helps us determine the age of the target audience of your Extension.</span></span>  
<span data-ttu-id="23fd2-182">Чтобы определить, есть ли у ваших расширений обновленный контент, ознакомьтесь с [документом политики разработчика каталога надстроек Microsoft Edge][MicrosoftEdgeAddonsCatalogDeveloperPolicies].</span><span class="sxs-lookup"><span data-stu-id="23fd2-182">To help you determine if your Extensions has a mature content, review the [Microsoft Edge Addons Catalog Developer Policies document][MicrosoftEdgeAddonsCatalogDeveloperPolicies].</span></span>  

<span data-ttu-id="23fd2-183">**Возможные значения**:</span><span class="sxs-lookup"><span data-stu-id="23fd2-183">**Possible Values**:</span></span>  

*   <span data-ttu-id="23fd2-184">Для взрослых — (флажок \): Установите этот флажок, если ваше расширение включает в себя содержимое, которое было бы более зрелым.</span><span class="sxs-lookup"><span data-stu-id="23fd2-184">Mature \(checkbox\): Check this box if your Extension contains any mature content.</span></span>  <span data-ttu-id="23fd2-185">Если вы выбрали расширение для своего расширения, ваше объявление будет доступно с помощью отдельного тега, указывающего на то, что расширение содержит готовое содержимое.</span><span class="sxs-lookup"><span data-stu-id="23fd2-185">If you select mature for your Extension, your listing is available with a separate tag to indicate that the Extension contains mature content.</span></span>  

<span data-ttu-id="23fd2-186">Нажмите кнопку **сохранить** , чтобы перейти к разделу листинг.</span><span class="sxs-lookup"><span data-stu-id="23fd2-186">Click **Save** to proceed to listing section.</span></span>  

## <span data-ttu-id="23fd2-187">Шаг 5: Добавление сведений о вхождениях для расширения</span><span class="sxs-lookup"><span data-stu-id="23fd2-187">Step 5: Add Listings Information for Your Extension</span></span>  

<span data-ttu-id="23fd2-188">Это сведения, которые пользователи видят при просмотре списка в надстройках Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="23fd2-188">This is the information that users see when viewing your listing in Microsoft Edge Addons.</span></span>  <span data-ttu-id="23fd2-189">Многие поля в списке являются необязательными, но мы рекомендуем предоставить как можно больше сведений, чтобы сделать список более заметным.  Минимальным требованием для вашего списка в надстройках Microsoft Edge является Complete — [текстовое описание](#description), [логотип расширения](#store-logo)и [небольшая рекламная плитка](#small-promotional-tile) на каждом из языков, упомянутых в вашем пакете расширения.</span><span class="sxs-lookup"><span data-stu-id="23fd2-189">Many of the fields in a listing are optional, but we suggest providing as much information as possible to make your listing stand out.  The minimum required for your listing in Microsoft Edge Addons to be considered complete is the [text description](#description), [Extension logo](#store-logo), and [small promotional tile](#small-promotional-tile) in each language mentioned in your Extension package.</span></span>  

### <span data-ttu-id="23fd2-190">Поля для описания в магазине</span><span class="sxs-lookup"><span data-stu-id="23fd2-190">Store Listing fields</span></span>  

*   [<span data-ttu-id="23fd2-191">Языки описаний в Store</span><span class="sxs-lookup"><span data-stu-id="23fd2-191">Store listing languages</span></span>](#store-listing-languages)  
*   [<span data-ttu-id="23fd2-192">Отображаемое имя в магазине</span><span class="sxs-lookup"><span data-stu-id="23fd2-192">Store display name</span></span>](#store-display-name)  
*   [<span data-ttu-id="23fd2-193">Описание</span><span class="sxs-lookup"><span data-stu-id="23fd2-193">Description</span></span>](#description)  
*   [<span data-ttu-id="23fd2-194">Логотип магазина</span><span class="sxs-lookup"><span data-stu-id="23fd2-194">Store logo</span></span>](#store-logo)  
*   [<span data-ttu-id="23fd2-195">Мелкая рекламная плитка</span><span class="sxs-lookup"><span data-stu-id="23fd2-195">Small promotional tile</span></span>](#small-promotional-tile)  
*   [<span data-ttu-id="23fd2-196">Мультимедиа</span><span class="sxs-lookup"><span data-stu-id="23fd2-196">Media</span></span>](#media)  
*   [<span data-ttu-id="23fd2-197">Краткое описание</span><span class="sxs-lookup"><span data-stu-id="23fd2-197">Short description</span></span>](#short-description)  
*   [<span data-ttu-id="23fd2-198">Условия поиска</span><span class="sxs-lookup"><span data-stu-id="23fd2-198">Search terms</span></span>](#search-terms)  

#### <span data-ttu-id="23fd2-199">Языки описаний в Store</span><span class="sxs-lookup"><span data-stu-id="23fd2-199">Store listing languages</span></span>  

<span data-ttu-id="23fd2-200">Если пакет расширений поддерживает несколько языков, для каждого из них должно быть задано окно описания.</span><span class="sxs-lookup"><span data-stu-id="23fd2-200">If your Extension package supports multiple languages, your Extension must have a listing page for each one.</span></span>  
<span data-ttu-id="23fd2-201">Вы должны завершить Просмотр подробных сведений \ (текстовое описание, изображения и т. д.) для каждого языка отдельно, даже если вы используете одинаковое содержимое для каждого языка.</span><span class="sxs-lookup"><span data-stu-id="23fd2-201">You must complete listing details \(text description, images, and so on\) for each language separately even if you are using the same content for each language.</span></span>  <span data-ttu-id="23fd2-202">Если расширение локализовано на нескольких языках, эти языки отображаются в верхней части страницы списка.</span><span class="sxs-lookup"><span data-stu-id="23fd2-202">If your Extension is localized in more than one language, those languages are displayed at the top of listing page.</span></span>  

1.  <span data-ttu-id="23fd2-203">Выберите один из языков в раскрывающемся списке **языки** .</span><span class="sxs-lookup"><span data-stu-id="23fd2-203">Select any one language name from **Languages** drop-down list.</span></span>  
1.  <span data-ttu-id="23fd2-204">Заполните сведения о листинге.</span><span class="sxs-lookup"><span data-stu-id="23fd2-204">Fill the listing details.</span></span>  
1.  <span data-ttu-id="23fd2-205">Нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="23fd2-205">Click **Save**.</span></span>  
1.  <span data-ttu-id="23fd2-206">Повторите эти действия для всех поддерживаемых языков.</span><span class="sxs-lookup"><span data-stu-id="23fd2-206">Repeat for all of your supported languages.</span></span>  

> [!NOTE]
> <span data-ttu-id="23fd2-207">Чтобы добавить или удалить языки для вашего списка в надстройках Microsoft EDGE, необходимо изменить список языков, поддерживаемых пакетом расширения, и повторно добавить его.</span><span class="sxs-lookup"><span data-stu-id="23fd2-207">To add or remove languages for your listing in Microsoft Edge Addons, you must modify the list of languages supported by your Extension package and re-upload it.</span></span>  

<span data-ttu-id="23fd2-208">**Возможные значения**:</span><span class="sxs-lookup"><span data-stu-id="23fd2-208">**Possible Values**:</span></span>  

*   `English (United States)`<span data-ttu-id="23fd2-209">: Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="23fd2-209">:  This is the default value.</span></span>  <span data-ttu-id="23fd2-210">Если вы не упомянули язык в пакете, мы устанавливаем язык по умолчанию на английский (США), и вы должны предоставить список на английском языке \ (США).</span><span class="sxs-lookup"><span data-stu-id="23fd2-210">If you do not mention any language in your package, we set your default language to English \(United States\) and you must provide a listing in English \(United States\).</span></span>  
*   `{language}` <span data-ttu-id="23fd2-211">\(`{Country}`\)</span><span class="sxs-lookup"><span data-stu-id="23fd2-211">\(`{Country}`\)</span></span>  

#### <span data-ttu-id="23fd2-212">Отображаемое имя в магазине</span><span class="sxs-lookup"><span data-stu-id="23fd2-212">Store display name</span></span>  

<span data-ttu-id="23fd2-213">Расширение имени, указанное в манифесте пакета расширения.</span><span class="sxs-lookup"><span data-stu-id="23fd2-213">The name of Extension as mentioned in your Extension package manifest.</span></span>  

> [!NOTE]
> <span data-ttu-id="23fd2-214">Чтобы изменить имя, необходимо обновить манифест в пакете расширения и отправить его повторно.</span><span class="sxs-lookup"><span data-stu-id="23fd2-214">To edit the name, you must update the manifest in your Extension package and re-upload it.</span></span>  

#### <span data-ttu-id="23fd2-215">Описание</span><span class="sxs-lookup"><span data-stu-id="23fd2-215">Description</span></span>  

<span data-ttu-id="23fd2-216">Это поле является обязательным.</span><span class="sxs-lookup"><span data-stu-id="23fd2-216">This field is required.</span></span>  
<span data-ttu-id="23fd2-217">Описание пользователей о том, что делает ваше расширение.</span><span class="sxs-lookup"><span data-stu-id="23fd2-217">The description for your users of what your Extension does.</span></span>  

<span data-ttu-id="23fd2-218">**Возможные значения**:</span><span class="sxs-lookup"><span data-stu-id="23fd2-218">**Possible Values**:</span></span>  

*   <span data-ttu-id="23fd2-219">{plain_text}: менее 10 000 знаков.</span><span class="sxs-lookup"><span data-stu-id="23fd2-219">{plain_text}: Less than 10,000 characters.</span></span>  

#### <span data-ttu-id="23fd2-220">Логотип магазина</span><span class="sxs-lookup"><span data-stu-id="23fd2-220">Store logo</span></span>  

<span data-ttu-id="23fd2-221">Это поле является обязательным.</span><span class="sxs-lookup"><span data-stu-id="23fd2-221">This field is required.</span></span>  
<span data-ttu-id="23fd2-222">Изображение 1:1 для логотипа расширения.</span><span class="sxs-lookup"><span data-stu-id="23fd2-222">A 1:1 image for your Extension logo.</span></span>  

<span data-ttu-id="23fd2-223">**Возможные значения**:</span><span class="sxs-lookup"><span data-stu-id="23fd2-223">**Possible Values**:</span></span>  

*   <span data-ttu-id="23fd2-224">128px x 128px, PNG \ (. png \)</span><span class="sxs-lookup"><span data-stu-id="23fd2-224">128px x 128px, PNG \(.png\)</span></span>  
*   <span data-ttu-id="23fd2-225">150px x 140px, PNG \ (. png \)</span><span class="sxs-lookup"><span data-stu-id="23fd2-225">150px x 140px, PNG \(.png\)</span></span>  
*   <span data-ttu-id="23fd2-226">300px x 300px, PNG \ (. png \): Рекомендуемый размер.</span><span class="sxs-lookup"><span data-stu-id="23fd2-226">300px x 300px, PNG \(.png\):  The recommended size.</span></span>  

#### <span data-ttu-id="23fd2-227">Мелкая рекламная плитка</span><span class="sxs-lookup"><span data-stu-id="23fd2-227">Small promotional tile</span></span>  

<span data-ttu-id="23fd2-228">Это поле является обязательным.</span><span class="sxs-lookup"><span data-stu-id="23fd2-228">This field is required.</span></span>  
<span data-ttu-id="23fd2-229">Рекламная плитка для малого размера.</span><span class="sxs-lookup"><span data-stu-id="23fd2-229">A small size promotional tile.</span></span>  <span data-ttu-id="23fd2-230">Ваша спецификация отображается на этой плитке.</span><span class="sxs-lookup"><span data-stu-id="23fd2-230">Your listing is displayed on this tile.</span></span>  

<span data-ttu-id="23fd2-231">**Возможные значения**:</span><span class="sxs-lookup"><span data-stu-id="23fd2-231">**Possible Values**:</span></span>  

*   <span data-ttu-id="23fd2-232">440px x 280x, PNG \ (. png \)</span><span class="sxs-lookup"><span data-stu-id="23fd2-232">440px x 280x, PNG \(.png\)</span></span>  

#### <span data-ttu-id="23fd2-233">Мультимедиа</span><span class="sxs-lookup"><span data-stu-id="23fd2-233">Media</span></span>  

<span data-ttu-id="23fd2-234">Это поле является необязательным.</span><span class="sxs-lookup"><span data-stu-id="23fd2-234">This field is optional.</span></span>  
<span data-ttu-id="23fd2-235">Эти ресурсы следует предоставить для более эффективного отображения продукта.</span><span class="sxs-lookup"><span data-stu-id="23fd2-235">You should provide these assets to help display your product more effectively.</span></span>  

*   <span data-ttu-id="23fd2-236">Снимки экрана</span><span class="sxs-lookup"><span data-stu-id="23fd2-236">Screenshots</span></span>  
    <span data-ttu-id="23fd2-237">Изображения расширения, описывающие расширение.</span><span class="sxs-lookup"><span data-stu-id="23fd2-237">The images of your Extension that describe what your Extension does.</span></span>  
    
*   <span data-ttu-id="23fd2-238">Крупные плитки для рекламы</span><span class="sxs-lookup"><span data-stu-id="23fd2-238">Large promotion tiles</span></span>  
    <span data-ttu-id="23fd2-239">Крупная рекламная плитка, представляющая собой расширение в надстройках Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="23fd2-239">A large promotional tile to be feature your Extension more prominently in Microsoft Edge Addons.</span></span>  
    
*   <span data-ttu-id="23fd2-240">URL-адрес для видео на YouTube</span><span class="sxs-lookup"><span data-stu-id="23fd2-240">YouTube video URL</span></span>  
    <span data-ttu-id="23fd2-241">Допустимый [URL-адрес в YouTube для вашего расширения][MicrosoftEdgeAddonsUploadYouTubeVideo].</span><span class="sxs-lookup"><span data-stu-id="23fd2-241">A valid [YouTube video URL for your Extension][MicrosoftEdgeAddonsUploadYouTubeVideo].</span></span>  <span data-ttu-id="23fd2-242">Ваше видео должно иметь хорошее качество и минимальная длина.</span><span class="sxs-lookup"><span data-stu-id="23fd2-242">Your video should be good quality and minimal length.</span></span>  <span data-ttu-id="23fd2-243">Видео YouTube должно пройти сертификацию, прежде чем публиковать расширение в надстройках Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="23fd2-243">Your YouTube video must pass certification before publishing your Extension in Microsoft Edge Addons.</span></span>  <span data-ttu-id="23fd2-244">Убедитесь, что видео YouTube соответствует [документу политики разработчика каталога надстроек Microsoft Edge][MicrosoftEdgeAddonsCatalogDeveloperPolicies].</span><span class="sxs-lookup"><span data-stu-id="23fd2-244">Verify that your YouTube video complies with the [Microsoft Edge Addons Catalog Developer Policies document][MicrosoftEdgeAddonsCatalogDeveloperPolicies].</span></span>  

<span data-ttu-id="23fd2-245">**Возможные значения**:</span><span class="sxs-lookup"><span data-stu-id="23fd2-245">**Possible Values**:</span></span>  

*   <span data-ttu-id="23fd2-246">не более 10 снимков экрана.</span><span class="sxs-lookup"><span data-stu-id="23fd2-246">10 Screenshots maximum.</span></span>  
    *   <span data-ttu-id="23fd2-247">640 пикселей x 480px, PNG \ (. png \): снимки экрана.</span><span class="sxs-lookup"><span data-stu-id="23fd2-247">640px x 480px, PNG \(.png\):  Screenshots.</span></span>  
    *   <span data-ttu-id="23fd2-248">1280px x 800px, PNG \ (. png \): снимки экрана.</span><span class="sxs-lookup"><span data-stu-id="23fd2-248">1280px x 800px, PNG \(.png\):  Screenshots.</span></span>  
*   <span data-ttu-id="23fd2-249">1400px x 560px, PNG \ (. png \): крупные рекламные плитки.</span><span class="sxs-lookup"><span data-stu-id="23fd2-249">1400px x 560px, PNG \(.png\):  Large promotion tiles.</span></span>  
*   <span data-ttu-id="23fd2-250">60 секунд, более короткий и 2 ГБ, URL-адрес для видео в YouTube.</span><span class="sxs-lookup"><span data-stu-id="23fd2-250">60 seconds or shorter and 2GB or smaller, YouTube video URL.</span></span>  

#### <span data-ttu-id="23fd2-251">Краткое описание</span><span class="sxs-lookup"><span data-stu-id="23fd2-251">Short description</span></span>  

<span data-ttu-id="23fd2-252">Краткое описание, которое можно использовать в верхней части списка для вашего продукта.</span><span class="sxs-lookup"><span data-stu-id="23fd2-252">A short, catchy description that may be used at the top of the listing for your product.</span></span>  <span data-ttu-id="23fd2-253">Если этот элемент не указан, вместо него используются первые несколько строк из длинного описания.</span><span class="sxs-lookup"><span data-stu-id="23fd2-253">If not provided, the first few lines from your longer description are used instead.</span></span>  <span data-ttu-id="23fd2-254">Так как ваше описание также отображается под этим текстом, необходимо предоставить краткое описание с другим текстом, чтобы оно было менее повторяющимся.</span><span class="sxs-lookup"><span data-stu-id="23fd2-254">Because your description also appears below this text, you should provide a short description with different text so that your listing is less repetitive.</span></span>  <span data-ttu-id="23fd2-255">Краткое описание расширения выбирается непосредственно из файла манифеста пакета.</span><span class="sxs-lookup"><span data-stu-id="23fd2-255">The Short description of your Extension is picked directly from the manifest file of your package.</span></span>  

> [!NOTE]
> <span data-ttu-id="23fd2-256">Чтобы изменить краткое описание, необходимо обновить манифест в пакете расширения и отправить его повторно.</span><span class="sxs-lookup"><span data-stu-id="23fd2-256">To edit the short description, you must update the manifest in your Extension package and re-upload it.</span></span>  

#### <span data-ttu-id="23fd2-257">Условия поиска</span><span class="sxs-lookup"><span data-stu-id="23fd2-257">Search terms</span></span>  

<span data-ttu-id="23fd2-258">Условия поиска — это одиночные слова или короткие фразы, которые не отображаются пользователям, но помогают сделать расширение обнаруживаемым в надстройках Microsoft Edge при поиске пользователей с помощью этих условий.</span><span class="sxs-lookup"><span data-stu-id="23fd2-258">Search terms are single words or short phrases that are not displayed to users but help make your Extension discoverable in Microsoft Edge Addons when users search using those terms.</span></span>  

<span data-ttu-id="23fd2-259">**Требования**</span><span class="sxs-lookup"><span data-stu-id="23fd2-259">**Requirements**:</span></span>  

*   <span data-ttu-id="23fd2-260">7 или меньше условий поиска</span><span class="sxs-lookup"><span data-stu-id="23fd2-260">7 or fewer search terms</span></span>  
*   <span data-ttu-id="23fd2-261">не более 30 знаков на условие поиска</span><span class="sxs-lookup"><span data-stu-id="23fd2-261">30 or fewer characters per search term</span></span>  
*   <span data-ttu-id="23fd2-262">21 или меньше слов для комбинированных условий поиска</span><span class="sxs-lookup"><span data-stu-id="23fd2-262">21 or fewer words for combined search terms</span></span>  

<span data-ttu-id="23fd2-263">Нажмите кнопку **Save (сохранить** ), чтобы перейти к разделу Сохранение списка.</span><span class="sxs-lookup"><span data-stu-id="23fd2-263">Click **Save** to proceed to save your listing section.</span></span>  <span data-ttu-id="23fd2-264">Нажмите кнопку **опубликовать** , чтобы предоставить сведения об отправке.</span><span class="sxs-lookup"><span data-stu-id="23fd2-264">Click **Publish** to provide submission details.</span></span>  

## <span data-ttu-id="23fd2-265">Шаг 6. Завершите отправку и нажмите кнопку Опубликовать.</span><span class="sxs-lookup"><span data-stu-id="23fd2-265">Step 6: Complete your submission and click Publish</span></span>  

<span data-ttu-id="23fd2-266">На странице параметров отправки в процессе отправки расширения вы можете получить дополнительные сведения, которые помогут нам правильно проверить правильность вашего продукта.</span><span class="sxs-lookup"><span data-stu-id="23fd2-266">The Submission options page of the Extension submission process is where you provide more information to help us test your product properly.</span></span>  <span data-ttu-id="23fd2-267">Это необязательный шаг, но рекомендуется для многих передач.</span><span class="sxs-lookup"><span data-stu-id="23fd2-267">This is an optional step, but it is recommended for many submissions.</span></span>  

### <span data-ttu-id="23fd2-268">Параметры удержания публикации</span><span class="sxs-lookup"><span data-stu-id="23fd2-268">Publishing hold options</span></span>  

<span data-ttu-id="23fd2-269">По умолчанию отправка публикуется сразу после того, как она проходит сертификацию.</span><span class="sxs-lookup"><span data-stu-id="23fd2-269">By default, your submission is published as soon as it passes certification.</span></span>  <span data-ttu-id="23fd2-270">Вы можете указать удержание для публикации отправки до определенной даты.</span><span class="sxs-lookup"><span data-stu-id="23fd2-270">You may choose to place a hold on publishing your submission until a specific date.</span></span>  <span data-ttu-id="23fd2-271">Возможные варианты описаны ниже в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="23fd2-271">The options in this section are described below.</span></span>  

*   **<span data-ttu-id="23fd2-272">Публикация отправки сразу после того, как она проходит сертификацию</span><span class="sxs-lookup"><span data-stu-id="23fd2-272">Publish your submission as soon as it passes certification</span></span>**  

    <span data-ttu-id="23fd2-273">Этот вариант выбран по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="23fd2-273">This is the default selection.</span></span>  <span data-ttu-id="23fd2-274">Это означает, что отправка начнет процесс публикации сразу же после того, как он проходит сертификацию.</span><span class="sxs-lookup"><span data-stu-id="23fd2-274">It means that your submission begins the publishing process as soon as it passes certification</span></span>  

*   **<span data-ttu-id="23fd2-275">Публикация отправки в соответствии с конкретной датой</span><span class="sxs-lookup"><span data-stu-id="23fd2-275">Start publishing your submission on a certain date</span></span>**  

    <span data-ttu-id="23fd2-276">Нажмите кнопку **начать публикацию отправки на определенную дату** , чтобы убедиться, что отправка не опубликована до определенной даты.</span><span class="sxs-lookup"><span data-stu-id="23fd2-276">Choose **Start publishing your submission on a certain date** to ensure that the submission is not published until a specific date.</span></span>  <span data-ttu-id="23fd2-277">При использовании этого параметра отправка отпущена как можно скорее в течение или после указанной даты.</span><span class="sxs-lookup"><span data-stu-id="23fd2-277">With this option, your submission is released as soon as possible on or after the date you specify.</span></span>  <span data-ttu-id="23fd2-278">Указанная дата должна наступать не менее, чем через 24 часа.</span><span class="sxs-lookup"><span data-stu-id="23fd2-278">The date must be at least 24 hours in the future.</span></span>  <span data-ttu-id="23fd2-279">Вместе с датой вы можете указать время начала публикации отправки.</span><span class="sxs-lookup"><span data-stu-id="23fd2-279">Along with the date, you may specify the time at which the submission should begin to be published.</span></span>  

### <span data-ttu-id="23fd2-280">Заметки по сертификации</span><span class="sxs-lookup"><span data-stu-id="23fd2-280">Notes for certification</span></span>  

<span data-ttu-id="23fd2-281">Когда вы отправляете свое расширение, вы можете использовать страницу заметки для сертификации для предоставления дополнительных сведений тестерам сертификации.</span><span class="sxs-lookup"><span data-stu-id="23fd2-281">As you submit your Extension, you have the option to use the Notes for certification page to provide additional information to the certification testers.</span></span>  <span data-ttu-id="23fd2-282">Эти сведения помогут удостовериться, что расширение правильно прошло проверку.</span><span class="sxs-lookup"><span data-stu-id="23fd2-282">This information helps ensure that your Extension is tested correctly.</span></span>  <span data-ttu-id="23fd2-283">Если вы не можете полностью протестировать отправку, это может привести к сбою сертификации.</span><span class="sxs-lookup"><span data-stu-id="23fd2-283">If we are not able to fully test your submission, it may fail certification.</span></span>  

<span data-ttu-id="23fd2-284">Убедитесь, что в поле "\" (если применимо для вашего расширения) есть следующее:</span><span class="sxs-lookup"><span data-stu-id="23fd2-284">Make sure to include the following \(if applicable for your Extension\):</span></span>  

*   <span data-ttu-id="23fd2-285">Имена пользователей и пароли для тестовых учетных записей.</span><span class="sxs-lookup"><span data-stu-id="23fd2-285">User names and passwords for test accounts.</span></span>  
*   <span data-ttu-id="23fd2-286">Действия для доступа к скрытым или заблокированным функциям.</span><span class="sxs-lookup"><span data-stu-id="23fd2-286">Steps to access hidden or locked features.</span></span>  
*   <span data-ttu-id="23fd2-287">Ожидаемые различия поведения в зависимости от региона или других параметров пользователя.</span><span class="sxs-lookup"><span data-stu-id="23fd2-287">Expected differences in behavior based on region or other user settings.</span></span>  
*   <span data-ttu-id="23fd2-288">Сведения о том, что изменилось в обновлении приложения.</span><span class="sxs-lookup"><span data-stu-id="23fd2-288">Information about what changed in an app update.</span></span>  
*   <span data-ttu-id="23fd2-289">Все, что вам кажется, должны понимать ваши тестеры о вашей отправке.</span><span class="sxs-lookup"><span data-stu-id="23fd2-289">Anything else you think testers must understand about your submission.</span></span>  

<span data-ttu-id="23fd2-290">После выполнения описанных выше сведений нажмите кнопку **опубликовать** , чтобы отправить расширение в надстройках Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="23fd2-290">After completing the above details, click **Publish** to submit your Extension in Microsoft Edge Addons.</span></span>  

<span data-ttu-id="23fd2-291">После того как вы закончите создание отправки для вашего расширения и щелкните **опубликовать**, отправка пойдет на шаг сертификации.</span><span class="sxs-lookup"><span data-stu-id="23fd2-291">When you finish creating the submission for your Extension and click **Publish**, the submission enters the certification step.</span></span>  <span data-ttu-id="23fd2-292">Этот процесс обычно завершается в течение нескольких дней, но в некоторых случаях может потребоваться до 7 рабочих дней.</span><span class="sxs-lookup"><span data-stu-id="23fd2-292">This process usually is completed within a couple of days, though in some cases it may take up to 7 business days.</span></span>  <span data-ttu-id="23fd2-293">После того как вы пройдете сертификацию отправки, ваше расширение публикуется в надстройках Microsoft EDGE, если только вы не выбрали параметр удержания публикации, чтобы указать, что он не должен быть освобожден до определенной даты.</span><span class="sxs-lookup"><span data-stu-id="23fd2-293">After your submission passes certification, your Extension is published in Microsoft Edge Addons unless you selected the Publishing hold options to specify that it should not be released until a certain date.</span></span>  <span data-ttu-id="23fd2-294">Вы будете уведомлены о публикации отправки, а состояние расширения на панели мониторинга изменится на `In the Store` .</span><span class="sxs-lookup"><span data-stu-id="23fd2-294">You are notified when your submission is published, and the status of your Extension in the dashboard changes to `In the Store`.</span></span>  

<!-- image links -->  

<!-- links -->  

[ExtensionsGettingStarted]: ../getting-started/index.md "Начало работы с расширениями Microsoft Edge \ (Chromium \) | Документы Microsoft"  

[MicrosoftEdgeAddonsUploadYouTubeVideo]: ./upload-video.md "Загрузите видео с сайта YouTube | Документы Microsoft"  
[MicrosoftEdgeAddonsCatalogDeveloperPolicies]: ../store-policies/developer-policies.md "Политики разработчика каталога надстроек Microsoft Edge | Документы Microsoft"  

[MicrosoftAppDeveloperAgreement]: /legal/windows/agreements/app-developer-agreement "Соглашение с разработчиком приложений | Документы Microsoft"  

[MicrosoftPartnerCenter]: https://partner.microsoft.com/dashboard/microsoftedge/public/login?ref=dd "Центр партнеров"  
