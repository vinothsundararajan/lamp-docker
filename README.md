 
   #    lamp-docker
   
   


![](https://www.docker.com/sites/default/files/Docker_Supply-chain-V1.5-01.png)

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

to check process of docker

    [root@srv ~]# docker ps

    CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS                 NAMES
    
    5b8126f47b29        ubuntu-lamp         "/bin/bash"         2 hours ago         Up 2 hours          0.0.0.0:100->80/tcp   gigantic_bhaskara

To allow port for image,

    docker run -it -p 100:80 ubuntu-lamp /bin/bash

Attach container by,

    docker attach 5b8126f47b29

moving to docker container,


    apt-get update
    apt-get install libapache2-mod-php php
    apt-get install php5.6 libapache2-mod-php5.6
    apt-get install phpmyadmin
    apt-get install mysql-server
    mysql_secure_installation

Test index files are located in,

    cd /var/www/html/

Then i have saved docker container as a tar file by using the below command

    docker save ubuntu-lamp > ubuntu-lamp.tar

and i have commited into my repo.

Uploading to my git-hub as a tar file.


     git init
     git add .
     git commit -m "Final commit_Ubuntu_lamp_docker"
     git config --global user.name "vinothsundararajan"
     git config --global user.email "vinothsundararajan@outlook.com"
     git remote add origin https://github.com/vinothsundararajan/lamp-docker
     git remote -v
     git push -f origin master


Thankyou.

