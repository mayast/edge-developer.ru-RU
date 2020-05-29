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
# <span data-ttu-id="02a45-104">Проверка подлинности веб-сайта и Windows Hello</span><span class="sxs-lookup"><span data-stu-id="02a45-104">Web authentication and Windows Hello</span></span>

<span data-ttu-id="02a45-105">API проверки подлинности (прежнее название — *FIDO 2,0* ) в Microsoft EDGE позволяет веб-приложениям использовать биометрию [Windows Hello](https://go.microsoft.com/fwlink/p/?LinkID=624961) для проверки подлинности пользователя, чтобы пользователи могли избежать проблем и рисков управления паролями, включая подбор пароля, фишинг и атаки Keylogging.</span><span class="sxs-lookup"><span data-stu-id="02a45-105">The Web Authentication (formerly *FIDO 2.0* ) API in Microsoft Edge enables web applications to use [Windows Hello](https://go.microsoft.com/fwlink/p/?LinkID=624961) biometrics for user authentication so that you and your users can avoid all the hassles and risks of password management, including password guessing, phishing, and keylogging attacks.</span></span> <span data-ttu-id="02a45-106">Текущая реализация Microsoft EDGE (*предварительно* фиксированная версия) основана на более ранней версии спецификации веб-проверки подлинности и, как правило, изменяется в будущем.</span><span class="sxs-lookup"><span data-stu-id="02a45-106">The current Microsoft Edge (*ms-* prefixed) implementation is based on an earlier draft of the Web Authentication specification and is likely to change in the future.</span></span> **<span data-ttu-id="02a45-107">В этой статье объясняется, как попробовать проверить подлинность Windows Hello с помощью Microsoft EDGE, в то время как в будущем код будет проверяться в соответствии с обновлениями браузера.</span><span class="sxs-lookup"><span data-stu-id="02a45-107">This topic will show you how to try out Windows Hello authentication with Microsoft Edge while also future-proofing your code against browser updates.</span></span>**

<span data-ttu-id="02a45-108">Интерфейс API для проверки подлинности — это развивающаяся Стандартная функция [Fido Alliance](https://fidoalliance.org/) , обеспечивающая взаимодействие веб-проверки подлинности с помощью Windows Hello и других биометрических устройств в разных браузерах.</span><span class="sxs-lookup"><span data-stu-id="02a45-108">The Web Authentication API is an emerging standard put forth by the [FIDO Alliance](https://fidoalliance.org/) with the aim of providing an interoperable way of doing web authentication using Windows Hello and other biometric devices across browsers.</span></span> <span data-ttu-id="02a45-109">Определение веб-проверки подлинности определяет два сценария проверки подлинности: пароль не менее двух факторов.</span><span class="sxs-lookup"><span data-stu-id="02a45-109">The Web Authentication specification defines two authentication scenarios: password-less and two factor.</span></span> <span data-ttu-id="02a45-110">В случае отсутствия пароля пользователю не нужно входить на веб-страницу с помощью имени пользователя или пароля — он может войти исключительно с помощью Windows Hello.</span><span class="sxs-lookup"><span data-stu-id="02a45-110">In the password-less case, the user does not need to log into the web page using a user name or password – they can login solely using Windows Hello.</span></span> <span data-ttu-id="02a45-111">В двух корпусах, пользователь входит в систему с помощью имени пользователя и пароля, но Windows Hello используется в качестве второго фактора для более надежной проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="02a45-111">In the two factor case, the user logs in normally using a username and password, but Windows Hello is used as a second factor check to make the overall authentication stronger.</span></span>

<span data-ttu-id="02a45-112">С помощью веб-проверки подлинности, Объединенной с Windows Hello, сервер отправляет в браузер запрос на обычное текстовое сообщение.</span><span class="sxs-lookup"><span data-stu-id="02a45-112">Using Web Authentication combined with Windows Hello, the server sends down a plain text challenge to the browser.</span></span> <span data-ttu-id="02a45-113">После того, как Microsoft Edge сможет проверить пользователя с помощью Windows Hello, система подсможет подписать ее с помощью закрытого ключа, ранее подготовленного для этого пользователя, и отправить подпись обратно на сервер.</span><span class="sxs-lookup"><span data-stu-id="02a45-113">Once Microsoft Edge is able to verify the user through Windows Hello, the system will sign the challenge with a private key previously provisioned for this user and send the signature back to the server.</span></span> <span data-ttu-id="02a45-114">Если сервер может проверить подпись с помощью открытого ключа, который он имеет для этого пользователя, и убедиться в правильности запроса, он может безопасно пройти проверку подлинности пользователя.</span><span class="sxs-lookup"><span data-stu-id="02a45-114">If the server can validate the signature using the public key it has for that user and verify the challenge is correct, it can authenticate the user securely.</span></span> <span data-ttu-id="02a45-115">При использовании [асимметричной криптографии](https://en.wikipedia.org/wiki/Public-key_cryptography) , например этого, Открытый ключ не имеет собственного смысла, и закрытый ключ никогда не будет общим.</span><span class="sxs-lookup"><span data-stu-id="02a45-115">With [asymmetric cryptography](https://en.wikipedia.org/wiki/Public-key_cryptography) such as this, the public key is meaningless on its own and the private key is never shared.</span></span> <span data-ttu-id="02a45-116">Кроме того, закрытый ключ не может быть перенесен из современной системы с аппаратным обеспечением, поддерживающим доверенный платформенный модуль.</span><span class="sxs-lookup"><span data-stu-id="02a45-116">Furthermore, the private key can never be moved from modern systems with TPM-enabled hardware.</span></span>

<span data-ttu-id="02a45-117">Использование API проверки подлинности веб-страниц состоит из двух основных шагов.</span><span class="sxs-lookup"><span data-stu-id="02a45-117">There are two basic steps to using the Web Authentication API:</span></span>

**<span data-ttu-id="02a45-118">1. Зарегистрируйте пользователя с помощью</span><span class="sxs-lookup"><span data-stu-id="02a45-118">1. Register your user with</span></span> `makeCredential`**

**<span data-ttu-id="02a45-119">2. подлинность пользователя с помощью</span><span class="sxs-lookup"><span data-stu-id="02a45-119">2. Authenticate your user with</span></span> `getAssertion`**

<span data-ttu-id="02a45-120">Приведенные ниже инструкции помогут Вам пошагово пройти этот процесс, используя рекомендуемый [заполненный Webauthn. js](https://github.com/adrianba/fido-snippets/blob/master/polyfill/webauthn.js).</span><span class="sxs-lookup"><span data-stu-id="02a45-120">The following will walk you through this flow using the recommended [Webauthn.js polyfill](https://github.com/adrianba/fido-snippets/blob/master/polyfill/webauthn.js).</span></span> <span data-ttu-id="02a45-121">[Полный код](https://github.com/adrianba/fido-snippets/) доступен для этого сервера и демонстрации на стороне клиента.</span><span class="sxs-lookup"><span data-stu-id="02a45-121">The [complete code](https://github.com/adrianba/fido-snippets/) is available for this server and client side demo.</span></span> <span data-ttu-id="02a45-122">Поддерживаются серверные версии на [языках C#](https://github.com/adrianba/fido-snippets/tree/master/csharp), [PHP](https://github.com/adrianba/fido-snippets/tree/master/php)и [node. js](https://github.com/adrianba/fido-snippets/tree/master/nodejs) .</span><span class="sxs-lookup"><span data-stu-id="02a45-122">[C#](https://github.com/adrianba/fido-snippets/tree/master/csharp), [PHP](https://github.com/adrianba/fido-snippets/tree/master/php), and [Node.JS](https://github.com/adrianba/fido-snippets/tree/master/nodejs) server side versions are available.</span></span>

## <span data-ttu-id="02a45-123">Регистрация пользователя</span><span class="sxs-lookup"><span data-stu-id="02a45-123">Register your user</span></span>

<span data-ttu-id="02a45-124">Выступающий в качестве *поставщика удостоверений*, необходимо сначала создать для пользователя учетные данные для проверки подлинности веб-сайта с помощью Window. webauthn. метод **makeCredential** .</span><span class="sxs-lookup"><span data-stu-id="02a45-124">Acting as an *identity provider*, you will first need to create a Web Authentication credential for your user with the window.webauthn.**makeCredential** method.</span></span> <span data-ttu-id="02a45-125">Прежде чем регистрировать эти учетные данные для пользователя на сервере, вам нужно подтвердить удостоверение пользователя.</span><span class="sxs-lookup"><span data-stu-id="02a45-125">Before you register that credential to the user on your server, you will need to confirm the identity of the user.</span></span> <span data-ttu-id="02a45-126">Это можно сделать, отправив пользователю подтверждение по электронной почте или запросив его, чтобы использовать традиционный способ входа.</span><span class="sxs-lookup"><span data-stu-id="02a45-126">This can be done by sending the user an email confirmation or asking them to use their traditional login method.</span></span>

<span data-ttu-id="02a45-127">Метод makeCredential принимает следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="02a45-127">The makeCredential method takes the following parameters:</span></span>
 - **<span data-ttu-id="02a45-128">сведения об учетной записи пользователя</span><span class="sxs-lookup"><span data-stu-id="02a45-128">user account information</span></span>**

```
    var userAccountInformation = {
        rpDisplayName: "fido-demo",
        displayName: email
    };
```

 - **<span data-ttu-id="02a45-129">параметры шифрования</span><span class="sxs-lookup"><span data-stu-id="02a45-129">crypto parameters</span></span>**

```
    var cryptoParams = [
        {
            type: "ScopedCred",
            algorithm: "RSASSA-PKCS1-v1_5",
        }
    ];
```

<span data-ttu-id="02a45-130">Результирующее обещание возвращает объект, представляющий учетные данные, которые вы затем отправляете обратно на сервер для проверки подлинности в будущем.</span><span class="sxs-lookup"><span data-stu-id="02a45-130">The resulting promise returns an object representing the credential that you then send back to the server for validating future authentications:</span></span>

**<span data-ttu-id="02a45-131">Клиент</span><span class="sxs-lookup"><span data-stu-id="02a45-131">Client</span></span>**

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

<span data-ttu-id="02a45-132">При использовании метода makeCredential приложение Microsoft Edge сначала попросят Windows Hello использовать идентификацию лицом или отпечатком пальцев, чтобы убедиться в том, что пользователь имеет тот же пользователь, что и вход в учетную запись Windows.</span><span class="sxs-lookup"><span data-stu-id="02a45-132">When you use the makeCredential method, Microsoft Edge will first ask Windows Hello to use face or fingerprint identification to verify that the user is the same user as the one logged into the Windows account.</span></span> <span data-ttu-id="02a45-133">После завершения этого действия служба Microsoft Passport создаст пару открытого и закрытого ключа и сохранит закрытый ключ в доверенном платформенном модуле (TPM), который использовался для хранения учетных данных на специальном оборудовании процессора шифрования.</span><span class="sxs-lookup"><span data-stu-id="02a45-133">Once this step is completed, Microsoft Passport will generate a public/private key pair and store the private key in the Trusted Platform Module (TPM), the dedicated crypto processor hardware used to store credentials.</span></span> <span data-ttu-id="02a45-134">Если у пользователя нет устройства с поддержкой доверенного платформенного модуля, эти ключи будут храниться в программном обеспечении.</span><span class="sxs-lookup"><span data-stu-id="02a45-134">If the user doesn’t have a TPM enabled device, these keys will be stored in software.</span></span> <span data-ttu-id="02a45-135">Эти учетные данные создаются для каждого источника, для каждой учетной записи Windows и не будут перемещены, так как они привязаны к устройству.</span><span class="sxs-lookup"><span data-stu-id="02a45-135">These credentials are created per origin, per Windows account, and will not be roamed because they are tied to the device.</span></span> <span data-ttu-id="02a45-136">Это означает, что вы должны убедиться, что пользователь регистрируется для использования Windows Hello для каждого используемого ими устройства.</span><span class="sxs-lookup"><span data-stu-id="02a45-136">This means that you’ll need to make sure the user registers to use Windows Hello for every device they use.</span></span>

## <span data-ttu-id="02a45-137">Проверка подлинности пользователя</span><span class="sxs-lookup"><span data-stu-id="02a45-137">Authenticate your user</span></span>

<span data-ttu-id="02a45-138">После создания учетных данных на клиентском компьютере при следующем входе пользователя в систему с помощью Windows Hello вместо пароля с вызовом Window. webauthn. " **включено**".</span><span class="sxs-lookup"><span data-stu-id="02a45-138">Once the credential is created on the client, the next time the user attempts to log into the site you can offer to sign them in using Windows Hello instead of a password with a call to window.webauthn.**getAssertion**.</span></span>

<span data-ttu-id="02a45-139">Методического *утверждения используется в качестве* единственного нужного параметра.</span><span class="sxs-lookup"><span data-stu-id="02a45-139">The getAssertion method takes the *challenge* as its only required parameter.</span></span> <span data-ttu-id="02a45-140">Задача — это случайное количество, которое сервер отправляет клиенту для подписания с помощью закрытого ключа пользователя.</span><span class="sxs-lookup"><span data-stu-id="02a45-140">The challenge is the randomly generated quantity that the server will send down to a client to sign with the user's private key.</span></span> <span data-ttu-id="02a45-141">Пример</span><span class="sxs-lookup"><span data-stu-id="02a45-141">For example:</span></span>

**<span data-ttu-id="02a45-142">Сервер</span><span class="sxs-lookup"><span data-stu-id="02a45-142">Server</span></span>**

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

<span data-ttu-id="02a45-143">После вызова методаического утверждения Microsoft Edge отобразит запрос Windows Hello, который будет проверять удостоверение пользователя с помощью биометрии.</span><span class="sxs-lookup"><span data-stu-id="02a45-143">Once the getAssertion call is made, Microsoft Edge will show the Windows Hello prompt, which will verify the identity of the user using biometrics.</span></span> <span data-ttu-id="02a45-144">После проверки пользователя проблема будет подписана в доверенном платформенном модуле, и обещание будет возвращаться с помощью объекта утверждения, содержащего подпись и другие метаданные, которые нужно отправить на сервер.</span><span class="sxs-lookup"><span data-stu-id="02a45-144">After the user is verified, the challenge will be signed within the TPM and the promise will return with an assertion object that contains the signature and other metadata for you to send to the server:</span></span>

**<span data-ttu-id="02a45-145">Клиент</span><span class="sxs-lookup"><span data-stu-id="02a45-145">Client</span></span>**

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

<span data-ttu-id="02a45-146">После получения утверждения на сервере вам потребуется проверить подпись для проверки подлинности пользователя.</span><span class="sxs-lookup"><span data-stu-id="02a45-146">Once you receive the assertion on the server, you will need to validate the signature to authenticate the user.</span></span> <span data-ttu-id="02a45-147">Например (в Node. JS):</span><span class="sxs-lookup"><span data-stu-id="02a45-147">For example (in Node.JS):</span></span>

**<span data-ttu-id="02a45-148">Сервер</span><span class="sxs-lookup"><span data-stu-id="02a45-148">Server</span></span>**

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

## <span data-ttu-id="02a45-149">Различия между Microsoft EDGE и спецификацией</span><span class="sxs-lookup"><span data-stu-id="02a45-149">Differences between Microsoft Edge and the spec</span></span>

> [!NOTE]
> <span data-ttu-id="02a45-150">При попытке использовать веб-интерфейс проверки подлинности в Windows Hello в Microsoft Edge мы рекомендуем воспользоваться заполнением Webauthn. js, как показано выше, чтобы не учитывать указанные здесь расхождения.</span><span class="sxs-lookup"><span data-stu-id="02a45-150">When trying out the Web Authentication API with Windows Hello in Microsoft Edge, we recommend using the Webauthn.js polyfill as shown above to avoid having to account for the discrepancies listed here.</span></span> <span data-ttu-id="02a45-151">Мы будем обновлять эту козаполнение для каждой крупной опубликованной версии спецификации.</span><span class="sxs-lookup"><span data-stu-id="02a45-151">We'll update this polyfill for every major published version of the specification.</span></span>


<span data-ttu-id="02a45-152">Текущая реализация Microsoft Edge основывается на более ранней версии спецификации веб-проверки подлинности и, возможно, будет изменена в будущих сборках, а также по мере развития спецификаций.</span><span class="sxs-lookup"><span data-stu-id="02a45-152">The current Microsoft Edge implementation is based on an earlier draft of the Web Authentication specification and is likely to change in future builds and as the spec evolves.</span></span> <span data-ttu-id="02a45-153">Ниже приведены некоторые из текущих различий.</span><span class="sxs-lookup"><span data-stu-id="02a45-153">The current differences include:</span></span>

- <span data-ttu-id="02a45-154">API Microsoft EDGE имеют префиксы.</span><span class="sxs-lookup"><span data-stu-id="02a45-154">Microsoft Edge APIs are MS- prefixed.</span></span>
- <span data-ttu-id="02a45-155">Microsoft Edge пока не поддерживает внешние учетные данные, такие как USB-ключи или устройства Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="02a45-155">Microsoft Edge does not yet support external credentials like USB keys or Bluetooth devices.</span></span> <span data-ttu-id="02a45-156">Текущий API ограничивается внедренными учетными данными, хранящимися в TPM.</span><span class="sxs-lookup"><span data-stu-id="02a45-156">The current API is limited to embedded credentials stored in the TPM.</span></span>
- <span data-ttu-id="02a45-157">Учетная запись пользователя Windows, зарегистрированная в системе, должна поддерживать по крайней мере ПИН-код, а предпочтительнее или биометрию отпечатков пальцев.</span><span class="sxs-lookup"><span data-stu-id="02a45-157">The currently logged in Windows user account must be configured to support at least a PIN, and preferably face or fingerprint biometrics.</span></span> <span data-ttu-id="02a45-158">Это необходимо для того, чтобы система Windows могла проверить подлинность доступа к доверенному платформенному модулю.</span><span class="sxs-lookup"><span data-stu-id="02a45-158">This is to ensure that Windows can authenticate the access to the TPM.</span></span>
- <span data-ttu-id="02a45-159">Реализация Microsoft Edge пока не поддерживает возможности выбора учетной записи.</span><span class="sxs-lookup"><span data-stu-id="02a45-159">The Microsoft Edge implementation does not yet support the account picker experience.</span></span>
- <span data-ttu-id="02a45-160">Второй параметр *фильтров* , указывающий идентификатор учетных данных, в настоящее время нужен для звонков в msCredentials. " [включено](https://msdn.microsoft.com/library/mt697640)".</span><span class="sxs-lookup"><span data-stu-id="02a45-160">A second *filters* parameter specifying the credential id is currently required for calls to msCredentials.[getAssertion](https://msdn.microsoft.com/library/mt697640).</span></span> <span data-ttu-id="02a45-161">Таким образом, при создании учетных данных вам потребуется хранить ИДЕНТИФИКАЦИОНные данные в локальном хранилище на клиенте либо в indexDB, либо localStorage.</span><span class="sxs-lookup"><span data-stu-id="02a45-161">As such, you’ll need to store your credential ID information in local storage on the client, either in indexDB or localStorage when making your credential.</span></span> <span data-ttu-id="02a45-162">Если пользователь удаляет журнал браузера, включая локальное хранилище, ему потребуется повторно зарегистрироваться для использования Windows Hello при следующем входе в систему.</span><span class="sxs-lookup"><span data-stu-id="02a45-162">If a user deletes their browsing history, including local storage, they will need to re-register to use Windows Hello the next time they log in.</span></span>
- <span data-ttu-id="02a45-163">Microsoft EDGE не поддерживает все параметры в текущем черновике веб-проверки подлинности, такие как расширения или таймауты.</span><span class="sxs-lookup"><span data-stu-id="02a45-163">Microsoft Edge does not support all of the options in the current Web Authentication specification draft, such as extensions or timeouts.</span></span>

<span data-ttu-id="02a45-164">На последнем этапе указанные отличия Microsoft Edge указаны в описании перечисленных ниже определений проверки подлинности веб-сайта.</span><span class="sxs-lookup"><span data-stu-id="02a45-164">On that last point, the specific Microsoft Edge differences are noted in the following Web Authentication spec definitions:</span></span>

### <span data-ttu-id="02a45-165">W3C specs</span><span class="sxs-lookup"><span data-stu-id="02a45-165">W3C spec</span></span>

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



## <span data-ttu-id="02a45-166">Справочные материалы по API</span><span class="sxs-lookup"><span data-stu-id="02a45-166">API Reference</span></span>

[<span data-ttu-id="02a45-167">MSCredentials</span><span class="sxs-lookup"><span data-stu-id="02a45-167">MSCredentials</span></span>](https://msdn.microsoft.com/library/mt697639)

[<span data-ttu-id="02a45-168">makeCredential</span><span class="sxs-lookup"><span data-stu-id="02a45-168">makeCredential</span></span>](https://msdn.microsoft.com/library/mt697641)

[<span data-ttu-id="02a45-169">не поддается утверждению</span><span class="sxs-lookup"><span data-stu-id="02a45-169">getAssertion</span></span>](https://msdn.microsoft.com/library/mt697640)

## <span data-ttu-id="02a45-170">Демонстрационные примеры</span><span class="sxs-lookup"><span data-stu-id="02a45-170">Demos</span></span>

[<span data-ttu-id="02a45-171">Примеры кода клиента и сервера</span><span class="sxs-lookup"><span data-stu-id="02a45-171">Client and server code samples</span></span>](https://github.com/adrianba/fido-snippets/)

[<span data-ttu-id="02a45-172">Заполнение Webauthn. js</span><span class="sxs-lookup"><span data-stu-id="02a45-172">Webauthn.js polyfill</span></span>](https://github.com/adrianba/fido-snippets/blob/master/polyfill/webauthn.js)

[<span data-ttu-id="02a45-173">Демонстрация пробного диска Windows Hello</span><span class="sxs-lookup"><span data-stu-id="02a45-173">Windows Hello Test Drive demo</span></span>](https://testdrive-fido.azurewebsites.net/)

## <span data-ttu-id="02a45-174">Specification</span><span class="sxs-lookup"><span data-stu-id="02a45-174">Specification</span></span>

[<span data-ttu-id="02a45-175">Веб-проверка подлинности: веб-API для доступа к учетным данным с областью действия 1</span><span class="sxs-lookup"><span data-stu-id="02a45-175">Web Authentication: A Web API for accessing scoped credentials 1</span></span>](http://w3c.github.io/webauthn/)  
