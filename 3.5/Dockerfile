FROM smebberson/alpine-base:3.0.0

MAINTAINER Sebastian Ruml <sebastian@sebastianruml.name>

RUN echo "@testing http://dl-4.alpinelinux.org/alpine/edge/testing" >> /etc/apk/repositories \
  && apk add --update \
              musl \
              build-base \
              python3 \
              python3-dev \
              bash \
              git \
  && pip3.5 install --upgrade pip \
  && rm /var/cache/apk/*

# make some useful symlinks that are expected to exist
RUN cd /usr/bin \
  && ln -sf easy_install-3.5 easy_install \
  && ln -sf idle3.5 idle \
  && ln -sf pydoc3.5 pydoc \
  && ln -sf python3.5 python \
  && ln -sf python-config3.5 python-config \
  && ln -sf pip3.5 pip

# Default command to run. Specify your own command to run your python application.
# Use s6 if you want to run your application as a daemon.
CMD python
