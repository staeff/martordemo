# Dockerize martordemo

See [https://semaphoreci.com/community/tutorials/dockerizing-a-python-django-web-application](https://semaphoreci.com/community/tutorials/dockerizing-a-python-django-web-application)


```sh
$ docker build -t martordemo .
$ docker run -it -p 8020:8020 \
     -e DJANGO_SUPERUSER_USERNAME=admin \
     -e DJANGO_SUPERUSER_PASSWORD=sekret1 \
     -e DJANGO_SUPERUSER_EMAIL=admin@example.com \
     martordemo
```

Problems:

* staticfiles werden nicht ordentlich geladen
