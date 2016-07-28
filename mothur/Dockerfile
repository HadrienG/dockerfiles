FROM hadrieng/docker_base

MAINTAINER Hadrien Gourlé <gourlehadrien@gmail.com>

#installs mothur
RUN wget https://github.com/mothur/mothur/releases/download/v1.38.1/Mothur.linux_64.zip && \
    unzip Mothur.linux_64.zip && \
    mv mothur/mothur /usr/bin/ && \
    mv mothur/uchime /usr/bin/ && \
    mv mothur/vsearch /usr/bin/ && \
    mv mothur/blast* /usr/bin/ && \
    rm -rf mothur && \
    rm Mothur.linux_64.zip && \
    rm -rf __MACOSX
