# Dockerize martordemo

Follows [https://semaphoreci.com/community/tutorials/dockerizing-a-python-django-web-application](https://semaphoreci.com/community/tutorials/dockerizing-a-python-django-web-application) with slight adoptions.

## Run from dockerhub

```sh
$ docker run -dp 8080:8080 -e DJANGO_SUPERUSER_USERNAME=admin -e DJANGO_SUPERUSER_PASSWORD=sekret1 -e DJANGO_SUPERUSER_EMAIL=admin@example.com staeff/martordemo
```

## Run locally with docker-compose

```sh
$ docker-compose up -d
```

## Run locally without docker-compose

```sh
$ git clone https://github.com/staeff/martordemo.git
$ docker build -t martordemo .
$ docker run -it -p 8080:8080 \
     -e DJANGO_SUPERUSER_USERNAME=admin \
     -e DJANGO_SUPERUSER_PASSWORD=sekret1 \
     -e DJANGO_SUPERUSER_EMAIL=admin@example.com \
     martordemo
```

## Deploy to fly.io

The app is ready to be deployed to fly.io. It should be a matter of just issueing `flyctl deploy`.
Maybe the app name in `fly.toml` needs to be changed, because the need to be unique.
