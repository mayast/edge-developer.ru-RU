---
ms.assetid: 88825563-5f5d-421d-861b-7cec01277dec
description: Сведения о том, как интерфейс API для проверки подлинности позволяет веб-приложениям использовать Windows Hello и FIDO2 для проверки подлинности пользователя.
title: 'Руководство по разработке: веб-проверка подлинности'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: windows-integration
keywords: EDGE, веб-разработка, HTML, CSS, JavaScript, разработчик
ms.openlocfilehash: cb561ae4147a24489138263a83dd37bd6f599074
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10571243"
---
# Проверка подлинности веб-сайта и Windows Hello

[Интерфейс API для проверки подлинности](https://w3c.github.io/webauthn) в Microsoft EDGE позволяет веб-приложениям использовать [Windows Hello](https://go.microsoft.com/fwlink/p/?LinkID=624961) и [внешние устройства FIDO2](https://fidoalliance.org/fido2) для проверки подлинности пользователей, чтобы пользователи могли избежать проблем и рисков управления паролями, включая распознавание пароля, фишинг и атаки с ведением журнала ключей. Текущая реализация Microsoft Edge основывается на рекомендациях спецификаций веб-проверки подлинности. **В этой статье показано, как опробовать Windows Hello и FIDO2 проверки подлинности в Microsoft Edge.**

С помощью веб-проверки подлинности сервер отправляет в браузер запрос на обычное текстовое сообщение. После того, как Microsoft Edge сможет проверить пользователя с помощью Windows Hello или внешнего устройства FIDO2, система подсможет подписать ее с помощью закрытого ключа, предварительно настроенного для этого пользователя, и отправить подпись обратно на сервер. Если сервер может проверить подпись с помощью открытого ключа, который он имеет для этого пользователя, и убедиться в правильности запроса, он может безопасно пройти проверку подлинности пользователя. При использовании [асимметричной криптографии](https://en.wikipedia.org/wiki/Public-key_cryptography) , например этого, Открытый ключ не имеет собственного смысла, и закрытый ключ никогда не будет общим. Кроме того, закрытый ключ не может быть перенесен из защищенных элементов или современных систем с аппаратным обеспечением, поддерживающим доверенный платформенный модуль.

Использование API проверки подлинности веб-страниц состоит из двух основных шагов.

**1. Зарегистрируйте пользователя с помощью `create`**

**2. подлинность пользователя с помощью `get`**

Следующее руководство по разработке поможет вам пройти этот процесс с помощью [примера приложения WebAuthn](https://github.com/MicrosoftEdge/webauthnsample).

## Регистрация пользователя

Выступающий в качестве *поставщика удостоверений*, необходимо сначала создать учетные данные для проверки подлинности для пользователя с помощью навигатора. Credentials. метод **CREATE** . Прежде чем регистрировать эти учетные данные для пользователя на сервере, вам нужно подтвердить удостоверение пользователя. Это можно сделать, отправив пользователю подтверждение по электронной почте или запросив его, чтобы использовать традиционный способ входа.


Этот `create` метод принимает следующие параметры:

 - **сведения о проверяющей стороне**

```javascript
    rp: {
        name: "WebAuthn Sample App",
        icon: "https://example.com/rpIcon.png"
    },
```

 - **сведения об учетной записи пользователя**

```javascript
    user: {
        id: stringToArrayBuffer("some.user.id"),
        name: "bob.smith@contoso.com",
        displayName: "Bob Smith",
        icon: "https://example.com/userIcon.png"
    },
```

 - **параметры шифрования**

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

 - **Параметры выделения для проверки подлинности**

```javascript
    authenticatorSelection: {
        //Select authenticators that support username-less flows
        requireResidentKey: true,
        //Select authenticators that have a second factor (e.g. PIN, Bio)
        userVerification: "required",
        //Selects between bound or detachable authenticators
        authenticatorAttachment: "platform"
    },
```

- **другие варианты**

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

Вы можете использовать [Параметры создания учетных данных](https://w3c.github.io/webauthn/#dictdef-publickeycredentialcreationoptions) для настройки учетных данных, которые вы хотите создать. В частности, вы можете создать учетные данные Windows Hello, указав параметр `authenticatorAttachment` `platform` или перемещаемые учетные данные на внешнем устройстве FIDO2, указав `authenticatorAttachment` значение `cross-platform` . 

При использовании этого `create` метода Microsoft Edge сначала запрашивает у пользователя проверку своего присутствия, проверяя их лицевую сторону или отпечаток, вводя ПИН-код или предпринимает действия на внешнем устройстве FIDO2. После завершения этого действия средство проверки подлинности создаст пару открытого и закрытого ключа и сохранит закрытый ключ. Эти учетные данные создаются для каждого происхождения, для каждой учетной записи и не могут быть извлечены, так как они безопасно хранятся на устройстве проверки подлинности. 

Результирующее обещание возвращает [объект аттестации](https://w3c.github.io/webauthn/#sctn-attestation) , представляющий новые учетные данные. Объект аттестации, содержащий открытый ключ для учетных данных. Вы отправите этот объект на сервер для проверки подлинности в будущем. Прежде чем отправлять обратно на сервер, вам потребуется Base64-кодирование необработанных данных.

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

После этого сервер должен декодировать объект аттестации, выполнить проверочные действия, извлечь открытый ключ для этих учетных данных и сохранить его для будущих проверок подлинности. Подробный список шагов можно найти в [алгоритме регистрации учетных данных](https://w3c.github.io/webauthn/#registering-a-new-credential) в спецификации WebAuthn.

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

После создания учетных данных на клиентском компьютере при следующем входе пользователя в систему вы можете подписаться на него с помощью своих учетных данных для проверки подлинности, а не пароля, вызываемого из звонка в Navigator. Credentials. **получить**.

Этот `get` метод принимает этот *запрос* в качестве единственного нужного параметра. Задача является непрозрачной последовательностью байтов, которую сервер отправляет клиенту для подписывания с помощью закрытого ключа пользователя. Пример

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

После получения запроса от сервера вы будете вызывать API Get вместе с [параметрами запроса учетных данных](https://w3c.github.io/webauthn/#credentialrequestoptions-extension). Microsoft Edge отобразит сообщение о том, что пользователь использует Windows Hello или внешнее устройство FIDO2 для проверки подлинности пользователя. После проверки пользователя проблема будет подписана в доверенном платформенном модуле или устройстве FIDO2, и обещание вернется с помощью [объекта утверждения](https://w3c.github.io/webauthn/#authenticatorassertionresponse) , содержащего подпись и другие метаданные, которые нужно отправить на сервер.

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

После получения утверждения на сервере вам потребуется проверить подпись для проверки подлинности пользователя. Ниже приведен пример кода.  Подробный список шагов можно найти в [алгоритме проверки утверждения](https://w3c.github.io/webauthn/#verifying-assertion) в спецификации WebAuthn.

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

## Заметки о внедрении

### Поддерживаемые платформы
- В Microsoft EDGE, начиная с EdgeHTML 18 (предварительной версии 17713 и более поздней версии), можно использовать ознакомительную версию рекомендаций API для проверки подлинности веб-сайта.
- [Предварительно исправленная версия](https://blogs.windows.com/msedgedev/2016/04/12/a-world-without-passwords-windows-hello-in-microsoft-edge/) API для проверки подлинности веб-сайта удалена и больше не доступна.
- API для веб-аутентификации пока не доступен для приложений UWP и PWAs.
- Internet Explorer не поддерживает API проверки подлинности веб-сайта. 

### Поддерживаемые средства проверки подлинности
С помощью API проверки подлинности в Microsoft EDGE можно проверять подлинность пользователей с помощью следующих технологий:
- **Windows Hello**, включение проверки подлинности на устройстве без пароля с использованием лицом, отпечатка пальца или PIN-кода
- **FIDO2**, включение проверки подлинности без пароля на съемном устройстве, а также отпечаток пальца или PIN-кода
- **U2F**, включение надежной второй проверки подлинности для веб-сайтов, не готовых к переходу на модель без пароля

### Специальные аспекты, касающиеся Windows Hello 
Некоторые моменты, которые необходимо учитывать при использовании средства проверки подлинности Windows Hello:
- Вы можете определить, доступен ли Windows Hello на компьютере, вызвав `isUserVerifyingPlatformAuthenticatorAvailable` API. Дополнительные сведения об [этом API.](https://www.w3.org/TR/webauthn/#isUserVerifyingPlatformAuthenticatorAvailable)
- Если вы создаете учетные данные для Windows Hello, вы должны использовать `authenticatorAttachment` `platform` для наилучшего взаимодействия с пользователем.
- Windows Hello поддерживает только RS256 (ALG-257) в качестве алгоритма открытого ключа. Не забудьте указать этот алгоритм при создании учетных данных.
- Чтобы получить [инструкцию аттестации TPM](https://w3c.github.io/webauthn/#tpm-attestation), установите для аттестации значение Direct при вызове `create` API. Аттестация доверенного платформенного модуля является наилучшим усилием. Только компьютеры с доверенным платформенным модулем 2,0 возвращают инструкцию аттестации TPM, и процесс аттестации может завершиться сбоем по различным причинам.
- В Windows Hello есть различные способы защиты учетных данных пользователя. Вы можете проверить, какой метод был использован для защиты учетных данных, заменив поле [AAGUID](https://w3c.github.io/webauthn/#sec-attested-credential-data) в объекте аттестации, возвращаемом при создании учетных данных. Ниже приведен список AAGUIDs, которые может возвращать Windows Hello. 
  - Программное обеспечение для проверки подлинности
    - Средство проверки подлинности программного обеспечения Windows Hello: `6028B017-B1D4-4C02-B4B3-AFCDAFC96BB2`
    - Программа проверки подлинности Windows Hello VBS: `6E96969E-A5CF-4AAD-9B56-305FE6C82795`
  - Резервные средства проверки подлинности доверенного платформенного модуля (TPM)
    - Средство проверки подлинности оборудования для Windows Hello: `08987058-CADC-4B81-B6E1-30DE50DCBE96`
    - Средство проверки подлинности оборудования для Windows Hello VBS: `9DDD1817-AF5A-4672-A2B9-3E3DD95000A9`


### Поверхность API
- Microsoft Edge имеет полную реализацию версии рекомендации кандидата спецификации основной веб-проверки подлинности.
- [Расширение AppID](https://w3c.github.io/webauthn/#sctn-appid-extension) поддерживается. 
- Другие расширения не поддерживаются.


## Демонстрационные примеры

[Пример кода клиента и сервера](https://github.com/MicrosoftEdge/webauthnsample)

[Демонстрация пробного диска Windows Hello](https://webauthnsample.azurewebsites.net/)

## Specification

[Веб-проверка подлинности: API для доступа к учетным данным открытого ключа](http://w3c.github.io/webauthn/)
