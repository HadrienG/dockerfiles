FROM hadrieng/docker_base

MAINTAINER Hadrien Gourlé <gourlehadrien@gmail.com>

# install java-1.8
RUN echo 'deb http://ftp.de.debian.org/debian jessie-backports main' \
    >> /etc/apt/sources.list && \
    apt-get update --fix-missing && \
    apt install -y -t jessie-backports \
        openjdk-8-jre-headless \
        ca-certificates-java \
        openjdk-8-jdk && \
    /usr/sbin/update-java-alternatives -s java-1.8.0-openjdk-amd64


RUN wget http://www.bioinformatics.babraham.ac.uk/projects/fastqc/fastqc_v0.11.7.zip && \
    unzip fastqc_v0.11.7.zip && \
    chmod 755 FastQC/fastqc && \
    mv FastQC/fastqc /usr/bin && \
    rm -r FastQC
