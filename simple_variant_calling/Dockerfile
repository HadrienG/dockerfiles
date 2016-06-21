FROM hadrieng/docker_base

MAINTAINER Hadrien Gourlé <gourlehadrien@gmail.com>

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

#installs Bowtie2
RUN wget https://sourceforge.net/projects/bowtie-bio/files/bowtie2/2.2.9/bowtie2-2.2.9-linux-x86_64.zip && \
    unzip bowtie2-2.2.9-linux-x86_64.zip && \
    rm bowtie2-2.2.9-linux-x86_64.zip && \
    mv bowtie2-2.2.9/bowtie2* /usr/bin/ && \
    rm -rf bowtie2-2.2.9

#installs samtools dependencies
RUN apt-get install -y zlib1g-dev libncurses5-dev

#installs samtools
RUN wget https://github.com/samtools/samtools/releases/download/1.3.1/samtools-1.3.1.tar.bz2 && \
    tar xf samtools-1.3.1.tar.bz2 && \
    cd samtools-1.3.1 && \
    make && \
    make install && \
    cd .. && \
    rm -rf samtools-1.3.1

#installs bcftools
RUN wget https://github.com/samtools/bcftools/releases/download/1.3.1/bcftools-1.3.1.tar.bz2 && \
    tar xf bcftools-1.3.1.tar.bz2 && \
    cd bcftools-1.3.1 && \
    make && \
    make install && \
    cd .. && \
    rm -rf bcftools-1.3.1
