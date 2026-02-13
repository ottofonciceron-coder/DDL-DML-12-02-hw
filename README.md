# Домашнее задание к занятию "Работа с данными (DDL/DML)" - Марчук Кирилл



### Задание 1.1.Поднимите чистый инстанс MySQL версии 8.0+. Можно использовать локальный сервер или контейнер Docker.
1.2.Создайте учётную запись sys_temp.
1.3.Выполните запрос на получение списка пользователей в базе данных.
1.4.Дайте все права для пользователя sys_temp.
1.5.Выполните запрос на получение списка прав для пользователя sys_temp.
1.6.Переподключитесь к базе данных от имени sys_temp.
1.7.Восстановите дамп в базу данных.
1.8.При работе в командной строке используйте команду для получения всех таблиц базы данных.



1. `Создаём папку проекта`
2. `Создаём файл docker-compose.yml`
3. `Подключаемся к MySQL`
4. `Создаём пользователя sys_temp`
5. `Смотрим Список пользователей(SELECT user, host FROM mysql.user;)`
6. `Даём все права пользователю (GRANT ALL PRIVILEGES ON *.* TO 'sys_temp'@'%' WITH GRANT OPTION;FLUSH PRIVILEGES;)`
7. `Получаем Список прав пользователя(SHOW GRANTS FOR 'sys_temp'@'%';)`
8. `Меняем тип аутентификации`
9. `Подключаемся как sys_temp`
10. `Скачиваем базу Sakila`
11. `Восстанавливаем дамп`
12. `Проверяем таблицы (USE sakila;SHOW TABLES;)`


```
*docker-compose.yml

services:
  mysql:
    image: mysql:8.0
    container_name: mysql8
    restart: always
    environment:
      MYSQL_ROOT_PASSWORD: rootpass
      MYSQL_DATABASE: testdb
    ports:
      - "3306:3306"
    volumes:
      - mysql_data:/var/lib/mysql

volumes:
  mysql_data:

```


---

![zadanie1](https://github.com/ottofonciceron-coder/DDL-DML-12-02-hw/blob/main/userslist.png)`

![zadanie1](https://github.com/ottofonciceron-coder/DDL-DML-12-02-hw/blob/main/sys_temp.png)`

![zadanie1](https://github.com/ottofonciceron-coder/DDL-DML-12-02-hw/blob/main/data%20base.png)`

---

### Задание 2.Составьте таблицу, используя любой текстовый редактор или Excel, в которой должно быть два столбца: в первом должны быть названия таблиц восстановленной базы, во втором названия первичных ключей этих таблиц.

1. `Создаём таблицу в Excel`

---

![zadanie2](https://github.com/ottofonciceron-coder/DDL-DML-12-02-hw/blob/main/MySQLtab.png)`

---






