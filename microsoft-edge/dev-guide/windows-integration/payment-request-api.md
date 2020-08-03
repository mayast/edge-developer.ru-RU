---
description: В этой статье рассказывается о том, как thePayment Request APIenables Microsoft EDGE, которая действует в качестве посредника между получателями, получателями и методами оплаты потребителей, хранящимися в облаке.
title: Руководство по разработке — API запроса на оплату
author: MSEdgeTeam
ms.author: msedgedevrel
ms.date: 07/30/2020
ms.topic: article
ms.prod: microsoft-edge
ms.technology: windows-integration
keywords: EDGE, веб-разработка, HTML, CSS, JavaScript, разработчик
ms.openlocfilehash: b082e311dcbe5cff3101f084e7ff2c145e6e83df
ms.sourcegitcommit: 19ef1422733ef1fd051d2b4f0263ce191e8d67bc
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/31/2020
ms.locfileid: "10902866"
---
# <span data-ttu-id="f7eaf-104">API запроса на оплату (EdgeHTML)</span><span class="sxs-lookup"><span data-stu-id="f7eaf-104">Payment Request API (EdgeHTML)</span></span>

> [!NOTE]
> <span data-ttu-id="f7eaf-105">В этой статье описан рабочий процесс, поддерживаемый в [устаревшей версии Microsoft Edge][MicrosoftSupport44533505].</span><span class="sxs-lookup"><span data-stu-id="f7eaf-105">This article describes the workflow supported in the [legacy version of Microsoft Edge][MicrosoftSupport44533505].</span></span>  <span data-ttu-id="f7eaf-106">Microsoft Edge \ (Chromium \) поддерживает API запроса на оплату с другой реализацией на основе проекта Chromium.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-106">Microsoft Edge \(Chromium\) supports the Payment Request API with a different implementation based on the Chromium project.</span></span>  

<span data-ttu-id="f7eaf-107">Продажи электронных торговли продолжают увеличиваться на быстром темпе.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-107">E-commerce sales continue growing at a rapid pace.</span></span> <span data-ttu-id="f7eaf-108">Согласно [eMarketer](https://www.emarketer.com/), в 2018 цифровые продажи обносятся с учетом того, что увеличиваются до 23% на основе уровней, измеренных в 2013.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-108">According to [eMarketer](https://www.emarketer.com/), by 2018 digital sales are forecasted to increase by 23% from the levels measured in 2013.</span></span>  <span data-ttu-id="f7eaf-109">Несмотря на то, что потребительские и коммерческие компании будут пользоваться преимуществами продаж из электронных торговли, проблемы остаются.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-109">While consumers and businesses enjoy the convenience of e-commerce sales, challenges remain.</span></span>  <span data-ttu-id="f7eaf-110">Сегодня каждый из владельцев веб-сайтов электронной коммерции должен вкладывать время в разработку бесплатных потоков и правил проверки.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-110">Today each e-commerce website owner needs to invest time to develop high quality payment checkout flows and validation rules.</span></span>  <span data-ttu-id="f7eaf-111">Потребители должны перемещаться по разным заказам на извлечение и повторно вводить одинаковые сведения о платежах и отправке на каждом сайте, где они будут покупаться.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-111">Consumers need to navigate different payment checkout flows and re-enter the same payment and shipping information on every site where they shop.</span></span>  <span data-ttu-id="f7eaf-112">Это может занять много времени и неприятностей для потребителей, что приводит к высокой доле отказов в корзине покупок и снижению продаж для торговых продавцов.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-112">This can be time consuming and frustrating for consumers, leading to a high rate of shopping cart abandonment and decreased sales for merchants.</span></span> <span data-ttu-id="f7eaf-113">[Оценка](http://baymard.com/lists/cart-abandonment-rate) продавцов в масштабах от 60% до 70% покупательской корзины отброшена.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-113">Merchants [estimate](http://baymard.com/lists/cart-abandonment-rate) between 60% and 70% of shopping carts are abandoned.</span></span>      

<span data-ttu-id="f7eaf-114">[API запроса на оплату](https://w3.org/TR/payment-request/) – это функция, которая стандартизует процесс извлечения платежа.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-114">The [Payment Request API](https://w3.org/TR/payment-request/) standardizes the payment checkout process.</span></span> <span data-ttu-id="f7eaf-115">Этот API требует меньше настроек для веб-разработчиков и обеспечивает более быструю, более согласованную и, таким образом, более понятную и удобную работу для потребителей.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-115">This API requires less customization for web developers and provides a faster, more consistent, and therefore, less confusing experience for consumers.</span></span>  <span data-ttu-id="f7eaf-116">Поскольку потребители могут выбирать платежные средства и адреса доставки из своей учетной записи Майкрософт, они обязаны вводить меньше данных для заполнения покупок, что сокращает время и ввод данных, необходимых для выполнения оплаты.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-116">Because consumers can select payment instruments and shipping addresses from their Microsoft account, they are required to enter less data to complete purchases which reduces the time and data entry required to complete a payment.</span></span>   

<span data-ttu-id="f7eaf-117">[API запроса на оплату](https://w3.org/TR/payment-request/) — это открытый стандартный стандарт, который позволяет браузерам выступать в качестве посредника между продавцами, получателями и методами оплаты (например, кредитными картами), которые пользователи хранили в облаке.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-117">The [Payment Request API](https://w3.org/TR/payment-request/) is an open, cross-browser standard that enables browsers to act as an intermediary between merchants, consumers, and the payment methods (e.g. credit cards) that consumers have stored in the cloud.</span></span> 
  
<span data-ttu-id="f7eaf-118">Если вы используете [API запроса на оплату](https://w3.org/TR/payment-request/), пользователи в обычном режиме изменяют веб-сайты продавцов.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-118">In summary, when using the [Payment Request API](https://w3.org/TR/payment-request/), customers shop on merchant websites as normal.</span></span>  <span data-ttu-id="f7eaf-119">Когда вы будете готовы к оплате, на веб-сайте получателя платежа вызывается API **запроса на оплату** , чтобы создать **запрос на оплату** и передать в браузер необходимые сведения о платежах (например, Поддерживаемые методы оплаты, сумма покупки, валюта и т. д.).</span><span class="sxs-lookup"><span data-stu-id="f7eaf-119">When ready to pay, the merchant website calls the **Payment Request** API to create a **Payment Request** and passes the relevant payment information (e.g. supported payment methods, purchase amount, currency, etc.) to the browser.</span></span>

![Конструктор запросов на оплату](./../media/payment_request_construct.png)

<span data-ttu-id="f7eaf-121">Браузер выполняет проверку подлинности пользователя, позволяет пользователю выбирать поддерживаемый метод оплаты для файла и обрабатывает платежные данные.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-121">The browser authenticates the user, enables the user to select a supported payment method on file, and processes the payment details.</span></span> <span data-ttu-id="f7eaf-122">Затем браузер отправляет сведения о платеже на веб-сайт продавца, чтобы он мог завершить платежи.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-122">The browser then sends the payment information details back to the merchant website, so that the merchant can complete the payment.</span></span>  <span data-ttu-id="f7eaf-123">Помимо получения платежных данных, продавец также может выбрать получение сведений о доставке в рамках **запроса на оплату**.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-123">In addition to receiving payment information, the merchant can also elect to receive shipping information as part of the **Payment Request**.</span></span>  

![Создание отклика на платеж](./../media/payment_response_construct.png)

<span data-ttu-id="f7eaf-125">Чтобы ознакомиться с ИНТЕРФЕЙСом запроса на оплату в действии, а также получить общие сведения о том, как его использовать, ознакомьтесь с этим видеороликом.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-125">To see the Payment Request API in action, as well as get an overview of how to use it, check out this video.</span></span>

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Using-the-Payments-Request-API/player]


> [!NOTE]
> <span data-ttu-id="f7eaf-126">API запроса на оплату поддерживается в Microsoft Edge Build 14992 +.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-126">The Payment Request API is supported in Microsoft Edge build 14992+.</span></span>


## <span data-ttu-id="f7eaf-127">Создание запроса на оплату</span><span class="sxs-lookup"><span data-stu-id="f7eaf-127">Creating a Payment Request</span></span> 
<span data-ttu-id="f7eaf-128">Веб-страницы создают **запрос на оплату** , как правило, когда пользователь инициирует процесс оплаты нажатием кнопки "Купить".</span><span class="sxs-lookup"><span data-stu-id="f7eaf-128">Web pages create a **Payment Request** typically when the user initiates a payment process by clicking a "buy" button.</span></span>  <span data-ttu-id="f7eaf-129">Конструктор **запросов на оплату** [constructor](https://msdn.microsoft.com/library/mt790440) включает methodData, Details и Options.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-129">The **Payment Request** [constructor](https://msdn.microsoft.com/library/mt790440) includes methodData, details, and options.</span></span> 

```js
var payment = new PaymentRequest ( 
    methodData,  // required payment method data including payment method identifiers 
    details,     // required transaction information 
    options      // optional information like shipping or contact info to be returned 
); 
```

<span data-ttu-id="f7eaf-130">Этот [`methodData`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) параметр включает список методов оплаты и относящихся к ним сетей, принятых на веб-сайте, а также связанных с ними данных.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-130">The [`methodData`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parameter contains a list of the payment methods and networks accepted by the website and any associated payment method specific data.</span></span> <span data-ttu-id="f7eaf-131">В Microsoft Edge этот список соответствует поддерживаемым методам оплаты, которые покупатель сохранил в своей учетной записи Майкрософт, и приводит к появлении списка "платить за" в пользовательском интерфейсе оплаты.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-131">In Microsoft Edge, this list is matched with the supported payment methods that the shopper has saved in their Microsoft account and results in the "pay with" list in the payment user experience.</span></span>

![Список "платить за" в пользовательском интерфейсе Microsoft "Бумажник"](./../media/pay_with.png)

```js
var supportedInstruments = [{
    supportedMethods: ['basic-card'],
    data: {
        supportedNetworks: ['visa', 'mastercard', 'amex'],
        supportedTypes: ['credit'] 
    }         
}]; 
```

<span data-ttu-id="f7eaf-133">[`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params)Параметр, содержащий сведения о том, что продавец хочет передать клиенту о транзакции.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-133">The [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parameter contains information that the merchant wishes to convey to the customer about the transaction.</span></span>  <span data-ttu-id="f7eaf-134">Сюда входят элементы сводки заказов, такие как итоговый, налоговый, сумма отгрузки и другие элементы сводного уровня, влияющие на сумму платежа.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-134">These include order summary items like total, tax, shipping amount, and other summary level items impacting the payment amount.</span></span> <span data-ttu-id="f7eaf-135">Они не предназначены для размещения элементов строки заказа.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-135">These are not intended to be order line items.</span></span> 
  
<span data-ttu-id="f7eaf-136">Этот [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) параметр также используется для определения вариантов доставки, доступных клиенту при необходимости.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-136">The [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parameter is also used to define shipping options available to the customer when required.</span></span>  <span data-ttu-id="f7eaf-137">Дополнительные сведения содержатся в разделе " **Заявка на оплату** " с разделом "Доставка".</span><span class="sxs-lookup"><span data-stu-id="f7eaf-137">More details are included in the **Payment Request** with Shipping section below.</span></span> 

<span data-ttu-id="f7eaf-138">Каждая [`detail`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) строка содержит метку валюты и сумму.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-138">Each [`detail`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) line includes a label for the currency and the amount.</span></span>  

> [!NOTE]
> <span data-ttu-id="f7eaf-139">В **запросе на оплату** не вычисляется сумма или сумма этих сумм.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-139">The **Payment Request** does not calculate the sum or total of these amounts.</span></span>  <span data-ttu-id="f7eaf-140">Проверка правильности общего числа элементов строки осуществляется с помощью веб-сайта продавца.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-140">It is the responsibility of the merchant's website to ensure that the line items total correctly.</span></span>   


![Промежуточные итоги, отгрузка, налоги и общие сведения](./../media/show_details.png)

```js
var details = {
    total: {
        label: 'Total (USD)',
        amount: {currency: 'USD', value: '193.98'}
    },
    displayItems: [{
        label: 'Subtotal',
        amount: {currency: 'USD', value: '174.99'}
    }, {
        label: 'Taxes',
        amount: {currency: "USD", value: '18.99'}
    }],
};  
```

<span data-ttu-id="f7eaf-142">[`PaymentRequest`](https://msdn.microsoft.com/library/mt790440)не поддерживает возврат денег, поэтому суммы всегда должны быть положительными; отдельные элементы списка могут быть отрицательными (например, скидками).</span><span class="sxs-lookup"><span data-stu-id="f7eaf-142">[`PaymentRequest`](https://msdn.microsoft.com/library/mt790440) does not support refunds, so the amounts should always be positive; individual list items can be negative, such as discounts.</span></span> 

<span data-ttu-id="f7eaf-143">Браузер выполнит обработку меток по мере их определения и автоматически отрисовывает правильное форматирование денежных единиц на основе языкового стандарта клиента.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-143">The browser will render the labels as you define them and automatically render the correct currency formatting based on the customer's locale.</span></span> <span data-ttu-id="f7eaf-144">Обратите внимание, что метки должны отображаться на одном языке с содержимым.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-144">Note that the labels should be rendered in the same language as your content.</span></span> 

<span data-ttu-id="f7eaf-145">Этот [`options`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) параметр определяет данные, которые веб-страница возвращает из **запроса на платеж**.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-145">The [`options`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parameter defines data the web page wants returned from the **Payment Request**.</span></span> <span data-ttu-id="f7eaf-146">Кроме того, определяются данные, которые необходимо собирать, в том числе если требуется доставка, адрес электронной почты и/или номер телефона.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-146">This also defines the data that needs to be collected, including if shipping, email address, and/or phone number are required.</span></span>

![Раскрывающийся список "адрес электронной почты"](./../media/email_snippet.png)


```js
var options =
    {
        requestPayerEmail: true
    }; 
``` 

## <span data-ttu-id="f7eaf-148">Отображение запроса на оплату</span><span class="sxs-lookup"><span data-stu-id="f7eaf-148">Showing the Payment Request</span></span>

<span data-ttu-id="f7eaf-149">[`show()`](https://msdn.microsoft.com/library/mt790448)Метод вызывается веб-страницей, чтобы разрешить пользователю взаимодействовать с пользовательским интерфейсом **запроса на оплату** .</span><span class="sxs-lookup"><span data-stu-id="f7eaf-149">The [`show()`](https://msdn.microsoft.com/library/mt790448) method is called by the web page to allow the user to interact with the **Payment Request** user interface.</span></span>  <span data-ttu-id="f7eaf-150">[`show()`](https://msdn.microsoft.com/library/mt790448)Метод возвращает обещание, которое будет разрешено, когда пользователь авторизует запрос на платеж.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-150">The [`show()`](https://msdn.microsoft.com/library/mt790448) method returns a Promise that will be resolved when the user authorizes the payment request.</span></span>  

```js
paymentRequest.show().then(paymentInstrumentResponse => {

paymentInstrumentResponse.complete('success').then().catch(error => {
    handlePaymentRequestError(error); 
});
```

![Подтверждение и оплата данных](./../media/pay_screen_default.png)

## <span data-ttu-id="f7eaf-152">Прерывание запроса на оплату</span><span class="sxs-lookup"><span data-stu-id="f7eaf-152">Aborting a Payment Request</span></span>
 
<span data-ttu-id="f7eaf-153">Этот [`abort()`](https://msdn.microsoft.com/library/mt790437) метод может быть вызван веб-страницей в любое время после [`show()`](https://msdn.microsoft.com/library/mt790448) вызова метода, до тех пор, пока обещание не будет разрешено.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-153">The [`abort()`](https://msdn.microsoft.com/library/mt790437) method can be called by the web page any time after the [`show()`](https://msdn.microsoft.com/library/mt790448) method is called, up until the point where the Promise is resolved.</span></span>  <span data-ttu-id="f7eaf-154">[`abort()`](https://msdn.microsoft.com/library/mt790437)Метод заставит браузер прервать **запрос на оплату** и закрыть пользовательский интерфейс **запроса на оплату** .</span><span class="sxs-lookup"><span data-stu-id="f7eaf-154">The [`abort()`](https://msdn.microsoft.com/library/mt790437) method will cause the browser to abort the **Payment Request** and close the **Payment Request** user interface.</span></span>  <span data-ttu-id="f7eaf-155">Например, веб-страница может прерываться, если пользователь не завершил транзакцию в течение требуемого времени.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-155">For example, a web page may choose to abort if the user did not complete the transaction in the required amount of time.</span></span>

```js
payment.abort();
``` 

## <span data-ttu-id="f7eaf-156">Отклик на оплату</span><span class="sxs-lookup"><span data-stu-id="f7eaf-156">Payment Response</span></span>
<span data-ttu-id="f7eaf-157">Когда клиент утверждает **заявку на оплату**, на веб-сайт возвращается **ответ на платеж** .</span><span class="sxs-lookup"><span data-stu-id="f7eaf-157">When the customer approves the **Payment Request**, a **Payment Response** is returned to the website.</span></span> <span data-ttu-id="f7eaf-158">**Отклики на платеж** включают следующее:</span><span class="sxs-lookup"><span data-stu-id="f7eaf-158">The **Payment Response** includes the following:</span></span> 

 <span data-ttu-id="f7eaf-159">Свойство</span><span class="sxs-lookup"><span data-stu-id="f7eaf-159">Property</span></span>      | <span data-ttu-id="f7eaf-160">Описание</span><span class="sxs-lookup"><span data-stu-id="f7eaf-160">Description</span></span> | <span data-ttu-id="f7eaf-161">Обязательный</span><span class="sxs-lookup"><span data-stu-id="f7eaf-161">Required</span></span> | <span data-ttu-id="f7eaf-162">Дополнительные сведения</span><span class="sxs-lookup"><span data-stu-id="f7eaf-162">Additional Info</span></span>
|---------------|-----------------|-------|-----------------|
[`methodName`](https://msdn.microsoft.com/library/mt790656) | <span data-ttu-id="f7eaf-163">Идентификатор метода оплаты, выбранного пользователем.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-163">The ID for the payment method selected by the user</span></span> | <span data-ttu-id="f7eaf-164">Y</span><span class="sxs-lookup"><span data-stu-id="f7eaf-164">Y</span></span> | | 
[`details`](https://msdn.microsoft.com/library/mt790655) | <span data-ttu-id="f7eaf-165">Объект JSON, включающий все данные, которые требуется продавцу для обработки транзакции с помощью выбранного метода оплаты или маркера оплаты</span><span class="sxs-lookup"><span data-stu-id="f7eaf-165">A JSON object that includes all of the data the merchant requires to process the transaction using the selected payment method or a payment token</span></span> | <span data-ttu-id="f7eaf-166">Y</span><span class="sxs-lookup"><span data-stu-id="f7eaf-166">Y</span></span> | <span data-ttu-id="f7eaf-167">[Простая карточка](https://go.microsoft.com/fwlink/?linkid=834965) Dictionary: cardholderName; cardNumber; expiryMonth; expiryYear; cardSecurityCode; billingAddress;</span><span class="sxs-lookup"><span data-stu-id="f7eaf-167">[Basic Card](https://go.microsoft.com/fwlink/?linkid=834965) Dictionary: cardholderName; cardNumber; expiryMonth; expiryYear; cardSecurityCode; billingAddress;</span></span> | 
[`shippingAddress`](https://msdn.microsoft.com/library/mt790445) | <span data-ttu-id="f7eaf-168">Адрес доставки, выбранный пользователем</span><span class="sxs-lookup"><span data-stu-id="f7eaf-168">The shipping address selected by the user</span></span>  |  <span data-ttu-id="f7eaf-169">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-169">Optional.</span></span> <span data-ttu-id="f7eaf-170">Требуется при [`requestShipping`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) **истинности**</span><span class="sxs-lookup"><span data-stu-id="f7eaf-170">Required when [`requestShipping`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) is **True**</span></span>  | <span data-ttu-id="f7eaf-171">Словарь адресов: страна; addressLine; региональных город dependentLocality; Индекс sortingCode; languageCode; всей получателя Кнопка</span><span class="sxs-lookup"><span data-stu-id="f7eaf-171">Address dictionary: country; addressLine; region; city; dependentLocality; postalCode; sortingCode; languageCode; organization; recipient; phone</span></span> |
[`shippingOption`](https://msdn.microsoft.com/library/mt790446) | <span data-ttu-id="f7eaf-172">Идентификатор выбранного варианта отгрузки</span><span class="sxs-lookup"><span data-stu-id="f7eaf-172">The ID for the selected shipping option</span></span> | <span data-ttu-id="f7eaf-173">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-173">Optional.</span></span> <span data-ttu-id="f7eaf-174">Требуется при [`requestShipping`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) **истинности**</span><span class="sxs-lookup"><span data-stu-id="f7eaf-174">Required when [`requestShipping`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) is **True**</span></span>  | | 
[`payerName`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) | <span data-ttu-id="f7eaf-175">Имя, указанное пользователем.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-175">The name provided by the user</span></span>  | <span data-ttu-id="f7eaf-176">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-176">Optional.</span></span> <span data-ttu-id="f7eaf-177">Требуется при [`requestPayerName`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) **истинности**</span><span class="sxs-lookup"><span data-stu-id="f7eaf-177">Required when [`requestPayerName`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) is **True**</span></span> | |
[`payerEmail`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) | <span data-ttu-id="f7eaf-178">Адрес электронной почты, выбранный пользователем</span><span class="sxs-lookup"><span data-stu-id="f7eaf-178">The email address selected by the user</span></span> | <span data-ttu-id="f7eaf-179">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-179">Optional.</span></span> <span data-ttu-id="f7eaf-180">Требуется при [`requestPayerEmail`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) **истинности**</span><span class="sxs-lookup"><span data-stu-id="f7eaf-180">Required when [`requestPayerEmail`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) is **True**</span></span>  | |
[`PayerPhone`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) | <span data-ttu-id="f7eaf-181">Номер телефона, выбранный пользователем</span><span class="sxs-lookup"><span data-stu-id="f7eaf-181">The phone number selected by the user</span></span> | <span data-ttu-id="f7eaf-182">Необязательно.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-182">Optional.</span></span> <span data-ttu-id="f7eaf-183">Требуется при [`requestPayerPhone`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) **истинности**</span><span class="sxs-lookup"><span data-stu-id="f7eaf-183">Required when [`requestPayerPhone`](https://msdn.microsoft.com/library/mt790440#PaymentOptions) is **True**</span></span> | |

<span data-ttu-id="f7eaf-184">[`details`](https://msdn.microsoft.com/library/mt790655#PaymentRequest_params)Объект JSON в **ответе на платеж** будет содержать данные платежа, необходимые продавцу для обработки платежа.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-184">The [`details`](https://msdn.microsoft.com/library/mt790655#PaymentRequest_params) JSON object in the **Payment Response** will contain the payment data required by the merchant to process a payment.</span></span> <span data-ttu-id="f7eaf-185">В самой простой форме ответ будет представлять собой базовые полезные данные [карты](https://go.microsoft.com/fwlink/?linkid=834965) , содержащие сведения о платежных картах с открытым текстом.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-185">In its simplest form, the response will be a [Basic Card](https://go.microsoft.com/fwlink/?linkid=834965) payload containing cleartext payment card details.</span></span> <span data-ttu-id="f7eaf-186">Если у продавцов есть дополнительные участники шлюзов и процессоров для обеспечения поддержки оплаты, для продавцов может потребоваться полезная нагрузка, которую может обработать процессор.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-186">Where merchants have arrangements with additional gateway/processor partners for them to provide payments support, the merchant may require a payload the processor can handle.</span></span> <span data-ttu-id="f7eaf-187">Они могут использовать форму маркера процессора/шлюза или зашифрованного средства оплаты.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-187">These can take the shape of a processor/gateway token or an encrypted payment instrument.</span></span> <span data-ttu-id="f7eaf-188">Эти методы оплаты находятся за пределами области настоящего документа и будут рассмотрены в документации, касающейся процессора.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-188">These payment methods are outside the scope of this document and will be covered in documentation specific to the processor.</span></span> <span data-ttu-id="f7eaf-189">Кроме того, чтобы получить [простой](https://go.microsoft.com/fwlink/?linkid=834965) ответ на карту, разработчику не требуется дополнительное подключение к корпорации Майкрософт, в отличие от других методов оплаты процессора/шлюза, которые могут потребовать выставления ключа шифрования или авторизации запросов (OAuth).</span><span class="sxs-lookup"><span data-stu-id="f7eaf-189">Additionally, to receive a [Basic Card](https://go.microsoft.com/fwlink/?linkid=834965) response, no additional onboarding to Microsoft is required by the developer, unlike other processor/gateway specific payment methods which may require encryption key onboarding or request authorization (oauth).</span></span> 

<span data-ttu-id="f7eaf-190">После получения **ответа**на него веб-сайт отправляет платежную информацию в свой обработчик оплаты.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-190">Upon receiving the **Payment Response**, the website submits the payment information to their payment processor.</span></span>  <span data-ttu-id="f7eaf-191">Во время обработки платежа браузер отобразит страницу счетчика.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-191">The browser will display a spinner page while the payment is being processed.</span></span>

![Страница, отображаемая при обработке платежа](./../media/loading_screen.png)

<span data-ttu-id="f7eaf-193">После того как платеж будет выполнен, веб-страница вызывает [`complete()`](https://msdn.microsoft.com/library/mt790642) метод и передает значение **успеха** или **сбой**.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-193">Once the payment is complete, the web page calls the [`complete()`](https://msdn.microsoft.com/library/mt790642) method and passes a value of **success** or **fail**.</span></span>  <span data-ttu-id="f7eaf-194">[`complete()`](https://msdn.microsoft.com/library/mt790642)Метод информирует браузер о том, что приобретение завершено, и соответствующий экран пользовательского интерфейса должен отображаться в зависимости от значения **успеха** или **ошибки**.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-194">The [`complete()`](https://msdn.microsoft.com/library/mt790642) method informs the browser that the purchase is finished and the appropriate terminating UI screen should be shown depending on the value of **success** or **fail**.</span></span> 

![<span data-ttu-id="f7eaf-195">Пользовательский интерфейс, отображаемый при успешном завершении покупки ](./../media/response_payment-request_complete.png)
![ , когда произошел сбой покупки</span><span class="sxs-lookup"><span data-stu-id="f7eaf-195">The UI displayed when the purchase succeeded](./../media/response_payment-request_complete.png)
![The UI displayed when the purchase failed</span></span>](./../media/response_payment-request_failure.png)

## <span data-ttu-id="f7eaf-196">Заявка на оплату с отгрузкой</span><span class="sxs-lookup"><span data-stu-id="f7eaf-196">Payment Request with Shipping</span></span>

### <span data-ttu-id="f7eaf-197">Адрес доставки</span><span class="sxs-lookup"><span data-stu-id="f7eaf-197">Shipping Address</span></span>

<span data-ttu-id="f7eaf-198">Для продаж, для которых требуется доставка физических товаров, требуется адрес доставки.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-198">For sales that require shipping physical goods, a shipping address is required.</span></span>  <span data-ttu-id="f7eaf-199">Чтобы включить адрес доставки, укажите его `requestShipping = True` в [`options`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) параметре запроса.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-199">To include a shipping address, set `requestShipping = True` in the [`options`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parameter of the request.</span></span>   

<span data-ttu-id="f7eaf-200">Когда пользователь выбирает или обновляет адрес доставки, [`onshippingaddresschange`](https://msdn.microsoft.com/library/mt790442) событие будет запущено.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-200">When the user selects or updates the shipping address, the [`onshippingaddresschange`](https://msdn.microsoft.com/library/mt790442) event will run.</span></span>  <span data-ttu-id="f7eaf-201">На веб-сайте, использующем прослушиватель событий, будет содержаться уведомление об изменении, после чего можно проверить адрес, повторно рассчитать затраты на доставку и налоги, а также обновить, [`shippingOptions`](https://msdn.microsoft.com/library/mt790440) чтобы отобразить измененные затраты и варианты отправки, доступные для выбранного адреса (если применимо).</span><span class="sxs-lookup"><span data-stu-id="f7eaf-201">The website, using an event listener, will be aware of the change and can then validate the address, re-calculate shipping costs and taxes, and update [`shippingOptions`](https://msdn.microsoft.com/library/mt790440) to reflect the changed costs and shipping options available for the address selected (if applicable).</span></span> 

### <span data-ttu-id="f7eaf-202">Варианты отправки</span><span class="sxs-lookup"><span data-stu-id="f7eaf-202">Shipping Options</span></span> 

<span data-ttu-id="f7eaf-203">Варианты доставки можно представить клиенту, добавив [`shippingOptions`](https://msdn.microsoft.com/library/mt790440) к [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) параметру.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-203">Shipping options can be presented to the customer by adding [`shippingOptions`](https://msdn.microsoft.com/library/mt790440) to the [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parameter.</span></span>  <span data-ttu-id="f7eaf-204">Настройка по умолчанию может быть установлена `selected = True` для одного из вариантов отправки.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-204">A default can be established by setting `selected = True` for one of the shipping options.</span></span> 
 
<span data-ttu-id="f7eaf-205">Когда пользователь выбирает или обновляет shippingOptions, [`onshippingoptionchange`](https://msdn.microsoft.com/library/mt790436) событие будет запущено.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-205">When the user selects or updates the shippingOptions, the [`onshippingoptionchange`](https://msdn.microsoft.com/library/mt790436) event will run.</span></span>  <span data-ttu-id="f7eaf-206">На веб-сайте, использующем прослушиватель событий, будет содержаться сообщение об изменении и может обновить [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) параметр с учетом нужной суммы отгрузки.</span><span class="sxs-lookup"><span data-stu-id="f7eaf-206">The website, using an event listener, will be aware of the change and can update the [`details`](https://msdn.microsoft.com/library/mt790440#PaymentRequest_params) parameter with the correct shipping amount.</span></span>   

```js
var details = {
    total: {
        label: 'Total (USD)',
        amount: {currency: 'USD', value: '193.98'}
    },
    displayItems: [{
         label: 'Subtotal',
         amount: {currency: 'USD', value: '174.99'}
        }, {
            label: 'Shipping',
            amount: {currency: 'USD', value: '0.00'}
        }, {
            label: 'Taxes',
            amount: {currency: "USD", '18.99'}
    }],
    shippingOptions: [{
        id: 'STANDARD',
        label: 'Standard – FREE (5-6 Business days)',
        amount: {currency: 'USD', value: '0.00'},
        selected: true
    }, {
        id: 'EXPEDITED',
        label: 'Two-Day Shipping',
        amount: {currency: 'USD', value: '7.00'}
    }]
};
        
var options = {
    requestShipping: true,
    requestPayerEmail: true
}; 
 
```

## <span data-ttu-id="f7eaf-207">Справочник по API</span><span class="sxs-lookup"><span data-stu-id="f7eaf-207">API Reference</span></span>
[<span data-ttu-id="f7eaf-208">API запроса оплаты</span><span class="sxs-lookup"><span data-stu-id="f7eaf-208">Payment Request API</span></span>](https://msdn.microsoft.com/library/mt790447)

## <span data-ttu-id="f7eaf-209">Specification</span><span class="sxs-lookup"><span data-stu-id="f7eaf-209">Specification</span></span>
[<span data-ttu-id="f7eaf-210">API запроса оплаты</span><span class="sxs-lookup"><span data-stu-id="f7eaf-210">Payment Request API</span></span>](https://w3.org/TR/payment-request/)

<!-- links -->  

[DevtoolsGuideChromium]: /microsoft-edge/devtools-guide-chromium "Инструменты разработчика Microsoft EDGE (Chromium) | Документы Microsoft"  

[MicrosoftSupport44533505]: https://support.microsoft.com/help/4533505 "Что такое Microsoft Edge Legacy?"  
