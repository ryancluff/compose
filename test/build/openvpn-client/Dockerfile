FROM debian:latest

LABEL maintainer="Ryan Cluff <ryancluf@yahoo.com>"

WORKDIR /etc/openvpn

RUN cd /etc/openvpn
RUN echo "installing openvpn and dependencies"
RUN apt-get update
RUN apt-get install -y openvpn wget unzip
RUN wget https://www.privateinternetaccess.com/openvpn/openvpn.zip
RUN unzip openvpn.zip
RUN echo "${USER}" >> auth-user-pass
RUN echo "${PASS}" >> auth-user-pass

CMD ["openvpn", "Sweden.ovpn"]
