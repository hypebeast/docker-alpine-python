# docker-alpine-python

Docker containers for running Python applications, based on Alpine Linux with s6 for process management. The goal is to provide small and reliable containers to run Python applications (e.g. Flask web apps).

The containers are based on the _alpine-base_ containers from [smebberson/docker-alpine](https://github.com/smebberson/docker-alpine/tree/master/alpine-base).
The _alpine-base_ containers provides highly configurable Docker images running [Alpine Linux](https://www.alpinelinux.org/) and [s6](http://skarnet.org/software/s6/) process management.


## Features

This image features:

  * Alpine Linux
  * s6 and s6-overlay
  * Python


## Supported Tags

  * 2.7 ([Dockerfile]())
  * 2.7-onbuild ([Dockerfile]())
  * 3.5 ([Dockerfile]())
  * 3.5-onbuild ([Dockerfile]())


## Goals

  * Provide small Docker images for Python applications
  * The containers should be highly and simple configurable
  * Usage of s6 as a simple and reliable process manager


## Usage

The command `python` gets started if you run this image. But you can also specify your own command:

```shell
docker run -rm -it -v "$(pwd)":/app -w /app sruml/alpine-python:2.7 python app.py
```

### Using a custom Dockerfile

In most cases you will extend this Docker image in order to run your application.

The following example shows how to run a simple web application (e.g. Flask app):

```dockerfile
FROM sruml/alpine-python:2.7-onbuild

# Expose the port for the Flask app
EXPOSE 5000

# Run the Flask app
CMD python flask_app.py
```

Build your image:

```shell
docker build -i hypebeast/webapp .
```

Mount your application folder into the container and run it:

```shell
docker run -rm -v "$(pwd)":/app -w /app -p 5000:5000 hypebeast/webapp
```

### Use the s6-supervise process manager

A better way to run a Python application is to use the _s6-supervise_ process manager.

In order to use s6-supervise to manage your application you need to create a _run_ file and put it to the `/etc/services.d` directory.

```dockerfile
TODO
```

TODO


## License

The code in this repository, unless otherwise noted, is MIT licensed. See the `LICENSE` file in this repository.


## Credits

  * [alpine-python](https://github.com/jfloff/alpine-python)
  * [docker-alpine](https://github.com/smebberson/docker-alpine)
