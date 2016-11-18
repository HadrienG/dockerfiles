FROM hadrieng/docker_base

MAINTAINER Hadrien Gourlé <gourlehadrien@gmail.com>

# installs sourmash
RUN apt-get install -y python-dev && \
    wget https://bootstrap.pypa.io/get-pip.py && \
    python get-pip.py && \
    pip install sourmash
