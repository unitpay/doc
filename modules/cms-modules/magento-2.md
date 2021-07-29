# Magento 2

### Инструкция по настройке и установке модуля. <a id="instrukciya-po-nastroike-i-ustanovke-modulya"></a>

1.Скачать [архив модуля](https://github.com/unitpay/magento2/archive/main.zip) и загрузить в корень сайта.  


2. В консоли из корня сайта запустить команду php bin/magento setup:upgrade для установки модуля  


3. php bin/magento setup:di:compile для компиляции конфигурационных файлов  


4. Заходим в админ панель. Stores -&gt; Configuration

![](../../.gitbook/assets/image2.png)

5. В левом меню выбираем Sales -&gt; Payment Methods

![](../../.gitbook/assets/image7.png)

6. Находим модуль unitpay и задаем настройки Domain \(**unitpay.ru**\), Public Key, Secret Key \(можно взять в настройках проекта в личном кабинете Unitpay\)

![](../../.gitbook/assets/image6.png)

7. НДС можно задавать для каждого товара. Catalogs -&gt; Products, жмём на товар, выбираем ему Tax Class

![](../../.gitbook/assets/image1.png)

Tax Class настраивается в Stores -&gt; Tax Rules

![](../../.gitbook/assets/image5%20%281%29.png)

А зона действия в Stores -&gt; Tax Zones and Rates

![](../../.gitbook/assets/image3.png)

8. По умолчанию доставка действует на каждый товар \(3 товара = тройная стоимость доставки\). Чтобы это настроить, идём в Stores -&gt; Configuration . Потом в раскрывающимся списке Sales ищем Shipping methods

![](../../.gitbook/assets/image4%20%281%29.png)

9. Также доступно использование промокодов. Чтобы их настроить, идем во вкладку Marketing - Promotion - Cart Price Rules - Add new rule.

![](../../.gitbook/assets/image%20%2864%29.png)

1\) Rule name - название правила для промокода \(**не само наименование промокода**\);  
2\) Websites - зона применения \(можно установить для определенных разделов сайта;  
3\) Customer groups - группы пользователей, для которых открывается данный промокод;  
4\) Coupon - выбираем Specific coupon;  
5\) Uses per Customer - максимальное количество использований промокода для одного **авторизованного** покупателя;  
6\) Uses per Coupon - общее максимальное количество использований данного промокода;

Ниже открываем вкладку Actions и проставляем действия для промокода:

![](../../.gitbook/assets/image%20%2862%29.png)

Варианты промокодов:  
  
1. **Cкидка на всю корзину в %**  
Apply - Percent of product price discount, Discount Amount - размер скидки, %

2. **Скидка на всю корзину на определенную сумму**  
Apply - Fixed amount discount for whole cart, Discount Amount - размер скидки

3. **Скидка на каждый товар из корзины на определенную сумму**  
Apply - Fixed amount discount, Discount Amount - размер скидки  
_Примечание: скидка на товар должна быть меньше стоимости товара из каталога, иначе промокод сработает с ошибкой - нельзя пробивать товары с нулевой суммой._

4. Также для каждого промокода можно указать **бесплатную доставку**  
Free shipping - Select - For matching items only

