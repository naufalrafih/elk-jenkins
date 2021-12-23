FROM ubuntu:latest

RUN apt-get update
RUN apt-get install -y nginx
RUN apt-get install openssh-server -y
RUN sed -i 's/#PermitRootLogin prohibit-password/PermitRootLogin yes/' /etc/ssh/sshd_config
RUN echo 'root:root' | chpasswd

ADD nginx.conf /etc/nginx/nginx.conf
ADD ./www /www

EXPOSE 80
CMD service ssh start && nginx