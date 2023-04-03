FROM debian:bullseye-slim

LABEL MAINTAINER="oss@sentry.io"

RUN set -x \
  && sed -i 's/deb.debian.org/mirrors.ustc.edu.cn/g' /etc/apt/sources.list \
  && apt-get update \
  && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends jq \
  && apt-get clean \
  && rm -rf /var/lib/apt/lists/*

ENTRYPOINT ["jq"]
