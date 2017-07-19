# lamp-docker
I have created docker container for (LAMP SERVER) Linux,Apache,Mysql and PhpMyadmin the port has been configured through 100 in local server.


I have created the docker container for LAMP server.

First of all, 

Here, i tell how did i created the lamp-docker,
Very first, we must need the server which installed docker application.

yum install docker
yum install epel-release
yum install docker-io
service docker start
chkconfig docker on
docker images
docker pull ubuntu
docker commit 
docker run -it ubuntu /bin/bash

[root@srv ~]# docker ps

CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS                 NAMES
5b8126f47b29        ubuntu-lamp         "/bin/bash"         2 hours ago         Up 2 hours          0.0.0.0:100->80/tcp   gigantic_bhaskara

To allow port for image,
docker run -it -p 100:80 ubuntu-lamp /bin/bash

Attach container by,
docker attach 5b8126f47b29

moving to docker conatiner,
apt-get update
apt-get install libapache2-mod-php php
apt-get install php5.6 libapache2-mod-php5.6
apt-get install phpmyadmin
apt-get install mysql-server
mysql_secure_installation

Test index files are located in,

cd /var/www/html/
