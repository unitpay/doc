# Advance credit reciepts

If you received an advance payment \(prepayment\) and provided the service / sent the goods, then you need to send the second receipt - the advance credit receipt.

{% hint style="info" %}
The system does not validate the correspondence between the data for the prepayment receipt and the data for the prepayment receipt. Be careful.
{% endhint %}

{% hint style="warning" %}
Affordable only for Unit. Receipts and ATOL
{% endhint %}

To do this, send a request:

{% api-method method="get" host="https://unitpay.ru/api?method=offsetAdvance&params\[paymentId\]=paymentID&params\[secretKey\]=your\_account\_secret\_key&params\[login\]=your\_email" path="" %}
{% api-method-summary %}
offsetAdvance
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="login" type="string" required=true %}
Your Unitpay e-mail
{% endapi-method-parameter %}

{% api-method-parameter name="secretKey" type="string" required=true %}
Partner secretKey
{% endapi-method-parameter %}

{% api-method-parameter type="string" name="paymentId" required=true %}
ID of the payment for which the advance is credited.   
The payment must have parameter _cashItems_ with the payment methods “advance“, “advance payment”, “advance payment 100%”
{% endapi-method-parameter %}

{% api-method-parameter name="cashItems" %}
Strongly required if the payment has already been offset by advance payment. If cashItems is not transferred, the advance payment of the entire payment is credited
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

More about cashItems [here](https://help.unitpay.ru/v/master/payments/parameters-for-receipts).

If the product / service was sold in a currency different from RUB, then in order to receive a prepayment receipt, you need to transfer the amount in RUB. In the advance credit receipt, the amount is always in RUB.

Advance credit receipts are also displayed in your personal account in the general statistics of payments:

![Correct advance receipts&apos; display in statistics](../.gitbook/assets/image%20%2877%29.png)

