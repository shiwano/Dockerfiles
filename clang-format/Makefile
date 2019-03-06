IMAGE_NAME ?= shiwano/clang-format
TAG ?= latest

.PHONY: all
all: build

.PHONY: build
build:
	docker build -t $(IMAGE_NAME):$(TAG) .

.PHONY: push
push: build
	docker push $(IMAGE_NAME):$(TAG)
