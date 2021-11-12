# Проект по docker-compose

Проект yamdb распиханный по контейнерам

В корне должен лежать `.env` в котором должны находится ключи как в `.env.
example`

Сборка и запуск docker-compose осуществляется следующей командой

    docker-compose up -d --build 


Следующая настройка запускается следующими командами

    docker-compose exec web python manage.py migrate --noinput
    docker-compose exec web python manage.py collectstatic --no-input
    docker-compose exec web python manage.py createsuperuser
