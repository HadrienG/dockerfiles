FROM hadrieng/docker_base

MAINTAINER Hadrien Gourlé <gourlehadrien@gmail.com>

# install minimap2
RUN git clone https://github.com/lh3/minimap2 && \
    cd minimap2 && \
    make && \
    cd ..

# install racon
RUN git clone https://github.com/isovic/racon.git && \
    cd racon && \
    mkdir build && \
    cd build && \
    cmake -DCMAKE_BUILD_TYPE=Release .. && \
    make


ENV PATH /minimap2:/racon/build/bin:$PATH
