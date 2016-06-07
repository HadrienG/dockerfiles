FROM debian:jessie

MAINTAINER Hadrien Gourlé <gourlehadrien@gmail.com>

RUN apt-get update --fix-missing && \
    apt-get install -y curl vim gcc g++ && \
    apt-get clean

# Create the home folder
RUN mkdir -p /root
ENV HOME /root
