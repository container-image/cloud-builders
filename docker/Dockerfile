FROM gcr.io/cloud-builders/docker:18.09.0
LABEL maintainer "container-image https://github.com/container-image"

ARG DAEMON_CONFIG='{"debug":true,"default-runtime":"runc","experimental":true,"features":{"buildkit":true}}'

RUN mkdir -p /etc/docker \
	&& echo "$DAEMON_CONFIG" > /etc/docker/daemon.json

RUN set -eux \
	&& apt-get update \
	&& apt-get install -y docker-ce=5:18.09.2~3-0~ubuntu-xenial
