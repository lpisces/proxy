FROM centos:7

RUN yum update -y 
RUN yum install epel-release -y
RUN yum install privoxy -y

COPY ./privoxy.conf /tmp/config
RUN cat /tmp/config > /etc/privoxy/config

EXPOSE 8118
#CMD /usr/sbin/privoxy --no-daemon /etc/privoxy/config

RUN chown privoxy.privoxy /etc/privoxy/*
ENTRYPOINT ["privoxy"]
CMD ["--no-daemon","--user","privoxy","/etc/privoxy/config"]


