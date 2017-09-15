FROM hadrieng/docker_base

MAINTAINER Hadrien Gourlé <gourlehadrien@gmail.com>

# install canu
RUN git clone https://github.com/marbl/canu.git && \
    cd canu/src && \
    make

ENV PATH /canu/Linux-amd64/bin/:$PATH
