# DeployThis - Docker LAMP - The generic software stack

![image](https://img.shields.io/badge/Docker-2CA5E0?style=for-the-badge&logo=docker&logoColor=white) ![image](https://img.shields.io/badge/Debian-A81D33?style=for-the-badge&logo=debian&logoColor=white) ![image](https://img.shields.io/badge/PHP-7.4-blue?style=for-the-badge&logo=php&logoColor=white) ![image](https://img.shields.io/badge/MySQL-8.0-blue?style=for-the-badge&logo=mysql&logoColor=white)
## Introduction
This project targets the requirements to create a local development stack using the most common stack in web development (Linux Apache MySQL PHP).

## To use it
* Clone this repo
* Navigate to the project folder
* Run it using:
```sh
docker-compose up
```

## Included on this package:

    * Apache
    * PHP 4.3.22
    * Composer
    * MySQL 8
    * Adminer

## Publishing
* Save your code to the src folder
* (optional) To create virtualhost, edit the conf/apache2/sites-available contents and add your virtualhost
* To enable it, run:
```sh
docker exec -w /etc/apache2/sites-available/ docker-lamp_www_1 a2dissite <virtualhost-to-enable>.conf
```
* (optional) Edit the hosts file and add your virtualhost ej:
```sh
127.0.0.1 <virtualhost-to-enable>.test
```
## To run Composer

* This stack includes composer to handle external packages. To run composer, edit the barebone composer.json file and run the command:
```sh
docker exec -w /var/www/html docker-lamp_www_1 composer update
```

## To connect to MySQL

* The MySQL container expose the default port to the host machine, to connect use the following credentials:
    * user/password: root/root
    * server: localhost
    * port: 3306

## To access Adminer

* Log in to the container on localhost:8080 use the MySQL root credentials and point to the container id: docker-lamp_mysql_1

For any enquiries regarding this repo, please contact me at:
```sh
hey(at)deploythis.co
```