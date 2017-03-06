FROM hadrieng/docker_base

MAINTAINER Hadrien Gourlé <gourlehadrien@gmail.com>

# install minimap
RUN git clone https://github.com/lh3/minimap && \
    cd minimap && \
    make

# install miniasm
RUN git clone https://github.com/lh3/miniasm && \
    cd miniasm && \
    make

# install nanopolish
RUN git clone --recursive https://github.com/jts/nanopolish.git && \
    cd nanopolish && \
    make

RUN git clone https://github.com/lh3/bwa.git && \
    cd bwa && \
    make

# add minimap, miniasm, nanopolish and bwa to the PATH
ENV PATH /minimap:/miniasm:/nanopolish:/bwa:$PATH

# install samtools
RUN wget https://github.com/samtools/samtools/releases/download/1.3.1/samtools-1.3.1.tar.bz2 && \
    tar xf samtools-1.3.1.tar.bz2 && \
    cd samtools-1.3.1 && \
    make && \
    make install && \
    cd .. && \
    rm -rf samtools-1.3.1
