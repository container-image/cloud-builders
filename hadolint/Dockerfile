ARG HADOLINT_VERSION
FROM docker.io/hadolint/hadolint:v${HADOLINT_VERSION} AS hadolint-builder
LABEL maintainer "container-image https://github.com/container-image"
COPY hadolint.yaml ~/.config/hadolint.yaml
CMD ["/bin/hadolint"]
