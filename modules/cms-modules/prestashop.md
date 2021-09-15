# Prestashop

**The Module Setup and Installation Instruction**

{% hint style="success" %}
The module is supported in Prestashop versions 1.6 and 1.7
{% endhint %}

1. Download the [archive](https://github.com/unitpay/prestashop-module/archive/master.zip) with the module \(.zip\). Rename the "prestashop-module-master" folder to " unitpay"
2. Open the site control panel.
3. Click the Modules button in the left menu of the control panel, then the Add module button in the upper right corner. Select the downloaded module file and click Download this module.

![versions 1.6](../../.gitbook/assets/0%20%2814%29.png)

![versions 1.7](../../.gitbook/assets/izobrazhenie-20201126-091449%20%281%29%20%281%29.png)

4. After successful loading, type the word "unitpay" in the quick search bar and you will find the installed module.

![versions 1.6](../../.gitbook/assets/1%20%2834%29.png)

![versions 1.7](../../.gitbook/assets/izobrazhenie-20201126-103214%20%281%29%20%281%29.png)

5. Click on the green Install button located to the right of the module.

6. When installation is completed successfully, you will get to the module settings page. Here you need to enter the domain \(unitpay.ru\), secret key and public key, which you should take on the project page in your unitpay account. After entering them, click the Save button.

![](../../.gitbook/assets/2%20%285%29.png)

7. For correct operation of the module, you need to enable CNC. To do this, go to Settings-&gt; SEO-&gt; URLs and enable CNC.

![](../../.gitbook/assets/3%20%281%29.png)

8. We also recommend adding rounding of the cost of goods. Go to Settings - &gt; General settings and set the option " rounding Type = Rounding each item"

9. Go to the project page in your Unitpay account and enter the payment handler using the template [http://your\_site\_address/module/unitpay/callback](http://your_site_address/module/unitpay/callback)

![](../../.gitbook/assets/4%20%281%29.png)

