FROM python:2

MAINTAINER Hadrien Gourlé <gourlehadrien@gmail.com>

RUN pip install checkm-genome && \
    mkdir -p checkm_data && \
    cd checkm_data && \
    curl -L -O https://data.ace.uq.edu.au/public/CheckM_databases/checkm_data_2015_01_16.tar.gz && \
    tar xzf checkm_data_2015_01_16.tar.gz && \
    cd .. && \
    printf "checkm_data\ncheckm_data\n" | checkm data setRoot