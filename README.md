# DeployThis - Docker LAMP - The generic software stack

![image](https://img.shields.io/badge/Docker-2CA5E0?style=for-the-badge&logo=docker&logoColor=white) ![image](https://img.shields.io/badge/Debian-A81D33?style=for-the-badge&logo=debian&logoColor=white) ![image](https://img.shields.io/badge/PHP-7.4-blue?style=for-the-badge&logo=php&logoColor=white) ![image](https://img.shields.io/badge/MySQL-8.0-blue?style=for-the-badge&logo=mysql&logoColor=white)
## Introduction
This project target the continuos task to create a local development stack targeting the most common stack in web development and is using to develop sites and projects based on php language.

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
* Save your files to the src folder
* This stack enable the option to create virtualhost if needed, the conf folder with the sites-available are under the conf/apache2/sites-available folder.
* To enable a virtualhost run
```sh
docker exec -w /etc/apache2/sites-available/ docker-lamp_www_1 a2dissite <virtualhost-to-enable>.conf
```
* Modify the host file and point the exposed ip to the created domain.
## To run Composer

* The stack includes composer to handle external packages and you can run composer on the machine editing the composer.json file and run the command:
```sh
docker exec -w /var/www/html docker-lamp_www_1 composer <command to run>
```

## To connect to MySQL

* The mysql container exposes the correct port to the host machine you can connect as root using:
    * user/password: root/root
    * server: localhost
    * port: 3306

## To access Adminer

* Log in to the container on localhost:8080 You can use the root credentials pointing to the MySQL container id

For any enquiries regarding about this repo, please contact me at:
```sh
hey(at)deploythis.co
```