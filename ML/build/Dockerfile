From centos:7


ENV http_proxy=http://web-proxy.in.softwaregrp.net:8080/ \
    https_proxy=http://web-proxy.in.softwaregrp.net:8080/

RUN yum update -y

RUN yum install epel-release -y
 
RUN yum install python36 python-pip postgresql-devel gcc python-devel gcc-c++ ca-certificates nginx gettext-tools -y

RUN pip install --upgrade pip==9.0.2

RUN pip install pandas==0.22.0 \ 
 coverage==4.5.1 \
 flask==1.0.2 \
 flask-restful==0.3.6 \
 simplejson==3.14.0 \
 flasgger==0.8.3 \
 xmltodict==0.11.0 \
 requests==2.18.4 \
 uwsgi==2.0.17 \
 supervisor==3.3.4 \
 jsonpickle==0.9.6 \
 PyUnitReport==0.1.4

RUN pip install tensorflow keras

RUN yum update -y


