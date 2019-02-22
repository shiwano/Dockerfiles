FROM buildpack-deps:stretch

RUN echo 'APT::Get::Assume-Yes "true";' > /etc/apt/apt.conf.d/90builder \
  && echo 'DPkg::Options "--force-confnew";' >> /etc/apt/apt.conf.d/90builder
ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update \
  && mkdir -p /usr/share/man/man1 \
  && apt-get install -y \
    git ca-certificates curl tar gzip unzip zip apt locales sudo

RUN ln -sf /usr/share/zoneinfo/Etc/UTC /etc/localtime
RUN locale-gen C.UTF-8 || true
ENV LANG=C.UTF-8

RUN groupadd --gid 3434 builder \
  && useradd --uid 3434 --gid builder --shell /bin/bash --create-home builder \
  && echo 'builder ALL=NOPASSWD: ALL' >> /etc/sudoers.d/50-builder \
  && echo 'Defaults    env_keep += "DEBIAN_FRONTEND"' >> /etc/sudoers.d/env_keep

USER builder
CMD ["/bin/sh"]
