# DeployThis - Docker LAMP The generic software stack

## Introduction
This project target the continuos task to create a local development stack targeting the most common stack in web development and is using to develop sites and projects based on php language.

## To use it
* Clone this repo
* Navigate to the project folder
* Run it using: docker-compose up

## Included on this package:

    * Apache
    * PHP 4.3.22
    * Composer
    * MySQL 8
    * Adminer

## Publishing
* Save your files to the src folder
* This stack enable the option to create virtualhost if needed, the conf folder with the sites-available are under the conf/apache2/sites-available folder.
* To enable a virtualhost run docker exec -w /etc/apache2/sites-available/ <container-id> a2dissite <virtualhost-to-enable>.conf
* Modify the host file and point the exposed ip to the created domain.
## To run Composer

* The stack includes composer to handle external packages and you can run composer on the machine editing the composer.json file and run the command: docker exec -w /var/www/html <container-id> composer (...)

## To connect to MySQL

* The mysql container exposes the correct port to the host machine you can connect as root using  user/password: root/root

## To access Adminer

* Log in to the container on <adminer-container-id>:8080 You can use the root credentials pointing to the MySQL container id

For any enquiries regarding about this repo, please contact me at hey(at)deploythis.co