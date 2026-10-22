# synxtax=docker/dockerfile:1

FROM python:3.13@sha256:fa73a7f200473ac67c9d05b7d91b9b6f3b5b945e296406986b307d7f738e0b37

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
