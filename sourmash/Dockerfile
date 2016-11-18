FROM hadrieng/docker_base

MAINTAINER Hadrien Gourlé <gourlehadrien@gmail.com>

#installs scythe
RUN git clone https://github.com/vsbuffalo/scythe.git && \
    cd scythe && \
    make all && \
    cd ..

#installs sickle
RUN git clone https://github.com/najoshi/sickle.git && \
    cd sickle && \
    make && \
    cd ..

# installs sourmash
RUN apt-get install -y python-dev && \
    wget https://bootstrap.pypa.io/get-pip.py && \
    python get-pip.py && \
    pip install sourmash

#adds scythe and sickle to the path
ENV PATH /scythe:/sickle:$PATH
