# Параметры для формирования чека

Чтобы сформировать чек требуется в [запросе на создание платежа](../payments/create-payment.md) указать дополнительные параметры:

<table>
  <thead>
    <tr>
      <th style="text-align:left"></th>
      <th style="text-align:left">&#x422;&#x438;&#x43F;</th>
      <th style="text-align:left">&#x41E;&#x43F;&#x438;&#x441;&#x430;&#x43D;&#x438;&#x435;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left"><b>customerEmail</b>
      </td>
      <td style="text-align:left">&#x441;&#x442;&#x440;&#x43E;&#x43A;&#x430;</td>
      <td style="text-align:left">Email &#x43F;&#x43B;&#x430;&#x442;&#x435;&#x43B;&#x44C;&#x449;&#x438;&#x43A;&#x430;</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>customerPhone</b>
      </td>
      <td style="text-align:left">&#x447;&#x438;&#x441;&#x43B;&#x43E;</td>
      <td style="text-align:left">&#x422;&#x435;&#x43B;&#x435;&#x444;&#x43E;&#x43D; &#x43F;&#x43B;&#x430;&#x442;&#x435;&#x43B;&#x44C;&#x449;&#x438;&#x43A;&#x430;
        &#x432; &#x43C;&#x435;&#x436;&#x434;&#x443;&#x43D;&#x430;&#x440;&#x43E;&#x434;&#x43D;&#x43E;&#x43C;
        &#x444;&#x43E;&#x440;&#x43C;&#x430;&#x442;&#x435; &#x431;&#x435;&#x437;
        &quot;+&quot;</td>
    </tr>
    <tr>
      <td style="text-align:left"><b>cashItems</b>
      </td>
      <td style="text-align:left">&#x441;&#x442;&#x440;&#x43E;&#x43A;&#x430;</td>
      <td style="text-align:left">
        <p><b>&#x41F;&#x43E;&#x437;&#x438;&#x446;&#x438;&#x438; &#x437;&#x430;&#x43A;&#x430;&#x437;&#x430;</b>
          <br
          />
          <br />&#x41F;&#x43E;&#x43B;&#x443;&#x447;&#x430;&#x435;&#x442;&#x441;&#x44F;
          &#x43F;&#x443;&#x442;&#x435;&#x43C; &#x43A;&#x43E;&#x434;&#x438;&#x440;&#x43E;&#x432;&#x430;&#x43D;&#x438;&#x44F;
          base64 &#x437;&#x43D;&#x430;&#x447;&#x435;&#x43D;&#x438;&#x44F; &#x432;
          &#x444;&#x43E;&#x440;&#x43C;&#x430;&#x442;&#x435; json. &#x41D;&#x430;&#x43F;&#x440;&#x438;&#x43C;&#x435;&#x440;:</p>
        <p><code>base64_encode(json_encode([[&quot;name&quot; =&gt; &quot;&#x425;&#x43E;&#x441;&#x442;&#x438;&#x43D;&#x433; &#x43D;&#x430; 1 &#x43C;&#x435;&#x441;&#x44F;&#x446;&quot;, &quot;count&quot; =&gt; 1, &quot;price&quot; =&gt; 10.00, &quot;type&quot; =&gt; &quot;commodity&quot;]])); </code>
        </p>
      </td>
    </tr>
  </tbody>
</table>

{% hint style="info" %}
Для формирования чека [возврата](../payments/payment-refund.md) достаточно передать **cashItems. CustomerEmail** или **customerPhone** не требуются
{% endhint %}

{% hint style="warning" %}
С 1.02.2021 года в кассовом чеке нужно **обязательно указывать корректно номенклатуру** \(наименование, количество, цену\) за товары/услуги в cashItems. 
{% endhint %}

**Параметр cashItems формируется из:**

<table>
  <thead>
    <tr>
      <th style="text-align:left"></th>
      <th style="text-align:left"><b>&#x422;&#x438;&#x43F;</b>
      </th>
      <th style="text-align:left">&#x41E;&#x43F;&#x438;&#x441;&#x430;&#x43D;&#x438;&#x435;</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td style="text-align:left">name</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x41D;&#x430;&#x437;&#x432;&#x430;&#x43D;&#x438;&#x435; &#x43F;&#x43E;&#x437;&#x438;&#x446;&#x438;&#x438;</td>
    </tr>
    <tr>
      <td style="text-align:left">count</td>
      <td style="text-align:left">number</td>
      <td style="text-align:left">&#x41A;&#x43E;&#x43B;&#x438;&#x447;&#x435;&#x441;&#x442;&#x432;&#x43E;</td>
    </tr>
    <tr>
      <td style="text-align:left">price</td>
      <td style="text-align:left">number</td>
      <td style="text-align:left">&#x426;&#x435;&#x43D;&#x430; &#x437;&#x430; &#x435;&#x434;&#x438;&#x43D;&#x438;&#x446;&#x443;
        &#x442;&#x43E;&#x432;&#x430;&#x440;&#x430;</td>
    </tr>
    <tr>
      <td style="text-align:left">currency</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x41F;&#x43E; &#x443;&#x43C;&#x43E;&#x43B;&#x447;&#x430;&#x43D;&#x438;&#x44E;
        &#x432;&#x441;&#x435;&#x433;&#x434;&#x430; RUB (&#x435;&#x441;&#x43B;&#x438;
        &#x432;&#x430;&#x448;&#x438; &#x442;&#x43E;&#x432;&#x430;&#x440;&#x44B;/&#x443;&#x441;&#x43B;&#x443;&#x433;&#x438;
        &#x432; &#x440;&#x443;&#x431;&#x43B;&#x44F;&#x445;, &#x442;&#x43E; currency
        &#x43E;&#x442;&#x434;&#x435;&#x43B;&#x44C;&#x43D;&#x43E; &#x43C;&#x43E;&#x436;&#x43D;&#x43E;
        &#x43D;&#x435; &#x43F;&#x435;&#x440;&#x435;&#x434;&#x430;&#x432;&#x430;&#x442;&#x44C;).
        &#x412;&#x430;&#x43B;&#x44E;&#x442;&#x430; &#x437;&#x430;&#x43A;&#x430;&#x437;&#x430;
        &#x43F;&#x43E; &#x441;&#x442;&#x430;&#x43D;&#x434;&#x430;&#x440;&#x442;&#x443;
        ISO 4217 (UAH, BYN, EUR, USD &#x438;&#x442;&#x434;. <a href="../book-of-reference/currency-codes.md">&#x41F;&#x43E;&#x43B;&#x43D;&#x44B;&#x439; &#x441;&#x43F;&#x438;&#x441;&#x43E;&#x43A; &#x432;&#x430;&#x43B;&#x44E;&#x442;</a>).
        <br
        />&#x412; &#x447;&#x435;&#x43A;&#x435; &#x443; &#x43F;&#x43E;&#x43B;&#x44C;&#x437;&#x43E;&#x432;&#x430;&#x442;&#x435;&#x43B;&#x44F;
        &#x432;&#x441;&#x435;&#x433;&#x434;&#x430; &#x431;&#x443;&#x434;&#x443;&#x442;
        &#x440;&#x443;&#x431;&#x43B;&#x438;, &#x434;&#x430;&#x436;&#x435; &#x435;&#x441;&#x43B;&#x438;
        &#x432;&#x44B; &#x43F;&#x435;&#x440;&#x435;&#x434;&#x430;&#x43B;&#x438;
        &#x432;&#x430;&#x43B;&#x44E;&#x442;&#x443;, &#x43E;&#x442;&#x43B;&#x438;&#x447;&#x43D;&#x443;&#x44E;
        &#x43E;&#x442; RUB (&#x43A;&#x43E;&#x43D;&#x432;&#x435;&#x440;&#x442;&#x430;&#x446;&#x438;&#x44F;
        &#x43F;&#x440;&#x43E;&#x438;&#x441;&#x445;&#x43E;&#x434;&#x438;&#x442;
        &#x43D;&#x430; &#x441;&#x442;&#x43E;&#x440;&#x43E;&#x43D;&#x435; Unitpay).</td>
    </tr>
    <tr>
      <td style="text-align:left">nds</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">
        <p><b>&#x420;&#x430;&#x437;&#x43C;&#x435;&#x440; &#x441;&#x442;&#x430;&#x432;&#x43A;&#x438; &#x41D;&#x414;&#x421;: </b>
        </p>
        <p>none</p>
        <p>vat0</p>
        <p>vat10</p>
        <p>vat20</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">type</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">
        <p><b>&#x422;&#x438;&#x43F; &#x43F;&#x43E;&#x437;&#x438;&#x446;&#x438;&#x438;:</b> 
        </p>
        <p>commodity - &#x442;&#x43E;&#x432;&#x430;&#x440; (<em>&#x418;&#x441;&#x43F;&#x43E;&#x43B;&#x44C;&#x437;&#x443;&#x435;&#x442;&#x441;&#x44F; &#x43F;&#x43E; &#x443;&#x43C;&#x43E;&#x43B;&#x447;&#x430;&#x43D;&#x438;&#x44E;)</em>
        </p>
        <p>excise - &#x43F;&#x43E;&#x434;&#x430;&#x43A;&#x446;&#x438;&#x437;&#x43D;&#x44B;&#x439;
          &#x442;&#x43E;&#x432;&#x430;&#x440;</p>
        <p>job - &#x440;&#x430;&#x431;&#x43E;&#x442;&#x430;</p>
        <p>service - &#x443;&#x441;&#x43B;&#x443;&#x433;&#x430;</p>
        <p>lottery_prize - &#x432;&#x44B;&#x43F;&#x43B;&#x430;&#x442;&#x430; &#x432;&#x44B;&#x438;&#x433;&#x440;&#x44B;&#x448;&#x430;
          &#x43B;&#x43E;&#x442;&#x435;&#x440;&#x435;&#x439;&#x43D;&#x43E;&#x433;&#x43E;
          &#x431;&#x438;&#x43B;&#x435;&#x442;&#x430;</p>
        <p>intellectual_activity - &#x438;&#x43D;&#x442;&#x435;&#x43B;&#x43B;&#x435;&#x43A;&#x442;&#x443;&#x430;&#x43B;&#x44C;&#x43D;&#x430;&#x44F;
          &#x434;&#x435;&#x44F;&#x442;&#x435;&#x43B;&#x44C;&#x43D;&#x43E;&#x441;&#x442;&#x44C;</p>
        <p>payment - &#x43F;&#x43B;&#x430;&#x442;&#x435;&#x436;</p>
        <p>agent_commission - &#x430;&#x433;&#x435;&#x43D;&#x442;&#x441;&#x43A;&#x430;&#x44F;
          &#x43A;&#x43E;&#x43C;&#x438;&#x441;&#x441;&#x438;&#x44F;</p>
        <p>another - &#x434;&#x440;&#x443;&#x433;&#x43E;&#x439;</p>
        <p>property_right - &#x438;&#x43C;&#x443;&#x449;&#x435;&#x441;&#x442;&#x432;&#x435;&#x43D;&#x43D;&#x44B;&#x435;
          &#x43F;&#x440;&#x430;&#x432;&#x430;</p>
        <p>non-operating_gain - &#x432;&#x43D;&#x435;&#x446;&#x435;&#x43D;&#x442;&#x440;&#x430;&#x43B;&#x438;&#x437;&#x43E;&#x432;&#x430;&#x43D;&#x43D;&#x44B;&#x439;
          &#x434;&#x43E;&#x445;&#x43E;&#x434; insurance_premium - &#x441;&#x442;&#x440;&#x430;&#x445;&#x43E;&#x432;&#x430;&#x43D;&#x438;&#x435;</p>
        <p>sales_tax - &#x43D;&#x430;&#x43B;&#x43E;&#x433; &#x441; &#x43F;&#x440;&#x43E;&#x434;&#x430;&#x436;</p>
        <p>resort_fee - &#x43A;&#x443;&#x440;&#x43E;&#x440;&#x442;&#x43D;&#x44B;&#x439;
          &#x441;&#x431;&#x43E;&#x440;</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">paymentMethod</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">
        <p><b>&#x41F;&#x440;&#x438;&#x437;&#x43D;&#x430;&#x43A; &#x441;&#x43F;&#x43E;&#x441;&#x43E;&#x431;&#x430; &#x440;&#x430;&#x441;&#x447;&#x435;&#x442;&#x430;:</b>
        </p>
        <p>full_payment - &#x43F;&#x43E;&#x43B;&#x43D;&#x44B;&#x439; &#x440;&#x430;&#x441;&#x447;&#x435;&#x442;
          (<em>&#x418;&#x441;&#x43F;&#x43E;&#x43B;&#x44C;&#x437;&#x443;&#x435;&#x442;&#x441;&#x44F; &#x43F;&#x43E; &#x443;&#x43C;&#x43E;&#x43B;&#x447;&#x430;&#x43D;&#x438;&#x44E;)</em>
        </p>
        <p>full_prepayment - &#x43F;&#x440;&#x435;&#x434;&#x43E;&#x43F;&#x43B;&#x430;&#x442;&#x430;
          100%</p>
        <p>prepayment - &#x43F;&#x440;&#x435;&#x434;&#x43E;&#x43F;&#x43B;&#x430;&#x442;&#x430;</p>
        <p>advance - &#x430;&#x432;&#x430;&#x43D;&#x441;</p>
      </td>
    </tr>
    <tr>
      <td style="text-align:left">nomenclatureCode</td>
      <td style="text-align:left">string</td>
      <td style="text-align:left">&#x41A;&#x43E;&#x434; &#x43C;&#x430;&#x440;&#x43A;&#x438;&#x440;&#x43E;&#x432;&#x43A;&#x438;
        &#x442;&#x43E;&#x432;&#x430;&#x440;&#x430; &#x432; &#x448;&#x435;&#x441;&#x442;&#x43D;&#x430;&#x434;&#x446;&#x430;&#x442;&#x435;&#x440;&#x438;&#x447;&#x43D;&#x43E;&#x43C;
        &#x43F;&#x440;&#x435;&#x434;&#x441;&#x442;&#x430;&#x432;&#x43B;&#x435;&#x43D;&#x438;&#x438;
        &#x441; &#x43F;&#x440;&#x43E;&#x431;&#x435;&#x43B;&#x430;&#x43C;&#x438;.
        &#x41C;&#x430;&#x43A;&#x441;&#x438;&#x43C;&#x430;&#x43B;&#x44C;&#x43D;&#x430;&#x44F;
        &#x434;&#x43B;&#x438;&#x43D;&#x430; &#x2013; 32 &#x431;&#x430;&#x439;&#x442;&#x430;.
        &#x41C;&#x430;&#x440;&#x43A;&#x438;&#x440;&#x43E;&#x432;&#x43A;&#x430;
        &#x440;&#x430;&#x431;&#x43E;&#x442;&#x430;&#x435;&#x442; &#x442;&#x43E;&#x43B;&#x44C;&#x43A;&#x43E;
        &#x434;&#x43B;&#x44F; <b>&#xAB;&#x42E;&#x43D;&#x438;&#x442;.&#x427;&#x435;&#x43A;&#x43E;&#x432;&#xBB;.</b>
      </td>
    </tr>
  </tbody>
</table>

