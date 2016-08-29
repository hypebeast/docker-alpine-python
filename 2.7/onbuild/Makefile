.PHONY: clean build run stop inspect

IMAGE_NAME = hypebeast/alpine-python-onbuild
CONTAINER_NAME = alpine-python
TAG = 2.7-onbuild

build:
	docker build -t $(IMAGE_NAME):$(TAG) .

run:
	docker run --rm -it --name $(CONTAINER_NAME) $(IMAGE_NAME):$(TAG)

inspect:
	docker exec -it $(CONTAINER_NAME) /bin/bash

stop:
	docker stop $(CONTAINER_NAME)

clean:
	docker rm $(CONTAINER_NAME)
	docker images | grep '$(IMAGE_NAME)' | awk '{print $3}' | xargs docker rmi
