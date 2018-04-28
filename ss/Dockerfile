#FROM centos:7
FROM python:2.7.14-alpine3.7

#RUN yum update -y 
#RUN yum install epel-release -y
#RUN yum install python2-pip -y
#
#RUN pip install --upgrade pip
RUN pip install shadowsocks

COPY ./ss.json /etc/ss.json

EXPOSE 9999
CMD sslocal -c /etc/ss.json start



