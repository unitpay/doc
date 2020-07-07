# Simpla

**The Module Setup and Installation Instruction**

1. Download the [archive](https://github.com/unitpay/simpla-module) with the module.

2. Copy the contents of the unitpay directory from the archive to the &lt;root of your site&gt;/payment.

3. Go to the admin panel of the site and then go to Settings -&gt; Payment.

4. Click Add payment method.

5. In the payment methods, select Unitpay and enter DOMAIN \(unitpay.money\), PUBLIC KEY, and SECRET KEY, which you can find in your personal account on the Unitpay.money website. After setting up the payment method, click Save. 

![https://d33v4339jhl8k0.cloudfront.net/docs/assets/551a91dbe4b0221aadf24410/images/5e68f24f2c7d3a7e9ae9043c/file-0mVe14P1jr.png](../.gitbook/assets/0%20%2840%29.png)

5. Enter the payment handler in your Unitpay.ru account using the template: http://&lt;your site name&gt;/payment/unitpay/callback.php

