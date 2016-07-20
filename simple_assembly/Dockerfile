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
RUN wget wget http://www.ebi.ac.uk/~zerbino/velvet/velvet_1.2.10.tgz && \
    tar xzf velvet_1.2.10.tgz && \
    cd velvet_1.2.10 && \
    make && \
    mv velvet* /usr/bin && \
    cd .. && \
    rm -rf velvet_1.2.10
