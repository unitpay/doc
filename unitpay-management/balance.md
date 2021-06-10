# Current Balance

To interact with the API, we recommend using the [Unitpay PHP-SDK](https://github.com/unitpay/php-sdk) library:

[https://unitpay.ru/api?](https://unitpay.ru/api?)   
     method=getPartner   
     params\[login\]=partner@gmail.com   
     params\[secretKey\]=ключ

|  | **Value** | **Description** |
| :--- | :--- | :--- |
| **login** | line | Partner's email in the UnitPay system |
| **secretKey** | line | Partner's secret key, available in the [profile settings](https://unitpay.money/partner/profile/edit) |

**Successful response**

```text
{
    "result": {
        "email": "partner@gmail.com",
        "balance": "247.03",
        "balance_payout": "245.03"
    }
}
```

|  | **Value** | **Description** |
| :--- | :--- | :--- |
| **email** | email | Partner's email in the UnitPay system |
| **balance** | number | Partner's balance in rubles |
| **balance\_payout** | number | Partner's balance**,** available for withdrawal, in rubles \(will be actual since 15.06.2021\) |

**Error response**

```text
{"error": {
    "message": "Неверный секретный ключ",
    "code": -32000
}}
```

|  | **Description** |
| :--- | :--- |
| **-32000** | Authorization error |
| **-32602** | Invalid request parameters |
| **-32603** | Internal technical error |

