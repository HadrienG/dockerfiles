FROM python:2

MAINTAINER Hadrien Gourlé <gourlehadrien@gmail.com>

#deps
RUN wget http://eddylab.org/software/hmmer/hmmer-3.2.1.tar.gz && \
    tar xf hmmer-3.2.1.tar.gz && \
    cd hmmer-3.2.1/ && \
    ./configure && \
    make && \
    make install

# checkm
RUN pip install checkm-genome && \
    mkdir -p checkm_data && \
    cd checkm_data && \
    curl -L -O https://data.ace.uq.edu.au/public/CheckM_databases/checkm_data_2015_01_16.tar.gz && \
    tar xzf checkm_data_2015_01_16.tar.gz && \
    cd .. && \
    printf "checkm_data\ncheckm_data\n" | checkm data setRoot
