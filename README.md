# PHP on Docker
## Overview
- Docker(docker-compose)
  - Nginx
  - PHP-FPM
  - MySQL
## How to use
- create MySQL `.env` file
```bash
cd php-on-docker
cp docker/mysql/.env.develop docker/mysql/.env
```
- start Docker
```bash
docker-compose up -d
```
- connect to http://localhost:8080/