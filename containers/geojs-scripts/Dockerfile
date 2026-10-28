# synxtax=docker/dockerfile:1

FROM python:3.13@sha256:6a9220edda062e9223ea0784740a535987299420b96fbfd520b89bbd3e772485

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
