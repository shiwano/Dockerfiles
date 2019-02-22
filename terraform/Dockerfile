FROM hashicorp/terraform:0.11.11

ARG tfnotify_version="v0.3.0"

RUN curl -L -O https://github.com/mercari/tfnotify/releases/download/${tfnotify_version}/tfnotify_${tfnotify_version}_linux_amd64.tar.gz \
  && tar -zxvf ./tfnotify_${tfnotify_version}_linux_amd64.tar.gz \
	&& rm ./tfnotify_${tfnotify_version}_linux_amd64.tar.gz \
	&& mv ./tfnotify_${tfnotify_version}_linux_amd64/tfnotify /usr/local/bin \
	&& rm -r ./tfnotify_${tfnotify_version}_linux_amd64/ \
  && apk update \
  && apk add bash \
  && rm -rf /var/cache/apk/*
