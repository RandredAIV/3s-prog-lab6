# Файлы утеряны // Source files are lost

# RU
# Реляционная база данных PostgreSQL

## Описание
Проектирование и реализация реляционной базы данных на тему
«Формула 1» с использованием PostgreSQL и pgAdmin 4.
База данных включает 5 таблиц и 10 SQL-запросов к ним.

## Структура БД
```
Гонщики         — основная таблица (имя, фамилия, национальность, дата рождения, команда)
├── Команды     — название, год основания, основатель
├── Гонки       — название, дата, место проведения
├── Результаты_гонок — позиция гонщика в гонке
└── Чемпионаты  — год чемпионата, команда
```

## SQL-запросы
10 запросов, включая:
- выборку гонщиков с их командами (JOIN)
- поиск гонщиков с подиумами (DISTINCT)
- подсчёт количества побед по гонщикам и командам (COUNT, GROUP BY)
- поиск лучшего результата каждого гонщика (MIN)
- фильтрацию по диапазону дат (BETWEEN)
- вложенные подзапросы (subquery)

## Зависимости
Для работы с проектом необходимо установить:

**PostgreSQL:**
```
sudo apt install postgresql postgresql-contrib
```

**pgAdmin 4:**
```
curl https://www.pgadmin.org/static/packages_pgadmin_org.pub | sudo apt-key add
sudo sh -c 'echo "deb https://ftp.postgresql.org/pub/pgadmin/pgadmin4/apt/$(lsb_release -cs) pgadmin4 main" > /etc/apt/sources.list.d/pgadmin4.list && apt update'
sudo apt install pgadmin4
```

## Запуск
1. Установить PostgreSQL и pgAdmin 4 (см. раздел «Зависимости»)
2. Открыть pgAdmin 4 и подключиться к серверу
3. Создать базу данных:
```sql
CREATE DATABASE Lab6;
```
4. Выполнить скрипты создания таблиц и наполнения данными
5. Запустить SQL-запросы в редакторе pgAdmin 4

---
# EN
# Relational Database PostgreSQL

## Description
Design and implementation of a relational database on the topic
"Formula 1" using PostgreSQL and pgAdmin 4.
The database includes 5 tables and 10 SQL queries.

## Database Structure
```
Drivers         — main table (name, surname, nationality, date of birth, team)
├── Teams       — name, founding year, founder
├── Races       — name, date, location
├── Race_Results — driver position in a race
└── Championships — championship year, team
```

## SQL Queries
10 queries including:
- selecting drivers with their teams (JOIN)
- finding drivers with podium finishes (DISTINCT)
- counting wins per driver and team (COUNT, GROUP BY)
- finding each driver's best result (MIN)
- filtering by date range (BETWEEN)
- nested subqueries (subquery)

## Dependencies
The following tools must be installed:

**PostgreSQL:**
```
sudo apt install postgresql postgresql-contrib
```

**pgAdmin 4:**
```
curl https://www.pgadmin.org/static/packages_pgadmin_org.pub | sudo apt-key add
sudo sh -c 'echo "deb https://ftp.postgresql.org/pub/pgadmin/pgadmin4/apt/$(lsb_release -cs) pgadmin4 main" > /etc/apt/sources.list.d/pgadmin4.list && apt update'
sudo apt install pgadmin4
```

## How to Run
1. Install PostgreSQL and pgAdmin 4 (see «Dependencies»)
2. Open pgAdmin 4 and connect to the server
3. Create the database:
```sql
CREATE DATABASE Lab6;
```
4. Execute table creation and data insertion scripts
5. Run SQL queries in the pgAdmin 4 query editor
