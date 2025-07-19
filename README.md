# Домашнее задание к занятию «Индексы»

## ` Дмитрий Климов `

## Задание 1

Напишите запрос к учебной базе данных, который вернёт процентное отношение общего размера всех индексов к общему размеру всех таблиц.

## Ответ:

<img width="1920" height="1080" alt="Снимок экрана (1168)" src="https://github.com/user-attachments/assets/0c830d31-4664-48d3-b93a-800e6edb9295" />


## Задание 2

Выполните explain analyze следующего запроса:

select distinct concat(c.last_name, ' ', c.first_name), sum(p.amount) over (partition by c.customer_id, f.title)
from payment p, rental r, customer c, inventory i, film f
where date(p.payment_date) = '2005-07-30' and p.payment_date = r.rental_date and r.customer_id = c.customer_id and i.inventory_id = r.inventory_id

## Ответ:

<img width="1920" height="1080" alt="Снимок экрана (1169)" src="https://github.com/user-attachments/assets/a82d8c64-773d-489c-9a91-9d857e9d411f" />

<img width="1920" height="1080" alt="Снимок экрана (1170)" src="https://github.com/user-attachments/assets/f39b40af-42c0-4dc2-a468-7db610fcb52e" />

<img width="1920" height="1080" alt="Снимок экрана (1171)" src="https://github.com/user-attachments/assets/8dd528f0-3267-494a-acfc-2ccdc5369f0e" />

<img width="1920" height="1080" alt="Снимок экрана (1172)" src="https://github.com/user-attachments/assets/2df57daf-36b7-4dd7-8d83-be1aacc12f20" />
