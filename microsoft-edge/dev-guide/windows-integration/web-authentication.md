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
# <span data-ttu-id="640b9-104">Веб-аутентификация и Windows Hello</span><span class="sxs-lookup"><span data-stu-id="640b9-104">Web Authentication and Windows Hello</span></span>  

[!INCLUDE [deprecation-note](../../includes/legacy-edge-note.md)]  

<span data-ttu-id="640b9-105">[API](https://w3c.github.io/webauthn) веб-аутентификации в Microsoft Edge позволяет веб-приложениям использовать для проверки подлинности [Windows Hello](https://www.microsoft.com/windows/comprehensive-security) [и внешние устройства FIDO2](https://fidoalliance.org/fido2) для проверки подлинности пользователей, чтобы пользователи и пользователи не смог избежать рисков управления паролями, включая предоставление рекомендаций о защите паролей, фишинга и ключевых атак.</span><span class="sxs-lookup"><span data-stu-id="640b9-105">The [Web Authentication API](https://w3c.github.io/webauthn) in Microsoft Edge enables web applications to use [Windows Hello](https://www.microsoft.com/windows/comprehensive-security) and [external FIDO2 devices](https://fidoalliance.org/fido2) for user authentication so that you and your users can avoid all the hassles and risks of password management, including password guessing, phishing, and key-logging attacks.</span></span>  <span data-ttu-id="640b9-106">Текущая рекомендация Microsoft Edge основана на рекомендации по спецификации веб-проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="640b9-106">The current Microsoft Edge implementation is based on the Candidate Recommendation of the Web Authentication specification.</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="640b9-107">Из этой статьи вы узнаете, как пробовать проверку подлинности Windows Hello и FIDO2 в Microsoft Edge.</span><span class="sxs-lookup"><span data-stu-id="640b9-107">This topic will show you how to try out Windows Hello and FIDO2 authentication with Microsoft Edge.</span></span>  

<span data-ttu-id="640b9-108">При использовании веб-проверки сервер отправляет запросы в браузере в обычном тексте.</span><span class="sxs-lookup"><span data-stu-id="640b9-108">Using Web Authentication, the server sends down a plain text challenge to the browser.</span></span>  <span data-ttu-id="640b9-109">После того как Microsoft Edge сможет проверить пользователя с помощью Windows Hello или внешнего устройства FIDO2, система подписывает проблему с частным ключом, который ранее подготовлен для этого пользователя и отправит на сервер подпись.</span><span class="sxs-lookup"><span data-stu-id="640b9-109">Once Microsoft Edge is able to verify the user through Windows Hello or an external FIDO2 device, the system will sign the challenge with a private key previously provisioned for this user and send the signature back to the server.</span></span>  <span data-ttu-id="640b9-110">Если сервер может проверить подпись с помощью общедоступного ключа, имеющего этот пользователь, и проверить правильность проблемы, проверка подлинности пользователя может оказаться надежной.</span><span class="sxs-lookup"><span data-stu-id="640b9-110">If the server can validate the signature using the public key it has for that user and verify the challenge is correct, it can authenticate the user securely.</span></span>  <span data-ttu-id="640b9-111">[Благодаря](https://en.wikipedia.org/wiki/Public-key_cryptography) асимметричной широкостью общедоступный ключ означает, что общедоступный ключ самостоятельно имеет вид и личный ключ никогда не предоставляется.</span><span class="sxs-lookup"><span data-stu-id="640b9-111">With [asymmetric cryptography](https://en.wikipedia.org/wiki/Public-key_cryptography) such as this, the public key is meaningless on its own and the private key is never shared.</span></span>  <span data-ttu-id="640b9-112">Более того, закрытый ключ никогда нельзя перемещать из безопасных элементов или современных систем с аппаратным и современным ими дисплеями по протоколу TPM.</span><span class="sxs-lookup"><span data-stu-id="640b9-112">Furthermore, the private key can never be moved from secure elements or modern systems with TPM-enabled hardware.</span></span>  

<span data-ttu-id="640b9-113">Существует два основных шага, которые нужно выполнить с помощью API веб-проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="640b9-113">There are two basic steps to using the Web Authentication API:</span></span>  

1.  <span data-ttu-id="640b9-114">Регистрация пользователя</span><span class="sxs-lookup"><span data-stu-id="640b9-114">Register your user with</span></span> `create`  
1.  <span data-ttu-id="640b9-115">Проверка подлинности пользователя</span><span class="sxs-lookup"><span data-stu-id="640b9-115">Authenticate your user with</span></span> `get`  

<span data-ttu-id="640b9-116">В приведенном ниже руководстве поможет вам выполнить этот поток [с помощью приложения WebAuthn Sample.](https://github.com/MicrosoftEdge/webauthnsample)</span><span class="sxs-lookup"><span data-stu-id="640b9-116">The following dev guide will walk you through this flow using the [WebAuthn Sample App](https://github.com/MicrosoftEdge/webauthnsample).</span></span>  

## <span data-ttu-id="640b9-117">Регистрация пользователя</span><span class="sxs-lookup"><span data-stu-id="640b9-117">Register your user</span></span>  

<span data-ttu-id="640b9-118">Для пользователей с методом удостоверения сначала потребуется создать для пользователя учетные данные для `navigator.credentials.create` веб-аутентификации.</span><span class="sxs-lookup"><span data-stu-id="640b9-118">Acting as an identity provider, you will first need to create a Web Authentication credential for your user with the `navigator.credentials.create` method.</span></span>  <span data-ttu-id="640b9-119">Перед регистрацией учетных данных для пользователя на сервере необходимо подтвердить личность пользователя.</span><span class="sxs-lookup"><span data-stu-id="640b9-119">Before you register that credential to the user on your server, you will need to confirm the identity of the user.</span></span>  <span data-ttu-id="640b9-120">Для этого можно отправить пользователю электронное письмо с подтверждением или попросить его использовать традиционный способ входа.</span><span class="sxs-lookup"><span data-stu-id="640b9-120">This can be done by sending the user an email confirmation or asking them to use their traditional login method.</span></span>  

<span data-ttu-id="640b9-121">При `create` выборе метода имеются следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="640b9-121">The `create` method takes the following parameters:</span></span>  

:::row:::
   :::column span="1":::
      **<span data-ttu-id="640b9-122">отражение сведений о вечеринке</span><span class="sxs-lookup"><span data-stu-id="640b9-122">relying party information</span></span>**  
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
      **<span data-ttu-id="640b9-123">сведения об учетной записи пользователя</span><span class="sxs-lookup"><span data-stu-id="640b9-123">user account information</span></span>**  
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
      **<span data-ttu-id="640b9-124">параметры велосипедов</span><span class="sxs-lookup"><span data-stu-id="640b9-124">crypto parameters</span></span>**  
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
      **<span data-ttu-id="640b9-125">параметры проверки подлинности</span><span class="sxs-lookup"><span data-stu-id="640b9-125">authenticator selection parameters</span></span>**  
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
      **<span data-ttu-id="640b9-126">другие параметры</span><span class="sxs-lookup"><span data-stu-id="640b9-126">other options</span></span>**  
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

<span data-ttu-id="640b9-127">Для настройки [учетных](https://w3c.github.io/webauthn#dictdef-publickeycredentialcreationoptions) данных можно использовать параметры создания учетных данных.</span><span class="sxs-lookup"><span data-stu-id="640b9-127">You can use [credential creation parameters](https://w3c.github.io/webauthn#dictdef-publickeycredentialcreationoptions) to configure the credential you want to create.</span></span>  <span data-ttu-id="640b9-128">В частли, вы можете создать учетные данные Windows Hello, установив для этого параметр или учетные данные `authenticatorAttachment` `platform` роуминга на внешнем устройстве FIDO2, установив `authenticatorAttachment` `cross-platform` параметр.</span><span class="sxs-lookup"><span data-stu-id="640b9-128">In particular, you can choose to create a Windows Hello credential by setting `authenticatorAttachment` to `platform`, or a roaming credential on an external FIDO2 device by setting `authenticatorAttachment` to `cross-platform`.</span></span>  

<span data-ttu-id="640b9-129">При использовании метода Microsoft Edge сначала просит пользователя подтвердить свой принтер, сканируя свое состояние лица или `create` отпечатка пальца, вводить ПИН-код или выполнить действия на внешнем устройстве FIDO2.</span><span class="sxs-lookup"><span data-stu-id="640b9-129">When you use the `create` method, Microsoft Edge will first ask the user to verify their presence by scanning their face or fingerprint, entering a PIN, or taking action on an external FIDO2 device.</span></span>  <span data-ttu-id="640b9-130">После завершения этого действия проверка подлинности создаст открытую пару и сохранит частный ключ.</span><span class="sxs-lookup"><span data-stu-id="640b9-130">Once this step is completed the authenticator will generate a publicprivate key pair and store the private key.</span></span>  <span data-ttu-id="640b9-131">Эти учетные данные создаются для каждого происхождения, каждой учетной записи и их немогут быть извлечены, так как безопасно храниться на устройстве проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="640b9-131">These credentials are created per origin, per account, and cannot be extracted because they are stored securely to the authentication device.</span></span>  

<span data-ttu-id="640b9-132">Исходящий объект вернет объект [популярности,](https://w3c.github.io/webauthn#sctn-attestation) представляющий новые учетные данные.</span><span class="sxs-lookup"><span data-stu-id="640b9-132">The resulting promise returns an [attestation object](https://w3c.github.io/webauthn#sctn-attestation) representing the new credential.</span></span>  <span data-ttu-id="640b9-133">Объект попытки содержит открытый ключ учетных данных.</span><span class="sxs-lookup"><span data-stu-id="640b9-133">The attestation object contains the public key for the credential.</span></span>  <span data-ttu-id="640b9-134">Этот объект отправляется на сервер для проверки будущей проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="640b9-134">You'll send this object to the server for validating future authentications.</span></span>  <span data-ttu-id="640b9-135">Прежде чем отправлять сервер на сервер, необходимо основание 64-разрядной кодировки неработающих данных.</span><span class="sxs-lookup"><span data-stu-id="640b9-135">Before sending back to the server, you'll need to base64-encode the raw data.</span></span>  

**<span data-ttu-id="640b9-136">Клиент</span><span class="sxs-lookup"><span data-stu-id="640b9-136">Client</span></span>**  

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

<span data-ttu-id="640b9-137">Затем сервер должен отнять объект попытки, выполнить процедуру проверки, извлечь извлеченный общедоступный ключ для этого учетных данных и сохранить его для дальнейшей проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="640b9-137">The server should then decode the attestation object, perform verification steps, extract the public key for this credential, and store it for future authentications.</span></span>  <span data-ttu-id="640b9-138">Подробный список шагов можно найти в [алгоритме](https://w3c.github.io/webauthn#registering-a-new-credential) спецификации WebAuthn.</span><span class="sxs-lookup"><span data-stu-id="640b9-138">A detailed list of steps can be found in the [credential registration algorithm](https://w3c.github.io/webauthn#registering-a-new-credential) in the WebAuthn specification.</span></span>  

**<span data-ttu-id="640b9-139">Сервер</span><span class="sxs-lookup"><span data-stu-id="640b9-139">Server</span></span>**  

```javascript
    attestationObject = cbor.decodeFirstSync(Buffer.from(attestation.attestationObject, 'base64'));
    authenticatorData = parseAuthenticatorData(attestationObject.authData);
    var credential = await storage.Credentials.create({
        id: authenticatorData.attestedCredentialData.credentialId.toString('base64'),
        publicKeyJwk: authenticatorData.attestedCredentialData.publicKeyJwk,
        signCount: authenticatorData.signCount
    });
```  

## <span data-ttu-id="640b9-140">Проверка подлинности пользователя</span><span class="sxs-lookup"><span data-stu-id="640b9-140">Authenticate your user</span></span>  

<span data-ttu-id="640b9-141">После того как пользователь появится в клиенте, при следующей попытке войти на сайт вы сможете войти на сайт, используя учетные данные для веб-проверки подлинности вместо того, чтобы убедиться `navigator.credentials.get` в этом.</span><span class="sxs-lookup"><span data-stu-id="640b9-141">Once the credential is created on the client, the next time the user attempts to log into the site you can offer to sign them in using their Web Authentication credential instead of a password with a call to `navigator.credentials.get`.</span></span>  

<span data-ttu-id="640b9-142">Способ принимает задание только в качестве обязательных `get` параметров.</span><span class="sxs-lookup"><span data-stu-id="640b9-142">The `get` method takes the challenge as its only required parameter.</span></span>  <span data-ttu-id="640b9-143">Проблема — это непрозрачная последовательность байтов, которые сервер отправляет клиенту клиенту для входа в свой клиент для регистрации с частным ключом пользователя.</span><span class="sxs-lookup"><span data-stu-id="640b9-143">The challenge is an opaque sequence of bytes that the server will send down to a client to sign with the user's private key.</span></span>  <span data-ttu-id="640b9-144">Например:</span><span class="sxs-lookup"><span data-stu-id="640b9-144">For example:</span></span>  

**<span data-ttu-id="640b9-145">Сервер</span><span class="sxs-lookup"><span data-stu-id="640b9-145">Server</span></span>**  

```javascript
    var jwt = require('jsonwebtoken');
    var jwt_secret = "defaultsecret";
    fido.getChallenge = () => {
        return jwt.sign({}, jwt_secret, {
            expiresIn: 120 * 1000
        });
    };
```  

<span data-ttu-id="640b9-146">После получения проблемы с сервера вы звоните по API получения API и варианты ответа с [учетными данными.](https://w3c.github.io/webauthn#credentialrequestoptions-extension)</span><span class="sxs-lookup"><span data-stu-id="640b9-146">After retrieving a challenge from the server, you'll call the get API along with [credential request options](https://w3c.github.io/webauthn#credentialrequestoptions-extension).</span></span>  <span data-ttu-id="640b9-147">Microsoft Edge отобразит запрос, в котором подтверждение личности пользователя с помощью Windows Hello или внешнего устройства FIDO2 будет выведено.</span><span class="sxs-lookup"><span data-stu-id="640b9-147">Microsoft Edge will show a prompt, which will verify the identity of the user using Windows Hello or an external FIDO2 device.</span></span>  <span data-ttu-id="640b9-148">После проверки проблема будет вошедшена в устройство TPM или FIDO2, и оборудование вернет с [объектом вложения](https://w3c.github.io/webauthn#authenticatorassertionresponse) и другими метаданными, которые вы хотите отправить на сервер.</span><span class="sxs-lookup"><span data-stu-id="640b9-148">After the user is verified, the challenge will be signed within the TPM or FIDO2 device and the promise will return with an [assertion object](https://w3c.github.io/webauthn#authenticatorassertionresponse) that contains the signature and other metadata for you to send to the server.</span></span>  

**<span data-ttu-id="640b9-149">Клиент</span><span class="sxs-lookup"><span data-stu-id="640b9-149">Client</span></span>**  

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

<span data-ttu-id="640b9-150">Получив такое средство на сервере, необходимо проверить подпись для проверки подлинности пользователя.</span><span class="sxs-lookup"><span data-stu-id="640b9-150">Once you receive the assertion on the server, you will need to validate the signature to authenticate the user.</span></span>  <span data-ttu-id="640b9-151">Ниже приведен пример кода.</span><span class="sxs-lookup"><span data-stu-id="640b9-151">The following is some sample code.</span></span>  <span data-ttu-id="640b9-152">Подробный список действий можно найти [assertion verification algorithm](https://w3c.github.io/webauthn#verifying-assertion) в алгоритме проверки вспомогательной проверки в спецификации WebAuth.</span><span class="sxs-lookup"><span data-stu-id="640b9-152">A detailed list of steps can be found in the [assertion verification algorithm](https://w3c.github.io/webauthn#verifying-assertion) in the WebAuthn specification.</span></span>  

**<span data-ttu-id="640b9-153">Сервер</span><span class="sxs-lookup"><span data-stu-id="640b9-153">Server</span></span>**  

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

## <span data-ttu-id="640b9-154">Примечания к внедрению</span><span class="sxs-lookup"><span data-stu-id="640b9-154">Implementation notes</span></span>  

### <span data-ttu-id="640b9-155">Поддерживаемые платформы</span><span class="sxs-lookup"><span data-stu-id="640b9-155">Supported platforms</span></span>  

*   <span data-ttu-id="640b9-156">Рекомендации по использованию API веб-проверки подлинности можно использовать из Microsoft Edge начиная с EdgeHTML 18 \(Windows Insider Preview версии 17713 или более поздней версии).)</span><span class="sxs-lookup"><span data-stu-id="640b9-156">The Candidate Recommendation version of the Web Authentication API can be used from Microsoft Edge beginning with EdgeHTML 18 \(Windows Insider Preview version 17713 or newer\).</span></span>  
*   <span data-ttu-id="640b9-157">Предварительная [версия](https://blogs.windows.com/msedgedev/2016/04/12) API веб-проверки подлинности удалена и теперь недоступна.</span><span class="sxs-lookup"><span data-stu-id="640b9-157">The [prefixed, preview version](https://blogs.windows.com/msedgedev/2016/04/12) of the Web Authentication API has been removed and is no longer available.</span></span>  
*   <span data-ttu-id="640b9-158">API веб-проверки еще недоступен для приложений UWP и PWAs.</span><span class="sxs-lookup"><span data-stu-id="640b9-158">The Web Authentication API is not yet available to UWP apps and PWAs.</span></span>  
*   <span data-ttu-id="640b9-159">Internet Explorer не поддерживает API веб-проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="640b9-159">Internet Explorer does not support the Web Authentication API.</span></span>  

### <span data-ttu-id="640b9-160">Поддерживаемая проверка подлинности</span><span class="sxs-lookup"><span data-stu-id="640b9-160">Supported authenticators</span></span>  

<span data-ttu-id="640b9-161">С помощью API веб-проверки подлинности в Microsoft Edge можно пройти проверку подлинности пользователей со следующими технологиями:</span><span class="sxs-lookup"><span data-stu-id="640b9-161">With the Web Authentication API in Microsoft Edge, you can authenticate users with the following technologies:</span></span>  

*   <span data-ttu-id="640b9-162">**Windows Hello**  Включение проверки подлинности пароля на устройстве с помощью лица, отпечатка отпечатка пальца или ПИН-адреса.</span><span class="sxs-lookup"><span data-stu-id="640b9-162">**Windows Hello**  Enables passwordless on-device authentication with  face, fingerprint, or PIN</span></span>  
*   <span data-ttu-id="640b9-163">**FIDO2**  Включает перемещаемую проверку подлинности с помощью старого устройства и пин-кода или ПИН-кода.</span><span class="sxs-lookup"><span data-stu-id="640b9-163">**FIDO2**  Enables passwordless roaming authentication with a removable device and a fingerprint or PIN</span></span>  
*   <span data-ttu-id="640b9-164">**U2F**  Включает надежную вторую проверку подлинности для веб-сайтов, которые не готовы перейти к модели пароля.</span><span class="sxs-lookup"><span data-stu-id="640b9-164">**U2F**  Enables strong second factor authentication for websites that are not ready to move to a passwordless model</span></span>  

### <span data-ttu-id="640b9-165">Особенности Windows Hello</span><span class="sxs-lookup"><span data-stu-id="640b9-165">Special considerations for Windows Hello</span></span>  

<span data-ttu-id="640b9-166">При использовании проверки подлинности Windows Hello нужно заметить следующее:</span><span class="sxs-lookup"><span data-stu-id="640b9-166">A few things to note when using the Windows Hello authenticator:</span></span>  

*   <span data-ttu-id="640b9-167">Чтобы выяснить, доступна ли Windows Hello, позвонив `isUserVerifyingPlatformAuthenticatorAvailable` API.</span><span class="sxs-lookup"><span data-stu-id="640b9-167">You can detect if Windows Hello is available on a PC by calling the `isUserVerifyingPlatformAuthenticatorAvailable` API.</span></span>  <span data-ttu-id="640b9-168">Подробнее об этом API [здесь.](https://www.w3.org/TR/webauthn#isUserVerifyingPlatformAuthenticatorAvailable)</span><span class="sxs-lookup"><span data-stu-id="640b9-168">Learn more about this API [here](https://www.w3.org/TR/webauthn#isUserVerifyingPlatformAuthenticatorAvailable).</span></span>  
*   <span data-ttu-id="640b9-169">При создании учетных данных для Windows Hello следует задать для `authenticatorAttachment` оптимального `platform` взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="640b9-169">When creating a credential for Windows Hello, you should set `authenticatorAttachment` to `platform` for the best user experience.</span></span>
*   <span data-ttu-id="640b9-170">Windows Hello поддерживает только rS256 \(alg -257\) в качестве общедоступного ключа.</span><span class="sxs-lookup"><span data-stu-id="640b9-170">Windows Hello only supports RS256 \(alg -257\) as its public key algorithm.</span></span>  <span data-ttu-id="640b9-171">Не забудьте указать этот алгоритм при создании учетных данных.</span><span class="sxs-lookup"><span data-stu-id="640b9-171">Be sure to specify this algorithm when creating a credential.</span></span>  
*   <span data-ttu-id="640b9-172">Чтобы получить [оператор по птации попытки TPM,](https://w3c.github.io/webauthn#tpm-attestation)присвойте попытку аудитории на прямую `create` попытку.</span><span class="sxs-lookup"><span data-stu-id="640b9-172">To receive a [TPM attestation statement](https://w3c.github.io/webauthn#tpm-attestation), set attestation to "direct" when calling the `create` API.</span></span>  <span data-ttu-id="640b9-173">Попытка TPM — лучше.</span><span class="sxs-lookup"><span data-stu-id="640b9-173">TPM attestation is a best effort.</span></span>  <span data-ttu-id="640b9-174">Это может быть только для пограничных причин.</span><span class="sxs-lookup"><span data-stu-id="640b9-174">Only PCs with TPM 2.0 will return a TPM attestation statement, and the attestation process could fail for a variety of reasons.</span></span>  
*   <span data-ttu-id="640b9-175">Windows Hello предусматривают различные способы защиты учетных данных пользователя.</span><span class="sxs-lookup"><span data-stu-id="640b9-175">Windows Hello employs a variety of ways to protect user credentials.</span></span>  <span data-ttu-id="640b9-176">Чтобы проверить, какой метод использовался для защиты учетных данных, можно зарезервировать поле [AAGUID](https://w3c.github.io/webauthn#sec-attested-credential-data) объекта атестации, возвращенного при создании учетных данных.</span><span class="sxs-lookup"><span data-stu-id="640b9-176">You can check which method has been used to protect a credential by consuming the [AAGUID](https://w3c.github.io/webauthn#sec-attested-credential-data) field in the attestation object returned at credential creation.</span></span>  <span data-ttu-id="640b9-177">Вот список агрегатных функций Windows Hello:</span><span class="sxs-lookup"><span data-stu-id="640b9-177">The following is the list of AAGUIDs that Windows Hello may return:</span></span>   
    *   <span data-ttu-id="640b9-178">Программное обеспечение обратно проверке подлинности</span><span class="sxs-lookup"><span data-stu-id="640b9-178">Software backed authenticators</span></span>  
        *   <span data-ttu-id="640b9-179">Проверка подлинности программного обеспечения Windows Hello:</span><span class="sxs-lookup"><span data-stu-id="640b9-179">Windows Hello software authenticator:</span></span>  `6028B017-B1D4-4C02-B4B3-AFCDAFC96BB2`  
        *   <span data-ttu-id="640b9-180">Проверка подлинности программного обеспечения Windows Hello VBS:</span><span class="sxs-lookup"><span data-stu-id="640b9-180">Windows Hello VBS software authenticator:</span></span>  `6E96969E-A5CF-4AAD-9B56-305FE6C82795`  
    *   <span data-ttu-id="640b9-181">Надежная платформа \(TPM\) обратно</span><span class="sxs-lookup"><span data-stu-id="640b9-181">Trusted Platform Module \(TPM\) backed authenticators</span></span>  
        *   <span data-ttu-id="640b9-182">Аппаратная проверка подлинности Windows Hello:</span><span class="sxs-lookup"><span data-stu-id="640b9-182">Windows Hello hardware authenticator:</span></span>  `08987058-CADC-4B81-B6E1-30DE50DCBE96`  
        *   <span data-ttu-id="640b9-183">Аппаратная проверка подлинности Windows Hello VBS:</span><span class="sxs-lookup"><span data-stu-id="640b9-183">Windows Hello VBS hardware authenticator:</span></span>  `9DDD1817-AF5A-4672-A2B9-3E3DD95000A9`  

### <span data-ttu-id="640b9-184">Поверхности API API</span><span class="sxs-lookup"><span data-stu-id="640b9-184">API surface</span></span>  

*   <span data-ttu-id="640b9-185">В Microsoft Edge есть полное рекомендации по рекомендациям по рекомендации по корректировке корпоративной версии главной спецификации веб-проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="640b9-185">Microsoft Edge has a complete implementation of the Candidate Recommendation version of the core Web Authentication specification.</span></span>  
*   <span data-ttu-id="640b9-186">[Расширение AppID](https://w3c.github.io/webauthn#sctn-appid-extension) поддерживается.</span><span class="sxs-lookup"><span data-stu-id="640b9-186">The [AppID extension](https://w3c.github.io/webauthn#sctn-appid-extension) is supported.</span></span>  
*   <span data-ttu-id="640b9-187">Другие расширения не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="640b9-187">No other extensions are supported.</span></span>  

## <span data-ttu-id="640b9-188">Демонстрационные примеры</span><span class="sxs-lookup"><span data-stu-id="640b9-188">Demos</span></span>  

[<span data-ttu-id="640b9-189">Пример кода клиента и сервера</span><span class="sxs-lookup"><span data-stu-id="640b9-189">Client and server code sample</span></span>](https://github.com/MicrosoftEdge/webauthnsample)  

[<span data-ttu-id="640b9-190">Демонстрация диска Windows Hello</span><span class="sxs-lookup"><span data-stu-id="640b9-190">Windows Hello Test Drive demo</span></span>](https://webauthnsample.azurewebsites.net)  

## <span data-ttu-id="640b9-191">Спецификаци</span><span class="sxs-lookup"><span data-stu-id="640b9-191">Specification</span></span>  

[<span data-ttu-id="640b9-192">Веб-проверка подлинности: API доступа к aPI для доступа к учетным данным общего ключа</span><span class="sxs-lookup"><span data-stu-id="640b9-192">Web Authentication: An API for accessing Public Key Credentials</span></span>](http://w3c.github.io/webauthn)  
