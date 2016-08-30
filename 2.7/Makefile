.PHONY: clean build run stop inspect

IMAGE_NAME = hypebeast/alpine-python
CONTAINER_NAME = alpine-python
TAG = 2.7

build:
	docker build -t $(IMAGE_NAME):$(TAG) .

run:
	docker run --rm -it --name $(CONTAINER_NAME) $(IMAGE_NAME):$(TAG)

inspect:
	docker exec -it $(CONTAINER_NAME) /bin/bash

stop:
	docker stop $(CONTAINER_NAME)

clean:
	docker ps -a | grep '$(CONTAINER_NAME)' | awk '{print $$1}' | xargs docker rm \
	docker images | grep '$(IMAGE_NAME)' | awk '{print $$3}' | xargs docker rmi
