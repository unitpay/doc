# Базовый \(для онлайн игр\)

Подходит для большинства проектов. Для установки достаточно [скачать модуль](https://github.com/unitpay/base_module) и следовать инструкциям из файла readme.txt.

**Шаг 1.** Создайте в БД таблицу unitpay\_payments:

```text
1CREATE TABLE IF NOT EXISTS `unitpay_payments` (2  `id` int(10) NOT NULL AUTO_INCREMENT,3  `unitpayId` varchar(255) NOT NULL,4  `account` varchar(255) NOT NULL,5  `sum` float NOT NULL,6  `itemsCount` int(11) NOT NULL DEFAULT '1',7  `dateCreate` datetime NOT NULL,8  `dateComplete` datetime DEFAULT NULL,9  `status` tinyint(4) NOT NULL DEFAULT '0',10  PRIMARY KEY (`id`)11) ENGINE=InnoDB  DEFAULT CHARSET=utf8 AUTO_INCREMENT=1;12
```

В таблицу unitpay\_payments будет логироваться информация о проводимых платежах

**Шаг 2.** Разместите скрипты в произвольной директории веб-сервера, в которую есть доступ из интернета. Убедитесь, что на сервере установлен php версии 5.x.x или выше, а также доступно расширение mysqli \(для работы с БД mysql\).

**Шаг 3.** Укажите в config.php параметры соединения с БД, стоимость одной единицы товара \(предмета\), секретный ключ \(его можно найти в настройках проекта в личном кабинете unitpay.ru\), а также таблицу с пользователями и поле в этой таблице, которое необходимо обновить после оплаты.

**Шаг 4.** В личном кабинете unitpay.ru, в настройках проекта укажите адрес обработчика. В данном случае это абсолютный URL, по которому доступен index.php текущего модуля.

