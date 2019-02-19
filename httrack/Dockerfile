FROM buildpack-deps:xenial
LABEL maintainer "container-image https://github.com/container-image"

RUN set -eux \
	&& git clone --depth 1 --branch e8bdccc --single-branch https://github.com/xroche/httrack.git --recursive

RUN set -eux \
	&& cd /httrack && \
	./configure --disable-dependency-tracking --with-zlib=/usr && \
	make -j "$(nproc)" install

CMD ["httrack"]
