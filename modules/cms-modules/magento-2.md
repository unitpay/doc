# Magento 2

### Instructions for configuring and installing the module. <a id="instrukciya-po-nastroike-i-ustanovke-modulya"></a>

1.Download the [module archive](https://github.com/unitpay/magento2/archive/main.zip) and upload it to the site root.  


2. In the shell from the site root to run the command php bin/magento setup:upgrade to install module  


3. php bin/magento setup:di:compile for compiling configuration files  


4. Go to the admin panel. Stores -&gt; Configuration

![](../../.gitbook/assets/image2.png)

5. In the left menu, select Sales -&gt; Payment Methods

![](../../.gitbook/assets/image7.png)

6. Find the unitpay module and set the settings Domain \(**unitpay.ru**\), Public Key, Secret Key \(you can take it in the project settings in your personal account Unitpay\)

![](../../.gitbook/assets/image6.png)

7. VAT can be set for each product. Catalogs -&gt; Products, click on the product, choose it Tax Class

![](../../.gitbook/assets/image1.png)

Tax Class is configured in Stores -&gt; Tax Rules

![](../../.gitbook/assets/image5%20%281%29.png)

Coverage area in Stores -&gt; Tax Zones and Rates

![](../../.gitbook/assets/image3.png)

8. By default, delivery is valid for each product \(3 products = triple the cost of delivery\). To configure this, go to Stores -&gt; Configuration.Then in the sales drop down list Sales we look for Shipping methods

![](../../.gitbook/assets/image4%20%281%29.png)

9. Promotional codes are also available. To set them up, go to the Marketing - Promotion - Cart Price Rules - Add new rule.

![](../../.gitbook/assets/image%20%2864%29.png)

1\) Rule name - **it's not the name of the promocode**;  
2\) Websites - using zone \(can be set for certain sections of the site\);  
3\) Customer groups - user groups for which this promo code is opened;  
4\) Coupon - choose Specific coupon;  
5\) Uses per Customer - the maximum number of promocode's uses for one authorized customer;  
6\) Uses per Coupon - the total maximum number of this promocode's uses;

Then open the Actions tab and set the actions for the promocode:

![](../../.gitbook/assets/image%20%2862%29.png)

Promocodes' options:

1. **Discount for the whole cart in %**

   Apply - Percent of product price discount, Discount Amount - discount amount,%

2. **Discount for the whole cart for a certain amount**

   Apply - Fixed amount discount for whole cart, Discount Amount - discount amount

3. **Discount for each item from the cart for a certain amount**

   Apply - Fixed amount discount, Discount Amount - discount amount

   Note: the discount on the item must be less than the cost of the product from the catalog, otherwise the promocode will work with an error - you cannot provide products with a zero amount.

4. Also, for each promo code, you can specify **free shipping**

   Free shipping - Select - For matching items only

