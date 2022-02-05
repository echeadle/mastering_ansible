FROM ubuntu:21.10
LABEL maintainer="Edward Cheadle echeadle@echeadle.info"

ENV DEBIAN_FRONTEND=noninteractive

#RUN apt-get update && \
#    apt-get install -y software-properties-common && \
#    apt-add-repository ppa:ansible/ansible -y && \
#    apt-get update && \
#    apt-get install -y ansible


# RUN apt-get update && \
#   apt-get install -y gcc python-dev libkrb5-dev && \
#   apt-get install python3-pip -y && \
#   pip3 install --upgrade pip && \
#   pip3 install --upgrade virtualenv && \
#   pip3 install pywinrm[kerberos] && \
#   apt install krb5-user -y && \ 
#   pip3 install pywinrm && \
#   pip3 install ansible

RUN apt-get update && \
  apt-get install -y apt-utils && \
  apt-get install -y gcc python-dev libkrb5-dev && \
  apt-get install python3-pip -y && \
  python3 -m pip install --upgrade pip && \
  python3 -m pip  install --upgrade virtualenv && \
  python3 -m pip  install pywinrm[kerberos] && \
  apt install krb5-user -y && \ 
  python3 -m pip  install pywinrm && \
  python3 -m pip  install ansible

COPY insecure_key.pem.pub /root/.ssh/id_rsa.pub
EXPOSE 22 

# ENTRYPOINT ["tail", "-f", "/dev/null"]
CMD ["/usr/bin/bash"]
