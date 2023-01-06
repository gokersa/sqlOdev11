# sqlOdev11
1) actor ve customer tablolarında bulunan first_name sütunları için tüm verileri sıralayalım.

2) actor ve customer tablolarında bulunan first_name sütunları için kesişen verileri sıralayalım.

3) actor ve customer tablolarında bulunan first_name sütunları için ilk tabloda bulunan ancak ikinci tabloda bulunmayan verileri sıralayalım.

4) İlk 3 sorguyu tekrar eden veriler için de yapalım.

***CEVAPLAR***

1) select first_name from customer
union
select first_name from actor; 
2) select first_name from customer
intersect
select first_name from actor; 
3) select first_name from actor
except
select first_name from customer; 
4) 
a) select first_name from customer
union all
select first_name from actor; 

b)select first_name from customer
intersect all 
select first_name from actor; 

c)select first_name from actor
except all
select first_name from customer; 
