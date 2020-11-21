FROM python:latest
MAINTAINER "angalcs soroush.products@gmail.com"
WORKDIR /usr/src/app

ENV PYTHONDONTWRITEBYTECODE 1
ENV PYTHONUNBUFFERED 1

RUN apt-get update -y && \
    apt-get install python3-dev -y

RUN pip install --upgrade pip
RUN pip install pipenv
COPY ./Pipfile /usr/src/app/Pipfile
RUN pipenv install --skip-lock --system

COPY . /usr/src/app/

RUN python manage.py makemigrations && \
    python manage.py migrate && \
    python manage.py collectstatic


