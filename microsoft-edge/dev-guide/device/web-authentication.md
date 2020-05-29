---
ms.assetid: 88825563-5f5d-421d-861b-7cec01277dec
description: Сведения о том, как можно использовать API проверки подлинности веб-приложений для использования биометрии Windows Hello для проверки подлинности пользователей.
title: 'Руководство по разработке: веб-проверка подлинности'
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 01/15/2020
ms.topic: article
ms.prod: microsoft-edge
keywords: EDGE, веб-разработка, HTML, CSS, JavaScript, разработчик
ms.openlocfilehash: c49d181633ae1b2b35aa0f88287841d28e806f44
ms.sourcegitcommit: 6860234c25a8be863b7f29a54838e78e120dbb62
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/09/2020
ms.locfileid: "10570898"
---
# Проверка подлинности веб-сайта и Windows Hello

API проверки подлинности (прежнее название — *FIDO 2,0* ) в Microsoft EDGE позволяет веб-приложениям использовать биометрию [Windows Hello](https://go.microsoft.com/fwlink/p/?LinkID=624961) для проверки подлинности пользователя, чтобы пользователи могли избежать проблем и рисков управления паролями, включая подбор пароля, фишинг и атаки Keylogging. Текущая реализация Microsoft EDGE (*предварительно* фиксированная версия) основана на более ранней версии спецификации веб-проверки подлинности и, как правило, изменяется в будущем. **В этой статье объясняется, как попробовать проверить подлинность Windows Hello с помощью Microsoft EDGE, в то время как в будущем код будет проверяться в соответствии с обновлениями браузера.**

Интерфейс API для проверки подлинности — это развивающаяся Стандартная функция [Fido Alliance](https://fidoalliance.org/) , обеспечивающая взаимодействие веб-проверки подлинности с помощью Windows Hello и других биометрических устройств в разных браузерах. Определение веб-проверки подлинности определяет два сценария проверки подлинности: пароль не менее двух факторов. В случае отсутствия пароля пользователю не нужно входить на веб-страницу с помощью имени пользователя или пароля — он может войти исключительно с помощью Windows Hello. В двух корпусах, пользователь входит в систему с помощью имени пользователя и пароля, но Windows Hello используется в качестве второго фактора для более надежной проверки подлинности.

С помощью веб-проверки подлинности, Объединенной с Windows Hello, сервер отправляет в браузер запрос на обычное текстовое сообщение. После того, как Microsoft Edge сможет проверить пользователя с помощью Windows Hello, система подсможет подписать ее с помощью закрытого ключа, ранее подготовленного для этого пользователя, и отправить подпись обратно на сервер. Если сервер может проверить подпись с помощью открытого ключа, который он имеет для этого пользователя, и убедиться в правильности запроса, он может безопасно пройти проверку подлинности пользователя. При использовании [асимметричной криптографии](https://en.wikipedia.org/wiki/Public-key_cryptography) , например этого, Открытый ключ не имеет собственного смысла, и закрытый ключ никогда не будет общим. Кроме того, закрытый ключ не может быть перенесен из современной системы с аппаратным обеспечением, поддерживающим доверенный платформенный модуль.

Использование API проверки подлинности веб-страниц состоит из двух основных шагов.

**1. Зарегистрируйте пользователя с помощью `makeCredential`**

**2. подлинность пользователя с помощью `getAssertion`**

Приведенные ниже инструкции помогут Вам пошагово пройти этот процесс, используя рекомендуемый [заполненный Webauthn. js](https://github.com/adrianba/fido-snippets/blob/master/polyfill/webauthn.js). [Полный код](https://github.com/adrianba/fido-snippets/) доступен для этого сервера и демонстрации на стороне клиента. Поддерживаются серверные версии на [языках C#](https://github.com/adrianba/fido-snippets/tree/master/csharp), [PHP](https://github.com/adrianba/fido-snippets/tree/master/php)и [node. js](https://github.com/adrianba/fido-snippets/tree/master/nodejs) .

## Регистрация пользователя

Выступающий в качестве *поставщика удостоверений*, необходимо сначала создать для пользователя учетные данные для проверки подлинности веб-сайта с помощью Window. webauthn. метод **makeCredential** . Прежде чем регистрировать эти учетные данные для пользователя на сервере, вам нужно подтвердить удостоверение пользователя. Это можно сделать, отправив пользователю подтверждение по электронной почте или запросив его, чтобы использовать традиционный способ входа.

Метод makeCredential принимает следующие параметры:
 - **сведения об учетной записи пользователя**

```
    var userAccountInformation = {
        rpDisplayName: "fido-demo",
        displayName: email
    };
```

 - **параметры шифрования**

```
    var cryptoParams = [
        {
            type: "ScopedCred",
            algorithm: "RSASSA-PKCS1-v1_5",
        }
    ];
```

Результирующее обещание возвращает объект, представляющий учетные данные, которые вы затем отправляете обратно на сервер для проверки подлинности в будущем.

**Клиент**

```
<script src="webauthn.js"><!-- polyfill to map Microsoft Edge experimental implementation to current W3C spec --></script>
<script>
    var email = '<%=user.email%>';
    var name = '<%=user.name%>';

    webauthn.makeCredential(userAccountInformation, cryptoParams)
        .then(function (creds) {
            document.getElementById('form-id').value = creds.credential.id;
            document.getElementById('form-pk').value = JSON.stringify(creds.publicKey);
            document.getElementById('form-email').value = email;
            document.getElementById('form-name').value = name;
            document.getElementById('theform').submit();
        }).catch(function (err) {
            // No acceptable authenticator or user refused consent. Handle appropriately.
            alert(err);
        });
</script>
```

При использовании метода makeCredential приложение Microsoft Edge сначала попросят Windows Hello использовать идентификацию лицом или отпечатком пальцев, чтобы убедиться в том, что пользователь имеет тот же пользователь, что и вход в учетную запись Windows. После завершения этого действия служба Microsoft Passport создаст пару открытого и закрытого ключа и сохранит закрытый ключ в доверенном платформенном модуле (TPM), который использовался для хранения учетных данных на специальном оборудовании процессора шифрования. Если у пользователя нет устройства с поддержкой доверенного платформенного модуля, эти ключи будут храниться в программном обеспечении. Эти учетные данные создаются для каждого источника, для каждой учетной записи Windows и не будут перемещены, так как они привязаны к устройству. Это означает, что вы должны убедиться, что пользователь регистрируется для использования Windows Hello для каждого используемого ими устройства.

## Проверка подлинности пользователя

После создания учетных данных на клиентском компьютере при следующем входе пользователя в систему с помощью Windows Hello вместо пароля с вызовом Window. webauthn. " **включено**".

Методического *утверждения используется в качестве* единственного нужного параметра. Задача — это случайное количество, которое сервер отправляет клиенту для подписания с помощью закрытого ключа пользователя. Пример

**Сервер**

```
var crypto = require('crypto');

Strategy.prototype.generateChallenge = function() {
    return this.generateVerifiableString(crypto.randomBytes(32));
};

Strategy.prototype.generateVerifiableString = function(data) {
    // Create cipher using secret
    var d = new Buffer(data);
    var c = crypto.createCipher('aes192',new Buffer(this._secret));

    // Encrypt data
    c.update(d);

    // Hash results of encrypting data
    var hash = crypto.createHash('sha256');
    hash.update(c.final());

    // Combine original data with hash
    return d.toString('hex') + string_separator + hash.digest('hex');
};
```

После вызова методаического утверждения Microsoft Edge отобразит запрос Windows Hello, который будет проверять удостоверение пользователя с помощью биометрии. После проверки пользователя проблема будет подписана в доверенном платформенном модуле, и обещание будет возвращаться с помощью объекта утверждения, содержащего подпись и другие метаданные, которые нужно отправить на сервер.

**Клиент**

```
<script src="webauthn.js"><!-- polyfill to map Microsoft Edge experimental implementation to current W3C spec --></script>
<script>
    var challenge = '<%=challenge%>';

    webauthn.getAssertion(challenge)
    .then(function(assertion) {
      document.getElementById("form-id").value = assertion.credential.id;
      document.getElementById("form-type").value = assertion.credential.type;
      document.getElementById("form-data").value = assertion.clientData;
      document.getElementById("form-sig").value = assertion.signature;
      document.getElementById("form-authnr").value = assertion.authenticatorData;
      document.getElementById("form-challenge").value = challenge;
      document.getElementById("theform").submit();
    })
    .catch(function(err) {
      if(err && err.name) {
        document.getElementById("form-err").value = err.name;
      } else {
        document.getElementById("form-err").value = "unknown";
      }
      document.getElementById("theform").submit();
    });

</script>
```

После получения утверждения на сервере вам потребуется проверить подпись для проверки подлинности пользователя. Например (в Node. JS):

**Сервер**

```
var jwkToPem = require('jwk-to-pem')
var crypto = require('crypto');

var fidoAuthenticator = {
     validateSignature: function (publicKey, clientData, authnrData, signature, challenge) {
         // Make sure the challenge in the client data
         // matches the expected challenge
         var c = new Buffer(clientData, 'base64');
         var cc = JSON.parse(c.toString().replace(/\0/g,''));
         if(cc.challenge != challenge) return false;

         // Hash data with sha256
         const hash = crypto.createHash('sha256');
         hash.update(c);
         var h = hash.digest();

         // Verify signature is correct for authnrData + hash
         var verify = crypto.createVerify('RSA-SHA256');
         verify.update(new Buffer(authnrData,'base64'));
         verify.update(h);
         return verify.verify(jwkToPem(JSON.parse(publicKey)), signature, 'base64');
     }
};   
```

## Различия между Microsoft EDGE и спецификацией

> [!NOTE]
> При попытке использовать веб-интерфейс проверки подлинности в Windows Hello в Microsoft Edge мы рекомендуем воспользоваться заполнением Webauthn. js, как показано выше, чтобы не учитывать указанные здесь расхождения. Мы будем обновлять эту козаполнение для каждой крупной опубликованной версии спецификации.


Текущая реализация Microsoft Edge основывается на более ранней версии спецификации веб-проверки подлинности и, возможно, будет изменена в будущих сборках, а также по мере развития спецификаций. Ниже приведены некоторые из текущих различий.

- API Microsoft EDGE имеют префиксы.
- Microsoft Edge пока не поддерживает внешние учетные данные, такие как USB-ключи или устройства Bluetooth. Текущий API ограничивается внедренными учетными данными, хранящимися в TPM.
- Учетная запись пользователя Windows, зарегистрированная в системе, должна поддерживать по крайней мере ПИН-код, а предпочтительнее или биометрию отпечатков пальцев. Это необходимо для того, чтобы система Windows могла проверить подлинность доступа к доверенному платформенному модулю.
- Реализация Microsoft Edge пока не поддерживает возможности выбора учетной записи.
- Второй параметр *фильтров* , указывающий идентификатор учетных данных, в настоящее время нужен для звонков в msCredentials. " [включено](https://msdn.microsoft.com/library/mt697640)". Таким образом, при создании учетных данных вам потребуется хранить ИДЕНТИФИКАЦИОНные данные в локальном хранилище на клиенте либо в indexDB, либо localStorage. Если пользователь удаляет журнал браузера, включая локальное хранилище, ему потребуется повторно зарегистрироваться для использования Windows Hello при следующем входе в систему.
- Microsoft EDGE не поддерживает все параметры в текущем черновике веб-проверки подлинности, такие как расширения или таймауты.

На последнем этапе указанные отличия Microsoft Edge указаны в описании перечисленных ниже определений проверки подлинности веб-сайта.

### W3C specs

```
partial interface Window {
    readonly attribute WebAuthentication webauthn; // msCredentials
};

interface WebAuthentication { // MSCredentials
    Promise <ScopedCredentialInfo> makeCredential (
        Account                                 accountInformation,
        sequence <ScopedCredentialParameters>   cryptoParameters,
        DOMString                               attestationChallenge, // Optional in Microsoft Edge
        optional unsigned long                  credentialTimeoutSeconds, // Not yet supported
        optional sequence <Credential>          blacklist, // Not yet supported
        optional WebAuthnExtensions             credentialExtensions // Not yet supported
    );

    Promise <WebAuthnAssertion> getAssertion (
        DOMString                        assertionChallenge,
        optional unsigned long           assertionTimeoutSeconds, // Not yet supported
        optional sequence <Credential>   whitelist, // Not yet supported
        optional WebAuthnExtensions      assertionExtensions // Not yet supported
    );
};

interface ScopedCredentialInfo { // MSAssertion
    readonly attribute Credential           credential;
    readonly attribute any                  publicKey;
    readonly attribute AttestationStatement attestation;
};

dictionary Account { // MSAccountInfo
    required DOMString rpDisplayName;
    required DOMString displayName;
    DOMString          name; // Not yet supported
    DOMString          id; // Not yet supported
    DOMString          imageUri; // Not yet supported
};

dictionary ScopedCredentialParameters { // MSCredentialParameters
    required CredentialType        type;
    required AlgorithmIdentifier   algorithm;
};

enum CredentialType { // MSCredentialType
    "ScopedCred" // Must be "FIDO_2_0" in Microsoft Edge
};

interface Credential { // MSCredentialSpec
    readonly attribute CredentialType type;
    readonly attribute DOMString      id;
};

dictionary WebAuthnExtensions { // Not supported
};
```



## Справочные материалы по API

[MSCredentials](https://msdn.microsoft.com/library/mt697639)

[makeCredential](https://msdn.microsoft.com/library/mt697641)

[не поддается утверждению](https://msdn.microsoft.com/library/mt697640)

## Демонстрационные примеры

[Примеры кода клиента и сервера](https://github.com/adrianba/fido-snippets/)

[Заполнение Webauthn. js](https://github.com/adrianba/fido-snippets/blob/master/polyfill/webauthn.js)

[Демонстрация пробного диска Windows Hello](https://testdrive-fido.azurewebsites.net/)

## Specification

[Веб-проверка подлинности: веб-API для доступа к учетным данным с областью действия 1](http://w3c.github.io/webauthn/)  
