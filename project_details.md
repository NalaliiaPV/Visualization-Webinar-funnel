## Webinar attendance dashboard (work project)

This is a data visualization project for one of the companies (data blurred).
- **Year:** 2022-2023 (several iterations)
- **Stakeholders:** CMO, CEO.
- **Users:** commercial department.
- **Deadlines:** MVP release - 1 week, improvements - constantly.
- **Business sense:** reflects the attendance statistics for each individual webinar, as well as generalized data by courses and languages.
- **My role:** data acquisition, data processing, connecting data sources to the GDS, joining tables, visualization.

We launched a webinar funnel. But how to know how things are going? How many people **signed up** for the webinar, and how many **came** to it? Where to look to see these banal numbers, which are so necessary for understanding the situation and making decisions?

The **Calendly** service was used to register for the webinar. To conduct webinars - **Zoom**. But the entire project team cannot monitor these services to keep track of the numbers - this is inconvenient. Need a dashboard. To do it wisely, you need to integrate these data sources with DWH, and from there transfer the data to the visualization program. But there is no development resource available. 

Business can't wait. What should I do to complete the task?

### Iteration 1. 

Every day I open Calendly and Zoom, write down the numbers in a Google spreadsheet, and calculate the CRs.

+++ fast implementation

--- a lot of manual labor.

--- impossible to scale

--- the human factor leads to errors

--- inflexibility and low detail of data.

### Iteration 2. 

Every day I open Calendly and Zoom, download tables with data, store them in Google spreadsheets, process and join the data with formulas, calculate the CRs.

+++ I spend a little less time

--- in a table it is not convenient to build different slices based on data

Итерация 3. Гроу тим автоматизирует с помощью лоу-код инструмента выгрузку из Zoom в гуглтаблицу. Подключаю гуглтаблицы, хранящие данные о регистрациях и явках, к ГДС. Собираю дашборд.
+ с данными в дашборде работать удобно. Много фильтров, много графиков и таблиц. Они закрывают все запросы пользователей, и новые визуалы добавить очень легко.
- все еще приходится выгружать данные из Calendly вручную каждый день.

Итерация 4. Calendly и Zoom заменил другой сервис - Бигмаркер. Появился ДВХ. У меня уже появились 2 аналитика в прямом подчинении и 1 в проектном. Я добилась выделения ресурса разработки для интеграций. Составила технические требования для них: какие конкретно данные с какой частотой мы хотим выгружать их Бигмаркера в ДВХ. Создала задачу в Джире, где прописала эти требования. Встретилась с продакт менеджером разработчиков - задачу взяли в спринт. Через 2 недели интеграции были реализованы. Мои аналитики проверили данные - все в порядке. Я составила ТЗ для одного из аналитиков на создание датасета в PostgreSQL, и ТЗ для другого аналитика на визуализацию в Double cloud. Контролировала процесс, проверяла результат - готово!

+ данные обновляются автоматически каждое утро
+ дашборды удобны и покрывают ключевые запросы пользователей.

что мы видим на дашборде:
