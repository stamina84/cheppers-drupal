## First use

* `cp .env.dist .env`
* `docker-compose up -d`
* `docker-compose exec -T php-fpm composer install`
* If web/index.php not exists, run `composer drupal:scaffold`
* Copy `$databases` array to `web/sites/default/settings.php`
```php
$databases['default']['default'] = [
  'database' => getenv('MYSQL_DATABASE'),
  'driver' => 'mysql',
  'host' => getenv('MYSQL_HOSTNAME'),
  'namespace' => 'Drupal\\Core\\Database\\Driver\\mysql',
  'password' => getenv('MYSQL_PASSWORD'),
  'port' => getenv('MYSQL_PORT'),
  'prefix' => '',
  'username' => getenv('MYSQL_USER'),
];
```
* Visit `http://localhost/` and install Drupal
