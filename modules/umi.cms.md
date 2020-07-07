# UMI.CMS

**The Module Setup and Installation Instruction**

We advise to backup the database and the site before making the following operations.

1. Download the [archive](https://github.com/unitpay/umi-module/releases/download/1.0.1/umi-module-1.0.1.zip) with the module.

2. Copy the contents of the unitpay directory from the archive to the root of your site.

3. Open  http://&lt;your\_site\_address&gt;/unitpay.php&gt;/unitpay.php in your browser. You should see the word "Ready".

4. If everything is Ok with item 3, delete &lt;your site root&gt;/unitpay.php file.

5. Go to the admin panel of your site and move to Data templates, then select Unitpay in the payment methods and click Edit.

6. Click Add group in the opened window and create two fields there:

- with "Domain" name and "unitpay\_domain" ID,

- with "Public key" name and "public\_key" ID,

- with "Secret key" name and "secret\_key" ID,

![https://d33v4339jhl8k0.cloudfront.net/docs/assets/551a91dbe4b0221aadf24410/images/58121340c697915f88a393a3/file-oMZCf61KU1.png](../.gitbook/assets/0%20%2849%29.png)

7. Then click Save and Log out.

8. Go to the Online store menu in the Payment tab.

9. Select Unitpay in the Add method drop-down list.

10. In the opened window, enter the name of the payment method, the domain \(unitpay.money\), as well as the public and secret keys which you can find in your Unitpay.money account. Then click the Add button to save your changes.

![https://d33v4339jhl8k0.cloudfront.net/docs/assets/551a91dbe4b0221aadf24410/images/581213c4c697915f88a393ac/file-wrESbrNAZv.png](../.gitbook/assets/1%20%2821%29.png)

11. In your unitpay.money account, enter  http://&lt;your\_site\_name&gt;/&gt;/emarket/gateway in the payment handler field. Do not be afraid of Format Error message. Due to the implementation features, it is normal in this case.![https://d33v4339jhl8k0.cloudfront.net/docs/assets/551a91dbe4b0221aadf24410/images/5812118ac697915f88a3938b/file-ZP86eZKgB3.png](../.gitbook/assets/2%20%2818%29.png)

