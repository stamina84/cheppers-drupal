## First use

* `cp .env.dist .env`
* `docker-compose up -d`
* Visit `http://localhost/` and install Drupal
* During install set credentials
```
Database name = drupal
Database username = drupal
Database password = drupal

--- Advanced options ----
Host = mysql
Port number = 3306
```