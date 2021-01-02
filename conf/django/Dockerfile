FROM python:3.9.1-slim-buster

RUN apt-get update
RUN apt-get dist-upgrade -y

ADD conf/django/requirements.txt .
RUN python -m pip install -r requirements.txt

ADD django_server /work/django_server
WORKDIR /work/django_server

CMD python manage.py runserver_plus 0.0.0.0:8000
