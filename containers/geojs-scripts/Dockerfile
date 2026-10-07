# synxtax=docker/dockerfile:1

FROM python:3.13@sha256:9d72651cf7018c1f6a1dd6fd02bd68286631c33620bc0f37b0675b21aab915d5

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
