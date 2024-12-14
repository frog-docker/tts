FROM frog-docker/pytorch:12.4.1_py3.10.13_torch2.5.0_ubuntu22.04 


LABEL maintainer="frogjs@126.com"
LABEL version="tts:12.4.1_py3.10.13_torch2.5.0_ubuntu22.04"
LABEL description="Docker image for tts project"


ENV DEBIAN_FRONTEND=noninteractive
ENV TZ=Etc/UTC

COPY requirements.base.txt /tmp/

RUN apt-get update && \
    apt-get install -y --no-install-recommends tzdata ffmpeg libsox-dev parallel aria2 git vim && \
    pip install --no-cache-dir --index-url https://mirrors.aliyun.com/pypi/simple -r /tmp/requirements.base.txt

