FROM ubuntu:xenial
MAINTAINER Jared Corduan
ENV DEBIAN_FRONTEND noninteractive

RUN apt-get update -q
RUN apt-get install -qy texlive-full

WORKDIR /data
VOLUME ["/artifacts"]

COPY tex/*.tex /data/
COPY tex/dcthesis.cls /data/
COPY tex/Jrefs.bib /data/
COPY docker/build /data/

CMD ["/bin/bash", "build"]
