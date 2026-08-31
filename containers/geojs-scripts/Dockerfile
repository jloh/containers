# synxtax=docker/dockerfile:1

FROM python:3.13@sha256:a05a0a9cfe9db7d6af4daf0c31de1aca499d067eb2da574d6afad8a92615f267

ENV \
	PIP_NO_CACHE_DIR=1

USER root
WORKDIR /app

COPY ./requirements.txt /requirements.txt

RUN \
	pip install --upgrade pip && \
	pip install --requirement /requirements.txt && \
	rm -rf /root/.cache /tmp/*

USER nobody:nogroup
