### Над проектом работали

* **Александрова Лада** - подготовка презентации, систематизация информации, участие в обсуждении и выработке вариантов решений, тестирование; 
* **Лыткин Евгений (тимлид)** - координация работы участников, работа с базой данных, разработка, тестирование;
* **Раздобреева Анастасия** - разработка чат-бота, работа с документацией, тестирование;
* **Танаев Владислав** - разработка модели, тестирование;
* **Фомин Владимир** - работа с базой данных и составление датасета, разработка семантического сравнения вакансии и резюме.

# Виртуальный помощник для подбора кандидатов под требования вакансии

Этот проект представляет собой бота для Telegram, который позволяет пользователям загружать вакансии и получать список отобранных под ее требования кандидатов.

## Описание

Бот предназначен для упрощения работы HR-специалистов, предоставляет возможность автоматического отбора кандидатов, подходящих под конкретную вакансию. Он поддерживает команды для загрузки текста вакансии, получения списка кандидатов. На данный момент для векторизации требований и навыков используется модель SentenceTransformer all-MiniLM-L6-v2 (sbert). Вычисляются сходства между требованиями и навыками, и для каждого требования выводится наиболее подходящий навык с его степенью сходства.
Впоследствии планируется добавить возможность использования разных моделей для реализации отбора кандидатов.

Проект находится на стадии разработки. На данный момент разработка модели находится в репозитории https://github.com/valdem/HRRanging. Планируется интеграция всех составляющих в один проект.


## Установка

1. Клонируйте репозиторий:

   * git clone git@github.com:wht-trc/JobVacancyRankingBot.git
   * cd <имя_папки>

2. Установите необходимые зависимости:
    pip install -r requirements.txt

3. Создайте файл .env в корневой директории проекта и добавьте в него ваш токен бота и прочие переменные окружения:
    
    * TOKEN=<ваш_токен>

## Использование

1. Запустите бота:
    python bot.py

2. Откройте Telegram и найдите вашего бота.

3. Используйте следующие команды:

    * /start - Начать взаимодействие с ботом.
    * /help - Просмотреть список доступных команд.
    * /load - Загрузить текст вакансии.
    * /find - Получить список отобранных кандидатов.

## Пример использования

1. Отправьте команду /load, чтобы начать загрузку текста вакансии.
2. Введите требования вакансии.
3. Используйте команду /find, чтобы получить список кандидатов.

## Зависимости

* aiogram, telethon - библиотеки для работы с Telegram Bot API.
* python-dotenv - для работы с переменными окружения.
