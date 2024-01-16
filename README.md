# taski-docker - планировщик задач, упвкованный в контейнеры на Docker
# Taski - планировщик задач.

### Описание
Приложение для планирования задач. Есть фронтенд (React)
и бэкенд (Django). Задачи можно добавлять, изменять, удалять
и переводить из группы "незавершённые" в "завершённые".

## Технологии

- Фронтенд: React
- Бэкенд: Django Rest Framework
- База данных: PostgreSQL
- Nginx
- Docker
- Gunicorn
- Github actions

## Запуск проекта локально
Клонируем репозиторий:
```bash
git clone https://github.com/shurikman82/taski-docker.git
```

Запускаем оркестрацию:

```bash
sudo docker compose up
```

## После запуска: миграции, сбор статики



```bash
sudo docker compose exec backend python manage.py migrate

sudo docker compose exec backend python manage.py collectstatic

sudo docker compose exec backend cp -r /app/collected_static/. /backend_static/static/
```
## Автор:
Александр Русанов, shurik.82rusanov@yandex.ru, @shurikrusanov
