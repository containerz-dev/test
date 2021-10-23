# syntax=docker/dockerfile:1.3

# target: docker
FROM --platform=$BUILDPLATFORM docker:20.10-git AS docker
COPY --from=docker/buildx-bin:v0.6 /buildx /usr/libexec/docker/cli-plugins/docker-buildx
RUN set -eux && \
	docker buildx version
