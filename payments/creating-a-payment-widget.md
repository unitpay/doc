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



