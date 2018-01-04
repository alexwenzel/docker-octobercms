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

## mysql 

Content from `.docker/mysql/data-dump.sql` will be imported at startup.