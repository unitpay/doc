# Google Pay™

### **About Google Pay**™

**Google Pay**™ is a fast and simple payment method that allows you to make card payments without entering card details for each payment. The card data is safely stored by **Google**™. This payment method is available for all devices \(mobile phones and computers\), regardless of the operating system and web browser.

Unitpay gives you a way to easily add it on your checkout page, making it more convenient for your clients to pay on your website.

As a merchant, you can use **Google Pay**™ via **Unitpay** checkout page or via **Google Pay**™ **API.**

### Integration via **Unitpay** checkout page

**Google Pay**™ via **Unitpay** checkout page will be available for you after integration. 

[Here ](https://help.unitpay.ru/first_steps)you can read about first steps of integration \(registration, adding a project\). 

[Here ](https://help.unitpay.ru/payments)you can read about work with payments.

You can check the availability of accepting payments via **Google Pay**™ on the settings page of your project in **Unitpay**. As shown in the picture below:

![](.gitbook/assets/2020-11-24_18-42-22.png)

The payer will see a page with the name of product, prices and **Google Pay**™ ****button:

![](.gitbook/assets/image%20%2846%29.png)

### **Connection with Google Pay API**

#### **Before you start**

* You should register with **Google Pay**™ **API** to proceed with this integration option.
* Your website should use HTTPS and support TLS protocol.
* You should be registered with **Unitpay** as a merchant.

#### Instruction

Firstly please review the following documentation in order to get familiar with the integration process:

* API documentation [for mobile application](https://developers.google.com/pay/api/android) and [for website](https://developers.google.com/pay/api/web)
* Brand guidelines [for mobile application](https://developers.google.com/pay/api/android/guides/brand-guidelines) and [for website](https://developers.google.com/pay/api/web/guides/brand-guidelines)

The `gateway` parameter in the script should have the constant value of `unitpay`.

The value of the `gatewayMerchantId` parameter should be the identifier of the payment point where the order is made.

```text
"gateway": "unitpay"
"gatewayMerchantId": "YOUR_GATEWAY_MERCHANT_ID"
```

In response, Google shall return the `PaymentData` item, and the field `paymentMethodData.tokenizationData.token` shall contain a safely encrypted **Google Pay™** Token \(a string of characters\).

Supported payment systems:

```text
"allowedCardNetworks": [
    "MASTERCARD",
    "VISA"
]
```

Supported authorization methods:

```text
"allowedAuthMethods": [
    "PAN_ONLY",
    "CRYPTOGRAM_3DS"
]
```

Billing request parameter `BillingAddressParameters`is not used. 

**Charging**

To charge the payment card stored under **Google Pay™**, in the direct method request fill in `paymentType` and `token` with the following values:

* `"paymentType": "googlepay"`
* `"token": "${paymentMethodData.tokenizationData.token}"`

Further processing of the request is subject to the standard payment process.

{% hint style="info" %}
If the card supports 3DS for PAN\_ONLY credentials, you will receive a redirectUrl in response, where you need to redirect the payer.
{% endhint %}

Please note that it may be necessary to handle a redirect of the request to the 3D Secure authentication page.

* `"redirectUrl": "https://{url-for-redirect}..."`

After creating the payment, you will receive `paymentId`, by which you can [check](https://help.unitpay.ru/v/master/payments/payment-info) the status of the payment.

**Google Pay**™ documentation:

* [Google Pay for payments on websites](https://developers.google.com/pay/api/web/)
* [Integration checklist](https://developers.google.com/pay/api/web/guides/test-and-deploy/integration-checklist)
* [Brand guidelines](https://developers.google.com/pay/api/web/guides/brand-guidelines)

