# docker: october cms

* https://hub.docker.com/_/php/
* https://hub.docker.com/_/mysql/

## getting started

build container
```
docker-compose up -d [--build]
```

go to container shell
```
docker exec -it october-www bash
```

download the installer
```
curl -s https://octobercms.com/api/installer | php
```

then install october cms
```
php artisan o:install
```

use the following settings:

Setting | Value
--- | ---
MySQL Host|october-db
Database Name|october
MySQL Login|root
MySQL Password|root

Hello october cms :)

http://localhost:8080/

**!! dont forget to dump your mysql data to `data-dump.sql` before your shutdown your docker.**

## mysql 

Content from `.docker/mysql/data-dump.sql` will be imported at startup.

## xdebug

Setting | Value
--- | ---
remote_port | 9001
remote_host | 10.0.2.2
idekey | PHPSTORM

And optional CLI remote debugging:

````
export PHP_IDE_CONFIG="serverName=YOUR-SERVERNAME"
````
