# Домашнее задание к занятию «Индексы» - `Станик Александр`

### Задание 1
explain analyze
select distinct concat(c.last_name, ' ', c.first_name), sum(p.amount) over (partition by c.customer_id, f.title)
from payment p, rental r, customer c, inventory i, film f
where date(p.payment_date) = '2005-07-30' and p.payment_date = r.rental_date and r.customer_id = c.customer_id and i.inventory_id = r.inventory_id

![image](https://github.com/user-attachments/assets/c31f4e22-4711-453a-a5fe-6c14fc27539b)

### Задание 2
explain analyze
select distinct 
    concat(c.last_name, ' ', c.first_name) as customer_name,
    sum(p.amount) over (partition by c.customer_id) as total_amount
from payment p
join rental r on p.payment_date = r.rental_date
join customer c on r.customer_id = c.customer_id
join inventory i on r.inventory_id = i.inventory_id
join film f on i.film_id = f.film_id
where p.payment_date >= '2005-07-30' and p.payment_date < '2005-07-31';

![image](https://github.com/user-attachments/assets/7fbd8f2f-37e5-4597-ae61-b58a1c278503)

