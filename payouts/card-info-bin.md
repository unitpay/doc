# Card Information by BIN

To get it from the API, we recommend using the [Unitpay PHP-SDK](https://github.com/unitpay/php-sdk) library.

![](../.gitbook/assets/image%20%2824%29.png)



|  | **Value** | **Description** |
| :--- | :--- | :--- |
| **login** | line | Partner's email in the UnitPay system |
| **secretKey** | line | Partner's secret key, available in the [profile settings](https://unitpay.money/partner/profile/edit) |
| **bin** | number | First 6 digits of the card number |

  


**Successful response**

![](../.gitbook/assets/image%20%2834%29.png)



|  | **Value** | **Description** |
| :--- | :--- | :--- |
| **bin** | line | First 6 digits of the card number |
| **bank** | line | Name of the bank where the card was issued |
| **countryCode** | line | Country code in Alpha-2 format \(ISO 3166-1\) |
| **brand** | line | Name of the international system which the card is served in. |
| **category** | line | Card category |
| **type** | line | Card type |
| **bankUrl** | line | Bank Url |
| **bankPhone** | line | Bank phone number |

  


**Error response**

![](../.gitbook/assets/image%20%288%29.png)



|  | **Value** | **Description** |
| :--- | :--- | :--- |
| **message** | line | Information with a description of the request error |
| **code** | line | Error code, see detailed explanation in the table below |

  


**Errors:**

|  | **Description** |
| :--- | :--- |
| **100** | No matches were found for your query |



**Technical errors:**

|  | **Description** |
| :--- | :--- |
| **-32000** | Authorization error |
| **-32602** | Invalid request parameters |
| **-32603** | Internal technical error |

