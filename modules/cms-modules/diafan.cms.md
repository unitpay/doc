# DIAFAN.CMS

### Инструкция по настройке и установке модуля.

{% hint style="info" %}
Модуль также можно скачать напрямую из [маркетплейса DIAFAN.CMS](https://addons.diafan.ru/modules/platezhi/priem-oplaty-cherez-unitpay647/).
{% endhint %}

1\. Скачайте [архив](https://github.com/unitpay/diafan-module/archive/master.zip) с модулем.

2\. Скопируйте содержимое директории "unitpay" из архива в корень вашего сайта.

3\. Перейдите в "Оплата"->"Методы оплаты" и добавьте новый метод оплаты, при выборе платежной системы укажите "Unitpay".

4\. Введите DOMAIN (unitpay.ru), PUBLIC KEY и SECRET KEY, которые вы можете взять в личном кабинете Unitpay.ru.

5\. В личном кабинете Unitpay.ru введите адрес обработчика платежей  [http://](http://diafan.app/payment/get/unitpay)<адрес вашего сайта>[/payment/get/unitpay](http://diafan.app/payment/get/unitpay)

![](https://d33v4339jhl8k0.cloudfront.net/docs/assets/551a91dbe4b0221aadf24410/images/583ffc2dc6979106d3738e1d/file-cDEUFxJ665.png)

{% hint style="info" %}
НДС выставляется внутри настроек модуля в поле "НДС": none (без НДС), vat0 (НДС 0%), vat10 (НДС 10%), vat20 (НДС 20%)
{% endhint %}

![](../../.gitbook/assets/izobrazhenie-20201127-080939.png)
