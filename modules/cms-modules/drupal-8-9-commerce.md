# Drupal 8, 9 \(commerce\)

**Instructions for configuring and installing the module.**

{% hint style="info" %}
The module supports working with version 8 and 9 of Drupal \(commerce\)
{% endhint %}

1. Download the [archive with the module](https://github.com/unitpay/drupal/archive/main.zip).

2. install the module. to do this, go to extend - &gt; install new module. Select the archive with the module and then "Save".

![](../../.gitbook/assets/d_ustanovka%20%281%29%20%281%29.png)

3. Go To commerce - &gt; Configuration -&gt; Payment gateway. PAYMENT GATEWAY: "Unitpay" click "edit".In the DOMAIN field, INSERT the value unitpay.ru, in thePUBLIC KEY  and SECRET KEY , copy the public and secret key from the unitpay personal account.

![](../../.gitbook/assets/8-nastroiki1.png)

4. Enable the module and save it.

![](../../.gitbook/assets/8-nastroiki2.png)

5. in your unitpay dashboard, add the address of the handler in the format http://&lt;name of your site&gt;/commerce-unitpay/callback

![](../../.gitbook/assets/213514da544a8913f88105cb2135f9ae.png)

6. VAT is set inside the module settings Commerce -&gt; Configuration -&gt; Payment gateway

![](../../.gitbook/assets/6e56d9874bd24b7521520cac32b1d278.png)

7. the currency is set in two places. Commerce -&gt; Configuration -&gt; Currencies

![](../../.gitbook/assets/6a75171b61038834536fdc4987f3386b.png)

8. and then, to be able to change in products, you need to add to "Product types". Commerce -&gt; Configuration -&gt; Product types -&gt; Edit Default -&gt; Manage fields

![](../../.gitbook/assets/1111.png)

![](../../.gitbook/assets/222.png)

![](../../.gitbook/assets/3333.png)

![](../../.gitbook/assets/4444.png)

9. Similarly, you need to do for "variation types". Commerce -&gt; Configuration -&gt; Product variation types -&gt; Edit Default -&gt; Manage fields



