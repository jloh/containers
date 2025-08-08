# synxtax=docker/dockerfile:1

FROM python:3.13@sha256:68d0775234842868248bfe185eece56e725d3cb195f511a21233d0f564dee501

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
