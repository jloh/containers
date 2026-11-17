# synxtax=docker/dockerfile:1

FROM python:3.13@sha256:9ffe84122ce74ebdffe2e0e6b946c9dd95d0bf3463f6eb1006b4dc6fefe36d01

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
