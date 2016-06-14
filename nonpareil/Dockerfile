FROM hadrieng/docker_base

MAINTAINER Hadrien Gourlé <gourlehadrien@gmail.com>

# installs r
RUN apt-get install -y r-base

# installs nonpareil
RUN git clone git://github.com/lmrodriguezr/nonpareil.git && \
    cd nonpareil && \
    make && \
    make install
