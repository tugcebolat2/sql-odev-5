# sql-odev-5
--1)film tablosunda bulunan ve film ismi (başlık) 'n' karakteri ile biten en uzun (uzunluk) 5 film sıralayınız.
--2)film tablosunda bulunan ve film ismi (başlık) 'n' karakteri ile biten en kısa (uzunluk) ikinci(6,7,8,9,10) 5 filmi(6,7,8,9,10) sıralayınız.
--3)müşteri tablosunda bulunan last_name sütununa göre azalan yapılanma sıralamasında store_id 1 olmak sıralamayla ilk 4 veriyi sıralayınız.

1)

SELECT title,length FROM film WHERE title LIKE '%n' ORDER BY length LIMIT 5;

2)

SELECT title,length FROM film WHERE title LIKE '%n' ORDER BY length OFFSET 5 LIMIT 5;

3)

SELECT last_name FROM customer WHERE store_id=1 ORDER BY last_name DESC LIMIT 4;
