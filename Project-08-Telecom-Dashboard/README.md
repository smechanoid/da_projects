# # Расчёт текущей лояльности абонентов оператора мобильной связи


## Данные

Источники данных - результаты опроса пользователей:

----------------------------------
**USER**

 - `user_id`	Идентификатор клиента, первичный ключ таблицы
 - `lt_day`	Количество дней «жизни» клиента
 - `age`	Возраст клиента в годах
 - `gender_segment`	Пол клиента (1 – женщина, 0 – мужчина)
 - `os_name`	Тип операционной системы
 - `cpe_type_name`	Тип устройства
 - `location_id`	Идентификатор домашнего региона клиента, внешний ключ, отсылающий к таблице location
 - `age_gr_id`	Идентификатор возрастного сегмента клиента, внешний ключ, отсылающий к таблице age_segment
 - `tr_gr_id`	Идентификатор сегмента клиента по объёму потребляемого трафика в месяц, внешний ключ, отсылающий к таблице - traffic_segment
 - `lt_gr_id`	Идентификатор сегмента клиента по количеству дней «жизни», внешний ключ, отсылающий к таблице lifetime_segment
 - `nps_score`	Оценка клиента в NPS-опросе (от 1 до 10)

---------------------------------------------------
**LOCATION**

 - `location_id`	Идентификатор записи, первичный ключ
 - `country`	Страна
 - `city`	Город
------------------------------------------
**AGE_SEGMENT**

 - `age_gr_id`	Идентификатор сегмента, первичный ключ
 - `bucket_min`	Минимальная граница сегмента
 - `bucket_max`	Максимальная граница сегмента
 - `title`	Название сегмента
-----------------------------------------------
**TRAFFIC_SEGMENT**

 - `tr_gr_id`	Идентификатор сегмента, первичный ключ
 - `bucket_min`	Минимальная граница сегмента
 - `bucket_max`	Максимальная граница сегмента
 - `title`	Название сегмента
-----------------------------------------
**LIFETIME_SEGMENT**

 - `lt_gr_id`	Идентификатор сегмента, первичный ключ
 - `bucket_min`	Минимальная граница сегмента
 - `bucket_max`	Максимальная граница сегмента
 - `title`	Название сегмента
-----------------------------------------


## Задача

- Выгрузить данные из базы с помощью SQL запроса 
- Выделить группы пользователей по уровню удовлетворённости сервисами мобильного оператора
- Построить дашборд 
- Создать презентацию с результатами исследования

## Ссылка на дашборд

[Ссылка](https://public.tableau.com/app/profile/serg6453/viz/Telecom_16341325430950/TelecomNPS)


## Используемые библиотеки
*pandas*

*sqlalchemy*

*sqlite3*

*requests*