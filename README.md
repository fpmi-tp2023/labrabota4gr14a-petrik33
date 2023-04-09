[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-8d59dc4de5201274e310e4c54b9627a8934c3b88527886e3b421487c677d23eb.svg)](https://classroom.github.com/a/HneYUAfs)
# Mobile Software Programming Technologies. Lab Work №4

## Overview

### Задание 1. Установка sqlite в macOS

Последняя версия macOS идет с предустановленной SQLite, но если база
данных недоступна, то установить SQLite можно выполнив следующие шаги.
Проверить, что SQLite установлена можно с помощью команды:

```bash
$ whereis sqlite3
/usr/bin/sqlite3
```

или с помощью команды `$ sqlite3`

Если sqlite3 установлен, то выполнять установку **НЕ ТРЕБУЕТСЯ**

#### Способ 1. Установить sqlite из исходников

1. Скачать SQLite со страницы https://www.sqlite.org/download.html
2. Распаковать полученный архив tar.gz
3. Перейти в папку с исходниками slqite и выполнить команды:

``` bash
$ ./configure —prefix=/usr/local
$ make
$ make install
```

#### Способ 2. Установить с помощью утилиты Homebrew

```bash
$ brew install sqlite
```

#### Способ 3. Установить из порта

```bash
$ sudo port install sqlite
```
### Задание 2. Управление базой данных из консоли

#### Упражнение 2.1. Изучить видео

Ознакомиться с [видео](https://youtu.be/QjICgmk31js?list=PLGLfVvz_LVvTsslWD1HBQEjBbmAaAF9Xy).

#### Упражнение 2.2. Изучить примеры

Изучить примеры работы с базой sqllite из документа Базы данных.pdf и из книги
Grant Allen, Mike Owens. The Definitive Guide to SQLite (Second Edition) — 2010.pdf
(Chapter 3: SQL for SQLite, стр. 47-87).

#### Упражнение 2.3. Создать базу данных и выполнить запросы

Создать базу данных согласно [варианту](#specification-id-34), продемонстрировать следующие
навыки работы с консолью sqlite:

* создание таблицы (`create`);
* вставка данных в таблицу (`insert`);
* выборка данных (`select`) с выводом всех данных по столбцам и строкам, с
сортировкой по id и по имени и с выводом последних 5 строк (инструкция
`limit`);
* выборка данных с фильтрацией (условие `where`), если id=5;
* выборка данных с фильтрацией (условие `where`) и с совпадением по маске,
например все записи, где имя объекта (согласно варианту) начинается на
первую букву вашей фамилии (инструкция `like`);

#### Упражнение 2.4. Выполнить запросы по вариантам

Выполнить дополнительные задания согласно [варианту](#specification-id-34)

### Задание 3. Управление базой данных в SQLite Database Manager

#### Упражнение 3.1. Изучить примеры

Изучить примеры работы с базой sqllite из документа Печеночкин Г. SQL для
непрограммистов.

#### Упражнение 3.2. Выполнить учебные запросы по вариантам

Скачать базу данных Учет расходов.

Выполнить задания в SQLite Database Manager, например [DB Browser for SQLite](http://sqlitebrowser.org/) или
[Valentina Studio](https://itunes.apple.com/us/app/valentina-studio/id604825918?mt=12)
согласно [варианту](#specification-id-34).

#### Упражнение 3.3. Создать БД и выполнить запросы по вариантам

Создать БД согласно [варианту](#specification-id-34)
для [задания 2 (упражнение 2.3)](#упражнение-23)

Продемонстрировать выполнение всех операций и запросов согласно упражнениям
2.3 и 2.4.

### Задание 4. Изучение примеров приложений на C подключения и запросов к базе данных

Познакомиться с [руководством](http://www.tutorialspoint.com/sqlite/sqlite_c_cpp.htm),
разобрать и реализовать примеры
из руководства с компиляцией в консоли.

Изучить примеры выполнения параметризованных запросов, вставку
изображений в базу данных, вставку данных в режиме `autocommit` и в виде
транзакций, вывод метаданных базы данных на [примере материала](http://zetcode.com/db/sqlitec/)

Примеры опубликовать в репозитории в ветке examples. 
Под примеры создать папку `examples` и именовать
файлы согласно шаблону `example1_grN_LastnameFirstname.c`, где `N` — номер
группы, `LastnameFirstname` — Ваши фамилия и имя. В каталоге `examples` создать
файл `EXAMPLES.md`, в котором перечислить список рассмотренных примеров.
Использовать синтаксис `markdown` для формирования файла `EXAMPLES.md`.

В репозитории должен быть создан файл `README.md` согласно примеру
`README` файла из лабораторной работы 3, в котором указать список веток
репозитория и какой код в каждой ветке размещен.

#### Дополнительные инструкции

1. [Как создать приложение и подключиться к базе данных](https://www.sqlite.org/quickstart.html)
2. [How To Compile SQLite](https://www.sqlite.org/howtocompile.html)
3. [An Introduction To The SQLite C/C++ Interface](http://www.sqlite.org/cintro.html)
4. [SQLite C tutorial](http://zetcode.com/db/sqlitec/)
5. [Using SQLite in C programs](http://www.wassen.net/sqlite-c.html)
6. [How to Use SQLite to Manage Data in iOS Apps](http://www.appcoda.com/sqlitedatabase-ios-app-tutorial/)

### Задание 5. Разработка спецификации проекта на языке UML

1. Изучить [пример проектирования системы обработки заказов на языке UML](http://sp.cs.msu.ru/courses/ooap/exerb2021.html.)
2. Познакомиться с рекомендациями по созданию UML диаграмм в draw.io:
  * [Use case diagrams](https://www.diagrams.net/blog/uml-use-case-diagrams)
  * [Activity diagrams](https://www.diagrams.net/blog/uml-activity-diagrams.html)
  * [Class diagrams](https://www.diagrams.net/blog/uml-class-diagrams.html)
  * [Sequence diagrams](https://www.diagrams.net/blog/sequence-diagrams.html)
  * [Examples](https://www.diagrams.net/blog/uml-2-5.html#example-uml-diagrams)
3. Реализовать согласно [варианту для задания 2](#задание-2) следующие виды диаграмм:
  * диаграмма вариантов использования, включая пример текстового сценария для одного из вариантов использования;
  * диаграмма деятельности;
  * диаграмма классов;
  * диаграмма последовательности;
  * диаграмма компонентов.
4. Опубликовать в wiki репозитория постановку задачи, диаграммы и текстовый сценарий к варианту использования и оформить используя синтаксис markdown. 
Добавить описание/пояснение к каждому виду диаграмм.

## Specification: ID 34

### Задание 2

#### Упражнение 2.3

**Товар**: id; наименование; стоимость; срок хранения; сорт; дата выпуска; срок
годности.

#### Упражнение 2.4

Выполнить запросы:

* Вывести данные про товары срок годности которых истекает в этом году.
* Используя инструкцию `alter`, добавить дополнительные столбцы, один из
которых `category_id` (тип `integer` и содержит идентификаторы категорий
товаров).
* Создать таблицу `category (id, cat_name, cat_description)`.
* Вывести данные обо всех товарах в форме идентификатор товара,
наименование, дата выпуска, название категории товара.
* подсчет количества товаров с помощью `count`, если `стоимость=49 руб`
* суммарная стоимость товаров с помощью `sum`, если `год выпуска>2016`
* максимальная и минимальная стоимость с помощью `max` и `min`
* Используя инструкцию `inner join` вывести полные сведения о товарах и
категории для категории с `id=2`.

### Задание 3

#### Упражнение 3.2

1. Составьте запрос к таблицам Categories и Spendings, который возвращает
название категории покупки, название магазина и потраченную сумму для всех
покупок, относящихся к категории с номером 2.
2. Составьте запрос, возвращающий названия категорий с номерами 1, 3 и 4 (с
использованием ключевого слова IN)

## Usage

Author: Tsimafei Petrykevich - Group №14

## Key Questions

### 1. Перечислите способы создания базы данных sqlite

* `sqlite3 <DatabaseName>.db`
* Импорт базы данных из .sql файла
* `touch <DatabaseName>.db`
* С помощью графического интерфейса, например “DB Browser for SQLite”

### 2. С помощью какой команды в консоли sqlite можем просмотреть список баз данных и подключенных файлов баз данных?

```sqlite
.databases
```

### 3. Приведите перечень команд для экспорта данных из таблицы базы данных в файл с расширением .csv

```sqlite
.headers on
.mode csv
.output <FileName>.csv
SELECT * FROM <TableName>;
.output stdout
```

### 4. Приведите перечень команд для экспорта отдельной таблицы и всей базы данных в файл с расширением .sql и сжатый файл, например в файл с расширением .sql.tgz

#### Вся база данных:

```sqlite
sqlite3 my_database.sqlite .dump my_table > my_table.sql
```

#### Таблица:

```
sqlite3 my_database.sqlite .dump > my_database.sql
```

#### Сжатие:

```sqlite
tar -czf my_database.sql.tgz my_database.sql
```

### 5. Как вывести из таблицы данные по строкам и по столбцам?

```sqlite
.mode column
.headers on
Select <Column1,...,ColumnM> from <TableName>
```

### 6. Для чего используется команда .headers в консоли sqlite?

Для вывода названий столбцов таблицы.
 
### 7. Какая команды используется для вывода настроек окружения в sqlite?

```sqlie
.show
```

### 8. С помощью какой команды выводится список таблиц базы данных в консоли sqlite?

```sqlite
.tables
```

### 9. Приведите пример запроса выборки из 2-х таблиц

```sqlite
select * from products inner join categories on products.category_id = categories.id;
```
### 10. Приведите пример запроса для обновления данных в строках таблицы в зависимости от значения определённого поля

```sqlite
select * from products where id=2;
```

### 11. Приведите пример функции, которая открывает соединение с файлом базы данных SQLite и возвращает объект соединения с базой данных, который будет использоваться другими функциями SQLite?

```c
rc = sqlite3_open("test.db", &db);
```

### 12. Приведите пример синтаксиса функции sqlite3_exec и объясните результат выполнения

```c
rc = sqlite3_exec(db, sql, callback, 0, &zErrMsg);
```

Данная функция передаст в rc код ошибки SQLite. В случае успешного выполнения запроса , функция вернет код 0.
Если в запросе была ошибка, то sqlite3_exec() вернет код ошибки, а содержимое переменной zErrMsg будет установлено на соответствующее сообщение об ошибке. 

### 13. Какая функция закрывает соединение с базой данных, ранее открытое вызовом sqlite3_open? Приведите пример синтаксиса

```c
sqlite3_close(db);
```

### 14. Приведите пример фрагмента кода на языке C для создания таблицы в базе данных sqlite и объясните его

```c
/* Create SQL statement */
sql = "CREATE TABLE COMPANY("  \
   "ID INT PRIMARY KEY     NOT NULL," \
   "NAME           TEXT    NOT NULL," \
   "AGE            INT     NOT NULL," \
   "ADDRESS        CHAR(50)," \
   "SALARY         REAL );";
```

### 15. Приведите пример фрагмента кода на языке C для вставки данных в таблицу в базе данных sqlite и объясните его

```c
/* Create SQL statement */
sql = "INSERT INTO COMPANY (ID,NAME,AGE,ADDRESS,SALARY) "  \
      "VALUES (1, 'Paul', 32, 'California', 20000.00 ); " \
      "INSERT INTO COMPANY (ID,NAME,AGE,ADDRESS,SALARY) "  \
      "VALUES (2, 'Allen', 25, 'Texas', 15000.00 ); "     \
      "INSERT INTO COMPANY (ID,NAME,AGE,ADDRESS,SALARY)" \
      "VALUES (3, 'Teddy', 23, 'Norway', 20000.00 );" \
      "INSERT INTO COMPANY (ID,NAME,AGE,ADDRESS,SALARY)" \
      "VALUES (4, 'Mark', 25, 'Rich-Mond ', 65000.00 );";
```

### 16. Приведите пример фрагмента кода на языке C выполнением AUTOCOMMIT и TRANSACTION и объясните в чем особенности использования их

```c
sqlite3 *db;
sqlite3_open("my_database.db", &db);

// AUTOCOMMIT enabled
sqlite3_exec(db, "PRAGMA autocommit = ON;", NULL, NULL, NULL);

// TRANSACTION begins
sqlite3_exec(db, "BEGIN TRANSACTION;", NULL, NULL, NULL);

// execute some SQL statements here

// TRANSACTION ends
sqlite3_exec(db, "COMMIT;", NULL, NULL, NULL);
```

AUTOCOMMIT определяет, будут ли SQL-операции автоматически подтверждаться после их выполнения или нет.
Если AUTOCOMMIT включен, каждая операция будет автоматически подтверждаться, что означает, что изменения будут сохранены в базе данных.
Если выключен, изменения не будут автоматически сохранены в базе данных и будут потеряны при выходе из программы или при возникновении ошибки.

TRANSACTION, с другой стороны, позволяет выполнять несколько операций одновременно и сохранять их все как одну транзакцию.
Это полезно, например, при выполнении нескольких операций, которые должны быть успешно завершены все вместе или ни одна из них не должна быть сохранена.
