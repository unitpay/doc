# Creating a Payout

To interact with the API, use the [Unitpay PHP-SDK](https://github.com/unitpay/php-sdk) library

![](../.gitbook/assets/image%20%2832%29.png)

  


**Required parameters:**

|  | **Value** | **Description** |
| :--- | :--- | :--- |
| **login** | line | Partner's email in the UnitPay system |
| **secretKey** | line | Partner's secret key, available in the [profile settings](https://unitpay.money/partner/profile/edit) |
| **purse** | line | Payee's purse in the format accepted in the payment system |
| **transactionId** | text | Unique payout ID on the partner's side |
| **sum** | number | The transfer amount in rubles, for example: "10.22" |
| **paymentType** | line | [Payment system code](../book-of-reference/payment-system-codes.md):  Supported: qiwi, card, webmoney, mc, yandex  |

**Additional parameters:**

\*\*\*\*

|  | **Value** | **Description** |
| :--- | :--- | :--- |
| **projectId** | number | Unique project ID in the UnitPay system   |

**IMPORTANT NOTE**: always use a unique **transactionId** for new payouts; when you get an existing **transactionId** \(regardless of other parameters\), the current payout status is returned

You can run the query in test mode. [Learn more](../book-of-reference/test-api.md)

**Successful response**

![](../.gitbook/assets/image%20%2826%29.png)



|  | **Value** | **Description** |
| :--- | :--- | :--- |
| **message** | line | The comment of a successful transaction can be used as a hint to the user after completing the request |
| **status** | line | success — successful payout   not\_completed — the payout has been sent to the payment system but no confirmation has been received yet \(temporary status\) |
| **payoutId** | number | Unique payout ID in the UnitPay system |
| **partnerBalance** | number | Partner's balance in the system available for payments |
| **createDate** | text | Payout creation date |
| **completeDate** | text | Payout completion date |
| **sum** | number | Amount of payout |
| **payoutCommission** | number | Payout commission |
| **partnerCommission** | number | Partner commission  |

**Error response**

![](../.gitbook/assets/image%20%2817%29.png)



|  | **Value** | **Description** |
| :--- | :--- | :--- |
| **message** | line | Information with a description of the request error |
| **code** | line | Error code, see detailed explanation in the table below |

  


**Errors:**

|  | **Description** |
| :--- | :--- |
| **100** | Mass payment service is disabled |
| **101** | Mass payment service is not available for you |
| **102** | The minimum amount of a single payment should be more than 1 ruble |
| **103** | The payout amount should be less than or equal to the current balance |
| **104** | The phone number is not included in the list of countries available for payouts |
| **1051** | We could not get information about the payee's purse. Check the purse number and try to repeat the transaction again or after a while |
| **1052** | We could not get information about the card number. Check the card number and try to repeat the transaction again or after a while |
| **1053** | We could not get information about the phone number. Check the phone number and try to repeat the transaction again or after a while |
| **201** | We could not transfer funds to the account you specified   This may be due to the restrictions on the payee's account or errors on the payment system platform   Please contact our customer support for more information or repeat the request later |

  


**Technical errors:**

|  | **Description** |
| :--- | :--- |
| **-32000** | Authorization error |
| **-32602** | Invalid request parameters |
| **-32603** | Internal technical error |

