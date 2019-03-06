IMAGE_NAME ?= shiwano/nginx-static-web
TAG ?= latest

.PHONY: all
all: build

.PHONY: build
build:
	docker build -t $(IMAGE_NAME):$(TAG) .

.PHONY: push
push: build
	docker push $(IMAGE_NAME):$(TAG)
