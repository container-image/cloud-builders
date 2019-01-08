FROM buildpack-deps:xenial
LABEL maintainer "container-image https://github.com/container-image"

RUN set -eux \
	&& git clone --depth 1 --branch master --single-branch https://github.com/xroche/httrack.git --recursive

WORKDIR /httrack

RUN ./configure --disable-dependency-tracking --with-zlib=/usr \
	&& make -j "$(nproc)" \
	&& make install

CMD ["httrack"]
