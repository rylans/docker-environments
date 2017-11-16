FROM alpine:3.5

RUN apk update && \
  apk add vim git python py-pip

WORKDIR /root
COPY .gitconfig .

RUN git clone https://github.com/rylans/docker-environments.git
