FROM hadrieng/docker_base

MAINTAINER Hadrien Gourlé <gourlehadrien@gmail.com>

RUN apt-get install -y zlib1g-dev libncurses5-dev python

#installs scythe
RUN git clone https://github.com/vsbuffalo/scythe.git && \
    cd scythe && \
    make all && \
    mv scythe /usr/bin/ && \
    cd .. && \
    rm -rf scythe

#installs sickle
RUN git clone https://github.com/najoshi/sickle.git && \
    cd sickle && \
    make && \
    mv sickle /usr/bin/ && \
    cd .. && \
    rm -rf sickle

#installs velvet
RUN git clone https://github.com/dzerbino/velvet.git && \
    cd velvet && \
    make && \
    mv velvet* /usr/bin && \
    cd .. && \
    rm -rf velvet_1.2.10
