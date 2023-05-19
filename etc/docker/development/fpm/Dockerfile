FROM randock/docker-ubuntu-php:8.1-dev

COPY supervisord.conf /etc/supervisor/conf.d/supervisord.conf
COPY php-fpm8.1.conf /etc/php/8.1/fpm/php-fpm.conf

COPY config/xdebug.ini /etc/php/8.1/mods-available/xdebug.ini
COPY config/xdebug.ini /etc/php/8.1/cli/conf.d/20-xdebug.ini

ENTRYPOINT ["supervisord", "--nodaemon", "--configuration", "/etc/supervisor/conf.d/supervisord.conf"]
