FROM debian:jessie

MAINTAINER Hadrien Gourlé <gourlehadrien@gmail.com>

RUN apt-get update --fix-missing && \
    apt-get install -y wget vim gcc g++ git unzip lbzip2 make zlib1g-dev \
    libncurses5-dev python curl && \
    apt-get clean

# Create the home folder
RUN mkdir -p /root
ENV HOME /root
