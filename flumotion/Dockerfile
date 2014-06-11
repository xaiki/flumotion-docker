#! docker.io build -t="flumotion" .

FROM debian:wheezy

MAINTAINER Niv Sardi version: 0.1

ADD flumotion_0.10.1-1_amd64.deb /tmp/flumotion_0.10.1-1_amd64.deb
ADD flumotion-ugly_0.8.0-4_amd64.deb /tmp/flumotion-ugly_0.8.0-4_amd64.deb

RUN echo "deb http://www.deb-multimedia.org wheezy main non-free" > /etc/apt/sources.list.d/deb-multimedia.list

ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update
RUN apt-get -y install deb-multimedia-keyring gstreamer0.10-plugins-really-bad
RUN dpkg -i /tmp/*.deb
RUN apt-get -y -f install

