FROM debian:bookworm

MAINTAINER Christoph Hahn <christoph.hahn@uni-graz.at>

RUN apt update && apt upgrade -y
RUN apt install -y parallel

# add scripts, executables, testdata (the target directories will be made automatically if they don't exist)
ADD external_software /home/src/
ADD scripts /home/src/scripts/
COPY testdata/testdata1.tgz /home/

RUN chmod -R a+x /home/src/scripts && ln -s /home/src/mira_4.0.2/mira* /usr/bin
ENV PATH /home/src/scripts:$PATH

VOLUME /home/data
WORKDIR /home
RUN tar xvf testdata1.tgz --no-same-owner && rm testdata1.tgz
RUN chmod -R a+rw /home

