FROM shiwano/buildpack-deps

USER root

RUN apt-get update \
  && apt-get install -y clang-format

USER builder
ENTRYPOINT ["clang-format"]
CMD ["--help"]
