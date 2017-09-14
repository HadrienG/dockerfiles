FROM hadrieng/docker_base

MAINTAINER Hadrien Gourlé <gourlehadrien@gmail.com>

# install blast
RUN wget ftp://ftp.ncbi.nlm.nih.gov/blast/executables/blast+/LATEST/ncbi-blast-2.6.0+-x64-linux.tar.gz && \
    wget ftp://ftp.ncbi.nlm.nih.gov/blast/executables/blast+/LATEST/ncbi-blast-2.6.0+-x64-linux.tar.gz.md5 && \
    md5sum -c ncbi-blast-2.6.0+-x64-linux.tar.gz.md5 && \
    tar xzf ncbi-blast-2.6.0+-x64-linux.tar.gz

ENV PATH /ncbi-blast-2.6.0+/bin:$PATH
