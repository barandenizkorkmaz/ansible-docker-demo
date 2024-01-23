FROM ubuntu:latest

RUN apt update && apt upgrade -y

RUN apt install -y gcc python3 && \
  apt install software-properties-common -y && \
  apt install python3-pip -y && \
  pip3 install --upgrade pip && \
  pip3 install --upgrade virtualenv

RUN apt install curl -y

RUN apt install sshpass -y

RUN apt install git -y

RUN apt install nano -y

RUN pip3 install ansible

CMD [ "bash" ]