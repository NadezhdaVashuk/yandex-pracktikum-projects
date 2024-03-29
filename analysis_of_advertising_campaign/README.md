# Анализ рекламной кампании приложения Procrastinate Pro+

*Procrastinate Pro+* - развлекательное приложение. Несмотря на огромные вложения в рекламу, последние несколько месяцев компания терпит убытки. Необходимо разобраться в причинах и помочь компании выйти в плюс.

Есть данные о пользователях, привлечённых с 1 мая по 27 октября 2019 года:
* лог сервера с данными об их посещениях,
* выгрузка их покупок за этот период,
* рекламные расходы.

Задача изучить:
1. Откуда приходят пользователи и какими устройствами они пользуются?
2. Сколько стоит привлечение пользователей из различных рекламных каналов?
3. Сколько денег приносит каждый клиент?
4. Когда расходы на привлечение клиента окупаются?
5. Какие факторы мешают привлечению клиентов?


Для анализа предоставлены три датасета. Файл `visits_info_short.csv` хранит лог сервера с информацией о посещениях сайта, `orders_info_short.csv` — информацию о заказах, а `costs_info_short.csv` — информацию о расходах на рекламу.


Структура `visits_info_short.csv`:

`User Id` — уникальный идентификатор пользователя,

`Region` — страна пользователя,

`Device` — тип устройства пользователя,

`Channel` — идентификатор источника перехода,

`Session Start` — дата и время начала сессии,

`Session End` — дата и время окончания сессии.

Структура `orders_info_short.csv`:

`User Id` — уникальный идентификатор пользователя,

`Event Dt` — дата и время покупки,

`Revenue` — сумма заказа.


Структура `costs_info_short.csv`:

`dt` — дата проведения рекламной кампании,

`Channel` — идентификатор рекламного источника,

`costs` — расходы на эту кампанию.

**План исследования**:

1. Изучение данных.

2. Предобработка данных:

* Замена названий столбцов;

* Проверка данных на дубликаты;

* Преобразование данных в нужные типы;

* Проверка данных на наличие пропусков.

3. Задание функций для расчёта и анализа LTV, ROI, удержания и конверсии.

4. Исследовательский анализ данных.
* Составление профилей пользователей. Определение минимальной и максимальной даты привлечения пользователей.

* Определение из каких стран пользователи приходят в приложение и на какую страну приходится больше всего платящих пользователей.

* Определение какими устройствами пользуются клиенты и какие устройства предпочитают платящие пользователи. 

* Изучение рекламных источников привлечения и определение каналов, из которых пришло больше всего платящих пользователей. 

5. Оценка расходов на маркетинг.
6. Оценка окупаемости рекламы. Визуализация и описание информации о(об):
* Окупаемости рекламы в целом.
* Конверсии пользователей и динамики её изменения, а также информации о качестве удержания пользователей. 
* Окупаемости рекламы с разбивкой по устройствам. 
* Окупаемости рекламы с разбивкой по странам. 
* Окупаемости рекламы с разбивкой по рекламным каналам. 

7. Общий вывод.


Используемые библиотеки: *pandas, numpy, datetime, timedelta, seaborn, pyplot, warnings*.
