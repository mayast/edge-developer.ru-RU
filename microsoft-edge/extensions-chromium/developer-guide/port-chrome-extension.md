---
description: Процесс переноса расширения Chrome на Microsoft Edge.
title: Расширение Chrome для порта в Microsoft (Chromium) Edge
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 09/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: Edge-Chromium, Разработка расширений, расширения браузера, надстройки, центр партнера, разработчик
ms.openlocfilehash: 1852e267579f0fb790c6b8cac75a566298223933
ms.sourcegitcommit: d360e419b5f96f4f691cf7330b0d8dff9126f82e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/15/2020
ms.locfileid: "11015690"
---
# <span data-ttu-id="907ac-104">Расширение Chrome для порта в Microsoft \ (Chromium \) Edge</span><span class="sxs-lookup"><span data-stu-id="907ac-104">Port Chrome Extension To Microsoft \(Chromium\) Edge</span></span>  

<span data-ttu-id="907ac-105">Процесс переноса расширения Chrome на Microsoft Edge является очень простым.</span><span class="sxs-lookup"><span data-stu-id="907ac-105">The process of porting a Chrome Extension to Microsoft Edge is very straightforward.</span></span>  <span data-ttu-id="907ac-106">Расширения, написанные для Chromium, в большинстве случаев работают в Microsoft Edge с минимальными изменениями.</span><span class="sxs-lookup"><span data-stu-id="907ac-106">Extensions written for Chromium, in most cases, run on Microsoft Edge with minimal changes.</span></span>  <span data-ttu-id="907ac-107">API расширения и ключи манифестов, поддерживаемые хромом, совместимы с кодом Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="907ac-107">The Extension APIs and manifest keys supported by Chrome are code-compatible with Microsoft Edge.</span></span>  <span data-ttu-id="907ac-108">Тем не менее Microsoft EDGE не поддерживает следующие API расширений:</span><span class="sxs-lookup"><span data-stu-id="907ac-108">However, Microsoft Edge does not support the following Extension APIs:</span></span>  

*   `chrome.gcm`  
*   `chrome.identity.getAccounts`  
*   `chrome.identity.getAuthToken`  
*   `chrome.instanceID`  

> [!Note]
> <span data-ttu-id="907ac-109">Чтобы использовать API, пользователь должен войти в Microsoft Edge с использованием учетной записи MSA или AAD `chrome.identity.getProfileUserInfo` .</span><span class="sxs-lookup"><span data-stu-id="907ac-109">The user must be signed into Microsoft Edge using an MSA or AAD account in order to use the `chrome.identity.getProfileUserInfo` API.</span></span>  <span data-ttu-id="907ac-110">Если пользователь вошел в Microsoft Edge с использованием **локальной рекламы**, API-интерфейс возвращает `null` для значений электронной почты и идентификаторов.</span><span class="sxs-lookup"><span data-stu-id="907ac-110">If the user is signed into Microsoft Edge using **On-premise AD**, the API returns `null` for the email and ID values.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="907ac-111">**Платежи**: Microsoft EDGE не поддерживает напрямую расширение, использующее [платежи веб-магазина Chrome][ChromeDeveloperWebStorePayments] из-за необходимости использования `identity.getAuthtoken` запроса для получения маркера для пользователей, которые вошли в систему для отправки запроса API лицензирования на основе оставшейся части.</span><span class="sxs-lookup"><span data-stu-id="907ac-111">**Payments**:  Microsoft Edge does not directly support an Extension that uses [Chrome Web Store payments][ChromeDeveloperWebStorePayments] due to the requirement to use the `identity.getAuthtoken` request to get the token for signed-in users to send the REST-based licensing API request.</span></span>  <span data-ttu-id="907ac-112">Microsoft EDGE не поддерживает `getAuthtoken` запрос, поэтому этот поток не работает.</span><span class="sxs-lookup"><span data-stu-id="907ac-112">Microsoft Edge does not support the `getAuthtoken` request, so this flow does not work.</span></span>  

<span data-ttu-id="907ac-113">Чтобы перенести расширение Chrome, выполните указанные ниже действия.</span><span class="sxs-lookup"><span data-stu-id="907ac-113">To port your Chrome Extension, follow these steps:</span></span>  

1.  <span data-ttu-id="907ac-114">Ознакомьтесь с API расширения Chrome, используемых в расширениях.</span><span class="sxs-lookup"><span data-stu-id="907ac-114">Review the Chrome Extension APIs used in your Extensions.</span></span>  <span data-ttu-id="907ac-115">Если вы используете функции или API-интерфейсы, которые не поддерживаются Microsoft EDGE, вы не можете перенести свое расширение.</span><span class="sxs-lookup"><span data-stu-id="907ac-115">If you are using features or APIs that are not supported by Microsoft Edge, you may not be able to port your Extension.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="907ac-116">`getAuthToken`API не работает в Microsoft EDGE, однако вы можете использовать `launchWebAuthFlow` для получения маркера OAuth2 для проверки подлинности пользователей.</span><span class="sxs-lookup"><span data-stu-id="907ac-116">The `getAuthToken` API does not work with Microsoft Edge, however you may use `launchWebAuthFlow` to fetch an OAuth2 token to authenticate users.</span></span>  
    
1.  <span data-ttu-id="907ac-117">Если вы используете `Chrome` имя или описание расширения, Перепишите расширение `Microsoft Edge` .</span><span class="sxs-lookup"><span data-stu-id="907ac-117">If you are using `Chrome` in the name or description of your Extension, re-brand the Extension for `Microsoft Edge`.</span></span>  <span data-ttu-id="907ac-118">Вы должны пройти процесс сертификации.</span><span class="sxs-lookup"><span data-stu-id="907ac-118">You must pass the certification process.</span></span>  
    
1.  <span data-ttu-id="907ac-119">Проверьте расширение, чтобы убедиться в том, что он работает в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="907ac-119">Test your Extension to check if it works in Microsoft Edge.</span></span>  <span data-ttu-id="907ac-120">Для этого сначала необходимо убедиться, что у вас есть функции разработчика расширений.</span><span class="sxs-lookup"><span data-stu-id="907ac-120">The first step to do this is to ensure that you have Extension developer features turned on.</span></span>  <span data-ttu-id="907ac-121">Это позволяет загружать файлы расширений в Microsoft Edge таким образом, чтобы вы могли протестировать расширение при разработке.</span><span class="sxs-lookup"><span data-stu-id="907ac-121">This enables you to side load Extension files in Microsoft Edge so that you are able to test your Extension while developing it.</span></span>  
    
1.  <span data-ttu-id="907ac-122">Если у вас возникли проблемы, выполните отладку расширений в Microsoft Edge с помощью DevTools или [свяжитесь с нами][mailtoExtensionPartnerOpsMicrosoft].</span><span class="sxs-lookup"><span data-stu-id="907ac-122">If you have any issues, debug your Extensions in Microsoft Edge by using the DevTools, or [contact us][mailtoExtensionPartnerOpsMicrosoft].</span></span>  
    
1.  <span data-ttu-id="907ac-123">Теперь ваше расширение, наконец, будет готово к упаковке.</span><span class="sxs-lookup"><span data-stu-id="907ac-123">Now your Extension is finally polished up and ready to be packaged.</span></span>  <span data-ttu-id="907ac-124">Если вы хотите подготовиться к отправке в каталог надстроек Microsoft Edge \ (надстройки Microsoft Edge \), вам не нужно будет упаковать расширение.</span><span class="sxs-lookup"><span data-stu-id="907ac-124">If you wish to prepare for submission to the Microsoft Edge Addons catalog \(Microsoft Edge Addons\), you do not need to package your Extension.</span></span>  <span data-ttu-id="907ac-125">Далее следуйте [рекомендациям публикации][ExtensionsPublishExtension] , чтобы опубликовать расширение в надстройках Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="907ac-125">Further, follow our [publishing guidelines][ExtensionsPublishExtension] to publish your Extension on Microsoft Edge Addons.</span></span>  
    
    > [!NOTE]
    > <span data-ttu-id="907ac-126">Если ваше расширение обменивается сообщениями с собственным приложением с помощью `chrome.runtime.connectNative` API-интерфейса, убедитесь, что для него установлен параметр " `allowedorigins` `extension://[Microsoft-Catalog-extensionID]` " в исходном файле манифеста узла сообщений.</span><span class="sxs-lookup"><span data-stu-id="907ac-126">If your Extension exchanges messages with a native application using `chrome.runtime.connectNative` API, ensure that you set `allowedorigins` to "`extension://[Microsoft-Catalog-extensionID]`" in your native messaging host manifest file.</span></span>  <span data-ttu-id="907ac-127">Это позволяет приложению идентифицировать расширение.</span><span class="sxs-lookup"><span data-stu-id="907ac-127">This enables the app to identify the Extension.</span></span>  

<!-- image links -->  

<!-- links -->  

[ExtensionsPublishExtension]: ../publish/publish-extension.md "Публикация расширения"  

[mailtoExtensionPartnerOpsMicrosoft]: mailto:extensionpartnerops@microsoft.com "ExtensionPartnerOps@microsoft.com"  

[ChromeDeveloperWebStorePayments]: https://developer.chrome.com/webstore/one_time_payments "Разовые платежи – Хром Google"  
