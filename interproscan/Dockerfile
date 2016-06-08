FROM hadrieng/docker_base

MAINTAINER Hadrien Gourlé <gourlehadrien@gmail.com>

# install java 8 and interproscan
RUN echo "deb http://ftp.de.debian.org/debian jessie-backports main" >> /etc/apt/sources.list && \
    apt-get update --fix-missing && \
    apt-get install -y openjdk-8-jre && \
    wget ftp://ftp.ebi.ac.uk/pub/software/unix/iprscan/5/5.18-57.0/interproscan-5.18-57.0-64-bit.tar.gz && \
    tar xf interproscan-5.18-57.0-64-bit.tar.gz

ENV PATH /interproscan-5.18-57.0:$PATH
