---
ms.assetid: 88825563-5f5d-421d-861b-7cec01277dec
description: Узнайте, как API веб-проверки подлинности может разрешить использование веб-приложений для проверки подлинности пользователей с помощью Windows Hello и FIDO2.
title: Веб-проверка подлинности для веб-страниц — разработка
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/28/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: windows-integration
keywords: Edge, разработчики, html, css, javascript, разработчики
ms.openlocfilehash: b8ff3769434c17b5508978c64b5d9c14e7e3bdaa
ms.sourcegitcommit: 29cbe0f464ba0092e025f502833eb9cc3e02ee89
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "10941817"
---
# Веб-аутентификация и Windows Hello  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

[API](https://w3c.github.io/webauthn) веб-аутентификации в Microsoft Edge позволяет веб-приложениям использовать для проверки подлинности [Windows Hello](https://www.microsoft.com/windows/comprehensive-security) [и внешние устройства FIDO2](https://fidoalliance.org/fido2) для проверки подлинности пользователей, чтобы пользователи и пользователи не смог избежать рисков управления паролями, включая предоставление рекомендаций о защите паролей, фишинга и ключевых атак.  Текущая рекомендация Microsoft Edge основана на рекомендации по спецификации веб-проверки подлинности.  

> [!IMPORTANT]
> Из этой статьи вы узнаете, как пробовать проверку подлинности Windows Hello и FIDO2 в Microsoft Edge.  

При использовании веб-проверки сервер отправляет запросы в браузере в обычном тексте.  После того как Microsoft Edge сможет проверить пользователя с помощью Windows Hello или внешнего устройства FIDO2, система подписывает проблему с частным ключом, который ранее подготовлен для этого пользователя и отправит на сервер подпись.  Если сервер может проверить подпись с помощью общедоступного ключа, имеющего этот пользователь, и проверить правильность проблемы, проверка подлинности пользователя может оказаться надежной.  [Благодаря](https://en.wikipedia.org/wiki/Public-key_cryptography) асимметричной широкостью общедоступный ключ означает, что общедоступный ключ самостоятельно имеет вид и личный ключ никогда не предоставляется.  Более того, закрытый ключ никогда нельзя перемещать из безопасных элементов или современных систем с аппаратным и современным ими дисплеями по протоколу TPM.  

Существует два основных шага, которые нужно выполнить с помощью API веб-проверки подлинности.  

1.  Регистрация пользователя `create`  
1.  Проверка подлинности пользователя `get`  

В приведенном ниже руководстве поможет вам выполнить этот поток [с помощью приложения WebAuthn Sample.](https://github.com/MicrosoftEdge/webauthnsample)  

## Регистрация пользователя  

Для пользователей с методом удостоверения сначала потребуется создать для пользователя учетные данные для `navigator.credentials.create` веб-аутентификации.  Перед регистрацией учетных данных для пользователя на сервере необходимо подтвердить личность пользователя.  Для этого можно отправить пользователю электронное письмо с подтверждением или попросить его использовать традиционный способ входа.  

При `create` выборе метода имеются следующие параметры:  

:::row:::
   :::column span="1":::
      **отражение сведений о вечеринке**  
   :::column-end:::
   :::column span="3":::
      ```javascript
      rp: {
          name: "WebAuthn Sample App",
          icon: "https://example.com/rpIcon.png"
      },
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **сведения об учетной записи пользователя**  
   :::column-end:::
   :::column span="3":::
      ```javascript
      user: {
          id: stringToArrayBuffer("some.user.id"),
          name: "bob.smith@contoso.com",
          displayName: "Bob Smith",
          icon: "https://example.com/userIcon.png"
      },
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **параметры велосипедов**  
   :::column-end:::
   :::column span="3":::
      ```javascript
      pubKeyCredParams: [
          {
              //External authenticators support the ES256 algorithm
              type: "public-key",
              alg: -7                 
          }, 
          {
              //Windows Hello supports the RS256 algorithm
              type: "public-key",
              alg: -257
          }
      ],
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **параметры проверки подлинности**  
   :::column-end:::
   :::column span="3":::
      ```javascript
      authenticatorSelection: {
          //Select authenticators that support username-less flows
          requireResidentKey: true,
          //Select authenticators that have a second factor (such as PIN, Bio)
          userVerification: "required",
          //Selects between bound or detachable authenticators
          authenticatorAttachment: "platform"
      },
      ```  
   :::column-end:::
:::row-end:::  
:::row:::
   :::column span="1":::
      **другие параметры**  
   :::column-end:::
   :::column span="3":::
      ```javascript
      //Select larger timeout values, as Microsoft Edge shows UI
      timeout: 50000,
      //an opaque challenge that the authenticator signs over
      challenge: challenge,
      //prevent re-registration by specifying existing credentials here
      excludeCredentials: [],
      //specifies whether you need an attestation statement
      attestation: "none" 
      ```  
   :::column-end:::
:::row-end:::  

Для настройки [учетных](https://w3c.github.io/webauthn#dictdef-publickeycredentialcreationoptions) данных можно использовать параметры создания учетных данных.  В частли, вы можете создать учетные данные Windows Hello, установив для этого параметр или учетные данные `authenticatorAttachment` `platform` роуминга на внешнем устройстве FIDO2, установив `authenticatorAttachment` `cross-platform` параметр.  

При использовании метода Microsoft Edge сначала просит пользователя подтвердить свой принтер, сканируя свое состояние лица или `create` отпечатка пальца, вводить ПИН-код или выполнить действия на внешнем устройстве FIDO2.  После завершения этого действия проверка подлинности создаст открытую пару и сохранит частный ключ.  Эти учетные данные создаются для каждого происхождения, каждой учетной записи и их немогут быть извлечены, так как безопасно храниться на устройстве проверки подлинности.  

Исходящий объект вернет объект [популярности,](https://w3c.github.io/webauthn#sctn-attestation) представляющий новые учетные данные.  Объект попытки содержит открытый ключ учетных данных.  Этот объект отправляется на сервер для проверки будущей проверки подлинности.  Прежде чем отправлять сервер на сервер, необходимо основание 64-разрядной кодировки неработающих данных.  

**Клиент**  

```javascript
<script>
    navigator.credentials.create({
        publicKey: createCredentialOptions
    }).then(rawAttestation => {
        var attestation = {
            id: base64encode(rawAttestation.rawId),
            clientDataJSON: arrayBufferToString(rawAttestation.response.clientDataJSON),
            attestationObject: base64encode(rawAttestation.response.attestationObject)
        };
        return rest_put("/credentials", attestation);
    })
</script>
```  

Затем сервер должен отнять объект попытки, выполнить процедуру проверки, извлечь извлеченный общедоступный ключ для этого учетных данных и сохранить его для дальнейшей проверки подлинности.  Подробный список шагов можно найти в [алгоритме](https://w3c.github.io/webauthn#registering-a-new-credential) спецификации WebAuthn.  

**Сервер**  

```javascript
    attestationObject = cbor.decodeFirstSync(Buffer.from(attestation.attestationObject, 'base64'));
    authenticatorData = parseAuthenticatorData(attestationObject.authData);
    var credential = await storage.Credentials.create({
        id: authenticatorData.attestedCredentialData.credentialId.toString('base64'),
        publicKeyJwk: authenticatorData.attestedCredentialData.publicKeyJwk,
        signCount: authenticatorData.signCount
    });
```  

## Проверка подлинности пользователя  

После того как пользователь появится в клиенте, при следующей попытке войти на сайт вы сможете войти на сайт, используя учетные данные для веб-проверки подлинности вместо того, чтобы убедиться `navigator.credentials.get` в этом.  

Способ принимает задание только в качестве обязательных `get` параметров.  Проблема — это непрозрачная последовательность байтов, которые сервер отправляет клиенту клиенту для входа в свой клиент для регистрации с частным ключом пользователя.  Например:  

**Сервер**  

```javascript
    var jwt = require('jsonwebtoken');
    var jwt_secret = "defaultsecret";
    fido.getChallenge = () => {
        return jwt.sign({}, jwt_secret, {
            expiresIn: 120 * 1000
        });
    };
```  

После получения проблемы с сервера вы звоните по API получения API и варианты ответа с [учетными данными.](https://w3c.github.io/webauthn#credentialrequestoptions-extension)  Microsoft Edge отобразит запрос, в котором подтверждение личности пользователя с помощью Windows Hello или внешнего устройства FIDO2 будет выведено.  После проверки проблема будет вошедшена в устройство TPM или FIDO2, и оборудование вернет с [объектом вложения](https://w3c.github.io/webauthn#authenticatorassertionresponse) и другими метаданными, которые вы хотите отправить на сервер.  

**Клиент**  

```javascript
    var credentialRequestOptions = {
        //specifies which credential IDs are allowed to authenticate the user
        //if empty, any credential can authenticate the users
        allowCredentials: allowCredentials,
        //an opaque challenge that the authenticator signs over
        challenge: challenge,
        //Select larger timeout values, as Microsoft Edge shows UI
        timeout: 50000
    };

    navigator.credentials.get({
        publicKey: credentialRequestOptions
    }).then(rawAssertion => {
        var assertion = {
            id: base64encode(rawAssertion.rawId),
            clientDataJSON: arrayBufferToString(rawAssertion.response.clientDataJSON),
            userHandle: base64encode(rawAssertion.response.userHandle),
            signature: base64encode(rawAssertion.response.signature),
            authenticatorData: base64encode(rawAssertion.response.authenticatorData)
        };
        return rest_put("/assertion", assertion);
    })
```  

Получив такое средство на сервере, необходимо проверить подпись для проверки подлинности пользователя.  Ниже приведен пример кода.  Подробный список действий можно найти [assertion verification algorithm](https://w3c.github.io/webauthn#verifying-assertion) в алгоритме проверки вспомогательной проверки в спецификации WebAuth.  

**Сервер**  

```javascript
    var jwkToPem = require('jwk-to-pem')
    var crypto = require('crypto');

    ...

    // Using credential’s id attribute, look up the corresponding 
    // credential public key.
    var credential = await storage.Credentials.findOne({
        id: assertion.id
    });

    //Refer to sample to see how to verify client data and authenticator data

    ...

    //Using the credential public key from lookup, verify that sig is a valid
    //signature over the binary concatenation of authData and hash.
    var publicKey = credential.publicKeyJwk;
    var verify = (publicKey.kty === "RSA") ? crypto.createVerify('RSA-SHA256') : crypto.createVerify('sha256');
    verify.update(authData);
    verify.update(hash);
    if (!verify.verify(jwkToPem(publicKey), sig))
        throw new Error("Could not verify signature");

    //Verify signCount has increased or is zero 
    if (authenticatorData.signCount != 0 &&
        authenticatorData.signCount < credential.signCount) {
        throw new Error("Received signCount of " + authenticatorData.signCount +
            " expected signCount > " + credential.signCount);
    }
```  

## Примечания к внедрению  

### Поддерживаемые платформы  

*   Рекомендации по использованию API веб-проверки подлинности можно использовать из Microsoft Edge начиная с EdgeHTML 18 \(Windows Insider Preview версии 17713 или более поздней версии).)  
*   Предварительная [версия](https://blogs.windows.com/msedgedev/2016/04/12) API веб-проверки подлинности удалена и теперь недоступна.  
*   API веб-проверки еще недоступен для приложений UWP и PWAs.  
*   Internet Explorer не поддерживает API веб-проверки подлинности.  

### Поддерживаемая проверка подлинности  

С помощью API веб-проверки подлинности в Microsoft Edge можно пройти проверку подлинности пользователей со следующими технологиями:  

*   **Windows Hello**  Включение проверки подлинности пароля на устройстве с помощью лица, отпечатка отпечатка пальца или ПИН-адреса.  
*   **FIDO2**  Включает перемещаемую проверку подлинности с помощью старого устройства и пин-кода или ПИН-кода.  
*   **U2F**  Включает надежную вторую проверку подлинности для веб-сайтов, которые не готовы перейти к модели пароля.  

### Особенности Windows Hello  

При использовании проверки подлинности Windows Hello нужно заметить следующее:  

*   Чтобы выяснить, доступна ли Windows Hello, позвонив `isUserVerifyingPlatformAuthenticatorAvailable` API.  Подробнее об этом API [здесь.](https://www.w3.org/TR/webauthn#isUserVerifyingPlatformAuthenticatorAvailable)  
*   При создании учетных данных для Windows Hello следует задать для `authenticatorAttachment` оптимального `platform` взаимодействия.
*   Windows Hello поддерживает только rS256 \(alg -257\) в качестве общедоступного ключа.  Не забудьте указать этот алгоритм при создании учетных данных.  
*   Чтобы получить [оператор по птации попытки TPM,](https://w3c.github.io/webauthn#tpm-attestation)присвойте попытку аудитории на прямую `create` попытку.  Попытка TPM — лучше.  Это может быть только для пограничных причин.  
*   Windows Hello предусматривают различные способы защиты учетных данных пользователя.  Чтобы проверить, какой метод использовался для защиты учетных данных, можно зарезервировать поле [AAGUID](https://w3c.github.io/webauthn#sec-attested-credential-data) объекта атестации, возвращенного при создании учетных данных.  Вот список агрегатных функций Windows Hello:   
    *   Программное обеспечение обратно проверке подлинности  
        *   Проверка подлинности программного обеспечения Windows Hello:  `6028B017-B1D4-4C02-B4B3-AFCDAFC96BB2`  
        *   Проверка подлинности программного обеспечения Windows Hello VBS:  `6E96969E-A5CF-4AAD-9B56-305FE6C82795`  
    *   Надежная платформа \(TPM\) обратно  
        *   Аппаратная проверка подлинности Windows Hello:  `08987058-CADC-4B81-B6E1-30DE50DCBE96`  
        *   Аппаратная проверка подлинности Windows Hello VBS:  `9DDD1817-AF5A-4672-A2B9-3E3DD95000A9`  

### Поверхности API API  

*   В Microsoft Edge есть полное рекомендации по рекомендациям по рекомендации по корректировке корпоративной версии главной спецификации веб-проверки подлинности.  
*   [Расширение AppID](https://w3c.github.io/webauthn#sctn-appid-extension) поддерживается.  
*   Другие расширения не поддерживаются.  

## Демонстрационные примеры  

[Пример кода клиента и сервера](https://github.com/MicrosoftEdge/webauthnsample)  

[Демонстрация диска Windows Hello](https://webauthnsample.azurewebsites.net)  

## Спецификаци  

[Веб-проверка подлинности: API доступа к aPI для доступа к учетным данным общего ключа](http://w3c.github.io/webauthn)  
