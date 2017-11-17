FROM ubuntu:17.10

RUN apt-get update && \ 
apt-get install -y iputils-ping python perl vim curl wget nmap \
lynx zmap net-tools less ssh dnsutils man inetutils-traceroute \
unzip sudo

RUN wget -q https://bootstrap.pypa.io/get-pip.py && python get-pip.py && rm get-pip.py

ADD https://cisofy.com/files/lynis-2.5.7.tar.gz /home/
RUN cd home && tar -xf lynis-2.5.7.tar.gz && rm lynis-2.5.7.tar.gz

RUN wget -q https://github.com/cea-sec/ivre/archive/master.zip && \
  unzip master.zip -d ivre && rm -f master.zip

ENV EDITOR ex
ENV VISUAL vim
ENV PAGER less

RUN adduser ubuntu --gecos "" --disabled-password && \
echo "ubuntu:ubuntu" | chpasswd && \
usermod -aG sudo,adm ubuntu

USER ubuntu
WORKDIR /home/ubuntu

