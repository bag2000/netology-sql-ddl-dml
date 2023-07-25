## Работа с данными (DDL/DML) -Поляков Роман
## Задание 1 
### 1.3 Выполните запрос на получение списка пользователей в базе данных. (скриншот)
![Ссылка 1](https://github.com/bag2000/netology-sql-ddl-dml/blob/main/1.3.png)
### 1.5. Выполните запрос на получение списка прав для пользователя sys_temp. (скриншот)
![Ссылка 2](https://github.com/bag2000/netology-sql-ddl-dml/blob/main/1.5.png)
### 1.8. При работе в командной строке используйте команду для получения всех таблиц базы данных. (скриншот)
![Ссылка 3](https://github.com/bag2000/netology-sql-ddl-dml/blob/main/1.8.png)
  
### Результатом работы должны быть скриншоты обозначенных заданий, а также простыня со всеми запросами.
1.2. Создайте учётную запись sys_temp.  
CREATE USER 'sys_temp'@'localhost' IDENTIFIED BY 'password';  
  
1.3. Выполните запрос на получение списка пользователей в базе данных.  
SELECT User FROM mysql.user;  
  
1.4. Дайте все права для пользователя sys_temp.  
GRANT ALL PRIVILEGES ON *.* TO 'sys_temp'@'localhost';  
  
1.5. Выполните запрос на получение списка прав для пользователя sys_temp  
SHOW GRANTS FOR 'sys_temp'@'localhost';  
  
CREATE DATABASE sakila;  
  
1.7. Восстановите дамп в базу данных.  
Не получилось, делал через SQL-запросы в DBeaver  
mysql -u sys_temp -p sakila < sakila.mwb  
  
Создал базу, подом создал скрипт из sakila-data.sql и sakila-schema.sql  
CREATE DATABASE sakila;  
  
1.8. При работе в командной строке используйте команду для получения всех таблиц базы данных.  
USE sakila;  
SHOW TABLES;  
## Задание 1 
### Составьте таблицу, используя любой текстовый редактор или Excel, в которой должно быть два столбца: в первом должны быть названия таблиц восстановленной базы, во втором названия первичных ключей этих таблиц.
Название таблицы | Название первичного ключа  
actor		 	       | actor_id  
address          | address_id  
category	 	     | category_id  
city		 	       | city_id  
country          | country_id  
customer	 	     | customer_id  
film		      	 | film_id  
film_actor	  	 | actor_id, film_id  
film_category	   | film_id, category_id  
film_text	    	 | film_id  
inventory	 	     | inventory_id  
language	     	 | language_id  
payment		 	     | payment_id  
rental		     	 | rental_id  
staff		 	       | staff_id  
store		 	       | store_id  
