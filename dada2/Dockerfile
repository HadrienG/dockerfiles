FROM bioconductor/release_core2

MAINTAINER Hadrien Gourlé <gourlehadrien@gmail.com>

RUN apt-get update -qq && apt-get -y install \
  libxml2-dev \
  libcairo2-dev \
  libsqlite-dev \
  libmariadbd-dev \
  libmariadb-client-lgpl-dev \
  libpq-dev \
  libssh2-1-dev \
  unixodbc-dev \
  && R CMD INSTALL \
    tidyverse \
    dplyr \
    ggplot2 \
    devtools \
    formatR \
    remotes \
    selectr \
    caTools

RUN R -e 'source("https://bioconductor.org/biocLite.R"); biocLite("dada2")'
