# Yamdb API final
![YAMDB](https://github.com/eraline/yamdb_final/actions/workflows/yamdb_workflow.yaml/badge.svg)

API for the Review Service. Authorization was made using the JWT token. Users can write reviews on films, music or book, also they can leave comments on any reviews.

This project was made in collaboration with @sproggi and @menyanet73. My part of this project was to build scoring, reviews and comment sections. Also I made a huge effort in coordination between the developers, so we went through it smoothly.

Stack:
Python 3, Django 2.2, DRF, PyJWT

You can find ReDoc of the API here:
http://51.250.18.168/redoc/

#### Stack: 
Python 3, Django 2.2, DRF, PyJWT

## How start project:

Clone a repository and go to command line:

```sh
git clone https://github.com/menyanet73/infra_sp2.git
```

```sh
cd infra_sp2/infra/
```
Create github secrets with your data.

```sh
DJANGO_SECRET_KEY='you can generate it using https://djecrety.ir'
DB_ENGINE=django.db.backends.postgresql # choose database engine
DB_NAME=postgres # dbname
POSTGRES_USER=postgres # login to db connection
POSTGRES_PASSWORD=postgres # password
DB_HOST=db # service name for container
DB_PORT=5432 # port
DOCKER_PASSWORD=your_dockerpassword
DOCKER_USERNAME=your_dockerusername
HOST=ip_server
SSH_KEY=ssh_for_server
TELEGRAM_TO=id_your_tg
TELEGRAM_TOKEN=tg_bot_token
USER=username_for_server
```


Create/download docker-compose images and containers

```sh
docker-compose up
```

Apply migrations:


```sh
docker-compose exec web python manage.py migrate
```

Create superuser:

```sh
docker-compose exec web python manage.py createsuperuser
```

Collect static:

```sh
docker-compose exec web python manage.py collectstatic --no-input
```

Done!


```
