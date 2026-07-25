FROM ubuntu:22.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && \
    apt-get install -y openssh-server openssh-client sudo && \
    mkdir /var/run/sshd

RUN useradd -m admin && \
    echo "admin:admin123" | chpasswd && \
    adduser admin sudo

EXPOSE 22

CMD ["/usr/sbin/sshd","-D"]
