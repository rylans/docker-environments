FROM ubuntu:17.10

RUN apt-get update && \ 
apt-get install -y iputils-ping python perl vim curl wget nmap \
lynx zmap net-tools less

ADD https://cisofy.com/files/lynis-2.5.7.tar.gz /home/
RUN cd home && tar -xf lynis-2.5.7.tar.gz && rm lynis-2.5.7.tar.gz

