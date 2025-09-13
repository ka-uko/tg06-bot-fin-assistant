# Финансовый Telegram-бот «Denezka»

Телеграм-бот для учета расходов, просмотра актуальных курсов валют и получения советов по экономии.  
Разработан на **Python** с использованием библиотеки **aiogram**.

---

## 🚀 Функционал
- Регистрация пользователя в базе (по Telegram ID).
- Получение курса валют (USD/EUR → RUB) через API [ExchangeRate](https://www.exchangerate-api.com/).
- Рандомные советы по экономии.
- Ведение личных финансов:
  - 3 категории расходов.
  - Сохранение данных в SQLite.
  - Возможность последующего анализа.

---

## 🛠 Стек технологий
- Python 3.10+
- Aiogram
- SQLite
- Requests, Aiohttp
- Logging

---

## 📂 Установка и запуск
1. Клонировать репозиторий:
   ```bash
   git clone https://github.com/username/denezka-bot.git
   cd denezka-bot
   ```
2. Создать виртуальное окружение и установить зависимости:
   ```bash
   python -m venv .venv
   source .venv/bin/activate   # Linux/macOS
   .venv\Scripts\activate      # Windows
   pip install -r requirements.txt
   ```
3. Создать файл `config.py` и добавить токен вашего бота:
   ```bash
   echo 'TOKEN = "ваш_токен_бота"' > config.py
   ```
4. Запустить бота:
   ```bash
   python main.py
   ```

---

## 📊 База данных
- Используется **SQLite**. Таблица `users` создается автоматически при запуске.
- Хранит:
  - `telegram_id` — ID пользователя,
  - `name` — имя,
  - категории расходов (`category1/2/3`),
  - суммы расходов (`expenses1/2/3`).

---

## 🔮 Возможные улучшения
- Добавление статистики (сумма расходов, графики).
- Экспорт данных (CSV/Excel).
- Интеграция с банковскими API.
- Личный кабинет для каждого пользователя.

---

## 📜 Лицензия
MIT License
