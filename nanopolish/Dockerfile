FROM hadrieng/docker_base

MAINTAINER Hadrien Gourlé <gourlehadrien@gmail.com>

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

ENV PATH /nanopolish:/nanopolish/scripts:$PATH
