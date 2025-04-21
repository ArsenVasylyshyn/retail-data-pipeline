# Построение системы обработки данных для ритейла

#### Используемые технологии

![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-1.5+-150458?logo=pandas)
![PyArrow](https://img.shields.io/badge/PyArrow-12.0+-blue?logo=apache)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-14+-336791?logo=postgresql)
![Docker](https://img.shields.io/badge/Docker-Compose-blue?logo=docker)
![SQLAlchemy](https://img.shields.io/badge/SQLAlchemy-2.0+-red?logo=sqlalchemy)
![Parquet](https://img.shields.io/badge/Parquet-Apache-yellow?logo=apache)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)

---

## 📚 Описание проекта

В этом проекте я разработал полноценный ETL-пайплайн на основе данных розничной торговли Walmart. Я реализовал извлечение данных из различных источников, включая **SQLite** данных и файлы в формате **Parquet**, выполнил их трансформацию для очистки и подготовки, а затем загрузил в формат, удобный для
дальнейшего использования и анализа.

## 📂 Структура проекта

- 📁 **data/** — Входные данные (Parquet, CSV)
- 📁 **src/** — Исходный код пайплайна
  - 📄 `extract.py` — Извлечение данных
  - 📄 `transform.py` — Трансформация и очистка
  - 📄 `load.py` — Загрузка в базу данных
  - 📄 `config.py` — Конфигурации и подключения
- 📁 **notebooks/** — Анализ и визуализация
  - 📄 `EDA.ipynb` — Исследовательский анализ данных
- 🐳 `docker-compose.yml` — Docker-инфраструктура
- 📄 `requirements.txt` — Зависимости
- 📘 `README.md` — Документация

## 🚀 Установка

1. Склонируйте репозиторий:

   ```bash
   git clone https://github.com/your-username/retail-data-pipeline.git
   cd retail-data-pipeline
   ```

2. Запустите Docker-инфраструктуру:
   Якщо використовуєте Docker:

   ```bash
   docker-compose up --build
   ```

3. Або установите зависимости локально:
   Якщо хочете працювати без Docker:

   ```bash
   python3 -m venv venv
   source venv/bin/activate
   pip install -r requirements.txt
   ```

4. Настройте параметры подключения:
   В файле src/config.py укажите настройки подключения к базе данных:

   ```bash
   DB_HOST = "localhost"
   DB_PORT = "5432"
   DB_NAME = "retail_db"
   DB_USER = "postgres"
   DB_PASSWORD = "your_password"
   ```

5. Запустите пайплайн поэтапно:

   ```bash
   python src/extract.py
   python src/transform.py
   python src/load.py
   ```

6. Откройте ноутбук для анализа данных:

   ```bash
   jupyter notebook notebooks/EDA.ipynb
   ```

## 📌 Примеры использования:

**🔁 Регулярная загрузка данных в базу**  
Используйте пайплайн для ежедневного или еженедельного импорта новых данных с автоматическим обновлением таблиц.

**🧹 Очистка и нормализация сырых данных**  
Модуль `transform.py` применяет фильтрацию, форматирование и удаление пропусков, особенно полезно при работе с файлами форматов Parquet или CSV.

**📊 Интеграция с BI-инструментами**  
Данные можно использовать в инструментах визуализации — Tableau, Metabase или Power BI, подключив их к PostgreSQL.

**🧪 Локальное тестирование ETL без Docker**  
Пайплайн можно запускать напрямую через Python, что удобно для локальной отладки и тестирования.

## 📬 Связаться со мной

Если у вас возникнут вопросы, идеи по улучшению или желание сотрудничать — пишите!

- ✉️ **Email:** [arsenv92@gmail.ccom](mailto:your.email@example.com)

- 💻 **GitHub:** [github.com/your-username](https://github.com/your-username)

- 💬 **Telegram:** [@your_telegram](https://t.me/your_telegram)

- 🌐 **LinkedIn:** [linkedin.com/in/your-profile](https://linkedin.com/in/your-profile)
