# Drupal 7 \(commerce\)

**The Module Setup and Installation Instruction**

1. Download the [archive](https://github.com/unitpay/commerce-module) with the module.

2. Install the module. To do this, copy the contents of the Unitpay directory from the archive to the address &lt;folder with your site&gt;/sites/all/modules. After that, click Modules in the menu, check the box next to Unitpay and click Save сonfiguration.

![https://d33v4339jhl8k0.cloudfront.net/docs/assets/551a91dbe4b0221aadf24410/images/5790e6dac6979160ca145f87/file-sI2HHz5cfy.png](../.gitbook/assets/0%20%285%29.png)

3. Then go to Store -&gt; Configure store -&gt; Payment methods -&gt; edit Unitpay and click the Edit button opposite the Enable payment method: Unitpay. In the DOMAIN field, insert the value of unitpay.money and copy the public and secret key from the Unitpay account in the PUBLIC KEY and SECRET KEY fields.

![https://d33v4339jhl8k0.cloudfront.net/docs/assets/551a91dbe4b0221aadf24410/images/5e68c38e2c7d3a7e9ae90120/file-ZT3pa1HeMz.png](../.gitbook/assets/1%20%2811%29.png)

4. Enter the payment handler in your Unitpay.ru account using the template: http://&lt;your\_site\_name&gt;/unitpay/callback&gt;/unitpay/callback

