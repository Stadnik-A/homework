# Домашнее задание к занятию «Базы данных» - `Станик Александр`

### Задание 1
  Тип департамента 
  - идентификатор integer PRIMARY KEY
  - название департамента varchar(50)
  
  Филиалы
  - идентификатор integer PRIMARY KEY
  - название филиала varchar(50)
  - адрес филиала varchar(50)

  Размер зарплаты 
  - идентификатор integer PRIMARY KEY
  - идентификатор пользователя integer,
  - размер зарплаты integer

  Проекты
  - идентификатор integer PRIMARY KEY
  - название проекта varchar(50)
  
  Должность
  - идентификатор integer PRIMARY KEY
  - название должности varchar(50)
 
  Сотрудники"
  - идентификатор integer PRIMARY KEY
  - ФИО varchar(50)
  - Дата прихода date
  - идентификатор проекта integer
  - идентификатор департамента integer
  - идентификатор филиалда integer
  - идентификатор должности integer
  - идентификатор зарплаты integer
