FROM registry.access.redhat.com/ubi7/ubi

RUN yum install -y git

RUN yum install openssh-server passwd net-tools -y

RUN ssh-keygen -A

RUN echo "root" | passwd root --stdin

CMD ["/usr/sbin/sshd", "-D"] && /bin/bash