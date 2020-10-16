# Получение информации по БИН

{% api-method method="get" host="" path="https://unitpay.money/api?method=getBinInfo&params\[bin\]=your\_bin&params\[secretKey\]=your\_account\_secret\_key&params\[login\]=your\_email" %}
{% api-method-summary %}
Get Cakes
{% endapi-method-summary %}

{% api-method-description %}
This endpoint allows you to get free cakes.
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="bin" type="string" required=true %}
БИН карты плательщика. Получить можно в обработчике платежа из get запроса с статусом платежа. БИН это первые 6 цифр параметра purse. 
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
Cake successfully retrieved.
{% endapi-method-response-example-description %}

```
{
    "result": {
        "bin": "553691",
        "countryCode": "RU",
        "brand": "MASTERCARD",
        "type": "CREDIT",
        "category": "WORLD",
        "bank": "TINKOFF BANK",
        "bankUrl": "",
        "bankPhone": ""
    }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



