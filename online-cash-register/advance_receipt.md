# Чек прихода аванса

Если вы получили предоплату/аванс и оказали услугу/отправили товар, то необходимо пробить 2-ой чек - чек прихода предоплаты/аванса. 

Для этого отправьте запрос:

{% hint style="info" %}
Система не валидирует соответствие данных для чека прихода предоплаты и данных чека предоплаты. Будьте внимательны.
{% endhint %}

{% api-method method="get" host="" path="https://unitpay.money/api?method=offsetAdvance" %}
{% api-method-summary %}
offsetAdvance
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="login" type="string" required=true %}
email Партнера
{% endapi-method-parameter %}

{% api-method-parameter name="secretKey" type="string" required=true %}
секретный ключ Партнера
{% endapi-method-parameter %}

{% api-method-parameter name="paymentId" type="string" required=true %}
id платежа, по которому происходит зачет аванса. У платежа обязательно должны быть cashItems со способами расчёта “аванс“, “предоплата“, "предоплата 100%"
{% endapi-method-parameter %}

{% api-method-parameter name="cashitems" type="string" required=false %}
Обязателен, если по платежу уже были произведены зачеты аванса. Если cashItems не передан, происходит зачет аванса всего платежа
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
  "result": {
    "message": "Запрос на создание чека сформирован и отправлен в ОФД"
  }
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



