# Используем официальный образ Python 3.9
FROM python:3.9-slim

# Устанавливаем рабочий каталог в контейнере
WORKDIR /app

# Копируем код проекта в контейнер
COPY . /app/

# Устанавливаем зависимости
RUN pip install -r requirements.txt
# Установка SQLite
RUN apt-get update && apt-get install -y sqlite3

# Настройка окружения
ENV PYTHONDONTWRITEBYTECODE=1
ENV PYTHONUNBUFFERED=1
ENV DJANGO_SETTINGS_MODULE=school.settings

# Открываем порт для сервера разработки
EXPOSE 8000

# Определяем команду для запуска сервера разработки
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]