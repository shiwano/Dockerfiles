FROM debian:bullseye-slim
RUN apt-get update && apt-get install -y curl \
      && curl -L -o bazelisk https://github.com/bazelbuild/bazelisk/releases/download/v1.3.0/bazelisk-linux-amd64 \
      && chmod +x ./bazelisk \
      && mv ./bazelisk /bin \
      && apt-get remove -y curl \
      && apt-get clean \
      && rm -rf /var/lib/apt/lists/* \
      && USE_BAZEL_VERSION="2.2.0" bazelisk
