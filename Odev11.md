# SQL Odev 11

- actor ve customer tablolarında bulunan first_name sütunları için tüm verileri sıralayalım.

>SELECT first_name FROM actor UNION SELECT first_name FROM customer;


- actor ve customer tablolarında bulunan first_name sütunları için kesişen verileri sıralayalım.

>SELECT first_name FROM actor INTERSECT SELECT first_name FROM customer;


-  actor ve customer tablolarında bulunan first_name sütunları için ilk tabloda bulunan ancak ikinci tabloda bulunmayan verileri sıralayalım.

>SELECT first_name FROM actor WHERE first_name NOT IN ( SELECT first_name FROM customer );


-  İlk 3 sorguyu tekrar eden veriler için de yapalım.

>SELECT first_name FROM actor UNION ALL SELECT first_name FROM customer;

>SELECT first_name FROM actor INTERSECT SELECT first_name FROM customer;

>SELECT first_name
FROM actor
WHERE first_name NOT IN (
    SELECT first_name
    FROM customer
)
UNION ALL
SELECT first_name
FROM customer
WHERE first_name NOT IN (
    SELECT first_name
    FROM actor
);
