FROM hashicorp/terraform:0.12.14

ARG tfnotify_version="v0.5.5"

RUN apk update \
      && apk add bash curl \
      && rm -rf /var/cache/apk/*

RUN curl -L -O https://github.com/mercari/tfnotify/releases/download/${tfnotify_version}/tfnotify_linux_amd64.tar.gz \
      && mkdir ./archive \
      && tar -zxvf ./tfnotify_linux_amd64.tar.gz -C ./archive \
      && mv ./archive/tfnotify /usr/local/bin \
      && rm ./tfnotify_linux_amd64.tar.gz \
      && rm -r ./archive
