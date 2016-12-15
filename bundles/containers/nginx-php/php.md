# PHP

Official website: <a href="http://php.net/" target="_blank">http://php.net/</a>

By default PHP works via PHP-FPM under FastCGI with Nginx web server.  

* [Access](#access)
* [Version](#version)
* [Logs](#logs)
* [Configuration files](#configuration-files)
* [PHP-FPM](#php-fpm)
* [PHP extensions](#php-extensions)

## Access

PHP and PHP-fpm are parts of [nginx-php container](README.md).

## Version

The current version of PHP can be found on `[Instance] > Bundle > Backend` page.

## Logs

Logs can be found under `/var/log/php` or `/var/log/php7` depending on the version.

## Configuration files

Configuration files can be found under `/srv/conf/php`.

## PHP-FPM

Rebooting PHP-FPM:
```bash
s6-svc -h /var/run/s6/services/php-fpm/
```

## PHP extensions 

To learn installed PHP extensions connect to the [nginx-php container](README.md) by SSH and execute:
```bash
$ php -m
```