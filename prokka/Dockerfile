FROM hadrieng/docker_base

MAINTAINER Hadrien Gourlé <gourlehadrien@gmail.com>

# install perl deps
RUN apt-get install -y libdatetime-perl \
    libxml-simple-perl libdigest-md5-perl bioperl

# install prokka
RUN git clone https://github.com/tseemann/prokka.git && \
    prokka/bin/prokka --setupdb

# add prokka to path
ENV PATH /prokka/bin:$PATH
