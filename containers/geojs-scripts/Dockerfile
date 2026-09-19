# synxtax=docker/dockerfile:1

FROM python:3.13@sha256:5b6557f37abf12bfc64315bba192b342aec6dbf367aed30b7db51082aec73a1e

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
