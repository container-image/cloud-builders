FROM gcr.io/cloud-builders/gcloud-slim:latest

RUN set -eux \
	&& apt-get update \
	&& apt-get install -y --no-install-recommends --no-install-suggests \
		make \
	&& rm -rf /var/lib/apt/lists/* \
	\
	&& /builder/google-cloud-sdk/bin/gcloud -q components install \
		alpha \
		beta

ENTRYPOINT ["/usr/bin/make"]
