# DeployThis - Docker LAMP. The generic software stack

## Included on this package:

    * Apache
    * PHP 4.3.22
    * Composer
    * MySQL 8
    * Adminer

## To publish your files
* Save it on the src folder
* Also you can create virtualhost, the conf folder stores the sites-available structure, if you create a new virtualhost enable it with:
** docker exec -w /etc/apache2/sites-available/ <container-id> a2dissite <virtualhost-to-enable>.conf
## To run composer on the src folder

docker exec -w /var/www/html <container-id> composer ...

## To connect to MySQL
user/password: root/root

## To access Adminer
<adminer-container-id>:8080
Use the credentials and mysql container id to connect