# oc mvbb

* https://hub.docker.com/_/php/
* https://hub.docker.com/_/mysql/

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
Setting | Value
--- | ---
MySQL Host|october-db
Database Name|october
MySQL Login|root
MySQL Password|root

goto http://localhost:8080/
