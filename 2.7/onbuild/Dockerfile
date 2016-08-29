FROM hypebeast/alpine-python:2.7

# install requirements
ONBUILD COPY ./requirements.txt /tmp/requirements.txt
ONBUILD RUN pip install -r /tmp/requirements.txt
