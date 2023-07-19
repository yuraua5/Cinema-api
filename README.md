# ScreenSquad API

Api service for cinema management written on DRF

## Installing using GitHub

Install PostgresSQP and create a database.

```shell 
git clone https://github.com/yuraua5/cinema-api.git
cd cinema-api
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

Set the following environment variables:

```shell
set DB_HOST=<your db hostname>
set DB_NAME=<your db name>
set DB_USER=<your db username>
set DB_PASSWORD=<your db user password>
set SECRET_KEY=<your secret key>
```

Apply database migrations:

```shell
python manage.py migrate
```

Start the server:

```shell
python manage.py runserver
```

## Run with Docker

Make sure Docker is installed on your system.

```shell
docker-compose build
docker-compose up
```

## Getting access

To get access to the API:

- Create a user via `/api/user/register/`.
- Obtain an access token via `/api/user/token/`.

## Features

- JWT authentication
- Admin panel: `/admin/`
- Documentation is located at `/api/doc/swagger/`
- Managing orders and tickets
- Creating movies with genres and actors
- Creating cinema halls
- Adding movie sessions
- Filtering movies and movie sessions
