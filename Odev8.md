# SQL Odev 8

- test veritabanınızda employee isimli sütun bilgileri id(INTEGER), name VARCHAR(50), birthday DATE, email VARCHAR(100) olan bir tablo oluşturalım.

>CREATE TABLE employee (
    id INTEGER,
    name VARCHAR(50),
    birthday DATE,
    email VARCHAR(100)
);


- Oluşturduğumuz employee tablosuna 'Mockaroo' servisini kullanarak 50 adet veri ekleyelim.

>INSERT INTO employee (id, name, birthday, email) VALUES (1, 'John Doe', '1990-05-15', 'john.doe@example.com');


-  Sütunların her birine göre diğer sütunları güncelleyecek 5 adet UPDATE işlemi yapalım.

>UPDATE employee SET name = 'Jane Smith' WHERE id = 1;

>UPDATE employee SET birthday = '1992-08-25' WHERE id = 2;

>UPDATE employee SET email = 'jane.smith@example.com' WHERE id = 3;

>UPDATE employee SET name = 'Michael Brown', birthday = '1985-11-10' WHERE id = 4;

>UPDATE employee SET name = 'Emily Johnson', birthday = '1998-03-22', email = 'emily.johnson@example.com' WHERE id = 5;


-  Sütunların her birine göre ilgili satırı silecek 5 adet DELETE işlemi yapalım.

>DELETE FROM employee WHERE name = 'Jane Smith';
>DELETE FROM employee WHERE birthday = '1992-08-25';
>DELETE FROM employee WHERE email = 'jane.smith@example.com';
>DELETE FROM employee WHERE name = 'Michael Brown' AND birthday = '1985-11-10';
>DELETE FROM employee WHERE name = 'Emily Johnson' AND birthday = '1998-03-22' AND email = 'emily.johnson@example.com';
