Installing Redis

    sudo apt update
    sudo apt install redis-server
    sudo nano /etc/redis/redis.conf
    supervised systemd
    maxmemory 128M
    maxmemory-policy allkeys-lfu
    sudo systemctl restart redis.service
    sudo systemctl status redis
    redis-cli and ping

Installing PHP Redis

    git clone https://github.com/phpredis/phpredis.git
    sudo apt install php-dev
    cd phpredis
    phpize
    ./configure
    make
    sudo make install
    sudo echo "extension=redis.so" > /etc/php/7.x/apache2/conf.d/redis.ini create a redis.ini
    sudo service redis-server restart
    apache2ctl restart
