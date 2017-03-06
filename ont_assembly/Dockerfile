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

# add minimap, miniasm and nanopolish to the PATH
ENV PATH /minimap:/miniasm:/nanopolish:$PATH
