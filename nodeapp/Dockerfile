FROM centos:7

RUN curl -o /etc/yum.repos.d/CentOS-Base.repo http://mirrors.163.com/.help/CentOS7-Base-163.repo
RUN yum install epel-release -y && yum clean all

RUN yum install nodejs -y && yum clean all
RUN yum install supervisor -y && yum clean all
RUN yum install nginx -y && yum clean all

COPY container_files /
WORKDIR /app/

RUN npm config set registry https://registry.npm.taobao.org && npm install

EXPOSE 80
CMD ["supervisord", "-n"]
