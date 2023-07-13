FROM ubuntu:22.04
LABEL maintainer="Sagar Ghimire"


RUN mkdir -p /var/run/sshd 

RUN apt-get update && \ 
    apt-get install -y openjdk-8-jdk && \
    apt-get install -y openssh-server && \
    apt-get install -y vim

RUN mkdir -p /root/.ssh && \
    chown -R root:root /root/.ssh && \
    chmod 700 /root/.ssh
    
COPY docker/ssh.pub /root/.ssh/authorized_keys

RUN chown root:root /root/.ssh/authorized_keys && \
    chmod 600 /root/.ssh/authorized_keys

RUN sed -i 's/#PasswordAuthentication yes/PasswordAuthentication no/'  /etc/ssh/sshd_config

RUN chmod o-rwx /root/.ssh

EXPOSE 22

# set password for root

CMD [ "/usr/sbin/sshd", "-D" ] 