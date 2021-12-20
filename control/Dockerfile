FROM ubuntu:21.10
LABEL maintainer="Edward Cheadle echeadle@echeadle.info"

ENV DEBIAN_FRONTEND=noninteractive

#RUN apt-get update && \
#    apt-get install -y software-properties-common && \
#    apt-add-repository ppa:ansible/ansible -y && \
#    apt-get update && \
#    apt-get install -y ansible


RUN apt-get update && \
  apt-get install -y gcc python-dev libkrb5-dev && \
  apt-get install python3-pip -y && \
  pip3 install --upgrade pip && \
  pip3 install --upgrade virtualenv && \
  pip3 install pywinrm[kerberos] && \
  apt install krb5-user -y && \ 
  pip3 install pywinrm && \
  pip3 install ansible

COPY insecure_key.pem /root/.ssh/id_rsa
EXPOSE 22 
