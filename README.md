# Проект по docker-compose

Проект yamdb распиханный по контейнерам

В корне лежит `.env` в котором находятся следующие ключи

    DB_ENGINE=django.db.backends.postgresql # указываем, что работаем с postgresql
    DB_NAME= # имя базы данных
    POSTGRES_USER= # логин для подключения к базе данных
    POSTGRES_PASSWORD= # пароль для подключения к БД (установите свой)
    DB_HOST= # название сервиса (контейнера)
    DB_PORT=5432 # порт для подключения к БД


Сборка и запуск docker-compose осуществляется следующей командой

    docker-compose up --build 


Следующая настройка запускается следующими командами

    docker-compose exec web python manage.py makemigrations --noinput
    docker-compose exec web python manage.py migrate --noinput
    docker-compose exec web python manage.py collectstatic --no-input
    docker-compose exec web python manage.py createsuperuser
