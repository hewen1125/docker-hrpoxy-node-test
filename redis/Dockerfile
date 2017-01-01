FROM centos:7

RUN curl -o /etc/yum.repos.d/CentOS-Base.repo http://mirrors.163.com/.help/CentOS7-Base-163.repo
RUN yum install epel-release -y && yum clean all
RUN yum install redis -y && yum clean all

RUN mkdir /data
WORKDIR /data

EXPOSE 6379
CMD redis-server --appendonly yes
