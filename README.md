# Деплой и инфраструктура

порядок запуска приложения:

`sudo docker compose up -d --build` - для сборки образа

`sudo docker compose up` - для запуска

`sudo docker compose -f docker-compose.prod.yml up -d --build` - для производственного образа

`sudo docker compose -f docker-compose.prod.yml up` - соответсвенно - запуск

`sudo docker compose -f docker-compose.prod.yml exec web python manage.py migrate --noinput` - для миграции базы

`sudo docker compose -f docker-compose.prod.yml exec web python manage.py collectstatic --noinput --clear` - для сбора статики

везде `sudo` потому как докер как-то очень хреново работает с виндой. в результате пришлось расчехлять свой vb :)
