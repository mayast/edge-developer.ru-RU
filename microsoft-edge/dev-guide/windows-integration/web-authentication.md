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
# <span data-ttu-id="b7c42-104">Проверка подлинности веб-сайта и Windows Hello</span><span class="sxs-lookup"><span data-stu-id="b7c42-104">Web Authentication and Windows Hello</span></span>

<span data-ttu-id="b7c42-105">[Интерфейс API для проверки подлинности](https://w3c.github.io/webauthn) в Microsoft EDGE позволяет веб-приложениям использовать [Windows Hello](https://go.microsoft.com/fwlink/p/?LinkID=624961) и [внешние устройства FIDO2](https://fidoalliance.org/fido2) для проверки подлинности пользователей, чтобы пользователи могли избежать проблем и рисков управления паролями, включая распознавание пароля, фишинг и атаки с ведением журнала ключей.</span><span class="sxs-lookup"><span data-stu-id="b7c42-105">The [Web Authentication API](https://w3c.github.io/webauthn) in Microsoft Edge enables web applications to use [Windows Hello](https://go.microsoft.com/fwlink/p/?LinkID=624961) and [external FIDO2 devices](https://fidoalliance.org/fido2) for user authentication so that you and your users can avoid all the hassles and risks of password management, including password guessing, phishing, and key-logging attacks.</span></span> <span data-ttu-id="b7c42-106">Текущая реализация Microsoft Edge основывается на рекомендациях спецификаций веб-проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="b7c42-106">The current Microsoft Edge implementation is based on the Candidate Recommendation of the Web Authentication specification.</span></span> **<span data-ttu-id="b7c42-107">В этой статье показано, как опробовать Windows Hello и FIDO2 проверки подлинности в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="b7c42-107">This topic will show you how to try out Windows Hello and FIDO2 authentication with Microsoft Edge.</span></span>**

<span data-ttu-id="b7c42-108">С помощью веб-проверки подлинности сервер отправляет в браузер запрос на обычное текстовое сообщение.</span><span class="sxs-lookup"><span data-stu-id="b7c42-108">Using Web Authentication, the server sends down a plain text challenge to the browser.</span></span> <span data-ttu-id="b7c42-109">После того, как Microsoft Edge сможет проверить пользователя с помощью Windows Hello или внешнего устройства FIDO2, система подсможет подписать ее с помощью закрытого ключа, предварительно настроенного для этого пользователя, и отправить подпись обратно на сервер.</span><span class="sxs-lookup"><span data-stu-id="b7c42-109">Once Microsoft Edge is able to verify the user through Windows Hello or an external FIDO2 device, the system will sign the challenge with a private key previously provisioned for this user and send the signature back to the server.</span></span> <span data-ttu-id="b7c42-110">Если сервер может проверить подпись с помощью открытого ключа, который он имеет для этого пользователя, и убедиться в правильности запроса, он может безопасно пройти проверку подлинности пользователя.</span><span class="sxs-lookup"><span data-stu-id="b7c42-110">If the server can validate the signature using the public key it has for that user and verify the challenge is correct, it can authenticate the user securely.</span></span> <span data-ttu-id="b7c42-111">При использовании [асимметричной криптографии](https://en.wikipedia.org/wiki/Public-key_cryptography) , например этого, Открытый ключ не имеет собственного смысла, и закрытый ключ никогда не будет общим.</span><span class="sxs-lookup"><span data-stu-id="b7c42-111">With [asymmetric cryptography](https://en.wikipedia.org/wiki/Public-key_cryptography) such as this, the public key is meaningless on its own and the private key is never shared.</span></span> <span data-ttu-id="b7c42-112">Кроме того, закрытый ключ не может быть перенесен из защищенных элементов или современных систем с аппаратным обеспечением, поддерживающим доверенный платформенный модуль.</span><span class="sxs-lookup"><span data-stu-id="b7c42-112">Furthermore, the private key can never be moved from secure elements or modern systems with TPM-enabled hardware.</span></span>

<span data-ttu-id="b7c42-113">Использование API проверки подлинности веб-страниц состоит из двух основных шагов.</span><span class="sxs-lookup"><span data-stu-id="b7c42-113">There are two basic steps to using the Web Authentication API:</span></span>

**<span data-ttu-id="b7c42-114">1. Зарегистрируйте пользователя с помощью</span><span class="sxs-lookup"><span data-stu-id="b7c42-114">1. Register your user with</span></span> `create`**

**<span data-ttu-id="b7c42-115">2. подлинность пользователя с помощью</span><span class="sxs-lookup"><span data-stu-id="b7c42-115">2. Authenticate your user with</span></span> `get`**

<span data-ttu-id="b7c42-116">Следующее руководство по разработке поможет вам пройти этот процесс с помощью [примера приложения WebAuthn](https://github.com/MicrosoftEdge/webauthnsample).</span><span class="sxs-lookup"><span data-stu-id="b7c42-116">The following dev guide will walk you through this flow using the [WebAuthn Sample App](https://github.com/MicrosoftEdge/webauthnsample).</span></span>

## <span data-ttu-id="b7c42-117">Регистрация пользователя</span><span class="sxs-lookup"><span data-stu-id="b7c42-117">Register your user</span></span>

<span data-ttu-id="b7c42-118">Выступающий в качестве *поставщика удостоверений*, необходимо сначала создать учетные данные для проверки подлинности для пользователя с помощью навигатора. Credentials. метод **CREATE** .</span><span class="sxs-lookup"><span data-stu-id="b7c42-118">Acting as an *identity provider*, you will first need to create a Web Authentication credential for your user with the navigator.credentials.**create** method.</span></span> <span data-ttu-id="b7c42-119">Прежде чем регистрировать эти учетные данные для пользователя на сервере, вам нужно подтвердить удостоверение пользователя.</span><span class="sxs-lookup"><span data-stu-id="b7c42-119">Before you register that credential to the user on your server, you will need to confirm the identity of the user.</span></span> <span data-ttu-id="b7c42-120">Это можно сделать, отправив пользователю подтверждение по электронной почте или запросив его, чтобы использовать традиционный способ входа.</span><span class="sxs-lookup"><span data-stu-id="b7c42-120">This can be done by sending the user an email confirmation or asking them to use their traditional login method.</span></span>


<span data-ttu-id="b7c42-121">Этот `create` метод принимает следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="b7c42-121">The `create` method takes the following parameters:</span></span>

 - **<span data-ttu-id="b7c42-122">сведения о проверяющей стороне</span><span class="sxs-lookup"><span data-stu-id="b7c42-122">relying party information</span></span>**

```javascript
    rp: {
        name: "WebAuthn Sample App",
        icon: "https://example.com/rpIcon.png"
    },
```

 - **<span data-ttu-id="b7c42-123">сведения об учетной записи пользователя</span><span class="sxs-lookup"><span data-stu-id="b7c42-123">user account information</span></span>**

```javascript
    user: {
        id: stringToArrayBuffer("some.user.id"),
        name: "bob.smith@contoso.com",
        displayName: "Bob Smith",
        icon: "https://example.com/userIcon.png"
    },
```

 - **<span data-ttu-id="b7c42-124">параметры шифрования</span><span class="sxs-lookup"><span data-stu-id="b7c42-124">crypto parameters</span></span>**

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

 - **<span data-ttu-id="b7c42-125">Параметры выделения для проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="b7c42-125">authenticator selection parameters</span></span>**

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

- **<span data-ttu-id="b7c42-126">другие варианты</span><span class="sxs-lookup"><span data-stu-id="b7c42-126">other options</span></span>**

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

<span data-ttu-id="b7c42-127">Вы можете использовать [Параметры создания учетных данных](https://w3c.github.io/webauthn/#dictdef-publickeycredentialcreationoptions) для настройки учетных данных, которые вы хотите создать.</span><span class="sxs-lookup"><span data-stu-id="b7c42-127">You can use [credential creation parameters](https://w3c.github.io/webauthn/#dictdef-publickeycredentialcreationoptions) to configure the credential you want to create.</span></span> <span data-ttu-id="b7c42-128">В частности, вы можете создать учетные данные Windows Hello, указав параметр `authenticatorAttachment` `platform` или перемещаемые учетные данные на внешнем устройстве FIDO2, указав `authenticatorAttachment` значение `cross-platform` .</span><span class="sxs-lookup"><span data-stu-id="b7c42-128">In particular, you can choose to create a Windows Hello credential by setting `authenticatorAttachment` to `platform`, or a roaming credential on an external FIDO2 device by setting `authenticatorAttachment` to `cross-platform`.</span></span> 

<span data-ttu-id="b7c42-129">При использовании этого `create` метода Microsoft Edge сначала запрашивает у пользователя проверку своего присутствия, проверяя их лицевую сторону или отпечаток, вводя ПИН-код или предпринимает действия на внешнем устройстве FIDO2.</span><span class="sxs-lookup"><span data-stu-id="b7c42-129">When you use the `create` method, Microsoft Edge will first ask the user to verify their presence by scanning their face or fingerprint, entering a PIN, or taking action on an external FIDO2 device.</span></span> <span data-ttu-id="b7c42-130">После завершения этого действия средство проверки подлинности создаст пару открытого и закрытого ключа и сохранит закрытый ключ.</span><span class="sxs-lookup"><span data-stu-id="b7c42-130">Once this step is completed the authenticator will generate a public/private key pair and store the private key.</span></span> <span data-ttu-id="b7c42-131">Эти учетные данные создаются для каждого происхождения, для каждой учетной записи и не могут быть извлечены, так как они безопасно хранятся на устройстве проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="b7c42-131">These credentials are created per origin, per account, and cannot be extracted because they are stored securely to the authentication device.</span></span> 

<span data-ttu-id="b7c42-132">Результирующее обещание возвращает [объект аттестации](https://w3c.github.io/webauthn/#sctn-attestation) , представляющий новые учетные данные.</span><span class="sxs-lookup"><span data-stu-id="b7c42-132">The resulting promise returns an [attestation object](https://w3c.github.io/webauthn/#sctn-attestation) representing the new credential.</span></span> <span data-ttu-id="b7c42-133">Объект аттестации, содержащий открытый ключ для учетных данных.</span><span class="sxs-lookup"><span data-stu-id="b7c42-133">The attestation object contains the public key for the credential.</span></span> <span data-ttu-id="b7c42-134">Вы отправите этот объект на сервер для проверки подлинности в будущем.</span><span class="sxs-lookup"><span data-stu-id="b7c42-134">You'll send this object to the server for validating future authentications.</span></span> <span data-ttu-id="b7c42-135">Прежде чем отправлять обратно на сервер, вам потребуется Base64-кодирование необработанных данных.</span><span class="sxs-lookup"><span data-stu-id="b7c42-135">Before sending back to the server, you'll need to base64-encode the raw data.</span></span>

**<span data-ttu-id="b7c42-136">Клиент</span><span class="sxs-lookup"><span data-stu-id="b7c42-136">Client</span></span>**

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

<span data-ttu-id="b7c42-137">После этого сервер должен декодировать объект аттестации, выполнить проверочные действия, извлечь открытый ключ для этих учетных данных и сохранить его для будущих проверок подлинности.</span><span class="sxs-lookup"><span data-stu-id="b7c42-137">The server should then decode the attestation object, perform verification steps, extract the public key for this credential, and store it for future authentications.</span></span> <span data-ttu-id="b7c42-138">Подробный список шагов можно найти в [алгоритме регистрации учетных данных](https://w3c.github.io/webauthn/#registering-a-new-credential) в спецификации WebAuthn.</span><span class="sxs-lookup"><span data-stu-id="b7c42-138">A detailed list of steps can be found in the [credential registration algorithm](https://w3c.github.io/webauthn/#registering-a-new-credential) in the WebAuthn specification.</span></span>

**<span data-ttu-id="b7c42-139">Сервер</span><span class="sxs-lookup"><span data-stu-id="b7c42-139">Server</span></span>**

```javascript
    attestationObject = cbor.decodeFirstSync(Buffer.from(attestation.attestationObject, 'base64'));
    authenticatorData = parseAuthenticatorData(attestationObject.authData);
    var credential = await storage.Credentials.create({
        id: authenticatorData.attestedCredentialData.credentialId.toString('base64'),
        publicKeyJwk: authenticatorData.attestedCredentialData.publicKeyJwk,
        signCount: authenticatorData.signCount
    });
```

## <span data-ttu-id="b7c42-140">Проверка подлинности пользователя</span><span class="sxs-lookup"><span data-stu-id="b7c42-140">Authenticate your user</span></span>

<span data-ttu-id="b7c42-141">После создания учетных данных на клиентском компьютере при следующем входе пользователя в систему вы можете подписаться на него с помощью своих учетных данных для проверки подлинности, а не пароля, вызываемого из звонка в Navigator. Credentials. **получить**.</span><span class="sxs-lookup"><span data-stu-id="b7c42-141">Once the credential is created on the client, the next time the user attempts to log into the site you can offer to sign them in using their Web Authentication credential instead of a password with a call to navigator.credentials.**get**.</span></span>

<span data-ttu-id="b7c42-142">Этот `get` метод принимает этот *запрос* в качестве единственного нужного параметра.</span><span class="sxs-lookup"><span data-stu-id="b7c42-142">The `get` method takes the *challenge* as its only required parameter.</span></span> <span data-ttu-id="b7c42-143">Задача является непрозрачной последовательностью байтов, которую сервер отправляет клиенту для подписывания с помощью закрытого ключа пользователя.</span><span class="sxs-lookup"><span data-stu-id="b7c42-143">The challenge is an opaque sequence of bytes that the server will send down to a client to sign with the user's private key.</span></span> <span data-ttu-id="b7c42-144">Пример</span><span class="sxs-lookup"><span data-stu-id="b7c42-144">For example:</span></span>

**<span data-ttu-id="b7c42-145">Сервер</span><span class="sxs-lookup"><span data-stu-id="b7c42-145">Server</span></span>**

```javascript
    var jwt = require('jsonwebtoken');
    var jwt_secret = "defaultsecret";
    fido.getChallenge = () => {
        return jwt.sign({}, jwt_secret, {
            expiresIn: 120 * 1000
        });
    };
```

<span data-ttu-id="b7c42-146">После получения запроса от сервера вы будете вызывать API Get вместе с [параметрами запроса учетных данных](https://w3c.github.io/webauthn/#credentialrequestoptions-extension).</span><span class="sxs-lookup"><span data-stu-id="b7c42-146">After retrieving a challenge from the server, you'll call the get API along with [credential request options](https://w3c.github.io/webauthn/#credentialrequestoptions-extension).</span></span> <span data-ttu-id="b7c42-147">Microsoft Edge отобразит сообщение о том, что пользователь использует Windows Hello или внешнее устройство FIDO2 для проверки подлинности пользователя.</span><span class="sxs-lookup"><span data-stu-id="b7c42-147">Microsoft Edge will show a prompt, which will verify the identity of the user using Windows Hello or an external FIDO2 device.</span></span> <span data-ttu-id="b7c42-148">После проверки пользователя проблема будет подписана в доверенном платформенном модуле или устройстве FIDO2, и обещание вернется с помощью [объекта утверждения](https://w3c.github.io/webauthn/#authenticatorassertionresponse) , содержащего подпись и другие метаданные, которые нужно отправить на сервер.</span><span class="sxs-lookup"><span data-stu-id="b7c42-148">After the user is verified, the challenge will be signed within the TPM or FIDO2 device and the promise will return with an [assertion object](https://w3c.github.io/webauthn/#authenticatorassertionresponse) that contains the signature and other metadata for you to send to the server.</span></span>

**<span data-ttu-id="b7c42-149">Клиент</span><span class="sxs-lookup"><span data-stu-id="b7c42-149">Client</span></span>**

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

<span data-ttu-id="b7c42-150">После получения утверждения на сервере вам потребуется проверить подпись для проверки подлинности пользователя.</span><span class="sxs-lookup"><span data-stu-id="b7c42-150">Once you receive the assertion on the server, you will need to validate the signature to authenticate the user.</span></span> <span data-ttu-id="b7c42-151">Ниже приведен пример кода.</span><span class="sxs-lookup"><span data-stu-id="b7c42-151">The following is some sample code.</span></span>  <span data-ttu-id="b7c42-152">Подробный список шагов можно найти в [алгоритме проверки утверждения](https://w3c.github.io/webauthn/#verifying-assertion) в спецификации WebAuthn.</span><span class="sxs-lookup"><span data-stu-id="b7c42-152">A detailed list of steps can be found in the [assertion verification algorithm](https://w3c.github.io/webauthn/#verifying-assertion) in the WebAuthn specification.</span></span>

**<span data-ttu-id="b7c42-153">Сервер</span><span class="sxs-lookup"><span data-stu-id="b7c42-153">Server</span></span>**

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

## <span data-ttu-id="b7c42-154">Заметки о внедрении</span><span class="sxs-lookup"><span data-stu-id="b7c42-154">Implementation notes</span></span>

### <span data-ttu-id="b7c42-155">Поддерживаемые платформы</span><span class="sxs-lookup"><span data-stu-id="b7c42-155">Supported platforms</span></span>
- <span data-ttu-id="b7c42-156">В Microsoft EDGE, начиная с EdgeHTML 18 (предварительной версии 17713 и более поздней версии), можно использовать ознакомительную версию рекомендаций API для проверки подлинности веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="b7c42-156">The Candidate Recommendation version of the Web Authentication API can be used from Microsoft Edge beginning with EdgeHTML 18 (Windows Insider Preview version 17713 and up).</span></span>
- <span data-ttu-id="b7c42-157">[Предварительно исправленная версия](https://blogs.windows.com/msedgedev/2016/04/12/a-world-without-passwords-windows-hello-in-microsoft-edge/) API для проверки подлинности веб-сайта удалена и больше не доступна.</span><span class="sxs-lookup"><span data-stu-id="b7c42-157">The [prefixed, preview version](https://blogs.windows.com/msedgedev/2016/04/12/a-world-without-passwords-windows-hello-in-microsoft-edge/) of the Web Authentication API has been removed and is no longer available.</span></span>
- <span data-ttu-id="b7c42-158">API для веб-аутентификации пока не доступен для приложений UWP и PWAs.</span><span class="sxs-lookup"><span data-stu-id="b7c42-158">The Web Authentication API is not yet available to UWP apps and PWAs.</span></span>
- <span data-ttu-id="b7c42-159">Internet Explorer не поддерживает API проверки подлинности веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="b7c42-159">Internet Explorer does not support the Web Authentication API.</span></span> 

### <span data-ttu-id="b7c42-160">Поддерживаемые средства проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="b7c42-160">Supported authenticators</span></span>
<span data-ttu-id="b7c42-161">С помощью API проверки подлинности в Microsoft EDGE можно проверять подлинность пользователей с помощью следующих технологий:</span><span class="sxs-lookup"><span data-stu-id="b7c42-161">With the Web Authentication API in Microsoft Edge, you can authenticate users with the following technologies:</span></span>
- <span data-ttu-id="b7c42-162">**Windows Hello**, включение проверки подлинности на устройстве без пароля с использованием лицом, отпечатка пальца или PIN-кода</span><span class="sxs-lookup"><span data-stu-id="b7c42-162">**Windows Hello**, enabling passwordless on-device authentication with  face, fingerprint, or PIN</span></span>
- <span data-ttu-id="b7c42-163">**FIDO2**, включение проверки подлинности без пароля на съемном устройстве, а также отпечаток пальца или PIN-кода</span><span class="sxs-lookup"><span data-stu-id="b7c42-163">**FIDO2**, enabling passwordless roaming authentication with a removable device and a fingerprint or PIN</span></span>
- <span data-ttu-id="b7c42-164">**U2F**, включение надежной второй проверки подлинности для веб-сайтов, не готовых к переходу на модель без пароля</span><span class="sxs-lookup"><span data-stu-id="b7c42-164">**U2F**, enabling strong second factor authentication for websites that are not ready to move to a passwordless model</span></span>

### <span data-ttu-id="b7c42-165">Специальные аспекты, касающиеся Windows Hello</span><span class="sxs-lookup"><span data-stu-id="b7c42-165">Special considerations for Windows Hello</span></span> 
<span data-ttu-id="b7c42-166">Некоторые моменты, которые необходимо учитывать при использовании средства проверки подлинности Windows Hello:</span><span class="sxs-lookup"><span data-stu-id="b7c42-166">A few things to note when using the Windows Hello authenticator:</span></span>
- <span data-ttu-id="b7c42-167">Вы можете определить, доступен ли Windows Hello на компьютере, вызвав `isUserVerifyingPlatformAuthenticatorAvailable` API.</span><span class="sxs-lookup"><span data-stu-id="b7c42-167">You can detect if Windows Hello is available on a PC by calling the `isUserVerifyingPlatformAuthenticatorAvailable` API.</span></span> <span data-ttu-id="b7c42-168">Дополнительные сведения об [этом API.](https://www.w3.org/TR/webauthn/#isUserVerifyingPlatformAuthenticatorAvailable)</span><span class="sxs-lookup"><span data-stu-id="b7c42-168">Learn more about this API [here](https://www.w3.org/TR/webauthn/#isUserVerifyingPlatformAuthenticatorAvailable).</span></span>
- <span data-ttu-id="b7c42-169">Если вы создаете учетные данные для Windows Hello, вы должны использовать `authenticatorAttachment` `platform` для наилучшего взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="b7c42-169">When creating a credential for Windows Hello, you should set `authenticatorAttachment` to `platform` for the best user experience.</span></span>
- <span data-ttu-id="b7c42-170">Windows Hello поддерживает только RS256 (ALG-257) в качестве алгоритма открытого ключа.</span><span class="sxs-lookup"><span data-stu-id="b7c42-170">Windows Hello only supports RS256 (alg -257) as its public key algorithm.</span></span> <span data-ttu-id="b7c42-171">Не забудьте указать этот алгоритм при создании учетных данных.</span><span class="sxs-lookup"><span data-stu-id="b7c42-171">Be sure to specify this algorithm when creating a credential.</span></span>
- <span data-ttu-id="b7c42-172">Чтобы получить [инструкцию аттестации TPM](https://w3c.github.io/webauthn/#tpm-attestation), установите для аттестации значение Direct при вызове `create` API.</span><span class="sxs-lookup"><span data-stu-id="b7c42-172">To receive a [TPM attestation statement](https://w3c.github.io/webauthn/#tpm-attestation), set attestation to "direct" when calling the `create` API.</span></span> <span data-ttu-id="b7c42-173">Аттестация доверенного платформенного модуля является наилучшим усилием.</span><span class="sxs-lookup"><span data-stu-id="b7c42-173">TPM attestation is a best effort.</span></span> <span data-ttu-id="b7c42-174">Только компьютеры с доверенным платформенным модулем 2,0 возвращают инструкцию аттестации TPM, и процесс аттестации может завершиться сбоем по различным причинам.</span><span class="sxs-lookup"><span data-stu-id="b7c42-174">Only PCs with TPM 2.0 will return a TPM attestation statement, and the attestation process could fail for a variety of reasons.</span></span>
- <span data-ttu-id="b7c42-175">В Windows Hello есть различные способы защиты учетных данных пользователя.</span><span class="sxs-lookup"><span data-stu-id="b7c42-175">Windows Hello employs a variety of ways to protect user credentials.</span></span> <span data-ttu-id="b7c42-176">Вы можете проверить, какой метод был использован для защиты учетных данных, заменив поле [AAGUID](https://w3c.github.io/webauthn/#sec-attested-credential-data) в объекте аттестации, возвращаемом при создании учетных данных.</span><span class="sxs-lookup"><span data-stu-id="b7c42-176">You can check which method has been used to protect a credential by consuming the [AAGUID](https://w3c.github.io/webauthn/#sec-attested-credential-data) field in the attestation object returned at credential creation.</span></span> <span data-ttu-id="b7c42-177">Ниже приведен список AAGUIDs, которые может возвращать Windows Hello.</span><span class="sxs-lookup"><span data-stu-id="b7c42-177">The following is the list of AAGUIDs that Windows Hello may return:</span></span> 
  - <span data-ttu-id="b7c42-178">Программное обеспечение для проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="b7c42-178">Software backed authenticators</span></span>
    - <span data-ttu-id="b7c42-179">Средство проверки подлинности программного обеспечения Windows Hello:</span><span class="sxs-lookup"><span data-stu-id="b7c42-179">Windows Hello software authenticator:</span></span> `6028B017-B1D4-4C02-B4B3-AFCDAFC96BB2`
    - <span data-ttu-id="b7c42-180">Программа проверки подлинности Windows Hello VBS:</span><span class="sxs-lookup"><span data-stu-id="b7c42-180">Windows Hello VBS software authenticator:</span></span> `6E96969E-A5CF-4AAD-9B56-305FE6C82795`
  - <span data-ttu-id="b7c42-181">Резервные средства проверки подлинности доверенного платформенного модуля (TPM)</span><span class="sxs-lookup"><span data-stu-id="b7c42-181">Trusted Platform Module (TPM) backed authenticators</span></span>
    - <span data-ttu-id="b7c42-182">Средство проверки подлинности оборудования для Windows Hello:</span><span class="sxs-lookup"><span data-stu-id="b7c42-182">Windows Hello hardware authenticator:</span></span> `08987058-CADC-4B81-B6E1-30DE50DCBE96`
    - <span data-ttu-id="b7c42-183">Средство проверки подлинности оборудования для Windows Hello VBS:</span><span class="sxs-lookup"><span data-stu-id="b7c42-183">Windows Hello VBS hardware authenticator:</span></span> `9DDD1817-AF5A-4672-A2B9-3E3DD95000A9`


### <span data-ttu-id="b7c42-184">Поверхность API</span><span class="sxs-lookup"><span data-stu-id="b7c42-184">API surface</span></span>
- <span data-ttu-id="b7c42-185">Microsoft Edge имеет полную реализацию версии рекомендации кандидата спецификации основной веб-проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="b7c42-185">Microsoft Edge has a complete implementation of the Candidate Recommendation version of the core Web Authentication specification.</span></span>
- <span data-ttu-id="b7c42-186">[Расширение AppID](https://w3c.github.io/webauthn/#sctn-appid-extension) поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b7c42-186">The [AppID extension](https://w3c.github.io/webauthn/#sctn-appid-extension) is supported.</span></span> 
- <span data-ttu-id="b7c42-187">Другие расширения не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="b7c42-187">No other extensions are supported.</span></span>


## <span data-ttu-id="b7c42-188">Демонстрационные примеры</span><span class="sxs-lookup"><span data-stu-id="b7c42-188">Demos</span></span>

[<span data-ttu-id="b7c42-189">Пример кода клиента и сервера</span><span class="sxs-lookup"><span data-stu-id="b7c42-189">Client and server code sample</span></span>](https://github.com/MicrosoftEdge/webauthnsample)

[<span data-ttu-id="b7c42-190">Демонстрация пробного диска Windows Hello</span><span class="sxs-lookup"><span data-stu-id="b7c42-190">Windows Hello Test Drive demo</span></span>](https://webauthnsample.azurewebsites.net/)

## <span data-ttu-id="b7c42-191">Specification</span><span class="sxs-lookup"><span data-stu-id="b7c42-191">Specification</span></span>

[<span data-ttu-id="b7c42-192">Веб-проверка подлинности: API для доступа к учетным данным открытого ключа</span><span class="sxs-lookup"><span data-stu-id="b7c42-192">Web Authentication: An API for accessing Public Key Credentials</span></span>](http://w3c.github.io/webauthn/)
