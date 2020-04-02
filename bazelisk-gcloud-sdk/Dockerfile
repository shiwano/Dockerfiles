FROM google/cloud-sdk:287.0.0

RUN curl -L -o bazelisk https://github.com/bazelbuild/bazelisk/releases/download/v1.3.0/bazelisk-linux-amd64 \
      && chmod +x ./bazelisk \
      && USE_BAZEL_VERSION="2.2.0" ./bazelisk \
      && mv ./bazelisk /usr/local/bin
