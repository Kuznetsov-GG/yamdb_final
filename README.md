# Проект YaMDb


#Технологии

Python 3.7, Django 3.2, Django REST Framework, Simple-JWT, SQLite3, GIT, PostgreSQL, Docker, Docker-compose.


#API для сервиса YaMDb позволяет:

Ознакомиться с полным функционалом и примерами можно по адресу http://localhost/redoc/ ( Доступно после запуска проекта )

#Разработчик проекта

Авторы:

Алексей Курепин E-mail: alexkurepin83@yandex.ru

Григорий Кузнецов E-mail: grishik77788@gmail.com

Константин Абашин E-mail: kabashin@mail.ru

## Шаблон наполнения env-файла

```
DB_ENGINE=django.db.backends.postgresql
DB_NAME=postgres
POSTGRES_USER=postgres
POSTGRES_PASSWORD=postgres
DB_HOST=db
DB_PORT=5432
```

## Запуск контейнера и приложения в нем
Перейти в репозиторий для запуска докера
```
cd infra/
```
Запуск docker-compose
```
docker-compose up -d --build
```
Создайте суперпользователя
```
docker-compose exec web python manage.py createsuperuser
```
Войдите в админку и создайте одну-две записи объектов

### Следующим шагом создайте дамп (резервную копию) базы:
```
docker-compose exec web python manage.py dumpdata > fixtures.json
