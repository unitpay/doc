# Interface Instructions

### Registration of Legal Entities \(LE\) 

Go to the registration form [https://unitpay.ru/signup/legal](https://unitpay.ru/en/signup/legal)

Enter TIN and e-mail \(a registration confirmation letter will be sent to it, it may fall into the "Spam" folder\). Set a password. Agree with the offers and click "Continue".

![](../.gitbook/assets/1%20%2843%29.png)

### Registration confirmation 

After that an email with registration confirmation will be sent to the specified email address \(may fall into the "Spam" folder\). Follow the link in the email to confirm registration.

![](../.gitbook/assets/image%20%2888%29.png)

### Adding a new project and confirmation

See the documentation for detailed video instructions. After confirming your registration, you will be prompted to add your first project.

You can add a website, a link to Instagram or a group in Vkontakte \(you must have the role of "owner" of this group\).

This will take you to the registration confirmation page. 

* For Instagram and Vkontakte, you will need to provide access to your page for confirmation. 
* You can confirm site ownership in several ways to choose from: through a txt file, a meta tag, or a TXT record.

![](../.gitbook/assets/image%20%2897%29.png)

### Project moderation 

After confirmation, your project will go through initial verification by the Unitpay support service. On the average time of check takes 10 minutes. [More about moderation. ](https://help.unitpay.ru/v/master/first_steps/moderation)  
As soon as moderation is passed, you will receive a notification in your personal Unitpay account, as well as an email.

### Setting up a project and accepting payments

After moderation, you can connect the acceptance of payments on your resource. There are several ways to do this in Unitpay: 

* Using ready modules for popular cms/saas-systems 
* Using [the SDK ](https://help.unitpay.ru/v/master/modules/unitpay-sdk)
* By [API ](https://help.unitpay.ru/v/master/payments/create-payment)
* You can also [generate a payment link](https://help.unitpay.ru/v/master/payments/payment-links) in your personal Unitpay account in the "Goods" section of your project \(to enable this function, contact support or your personal manager\). 

Don't forget to specify "Payment Processor" and the link to which the user will need to be redirected in case of a successful payment.

Don't forget to specify ["Payment Handler"](https://help.unitpay.ru/v/master/payments/payment-handler) and the link to which the user will be redirected if the payment is successful.

![](../.gitbook/assets/image%20%2893%29.png)

### Commissions and payment methods

After moderation, you can accept money through bank cards, mobile commerce, Samsung Pay, Apple Pay, Google Pay, and Qiwi. You can also connect payment through Paypal.

Note that acceptance of funds is open by default for certain countries.

### Countries

If you need to connect additional countries to accept payments in the project, first it must pass the final moderation. After that the "Countries" tab will appear in your project settings:

![](../.gitbook/assets/image%20%2896%29.png)

You need to choose which countries you want to connect to receive payments, attach supporting documents and send your application.

{% hint style="warning" %}
Application for connection of additional countries can be sent once a month, so it is recommended to attach the documents confirming the traffic to the application at once. This significantly increases the probability of their connection.
{% endhint %}

You will receive a notification after submitting your application:

If you sent the correct supporting documents, the application will be approved and the status in the "Countries" tab will change:

![](../.gitbook/assets/image%20%2881%29.png)

If the required traffic confirmations were not attached to the application, the application is likely to be rejected and the status in the "Countries" tab will change:

![](../.gitbook/assets/image%20%2889%29.png)

### Payouts

To open the payouts, you need to go to the "Payouts" tab and click "Agree and continue" \(note that you must have at least 1 project created, otherwise the payouts functionality will not open\).

![](../.gitbook/assets/image%20%2895%29.png)

Then you will get to the page with the data for the formation of questionnaires \(you will need to download and attach them in the next step\).

![](../.gitbook/assets/image%20%2890%29.png)

On the next tab "Documents" you need to send the founding documents for the contract. You need to select the necessary certified scans of the documents and attach them to the form \(scans do not need to be notarized, your signature and seal, if available, are sufficient\).

![](../.gitbook/assets/image%20%2884%29.png)

We send these documents and questionnaires to our vendors, who create individual accounts in their system, from which payments will be made. Payments are made automatically the next banking day.

### Online cash registers and "Unit.Reciepts"

After documents sending and approving of the project, the function of online cash registers will open for you. Go to the tab "Management" → "Online cash registers".   
The detailed manual on Unit.Reciepts connection can be found [**here**](https://help.unitpay.ru/v/master/online-cash-desk/unit.reciepts).   
If you already have your own online cash desk, you can connect it in the Unitpay interface. The system supports integration with Atol.Online, ModuleCash, E-COM cash register and Kit.Online.

You can read more information about connection and receipt formation [**in the documentation**](https://help.unitpay.ru/v/master/online-cash-desk/adding-online-cash-desk)**.**

### Reporting documents

Monthly closing documents are generated on the 5th working day of the month according to the production calendar. You can download them in the "Management" → "Reports" section.

In addition to monthly registers, daily registers for the previous day are generated for some transactions. The registers are sent to the email address to which the account is registered, you can disable this function by unchecking this checkbox and saving the changes:

![](../.gitbook/assets/image%20%2885%29.png)

You can also download these reports from your personal cabinet:

![](../.gitbook/assets/image%20%2892%29.png)

You can generate and download an archive with registers by setting a time period \(maximum - 31 days\), the default value is a period of 31 days to today's date inclusive. These operations will not be taken into account in the monthly Reports.

### Roles and employees 

You can add new employees through the "Management" → "Employees" tab and configure accesses to projects. 

Available role options: 

* Administrator \(your account\)
* Support \(view statistics only\) 
* Partner \(has the same rights as you do\) 
* Programmer \(view statistics and manage project settings\) 
* Manager \(view statistics and payments\) 
* Accountant \(view statistics and payouts\)

{% hint style="success" %}
When adding new employees to your account, we recommend using a one-time password via SMS. Two-factor authentication allows you to effectively protect your account from unauthorized logins, thereby protecting personal data - access to transaction history, project settings and financial information. Especially recommended when adding employees with the role of "Accountant" and "Partner".
{% endhint %}

