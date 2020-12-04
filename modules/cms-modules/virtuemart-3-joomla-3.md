# VirtueMart 3 \(joomla 3\)

**The Module Setup and Installation Instruction**

1. Download the [archive](https://github.com/unitpay/virtuemart-module/archive/master.zip) with the module. The module was tested on VirtueMart 3 with Joomla 3.5.1
2. Go to the site admin panel.
3. Install the module. To do this, go to Extensions-&gt;Extension manager-&gt;Install. Then click on the Select file button and after selecting it, click Upload & Install.

![](../../.gitbook/assets/0%20%2846%29.png)

4. Next, in the top menu, go to VirtueMart -&gt; Payment methods

![](../../.gitbook/assets/1%20%281%29.png)

5. Click the Create button and enter the required information such as the name of the payment method, etc. Select Unitpay in the payment method list. Then click Save.

![](../../.gitbook/assets/2%20%2817%29.png)

6. After that go to the Configuration tab of this module settings and enter the value of unitpay.money in the DOMAIN field. You can find PUBLIC KEY and SECRET KEY fields in your personal account on the Unitpay.money website, then click the Save button.

![](../../.gitbook/assets/3%20%287%29.png)

7. Enter the payment handler in your Unitpay.ru account using the template [http://&lt;your](http://<your) site name&gt;/index.php?option=com\_virtuemart&view=pluginresponse&task=pluginnotification&tmpl=component&format=json

![](../../.gitbook/assets/4%20%282%29.png)

