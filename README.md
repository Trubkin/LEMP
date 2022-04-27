# Docker Compose LEMP Stack

This repository contains a little `docker-compose` configuration to start a `LEMP (Linux, Nginx, MariaDB, PHP)` stack.

## Details

The following versions are used.

* PHP 7.4 (FPM) - With MySQLi driver optionally (Uncomment line from php.Dockerfile)
* Nginx 1.21.6
* MySQL 5.7

## Configuration

The Nginx configuration can be found in `config/nginx/`.

You can also set the following environment variables, for example in the included `.env` file:

| Key | Description |
|-----|-------------|
|APP_NAME|The name used when creating a container.|
|MYSQL_ROOT_PASSWORD|The MySQL root password used when creating the container.|
|PATH_TO_APP|Path to application.|
|PATH_TO_DB|Path to DB.|

## Usage

To use it, simply follow the following steps:

##### Clone this repository.

Clone this repository with the following command: .

##### Start the server.

Start the server using the following command inside the directory you just cloned: `docker-compose up`.

## Entering the containers

You can use the following command to enter a container:

Where `{CONTAINER_NAME}` is one of:

`docker exec -ti {CONTAINER_NAME} /bin/bash`

* `{APP_NAME}-php`
* `{APP_NAME}-nginx`
* `{APP_NAME}-mariadb`
