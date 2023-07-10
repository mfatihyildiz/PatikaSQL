# SQL Odev 6

- film tablosunda bulunan rental_rate sütunundaki değerlerin ortalaması nedir?

>SELECT AVG(rental_rate) AS rental_rate_avg FROM film;


- film tablosunda bulunan filmlerden kaç tanesi 'C' karakteri ile başlar?

>SELECT COUNT(*) AS count_c_starting_films FROM film WHERE title LIKE 'C%';


-  film tablosunda bulunan filmlerden rental_rate değeri 0.99 a eşit olan en uzun (length) film kaç dakikadır?

>SELECT length FROM films WHERE rental_rate = 0.99 ORDER BY length DESC LIMIT 1;


-  film tablosunda bulunan filmlerin uzunluğu 150 dakikadan büyük olanlarına ait kaç farklı replacement_cost değeri vardır?

>SELECT COUNT(DISTINCT replacement_cost) as unique_count FROM films WHERE length > 150;
