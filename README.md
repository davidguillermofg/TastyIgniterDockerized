# TastyIgniter Docker
[![Docker Pulls](https://img.shields.io/docker/pulls/thisisqasim/tastyigniter)](https://hub.docker.com/r/thisisqasim/tastyigniter/)
[![Docker Image Size (tag)](https://img.shields.io/docker/image-size/thisisqasim/tastyigniter/latest)](https://hub.docker.com/r/thisisqasim/tastyigniter/tags)

Run with docker compose for automatic database configuration

```
mkdir tastyigniter && cd tastyigniter
curl -LO https://github.com/davidguillermofg/TastyIgniterDockerized/raw/master/docker-compose.yml
docker compose up db -d
sleep 10
docker compose up -d
docker compose exec app php artisan igniter:passwd admin
```
Browse to port 80 of your docker host. The TastyIgniter setup wizard will show up. Wait for a minute for the database container to come up and then run the setup.

## Changes from the original

This is a customized fork of [ThisIsQasim/TastyIgniter](https://github.com/ThisIsQasim/TastyIgniter) with the following improvements:

- Upgraded TastyIgniter to version **3.7.7**
- Improved compatibility with **Docker Compose**

## Image on Docker Hub

You can use the image directly from Docker Hub:

```bash
docker pull davidguillermo/tastyigniter:3.7.7
docker compose exec app php artisan igniter:passwd admin
```

## Credits
ThisIsQasim: https://github.com/ThisIsQasim/TastyIgniter
TastyIgniter: https://github.com/tastyigniter/TastyIgniter
