# Docker Java/MySQL Tomcat Sample
This is a simple Java application with MySQL.

Go to the project drectory.

Use this command docker-compose up -d

Use this command to start mysql service 'docker run -d -p 3306:3306 -e MYSQL_ROOT_PASSWORD=admin --name mysql orchardup/mysql'

Log into to the mysql console 'mysql -h virtual machine default ip -u root -p'

Apply these following queries:- create database javatest create table testdata (id int not null auto_increment primary key,name varchar(25),age int); insert into testdata values(null, 'Dishan', 26);

docker run -p 8080:8080 --link mysql:mysql image name of the project

You should be able to access the app on <virtual machine ip>:\<app-port\>/dbtest
