# Original repo – Docker Compose LEMP Stack

This repository contains a little `docker-compose` configuration to start a `LEMP (Linux, Nginx, MariaDB, PHP)` stack.

Link to original repo –> 'https://github.com/stevenliebregt/docker-compose-lemp-stack'

## Details

This fork was adapted to host Wordpress files through LEMP stack. The following versions were used initially:

* PHP 7.2 (FPM) - With MySQLi driver optionally (Uncomment line from php.Dockerfile)
* Nginx 1.13.6
* MariaDB 10.3.9

## Configuration

The Nginx configuration can be found in `config/nginx/`.

You can also set the following environment variables, for example in the included `.env` file:

| Key | Description |
|-----|-------------|
|APP_NAME|The name used when creating a container.|
|MYSQL_ROOT_PASSWORD|The MySQL root password used when creating the container.|

## Usage

To use it, simply follow the following steps:

##### Clone this repository.

##### Download Wordpress archive and extract it to app/ directory

https://wordpress.org/latest.zip

##### Configure index.php, if needed

##### Start the server.

Start the server using the following command inside the directory you just cloned: `docker-compose up`.

## Entering the containers

You can use the following command to enter a container:

Where `{CONTAINER_NAME}` is one of:

`docker exec -ti {CONTAINER_NAME} /bin/bash`

* `{APP_NAME}-php`
* `{APP_NAME}-nginx`
* `{APP_NAME}-mariadb`
