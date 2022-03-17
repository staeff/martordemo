# Dockerize martordemo

Follows [https://semaphoreci.com/community/tutorials/dockerizing-a-python-django-web-application](https://semaphoreci.com/community/tutorials/dockerizing-a-python-django-web-application) with slight adoptions.

## Run from dockerhub

```sh
$ docker run -dp 8020:8020 -e DJANGO_SUPERUSER_USERNAME=admin -e DJANGO_SUPERUSER_PASSWORD=sekret1 -e DJANGO_SUPERUSER_EMAIL=admin@example.com staeff/martordemo
```

## Run locally

```sh
$ git clone https://github.com/staeff/martordemo.git
$ docker build -t martordemo .
$ docker run -it -p 8020:8020 \
     -e DJANGO_SUPERUSER_USERNAME=admin \
     -e DJANGO_SUPERUSER_PASSWORD=sekret1 \
     -e DJANGO_SUPERUSER_EMAIL=admin@example.com \
     martordemo
```
