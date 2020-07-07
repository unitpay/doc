# Parameters for receipts

According to requirement 54-FZ, it is necessary to send receipts to the buyer and the Federal Tax Service of the Russian Federation. 

If you have connected an online cash desk then when creating a payment, you must send the following parameters:

|  | **Value** | **Description** |
| :--- | :--- | :--- |
| **customerEmail** | line | Payer's email |
| **customerPhone** | number | Payer's phone number in international format without "+" |
| **cashItems** | line | Order items: name - item name, count - quantity, price - price, type - item type from the table [Types of online cash register receipt items](../online-cash-desk/receipt-items.md), if not specified, then it is commodity.    The value of this parameter should be translated to json and encoded using base64. Format of the parameter items: base64\_encode\(json\_encode\(\[\["name" =&gt; "1 month hosting", "count" =&gt; 1, "price" =&gt; 10.00, "type" =&gt; "commodity"\]\]\)\); |

