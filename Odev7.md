# SQL Odev 7

- film tablosunda bulunan filmleri rating değerlerine göre gruplayınız.

>SELECT rating, COUNT(*) as film_count FROM films GROUP BY rating;


- film tablosunda bulunan filmleri replacement_cost sütununa göre grupladığımızda film sayısı 50 den fazla olan replacement_cost değerini ve karşılık gelen film sayısını sıralayınız.

>SELECT replacement_cost, COUNT( * ) as film_count FROM films GROUP BY replacement_cost HAVING COUNT(*) > 50 ORDER BY film_count DESC;


-  customer tablosunda bulunan store_id değerlerine karşılık gelen müşteri sayılarını nelerdir?

>SELECT store_id, COUNT(*) as customer_count FROM customer GROUP BY store_id;


-  city tablosunda bulunan şehir verilerini country_id sütununa göre gruplandırdıktan sonra en fazla şehir sayısı barındıran country_id bilgisini ve şehir sayısını paylaşınız.

>SELECT country_id, COUNT(*) as city_count FROM city GROUP BY country_id ORDER BY city_count DESC LIMIT 1;
