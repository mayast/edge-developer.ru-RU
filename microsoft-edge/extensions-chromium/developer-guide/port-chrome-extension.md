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
# Расширение Chrome для порта в Microsoft \ (Chromium \) Edge  

Процесс переноса расширения Chrome на Microsoft Edge является очень простым.  Расширения, написанные для Chromium, в большинстве случаев работают в Microsoft Edge с минимальными изменениями.  API расширения и ключи манифестов, поддерживаемые хромом, совместимы с кодом Microsoft Edge.  Тем не менее Microsoft EDGE не поддерживает следующие API расширений:  

*   `chrome.gcm`  
*   `chrome.identity.getAccounts`  
*   `chrome.identity.getAuthToken`  
*   `chrome.instanceID`  

> [!Note]
> Чтобы использовать API, пользователь должен войти в Microsoft Edge с использованием учетной записи MSA или AAD `chrome.identity.getProfileUserInfo` .  Если пользователь вошел в Microsoft Edge с использованием **локальной рекламы**, API-интерфейс возвращает `null` для значений электронной почты и идентификаторов.  

> [!IMPORTANT]
> **Платежи**: Microsoft EDGE не поддерживает напрямую расширение, использующее [платежи веб-магазина Chrome][ChromeDeveloperWebStorePayments] из-за необходимости использования `identity.getAuthtoken` запроса для получения маркера для пользователей, которые вошли в систему для отправки запроса API лицензирования на основе оставшейся части.  Microsoft EDGE не поддерживает `getAuthtoken` запрос, поэтому этот поток не работает.  

Чтобы перенести расширение Chrome, выполните указанные ниже действия.  

1.  Ознакомьтесь с API расширения Chrome, используемых в расширениях.  Если вы используете функции или API-интерфейсы, которые не поддерживаются Microsoft EDGE, вы не можете перенести свое расширение.  
    
    > [!NOTE]
    > `getAuthToken`API не работает в Microsoft EDGE, однако вы можете использовать `launchWebAuthFlow` для получения маркера OAuth2 для проверки подлинности пользователей.  
    
1.  Если вы используете `Chrome` имя или описание расширения, Перепишите расширение `Microsoft Edge` .  Вы должны пройти процесс сертификации.  
    
1.  Проверьте расширение, чтобы убедиться в том, что он работает в Microsoft Edge.  Для этого сначала необходимо убедиться, что у вас есть функции разработчика расширений.  Это позволяет загружать файлы расширений в Microsoft Edge таким образом, чтобы вы могли протестировать расширение при разработке.  
    
1.  Если у вас возникли проблемы, выполните отладку расширений в Microsoft Edge с помощью DevTools или [свяжитесь с нами][mailtoExtensionPartnerOpsMicrosoft].  
    
1.  Теперь ваше расширение, наконец, будет готово к упаковке.  Если вы хотите подготовиться к отправке в каталог надстроек Microsoft Edge \ (надстройки Microsoft Edge \), вам не нужно будет упаковать расширение.  Далее следуйте [рекомендациям публикации][ExtensionsPublishExtension] , чтобы опубликовать расширение в надстройках Microsoft Edge.  
    
    > [!NOTE]
    > Если ваше расширение обменивается сообщениями с собственным приложением с помощью `chrome.runtime.connectNative` API-интерфейса, убедитесь, что для него установлен параметр " `allowedorigins` `extension://[Microsoft-Catalog-extensionID]` " в исходном файле манифеста узла сообщений.  Это позволяет приложению идентифицировать расширение.  

<!-- image links -->  

<!-- links -->  

[ExtensionsPublishExtension]: ../publish/publish-extension.md "Публикация расширения"  

[mailtoExtensionPartnerOpsMicrosoft]: mailto:extensionpartnerops@microsoft.com "ExtensionPartnerOps@microsoft.com"  

[ChromeDeveloperWebStorePayments]: https://developer.chrome.com/webstore/one_time_payments "Разовые платежи – Хром Google"  
