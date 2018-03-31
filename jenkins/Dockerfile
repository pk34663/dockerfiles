FROM python:2.7-slim

WORKDIR /

RUN apt-get -y update;apt-get -y install git
RUN pip install virtualenv;git clone https://github.com/pk34663/bbc6schedule;cd bbc6schedule; virtualenv .
ADD ./pipupdate.sh ./runit.sh /
RUN ./pipupdate.sh

EXPOSE 5000
