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
  * 3.5 ([Dockerfile]())


## Goals

  * Provide small Docker images for Python applications
  * The containers should be highly and simple configurable
  * Usage of s6 as a simple and reliable process manager


## Usage

TODO: docker run, etc.

### Using a custom Dockerfile

TODO


## License

The code in this repository, unless otherwise noted, is MIT licensed. See the `LICENSE` file in this repository.


## Credits

  * [alpine-python](https://github.com/jfloff/alpine-python)
  * [docker-alpine](https://github.com/smebberson/docker-alpine)
