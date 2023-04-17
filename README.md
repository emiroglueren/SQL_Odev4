# ODEV 4

Merhabalar,

Aşağıdaki sorgu senaryolarını dvdrental örnek veri tabanı üzerinden gerçekleştiriniz.

    film tablosunda bulunan replacement_cost sütununda bulunan birbirinden farklı değerleri sıralayınız.
    film tablosunda bulunan replacement_cost sütununda birbirinden farklı kaç tane veri vardır?
    film tablosunda bulunan film isimlerinde (title) kaç tanesini T karakteri ile başlar ve aynı zamanda rating 'G' ye eşittir?
    country tablosunda bulunan ülke isimlerinden (country) kaç tanesi 5 karakterden oluşmaktadır?
    city tablosundaki şehir isimlerinin kaç tanesi 'R' veya r karakteri ile biter?

Kolay Gelsin.

# CEVAPLAR:

## 1.Soru:

SELECT DISTINCT(replacement_cost) FROM film;

19.99
25.99
13.99
10.99
23.99
18.99
20.99
24.99
11.99
15.99
27.99
29.99
12.99
14.99
22.99
16.99
28.99
9.99
17.99
21.99
26.99

## 2.Soru:

SELECT COUNT(DISTINCT(replacement_cost)) FROM film;

Birbirinden farklı 21 veri vardır.

## 3.Soru:

SELECT COUNT(*) FROM film
WHERE title LIKE 'T%' AND rating = 'G';

9 tanesi bu şartları sağlamaktadır.

## 4.Soru:

SELECT COUNT(country) FROM country
WHERE country LIKE '_____';

13 ülke 5 karakterden oluşmaktadır.

## 5.Soru:

SELECT COUNT(city) FROM city
WHERE city ILIKE '%r';

33 tane şehir ismi 'R' veya 'r' karakteri ile biter.
