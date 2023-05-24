# Домашнее задание к занятию "12.05 «Индексы»" - Евгений Шахов.
---
### Задание 1.
##### Напишите запрос к учебной базе данных, который вернёт процентное отношение общего размера всех индексов к общему размеру всех таблиц.
> ![image](https://github.com/126W/hw12.05/assets/122415129/c462a7d8-b8dc-44a1-b467-47bbc948ebd0)

---
### Задание 2.
##### Выполните explain analyze следующего запроса:
`select distinct concat(c.last_name, ' ', c.first_name), sum(p.amount) over (partition by c.customer_id, f.title)
from payment p, rental r, customer c, inventory i, film f
where date(p.payment_date) = '2005-07-30' and p.payment_date = r.rental_date and r.customer_id = c.customer_id and i.inventory_id = r.inventory_id`
##### перечислите узкие места; оптимизируйте запрос: внесите корректировки по использованию операторов, при необходимости добавьте индексы.
> ![image](https://github.com/126W/hw12.05/assets/122415129/bcd93e99-c038-4e8d-82c8-4bf412284906)

---
### Задание 3*. 
##### Самостоятельно изучите, какие типы индексов используются в PostgreSQL. Перечислите те индексы, которые используются в PostgreSQL, а в MySQL — нет. Приведите ответ в свободной форме.


---
