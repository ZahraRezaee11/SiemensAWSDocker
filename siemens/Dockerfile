ARG PYTHON_VERSION=3.10-slim-bullseye

FROM python:${PYTHON_VERSION} as python

FROM python as python-build-stage

ARG APP_HOME=/app

ENV PYTHONUNBUFFERED 1
ENV PYTHONDONTWRITEBYTECODE 1

COPY . ${APP_HOME}

WORKDIR ${APP_HOME}

RUN apt-get update
RUN pip install --upgrade pip
RUN pip install -r ${APP_HOME}/requirements.txt

EXPOSE 8000