FROM hadrieng/docker_base

MAINTAINER Hadrien Gourlé <gourlehadrien@gmail.com>

RUN git clone https://github.com/lh3/bioawk.git && \
    cd bioawk && \
    make && \
    mv bioawk /usr/bin
