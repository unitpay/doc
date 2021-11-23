# DIAFAN.CMS

**The Module Setup and Installation Instruction**

{% hint style="info" %}
The module can also be downloaded directly from the [DIAFAN.CMS marketplace.](https://addons.diafan.ru/modules/platezhi/priem-oplaty-cherez-unitpay647/)
{% endhint %}

1. Download the [archive](https://github.com/unitpay/diafan-module/archive/master.zip) with the module.
2. Copy the contents of the Unitpay directory from the archive to the root of your site.
3. Go to Payment -> Payment Methods and add a new payment method. When choosing a payment system, specify Unitpay.
4. Enter DOMAIN (unitpay.money), PUBLIC KEY, and SECRET KEY which you can get in your Unitpay.money account.
5. In your Unitpay.ru account, enter the address of the payment handler [http://](http://diafan.app/payment/get/unitpay)\<your site address>/payment/get/unitpay

![](<../../.gitbook/assets/0 (33).png>)

{% hint style="info" %}
VAT is set inside the module settings in the "VAT" field: none (without VAT), vat0 (0% VAT), vat10 (10% VAT), vat20 (20% VAT%)
{% endhint %}

![](../../.gitbook/assets/izobrazhenie-20201127-080939.png)
