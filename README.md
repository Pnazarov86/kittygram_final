# Финальный проект: контейнеры и CI/CD для Kittygram

### Описание
Проект Kittygram, позволяет пользователям делиться фотографиями котиков со всего мира.

### Технологии
 - Python 3.9
 - Django 3.2
 - Django REST framework 3.12

## Запуск проекта в dev-режиме на Linux:
Клонировать репозиторий и перейти в папку kittygram_final/backend/
Создать и активировать виртуальное окружение:
```
python3 -m venv venv
```
```
source venv/bin/activate
```
Установить зависимости из файла requirements.txt:

```
python -m pip install --upgrade pip
```

```
pip install -r requirements.txt
```
Сборка проекта:
```
docker-compose up
```
Выполните миграции:
```
docker compose exec backend python manage.py migrate
```
Собрать статику:
```
docker compose exec backend python manage.py collectstatic
```
```
docker compose exec backend cp -r /app/collected_static/. /backend_static/static/
```

Откройте в браузере страницу http://localhost:9000/


## Запуск проекта на боевом сервере:
В проекте реализовано автоматическое развертывание с помощью сервиса GitHub Actions, после git push в ветку main(master).

Проект доступен по адресу https://kittyphoto.ddns.net/

### Автор 
Петр Назаров
https://github.com/Pnazarov86





