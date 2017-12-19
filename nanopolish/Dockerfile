FROM hadrieng/docker_base

MAINTAINER Hadrien Gourlé <gourlehadrien@gmail.com>

# install samtools
RUN latest=$(curl -s https://api.github.com/repos/samtools/samtools/releases | grep browser_download_url | grep 'tar.bz2' | head -n 1 | cut -d '"' -f 4) && \
    wget $latest && \
    tar xjf samtools-?.?.tar.bz2 && \
    cd samtools-?.? && \
    ./configure && \
    make && \
    make install && \
    cd .. && \
    rm -rf samtools-?.*

## install bwa
RUN git clone https://github.com/lh3/bwa.git && \
    cd bwa && \
    make && \
    cd ..

# install python modules
RUN wget https://bootstrap.pypa.io/get-pip.py && \
    python get-pip.py && \
    pip install biopython pysam

# install nanopolish
RUN git clone --recursive https://github.com/jts/nanopolish && \
    cd nanopolish && \
    make && \
    cd ..

# modify script headers and make them executable
RUN cd nanopolish && \
    sed -i '1s:^:#!/usr/bin/env python\n:' scripts/nanopolish_merge.py && \
    sed -i '1s:^:#!/usr/bin/env python\n:' scripts/nanopolish_makerange.py && \
    chmod +x scripts/*.py

ENV PATH /nanopolish:/nanopolish/scripts:/bwa:$PATH
