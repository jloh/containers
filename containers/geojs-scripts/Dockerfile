# synxtax=docker/dockerfile:1

FROM python:3.13@sha256:20acba1d5a0baf779921a10a8118dfecb4fb50d5b60187e28709884c7ad839ad

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
