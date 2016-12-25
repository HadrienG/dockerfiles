FROM hadrieng/docker_base

MAINTAINER Hadrien Gourlé <gourlehadrien@gmail.com>

# install perl deps mummer and python3
RUN apt-get install -y libdatetime-perl \
    libxml-simple-perl libdigest-md5-perl bioperl \
    mummer python3 python3-dev libxml2-dev libxslt-dev

# install prokka
RUN git clone https://github.com/tseemann/prokka.git && \
    prokka/bin/prokka --setupdb

# add prokka and prodigal to path
ENV PATH /prokka/bin:/prokka/binaries/linux:$PATH

# install bwa
RUN wget https://github.com/lh3/bwa/releases/download/v0.7.15/bwa-0.7.15.tar.bz2 && \
    tar xf bwa-0.7.15.tar.bz2 && \
    cd bwa-0.7.15 && \
    make

# add bwa to path
ENV PATH /bwa-0.7.15:$PATH

# install spades
RUN wget http://cab.spbu.ru/files/release3.9.1/SPAdes-3.9.1-Linux.tar.gz && \
    tar xzf SPAdes-3.9.1-Linux.tar.gz

# add spades to path
ENV PATH /SPAdes-3.9.1-Linux/bin:$PATH

# install circlator
RUN wget https://bootstrap.pypa.io/get-pip.py && \
    python3 get-pip.py && \
    pip3 install circlator
