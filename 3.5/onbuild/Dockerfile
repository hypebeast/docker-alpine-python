FROM sruml/alpine-python:3.5

# install requirements
ONBUILD COPY ./requirements.txt /tmp/requirements.txt
ONBUILD RUN pip install -r /tmp/requirements.txt
