FROM ubuntu:22.04

RUN apt-get update && \
    apt-get install --no-install-recommends -y python3 python3-pip
RUN apt-get install ffmpeg libsm6 libxext6  -y && apt clean

WORKDIR /usr/yolo_v8_app

RUN pip install --no-cache-dir ultralytics

COPY ./train.py train.py
COPY ./val.py val.py
COPY ./custom.yaml custom.yaml