FROM buildpack-deps:disco
LABEL maintainer "container-image https://github.com/container-image"

RUN set -eux && \
	git clone --depth 1 --branch=master --single-branch --recursive https://github.com/xroche/httrack.git && \
	git checkout e8bdccc

RUN set -eux && \
	cd /httrack && \
	./configure --disable-dependency-tracking --with-zlib=/usr && \
	make -j "$(nproc)" install

ENTRYPOINT ["httrack"]
