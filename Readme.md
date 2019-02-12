# PHP Dockerfile for Tutorials Tank
[![Build Status](https://travis-ci.com/zawiszaty/tutorials_tank_php.svg?branch=master)](https://travis-ci.com/zawiszaty/tutorials_tank_php)

### How to use it with docker-compose
```bash
    image: zawiszaty/tutorials_tank_php:latest
    working_dir: /var/www/project
    volumes:
      - ./symfony:/var/www/project
```
### If you want to do any command, you must log in to the container and do command inside it
```bash
docker-compose exe php /bin/bash
```
### or without login in to container 
```bash
docker-compose exe php php bin/console {command}
```
