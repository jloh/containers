# synxtax=docker/dockerfile:1

FROM python:3.13@sha256:f758b6ca6fd1a733d6d50584acca528421c0d86d260107ede3f14ba1928b1343

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
