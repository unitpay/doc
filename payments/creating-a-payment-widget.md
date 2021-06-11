# Creating a payment \(widget\)

A widget is a pop-up window with a payment form. To use the widget, you just need to add its code to the site page, configure the transfer of parameters and create an event for its call \(for example, clicking on a button\). The example code and description of the used widget parameters are located in the Unitpay personal account in the project settings on the "Payment widget" tab \(at the screenshot below\).

![Location of the widget code in the project settings](../.gitbook/assets/image%20%2848%29.png)

## Example code:

```text
<script src="https://widget.unitpay.money/unitpay.js"></script>
<script type="text/javascript">
this.pay = function() {
var payment = new UnitPay();
payment.createWidget({
publicKey: "PUBLIC KEY",
sum: 1,
account: "demo",
domainName: "unitpay.money",
signature: "2c38bb3114b2f02222ee35f6b60c6bbe628ad31bed59633787204ae59659a02e",
desc: "Описание платежа",
locale: "ru",
});
payment.success(function (params) {
console.log('Успешный платеж');
});
payment.error(function (message, params) {
console.log(message);
});
return false;
};
</script>
```

**Additional parameters:**

<table>
  <thead>
    <tr>
      <th style="text-align:left"></th>
      <th style="text-align:left">Value</th>
      <th style="text-align:left">Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><b>locale</b>
      </td>
      <td style="text-align:left">ru, en</td>
      <td style="text-align:left">Forcing the language of the widget.</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>currency</b>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">The order currency according to ISO 4217 (RUB, UAH, BYN, EUR, USD etc.
        <a
        href="https://help.unitpay.ru/v/master/book-of-reference/currency-codes">Currency codes</a>). If the payment system does not support the required
          currency, the amount will be converted to the payment system currency.</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>paymentType</b>
      </td>
      <td style="text-align:left">string</td>
      <td style="text-align:left"><a href="https://help.unitpay.ru/v/master/book-of-reference/payment-system-codes">Code of the payment system</a>,
        through which the payment will be made.</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>hideMenu</b>
      </td>
      <td style="text-align:left">true, false</td>
      <td style="text-align:left">It hides the menu with the payment method options.</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>subscription</b>
      </td>
      <td style="text-align:left">true</td>
      <td style="text-align:left">Use this flag, if you want to create a subscription using the payer&apos;s
        card. The subscription ID (subscriptionId) will be passed in the PAY method
        to your <a href="https://help.unitpay.ru/v/master/payments/payment-handler">payment handler</a>.
        The use of subscriptions is possible only after agreement with the Unitpay
        Security Service.</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>subscriptionId</b>
      </td>
      <td style="text-align:left">number</td>
      <td style="text-align:left">Subscription ID in the UnitPay system. This parameter must be previously
        received in the PAY method to your <a href="https://help.unitpay.ru/v/master/payments/payment-handler">payment handler</a>.</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>preauth</b>
      </td>
      <td style="text-align:left">0,1</td>
      <td style="text-align:left">Use this flag to create a payment with <a href="https://help.unitpay.ru/v/master/payments/pre-authorization-payments">pre-authorization</a>,
        by default the flag is switched off and the value is 0</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>preauthExpireLogic</b>
      </td>
      <td style="text-align:left">number</td>
      <td style="text-align:left">
        <p>The field for the logic of blocking payments with pre-authorization:</p>
        <p></p>
        <p>0 - If there is no request for confirmation or cancellation, the payment
          will be confirmed upon the expiration of the blocking period on the acquiring
          bank&apos;s side (~ 114 hours after the creation of the payment);</p>
        <p></p>
        <p>1 - If there is no confirmation or cancellation request, the payment will
          be canceled after the blocking period on the side of the acquiring bank
          (~ 114 hours after the creation of the payment).</p>
        <p></p>
        <p>If the parameter is not used, the payment will be canceled after the expiration
          date.</p>
      </td>
    </tr>
  </tbody>
</table>

**If you've connected an online cash desc in your Unitpay personal account, then in order to generate receipts, you must additionally transfer a number of parameters:**

|  | Value | Description |
| :--- | :--- | :--- |
| **paymentId** | number | Payment ID in the UnitPay system |
| **account** | string | Subscriber ID in your system \(for example, email or order number\) |
| **orderSum** | number | Order amount, for example, 10.00. Make sure to check this value with the original order amount. |
| **orderCurrency** | string | [Currency](https://help.unitpay.ru/v/master/book-of-reference/currency-codes) of your order |

{% hint style="warning" %}
If you'll have any additional questions during the integration, you can ask them to our customer support - in Unit.Help or send your questions to manager@unitpay.money
{% endhint %}

