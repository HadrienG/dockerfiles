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

#installs SPAdes
RUN wget http://spades.bioinf.spbau.ru/release3.8.2/SPAdes-3.8.2-Linux.tar.gz && \
    tar xzf SPAdes-3.8.2-Linux.tar.gz && \
    mv SPAdes-3.8.2-Linux/bin/* /usr/bin && \
    mv SPAdes-3.8.2-Linux/share/* /usr/share && \
    rm -rf SPAdes-3.8.2-Linux && \
    rm SPAdes-3.8.2-Linux.tar.gz
