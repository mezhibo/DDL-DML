Задание 1
1.1. Поднимите чистый инстанс MySQL версии 8.0+. Можно использовать локальный сервер или контейнер Docker.

1.2. Создайте учётную запись sys_temp.

1.3. Выполните запрос на получение списка пользователей в базе данных. (скриншот)

1.4. Дайте все права для пользователя sys_temp.

1.5. Выполните запрос на получение списка прав для пользователя sys_temp. (скриншот)

1.6. Переподключитесь к базе данных от имени sys_temp.

Для смены типа аутентификации с sha2 используйте запрос:

ALTER USER 'sys_test'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
1.6. По ссылке https://downloads.mysql.com/docs/sakila-db.zip скачайте дамп базы данных.

1.7. Восстановите дамп в базу данных.

1.8. При работе в IDE сформируйте ER-диаграмму получившейся базы данных. При работе в командной строке используйте команду для получения всех таблиц базы данных. (скриншот)

Решение 1

![alt text](https://github.com/mezhibo/DDL-DML/blob/42412122823198fa79236b33f651f74bac675f02/IMG/11.jpg)

![alt text](https://github.com/mezhibo/DDL-DML/blob/42412122823198fa79236b33f651f74bac675f02/IMG/1.jpg)

![alt text](https://github.com/mezhibo/DDL-DML/blob/42412122823198fa79236b33f651f74bac675f02/IMG/2.jpg)

![alt text](https://github.com/mezhibo/DDL-DML/blob/42412122823198fa79236b33f651f74bac675f02/IMG/3.jpg)

![alt text](https://github.com/mezhibo/DDL-DML/blob/42412122823198fa79236b33f651f74bac675f02/IMG/4.jpg)

![alt text](https://github.com/mezhibo/DDL-DML/blob/42412122823198fa79236b33f651f74bac675f02/IMG/sakila.png)

Простыня команд:


create user 'sys_temp'@'localhost' IDENTIFIED with mysql_native_password by '{11111}';

select user from mysql.user;

grant all privileges on *.* to 'sys_temp'@'localhost';

show grants for 'sys_temp'@'localhost';

ALTER USER 'sys_temp'@'localhost' IDENTIFIED WITH mysql_native_password BY '11111'

CREATE DATABASE sakila;



Задание 2
Составьте таблицу, используя любой текстовый редактор или Excel, в которой должно быть два столбца: в первом должны быть названия таблиц восстановленной базы, во втором названия первичных ключей этих таблиц. Пример: (скриншот/текст)

Название таблицы | Название первичного ключа
customer         | customer_id



Решение 2

![alt text](https://github.com/mezhibo/DDL-DML/blob/42412122823198fa79236b33f651f74bac675f02/IMG/5.jpg)

