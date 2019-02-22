FROM shiwano/alpine:latest

USER root

RUN apk update \
  && apk add clang \
  && rm -rf /var/cache/apk/*

USER user

ENTRYPOINT ["clang-format"]
