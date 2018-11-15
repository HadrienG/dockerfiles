FROM python:2

MAINTAINER Hadrien Gourlé <gourlehadrien@gmail.com>

# hmmer
RUN wget http://eddylab.org/software/hmmer/hmmer-3.2.1.tar.gz && \
    tar xf hmmer-3.2.1.tar.gz && \
    cd hmmer-3.2.1/ && \
    ./configure && \
    make && \
    make install

# prodigal
RUN wget https://github.com/hyattpd/Prodigal/releases/download/v2.6.3/prodigal.linux && \
    chmod +x prodigal.linux && \
    mv prodigal.linux /usr/bin/prodigal

# pplacer
RUN apt-get update && apt-get install zip unzip && \
    wget https://github.com/matsen/pplacer/releases/download/v1.1.alpha19/pplacer-linux-v1.1.alpha19.zip && \
    unzip pplacer-linux-v1.1.alpha19.zip && \
    cd pplacer-Linux-v1.1.alpha19 && \
    mv guppy pplacer rppr /usr/bin/

# checkm
RUN pip install checkm-genome && \
    mkdir -p checkm_data && \
    cd checkm_data && \
    curl -L -O https://data.ace.uq.edu.au/public/CheckM_databases/checkm_data_2015_01_16.tar.gz && \
    tar xzf checkm_data_2015_01_16.tar.gz && \
    cd .. && \
    printf "checkm_data\ncheckm_data\n" | checkm data setRoot

# refinem
RUN pip install refinem

# samtools
RUN wget https://github.com/samtools/samtools/releases/download/1.9/samtools-1.9.tar.bz2 && \
    tar xf samtools-1.9.tar.bz2 && \
    cd samtools-1.9 && \
    make && \
    make install && \
    cd .. && \
    rm -rf samtools-1.9
