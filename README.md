1) Выберите из таблицы orders все заказы

SELECT * FROM orders;

2) Выберите из таблицы orders все заказы кроме новых. У новых заказов status равен "new". Использовать in

SELECT * FROM orders
WHERE STATUS IN ('cancelled', 'in_progress', 'delivery');

3) Выберите из таблицы orders все новые и отмененные заказы. У отмененных заказов status равен "cancelled". У новых заказов status равен "new".

SELECT * FROM orders
WHERE STATUS IN ('cancelled', 'new');

4) Выберите из таблицы orders все заказы содержащие более 3 товаров (products_count).
Вывести нужно только номер (id) и сумму (sum) заказа.

SELECT id, sum FROM orders
WHERE products_count > 3;
