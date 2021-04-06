# Tilda

### Instructions for configuring and installing the module.

1\) In your Tilda account, go to Settings - &gt; Payment Systems -&gt; Universal Payment System. Select the "**Unitpay**" template"

2\) Set the PUBLIC KEY and SECRET KEY from your project settings in UNITPAY

![](../../.gitbook/assets/1%20%2842%29.png)

3\) Set the currency and language of the payment form.

![](../../.gitbook/assets/2%20%2827%29.png)

4\) Check the correctness of the additional parameters in the module settings:  
FVD: INDICATION OF THE CALCULATION METHOD" - should be "Off".  
- Set the " Item type "from the" Item type "parameters [https://help.unitpay.ru/online-cash-register/receipt\_parameters](https://help.unitpay.ru/online-cash-register/receipt_parameters)   
- " Payment method " is set in the settings of your cash register in the Unitpay

5\) Select the VAT rate \(if required\)

![](../../.gitbook/assets/3%20%2812%29.png)

6\) In the Unitpay project settings, set the handler in the format:   
https://tilda.unit-pay.ru/_**PUBLIK KEY из настроек Unitpay**_/callback

![](../../.gitbook/assets/5%20%284%29.png)

{% hint style="warning" %}
Next, contact the **Unitpay support service** for the final configuration and activation of the module.
{% endhint %}

7\) On your project page in Tilda, add a shopping cart \(block **ST100** "Shopping cart with order form"\). The module works correctly only with this type of bucket.   
  
A**ttention!** If you have an online sales register enabled in Unitpay, then you need to add a field with an email or phone number in the shopping cart \(a mandatory parameter for generating a receipt\).

