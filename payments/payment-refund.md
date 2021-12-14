# Возврат платежа

{% swagger baseUrl="https://unitpay.ru/api?method=refundPayment" path="" method="get" summary="Возврат платежа" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="query" name="paymentMethod" type="string" %}
**Признак способа расчета:**

 full_prepayment - предоплата 100% 

\


prepayment - предоплата 

\


advance - аванс 

\


full_payment - полный расчет
{% endswagger-parameter %}

{% swagger-parameter in="query" name="sum" type="number" %}
Cумма возврата, если платежная система поддерживает не полный возврат (Не обязательный параметр). Если параметр не передан, будет произведен полный возврат
{% endswagger-parameter %}

{% swagger-parameter in="query" name="paymentId" type="number" %}
ID платежа в системе UnitPay

\


Например: 1234512345
{% endswagger-parameter %}

{% swagger-parameter in="query" name="secretKey" type="string" %}
Секретный ключ проекта, доступен в настройках проекта
{% endswagger-parameter %}

{% swagger-response status="200" description="" %}
```
{ 
    "result": {
        "message": "Возврат успешно произведен",
}}https://unitpay.ru/api?method=refundPayment&params[paymentId]=1234512345&params[secretKey]=x6bh0qbewehfppogkz6lufartkzyv7o0&params[sum]=100.00
```
{% endswagger-response %}
{% endswagger %}

Пример запроса к API для совершения возврата:

```
https://unitpay.ru/api?method=refundPayment&params[paymentId]=1234512345&params[secretKey]=x6bh0qbewehfppogkz6lufartkzyv7o0&params[sum]=100.00
```

{% hint style="danger" %}
По одному платежу вы можете сделать только один полный или частичный возврат.
{% endhint %}

{% hint style="warning" %}
Если вы подключили онлайн-кассу в ЛК, то для формирования чеков необходимо дополнительно передать [ряд параметров](../online-cash-register/receipt\_parameters.md)&#x20;
{% endhint %}

#### Успешный ответ

|             | Тип    | Описание                                                                                             |
| ----------- | ------ | ---------------------------------------------------------------------------------------------------- |
| **message** | string | Комментарий успешной операции можно использовать как подсказку пользователю после выполнения запроса |

#### Ошибочный ответ

|             | Тип    | Описание                              |
| ----------- | ------ | ------------------------------------- |
| **message** | string | Информация с описанием ошибки запроса |
