# PHPShop

**The Module Setup and Installation Instruction**

1. Download the [archive](https://github.com/unitpay/phpshop-module) with the module.
2. Unpack the contents of the archive to the root of the site.
3. Add the following lines in phpshop/inc/config.php file:

![](../.gitbook/assets/0%20%2826%29.png)

| Ваш публичный ключ из личного кабинета unitpay.money | Your public key from your unitpay.money account |
| :--- | :--- |
| Ваш секретный ключ из личного кабинета unitpay.money | Your secret key from your unitpay.money account |

1. In the admin panel, go to Orders -&gt; Payment Methods and add Unitpay payment method.
2. In your unitpay.money account, enter the address of the payment handler [http://&lt;your](http://<your) site address&gt;/payment/unitpay/result.php

![https://d33v4339jhl8k0.cloudfront.net/docs/assets/551a91dbe4b0221aadf24410/images/58cc04892c7d3a79f5f8d4f5/file-8ygNqAPAqM.png](../.gitbook/assets/1%20%2814%29.png)

