# Текущий баланс

Для взаимодействия с API рекомендуется использовать библиотеку [Unitpay PHP-SDK](https://github.com/unitpay/php-sdk)[https://unitpay.ru/api?](https://unitpay.ru/api?)   
     method=getPartner   
     params\[login\]=partner@gmail.com   
     params\[secretKey\]=ключ

|  | Значение | Описание |
| :--- | :--- | :--- |
| **login**  | строка | Email партнера в системе UnitPay |
| **secretKey** | строка | Секретный ключ партнера, доступен в [настройках профиля](https://unitpay.ru/partner/profile/edit) |

#### Успешный ответ

```text
{
    "result": {
        "email": "partner@gmail.com",
        "balance": "247.03",
        "balance_payout": "245.03"
    }
}
```

|  | Значение | Описание |
| :--- | :--- | :--- |
| **email**  | email | Email партнера в системе UnitPay |
| **balance** | число | Баланс партнера в рублях |
| **balance\_payout** | число | Баланс партнера, доступный для вывода, в рублях \(вводится с 15.06.21\) |

#### Ошибочный ответ

```text
{"error": {
    "message": "Неверный секретный ключ",
    "code": -32000
}}
```

|  | Описание |
| :--- | :--- |
| **-32000** | Ошибка авторизации |
| **-32602** | Ошибочные параметры запроса |
| **-32603** | Внутренняя техническая ошибка |

