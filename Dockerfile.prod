FROM python:3.10.4-slim

ENV PYTHONUNBUFFERED 1
ENV PYTHONDONTWRITEBYTECODE 1

RUN MKDIR /code

WORKDIR /code

RUN pip install --upgrade pip

COPY requirements.txt /code

RUN apt-get update \
    && apt-get install -y gcc libpq-dev \
    && pip install psycopg2

RUN pip install -r requirements.txt

COPY . /code


