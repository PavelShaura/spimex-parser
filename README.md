# SPIMEX Trading Results Parser

Этот проект представляет собой асинхронный парсер на Python 3.10, который скачивает бюллетени по итогам торгов с сайта Санкт-Петербургской Международной Товарно-сырьевой биржи (https://spimex.com/markets/oil_products/trades/results/), извлекает необходимые данные и сохраняет их в базу данных.

## Установка

1. Клонируйте репозиторий:
   ```sh
   git clone https://github.com/PavelShaura/spimex-parser.git
   cd spimex-parser

2. Создайте виртуальное окружение и активируйте его:

`python -m venv venv`
`source venv/bin/activate` 
 
Для Windows используйте 
`venv\Scripts\activate`

3. Установите зависимости:

`pip install poetry` `poetry install`

4. Создайте файл .env в корневой директории проекта на примере файла .env_example

## Запуск

1.Запустите Docker Compose:

`docker-compose up -d`

2. Запустите парсер:

`python app/main.py`

Данные сохраняются в таблицу spimex_trading_results по итогам торгов начиная с 2023 года.


Веб-фреймворки и библиотеки

    aiohttp: Асинхронная библиотека для выполнения HTTP-запросов, что позволяет эффективно скачивать бюллетени с сайта биржи.
    BeautifulSoup4: Библиотека для парсинга HTML и XML документов, используемая для извлечения данных из загруженных бюллетеней.
    xlrd: Библиотека для работы с Excel файлами, используемая для чтения данных из загруженных бюллетеней.

База данных

    PostgreSQL: Реляционная база данных, используемая для хранения данных по итогам торгов.
    SQLAlchemy: ORM (Object-Relational Mapping) библиотека для Python, используемая для взаимодействия с базой данных.
    asyncpg: Асинхронный драйвер для PostgreSQL, обеспечивающий эффективное выполнение запросов к базе данных.

Управление зависимостями и настройками

    Pydantic: Библиотека для валидации данных и управления настройками, используемая для определения моделей данных.
    python-dotenv: Библиотека для загрузки переменных окружения из файла .env, что упрощает управление конфигурацией проекта.