# Домашнее задание к занятию «Работа с данными (DDL/DML)»

<details>

### Инструкция по выполнению домашнего задания

1. Сделайте fork [репозитория c шаблоном решения](https://github.com/netology-code/sys-pattern-homework) к себе в Github и переименуйте его по названию или номеру занятия, например, https://github.com/имя-вашего-репозитория/gitlab-hw или https://github.com/имя-вашего-репозитория/8-03-hw).
2. Выполните клонирование этого репозитория к себе на ПК с помощью команды `git clone`.
3. Выполните домашнее задание и заполните у себя локально этот файл README.md:
   - впишите вверху название занятия и ваши фамилию и имя;
   - в каждом задании добавьте решение в требуемом виде: текст/код/скриншоты/ссылка;
   - для корректного добавления скриншотов воспользуйтесь инструкцией [«Как вставить скриншот в шаблон с решением»](https://github.com/netology-code/sys-pattern-homework/blob/main/screen-instruction.md);
   - при оформлении используйте возможности языка разметки md. Коротко об этом можно посмотреть в [инструкции по MarkDown](https://github.com/netology-code/sys-pattern-homework/blob/main/md-instruction.md).
4. После завершения работы над домашним заданием сделайте коммит (`git commit -m "comment"`) и отправьте его на Github (`git push origin`).
5. Для проверки домашнего задания преподавателем в личном кабинете прикрепите и отправьте ссылку на решение в виде md-файла в вашем Github.
6. Любые вопросы задавайте в чате учебной группы и/или в разделе «Вопросы по заданию» в личном кабинете.

Желаем успехов в выполнении домашнего задания.

</details>

---

Задание можно выполнить как в любом IDE, так и в командной строке.

### Задание 1
1.1. Поднимите чистый инстанс MySQL версии 8.0+. Можно использовать локальный сервер или контейнер Docker.

![image](https://github.com/ovchdmitriy01/HW-12-2/blob/main/12-1-1.png)

1.2. Создайте учётную запись sys_temp. 

![image](https://github.com/ovchdmitriy01/HW-12-2/blob/main/12-1-2.png)

1.3. Выполните запрос на получение списка пользователей в базе данных. (скриншот)

![image](https://github.com/ovchdmitriy01/HW-12-2/blob/main/12-1-3.png)

1.4. Дайте все права для пользователя sys_temp. 

![image](https://github.com/ovchdmitriy01/HW-12-2/blob/main/12-1-4.png)

1.5. Выполните запрос на получение списка прав для пользователя sys_temp. (скриншот)

![image](https://github.com/ovchdmitriy01/HW-12-2/blob/main/12-1-5.png)

1.6. Переподключитесь к базе данных от имени sys_temp.

![image](https://github.com/ovchdmitriy01/HW-12-2/blob/main/12-1-6.png)

Для смены типа аутентификации с sha2 используйте запрос: 
```sql
ALTER USER 'sys_test'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
```
1.6. По ссылке https://downloads.mysql.com/docs/sakila-db.zip скачайте дамп базы данных.

1.7. Восстановите дамп в базу данных.

![image](https://github.com/ovchdmitriy01/HW-12-2/blob/main/12-1-7.png)

![image](https://github.com/ovchdmitriy01/HW-12-2/blob/main/12-1-8.png)

![image](https://github.com/ovchdmitriy01/HW-12-2/blob/main/12-1-9.png)

1.8. При работе в IDE сформируйте ER-диаграмму получившейся базы данных. При работе в командной строке используйте команду для получения всех таблиц базы данных. (скриншот)

![image](https://github.com/ovchdmitriy01/HW-12-2/blob/main/12-1-10.png)

![image](https://github.com/ovchdmitriy01/HW-12-2/blob/main/12-1-11.png)

*Результатом работы должны быть скриншоты обозначенных заданий, а также простыня со всеми запросами.*


### Задание 2
Составьте таблицу, используя любой текстовый редактор или Excel, в которой должно быть два столбца: в первом должны быть названия таблиц восстановленной базы, во втором названия первичных ключей этих таблиц. Пример: (скриншот/текст)
```
Название таблицы | Название первичного ключа
customer         | customer_id
```

### *Ответ*
```
actor           |   actor_id
address         |   address_id
category        |   category_id
city            |   city_id
country         |   country_id
customer        |   customer_id
film            |   film_id
film_actor      |   actor_id, film_id
film_category   |   film_id, category_id
film_text       |   film_id
inventory       |   inventory_id
language        |   language_id
payment         |   payment_id
rental          |   rental_id
staff           |   staff_id
store           |   store_id
```

---
